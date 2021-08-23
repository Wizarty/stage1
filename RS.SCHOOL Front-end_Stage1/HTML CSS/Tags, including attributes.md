#html/css

# Genereal
-   All HTML elements can have **attributes**
-   The `href` attribute of `<a>` specifies the URL of the page the link goes to
-   The `src` attribute of `<img>` specifies the path to the image to be displayed
-   The `width` and `height` attributes of `<img>` provide size information for images
-   The `alt` attribute of `<img>` provides an alternate text for an image
-   The `style` attribute is used to add styles to an element, such as color, font, size, and more
-   The `lang` attribute of the `<html>` tag declares the language of the Web page
-   The `title` attribute defines some extra information about an element

# Body tag and attributes

`<BODY>...</BODY>`	Contains the viewed portion of the document
`<BODY bgcolor="color">` Sets the color of the background in hexadecimal code
`<BODY background="filename.xxx">`	Sets an image as a page's background (wallpaper)
`<BODY text="color">`	Specifies the color of normal text in hexadecimal code
`<BODY link="color">`	Specifies the default color of unvisited links in hexadecimal code
`<BODY alink="color">`	Specifies the color of links on click in hexadecimal code
`<BODY vlink="color">`	Specifies the color of followed links in hexadecimal code
 
# Font tag and attributes

`<FONT>...</FONT>`	Changes font attributes for text within the tags
`<FONT size="value">...</FONT>`	Sets the font to a size from 1 to 7, with 1 the smallest and 7 the largest
`<FONT face="name">...</FONT>`	Sets the font face
`<FONT color="color">...</FONT>`	Sets the font color using hexadecimal code

# Image tag and attributes

`<IMG>`	Embeds an image in the document at the location of the tag
`<IMG src="url" alt="text">`	Adds an image with a text description
`<IMG src="url" alt="text" align="direction">`	Aligns an image to the left, right, center, bottom, or top
`<IMG src="url" alt="text" border="number">`	Sets the size of the border around an image
`<IMG src="url" alt="text" height="pixels">`	Sets the height of an image
`<IMG src="url" alt="text" width="pixels">`	Sets the width of an image
`<IMG src="url" alt="text" hspace="pixels">`	Sets a horizontal margin to be placed around an image
`<IMG src="url" alt="text" vspace="pixels">`	Sets a vertical margin to be placed around an image
`<IMG src="url" alt="text" usemap="map-name">`	Designates an image as a client-side image map
 
# Anchor tag and attributes
	
`<A>...</A>`	Designates the origin and destination of a hyperlink
`<A HREF="url">...</A>`	Creates a hyperlink
`<A HREF="#NAME">...</A>`	Links to a target location in the current page
`<A HREF="URL#NAME">...</A>`	Links to a target location in a page outside your site
`<A NAME="NAME">...</A>`	Sets a target location within a document
`<A HREF="mailto:email">...</A>`	Creates a mailto link

# Optional attributes:
	
`<A HREF="?" target="?">...</A>`	Specifies where the linked-to document is to be placed
`<A HREF="?" rel="?">...</A>`	Sets up a relationship between the linked-to document and the current page
`<A HREF="?" rev="?">...</A>`	Sets up a reverse relationship between the current page and the linked-to document
 
# Table tags and attributes
	
`<TABLE>...</TABLE>`	Generates a table
`<TABLE border="pixels">`	Sets the size of cell borders
`<TABLE cellspacing="pixels">`	Sets the amount of space between cells
`<TABLE cellpadding="pixels">`	Sets the amount of space between a border and cell content
`<TABLE height="pixels" or "%">`	Sets the height of a table
`<TABLE width="pixels" or "%">`	Sets the width of a table
`<TD>...</TD>`	Defines a table data cell
`<TD colspan="columns">`	Sets a cell to span columns
`<TD rowspan="rows">`	Sets a cell to span rows
`<TD nowrap>`	Prevents the lines within a cell from wrapping
`<TH>...</TH>`	Defines a table header with bold, centered table data
`<TR>...</TR>`	Defines a table row
`<TR align="?">` or `<TD align="?">`	Aligns the contents of a row or cell to the left, right, or center
`<TR valign="?">` or `<TD valign="?">`	Sets the vertical alignment of a row or cell to the top, middle, or bottom
 
# Frame tags and attributes
	
`<FRAMESET>...</FRAMESET>`	Specifies the layout of subsections in the main browser window
`<FRAMESET rows="value,value">`	Defines the rows within a frameset
`<FRAMESET cols="value,value">`	Defines the columns within a frameset
`<NOFRAMES>...</NOFRAMES>`	Provides alternate content for browsers that do not support frames
`<FRAME src="?">`	Defines the appearance and content of a single frame
`<FRAME name="name">`	Labels the frame for targeting by other frames
`<FRAME marginwidth="#">`	Sets the margin width of a frame
`<FRAME marginheight="#">`	Sets the margin height of a frame
`<FRAME scrolling="value">`	Creates a frame scrollbar
`<FRAME noresize>`	Prevents the resizing of a frame
 
# Form tags and attributes
	
`<FORM>...</FORM>`	Generates a container for all form elements
`<FORM action="url">`	Designates the path of the script to process input from the form
`<FORM method="get|post">`	Instructs the browser how to interact with the form URL
`<FORM accept="media type">`	Defines which MIME types are supported by the server processing the form
`<FORM accept-charset="text">`	Defines which character sets are supported by the server processing the form
`<FORM enctype="media type">`	Defines the format of the submitted data
`<OPTION>`	Defines each menu item
`<SELECT name="NAME">...</SELECT>`	Generates a pull-down menu
`<INPUT type="checkbox">`	Generates a check box
`<INPUT type="hidden">`	Conceals a field from view
`<INPUT type="image">`	Generates an image that acts like a Submit button
`<INPUT type="password">`	Generates a one-line password box
`<INPUT type="radio">`	Generates a radio button
`<INPUT type="text">`	Generates a one-line text box
`<INPUT type="submit">`	Generates a Submit button (send form)
`<INPUT type="reset">`	Generates a Reset button (clear form)