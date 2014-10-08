#### Example

Open both the Forum View and the User's Profile View in a Tabbed Activity:

    AppSteroidActivity.startTabbedActivity(
        getApplicationContext(), 
        new ShowTabsCollection(
            TabGroup.FORUM, 
            TabGroup.PROFILE));


