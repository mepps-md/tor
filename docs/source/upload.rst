.. _upload:

Uploading Documents
===================

All of the document uploading API endpoints follow the same set of rules.

Upload document with registration
---------------------------------

#. `Register document upload in document service <documentservice:register-document-upload>`_.

#. Add document in API:

    .. include:: tutorial/upload-tender-notice.http
        :code:

#. `Upload document in document service <documentservice:upload-document>`_.

Upload document w/o registration
--------------------------------

#. `Register document upload in document service <documentservice:upload-document-w-o-registration>`_.

#. Add document in API:

    .. include:: tutorial/upload-tender-notice.http
        :code:

    
