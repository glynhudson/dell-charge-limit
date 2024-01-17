# dell-charge-limit

Linux command line scripts to limit Dell laptop charge level.

Laptop battery life can be prolonged by limiting the charge level to 80%. E.g when plugged into AC for long periods. 

Tested on:
#### 1. Configuration
- Dell XPS 13 9360
- Ubuntu 20.04 
- Dell Command | Configure 4.3 
#### 2. Configuration
- Dell Vostro 10 3510
- Ubuntu 20.04
- Dell Command | Configure 4.7
#### 3. Configuration
- Dell XPS 17 9720
- Ubuntu 23.10
- Dell Command | Configure 4.11.0

It's possible to set a charge limit in the BIOS, however it's inconvenient to have to reboot to charge the level e.g when a full charge is required. 

The Dell Command Config tool provides a way to adjust the charge limit via command line, I’ve wrapped up these commands into a simple bash script to make them easy and quick to run.

## Install Dell Command Config 

Download pre-compiled .deb from: https://www.dell.com/support/article/en-uk/sln311302/dell-command-configure?lang=en

## Clone this repo 

```
git clone https://github.com/glynhudson/dell-charge-limit
cd dell-charge-limit
```

## Set charge limit 60%-80% (longlife)

`./battery-charge-longlife.sh`

## Set charge limit to default (‘adaptive’)

`./battery-charge-full.sh`

‘Adaptive’ will result in a full 100% charge, but I think may reduce this charge level if plugged in for a long period. 
 
In my experience the setting is persistent over reboots, as expected since we’re adjusting a BIOS setting.  

Source: https://www.dell.com/community/Linux-Developer-Systems/Setting-the-battery-charge-level-within-Linux/td-p/5087362




