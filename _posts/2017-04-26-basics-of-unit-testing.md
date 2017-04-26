---
layout: post
title: Basics of Unit Testing
pulished: true
---

### What is Unit Testing?
Unit testing is a way of testing software where individual pieces of a system are tested. The purpose of unit testing is to validate that each individual piece operates as designed. A unit should be the smallest testable part of a system. Usually a unit will have 
very few inputs and outputs.

The most efficient way of doing unit testing is to use a unit testing framework. A few popular ones for .NET are MSTest (comes with Visual Studio), NUnit, and XUnit. A few popular ones for JavaScript are jasmine and mocha. Unit testing frameworks will help you create and run the tests.

### .NET Unit Testing
Visual Studio has MSTest built in for unit testing. To perform unit testing you'll want to add a unit testing project to your solution, create unit test class(es), create unit test method(s), build, and run the tests.

1. Create the Unit Testing Project
* File -> Add -> New Project
* Expand Installed -> Expand Visual C# -> Choose Test
* Select Unit Test Project from the list of templates
* Enter a name and click OK
* In the newly added Unit Test project add a reference to the project that is to be tested
2. Create the Unit Testing Class(es)
* Based on the example Unit Test class that was added by default, add a class to the project that mirrors the name of the classes you want to test in your software project with a suffix of "Tests'. For example, to test the Bank class in your project, you will add a class to the Unit Test project named "BankTests". Also, you'll want to add a using statment to the top of the class so you can access the methods to be tested in your software project (e.g. Using BankAccountNS;) The class will look something like this:
```
using System;  
using Microsoft.VisualStudio.TestTools.UnitTesting;  
using BankAccountNS;
namespace BankTests  
{  
    [TestClass]  
    public class BankAccountTests  
    {  
        [TestMethod]  
        public void TestMethod1()  
        {  
        }  
    }  
}
```
3. Create the Unit Testing Method(s)
* Analyze the method you want to test and determine the behaviors that need to be checked. Each of the test methods must: be decorated with [TestMethod] attribute, return void, and have zero parameters. Here is an example method that can be added to the BankAccountTests class:
```
[TestMethod]  
public void Debit_WithValidAmount_UpdatesBalance()  
{  
    // arrange  
    double beginningBalance = 11.99;  
    double debitAmount = 4.55;  
    double expected = 7.44;  
    BankAccount account = new BankAccount("Mr. Bryan Walton", beginningBalance);  
    // act  
    account.Debit(debitAmount);  
    // assert  
    double actual = account.Balance;  
    Assert.AreEqual(expected, actual, 0.001, "Account not debited correctly");  
}
```
4. Build and Run the Tests
* Build > Build Solution
* Choose Run All to run the test
* If a test fails then the test method is moved to the Failed Tests group in Test Explorer. You can select it to view the details at the bottom of the window.

For more information on how to create and run unit tests in Visual studio check out this MSDN page: <a href="https://msdn.microsoft.com/en-us/library/ms182532.aspx">Walkthrough: Creating and Running Unit Tests for Managed Code</a>.

### JavaScript Unit Testing
The Jasmine and Mocha frameworks are very similar in many ways. For this example we'll use the Mocha framework.
1. Install mocha
* Open a terminal and navigate to your project directory
* Install globally: `# npm install --global mocha` OR install for project: `# npm install --save-dev mocha`
* `# mkdir test`
* `# vi test/test.js` and add the following code, save, and close the file
```
var assert = require('assert');
describe('Array', function() {
  describe('#indexOf()', function() {
    it('should return -1 when the value is not present', function() {
      assert.equal(-1, [1,2,3].indexOf(4));
    });
  });
});
```
* `# ./node_modules/mocha/bin/mocha`
* `# vi package.json` and add the following text to set up a test script
```
"scripts": {
    "test": "mocha"
  }
```
* run the tests with #npm test
* To perform various tests and for more information check out the <a href="https://mochajs.org/#table-of-contents">MochaJS Table of Contents</a>.

### What to do Next
A single test doesn't finish your job of testing a system. Try to think about all possible tests you could perofrm. Unit tests should primarily look at two things: a succesful path and a failure path. You will want to know what happens when tests fail and what happens when tests succeed. Also, it may be helpful to write the tests as you go. You can refactor your methods into small testable units and create the unit tests as you are developing each section of code.
