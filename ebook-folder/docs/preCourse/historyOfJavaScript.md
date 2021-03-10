# A VERY Brief History of JavaScript

Taken from [A Brief History of JavaScript](https://auth0.com/blog/a-brief-history-of-javascript/) written by [Sebastian Peyrott](https://twitter.com/speyrott?lang=en) at Auth0. Be sure to read the bullet points, they could help you in an interview someday...

1. **May-Dec 1995** Netscape Communicator and NCSA Mosaic were the first popular web browsers.
1. Netscape was founded by the same people that built Mosaic, but now had money and time to build it better. Marc Andreessen, founder of Netscape Communications wanted the web to become more dynamic. Animations, interaction and other forms of small automation should be part of the web of the future.
1. To do that they would need a **small scripting language** that could interact with the Document Object Model (DOM) (which was not set in stone as it is right now).
1. And it should be accessible to non-developers, better yet for designers the way HTML already was.
1. And so the idea of **Mocha** was born. Mocha was to become a scripting language for the web. Simple, dynamic, and accessible to non-developers.
1. **Brendan Eich**, father of JavaScript, was contracted by Netscape Communications to develop a "Scheme for the browser".
1. This Scheme was to be dynamic, powerful, and functional in nature, easy to grasp syntactically and to reduce verbosity and speed up development.
1. There was a lot of pressure to come up with a working prototype as soon as possible. The **Java** (not JS!) language was starting to get traction. **Sun Microsystems** was making a big push for it and Netscape Communications was about to close a deal with them to make Java available in the browser.
1. Enter a new language, Mocha. The idea at the time was that Java was not suited for the type of audience that would consume Mocha: Scripters, amateurs, designers. Java was just too big, too enterprisy (sic) for the role.
1. There was a lot of internal pressure to pick one language as soon as possible. **Python**, **Tcl** and **Scheme** itself were all possible candidates. So Eich had to work fast.
1. **May 1995** - Eich had the luxury to choose features but had little time to build the language. In a matter of weeks, a working prototype was integrated into Netscape Communicator in May 1995.
1. In the end, a Java-like syntax was required, and familiar semantics for many common idioms was also adopted. So Mocha was not like Scheme at all. It looked like a dynamic Java, but underneath it was a very different beast: a premature lovechild of **Scheme** and **Self**, with Java looks.
1. Mocha was renamed to **LiveScript**. And later when Sun and Netscape closed the deal it was renamed JavaScript, a scripting language for small client-side tasks.
1. Java would be promoted as a bigger, professional tool to develop rich web components.
1. This first version of JavaScript set in stone many of the traits the language is known for today. In particular, its **object-model**, and its **functional features** were already present in this first version.
1. **August 1996** - At the moment (and for a very long time), web standards were not strong. So Microsoft implemented its own version of JavaScript, called JScript. **JScript** was different in more than just name. Slight differences in implementation, in particular with regards to certain DOM functions, caused ripples that would still be felt many years into the future. JavaScript wars were fought in more fronts than just names and timelines and many of its quirks are just the wounds of these wars. The first version of JScript was included with Internet Explorer 3.0, released in August 1996.
1. In the fall of 1996, Eich rewrote most of Mocha into a cleaner implementation to pay off for the technical debt caused by rushing it out of the door. This new version of Netscape's JavaScript engine was called **SpiderMonkey**. SpiderMonkey is still the name of the JavaScript engine found in Firefox, Netscape Navigator's grandson.

For the full article, that link again is [A Brief History of JavaScript](https://auth0.com/blog/a-brief-history-of-javascript/).