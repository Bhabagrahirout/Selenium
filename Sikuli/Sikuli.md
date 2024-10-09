# Sikuli


### The screen Should be open so that it matches  the images.    
  
		Screen sc= new Screen();  


*		Check Element Present or not   
		 sc.wait("imgpath",10);  // it throws Exceptions   
					OR   
		 Match status=sc.exists("imgpath",10);  
		 if(status!=null)  
			System.out.println("element Found");   
		 else   
			System.out.println("element  Not Found");



		String imgpath="img1.png";
			Screen sc= new Screen();  
	
				
			
	
	
