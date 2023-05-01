DAY 5 TASK

1.Anonymous and IIFE function

console.log(`a.print odd numbers in an array`)
//anonymous function
let array1=[1,2,3,4,5,6,7,8,9,10]
let oddnum = function(arr){
     odd_arr = [];
    for(let num of arr){
        (num%2!==0)?odd_arr.push(num):num;                          //ternary operator to split the odd number
}
return odd_arr
}
console.log(`Odd numbers in an array using anonymous function : [${(oddnum(array1))}]`)    //printing in the result in terminal/console


//IIFE(Immediately invoked function)
let array2=[1,2,3,4,5,6,7,8,9,10]
console.log(`Odd numbers ina an array using IIFE function : [${
    function(arr){
        odd_arr = [];
        for (let num of arr){
            (num%2!==0)?odd_arr.push(num): num;
        }return odd_arr
    }
(array2)}]`)
console.log(

)

//b.Convert all the strings to title caps in a string array
//Anonymous function :
console.log(`b.convert all the strings to title caps in a string array`)
let str_arr=["deepak","kumar","ramesh","kishore"]
let title_cap=function(arr){
title_capped_arr=[];
    for (let index in arr){
        title_capped_arr.push(arr[index].charAt(0).toUpperCase()+arr[index].slice(1));     /*this line have push,charAt,toUpperCase,slice method 
                                                                                             to remove the word at the begining and add at the end.*/
}
console.log(`Title caps in a string array : [${title_capped_arr}]`);
}
title_cap(str_arr)                                             //calling the function.

//IIEF function:
let str_arr1=["deepak","kumar","ramesh","kishore"]
console.log(`Title caps in a string array :[${
(function(str_arr){
   let title_capped_arr=[];
    for(let str of str_arr){
        title_capped_arr.push(str.charAt(0).toUpperCase()+str.slice(1));
}
return title_capped_arr
})(str_arr1)}]`);     

console.log(

)

//c)sum of all number in an array:
console.log(`c.sum of all number in an array`)
//anonymous function:  
let num1=[1,2,3,4,5]
let sum=function(...arr){                                      //here using spread operator .
    for (let index in arr){
        console.log(`Sum of all number using anonymous function : ${(arr[index].reduce((prev, current) => prev + current,0))}`);
        }
}
sum(num1)  

//IIEF function:
let num21=[1,2,3,4,5]
console.log(`Sum of all number using IIFE function :${
(function(num2){
let result=0;
for (let index in num2){
    result+=num2[index];                                       //adding result to the varialbe in this line.
   }
   return result;
})(num21)}`)   
console.log(

)
// d)Return all prime number in an array:
console.log(`d.Return all prime number in an array`)
//anonymous function:
let num12=[1,2,3,4,5,6,7,8,9,10]
let primenum=[];
let primenumber=function(arr){
      for(let aa of arr){
      if(aa>1){
            let flag=true;                                      //here using flag varialbe.
            for(let i=2;i<aa;i++){
                  aa%i===0? flag=false:true;                    //ternary and modulo operator using here.
            }flag?primenum.push(aa):true;
      }
}}
primenumber(num12)
console.log(`Prime numbers is: ${primenum}`);

//IIEF function:
let num123=[1,2,3,4,5,6,7,8,9,10]
console.log(`Prime numbers are: ${                              // make a function inside a console.log method.
 (function(num1){
  let primenum=[];
  for (let v of num1){
        if(v>1){
              let flag=true;
              for(let i=2;i<v;i++){                             //normal for loop to start the loop from 2.
                    v%i===0?flag=false:true;                    //modulo operator and ternary operator.
              }flag?primenum.push(v):true;
        }
  }
  return primenum;
 }(num123))                                                     //giving parameters to IIFE function.
}`)
console.log(

)
//e)Palandrome in an array:
console.log(`e.Palandrome in an array`)
//Annonymous functon:
   let arr12=["did","asddsa","dkdd",123321,121,1234];
   let reverse=function(num){
        let a=String(num).split("")
        let rev=[];
        let l=a.length;
        for(let i=l-1;i>=0;i--){                                    //using normal loop to generate index from descendeing order.
            rev.push(a[i]);
            }
        rev=rev.join("");                                           //joining the elements in the array using join function and make a string word.
        return rev;
        }
        result1_arr=[];
        for(let v of arr12){
            v=String(v);                                            //convering number to string by using type casting.
            v==reverse(v)? result1_arr.push(v):false;
        }
   console.log(result1_arr);

//IIEF function:
       let arr13=["did","asddsa","dkdd",123321,121,1234];
       console.log(
       (function(arr){
            result=[];
            for(let num of arr){                                     //for of loop.
            let a=String(num).split("")
            let rev=[];
            let l=a.length;
            for(let i=l-1;i>=0;i--){
                rev.push(a[i]);
            }
            rev=rev.join("");
            a=a.join("")
            rev===a? result.push(rev):false;
       }   return result;
       })(arr13));
       console.log(

       )
//f)Median of two sorted arrays of same size:
console.log(`f.Median of two sorted arrays of same size`)
//annonymous Function:
let arr121=[2, 3, 5, 8]
let arr222=[10, 12, 14, 16, 18, 20]
let median=function(arr1,arr2){
     let arr_com=[...arr1,...arr2];                            //using spread opertor to combine a array.
     arr_com.sort((a,b)=>a-b)                                  //sorting  an array using bubble sort method.
     let len=arr_com.length;
     let arr_l=len/2;
     let result=arr_com[arr_l]+arr_com[arr_l-1];
     return result/2;
}
console.log(`Median for given two equal arrays are: ${median(arr121,arr222)}`);

//IIFE Function:
let arr111=[2, 3, 5, 8];
let arr221=[10, 12, 14, 16, 18, 20];
console.log(`Median for given two equal arrays are: ${
(function(arr1,arr2){
     let arr_com=[...arr1,...arr2];
     arr_com.sort((a,b)=>a-b);
     let len=arr_com.length;                                    //finding length by using length method.
     let arr_l=len/2;
     let result=arr_com[arr_l]+arr_com[arr_l-1];
     return result/2;
})(arr111,arr221)
}`);
console.log(

)

//g)Remove duplicates from a array:
console.log(`g.Remove duplicates from a array`)
//Annonymous function:
var arr_s = ["apple", "mango", "apple","orange", "mango", "mango"];

let remove_duplicates=function(arr){
     let a=[];
     console.log([...new Set(arr)])                              //using set remove duplicate and make new array using spread operator.
}
remove_duplicates(arr_s);

//IIFE Function:
var arr_s1 = ["apple", "mango", "apple",
        "orange", "mango", "mango"];
(function(arr){
     let a=[];
     console.log([...new Set(arr)])
}(arr_s1));                                                      //input parameter.
console.log(

)

//h)Rotate an array bye K times:
console.log(`h.Rotate an array bye K times`)
//Annonymous function:
let arr10=["santa","monica","colombia","zimbabe","hutson"];
let k1=5;
let rotate_array=function(arr1,k){
     let arr=[...arr1];
     arr.push(arr.shift());
     for(let i=1;i<=k;i++){
     }
     return arr;
};
console.log(rotate_array(arr10,k1));                             //calling function and insert input parameter inside the console.log.

//IIFE Function:
let arr100=["santa","monica","colombia","zimbabe","hutson"];
let k=3;
(function(arr1,k){
     let arr=[...arr1];                                          //copying array value using spread operator.
     for(let i=1;i<=k;i++){
     arr.push(arr.shift());
     }
     console.log(arr);
}(arr100,k));
console.log(


)


2.Arrow function
// a) Print odd number in an array: 
console.log(`a.Print odd number in an array`)
let arr=[1,2,3,4,5,6,7,8,9,10];
const oddnum1=(arr)=>{
let result=[];
for(let v of arr){
    v%2!==0?result.push(v):false;                          //identifying odd number and then insert into the resutl array in this line..
};
return result;
}
console.log(`Odd number array is: [${oddnum1(arr)}]`);
//  Output array is ===>   Odd number array is: [1,3,5,7,9]
console.log(

)

// b)Convert all the strings to title caps in a string array
console.log(`b.Convert all the strings to title caps in a string array`)
let arr1=["deepak","kumar","kishore","lodash","harry"];
const titlecap=(arr)=>{
    let res=[];
    for(let v of arr){
       res.push(v[0].toUpperCase()+v.slice(1,v.length))    //Changing the first element to caps and added to res array.
}
return res;
}
console.log(titlecap(arr1));                               //here calling the function and also passing the parameters.
//   Output array is ===>  Title caped array is : [Deepak,Kumar,Kishore,Lodash,Harry]
console.log(

)

// c) Sum of all numbers in an array:
console.log(`c.Sum of all numbers in an array`)
let arr2=[1,2,3,4,5,6,7,8,9,10];
const sum_arr=(arr)=>{
     return arr.reduce((a,b)=>a+b,0);                      //one liner for modern js. we are using arrow function to reduce.
}
console.log(`Sum of all number in an array is: ${sum_arr(arr2)}`);
// Output array is ===>    Sum of all number in an array is: 55
console.log(

)

// d) Return all prime numbers in an array:
console.log(`d.return all prime numbers in an array`)
let arr3=[1,2,3,4,5,6,7,8,9,10];
let prime_number=(array)=>{                                //function to sort prime numbers.
   let result=[];
   for(let v of array){
       let flag=true;
       if(v>1){
           for(let i=2;i<v;i++){
               if(v%2===0){
                   flag=false;
                   break;
               }
           }
       }(flag)? result.push(v):false;                     //Ternary operator.
     }return result;
}
let resultvbl=prime_number(arr3);
console.log(`Prime numbers in an array : [${resultvbl}]`); 
// Output array is ===>   Prime numbers in an array : [1,2,3,5,7,9]
console.log(

)

// e) Return all palindromes in an array:
console.log(`e.Return all palindromes in an array`)
let arr4=["did","asddsa","dkdd",123321,121,1234];
let palindrome=(array)=>{                                 //function to find palindrome in array.
   let res1=[];
   for(let v of array){                                  //for of loop to loop the values.
       v=String(v);
       let l=v.length;
       let tem="";
       for(i=l-1;i>=0;i--){                              //normal for loop in descending order.
           tem+=v[i]
           // console.log(tem);
       }v===tem? res1.push(v):false;
   }
  return res1;
};
let z=palindrome(arr4);                                   //storing function output in variable.
console.log(`Palindrome array is ; [${z}]`);


