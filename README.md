# API Introduction

## 1.document 
(1) **sceneInfo.json** : A true message socket show the connection between the scenes and users.  
(2) **sceneInfo.py**: Input API, Users can print the information in json source file, and learn how to use the API quickly.

## 2.Input API
These APIs are what information that users can get from the scenes.  
FILE: **sceneInfo.py** : You can excute the program and print the string from the 


***API Init**  
We have Init the Object for you in ***main.py*** function
`dataState, apiList = socketServer.socket_launch()`  

Then the ***apilist*** is what you can get from the scene API. And you can get the scene, here are the usage of the api, all the return v
alue data ***type*** is ***Dictionary***:   

### 2.1 **apiList.trajListLenAPI()** : 
You can get the length of the scene alternative path 
```
def trajListLenAPI(self):
    return self.__trajList['trajectorySize']
```
And the print result is: 
```
print(apiList.trajListLenAPI())
#
20 
```
### 2.2 **apiList.trajListAPI()** : 
You can get the scene alternative path 
```
def trajListAPI(self):
    return self.__trajList
```
And the print result is: 

```
print(apiList.trajListAPI())
###
# {'trajectorySize': 20, 'trajectory': 
# [{'P': {'x': -1.88, 'y': -27.07, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -28.06, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -29.06, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -30.05, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -31.05, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -32.06, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -33.04, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -34.04, 'z': 0.0}, 'V': None},
#  {'P': {'x': -1.88, 'y': -35.04, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -36.04, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -37.06, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -38.04, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -39.05, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -40.05, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -41.04, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -42.06, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -43.03, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -44.03, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -45.03, 'z': 0.0}, 'V': None}, 
#  {'P': {'x': -1.88, 'y': -51.03, 'z': 0.0}, 'V': None}]}
```
### 2.3 **apiList.DataGnssAPI()** : 
You can get the pose of the vehicle
```
def DataGnssAPI(self):
    return self.__DataGnss['poseGnss']
```
And the print result is: 
```
print(apiList.DataGnssAPI())
#{'posX': -1.883, 'posY': -27.955, 'posZ': -0.042, 
#'velX': 7.03, 'velY': 0.0, 'velZ': -0.026, 
#'oriX': 0.0, 'oriY': -359.79, 'oriZ': 90.019}
```

### 2.4 **apiList.DataMainVehilceAPI()** : 
You can get the main vehicle properties.
```
def DataMainVehilceAPI(self):
    return self.__DataMainVehilce
```
And the print result is: 
```
print(apiList.DataMainVehilceAPI())
# {'mainVehicleId': 0, 'speed': 7.03, 'gear': 3, 'throttle': 0.0, 
# 'brake': 0.0, 'steering': 0.0, 'length': 4.814, 'width': 2.18, 
# 'height': 1.908}
```

### 2.5 **apiList.VehicleSignalLightAPI()** : 
You can get the vehicle signal. 
```
def VehicleSignalLightAPI(self):
    return self.__VehicleSignalLight
```

And the print result is: 
```
print(apiList.DataMainVehilceAPI())
# {'mainVehicleId': 0, 'speed': 7.03, 'gear': 3, 'throttle': 0.0, 
# 'brake': 0.0, 'steering': 0.0, 'length': 4.814, 'width': 2.18, 
# 'height': 1.908}
```

### 2.6 **apiList.ObstacleEntryListAPI()** : 
You can get the obstacles information in our scene. 
```
def ObstacleEntryListAPI(self):
    return self.__ObstacleEntryList
```

And the print result is: 
```
print(apiList.ObstacleEntryListAPI())
# 
```
### 2.7 **apiList.TrafficLightListAPI()** : 
You can get the traffic light information in our scene. 
```
def TrafficLightListAPI(self):
    return self.__TrafficLightList
```

And the print result is: 
```
print(apiList.TrafficLightListAPI())
# 
```

### 2.8 **apiList.RoadLineListAPI()** : 
You can get the road line information in our scene. 
```
def RoadLineListAPI(self):
    return self.__RoadLineList
```

And the print result is: 
```
print(apiList.RoadLineListAPI())
# 
```

## 3.Output API
These APIs are what users should send to the scenes. 
file: vehicleControl.py. 

API:json_encoder: