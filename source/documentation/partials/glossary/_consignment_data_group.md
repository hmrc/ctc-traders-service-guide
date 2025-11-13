The restructuring of the IE015 declaration in NCTS5 provides for greater flexibility of consignor, consignee, and goods related documentation on a hierarchical basis.

The NCTS5 transit declaration introduces the ability to specify either single or multiple consignor information to associated single or multiple consignees.

The basic consignment hierarchy is as follows:

1. Consignment
2. Consignment > House consignment
3. Consignment > House consignment > Consignment item

### Consignment
Consignment level provides for master, overarching information about a  movement. For example, if there is only one consignor and/or one consignee, it would be declared at this level. Also, any documentation (previous, supporting, transport, and so on) that applies to the movement as a whole may be declared at this level.

### House consignment
At least one house consignment level data block must be provided, such as for a single consignor. If a transit movement contains goods from more than one consignor, multiple house consignment data blocks must be used. The same consignor can be used in more than one house consignment block, but at least one of the house consignment blocks must have a different consignor.

Additionally, if there is more than one consignee, house consignment blocks can be used on a per consignee basis to specify individual consignee details only once at this level to cover all the goods in the house consignment block. For example, this would apply if a single consignor is moving goods to multiple consignees. The same consignee can be used in more than one house consignment block, but at least one of the house consignment blocks must have a different consignee.

The benefit of this over current NCTS4 operation is the need to provide the consignee details only once for multiple goods instead of repeating the same data for every goods item entered.

If more than one house consignment block is used, the consignor and/or consignee details at this level must be different to those in at least one other block. In other words, you cannot use two or more house consignment blocks if there is only a single consignor and consignee for the movement, irrespective of whether there are more than 999 items (the limit per house consignment).

The maximum number of house consignments per declaration is 1999.

### Consignment item

Consignment Item level is where details of all the goods being moved must be declared insofar as they relate to the consignor and/or consignee declared at the higher consignment or house consignment levels.

Goods must be declared on a line-by-line basis, each with an individual item number, description, packaging details, weight, and commodity code (which is mandatory post-transition) details. Consignee details can be entered per goods item at this level only during the transition period.

Previous document, supporting document, and other supporting documentation can all be declared in the same hierarchal fashion explained above at either consignment, house consignment, or consignment item level depending on the coverage of the documents in relation to the goods items.

### Example usage

| Goods being moved on behalf of                | Declare consignor(s) at consignment level | Declare consignor(s) at house consignment level | Declare consignee(s) at consignment level | Declare consignee(s) at house consignment level | Maximum total goods items per MRN |
|-----------------------------------------------|-------------------------------------------|-------------------------------------------------|-------------------------------------------|-------------------------------------------------|-----------------------------------|
| Co. A to Co. B                                | X                                         |                                                 | X                                         |                                                 | 999                               |
| Co. A to (Co. B, Co. C, and so on)            | X                                         |                                                 |                                           | X                                               | 1,999*                            |
| (Co. A + Co. B, and so on) to Co. C           |                                           | X                                               | X                                         |                                                 | 1,999*                            |
| Co. A to Co. B and; Co. C to Co. D, and so on |                                           | X                                               |                                           | X                                               | 1,999*                            |