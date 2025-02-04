# Objective-C: Incorrect `self` Usage in Initializer

This repository demonstrates a common, yet subtle, error in Objective-C: improper use of `self` within an initializer method.  Accessing instance variables before they've been properly initialized within `init` (or other designated initializers) can result in unexpected behavior, including null pointer exceptions or crashes.

## The Bug
The `bug.m` file contains code that attempts to access an instance variable (`myString`) before it has been assigned a value.  This leads to undefined behavior.

## The Solution
The `bugSolution.m` file shows the corrected version.  It properly initializes the instance variable *before* attempting to use it, ensuring predictable and correct program execution.

## How to Reproduce
1. Clone this repository.
2. Open the project in Xcode.
3. Run the code. Observe the different output between the buggy and corrected versions.