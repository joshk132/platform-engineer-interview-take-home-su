### General
Had to modify the code a bit to make it work properly. CORS was breaking, also really didn't like the naming of `.env.frontend` since that meant bringing in more tooling to support odd naming of ENV files. I just did a simple `mv` on it.

One thing I noticed that was odd was the backend URL variable for the frontend used a sub path on it. Normally I'd think it would make sense to use the base domain and handle the routes inside of the app itself rather than expecting a sub path.

### GHA improvements
If I was making this application for something long standing with updates I would have rules/filters on the changes to scope what gets built and when. I would also include the test suites and linting as different jobs. I didn't see that in the requirements so I left it out as it was well beyond the scope of it and would have added another 10-15 minutes to verify everything was working properly.

### DX
I am not a fan of that you have to know a docker command to make this work so I would add a script in `/scripts` to run docker compose and then a note in the README on it. Would allow for a cleaner run and to "hide" some magic to make it so that a platform team can update the underlying part of it without developers needing to change a command incase they decide to alais it. 