from nltk import FreqDist
from nltk.corpus import words
from tkinter import *

#word descrambler function
def puzzler(inp):
    puzzle_letters = FreqDist(inp)
    wordlist = words.words()
    solve_bank = []
    for w in wordlist:
        if len(inp)==len(w) and FreqDist(w) == puzzle_letters:
            solve_bank.append(w)
    return solve_bank

#take input of puzzle, clear it, and print puzzler(puzzle)
def take_input():
    user_input = str(puzzle.get())
    user_input = user_input.lower()
    solve_list.set(puzzler(user_input))

#setting up a simple UI
root = Tk()
root.title('Word Descrambler')

w = Label(root, text="please type a word to descramble")
w.pack()

puzzle = StringVar()
puzzle = Entry(root, textvariable=puzzle)
puzzle.pack()

b = Button(root, text='Run!',command=take_input)
b.pack()
q = Button(root, text='Quit', command=root.destroy)
q.pack()

solve_list = StringVar()
l1 = Label(root, text="Unscrambled word(s):")
l1.pack()
l2 = Label(root, textvariable=solve_list)
l2.pack()

root.mainloop()
