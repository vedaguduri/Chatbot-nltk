# Chatbot-nltk
simple chat bot using nltk library 
Lets Import the libraries
from nltk.chat.util import Chat, reflections
1
from nltk.chat.util import Chat, reflections
Create the chatbots list of recognizable patterns and it’s a response to those patterns. To do this we will create a variable called pairs.

#Pairs is a list of patterns and responses.
pairs = [
    [
        r"(.*)my name is (.*)",
        ["Hello %2, How are you today ?",]
    ],
    [
        r"(.*)help(.*) ",
        ["I can help you ",]
    ],
     [
        r"(.*) your name ?",
        ["My name is thecleverprogrammer, but you can just call me robot and I'm a chatbot .",]
    ],
    [
        r"how are you (.*) ?",
        ["I'm doing very well", "i am great !"]
    ],
    [
        r"sorry (.*)",
        ["Its alright","Its OK, never mind that",]
    ],
    [
        r"i'm (.*) (good|well|okay|ok)",
        ["Nice to hear that","Alright, great !",]
    ],
    [
        r"(hi|hey|hello|hola|holla)(.*)",
        ["Hello", "Hey there",]
    ],
    [
        r"what (.*) want ?",
        ["Make me an offer I can't refuse",]
        
    ],
    [
        r"(.*)created(.*)",
        ["Aman Kharwal created me using Python's NLTK library ","top secret ;)",]
    ],
    [
        r"(.*) (location|city) ?",
        ['New Delhi, India',]
    ],
    [
        r"(.*)raining in (.*)",
        ["No rain in the past 4 days here in %2","In %2 there is a 50% chance of rain",]
    ],
    [
        r"how (.*) health (.*)",
        ["Health is very important, but I am a computer, so I don't need to worry about my health ",]
    ],
    [
        r"(.*)(sports|game|sport)(.*)",
        ["I'm a very big fan of Cricket",]
    ],
    [
        r"who (.*) (Cricketer|Batsman)?",
        ["Virat Kohli"]
    ],
    [
        r"quit",
        ["Bye for now. See you soon :) ","It was nice talking to you. See you soon :)"]
    ],
    [
        r"(.*)",
        ['That is nice to hear']
    ],
]
1
#Pairs is a list of patterns and responses.
2
pairs = [
3
    [
4
        r"(.*)my name is (.*)",
5
        ["Hello %2, How are you today ?",]
6
    ],
7
    [
8
        r"(.*)help(.*) ",
9
        ["I can help you ",]
10
    ],
11
     [
12
        r"(.*) your name ?",
13
        ["My name is thecleverprogrammer, but you can just call me robot and I'm a chatbot .",]
14
    ],
15
    [
16
        r"how are you (.*) ?",
17
        ["I'm doing very well", "i am great !"]
18
    ],
19
    [
20
        r"sorry (.*)",
21
        ["Its alright","Its OK, never mind that",]
22
    ],
23
    [
24
        r"i'm (.*) (good|well|okay|ok)",
25
        ["Nice to hear that","Alright, great !",]
26
    ],
27
    [
28
        r"(hi|hey|hello|hola|holla)(.*)",
29
        ["Hello", "Hey there",]
30
    ],
31
    [
32
        r"what (.*) want ?",
33
        ["Make me an offer I can't refuse",]
34
        
35
    ],
36
    [
37
        r"(.*)created(.*)",
38
        ["Aman Kharwal created me using Python's NLTK library ","top secret ;)",]
39
    ],
40
    [
41
        r"(.*) (location|city) ?",
42
        ['New Delhi, India',]
43
    ],
44
    [
45
        r"(.*)raining in (.*)",
46
        ["No rain in the past 4 days here in %2","In %2 there is a 50% chance of rain",]
47
    ],
48
    [
49
        r"how (.*) health (.*)",
50
        ["Health is very important, but I am a computer, so I don't need to worry about my health ",]
51
    ],
52
    [
53
        r"(.*)(sports|game|sport)(.*)",
54
        ["I'm a very big fan of Cricket",]
55
    ],
56
    [
57
        r"who (.*) (Cricketer|Batsman)?",
58
        ["Virat Kohli"]
59
    ],
60
    [
61
        r"quit",
62
        ["Bye for now. See you soon :) ","It was nice talking to you. See you soon :)"]
63
    ],
64
    [
65
        r"(.*)",
66
        ['That is nice to hear']
67
    ],
68
]
Okay, so as we finished the patterns and responses, let’s take a look at something called reflections. Reflections is a dictionary file that contains a set of input values and corresponding output values.

For example, if the string input was “I am a programmer”, then the output would be “you are a programmer”.

print(reflections)
1
print(reflections)
1
#Output
2
{'i am': 'you are',
3
'i was': 'you were',
4
'i': 'you',
5
"i'm": 'you are',
6
"i'd": 'you would',
7
"i've": 'you have',
8
"i'll": 'you will',
9
'my': 'your',
10
'you are': 'I am',
11
'you were': 'I was',
12
"you've": 'I have',
13
"you'll": 'I will',
14
'your': 'my',
15
'yours': 'mine',
16
'you': 'me',
17
'me': 'you'}
We can also create our own reflections dictionary in the same format as reflections above. Below is an example of how to do this:

my_dummy_reflections= {
    "go"     : "gone",
    "hello"    : "hey there"
}
1
my_dummy_reflections= {
2
    "go"     : "gone",
3
    "hello"    : "hey there"
4
}
Now let’s print a default message, and finish our chatbot:

#default message at the start of chat
print("Hi, I'm thecleverprogrammer and I like to chat\nPlease type lowercase English language to start a conversation. Type quit to leave ")
#Create Chat Bot
chat = Chat(pairs, reflections)
1
#default message at the start of chat
2
print("Hi, I'm thecleverprogrammer and I like to chat\nPlease type lowercase English language to start a conversation. Type quit to leave ")
3
#Create Chat Bot
4
chat = Chat(pairs, reflections)
Now, let’s start a conversation
#Start conversation
chat.converse()
1
#Start conversation
2
chat.converse()
