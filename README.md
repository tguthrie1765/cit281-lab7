In this lab I setup my Github account. I had a JS file that thowed custom errors and I used Github to save the changes. 

<br>

Here is the code for lab 7
```js
/*
cit 281: lab 07
author: Thomas Guthrie
*/

class CustomError extends Error{
    constructor(args){
        super(args);
        this.message='Error: custom error';
    }
}

function throwGenericError(){
    throw new Error('Error: generic error');
}
function throwCustomError(){
    throw new CustomError('custom error');
}


console.log("force generic error");
try{
    console.log('generic error try block');
    throwGenericError();
} catch (err){
    console.log('generic error catch block');
    console.log(err.message);
} finally{
    console.log('generic error finally blocked');
};


console.log('force custom error');
try{
    console.log('custom error try block');
    throwCustomError();
} catch (err){
    console.log('custom error catch block');
    console.log(err.message);
} finally{
    console.log('custom error final block');
}
```
