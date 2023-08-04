.. _create:

How to Create a Document
=========================

If you have not yet used Read the Docs (RTD), it is highly recommended that you start with the `Read the Docs tutorial`_.

.. _Read the Docs tutorial: https://docs.readthedocs.io/en/stable/tutorial/

NCSA Document Template
-----------------------

The `NCSA document template`_ is available in the NCSA GitHub. This template will be updated, as needed, so please start here when generating a new document.

.. _NCSA document template: https://github.com/ncsa/user_documentation_template

.. _drafting_new:

Drafting a New Document
------------------------

To start a new document, you will need access to the NCSA Organization in GitHub. If you do not currently have access, request access `here`_.

.. _here: https://wiki.ncsa.illinois.edu/display/NCSASoftware/GitHub

It is expected that new documentation will have at least one editorial review and one SME peer review prior to advertising the RTD link to users. This will help to minimize errors in the initial user-presented product.

1. Use the `NCSA document template`_ from the NCSA GitHub to create your new repository. Instructions on how to create a repository from a template are available on `GitHub <https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template/#creating-a-repository-from-a-template>`_.
2. Contact X to import your new repository into the NCSA Read the Docs account. This can be completed right after you create your initial GitHub repository, or after you've built it out (or anywhere in between).
3. *Before* you start adding content into your new repository, it is highly recommended that you create an outline for your documentation. The outline doesn't have to be anything fancy (pen and paper works!) but it *will* save you time in the long run.
4. Add your content into the various files in your repository, following the :ref:`style`.
5. During initial documentation development (before users have access to the RTD link), it is acceptable to build the documentation by committing changes to the main branch. When committing, include a brief description of the change(s) you made to the file in the 'Commit message' line and a more detailed description in the 'Extended description'.
6. If your repository has been imported into RTD, after you make changes to the GitHub repository, wait for RTD to rebuild the page (can take 1-3 minutes) and refresh the RTD page to view your changes. 
7. If changes don't reflect after 3 minutes, check the build for error messages. If there are no build errors, check your RST in the GitHub repository for syntax errors, RST is particularly sensitive to indentation and line spacing.
8. Once the content is complete, proceed to the :ref:`create_review`.

Migrating an Existing Document into RTD
----------------------------------------

If you would like to migrate the content from an existing wiki page into Read the Docs, you can follow the below steps to convert the wiki html into rst.

To migrate a document, you will need access to the NCSA Organization in GitHub. If you do not currently have access, request access `here`_.

.. _here: https://wiki.ncsa.illinois.edu/display/NCSASoftware/GitHub

1. Go to the page on the wiki you want to migrate.
2. Click on the "..." in the upper right and select "View Storage Format" from the menu.
3. Copy the html out of the pop-up window.
4. Create a blank file on your local machine. This example uses sample_raw.html.
5. On your local machine, run the magic perl script *link*(attached) to scrub out the code blocks and replace them with <pre>. 
   html_transform_embedded_code_versB.pl sample_raw.html sample_blocked.html. 
   this produces sample_blocked.html that has the block features from the wiki fixed.
6. Run the resulting file through the "prune" perl script to remove any non-breakable spaces.
   prune_nbsp_from_html_versB.pl sample_blocked.html sample_blocked_pruned.html
7. Run the resulting source file through pandoc to produce an .rst file.
   pandoc -t rst -o sample_blocked_pruned.rst sample_blocked_pruned.html
8. If you have not already, create a GitHub repository for the documentation by following the steps in drafting_new_.
9. Create an empty .rst file in the GitHub repository, if needed, or open the applicable .rst file from the templated files.  Our example is that we'll put the output into sample.rst.
10. Copy the contents of the final .rst file on your local machine (sample_blocked_pruned.rst in example above) into the GitHub repository file (sample.rst in the example).
11. In GitHub, click the "Commit changes..." button in the top-right.
12. put a couple-of-word descriptive tag in the first line right below "Commit changes".
13. In the commit pop-up window, include a brief description of the change(s) you made to the file in the 'Commit message' line and a more detailed description in the 'Extended description'.
14. Select "commit directly to main branch" if you're working on an isolated piece and you have permissions.  Select "Create a new branch for this commit and start a pull request." if you need approvals. 
15. Click "Commit Changes" to enter the changes
16. If you committed directly to the main branch and your GitHub repository has been imported into RTD, after you make changes to the GitHub repository, wait for RTD to rebuild the page (can take 1-3 minutes) and refresh the RTD page to view your changes. 
17. If changes don't reflect after 3 minutes, check the build for error messages. If there are no build errors, check your RST in the GitHub repository for syntax errors, RST is particularly sensitive to indentation and line spacing.
18. Repeat this process for any additional wiki pages that you want to migrate into your RTD page. You will likely need to copy contents from the rst file that was converted from html to different folders in the GitHub repository to align with the GitHub NCSA user documentation template.
19. Once the content is complete, proceed to the :ref:`create_review`.

.. _create_review:

New RTD Document Review/Approval Process
-----------------------------------------

It is expected that any new RTD document will have a minimum of one SME peer review and one editorial review prior to getting approved to go live to users.

This expectation applies to new documentation and existing wiki documentation that is migrated to RTD.

For the recommended review/approval process for document edits/revisions see :ref:`edit_review`.
