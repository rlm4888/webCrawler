== INCLUDED FILES ==

WebCrawler.java            This is some sample code that crawls pages; run this to run the crawler
CrawlingMarkupHandler.java Crawler code goes here
Index.java                 A class with serialization code
WebIndex.java              Index goes here
WebServer.java             Sample code for a simple server; run this to run the webserver
WebQueryEngine.java        Query engine goes here
Page.java                  A wrapper class for page results
tsoogle.png                Part of the web interface
attoparser-*.jar           A library used for crawling
superspoof.zip             A small website for you to test with
rhf.zip                    A larger website to aid in testing

== CRAWLER INSTRUCTIONS ==

First, make sure you add the attoparser library to your classpath! Then, you can run the WebCrawler
class, providing it ABSOLUTE URLS, on the two provided testing websites. Absolute URLS are prefixed
by "file://", and look something like this:

file://<absolute-path-to-file>

For example, on the command line, using linux:

java -cp attoparser-2.0.0.BETA2.jar:bin assignment.WebCrawler file:///<path-to-project>/superspoof/index.html

This should run your crawler and save an index to "index.db"!

== WEBSERVER INSTRUCTIONS ==

To run the webserver, run the assignment.WebServer class; this will load your previously generated
index.db file from your crawler, and then set up an HTTP webserver you can connect to in your
browser:

java -cp attoparser-2.0.0.BETA2.jar:bin assignment.WebServer

The program will output "listening on port 1989"; to see the actual website, go to

localhost:1989

in your browser; the UI should show up promptly.
