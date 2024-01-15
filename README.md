# BulletChanger - Make that bullet fit

This project helps Air Force personnel write EPR and awards packages "bullets" (one-line narratives) by making changes, substitutions, or suggestions to the bullet.  The AF requires these bullets not exced a single line, and the unwritten rule of allowing minimal white space creates a dilemma where the most accurate word is substituted for the best fitting word.  This tool aims to assist the writer by using varius techniques to quickly find the best way to shorten or lengthen a bullet and make it fit.

See [test.bulletchanger.com](https://test.bulletchanger.com) for test site, hosted on Azure static web apps service.

As with any software development project, possibilities are endless.  You can build endless modules to extend the functionality, and you can go about doing it in a variety of methods.  This site, much like its creator, will not succumb to scope creep.  Here, we explain the priorities of development on this site, in order to tackle them with diligence.

Project Planning requirements:
Requirement #1.) Portability: Status = Complete. The solution must maximize portability in order to provide ubiquitous access to the solution. Air Force members have

Requirement #2.) Local calculation: Status = Complete. The solution must lean on client-side resources. With the current state of IT in mind, the most effective solution is to place the majority of code in the browser and that leads us to JavaScript. JavaScript is the only in-browser language at this time, thus narrowing the solution set.

Requirement #3.) Reverse engineering line-length calculation: Status = Complete. This site has a unique calculation built in to the JavaScript which calculates the length of your bullet in relation to an Air Force form 910, 911, or 1096. This module is the foundation of the site, enabling all subsequent modules to pre-calculate bullet length, in the browser (wicked fast), before any changes to the bullet are made. This predicts bullet length for the user, providing the basic value proposition of the site.


Project Modules:
Module #1.) SpacedOut: Status = Complete. This module inserts wide spaces and narrow spaces to either lengthen or shorten the bullet by a margin of 2-3% in order to make the bullet just the right length.

Module #2.) SuggestSubs: Status = 50%. This module suggests the removal and replacement of commonly shortened words in the Air Force writing world. For example, replacing “mission” with “msn” is a common thing. This module relies on a dictionary of words, and this dictionary is never complete. The next step for this module is to auto-flip from lengthen to shorten, in order to elongate the bullet when needed.

Module #3.) Thesaurus: Status = 0%. This module would provide a built-in thesaurus feature with pre-calculated line-length in order to predict the best fitting synonyms, in order to predictably swap out words for better fitment and/or meaning. Because there is no API for our favorite thesaurus www.powerthesaurus.com, I will have to get creative with this.

Dropped paying for ~~www.bulletchanger.com~~, the ~~current~~ old example of site.  It is now hosted above.
