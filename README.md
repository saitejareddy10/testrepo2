def __init__(self, x=0, y=0, dest=None):
        self.t = turtle.Turtle()
        self.t.speed(0)
        
        self.t.up()
        self.t.goto(x, y)
        self.t.down()
        
        if dest is None:
            # use start point as destination point
            self.destination(x, y)
        else:
            self.destination(*dest)
            
        # it is needed by `move` to execute `ontimer`
        self.screen = turtle.Screen()

        # start moving
        self.move() 
wtf
