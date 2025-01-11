# sassychatbot
A simple chat bot...but sassy.



#bash
$ pip install nltk



#python 
import nltk
from nltk.chat.util import Chat, reflections

# Define a list of patterns and responses
pairs = [
    [
        r"my name is (.*)",
        ["Hey gurl, how can I help you today?",]
    ],
    [
        r"hi|hey|hello",
        ["what do you want, is this a 'you up' text?", "Hey gurl",]
    ],
    [
        r"what is your name?",
        ["I am a bot-daddy created by BudT.",]
    ],
    [
        r"how are you?",
        ["I'm living the dream, what do you want?",]
    ],
    [
        r"sorry (.*)",
        ["It's okay, no worries.. I guess.",]
    ],
    [
        r"quit",
        ["Bye! Smell you later!.",]
    ],
]

def chatbot():
    print("Hi, I'm a chatbot. Type 'quit' to exit.")
    chat = Chat(pairs, reflections)
    chat.converse()

# Start the chatbot
if __name__ == "__main__":
    chatbot()
