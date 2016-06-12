
<style type='text/css'>
    pre, code {
        white-space: pre-wrap;
    }
</style>

# 5+1 ways of managing program's memory in 5+0 minutes

---

> My memory is already managed, why ?

<pre>
<code data-trim class="C">
int double_value(int x) // x is 'allocated'
{
	return 2*x;
} // x gets 'destroyed'

int main()
{
	int value = 5;
	int value_doubled = double_value(5);
	printf("value %i is %i when doubled\n", value, value_doubled);
} // all stuff 'destroyed'
</code>
</pre>
<pre>
$ valgrind ./a.out    
==1729== Memcheck, a memory error detector
[...]
value 5 is 10 when doubled
[...]
==1729== All heap blocks were freed -- no leaks are possible
</pre>

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

# Somewhat automatic, sync
> ARC in objc

---

# Automatic, async 
> garbage collection in JVM and .Net

---


