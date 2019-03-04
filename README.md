master & servant webapp thingy
first feature should be creating a "session" and "joining" it
\- the session being essentially a WebSocket connection.

to-be-master sends a request to start a session, stating e-mail addresses to invite as slaves.

The server creates a session, with the initiator being the "master". Invitation emails include links to join as slaves.

Stuff to do:
1) web page for session creation
2) REST API that it calls
3) email sending for the invites and
4) web page for displaying a session
5) a skeletal WS connection handling joining the session and informing the master of joinees.
there should be an API for joining, of course.

Each "session" or "room" or whatever would have a unique identifier assigned to it, so that the web part can support multiple concurrent sessions.
Back-end could at first just hold everything in-memory, since sessions won't survive reboots or crashes anyway.
And there wouldn't be much to hold: basically a data structure storing the sessions, and the users and their roles.

Angular on the front and Java+Vert.x in the back?
Optional Vue or React and Kotlin+Vert.x
