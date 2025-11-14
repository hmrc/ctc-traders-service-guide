The Authorisation data group is a new addition to NCTS5. It allows the holder of the transit procedure to indicate which transit simplifications they wish to use for the movement that they have been previously authorised for.

Example authorisations include the following.

| Authorisation | Description                                                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------------------------------|
| ACR           | Authorisation for the status of authorised consignor for Union transit (Column 9b, Annex A of Delegated Regulation (EU) 2015/2446) |
| SSE           | Authorisation for the use of seals of a special type (Column 9d, Annex A of Delegated Regulation (EU) 2015/2446)                   |
| TRD           | Authorisation to use transit declaration with a reduced dataset (Column 9e, Annex A of Delegated Regulation (EU) 2015/2446)        |
| ACE           | Authorisation for the status of authorised consignee for Union transit (Column 9c, Annex A of Delegated Regulation (EU) 2015/2446) |

Authorisations can be used individually or combined as appropriate.

For a trader to use any transit simplification that it has been authorised to use, such as Authorised consignor for simplified procedure departure, the correct authorisation details must be present in the Authorisation data group and its usage is validated by NCTS.

Where the declarant wishes to use an Authorisation data block must be created with `Authorisation > Type` entry as follows.

| Authorisation type | Description                                                   |
|--------------------|---------------------------------------------------------------|
| C521               | Authorised consignor for simplified departure process (IE015) |
| C522               | Authorised consignee for simplified arrival process (IE007)   |
| C523               | Authorised to use seals                                       |
| C524               | Authorised to use reduced dataset                             |

The trader’s authorisation number must also be given in the data field `Authorisation > Reference Number`. This will be the reference number given to the trader when they first applied to use simplifications, an example of which may look like `AUTH123A`.

This should not be confused with the data field `Location of Goods > authorisation number` that indicates the exact location the movement will be departing from/arriving at when using the simplified procedure.