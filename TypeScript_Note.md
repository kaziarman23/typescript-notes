TypeScript is a devlopment tool for JavaScript.When we write rew javaScript it help us to make our code more clean.

## How to install TypeScript:

1. Open your commend line and type a commend that will install the type Script globally.
        npm install -g typescript
        // Then you can make a file and work on it

2. To run any commend we have to write (tsc) first and this is a syntex.

3. To check you'r depandanci is install we have this commend and it will show you'r downloaded version in you file.
        tsc -v


## Convert in JS:

1. we can't see the result/output in the typeScript.We have to convert it in a javaScript and then we have to see the output of our code.The commend of converting typeScript to javaScript is:
        tsc TS_File_Name


## Functions in TypeScript:
## file number 02
1. we need to set Data type in the function because it's a good practice.

2. In typeScript we have to declare what kind of function and peramitar's are we taking.
        
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

1. Passing obj in the function  is requred some syntex:

        function createObj():{Name: string, price: number}{
                return {Name: ReactJs, price: 599}
        }

        createObj() //output: {Name: ReactJs, price: 599}

        

        // In this function we set an obj as a Data type after the parenthesis and before the definition

2. Passing obj in the function peramitar is requred some syntex also:

## Have to read decoment's for this;









## Type Aliases in functions:

1. we can set obj property in the function peramiter as many as we want with the help of Type Aliases :

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
## file number 03


1. readonly: Marks a property or parameter as read-only, meaning its value cannot be changed after initialization.  Use the readonly keyword before the property name during declaration.

2. optional: Indicates that a property in an interface or object literal might be absent.Use a question mark (?) after the property name during declaration.

3. Interfaces: Interfaces in TypeScript are powerful tools for defining the structure of objects. They act like blueprints or contracts that specify the properties and methods that an object must have.


