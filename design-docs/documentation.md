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

* [ ] When a user arrives at the `Landing Page`:
  * [ ] They quickly understand the site's purpose.
  * [ ] They have clear options to log in as an individual, or on behalf of a
          non-profit.
* [ ] When a user logs in (either as an individual or non-profit):
  * [ ] Their user credentials are stored to authenticate their session
  * [ ] They arrive at the relevant `Dashboard page`
* [ ] When an **individual** arrives at the `Individual dashboard page`:
  * [ ] The user **can see** the following things in the `Main content area`:
    * TODO
  * [ ] The user **can do** the following things:  
    * TODO
* [ ] When a **non-profit** arrives at their `Organization dashboard page`:
  * [ ] The non-profit **can see** the following things in the `Main content area`:
    * TODO
  * [ ] The user **can do** the following things in the `Main content area`:  
    * TODO

## MVC Model

### Views

#### Pages

* The `Landing page`:
  * Is:
    * The first page a logged-out user sees when visiting the app
    * The static page initially served at '/'
  * Contains:
    * The `Site header [logged out]`
    * The `App overview`
    * The `Login / Create account form`
  * Layout:
    * The `Site header`, `App overview`, and `Login / Create account form`
        are stacked in a single column.
* The `Dashboard page`:
  * Is:
    * The primary user interface for a logged-in user
    * The static page served at '/dashboard' __(or '/', dynamically?)__
  * Contains:
    * The `Site header [logged-in]`
    * The `Application menu`
    * The `Main content area`
  * Layout:
    * Small and Medium:
      * The `Site header`, `Application menu`, and `Main content area`
          are stacked in a single column.
    * Large:
      * The `Site header` is full-width across the top of the screen
      * The `Application menu` is a narrow left-hand column
      * The `Main content area` is the right-hand content area

#### Components

* The `Site header`:
  * Is:
    * A mixed-use content area
  * Contains:
    * The `Site title`
    * `[logged in]`
      * The `Utilities menu`
  * Layout:
    * `[logged-out]`
      * The `Site title` is center-aligned
      * The `Utilities menu` is hidden
    * `[logged-in]`
      * The `Site title` is left-aligned
      * Small and Medium displays:
        * The `Utilities menu` is collapsed to a right-aligned 'cog icon'
      * Large displays:
        * The `Utilities menu` is expanded, and right-aligned
* The `Utilities menu`:
  * Is:
    * A menu
  * Contains:
    * A link to `Account settings` (View component)
    * A link to `Contact support` (mailto href)
    * A link to `Sign out` (controller)
  * Layout:
    * Small and medium displays:
      * A dropdown menu from a collapsed 'cog icon'
    * Large displays:
      * A single row of right-aligned text links

////////////// STOPPING POINT ///////////////////

* The `Application menu`:
  * Is:
    * A responsive menu (reduceds to collapse/expand icon on small screens)
    * On large screens:
      * A column on the left side of the viewport
  * Contains:
    * The following list of actions a user can take to interact with the app:
      * Individual actions:
        * View/edit profile
        * Browse/search non-profits
        * Browse/search board openings
      * Organization actions:
        * View/edit profile
        * Manage openings
        * Browse/search individuals
* The `Main content area`:
  * Is:
    * The bulk of the viewport, minus the `Header bar` and `Application menu`.
  * Contains:
    * The user's selected data view and data manipulation UI elements
* The `Account settings` view:

### Models

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

### Controllers




## Scratchpad: Misc. thoughts & notes

When a user arrives at their dashboard, they should see summaries of each of
the key components of the site, and clear CTAs for the primary actions they
can take in each section.

* Key sections:
  * Individuals
  * Organizations
  * Openings

For each of the key sections, individuals can see:
* Short version of their profile
  * And an "edit profile" button
* Featured organizations (5?)
  * And a "browse organizations" button
* Featured open positions (5?)
*   And a "Browse openings" button