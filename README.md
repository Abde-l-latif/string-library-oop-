# cls_string Library

A lightweight C++ string utility class that extends std::string functionality with useful operations for text manipulation, formatting, and analysis.

<hr>
🚀 Features

The cls_string class provides both static and instance methods to work with strings:

🔤 Case Manipulation

Convert string to upper or lower case.

Convert first letter of each word to upper/lower.

Invert case of each character.

Check if a character is uppercase or lowercase.

<hr>

✍️ Word Operations

Count words in a sentence.

Print each word in a string.

Split a string into a vector of words.

Join words back into a string (from array/vector).

Reverse word order in a sentence.

Replace words in a string.

<hr>

🔎 Character Analysis

Count capital and small letters.

Count occurrences of a specific letter (case-sensitive or not).

Check if a letter is a vowel.

Count and print all vowels in a string.

<hr>

🧹 Trimming & Cleaning

Trim left, trim right, and trim both sides.

Remove all punctuation.

<hr>

🛠️ Additional Helpers

Get the first letter of words in a string.

Enum-based helpers for case checking and sensitivity handling.

<hr>

📦 Installation

Just include the header file in your project:

#include "cls_string.h"


Make sure you have C++11 or later enabled.

<hr>

📝 Usage Examples
#include <iostream>
#include "cls_string.h"
using namespace std;

int main() {
    cls_string myStr("hello world from cpp");

    // Convert to uppercase
    myStr.convert_to_upper();
    cout << myStr.value << endl;   // HELLO WORLD FROM CPP

    // Invert string case
    myStr.value = "HeLLo WoRLd";
    myStr.invert_string_case();
    cout << myStr.value << endl;   // hEllO wOrlD

    // Count vowels
    cout << "Vowels: " << myStr.count_vowels() << endl;

    // Split string
    vector<string> words = cls_string::SplitString("C++ is awesome", " ");
    for (auto &w : words) cout << w << endl;

    // Replace words
    myStr.value = "I like Java, Java is great!";
    myStr.ReplaceWordsInString("Java", "C++");
    cout << myStr.value << endl;   // I like C++, C++ is great!

    return 0;
}
<hr>
🏗️ Design

Static methods → work directly on std::string without creating an object.

Instance methods → operate on the _value stored in the object.

value is exposed as a property for convenience (.value).

<hr>

📌 TODO / Future Enhancements

Add support for regex-based search/replace.

Add more localization-friendly methods (Unicode support).

Add unit tests for reliability.
