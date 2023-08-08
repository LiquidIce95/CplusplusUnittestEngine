# CplusplusUnittestEngine
test engine for C++, inspiered by python unittests

created with C++20, the function feedback prints the unicode character ● , your console needs to support this or change it in the header.

example:

//create an testcase object;
TestCase S;

define arguments for the function to be tested and the solution, first argument of S.asser is a name for the test, then the solution and then the output of the function to be tested
vector<int> positions = {1,3,1,4,2,3,5,4};
S.asser("test1",6,solution(5,positions));

positions = {1,3};
S.asser("test2",-1,solution(3,positions));

positions = {1,1};
S.asser("test3",-1,solution(3,positions));

positions = {1,1};
S.asser("test1",0,solution(1,positions));

//call this to get the summary below 
S.feedback();

output--

the dots below are green or red depending on test outcome!
● ● ● ● 
test1 SUCCESS , time in miliseconds for this test : 0
test2 SUCCESS , time in miliseconds for this test : 0
test3 FAILED ,expected: 0 actual: -1, time in miliseconds for this test : 0
test1 SUCCESS , time in miliseconds for this test : 0
16 microsseconds total time 
0 milliseconds total time  


it also catches errors during test
