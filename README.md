Download Link: https://assignmentchef.com/product/solved-cmsc-204-assignment-2
<br>
Office Depo, an office supply retailing company, donates its surpluses to colleges at the end of each year. Volunteers will help deliver packages of supplies to representatives of colleges (Recipient of supplies). Write an application to simulate delivering packages from the container of packages by the volunteers to recipients.

<strong> Concepts tested:</strong>

Generic Queue

Generic Stack

Exception handling

<strong>Data Elements </strong>

<strong>      Volunteer- </strong>Holds the relevant information for a Volunteer:  <em>name</em>

<strong>      DonationPackage- </strong>Holds the information of the package to be donated: <em>description, weight</em>

<strong>      Recipient- </strong>Holds the information of the recipients: <em>name</em>

<strong> </strong>

<strong>Data Structures</strong>

<ol>

 <li>Create a generic queue class called <strong>MyQueue</strong> that implements the <strong>QueueInterface</strong> given you.</li>

 <li>Create a generic stack class called <strong>MyStack</strong> that implements the <strong>Stack</strong> <strong>Interface</strong> given you.</li>

 <li>Create a class <strong>VolunteerLine</strong> that implements <strong>VolunteerLineInterface</strong>.</li>

</ol>

This class contains a queue of Volunteers and simulates queuing and dequeuing volunteers to and from the volunteers’ line.

<ol start="4">

 <li>Create a class <strong>RecipientLine</strong> that implements <strong>RecipientLineInterface</strong> .</li>

</ol>

This class contains a queue of Recipients and simulates queuing and dequeuing Recipients to and from the recipients’ line.

<ol start="5">

 <li>Create a class <strong>Container</strong> that implements <strong>ContainerInterface</strong>.</li>

</ol>

This class contains a stack of <strong>DonationPackage</strong> and simulates adding and removing package from the container’s stack.




<strong>Assumptions</strong>

<ul>

 <li>When a volunteer enters a queue they will stay in the queue and every time that the volunteer is removed from the line they will be go back to the end of the line.</li>

 <li>When a recipient receives a donation package they will leave their queue.</li>

 <li></li>

</ul>

<strong>Data Manager</strong>The <strong>DonationManager</strong> class will manage adding a new package to the container, a new volunteer to the volunteer queue line, a new recipient to the recipient queue and donating package by the volunteer to the recipient.  <strong>DonationManager</strong>   will implement the interface <strong>DonationManager Interface</strong>.

<strong>Exception Classes</strong>

<ol>

 <li><u>RecipientException</u>:</li>

</ol>

<strong>public</strong> <strong>class</strong> <u>RecipientException</u> <strong>extends</strong> RuntimeException {




<strong>public</strong> RecipientException(){};




RecipientException(String message) {

<strong>super</strong>(message);

}




If the user attempts to add new Recipient and the recipient line is full, throw RecipientException(“Recipient Queue is full”).  If user attempts to remove a recipient and the recipient is empty, throw RecipientException(“Recipient Queue is empty”);

<ol start="2">

 <li>VolunteerException – similar to RecipientException except throws VolunteerException when the Volunteer Queue is full or empty</li>

 <li>ContainerException – similar to RecipientException except throws ContainerException when the Volunteer Stack is full or empty</li>

</ol>




<strong>You may add additional methods and attributes to your classes.</strong>

<strong>GUI Driver – provided for you</strong>




<ol>

 <li>Initially there is no package on the container stack, or any volunteers or recipients on the queue.</li>

 <li>Allows the user to load new packages to the container and add new volunteers to volunteer’s line and new recipient to recipients’ line.</li>

 <li>Allows the user to simulate the process of donating a package from the container by the volunteer on the front of the Volunteer queue to the recipient on the front of the Recipient queue. When a volunteer finishes donating the package to the recipient, he/she will be<u> placed at the back of the queue of volunteers</u> to continue the process of donation. <strong><u>Each volunteer takes one package at a time to deliver to the recipient.</u></strong></li>

</ol>

<strong> </strong>

<strong> </strong>

<strong>Examples:</strong>

<strong> </strong>

At startup

<strong>             </strong>

<strong> </strong>

























After selecting “Stack New Package”

Pen(first) and Books (second).














































After adding new Volunteers John (first),          After adding new Recipients MC (first),

Nicole (second)                                                   Maryland (second)





































After selecting Donate Package                                                  After selecting Donate Package Second time

First Time





































After selecting Donate Package Third time














































If the user tries to add a new volunteer and

The line of volunteers is full:








































<strong> </strong>




<strong>Grading Rubric – CMSC 204 Project #2</strong>

<strong> </strong>

Name _____________________________    .




<strong><u>PROGRAMMING</u></strong><strong>    </strong>(100 pts)<strong>                                                                                                </strong>

Compiles                                                                                                    40 pts _____

Accuracy

Passes public JUnit tests (provided)                                                   10 pts _____

Passes STUDENT tests                                                                        5 pts _____

Execution: runs without errors (either run-time or logic errors)               45 pts _____

Possible Sub-total                                                                               100 pts _____

<strong><u>REQUIREMENTS</u></strong>  (Subtracts from Programming total)

<strong><u>Documentation:</u></strong>

Javadoc was not provided                                                                          – 5 pts _____

Documentation within source code was missing or incorrect                     – 5 pts _____

Description of what class does was missing

Author’s Name, @author, was missing

Methods not commented properly using Javadoc @param, @return

UML diagram was not provided                                                                 – 5 pts _____

JUnit Test Class: STUDENT methods were not implemented                   – 5 pts _____

In 3+ paragraphs, highlight your lessons learned and learning experience          – 5 pts ______

from working on this project.  How did you do?  What have you learned?  What

did you struggle with? How will you approach your next project differently?