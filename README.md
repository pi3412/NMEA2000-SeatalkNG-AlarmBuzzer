# NMEA2000-SeatalkNG-AlarmBuzzer
This is exteranal buzzer for NMEA2000 / SeaTalk-NG Alarms.

See Canboat project for PGN details and alarm types (LOOKUP_SEATALK_ALARM_ID and PGN 65288): https://github.com/canboat/canboat/blob/master/analyzer/pgn.h

Currently PGN 65288 alarms are supported. Other NMEA2000 alarms can be integrated if required (e.g engine related).

An external Buzzer have to be connected to GPIO 5 (with an additional relay).

The wanted alarms have to be defined in able in the code:

struct Seatalk_Alarm Seatalk_Alarm_table[] = {
  { 1,  0 },  // Shallow depth
  { 5,  0 },  // Off Course
  { 14, 0 },  // WP Arrival
  { 20, 0 },  // Pilot Off Course
  { 21, 0 },  // Pilot Wind Shift
  { 22, 0 },  // Pilot Low Battery
  { 29, 0 },  // Pilot Way Point Advance
  { 37, 0 },  // GPS Failure
  { 38, 0 },  // MOB
  { 104, 0 }, // AIS Dangerous Target
};

Just change/add/delete alarms as wanted.

# Update
Verion 0.1 - 28.07.20: Initial version.
