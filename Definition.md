# Definitionen

| _**Up & Going 1**_ |
|---|

_**Statement**_
> **Befehl, Kommando**
```javascript
a = b * 2;
```

_**Expression**_
> **Ausdruck**
> - **2** is a literal value expression
> - **b** is a variable expression
> - **b * 2** is an arithmetic expression
> - **a = b * 2** is an assignment expression

_**Interpreting**_
> Ausführen von Code Zeile für Zeile von oben nach unten

_**Compiling**_
> Erst wird der Code kompiliert, dann interpretiert

_**Coercion**_
> Typumwandlung

_**Iteration**_
> Jedesmal wenn der Codeblock in einer Schleife ausgeführt wird, ist es eine Iteration

_**Parameters**_
> Aliases die der Funktion übergeben werden
```javascript
function myfunc(a,b) {}
```

_**Arguments**_
> Werte mit denen die Funktion aufgerufen wird
```javascript
myfunc(1,2);
```

| _**Up & Going 2**_ |
|---|

FUNKTIONEN ALS WERTE
function foo() {}
foo ist eine Variable im äußeren umschließenden Scope mit einer Referenz auf die deklarierte Funktion
-> Funktionen an sich sind Werte wie 42 oder [1,2,3]
D.h. Funktionen können Variablen zugewisen werden, als Argumente verwendet werden oder von anderen Funktionen zurückgegeben werden

As such, a function value should be thought of as an expression, much like any other value or expression.

IMMEDIATELY INVOKED FUNCTION EXPRESSIONS (IIFEs)
(function iife() {
console.log("Hi!");
})();
// "Hi!"

Because an IIFE is just a function, and functions create variable scope, using an IIFE in this fashion is often used to declare variables that won't affect the surrounding code outside the IIFE

var x = (function returnedNumber() {
return 42;
})();

x; // 42

returnedNumber wird ausgeführt und weist x den Wert 42 zu

CLOSURE
