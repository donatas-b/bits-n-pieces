
 | XPath locator | Explanation | 
 | -------------- | ------------ | 
 | //img  | image element | 
 | //img[@id='myId'] | image element with @id= 'myId' | 
 | //img[@id!='myId'] | image elements with @id not equal to 'myId' | 
 | //img[@name] | image elements that have name attribute | 
 | //*[contains(@id, 'Id')] | element with @id containing | 
 | //*[starts-with(@id, 'Id')] | element with @id starting with | 
 | //*[ends-with(@id, 'Id')] | element with @id ending with | 
 | /*[matches(@id, 'r')] | element with @id matching regex ‘r’ | 
 | //img[@name='myName'] | image element with @name= 'myName' | 
 | //*[@id='X' or @name='X'] | element with @id X or a name X | 
 | //*[@name="N"][@value="v"] | element with @name N & specified @value ‘v’ | 
 | //*[@name="N" and @value="v"] | element with @name N & specified @value ‘v’ | 
 | //*[@name="N" and not(@value="v")] | element with @name N & not specified @value ‘v’ | 
 | //input[@type="submit"] | input of type submit | 
 | //section[//h1[@id='hi']] | returns `<section>` if it has an `<h1>` descendant with @id= 'hi' | 
 | //table[count(tr) > 1] | return table with more than 1 row | 
 | //*[.="t"] | element containing text 't' exactly | 
 | //a[contains(text(), "Log Out")] | anchor with inner text containing 'Log Out' | 
 | //a[not(contains(text(), "Log Out"))] | anchor with inner text not containing 'Log Out' | 
 | //a[@href="url"] | anchor with target link 'url' | 
 | //img/*[1] | first child of element img | 
 | //ul/child::li | first child 'li' of 'ul' | 
 | //img[1] | first img child | 
 | //img/*[last()] | last child of element img | 
 | //img[last()] | last img child | 
 | //img[last()-1] | second last img child | 
 | //input/following-sibling::a | 'a' following some sibling 'input' | 
 | //a/following-sibling::* | sibling element immediately following 'a' | 
 | //input/preceding-sibling::a | 'a' preceding some sibling 'input' | 
 | //input/preceding-sibling::*[1] | sibling element immediately preceding 'input' | 
 | //img[@id='MyId']::parent/* | the parent of image with id | 
 | //*[@id="TestTable"]//tr[3]//td[2] | cell by row and column | 
 | //td[preceding-sibling::td="t"] | cell immediately following cell containing 't' exactly | 
 | //td[preceding-sibling::td[contains(.,"t")]] | cell immediately following cell containing 't' | 
 | //input[@checked] | checkbox (or radio button) that is checked | 
 | //a[@disabled] | all 'a' elements that are disabled | 
 | //a[not(@disabled)] | all 'a' elements that are not disabled | 
 | //a[@price > 2.50] | 'a' with price > 2.5 | 
 | //ul[*] | 'ul' that has children | 