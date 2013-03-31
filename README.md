#DCPathButton  
### __________Create by Tangdixi
#Date:2013/3/25
---------------------

How to use DCPathButton:
=================================================
### Create a dcPathButton

     DCPathButton *dcPathButton=[[DCPathButton alloc]initWithButtonCount:count 
								totalRadius:totalRadius 
							       centerRadius:centerRadius 
								centerImage:centerImage
					              centerBackgroundImage:centerBackgroundImage 
						 centerButtonHighLightImage:centerButtonHighLightImage 
						 	       buttonRadius:buttonRadius 
						      buttonBackgroundImage:buttonBackgroundImage 
						               buttonImages:buttonImages];	
### Custom Your Button Action
	  [dcPathButton.button_tag addTarget:self 
					  action:@selector(button_tag_Press:) 
				forControlEvents:UIControlEventTouchUpInside];
	  - (IBAction)button_tag_Press:(id)sender{}  

### Parameter illustrte

	  -- Parameter illustrte
	  Count: How many button you want to show, range between 3 to 5, if you set this parameter above 
	         5,it will set the maximum value 5, the same to the minimum value 3.
	  TotalRadius: The radius that whole the buttons expanded, maximum half screen width minus button
	               radius, this parameter shouldn't be 0.
	  CenterRadius: The center button's radius, shouldn't be nil but it already have a normal radius,
	                maximum 100.
	  ButtonRadius: The button which around the center button, they will have a same radius you give,
	                shouldn't be nil but have a normal radius, maximum 80.
	  ButtonImages: Use an array to save whole the button images, you have to keep the images' number
	                equal to the parameter count, or greater than it.
	  CenterBackgroundImage & buttonBackgroundImage: If you set this parameter nil, it will use the 
	    						   normal background image, hope you like it. (^_^)
	
	
### The tag in Three different button types

	  ***********************************************************************************************
	
	  Button tag: For example, you want to add a new image in (0),just add it in the buttonImags
	                array at index 0.
	
	  *-------------------------------------------------------------------------------------------*
	  |                                                                                           |
	  |              (0)     (1)                 (0)     (1)                   (0)     (1)        |
	  |                                                                                           |
	  |                 \   /                       \   /                         \   /           |
	  |     (type_1) ->  (x)           (type_2) ->   (x)             (type_3) ->   (x)            |
	  |                   |                         /   \                         / | \           |
	  |                                                                       (3)       (4)       |
	  |                  (2)                     (2)     (3)                       (2)            |
	  |                                                                                           |
	  *-------------------------------------------------------------------------------------------*
	
	  ***********************************************************************************************