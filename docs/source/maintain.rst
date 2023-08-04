.. _maintain:

How to Edit and Maintain Documents
====================================

The instructions on this page assume that you have an existing page that is in a GitHub repository which feeds an existing readthedocs.io page. If you don't yet have a page in readthedocs.io, see :ref:`create`. This page details what happens when an existing part of the documentation on a page needs to be modified in some way. 

We assume the repository has a default that's called "main". When the readthedocs.io page builds, it pulls a copy of the repository at the "head" of the "main" branch and builds that. The head (or latest commit) of the main branch is the definitive, current version of the documentation.

Document edits and revisions should be performed through either a pull request or creation of an issue. It is not recommended, in most cases, for an individual to change the document and automatically commit it to the main branch.

Editing Documents Using GitHub Pull Requests
---------------------------------------------

Here is the process for making a document change using a pull request. In this example, Person A is administratively in charge, person B is the person doing the edit, and person C is another documentation writer that's not in charge of this edit.

1. A sends an email to B that says, "please add this table to the front page of X documentation".
2. B goes to the repository and opens the relevant source file for editing.
3. After doing an initial pass at the table, B goes to the top-right of the page and clicks the 'Commit changes..." button.
   
   .. image:: images/commit-button.png
      :alt: GitHub commit button
      :width: 400

   - B adds "initial table add" to the "Commit message".
   - B adds "Added preliminary version of table upon instructions from A.  Table isn't ready yet, but checking in to make sure the structure is correct and check the formatting." to the "Extended description".
   - B selects "create new branch and start a pull request". This will change the Commit changes pop-up to the Propose changes pop-up.

   .. image:: images/Propose-changes-pop-up-marked.png
      :alt: GitHub propose changes pop-up
      :width: 400

   - B clicks the "Propose changes" button.
4. The Open pull request window then opens and B reviews the comments for completeness and clicks the "Create pull request" button.

   .. image:: images/pull-request.png
      :alt: GitHub open pull request window
      :width: 700

5. B then goes to the pull request and adds a comment @-mentioning A and C, asking them to check the initial version.

   .. image:: images/pull-comment.png
      :alt: GitHub pull request comment window
      :width: 700

6. A and C receive emails about the comment in the pull request (just like receiving notifications about a comment on a Jira ticket).
7. A replies to the thread in email, and says "Yep, the structure of the table looks good, let me know when you've filled it out completely.
8. B continues to work on the edits, fills out the table, and then decides the changes are ready.  
9. B comments again in the pull request, asking A and C to review and approve the changes.
10. A looks at the repository and then comments in the pull request: "The table is fine in final form. C, please do a syntax and build check, and then B please commit it."
11. C goes to the pull request and clicks "approve" in the review box.
12. B sees the approve notification, goes to the pull request, sees the approval, checks A's message, and then clicks "merge pull request".

   .. image:: images/merge-pull.png
      :alt: GitHub merge pull request button
      :width: 700

13. B checks the readthedocs.io page in a few minutes to make sure the build finished, and the changes are correct.

.. _issues:

Requesting Document Changes Using GitHub Issues
------------------------------------------------

Instead of sending an email to someone or initiating the changes yourself and generating a pull request, you can notify the page owners that something needs to be modified/added to a page by creating an issue. Issue creation is preferred over email notifications because it creates a trackable log of requests that the document owner(s) can work through and allows others to address issues when one individual is out of office.

1. From the readthedocs.io page click on the "Read the Docs v:latest" section in the bottom-left.

   .. image:: images/rtd-footer.png
      :alt: Read the Docs footer button
      :width: 400

2. From the menu that pops-up, select "View" from On GitHub.

   .. image:: images/rtd-footer-open.png
      :alt: Read the Docs footer menu opened
      :width: 400

3. In the GitHub screen, select "Issues" from the top menu bar.

   .. image:: images/menu-bar-issue.png
      :alt: GitHub menu bar
      :width: 700

4. Click on green "New issue" button in the top-right to initiate a new issue.

   .. image:: images/new-issue-button.png
      :alt: GitHub new issue button
      :width: 400

   Fill in the Title with a brief description of the modification requested.
   Fill in the Comment section with a detailed description of requested modification. You can also directly mention someone using the @ button.
5. Once the Issue description is thoroughly filled out, click the green "Submit new issue" button towards the bottom-right.

   .. image:: images/issue-submit.png
      :alt: GitHub issue submit window
      :width: 700

6. This will create an issue that the person(s) responsible for the documentation will be notified of and can review and modify the document, as needed.

.. _edit_review:

Existing RTD Document Review/Approval Process
----------------------------------------------

For document changes, it is recommended that at least one SME peer or editorial review be performed, depending on the nature of the change. If it is a major section addition or rewrite, it is recommended that one SME peer review AND one editorial review be performed prior merging a change to the main branch. These reviews are initiated and documented by following the pull request process described above.

For the recommended review/approval process of new documents, see :ref:`create_review`.
