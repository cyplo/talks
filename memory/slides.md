# 5+1 ways of managing program's memory in 5+0 minutes

---

# Manual
<pre>
<code data-trim class="C">
int main()
{
    int* a = malloc(sizeof(int));
}
</code>
</pre>

---

# Somewhat manual
> manual reference counting, in e.g. objc

---

# Automatic, stack-based, sync
> scope-based variables in almost all languages

---

# Somewhat automatic, sync
> ARC in objc

---

# Automatic, async 
> garbage collection in JVM and .Net

---


