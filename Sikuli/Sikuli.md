# Sikuli


### The screen Should be open so that it matches  the images.    
  
		 Screen sc= new Screen();  
		 String imgpath="img1.png";


*		Check Element Present or not   
		 sc.wait("imgpath",10);  // it throws Exceptions   
				OR   
		 Match status=sc.exists("imgpath",10);  
		 if(status!=null)  
			System.out.println("element Found");   
		 else   
			System.out.println("element  Not Found");


*		Click   
		 sc.click("imgpath"); 
		
*		SendKeys / Type   
		 sc.click("imgpath");  
		 sc.type("tshirt");    
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
	
	
