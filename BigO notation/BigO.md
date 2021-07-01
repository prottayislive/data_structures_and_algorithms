# BigO Notation

## Time Complexity

What is Time Complexity and why do we care? 

When you want to express how fast an algorithm runs, simply just measuring the time of how long it takes to run would not be such a good idea that's
because the results would depend on other factors like how fast the computer is or the size of the input for example a function working on an input of five elements would probably end faster than if it were to work on an input of 5000 elements so we need a generalized way of expressing how fast an algorithm is
able to run
regardless of the size of the input or
other factors
and that is what time complexity is all
about
time complexity is often expressed with
big o
notation the big o is used to classify
algorithms
by how it behaves as the input size
increases
different time complexities linear
constant quadratic
let's say there is a series of lockers
and you have a book
in one of those lockers okay your task
is to find the book and how you find the
book
represents the algorithm you're using
linear first let's say you have no
information
about where the book is and you need to
look into
each locker one by one until you find
the book
if it takes one second to open a locker
and there are five lockers in the worst
case it's going to take you five seconds
where the worst case would be when the
book is in the
last locker if there are 10 lockers it
will take 10 seconds
100 lockers 100 seconds and so on
you can see that the time needed to find
that book
increases linearly as the number of
lockers you need to check gets larger
in big o notation this would be
expressed as
o of n where n represents the number of
lockers you'll need to scan
no matter how the line graph looks when
the time
increases linearly to the input the big
o
of the algorithm will still be o of n
for example if it takes you three
seconds to check one locker instead of
one second
or you're super fast and it only takes
you half a second
to check a locker you might find the
book slower or quicker
but the big o of finding the book will
still be
of n some algorithms might have a slow
startup time let's say you and me we are
both
able to open a locker in half a second
but for me
i have to eat a sandwich for 10 seconds
before i start the search
even though i have a longer startup time
my algorithm
is still asymptotically equivalent to
yours
we'll talk about what asymptotically
means later
so in summary when we are talking about
big-o notation
the coefficients or constants don't
matter it's just of n
we call this linear time complexity now
let's look at another complexity
which we call constant time o of one
algorithms with constant time are
considered to be good
because no matter how large the input
gets it will still take the same time
to perform a certain task if we go back
to the lockers
this time let's say we have another
person who's
psychic and can guess which locker has
the book
if the process of retrieving the book
takes one second and there are five
lockers
it will take one second to get the book
if there are ten lockers
it'll still be one second because we
know where the book is
and then a hundred lockers still one
second
let's say our psychic friend can guess
the locker correctly
but it takes five seconds to use their
powers
it might be slower than the one second
algorithm but it's still considered
constant time
another common time complexity would be
quadratic time
complexity o of n squared where the time
increases quadratically to the input
size
let's put a little twist to the first
example let's say you need a key
to open each locker and the keys are
jumbled up in a paper bag
you pick a random key and place it
outside of the bag
until you get the key for the locker you
want to open
once you have opened the locker you'll
put everything back in the bag
and start again you will have to repeat
this process to open each locker
and find the book when n equals five in
the worst case
you need to pick the keys five times for
each locker
so in total you would have to pick the
keys 25 times
if picking a key takes one second and we
just assume
that opening the locker doesn't take any
time it will take 25 seconds to find the
book
when n is 10 you would have to pick the
keys 100 times
10 times for each locker so the time
needed to find the book will
increase quadratically to the input
now that we have a better understanding
of what time complexity is
let's look a bit more into what
asymptotic analysis
means so far we looked into three
different types of
time complexities constant linear and
quadratic
when we plot them together it would look
like this
let's say you want to compare two
algorithms one has linear time
complexity
and the other one is quadratic the plot
would look
something like this you can see that
linear time complexity runs faster
and this seems right linear is
considered to be faster than quadratic
but let's say you run linear time
complexity algorithm on a really slow
computer
then your plot would look something more
like this
it seems here that the quadratic time
complexity algorithm is
actually faster than the linear do you
see the problem here
when you're trying to say that this
algorithm is more efficient than the
other
the runtime shouldn't change depending
on external factors like
computing power so we need a generalized
way of expressing how fast an
algorithm is which is where asymptotic
analysis comes in
as we put in a larger input coefficients
and constants in the function will
become less significant
when we were running the linear
complexity algorithm in
a slower computer we were changing the
coefficient
but as the input size grows you can see
that it doesn't matter at the end
eventually linear time complexity
algorithms will
run faster this is what i was talking
about in the sandwich eating example
even if i eat a sandwich for 10 seconds
before i start looking for the book
that wouldn't be such a big deal if
there are hundreds and hundreds of
lockers to search
when you compare an algorithm that is
asymptotically
more efficient than the other then it's
guaranteed to be faster
eventually as you keep increasing the
input size
no matter the constants or the
coefficients
and when we are trying to figure out the
big o of an algorithm
we also need to drop the non-dominant
terms
for example let's say there is a
function that consists of three parts
that runs sequentially the first part
and the second part has an algorithm of
o of n squared and the third part is an
algorithm of o of n you would think that
this would be
o of two times n squared plus n
but this function is actually just o of
n squared
because first we drop the constant and
the coefficients
then we only choose the highest order
and drop the rest
so it's just an o of n squared so we've
seen
three types of time complexities
constant time complexity is when we're
just doing a simple operation
linear time complexity is when we have
to loop through the input
and quadratic time complexity is when
there is a loop in a loop
there is also logarithmic time
complexity o
of log n a common example for this is
when
the input size is divided into half for
each loop
so the number of loops we need to run
will be less than just a normal loop
there are also linearity algorithms o of
n log n
which is worse than linear time
complexity but better than quadratic
cubic time complexities are even worse
than quadratic time complexities
just think of a loop in a loop in a loop
that would be horrible
exponential time complexities o of 2 to
the n
will multiply the number of operations
whenever there is an
additional input think about the number
of attempts we need to take to guess
3-digit password and 4-digit password we
increased the password length by one
but the number increased from one
thousand to ten thousand
if you see the six types of time
complexities in this plot
it is pretty clear that in this order
the time complexity gets good
to bad when you compare an algorithm
that is asymptotically more efficient
than the other
then it's guaranteed to be faster
eventually as you keep
increasing the input size no matter the
constants
or the coefficients and when you're
trying to decide which is the dominant
term in your algorithm
you need to pick the worst one which you
can decide from this order
let's look into an example this example
is about finding the two numbers
in an array that sums up to the target
let's say you can use the same number
twice for example
if the target is 12 and its input array
is
7 2 9 3 11
it will return the indices of the values
9
and 3. if the target is 4 the function
is looping
each index of the array and for each
index it loops again
to see if they add up to the target so
it's a loop in a loop
this algorithm will have a quadratic
time complexity
if there are 5 elements in the array in
the worst case this line will be
executed 25 times
if there are 6 elements then 6 times 6
36
36 times and then so on let's look at
another example
the first part of the function is a loop
in the loop this line
will run n squared times so the time
complexity of this
would be o n squared the second part
will run
n times we are just looping n times so
it will be
of n we drop the o of n because it is
not dominant so the time complexity of
this function
will be o n squared so far we talked
about what time complexity is
why we should care about it we also
talked about linear constant and
quadratic time complexity
and we talked about asymptotic analysis
that's it for time complexity i hope
this was helpful and i'll see you in the
next one
