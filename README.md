# CplusplusUnittestEngine
test engine for C++, inspiered by python unittests<br>

created with C++20, the function feedback prints the unicode character ● , your console needs to support this or change it in the header.<br>

example:<br>

//create an testcase object;<br>
TestCase S;<br>

define arguments for the function to be tested and the solution, first argument of S.asser is a name for the test, then the solution and then the output of the function to be tested<br>
vector<int> positions = {1,3,1,4,2,3,5,4};<br>
S.asser("test1",6,solution(5,positions));<br>
<br>
positions = {1,3};<br>
S.asser("test2",-1,solution(3,positions));<br>
<br>
positions = {1,1};<br>
S.asser("test3",-1,solution(3,positions));<br>

positions = {1,1};<br>
S.asser("test1",0,solution(1,positions));<br>
<br>
//call this to get the summary below <br>
S.feedback();<br>
<br>
output--<br>
<br>
the dots below are green or red depending on test outcome!<br>
● ● ● ● <br>
test1 SUCCESS , time in miliseconds for this test : 0<br>
test2 SUCCESS , time in miliseconds for this test : 0<br>
test3 FAILED ,expected: 0 actual: -1, time in miliseconds for this test : 0<br>
test1 SUCCESS , time in miliseconds for this test : 0<br>
16 microsseconds total time <br>
0 milliseconds total time  <br>
<br>

it also catches errors during test<br>


the timer makes no sense... will update in future
