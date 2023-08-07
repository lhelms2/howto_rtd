.. _maintain:

How to Edit and Maintain Documents
====================================

The instructions on this page assume that you have an existing page in a GitHub repository that feeds an existing readthedocs.io page. If a page is not yet in readthedocs.io, see :ref:`create`. This page details the process for modifying part of an existing documentation page. 

These instructions assume the repository has a default that's called "main". When the readthedocs.io page builds, it pulls a copy of the repository at the "head" of the "main" branch and builds that. The head (or latest commit) of the main branch is the definitive, current version of the documentation.

Document edits and revisions should be performed through either a pull request or creation of an issue. It is not recommended, in most cases, for an individual to change the document and automatically commit the change to the main branch.

Editing Documents Using GitHub Pull Requests
---------------------------------------------

This is the process for making a document changes using a pull request. These changes may be prompted by request from someone else (ideally through an Issue on the GitHub page).

For document changes, it is recommended that at least one SME peer or editorial review be performed, depending on the nature of the change. If it is a major section addition or rewrite, it is recommended that one SME peer review AND one editorial review be performed prior merging a change to the main branch. These reviews are initiated and documented by following the pull request process.

1. Navigate to the GitHub repository file for the page you want to modify and click on the edit button (pencil icon).
   
   .. image:: images/edit-button-marked.png
      :alt: GitHub edit button
      :width: 700

2. Make the changes. Using the preview function in GitHub can help you identify most RST syntax issues prior to committing the changes.

   .. image:: images/preview-button.png
      :alt: GitHub preview button
      :width: 400

3. Once the changes are complete, click the green "Commit Changes" button.

   .. image:: images/commit-button.png
      :alt: GitHub commit changes button
      :width: 400

4. In the "Commit changes" pop-up window:
   - Add a brief description of the changes in the "Commit message" field.
   - Add a detailed description of the changes in the "Extended description" field.
   - Select "Create a new branch for this commit and start a pull request". This will change the "Commit changes" pop-up title to "Propose changes".
   - Click the "Propose changes" button.

   .. image:: images/propose-changes2-marked.png
      :alt: GitHub propose changes pop-up window
      :width: 500

5. The Open Pull request window will now open. Review the comments for completeness and click the "Create pull request" button.

   .. image:: images/create-pull2-marked.png
      :alt: GitHub open pull request window
      :width: 700

6. Add a comment to the pull request asking your reviewer(s) to review the changes. Use @ to mention the reviewers.

   .. image:: images/comment2.png
      :alt: GitHub pull request comment window
      :width: 700

7. The reviewer(s) then review the changes and add comments to the pull request for revisions or approval.
8. Once the reivewer(s) approves the changes, merge the pull request by clicking the green "Merge pull request" button.

   .. image:: images/merge-pull.png
      :alt: GitHub merge pull request button
      :width: 700

9. Refresh the readthedocs.io page a few minutes after merging to make sure the build finished, and the changes are correct. RTD builds can take 1-3 minutes to complete.

.. _issues:

Requesting Document Changes Using GitHub Issues
------------------------------------------------

Instead of sending an email to someone or initiating the changes yourself and generating a pull request, you can notify the page owners that something needs to be modified/added to a page by creating an issue. Issue creation is preferred over sending an email because it creates a trackable log of requests that the document owner(s) can work through and allows others to address issues when one individual is out of office.

1. From the readthedocs.io page click on "Read the Docs v:latest" in the bottom-left.

   .. image:: images/rtd-footer.png
      :alt: Read the Docs footer button
      :width: 400

2. From the menu that pops-up, select "View" from the On GitHub options.

   .. image:: images/rtd-footer-open.png
      :alt: Read the Docs footer menu opened
      :width: 400

3. On the GitHub page, select "Issues" from the top menu bar.

   .. image:: images/menu-bar-issue.png
      :alt: GitHub menu bar
      :width: 700

4. Click the green "New issue" button in the top-right to initiate a new issue.

   .. image:: images/new-issue-button.png
      :alt: GitHub new issue button
      :width: 400

5. Fill in the Title with a brief description of the modification requested.
6. Fill in the Comment section with a detailed description of requested modification. You can also directly mention someone using the @ button.
7. Once the Issue description is thoroughly filled out, click the green "Submit new issue" button towards the bottom-right.

   .. image:: images/issue-submit.png
      :alt: GitHub issue submit window
      :width: 700

8. This will create an issue that the person(s) responsible for the documentation will be notified of and can review and modify the document, as needed.

.. _edit_review:

Existing RTD Document Review/Approval Process
----------------------------------------------

For document changes, it is recommended that at least one SME peer or editorial review be performed, depending on the nature of the change. If it is a major section addition or rewrite, it is recommended that one SME peer review AND one editorial review be performed prior merging a change to the main branch. These reviews are initiated and documented by following the pull request process described above.

For the recommended review/approval process of new documents, see :ref:`create_review`.
