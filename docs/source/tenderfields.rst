.. _tenderfields:

Tender fields and data validation
=================================

.. hint::

         It is best advised that the majority of information is retrieved automatically from the respective profile and not filled out manually.

Procuring entity creates a tender on the Platform and fills out the following fields, which are transferred to the CDB:

:title: 
   procurement title

:procurementMethod: 
   procedure kind = Open

:procurementMethodType: 
   procedure type  = belowThreshold

:description: 
   procurement procedure

:procuringEntity.name: 
   shortened entity name (for example - Ministry of Finance)

:procuringEntity.identifier.legalName:
   full entity name (for example - Ministry of Finance of Republic of Moldova), required

:procuringEntity.identifier.scheme: 
   MD-IDNO (according to :ref:`rst_codebooks`)

:procuringEntity.identifier.id: 
   IDNO (according to :ref:`rst_codebooks`)

:procuringEntity.contactPoint.name: 
   first and last name of the person responsible for the procurement procedure

:procuringEntity.contactPoint.telephone: 
   cell phone of the person responsible for the procurement procedure

:procuringEntity.contactPoint.email: 
   email address of the person responsible for the procurement procedure

:procuringEntity.contactPoint.url: 
   website address of the procuring entity

:procuringEntity.address.countryName: 
   **Moldova** (for procuring entities that are residents only) 

:procuringEntity.address.postalCode: 
   postal code

:procuringEntity.address.region: 
   region according to :ref:`rst_codebooks`

:procuringEntity.address.locality: 
   town/city

:procuringEntity.address.streetAddress: 
   address: street number 

:documents.format: 
   "text/plain" text format

:documents.title: 
   document title

:documents.documentOf: 
   indication of what does the document concern - procuring procedure 

:value.amount: 
   procurement’s expected price

:value.amount: 
   MDL, EUR, USD

:value.valueAddedTaxIncluded:
   false (without VAT)

:items:

:items.description: 
   procurement’s nomenclature description

:items.classification.scheme:
   CPV name according to :ref:`rst_codebooks`

:items.classification.id: 
   CPV code which describes the procurement item

:items.classification.description: 
   classification code title in Romanian

:items.unit.code: 
   measurement unit code  (has to go in line with the  UN/CEFACT standard, for example - KGM)
   according to :ref:`rst_codebooks`

:items.unit.name: 
   measurement unit name in Romanian according to :ref:`rst_codebooks`

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

:enquiryPeriod.endDate: 
   date until which clarification period is valid

:tenderPeriod.startDate: 
   offer submission beginning period date

:tenderPeriod.endDate: 
   offer submission end period date

:minimalStep.amount: -minimum amount of price reduction (sum and  % from the expected price, with automatic recalculation)

Checks that are performed on the CDB level:

:title: 
   filled out

:procurementMethod: 
   filled out

:procurementMethodType: 
   filled out

:description: 
   filled out

:procuringEntity.name: 
   filled out

:procuringEntity.identifier.legalName: 
   filled out

:procuringEntity.identifier.scheme:  
   filled out with one of the codes from the IATI list

:procuringEntity.identifier.id:
   filled out

:procuringEntity.contactPoint.name: 
   filled out

:procuringEntity.contactPoint.telephone: 
   filled out if no email is indicated

:procuringEntity.contactPoint.email: 
   filled out if no telephone is indicated. The following `validation rules <https://github.com/schematics/schematics/blob/development/schematics/types/net.py>`_ are applied additionally.

:procuringEntity.contactPoint.url: 
   filled out if no telephone is indicated. The following `validation rules <https://github.com/schematics/schematics/blob/development/schematics/types/net.py>`_ are applied additionally.

:procuringEntity.address.countryName: 
   filled out

:procuringEntity.address.postalCode: 
   filled out

:procuringEntity.address.region: 
   filled out

:procuringEntity.address.locality: 
   filled out

:procuringEntity.address.streetAddress: 
   filled out

:documents.format: 
   filled out if documents can be uploaded

:documents.title: 
   filled out if documents can be uploaded

:documents.documentOf: 
   filled out if documents can be uploaded

:value.amount: 
   filled out

:value.currency: 
   filled out

:value.valueAddedTaxIncluded: 
   filled out

:items: 
   filled out

:items.description: 
   filled out

:items.classification.scheme: 
   filled out according to :ref:`rst_codebooks`

:items.classification.id: 
   filled out according to :ref:`rst_codebooks`

:classification.description: 
   filled out according to :ref:`rst_codebooks`

:items.unit.code: 
   filled out according to :ref:`rst_codebooks`

:items.unit.name: 
   filled out according to :ref:`rst_codebooks` 

:items.quantity: 
   filled out with numeric value

:items.deliveryDate.startDate: 
   if filled out, data has to be field type

:items.deliveryDate.endDate: 
   if deliveryDate:startDate field is filled out, then this field type has to be a date further than deliveryDate:startDate

:enquiryPeriod.endDate: 
   filled out, date is further than enquiryPeriod:startDate

:tenderPeriod.startDate: 
   filled out, date is further than enquiryPeriod:endDate

:tenderPeriod.endDate: 
   filled out, date is further than tenderPeriod:startDate

:minimalStep.amount: 
   filled out, numeric value

Having received and validated the document, the CDB automatically fills out the following fields:

:id: 
   ID (For example - 64fb59935cd5402691b1d1c43765a6ba)

:tenderID: 
   procurement ID (for example - MD-2017-01-14-000160-a)

:dateModified: 
   change date (publication)

:status: 
   procurement status = **active.enquiries**

:documents.url: 
   link to the document (generated while it’s being uploaded)

:documents.datePublished: 
   document publication date

:documents.dateModified: 
   document change date

:documents.id: 
   ID given to the document by the CDB

























