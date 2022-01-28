# First bug in week 3, out of memory error
Our first bug in week three lab appeared when trying to run [this](https://michaeleung.github.io/cse15l-lab-reports/markdown1.html) test file, with two links and characters after the two links. There were no bugs during compile time, but in run time the symptom was an OutofMemoryError correlating with heap space. 

![image](OutofMemoryError.png)

In order to fix this, our group decided that the while loop needed to break when no more parenthesis or brackets could be found by indexOf. 

![image](gitchanges.png)

Here, the failure inducing input caused a bug and a symptom to be seen because characters were placed after the links. The bug, a faulty while loop unable to break after no links are find, and the symptom, an OutofMemoryError are tightly intertwined. This is because the symptom of OutofMemoryError is a direct result of an infinite while loop. 

# Second bug in week 3, avoiding an image when finding links

Another bug our group encountered when debugging the original MarkdownParse code was what to do when an image is within the markdown file. As seen in the test [file](https://michaeleung.github.io/cse15l-lab-reports/markdown2.html) , the markdown file contains an image. As our code is now, the getLinks method will retrieve this image as a file, which we don't want, as seen here: 

![image](pizzalink.png)

In order to fix this, we added a piece of code that will `continue` in the while loop if there is a `!` before the open bracket. 

![image](breakimage.png)

From the file of an image, there were no compile time errors or runtime errors, however there was still a bug and symptom within the system. The bug was that the code was unable to separate image and links within the markdown files, and the symptom was printing out the image when nothing should be printed within the file. So here, the bug of not being able to separate link and images caused the symptom. 

# third bug in week 4, 

