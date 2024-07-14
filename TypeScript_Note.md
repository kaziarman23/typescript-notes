TypeScript is a devlopment tool for JavaScript.When we write rew javaScript it help us to make our code more clean.

## How to install TypeScript:

1. Open your commend line and type a commend that will install the type Script globally.
        "npm install -g typescript"

2. To run any commend we have to write (tsc) first and this is a syntex.

3. To check you'r depandanci is install we have this commend and it will show you'r downloaded version in you file.
    "tsc -v"

4. we can config typeScript my installing ts.config file.
        "tsc -init"
        <!-- by the help of this config file we can select the compiler file(rootDir) and the output file(outDir) -->


## Convert in JS:

1. we can't see the result/output in the typeScript.We have to convert it in a javaScript and then we have to see the output of our code.The commend of converting typeScript to javaScript is:
   "tsc TS_File_Name"

2. or we can set an autoCompiler by giving this commend. And it will auto compile
        "tsc -w"

   ## importent part
3. usually type script use module commonJs and that's not support es6(import export stuff's) that's why we have to change some configaretion in the ts.config file. The change's are in:
        file name : ts.config 
                target: es6,
                module: es2015  
        and where the html file is conacting with the javaScript file by the script  tag, over there you have to add a attribute.
                type="module"
        when you are importing something we have to declar that file as a JS file.

## Functions in TypeScript:

1.  we need to set Data type in the function because it's a good practice.

2.  In typeScript we have to declare what kind of function and peramitar's are we taking.

        function addTwo(num: Number):Number {
                return num + 2
        }

        console.log(addTwo(8))


        // In the peramitar we declare the type of peramitar by saying it's Data type.

        // In this function after the parenthesis  we declare the type of function by saying it's Data type.

        // If the function is not going to return anything, we need to set void Data type declaretion in that funcion.

        // When we are not going to return anything and throw a error, we need to set naver Data type declaretion in that funcion. It's commonly used in handling Error function.

                function handleError(errormsg: string): naver{
                        throw new Error(errormsg)
                }

## Passing obj in the function:

1.  Passing obj in the function is requred some syntex:

        function createObj():{Name: string, price: number}{
                return {Name: ReactJs, price: 599}
        }

        createObj() //output: {Name: ReactJs, price: 599}



        // In this function we set an obj as a Data type after the parenthesis and before the definition

2.  Passing obj in the function peramitar is requred some syntex also:

        //have to use Alises to pass the obj in the peramitar

## Type Aliases in functions:

1.  we can set obj property in the function peramiter as many as we want with the help of Type Aliases :

        type Number = {
                ex: number;
                Current: number;
        }

        function printNumber(details: Number){
                console.log("my ex number is:"+ details.ex)
                console.log("my Current number is:"+ details.Current)
        }

        printNumber({ex:123, Current:456})

## readonly, optional, Interfaces:

1. readonly: Marks a property or parameter as read-only, meaning its value cannot be changed after initialization. Use the readonly keyword before the property name during declaration.

2. optional: Indicates that a property in an interface or object literal might be absent.Use a question mark (?) after the property name during declaration.

3. Interfaces: Interfaces in TypeScript are powerful tools for defining the structure of objects. They act like blueprints or contracts that specify the properties and methods that an object must have.

## Union:

1. In TypeScript, union types allow you to specify that a variable or function parameter can hold more than one data type. It's like saying "this value can be either this type or that type." The pipe symbol | is used to separate the allowed types in a union.

2. TypeScript won't always know the exact type within a union at compile time. You might need to use type guards (like conditional statements) to narrow down the type before using specific methods.

## Tuples:

1. Tuples: Typed Arrays for Structured Data. In TypeScript, tuples provide a way to represent an ordered list of elements with specific types

## private & public:

1. Use public for properties that need to be directly accessed and modified by other parts of your code.

2. Use private for properties that represent internal state or data that should be managed within the class and accessed/modified through public methods.

## getters & setters:

<Getters>:

1. Defined using the get keyword followed by the property name.
2. Act as accessor methods, allowing you to retrieve the value of a private property.
3. Can perform additional logic before returning the value, such as formatting or calculations.

<Setters>:

1. Defined using the set keyword followed by the property name and an argument representing the new value.
2. Act as mutator methods, enabling you to modify the value of a private property.
3. Can implement validation checks on the new value before assigning it to the property.
4. Can't directly return a value (unlike regular methods).

## Abstract Class:

learn from Ai

আচ্ছা, চলো আজকে একটা মজার খেলনা তৈরি করা যাক! কিন্তু এটা একটু বিশেষ খেলনা, এটা অন্য খেলনাগুলোর জন্য নির্দেশাবলী দেয়!

খেলনাগুলো সব ভাইবোন। এই বিশেষ খেলনাটা বড় ভাইয়ের মতো, সে ছোট ভাইবোনদেরকে কিভাবে খেলতে হবে সেটা শেখায়। কিন্তু নিজে খেলে না।

এই বিশেষ খেলনাটাকেই আমরা TypeScript-এ বলি abstract class ।

নিজে খেলে না: abstract class থেকে সরাসর কোনো কিছু তৈরি করা যায় না (যেমনটা আমরা গাড়ি বা পুতুল তৈরি করি)।

1. নির্দেশাবলী দেয়: এটা ছোট ভাইবোনদেরকে (অর্থাৎ, subclass বা সাবক্লাস) নির্দেশ দেয় কিভাবে খেলতে হবে। এই নির্দেশাবলী হলো abstract methods যা বড় ভাই তো বলে দেয় কিন্তু নিজে করে না।

2. ছোট ভাইবোনরা শেখে: subclass-গুলো এই abstract methods গুলোকে শেখে নেয় আর নিজের মতো করে খেলে (অর্থাৎ, সেগুলো নিজের কোড লিখে abstract methods গুলোকে বাস্তবায়ন করে)। এর ফলে সব খেলনা (subclass) একই রকমের কিছু জিনিস (shared functionality) করতে পারে কিন্তু নিজের মতো করেও খেলতে পারে (polymorphism)।

3. উদাহরণ:

কল্পনা করো আমাদের একটা গোল (circle) খেলনা আছে এবং একটা বর্গাকার (square) খেলনা আছে।
কিন্তু আমাদের আছে আরো একটা খেলনা "আকার" (shape) যা নিজে কোনো আকারের না কিন্তু গোল এবং বর্গাকার খেলনা দুটিকে নির্দেশ দেয় যে তাদের একটা क्षेत्रফল (kṣétraphól) নামের কিছু থাকতে হবে।

## Generics:

1. Generics are a powerful feature in TypeScript that allow you to write code that can work with different data types without sacrificing type safety.

## Narrowing:

1.  Narrowing refers to the process of making the type of a variable more specific during the execution of your code.

        // You use statements like if conditionals or type predicates (functions that check types) to refine the type of the variable.

        // These checks help the TypeScript compiler understand the variable's actual type at that specific point in your code.

# -- Instanceof:

1.  It's allow us to check the type of the class that we want to know. We can say that typeof and instanceof is kind of same.
    example it say's that :

                  if(data instanceof boolean){
                          //rest of the code
                  }

                  // In the condition it say's that the data is a boolean

# -- type predicates:

1. Predicate is a special kind of function that takes a value and returns a boolean indicating whether that value belongs to a specific type or satisfies certain conditions.
2. They are a powerful tool for type narrowing and improving code clarity.

# -- Exhaustiveness:

1.  you're writing code that handles different scenarios based on a variable's type. Exhaustiveness checking ensures you've considered all possible types that variable can hold and written logic to address each one. This helps catch potential bugs where you forget to handle a specific case.

## Type Assertions:

1.  We use type assertions (shape as Circle and shape as Square) to tell the compiler to trust us that shape is actually of the specified type (Circle or Square) within the case block. This allows us to access radius and side properties without worrying about potential null or undefined values.

        function getArea(shape: Shape) {
                switch (shape.kind) {
                        case "circle" :
                        return Math.PI * (shape as Circle).radius ** 2  // used Type Assertions
                }
        }
