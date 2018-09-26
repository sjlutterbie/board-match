# boardMatch

## Overview

boardMatch is a platform that connect service-oriented individuals with
non-profits in their local communities who are in need of board-level support.

## Motivation

Many communities enjoy vibrant non-profit and service-oriented communities.
However, these communities are often held back by a two-fold problem:

* Service-oriented individuals are unaware of the range of non-profits in their
    community, and often have not considered board-level involvement as a means
    of giving back and making a difference.
* Non-profits are limited by their current members' existing social and
    professional networks. They struggle to broaden their base of support by
    connecting with new individuals who are passionate about their cause.

boardMatch is a community-level platform on which individuals can create a
profile that summarizes their professional and service experience, and in which
ways they would most like to give back to their community. Non-profits can also
create profiles summarizing their organization, and highlighting open positions
on their boards. Individuals and non-profits can then reach out to each other,
building new connections and working together to strengthen their communities.

## User Stories (work in progress)

* [ ] When a user arrives at the `Homepage`:
  * [ ] They quickly understand the site's purpose.
  * [ ] They have clear options to log in as an individual, or on behalf of a
          non-profit.
* [ ] When a user logs in (either as an individual or non-profit):
  * [ ] Their user credentials are stored to authenticate their session
  * [ ] They arrive at the relevant `Dashboard page`
* [ ] When an **individual** arrives at the `Individual dashboard page`:
  * [ ] The user **can see** the following things:
    * [ ] If they have **NOT** created a `Individual profile`:
      * TODO
    * [ ] If they **HAVE** created a `Individual profile`:
      * TODO
  * [ ] The user **can do** the following things:  
    * [ ] If they have **NOT** created a `Individual profile`:
      * TODO
    * [ ] If they **HAVE** created a `Individual profile`:
      * TODO
* [ ] When a **non-profit** arrives at their `Organization dashboard page`:
  * [ ] The non-profit **can see** the following things:
    * [ ] If they have **NOT** created a `Organization profile`:
      * TODO
    * [ ] If they **HAVE** created a `Organization profile`:
      * TODO
  * [ ] The user **can do** the following things:  
    * [ ] If they have **NOT** created a `Organization profile`:
      * TODO
    * [ ] If they **HAVE** created a `Organization profile`:
      * TODO

## Element definitions

* The `Homepage`:
  * TODO
* The `Dashboard page`:
  * Is:
    * The primary user interface for a logged-in user
        (either individual or non-profit)
  * Contains:
    * Three primary content areas:
      * The `header bar`:
        * Is:
          * A horizontal bar across the top of the screen
        * Contains:
          * The site title/logo
          * The `Utilities menu`
      * The `sideBar menu`:
        * Is:
          * A responsive menu (reduceds to collapse/expand icon on small screens)
          * On large screens:
            * A column on the left side of the viewport
        * Contains:
          * The following list of actions a user can take to interact with the app:
            * Individual actions:
              * TODO
            * Organization actions:
              * TODO
* The `Utilities menu`:
  * Is:
    * A responsive menu (reduces to collapse/expand icon on small screens)
  * Contains:
    * A link to `Account settings` (updates `Main content area`)
    * A link to `Contact support` (mailto href)
    * A link to `Sign out` (system action)
* An `Individual profile`:
  * Is:
    * A JSON object
    * Stored as a document in the app's MongoDB
  * Contains:
    * Identity:
      * First name
      * Last name
      * Title
    * Contact information:
      * Email address(es):
        * For each:
          * Primary address? (boolean)
          * Email address
          * Email type (work, personal)
      * Phone number(s):
        * For each: 
          * Primary number? (boolean)
          * Phone number
          * Phone type (Work, mobile, home)
    * Summary statement
      * TODO
    * Professional experience
      * TODO
    * Community service experience
      * TODO
    * Matching characteristics:
      * TODO
* An `Organization profile`:
  * Is:
    * A JSON object
    * Stores as a document in the app's MongoDB
  * Contains:
    * Identity:
      * Organization name
      * Organization type
        * 501(c)3, unincorporated, etc.
    * Contact information:
      * Website
      * Mailing address
      * Phone number
      * Email address
      * Primary contact:
        * First name
        * Last name
        * Title
    * Summary statement
      * TODO
    * Primary activities
      * TODO
    * Matching characteristics:
      * TODO