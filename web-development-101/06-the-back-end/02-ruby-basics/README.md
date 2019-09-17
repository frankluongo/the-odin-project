# Ruby Basics

## Lesson Outcomes

After doing the assignments, answer these questions:

### What is an “interpreted” language

A language that can't run on your processor directly. It has to be fed through a virtual machine

### What is IRB

IRB is Ruby's version of a REPL (Read, evaluate, print, loop). You can open it from the console by typing `irb`

### What are Objects

In Ruby, everything is an Object. An object is something that holds attributes and can perform methods

### What are Methods

Methods are actions associated with an object

### What are Classes

Classes represent collection of attributes and methods associated to one particular type of thing. Ex.) a student

### What are Blocks

Blocks are reusable pieces of code that perform a certain task

### What is an Array

An array is a collection of data

### What is an Iterator

Methods that perform an action on each item in an array

### What are hashes

A hash is a collection of data where each element of data is addressed by a name.

### What is a library

A third-party collection of code that can help you perform tasks quicker and easier

### What is a gem

A packaged library

## Assignments

- [Ruby in 100 Minutes](http://tutorials.jumpstartlab.com/projects/ruby_in_100_minutes.html)
- [Learn To Program](https://pine.fm/LearnToProgram/chap_00.html)
- [Learn To Program Answers](http://learntoprogramanswers.blogspot.com/)
- [Variables In Ruby](http://ruby-for-beginners.rubymonstas.org/variables.html)
- [Built-in Data Types In Ruby](http://ruby-for-beginners.rubymonstas.org/built_in_classes.html)
- [Ruby For Beginners](http://ruby-for-beginners.rubymonstas.org/index.html)

## Assignment Notes

### [Ruby in 100 Minutes](http://tutorials.jumpstartlab.com/projects/ruby_in_100_minutes.html)

#### 02. Variables

- Ruby doesn't need to declare variables. They're created when you assign a value to them
- Ruby evaluates right to left
- Ruby's variables are flexible -- They can be assigned any type

##### 02.1 Naming Variables

- local variables always start with a lowercase letter
- They have no spaces
- do not contain special characters
- They are typically in snake case
- Named after the meaning of their contents, not the type of their contents
- not abbreviated

#### 03. Strings

- Negative positions in a string start at the end and count backwards

##### 03.3 Common String Methods

- **.length** - How many characters are in a string (including spaces)
- **.split** - splits a string into an array, using spaces by default unless you pass an argument
- **.sub** - replace a part of a string in one instance
- **.gsub** - replace a part of a string in every instance which it occurs

##### 03.4 Combining Strings and Variables

- interpolation only works in a double quoted string

#### 04. Symbols

It's basically a named integer. Any reference to a symbol will always return the same value

#### 05. Numbers

- Integers are whole numbers, floats have a decimal point
- Integers in Ruby have methods on them to make using them easier. Ex.) `5.times` will do something 5 times

#### 06. Blocks

- A way to bundle up instructions for use elsewhere
- They start with "do" and end with "end"
- When there's a single instruction, we can use brackets `5.times{ puts "Hello, World!" }`

##### 06.3 Block Parameters

When we have to reference the value a block is currently working with, we use pipes

```rb
5.times do |i|
  puts "#{i}: Hello, World!"
end
```

#### 07. Arrays

- We use "shovels" to add elements to arrays `<<`
- **.sort** will sort an array
- **.each** will iterate through an array so you can perform operations
- **.join** will mash them together into one string
- **.include?** will check for a value

#### 08. Hashes

- These are key/value pairs
- If there are symbols as the keys, we can use colons instead of arrows

```rb
produce = {
  "apples" => 3,
  "oranges" => 7
}

produce = {
  apples: 3,
  oranges: 7
}
```

#### 09. Conditionals

- We use && and || for and/or

```rb
def water_status(minutes)
  if minutes < 7
    puts "The water is not boiling yet."
  elsif minutes == 7
    puts "It's just barely boiling"
  elsif minutes == 8
    puts "It's boiling!"
  else
    puts "Hot! Hot! Hot!"
  end
end
```

#### 10. Nil and Nothingness

- `nil` is when something doesn't exist

#### 11. Objects, Attributes, and Methods

- Ruby is an object-oriented language
- Objects hold information, called attributes, and they can perform actions, called methods.

##### 11.2 Classes and Instances

- classes are abstract descriptions of a category or type of thing. It defines what attributes and methods all objects of that type have.

```rb
class Student
  attr_accessor :first_name, :last_name, :primary_phone_number

  def introduction
    puts "Hi, I'm #{first_name}!"
  end
end
```

- The `attr_accesor` method which is used to define attributes for instances of a class.

###### 11.2.1 Creating Instances

- The class above does nothing until we instantiate it with an instance

```rb
frank = Student.new
```

##### 11.4 Return Value

- In Ruby, every time you call a method you get a value back. By default, a Ruby method returns the value of the last expression it evaluated

```rb
class Student
  attr_accessor :first_name, :last_name, :primary_phone_number

  def introduction(target)
    puts "Hi #{target}, I'm #{first_name}!"
  end

  def favorite_number
    7
  end
end

frank = Student.new
frank.first_name = "Frank"
puts "Frank's favorite number is #{frank.favorite_number}."
```

### Chris Pine's Learn To Program

- Procs are methods stored as variables that can be passed into other methods and objects
- Proc stands for "Procedure"
-
