# puber
*Everyone's personal...*

Puber is an app that helps you know before you go.  


## General

Visit http://brendano86.github.io/puber to get started.

## How it works

When you need to sit down for a time, simply let Puber know so that other users know before *they* go.  When you're done you can either sound the all clear or "give it a minute" (see timing below).

Before you go, check Puber to see the current status of the "passenger's seat."

### Statuses

There are 5 possible Puber statuses, similar to other alert systems in the world.

1. Severe (red) - Ride in progress.  Abort mission.
2. High (orange) - Ride has been in progress for 10 minutes or more and/or an UPU (Unidentifed Puber User) has been spotted.  Could be okay.  Could be the opposite of okay.
3. Elevated (yellow) - Ride is over, but need to give it a minute.  5 minutes or so after this status, Puber will sound the all clear
4. Gaurded (blue) - Ride has been in progress for 20 minutes or more.  Please be okay...please...
5. Low (green) - Ride is over or it has been 25 minutes or more since last ride or the give it a minute has expired.

### Timing

Every 5 minutes the Puber clean up service (PCS) checks for the current puber status.  Based on the status level at the time, the following rules are applied:

* If the status is red
 * If it has been 10 minutes or more since status change, change status to orange
* If the status is orange
 * If it has been 10 minutes or more since status change, change status to blue
* If the status is yellow
 * If it has been 5 minutes or more since status change, change status to green.
* If the status is blue
 * If it has been 5 minutes or more since status change, change status to green.
* If the status is green
 * Do nothing
