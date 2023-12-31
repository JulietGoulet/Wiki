# DB2 Table

## 1. Overview

[DB2](https://www.ibm.com/products/db2) (Formerly _Db2_ for LUW) is a relational database that delivers advanced data management and analytics capabilities for transactional workloads.&#x20;

Prior to setting up your data sync destination, [ensure that you've configured your Source.](../supported-data-sync-sources/)

{% hint style="success" %}
The DB2 Table destination supports batch and real-time syncs.
{% endhint %}

## 2. Destination Tab

The following table outlines the mandatory and optional parameters you will find on the Destination tab _(Image 1)._

{% tabs %}
{% tab title="Destination Details" %}
The following parameters will help to define your data sync destination and how it functions.

<table><thead><tr><th>Parameter</th><th width="289.66666666666663">Description</th><th>Example</th></tr></thead><tbody><tr><td>Destination</td><td><strong>Mandatory.</strong> Select your destination from the drop down menu.</td><td>DB2 Table</td></tr><tr><td>Connection String</td><td><strong>Mandatory.</strong>  The encrypted Connection String used to connect to your DB2 database. <strong>The Connections UI will automatically encrypt this value for you.</strong></td><td>You can find an example <a href="https://www.connectionstrings.com/ibm-db2/">Connection String here.</a></td></tr><tr><td>Table</td><td><strong>Mandatory.</strong> The name of the DB2 table that you want to sync your data to, including the schema</td><td>dbo.employees</td></tr><tr><td>ID Column</td><td>The name of the identity column that exists in the destination (or a single column that is guaranteed to be unique and automatically populated for every new record) </td><td></td></tr><tr><td>ID Column Data Type</td><td>The data type of the above ID Column. </td><td></td></tr></tbody></table>
{% endtab %}

{% tab title="Column Mapping" %}
**The** [**Column Mapping**](../building-data-syncs/columns-and-mappings/#3.-column-mappings) **section** is where you define which source columns you want to sync to which destination columns. You can repeat the values for multiple columns.

| Parameter     | Description                                                              | Example |
| ------------- | ------------------------------------------------------------------------ | ------- |
| Source Column | **Mandatory.** The name of your column as it appears in the source.      | Name    |
| Target Column | **Mandatory.** The name of your column as it appears in the destination. | Name    |
{% endtab %}

{% tab title="Filter" %}
You have the option to add a destination filter to your data sync. Please review the documentation here for more information on [destination filters.](../building-data-syncs/advanced-settings/filters.md#target-filters)
{% endtab %}
{% endtabs %}

<figure><img src="../../.gitbook/assets/image (138).png" alt=""><figcaption><p>Image 2: Define your Destination</p></figcaption></figure>

## 4. Next Steps

* Define your[ Sync Behaviour](../building-data-syncs/sync-behaviour.md).
* Add in your [Post Sync Scripts](../building-data-syncs/advanced-settings/post-sync-scripts.md), if required.
* Define your [Permissions](../building-data-syncs/#2.-create-a-data-sync-configuration).
* If you are running a real-time sync, [set up your Listener Config](../supported-real-time-sync-stream-sources/) and enable it to begin your sync.
* If you are running a batch sync, click **Jobs > Start a Job** to begin your sync.
