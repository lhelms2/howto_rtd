.. _style:

NCSA User Documentation Style Guide
====================================

This style guide should be followed when developing, editing, or reviewing NCSA user documentation. Adhering to the style guide will ensure that NCSA user documentation has a consistent look and feel to improve user readability.

Default Style Manual
----------------------

NCSA user documentation should follow the Chicago Manual of Style (CMOS), `available online`_ through the UIUC Library.

.. _available online: https://www-chicagomanualofstyle-org.proxy2.library.illinois.edu/home.html

Inclusivity Guidelines
-----------------------

NCSA user documentation should follow the Association for Computing Machinery `(ACM) Guidelines`_ to eliminate non-inclusive language.

.. _(ACM) Guidelines: https://www.acm.org/diversity-inclusion/words-matter

General Writing Guidelines
---------------------------

Use active voice when writing.

Use imperative mood and talk to the user in the second person.

Be concise. Avoid unnecessary qualifiers, for example instead of "In order to..." use "To..."

Avoid negatives, where practical, unless in a warning statement.

Avoid unnecessary non-English words, including Latin abbreviations (i.e., e.g., et.al., etc.)

Use the serial/Oxford comma.

Use one space between sentences.

.. _headings_style:

Headings
----------

In reStructuredText (RST), the below :ref:`headings_rst` hierarchy should be followed.

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

Bold and Italics
-----------------

Bold should be used to emphasize an action. Use bold sparingly or the effect will be lost.

Italics should be used for general emphasis. Use italics sparingly or the effect will be lost.

.. _lists:

Bullet and Numbered Lists
--------------------------

A list should have a least 3 items; if less than 3, use paragraphs.

Lists should use sentence case.

List items can be phrases or full sentences, but consistency should be maintained within the list.

Use :ref:`bullet` for items when the order does not matter.

Use :ref:`numbered` for items when the order matters.

Images
-------

Images should include *meaningful* alt text to support accessibility. `Web Accessibility in Mind (WebAIM)`_ is a good resource to learn the basics of alt text.

.. _Web Accessibility in Mind (WebAIM): https://webaim.org/techniques/alttext/

Table of Contents
------------------

Recommend formatting a :ref:`toc` with a max depth of 2 for readability. This is preset in the index.rst file in the `NCSA documentation template`_.

.. _NCSA documentation template: https://github.com/ncsa/user_documentation_template

Notes and Warnings
-------------------

Insert a note for information the user needs to pay particular attention to. Use notes sparingly or the effect will be lost.

Insert a warning for information that the user needs to know to avoid a *negative consequence*. Use warnings sparingly or the effect will be lost.

How to insert :ref:`warning` in RST.

General Descriptions of NCSA Resources
---------------------------------------

For general descriptions of NCSA resources, recommend maintaining consistency with the `NCSA Facilities Statement Home`_ and `Computing Systems and Services`_ pages, whenever practical.

.. _NCSA Facilities Statement Home: https://wiki.ncsa.illinois.edu/pages/viewpage.action?spaceKey=NFS&title=NCSA+Facilities+Statement+Home

.. _Computing Systems and Services: https://www.ncsa.illinois.edu/expertise/compute-resources/computing-systems-and-services/

Acronyms
---------

Common acronyms (common to a beginner user) such as RAM do not need to be defined at first use, all others should be defined at first use on a page (unless it is already defined on the documentation’s landing page).

Naming Conventions
--------------------

Slurm - on first use, can refer to it as "Slurm, formerly known as Simple Linux Utility for Resource Management (SLURM)", second and all future references should simply be stated as "Slurm" (title case).

Spack - use title case
