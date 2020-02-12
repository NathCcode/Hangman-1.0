## Thanks for checking out my hangman program!

How to play:

1.)it will ask you if you want to play(yes,no)
2.)choose a difficuly(e,m,h)
(easy, medium, hard)
3.) start guessing letters. Think you got the word? type it all in!
### THE CODE!
```markdown
Syntax highlighted code block

#Hangman 1.0
#by Nathan

#how to play
#---------------------------------------------------------------------------------
#imput 1 letter at a time
#if you think you got the word put the whole word e.g

#'-''e''l'l''-'
 #hello
#you win!

#----------------------------------------------------------------------------------------------------------

#Start
def main():
    q = input('would you like to play a game of hangman?yes/no:')
        
    if q =='yes':
            
        def game( ):
            #decides a random word in the list
            import random
            x = random.uniform(0,5)
            X= round(x)

            d = input('select difficulty. Easy,Medium,hard' '(e,m,h):')
            if d == 'e':
                words =['seven', 'pizza', 'happy', 'again']
            if d == 'm':
                words =['glyph','shift','drift','sifts','lifts']
            if d == 'h':
                words = ['ivory','banjo','rouge','crypt','jiffy','haiku','kiosk','pixel',]
            
            L =list(words[X])
            #calculates number of words
            dashes =  '-----'
            
            D = list(dashes)
            
            print(D)
            #word replacement system
            #10 = number of turns allowed in hangman
            for i in range(10):
            
                original = dashes
            
                answer = input('guess a word/letter:')
            #1
                if answer == L[0]:
                    search = L.index(answer)
                    print(search)
                    print("you got a word") 
                    D[0] = answer
                     
            #2
                if answer == L[1]:
                    search = L.index(answer)
                    print(search)
                    print("you got a word")
                    D[1] = answer
                     
            #3    
        
                if answer == L[2]:
                    search = L.index(answer)
                    print(search)
                    print("you got a word")
                    D[2] = answer
                     
            #4   
                if answer == L[3]:
                    search = L.index(answer)
                    print(search)
                    print("you got a word")
                    D[3] = answer
                     
            #5
                if answer == L[4]:
                    search = L.index(answer)
                    print(search)
                    print("you got a word")
                    D[4] = answer
                        
                print(D)
            
#win/loose decision                
                if answer not in L:
                    print('wrong word')
                
                A = list(answer)
                
                p2 = print(A)
                
                if D == L:
                    print('you win!')
                    exit()
                  
                if A == L:
                    print('you win!')
                    exit()

#loose decision
            print('you loose')
            print('the word was ' +  words[X])
            exit()
 
                
        game()
main()

```

### if there are any bugs, lmk and i will try fix it, or if you have any ideas, feel free to share!
