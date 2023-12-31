# Copper

1\. Overview

[Copper](https://www.copper.com/) is a **Customer Relationship Management (CRM)** software. Copper is a tool focused on automation and simplicity, most known for its Google Workspace integration.

**Example Use Case:** You have customer information currently sitting in the Copper CRM software. You want to sync this data into Cinchy through a batch sync in order to liberate your data from the silo.

{% hint style="success" %}
The Copper source supports batch syncs.
{% endhint %}

## 2. Info Tab

You can review the parameters that can be found in the info tab below _(Image 1)._

#### Values

| Parameter  | Description                                                                                                                                                | Example          |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- |
| Title      | **Mandatory.** Input a name for your data sync                                                                                                             | Copper to Cinchy |
| Version    | **Mandatory.** This is a pre-populated field containing a version number for your data sync. You can override it if you wish.                              | 1.0.0            |
| Parameters | **Optional.** Review our documentation on [Parameters here](../building-data-syncs/advanced-settings/parameters.md) for more information about this field. |                  |

<figure><img src="../../.gitbook/assets/image (294).png" alt=""><figcaption><p>Image 1: The Info Tab</p></figcaption></figure>

## 3. Source Tab

The following table outlines the mandatory and optional parameters you will find on the Source tab.

{% tabs %}
{% tab title="Source Details" %}
The following parameters will help to define your data sync source and how it functions.

<table><thead><tr><th>Parameter</th><th width="289.66666666666663">Description</th><th>Example</th></tr></thead><tbody><tr><td>Source</td><td><strong>Mandatory.</strong> Select your source from the drop down menu.</td><td>Copper</td></tr><tr><td>Entity</td><td><strong>Mandatory.</strong> The name of the entity you want to sync as it appears in your Copper CRM.</td><td>Companies</td></tr><tr><td>Access Token</td><td><strong>Mandatory.</strong> An encrypted version of your <a href="https://support.copper.com/hc/en-us/articles/360000520851-Generating-an-API-Key-">Copper API Key.</a> <strong>The Connections UI will automatically encrypt this value for you.</strong></td><td>"e98HGU72Lp0-fd34"</td></tr><tr><td>User Email</td><td><strong>Mandatory.</strong> The encrypted user email associated with the API key used above. <strong>The Connections UI will automatically encrypt this value for you.</strong></td><td>"e98HGU72Lp0-fd34hf990b4kLL23"</td></tr></tbody></table>
{% endtab %}

{% tab title="Schema" %}
**The** [**Schema**](../building-data-syncs/columns-and-mappings/#2.-schema-columns) **section** is where you define which source columns you want to sync in your connection. You can repeat the values for multiple columns.

| Parameter   | Description                                                                                                   | Example |
| ----------- | ------------------------------------------------------------------------------------------------------------- | ------- |
| Name        | **Mandatory.** The name of your column as it appears in the source.                                           | Name    |
| Alias       | **Optional.** You may choose to use an alias on your column so that it has a different name in the data sync. |         |
| Data Type   | **Mandatory.** The data type of the column values.                                                            | Text    |
| Description | **Optional.** You may choose to add a description to your column.                                             |         |



There are other options available for the Schema section if you click on **Show Advanced.**

| Parameter       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Example |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| Mandatory       | <ul><li><strong>If both Mandatory and Validated</strong> <strong>are checked</strong> on a column, then rows where the column is empty are rejected</li></ul><ul><li><strong>If just Mandatory is checked</strong> on a column, then all rows are synced with the execution log status of failed, and the source error of <strong>"Mandatory Rule Violation"</strong></li></ul><ul><li><strong>If just Validated is checked</strong> on a column, then all rows are synced.</li></ul> |         |
| Validate Data   | <ul><li><strong>If both Mandatory and Validated</strong> <strong>are checked</strong> on a column, then rows where the column is empty are rejected</li></ul><ul><li><strong>If just Validated is checked</strong> on a column, then all rows are synced.</li></ul>                                                                                                                                                                                                                   |         |
| Trim Whitespace | **Optional if data type = text.**  If your data type was chosen as "text", you can choose whether to **trim the whitespac**e _(that is, spaces and other non-printing characters)._                                                                                                                                                                                                                                                                                                   |         |
| Max Length      | **Optional if data type = text.** You can input a numerical value in this field that represents the maximum length of the data that can be synced in your column. If the value is exceeded, the row will be rejected (you can find this error in the Execution Log).                                                                                                                                                                                                                  |         |

You can choose to add in a **Transformation > String Replacement** by inputting the following:

| Parameter   | Description                                                                                                                           | Example |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| Pattern     | **Mandatory if using a Transformation.** The pattern for your string replacement, i.e. the string that will be searched and replaced. |         |
| Replacement | What you want to replace your pattern with.                                                                                           |         |

{% hint style="info" %}
Note that you can have more than one String Replacement
{% endhint %}
{% endtab %}

{% tab title="Filter" %}
You have the option to add a source filter to your data sync. Please review the documentation here for more information on [source filters.](../building-data-syncs/advanced-settings/filters.md)
{% endtab %}
{% endtabs %}

## 4. Next Steps

* Configure your [Destination](../supported-data-sync-destinations/)
* Define your[ Sync Behaviour](../building-data-syncs/sync-behaviour.md).
* Add in your [Post Sync Scripts](../building-data-syncs/advanced-settings/post-sync-scripts.md), if required.
* Define your [Permissions](../building-data-syncs/#2.-create-a-data-sync-configuration).
* Click **Jobs > Start a Job** to begin your sync.
