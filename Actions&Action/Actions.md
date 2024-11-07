# Actions  





*	Official Link:[https://www.selenium.dev/selenium/docs/api/java/org/openqa/selenium/interactions/Actions.html#dragAndDropBy(org.openqa.selenium.WebElement,int,int)]   
  	

		Actions action=new Actions(driver);
		WebElement ele=wd.findElement(By.id("male"));

*		Wait
		action.pause(Duration.ofSeconds(10)).perform();		
		
*		Scroll
		 action.moveToElement(ele).perform();  // the crusor move to the element
		 action.scrollToElement(ele).perform();   
		 action.scrollFromOrigin(WheelInput.ScrollOrigin.fromViewport(0, 0), 0, 600).perform();// from(x,y) to x,y

*		Move crusor pointer
		 action.moveByOffset(200, 50).doubleClick().perform(); 
		 action.moveToLocation(200,50).doubleClick().perform();			
		 //it does't show in UI  but goes
		
*		Click
		 action.click(element).perform();
		 or
		 action.moveToElement(element).click().perform();
		 
*		Double Click		 
		action.doubleClick(element).perform();

*		RightClick
		action.contextClick(ele).perform();

*		clickAndHold()  
		action.clickAndHold(ele).perform();		
		 
*		Sendkeys   
		action.sendKeys(element, "Bhaba").perform();	
		 
*		Sendkeys
			a)direct
				ele=wd.findElement(By.id("name"));
				action.sendKeys(ele, "Bhaba:").perform();   

			b)Through Keyboard
				action.keyDown(ele, "B").perform(); // we can press only one char at a time and caseSensitive
				action.keyDown("h").perform();	
				action.keyDown(Keys.SHIFT).perform();
				action.keyDown(Keys.SEMICOLON).perform();
				action.keyUp(Keys.SHIFT).perform();
				// for character kayUp() maynot needed but for Shift,ctrl,Alt etc require
				Keys keycode=Keys.getKeyFromUnicode('a');//it is use for  special characters or symbols that have associated key codes , not work for char
				action.keyUp(keycode).perform();	
			
*		Enter 
		 ele=wd.findElement(By.id("Wikipedia1_wikipedia-search-input"));
		 action.sendKeys(ele, Keys.ENTER).perform();
		 //OR direct through element
		 ele.sendKeys(Keys.ENTER);	
			
*		Page up,Down   
  
		 a)For a element           
		    ele=wd.findElement(By.id("male"));
		    ele.click();
		    ele.sendKeys(Keys.ARROW_UP);
		    //we can press more like pagedown,pageup,Tab etc   

		 b)For entire page
		    action.keyDown(Keys.PAGE_DOWN).perform(); 
		    action.keyUp(Keys.PAGE_DOWN).perform(); 
		    //scroll one page						 	
		 
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

			
				
		
 