
# You move a value to a new owner by default

Note:
This is different !
https://play.rust-lang.org/?code=fn%20main()%20%7B%0A%20%20%20%20fn%20take(v%3A%20Vec%3Ci32%3E)%20%7B%0A%20%20%20%20%2F%2F%20what%20happens%20here%20isn%E2%80%99t%20important.%0A%7D%0A%0Alet%20v%20%3D%20vec!%5B1%2C%202%2C%203%5D%3B%0A%0Atake(v)%3B%0A%0Aprintln!(%22v%5B0%5D%20is%3A%20%7B%7D%22%2C%20v%5B0%5D)%3B%0A%7D

Vec has a 'pointer' on the stack to stuff on the heap
Rust disallows having two pointers to the same stuff at the same time

https://doc.rust-lang.org/stable/book/ownership.html

---

# But there are `Copy` types

Note:
https://play.rust-lang.org/?code=fn%20main()%20%7B%0A%20%20%20%20let%20a%20%3D%205%3B%0A%0A%20%20%20%20let%20_y%20%3D%20double(a)%3B%0A%20%20%20%20println!(%22%7B%7D%22%2C%20a)%3B%0A%7D%0A%0Afn%20double(x%3A%20i32)%20-%3E%20i32%20%7B%0A%20%20%20%20x%20*%202%0A%7D%0A

---

# And Borrowing

Note:
https://play.rust-lang.org/?code=fn%20main()%20%7B%0A%20%20%20%20%2F%2F%20Don%27t%20worry%20if%20you%20don%27t%20understand%20how%20%60fold%60%20works%2C%20the%20point%20here%20is%20that%20an%20immutable%20reference%20is%20borrowed.%0A%20%20%20%20fn%20sum_vec(v%3A%20%26Vec%3Ci32%3E)%20-%3E%20i32%20%7B%0A%20%20%20%20%20%20%20%20return%20v.iter().fold(0%2C%20%7Ca%2C%20%26b%7C%20a%20%2B%20b)%3B%0A%20%20%20%20%7D%0A%20%20%20%20%2F%2F%20Borrow%20two%20vectors%20and%20sum%20them.%0A%20%20%20%20%2F%2F%20This%20kind%20of%20borrowing%20does%20not%20allow%20mutation%20to%20the%20borrowed.%0A%20%20%20%20fn%20foo(v1%3A%20%26Vec%3Ci32%3E%2C%20v2%3A%20%26Vec%3Ci32%3E)%20-%3E%20i32%20%7B%0A%20%20%20%20%20%20%20%20%2F%2F%20do%20stuff%20with%20v1%20and%20v2%0A%20%20%20%20%20%20%20%20let%20s1%20%3D%20sum_vec(v1)%3B%0A%20%20%20%20%20%20%20%20let%20s2%20%3D%20sum_vec(v2)%3B%0A%20%20%20%20%20%20%20%20%2F%2F%20return%20the%20answer%0A%20%20%20%20%20%20%20%20s1%20%2B%20s2%0A%20%20%20%20%7D%0A%0A%20%20%20%20let%20v1%20%3D%20vec!%5B1%2C%202%2C%203%5D%3B%0A%20%20%20%20let%20v2%20%3D%20vec!%5B4%2C%205%2C%206%5D%3B%0A%0A%20%20%20%20let%20answer%20%3D%20foo(%26v1%2C%20%26v2)%3B%0A%20%20%20%20println!(%22%7B%7D%22%2C%20answer)%3B%0A%7D%0A

https://rufflewind.com/2017-02-15/rust-move-copy-borrow

---

# Form groups of 2-3 people
# open a laptop
# join #rust-workshop

Note:
Ask for the experience in the group, mix and match, e.g. ask for low level programming experience vs web and match those people in the groups

---

# Go through Rustlings on playpen

Note:
https://github.com/carols10cents/rustlings
check on all groups regularly
15-30 minutes max
highlight tests and borrowing and ownership
talk about returning to Rustlings as needed later

---

# Local env setup
* rustup or download installer for windows
* VSCode
* IntelliJ
* Vim
* others

Note:
let's setup the envs together - all computers, even the ones not used as primary in the group

---

# End of part 1

* into_rust
* the book v1 and v2
* rust by example
* this week in rust
* conference videos
* borrowing explained https://rufflewind.com/2017-02-15/rust-move-copy-borrow

---

# Let's build an echo server TDD way

Note:
Introduce test framework
Can be TCP-level, using hyper or nickel

---

# Let's build an echo server TDD way

Note:
Introduce test framework

---

# Let's build a chat client

Note:
groups can either be building client or server software

---

# Retrospective

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

* into_rust
* the book v1 and v2
* rust by example
* this week in rust
* conference videos
* borrowing explained https://rufflewind.com/2017-02-15/rust-move-copy-borrow
