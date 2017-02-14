.. _belowthresholdprocurements:

Below Threshold Procurements
============================

Procedures not covered by PPL 131 (below 100.000 MDL - for work assignments and 80.000 MDL - for goods and services) are held in line with this procedure. The procurement process is carried out in the following sequence:

#. Clarify the procurement conditions
#. Accept bids
#. Conduct an auction
#. Qualify the participants, determine a winner
#. Conclude an agreement

Creating a tender
-----------------

Creating a tender, CA determines key fields of the yet-to-be announced procurement, uploads tender documentation, with  the requirements to the procurement object indicated, EO, expected procurement price, and other information related to the tender should be set out, as well as that which determines winner selection criteria:

* Price

Peculiarities of a multi-lot tender
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

PE can split the procurement into several lots preserving the first three CPV digits. Creating a procurement, the first lot is created automatically. Provided PE has not created any new lots, the procurement is then regarded as a single lot one. 

The document structure is depicted below:

:CHART:

Lots can differ in goods or services quantity, estimated value, delivery place, procurement item (preserving the first three digits).

An example of the data structure of a multi-lot tender:

:lots.status:     
   lot status (active, cancelled, unsuccessful), not displayed

:lots.description:
   lot remarks (other info PE sees as fit)

:lots.title:
   Generalized lot name

:lots.minimalStep.currency:
   by default the same as lots.value.currency, not displayed

:lots.minimalStep.amount:
   minimal step (price and % from the estimated value, with automatic calculation)

:lots.minimalStep.valueAddedTaxIncluded:
   by default the same as lots.value.valueAddedTaxIncluded

:lots.auctionPeriod.startDate:
   start date of the auction

:lots.auctionPeriod.endDate:
   end date of the auction

:lots.value.currency:
   Currency (MDL,EUR,USD)

:lots.value.valueAddedTaxIncluded:
   false

:lots.auctionURL:
   link to the auction

:lots.id:
   lot ID

Document types
~~~~~~~~~~~~~~

Uploading documents into the tender announcement, CA can choose the document type. The following document types are not obligatory but it is best advised to regard them as such:

* Tender documentation (*biddingDocuments*)
* Technical requirements to the procurement item (*technicalSpecifications*)
* Qualification criteria (*eligibilityCriteria*)
* Evaluation criteria (*evaluationCriteria*)
* Draft contract (*contractProforma*)
* Other (no documentType) 
* Commercial proposal (*commercialProposal*)
* Technical proposal (*technicalProposal*)

Procurement nomenclature
~~~~~~~~~~~~~~~~~~~~~~~~

CA can divide a procurement into separate elements, determining the required quantity of every item. Items can differ according to the classification code (preserving the same CPV group, e.g. the first three digits shall not change ), delivery place and  time, along with the procurement process description. At least one nomenclature shall be created in the tender. 

:items.description: 
   procurement object name

:items.classification.scheme: 
   CPV according to Common Procurement Vocabulary (CPV), not shown

:items.classification.description: 
   CPV code which describes the procurement item

:items.classification.id: 
   classification code title in Romanian

:items.deliveryAddress.postalCode: 
   postal code

:items.deliveryAddress.countryName: 
   country

:items.deliveryAddress.streetAddress: 
   street

:items.deliveryAddress.region: 
   region

:items.deliveryAddress.locality: 
   town/city

:items.deliveryDate.endDate: 
   goods delivery time/execution time of works/ services provision time

:items.unit.code: 
   measurement unit code

:items.unit.name:
   measurement unit 

:items.quantity: 
   goods quantity or the scope of execution of works or services provision 

:items.estimatedValue: 
   expected value

Clarification period
--------------------

Clarification period is separately distinguished in the procurement procedure during the which participants can ask questions regarding the procurement requirements (participant qualification requirements or procurement object requirements), demand issue resolution, and submit a complaint, while procuring entities can provide answers to questions and introduce changes into the procurement conditions. The duration of the clarification period and offer submission is determined by a Procuring Entity. 

Submission of offers
--------------------

Legal entities, sole entrepreneurs and natural persons (residents and non-residents).

Once the clarification period is over, the system automatically chooses date and time of the auction, and Platforms inform participants and procuring entities about it; procuring entities can no longer introduce changes into the tender announcement. Participants submit offers that are confidential.

Fields filled out by the user
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:bids.value.amount: 
   offer value without VAT

Fields generated by the CDB automatically
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:bids.date: 
   offer submission date

:bids.id: 
   offer ID

:suppliers.contactPoint.telephone: 
   participant’s contact phone

:suppliers.contactPoint.name: 
   participant’s name

:suppliers.contactPoint.email: 
   participant’s email address 

:suppliers.identifier: 
   identification scheme according to the IATI standard (for instance, for Moldova: MD-IDNO)

:suppliers.id: 
   Moldovan National Registry ID

:suppliers.name: 
   participant’s name

:suppliers.address.postalCode: 
   postal code

:suppliers.address.countryName: 
   country

:suppliers.address.streetAddress:
   street name, building number and office number

:suppliers.address.region: 
   region

:suppliers.address.locality: 
   town/city

:bids.value.currency: 
   currency

:bids.value.valueAddedTaxIncluded: 
   false (VAT not included)


Peculiarities of a multi-lot tender
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If a procurement was split into lots, Participant can submit one offer for one or several lots simultaneously. Participant can upload files on the entire procurement (if the documents for all the lots are the same) or for each lot separately (if the documents differ).

Fields filled out by User:

:bids.lotValues.value.amount:
   bid value

Fields filled out automatically:

:suppliers.address.locality:
   City/Town/Village

:bids.lotValues.value.currency:
   Currency

:bids.lotValues.value.valueAddedTaxIncluded:
   false (VAT not included)


Auction
-------

Platform receives the links to two pages from the CDB - an individual link of the auction participant which has to be sent to this participant only and no one else and a public link to the auction which is published on platforms and official website.

Auction participant accesses his personal page via this link and participates in the auction. Auction is held centrally, with the help of separate CDB components.

Peculiarities of a multi-lot procurement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Auctions are held for each lot separately. Information disclosure on participants occurs once the last auction in the procurement is completed.

During the auction
~~~~~~~~~~~~~~~~~~

.. important::

              Do not accept a bid higher than the estimated value of the contract!

Date and time of the auction is determined by the CDB automatically, once the clarification period is completed. Platforms have to inform their users about the upcoming auction beginning date. If no participant is  registered after the end of the clarification period, the system automatically changes the procurement status to ‘unsuccessful’. If only one participant submitted the offer, the System then automatically registers the participant as a candidate, and procurement procedure then moves to ‘active: qualification’ status.

If more than one participant is registered, the System activates the single ‘Auction’ module. Those participants who registered their offer for this particular procurement can participate in the auction. All the other users, including the procuring entity of this procurement process, can observe how the auction develops via a public link that is published on platforms and the official website.


Once the Auction module begins, the Platforms are granted access to the auction Internet page for participant authorization and access provision to the auction. By clicking on the link, the Participant agrees to its conditions, after which he receives access to the auction. The following is on the auction page:

* Auction number
* Procurement objects
* ‘Participant’s auction number’ which ensures anonymous participation
* Every participant’s starting bid
* Time till the beginning of the auction and/or participant’s bid

Upon the auction beginning, the System makes a 5 minute pause and announces a round. After the pause, the System automatically announces a round. In every round participants in the order of bid registration during the time period of 2 minutes can make a bid to lower minimum for one reduction step their previous bid.

If the participant has made his choice earlier, the System allows him to introduce changes until the time runs out. If the participant has not performed any action, once the 2 minute period is over, the System keeps unchanged the earlier submitted bid and allows the next participant to make a bid. Once the first round is over, the System makes a 2 minute pause and announces round 2. Auction consists of 3 rounds.

Qualification of participants and identification of the procurement winner
--------------------------------------------------------------------------

Procuring entity sequentially reviews the received tender offers, beginning with the smallest suggested price till the highest. If the participant’s offer with the lowest bid is in compliance with  the procuring entity’s requirements, Procuring entity uploads a document that reflects his decision and determines this offer a winner (**awards:status:active**).

If it is not in compliance with the requirements, Procuring entity uploads a protocol confirming his decision to disqualify the participant, and declines such an offer (**awards:status:unsuccessful**). The systems then begins to evaluate the next, from the lowest price point of view, participant (**awards:status:pending**). 

If all the offers were declined by Procuring entity upon the completion of clarification process, the tender automatically changes to status ‘unsuccessful’.

While making the final decision (upload of the tender offer review protocol and tender offer change to one of the two possible statuses).

Additionally, CA confirms participant’s (that was determined as a winner) qualification with checkboxes:

* *Award.qualified* - complies with qualification criteria set by CA in the tender documentation

* *Award.eligible* - no grounds to reject the offer according to the Law of the Republic of Moldova exist

Having decided on the winner, the participant that was determined as a winner can upload additional documents to his tender offer (certificates).

Declining the offer, CA has to choose one or several reasons from the dropdown list. Based on his/her choice, fields **title** (grounds for declining) and **description** (argumentation). In case several reasons were selected, the respective fields are merged into one. 

CA, in free form, indicates grounds for declining in the ‘argumentation’ field (**description**). The user cannot change the wording of the grounds for declining (**title**) chosen from the dropdown list. The procedure is executed for each declined participant and his tender offer separately.

.. hint:: 

         Attempting to click the button to change status, the following warning should be displayed: ‘Attention! Pressing the button ‘Decline the offer’ is of irreversible character. This decision can changes only if the participants wishes to appeal against the CA’s decision in the prescribed by the Law order. Please make sure that all the published documents are in line and that you have made the right decision regarding qualification’.

If all the offers were declined by CA upon the qualification, the tender automatically changes to status *‘unsuccessful’*.

Procurement cancellation
------------------------

Procuring entity can cancel the procedure anytime before its completion, apart from terminal statuses (e.g. cancelled, unsuccessful, complete), with compulsory indication of cancellation reason (*cancellations:reason field*).

Concluding an agreement
-----------------------

No sooner than two working days after the announcement of the winner, procuring entity shall publish and change to active status the concluded agreement, filling out the following compulsory fields (meta-info):

:Contracts.contractNumber: 
   contract number 

:Contracts.dateSigned: 
   signature date

:Contracts.period.startDate: 
   contract term

:Contracts.period.endDate: 
   contract term

Before the contact’s status is changed to **active**, Procuring entity should be able to:

* Modify the information and the uploaded files (PUT / contracts / {cid} / documents / {did}). Upon it, procuring entity signs the agreement with EDS (in such case, the status changes to **active**)

* Change contract status to active without EDS (only for belowThreshold)

CA changes the agreement to signed status (active), upon which CA has to change tender to complete status by a separate action.

At this point, the process is completed, and no further actions in the documents are required.



