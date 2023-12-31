.. _style:

NCSA User Documentation Style Guide
====================================

Follow this style guide when developing, editing, or reviewing NCSA user documentation. Adhering to the style guide will ensure that NCSA user documentation has a consistent look and feel for user readability.

Default Style Manual
----------------------

NCSA user documentation should follow the Chicago Manual of Style, `available online`_ through the UIUC Library.

.. _available online: https://www-chicagomanualofstyle-org.proxy2.library.illinois.edu/home.html

Inclusivity Guidelines
-----------------------

NCSA user documentation should follow the Association for Computing Machinery `(ACM) Guidelines`_ to eliminate non-inclusive language.

.. _(ACM) Guidelines: https://www.acm.org/diversity-inclusion/words-matter

General Writing Guidelines
---------------------------

- Write in the active voice.

  - Example:
    
    - NCSA experts manage the complex requirements surrounding sensitive data.

  - NOT

    - The complex requirements surrounding sensitive data are managed by NCSA experts.

- Write in the imperative mood and talk to the user in the second person.

  - Example:

    - Email help@ncsa.illinois.edu to request a refund.

  - NOT

    - Projects wishing to request a refund should email help@ncsa.illinois.edu.

- Be concise and avoid unnecessary qualifiers. For example, instead of "In order to..." use "To..."
- Avoid unnecessary non-English words, including Latin abbreviations (i.e., e.g., et.al., etc.)
- Use the serial/Oxford comma.
- Insert *one* space between sentences.
- Common acronyms, such as RAM, do not need to be defined at first use, all others should be defined at first use on a page (unless it is already defined on the documentation’s landing page).

.. _headings_style:

Headings
----------

Write headings in title case.

Follow the below :ref:`headings_rst` hierarchy in reStructuredText (reST).

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
  

Bold and Italics
-----------------

Boldface text emphasizes an action. Use boldface sparingly or the effect will be lost.

Italics are for general emphasis. Use italics sparingly or the effect will be lost.

.. _lists:

Bullet and Numbered Lists
--------------------------

A list has at least 3 items; if less than 3, use paragraphs.

Lists use sentence case.

List items can be phrases or full sentences but maintain consistency within the list.

Use :ref:`bullet` for items when the order *does not* matter.

Use :ref:`numbered` for items when the order matters.

Hyperlinks
-----------

Create hyperlinks that are descriptie and make sense out of context, for accessibility. For example, instead of 'click here', the hyperlink text for the NCSA homepage would be 'NCSA homepage'. 

Do not include the word 'link' in the hyperlink text, it is redundant; for accessibility, a screen reader will automatically announce the presence of a link.

Images
-------

Include *meaningful* alt text in images to support accessibility. `Web Accessibility in Mind (WebAIM)`_ is a good resource to learn the basics of alt text.

.. _Web Accessibility in Mind (WebAIM): https://webaim.org/techniques/alttext/

Do not include the words 'image of' or 'picture of' in alt text, it is redundant.

Table of Contents
------------------

The recommend formatting for a :ref:`toc` is with a max depth of 2 for readability. This is preset in the index.rst file in the `NCSA user documentation template`_.

.. _NCSA user documentation template: https://github.com/ncsa/user_documentation_template

Notes and Warnings
-------------------

Notes are for information the user needs to pay particular attention to. Use notes sparingly or the effect will be lost.

Warnings are for information the user needs to know to avoid a *negative consequence*. Use warnings sparingly or the effect will be lost.

How to insert :ref:`warning` in reST.

General Descriptions of NCSA Resources
---------------------------------------

General descriptions of NCSA resources should maintain consistency with the `NCSA Facilities Statement Home`_ and `Computing Systems and Services`_ pages, whenever practical.

.. _NCSA Facilities Statement Home: https://wiki.ncsa.illinois.edu/pages/viewpage.action?spaceKey=NFS&title=NCSA+Facilities+Statement+Home

.. _Computing Systems and Services: https://www.ncsa.illinois.edu/expertise/compute-resources/computing-systems-and-services/

Naming Conventions
--------------------

CUDA - Use all caps.

Duo (MFA) - Use title case.

i/o - Use lowercase.

Jupyter - Use title case.

Lmod - Use title case.

POSIX - Use all caps.

PyTorch - Use unique casing shown.

ROCm - Use unique casing shown.

Slack - Use title case.

Slurm - On first use, can refer to it as "Slurm, formerly known as Simple Linux Utility for Resource Management (SLURM)", second and all future references on a page should simply be stated as "Slurm" (title case).

Spack - Use title case.

SSH - Use all caps.

TensorFlow - Use unique casing shown.

Unix - Use title case (not UNIX).

URL - Use all caps.
