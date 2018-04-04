# Final Project Proposal

Evan Cernea's and Xiao Wu's Project Proposal

## Problem / Question

We are working on a project for the City of Minneapolis to predict what parcels
may have lead remaining in the house. We want to create a application that is
multi-purposes.

First, we want the application to contextualize why it is important to have your
house inspected for lead. Lead exposure in young children can lead to behavioral
and developmental problems later in life. To show the prevalence of lead, we
will map the elevated blood lead Levels in young children in the state of
Minnesota's counties and the census tracts of Minneapolis proper. This "story"
is intended to demonstrate that lead is not a problem that disappeared after the
EPA declared it illegal to use in housing substances, and demonstrate the
necessity of our predictive model.

Second, we want residents to understand their risk of lead exposure. Users
will enter their address, the age of their house, the last sale price, and the
exterior of the home in a dialogue box. This will let the users calculate a
risk score of their house having lead.

Third, we want to help people get services they need. We will route people with
risk scores above a 50 percent chance of lead exposure to a store where they
could purchase a lead testing kit, and route them to a blood work site where
they could be tested for lead.


## The data

- Elevated Blood Lead Levels GeoJSON (counties and census tract)
- Shapefile of positive lead presence in Minneapolis
  - This is necessary for the model. It will not be visible to the user, but
    it will be used internally to calculate the distance to the nearest three
    lead sites, which is necessary for the model calculation
- The model we have built in R to calculate lead probability
- List of blood testing locations in Minneapolis
  - Must be geocoded
- List of hardware stores that sell lead inspection kits in Minneapolis
  - Must be geocoded

## Technologies used

We plan on using basic GeoJSON mapping to map the elevated blood levels. We
will need to extend Leaflet to make it more interactive.

We are not yet sure how we can create a calculator using JavaScript tools yet.
It should just be a simple calculation where users are able to alter certain
coefficients of the model to generate a score.

We will use the mapbox API to calculate driving routes in Minneapolis from
user-entered addresses to stores to buy a lead test and places to get blood
work done.

Review the APIs/online examples of leaflet, turf, jQuery, underscore (or
any library not explicitly covered in class) for functions/uses which
you'd like to explore. Briefly describe how you might use them.

## Design spec

#### User experience

At a high level, we expect that people will use the application to give
users an ability to figure out if they should be worried about lead presence
in their homes. We assume most of the users will be parents of young children
figuring out if their children need to get tested. This application will help
parents understand the dangers of lead poisoning in their area, and then help
them determine their risk. If they are at risk, the application will help them
determine if there is something to actually worry about and the steps they may
take to remedy the lead in their houses.

#### Layouts and visual design


The application will most likely use the sidebar feature that we have used
in our previous models. The side will explain
So far, we've built all our applications with a side bar for
representing non-map content and navigation. This is not the only
successful design. Extra content could be displayed in a top bar,
through modals, through side bars on both sides, and any combination of
these as well as a number not mentioned. Try to describe your
application's visual layout. Conceptually (no need for extensive CSS
here), what will this design require?

## Anticipated difficulties

Thinking about weaknesses can be useful. What do you anticipate being
most difficult about this project? How will you attempt to cope with
these difficulties? For example, asynchronous behavior (ajax, events)
are hard to use and think about. Global variables are a strategy for
coping with that difficulty by breaking data out of the asynchronous
context.

## Missing pieces

We've only managed to scratch the surface of the available technologies
by which you could construct an application. What use-cases haven't we covered
that you think would be useful? What technologies not covered seem exciting to
you (you don't necessarily have to fully understand what they're for,
this is a chance for you to get our help interpreting a technology's
purpose/usage).
