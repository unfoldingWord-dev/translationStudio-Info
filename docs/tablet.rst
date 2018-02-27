translationStudio for Android
=============================

The translationStudio for Android app is a mobile app for translators to do offline translating. 
It can be downloaded for Android devices: see https://play.google.com/store/apps/details?id=com.translationstudio.androidapp&hl=en. 
It contains the content that needs to be translated as well as translationHelps. You can share information directly from device to
device, and you can upload finished content to Door43 where it can be digitally published.




Installation
------------
1.	Tap the Google Play Store icon on the Android device. Google Play Store opens.
 
2.	In the search bar at the top of the screen, type translationStudio with no spaces and tap the magnifying glass on the keyboard.
 
3.	When the Play Store has found the program, tap the tS icon.
 
4.	Tap Install. The program downloads and then installs.
 
5.	Once the program is installed, tap Open.

6.	Tap ALLOW to enable translationStudio to access photos, media, and files on your device.
 
There may be an automatic update before the translationStudio app opens.



Login Options
-------------

When translationStudio first opens, you are presented with a request to create or log in to an account. 
There are two types of accounts that you can use:
1. Offline Account – user has full use of the program except for uploading to Door43. You may want to start with an offline account and then switch to a Door43 account later when you want to upload your work (the work is attached to the device, not to the account). If you want to use an offline account, skip to the Local Login or Offline Account section. 
2. Door43 Account – user has full use of the program and can upload to Door43 (requires Internet connection.)



Dictionary
----------

A standalone dictionary of terms. Currently all dictionary resources must use the markdown format.

The dictionary terms are used as the chapter slug and the translation of the term is placed inside a single 01.txt file:

.. code-block:: none

    content/
        |-config.yml
        |-aaron/
        |    |-01.txt
        |
        |-abel/
        ...
        |-unclean/

NOTE: lengthy dictionary terms may be split into more than one chunk.

The 01.txt file contains the translation of the term where the header is the title of the term and the rest is the description:

.. code-block:: none

    #Aaron

    God chose Aaron to be the first high priest for the people of Israel.

The config.yml is used to indicate related terms, aliases, and examples.

.. code-block:: yaml

    ---
      aaron: 
        see_also: 
          - "covenant"
          - "testimony"
        aliases:
          - aaronalias # note: not a real alias for this word
        examples:
          - "09-15"
          - "10-05"

Examples are tricky because a dict may be referenced by many different projects/resources. Therefore we cannot specify a resource link but instead must simply provide the chapter and chunk that contains the example.


Manual
------

A user manual. For now manual resources must use the markdown format.

Manuals are a collection of modules (articles):

.. code-block:: none

    content/
        ...
        |-translate-unknowns
        |    |-title.txt
        |    |-sub-title.txt
        |    |-01.txt
        ...
        |-writing-decisions/

The 01.txt file contains the translation of the module. The title.txt file contains the name of the module. And sub-title.txt contains the question that is answered by this module.

NOTE: if desired the module can be split into multiple chunks.
The config.yml indicates recommended and dependent modules:

.. code-block:: yaml

    ---
      translate-unknowns: 
        recommended: 
          - "translate-names"
          - "translate-transliterate"
        dependencies: 
          - "figs-sentences"

Dependencies are id's of modules that should be read before this one. Recommendations are modules that would likely benefit the reader next.
