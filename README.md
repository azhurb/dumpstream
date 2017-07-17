# Dumpstream

MPEG-TS stream dump. Can works with rtp/udp streams. 

## Usage

```
usage: dumpstream [-h] [-a IP_ADDRESS] [-p PORT] [-d SAVE_DIRECTORY]
                  [-n PIECES_NUMBER] [-c CALLBACK_URL] [-l LENGTH]
                  [-s START_DELAY] [-o OUT_FILE] [-b BUFFERING]

Stream dump. Can work with rtp and udp streams.

optional arguments:
  -h, --help            show this help message and exit
  -a IP_ADDRESS, --ip_address IP_ADDRESS
                        ip address
  -p PORT, --port PORT  port
  -d SAVE_DIRECTORY, --save_directory SAVE_DIRECTORY
                        directory to save pieces
  -n PIECES_NUMBER, --pieces_number PIECES_NUMBER
                        number of pieces
  -c CALLBACK_URL, --callback_url CALLBACK_URL
                        callback url, use to send HTTP PUT with
                        start_time/end_time params
  -l LENGTH, --length LENGTH
                        recording length
  -s START_DELAY, --start_delay START_DELAY
                        delay before start recording
  -o OUT_FILE, --out_file OUT_FILE
                        save output to file with specified name
  -b BUFFERING, --buffering BUFFERING
                        buffer to use when opening files
```
