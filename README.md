# react-native-maps

![image](https://user-images.githubusercontent.com/13164162/114550257-0ab8fe00-9c73-11eb-9406-35fc803876f9.png)


![image](https://user-images.githubusercontent.com/13164162/114550283-11477580-9c73-11eb-8320-f5e62a1d332f.png)


![image](https://user-images.githubusercontent.com/13164162/114550311-16a4c000-9c73-11eb-92f4-d7a94b0d5994.png)


![image](https://user-images.githubusercontent.com/13164162/114550323-1b697400-9c73-11eb-9fc8-19155cb2c35c.png)


Programmatically Changing Region

One can change the mapview's position using refs and component methods, or by passing in an updated region prop. The component methods will allow one to animate to a given position like the native API could.

![image](https://user-images.githubusercontent.com/13164162/114550363-26bc9f80-9c73-11eb-831f-dc10deec8ba0.png)

![image](https://user-images.githubusercontent.com/13164162/114550373-2a502680-9c73-11eb-866d-beb9959bd1d6.png)

Changing the style of the map
![image](https://user-images.githubusercontent.com/13164162/114550398-3340f800-9c73-11eb-965c-96d171386d45.png)


Arbitrary React Views as Markers

![image](https://user-images.githubusercontent.com/13164162/114550432-3e942380-9c73-11eb-941a-439d197db6e7.png)

![image](https://user-images.githubusercontent.com/13164162/114550442-4227aa80-9c73-11eb-937d-4866bdb9ff32.png)

Using the MapView with the Animated API

The <MapView /> component can be made to work with the Animated API, having the entire region prop be declared as an animated value. This allows one to animate the zoom and position of the MapView along with other gestures, giving a nice feel.

Further, Marker views can use the animated API to enhance the effect.

![image](https://user-images.githubusercontent.com/13164162/114550498-51a6f380-9c73-11eb-86ca-af6b59c05ee3.png)

![image](https://user-images.githubusercontent.com/13164162/114550508-553a7a80-9c73-11eb-8e07-d78e6520727d.png)

Issue: Since android needs to render its marker views as a bitmap, the animations APIs may not be compatible with the Marker views. Not sure if this can be worked around yet or not.

Markers' coordinates can also be animated, as shown in this example:

![image](https://user-images.githubusercontent.com/13164162/114550532-5d92b580-9c73-11eb-8502-fe4bb34db438.png)

![image](https://user-images.githubusercontent.com/13164162/114550538-61263c80-9c73-11eb-9402-d8686ec1199b.png)

Other Overlays

So far, <Circle />, <Polygon />, and <Polyline /> are available to pass in as children to the <MapView /> component.

![image](https://user-images.githubusercontent.com/13164162/114550583-6b483b00-9c73-11eb-96f9-8a7974fc794f.png)

![image](https://user-images.githubusercontent.com/13164162/114550600-6f745880-9c73-11eb-89f1-876345a1d48e.png)

Default Markers

Default markers will be rendered unless a custom marker is specified. One can optionally adjust the color of the default marker by using the pinColor prop.
![image](https://user-images.githubusercontent.com/13164162/114550638-78652a00-9c73-11eb-810e-cdb501953ad3.png)

![image](https://user-images.githubusercontent.com/13164162/114550648-7b601a80-9c73-11eb-953b-96427a45aad4.png)


Custom Callouts

Callouts to markers can be completely arbitrary react views, similar to markers. As a result, they can be interacted with like any other view.

Additionally, you can fall back to the standard behavior of just having a title/description through the <Marker />'s title and description props.

Custom callout views can be the entire tooltip bubble, or just the content inside of the system default bubble.

To handle press on specific subview of callout use <CalloutSubview /> with onPress. See Callouts.js example.

![image](https://user-images.githubusercontent.com/13164162/114550674-84e98280-9c73-11eb-9224-cae927f7e7cc.png)

![image](https://user-images.githubusercontent.com/13164162/114550688-887d0980-9c73-11eb-8a9b-a9981a12ec07.png)


Draggable Markers

Markers are draggable, and emit continuous drag events to update other UI during drags.

![image](https://user-images.githubusercontent.com/13164162/114550726-929f0800-9c73-11eb-89b3-e001e6d02e51.png)

![image](https://user-images.githubusercontent.com/13164162/114550735-96328f00-9c73-11eb-8f19-7ba22c7d09b0.png)


On Poi Click (Google Maps Only)

Poi are clickable, you can catch the event to get its information (usually to get the full detail from Google Place using the placeId).
![image](https://user-images.githubusercontent.com/13164162/114550771-a2b6e780-9c73-11eb-8989-86aff8650d5d.png)


