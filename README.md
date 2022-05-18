# @devdamo/cuid

cuid is a javascript package that generates a random variable string id.

cuid gives you the option to generate id that contains numbers and letters,
generation of id that is only numbers and generation of id that is only letters

cuid stands for : customized unique id

## Functionality

When calling the function cuid(), we need to enter two parameters, the size of the id and which option to use, ranging from 1-3.

1) numbers and letters
2) numbers only
3) letters only

Depending on the option that you have chosen, the unique id will be generated.

The id's are generated with the use of a for loop. This loop loops as many times as the id size provided. In this loop, each digit/letter of the id is generated.
It is a 50/50 chance that an element of the id will be a letter or a digit. 

```javascript
var chance = Math.floor(Math.random() > 0.5);
```

The code above is responsible for deciding will the next element be a number or a letter. The code generates a value of either 1 or 0. This value is then used to decide will the next element of the id be a number or letter.

```javascript
// the alphabet
const alphabet = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]

if (chance == 0) {
  // generating a single digit number
  value = Math.floor(Math.random() * 10)
} 
else if (chance == 1) {
  // we get a random number from alphabet and use it as value for final id
  value = alphabet[Math.floor(Math.random() * 26)]
}
```

The other 2 options are almost the same as the first option.

Then the cuid function returns a string of the id.

```javascript
return stringId;
```

## Installation

```
npm install @devdamo/cuid
```
```
npm i @devdamo/cuid
```

## Usage

```javascript
const cuid = require('@devdamo/cuid');

// generates an id that is 10 digits/letters long
cuid(10,1); // generates > r7pd7a55p0

// generates an id that is 10 numbers long and only numbers
cuid(10,2); // generates > 7621902562

// generates an id that is 10 numbers letters long and only letters
cuid(10,3); // generates > mletbuywgm
```

## Contributing
Please do not attempt to create pull requests or try to contribute.

## License
[MIT](https://choosealicense.com/licenses/mit/)
