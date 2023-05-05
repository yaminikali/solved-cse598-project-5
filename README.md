Download Link: https://assignmentchef.com/product/solved-cse598-project-5
<br>
The aim of this assignment is to make sure that you have read the slides and the text and have understood the concepts covered in the lectures and in the text, including big data management and analytics, Hadoop, recommendation system, ontology, semantic Web, and cloud computing. By the end of the assignment, you should have a good understanding of the concepts and have applied these concepts in developing operational programs.

<h1>Practice Exercises</h1>

<ol>

 <li>Reading: Textbook chapter 11, and lecture slides.</li>

 <li>Answer the multiple choice questions in the Exercises and Projects part in chapter 11. Study the material covered in these questions can help you to prepare for the class exercises, quizzes, and the exam.</li>

 <li>Study for the short answer questions in the Exercises and Projects part in chapter 11. Make sure that you understand these questions and can briefly answer these questions. Study the material covered in these questions can help you to prepare for the exam and understand the homework assignment.</li>

 <li>Study Textbook section 11.3 on Big Data Processing and 14.8 on Hadoop. Make sure you understand how the program works. Implement the program on the Hadoop environment that you have installed.</li>

 <li>Use VIPLE to calculate the average of 1, 2, 3, …, 2000 using a single thread and using four parallel threads.</li>

 <li>Hadoop Exercise. Install Hadoop on a Linux computer.

  <ol start="11">

   <li>Modify the WordCount program given in the lecture slides or Textbook section 11.2. You must add time stamps at the beginning and the end of the Map part of the program, and at the beginning and the end of the Reduce part of the program, so that you can measure the time consumed in each part of computation. You must add print statements to print the four time stamps and the time consumed in each part as your program output. The program must also print the number of words counted.</li>

   <li>Create a text file as the input file to test the WordCount program in your Hadoop environment. Instruction for testing your program.</li>

  </ol></li>

</ol>

<strong> </strong>




<h1>Assignment Questions</h1>




There are two questions in this assignment. You choose one question of the two questions to implement. If you implement both questions, we will grade question 1 only.

<ol>

 <li>In this assignment, you will create a Web application platform that allows user to perform automated parallel computing that mimics the Hadoop process. A sample user interface is given in Figure 1.</li>

</ol>

<table width="361">

 <tbody>

  <tr>

   <td width="17"></td>

   <td width="344">


    <table width="341">

     <tbody>

      <tr>

       <td width="341"><strong>Web Application Performing Automated MapReduce</strong>

        <table width="177">

         <tbody>

          <tr>

           <td width="106">Choose Data File</td>

           <td width="9"> </td>

           <td width="63">Upload</td>

          </tr>

         </tbody>

        </table>StatusChoose N, the number of parallel threads. N &gt;= 1

        <table width="42">

         <tbody>

          <tr>

           <td width="42">4</td>

          </tr>

         </tbody>

        </table>Provide the Web service address for Map function

        <table width="316">

         <tbody>

          <tr>

           <td width="316">http://</td>

          </tr>

         </tbody>

        </table>Provide the Web service address for Reduce function

        <table width="316">

         <tbody>

          <tr>

           <td width="316">http://</td>

          </tr>

         </tbody>

        </table>Provide the Web service address for Combiner function

        <table width="316">

         <tbody>

          <tr>

           <td width="316">http://</td>

          </tr>

          <tr>

           <td width="316">Perform MapReduce Computation</td>

          </tr>

         </tbody>

        </table>Display Results</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

Provide different

Web

services to perform different parallel computing functions




Figure 1. Web application GUI with Web service calls

The Web application consists of the following components.

<ul>

 <li>GUI component and the connection to the other components. [10 points]</li>

 <li>NameNode: It splits the uploaded Data File into N subsets and provides a subset to each</li>

</ul>

TaskTracker.                                                                                                                   [10 points]

<ul>

 <li>TaskTracker: It consists of Map function and a Reduce function.</li>

 <li>Map function: It converts data from subset of Data File into Key-value pairs, based on the functionality requirement.           [10 points]</li>

 <li>Reduce function: It reduces the key-value pairs into one or smaller number of key-value pairs, based on the functionality requirement. [10 points]</li>

 <li>Combiner: It synchronizes and combines the results from all the Reduce functions and put the final results.      [10 points]</li>

</ul>

In this assignment, you will implement the Word Count application. It counts the number of occurrences each word in the uploaded Data File. The components and the computation process is illustrated in Figure 2.

Figure 2. Map and Reduce execution with N = 2

You can implement the Web application either as an ASP .Net Website application, HTML5 application, or MVC Web application on localhost. For the components used in the application, you can also choose to implement this application in one of the following options.

<strong>Option 1</strong>: You implement the Web application as a service-oriented application. You implement Map, Reduce, and Combiner as Web services (either RESTful services or WSDL services). You make parallel calls to the services for each Map and Reduce, and you configure or assume that a new instance of service will be created for each call, and thus the tasks are done in parallel. The sample GUI given in Figure 1 is for Option 1.

<strong>Option 2</strong>: You implement the Web application without calling Web services. You implement Map, Reduce, and Combiner as local components. You must use multithreading techniques (read Text Chapter 2) to run the Map and Reduce functions in parallel. In this option, a large Data file, with at least 5000 words must be used. The execution times for single thread execution and for multithread execution must be reported. A sample GUI for Option 2 is given Figure 3.

<table width="286">

 <tbody>

  <tr>

   <td width="286"><strong>Web Application Performing Automated MapReduce</strong>

    <table width="149">

     <tbody>

      <tr>

       <td width="89">Choose Data File</td>

       <td width="7"> </td>

       <td width="53">Upload</td>

      </tr>

     </tbody>

    </table>Status Choose the number of parallel threads

    <table width="35">

     <tbody>

      <tr>

       <td width="1"> </td>

       <td width="35">4</td>

       <td width="229"> </td>

      </tr>

      <tr>

       <td colspan="3" width="265">Perform MapReduce Computation</td>

      </tr>

      <tr>

       <td width="1"></td>

       <td width="33"></td>

       <td width="43"></td>

      </tr>

     </tbody>

    </table>Display ResultsSingle thread execution time:Multithread execution time</td>

  </tr>

 </tbody>

</table>

Figure 3. Web application GUI without Web service calls

<ol start="2">

 <li>In this question, you will implement the same function as described in question 1. However, you will use VIPLE, to simulate the Hadoop process, instead of using a web application. Figure 4 and Figure 5 give a sample application, where string’s characters are counted. It is not a realistic application that improves the performance of computing. The main purpose of this example is to show how you can automatically start N threads to perform parallel computing, where N can be entered from the keyboard. In your assignment question, you will count words, just like described in question 1, instead of counting characters.</li>

</ol>

The key idea of generating N threads based on the input N is to use event-driven programming. The Custom Activity NameNode will generate an event output (circular output port in Figure 5), instead of a data output (triangular port in Figure 5). Once the event output port is used, it will trigger an event through the Custom Event activity in the Main Diagram every time it is executed. As can be seen in Figure 5, there is no computation inside the activity. Its purpose is to trigger a new thread.

In the Main diagram, the NameNode is placed in a loop, which will be called N times. Each time will trigger a new thread through the Custom Event activity. The main computations are performed in these parallel threads. The loop will be executed sequentially. Since we do not have much computation in the activity, it will be iterated and the parallel threads are generated without delay.

You tasks in the option are as follows. You can make use of the given code as your starting point.

<ul>

 <li>Write a service, a code activity, or a custom activity to load the text in a text file into variable</li>

</ul>

InputData. Use it to replace the Data activity that provided the Input data.                   [10 points]

<ul>

 <li>Write a service, a code activity, or a custom activity to counts number of appearances for each word in the InputData. [10 points]</li>

 <li>In the main diagram, you must automatically create the threads based on the input N, as shown in Figures 4 and 5. [10 points]</li>

 <li>Write a code activity to save the result (the number of words) into a text file called</li>

</ul>

FileForOutput.txt.                                                                                                           [10 points]

<ul>

 <li>Make sure that your program can execute correctly even if the data length is not a multiple of N. In the given example program in Figure 4, this check is not performed to keep the program</li>

</ul>

small.                                                                                                                               [10 points]




Figure 4. The Main diagram of the automated parallel threads example




Figure 5. The Custom Activity diagram of the automated parallel threads example

Figure 6 shows the execution output when the input number N is 2, 4, and 6, respectively.




Figure 6. The output when the input number N is 2, 4, and 6, respectively.




Figure 7. Sample application that reads a text file into a string.




Figure 8. The CodeActivity reading a text file into a string.


