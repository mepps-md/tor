.. _qualification:

Qualification Operations
========================

When the auction is over, the qualification process starts. The status of tender
is `active.qualification` then.  Right after results are submitted to
Central DB, there is an award generated for the auction winner.

Listing awards
~~~~~~~~~~~~~~

The pending award can be retrieved via request to list all available awards:

.. include:: qualification/awards-get.http
   :code:


When the award is in `pending` status, it means that procuring entity has
to review documents describing the bid and other bidder documents.

Disqualification
~~~~~~~~~~~~~~~~

The protocol of Qualification Committee decision should be uploaded as
document into award and later its status should switch to either `active`
(if it is accepted) or `unsuccessful` (if rejected).

.. include:: qualification/award-pending-upload.http
   :code:

The Qualification Committee can upload several documents, for example, decisions to
prolong the qualification process - in order to allow the bidder to collect all the
necessary documents or correct errors.  Such documents would help to have
procedure as transparent as possible.

.. include:: qualification/award-pending-unsuccessful.http
   :code:

Note that after award rejection the next bid in the value-sorted bid
sequence becomes subject of subsequent award.  For convenience you can use
the `Location` response header from the response above that is pointing
to an award in "pending" state.


Contract Awarding
~~~~~~~~~~~~~~~~~

Protocol upload:

.. sourcecode:: http

  POST /tenders/64e93250be76435397e8c992ed4214d1/awards/{}/documents HTTP/1.1

Confirming the Award:

.. sourcecode:: http

  PATCH /tenders/64e93250be76435397e8c992ed4214d1/awards/{} HTTP/1.1

  {
      "data":{
          "status": "active"
      }
  }

.. sourcecode:: http

  HTTP/1.1 200 OK

The procuring entity can wait until bidder provides all the missing documents
(licenses, certificates, statements, etc.) or update original bid documents
to correct errors.  Alternatively, they can reject the bid if provided
documents do not satisfy the pass/fail criteria of tender (even before
full package of supplementary documents is available).

Cancelling Active Award
~~~~~~~~~~~~~~~~~~~~~~~

Sometimes Bidder refuses to sign the contract even after having passed
qualification process.  In this case, Procuring Entity is expected to be able
to reject approved award and disqualify Bid afterwards.

After we have Award with active status:

.. include:: qualification/award-active-get.http
   :code:

There is need to cancel it:

.. include:: qualification/award-active-cancel.http
   :code:

Note that there is Location header returned that aids in locating the "fresh"
award that is most likely subject for disqualification:

.. include:: qualification/award-active-cancel-upload.http
   :code:

.. include:: qualification/award-active-cancel-disqualify.http
   :code:

In the case when there is another Bid for qualification, there will be
Location header in the response pointing to its Award.


