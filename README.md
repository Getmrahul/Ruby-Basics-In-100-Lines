# Ruby Basics in 100 Lines of Code
If you are already familiar with the programming language like python, then I recommend you to go with this. You can either see the below code or try <b>QuickStart.rb</b>.<br/>
To learn more I recommend you to check out https://learnrubythehardway.org/book.

## How to Run
In terminal type <b>ruby QuickStart.rb</b>.

## Code
```rb
#   
#   Basics of Ruby!
#   - @rahulmfg
#   - www.rahulm.me
#

# Print 
puts "Welcome, let's code in Ruby!" # this will add new line(\n)
print "So, what is your name? " # this will not add a new line(\n)

# STD Input
your_awesome_name = $stdin.gets.chomp # google about $stdin.gets.chomp vs gets.chomp!

# Printing var w/ string
puts "Yo, #{your_awesome_name}"

# Hash
about = {"name" => your_awesome_name, "id": 1, "key": "qKsa1O"}

# Simple Module
module Emoji
    def Emoji.smile()
        return "😊"
    end

    def Emoji.cry()
        puts "😭"
    end
    ABOUT = "My job is to print an Emoji"
end

puts Emoji::ABOUT
smile = Emoji.smile()
puts smile

Emoji.cry()

# IF Statement
if true
    puts "Hey, I'm from IF"
end

# IF-ELSE
puts "Do you like Ruby so far?\n1 - Yes\n2 - No"
print '> '
answer = $stdin.gets.chomp.to_i # google about ruby to_i

if answer == 1
    puts Emoji.smile()
elsif answer == 2
    Emoji.cry()
else
    puts "Mmm..."
end

# FOR Loop
numbers = [1, 2, 3, 4]
words = ["Random", "Air", "Hot", "Ufo", "Like"]

for number in (0..10)
    puts number
end

numbers.each do |number|
    puts number
end

words.each {|word| puts word}

# While Loop
i = 0
while i < words.length
    puts words[i]
    i += 1
end

# Class
class MoodEmoji
    attr_reader :mood # check https://stackoverflow.com/a/5046915/2182940
    
    def initialize(mood)
        @mood = mood
    end

    def emoji()
        if @mood == "happy"
            puts "You're happy 😊😇"
        elsif @mood == "sad"
            puts "You're sad ☹️😞"
        else
            puts "🤔"
        end
    end
end

happy = MoodEmoji.new("happy")
sad = MoodEmoji.new("sad")

happy.emoji()
sad.emoji()

```
