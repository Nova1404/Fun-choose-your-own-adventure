# Fun-choose-your-own-adventure
Just a nice choose your own adventure, does try to kill you


# Code for the game
def wake():
    print('You just woke up, (1) would you like to go back to sleep? or (2)Open the front door and start an adventure (3) Combust into a ball of flames')
def bridge():
    print('You walk up to the bridge and find a troll, he asks for 10 Gold')
def cave():
    print('You walk over to the cave, you see a torch hanging from the wall ')
def hold():
    print('hold')
def bridgescence():
    print('you remeber there being a torch next to the bridge, would you like to grab it?: ')
    choice = int(input('1: Yes 2: No: '))
    if(choice == 1):
        print('You go back to the the start of the bridge, and you walk to grab it, you grab the torch, you walk to the end of the bridge')
        arson()
    elif(choice == 2):
        print('You proceed to drown')
        print('remember kids, arson is fun!')
def arson():
    burn = int(input('Would you like to burn down the village? 1:Y / 2:N '))
    if(burn == 1):
        print('you throw the torch just in time, as you notice the fact it started to burn your clothes')
        print('As the village burns slowly you see a dragon, you admire it for a moment in all of its glory, you watch it come down as you raise your sword....')
        print('The end?')
    elif(burn == 2):
        print('you keep holding onto the torch and its too late, you have burned alive')

gold = 10
sword = 0
torch = 0


try:
    grab = int(input('Would you like to grab your sword? 1: Yes 2: No: '))
    if(grab == 1):
        print('You grab the sword from the rack')
        sword = 1
    elif(grab == 2):
        print('You leave the sword in its rack')
    wake()
    select1 = int(input('Please choose: '))
    if(select1 == 1):
        print("You ended up sleeping until the end of time")
    elif(select1 == 2):
        start = int(input('You open the front door smelling the fresh air, you see a bridge and a cave, where would you like to go? 1: Bridge 2: Cave: '))
        if(start == 1):
            bridge()
            troll = int(input('1: Give gold 2: Attack: '))
            if (troll == 1):
                if(gold >= 10):
                    print("The troll lets you pass -10 gold")
                    gold -= 10
                    print('you have', gold, 'gold')
                    print('You cross the bridge and see a village')
                    bridgescence()
                    
                elif(gold < 10):
                    print('you dont have enough')
                    print('the troll kills you')
            elif(troll == 2):
                if(sword == 1):
                    print("You attack the Troll, +10 gold")
                    gold += 10
                    print('you have', gold, 'gold')
                    print('You cross the bridge and see a village')
                    bridgescence()
                    

                elif(sword == 0):
                    print("You got curb stomped L")
        elif(start == 2):
            cave()
            grabt = int(input('Would you like to grab the torch? 1:Yes 2:No '))
            if(grabt == 1):
                print('You grab the torch')
                print('Would you like to dwell further into the cave?: ')
                dwell = int(input('1: Yes 2: No: '))
                if(dwell == 1):
                    print('you go into the cave ligting the way as you go')
                    rl = int(input('You see 2 ways, one up, one down which do you choose? 1:up 2: Down '))
                    if(rl == 1):
                        print('you go up the cave more, you find a medow with a sleeping dragon')
                        fight = int(input('Do you fight the dragon? 1: Yes 2: No '))
                        if(fight == 1):
                            if(sword == 1):
                                print('You fight the dragon and it is a hard fight, but you win, you head back home and lay down, you rest your eyes proud of your work')
                            elif(sword == 0):
                                print('You approach the dragon, you prepare to strike it when you realize you didnt get your sword, the beast wakes up and kills you')
                                print('You have died')
                        elif(fight == 2):
                            print('you slip your next step and fall into the cave, you hit your head on the bottom rock')
                            print('You have died')
                    elif(rl == 2):
                        print('You go down')
                        spid = int(input('You dwell further into the depths of the cave where you find a spider, 1: Attack 2: Dont attack '))
                        if(spid == 1):
                            if(sword == 1):
                                print('You attack the spider finding a book, it has 2 options')
                                wish = int(input('Wish 1: Kill the dragon freeing the village, Wish 2: End your adventure '))
                                if(wish == 1):
                                    print('You hear a loud rumble, you quickly exit the cave to see what it was, you see a dragon dead on the ground')
                                    print('The dragon is slain, you go back home and rest, your adventure complete')
                                elif(wish == 2):
                                    print('You hear a voice, or is it a voice? it sounds familiar, it says your soul shall be mine for the taking, next thing you see is fire')
                                    print('You have been sent to the depths of hell')
                        elif(swprd == 2):
                            print('The spider eats you')
                            print('You have died')
                elif(dwell == 2):
                    print('Your clothes catch fire')
                    print('You die')
            elif(grabt == 2):
                print('You dont grab the torch, when suddenly your pulled into the depths and get eaten')
    elif(select1 == 3):
        print("You died.")
except:
    print("Invalid input")
