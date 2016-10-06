# Sleep_Until.sh - YAD GUI for RTCWake: Make your computer sleep and wake up at a given time
## by Jorge A. Duarte

SleepUntil is a bash script, which makes use of [YAD](https://code.google.com/archive/p/yad/) to capture data for *rtcwake* through a GUI Dialog. Through *rtcwake* the OS sleeps, and wakes up at a given time (today or tomorrow).

### Requirements:
    
    #### Ubuntu: (might work on other distros)
        - For now it has been tested on Ubuntu 16.04
    #### YAD:
    
        ```
        $ sudo apt-get install yad
        ```
    #### Hardware Clock:
        - Hardware clock must be set to UTC. If not, the script must be edited (remove the -d flag from rtcwake)
        
### Instructions:

    - Download the script *'sleep_until.sh'*
    
    - Change permissions to allow execution:
      ```
      $ chmod +x sleep_until.sh
      ```
    - Execute the script:
      ```
      $ ./sleep_until.sh
      ```
    - Input parameters on GUI:
      - Day: ['today' / 'tomorrow']
      - Time: [Time in 24h format (i.e. 06:30 or 22:15)]
