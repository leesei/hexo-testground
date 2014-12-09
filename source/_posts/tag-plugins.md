title: Tag Plugins
date: 2014-12-01 13:21:57
tags:
- hexo
- tutorial
toc: true
---

Taken from Hexo's [doc page](https://github.com/hexojs/site/blob/master/source/docs/tag-plugins.md). Also see [tag-bootstrap](http://hahack.tk/hexo-theme-freemind/2014/03/16/tag-plugins/).

Tag plugins are different from tags in posts. They're ported from Octopress and can help you insert specific contents in posts quickly.

<!-- more -->

## Block Quote

Inserts quotes with author, source and title in posts.

**Alias:** quote

{% raw %}
<figure class="highlight"><pre>{% blockquote [author[, source]] [link] [source_link_title] %}
content
{% endblockquote %}
</pre></figure>
{% endraw %}

### Example

**No arguments given. Only output plain blockquote**

{% raw %}
<figure class="highlight"><pre>{% blockquote %}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque hendrerit lacus ut purus iaculis feugiat. Sed nec tempor elit, quis aliquam neque. Curabitur sed diam eget dolor fermentum semper at eu lorem.
{% endblockquote %}
</pre></figure>
{% endraw %}

{% blockquote %}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque hendrerit lacus ut purus iaculis feugiat. Sed nec tempor elit, quis aliquam neque. Curabitur sed diam eget dolor fermentum semper at eu lorem.
{% endblockquote %}

**Quote from a book**

{% raw %}
<figure class="highlight"><pre>{% blockquote David Levithan, Wide Awake %}
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.
{% endblockquote %}
</pre></figure>
{% endraw %}

{% blockquote David Levithan, Wide Awake %}
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.
{% endblockquote %}

**Quote from Twitter**

{% raw %}
<figure class="highlight"><pre>{% blockquote @DevDocs https://twitter.com/devdocs/status/356095192085962752 %}
NEW: DevDocs now comes with syntax highlighting. http://devdocs.io
{% endblockquote %}
</pre></figure>
{% endraw %}

{% blockquote @DevDocs https://twitter.com/devdocs/status/356095192085962752 %}
NEW: DevDocs now comes with syntax highlighting. http://devdocs.io
{% endblockquote %}

**Quote from an article on the web**

{% raw %}
<figure class="highlight"><pre>{% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing %}
Every interaction is both precious and an opportunity to delight.
{% endblockquote %}
</pre></figure>
{% endraw %}

{% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing %}
Every interaction is both precious and an opportunity to delight.
{% endblockquote %}

## Code Block

Inserts code snippets in posts.

**Alias:** code

{% raw %}
<figure class="highlight"><pre>{% codeblock [title] [lang:language] [url] [link text] %}
code snippet
{% endcodeblock %}
</pre></figure>
{% endraw %}

### Example

**A normal code block**

{% raw %}
<figure class="highlight"><pre>{% codeblock %}
alert('Hello World!');
{% endcodeblock %}
</pre></figure>
{% endraw %}

{% codeblock %}
alert('Hello World!');
{% endcodeblock %}

**Specify language**

{% raw %}
<figure class="highlight"><pre>{% codeblock lang:objc %}
[rectangle setX: 10 y: 10 width: 20 height: 20];
{% endcodeblock %}
</pre></figure>
{% endraw %}

{% codeblock lang:objc %}
[rectangle setX: 10 y: 10 width: 20 height: 20];
{% endcodeblock %}

**Add caption to code block**

{% raw %}
<figure class="highlight"><pre>{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}
</pre></figure>
{% endraw %}

{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}

**Add caption with an optional URL**

{% raw %}
<figure class="highlight"><pre>{% codeblock _.compact http://underscorejs.org/#compact Underscore.js %}
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
{% endcodeblock %}
</pre></figure>
{% endraw %}

{% codeblock _.compact http://underscorejs.org/#compact Underscore.js %}
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
{% endcodeblock %}

## Backtick Code Block

This plugin is same as code block, but in backtick style.

{% code %}
``` [language] [title] [url] [link text]
code snippet
```
{% endcode %}

## Pull Quote

This plugin helps you insert a pull quote in posts.

{% raw %}
<figure class="highlight"><pre>{% pullquote [class] %}
content
{% endpullquote %}
</pre></figure>
{% endraw %}

## jsFiddle

Embeds jsFiddle snippets in posts.

{% raw %}
<figure class="highlight"><pre>{% jsfiddle shorttag [tabs] [skin] [width] [height] %}
</pre></figure>
{% endraw %}

## Gist

Embeds Gist snippets in posts.

{% raw %}
<figure class="highlight"><pre>{% gist gist_id [filename] %}
</pre></figure>
{% endraw %}

## iframe

Embeds an iframe in posts.

{% raw %}
<figure class="highlight"><pre>{% iframe url [width] [height] %}
</pre></figure>
{% endraw %}

## Image

Inserts an image in posts with specified size.

{% raw %}
<figure class="highlight"><pre>{% img [class names] /path/to/image [width] [height] [title text [alt text]] %}
</pre></figure>
{% endraw %}

## Link

Inserts a link with `target="_blank"` attribute.

{% raw %}
<figure class="highlight"><pre>{% link text url [external] [title] %}
</pre></figure>
{% endraw %}
{% link "Visit Google" https://www.google.com %}

## Include Code

Inserts code snippets in `source` folder.

{% raw %}
<figure class="highlight"><pre>{% include_code [title] [lang:language] path/to/file %}
</pre></figure>
{% endraw %}

## Youtube

Inserts a Youtube video in posts.

{% raw %}
<figure class="highlight"><pre>{% youtube video_id %}</pre></figure>
{% endraw %}
<pre>{% youtube G5MzkDJQkoQ %}</pre>

## Vimeo

Inserts a Vimeo video in posts.

{% raw %}
<figure class="highlight"><pre>{% vimeo video_id %}
</pre></figure>
{% endraw %}
<pre>{% vimeo 58817138 %}</pre>

## Raw

If there're some contents can't be processed in posts, you can wrapped it with `rawblock` tag.

{% raw %}
<figure class="highlight"><pre>{% rawblock %}
content
{% endrawblock /%}
</pre></figure>
{% endraw %}
