function processString(s) {
    let i = 0;
    s = s.split(''); // Convert string to array for easier manipulation

    for (i = s.length - 1; i >= 0; i--) {
        if (s[i] === '*' && i >= 2 && s[i - 1] === s[i - 1].toLowerCase() && s[i - 2] === s[i - 2].toUpperCase()) {
            // Swap s[i-1] and s[i-2]
            let temp = s[i - 1];
            s[i - 1] = s[i - 2];
            s[i - 2] = temp;
            s.splice(i, 1); // Remove the '*' character
        }
        if (s[i] === '0') {
            s[i] = s[0]; // Replace '0' with the first character
            s.splice(0, 1); // Remove the first character
        }
    }
    
    return s.join(''); // Convert array back to string
}

// Example usage:
let s = "A*bC*de0";
console.log(processString(s)); // Output: "CbdeA"
