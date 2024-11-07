# Action 


  ##### Through Action interface first build and store multiple actions ,then perform
		
		Actions action=new Actions(wd);
		Action multiAct=action.moveToElement(ele).click().build();
		multiAct.perform();
				