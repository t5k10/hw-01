# otus-cpp-elementary.
Each C++ expression (an operator with its operands, a literal, a variable name, etc.) is characterized by two 
independent properties: a type and a value category. Each expression has some non-reference type, and each 
expression belongs to exactly one of the three primary value categories: prvalue, xvalue, and lvalue.
    - a glvalue (“generalized” lvalue) is an expression whose evaluation determines the identity of an object or 
        function;
    - a prvalue (“pure” rvalue) is an expression whose evaluation 
        computes the value of an operand of a built-in operator (such prvalue has no result object), or 
        initializes an object (such prvalue is said to have a result object). 
        The result object may be a variable, an object created by new-expression, a temporary created by temporary 
        materialization, or a member thereof. Note that non-void discarded expressions have a result object 
        (the materialized temporary). Also, every class and array prvalue has a result object except when it is 
        the operand of decltype;
    - an xvalue (an “eXpiring” value) is a glvalue that denotes an object whose resources can be reused;
    - an lvalue (so-called, historically, because lvalues could appear on the left-hand side of an assignment 
        expression) is a glvalue that is not an xvalue;
    - an rvalue (so-called, historically, because rvalues could appear on the right-hand side of an assignment 
        expression) is a prvalue or an xvalue.
Note: this taxonomy went through significant changes with past C++ standard revisions,see History below for details.
