# Proto!MultiSelect

Prototype version required: 6.0

Copyright: InteRiders <http://interiders.com/> - Distributed under MIT - Keep this message!
  
## Credits

 - Idea: Facebook + Apple Mail
 - Caret position method: Diego Perini <http://javascript.nwbox.com/cursor_position/cursor.js>
 - Guillermo Rauch: Original MooTools script
 - Ran Grushkowsky/InteRiders Inc. : Porting into Prototype and further development
 - Loren Johnson, Venado Partners, LLC Modifications
 - Zuriel Barron, severelimitation.com
 - Sean Cribbs
 - [skaue]

## Changelog

### 0.1
  - translation of MooTools script

### 0.2
  - renamed from Proto!TextboxList to Proto!MultiSelect, added new features/bug fixes
  - added feature: support to fetch list on-the-fly using AJAX    Credit: Cheeseroll
  - added feature: support for value/caption
  - added feature: maximum results to display, when greater displays a scrollbar   Credit: Marcel
  - added feature: filter by the beginning of word only or everywhere in the word   Credit: Kiliman
  - added feature: shows hand cursor when going over options
  - bug fix: the click event stopped working
  - bug fix: the cursor does not 'travel' when going up/down the list   Credit: Marcel

### 0.3
  - bug fix: moved class variables into initialize so they happen per instance. This allows multiple controls per page
  - bug fix: added id_base attribute so that multiple controls on the same page have unique list item ids (won't work otherwise)
  - feature: Added newValues option and logic to allow new values to be created when ended with a comma (tag selector use case)           
  - mod: removed ajax fetch file happening on every search and moved it to initialization to laod all results immediately and not keep polling
  - mod: added "fetchMethod" option so I could better accomodate my RESTful ways and set a "get" for retrieving
  - mod: added this.update to the add and dispose methods to keep the target input box values always up to date
  - mod: moved ResizableTextBox, TextBoxList and FaceBookList all into same file
  - mod: added extra line breaks and fixed-up some indentation for readability
  - mod: spaceReplace option added to allow handling of new tag values when the tagging scheme doesn't allow spaces, this is set as blank by default and will have no impact

### 0.4 
  - bug fix: fixed bug where it was not loading initial list values
  - bug fix: new values are not added into the autocomplete list upon removal
  - bug fix: improved browser compatibility (Safari, IE)
  
### 0.5
  - Add search timeout to increase responsiveness to typing.
  - Add non-standard autocomplete attribute to main input to prevent browser-supplied autocompletion in Gecko and some other browsers.
  - bug when gsub'ing space wth "spaceReplace". Input-field does not have a function gsub, though its value has.