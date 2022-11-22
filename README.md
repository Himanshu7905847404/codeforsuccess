# codeforsuccess
#code
# program 
import random
print("~~~~ The Project game ~~~~~~~")
while(True):
    print('''
    Press 1. For "Start"
    Press 2. For "Exit" \n ''')
    
    choice = int(input("Enter your choice: \n"))
    
    if choice == 1 :
        
        numberOfMember = int(input("How many members in your Project: \n"))
        headName = input("Who is the Head of this Project: \n")
        
        while(numberOfMember>1):
            memberName = input("Enter the name of other member's one by one after enter : \n")
            numberOfMember -= 1
        
        print(''' 
        Instuction of this game:
        
        ~~~~*** Every participant/user will attempt '5' rounds 
            and in each round random  quiz question  ***~~~~~ \n ''')
        
        list1 = [True,False,True,False,True]
        
        gainPoint = 0
        
        lossPoint = 0
        
        for i in range(5):
            computerGuess = random.choice(list1)
            
            print(" Guess what computer choice out of 'True / False'  ")
            
            userGuess = int(input('''
                                Press 1. For True
                                Press 0. For False \n'''))
            
            if (userGuess == 1) and (computerGuess == True) :
                
                print("congratulate you win : \n")
                gainPoint +=1
            
            if (userGuess == 0) and (computerGuess == False) :
                
                print("congratulate you win : \n")
                gainPoint +=1
            
            if (userGuess == 1) and (computerGuess == False) :
                
                print("hey you Loss ")
                lossPoint +=1 
                
            if (userGuess == 0) and (computerGuess == True) :
                
                print("hey you Loss ")
                lossPoint +=1 
                
        print("-------********---------- \n")
                
        print("participant details:")
        
        if gainPoint > lossPoint :
            
            print("Congratulate You are the winner ")
            print("Total Score is " ,(gainPoint + lossPoint))
            print("Participant Score",gainPoint)
            print("lossPoint is",lossPoint)
            
        if gainPoint < lossPoint :
            
            print(" You loss ")
            print("Total Score is " ,(gainPoint + lossPoint))
            print("Participant Score",gainPoint)
            print("lossPoint is",lossPoint)
            
        if gainPoint == lossPoint :
            
            print(" Draw ")
            print("Total Score is " ,(gainPoint + lossPoint))
            print("Participant Score",gainPoint)
            print("lossPoint is",lossPoint)
        
    else:
        
        print("Thanks For visiting this game Project \n")
        break
