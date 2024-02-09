# JavaScript-Q13
Write a JavaScript program that uses a try-catch block to catch and handle a 'SyntaxError' when parsing an invalid JSON string

function parse_JSON(jsonString) {
  try {
    const parsedData = JSON.parse(jsonString);
    console.log('Parsed data:', parsedData);
  } catch (error) {
    if (error instanceof SyntaxError) {
      console.log('SyntaxError:', error.message);
    } else {
      console.log('Error:', error.message);
    }
  }
}

// Example:
parse_JSON('{"name": "Rowan Octave", "age": 30}'); // Valid JSON
parse_JSON('{"name": "Rowan Octave", "age": 30,}'); // Invalid JSON

**Sample Output:**

"Parsed data:"
[object Object] {
  age: 30,
  name: "Rowan Octave"
}
"SyntaxError:"
"Expected double-quoted property name in JSON at position 35"
