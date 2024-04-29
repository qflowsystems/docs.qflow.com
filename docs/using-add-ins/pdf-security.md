---
layout: default
title: PDF Security
nav_order: 2
parent: Add-ins
has_children: false
has_toc: false
---
# PDF Security

The security on a PDF document impacts how the document behaves with the Acrobat Add-In as well as within Q-Action.

## Unprotected

For unprotected documents, the add-in will be able to perform all expected functionality.  Unprotected documents will have security settings that look like this:

![](/assets/images/security-settings-unprotected.png)

## Already Signed

Documents that are added to Q-Action without any signatures, then checked out and signed and check back in again, will work just like unprotected documents.

However, when a document is _added_ to Q-Action that _already_ has a signature on it, there are some functions that Q-Action is unable to perform on the document, which affects the way the add-in will work.

In particular, when the user checks out a document that was already signed when it was added, and then opens the document in Acrobat, the add-in is not able to finish the check out process automatically, and the user must intervene.  In these situations, when the user first opens the Q-Action Menus, there will be a Finish Check Out menu item instead of the usual Check In etc.

![](/assets/images/finish-checkout-menu-item.png)

Once you select the Finish Check Out menu item, then you can go about making the necessary changes to the document, and when you are done, the ‘Check In’ etc menu will be available.

## Encrypted

Encrypted documents require a password to edit the document, which prevents the add-in from manipulating the PDF in ways that are required to do anything other than add the document to Q-Action. 

The user will still be able to check out an encrypted document, make changes in Acrobat, and then check in the document using Q-Action directly, but will not be able to check the document in through the Add-In.

Encrypted documents will have security settings like this:

![](/assets/images/security-settings-encrypted.png)

## Locked

Locked documents are documents that have been certified, and the user selected No Changes Allowed as shown below:

![](/assets/images/lock-after-signing.png)

This prevents the add-in from making any further edits to the document. So, if someone checks out such a document and opens it in Acrobat with the add-in installed, then the add-in cannot finish the checkout itself, and when the user click **Finish Check Out**, the add-in will inform the user that the document is locked.

![](/assets/images/locked-add-in-error.png)

Locked documents will have security settings like this:

![](/assets/images/security-settings-locked.png)

## Restricted

Restricted documents require a password just to open the document.   If a user uploads a restricted document through the browser, they will see an error message explaining that the document cannot be added.

![](/assets/images/pw-protected-error-qaction.png)

If a user adds a restricted document using the Outlook or Acrobat Add-In, then the document will appear in the upload queue in an error state.

![](/assets/images/pw-protected-error-addin.png)

The user can then click **Upload** to add a new document that is not restricted instead, or click **Delete** to remove the document from the upload queue.