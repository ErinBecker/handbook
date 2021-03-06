
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jstimezonedetect/1.0.4/jstz.min.js"></script>
<script type="text/javascript">
  $(function(){
  var timezone = jstz.determine();
  var frame_setup = '<iframe src="https://calendar.google.com/calendar/embed?title=The%20Carpentries%20Zoom%20Room%20Calendar&mode=DAY&'
  var rm1 = 'src=carpentries.org_31323339303138313831%40resource.calendar.google.com&color=%23711616&'
  var rm2 = 'src=carpentries.org_32323738323534333230@resource.calendar.google.com&color=%23BE6D00&'
  var rm3 = 'src=carpentries.org_393634313731303431@resource.calendar.google.com&color=%232F6309&'
  var tz_flag = 'ctz='
  var frame_close = '" style="border: 0" width="700" height="550" frameborder="0" scrolling="no"></iframe>'
  var full_link =  frame_setup + rm1 + rm2 + rm3 + tz_flag + timezone.name() + frame_close;
  document.getElementById('zoom_calendar').innerHTML = full_link;
  // console.log(full_link); 
  });
</script>

### Scheduling Online Community Events

The Carpentries offers three Zoom rooms for public community events.  Zoom rooms are available for events such as discussion sessions, teaching demos, and committee meetings.


#### General Room Usage and Links

Rooms are generally used as follows.  However, any room can be used for other purposes if it is available.
Links below will open Zoom and enter the respective room.

* [**Room 1:**](https://carpentries.zoom.us/my/carpentriesroom1) Instructor Training
* [**Room 2:**](https://carpentries.zoom.us/my/carpentriesroom2) Instructor Training backup
* [**Room 3:**](https://carpentries.zoom.us/my/carpentriesroom3) Community events (teaching demos, discussion sessions, committee meetings, etc.)


Each room can have a host who will have privileges to mute people, create breakout rooms, etc.  Please contact team@carpentries.org if you would like host privileges for an event.

#### Viewing Zoom Room availability

Zoom room calendar views are public - anyone can view whether a room is available.  Only Carpentries staff members can actually book a room. If a room is available, please contact a staff member or team@carpentries.org if you would like to make a room reservation.

Room availability can be viewed below. 
* Red: Room 1
* Orange: Room 2
* Green: Room 3

<div id = 'zoom_calendar'>Placeholder: Embedded Zoom Room Calendar</div>

<p>

#### Adding an Event to the Community Calendar

Note while anyone can view room availability, only Carpentries staff members may book events or reserve a Zoom room.

To add an event to the [Community Calendar](https://calendar.google.com/calendar/embed?src=oseuuoht0tvjbokgg3noh8c47g%40group.calendar.google.com&ctz=America%2FNew_York) and book a Zoom Room for it:

* Give the event a meaningful title ("Demos" is not as good as "Instructor Training Teaching Demos")
* List the time zone in UTC - not your local time zone.  Events set in local time zones do not always correctly adjust for daylight savings time.
* Add a description, including a link to the relevant etherpad or other document.

![Event Setup](images/event_setup.png)

* Select a room.

    ![View Rooms](images/view_rooms.png)

    * Each available room will be listed. If you are scheduling a recurring event, any future conflict will prevent a given room from being listed as available.
    * Multiple rooms can be selected for a single event.
    * Click on a room to select it.  The Zoom link will now appear in the location.

    ![Reserved Room](images/reserved_room.png)

    * If you select a room and immediately remove it, it may not appear as available again until you close out the edit event screen and enter it again.
    * Save the event.
    * The event will now show up on the Carpentries Community Calendar and the Zoom Rooms Calendar.


Be sure to complete the above steps in order (i.e., do not select a room before setting the exact date and time).


<p>

#### Creating a Zoom Room Option on Google Calendars

This will only need to be done once for each new room.  This is already done for Zoom Rooms 1, 2, and 3.  If additional Zoom rooms are added, they will need to be set up here.  This must be done by someone with admin access to The Carpentries' Google console.  

Go to the [Google admin console](https://admin.google.com/AdminHome?hl=en).  Click on "Buildings and Resources" and then click "Edit Resources" under "Resource Management."

You will see all existing buildings and rooms listed. This feature is meant for physical buildings; we are using it for virtual videoconferencing rooms. One "building" is set up, called "Zoom Rooms" that contains three resouces -- Zoom Room 1, Zoom Room 2, and Zoom Room 3.  

To add a new "room" in this "building" - click on the yellow plus sign next to "Resources."  Fill out the following information:

* Category: (no category set)
* Type: *leave blank*
* Building: Undefined
* Floor: Undefined
* Floor section: *leave blank*
* Resource name: Link to the Zoom Room
* Capacity: 100 (standard for all Zoom rooms)
* Features: *leave blank*
* User visible description: Note what this room is used for.

When done, click "ADD RESOURCE" and this new room should be on your list of rooms.  This room will now be available for scheduling events as described below.


