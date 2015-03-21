---------------------------
Back Button with Flash

Attention, K-Mart shoppers!  Lend me your ears, Flash usability specialists!  You can no longer say that Flash "breaks the back button".  These precious files allow the navigation of sections within a Flash movie to be tracked in the browser history, so the back and forward buttons navigate without leaving the page.  This relatively simple solution works in the vast majority of browsers (excluding Mac Internet Explorer and Opera).


Revised May 9, 2001
- put a function on the main Flash page; individual pages call the function  -- easier to avoid bugs and update
- blank.html is no longer needed
- fixed an obscure bug that occured when back button was hit immediately (thanks to Cyborx from paletteworks.com for detecting it)

source@robertpenner.com
---------------------------


Files
-----

1. The main HTML file of this archive is backbutton_frameset.html.

2. The file backbutton_code.html is basically the same, but with a bigger second frame so you can see it.

3. The Flash movie is on flashpage.html, which is in backbutton_frameset.html.

4. The numbered HTML pages, "1.html, 2.html", etc. are loaded into the hidden frame to generate a browser history of visited sections withint the Flash movie.



Explanation
-----------

1. Normally, pressing the back button on a Flash page takes you out of the movie. I don't like that!

2. In order to use the browser back button, you have to generate a history of web pages.

3. I use a hidden frame to store HTML pages that generate a browser history.

4. In this Flash movie, pressing a number button does two things:
  a) navigates the movie to a new section by
      setting a variable (_root.page)
  b) loads an HTML page in the hidden frame

5. I created one HTML page for each section of the movie that I want in the history.  For simplicity, I called my pages "1.html", "2.html", etc.

6. On each HTML page is a little piece of Javascript that sets a variable in the Flash movie.
For example, "4.html" sets _root.page = 4.

7. After the HTML sends the signal to Flash, it's up to you to notice and navigate to the appropriate section.  I coded something simple for this demo; yours may have to be more complex.

8.The back button will not do anything in Internet Explorer for the Mac.  Mac IE does not allow Javascript to communicate with Flash.  However, the internal Flash navigation works.  Also problems with Opera and maybe Netscape 6.  But hey, >90% of browsers ain't bad!

Robert Penner - May 9, 2001