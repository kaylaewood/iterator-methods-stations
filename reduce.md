# .reduce

1. What does `.reduce` do? Reduces an array of elements down to a single value
2. Is the original array modified? No
3. How many arguments does `.reduce` take? 2 - callback and initial value
4. How many arguments does the _callback function_ take? 2 - accumulator, current element, index, array
5. Which arguments are required (for both the method and its callback)? accumulator, current element, and callback
6. Does the callback need a return value? If so, what needs to be returned? Yes, the accumulator must be returned


Given an array of numbers, write a function that returns the product of all the numbers.

```
var numbers = [1,2,5,7]

function getProduct() {
  let product = numbers.reduce((acc, number) => {
    acc *= number;
    return acc;
  }, )
  return product;
};

getProduct();
```

Given a list of countries, write a function that returns a new object where the keys are country names and their values are an object containing the rest of the country's data.

```js
var countries = [
  {
    "countryCode": "AF",
    "countryName": "Afghanistan",
    "population": "29121286",
    "capital": "Kabul",
    "continentName": "Asia"
  },
  {
    "countryCode": "AL",
    "countryName": "Albania",
    "population": "2986952",
    "capital": "Tirana",
    "continentName": "Europe"
  },
  {
    "countryCode": "DZ",
    "countryName": "Algeria",
    "population": "34586184",
    "capital": "Algiers",
    "continentName": "Africa"
  },
]

organizeByCountry(countries)
/*
output:
{
  Afghanistan: {
    "countryCode": "AF",
    "population": "29121286",
    "capital": "Kabul",
    "continentName": "Asia"
  },
  Albania: {
    "countryCode": "AL",
    "population": "2986952",
    "capital": "Tirana",
    "continentName": "Europe"
  },
  Algeria: {
    "countryCode": "DZ",
    "population": "34586184",
    "capital": "Algiers",
    "continentName": "Africa"
  },
}
*/
```



```
// EXAMPLE 1 ES6
// var numbers = [1,2,5,7]

// function getProduct() {
//   let product = numbers.reduce((acc, number) => {
//     acc *= number;
//     return acc;
//   }, )
//   return product;
// };

// getProduct();

// EXAMPLE 1 ES5
// var numbers = [1,2,5,7]

// function getProduct() {
//   return numbers.reduce(function(acc, number) {
//     acc = acc * number;
//     return acc;
//   }, 1)
//   return product;
// };

// getProduct();

// EXAMPLE 2 ES5
// var countries = [
//   {
//     "countryCode": "AF",
//     "countryName": "Afghanistan",
//     "population": "29121286",
//     "capital": "Kabul",
//     "continentName": "Asia"
//   },
//   {
//     "countryCode": "AL",
//     "countryName": "Albania",
//     "population": "2986952",
//     "capital": "Tirana",
//     "continentName": "Europe"
//   },
//   {
//     "countryCode": "DZ",
//     "countryName": "Algeria",
//     "population": "34586184",
//     "capital": "Algiers",
//     "continentName": "Africa"
//   },
// ]

// function organizeByCountry(countries) {
//   return countries.reduce(function(acc, country) {
//      acc[country.countryName] = {
//        countryCode: country.countryCode,
//        population: country.population,
//        capital: countries.capital,
//       continentName: countries.continentName
//      }
//      return acc;
//   }, {});
// };

// organizeByCountry(countries);
```
