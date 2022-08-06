AzaadiSAT - LoRa Parameters:
Carrier Frequency: 437.4 Mhz
Bandwidth: 125.0 kHz
Spreading Factor: 9
Coding Rate: 7
Output Power: 22 dBm
Preamble Length: 8 Symbols
Sync Word: 0x12
Gain: 0


AzaadiSAT - AX.25 Parameters:
Frequency: 437.4 Mhz
Output Power: 22 dBm
Frequency Shift: 425 Hz
Baud Rate: 1k2 Baud
Stop Bits: 1


Health Beacon Frame Structure:
Satellite Callsign, Frame Number, Tx Power, Packet Type, Boot Count, Internal Temperature,
Power Bus Voltage, Power Bus Current, Solar Panel Voltage, Panel Number, Battery
Temperature, Radiation Sensor Data


Store and Forward Message:
Satellite Callsign, Frame Number,1,[MESSAGE]


Uplink Command for Store and Forward Message:
#[MESSAGE]


Note: The maximum length of the beacon message should be no longer than 50 characters.
Should only contain A-Z, a-z, 0-9, !, @ $ % ^ ( ) ? ; : <SPACE>
  
  
Transmission Cycle:
Start → Receive Mode (45 sec) → LoRa Health Packet → AX.25 Health Packet → CW Beacon
→ Store and Forward Message (LoRa) → End (Loop)
This entire transmission takes 15 seconds to happen and there will be 45 seconds in receive
mode, so totally there will be one transmission loop every minute.
