---
title: "Mathematical Expression Evaluator"
eventname: "Recursive calculator program and demo of the Shunting Yard Algorithm"
date: 2020-10-07
publishDate: 2020-10-07
author: "Rayyan Shaik & Andrew Diab"
draft: false
images: []
tags: ["Java", "Algorithm", "Collaboration", "Featured"]
projects: ["Programming Projects"]
---

### Description
This repository features 2 programs that can solve mathematical expressions. Both projects were planned and thought out before writing, and my partner, Andrew Diab, and I each wrote one implementation. The first one, under the subdirectory `/Dijkstra` was completed by Andrew Diab - this implements the Shunting-Yard Algorithm by Edsger Dijkstra, and the simpleSolve() method created by myself. I created the second implementation found under the subdirectory `Recursive`. This program contains a class which can solve unordered mathematical expressions folling PEMDAS (no brackets or parentheses) under the method `simpleSolve()`. Within this same class, the `solve()` method "searches" for parenthetical expressions and recursively solves the general equation by calling `simpleSolve()` multiple times.

### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/Calculator)

### What were my goals with this project?
* Design/write under an efficient workflow with my partner
* Create an expression solver without external resources
* Make the driver code relatively easy to use
* Have the solution be as efficient as possible
* Accounts for a wide variety of statements.  Allows for negative numbers, PEMDAS, and is precise.

### Project Images
{{< figure src="../../images/calculator1.jpg" alt="calculator1.jpg" width=600 >}}
---

### Driver code
{{< highlight java >}}
e = new Equation("("+input+")");
System.out.println("Output: " + e.solve());
{{< /highlight >}}

### Testing outputs
{{< highlight java >}}
Your expression (+ - / * ^ !): 
>>> (-2)((((2+2)*3/9-4)*3-1) + (3) + -1^3)/9 + (-10 - (-3))
---------------------
Evaluating: ((-2)((((2+2)*3/9-4)*3-1) + (3) + -1^3)/9 + (-10 - (-3))) >>>
---------------------
Output: -5.444444444444445
Calculation time (ms): 2
Would you like to exit? (y/n) :
>>> yes
{{< /highlight >}}

### Recursive solve() code
{{< highlight java >}}
public double solve() {
        if (this.equation.contains("(")) {
            /* This 'portion' of the method, recursively breaks down parenthetical statements
            into simple expressions. It then takes the outputs of all the
            parenthetical statements and calculates the rest of the expression using
            simpleSolve() */
            
            int parenthesisCount = 0;
            char[] charEquation = this.equation.toCharArray();
            String finalEquation = "";
            int index1 = -1;
            int index2 = -1;

            for (int i=0; i < charEquation.length; i++) {
                if (charEquation[i] == '(') {
                    if (index1 == -1) {
                        index1 = i;
                    }
                    parenthesisCount ++;
                }
                else if (charEquation[i] == ')') {
                    parenthesisCount --;
                    /* When the parenthesis count is at 0 on a closed parenthesis
                    that means that a parenthetical expression has ended. This is to
                    be parsed, and solved in a new Equation object */
                    if (parenthesisCount == 0) {
                        index2 = i;  
                        // Recursive statement
                        finalEquation += new Equation(this.equation.substring(index1, index2+1), this.printOperations).solve();  
                        index1 = -1;
                    }
                }
                else if (parenthesisCount == 0) {
                    finalEquation += charEquation[i];
                }
            }
            return simpleSolve(finalEquation);
        }
        // If there are no parentheses, "order" does not matter
        else {
            return simpleSolve(this.equation);
        }
    }
{{< /highlight >}}