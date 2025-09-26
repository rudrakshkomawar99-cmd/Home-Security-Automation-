# Home-Security-Automation-
this project is made using basics of C programing (like if else loop) to automate home security features 
#include <stdio.h>
  int main() {
 
    int fireAlarmSystem, doorLockSystem, fireSprinklerSystem, masterSystem;

    printf("                        WELCOME TO YOUR SECURITY ASSISTANT \n");
    printf("THE MOTION DETECTORS AND SMOKE ALARM HAS DETECTED SOMETHING CHECK THE CCTV AND TAKE APPROPRIATE STEPS \n ");
    printf("Enter 1 to turn ON, 0 to turn OFF:\n");

    printf("Master Switch (1 = ON, 0 = OFF): ");
    scanf("%d", &masterSystem);

    if (masterSystem == 1) {
        // Full home ON: all systems active
        fireAlarmSystem = 1;
        doorLockSystem = 1;
        fireSprinklerSystem = 1;

        printf("Total Home Shutdown mode ACTIVATED!\n");
        printf("All systems are now ON.\n");
        return 0;
    } else {
    printf("Door Lock System (1 or 0): ");
    scanf("%d", &doorLockSystem);

    printf("Fire Safety Alarm System (1 or 0): ");
    scanf("%d", &fireAlarmSystem);

    printf("Fire Sprinkler System (1 or 0): ");
    scanf("%d", &fireSprinklerSystem);


    // Control Door Lock
    if (doorLockSystem == 1) {
        printf("Door Lock is ENGAGED (Unlocked)\n");
    } else {
        printf("Door Lock is  NOT ENGAGED (Locked)\n");
    }

    // Control Fire Alert Alarm
    if (fireAlarmSystem == 1) {
        printf("Fire Safety Alarm is ON\n");
    } else {
        printf("Fire Alarm is OFF \n ");
    }
 
    // Control Fire Sprinkler System
   if (fireSprinklerSystem == 1) {
        printf("Fire Sprinkler System is ACTIVATED\n");
    } else  {
        printf("Fire Sprinkler System is DEACTIVATED\n");
    }

    return 0;
   }
}
