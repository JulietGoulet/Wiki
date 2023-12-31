---
description: >-
  This page outlines Step 6 of Deploying CinchyDXD: Reinstalling the Data
  Experience
---

# Reinstalling the Data Experience (CinchyDXD)

## Table of Contents

| Table of Contents                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------- |
| [#1.-re-run-cinchydxd-install](reinstalling-the-data-experience-cinchydxd.md#1.-re-run-cinchydxd-install "mention") |
| [#2.-validate-install](reinstalling-the-data-experience-cinchydxd.md#2.-validate-install "mention")                 |

## 1. Re-Run CinchyDXD Install&#x20;

Using Powershell, you must now install the Data Experience you have exported out of Cinchy.

1. Open File Explorer and navigate to your exported folder _(Image 1)._

![Image 1: Step 1](<../../../.gitbook/assets/image (290).png>)

2\. In the **folder path URL** for the exported data experience type in **powershell** to launch Powershell for that path.

3\. Hit **Enter** on your keyboard _(Image 2)._

![Image 2: Step 3](<../../../.gitbook/assets/image (277).png>)

4\. In the Powershell window, type **cin** and hit **Tab** on your keyboard. Type **install** _(Image 3)._

![Image 3: Step 4](<../../../.gitbook/assets/image (640).png>)

5\. Enter the install parameters into the Powershell window:

{% hint style="info" %}
The parameters executed in Powershell can exist on one line in powershell, however for legibility (below) the parameters have been put on separate lines. If you are putting your parameters on separate lines you will be required to have backticks quote \`  for the parameters to execute
{% endhint %}

Sample _(Image 4):_\
&#x20;`.\CinchyDXD.ps1 install` \
`` -s "<taget Cinchy url>" ` ``\
`` -u "<target user id>" ` ``\
`` -p "<target password>" ` ``\
`` -c "C:\Cinchy CLI v4.0.2" ` ``\
`` -d "C:\CLI Output Logs" ` ``

![Image 4: Step 5](<../../../.gitbook/assets/image (536).png>)

6\. Hit **Enter** on your keyboard to run the install command. Once the Data Experience has been installed you will get a message in Powershell that the install was completed _(Image 5)._

![Image 5: Step 6](<../../../.gitbook/assets/image (639).png>)

## 2. Validate Install

1. Ensure that the **Models Table** is populated in the target environment with the model that was installed _(Image 6)._

![Image 6: Step 1](<../../../.gitbook/assets/image (399).png>)

2\. Ensure that the **Currency Exchange Rate** table exists in the target environment with the new column names _(Image 7)._

![Image 7: Step 2](<../../../.gitbook/assets/image (86).png>)

3\. Ensure that the **Currency Converter** query exists in the target environment with the new column names and labels _(Image 8)._

![Image 8: Step 3](<../../../.gitbook/assets/image (183).png>)

4\. Ensure that the **Data Experience Definitions** table has not changed, unless you have added or removed column details within this table _(Image 9)._

![Image 9: Step 4](<../../../.gitbook/assets/image (275).png>)

5\. Ensure that the **Data Experience Releases** table in the target environment is populated with the new release version number from the install (e.g. 2.0.0) _(Image 10)._

![Image 10: Step 5](<../../../.gitbook/assets/image (503).png>)
