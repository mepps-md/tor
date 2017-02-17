.. _procurementplans:

Procurement plans
=================

A brief overview
----------------

Upon the approval of budget / business plan of an organization, this structured data is entered into the system. The record on the planned procedure in the annual procurement plan is elaborated until the third CPV digit. Gradually, this data is further elaborated by the CA by introducing changes into the annual plan where the procurement item details are indicated.

Plan creation
~~~~~~~~~~~~~

:procuringEntity.identifier.scheme:
   identification scheme according to the 
   `IATI standard <http://iatistandard.org/201/upgrades/decimal-upgrade-to-2-02/>`_
   (`Codelist in JSON format <http://standards.openprocurement.org/codelists/organization-identifier-scheme/en.json>`_)

:procuringEntity.identifier.id:
   CA code in the chosen identification scheme

:procuringEntity.name*:
   CA name

:procuringEntity.identifier.legalName:
   CA full name

:budget.year:
    year

:budget.project.id:
    project code 

    .. important:: 
   
       Should be hidden in the platform’s interface

:budget.project.name:
    project name

    .. important::
   
       Should be hidden in the platform’s interface

:budget.id: 
    procurement plan number

:budget.description:  
    procurement item name

:budget.source of financing.id: 
    source of finance 

:budget.source of financing.name: 
    source of finance title 

:budget.notes: 
    remarks

:budget.amount: 
    expected procurement price with VAT

    .. important::
   
       Should be hidden in the platform’s interface

:budget.currency: 
    currency according to :ref:`rst_codebooks`

:budget.amountNet: 
    expected price without VAT

:tender.tenderPeriod.startDate: 
    approximate beginning date of the procurement procedure (there should be an opportunity to choose a month (e.g. March, 2016))

:tender.procurementMethodType: 
    procedure type

:classification.scheme: 
    CPV according to :ref:`rst_codebooks`

:classification.id: 
    CPV classification code which defines the procurement item 

:classification.description: 
    CPV classification code name

:id: 
    procurement plan identificator, required

:planID: 
    procurement plan identificator, required
    
Data entered by CA introducing procurement plan details
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:items.description: 
    procurement item name, required

:items.quantity: 
    amount of goods/the volume of work assignments or services provision, required

:item.unit.code: 
    measurement unit code according to :ref:`rst_codebooks`, required

:items.unit.name: 
    measurement unit name according to :ref:`rst_codebooks`, required

:items.deliveryDate.endDate: 
    end time of goods delivery / work assignments execution / services provision, required

:items.classification.scheme: 
    CPV according to :ref:`rst_codebooks`, required

:items.classification.id: 
    CPV classification code which defines the procurement item, required
    
:items.classification.description: 
    CPV classification code name, required
    
Validations executed on the CDB level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:procuringEntity.identifier.scheme: 
    filled out with one of the codes from the IATI list

:procuringEntity.identifier.id: 
    filled out

:procuringEntity.name: 
    filled out

:procuringEntity.identifier.legalName: 
    filled out

:budget.description: 
    filled out

:budget.amount: 
    filled out

:tender.tenderPeriod.startDate: 
    planned date of procedure start

:tender.procurementMethod: 
    filled out

:classification.scheme: 
    filled out according to :ref:`rst_codebooks`

:classification.id: 
    filled out according to :ref:`rst_codebooks`

:classification.description: 
    filled out according to :ref:`rst_codebooks`

:items.description: 
    filled out if there is at least one item

:items.quantity: 
    filled out if there is at least one item

:items.unit.code: 
    filled out according to  :ref:`rst_codebooks` if there is at least one item

:items.unit.name:  
    filled out according to :ref:`rst_codebooks` if there is at least one item

:items.deliveryDate.endDate: 
    filled out if there is at least one item

:items.classification.scheme: 
    filled out according to :ref:`rst_codebooks` if there is at least one item

:items.classification.id: 
    filled out according to :ref:`rst_codebooks` if there is at least one item

:items.classification.description: 
    filled out according to :ref:`rst_codebooks` if there is at least one item

Introducing changes into the plan
---------------------------------

CA can add new or modify earlier entered articles of the plan, increase or decrease the existing articles, and introduce other changes into the plan.

To delete an article of the plan, CA enters zero value into the Amount and Expected procurement value fields.









