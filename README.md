# Tic-Tac-Toe-Using-Ursina

Tic Tac Toe is a two-player game that is played on a 3x3 grid. The game is played by placing X's and O's in the empty cells of the grid, with one player using X's and the other player using O's. The objective of the game is to get three X's or O's in a row, either horizontally, vertically, or diagonally. The first player to get three in a row wins the game. If all cells are filled without any player achieving three in a row, the game is a draw.

## Instructions to run the game

* Open the Github repository where the game code is hosted.

* Click on the green "Code" button and then select "Download ZIP" to download the code as a ZIP file.

* Extract the ZIP file to a folder on your computer.

* Open a command prompt or terminal window and navigate to the folder where you extracted the code.

* Type ```python tic.py``` and press Enter to start the game.

* Follow the prompts to play the game.

## Functionality of the code

* ```from ursina import *``` - Import the Ursina game engine.

* ```if __name__ == '__main__'```: - A conditional statement that checks if the script is being run as the main program.

* ```app = Ursina()``` - Create an instance of the Ursina game engine.

* ```camera.orthographic = True``` - Set the camera to use an orthographic projection.

* ```camera.fov = 4``` - Set the camera's field of view.

* ```camera.position = (1, 1) ```- Set the camera's position.

* ```Text.default_resolution * = 2 ```- Double the default resolution for text objects.

* ```player = Entity(name='o', color=color.azure)``` - Create an entity to represent the current player.

* ```cursor = Tooltip(player.name, color=player.color, origin=(0,0), scale=4, enabled=True)``` - Create a tooltip to show the current player's name and color.

* ```cursor.background.color = color.clear ```- Set the background color of the tooltip to be transparent.

* ```bg = Entity(parent=scene, model='quad', texture='shore', scale=(16,8), z=10, color=color.light_gray)``` - Create a background entity for the game.

* ```mouse.visible = False``` - Hide the mouse cursor.

* ```board = [[None for x in range(3)] for y in range(3)] ```- Create a 3x3 matrix to store the buttons in.

* ```for y in range(3):``` - Loop through the rows of the matrix.

* ```for x in range(3):``` - Loop through the columns of the matrix.

* ```b = Button(parent=scene, position=(x,y))``` - Create a button entity and set its position.

* ```board[x][y] = b``` - Store the button entity in the matrix.

* ```def on_click(b=b):``` - Define a function that will be called when the button is clicked.

* ```b.text = player.name``` - Set the text of the button to be the current player's name.

* ```b.color = player.color``` - Set the color of the button to be the current player's color.

* ```b.collision = False``` - Disable the collision of the button so it cannot be clicked again.

* ```check_for_victory()``` - Check if the current player has won the game.

* ```if player.name == 'o': ```- Check if the current player is 'o'.

* ```player.name = 'x'``` - Set the current player to 'x'.

* ```player.color = color.orange``` - Set the current player's color to orange.

* ```else:``` - If the current player is 'x', set it to 'o'.

* ```player.name = 'o'```

* ```player.color = color.azure```

* ```cursor.text = player.name ```- Set the tooltip's text to be the current player's name.

* ```cursor.color = player.color``` - Set the tooltip's color to be the current player's color.

* ```b.on_click = on_click``` - Set the button's on-click function to be the on_click function.

* ```def check_for_victory():``` - Define a function to check if the current player has won the game.

* ```name = player.name``` - Get the name of the current player
