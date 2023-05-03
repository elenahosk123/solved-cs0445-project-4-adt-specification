Download Link: https://assignmentchef.com/product/solved-cs0445-project-4-adt-specification
<br>
Imagine that you are starting a streaming radio business. Partnerships have been established to provide you with audio content, and you will stream that content to users. You plan to use your knowledge of what songs your users like/dislike to make effective suggestions for new songs that they will like.

In this assignment, you will be <strong>designing an abstract data type (ADT)</strong> that stores the service’s music library and users’ ratings of songs. This ADT represents a data structure that will be used by both client applications and for administrative uses (like adding new songs to the library).

Once you complete this ADT, you could provide it to the programmers of the client applications, and they will be able to develop applications based on this specification – like you did in project 1.

You could also distribute the ADT to the engineers in charge of <em>implementing</em> the functionality of the data structure. Then these two groups can work in parallel on their respective components, which can work together since they both follow the “contract” that your ADT provides.

You will not be implementing this data structure.

You do not need to consider implementation-level details, since you are only writing the ADT. This means that you must specify the full set of details that a <strong>client needs to know</strong> in order to use the data structure, but <strong>not the details of how the operations will be carried out</strong> or how the data will be organized in memory. The implementation details should be left up to the implementers.

<h2>Starting point</h2>

<a href="/teaching/classes/cs0445/projects/cs0445_proj4_materials.zip">Download and extract these materials.</a> Contained are:

<ul>

 <li>the StreamingRadio interface, <strong>the file you will modify.</strong></li>

 <li>User, Song, and Station are interfaces you can use for your your methods’ parameters and return types.

  <ul>

   <li><strong>You do not need to implement these!</strong> They’re just there for that reason.</li>

   <li><strong>You do not need to assume any of their methods or add methods.</strong> Just use their names.</li>

  </ul></li>

 <li>doc/ is a directory containing the Javadoc output.

  <ul>

   <li>open index.html to view the docs.</li>

  </ul></li>

</ul>

<h2>Your task</h2>

You must write an abstract data type as a Java interface.

We have given you the names of several abstract methods that the data structure would need to support. You must specify them in the Javadoc comments above each method.

You should consider all possible corner cases in your specification, and describe what the class should do in all cases. A client that reads your ADT should know all the things that could go wrong, and how each will be handled.

Error cases should be unambigous to the client, and they should always know which specific error was encountered. For some corner cases, you will need to make a design decision regarding the best way to handle them. You have the freedom to make these decisions any way you wish, as long as you are consistent, thorough, and clear in your descriptions.

Remember that you document parameters by using the @param name command; return values with @return, and exceptions with @throws name.

<h3>The methods</h3>

There are 8 methods. 1 has been done for you, as an example of the kind of specification we are looking for. So you must do the remaining 7. You will be adding parameters, return types, and exceptions to throw to each. Each one has a short description in StreamingRadio.java, so read those.

<ul>

 <li>addSong</li>

 <li>removeSong</li>

 <li>addToStation</li>

 <li>removeFromStation</li>

 <li>rateSong</li>

 <li>clearRating

  <ul>

   <li>we’ve specified this one for you.</li>

   <li>you can change its specification, if you need to make it work better with your other methods.</li>

  </ul></li>

 <li>predictRating</li>

 <li>suggestSong</li>

</ul>

<h3>Notes</h3>

<ul>

 <li>You can assume that the set of users and the set of radio stations are fixed.

  <ul>

   <li>That way, you do not need to include operations to change these collections.</li>

  </ul></li>

 <li>When coming up with exceptions, you can use <a href="https://www.tutorialspoint.com/java/java_builtin_exceptions.htm">the standard Java exceptions</a> where they make sense.

  <ul>

   <li>If none of them fit, you are free to create your own exception classes.</li>

   <li>Follow the template of the exception classes we gave in projects 1 and 3.</li>

  </ul></li>

 <li>Remember, <em>you are specifying the interface to the client.</em>

  <ul>

   <li>The implementors will <em>use</em> this interface, but they will come up with their own implementation.</li>

  </ul></li>

</ul>

<h2>Testing</h2>

Well, you’re not writing any code, but you <em>are</em> writing documentation, and your interface <em>should</em> compile with javac. You won’t be able to run it, of course &#x1f609;

Use this command to produce the HTML documentation:

javadoc -html5 -d doc *.java

If your documentation parses fine, it will produce a file in doc/ named index.html which you can open to view it.

If you are using a version of Java older than 1.9, upgrade. If you can’t, use this command: javadoc -d doc *.java