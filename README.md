#JPaintApp
JPaintApp is a straightforward painting program created in Java using Swing. It lets users click and drag to create filled-in rectangles on a canvas.
#Features
Draw filled-in rectangles by clicking and dragging the mouse on the canvas. The mouse movement's size and direction will be reflected in the rectangle. Once the mouse is released, the rectangle will appear on the screen.
#Getting Started
Step 1: Import Required Libraries
The relevant Java libraries must be imported first in the code. The AWT (Abstract Window Toolkit) and Swing classes are included in the code to create the graphical user interface (GUI).
Step 2: Define Constants
CANVAS_WIDTH and CANVAS_HEIGHT, which indicate the drawing canvas's dimensions, as well as DEFAULT_PRIMARY_COLOR and DEFAULT_SECONDARY_COLOR, which establish the painting's default primary and secondary colors, are just a few of the constants defined in the code.
Step 3: JPaintApp Class
The primary class of the programme is JPaintApp. It oversees the drawing and shape-creation functions, initialises the canvas, and sets up the GUI window.
Step 4: JPaintApp Constructor
Several data structures, including lists for storing shapes and undo/redo stacks, are initialised by the JPaintApp constructor. Additionally, it returns the primary and secondary colors to their initial settings. Additionally, it creates a Canvas instance, sets up the JFrame, and adds mouse listeners to handle the generation and interaction of shapes.
Step 5: Mouse Listeners
Two MouseListeners are included in the code for the JPaintApp class. When a user clicks and holds the mouse button, the mousePressed listener begins producing a new form. When the user releases the mouse button, the mouseReleased listener completes the shape construction. The mouseDragged listener adjusts the shape's width and height when the user drags the mouse between the two events.
Step 6: Canvas Class
The Canvas class extends JPanel and is an inner class of JPaintApp. To manage the painting of forms on the canvas, it overrides the paintComponent function. The Graphics2D object is used by the paintComponent function to iteratively draw each shape in the list of shapes.
Step 7: Shape Abstract Class
The fundamental structure of all forms is represented by the Shape abstract class. It has getter and setter methods as well as position, dimension, and color fields. Additionally, it specifies an abstract drawShape method that the subclasses implement.
Step 8: Shape Subclasses
Several subclasses of the abstract Shape class, which represent various shapes, are included in the code. These comprise the shapes Triangle, FilledTriangle, OutlineAndFilledRectangle, Ellipse, and FilledEllipse. Every subclass implements the drawShape function, which uses the supplied Graphics2D object to draw each subclass's unique form.
Step 9: CreateShape Method
According to the user's choice of outline-only, filled-in, or outline and filled-in choices, the JPaintApp class's createShape method generates instances of various forms. In accordance with the selected settings, it returns a Shape object.
Step 10: Main Method
The application begins with the main method. It uses the SwingUtilities.invokeLater function to schedule the construction of the JPaintApp object, ensuring that the GUI is built and updated in the event dispatch thread.
Bugs (if any):
The application does not currently have a graphical user interface (GUI) that is user-friendly. Keyboard inputs are used by users to interact with the programme, as explained in the Usage section.
When selecting and removing overlapping shapes, the programme might not handle them properly.
