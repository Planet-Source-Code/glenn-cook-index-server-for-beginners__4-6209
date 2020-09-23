<div align="center">

## Index Server for Beginners


</div>

### Description

It's easy to look smart! This tutorial will help you grasp the basics to utilize Index Server in your organization quickly! Read this tutorial, play with some code, put your arms behind your head, lean back in your chair, and watch as others admire your technical handy-work.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Glenn Cook](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/glenn-cook.md)
**Level**          |Beginner
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |ASP \(Active Server Pages\), VbScript \(browser/client side\)

**Category**       |[Server Side](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/server-side__4-31.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/glenn-cook-index-server-for-beginners__4-6209/archive/master.zip)





### Source Code

<p><big><font face="Verdana"><strong><big>B</big></strong>rief Overview of Index
Server!</font></big></p>
<p><small><font face="Verdana"><img align="left" src="http://www.aspalliance.com/glenncook/images/index.jpg" width="128" height="95">1.
Index server is not a bunch of hardcore ASP code that does amazingly fast
searches.&nbsp; It is an incredibly well coded server-side executable that does
full-text extraction for creating index files for fast web-based queries. By
leveraging the power of Index Server with ASP and HTML, you can easily develop
amazing applications.<br>
<br>
2. The core of Index Server that you will be most concerned with is made up of
two types of files: *.HTX- The template file.&nbsp; *.IDQ- This file tells Index
Server what to do. &nbsp; It tells Index server what to search, how to organize
the data, and what to send to the HTX file.&nbsp; The HTX file then takes the
data and formats it so it's pretty for the user. (In other words, the IDQ file
is the playdough and the HTX file is the cookie cutter.)<br>
3. The core of Index server you'll be less concerned with but which does the
most work: The Index Server EXECUTABLE- The engine!&nbsp; The other file(s) is
the Index CATALOGUE- Index Server makes an index catalogue that is made up of
&quot;keywords&quot; that points to the files you/the administrator have chosen
to index. This catalogue is transparently maintained by Index server once you've
set everything up.&nbsp; Basically when it senses that it's got a little
downtime, it will start crawling through your designated directories making
indexes of keywords.&nbsp; It updates, adds, and deletes keywords and keeps your
indexes up to date...automatically!<br>
4. Currently, Index Server can perform full text exctraction for all of
Microsoft's file types- *.doc,*.xls, *.mdb, etc.&nbsp; Microsoft has also
provided a filter interface for third parties to develop filters that will index
other file types but these third party filters are often poorly documented and
are not supported by the manufacturers. For example, Adobe makes a filter that
extracts keywords from PDF files.</font></small></p>
<p><font face="Verdana"><strong><big>H</big>ere is the complete process:</strong></font></p>
<p><small><font face="Verdana">You type in a search word or phrase and click
&quot;submit&quot; on the asp/htm page. &nbsp; Your information is passed to the
IDQ file which defines the properties that the Index Server executable will use.&nbsp;
This information gets passed to the Index Server engine which crunches the
information you want against it's index catalogue. The information Index Server
finds is then passed to the HTX file which takes all the information and filters
it to make it pretty to deliver you the useful HTML/ASP file you want.....with
hyperlinks to the information! Now, you have a page of useful data that you can
integrate into any ASP application!</font></small></p>
<p><font face="Verdana"><big><strong>Tools you need!</strong></big></font></p>
<p><small><font face="Verdana">Assuming you have IIS 3.0 or 4.0 with Index
server installed the first logical step is to get your hands dirty by looking at
the file types you'll be most concerned with. &nbsp; The HTM, HTX and IDQ files.
(Unless you are an Index Server expert ready to code for the <strong>filter
interface, </strong>leave the other file types to the experts.) Now, <a href="http://www.microsoft.com/sitebuilder/vinterdev/vionsbn.asp"><font color="mediumblue" face>download
Interdev 6.0!</font></a>You'll need it for this exercise, and trust me, you'll
love it!</font></small></p>
<p><small><font face="Verdana">&nbsp;</font></small></p>
<p><font face="Verdana"><strong>Steps to Greatness!</strong></font></p>
<p><small><font face="Verdana">1. First, put a bug in management's ear by
suggesting how cool it would be to have full-text searching capabilities on
directories containing popular company documents on the company
Intranet/Extranet/Internet site.&nbsp; Watch the Java and Unix coders scramble
for an affordable solution.&nbsp; You see, developers will sell what they
know,(I'm no exception), but they will not be able to find a more cost effective
quality solution-<a href="http://www.aspalliance.com/glenncook/ifilter.asp"><font color="mediumblue" face>
trust me</font></a>.&nbsp; Let them come to the table with their plans of attack
and when they are done trying to impress the bosses say, &quot;If you give <em>me</em>
an afternoon I'll have a working prototype for you the following morning.&quot;&nbsp;</font></small></p>
<p><small><font face="Verdana">2. Go right to your IIS server and make sure that
Index Server is loaded.&nbsp; It will automatically create a sample query page
which you will edit to suit your needs.&nbsp; Now check out the &quot;Index
Server Administration&quot; shortcut. Make sure that Index server only indexes
the directories that YOU want indexed.&nbsp; If the directory you want indexed
is not listed you will have to add a virtual directory in IIS Manager.&nbsp;</font></small></p>
<p><font face="Verdana"><small>3. Find the physical directory that contains the
queryhit.htm page (I think it's in Inetpub/samples/search/ but I'll have to
check tomorrow.)&nbsp; Open up the queryhit.htm, queryhit.htx, and queryhit.idq
files that are used in the Index Server example query using your Interdev 6.0
and look at the code.&nbsp; </small><strong>****<small>IMPORTANT NOTE:</small></strong><small>
Never, ever, open and save any of these files with FrontPage. &nbsp;
Unfortunately, FrontPage has a tendency to think that it a smarter coder than we
are and will totally destroy the working code.&nbsp;What you should use to view
all your ASP code is Microsoft's Visual Interdev 6.0!<strong>&nbsp;</strong></small><strong>
**** </strong><small>Although my first inclination is to suggest start playing
with the code, let me recommend looking at the code <em>while</em> you play with
the sample queries to understand how it's working.</small></font></p>
<p><small><font face="Verdana">4. You'll notice that queryhit.htm does a simple
&quot;GET&quot; submission to the queryhit.idq file based on the text the user
has input.&nbsp; If you look at the IDQ file you'll see a bunch of code you're
not familiar with.&nbsp; What is this crap? &nbsp; Well, it's the stuff that the
Index Server executable understands ie. &lt;%CiTotalNumberPages%&gt;.&nbsp;
Since this is not &quot;indexserverpages.com&quot; I'm not going to go into
editing all of these properties.&nbsp; Honestly, you can get away with using the
default code that Microsoft offers in it's samples.&nbsp; If you want some good
resources to learn more about these properties check out <a href="http://www.microsoft.com/ntserver/search/step111dl.htm"><font color="mediumblue" face>Microsoft's
site</font></a>or buy a book (<a href="http://www.rapid.wrox.com/books/1266/1266.asp"><font color="mediumblue" face>Wrox's
Professional Active Server Pages.</font></a><font color="mediumblue" face>)!</font></font></small></p>
<p><small><font face="Verdana">5.&nbsp; One of the long awaited Interdev 6.0
features is a WYSIWYG editor that doesn't screw up the code like FrontPage.&nbsp;
Use Interdev to look at your HTX file.&nbsp; This is the file that formats the
results Index Server returns and is the best place to really learn how Index
server works.&nbsp; You'll notice that it has a healthy mixture of several types
of code:&nbsp; Index server properties, HTML and ASP.&nbsp; You'll also notice
that Microsoft does a pretty good job of documenting what the code is doing.</font></small></p>
<p><small><font face="Verdana">6. Make a backup of the queryhit.htx file.&nbsp;
Now go back to your WYSIWYG editor and start making changes that suit your
needs. Throw in your company logo. Delete output that you don't need! Add, edit
or delete text as you see fit.&nbsp; It's surprisingly easy!</font></small></p>
<p><small><font face="Verdana">7. Test your changes and go show off!</font></small></p>
<p><small><font face="Verdana">The reason why I wrote this tutorial is because
when I first played with Index Server I couldn't believe how easy it was.&nbsp;
Within a week after I accomplished this nominal feat at one company, through
word-of-mouth, another company was calling me to do the same thing for them.&nbsp;
I told them that it was so easy they could do it themselves but they would hear
nothing of it.&nbsp; They wanted ME?!&nbsp; No, they wanted this knowledge!
&nbsp; You don't have to be smart in this industry, you just have to have the
knowledge people are willing to pay for. Well, maybe you can define intelligence
by knowing what knowledge people are willing to pay for.&nbsp; In that case, by
reading this, your IQ just went up about $50 an hour.</font></small></p>

