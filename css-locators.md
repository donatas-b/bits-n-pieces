
 | CSS locator | Explanation |  
 | -------------- | ------------ |  
 | ul#myId | ‘ul’ element with @id= ‘myId’ | 
 | ul[id = "myId"] | 'ul' element with @id='myId' | 
 | ul[@id] | 'ul' elements with @id attribute | 
 | #myUniqueId | any element with @id= ‘myId’ | 
 | a:contains('Log Out') | anchor with inner text containing 'Log Out' | 
 | a[href='url'] | anchor with target link 'url' | 
 | ul.myForm | ‘ul’ element with @class = ‘myForm’ | 
 | .myForm.front | any element with @classes = ‘myform’ and ‘front’ | 
 | ul#myUniqueId > li | direct child element | 
 | ul#myUniqueId li | sub child element | 
 | ul[name = "automateName"][style = "style_name"] | ‘ul’ element with attributes @name =‘automateName’ and @style= ‘style name’ | 
 | *[name='N'][value='v’] | elements with name N and specified value ‘v’ | 
 | ul[id ^= "my"] | all elements with an attribute beginning with ‘my’ | 
 | ul[id$= "Id"] | all elements with an attribute ending with ‘Id’ | 
 | ul[id *= “unique"] | all elements with an attribute containing the substring ‘unique’ | 
 | ul[id ~= “unique"] | all elements with an attribute containing the word ‘unique’ | 
 | ul#myUniqueId li:first-child | first child element | 
 | ul#myUniqueId li:nth-of-type(1) | first child element | 
 | ul#myUniqueId li:last-child | last child element | 
 | ul#myUniqueId li:nth-of-type(3) | third child element | 
 | div > p | all `<p>` elements that are a direct descendant of a <div> element | 
 | div + p | all `<p>` elements that are the next sibling of a <div> element (i.e. placed directly after) | 
 | div ~p | all `<p>` elements that follow, and are siblings of <div> elements | 
 | a:link | all unvisited links | 
 | a:visited | all visited links | 
 | a:hover | all links on mouse hover | 
 | input:active | every active `<input>` element | 
 | input:disabled | every disabled `<input>` element | 
 | input:enabled | every enabled `<input>` element | 
 | input:focus | the `<input>` element which has focus | 
 | input:read-only | `<input>` elements with the ‘readonly’ attribute specified | 
 | input:required | `<input>` elements with the ‘required’ attribute specified | 
 | input:checked | checkbox (or radio button) that is checked | 
 | form myForm.front + ul | next sibling | 
 | #TestTable tr:nth-child(3) td:nth-child(2) | cell by row and column (e.g. 3rd row, 2nd column) | 
 | td:contains('t') ~td | cell immediately following cell containing 't' | 
 | p:lang(language) | all `<p>` elements with a @lang attribute equal to ‘language’ | 

