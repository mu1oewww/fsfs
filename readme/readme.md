# <span style ="color: darkblue">JavaScript Data Structures: Date, Map, and Set Explained
 ![js picture](/img//image%20copy%206.png)
## ***JavaScript provides several built-in data structures for organizing and manipulating data. This guide explores three essential structures: `Date`, `Map`, and `Set`. We'll discuss their key features, provide examples, and show how you can use them effectively in your code.***

# 1. Date: Working with Time and Dates

## ***The `Date` object represents a specific point in time. It provides methods for manipulating dates, times, and time zones.***

**Creating a Date Object:**

```javascript
const today = new Date(); // Creates a Date object representing the current date and time
console.log(today); // Output: (Current Date and Time)

const birthday = new Date("December 17, 1995"); // Creates a Date object for a specific date
console.log(birthday); // Output: (December 17, 1995 00:00:00 GMT)

const specificTime = new Date(2023, 11, 25, 10, 30, 0); // Creates a Date object with year, month, day, hour, minute, second
console.log(specificTime); // Output: (December 25, 2023 10:30:00 GMT)  

```
## **Methods for Manipulating Dates:**
```javascript
console.log(today.getFullYear());  // Get the year
console.log(today.getMonth() + 1); // Get the month (0-indexed, so add 1)
console.log(today.getDate());    // Get the day of the month
console.log(today.getHours());   // Get the hour
console.log(today.getMinutes()); // Get the minute

today.setDate(1); // Set the day of the month to 1
console.log(today); // Output: (Current year, month, 1st day, time)
```
# **Key Points:**
```javascript
The Date object is used for representing and manipulating dates and times.
It uses the new keyword to create a new instance.
Methods like getFullYear(), getMonth(), getDate(), etc., allow you to retrieve specific date and time components.
2. Map: Storing Key-Value Pairs with Efficient Lookup
The Map object provides a way to store key-value pairs, similar to an object, but with several advantages:
```
## ***Any Key Type: Keys can be any data type (numbers, strings, objects, etc.), unlike objects, which are limited to string keys.
Ordered: Keys are stored in the order they were added.
No Hidden Properties: Maps do not have hidden prototype properties.***

### **Creating and Using a Map:**
```javascript
const myMap = new Map();

myMap.set("name", "Alice");  // Add a key-value pair
myMap.set(123, "Some data"); 

console.log(myMap.get("name")); // Output: Alice
console.log(myMap.get(123)); // Output: Some data

console.log(myMap.has("name")); // Output: true
console.log(myMap.has(456)); // Output: false

myMap.delete("name"); // Delete a key-value pair
console.log(myMap.has("name")); // Output: false

for (const [key, value] of myMap) { 
  console.log(`${key}: ${value}`); 
} // Output: 123: Some data
```
# ***Key Points:***
## ***Maps are ideal for scenarios where you need to store key-value pairs with flexible key types and maintain insertion order. set(), get(), has(), and delete() are essential methods for manipulating the map. 


## <span style ="color: darkgreen"> ***3. Set: Storing Unique ValuesThe Set object is used to store a collection of unique valuesDuplicatesareautomatically removed.***

# Creating and Using a Set:
``` javascript
const mySet = new Set();

mySet.add("apple"); 
mySet.add("banana");
mySet.add("apple"); // Duplicate - will not be added

console.log(mySet.size); // Output: 2 (because "apple" is only added once)

console.log(mySet.has("apple")); // Output: true
console.log(mySet.has("grape")); // Output: false

mySet.delete("banana"); 
console.log(mySet.size); // Output: 1

for (const item of mySet) {
  console.log(item);
} // Output: apple
```