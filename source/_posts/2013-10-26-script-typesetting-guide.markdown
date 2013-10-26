---
layout: post
title: "Script Typesetting Guide"
date: 2013-10-26 03:01
comments: false
categories: ["Guides", "Writing"]
---

We are using **Markdown** for the overall script, and $LaTeX$ for typesetting equations, chemicals and those technical shebang.

What for? Well,

- We won't be dependent on a certain system (be it Microsoft Word, Google Docs, Pages etc). They all have different formats, and conversion is painful as hell.
- This means that you can **write on anything**. Be it Notepad, TextEdit, Sublime, EMacs or your favorite word processor, they're all the same to us since all we care about is the word, not formatting
- This also helps you to **focus**, since you only need to be concerned with the *text*, and not the *formatting*

But what does this trouble translate into?

- Render the script into **transcripts** for filming easily
- **Displaying** the scripts online
- Process these scripts into **notes** beautifully
- **Archive** the scripts conveniently

With that, let's begin!

## Editor Choice

Markdown and $LaTeX$ can be written anywhere. So long as you have any basic text editor, it should work. We recommend Sublime Text.

However, you'd only see the "source code" of the file. You won't see the finished product. If you're the kind that likes to see that side by side, then here's what you do.

1. Go to Google Drive
2. Click on "Create" as if you were going to create a new document
3. If you see a button titled "Stackedit", click on it. If you don't, here's how you get it.
	- Click on "Connect more apps"
	- Search for "Stackedit"
	- Click on "Connect"
	- Check "Make StackEdit the default app for files it can open"
	- Click on "OK"
	- Now go back and click on "Create" again. You should see "Stackedit"
4. This is basically a side by side editing tool that allows you to see the code you type on the left, and the finished product on the right.

Cool right?

## Format

### Sample Script

This is a redacted version of a chemistry script.

```
---
subject: Chemistry
topic: Atoms and Molecules
lesson: Moles, Mass, and Number of Particles
---

## Moles and Avogadro’s Number

<1> Whenever you get some eggs from the supermarket, you usually get half a dozen, a dozen, or if you’re really hungry, two dozen instead of asking for 4 eggs or 3 eggs or 9 eggs. A dozen eggs is 12 eggs, and we use this special unit out of habit.

In chemistry, we use another special unit to describe how many atoms of an element that we have. It is called a <2> mole, which represents <3> $6.022 \times 10^{23}$ atoms. A mole of hydrogen for example, contains 6.022 times ten raised to the 23 hydrogen atoms. <4> $6.022 \times 10^{23}$ is known as Avogadro’s number. Moles and the number of particles in a mole are important when it comes to controlling reactions. If I had to react sodium and water to make an explosion, I would control <5> how big the explosion would be by controlling the moles of sodium, aka the number of sodium atoms, to add to the water. 

## Molecular Weight aka Molar Mass

<1> Let’s say you have a donut made of two things: <2> cream and flour. We can find the donut mass by adding the mass of the flour in the donut to the mass of of the cream on the donut. Let’s say the flour has a mass of 20 g and creme has a mass of 10 g. Then, one donut has a mass of 30 g. 

In a similar way, we can find the mass of molecules. Let’s look at the water molecule. <3> We know that it is composed of two hydrogen atoms and a single oxygen atom, or $\ce{H2O}$. To find the molecular weight of water, we take the atomic mass of each element making up the molecule, and add them all together.
```

### Header

First, you'll see the Subject, Topic, and Lesson of the checkpoint at the top sandwiched by dashed lines `---`.

```
---
subject: Chemistry
topic: Atoms and Molecules
lesson: Moles, Mass, and Number of Particles
---
```

This is really self explanatory. Just type it in as it is. 

### Checkpoint Title

Each checkpoint title should have **two hashes** in front like this `## Checkpoint Title` followed by a **line break**. This tells Markdown that this should be a Heading.

Hence, for the checkpoint titled **Moles and Avogadro's Number**, it begins with this line.

```
### Moles and Avogadro’s Number

```

### Checkpoint Content

Then comes the content of the checkpoint. Just type them in, with a double paragraph break separating paragraphs.

So this is **good**.

```
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.

Quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor.
```

This is **bad** and a whole lot harder to read.

```
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.
Quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor.
```

Save your eyes.

### Slide Markers

You'll find stuff like this `<1>` and `<2>` in the scripts. Fret not. They are simply markers for the slide maker. In other words, after you write a script, you'll be drawing the animations on a storyboard. These tell the slide maker to match the slide numbers drawn with the script position. This helps the animators to time the slides.

If you see them added already, simply ignore them.

**With this, you should be able to draft a set of slides on English Literature**.

However, we are working with subjects like Mathematics and Chemistry. They require strange notation like $\frac{3}{4}$ that you don't want to just leave as 3/4. Why not? Ugly. And ugly stuff belong in hell, not in our documents.

Enter $LaTeX$ (pronounced Laa-Tech)

## Cross Subject

### Basics

There are two types of equations you are going to write. Stuff that appears within a paragraph like $3x = 9 + 7y$ here. These are called **inline equations**, since they appear *in the line* with the paragraph text.

To do that, simply insert the equation between two dollar signs. Like so `$3x = 9 + 7y$`. This will give the exact same thing as above. Make sure that there are no spaces to the right of the first `$`, or to the left of the second `$`. So `$ 3x = 9 + 7y $` won't work. When it's being rendered, Markdown will throw you all sorts of errors.

There's another type here. We want to prove that no three positive integers $a$, $b$, and $c$ ($a$, $b$, and $c$, were typed using **inline equations** by the way) can satisfy this equation 

$$a^n + b^n = c^n$$

for any integer value of $n>2$.

Now this equation appears right smack in the middle right? That's what we call **display** equations. They're typed using two `$`s instead of one. So, to produce that, I simply typed `$$a^n + b^n = c^n$$`

So to type that entire paragraph, I will type

```
There's another type here. We want to prove that no three positive integers $a$, $b$, and $c$ ($a$, $b$, and $c$, were typed using **inline equations** by the way) can satisfy this equation 

$$a^n + b^n = c^n$$

for any integer value of $n>2$.
```

Cool right?

## Mathematics

Feel free to replace the **inline** with **display** notation. 

- Superscript and subscript are done using `^` and `_` characters. Note that if you want multiple characters in the super/subscript then you need to surround them with curly braces: `$e^i\pi = -1$` gives $e^i\pi = -1$ whereas `$e^{i\pi} = -1$` gives $e^{i\pi} = -1$.
- Fractions are done using `$\frac{1}{2}$` which gives $\frac{1}{2}$.
- To do a binomial coefficient, use `$\binom{n}{k}$` which gives $\binom{n}{k}$.
- $\forall$ and $\exists$ are written as `$\forall$` and `$\exists$`.
- $\neq$, $\geq$, and $\leq$ are `$\neq$`, `$\geq$`, and `$\leq$`.
- $\cdot$ (e.g. for multiplication) is `$\cdot$`.
- $\circ$ is `$\circ$`.
- $\cup$ and $\cap$ are `$\cup$` and `$\cap$`.
- $\oplus$ is written with `$\oplus$`.
- Large $\cup$, $\cap$, $\oplus$ signs that behave like summations (see below for summations) are written as `$\bigcup$`, `$\bigcap$`, `$\bigoplus$`.
- $\{\}$ are done with `\{` and `\}`.
- $\approx$ is produced with `$\approx$`.
- $\hat{x}$ and $\bar{x}$ are done with `\hat{x}` and `\bar{x}`. A longer bar may be written using `\overline{abcd}`, which produces $\overline{defg}$.
- Greek characters are simply what they are. For example, capital Delta $\Delta$ is simply `$\Delta$` while lower case delta $\delta$ is simply `$\delta$`.
- The probability sign is defined as `$\Pr$`, i.e. $\Pr$.
- To draw parentheses that grow to match the contents, use `$\left$` to precede the left parenthesis and `$\right$` to precede the right:\
Source:
```
$$\Pr\left[\sum_{i=1}^k X_i > c \right] \leq 2^{-\Omega(c^2 k)}$$
```
Output: 

$$\Pr\left[\sum_{i=1}^k X_i > c \right] \leq 2^{-\Omega(c^2 k)}$$

- Summations and products are done using `$\sum$` and `$\prod$` respectively. Parameters can be given for the summation/product as well:
Source:
``` 
$$\sum_{i=1}^\infty \frac{1}{2^i} = 1$$
```

Output:

$$\sum_{i=1}^\infty \frac{1}{2^i} = 1$$

## Chemistry

- Chemical equations can be done using the command `$\ce{whatever chemical}$`. For example, to show the chemical $\ce{NaCl}$, just type `$\ce{NaCl}$`.
	- In short, $\ce{NaCl}$ can be typed using `$\ce{NaCl}$`
	- Ions like $\ce{Na^+}$ or $\ce{Cl^-}$ can be typed with a simple **superscript** like `$\ce{Na^+}$` or `$\ce{Cl^-}$`
	- Reaction equations can be typed by literally drawing out the right arrow `->`. Hence $\ce{Ag^+ + Cl^- -> AgCl}$ can be typeset using `$\ce{Ag^+ + Cl^- -> AgCl}$`
	- State symbols can be typed using `(s)` or `(aq)`. So $\ce{Ag^+(aq) + Cl^-(aq) -> AgCl (s)}$ is typed using `$\ce{Ag^+(aq) + Cl^-(aq) -> AgCl (s)}$`
	- Reversible reactions like $\ce{2NaCl + CaCO3 <=> Na2CO3 + CaCl2}$ is produced from `$\ce{2NaCl + CaCO3 <=> Na2CO3 + CaCl2}$`
	- If you're the fancy type that likes to add little things on top of reaction arrows like this $\ce{->C[I-]}$ then do it like this `$\ce{->C[I-]}$`. This works too $\ce{<=>C[+e]}$ from `$\ce{<=>C[+e]}$`
- Typing units can be a pain in the ass. I mean who wants to type $ms^{-1}$ all the time like `$ms^{-1}$`. Don't you wish you could just type **SI Units**? Besides, the *italics* makes it kind of ugly. Fortunately, there's a way.
	- $5 \si{\metre\per\second}$ can be typeset using  `$5 \si{\metre\per\second}$`
	- The rest of the SI units work as well. Experiment, or look up the guide here <http://mirror.utexas.edu/ctan/macros/latex/contrib/siunitx/siunitx.pdf>

## Final Tips

- Do not leave any equations in plain text. That is plain ugly.
- If the Stackedit preview fails to render, or produces weird shit, you're probably making a mistake somewhere (most likely a missing or additional `$` sign).
- Once you get used to this, you'll never go back.