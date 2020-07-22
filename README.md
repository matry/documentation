
# Documentation

The Matry programming language is the first domain-specific language created explicitly for user interface designers.

Matry is clean, efficient, and expressive.
Its syntax conforms to designers mental models, allowing them to express their ideas with clarity and ease.
It is also platform-agnostic, hiding unnecessary implementation details that are best left to developers.

## Design Principles

The ultimate goal for Matry is to enhance design tooling such that it is on par with developer tooling.
In order to achieve this goal, the language needs to offer the following features:

1. **Component-oriented**  
Instead of designing for pages or views, design tooling needs to be oriented towards components.
This approach encourages designers to use systems-level thinking.

2. **Parametric**  
Any one value within a design can be calculated or inferred from any other design value.
This gives designers the ability to fully express their intentions.

3. **Semantic**  
The words and syntax used by the language should mirror verbal language as closely as possible, to facilitate conversations between designers and developers.

4. **Generative**  
The language should strip away as much manual work as is feasible, allowing designers to focus on designing, rather than laborious grunt work.

---

## A Quick Tour

All Matry projects are split into three modules - Tokens, Components, and Stories.

### Tokens

*Tokens* are placeholders for indivisible design attributes.
They sit outside of any single component in a Matry project, and are selectively used by components to inform their internal design logic.
Below is a small sample of a few tokens:

```
tokens Branding
  primary-blue color: #007BFF
  secondary-blue color: #000080
  light-logo image: /assets/white-logo.svg
  dark-logo image: /assets/dark-logo.svg
```

### Components

All designs created within Matry are based on *Components*.
A Component in Matry is technically defined as "an instance of encapsulated visual state".
More plainly, a Component is simply a slice of UI that can be considered and designed for independently.
Below is a simple example of a Component titled "Block".

```
component Block

elements
  Container shape

style Container
  width: 100
  height: 100
  fill: red
```

### Stories

*Stories* are repeated instances of Components with varying parameters.
Each instance is called a "frame", and a Story can be thought of as a slideshow of a set of frames.
They can be used by designers for a variety of purposes, but most purposes are centered around presentation.
Common usages might be
(1) demonstrating all the possible visual states for a given component, 
(2) presenting a particular user flow to stakeholders, or 
(3) visualizing an animation sequence for developers.

Below is a sample of a simple Story:

```
story LoginFlow

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
```
