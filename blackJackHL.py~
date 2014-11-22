'''This is a program that will help you keep a Hi-Lo count (not advertising but watch the movie '21' for more info or just google Hi-Lo BlackJack) so you could have more chances of winning at online blackjack tables. Please note the number of decks you are playing and change the variable deckNum to that number, eg. I was playing with 6 deck of cards so for me it was <<deckNum = 6>> at MyVars block of code (look below). To run the program simply open a terminal cd into the folder that you have the file and give <<python blackJackHL.py>>, also while playing and counting the cards note the terminal, it will give you info about how many decks are left in the "dealer's shoe". If you have any questions feel free to contact me, Marios Balamatsias mbalamatsias@gmail.com. In the end, always keep in mind that online blackjack gambling companies, don't want you to win so if they want you to loose you WILL LOOSE, so play for fun and use your mind don't gamble...!'''

#~~~~~~~~~~~Library Importation Area~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
from Tkinter import *
import sys
#~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


def addCard():
        global cardCount
        global rc
        global deckNum
        cardCount+=1
        if cardCount==52:
            if deckNum!=0:
                deckNum-=1
                if deckNum!=0:
                        x=rc/deckNum
                else:
                        print "No Decks Left"
                        sys.exit(1)
                rc=int(round(x))
                print str(deckNum)+" decks remaining"
                cardCount=0
                return cardCount
                return rc
            else:
                print "No Decks Left"
                sys.exit(-1)
        return cardCount


def buttonPressed1():
    global rc
    rc=rc+1
    addCard()
    zstr="The count is: %d" % rc
    mlabel0 = Label(root,text=zstr).place(relx=0.3, rely=0.8, anchor=CENTER)
    return rc

def buttonPressed2():
    global rc
    rc=rc+0
    addCard()
    zstr="The count is: %d" % rc
    mlabel0 = Label(root,text=zstr).place(relx=0.3, rely=0.8, anchor=CENTER)
    return rc

def buttonPressed3():
    global rc
    rc=rc-1
    addCard()
    zstr="The count is: %d" % rc
    mlabel0 = Label(root,text=zstr).place(relx=0.3, rely=0.8, anchor=CENTER)
    return rc

         







#create window
root = Tk()
#Top:~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
root.title("BlackJack Hi-lo by ~mbalamat")
root.geometry("400x200")

frame= Frame(root)
frame.pack()

mlabel = Label(text="Program that keeps a 'Hi-Lo' count of cards played \nin the BlackJack game ").pack()




#MyVars~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
deckNum = 6					#~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~Insert here the number of the deck of cards you are starting to play with,  in my case I was playing with 6 decks.
cardCount = 0
rc = 0
#~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
topframe = Frame(root)
topframe.pack(side = TOP)




#Buttons Block of Code~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
#Button1 instead of root use topframe
button1 = Button(topframe, padx=16, bd=8, text="+1",command=buttonPressed1, fg="red")
button1.pack(side =LEFT)
#Button2
button2 = Button(topframe, padx=16, bd=8, text="0",command=buttonPressed2, fg="black")
button2.pack(side =LEFT)
#Button3
button3 = Button(topframe, padx=16, bd=8, text="-1",command=buttonPressed3, fg="orange")
button3.pack(side =LEFT)
#~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~




#Bottom: End of GUI this line must be at the end of the code~~~~~~~~~~~~~~~~~~~~
root.mainloop()

