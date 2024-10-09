# Sikuli


### The screen Should be open so that it matches  the images.    
  
		 Screen sc= new Screen();
		  	OR 
		 Region elementRegion = new Region(x,y,w,h);  
		  Both have same functionality but screen for total screen and region for a specific palce
		 String imgpath="img1.png";


*		 Check Element Present or not  
		 sc.wait("imgpath",10);  // it throws Exceptions   
				OR   
		 Match status=sc.exists("imgpath",10);  
		 if(status!=null)  
			System.out.println("element Found");   
		 else   
			System.out.println("element  Not Found");
		 It's better to check if the image is present first, then perform the action .Match contains all the functionality of the Screen class.
		 

*		Click   
		 sc.click("imgpath");    
		   OR
		 status.click();  
		 If you don't provide any arguments, it will click in the middle of the screen. 
		 
		 
*		Double Click
		 status.doubleClick();
		
		
*		Right Click
		 status.rightClick();		
		
		
*		SendKeys / Type   
		 sc.click("imgpath");  
		 sc.type("tshirt");   
		 sc.type("tshirt",1);   // The second parameter indicates pressing the Shift key. There are many options available like 100 for window+alt
		 We can't directly send the values, so we must first click, then use sendKeys.


*		Screen height,width   
		 int height = sc.h;  
		 int width = sc.w;	  
		 int x = sc.x;	  // bydefault (x,y)=(0,0)
		 int y = sc.y;					
			
			
*		Element height,width   
		 Match status=sc.exists("imgpath",10);
		 int h=status.h;
		 int w=status.w;
		 int x=status.x;
		 int y=status.y;
		 
		 
*		Click using Coordinate   
		 Region elementRegion = new Region(x,y,w,h);   // first find coordinate   
		 elementRegion.click();   
			  OR
		 sc.click(elementRegion);
		  
		 
*		Click an Dynamic Element i.e changes its color or size    
		a)Match
			Match status=sc.exists("imgpath",10);  
		 	Region r=status.above(100);  
		 	r.click(); 
		 	OR
		 	status.above(100).click();   
		b)Region   
			Region elementRegion = new Region(x,y,w,h);   
			elementRegion.above(100).click();
		 	From imgpath element to upper 100px click     
			
		 
	
