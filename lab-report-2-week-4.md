# Lab Report 2
By: jt

## Code Error #1
1) Changed the code to consider the test case of an image link.  markdownParse shouldn't get the link of the image because its purpose is to get only links.

[Link to Test Case Code #1](https://github.com/jt-ucsd/markdown-parser/commit/dbac799f55482352e389c69396f4fbf62583a2cd)

![Test Case 1](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20-%20Error%201.jpg)

2) Error Output: `[image.com]`

3) For Test Case #1, the failure inducing input was `![image](image.com)`.  Inside of the program, there is a logical bug where it wouldn't consider the situation where an image is displayed and since it follows the same format as a regular link but with a `!` in front, it would try to get the link of both images and URLs when it should just be URLs.  The symptom is the output of `[image.com]` when it should be `[]`.

4) Fix:  Note that for test case #1 and #2, I accidently fixed both errors at the same time.

[Link to Test Case 1 Fix](https://github.com/jt-ucsd/markdown-parser/commit/253271ef90e8b0c6990ec5937203689abb0fc4c5)

![Test Case 1 Fix](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20Fix%201%20and%202.jpg)

## Code Error #2
1) Changed the code to consider just `[Hello]` with no parantheses following up.  Since there is no parantheses, the program should return `[]` as no links were found.

[Link to Test Case Code #2](https://github.com/jt-ucsd/markdown-parser/commit/ef0998301dbafcc8463116c0367be08a493e339b)

![Test Case 2](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20-%20Error%202.jpg)

2) Error Output: 

`Exception in thread "main" java.lang.StringIndexOutOfBoundsException: begin 0, end -1, length 7
   at java.base/java.lang.String.checkBoundsBeginEnd(String.java:4601)
   at java.base/java.lang.String.substring(String.java:2704)
   at MarkdownParse.getLinks(MarkdownParse.java:28)
   at MarkdownParse.main(MarkdownParse.java:39)`

3) For test case #2, the failure inducing input that triggered the error was `[Hello]`.  The code had a logical error bug where it would loop and proceed through the file until it finds a link.  However, since it kept on proceeding through the file and there is no links, it would try to access an out of bound part of the text.  As a result, we see the out of bound symptom.

4) Fix:  Note that for test case #1 and #2, I accidently fixed both errors at the same time.  I also edited the fix for this part again at the very end, hence the two part fix.

[Link to Test Case 2 Fix Part 1](https://github.com/jt-ucsd/markdown-parser/commit/253271ef90e8b0c6990ec5937203689abb0fc4c5)

[Link to Test Case 2 Fix Part 2](https://github.com/jt-ucsd/markdown-parser/commit/00c390a2476a6e5a84d99137a5ac92d3df82823a)

![Test Case 2 Fix Part 1](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20Fix%201%20and%202.jpg)

![Test Case 2 Fix Part 2](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20Fix%202%20Part%202.jpg)

## Code Error #3
1) Changed the code to consider just `(Hello)`.  Since it is just parantheses, there should be no links found and return `[]`.

[Link to Test Case Code #3](https://github.com/jt-ucsd/markdown-parser/commit/09092c45967fb13977b218066e38e129addcb213)

![Test Case 3](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20-%20Error%203.jpg)

2) Error Output: `[Hello]`

3) For test case #3, the failure inducing input that triggered the error was `(Hello)`.  The code had a logical error, or bug, where anything between two `()` and saves it as a link even if it's not.  As a result, it would produce the symptom of `[Hello]` instead of `[]`.

4) Fix:

[Link to Test Case 3 Fix](https://github.com/jt-ucsd/markdown-parser/commit/503b836969969823fb1bbdcb85f89f2e3337595a)

![Test Case 3](https://raw.githubusercontent.com/jt-ucsd/cse15l-lab-report-2/main/Lab%20Report%202%20Fix%203.jpg)