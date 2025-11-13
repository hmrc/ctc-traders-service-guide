The transition period is the period of time during which countries may switch to operating NCTS5 at any point and will run until all countries have switched to operating NCTS5. NCTS operations are currently considered to be in the transition period.

**Note:** For information about the end date of the transition period, see [NCTS phase 5 technical interface specification](/guides/ctc-traders-phase5-tis/#ncts5-key-dates).

During the transition period, those countries that are operating NCTS5 must do so in transitional mode, which is equivalent to a 'backwards compatibility' mode. This is to ensure that messages can be exchanged between NCTS4 and NCTS5 countries, which is handled by an upgrade/downgrade convertor in the common domain, where messages are exchanged at country to country level. For example, notifying the country of destination that the movement has been released or notifying the country of departure that the movement has arrived, and so on.

The UK’s NCTS5 service will go live during the transition period.

To ensure backwards compatibility with NCTS4 during transition, special rules and conditions have been defined to restrict/prevent usage of new data fields and some functionality until all countries are operating NCTS5. This allows downgrading of NCTS5 messages to NCTS4.

The prefixes of these rules and conditions are as follows.

| Rule prefix | Description                                                       |
|-------------|-------------------------------------------------------------------|
| B           | Restrictive business rules effective during transitional period.  |
| E           | Restrictive technical rules effective during transitional period. |

During the transition period, NCTS will observe and apply these business ([Rules B](/guides/ctc-traders-phase5-tis/documentation/rules-b.html)) and technical ([Rules E](/guides/ctc-traders-phase5-tis/documentation/rules-e.html)) rules as defined in the [NCTS Phase 5 technical interface specification](/guides/ctc-traders-phase5-tis/).