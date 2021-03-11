bring in the lessons:

Low Level Concepts
https://studio.zollege.com/container/block-v1:ACA+JS211+JS211_PT_MASTER+type@vertical+block@60f749e683ee418c963b9cf0f0c8a9b7

Read It - How a Computer Works Under-the-Hood
As a fledgling programmer, one of your prime directives is learning to think like a computer, or, more specifically, learning to understand what your computer expects.

A fundamental feature of any modern programming language is the ability to represent values. There are two fundamental ways to create values—statements and expressions.

Before diving in, let's start by taking a step back and looking at the big picture. Though it may not be immediately apparent, I promise this brief detour will become relevant in the end, when we start talking expressions and statements.

Everything a computer does, it does because of software.
Software consists of programs (otherwise known as applications).
In order for a program to do anything at all, that program must provide values for the computer to manipulate, and tell it how to manipulate them.
Programming then amounts to nothing more than writing instructions for a computer to follow.

These instructions primarily consist of:

values - corresponding to words, numbers, URLs, files on your hard drive, ASCII codes for rendering text, etc
and

operations - actions to be performed on those values.
Early computers did this in a very rudimentary way, and as such were mostly reserved for performing complex mathematical operations.

Fortunately, computers evolved into sophisticated machines and we no longer find ourselves restricted to using convoluted machine-level operations to write our programs.

Nevertheless, the fundamental concepts are still very much the same. We give values to the computer and instruct it to perform actions upon them.

Underneath the surface of your operating system's sleek, user-friendly UI, there are programs running all the time, each responsible for (hopefully) keeping your computer functioning properly.

Let's peer under the hood and see if we can't glimpse what I'm talking about:

MacOS/Linux, open your terminal and type top.
Windows users can open Task Manager and switch to the Processes tab.
What you're looking at is a list of all the little programs that keep your computer running smoothly. On the surface, it may appear that you're only using a handful of applications—glancing at your task bar, it seems that you're just running a web browser, an email client, Spotify, etc...

In fact, all these graphical applications idling in userspace, not to mention your Operating System itself, are underpinned by a large assortment of little processes and programs. And beyond that, there's yet another layer of housekeeping workers. These little "worker bees" are a set of low-level instructions for shifting bits around: how much memory to allocate for this, where to allocate memory for that.

If this wasn't a bit of an 'a-ha moment' in thinking about your programs: all the magic of computers—that is, all programs and applications—can be ultimately reduced to the creation and manipulation of values.

In JavaScript, a value is represented in one of two fundamental ways: a statement, or an expression.

The key distinction between the two is how you will arrive at that value.

## STATEMENTS

When we declare a statement we're making a self-evident claim about a value, with the intent of later performing some kind of action upon it.

Open your console in the Chrome DevTools (CMD + SHIFT + c), declare a variable like the one below, and watch what happens:

```javascript
  const a = 1;
  // > undefined
```

" Why undefined? I mean, we just defined a variable, didn't we? "
It's true—we have declared a variable a and asked that it represent the value 1. But we really didn't ask the computer to do anything beyond that.

"The thing I really enjoy about programming is just the fact that you really can tell the computer exactly what to do, and it will do what you tell it, and nothing more."
—Linus Torvalds

The R.E.P.L. (as in Repl.it ) merely Reads your input, Evaluates it, Prints any returned value, and then Loops back around, resetting your prompt. In this case, when it arrived at the third step, the REPL had to print something, but it didn't have any return value, so it just spit out the default: undefined.

If we want to see the value of a, we have to explicitly ask for it—or rather, call it.

If you imagine that you and your browser are having a conversation in JavaScript, declaring the statement const a = 1; is like you saying,

"Let's set a variable called a to a value of the integer 1."
Your browser hears you, nods, makes a mental note of it, but doesn't say anything back.

But when you call the variable with a, it's as if you're asking a question:

"Can you give me that a thing I mentioned earlier?"
Your browser thinks to itself, trying to remember if you ever told it to do anything with a variable called a.

"Oh yeah, a. I remember you wanted a variable called a. Hang on while I see if we ever attached it to a value."
Now the browser iterates once more, this time trying to remember if it ever set a to a value.

"Ah, here it is. a is bound to 1"

```terminal
> const a = 1;
undefined
> a;
1
```

## Expressions

When we call a; we are in fact writing our first expression:

"Expressions are a combination of one or more explicit values, constants, variables, operators, and functions that the programming language interprets...and computes to produce ("to return", in a stateful environment) another value. (from Wikipedia)"
When you call a with the expression "a", the browser interprets that expression—sees that you are asking for the variable a—then computes (it goes and looks for a value associated with a variable called a).

Reload your browser to refresh the console. Now try calling a without defining it:

```terminal
  > a;
  Uncaught ReferenceError: a is not defined
  >
```

Notice we didn't simply get undefined as before. Why?

Let's go one step further before getting into it. Define a variable a, but don't set it to anything:

```terminal
> a;
Uncaught ReferenceError: a is not defined
> let a;
undefined
> a;
undefined
>
```

On our first attempt to call a, the JS REPL Reads the input and Evaluates it, but it doesn't find any mention of a, because a hasn't been set to any value.

When you call a variable that hasn't been set, the JavaScript engine is programmed to throw a ReferenceError. That's JavaScript's way of letting you know that a isn't set to anything.

When you call a—regardless of whether or not you've defined it—you are writing an expression. Or, if you like, the act of calling a is an expression. And expressions, as we've seen, are interpreted and computed to produce value.

That's why we can declare a in a statement without setting it to anything, call it with the expression a, and get a value back: undefined.

Going back to our JavaScript conversation, it's as if we're just saying out loud,

"Let's create a variable called a."
JavaScript nods in acknowledgement. Then we ask,

"Can you give me the value of a?"
JavaScript thinks back for a moment and says,

"I know you asked for a variable called a, but you didn't give it any value, so I just set it to undefined."
After all, [undefined is a value too](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined). The authors of JavaScript created undefined to make grown men cry to represent the value of variables that have been named, but not set. Without it, we'd have a much harder time debugging our applications.

## Tie it All Together

Statements are the "definitions" we write for values we'd like JavaScript to retrieve at some point, or, in the case of an if statement, where we specify how we'd like a value to be returned. Expressions are what we use to ask for those values, or even to just ask for values on the spot, without attaching them to a variable at all.

```terminal
> 1 + 2;
3
>
Remember, the above expression is distinctly different from this statement:

> const three = 1 + 2;
undefined
>
To get that value back, we have to ask for it:

> const three = 1 + 2;
undefined
> three;
3
>
Expressions, then, can be thought of as any block of code where you're asking the computer to perform some kind of "work". That is, work that isn't just the typical "housekeeping" of storing variables in memory, remembering function declarations, etc.

In fact, by that definition, the above example actually represents an expression inside a statement!

( const three = ) (    1 + 2     )
  ^ statement ^    ^ expression ^
```

As you glanced at the example, you saw the + operator and summed 1 and 2 in your head so quickly you didn't even realize it. Although it required very little effort to do so, you still asked your brain to perform work to arrive at the result.

The JavaScript interpreter is functioning in much the same way. It recognizes the + plus sign as an indication that an addition operation needs to take place, and it performs the work necessary—it evaluates.

In short, 1 + 2 is just another way of saying—or rather, expressing—3. One that requires a bit more work than just saying 3, but analogous nonetheless.

The takeaway here is recognizing where we asked the computer to do work, with an expression:

1 + 2

...and where we told it how to perform that work, using a statement:

"Bind it to a constant variable called three".

## Wrapping Up

At a glance these concepts can seem daunting, overly complicated, and hard to understand. The only reason you may feel this way is because you haven't been required to think this way before and now you are. It's okay, trust the process by writing notes, drawing pictures, connecting dots, and understand that at one point you didn't know how to drive, ride a bike, or read. You don't know how to code right now but you soon will!

