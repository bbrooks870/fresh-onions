## Footnotes

- This file (`README.md`) is auto-generated
  - *Do NOT submit changes NOR pull-requests for it*
  - Please submit an `Issue` for consideration / change requests
- If both v2 and v3 addresses are provided for a service, the v3
  address will be preferred / cited
- At the moment where an organisation runs 2+ onion addresses for
  closely related services that do not reflect distinct languages /
  national interests, I am posting a link to an index of their
  onions. Examples: Riseup, Systemli, TorProject, ...
- The master list of Onion SSL EV Certificates may be viewed at
  https://crt.sh/?q=%25.onion

### RWOS Status Detector

- :heavy_check_mark: site up
- :eight_spoked_asterisk: site up, and redirected to another page
- :no_entry_sign: site up, but could not access the page
- :stop_sign: site up, but reported a system error
- :sos: site returned no data, or is down, or curl experienced a
  transient network error
- :new: site is newly added, no data yet

### Codes & Exit Statuses

Mouse-over the icons for details of HTTP codes, curl exit statuses,
and the number of attempts made on each site.

- codes [are from HTTP and are documented elsewhere](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes); RWOS-internal ones include:
  - `901`, `902`, `903` - malformed HTTP response
  - `904` - HTTP status code parse error
  - `910` - connection timeout
- exits [are from Curl and are documented elsewhere](https://curl.haxx.se/libcurl/c/libcurl-errors.html); common ones include:
  - `7` - "curl couldn't connect"
  - `52` - "curl got nothing", received no data from upstream

### TLS Security

Due to the fundamental protocol differences between `HTTP` and
`HTTPS`, it is not wise to consider HTTP-over-Onion to be "as secure
as HTTPS"; web browsers **do** and **must** treat HTTPS requests in
ways that are fundamentally different to HTTP, e.g.:

- with respect to cookie handling, or
- where the trusted connection terminates, or
- how to deal with loading embedded insecure content, or
- whether to permit access to camera and microphone devices (WebRTC)

...and the necessity of broad adherence to web standards would make it
harmful to attempt to optimise just one browser (e.g. Tor Browser) to
elevate HTTP-over-Onion to the same levels of trust as HTTPS-over-TCP,
let alone HTTPS-over-Onion.  Doubtless some browsers will *attempt* to
implement "better-than-default trust and security via HTTP over
onions", but this behaviour will not be **standard**, cannot be
**relied upon** by clients/users, and will therefore be **risky**.

**tl;dr** - HTTP-over-Onion should not be considered as secure as
HTTPS-over-Onion, and attempting to force it thusly will create a
future compatibility mess for the ecosystem of onion-capable browsers.

- :wrench: semi-secure HTTP Onion site, protected by Onion circuits at
  best; will not respect browser secure/HTTPS behaviour
- :closed_lock_with_key: secure HTTPS Onion site, protected by both
  Onion circuits and TLS, will respect browser secure/HTTPS behaviour

## Setup

This script runs on a Linux System.

You can also run a linux system on Windows OS as shown [here](https://gist.github.com/alx-xlx/82db67e2b2b06602625a0ee0bfc3d9a9)

### Pre-Requisites
```sh
sudo apt-get install tor -y  # Install TOR
sudo apt-get install python3 -y # Install Python3
sudo apt-get install python3-pip -y # Install Python3 Package Manager
```



```sh
git clone https://github.com/alx-xlx/fresh-onions.git
cd fresh-onions
bash run.sh
```

### Troubleshoot

```sh
curl http://checkip.amazonaws.com   # Check Surface IP (Original IP)
curl --socks5 127.0.0.1:9050 http://checkip.amazonaws.com   # Check Tor IP
```

### Source Code

author : [lecmuffett](https://github.com/alecmuffett/real-world-onion-sites)

----
[Back to Top](#fresh-onions)
