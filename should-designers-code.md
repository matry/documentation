
# Should Designers Code?

This horse has been beaten to death many times over, but it needs revisiting in the context of Matry.
If you're a designer who doesn't want to code, I'm going to try to convince you to reconsider.
Hopefully, by the end of this article, you'll agree with me.

## What is code?

The question itself is too vague - what do we mean by "code"?
The truth is that when we talk about code, we're actually talking about two _very_ different things.

In one sense, code is simply text that both humans and computers understand.
This is so broad that it even includes keyboard shortcuts.
Most designers know that `cmd+c` means "copy the current user selection."
Imagine asking "should designers use keyboard shortcuts?"

It doesn't make as much sense, does it?

Now consider the _other_ use of the word "code", which effectively means "implementing the functional behavior of a computer".
If that definition sounds unclear, let's use my favorite example to demonstrate this concept - a calculator.

In a calculator you typically have a set of numeric buttons 0-9, some operative buttons like plus and minus, a submit button, and a window displaying the result of the calculation.
All of these elements have various visual states - for instance, the buttons may have a hover or active state that triggers when the user presses on them.
These behaviors are primarily visual, interface-level behaviors.
On the other hand, there are the calculations themselves; i.e. "2 + 2 should give you 4".
Let's call these functional behaviors.
When developers write code, they are _usually_ (but not always) writing instructions for the computer to perform functional behaviors.

With that in mind, let's rephrase the original question "should designers code" to something more meaningful - "should designers implement functional behavior?"
To this more specific question, I believe the correct answer is overwhelmingly _no_.
That's not to say that a designer couldn't do so, but if they do, they are acting outside of the _scope of design_.

## So wait, designers shouldn't code?

Correct, though to be more specific, designers _shouldn't implement functional behavior_.
In other words, as a designer you shouldn't be responsible for making sure that "2 + 2 = 4".
But remember that code has two definitions, the first simply being "text that both humans and computers understand".

So, should designers do this? I think the answer is "maybe!"

In certain cases, writing text is _vastly_ more efficient and easy than using an interface.
This comes as a surprise to many people, but is common knowledge among developers.
If designers had a tool that allowed them to write out their ideas, I believe many of them would quickly see the benefits.

This doesn't mean it would be for everyone, of course.
There are certainly many developers who've become so entrenched in their toolset that they couldn't imagine anything else, and that's perfectly fine!
But you may be surprised at just how efficient you could be.

## But isn't code really complex?

This may be surprising to hear, but actually no!
It's not complex, or at least...it's not _inherently_ complex.
The truth is that code is only as complex as the problem it's trying to solve.

If you were writing code that powers a SpaceX rocket, then even my 14 years of experience probably wouldn't prepare me to understand it.
But consider this example:

```
begin dishwashing:
  gather(plates)
  sink.load(plates)
  each plate(rinse)
  each plate(dishwasher.load)
  dishwasher.on()
end dishwashing
```

Now, for those unfamiliar with programming conventions, you may need to think a bit about this before you understand it.
But if I were a gambler, I'd bet that virtually everyone can understand what this code is meant to do, regardless of your level of technical knowledge.
That's because we all understand the _problem_, even if we don't fully understand the syntax of the language.

Now imagine a language that is built to solve the problems you're used to solving as a designer.
This would be a language that uses the same terminology, verbiage, and mental models that you use every day.

That's Matry.

### End

To summarize, designers may actually want to write code, as long as they aren't responsible for implementing functional behavior.
But in order to make this a reality, you need a language that is custom-tailored to solve the problems that designers aim to solve.
Matry is an attempt to create that language.

If you're a designer who is skeptical of the idea that "designers should code", I hope I've been able to convince you to at least give it a shot. You may be surprised at how delightful it can be.
