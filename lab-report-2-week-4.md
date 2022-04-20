# Lab Report 2
By: jt

## Code Error #1
1) Changed the code to consider the test case of an image link, which the markdown parse should ignore.

![Test Case 1](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20-%20Error%201.jpg)

[Link to Test Case Code #1](https://github.com/jt-ucsd/markdown-parser/commit/dbac799f55482352e389c69396f4fbf62583a2cd)

2) Error Output: `[image.com]`

3) Relationship explanation here

## Code Error #2
1) Changed the code 

![Test Case 2](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20-%20Error%202.jpg)

[Link to Test Case Code #2](https://github.com/jt-ucsd/markdown-parser/commit/ef0998301dbafcc8463116c0367be08a493e339b)

2) Error Output: 

`Exception in thread "main" java.lang.StringIndexOutOfBoundsException: begin 0, end -1, length 7
   at java.base/java.lang.String.checkBoundsBeginEnd(String.java:4601)
   at java.base/java.lang.String.substring(String.java:2704)
   at MarkdownParse.getLinks(MarkdownParse.java:28)
   at MarkdownParse.main(MarkdownParse.java:39)`

3) Relationship explanation here

## Code Error #3
1) Changed the code to consider the test case of an image link, which the markdown parse should ignore.

![Test Case 3](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20-%20Error%203.jpg)

[Link to Test Case Code #3](https://github.com/jt-ucsd/markdown-parser/commit/09092c45967fb13977b218066e38e129addcb213)

2) Error Output: `[Hello]`

3) Relationship explanation here