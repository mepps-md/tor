.. _report:

Report on concluded agreements
==============================

* procurementMethod: limited
* procurementMethodType: reporting

Having entered the information regarding the procedure, CA enters information on the winner and the agreement (*contracts: status:active*). 

.. hint::

   Provided the sum entered by the user adding the information regarding the participant (awards:value:amount)  differs from the earlier entered estimated value of the procurement (value:amount) in five times (either bigger or smaller), the following message shall be displayed: *‘Please note that the procedure will be published on the website of the Authorized Body only once you enter the information regarding the winner and the agreement, sign it with EDS, and complete the procedure’.*

Publication of a decision on intent to conclude an agreement 
------------------------------------------------------------

CA publishes the concluded agreement and enters information regarding the EO immediately (awards:status:active).

This information is published on the official website of the Authorized Body along with the platform’s website as a report on the concluded agreement. It is not possible to submit a complaint at this point.

CA enters the following information on the procurement (automatically filled out fields are marked with*)

:title: 
   generalized procurement name

:description: 
   remarks, not obligatory

:items.description:
   procurement’s nomenclature description

:items.classification.scheme: 
   CPV

:items.classification.id: 
   CPV code which describes the procurement item

:items.classification.description: 
   classification code title in Romanian

:items.unit.code: 
   measurement unit code  (has to go in line with the  UN/CEFACT standard, for example - KGM)

:items.unit.name: 
   measurement unit name in Romanian

:items.quantity: 
   quantity

:items.deliveryDate.startDate: 
   goods delivery period (beginning date) 

:items.deliveryDate.endDate: 
   goods delivery date (end date) 

:items.deliveryAddress:  
   delivery address

:items.deliveryLocation: 
   delivery place’s geographical coordinates 

:value.currency: 
   MDL, EUR, USD

:value.amount: 
   estimated procurement price

:value.valueAddedTaxIncluded: 
   without VAT 

Entering information on EO on the basis of the concluded agreement
------------------------------------------------------------------

CA enters information on EO on the basis of the concluded agreement. Editing is possible only until change to active status is executed. Only one option should be visible next to each participant - ‘EO on agreement’ (*awards:status:active*)

Additionally for a certain EO on the agreement, CA notes compliance with qualification criteria assigning ‘true’ value to the Award.qualified parameter.

*Award.qualified:true* - in line with qualification criteria set by the CA in the tender documentation

The following information regarding tenderers is entered by the CA (automatically filled out fields are marked with*)

:awards.documents.format: 
   document format, required

:awards.documents.url: 
   document URL, required

:awards.documents.title: 
   document title, required

:awards.documents.documentOf: 
   what does the document concern (tender), required

:awards.documents.datePublished: 
   publication date, required

:awards.documents.documentType: 
   document type

:awards.documents.dateModified: 
   modification date, required

:awards.documents.id: 
   document ID

:awards.suppliers.contactPoint.telephone: 
   contact person’s telephone

:awards.suppliers.contactPoint.name: 
   contact person’s first and last name

:awards.suppliers.contactPoint.email: 
   participant’s email

:awards.suppliers.identifier.scheme: 
   organization’s IATI identification scheme

:awards.suppliers.identifier.id: 
   organization’s code in the indicated scheme

:awards.suppliers.identifier.legalName: 
   participant’s full legal name

:awards.suppliers.name: 
   participant’s name

:awards.suppliers.address.postalCode: 
   postal code (of participant’s location)

:awards.suppliers.address.countryName: 
   country (of participant’s location)

:awards.suppliers.address.streetAddress: 
   street (of participant’s location)

:awards.suppliers.address.region: - region (of participant’s location)

:awards.suppliers.address.locality: 
   town/city

:awards.value.currency: 
   currency (MDL, EUR, USD)

:awards.value.amount: 
   offer price

:awards.value.valueAddedTaxIncluded: 
   without VAT

:awards.status: 
   active

:award.subcontractingDetails: 
   subcontractor details

:awards.id: 
   participant’s ID (CDB), required

:awards.date: 
   date when the information on the participant was entered (CDB), required

Once the EO is determined, no further actions are performed by the CA.

Concluding an agreement
-----------------------

Once the EO information is entered, CA can publish the concluded agreement. Conclusion of agreement, report on the introduced changes into the agreement, and execution of agreement is executed in the following manner:

#. EDS while change the agreement’s status to active and terminated, as well as changes to the status active, is obligatory.

#. Entering information on the agreement is optional. Upon affixation of EDS, CA can finish the procedure (complete).

#. Provided the changes introduced into the contract by the CA are insignificant, an upload of the modified contract is optional. 

Uploading the agreement, CA enters the following information (the fields automatically  filled out by the system are marked with*).

:Contracts.contractNumber: 
   agreement number

:Contracts.dateSigned: 
   agreement conclusion date

:Contracts.period.startDate: 
   agreement start date

:Contracts.period.endDate: 
   agreement end date

:Contracts.value.currency: 
   currency (by default, the same as value.currency), required

:Contracts.value.amount: 
   agreement value (awards.value.amount), required

:Contracts.value.valueAddedTaxIncluded: 
   without VAT (by default, the same as value.valueAddedTaxIncluded), required

:Contracts. status: 
   agreement status (once the agreement is uploaded - active), required

:Contracts.documents.format: 
   document format (agreement), required

:Contracts.documents.url:
   document URL, required

:Contracts.documents.title: 
   document title, required

:Contracts.documents.documentOf: 
   what does the document concern (tender), required

:Contracts.documents.documentType: 
   document type - signed (contractSigned), required

:Contracts.documents.datePublished: 
   publication date, required

:Contracts.documents.dateModified: 
   modification date, required

:Contracts.documents.id: 
   document ID, required

:Contracts.items.description: 
   procurement item name, required

:Contracts.items. classification.scheme: 
   CPV according to Common Procurement Vocabulary (CPV), required

:Contracts.items. classification.description: 
   CPV classification code which defines the procurement item, required

:Contracts.items.classification.id: 
   CPV code classification ID, required

:Contracts.items.deliveryAddress.postalCode: 
   postal code (delivery place), required

:Contracts.items.deliveryAddress.countryName: 
   country, required

:Contracts.items.deliveryAddress.streetAddress: 
   street, required

:Contracts.items.deliveryAddress.region: 
   region, required

:Contracts.items.deliveryAddress.locality: 
   residence place, required

:Contracts.items.id: 
   postal code, required

:Contracts.items.unit.code: 
   measurement unit code, required

:Contracts.items.unit.name: 
   measurement unit, required

:Contracts.items.quantity: 
   amount of goods / volume of work assignments, required

:Contracts.suppliers.contactPoint.telephone: 
   winner’s contact phone number, required

:Contracts.suppliers.contactPoint.name: 
   winner’s first and last name, required

:Contracts.suppliers.contactPoint.email: 
   winner’s e-mail, required

:Contracts.suppliers. identifier.scheme: 
   international identification scheme, required

:Contracts.suppliers.identifier.id:
   required

:Contracts.suppliers.identifier.legalName: 
   winner’s full legal name, required

:Contracts.suppliers.name: 
   winner’s name, required

:Contracts.suppliers.address.postalCode: 
   postal code (of winner’s location), required

:Contracts.suppliers.address.countryName: 
   country (of winner’s location), required

:Contracts.suppliers.address.streetAddress: 
   street (of winner’s location), required

:Contracts.suppliers.address.region: 
   region (of winner’s location), required

:Contracts.suppliers.address.locality: 
   place (of winner’s location), required

:Contracts.awardID: 
   qualification ID, required

:Contracts.id: 
   agreement ID, required

:Contracts.contractID: 
   agreement ID (MD-...), required

Procedure completion
--------------------

Once the agreement was uploaded and EDS added, the procedure automatically changes to ‘complete’ status.














