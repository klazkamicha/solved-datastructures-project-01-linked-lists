Download Link: https://assignmentchef.com/product/solved-datastructures-project-01-linked-lists
<br>
The purpose of this project is to make you used to handling linked lists. You are required to implement two different types of linked lists, namely, cyclic linked list, and doubly linked list. You are also required to create UML diagrams for each of the classes that you create. Finally, you have to provide the means to test your system by developing a menu program that allows the user to manipulate your linked lists.

<h1>Deliverables</h1>

<ul>

 <li>A 1 page pdf report with your UML diagrams and a brief explanation.</li>

 <li>An implementation of a cyclic linked list data structure.</li>

 <li>An implementation of a doubly linked list data structure.</li>

 <li>A menu program to test the implemented data structures.</li>

</ul>

<h1>1           Cyclic Linked List</h1>

In this part of the project, you need to implement two classes, and create their respective UML diagrams. Figure 1 shows examples of cyclic linked lists.

<ul>

 <li>Singly linked list with three nodes.</li>

 <li>An empty singly linked list.</li>

</ul>

<strong>Figure 1: </strong>Examples of singly linked lists.

<em>1.1      Deliverables</em>

<h2>1.1         Deliverables</h2>

<ul>

 <li>Singly linked node class with UML diagram.</li>

 <li>Cyclic linked list class with UML diagram.</li>

</ul>

<h2>1.2         SingleNode Class</h2>

<h3>1.2.1         Description</h3>

A class that stores an element of any type and a pointer to the next node in a list.

<h3>1.2.2         Data Members</h3>

<ol>

 <li>A <em>Type </em>variable that contains the <em>data </em>information of the node.</li>

 <li>A pointer to a SingleNode object, referred to as the <em>next </em></li>

</ol>

<strong>1.2.3        Member Functions</strong>

<strong>Constructor</strong>

<h3>SingleNode( Type const &amp;, SingleNode *)</h3>

This constructor takes two arguments: a constant reference to a Type (by default, an integer) and a pointer to a SingleNode (by default nullptr). These are assigned to the member variables, respectively.

<strong>Destructor</strong>

This class uses the default destructor.

<h3>Accessors</h3>

<strong>Type getData() const         </strong>Returns the <em>data </em>element of the node.

<strong>SingleNode *getNext() const          </strong>Returns the <em>next </em>pointer.

<strong>Mutators</strong>

This class has no mutators.

<h3>Friends</h3>

This CyclicLinkedList<em>&lt; Type &gt; </em>is a friend of this class.

<em>1.3        CyclicLinkedList Class</em>

<h2>1.3         CyclicLinkedList Class</h2>

<h3>1.3.1         Description</h3>

This class stores a finite list of n (zero or more) elements stored in singly linked nodes. If there are zero elements in the list, the list is said to be empty. Each element is stored in an instance of the SingleNode<em>&lt; Type &gt; </em>class. If the list is empty, the head pointer is assigned nullptr. Otherwise, head pointer points to the first node, the next pointer of the <em>ith </em>node (1 ≤ <em>i &lt; n</em>) points to the (<em>i </em>+ 1)st node, and the next pointer of the nth node points to the first node.

<h3>1.3.2         Data Members</h3>

<ol>

 <li>A pointer to the head of the list, referred to as the <em>head </em></li>

 <li>A pointer to the tail of the list, referred to as the <em>tail </em></li>

 <li>An integer that holds the <em>size </em>of the linked list. The number of elements in the list.</li>

</ol>

<strong>1.3.3        Member Functions</strong>

<h3>Constructors</h3>

<strong>CyclicLinkedList() </strong>This constructor sets all member variables to 0 or nullptr, as appropriate.

<h3>Destructor</h3>

The destructor must delete each of the nodes in the linked list.

<strong>Accessors int size() const;            </strong>returns the number of items in the list. <strong>bool empty() const;              </strong>Returns true if the list is empty, false otherwise.

<strong>Type front() const; </strong>Retrieves the object stored in the node pointed to by the head pointer. This function throws a underflow if the list is empty.

<strong>Type back() const; </strong>Retrieves the object stored in the node pointed to by the tail pointer. This function throws a underflow if the list is empty.

<strong>SingleNode</strong><em>&lt; Type &gt; </em><strong>*head() const;          </strong>Returns the head pointer.

<strong>SingleNode</strong><em>&lt; Type &gt; </em><strong>*tail() const;          </strong>Returns the tail pointer.

<em>1.3        CyclicLinkedList Class</em>

<strong>int count( Type const &amp; ) const;           </strong>Returns the number of nodes in the

linked list storing a value equal to the argument.

<h3>Mutators</h3>

<strong>void push </strong><strong>front( Type const &amp; ); </strong>Creates a new SingleNode<em>&lt; Type &gt; </em>storing the argument, the next pointer of which is set to the current head pointer. The head pointer is set to this new node. If the list was originally empty, the tail pointer is set to point to the new node.

<strong>void push back( Type const &amp; );             </strong>Similar to push front, this places a

new node at the back of the list.

<strong>Type pop front(); </strong>Delete the node at the front of the linked list and, as necessary, update the head and tail pointers. Return the object stored in the node being popped. Throw an underflow exception if the list is empty.

<strong>void pop back();           </strong>Similar to pop front, this deletes the node at the back

of the list and returns the object.

<strong>int erase( Type const &amp; ); </strong>Delete the node(s) (from the front) in the linked list that contains the element equal to the argument (use == to to test for equality with the retrieved element). As necessary, update the head and tail pointers and the next pointer of any other node within the list. Return the number of nodes that were deleted.

<strong>Friends</strong>

This class has no friends.

<h1>2           Doubly Linked List</h1>

In this part of the project, you need to implement two classes, and create their respective UML diagrams. Figure 2 shows examples of doubly linked lists.

<ul>

 <li>Doubly linked list with three nodes.</li>

 <li>An empty doubly linked list.</li>

</ul>

<strong>Figure 2: </strong>Examples of doubly linked lists.

<h2>2.1         Deliverables</h2>

<ul>

 <li>Doubly Linked node class with UML diagram.</li>

 <li>Doubly linked list class with UML diagram.</li>

</ul>

<h2>2.2         DoubleNode Class</h2>

<h3>2.2.1         Description</h3>

A class which stores an object, a pointer to the next node in a linked list, and a pointer to the previous node in the linked list.

<h3>2.2.2         Data Members</h3>

<ol>

 <li>A <em>Type </em>variable that contains the <em>data </em>information of the node.</li>

 <li>A pointer to a DoubleNode object, referred to as the <em>next </em></li>

 <li>A pointer to a DoubleNode object, referred to as the <em>previous </em></li>

</ol>

<strong>2.2.3        Member Functions</strong>

<strong>Constructor</strong>

<h3>DoubleNode( Type const &amp;, DoubleNode *, DoubleNode *)</h3>

This constructor takes three arguments: a constant reference to an Type (by default, an integer) and two pointers to a DoubleNode (each by default nullptr). These are assigned to the member variables, respectively.

<h3>Destructor</h3>

This class uses the default destructor.

<em>2.3        DoublyLinkedList Class</em>

<h3>Accessors</h3>

<strong>Type getData() const        </strong>Returns the element of the node.

<strong>DoubleNode *getNext() const          </strong>Returns the next pointer.

<strong>DoubleNode *getPrevious() const         </strong>Returns the previous pointer.

<strong>Mutators</strong>

This class has no mutators.

<strong>Friends</strong>

This DoublyLinkedList<em>&lt; Type &gt; </em>is a friend of this class.

<h2>2.3         DoublyLinkedList Class</h2>

<h3>2.3.1         Description</h3>

This class stores a finite list of n (zero or more) elements stored in doubly linked nodes. If there are zero elements in the list, the list is said to be empty. Each element is stored in an instance of the DoubleNode<em>&lt; Type &gt; </em>class. If the list is empty, the head and tail pointers are assigned nullptr. Otherwise, the head pointer points to the first node, the tail pointer points to the nth node, the next pointer of the <em>ith </em>node (1 ≤ <em>i &lt; n</em>) points to the (<em>i</em>+1)st node, the next pointer of the nth is assigned nullptr, the previous pointer of the <em>ith </em>node (2 ≤ <em>i </em>≤ <em>n</em>) points to the (<em>i</em>−1)st node, and the previous pointer of the first node is assigned nullptr.

<h3>2.3.2         Data Members</h3>

<ol>

 <li>A pointer to the head of the list, referred to as the <em>head </em></li>

 <li>A pointer to the tail of the list, referred to as the <em>tail </em></li>

 <li>An integer that holds the <em>size </em>of the linked list. The number of elements in the list.</li>

</ol>

<strong>2.3.3        Member Functions</strong>

<h3>Constructors</h3>

<strong>DoublyLinkedList() </strong>This constructor sets all member variables to 0 or nullptr, as appropriate.

<h3>Destructor</h3>

The destructor must delete each of the nodes in the linked list.

<em>2.3        DoublyLinkedList Class</em>

<strong>Accessors int size() const;            </strong>returns the number of items in the list. <strong>bool empty() const;              </strong>Returns true if the list is empty, false otherwise.

<strong>Type front() const; </strong>Retrieves the object stored in the node pointed to by the head pointer. This function throws a underflow if the list is empty.

<strong>Type back() const; </strong>Retrieves the object stored in the node pointed to by the tail pointer. This function throws a underflow if the list is empty.

<strong>DoubleNode</strong><em>&lt; Type &gt; </em><strong>*head() const;           </strong>Returns the head pointer.

<strong>DoubleNode</strong><em>&lt; Type &gt; </em><strong>*tail() const;          </strong>Returns the tail pointer.

<strong>int count( Type const &amp; ) const;           </strong>Returns the number of nodes in the

linked list storing a value equal to the argument.

<h3>Mutators</h3>

<strong>void push front( Type const &amp; ); </strong>Creates a new DoubleNode<em>&lt; Type &gt; </em>storing the argument, the next pointer of which is set to the current head pointer. The head pointer is set to this new node. If the list was originally empty, the tail pointer is set to point to the new node.

<strong>void push back( Type const &amp; );             </strong>Similar to push front, this places a

new node at the back of the list.

<strong>Type pop front(); </strong>Delete the node at the front of the linked list and, as necessary, update the head and tail pointers. Return the object stored in the node being popped. Throw an underflow exception if the list is empty.

<strong>void pop back();           </strong>Similar to pop front, this deletes the node at the back

of the list and returns the object.

<strong>int erase( Type const &amp; ); </strong>Delete the node(s) (from the front) in the linked list that contains the element equal to the argument (use == to to test for equality with the retrieved element). As necessary, update the head and tail pointers and the next pointer of any other node within the list. Return the number of nodes that were deleted.

<strong>Friends</strong>

This class has no friends.

<h1>3           The Menu Program &amp; Submission Guidelines</h1>

In order to test your program, you are required to implement a menu program that provides the means to run each of the functions in your classes. Please choose the <em>double </em>simple data type to create the linked lists in your menu program. So for example, when asked to create a linked list, its nodes should hold double elements in their data fields. The TA will randomly choose one group to defend the demo, and the same grade will be assigned to all of the members of the group.

<h2>Format for the Menu Program</h2>

First, take a character, ’s’ or ’d’ (lowercase) that specifies whether we will be working with a singly or doubly linked list. Next, give the options (please have them in this <strong>EXACT </strong>order for grading purposes):

<ol>

 <li>Create list</li>

 <li>Count number of items</li>

 <li>Retrieve first item</li>

 <li>Retrieve last item</li>

 <li>Count instances of an item</li>

 <li>Push front</li>

 <li>Push back</li>

 <li>Pop front</li>

 <li>Pop back</li>

 <li>Delete instance(s) of an item</li>

 <li>Print list</li>

 <li>Exit</li>

</ol>