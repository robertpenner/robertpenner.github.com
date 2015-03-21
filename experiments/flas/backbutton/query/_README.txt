This set of files provides a method for restoring the functionality of the browser's
back button when using full flash sites.
It is based on the original concept and programs by Robert Penner (www.robertpenner.com)
but tries to reduce the number of files required. Many thanks to Robert for a fine
solution to this problem.

email: james@forestbeacon.f2s.com
www:   http://www.forestbeacon.f2s.com/


FUNCTIONS
---------
- The changePage() function in the flash movie can be altered to include as many
  arguments as you need.  All these arguments should then be passed on to 
  'pageChanger.html' by including them in the 'getURL' location argument.
  (you can see how this is done by studying how it looks by default).
  In turn, you will have to alter the 'changePage()' function in 'pageChanger.html'
  to extract these new arguments and use them accordingly.



NAMING CONVENTIONS
------------------
- In the frameset, the hidden frame must be called 'pageChanger' (case is important):
	<frame name="pageChanger" src="pageChanger.html">

- The name of the frame containing the flash movie, can be called whatever you like,
  but must be set in the 'changePage()' function in pageChanger.html where, by default,
  it says 'FLASHFRAME'.
	e.g
	default: parent.FLASHFRAME.document.FLASHCONTENT.SetVariable("curPage", page);

	if frame is called 'catfish': parent.catfish.document.FLASHCONTENT.SetVariable("curPage", page);

- The flash movie must be called 'FLASHCONTENT'


NOTES
-----
- The 'curPage' variable in the flash movie must be set in the _root

- If your frame set has nested framesets, be careful to make sure the following line
  actually points to the correct frame:

	parent.FLASHFRAME.document.FLASHCONTENT.SetVariable("curPage", page);

  You may have to add extra 'parent.' lines to the beginning of this line.


