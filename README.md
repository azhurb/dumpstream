# Dumpstream

MPEG-TS stream dump. Can works with rtp/udp streams.  
rtpdump compatible.

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

## Examples
```
python ./dumpstream -a 224.1.1.1 -p 1234 -s 60 -l 3600 -c /api/callback/ -o /save/path/dump.mpg -b 1
```

```
python ./dumpstream -a 224.1.1.1 -p 1234 -d /save/path/ -n 24 -b 1
```
Stores pieces of 1 hour duration in a directory `/save/path/` for 24 hours.

## License
Licensed under the MIT license.
