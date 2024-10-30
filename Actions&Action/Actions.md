# Actions  


	


*	Official Link:[https://www.selenium.dev/selenium/docs/api/java/org/openqa/selenium/interactions/Actions.html#dragAndDropBy(org.openqa.selenium.WebElement,int,int)]   
  	

		Actions action=new Actions(driver);
		
		
*		Click
		 WebElement element=wd.findElement(By.xpath("//button[@name=\"start\"]"));
		 action.click(element).perform();		
		 
*		Double Click		 
		 action.doubleClick(element).perform();
		 
*		Sendkeys   
		 action.sendKeys(element, "Bhaba").perform();		
		 
*		KeyBoard   
  
		 1)sendkeys     
			a)first click an input, then pass  
				action.keyDown(Keys.SHIFT).perform();
				action.keyDown("a").perform();
				Keys keycode=Keys.getKeyFromUnicode('a');//it is not work 
				action.keyUp(Keys.SHIFT).perform();
				// for character kayUp() maynot needed but for Shift,ctrl,Alt etc require
			b)without click
				action.keyDown(ele, "a").perform(); // we can press only one char at a time
		 2)actions   
			 		
		 
*		Drag and Drop	  
  
		 a)Element   
			WebElement source=wd.findElement(By.xpath("//p[text()='Drag']"));
			WebElement dest=wd.findElement(By.id("droppable")); 
			action.dragAndDrop(source, dest).perform();  
		 
   		 b)Slider   
			WebElement draw=wd.findElement(By.xpath("//*[@id='slider']/span"));
			action.dragAndDropBy(draw,150, 0).perform();  
  
		c)Resizeable (TextBox)   
			WebElement resize=wd.findElement(By.xpath("//*[@id='resizable']/div[3]"));
			action.dragAndDropBy(resize,300,0).perform(); // x, y start from the element   

*		Wait   
			action.pause(Duration.ofSeconds(10)).perform();
			
*					
		
 