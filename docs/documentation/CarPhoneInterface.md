**Phone to Car**



interface CarControl{

public void automaticDrive(Gps gpsData) 

public void getGpsData();

public void startGpsData(int interval); //interval  ms Takt 

public void stopGpsData();

public void startManualDrive();

public void stopManualDrive();

public void emergencyStop();

public void continueDriving();

public void manualDirection(Drive direction1, Steering direction2);

}



**Car to Phone **

interface PhoneControl{

public void sendStatus( Status state);

public void sendLocation( Gps gpsData);

}



**Structs and enums**



enum Drive{

"stop"

"front"

"back"

}



enum Steering{

"forward"

"left"

"right"

}



enum Status:{

"destination",

"driving",

"error" (String errorMessage )

}



Struct Gps{

float latitude;

float longitude;

}









