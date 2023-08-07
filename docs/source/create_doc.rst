.. _create:

How to Create a Document
=========================

If you have not used Read the Docs (RTD), start with the `Read the Docs tutorial`_.

.. _Read the Docs tutorial: https://docs.readthedocs.io/en/stable/tutorial/

NCSA Document Template
-----------------------

The `NCSA document template`_ is available on the NCSA GitHub. This template will be updated, as needed, so always start here when generating a new document.

.. _NCSA document template: https://github.com/ncsa/user_documentation_template

.. _drafting_new:

Drafting a New Document
------------------------

To start a new document, you will need access to the NCSA Organization in GitHub. If you do not have access, request access `here`_.

.. _here: https://wiki.ncsa.illinois.edu/display/NCSASoftware/GitHub

The expectation is that new RTD documentation will have at least one SME/peer review AND one editorial review prior to going live to users to minimize errors in the initial user-presented product.

1. Use the `NCSA document template`_ from the NCSA GitHub to create your new repository. Instructions on how to create a repository from a template are available on `GitHub <https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template/#creating-a-repository-from-a-template>`_.
2. Contact XXXX to request your new repository be imported into the NCSA RTD account. This can be completed right after you create your initial GitHub repository, after you've built it out, or anywhere in between.
3. *Before* you start adding content into your new repository, it is highly recommended that you create an outline for your documentation. The outline does not need to be fancy (pen and paper works!) but it *will* save you time in the long run.
4. Add your content into the various files in your repository, following the :ref:`style`.

   - Click the pencil icon in the top-right to edit a file.

     .. image:: images/edit-button-marked.png
        :alt: GitHub edit button
        :width: 700

   - Use the preview function in GitHub *before* committing changes. This will help you identify most syntax issues prior to committing the changes.

     .. image:: images/preview-button.png
         :alt: GitHub preview button
         :width: 400

   - Save changes by committing them using the green **Commit changes...** button in the top-right.

     .. image:: images/commit-button.png
         :alt: GitHub commit button
         :width: 400

   - In the commit changes pop-up window, include a brief description of the change(s) you made to the file in the 'Commit message' field and a more detailed description in the 'Extended description' field.
     
   - Click the **Commit changes** button.

     During initial documentation development (before it is live to users), it is acceptable to build the documentation by committing changes to the main branch. For information on creating a pull request see :ref:`pull_request`.

     .. image:: images/commit-pop-up-marked.png
         :alt: GitHub commit changes pop-up window
         :width: 400

5. If your repository has been imported into RTD, after you commit changes to the GitHub repository, wait for RTD to rebuild the page (can take 1-3 minutes) and refresh the RTD page to view your changes. 
6. If the changes do not reflect after 3 minutes, check your reST in the GitHub repository for syntax errors; reST is particularly sensitive to indentation and line spacing. 
7. When content entry is complete, submit the documentation to at least one SME peer reviewer AND one editorial reviewer.
8. After reviewer comments are incorporated, the new document can be approved to go live to users.

Migrating an Existing Document into RTD
----------------------------------------

To migrate content from an existing wiki page into RTD, follow the below steps to convert the wiki html into reST.

To migrate a document, you will need access to the NCSA Organization in GitHub. If you do not have access, request access `here`_.

.. _here: https://wiki.ncsa.illinois.edu/display/NCSASoftware/GitHub

The expectation is that new RTD documentation will have at least one SME/peer review AND one editorial review prior to going live to users to minimize errors in the initial user-presented product.

1. Go to the page on the wiki you want to migrate.
2. Click on the **...** button in the upper right and select "View Storage Format".
3. Copy the html in the pop-up window.
4. Create a blank file on your local machine and paste your copied html into the file. This example uses sample_raw.html.
5. On your local machine, run the magic perl script :download:`(attached) <documents/html_transform_embedded_code_versA.pl>` to scrub out the code blocks and replace them with <pre>. 

   .. code-block:: console

      html_transform_embedded_code_versB.pl sample_raw.html sample_blocked.html. 

   - This produces sample_blocked.html that has the block features from the wiki fixed.

6. Run the resulting file through the "prune" perl script to remove any non-breakable spaces.

   .. code-block:: console
      
      prune_nbsp_from_html_versB.pl sample_blocked.html sample_blocked_pruned.html

7. Run the resulting source file through pandoc to produce an .rst file.

   .. code-block:: console

      pandoc -t rst -o sample_blocked_pruned.rst sample_blocked_pruned.html

8. If you have not already, create a GitHub repository for the documentation by following the steps in :ref:`drafting_new`.
9. Open the applicable .rst file from the templated files in your GitHub repository or create an empty .rst file in the repository, if needed. This example will paste the output into index.rst in the GitHub repository.
10. Copy the contents of the final .rst file on your local machine (sample_blocked_pruned.rst in the example) into the GitHub repository file (index.rst in the example).
11. Use the preview function in GitHub *before* committing changes. This will help you identify most syntax issues prior to committing the changes.

    .. image:: images/preview-button.png
       :alt: GitHub preview button
       :width: 400

12. Click the **Commit changes...** button in the top-right.

    .. image:: images/commit-button.png
       :alt: GitHub commit changes button
       :width: 400

    - In the commit changes pop-up window, include a brief description of the change(s) you made to the file in the 'Commit message' line and a more detailed description in the 'Extended description'.

    - Click the **Commit changes** button.

      During initial documentation development (before it goes live to users), it is acceptable to build the documentation by committing changes to the main branch. For information on creating a pull request see :ref:`pull_request`.

      .. image:: images/commit-pop-up-marked.png
          :alt: GitHub commit changes pop-up window
          :width: 500

13. If your repository has been imported into RTD, after you commit changes to the GitHub repository, wait for RTD to rebuild the page (can take 1-3 minutes) and refresh the RTD page to view your changes. 
14. If the changes do not reflect after 3 minutes, check your reST in the GitHub repository for syntax errors; reST is particularly sensitive to indentation and line spacing. 
15. Repeat this process for any additional wiki pages that you want to migrate into your RTD documentation. You will likely need to cut contents out the .rst file that was converted from html and paste it into various files (index, user guide, quick start, help, ...) in the GitHub repository to align with the GitHub NCSA documentation template.
16. When content entry is complete, submit the documentation to at least one SME peer reviewer AND one editorial reviewer.
17. After reviewer comments are incorporated, the new document can be approved to go live to users.

.. _create_review:

New RTD Document Review/Approval
---------------------------------

The expectation is that new RTD documentation will have at least one SME/peer review AND one editorial review prior to going live to users to minimize errors in the initial user-presented product.

This expectation applies to new documentation and existing wiki documentation that is migrated to RTD.
