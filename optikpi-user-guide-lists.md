# Optikpi User Guide : Lists

* [Retention](optikpi-user-guide-lists.md#Lists-Retention)
  * [Customer](optikpi-user-guide-lists.md#Lists-Customer)
  * [Event](optikpi-user-guide-lists.md#Lists-Event)
* [Acquisition](optikpi-user-guide-lists.md#Lists-Acquisition)
* [API](optikpi-user-guide-lists.md#Lists-API)
  * [Create](optikpi-user-guide-lists.md#Lists-Create)
  * [Update](optikpi-user-guide-lists.md#Lists-Update)
  * [Delete](optikpi-user-guide-lists.md#Lists-Delete)
* [CSV](optikpi-user-guide-lists.md#Lists-CSV)
  * [Create](https://app.gitbook.com/@puru/s/optikpi-user-guide/\~/drafts/-MYubqWgT-SbgBLgFFF9/optikpi-user-guide-lists#Lists-Create.1)
  * [Update](optikpi-user-guide-lists.md#Lists-Update.1)
  * [Delete](optikpi-user-guide-lists.md#Lists-Delete.1)
  * [Data Types](optikpi-user-guide-lists.md#Lists-DataTypes)
  * [Add to Rule ](optikpi-user-guide-lists.md#Lists-AddtoRule)

## Retention <a href="#lists-retention" id="lists-retention"></a>

Use Retention List for keeping or containing data of existing customers. You can push data into the list using a unique User ID.

### Customer <a href="#lists-customer" id="lists-customer"></a>

Lists are storage units to track customer profiles and events.

{% hint style="info" %}
Customer List is a place where you can track the profiles of your customers. The Customer List holds the user profile data like Email, Phone, etc.
{% endhint %}

### Event

Lists are storage units to track customer profiles and events.

{% hint style="info" %}
Event List is a place where you can track customers' events. Like “Login", "Transaction", "Clicks" etc. Event List is a list that tracks relevant user events. There can be more than one event list.
{% endhint %}

## Acquisition <a href="#lists-acquisition" id="lists-acquisition"></a>

Use Acquisition List for proceeding data for customers which are not yet in the System.

## API <a href="#lists-api" id="lists-api"></a>

### Create <a href="#lists-create" id="lists-create"></a>

Here you will know how to create an API List.

I. Start creating a List by pressing the "New Customer List" button From the "Lists" home screen.

![](<.gitbook/assets/285310979 (1).jpg>)

2\. Provide List name, List source (API List), List Mode (Active), and List Description.

![](<.gitbook/assets/image (23) (1).png>)

3\. Choose a file that contains data.

![](<.gitbook/assets/image (46) (1).png>)

4\. Set Schema Definition.

![](<.gitbook/assets/image (43).png>)

5\. Clicking on the field **Add to rule engine** you can switch on/off of adding this data to your List.

![](<.gitbook/assets/image (51).png>)

6\. Switching on the field **“Is metric field”** you can point this data like a metric.

![](<.gitbook/assets/image (11).png>)

7\. Switching on the field “ **Add to Table”** you can add/remove data to/from your List.

![](<.gitbook/assets/image (21).png>)

8\. Switching on the field **“Anonymize”** you can change the visibility of data in the list, as well in the cards and segments.

![](<.gitbook/assets/image (55).png>)

9\. Clicking on the field **X** you can delete data from the list.

![](<.gitbook/assets/image (6) (1).png>)

10\. Map the following details from the List fields.

| **Name**           | **Description**                                                                                 |
| ------------------ | ----------------------------------------------------------------------------------------------- |
| `Unique Id`        | Unique Identifier of each record in the list                                                    |
| `User/Customer Id` | Unique Identifier of each Customer. Please note, this should be the same column in all the list |
| `Email`            | Field which stores the customer email, used for Email Communication                             |
| `Phone Contact`    | Field which stores the customer phone number value, used in SMS Communication                   |
| `Push Tokens`      | Field which stores device-specific push tokens as a string array                                |

11\. Click the button “**Create API List”** and your list will be created.

![](.gitbook/assets/271515799.png)

12\. At any time you can peek into your list content from the List details page.

![](<.gitbook/assets/285311089 (1).jpg>)

13\. Start pushing data into the list using standard Http Post call.

For Example.

```
 curl --location --request POST 'https://customer.optikpi.com/lists/User' 
    --header 'Content-Type: application/json' 
    --data-raw '{
        "PK_USER_ID":"xxxxx",
        "EMAIL":"xxx@email.com",
        "PHONE":"345666699"
    }'
```



### Update <a href="#lists-update" id="lists-update"></a>

I. You can change any List by clicking on the “pen” icon.

![](.gitbook/assets/288981017.jpg)

2\. Or you can change any List by clicking the "Edit List" on the Up Panel inside the List.

![](.gitbook/assets/288325679.jpg)

3\. While Updating List you can update List Description, set new Schema Definition, delete or add a new column.

![](.gitbook/assets/289046547.jpg)

4\. Clicking the "Update API List" you will see your List updating.

![](.gitbook/assets/285573339.jpg)



### Delete <a href="#lists-delete" id="lists-delete"></a>

**Be careful!**

**List can be deleted only by the administrator.**\
**At this moment it is impossible to identify if the list is used in another Optikpi tool: cards, segments or actions.**

**If you delete a list that is using in another Optikpi tool you can break Cards or Segments or stop a Campaign.**

I. You can delete any List by clicking on the “Trash” icon.

![](<.gitbook/assets/288096266 (1).jpg>)

2\. System will ask you “Do you really want to delete the List?”

![](.gitbook/assets/288096279.jpg)

{% hint style="danger" %}
When you confirm and press the “Delete” button the List will be deleted permanently, without the possibility of recovery.
{% endhint %}

## CSV <a href="#lists-csv" id="lists-csv"></a>

### Create <a href="#lists-create.1" id="lists-create.1"></a>

Here you will know how to create a CSV List.

**This tutorial video will help you to Upload an Acquisition List**

[https://youtu.be/Nsao5qHG0C0](https://youtu.be/Nsao5qHG0C0)

I. Start creating a List by pressing the "**Create Customer List**" button from the "Lists" home screen.

![](<.gitbook/assets/image (64).png>)

2\. Provide **General Information**:

step 1 - List name

step 2 - List Source (CSV File)

step 3 - List Mode (should be Active)

step 4 - List Description (if necessary)

![](<.gitbook/assets/image (71).png>)

**Please Note:**

Draft mode is the default mode for opening a draft List for viewing and editing. All commands are available. **But List in a draft mode is not available for Card/Segment creation**. You can set a draft List to active mode using the Edit by choosing Active Mode in the List Mode field.

3\. In the "**Schema Definition**" tab select the CSV file and download it.

![](<.gitbook/assets/image (59).png>)



3.1 If it's necessary you can set set Schema Definition.

![](.gitbook/assets/lu\_6jpg.jpg)

3.2. Clicking on the field **Add to rule engine** you can switch on/off of adding this data to your List.

![](.gitbook/assets/lu\_8.jpg)

3.3. Switching on the field **“Is metric field”** you can point this data like a metric.

![](.gitbook/assets/lu\_7.jpg.jpg)

3.4. Switching on the field “**Add to Table”** you can add/remove data to/from your List.

![](.gitbook/assets/lu\_9.jpg)

3.5. Switching on the field **“Anonymize”** you can change the visibility of data in the list, as well in the cards and segments.

![](.gitbook/assets/lu\_10.jpg)

3.6. Clicking on the field **X** you can delete data from the list.

![](.gitbook/assets/lu\_11.jpg)

&#x20;3.7.  You can add a new column by providing Field Name, Header, Data Type and set other scheme definitions. Press the "Add" button in final.

![](.gitbook/assets/lu\_12.jpg)

4\.  Press the "Next" button to go to the next step.

![](<.gitbook/assets/image (60).png>)

5\. **Field Mapping**.  Map the following details from the List fields.

Choose relevant data for each field. If respective data is not available in your list select None.

| **Name**        | **Description**                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------ |
| `Unique Id`     | Unique Identifier of each record in the list                                                     |
| `User/customer` | Unique Identifier of each Customer. Please note, this should be the same column in all the lists |
| `Email`         | Field which stores the customer email, used for Email Communication                              |
| `Phone Contact` | Field which stores the customer phone number value, used in SMS Communication                    |
| `Push Tokens`   | Field which stores device-specific push tokens as a string array                                 |

![](<.gitbook/assets/image (65).png>)

6\. Press the button “**Create CSV List”** and your list will be created.

![](<.gitbook/assets/image (67).png>)

![](<.gitbook/assets/image (66).png>)

### Update <a href="#lists-update.1" id="lists-update.1"></a>

You can add Add CSV Data at your existing Acquisition List

I. From the Acquisition upper menu part go to the List where you want to add data and click the "Add CSV Data" button.

![](<.gitbook/assets/286163104 (1).jpg>)

2\. Select and Upload CSV file which has to have the same structure as an initial one.

![](.gitbook/assets/286163115.jpg)

3\. You will see new data lines in the List.

### Delete <a href="#lists-delete.1" id="lists-delete.1"></a>

Be careful!

List can be deleted only by the administrator.\
At this moment it is impossible to identify if the list is used in another Optikpi tool: cards, segments or actions.

If you delete a list that is using in another Optikpi tool you can break Cards or Segments or stop a Campaign.

I. You can delete any List by clicking on the “Trash” icon.

![](<.gitbook/assets/288096266 (1).jpg>)

2\. System will ask you “Do you really want to delete the List?”

![](.gitbook/assets/288096279.jpg)

{% hint style="danger" %}
When you confirm and press the “Delete” button the List will be deleted permanently, without the possibility of recovery.
{% endhint %}

### Data Types <a href="#lists-datatypes" id="lists-datatypes"></a>

**String Data Type**

A string data type is a sequence of characters, either as a literal constant or as some kind of variable. The latter may allow its elements to be mutated and the length changed, or it may be fixed (after creation). A string is generally considered a data type and is often implemented as an array data structure of bytes (or words) that stores a sequence of elements, typically characters, using some character encoding.

**Boolean Data Type**

A Boolean data type has one of two possible values (usually denoted true and false), intended to represent the two truth values of logic and Boolean algebra. The Boolean data type is primarily associated with conditional statements, which allow different actions by changing control flow depending on whether a programmer-specified Boolean condition evaluates to true or false.

**Date Data Type**

The Date data type stores the calendar date.

**Float Data Type**

A floating-point data type uses a formulaic representation of real numbers as an approximation so as to support a trade-off between range and precision. For this reason, floating-point computation is often found in systems which include very small and very large real numbers, which require fast processing times. A number is, in general, represented approximately to a fixed number of significant digits and scaled using an exponent in some fixed base

**Integer Data Type**

An integer data type represents some range of mathematical integers. Integral data types may be of different sizes and may or may not be allowed to contain negative values. Integers are commonly represented in a computer as a group of binary digits (bits).

**Long Data Type**

The long data type is a 64-bit two’s complement integer.

### Add to Rule  <a href="#lists-addtorule" id="lists-addtorule"></a>

Clicking on the field **Add to rule engine** you can switch on/off of adding this data to your List.

![](.gitbook/assets/271941645.jpg)

You can add a column by providing data manually.

Provide Field Name, Header, choose the type of Data and press the “Add” button.

![](.gitbook/assets/285573355.jpg)
