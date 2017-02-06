.. index:: Bid, Parameter, LotValue, bidder, participant, pretendent

.. _bid:

Bid
===

Schema
------

:tenderers:
    List of :ref:`Organization` objects

:date:
    string, :ref:`Date`, auto-generated

:id:
    uid, auto-generated

:status:
    string

    Possible values are:

    * `draft`
    * `active`

:value:
    :ref:`Value`, required

    Validation rules:

    * `amount` should be less than `Tender.value.amout`
    * `currency` should either be absent or match `Tender.value.currency`
    * `valueAddedTaxIncluded` should either be absent or match `Tender.value.valueAddedTaxIncluded`

:documents:
    List of :ref:`Document` objects

:parameters:
    List of :ref:`Parameter` objects

:participationUrl:
    url

    A web address for participation in auction.

.. _Parameter:

Parameter
=========

Schema
------

:code:
    string, required

    Code of the feature.

:value:
    float, required

    Value of the feature.

.. _LotValue:

LotValue
========

Schema
------

:value:
    :ref:`Value`, required

    Validation rules:

    * `amount` should be less than `Lot.value.amout`
    * `currency` should either be absent or match `Lot.value.currency`

:date:
    string, :ref:`Date`, auto-generated

:participationUrl:
    url

    A web address for participation in auction.
    
