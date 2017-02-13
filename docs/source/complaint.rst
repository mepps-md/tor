.. _complaint:

Complaint Procedure
===================

.. note:: 

         This is not realized in the pilot MePPS and will be added to the system once the legislative framework for the complaint procedure is established.

Below Threshold Procurements
----------------------------

Below Threshold Appeals are sent to the Review Commission,  a body established by non-governmental organizations that are legally entitled to issue only recommendations to the CA.
If simplified, the procedure looks like this: 

In addition to the existing possibility to ask a question regarding a procurement, every registered user (but CAs) also can address the CA with a demand to eliminate a violation.

CA has three days to review a Demand and make a decision concerning it. Within this period of time, CA shall reply to the Demand and (provided it is satisfied) introduce respective changes into procurement requirement or qualification decision. Providing an explanation regarding the decision is obligatory, simply selecting ‘satisfied’, ‘rejected’, ‘unsatisfied’ status is not enough.

Complainant shall evaluate CA’s decision. If he/she is satisfied with the decision, the issue is resolved, and the process is completed. If he/she is not, and provided CA has not reviewed the Demand (within a 3-day period), it automatically becomes a Complaint which goes to the Review Commission. Provided complainant has not reacted to CA’s decision, the issue is considered resolved.

Commission reviews the demand and publishes a decision on it about which the CA and participants are informed, it is also published on the website of the platforms and the official website of the Authorized Body. The Commission’s decision is of advisory nature to the CA and does not result in a blocked procedure, with the only exclusion being inability to activate the uploaded agreement, provided there are yet-to-be reviewed appeals.

The user who submitted the complaint shall be able to recall it at any point until the Commission decision is made (terminal statuses: resolved, declined, invalid).

Detailed overview of the process
--------------------------------

Demand to remove violations
~~~~~~~~~~~~~~~~~~~~~~~~~~~

In below threshold procurement, a claim (complaints:type:claim) is submitted during clarification period and CA’s decision upon qualification. Awards:complaints can be submitted within 2 working days. The claim is enough to reinforce evaluation on below threshold level again (awards:complaints:type:claim, status:claim), upon which CA can cancel its decision concerning the respective participant (as to whom the claim was submitted), change it to cancelled. Afterwards, this award, and the next upon it (upon which the decision has been reached), change to cancelled status, and new awards (pending) are generated to be evaluated. Once the evaluation was carried out again, CA can react to the demand similarly as it is during the clarification period, with indication of decision (‘Satisfied’, ‘Not satisfied’, or ‘Declined’ - resolved, declined, invalid).

The information about the user who submitted the complaint is confidential.

Fields filled out by the user:

:description: 
   main body of the demand

:title: 
   shortened name

Fields filled out automatically:

:author.name: 
   participant’s name

:author.address.countryName: 
   country

:author.address.locality: 
   town/city

:author.address.postalCode: 
   postal code

:author.address.region: 
   region

:author.address.streetAddress: 
   street

:author.identifier.legalName: 
   participant’s full legal name
   
:author.identifier.scheme: 
   identification scheme according to the IATI standard

:author.identifier.id: 
   code in the scheme provided

:author.identifier.url: 
   website address

:tender.id: 
   tender ID

:type: 
   claim

:date: 
   claim submission date

:dateSubmitted: 
   claim registration date in the CDB

:id: 
   claim ID

:status: 
   claim status

User can attach files. 

CA reviews the claim and registers his/her answer, with compulsory indication of its decision in the field. This reply fills out the following fields in the same document:

:resolution: 
   CA’s reply

:resolutionType: 
   ‘Satisfied’, ‘Rejected’, ‘Unsatisfied’ (resolved, invalid, declined)

Fields filled out automatically:

:dateAnswered: 
   answer registration date in the CDB

:status: 
   status (reviewed)

User can attach files. 

Escalating a claim to a complaint
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If CA has not reviewed the Claim within a 3-day period, it automatically changes to Complaint (complaints:type->complaint). If CA has reviewed the claim, complainant evaluates the CA’s decision:

:satisfied: 
   true / false

If complainant is not satisfied with the decision he/she can escalate it to complain, provided a demand to remove violations has not been submitted earlier. If complainant has not reacted to CA’s answer regarding the Demand within 3 days, it is automatically considered resolved.

User should have a possibility to recall his/her Demand at any point of the process.

During the escalation, the following fields are automatically filled out:

:dateEscalated: 
   escalation registration date in the CDB

:status: 
   pending

:type: 
   complaint

Complaint on CA’s decision
~~~~~~~~~~~~~~~~~~~~~~~~~~

Complaint on CA’s decision can be submitted only by a tenderer no later than 10 days after the decision regarding the winner or offer declination was reached. Complaint review body has to come to a decision as to whether it will review the complaint within 3 days. If it decides not to do so, there are the following statuses:

* Invalid ‘not reviewed’

* Mistaken ‘declined as submitted by mistake’

The procedure is not blocked. If complaint review body has not registered its decision at all (status:pending) or registered its decision to accept the complaint (status:accepted), the procedure is blocked.

Blocking the procedure, CA loses a possibility to publish an agreement with the winner, further actions concerning  the qualification of participants are blocked. A possibility to carry out evaluation again appears only if the complaint has been satisfied by the Complaint review body (status:satisfied). If it is satisfied, CA can carry out qualification from the very beginning, cancelling his decision concerning the corresponding award. Upo cancellation, all awards concerning the which a decision has been reached, change to status cancelled, to evaluate again new awards with pending status are generated. Afterwards, CA reviews it again and submits a report on his action, changing the complaint to resolved status.
Procedure deblocking (submitting offers stage) occurs only upon Review Commission’s publication of decision regarding the complaint and CA’s reaction to it. Procedure deblocking (qualification stage) occurs only after the decision of the complaint body has been published and repeated qualification along with CA making the respective decision (fields tendererAction, resolution).

Procedure deblocking is ensured by complaint’s change to the terminal status resolved. Also, claims on CA’s decision can be submitted, though they do not influence the workflow, even if CA ignores it. Further escalation of such claims is not possible, they exist only for the sake of providing additional information, because the offer has been declined or determined as a winning one. CA replies to such requirements similarly as to the ones concerning the procurement requirements, indicating his answer and changing the status.

Complaint on CA’s decision
~~~~~~~~~~~~~~~~~~~~~~~~~~

Once the Review Body’s decision regarding the complaint was published, CA removes the violation and publishes a notice regarding it on his platform. The following fields are filled out in the document:

:claims.tendererAction: 
   notice of removal of violations in free form

Cancelling the claim on behalf of the complainant
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
At any moment up until the publication of decision of the Review Body (while claim is in pending or accepted status), complainant can cancel his/her claim filling out the following fields:

:claims.dateCancelled: 
   feedback registration date in the CDB

:claims.cancellationReason: 
   argumentation of reasons

If the claim has been cancelled, it changes to ‘stopping’ status. Review Body has to come to a decision regarding stopping of claim review, upon which the status changes to terminal status ‘stopped’, and further actions in the procedure are blocked. Also, review body can ‘Leave such complaint without reviewal’ (invalid).



