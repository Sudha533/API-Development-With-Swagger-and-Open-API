### YAML

YAML, which stands for "YAML Ain't Markup Language," is a human-readable data serialization standard that can be used in conjunction with all programming languages. Here are some key points about YAML:

**Human-Readable:** YAML is designed to be easily readable by humans. Its syntax is simple and intuitive, making it accessible for users to write and understand.

**Data Serialization:** YAML is used to serialize data, which means converting data structures or objects into a format that can be stored and transferred. It is often used for configuration files, data exchange between languages with different data structures, and for storing complex data structures.

**Hierarchical Data:** YAML supports hierarchical data structures through indentation. Nested elements are indicated by leading spaces, making it easy to represent complex data hierarchies.

**Compatibility:** YAML can be used with most programming languages, as there are libraries available for parsing and generating YAML data in many languages.

**Common Uses:** YAML is often used for configuration files (e.g., Docker Compose files, Ansible playbooks), data exchange, and log files. It is also utilized in settings where complex data structures need to be represented in a simple, readable format.

Example of YAML Syntax

```
# This is a comment
person:
  name: John Doe
  age: 30
  address:
    street: 123 Main St
    city: Anytown
    state: CA
  phone_numbers:
    - type: home
      number: 555-555-5555
    - type: work
      number: 555-555-5556
```

In this example:

person is a key with a nested structure.
name, age, and address are keys under person.
address itself contains a nested structure with street, city, and state.
phone_numbers is a list containing two items, each with type and number keys.
YAML's readability and simplicity make it a popular choice for configuration files and data serialization.

YAML Structure
To begin exploring YAML, let’s take a look at an example YAML file called example.yaml:
```
---
# Our first YAML document
bottle: wine
capitals:
  Japan: Tokyo
  Argentina: Buenos Aires
oceans:
  - Indian
  - Atlantic
  - Arctic
  - Pacific
…
```


A YAML document begins with three dashes (---) and ends with three dots (…). These characters can separate multiple YAML documents within a single file. In a YAML file with a singular document (e.g., the above example), most parsers treat these characters as optional.

The second line begins with #, which makes it a comment. Comments are ignored by parsers but are helpful since YAML files are often shared by different developers and can provide insight into the document’s purpose.

The bulk of this YAML document consists of mappings or key-value pairs, which are separated by a colon and a space (: ). Every key must be a string and must be unique. Values can be nested mappings, as is the case with the value of capitals. They can also be sequences, as with the value of oceans, or scalars, as with the value of bottle. We’ll learn more about these data types a bit later in this article.

The use of whitespace is a crucial aspect of YAML. Notice how a line break separates each mapping. When objects are nested, indentation indicates which objects are a part of the same value. Indentation must consist of one or more spaces. Tabs, however, are forbidden in YAML.

While not explicitly shown, note that YAML files should end with the extension .yaml or .yml.

### Sequences
YAML sequences look a bit like lists or arrays in programming languages. They can contain any mix of data types, including nested sequences or mappings. Sequences are usually displayed on multiple lines, where each element begins with a dash, followed by a space, and ends with a line break. Take a look at an example:
```
fish:
  - Tuna
  - Trout
  - Salmon
numbers:
  - pi
  - 7
  - 1.1
```
Sequences can also be written on a single line surrounded by brackets. In this case, elements are separated by a comma and a space, like this:
```
planets: [Mercury, Venus, Mars]
```

### Scalars
All remaining data types in YAML are scalars, also known as single value data types. These include integers, floating-point numbers, booleans, null, and strings. Let’s see scalars in action:
```
scalars:
  - 1
  - 1.0
  - True
  - null
  - "string"
```

Let’s break down the types above:

**Numbers:** In YAML, numbers are classified by a single rule. Any number that doesn’t have a decimal point is an integer, while numbers that do are floats.

**Booleans:** For booleans, the keywords True, On, and Yes evaluate to true. The keywords False, Off, and No will to false. Here are some examples:
```
elephant:
  - big: True
  - mammal: Yes
  - yellow: Off
```

**Null: **A null value can be represented by either ~ or null (could also be written as Null or NULL), like this:
```
nulls:
  - null
  - ~
```

**Strings:** In YAML, strings generally do not need quotes. Two notable exceptions are as follows:
Use single or double quotes to create a value that would normally be interpreted as a different data type to be a string, i.e., “10” or "null"
Use double quotes to allow specific sequences to be escaped instead of treated as literals, such as "\n" representing a line break
Here are some more examples of strings in action:
```
strings:
  - This string ends with a slash followed by n \n
  - "This string ends with a line break \n"
  - 'True'
```
