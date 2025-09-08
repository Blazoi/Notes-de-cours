# Guide d'étude C#

## Variables

Types **valeurs** : Donnée sauvegardée dans le stack.
types **références** : Pointeur sauvegardée dans le stack, donnée sauvegardée dans le heap.


### 🔹 Value Types

| Type    | Size (bytes) | Range | Example |
|---------|--------------|-------|---------|
| `byte`  | 1 | 0 to 255 | `byte b = 200;` |
| `sbyte` | 1 | -128 to 127 | `sbyte sb = -50;` |
| `short` | 2 | -32,768 to 32,767 | `short s = -300;` |
| `ushort`| 2 | 0 to 65,535 | `ushort us = 60000;` |
| `int`   | 4 | -2B to 2B| `int age = 25;` |
| `uint`  | 4 | 0 to 4B | `uint id = 1000;` |
| `long`  | 8 | -9Q to 9Q | `long l = 1000000000;` |
| `ulong` | 8 | 0 to 18Q | `ulong ul = 9999999999;` |
|**Décimaux**|
| `float` | 4 | ~±1.5e−45 to ±3.4e38 (7 digits) | `float f = 3.14f;` |
| `double`| 8 | ~±5.0e−324 to ±1.7e308 (15–16 digits) | `double d = 3.14159;` |
| `decimal`| 16 | ±1.0e−28 to ±7.9e28 (28–29 digits) | `decimal m = 19.99m;` |
|**Autres**|
| `char`  | 2 | Unicode (U+0000 to U+FFFF) | `char c = 'A';` |
| `bool`  | 1 | `true` or `false` | `bool isActive = true;` |

## 🔹 Reference Types

| Type    | Size | Description | Example |
|---------|------|-------------|---------|
| `string` | varies | Immutable sequence of chars | `string name = "Alice";` |
| `object` | 4/8 | Base type of all types | `object o = 42;` |
| `dynamic` | varies | Type resolved at runtime | `dynamic d = "text";` |

---

## 🔹 Special Types

| Type    | Description | Example |
|---------|-------------|---------|
| `enum`  | Named constants | `enum Days { Mon, Tue, Wed }` |
| `struct`| Lightweigh | `struct Point { int X; int Y; }` |
| `Nullable<T>` | Value type that can be `null` | `int? score = null;` |
## Fonctions
### Contrôle de flow
Contrôle de l'ordre d'exécution du programme



# C# Control Flow

| Concept | Définition | Syntaxe |
|-------------------|------------------|--------|
| `if` / `else`     | Run code if condition true, else otherwise. | `if (condition) { } else { }` |
| `switch`          | Pick one block from many cases. | `switch (value) { case ...: break; }` |
| `for`             | Loop with counter. | `for (init; condition; step) { }` |
| `while`           | Loop while condition true. | `while (condition) { }` |
| `do...while`      | Loop runs at least once. | `do { } while (condition);` |
| `foreach`         | Loop through collection items. | `foreach (var item in collection) { }` |
| `break`           | Exit loop or switch. | `break;` |
| `continue`        | Skip to next loop step. | `continue;` |
| `return`          | Exit method, optionally give value. | `return value;` |

## Méthodes
# C# Methods

| Feature             | Short Definition | Syntax |
|---------------------|-----------------|--------|
| Method declaration  | Define reusable code block. | `returnType MethodName(params) { }` |
| Parameters          | Inputs for a method. | `void Greet(string name) { }` |
| Return value        | Sends a value back. | `int Add(int a, int b) { return a+b; }` |
| Overloading         | Same name, different parameters. | `int Square(int x) { }` <br> `double Square(double x) { }` |
| `ref` / `out`       | Pass arguments by reference. | `void Double(ref int n) { }` <br> `void GetValue(out int n) { }` |
| Optional parameters | Parameters with default values. | `void Print(string msg="Hello") { }` |
| Static methods      | Belong to class, not object. | `static void Info() { }` |

##


## OOP


### Attributs 
`public Point Centre { get; private set }`


|||
|-|-
`static` : Class or method can be called but not <br> instantiated| `Calc.cube(x)` returns x^3
`abstract` : Can instantiate a subclass <br>but not itself|:x: `Shape s = new Shape()` <br> :white_check_mark: `Shape s = new Circle()`
**Static variable** <br> Owned by the class and not the objects <br> Example: How many times a thing <br> was used today|`static int compteur`


## Data Structures

|Data Structures ||
|-|-|
|**Stack**| **LIFA** (Last In First Out)
|**Queue**|**FIFO** (First In First Out)
|**List**|