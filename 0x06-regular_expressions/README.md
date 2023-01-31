# Regular expression

A regular expression (regex) is a text pattern that can be used for searching and replacing. Regular expressions are similar to Unix wild cards used in globbing, but much more powerful, and can be used to search, replace and validate text.

Regular expressions are used in many Unix commands such as find and grep, and also within most programming languages such as R and Python.


![image](https://user-images.githubusercontent.com/105078661/215861022-843c0fd3-0bb5-499b-bd9d-76835b1c5eaa.png)

# Background Context
For this project, you have to build your regular expression using Oniguruma, a regular expression library that which is used by Ruby by default. Note that other regular expression libraries sometimes have different properties.

Because the focus of this exercise is to play with regular expressions (regex), here is the Ruby code that you should use, just replace the regexp part, meaning the code in between the //:

sylvain@ubuntu$ cat example.rb
#!/usr/bin/env ruby
puts ARGV[0].scan(/127.0.0.[0-9]/).join
sylvain@ubuntu$
sylvain@ubuntu$ ./example.rb 127.0.0.2
127.0.0.2
sylvain@ubuntu$ ./example.rb 127.0.0.1
127.0.0.1
sylvain@ubuntu$ ./example.rb 127.0.0.a

# Basic Regular expressions
# Symbol	# Descriptions
- .	        replaces any character
- ^	        matches start of string
- $	        matches end of string
- *	        matches up zero or more times the preceding character
- \	        Represent special characters
- ()	    Groups regular expressions
- ?	        Matches up exactly one character 


![image](https://user-images.githubusercontent.com/105078661/215859562-3dc5dd22-aec0-4439-ba2c-16a35b43548e.png)
