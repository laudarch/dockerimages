
# Mailcatcher

Super small 13MB image of the latest BETA version 0.7.0.beta1 release of [mailcatcher][1]. 

## Pull

`docker pull beardyjay/mailcatcher`

## Run 

To run the image in the foreground and delete when stopped: 

`docker run -p 1080:1080 -p 1025:1025 -ti --rm beardyjay/mailcatcher`

Start the image in the background:

`docker run -d -p 1080:1080 -p 1025:1025 -ti beardyjay/mailcatcher`

Now connect to http://127.0.0.1:1080 to view messages send messages to 127.0.0.1:1025


[1]: https://mailcatcher.me/

