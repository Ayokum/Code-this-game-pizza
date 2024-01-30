# This is my attempt at Code-this-game-pizza
#code this game pizza by meg ray


#set up Game

#import Libraries
import pygame
from pygame import *
#initialize pygame
pygame.init()

#define Window resolution
WINDOW_WIDTH = 900
WINDOW_HEIGHT = 400
WINDOW_RES = WINDOW_WIDTH, WINDOW_HEIGHT

#create game window
#to do Replace the argument in the set_mode method below
game_window = display.set_mode ((WINDOW_RES))
#Display caption

display.set_caption('Attack of the Vampire Pizzas!')

#------------------------------------------------------
#start main game loop
game_running = True
#game loop
while game_running:

#check for events
    
    #checking for and handling events
    for event in pygame.event.get():
        
        #exit loop on quit
        if event.type == QUIT:
            game_running = False

#update display
    display.update()
            
#close main game loop
#--------------------------------------------------
    
#Clean up game
pygame.quit()
            
