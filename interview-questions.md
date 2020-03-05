# General Knowledge Questions:

Please write your answers in the code blocks.

**NOTICE:** Some (but not all) questions may be easier to answer with code or pseudocode. As an example, all of these are an acceptable answer to the question "How do you iterate a variable in PHP?"

```
$number++;
```

```
num = num + 1
```

```
variable "num" now equals "num" + 1
```

-----------------------------------------------------------------------

## Section: PHP

1. How do you get information from a form that is submitted using the "get" method?

```
$information = $_GET['information'];
```

2. What is the correct way to create a function in PHP?

```
function a_function(){
    //some code here
    
}
```

3. Name a method to output an array?

```
var_dump()
```

4. Which operator is used to check if two values are equal and of same data type?

```
===
```

5. Which superglobal variable holds information about headers, paths, and script locations?

```
$_SERVER
```

6. Explain how `static function` works in PHP class methods.

```
Declaring the methods of a class as static makes the method accessible without having to instantiate the class.
Therefore one can call a static method without having to create an instance of the method's class.
```


7. What is the commonly used library for database connections?

```
PHP Data Objects (PDO)
```

8. What is the commonly used library for making requests?

```
Guzzle
```

9. What is PHP function strlen?

```
The function strlen takes a string as a parameter and returns the length of that string.
```


## Section: SQL

For the below questions, assume you are using this table (named `Persons`):

| Id | FirstName | LastName  |
|----|-----------|-----------|
| 1  | Peter     | Jackson   |
| 2  | Adam      | Savage    |
| 3  | Linus     | Sebastian |
| 4  | Brent     | Spiner    |
| 5  | Doom      | Guy       |

1. How would you select just the first record and only the column `FirstName`?

```
SELECT Firstname FROM Persons LIMIT 1;
```

2. How would you select all the records where the `FirstName` is "Peter" and the `LastName` is "Jackson"?

```
SELECT * FROM Persons WHERE Firstname='Peter' AND Lastname='Jackson';
```

3. How would you select all the records where the `LastName` starts with an "s"?

```
SELECT * FROM Persons WHERE Lastname Like 's%';
```

4. How would you select all the records where the `FirstName` is alphabetically between "Brent" and "Linus"?

```
SELECT * FROM Persons WHERE Firstname >= 'Brent' AND Firstname <= 'Linus';
```

5. How would you insert the name "David Tennant"?

```
INSERT INTO 
Persons (Firstname, Lastname)
VALUES 
        ('David', 'Tennant');
```

6. How would you change all the records where the `FirstName` is equal to "Peter" into "Samuel"?

```
UPDATE Persons
SET Firstname = 'Samuel'
WHERE Firstname = 'Peter';
```

7. How would you delete the records where the `LastName` is "Sebastian"?

```
DELETE FROM Persons WHERE Lastname = 'Sebastian';
```

8. How would you get the number of records in the `Persons` table?

```
SELECT COUNT(*) FROM Persons;
```

9. Give an example of how would you join 2 related tables together?

```
Table: Persons_Email
| Id | FirstName | LastName  | Email
|----|-----------|-----------|-------
| 1  | Peter     | Jackson   | peter@gmail.com
| 2  | Adam      | Savage    | adam@gmail.com
| 3  | Linus     | Sebastian | linus@gmail.com
| 4  | Brent     | Spiner    | brent@gmail.com
| 5  | Doom      | Guy       | doom@gmail.com

Table: Persons_Contact_Info
| Id | FirstName | LastName  | Phone
|----|-----------|-----------|-------
| 1  | Doom      | Guy       | 555-555-5555
| 2  | Peter     | Jackson   | 111-111-1111
| 3  | Brent     | Spiner    | 444-444-4444
| 4  | Linus     | Sebastian | 333-333-3333
| 5  | Adam      | Savage    | 222-222-2222



We could combine these two tables together in order to make it easier to read the phone and email tied to each person.

SELECT Persons_Contact_Info.Id, Persons_Contact_Info.FirstName, Persons_Contact_Info.LastName, Persons_Contact_Info.Phone, Persons_Email.Email
FROM Persons_Email
JOIN Persons_Contact_Info ON Persons_Contact_Info.Firstname = Persons_Email.Firstname WHERE Persons_Contact_Info.Lastname = Persons_Email.Lastname;
```


## Section: Vanilla Javascript

1. How do you create a function in JavaScript?

```
function aFunction() {
    
}
```

2. How do you call a function named "myFunction"?

```
myFunction();
```

4. How to write an IF statement for executing some code if "i" is NOT equal to 5?

```
if (i!=5) {
    //some code
}
```

5. How does a WHILE loop start?

```
while (someConditionHere) {
    //code if condition met
}//end while loop
```

6. How does a FOR loop start?

```
for (let index = 0; index < arrayToIterateThrough.length; index++) {
    //some code here
    
}//end loop
```

7. How do you round the number 7.25, to the nearest integer?

```
Math.round(7.25)
```

8. What will the following code return: Boolean(10 > 9)

```
true
```

## Section: jQuery

1. Can jQuery animate() method can be used to animate ANY CSS property?

```
No
```

2. Which jQuery method is used to hide selected elements?

```
hide()
```

3. Which jQuery method is used to perform an asynchronous HTTP request?

```
ajax()
```

4. Look at the following selector: $("div p"). What does it select?

```
It selects all <p> that are descendents of <div>
```


## Section: React

1. What is JSX?

```
JSX is a syntax extension to Javascript, used to create React elements for the UI of React applications, similar in appearance to, but more powerful and versatile than a traditional template language, you can use any valid JavaScript expression within the curly braces of JSX. After being compiled JSX expressions become regular Javascript function calls and evaluate to objects meaning that JSX can be used inside if statements, for loops, assigned to variables, accepted as arguments and returned from functions.
```

2. What triggers a render cycle?

```
A change in component state.
```

3. What is a React Hook?

```
A React Hook is a function that lets you use or "hook into" React state and other features directly from function components without having to write a class. The built-in useState hook for instance lets you add state to your React components. 
```

4. Which method in a React Component should you override to stop the component from updating?

```
shouldComponentUpdate()
```

5. Which method in a React Component is called after the component is rendered for the first time?

```
componentDidMount()
```

6. What happens when you call setState() inside render() method?

```
Calling setState() inside the render() method makes components susceptible to producing infinite loops. The render() function should not modify component state, but should instead be left "pure".
```

