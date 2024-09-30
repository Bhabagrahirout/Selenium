# JavaScriptExecutor



	JavascriptExecutor js = (JavascriptExecutor) wd;

*		 launch site
		js.executeScript("window.location='https://google.com'");

*		 coloring
		WebElement element1 = wd.findElement(By.cssSelector("textarea[name=\"q\"]"));
		js.executeScript("arguments[0].style.border='3px solid red'", element1); 
		js.executeScript("document.body.style.backgroundColor = 'yellow';"); 

		
*		Zoom
		js.executeScript("document.body.style.zoom = '40%';"); 
		
*		 return
		Object domain_name = js.executeScript("return document.domain");
		Object yOffSet = js.executeScript("return window.pageYOffset");
		Object scrollHeight = js.executeScript("return document.body.scrollHeight");  
		Many More....

*		send text
		js.executeScript("arguments[0].value = 'Selenium WebDriver';", element1);

*		click
		js.executeScript("arguments[0].click();", element1);

*		Double click
		js.executeScript("arguments[0].dispatchEvent(new MouseEvent('dblclick', { bubbles: true }));", element1);

*		context click(Right Click)
		js.executeScript("arguments[0].dispatchEvent(new MouseEvent('contextmenu', { bubbles: true }));", element1);

*		remove and add attribute
		js.executeScript("arguments[0].removeAttribute('disabled');", element1);
		js.executeScript("arguments[0].setAttribute('disabled');", element1);
		js.executeScript("arguments[0].setAttribute('country','india');", element1);
		js.executeScript("arguments[0].removeAttribute('id','sname');", element1);
		
		

*		Vertican scroll
		--By Pixel
		js.executeScript("window.scrollBy(0,1000)"); //downward
		js.executeScript("window.scrollBy(0,-1000)");//upward   
	    --By visibleText
		js.executeScript("arguments[0].scrollIntoView();", element1);	  
		--By height
		js.executeScript("window.scrollTo(0,document.body.scrollHeight)");   
		--Horizental scroll
		js.executeScript("arguments[0].scrollIntoView();", element1);   


*		 create alert
		try {
			js.executeScript("alert('hii')");
			Thread.sleep(1000);
			Alert alert = wd.switchTo().alert();
			String str = alert.getText();
			System.out.println(str);
			alert.accept();
		} catch (Exception e) {
			e.printStackTrace();
		}
		through document we can get many things like create alert,
		
		
		
*		 we can do multiple action at a time
		js.executeScript("arguments[0].value = arguments[1];arguments[2].click(); arguments[3].removeAttribute('disabled');",element1, "Selenium WebDriver", element1, element1);  
		 first index value for 1st arguments
				
				
	


