
# What makes you like a programming language ?

Note:
Okay to interrupt
What do you look for when choosing a programming tool ? 
What makes you "like" a programming language ?
Discuss


---

# The most *loved* language of 2016

Note: 
What makes the language *loved* ?
The "ecosystem" => community much more than the language itself
Trust in the tools, people, to get the job done 
Stackoverflow survey 2016

---

# Rust has been built community-first 

Note: 
Rust founders were acutely aware of this, and added community tools early
* github - development in the open, listening to feedback
* rfc process, on github as well
* forums, irc
* "Only work with languages starting with `Ru`" - Steve Klabnik

---

# Package manager

Note:
A small but important step towards sanity
Made by experience package manager makers

---

# Release train + stability


Note:
It is very often. It is very stable as well.
crater, big query

"
We will use a variation of the train model, first introduced in web browsers and now widely used to provide stability without stagnation:
New work lands directly in the master branch.
Each day, the last successful build from master becomes the new nightly release.
Every six weeks, a beta branch is created from the current state of master, and the previous beta is promoted to be the new stable release.
In short, there are three release channels – nightly, beta, and stable – with regular, frequent promotions from one channel to the next.
"

---

# Editors/IDEs

Note:
* VSCode
* IntelliJ
* Vim
* others
* linters
* formatters
* unit testing + integration testing

---

# Usage in the wild

Note:
* VLC
* Dropbox
* Sentry / tilde
* Firefox
* FFI for critical (perf, security) parts a huge use case
* general purpose tech stack coming up quickly though
* growing community of existing legacy projects
"For a long while now I’ve been worried that the GNOME project would struggle to grow its contribution and stay attractive if it stuck to C in the long run (i.e. next 10-20 years)." - Alberto Ruiz

---

# Rust - the language

* no exceptions
* no gc
* no inheritance
* no segfaults
* no data races
* no null

Note:
we haven't touched the language itself yet
I think this is a modern language.
Multiparadigm, functional, procedural

---

# Fast, safe, concurrent.  
# Pick three.

Note:
same-process multithreaded shared-state is safe !

---

# Everything is almost the same

Note:
you have package manager, tools support
everything seems normal
then suddenly

---

# Except for ownership

```
fn take(v: Vec<i32>) {
    // what happens here isn’t important.
}

fn main() {
    let v = vec![1, 2, 3];

    take(v);

    println!("v[0] is: {}", v[0]);
}
```
Note:
what's wrong with the code on the screen ?
it does not compile !
too big of a topic to explain in 5 minutes but it will blow your mind
https://play.rust-lang.org/?gist=ef8d8f5bac2383e5e3bd0aaa4c593650&version=stable&backtrace=0

---

# Need for Rust consulting on the rise

Note:

Friends of Rust
Rust commercial user survey - https://internals.rust-lang.org/t/2016-rust-commercial-user-survey-results/4317
Rust Survey - https://blog.rust-lang.org/2016/06/30/State-of-Rust-Survey-2016.html

* Consulting needs

"
I'm a bit confused here. On the other hand, we have an ample amount of experienced Rust people that would love to do Rust jobs/trainings, and don't find any opportunites. But they are mainly freelance or running their business. [1][2]

It seems to me that these companies want to only work with their inside teams because someone came up with the idea to use Rust. It seems odd that the consulting market doesn't happen, though, even if it would make sense to hire externals for a PoC for example. It's not an unusual pattern though, my usual bread-and-butter software (Elasticsearch) is only now developing a freelance/consulting market.

Would anyone know ways to kickstart that?
"

---

# Learning materials

* rustlings
* into_rust
* the book v1 and v2
* rust by example
* this week in rust
* conference videos

---

# Questions ?



