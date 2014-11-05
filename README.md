Formatting phone number 
=======================

Abstract
--------

As its name suggests, this module simply allows you to format a phone number to appear in Odoo 8.0. 

This is a version of "bss_phonenumbers" module available here lp: bss-phonenumbers-addons / 7.0

NOTE:: 
    To used this module, you have to install python-phonenumbers 
    links: 
        - https://github.com/daviddrysdale/python-phonenumbers
        - https://pypi.python.org/pypi/phonenumbers

Description
-----------

Well formed standard phone numbers field
Add an ORM field type "phonenumber" which ensures that all phone numbers will be stored in E.164 format (like "+41327200890") and displayed in international format (like "+41 32 720 08 90") with a RFC 3966 Tel URI (like "tel:+41-32-720-08-90"). Many formats are recognized when the field is edited. After validation, the ORM field will transform the entered value in E.164 format before storing it. If you type a phone number without country code, the country set for your user in OpenERP will be used.

The RFC 3966 Tel URI can be opened by your desktop phone application to easily dial the number directly from an OpenERP partner form view. With E.164 format for phone numbers in database, you can imagine server-side features with OpenERP phone numbers and a phone server.

For phone number format transformation, the module uses python-phonenumbers from David Drysdale (Apache License 2.0) which have to be installed separately on your OpenERP server. python-phonenumbers is a Python port of the Java libphonenumber library by Google.

See bss_partner_phone_numbers and bss_crm_phone_numbers for usage.

Links

    E.164 format on Wikipedia : http://en.wikipedia.org/wiki/E.164
    RFC 3966 Tel URI : http://www.ietf.org/rfc/rfc3966.txt
    python-phonenumbers : https://github.com/daviddrysdale/python-phonenumbers
    libphonenumber : https://code.google.com/p/libphonenumber
    bss_partner_phone_numbers and bss_crm_phone_numbers sources : https://launchpad.net/bss-phonenumbers-addons
