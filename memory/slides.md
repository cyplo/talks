
<style type='text/css'>
    pre, code {
        white-space: pre-wrap;
    }
</style>

# 5+1 ways of managing program's memory in 5+0 minutes

---

# Manual
<pre>
<code data-trim class="C">
int main()
{
    int* pointer = malloc(sizeof(int));
    *pointer = 5;
    printf("there's value of %i under address of %x\n", *pointer, pointer);
    free(pointer);
    printf("there's probably some value of %i under address of %x, or we just crash here, who knows\n", *pointer, pointer);
    free(pointer); // we maybe crash or not
}
</code>
</pre>

<pre>
there's value of 5 under address of 1f70010
there's probably some value of 0 under address of 1f70010, or we just crash here, who knows
*** Error in `./a.out': double free or corruption (fasttop): 0x0000000001f70010 ***
[1]    31312 abort      ./a.out
<pre>

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


