# OpenStreetMap MCAC Bike Parking Tagging Guide

## Table of Contents

<ul>
  <li><a href='#Parking-Attributes'>Bike Parking Attributes</a></li>
  <li><a href='#Parking-Types'>Bike Parking Types</a></li>
  <li><a href='#Parking-Capacity'>Bike Parking Capacity</a></li>
  <li><a href='#Parking-Access'>Bike Parking Access</a></li>
</ul>

<h2 id="Parking-Attributes">Bike Parking Attributes</h2>

The following typical tags are applied to define bike parking attributes within OpenStreetMap.  For bike parking data collected it is desired to record bicycle_parking and capacity attributes for all entries.  Where access is more restricted on non-city owned properties it is desired to indicate the access type as customers or private where required.

| Tag   | Description      |
| ----- | ---------------- |
| <a href="https://wiki.openstreetmap.org/wiki/Key:name">name</a>=* |	Larger areas of bike parking may be named.|
| <a href="https://wiki.openstreetmap.org/wiki/Key:operator">operator</a>=* | 	Cycle parking may be operated by some organisation.|
| <a href="https://wiki.openstreetmap.org/wiki/Key:covered">covered</a>=* | 	Parked bikes are protected from rain. |
| <a href="https://wiki.openstreetmap.org/wiki/Key:access">access</a>=* |	Public access is implied in most roadside cases. Some bike racks may be private with access limited to memberts of a university, company, or other organisation, possibly requiring keys or codes to access. |
| <a href="https://wiki.openstreetmap.org/wiki/Key:capacity">capacity</a>=* | 	The number of bikes that can be parked here. |
| <a href="https://wiki.openstreetmap.org/wiki/Key:fee">fee</a>=* |	In some places, one must pay to park one's bike. |
| <a href="https://wiki.openstreetmap.org/wiki/Key:bicycle_parking">bicycle_parking</a>=* | 	Details the type of bicycle parking (e.g. stands, wall loops...).|
| <a href="https://wiki.openstreetmap.org/wiki/Key:maxstay">maxstay</a>=* |	Maximum time the bicycle is allowed to be parked at that place - given sometimes at covered parking-places.|
| <a href="https://wiki.openstreetmap.org/wiki/Key:surveillance">surveillance</a>=* |	Closed-circuit television (CCTV) security cameras can be marked with this. See the linked page for details of the values in use. Depending on the layout, a separate node nearby may be enough. |

<h2 id="Parking-Types">Bike Parking Types</h2>

The following are local examples of different types of bicycle_parking attributes within OpenStreetMap. 

|Key 	|Value 	|Element 	|Comment 	|Photo |
|--|--|--|--|--|
|bicycle_parking |stands |![node](img/node.png) ![area](img/area.png) |	A bent piece of metal against which you can lean your entire bicycle. Makes it possible to lock the frame and a wheel to it. Moderate security. Rectangular stands are sometimes called "staple racks" in North America due to their shape, and "Sheffield stands" in the UK. Use this tag for non-rectangular stands as well (e.g. round ones, fancy artistic ones, w-shaped). |<img style='min-width:300px;max-width:300px' src='img/parking/stands.png'><img style='min-width:300px;max-width:300px' src='img/parking/stands2.png'><img style='min-width:300px;max-width:300px' src='img/parking/hoop_stand.png'>|
|bicycle_parking | rack |![node](img/node.png) ![area](img/area.png) | A rack is similar to a stand above, but typically larger and holds many more bikes. |<img style='min-width:300px;max-width:300px' src='img/parking/rack.png'>|
|bicycle_parking |wave |![node](img/node.png) ![area](img/area.png) |	A piece of metal bent to resemble a wave.  Similar to a stand, but in use there is only really one attachment point for the bike |<img style='min-width:300px;max-width:300px' src='img/parking/wave.png'>|
|bicycle_parking | wall_loops |![node](img/node.png) ![area](img/area.png)  |Often scathingly referred to as "wheelbenders" by cyclists. Mostly attached to walls or fixed into the ground. Secures only the front wheel (or possibly back wheel), the front bit or lower bit. With application of force, the bike's wheels can be damaged. Low security. 	|<img style='min-width:300px;max-width:300px' src='img/parking/wall_slot.png'><img style='min-width:300px;max-width:300px' src='img/parking/wall_slot2.png'>|
|bicycle_parking | anchors |![node](img/node.png) ![area](img/area.png)  | A mere anchor hammered into a wall, the ground, or boulders. Low security.| 	|
|bicycle_parking | lockers |![node](img/node.png) ![area](img/area.png)  |Parking takes the form of lockers which enclose bicycles fully and individually, typically secured with some form of key or combination system. Good security. Often used at train stations. ||
|bicycle_parking | shed | ![node](img/node.png) ![area](img/area.png)   | A custom-built closed shed in which many bikes can be stored, possibly with individual stands inside. Good security. Use supervised=* to indicate whether bikes are guarded. Alternatively, you can tag it with covered=yes and set the value of bicycle_parking=* to the type of bicycle parking that is inside. ||
|bicycle_parking | bollard |![node](img/node.png) ![area](img/area.png)  |A special kind of bollard designed for bike locking. Generally, the bike is locked to the central pole and "arms" of some sort prevent thieves from simply lifting the bike over the pole. If it doubles as a barrier, add barrier=bollard. |<img style='min-width:300px;max-width:300px' src='img/parking/ring_post.png'>|
|bicycle_parking | ground_slots |![node](img/node.png) ![area](img/area.png)  | Slots in the ground for a wheel. No security. |<img style='min-width:300px;max-width:300px' src='img/parking/ground_slot.png'>|
|bicycle_parking | building |![node](img/node.png) ![area](img/area.png)   | Like shed above, but with a proper building, which means that bicycles are protected from wind, heavy rain etc. Good security. Use supervised=* to indicate whether bikes are guarded. Use opening_hours=* if applicable. Alternatively, if the bicycle parking is not part of another building, you can tag it with building=yes and set the value of bicycle_parking=* to the type of bicycle parking that is inside. ||


<h2 id="Parking-Capacity">Bike Parking Capacity</h2>

The following are examples illustrating expected capacity of different types of bicycle parking.  There is some leeway in how many bikes can be expected to fit, but capacity should be assumed to be how many standard bicycles can be assumed to reasonably fit.

|Type 	|Photo |Capacity|Comment|
|--|--|--|--|
|stands|<img style='max-width:50px' src='img/parking/stands.png'>|8|Enough room to fit a bike on either side of each stand|
|stands|<img style='max-width:50px' src='img/parking/stands2.png'>|9|Only enough room to fit one bike between each stand and a bike can be connected to either outside end|
|stands|<img style='max-width:50px' src='img/parking/hoop_stand.png'>|2|One bike can be attached on either side of the stand|
|wave|<img style='max-width:50px' src='img/parking/wave.png'>|4|Two bikes can been locked inside the wave and one bike can be attached each end of the wave|
|wall_slot|<img style='max-width:50px' src='img/parking/wall_slot.png'>|10|There are 10 slots for bike wheels to be connected to|
|wall_slot|<img style='max-width:50px' src='img/parking/wall_slot2.png'>|6|There are 6 slots for bike wheels to be connected to|
|rack|<img style='max-width:50px' src='img/parking/rack.png'>|5|Five bikes can fit within and be locked to the rack|
|ground_slot|<img style='max-width:50px' src='img/parking/ground_slot.png'>|6|There are 6 slots that bike wheels can be put within|
|bollard|<img style='max-width:50px' src='img/parking/ring_post.png'>|6|Two bikes can be connected to each of the 3 bollards|

<h2 id="Parking-Access">Bike Parking Access</h2>

Access can be left blank for roadside parking that is assumed to be available to everyone within the city.  If usage should be restricted based on ownership the following attributes may be considered.

|Value 	|Description |
|--|--|
|customers|This access type is intended to be used to indicate that the parking is primarily available to customers visiting a business|
|private|This access type is primarily to be used to indicate the use of the parking is limited to to the owner or visitors to the premise.  Ex: School, Place of Worship, etc...|