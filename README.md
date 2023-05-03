Download Link: https://assignmentchef.com/product/solved-cs1331-homework-13-ls-cat
<br>
<h1>Problem Description</h1>

Still stuck in the future, you’re starting to enjoy it. You’ve helped space explorers improve their data infrastructure, and briefly got launched into the world of Pokémon where you’ve left Professor Oak and the Pokemon Center eternally grateful for your services.

Unfortunately, you learn that “Georgia Tech University” was really just a front for a school named “Georgia

Tech”! Professor Oak reveals himself to be the professor of a class named CS 1331 and tells you to get back to your homework and to stop reading pointless problem descriptions.

<h1>Solution Description</h1>

For this assignment, create the following files:

<ul>

 <li>java</li>

 <li>java</li>

 <li>java</li>

</ul>

<strong>FileHelper Class:</strong>

FileHelper will contain static helper methods that have functionality similar to the <a href="https://en.wikipedia.org/wiki/Ls">ls</a> and <a href="https://en.wikipedia.org/wiki/Cat_(Unix)">cat</a> unix commands.

Methods:

<ul>

 <li>public static void printLs(String path)

  <ul>

   <li>This will print out all of the files and folders that are contained within the folder located at path.</li>

   <li>You must use the printLsHelper method below.</li>

   <li>You may assume that the path parameter contains the path to a folder.</li>

  </ul></li>

 <li>private static void printLsHelper(String path, int indentationLevel)

  <ul>

   <li><strong>Must recursively call itself</strong></li>

   <li>For every indentationLevel, print 4 spaces at the beginning of the line before printing anything else.</li>

   <li>If the path that is passed in is a path to a file, print out the name of the file.</li>

   <li>If the path that is passed in is the path to a folder, print out the name of the folder and then, indented a level, print out the contents of the folder (Hint: recursion).</li>

   <li>This problem must be solved recursively or you will receive a heavy deduction (Hint: if you are not making at least one recursive call per folder, you are probably doing it wrong). <strong>– </strong>See the example below in testing your code for formatting to follow!</li>

  </ul></li>

 <li>public static void printCat(String path)

  <ul>

   <li>If path isn’t a path to a real file or is a directory, throw a CatException. The message should be “Path invalid.” and pass in the path.</li>

   <li>Otherwise</li>

  </ul></li>

</ul>

∗ For each line in the file, print out “{line number}: {line from text file}” ∗ See the example below in testing your code for formatting to follow!

<strong>CatException Class:</strong>

<ul>

 <li>Make this custom Exception be a Checked Exception</li>

 <li>Take a String message and String problemFile into the constructor. Pass message to super and store problemFile in a private final field called problemFile to keep track of the path to the file.</li>

 <li>Override getMessage() to include the original message (Hint: use super’s getMessage()) plus the absolute path to the problemFile in the following format: “{original message}. Problem with file {absolute path}!”

  <ul>

   <li>problemFile may be an absolute path or a relative path. Make sure to print out an absolute path.</li>

  </ul></li>

</ul>

<strong>Tester Class:</strong>

<ul>

 <li>Have a main method that takes in a file path in a command line argument. Print the output of ls of the current directory and then print the output of cat with the passed in file.

  <ul>

   <li><strong>Make sure your path to the current directory is a relative path and not a hard-coded or absolute path.</strong></li>

   <li><strong>Do not use backslashes (“”) when indicating the current directory. Use forward slashes instead.</strong></li>

   <li>Your main method should not handle any Exceptions that could occur when calling printLs or printCat and instead propogate them to the caller of the main method.</li>

  </ul></li>

</ul>

<strong>Testing your code:</strong>

The below examples will use the folder structure

Foo

|- Bar

| |- Biz

| | |- Hi.txt

| | |- Shishi.png

| |- Lambda.java

|- Bat

| |- Scary.gif

|- Stop.txt

|- Spooky.txt

|- FileHelper.java

|- FileHelper.class

|- CatException.java

|- CatException.class

|- Tester.java

|- Tester.class

Assume that Spooky.txt contains:

In the cool of the evenin’ when ev’rything is gettin’ kind of groovy

I call you up and ask you if you’d like to go with me and see a movie

First you say “no”, you’ve got some plans for the night And then you stop, and say, “all right”

Love is kinda crazy with a spooky little girl like you and Stop.txt contains:

In Defense of Christmas Music in October.

Ah, Christmas music! The warm tunes that remind so many of us of

huddling around a fire surrounded by family.

The sounds that remind of pine scents, mistletoe, and holiday cheer. There’s so much good feeling attached to Christmas music that it’s nice to dip into the holiday playlists early and get excited about what’s to come.

printLs(“Foo”) would print out

Foo

Bar

Biz

Hi.txt

Shishi.png

Lambda.java

Bat

Scary.gif

Stop.txt

Spooky.txt

FileHelper.java

FileHelper.class

CatException.java

CatException.class

Tester.java

Tester.class printCat(“Foo/Spooky.txt”) would print out

1: In the cool of the evenin’ when ev’rything is gettin’ kind of groovy

2: I call you up and ask you if you’d like to go with me and see a movie

3: First you say “no”, you’ve got some plans for the night

4: And then you stop, and say, “all right”

5: Love is kinda crazy with a spooky little girl like you

Running java Tester ./Stop.txt would output the following assuming that you are currently in the Foo directory

Foo

Bar

Biz

Hi.txt

Shishi.png

Lambda.java

Bat

Scary.gif

Stop.txt

Spooky.txt

FileHelper.java

FileHelper.class

CatException.java

CatException.class

Tester.java

Tester.class

1: In Defense of Christmas Music in October.

2: Ah, Christmas music! The warm tunes that remind so many of us of 3: huddling around a fire surrounded by family.

4: The sounds that remind of pine scents, mistletoe, and holiday cheer. 5: There’s so much good feeling attached to Christmas music that it’s nice to dip 6: into the holiday playlists early and get excited about what’s to come.

Depending on how you implement it Foo may just be . or ./ in all of the above examples and that is okay.

<h1>Allowed Imports</h1>

<ul>

 <li>You are only allowed to import the following classes:</li>

</ul>

<ul>

 <li>util.Scanner</li>

 <li>io.*</li>

 <li>nio.file.*</li>

</ul>

<h1>Rubric</h1>

<ul>

 <li>[55] FileHelper.java

  <ul>

   <li>[2.5] printLs()</li>

  </ul></li>

</ul>

∗ [2.5] Correct method header

<ul>

 <li>[35] printLsHelper()</li>

</ul>

∗ [2.5] Correct method header

∗ [12.5] Calls itself recursively

∗ [10] Output has correct spacing for each indentation level

∗ [10] Prints file name when appropriate

<ul>

 <li>[17.5] printCat()</li>

</ul>

∗ [2.5] Correct method header

∗ [10] Cat command has correct output

∗ [5] Throws CatException

<ul>

 <li>[25] CatException.java

  <ul>

   <li>[5] Overrides getMessage() with correctly formatted message</li>

   <li>[5] Is a checked exception</li>

   <li>[2.5] Call to super in constructor</li>

   <li>[2.5] Call to super in getMessage()</li>

   <li>[5] Correct instance fields</li>

   <li>[5] Constructor with two parameters correctly assigned</li>

  </ul></li>

 <li>[20] Tester.java

  <ul>

   <li>[10] Takes in command line arguments</li>

   <li>[10] Handles exceptions thrown when calling printLs or printCat</li>

  </ul></li>

</ul>

<h1>Javadocs</h1>

For this assignment, you will be commenting your code with Javadocs. Javadocs are a clean and useful way to document your code’s functionality. For more information on what Javadocs are and why they are awesome, the <a href="http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html">online overview</a> for them is extremely detailed and helpful.

You can generate the javadocs for your code using the command below, which will put all the files into a folder called javadoc:

$ javadoc *.java -d javadoc

The relevant tags that you need to include are @author, @version, @param, and @return. Here is an example of a properly Javadoc’d class:

<strong>import </strong>java.util.Scanner;

<em>/**</em>

<em>* </em>This class represents a Dog object<em>. * </em><strong>@author </strong>George P<em>. </em>Burdell

<table width="632">

 <tbody>

  <tr>

   <td width="632">* <strong>@version </strong><em>1.0</em><em>*/ </em><strong>public class </strong>Dog {<em>/**</em>* Creates an awesome dog <em>(</em>NOT a dawg<em>!) */</em><strong>public </strong>Dog() { …}<em>/**</em>* This method takes in two ints and returns their sum* <strong>@param a </strong>first number* <strong>@param b </strong>second number <em>* </em><strong>@return </strong>sum of a and b<em>*/</em><strong>public </strong>int add(int a, int b) {…}}</td>

  </tr>

 </tbody>

</table>

A more thorough tutorial for Javadocs can be found <a href="https://cs1331.gitlab.io/cs1331-style-guide.html">here</a>. Take note of a few things:

<ol>

 <li>Javadocs are begun with /** and ended with */.</li>

 <li>Every class you write must be Javadoc’d and the @author and @verion tag included. The comments for a class should start with a brief description of the role of the class in your program.</li>

 <li>Every non-private method you write must be Javadoc’d and the @param tag included for every method parameter. The format for an @param tag is @param &lt;name of parameter as written in method header&gt; &lt;description of parameter&gt;. If the method has a non-void return type, include the @return tag which should have a simple description of what the method returns, semantically.</li>

</ol>


