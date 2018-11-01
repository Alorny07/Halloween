# Halloween
def setup ():
    size (640,480)

x = 0
y = 0
def draw ():
    global x
    x += 3
    if x > 340:
        x = 340
    global y
    y += 3
    fill(255,165,0)
    background ("#7f1fe5")
    noStroke()
    fill ("#f0f5d8")
    
#draw ghost
    fill ("#f0f5d8")
    ellipse (x, 400, 50,50 ) #ghost's head
    rect(x-25, 400, 50,300)  #ghost's body
    noStroke()
    fill ("#000000")
    ellipse (x-10, 400,10,10)
    ellipse (x+10,400,10,10)
    fill ("#000000")
    triangle (x-20, 428, x-15, 438, x+5, 420)
    triangle (x+25, 420, x+25, 430, x+50, 410)
    
#draw hat
    fill ("#000000")
    rect (x-32, 375, 62, 10)
    rect (x-22, 360, 40, 20)
    
#draw light
    fill ("#000000")
    rect (x+45, 412, 3, 30) 
    fill ("#FF8C00")  
    ellipse (x+48,435,20,20)
    

#draw house
    fill(0)
    rect(400,200,200,480)
    fill(255)
    rect(525,390,50,50)
    rect(425,310,50,50)
    rect(525,310,50,50)
    rect(425,230,50,50)
    rect(525,230,50,50)
    fill("#8B4513")
    rect(425,390,50,90)
    fill("#FFFF00")
    ellipse(465,435,10,10)  #draw the house
    
#draw candy
    ellipse( 50, y, 10,10) 
    ellipse (100,y+180,10,10)
    ellipse (150,y-10,10,10)
    ellipse (200,y+60,10,10)
    ellipse (250,y-20,10,10)
    ellipse (300,y+80,10,10)
    ellipse (350,y-50,10,10)
    ellipse (400,y+60,10,10)
    ellipse (450,y-100,10,10)
    ellipse (500,y+40,10,10)
    ellipse (550,y+160,10,10)
    fill("#f0f5d8")

# text    
def mousePressed():
    if x == 340:
        textSize(68)
        text("HAPPY HALLOWEEN", CENTER, 240)
