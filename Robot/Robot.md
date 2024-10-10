# Robot


		Robot rb=new Robot();

		
*		KeyPress	  
		 rb.keyPress(KeyEvent.VK_TAB);
		 rb.keyRelease(KeyEvent.VK_TAB);  
			OR
		 int keyCod=KeyEvent.VK_A; 
		 int keyCode = KeyEvent.getExtendedKeyCodeForChar('a'); // it take only char
		 rb.keyPress(keyCod);
		 rb.keyRelease(keyCod);			
		 Every key has a keyCode ,we can direcctly pass it (For symbol and other things you manage accordingly)  
		 if (!char.isLetterOrDigit(c)) {
		    robot.keyPress(KeyEvent.VK_SHIFT);
		    robot.keyPress(keyCode);
		    robot.keyRelease(keyCode);
		    robot.keyRelease(KeyEvent.VK_SHIFT); }
		            
		
*		Move to element	  
		 rb.mouseMove(500, 500);			
		 
		 
*		Mouse Press	  
		 rb.mousePress(InputEvent.BUTTON1_DOWN_MASK);  
		 rb.mouseRelease(InputEvent.BUTTON1_DOWN_MASK);	  
		 BUTTON1 for left, BUTTON2 for middle, BUTTON3 for right   
            
            
*		Scroll			
		 rb.mouseMove(x, y);
		 rb.mouseWheel(5);
	     First move to the page, then scroll using the mouse wheel 
	     
	     
*		Wait   
		 rb.delay(10000); // like sleep()   


*		Delay   
		 rb.setAutoDelay(1000);	    
		 Set a delay to allow time for performing actions. It completes its tasks as usual but keeps   
 		 the processor occupied for this duration.(time taken to perform an Action)
		    
	     
	     
	     
	     
            
             