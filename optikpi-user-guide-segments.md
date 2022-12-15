# Optikpi User Guide : Segments

* [Rule Engine](optikpi-user-guide-segments.md#rule-engine)
* [Create](optikpi-user-guide-segments.md#segments-create)
* [Download](optikpi-user-guide-segments.md#segments-download)
* [Add action to Segment](optikpi-user-guide-segments.md#segments-addactiontosegment)
* [Edit](optikpi-user-guide-segments.md#segments-edit)
* [Clone](optikpi-user-guide-segments.md#segments-clone)
* [Delete](optikpi-user-guide-segments.md#segments-delete)
* [Inactivate Segment](optikpi-user-guide-segments.md#inactivate-segment)

Segments represent unique players of given Lists based on different criterias. Segments can be bounded to several Retention Lists.

Use segments to create higher level customer buckets.

## Rule Engine

### Include Filter > Rule

which identifies the root rule to which the filter is applied.

Rules for the criteria of a string data (User ID, USERNAME, EMAIL ID) can be presented in the next values:

* equal (you should specify the value, or copy paste it)
* not equal (you should specify the value, or copy paste it)
* Exists (Fields with existing data)
* Not Exists (Fields where there is no data)
* Empty (empty Fields)
* Not Empty (not empty Fields)&#x20;
* one of (you can select multiple values from the dropdown)
* not one of (you can select multiple values from the dropdown)

### Include Filter > +Add Rule

Operators OR/AND are used between different rules in your Segment to help you build more sophisticated segments.

In Include filter

AND: if you want the (outcome) users to satisfy all the conditions specified in the Include block ( multiple rules)

OR : if you want the (outcome) users to satisfy any one of the rules specified in the include block&#x20;

AND feature combines two or more conditions and produces results that satisfy both.

Example for AND: Status of deposit success AND the sum of deposit more than 10 Euros. The result will strictly contain players who made a successful deposit of more than 10 Euros.

OR feature combines two or more conditions and produces results that satisfy either one or the other.

Example for OR: Status of deposit success OR the sum of deposit more than 10 Euros. The result will contain data of all players who have a successful deposit and also data of players whose deposit exceeds 10 Euros.

AND Filters are usually used in most cases with Include filter.

## Exclude Filter > Rule

if the out-coming users of the exclude block has to satisfy each and every rule defined inside exclude block, then AND should be used,

if the out-coming users of the exclude block has to satisfy any one of the rules (users satisfying any one of the rules individually), OR should be used.

Out-coming users - these are the users we want to exclude from the segment.

For example,

You can use OR Filter for boosting responsible gaming - you can Exclude all the users whose account is either frozen OR inactive OR closed.  In this case out-coming users satisfying any one of the rules individually, so they will not be presented in the Segment.

You can use AND Filter if you want to exclude those users who satisfy all pointed criterias, it means that among out-coming users will be only whose account is frozen AND inactive AND closed. Users whose account is only frozen, but not inactive will be presented in the Segment, as well as users whose account is only inactive, but not frozen.

## Create <a href="#segments-create" id="segments-create"></a>

Go to the main Segments screen to start working with Segments.

I. Start creating a Segment pressing the "Create Segment" button From the "Segments" home screen panel .

![](.gitbook/assets/271941781.jpg)

2\. Provide a meaningful name for your Segment.

![](<.gitbook/assets/image (105).png>)

3\. Add criteria for your Segment at the “Filters” section.

![](.gitbook/assets/demo1\_27.jpg)

4\. By clicking on the “Add rule” button you can add more criteria.

![](<.gitbook/assets/image (108).png>)

5\. By clicking ![](<.gitbook/assets/image (106).png>) you can add more criteria based on the same List.

![](<.gitbook/assets/image (110).png>)

6\. After settings all rules, press the "Execute" button.

![](<.gitbook/assets/image (109).png>)

7\. Customers matching those selection criteria will be displayed in the table below.

![](<.gitbook/assets/image (104).png>)

8\. Save your newly created Segment.

![](<.gitbook/assets/image (111).png>)

9\. You will see the new Segment from the "Segments" home screen.

![](<.gitbook/assets/image (94).png>)



## Download <a href="#segments-download" id="segments-download"></a>

Optikpi gives the opportunity to download data in CSV format from your Segment.

I. By Clicking on 3 dots on Segment panel, a popup with comes up.

![](.gitbook/assets/271384687.jpg)

2\. Click **Table View** to see which data contains your Segment.

![](.gitbook/assets/271384693.jpg)

3\. Set your own Column Setting by choosing Available Fields.

![](.gitbook/assets/271384699.jpg)

4\. You can download data in CSV format.

![](.gitbook/assets/271384705.jpg)

5\. You can sort data in ascending or descending order.

![](.gitbook/assets/271384711.jpg)

## Add action to Segment <a href="#segments-addactiontosegment" id="segments-addactiontosegment"></a>

By Clicking on 3 dots on the Segment panel, a popup with comes up. **Add Action** links you to the Confirmation panel where you can select the type of action and the channel for the action.

![](.gitbook/assets/271286420.jpg)

![](.gitbook/assets/271286426.jpg)

## Edit <a href="#segments-edit" id="segments-edit"></a>

By Clicking on 3 dots on Segment panel, a popup with comes up. **Edit** allows changing Segment Information, criteria of the Segment.

![](.gitbook/assets/271286434.jpg)

## Clone <a href="#segments-clone" id="segments-clone"></a>

By Clicking on 3 dots on the Segment panel, a popup with comes up. **Clone** allows creating an identical Segment.

![](.gitbook/assets/271286442.jpg)

## Delete <a href="#segments-delete" id="segments-delete"></a>

By Clicking on 3 dots on the Segment panel, a popup with comes up. **Delete** allows delete Segment.

![](.gitbook/assets/271220812.jpg)

## Inactivate Segment

**Any newly created Segment is active by default.**&#x20;

There is a feature to **deactivate Segments**.&#x20;

_**Deactivated Segments are not available in the Dashboards.**_&#x20;

_**Deactivated Segments are not available for Actions creation.**_

**How to deactivate Segments.**

1. Getting start with the Segment main screen.

Check if your page is in the Card View Mode.

![](<.gitbook/assets/image (9) (2).png>)

2\. The activation toggle switcher is located in the in the lower right corner of the segment card.

![](<.gitbook/assets/image (63).png>)

3\. For state changing of the Segment click on the Toggle once.

<figure><img src=".gitbook/assets/2022-10-07 1.gif" alt=""><figcaption></figcaption></figure>

_**Deactivated Segments are not available in the Dashboards.**_&#x20;

_**Deactivated Segments are not available for Actions creation.**_&#x20;

_**Deactivated Segments are not availible for editing and updating.**_

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

_****_

~~``~~
