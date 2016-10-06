# Sleep_Until.sh - YAD GUI for RTCWake: Make your computer sleep and wake up at a given time
## by Jorge A. Duarte

SleepUntil is a bash script, which makes use of [YAD](https://code.google.com/archive/p/yad/) to capture data for *rtcwake* through a GUI Dialog. Through *rtcwake* the OS sleeps, and wakes up at a given time (today or tomorrow).

![Alt text](SleepUntil.png?raw=true "Application Screenshot")

### Requirements:
####  Ubuntu: (might work on other distros):
- For now it has been tested on Ubuntu 16.04

#### YAD:
- Install YAD using apt-get:
```
$ sudo apt-get install yad
```

#### Hardware Clock:
- Hardware clock must be set to UTC. If not, the script must be edited (remove the -u flag from rtcwake):
```
[FILE: sleep_until.sh]
...
# replace "sudo rtcwake -m mem -u -t $(date +%s -d "$foo")" for:
sudo rtcwake -m mem -t $(date +%s -d "$foo")
...
```

### Instructions:
- Download the script *'sleep_until.sh'*:
```
$ git clone https://github.com/babetoduarte/SleepUntil.git
$ cd SleepUntil
```
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
