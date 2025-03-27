# Hotel release - automation

The Hotel release automation is intended to automatically manage all the hotel room releases according to rules that are being set in the Tourpaq Office administration area.

The service will run daily for each company in the system. It's main goal is to compute the number of rooms that are still available for booking and change the status of their hotel allotment to “suitable for release”, providing the hotel supplier the possibility to log in the Tourpaq system and manage the allotments at will. Secondarily, the service is sending an email to each hotel supplier that had at least one room released in the day the service has run. The email will contain a list of all the rooms that were set as “suitable for release” and were released by applying a release rule that had the supplier's email address set. The service also keeps a log file in the system of all the rooms that were released at each service run.

The Service must be able to execute the following actions:

* For all the hotels of a given company, determine what release rules apply to the date the service runs and retrieve the hotel allotments that fall under those rules.
* For each hotel allotment obtained at step 1, compute the number of rooms to be released (the difference between the number of allocated rooms and booked rooms to this date) and release the room. In the same time, the system must keep record of the released rooms.
* After all the company's hotels have been processed, it must inform the hotel suppliers of the changes made to the system. This must be made by using an email address set in the release rule in Tourpaq Office by which the release was produced. It also must build a log file to record the service activity. For a more detailed example scenario, please refer to \[\[releases]] section from Hotel specification.
