---
uid: Best_Practices_When_Creating_Catalog_Items
keywords: catalog, description, solution, tag, metadata, kata, publish, upload, topic
---

# Best practices when creating Catalog items

On this page, you will find recommendations for creating Catalog items. These will ensure that when you publish a Catalog item, users can easily find it, and they can clearly understand what it is meant for.

> [!TIP]
> To find out how you can publish Catalog items, follow the tutorial [Registering a new version of a user-defined API to the Catalog using Visual Studio and GitHub](xref:CICD_Tutorial_For_Other_Items_User_Defined_API_VisualStudio_And_GitHub).

## Optimize the visibility of your Catalog item

You can optimize the visibility of your Catalog item by making sure the [**Manifest file**](xref:Register_Catalog_Item#manifest-file) is correctly defined:

- Ensure the **name** is clear to the user, so they will know what the solution is meant to be used for. Avoid using technical terms.

- Assign the correct **type** to your Catalog item. Generally, avoid using "Custom Solution" for public Catalog items. For more information about the different types, see [About Catalog items](xref:About_the_Catalog_app#about-catalog-items).

- Add **tags** to help users find your Catalog item. The main goal of tags is to expose the Catalog item to relevant searches. Follow these rules of thumb for the tags:

  - Do not use the name of your Catalog item as a tag.
  - Do not use the type of your Catalog item as a tag.
  - Tags should be user-centric or market-centric.
  - Do not use general DataMiner terms (e.g. "dataminer").
  - Avoid uncommon abbreviations.
  - Use at most 5 tags for one Catalog item.
  - Avoid using plurals when not necessary (e.g. use "Source" instead of "Sources").
  - Use [title case](xref:Title_case).
  - Use at most three words per tag.

- Assign an **icon** to your Catalog item to catch the user's attention. You can do this by defining a vendor for your Catalog item with the `vendor_id` field in the [Manifest file](xref:Register_Catalog_Item#manifest-file). If you need assistance with this, please reach out to your technical contact.

## Optimize the accessibility of your Catalog item

- Help users understand what your Catalog item is, what it does, and what it looks like, by **adding documentation**. This will be shown in the item's description. For details, refer to [Best practices when documenting Catalog items](xref:Best_Practices_When_Documenting_Catalog_Items).

- When you release a version of a Catalog item, make sure to **adhere to [semantic versioning (A.B.C)](xref:About_the_Catalog_app#versioning-of-catalog-items)**.

  Using a postfix (such as -CU1) is only necessary in exceptional circumstances (e.g. if you released a version that you immediately unlisted because of a severe bug. You should not delete such a version, but unlist it. Once a fix has been made, it is appropriate to use CU to clarify the situation to users).

  For the version description, clearly state what has changed, and if there are bug fixes or new features. Use the following phrases as appropriate: "Change:", "Fix:", "New Feature:". Each phrase can be used multiple times.

- Use the appropriate **state for the range** (*Active*, *Main*, custom tag, or *Deprecated*):

  - As a rule of thumb, there should be **only one Main range**, and as **few *Active* ranges as possible**.
  - When a range is *Active*, this indicates that the range is still being maintained and bug fixes should always be added to these ranges.
  - The *Main* range indicates the latest and most recommended range to install.
  - Custom tags on a range should only be used in exceptional cases, where two ranges might be considered but each has its specifics.

## Follow the naming conventions

See [Naming conventions for Catalog item components](xref:Naming_Conventions_For_Catalog_Item_Components).
