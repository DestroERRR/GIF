# GIF
Programming 11 GIF Project

/* Programming 11
  GIF Project
  Jason.Shi April,18,2020
*/

ArrayList<PImage> gif;
int pic = 0;


void setup(){

  size(600,600);
  
  gif = new ArrayList<PImage>(); 
  
  int i = 0;
  
  while (i < 15) {
  
    String zero = ""; //empty string is 2 quotations side by side
    
    if (i < 10) zero = "0";
    
    gif.add(loadImage("frame_" + zero + i + "_delay-0.05s.gif"));
    
    i++;
    
  }
  
  
}

void draw(){

  PImage frame = gif.get(pic);
  
  image(frame, 0, 0, width,height);
  
  pic++;
  
  if (pic > 14) pic = 0;
  
}
