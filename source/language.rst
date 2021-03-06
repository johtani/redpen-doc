Language Settings
==================

RedPen processes documents written in any language, such as German, French or Japanese.
RedPen default configuration will process documents written in English or other Latin-based languages.
Therefore, to make RedPen process documents written in other languages, users need to specify
that language in the RedPen configuration file.

Override Language
----------------------

Currently there are two language settings, "en" and "ja". "en" is for documents written in Latin-based languages such as English and German.
"ja" is for Japanese documents.

In order to override the language, you must change the "lang" property of the "symbols" section of the configuration file.
In the following example, the config file specifies Japanese ("ja") as the document language.

.. code-block:: xml

    <symbols lang="ja">
        <symbol name="EXCLAMATION_MARK" value="!" invalid-chars="！" after-space="true" />
        <symbol name="LEFT_QUOTATION_MARK" value="\'"  invalid-chars="“" before-space="true" />
        <symbol name="RIGHT_QUOTATION_MARK" value="\'"  invalid-chars="”" after-space="true" />
        <symbol name="NUMBER_SIGN" value="#" invalid-chars="＃" after-space="true" />
        <symbol name="FULL_STOP" value="。" invalid-chars="．." after-space="true" />
        <symbol name="COMMA" value="、" invalid-chars="," after-space="true" />
    </symbols>

Override Symbol Settings
-----------------------------

Depending on the documents and their authors, the characters and symbols used may differ.
For example, one author might use "'" for a left single quotation mark, whereas another
author might use "‘" for a left single quotation mark.

For such cases, RedPen provides the way to override the default symbols (
see :ref:`setting-characters-section` section) used in the document,
and in addition, specify which symbols should not used in the input documents.

The following overrides the setting for single quotation marks to enforce the use of the ascii quotation mark "'".

.. code-block:: xml

  <symbols>
    <symbol name="LEFT_SINGLE_QUOTATION_MARK" value="'"  invalid-chars="‘" />
    <symbol name="RIGHT_SINGLE_QUOTATION_MARK" value="'" invalid-chars="’"/>
  </symbols>

