### General
Had to modify the code a bit to make it work properly. CORS was breaking, also really didn't like the naming of `.env.frontend` since that meant bringing in more tooling to support odd naming of ENV files. I just did a simple `mv` on it.

One thing I noticed that was odd was the backend URL variable for the frontend used a sub path on it. Normally I'd think it would make sense to use the base domain and handle the routes inside of the app itself rather than expecting a sub path.

