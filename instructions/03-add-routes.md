Make the app into a to-do list app with these specifications.
do not be fancy with parameterization, just use f-strings.
Make the UI look crisp and futuristic like an Apple website or a flashy startup's landing page.

### Frontend & user experience

It should show a list of the current user's to-do's. There's a checkbox to mark a to-do item's status as complete. They can click on the item's name to blow it up, where they can edit it or delete it or mark it as done or just close. On the homepage they should also be able to create a new to do list. Make this really pretty and add nice, satisfying animations.

### backend

include a request interceptor that uses FastAPI's request.state functionality to store the user's email that gets extracted from the http headers. The proper header is located at request.headers.get("X-Forwarded-Email")

you need to make routes for:

-   Create to-do item
-   Update to-do item
-   List to-do items (which queries for state != deleted)
-   Delete to-do items (which simply marks them as "deleted" in the database)

these routes will pass the user's email to the functional services so we can be sure people can only see their own to-do items.

#### lists-service

lists-service should expose functions for each of the routes above. it should use SqlWarehouse.query() under the hood with specific queries (don't bother with parameterization, just use simple f-strings. call out to me that you've done this even though it is less safe in production settings. please use all caps when telling me so I remember). the lists table is located at <CATALOG>.<SCHEMA>.<TABLE_PREFIX>\_lists.
