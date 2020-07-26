
# Philosophy

Matry is an attempt to "bridge the gap", so to speak, between designers and developers. Many such attempts currently exist, and more are being introduced with each passing day. However, we think our approach is unique. In the following document, we will outline that approach, and hopefully shed some light on the logic underpinning Matrys design decisions.

## The State of The Industry

Before delving into our solution, it would be helpful to first explore the current landscape with respect to this effort. Because while there are many contemporary discussions around this issue, nearly all of them suffer from a few problems.

The first problem is that the discussion is heavily focused on the web. Consequently most tooling dedicated to solving this problem focuses on CSS and Javascript, and even worse, usually only React (at the time of this writing). When other platforms are mentioned, they are typically iOS and Android. All three of these platforms are important, but they are not the only platforms in existence. Should designers be forced to change their tooling if they suddenly need to design for a TV or Windows application? We feel strongly that they shouldn't.

Another issue is the shallow thinking around the question of whether designers should learn to code. Most conversations and thoughts we've seen on this topic tend to fall into a categorical trap, which is the idea that designers are "creative" and developers are "technical". Usually these sentiments carry with them the implicit conclusion that since code is "technical" and not "creative", then designers should steer clear of it. On the opposing end of this line of thought exists an equally dubious claim - that the category itself has no merit and that perhaps it should be discarded entirely. Unfortunately, egos inevitably get involved and people are made to feel as if their profession is being diluted or devalued.

## The Matry Solution - An Introduction

At Matry, we believe that the difference between "design" and "code" is not a difference of competence, ability, intelligence, or level of technicality. We prefer to view the distinction simply as one of domain-level concerns. Designers are concerned with the interfacial behavior of a given application, whereas developers are concerned with the implementation of that behavior. Any tooling should track as closely as possible to that line of distinction, and should present to each team whatever tools they need to be as efficient and expressive as possible within their respective domain. The idea that "developers write code", and that designers do not, is a poorly construed conclusion that we should critically analyze.

Instead of asking the question "should designers code", we should ask "should designers implement?" Phrased in that manner, we believe the question is "typically no." There are mountains of extraneous detail involved in actually building a working digital product, and it varies wildly even between different applications of a single platform. It varies even more so between platforms, such that finding a software developer who can competently build products in more than one platform is relatively rare. Our answer is "typically no" because there do exist many designers who are able to write production-quality CSS, as well as UI code for native environments like iOS and Android. If a designer *happens* to feel comfortable doing so, then of course that's a good solution! However, we firmly believe that it should never become an industry-standard requirement.

Now that we have settled the matter of *implementation*, we can safely revisit the original question with a fresh set of eyes.

## Should designers write code?

Code can be thought of as a tool for indirect manipulation, whereas most design tools are oriented towards direct manipulation (using drawing tools against a digital "canvas"). While some things might be easier with direct manipulation, there are several benefits to indirect manipulation. Simply put - yes, designers should write code. Code is an extremely useful tool; it forces people to clarify their thinking as well as their intentions. Once a coding language is sufficiently grasped, it bestows upon its author extraordinary powers. You become vastly more efficient and expressive. There is a popular conception that writing code is more analytical and rigid, and thus less "creative". Nothing is further from the truth. Used correctly, code is a creativity *multiplier*.

If designers *should* write code, but also *should not* implement, then what sort of language might designers use? This is the question that we at Matry are attempting to answer.


