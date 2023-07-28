
# Documentation

The Matry programming language is the first domain-specific language created explicitly for user interface designers.

Matry's syntax has been carefully crafted to avoid conventions from the programming world, and to use common verbiage and mental models from the design industry.
This allows designers to express their ideas with clarity and ease.
It is also platform-agnostic, hiding unnecessary implementation details that are best left to developers.

---

## Design Principles

The ultimate goal for Matry is to enhance design tooling such that it is on par with developer tooling.
In order to achieve this goal, a design tool needs to have the following qualities:

1. **Portable**  
Whatever tool is used to create a design, the "data" of the design must not be _owned_ by the tool, and should instead entirely be owned by the designer.

2. **Expressive**  
Design tooling should allow significant depth of expression, such that complex application interfaces can be described.
At some point, all visual tools lose their ability to express behavior beyond a certain depth.
One of Matry's core propositions is that formal language will always be better in these scenarios.

2. **Component-oriented**  
Instead of designing for pages or views, design tooling needs to be oriented towards components.
This approach encourages designers to use systems-level thinking.

3. **Parametric**  
Any one value within a design can be calculated or inferred from any other design value.
This gives designers the ability to fully express their intentions.

4. **Semantic**  
The words and syntax used by the language should mirror verbal language as closely as possible, to facilitate conversations between designers and developers.

---

## A Quick Tour

All Matry projects are split into three modules - tokens, components, and stories.

Note: _apologies for the lack of syntax highlighting, Matry is obviously not yet recognized by Github :p_

### Tokens

*Tokens* are placeholders for indivisible design attributes.
They sit outside of any single component in a Matry project, and are selectively used by components to inform their internal design logic.
Below is a small sample of a few tokens:

```
tokens branding
  primary-blue color: #007BFF
  secondary-blue color: #000080
  light-logo image: /assets/white-logo.svg
  dark-logo image: /assets/dark-logo.svg
```

To use a token from above:

```
background-color: $branding.primary-blue
background-image: $branding.dark-logo
```

### Components

All designs created within Matry are based on *components*.
A component in Matry is technically defined as "a repeatable instance of encapsulated visual state".
More plainly, a component is simply a slice of UI that can be considered and designed for independently.
Below is a simple example of a component titled "RedSquare".

```
component RedSquare {
  elements
    shape square

  style square
    width: 100px
    height: 100px
    fill: red
}
```

As can probably be inferred from the above code sample, components are comprised of (1) elements and (2) styles.
In this case the component has a single element - a generic shape named "square".
At first glance this probably looks like CSS, and in fact much of it is inspired by it of course.

However, a massive difference here is that style values cannot be overridden.
Thus, in Matry there is no cascade.

Instead, a component in Matry must explicitly define all visual states for the component directly within the component definition.
In order to accomplish this, we have an additional concept called a "variant":

```
component RedSquare {
  variants
    switch size: small, medium*, large

  elements
    shape square

  style square
    fill: red

  style square when $size
    is small:
      width: 50px
      height: 50px
    is medium:
      width: 100px
      height: 100px
    is large:
      width: 200px
      height: 200px
}
```

In order to render the `RedSquare` component in a particular visual state, the syntax would look like this:

```
RedSquare
  size: small
```

### Stories

*Stories* are repeated instances of components with varying parameters.
Each instance is called a "frame", and a story can be thought of as a slideshow of a set of frames.
They can be used by designers for a variety of purposes, but most purposes are centered around presentation.
Common usages might be
(1) demonstrating all the possible visual states for a given component, 
(2) presenting a particular user flow to stakeholders, or 
(3) visualizing an animation sequence for developers.

Below is a sample of a simple story, demonstrating the happy path for a login form:

```
story LoginFlow {
  frame NoUsernameOrPassword
    LoginForm
  
  frame HasUsername
    LoginForm
      username: Jane Doe
  
  frame HasUsernameAndPassword
    LoginForm
      username: Jane Doe
      password: 123456789
  
  frame LoginIsComplete
    LoginForm
      username: Jane Doe
      password: 123456789
      complete: true
}
```
