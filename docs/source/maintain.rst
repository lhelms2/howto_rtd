.. _maintain:

How to Edit and Maintain Documents
====================================

This page details the process for modifying part of an existing documentation page. These instructions assume that you have documentation in an existing GitHub repository that feeds an existing readthedocs.io page. If the documentation is not in readthedocs.io, see :ref:`create`.  

These instructions assume the repository has a default that's called "main". When the readthedocs.io page builds, it pulls a copy of the repository at the "head" of the "main" branch and builds that. The head (or latest commit) of the main branch is the definitive, current version of the documentation.

Documentation edits and revisions should be performed through either a pull request either directly or through creation of an issue. It is not recommended, in most cases, for an individual to change documentation and automatically commit the changes to the main branch.

.. _pull_request:

Editing Documents Using GitHub Pull Requests
---------------------------------------------

This is the process for making document changes using a pull request. These changes may be prompted by request from someone else (ideally through an issue on the GitHub page).

The expectation for documentation changes is that at least one SME/peer or editorial review will be performed, depending on the nature of the change. If the change is a major section addition or rewrite, it is recommended that one SME/peer review AND one editorial review be performed prior merging a change to the main branch. These reviews are initiated and documented by following the pull request process.

1. Navigate to the GitHub repository file for the page you want to modify and click on the edit button (pencil icon).
   
   .. image:: images/edit-button-marked.png
      :alt: GitHub edit button
      :width: 700

2. Make the changes. Using the preview function in GitHub can help you identify most reStructuredText syntax issues prior to committing the changes.

   .. image:: images/preview-button.png
      :alt: GitHub preview button
      :width: 400

3. Once the changes are complete, click the green **Commit Changes** button in the top-right.

   .. image:: images/commit-button.png
      :alt: GitHub commit changes button
      :width: 400

4. In the "Commit changes" pop-up window:

   - Add a brief description of the changes in the "Commit message" field.
   - Add a detailed description of the changes in the "Extended description" field.
   - Select "Create a new branch for this commit and start a pull request". This will change the "Commit changes" pop-up title to "Propose changes".
   - Click the **Propose changes** button.

     .. image:: images/propose-changes2-marked.png
        :alt: GitHub propose changes pop-up window
        :width: 500

5. The Open Pull Request window will now open. Review the comments for completeness and click the **Create pull request** button.

   .. image:: images/create-pull2-marked.png
      :alt: GitHub open pull request window
      :width: 700

6. Add a comment to the pull request asking your reviewer(s) to review the changes. Use @ to mention the reviewers.

   .. image:: images/comment2.png
      :alt: GitHub pull request comment window
      :width: 700

7. The reviewer(s) then reviews the changes and add comments to the pull request for revisions or approval.
8. Once the reviewer(s) approves the changes, merge the pull request by clicking the **Merge pull request** button.

   .. image:: images/merge-pull.png
      :alt: GitHub merge pull request button
      :width: 700

9. Refresh the readthedocs.io page a few minutes after merging to make sure the changes render as expected. Read the Docs builds can take 1-3 minutes to complete.

.. _issues:

Requesting Document Changes Using GitHub Issues
------------------------------------------------

Instead of sending an email or initiating the changes yourself and generating a pull request, you can notify the documentation owner(s) that something needs to be modified/added to a page by creating an issue. Creating an issue is preferred over sending an email because it creates a trackable log of requests that the documentation owner(s) can work through and allows others to address issues when an individual is out of office.

1. From the readthedocs.io page, click on **Read the Docs v:latest** in the bottom-left.

   .. image:: images/rtd-footer.png
      :alt: Read the Docs footer button
      :width: 400

2. From the menu that opens, click on **View** from the On GitHub options.

   .. image:: images/rtd-footer-open.png
      :alt: Read the Docs footer menu opened
      :width: 400

3. On the GitHub page, select "Issues" from the top menu bar.

   .. image:: images/menu-bar-issue.png
      :alt: GitHub menu bar
      :width: 700

4. Click the green **New issue** button in the top-right to initiate a new issue.

   .. image:: images/new-issue-button.png
      :alt: GitHub new issue button
      :width: 400

5. Fill in the Title with a brief description of the requested modification.
6. Fill in the Comment section with a detailed description of the requested modification. You can also use @ to directly mention someone.
7. Once the Issue description is thoroughly filled out, click the green **Submit new issue** button towards the bottom-right.

   .. image:: images/issue-submit.png
      :alt: GitHub issue submit window
      :width: 700

8. This will create an issue and the person(s) responsible for the documentation will be notified.

.. _edit_review:

Existing Read the Docs Document Review/Approval
------------------------------------------------

The expectation for documentation changes is that at least one SME/peer or editorial review will be performed, depending on the nature of the change. If the change is a major section addition or rewrite, it is recommended that one SME/peer review AND one editorial review be performed prior merging a change to the main branch. These reviews are initiated and documented by following the pull request process.
