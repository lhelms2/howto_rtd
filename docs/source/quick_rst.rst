.. quick:

Quick Start Guide to reStructuredText
======================================

This quick start guide is intended to cover the basics of reStructuredText (RST) so that you can start generating your user documentation. More information about RST is available `here`_.

.. _here: https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html

Headings
---------

The document title and headings are created using non-alphanumeric 7-bit ASCII characters. Underline each heading (under- and over-line the title) with the chosen character, ensuring the line is *at least* as long as the heading, or title. The below characters match the *link* style guide.

::
 
  #################################
  Top Document Title (pound signs)
  #################################
  
  Heading 1 (equal signs)
  ========================
  
  Heading 2 (hyphens)
  --------------------
  
  Heading 3 (tildes)
  ~~~~~~~~~~~~~~~~~~~
  
  Heading 4 (dollar signs)
  $$$$$$$$$$$$$$$$$$$$$$$$$$

Paragraphs
-----------
Paragraphs are created by separating text with blank lines, see the example below.

::

  This is a paragraph.

  This is another paragraph.

Inline Markup
--------------

Bold
~~~~~

To make a word or phrase display in boldface, surround it with double asterisks.

This is an example of **boldface**

::

  This is an example of **boldface**

Italics
~~~~~~~~

To make a word or phrase display in italics, surround it with single asterisks.

This is an example of *italics*

::

  This is an example of *italics*

Hyperlinks
~~~~~~~~~~~

External Targets
$$$$$$$$$$$$$$$$$

To create single word hyperlinks to external targets, insert an underscore after the word and define the target on a separate line. See the example below.

External hyperlink example with Google_.

.. _Google: https://www.google.com

::

  External hyperlink example with Google_.

  .. _Google: https://www.google.com

For hyperlinks that include spacing or punctuation, surround the word or phrase with backticks (`) prior to appending the underscore.

This `links to Wikipedia`_

.. _links to Wikipedia: https://en.wikipedia.org

::

  This `links to Wikipedia`_

  .. _links to Wikipedia: https://en.wikipedia.org

Internal targets
$$$$$$$$$$$$$$$$$

To create hyperlinks to sections within the document, precede the heading with an underscore. If the heading has spaces or punctuation, surround it with backticks (`).

This links to the Headings_ section.

::

  This links to the Headings_ section.

**fix** To link to another page within the document, add a label to the section and use the label as the target. See example below. 

::

  .. style:

  User Documentation Style Guide
  ================================

This links to the :ref: `style`.

::

  This links to the style_.

The Importance of Indentation
------------------------------

Indentation is critical in RST. Many RST tags begin with a certain set of characters and those are assumed to start at the left margin. But the Sphinx engine then assumes that everything after the tag that is indented is also part of that tag. 

If you fail to indent tag contents after the tag, they will not be associated with the tag. 

If you inadvertently indent contents after a tag that you don't want associated with that tag, they are assumed to be associated with the tag and may result in rendering issues.

If you're having issues with something rendering correctly, check your indentation and line spacing first!

Lists
------

For guidelines on when to use bullet or numbered lists, see the *link* style guide.

Bullet Lists
~~~~~~~~~~~~~

Bullet lists can be created using - (hyphen), * (asterisk), or + (plus sign). 

There must be a blank line inserted before the first item in the list and after the last item.

::

  This is a bullet list:

  - This is the first bullet
  - This is the second bullet
  - This is the last bullet

This is a bullet list:

- This is the first bullet
- This is the second bullet
- This is the last bullet

Numbered Lists
~~~~~~~~~~~~~~~~

Numbered lists can be created by manually numbering each item (1, 2, 3, ...) or through automatic numbering using #. 

Same as a bullet list, there must be a blank line before the first item and after the last item.

::

  This is a numbered list:

  1. One is the first number on the list
  #. This number was auto-generated
  #. This number was also auto-generated and is the last number on the list

This is a numbered list:

1. One is the first number on the list
#. This number was auto-generated
#. This number was also auto-generated and is the last number on the list

.. _warning:

Notes and Warnings
-------------------

Notes and warnings use the .. note:: and .. warning:: tags, respectively. The content of the note is then indented on subsequent lines.

::

  .. note:: 

    This is a note. Use notes sparingly.

  .. warning::

    This is a warning. Warnings should be used for information the user needs to know to avoid negative consequences. Use warnings sparingly.

.. note::

  This is a note. Use notes sparingly.

.. warning::

  This is a warning. Warnings should be used for information the user needs to know to avoid negative consequences. Use warnings sparingly.

Images
-------

Images can be inserted using .. image:: or .. figure:: .

A figure is an image with a caption.

::
  .. image:: theimage.jpeg
    :alt: This is the alternative text for the image.

  .. figure:: thefigure.jpeg
    :alt: This is the alternative text for the figure.

    This is the caption for the figure.

Code Block
-----------

Code block is inserted using :: . The content of the code block is then indented under the :: with one blank line below the tag. If you omit the blank line or don't indent, the code block will not render correctly. 

::

  :: 

    This is the content of the code block

    This is more content and it's still indented

::

  This is the content of the code block

  This is more content and it's still indented

Table of Contents
------------------

Table of contents are generated by created with the .. toctree:: tag. The recommended max depth of a toctree is 2. There is an example of a toctree on the landing page of this how to document.

::

  .. toctree::
    :maxdepth: 2

    source_file_1
    source_file_2

Labels
-------

Add a label to a section using the syntax below.

::

  .. _alias:

Comments
---------

Comments can be inserted using the .. tag. Indent the content of the comment.

::

  ..
    This is a comment. It will not be rendered.

Tables
-------

Simple Tables
~~~~~~~~~~~~~~

Simple tables use = (equal sign) and - (hyphen) to define the heading(s), rows, and columns as shown in the example below. Simple tables are simple to create but have limitations on row and column spanning.

::
  
    === === ===
    Addends Sum
    ------- ---
     a   b  a+b
    === === ===
     1   2   3
     5   6   11
     4   2   6
    === === ===


=== === ===
Addends Sum
------- ---
 a   b  a+b
=== === ===
 1   2   3
 5   6   11
 4   2   6
=== === ===

Grid Tables
~~~~~~~~~~~~

Grid tables are crated using - (hyphen) for row delineators, + (plus sign) for corner delineators, and | (vertical bar) for column delineators. Grid tables are more cumbersome to create but offer more flexibility in row and column spanning.

::

    +------------+------------+-----------+
    |     Header of the Addition Table    |
    +============+============+===========+
    |         Addends         |    Sum    |
    +------------+------------+-----------+
    |     2      |            |     7     |
    +------------+     5      +-----------+
    |     4      |            |     9     |
    +------------+------------+-----------+
    |     6      |     7      |     13    |
    +------------+------------+-----------+

+------------+------------+-----------+
|     Header of the Addition Table    |
+============+============+===========+
|         Addends         |    Sum    |
+------------+------------+-----------+
|     2      |            |     7     |
+------------+     5      +-----------+
|     4      |            |     9     |
+------------+------------+-----------+
|     6      |     7      |     13    |
+------------+------------+-----------+

Where to go for help with RST (at NCSA)
-----------------------------------------

There is an abundance of Sphinx/RST resources available online but if you're having an issue that you cannot resolve, reach out to XXXX. 
