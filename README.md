# Assignment: C++ Working with Strings
An introduction to string functions and string manipulation.

### 0. Get Started
You will always do these two steps:
1. Launch Xcode and clone this repository.
2. Update the comment header with your name/date.

### 1. Get the Length of a String
#### Preliminary Note
In programming, a __function__ is a block of code that can be called to perform a specific task.
String functions can be used to modify a string or give us information about the string. 

#### Steps
Edit your code so that the main body is similar to the following, and then build/run it:
```
int main()  {

    string hthnc = "High Tech High North County";
    cout << hthnc.length() << endl;

    return 0;
}
```
$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 2}}}$$

__\*\*Commit/Push to GitHub\*\*__ with commit message that matches the section heading: _1. Get the Length of a String_.

### 2. Accessing Invidual Characters
#### Preliminary Note
Rather than working with a whole string, it is possible to access individual characters within a string.

#### Steps
Copy the following code snippet and paste into your code before `return 0;`
```
  cout << hthnc[0] << hthnc[1] << hthnc[2] << hthnc[3] << endl;
```
Run the code.

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 3}}}$$

The __square bracket notation__, such as `hthnc[0]`, allow us to select a character from the string using a number for its position in the string (technically, this is known as an __index__). It is really important to note that when counting positions (indices), we always start with `0` as the first position (_index_). What would be the position (_index_) of the last character in the string? Test your answer by adding the necessary code in your program.

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 3}}}$$

__\*\*Commit/Push to GitHub\*\*__ with a commit message that matches the section heading: _2. Accessing Invidual Characters_.

### 3. Modifying Invidual Characters
#### Preliminary Note
In addition to accessing individual characters within a string, it is also possible to modify individual characters.

#### Steps
Copy the following code, paste into your program before `return 0;`, and then build/run it to observe what happens.
```
string hthnc = "High Tech High North County";
hthnc[0] = 'Z';
cout << hthnc << endl;
```
Modify your code so that individual characters are modified and it prints:
    high tech high north county

__\*\*Commit/Push to GitHub\*\*__ with a commit message that matches the section heading.

### 4. Finding Substrings
#### Preliminary Note
It is also possible to use the `find()` function to find where specific __substrings__ are located within a string.

To do this, we need to pass the function __parameters__ (also known as __arguments__) so that it can perform the task that we want it to do. 

#### Steps
Copy the following code and paste into your program.
```
string hthnc = "High Tech High North County";
cout << hthnc.find("Tech", 0)  << endl;
```
In this code, `Tech"` is the _substring_ we want to find and `0` is the starting _index_ for the search. In this example, the search starts at the beginning of the string. Build/run the code to observe what happens.

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 4}}}$$

Edit yuor code to use
```
cout << hthnc.find("High", 0)  << endl;
```
and run your code to see what happens.

$$\large{{\text{\color{red}In Desmos, respond to Prompt 2 on Screen 4}}}$$

Add code to your program to find a substring that does not exist in `hthnc`.

$$\large{{\text{\color{red}In Desmos, respond to Prompt 3 on Screen 4}}}$$

__\*\*Commit/Push to GitHub\*\*__ with a commit message that matches the section heading.

### 5. Getting Substrings
#### Preliminary Note
It happens frequently that we have a string and we only want a portion of it (a substring). We can do this with the `substr()` function, which takes two parameters:
1. The starting index.
2. The ending index.

For example, `hthnc.substr(4, 6)` would get 3 characters starting at index 4 and ending at index 6.

#### Steps
Add a line of code to your Repl to get and print "North County" from the `hthnc` string. 

$$\large{{\text{\color{red}In Desmos, respond to Prompts 1 and 2 on Screen 5}}}$$

__\*\*Commit/Push to GitHub\*\*__ with a commit message that matches the section heading.

### 6. Wrap Up
You will always do these two steps:

1. Double-check you have properly committed/pushed all steps (view your change history on GitHub).
2. Read the _Notes.md_ and summarize the main points in your composition book.
