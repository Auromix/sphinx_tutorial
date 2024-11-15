

Links
======
In Sphinx documentation, reStructuredText (reST) provides several ways to insert links. These links can be external, internal, or to images. Below are examples of common usage for each type.

External Links
--------------
To insert an external link, use the following syntax:

See the `Auromix <https://github.com/Auromix>`_ for more details.


.. code-block:: rst

    See the `Auromix <https://github.com/Auromix>`_ for more details.

This will create a clickable link to the specified URL with the text "Auromix."

Explanation:

- The link text (`Auromix`) is enclosed in backticks, followed by the target URL inside angle brackets (`< >`).

- The underscore (`_`) at the end of the link marks it as an external link.


Internal Links
--------------
Sphinx allows you to create internal links within your documentation. Internal links are useful for referencing other sections of the same document or linking across multiple pages. 

Link to Sections Within the Same Document
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Linking to Sections Within the Same Document
You can link to specific sections of the current document by using the section's header with a `#` symbol.

Example:

See the `External Links <#external-links>`_ for more details.


.. code-block:: rst

    See the `External Links <#external-links>`_ for more details.

This will create a link to the "External Links" section within the same document. 

Explanation:

- The link text (`External Links`) is followed by `<#external-links>`, which references the target section with an anchor that matches the section title, converted to lowercase and spaces replaced by hyphens.

Link to Cross-Document or Cross-Page Sections
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
To reference a section from another document, you need to define a label in the target document and use the `:ref:` directive to link to it.

Example:

In the target document (e.g., `index.rst`), add a label to the section you want to link to:

.. code-block:: rst

    .. _table-of-contents:

    Table of Contents
    =========================

Then, in any other document, you can link to this section using the `:ref:` directive:

See the :ref:`table-of-contents` for more details.


.. code-block:: rst

    See the :ref:`table-of-contents` for more details.

Explanation:

- The label `.. _table-of-contents:` is defined at the target location (e.g., the "Table of Contents" section).

- The `:ref:` directive is used to link to that label from another part of the documentation.

Image Links
-----------
Images can also be linked in a similar way to external links. You can specify an image file and also link the image to a URL. To create an image link, use the `.. image::` directive with the `:target:` option.

Example:

..  image:: ../_static/auromix_name.webp
    :align: center
    :target: https://github.com/Auromix
    
.. code-block:: rst

    ..  image:: ../_static/auromix_name.webp
        :align: center
        :target: https://github.com/Auromix

Explanation:

- The `.. image::` directive is used to insert the image. The `:alt:` option provides an optional description of the image for accessibility purposes.

- The `:target:` option specifies the URL to which the image will link when clicked.

