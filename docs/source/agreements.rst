.. _agreements:

Working with agreements
=======================

Introducing changes into the agreement

Once the tender is completed, a new document, ‘Contract’, is formed in the CDB that can be modified while participants shall report on contract completion. This can be applied to receive the number of contracts:

GET / contracts to get the number of contracts

GET / contracts / {cid} to receive meta-information on the contract

GET / contracts / {cid} / documents / {did} to receive meta-information on the document

GET / contracts / {cid} / documents / {did}? download = {key to receive one-time link to the file

.. hint:: 
         You can find an agreement by first searching the tender to which the agreement is linked or by filling out a separate search form with details (code or name) of the EO, agreement’s ID in the format MD-... or by the actual number of the agreement indicated in meta-information etc.

The agreement contains links to the files attached that were uploaded by the CA prior to the completion of tender, meta-information about the agreement and a copy of items from the tender.

To introduce changes, CA presses the button ‘Publish changes in the agreement’ on the platform. Such an action creates a possibility to upload new files and meta-information regarding the additional agreement(s).

CA fills out the following fields:

:changes.contractNumber: 
   agreement number

:changes.rationaleTypes: 
   cases to introduce changes into substantial conditions of the agreement. CA can choose one or several reasons.

:changes.rationale: 
   description of changes introduced into the substantial conditions (free field)

The following is executed to introduce changes in the CDB:


*PATCH / contracts / {cid}* to change meta-information in the contract

*GET / contracts / {cid} / documents* to receive all documents

*POST / contracts / {cid} / documents* to upload additional documents

*PATCH / contracts / {cid} / documents / {did }* to change information regarding documents

*PUT / contracts / {cid} / documents / {did}* to upload new version of the document


These changes go into the ‘changes’ envelope, the files attached - into the ‘documents’ envelop with a link to the ID of the respective change. Change status at this point: *pending*.

For editing purposes, the following fields are displayed to CA, depending on the chosen rationaleTypes:
If rationaleTypes: volumeCuts, itemPriceVariation, priceReduction, taxRate, thirdParty were chosen

* ‘Sum of additional agreement’ contactNumber

If rationaleTypes: durationExtension, fiscalYearExtension were chosen:

* ‘Agreement End Date’ contacts.period.endDate

If rationaleTypes: volumeCuts was chosen:

* A block concerning the information on items is displayed

Once there is status active, information cannot be updated. If needed, a user should register new Change.

CA can update information on nomenclature (items) all the time beginning with automatic creation of the Contract document and up until the Contract execution.

Agreement termination
---------------------

In case of termination, CA presses the button ‘Terminate the agreement’  on the platform site.

CA fills out the following fields:

:contracts.amountPaid: 
   amount of money paid on the agreement, required

:contracts.terminationDetails: 
   reasons for agreement termination if applies (free text)

CA can attach files.

.. hint::
         Prior to changing the agreement’s status, a user should be warned about the irreversibility of such an action. The optimum version is to display a banner warning that the agreement will be changed to the status ‘Agreement terminated’. A checkbox ‘*I confirm*’ can be displayed on the banner, empty by default, and inactive button ‘*Continue*’. Upon activation of this field, the ‘*Continue*’ button becomes active.

At this point, no further actions on the agreement are made.

Agreement execution
-------------------

To report on agreement execution, CA presses the ‘Report on agreement execution’ button on the platform.

CA fills out the following fields:

:contracts.amountPaid: 
   the amount of money paid on the agreement, cannot be zero, required.

User can attach files.









