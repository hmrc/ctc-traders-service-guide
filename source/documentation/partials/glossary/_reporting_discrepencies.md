Discrepancies between what has arrived and what was declared (and released for transit after any amendments) **must** be reported in the IE044 message. To provide discrepancies information, set the data element ‘UNLOADING REMARK.Conform‘ to ‘0‘ to indicate that there are unloading remarks (see rule [G0205](/guides/ctc-traders-phase5-tis/documentation/rules-g.html#g0205)).

When providing details about the discrepancies, you must provide consignment information only for those data groups where there has been a change from the initially released declaration (see rule [G0360](/guides/ctc-traders-phase5-tis/documentation/rules-g.html#g0360)).

**Note:** When reporting a discrepancy, you must provide the same level of consignment detail as you provided in the IE015 (‘Declaration Data‘) message for the transit movement.

The IE044 message should identify the affected data group when reporting new ‘actual’ consignment details by matching its sequence number; or for consignment items, the ‘goods item number‘, and ‘declaration goods item number‘.

If data or goods items are missing entirely, the sequence number or goods item number and declaration goods item number should be matched as appropriate, but omit any additional data elements.

If consignment information in excess of what was initially declared (and released) is identified during unloading, the sequence number (or ‘goods item number‘ and ‘declaration goods item number‘) should equate to the highest sequence number or declaration goods item number/goods item number **+1** for each new data group instance.

For example, if 10 items were initially declared, and an 11th item is identified upon unloading, the consignment item ‘goods item number’ and ‘declaration goods item number’ should equate to the highest existing numbers for the consignment +1. (In this example and during the transition period where multiple house consignments are not used, this would be 11.)

For more information about proper completion of IE044 consignment data groups when discrepancies have been identified, see rules [R0054](/guides/ctc-traders-phase5-tis/documentation/rules-r.html#r0054) and [R0055](/guides/ctc-traders-phase5-tis/documentation/rules-r.html#r0055).