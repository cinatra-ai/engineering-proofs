# Google appointment schedules — cinatra pull request 3173

Six full-window pictures of the connector's setup page in both themes, taken on the running application at the head of the pull request against the live Google connection. They show the behaviour of the two acceptance items: a schedule added with a live calendar pick and listed, then deleted; and the list clean after the assistant added and removed schedules through its own tool. Pictures that show the booking page's link are kept out of this set. The drawn-surface misses on this page are filed as follow-up issues named in the pull request.

## The schedule listed after the add, light theme

![](https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-listed-cleared-light.png?raw=true)

https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-listed-cleared-light.png?raw=true

One schedule added through the app's own form with the calendar picked from the live list; the row lists as its own card with the title the server derived from the booking page, the connection reads Connected.

## The schedule listed after the add, dark theme

![](https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-listed-cleared-dark.png?raw=true)

https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-listed-cleared-dark.png?raw=true

The same state in the dark theme through the application's own theme control.

## The list after the delete, light theme

![](https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-empty-after-delete-light.png?raw=true)

https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-empty-after-delete-light.png?raw=true

The schedule deleted through its own row control; the list falls to its empty reading and the connection still reads Connected.

## The list after the delete, dark theme

![](https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-empty-after-delete-dark.png?raw=true)

https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-ac1-empty-after-delete-dark.png?raw=true

The same empty state in the dark theme.

## The list empty after the assistant half, light theme

![](https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-cleanup-list-empty-light.png?raw=true)

https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-cleanup-list-empty-light.png?raw=true

After the three assistant turns (a schedule on the primary calendar, one on an explicit calendar, one refused for an invalid calendar id) every entry was removed through the app; the list reads empty and the owner's calendar ends clean.

## The list empty after the assistant half, dark theme

![](https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-cleanup-list-empty-dark.png?raw=true)

https://github.com/cinatra-ai/engineering-proofs/blob/main/cinatra/3173/vr5-cleanup-list-empty-dark.png?raw=true

The same clean end state in the dark theme.
