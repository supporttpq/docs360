# Flight Change - How it Works

### Steps:

1. When a change is made to a flight, the Flight Change Type field is automatically filled in (but can be edited later).

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. To save the changes made to the timetable, select the row(s) where changes were made, and 2 options now appear:

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Send Flight Change - The changes to the timetable are saved, and an email is sent to all bookings affected by the changes to the timetable.
* Queue Flight Change - the changes in the timetable are saved and placed in the flight change queue with the change type set in the flight change type in the timetable

3. After all this has been done, go to the [Flight Change](./) menu to complete the flight change process. Select one or more flight changes (only those in the queue) and send an email or SMS using the Send/Send SMS buttons.

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;      Drop - if a flight change is selected and the drop button is used, that flight change is completed, and no more emails/SMS can be sent for that change.

### Flight Change Status

Queued – Initial state; the process has not started yet.

Sent – The process starts manually after the first email or SMS is sent.

Resend First – If the user does not confirm the first email, a follow-up email is sent asking for confirmation. The resend timing is based on configuration settings.

Resend Second – If the user still hasn’t confirmed after the first resend, a second follow-up email is sent, again based on the configured timing.

SMS – If there is no confirmation via email, an SMS is sent a certain number of hours before departure (as specified in the configuration).

Confirmed – Final state. The user confirms the flight changes via email, and the status is updated to confirmed.

Dropped – The process is manually stopped, and the flight change will not proceed or continue.

