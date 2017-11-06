# CyberSecurity_Week9_Assignment

Time spent: 6 hours spent in total

> Objective: Setup a honeypot and provide an exfil data.

### Required: writeup 
- For this assignment I setup Honey pot via gcloud. On the admin console I setup 3 honeypots dianos, Snort and amun(This one is the best). One major issue is that running mongeDB on my admin client crashed and corrupted my system so i had to reset my honeypot the day before the project was due. Other than that i ended up being scaned 8 times in 1 min which was interesting. 
- One Issue i have been unable to resolve is exfilling data from the admin VM. Currently running mongeDB crashes my admin console and renders thte VM useless.  
- Reinstalling seemed to fix that issue
## Video Walkthrough


Here's a walkthrough of implemented user stories:

<img src='https://github.com/lquinn2015/CyberSecurityCourse/blob/master/Attacks.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Attack Reports
-All of the attacks i have records on were telnet attacks to my amun server which seems simplistic but i suppose this is the most common way to check if your attackable.

## Notes
This lab was fun.

## License

Copyright [2017] [Luke Quinn]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
