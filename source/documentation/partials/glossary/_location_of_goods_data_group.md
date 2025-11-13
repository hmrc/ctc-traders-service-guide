The Location of Goods data group is used to declare the type and geographical position of the location from which a transit movement is intended to depart. The location types available are the same in NCTS4 and NCTS5, but NCTS5 uses a different naming convention and method for identifying a location type being used.

Location designations have been revised for NCTS5 as follows.

| NCTS4 designation        | NCTSS5 designation  | NCTS5 identifier |
|--------------------------|---------------------|------------------|
| Customs sub place        | Designated location | `A`              |
| Authorised location code | Authorised place    | `B`              |
| Agreed location          | Approved place      | `C`              |

You must provide the location of goods before the release of a transit movement, either in an IE015 message for a standard departure or in an IE170 message for a pre-lodged departure. You must specify both the type of location (using a single alphabetic character as shown in the table), and the qualifier of that location. The location qualifier is the means you will use to provide the exact locations, such as  address, UN Locode, and so on.

Only certain qualifiers can be used with specific location types. The following table shows the acceptable location type and qualifier combinations (indicated by square brackets []) permitted for NCTS5.


| Location qualifier            | Location type code A | Location type code B | Location type code C | Location type code D |
|-------------------------------|----------------------|----------------------|----------------------|----------------------|
| T (Postal code)               | A + T	               | B + T	               | [C + T]              | [D + T]              |
| U (UN/Locode)                 | [A + U]              | B + U	               | [C + U]              | [D + U]              |
| V (Customs office identifier) | [A + V]              | B + V	               | C + V	               | D + V                |
| W (GNSS coordinates)          | A + W	               | B + W	               | [C + W]              | [D + W]              |
| X (EORI number)               | A + X	               | B + X	               | [C + X]              | D + X                |
| Y (Authorisation number)      | A + Y	               | [B + Y]	             | C + Y	               | D + Y                |
| Z (Address)                   | A + Z	               | B + Z	               | [C + Z]              | D + Z                |


Although these are all combinations that NCTS5 supports, see the Location of Goods data group in [Declaration data](#declaration-data) for acceptable practical usage in the UK.

You must provide the actual information relating to the chosen qualifier in the appropriate data subgroup within the Location of Goods data group.

The Location Qualifier > Authorisation Number (`Y`) is correlated with the NCTS4 Authorised Location Code.

A simplified departure procedure declared in NCTS5 must contain the following:

- Authorisation data group: the appropriate Reference number under which the Authorised Consignor status is held, which is an umbrella reference number under which all authorised location codes are contained
- Location of Goods data group: Location Type Code `B` (authorised place), Location Qualifier `Y` (authorisation number), and the Authorisation Number (NCTS4 authorised location code) in the appropriate data subgroup from which the movement will be started.

If the combination `B` +`Y` is used, NCTS validates all authorisation data provided.