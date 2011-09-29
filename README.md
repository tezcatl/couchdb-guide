<h1>CouchDB: The Definitive Guide</h1>

<p>This is the source code repository for a free book about Apache CouchDB.

<h2>Introduction</h2>

<p>The book is called <em>CouchDB: The Definitive Guide</em> and is published by O’Reilly Media under a <a href="http://creativecommons.org/licenses/by/3.0/">free license</a>.

<p>We believe that community software needs community documentation. You can inspect the source code for CouchDB and make improvements to it, and similarly you can inspect the source code for this book and make improvements to it. If you want to contribute, please do so! Fork it, hack on it, and send back your changes! If you want to support the project, you can do so by <a href="http://oreilly.com/catalog/9780596155902">buying a copy</a> of the book in digital or printed form.

<<<<<<< HEAD
<h2>Organisation</h2>

<p>The source is organised into the following directories:

<dl>

<dt><code>draft/</code></dt>

<dd><p>The draft of next edition.</dd>

<dt><code>editions/</code></dt>

<dd><p>Published editions of the book.</dd>

<dt><code>editions/1</code></dt>

<dd><p>Edition 1 of the book.</dd>

<dt><code>editions/1/en</code></dt>

<dd><p>The English version of edition 1 of the book.</dd>

</dl>

<p>The draft of the next edition is a work in progress. Like the trunk of an open source project, we will eventually cut from this and hand it over to our publishers. Once the publishing process is complete, we will take back the XML and convert it into HTML. Like a tag of an open source project, this will be frozen in place as an official edition of the book. Translations are subject to change and may be updated at any time.

<h2>Contributions</h2>

<p>The book is made available under a <a href="http://creativecommons.org/licenses/by/3.0/">Creative Commons Attribution</a> license.

<p>We encourage you to fork our work and make your own improvements under the terms of the license. If you have any changes you want to send back our way, please make a regular pull request via Github. If the authors like your changes, they may integrate them into the official book and give you a credit in the next edition. If you just have an issue to report, please use the regular Github issue system.

<h2>Translations</h2>

<p>We’d like to encourage people to start translating the book into other languages. If you’d like to start a new translation, please first check to see if one exists in that language. If not, you can get started right away. You’re free to publish a translation under the aforementioned license. Our publishers may be interested in your translation if you think the market would be big enough. Please contact us directly to discuss this.

<p>Please observe the following guidelines:

<ul>

<li><p>Do start your translation from the <code>en/</code> directory</li>

<li><p>Do use the appropriate <a href="http://en.wikipedia.org/wiki/IETF_language_tag">language tag</a> for your new directory</li>

<li><p>Do not translate the <code>draft/</code> directory, as this is will be a work in progress</li>

<li><p>Do not translate from anything other than the <code>en/</code> directory, as this will introduce errors</li>

<li><p>Do not modify the general markup or structure of the documents</li>

<li><p>Do not include your own styles or scripts</li>

</ul>

<p>Here’s an example of how to start a new translation:

<pre>
cd editions/1
cp -r en de
git add de
git commit -m 'new German translation' de
</pre>
=======
<h2>Dependencies</h2>

<p>We edit the book in HTML and accept contributions in HTML.

<p>HTML allows us a lot of freedom as authors, and makes editing much easier. Before going to print we hand the HTML to O’Reilly Media, and they convert this into DocBook. DocBook allows a lot of control over the typesetting and publishing of the book. Once that process is complete, O’Reilly Media hand us back the final DocBook, which now includes any modifications from our editors. We then transform this into HTML, and tidy it up.

<p>You must install the DocBook XSL stylesheets to generate the HTML:

<pre>
sudo port install docbook-xsl
</pre>

<p>You must install Tidy to clean the HTML:

<pre>
sudo port install tidy
</pre>

<p>You can now generate HTML from the DocBook source.

<h2>Instructions</h2>

<p>The DocBook source for the book is under:

<pre>
src/EDITION
</pre>

<p>So, the first edition of the book can be found at:

<pre>
src/01/book.xml
</pre>

<p>And the images used for the first edition of the book can be found at:

<pre>
src/01/figs
</pre>

<p>The tools we use to convert this into HTML can be found at:

<pre>
bin/
</pre>

<p>You can transform the DocBook to HTML by running:

<pre>
bin/transform.sh src/EDITION/book.xml
</pre>

<p>You can tidy the HTML files by running:

<pre>
bin/tidy.sh ch01.html
</pre>

<p>The HTML we generate with this process is held in the <a href="http://github.com/oreilly/couchdb-guide/tree/gh-pages">gh-pages</a> branch.

<h3>Building an epub</h3>

<p>Build an epub with off-the-shelf docbook-xsl <code>dbtoepub src/01/book.xml</code>. (The script lives in the <code>DOCBOOK_XSL_ROOT/epub/dbtoepub</code> at least as of docbook-xsl version 1.75.2.)
>>>>>>> upstream/master

<p>Relax.
