#set up Game

#import Libraries
import pygame
from pygame import *
#initialize pygame
pygame.init()

#define Window resolution
WINDOW_WIDTH = 1100
WINDOW_HEIGHT = 600
WINDOW_RES = WINDOW_WIDTH, WINDOW_HEIGHT

#define tiel parameters
WIDTH = 100
HEIGHT = 100
#to do: add height here

#define colors
WHITE = 255, 255, 255


#create game window
#to do Replace the argument in the set_mode method below
game_window = display.set_mode ((WINDOW_RES))
#Display caption

display.set_caption('Attack of the Vampire Pizzas!')

#load Background image
background_img = image.load('restaurant.jpg')

#convert image to surf
background_surf = Surface.convert_alpha(background_img)
BACKGROUND = transform.scale(background_surf,WINDOW_RES)


#set up the enemy image

    #load the image into the program
pizza_img = image.load('vampire.png')
    
        #convert the image to a surface
pizza_surf = Surface.convert_alpha(pizza_img)
VAMPIRE_PIZZA = transform.scale(pizza_surf, (WIDTH, HEIGHT))

#------------------------------------------------------------------
        #initialize and draw background, enemy, and grid 
tile_color = WHITE
#populate grid
for row in range(6):
    for column in range (11):
        draw.rect(BACKGROUND, tile_color,
                  (WIDTH * column, HEIGHT * row, WIDTH, HEIGHT), 1)

game_window.blit(BACKGROUND, (0, 0))        
game_window.blit(VAMPIRE_PIZZA, (900, 400))


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
            
