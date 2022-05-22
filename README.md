Chris N

Question 3 

Question #3: Compressing Strings
Write an algorithm that takes a string with repeated characters and compresses them, using a number to show how many times the repeated character has been compressed. For instance, aaa would be written as 3a. Solve the problem with and without recursion.
Example
Input: "aaabccdddda"
Output: "3ab2c4da"

function CompressString (string, i  = 0, output = “”, count = 1) {

if (i >= string.length) {

return output;

}

if (string[i} != string[i+1])  {
if (count != 1) {

output += count + string[i};

return CompressString(string, i+1, output);
} else {

output += string [i];
return CompressString (string, i+1, output);

}
}
return CompressString (string, i+1, output, count+1)

Non RECURSIVE

function CompressString(string) {

let output = “”;
let count = 0;

for (let i = 0; i < string.length; i++) {

count ++;

if (string[i] != string[i=1])  {
if (count != 1 {
output += count + string[i];
} else {
output += string[i];
}
count = 0;
}
}
return output;
}
