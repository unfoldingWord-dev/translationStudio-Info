tS for Desktop: Working with Footnotes 
==========================================================

.. image:: ../images/tSforDesktop.gif
    :width: 205px
    :align: center
    :height: 165px
    :alt: translationStudio for Desktop


A footnote is additional text that usually appears at the bottom of a book’s page and is referenced within the page.

In translationStudio, a footnote is shown as a black page icon that you click to display the footnote. For example, there is a footnote in 1 Cor. 10.28.

Footnotes can provide further explanation when:

* There are proper names, words or terms that differ between various Bible versions

* There are missing words or verses in the ULB. (There may be text in one Bible version that is not present in the ULB.)

To translate a footnote:
************************

1)	Copy the footnote.

    *	Click the footnote icon to open it (for example, in 1 Cor. 10:28)  

    * Highlight the text of the footnote.

    *	Copy the footnote text – [Ctrl + C] on Windows.

    * Dismiss the footnote.
 
2)	Paste the footnote into the translated text.

    * If the chunk has been marked “done”, click the toggle at bottom right of the translated chunk.
 
    * Click the Edit icon (pencil).
 
    * Click the appropriate spot in the translated text.

    * Paste the footnote text – [Ctrl + V] on Windows).
 
3)	Add footnote coding. Footnote coding identifies the text as a footnote and separates it from the surrounding text. To add footnote coding:

    * Type the following text at the beginning of the footnote, separated from the surrounding text by spaces:

      ::
 
         \f + \ft

    * Type the following text at the end of the footnote, separated from the surrounding text by spaces: 
 
      ::
 
          \f* 
 
    * If there is a quote within the footnote:
      
      * Replace the beginning quotation mark with: 
      
        ::
            
           \fqa
           
        and separate from the surrounding text by spaces.
      
      *	Replace the ending quotation mark with: 
      
        ::
            
           \fqb
           
        and separate from the surrounding text by spaces. 
 
4)	Translate the footnote text.

    * Translate the text of the footnote.
 
    * Click the check mark to save the edits on the chunk.
 
    * Mark the chunk as done.
    
For example, the code for the chunk containing the footnote in 1 Cor. 10:28 looks like this:

::

    \v 28 But if someone says to you, "This food was from a pagan sacrifice," do not eat it. This is 
    for the sake of the one who informed you, and for the sake of conscience.  \f + \ft Some older 
    copies add, \fqa For the earth and everything in it belong to the Lord. \fqb But the best copies 
    do not have this. \f* \v 29 I do not mean your own conscience, but the other person's conscience. 
    For why should my freedom be judged by another's conscience? \v 30 If I partake of the meal with 
    gratitude, why am I being insulted for that for which I gave thanks?

