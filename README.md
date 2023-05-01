Download Link: https://assignmentchef.com/product/solved-cis-212-assignment-6-building-a-new-generic-data-structure
<br>
The goal of this assignment is to provide exposure to building a new generic data structure.  Specifically, this project will involve building a new Set structure that maintains the “add” counts of its unique elements, so that they can be iterated in sorted order with respect to how many times they’ve been added to the set.  The Set implementation will be optimized for efficient add/remove/contains over efficient iteration.

<ol>

 <li>Create a new class OccurrenceSet&lt;T&gt; that implements Set&lt;T&gt;. Your OccurrenceSet implementation should create and maintain a HashMap&lt;T, Integer&gt;; doing so will allow you to easily track the integer “add” count for each element in the set.  All methods should function as specified in the Set documentation.  Additionally:

  <ul>

   <li> The <em>add</em> and <em>addAll</em> methods will need to keep track of how many times an element has been added to the set. We are optimizing for efficient add, so <em>add</em> should be <em>O(1)</em> and <em>addAll</em> should be <em>O(n) </em>for <em>n</em> added elements.</li>

   <li> The <em>remove</em>, <em>removeAll</em>, and <em>retainAll</em> methods should remove the necessary elements from the set completely (i.e., not just decrement their counts). We are optimizing for efficient remove, so <em>remove</em> should be <em>O(1)</em> and <em>removeAll</em> should be <em>O(n) </em>for <em>n</em> removed elements.</li>

   <li> The <em>contains</em> and <em>containsAll</em> methods should behave as documented and operate in <em>O(1)</em> and <em>O(n) </em>time (i.e., for <em>n</em> query elements), respectively.</li>

   <li>The s<em>ize</em> method should return the number of unique elements currently in the set (i.e., not considering “add” counts). This method should be <em>O(1)</em>.  The <em>clear </em>and <em>isEmpty</em> methods should behave as documented.</li>

   <li>The <em>iterator</em> and <em>toArray</em> methods should return an Iterator or array, respectively, with elements sorted by their “add” counts in ascending order. We are optimizing for efficient add/contains over iteration, but these methods should still be <em>O(n lg n)</em>.  The Iterator <em>remove </em>method can be left blank for this assignment.</li>

  </ul></li>

</ol>

Hint: Creating a new List and using the Collections <em>sort</em> method is reasonable here, though note that you’ll need to implement a Comparator object so that the elements can be sorted by their associated counts.

<ul>

 <li>Add a <em>toString</em> method that returns a string representation of the elements in the list in sorted order (i.e., ascending with respect to their “add” counts). This method should be <em>O(n lg n)</em>.</li>

</ul>

<ol start="2">

 <li>Create a Main class that creates a few OccurrenceSets of various types to test the functionality of your new data structure. For example, a test like:</li>

</ol>

OccurrenceSet&lt;Integer&gt; intSet = <strong>new</strong> OccurrenceSet&lt;Integer&gt;();

intSet.add(1); intSet.add(3); intSet.add(5); intSet.add(5); intSet.add(3); intSet.add(3); intSet.add(3);

System.<strong><em>out</em></strong>.println(intSet);

OccurrenceSet&lt;String&gt; stringSet = <strong>new</strong> OccurrenceSet&lt;String&gt;(); stringSet.add(“hello”); stringSet.add(“hello”); stringSet.add(“world”); stringSet.add(“world”); stringSet.add(“world”); stringSet.add(“here”); System.<strong><em>out</em></strong>.println(stringSet); Should have the output:

[1, 5, 3]

[here, hello, world]

<ol start="3">

 <li>Write code that is clear and efficient. Specifically, your code should be indented with respect to code blocks, avoid unnecessarily repetitive code, avoid code that is commented out or otherwise unused, use descriptive and consistent class/method/variable names, etc.</li>

</ol>