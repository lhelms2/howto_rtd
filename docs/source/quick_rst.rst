.. _quick:

Quick Start Guide to reStructuredText
======================================

This quick start guide is intended to cover the basics of reStructuredText (reST) so that you can start generating your user documentation. More comprehensive information about reST is available `here`_.

.. _here: https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html

The Importance of Indentation and Line Spacing
-----------------------------------------------

Indentation and line spacing are critical in reST.

Many reST tags begin with characters that are assumed to start at the left margin and the Sphinx engine then assumes that everything indented after the tag is also part of that tag. If you inadvertently indent contents after a tag that you do not want associated with that tag, they are assumed to be associated with the tag and will result in rendering issues. If you fail to indent tag contents after the tag, they will not be associated with the tag and will result in rendering issues. 

Having a blank line where one *is not* supposed to be or the absence of a blank line where one *is* supposed to be will also result in rendering issues.

If you are having issues with something rendering correctly, check your indentation and line spacing first!

.. _headings_rst:

Headings
---------

The document title and headings are created using non-alphanumeric 7-bit ASCII characters. Underline each heading (under- and over-line the title) with the chosen character, ensuring the character line is *at least* as long as the heading or title text. The below characters match the :ref:`style`.

.. code-block:: rst
 
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
Create paragraphs by separating text with blank lines, see the example below.

.. code-block:: rst

  This is a paragraph.

  This is another paragraph.

Inline Markup
--------------

Bold
~~~~~

Make a word or phrase display in boldface by surrounding it with double asterisks.

.. code-block:: rst

  This is an example of **boldface**

This is an example of **boldface**

Italics
~~~~~~~~

Make a word or phrase display in italics by surrounding it with single asterisks.

.. code-block:: rst

  This is an example of *italics*

This is an example of *italics*

Hyperlinks
-----------

External Targets
~~~~~~~~~~~~~~~~~

- Create single-word hyperlinks to external targets by appending an underscore to the end of the word and defining the target on a separate line. See the example below.

  .. code-block:: rst

    External hyperlink example with Google_.

    .. _Google: https://www.google.com

  External hyperlink example with Google_.

  .. _Google: https://www.google.com

- Create hyperlinks that include spacing or punctuation by surrounding the word or phrase with backticks (`) prior to appending the underscore.

  .. code-block:: rst

    This `links to Wikipedia`_

    .. _links to Wikipedia: https://en.wikipedia.org

  This `links to Wikipedia`_

  .. _links to Wikipedia: https://en.wikipedia.org

- Targets can also be defined inline, as shown below.

  .. code-block:: rst

    This `links to Wikipedia <https://en.wikipedia.org>`_

Internal targets
~~~~~~~~~~~~~~~~~

- Create hyperlinks to sections within the page by appending an underscore to the end of the heading name. If the heading has spaces or punctuation, surround it with backticks (`).

  .. code-block:: rst

    This links to the Headings_ section.

  This links to the Headings_ section.

- Link to a section on another page within the documentation by adding a label to the section and using the label as the target. See example below. 

  .. code-block:: rst

    .. _style:

    NCSA User Documentation Style Guide
    ====================================

  .. code-block:: rst

    This links to the :ref:`style`.

  This links to the :ref:`style`.

Lists
------

For guidelines on using bullet and numbered lists, see :ref:`lists` in the style guide.

.. _bullet:

Bullet Lists
~~~~~~~~~~~~~

Bullet lists are created using - (hyphen), * (asterisk), or + (plus sign). 

There must be a blank line before the first item in the list and after the last item.

.. code-block:: rst

  This is a bullet list:

  - This is the first bullet
  - This is the second bullet
  - This is the last bullet

  A new paragraph.

This is a bullet list:

- This is the first bullet
- This is the second bullet
- This is the last bullet

A new paragraph.

.. _numbered:

Numbered Lists
~~~~~~~~~~~~~~~~

Numbered lists are created by manually numbering each item (1, 2, 3, ...) or through automatic numbering using #. 

Same as a bullet list, there must be a blank line before the first item and after the last item.

.. code-block:: rst

  This is a numbered list:

  1. One is the first number on the list
  #. This number was auto-generated
  #. This number was also auto-generated and is the last number on the list

This is a numbered list:

1. One is the first number on the list
#. This number was auto-generated
#. This number was also auto-generated and is the last number on the list

Images
-------

Images are inserted using either the .. image:: path/filename.jpg or .. figure:: path/filename.jpg tag. 

The image options are indented under the tag, with no blank line below the tag. The most common image options are alt text (:alt:) and width (:width:).

A figure is an image with a caption.

.. code-block:: rst
  
     .. image:: images/new_bldg-1024x681.jpg
       :alt: NCSA building.
       :width: 400

     .. figure:: images/new_bldg-1024x681.jpg
       :width: 400
       :alt:

       NCSA Building. (this is the caption for the figure)

.. image:: images/new_bldg-1024x681.jpg
  :alt: NCSA building.
  :width: 400

.. figure:: images/new_bldg-1024x681.jpg
  :width: 400
  :alt:

  NCSA Building. (this is the caption for the figure)

Code Block
-----------

Code block is inserted using the .. code-block:: <language> tag. 

The content of the code block is indented under the tag with one blank line below the tag. If you omit the blank line or do not indent, the code block will not render correctly. 

Adding the language at the end of the tag allows the code block to render with syntax highlighting.

.. code-block:: rst

  .. code-block:: rst 

    This is the content of the code block

    This is more content and it's still indented

.. code-block:: rst

  This is the content of the code block

  This is more content and it's still indented

Labels
-------

Add a label to a section using the syntax below.

.. code-block:: rst

  .. _alias:

Call the label in another section of the documentation as shown below.

.. code-block:: rst

  :ref:`alias`

.. _toc:

Table of Contents
------------------

Create a table of contents with the .. toctree:: tag. The recommended max depth of a toctree is 2. 

There is an example of a toctree on the home page of this how to document (view on GitHub).

.. code-block:: rst

  .. toctree::
    :maxdepth: 2

    source_file_1
    source_file_2

.. _warning:

Notes and Warnings
-------------------

Notes and warnings use the .. note:: and .. warning:: tags, respectively. 

The content of the note or warning is indented under the tag, with one blank line below the tag.

.. code-block:: rst

  .. note:: 

    This is a note. Use notes sparingly.

  .. warning::

    This is a warning. Warnings are used for information the user needs to know to avoid *negative consequences*. Use warnings sparingly.

.. note::

  This is a note. Use notes sparingly.

.. warning::

  This is a warning. Warnings are used for information the user needs to know to avoid *negative consequences*. Use warnings sparingly.

Tables
-------

Simple Tables
~~~~~~~~~~~~~~

Simple tables use = (equal sign) and - (hyphen) to define the heading(s), rows, and columns as shown in the example below. 

Simple tables are simple to create but have limitations on row and column spanning.

.. code-block:: rst
  
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

Grid tables use - (hyphen) for row delineators, + (plus sign) for corner delineators, and | (vertical bar) for column delineators. 

Grid tables are more cumbersome to create but offer more flexibility in row and column spanning.

.. code-block:: rst

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

Comments
---------

Comments are inserted using the .. tag. Indent the content of the comment.

.. code-block:: rst

  ..
    This is a comment. It will not be rendered.
