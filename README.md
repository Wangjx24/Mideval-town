# Mideval-town
public class medievaltown{
	
	public static void main(String[] args){
	Turtle t = new Turtle();
	t.delay(0);
	medievaltown(t);
	}

	//draw/combine the medieval town with all the functions
	public static void medievaltown(Turtle t){
	t.penup();
	t.backward(400);
	t.left(90);
	t.forward(400);
	t.right(90);
	t.pendown();
	//move the turtle to start at an appropriate location
	starsky(t);
	//draw the stars in the sky
	t.penup();
	t.backward(50);
	t.right(90);
	t.forward(160);
	t.left(90);
	t.pendown();
	//move the turtle to the location for the mountain 
	multimountain(t);
	t.penup();
	t.right(90);
	t.forward(150);
	t.left(90);
	t.forward(80);
	t.pendown();
	//move the turtle to the location for the tower
	tower(t);
	t.penup();
	t.forward(50);
	t.pendown();
	//move the turtle to the location for the wall
	wall(t);
	t.penup();
	t.forward(80);
	t.pendown();
	//move the turtle to the location for the arc
	arc(t);
	t.penup();
	t.forward(40);
	t.pendown();
	//move the turtle to the location for the second wall
	wall(t);
	t.penup();
	t.forward(80);
	t.pendown();
	//move the turtle to the location for the second tower
	tower(t);
	t.penup();
	t.forward(80);
	t.left(90);
	t.forward(30);
	t.right(90);
	t.pendown();
	//move the turtle to the location for the arces
	arces(t);
	t.penup();
	t.forward(70);
	t.right(90);
	t.forward(50);
	t.left(90);
	t.pendown();
	//move the turtle to the location for the treegrid
	treegrid(t);
	t.penup();
	t.backward(430);
	t.left(90);
	t.forward(335);
	t.right(90);
	t.pendown();
	//move the turtle back to the orginal starting point
	}

	//draw one star
	public static void star(Turtle t){
		for(int i = 0; i < 8; i++){
			t.forward(10);
			t.penup();
			t.backward(10);
			t.right(360.0 / 8);
			t.pendown();
		}
	}

	public static void starsky(Turtle t){
		//draw the sky that contains multiple stars
		star(t);
		t.penup();
		t.right(90);
		t.forward(40);
		t.left(90);
		t.forward(40);
		t.pendown();
		//move the turtle to the location for the second star, draw the star
		star(t);
		t.penup();
		t.forward(40);
		t.left(90);
		t.forward(40);
		t.right(90);
		t.pendown();
		//move the turtle to the location for the third star, draw the star
		star(t);
		t.penup();
		t.forward(80);
		t.left(90);
		t.forward(30);
		t.right(90);
		t.pendown();
		//move the turtle to the location for the fourth star, draw the star
		star(t);
		t.penup();
		t.right(90);
		t.forward(70);
		t.left(90);
		t.forward(40);
		t.pendown();
		//move the turtle to the location for the fifth star, draw the star
		star(t);
		t.penup();
		t.forward(130);
		t.left(90);
		t.forward(50);
		t.right(90);
		t.pendown();
		//move the turtle to the location for the sixth star, draw the star
		star(t);
		t.penup();
		t.right(90);
		t.forward(60);
		t.left(90);
		t.forward(60);
		t.pendown();
		//move the turtle to the location for the seventh star, draw the star
		star(t);
		t.penup();
		t.forward(80);
		t.left(90);
		t.forward(50);
		t.right(90);
		t.pendown();
		//move the turtle tot eh location to the eigth star, draw the star
		star(t);
		t.penup();
		t.backward(470);
		t.pendown();
	}

	//draw one mountain, first turn the turtle to the right angle
	public static void mountain(Turtle t){
		t.left(26.6);
		t.forward(Math.sqrt(35300));
		t.right(90);
		t.forward(Math.sqrt(18000));
	}

	//draw the multimountain, move the turtle to the next location after drawing the previous one
	public static void multimountain(Turtle t){
		mountain(t);
		t.penup();
		t.left(63.4);
		t.backward(40);
		t.left(90);
		t.forward(80);
		t.right(90);
		t.pendown();
		//move the turtle to the location for the second mountain, draw the mountain
		mountain(t);
		t.penup();
		t.left(63.4);
		t.backward(10);
		t.left(90);
		t.forward(20);
		t.right(90);
		t.pendown();
		//move the turtle to the location for the third mountain, draw the mountain
		mountain(t);
		t.penup();
		t.left(63.4);
		t.backward(630);
		t.left(90);
		t.forward(20);
		t.right(90);
		t.pendown();
		//move the turtle back to the original starting location
	}

	//draw one window on the tower
	public static void window(Turtle t){
		for(int i = 0; i < 4; i++){
			t.forward(10);
			t.left(90);
		}
	}

	//draw the 2 windows in one line on the tower
	public static void windowline(Turtle t){
		for(int i = 0; i < 2; i++){
			window(t);
			t.penup();
			t.forward(20);
			t.pendown();
		}
		t.penup();
		t.backward(40);
		t.pendown();
	}

	//draw the grid of window with the window line
	public static void windowgrid(Turtle t){
		for(int i = 0; i < 3; i++){
			windowline(t);
			t.penup();
			t.left(90);
			t.forward(20);
			t.right(90);
			t.pendown();
		}
		t.penup();
		t.left(90);
		t.backward(60);
		t.right(90);
		t.pendown();
		//move the turtle back to original starting location
	}

	//draw the outline of the tower
	public static void toweroutline(Turtle t){
		t.left(90);
		t.forward(100);
		t.left(63.4);
		t.forward(Math.sqrt(5) * 10);
		t.right(63.4);
		t.forward(10);
		//draw the top "zigzag" part of the tower
		for (int i = 0; i < 4; i++){
			t.forward(10);
			t.right(90);
			t.forward(10);
			t.right(90);
			t.forward(10);
			t.left(90);
			t.forward(10);
			t.left(90);
		}
		//the rest of the outline
		t.forward(10);
		t.right(90);
		t.forward(10);
		t.right(90);
		t.forward(20);
		t.right(63.4);
		t.forward(10 * Math.sqrt(5));
		t.left(63.4);
		t.forward(100);
		t.right(90);
		t.forward(50);
		t.left(90);
		t.left(90);
	}

	//draw the tower, combine the outline and the windowgrid together
	public static void tower(Turtle t){
		toweroutline(t);
		t.penup();
		t.forward(10);
		t.left(90);
		t.forward(40);
		t.right(90);
		t.pendown();
		//move the turtle to the locaiton for the windows, draw the window
		windowgrid(t);
		t.penup();
		t.backward(10);
		t.right(90);
		t.forward(40);
		t.left(90);
		t.pendown();
		//move the turtle back to the original starting location
	}

	//draw one rectangle for the wall
	public static void rect(Turtle t){
		for (int i = 0; i < 2; i++){
			t.forward(10);
			t.left(90);
			t.forward(5);
			t.left(90);
		}
	}

	//draw one square for the wall
	public static void square(Turtle t){
		for (int i = 0; i < 4; i ++){
			t.forward(5);
			t.left(90);
		}
	}

	//draw one line of the wall that starts with the rectangle
	public static void wallline1(Turtle t){
		for (int i = 0; i < 8; i++){
			rect(t);
			t.penup();
			t.forward(10);
			t.pendown();
		}
		t.penup();
		t.backward(80);
		t.pendown();
		//move the turtle back 
	}

	//draw one line of the wall that starts with the square
	public static void wallline2(Turtle t){
		square(t);
		t.penup();
		t.forward(5);
		t.pendown();
		//draw the middle rectangles for the wall
		for (int i = 0; i < 7; i++){
			rect(t);
			t.penup();
			t.forward(10);
			t.pendown();
		}
		//draw the last square for the line
		square(t);
		t.penup();
		t.backward(75);
		t.pendown();
		//move the turtle back
	}

	//draw the wall by combining the 2 different types of wallline together
	public static void wall(Turtle t){
		//3 sets of the wallline1 and wallline2
		for (int i = 0; i < 3; i++){
			wallline1(t);
			t.penup();
			t.left(90);
			t.forward(5);
			t.right(90);
			t.pendown();
			wallline2(t);
			t.penup();
			t.left(90);
			t.forward(5);
			t.right(90);
			t.pendown();
		}
		//one last wallline1
		wallline1(t);
		t.penup();
		t.left(90);
		t.backward(30);
		t.right(90);
		t.pendown();
		//move the turtle back to the original starting point
	}

	//draw the outer (bigger) arc of the arc
	public static void outerarc(Turtle t){
		for (int i = 0; i < 180; i ++){
			t.forward(Math.PI * 20 / 180);
			t.left(1);
		}
	}

	//draw the inner (smaller)arc of the arc
	public static void innerarc(Turtle t){
		for (int i = 0; i < 180; i ++){
			t.forward(Math.PI * 10 / 180);
			t.left(1);
		}
	}

	//draw the base part of the arc
	public static void arcbase(Turtle t){
		for(int i = 0; i < 2; i++){
			t.left(90);
			t.forward(30);
			t.penup();
			t.backward(30);
			t.right(90);
			t.pendown();
			t.forward(10);
			t.left(90);
			t.forward(30);
			t.penup();
			t.backward(30);
			t.right(90);
			t.forward(20);
			t.pendown();
		}
		//move the turtle back to the original location
		t.penup();
		t.backward(60);
		t.pendown();
	}

	//draw the whole arc by combining the parts together
	public static void arc(Turtle t){
		arcbase(t);
		t.penup();
		t.forward(30);
		t.left(90);
		t.forward(30);
		t.pendown();
		//draw the base part and the move the turtle to the location for the inner arc, draw the inner arc
		innerarc(t);
		t.penup();
		t.left(90);
		t.forward(30);
		t.left(90);
		t.pendown();
		//move the turtle to the location for the location for the outer arc, draw the outer arc 
		outerarc(t);
		t.penup();
		t.forward(30);
		t.left(90);
		t.pendown();
		//move the turtle back to the original starting location
	}

	//draw the 3 arces grid with the existing arc
	public static void arces(Turtle t){
		for(int i = 0; i < 3; i++){
			arc(t);
			//move the turtle to the location for the next arc
			t.penup();
			t.forward(50);
			t.left(90);
			t.forward(20);
			t.right(90);
			t.pendown();
		}
		t.penup();
		t.backward(150);
		t.right(90);
		t.forward(60);
		t.left(90);
		t.pendown();
		//move the turtle back to the original starting location
	}

	//draw one tree
	public static void tree(Turtle t){
		//draw the trunk of the tree
		t.left(90);
		t.forward(40);
		t.penup();
		t.backward(20);
		t.pendown();
		//draw the right side of the branches of the tree
		for(int i = 0; i < 5; i++){
			t.right(135);
			t.forward(Math.sqrt(2) * 10);
			t.penup();
			t.backward(Math.sqrt(2) * 10);
			t.left(135);
			t.forward(5);
			t.pendown();
			//move the turtle to the next location after drawing each branch
		}
		//move the turtle back for the left side of the branches
		t.penup();
		t.backward(25);
		t.pendown();
		//draw the left side of the branches of the tree
		for(int i = 0; i < 5; i++){
			t.left(135);
			t.forward(Math.sqrt(2) * 10);
			t.penup();
			t.backward(Math.sqrt(2) * 10);
			t.right(135);
			t.forward(5);
			t.pendown();
			//move the turtle to the next location after drawing each branch
		}
		t.penup();
		t.backward(45);
		t.right(90);
		t.pendown();
		//move the turtle back the original starting location
	}

	//draw a line of tree
	public static void treeline(Turtle t){
		for(int i = 0; i < 4; i++){
			tree(t);
			t.penup();
			t.forward(30);
			t.pendown();
			//move the turtle to the next location after drawing each tree
		}
		t.penup();
		t.backward(120);
		t.pendown();
		//move the turtle back to the original staring location
	}

	//draw a grid of tree with the treeline
	public static void treegrid(Turtle t){
		for (int i = 0; i < 2; i++){
			treeline(t);
			t.penup();
			t.forward(40);
			t.left(90);
			t.forward(40);
			t.right(90);
			t.pendown();
			//move the turtle to the next location after a line
		}
		t.penup();
		t.backward(80);
		t.right(90);
		t.forward(100);
		t.left(90);
		t.pendown();
		//move the turtle back to the oringal starting location
	}


}
