PASSWORD GENERATOR
==================
By Al Takura Mujati


DAD JOKE
--------
Why did the password get rejected?
It wasn't strong enough to handle the relationship.


WHAT IT IS
----------
A tool that generates secure, random passwords directly in your browser.
You control the length and which character types to include.
Nothing is sent to a server. Everything runs locally on your machine.


HOW IT WORKS
------------
There is no backend. This is a pure frontend project.

When you adjust the settings and click Generate, the browser runs a
JavaScript function that builds a pool of characters based on your
chosen options (uppercase, lowercase, numbers, symbols).

It then uses the Web Cryptography API, specifically:

    crypto.getRandomValues()

This is a built-in browser function that generates cryptographically
secure random numbers. It is the same standard used in encryption
and security software. It is much stronger than Math.random(), which
is not suitable for passwords because it is predictable.

The random numbers are mapped to characters in the pool to produce
the final password string.


STRENGTH METER
--------------
The strength is calculated using entropy, which is a measure of
how unpredictable the password is.

The formula is:

    entropy = length x log2(pool size)

A larger character pool (more character types enabled) and a longer
password both increase entropy. Higher entropy means more possible
combinations, which means harder to crack.

The crack time estimate is a rough category based on entropy bits:

    Under 28 bits   = Instant
    28 to 40 bits   = Minutes
    40 to 56 bits   = Days
    56 to 72 bits   = Years
    Over 72 bits    = Centuries


TECH USED
---------
HTML, CSS, JavaScript
Web Cryptography API (crypto.getRandomValues)
No libraries, no frameworks, no backend


HOW TO RUN IT
-------------
Just open the HTML file in any browser. That is it.
No install, no server, no dependencies.


WHY IT IS ON MY PORTFOLIO
--------------------------
It demonstrates an understanding of cryptographic randomness and
why it matters for security. It also ties into my Honours studies
in Security and Network Engineering at Eduvos.
