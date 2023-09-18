
# Design Inclusion

In the spring of 2022, I gave my first public talk about Matry.
The event was SoFlo DevCon, a conference for everything from design to engineering.
I began my talk with a question, asking "who in here is a designer - can I get a raise of hands?"
To my dismay, no one raised their hand.
A room full of developers, all hearing me talk about this crazy idea of a programming language...for designers.
After the talk I had a few questions, but not much general interest.

I anticipated this because I've experienced it several times now.
Developers just don't seem to be too interested in the idea.
Most of the excitement I receive is from the design side.
Now, I don't want to come off as _expecting_ excitement by any means.
But what's interesting is the delta between the two responses.

In fact, over the years I've noticed this trend where the design world is striving to work more closely with developers.
This is especially true in design tooling - Figma, Sketch, AdobeXD, Webflow, the list goes on.
Figma has especially been foward-leaning on this front, and have gone to great lengths to carve out a space in the design toolchain for developers.

Yet, while the design world is clearly aching for a more integrated workflow, the interest does not seem to be mutual.

When was the last time you saw a _developer tool_ carve out space for _designers_?
The only example I can think of is Storyboard, which is a GUI tool used by Apple's XCode for arranging the views of a Mac app (iOS, desktop, etc).
But the idea that a designer would actually use the tool is somewhat laughable - it seemed to be built more for visual programming than for design itself.

So why aren't developers interested in bridging the gap with designers?
After all, the workflow is typically one-way - designs are handed off to developers for implementation.
So developers are in a better position to understand what they need from designers, and could build tooling that makes that hand-off easier.

I'm not going to opine on the reasons why, because I honestly don't know.
But what I am confident in stating is that it should change.
We need more of what I would call "design inclusivity" - we should be inviting designers to take a more active role in the development of our products.

Obviously this is easier said than done, which is why I'm trying to create a technology that helps to bridge that gap.
The technology should be (a) open source, (b) tool agnostic, and therefore (c) focused on the "data" of design rather than any one representation of it.
An excellent step forward in this regard is the [Design Tokens Community Group](https://github.com/design-tokens), which is building a standardized schema for specifying design tokens.
Matry intends to build a language on top of this schema, further helping design and development teams collaborate more closely together.
