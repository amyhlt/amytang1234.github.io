---
layout: post
title: "String.split()"
date: 2021-10-19
---

const str = 'The quick brown fox jumps over the lazy dog.';
const words = str.split(' ');
console.log(words[2]);


const chars = str.split('');
console.log(chars[3]);


const str = str.split();
console.log(str);

Answer:
brown
e
[ 'The quick brown fox jumps over the lazy dog.' ]

EX:
1)function isPalindrome(str){
   const arrStr=str.split("");
  let start=0;
  let end=arrStr.length-1;
  while (start <= end){
      if(arrStr[start].toLowerCase()===arrStr[end].toLowerCase())
      {
          start++;
          end--;
      } else {
          break;
      }
  }
  if(start >end){
      return true;
  } else{
      return false;
  }
}
console.log(isPalindrome("Anna"));
console.log(isPalindrome("NOON"));
console.log(isPalindrome("1122 2211"));

2)function isPalindrome(str){
     const str1=str.replace(/[\w_]/g,'').toLowerCase();
     const str2=str1.split('').reverse().join('').toLowerCase();
     return str1===str2;
 }
 console.log(isPalindrome("Anna"));
 console.log(isPalindrome("Hello world!"));
