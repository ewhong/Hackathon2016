


Record the details of your config here.

VPN Name: `hackathon`

| Name | Location  | Router_IP  |  RouterName |AWS Region | Notes  |
|------|-----------|------------|-------------|--------|----------|
| Aaron Lee | Hong Kong | 52.78.245.158 | hkgsolaa01 | AP NE (Seoul) | |
| David Wray | London | 52.31.220.231 | DavidHackathon   | EU (Ireland) | |
| Phil Scanlon | Singapore | 52.77.102.138  | hackathon-singapore-vmr | Asia Pacific (Singapore) | |
| Phil Scanlon | Singapore | 52.220.111.223 | pscanlon-vmr   | Asia Pacific (Singapore) | |
| Sumeet Koshal | Singapore | 52.220.165.194 | sumeet-vmr   | Asia Pacific (Singapore) | |
| Vidyadhar Kothekar | Sydney | 13.54.186.240  | Vidya-VMR-Sydney | Asia Pacific (Sydney) | |


# Link Costs:

<b>Note: should be symmetric!!</b>
How to enforce??

| Between | And | Cost |
|---------|-----|------|
| pscanlon-vmr | hkgsolaa01 | 30 |
| hkgsolaa01 | DavidHackathon | 100 |

# Config

Rather than just use the defaults, we could tune a few things... practice!

 - Enable compression on your neighbour links
   - Ensure port 55003 is exposed in AWS
 - Tune TCP params:
   - max-wnd = 1024 (1MB)
   - initial-cwd = 10
 - Tune the CSPF NAB queues if you really want
   - max-length = 40000
   - min-burst = 500

