
# Mailcatcher

Super small 13MB image of the latest 0.6.4 release of [mailcatcher][1]. 

To run the image in the foreground and delete when stopped: 

`docker run -p 1080:1080 -p 1025:1025 -ti --rm beardyjay/mailcatcher`

Start the image in the background:

`docker run -d -p 1080:1080 -p 1025:1025 -ti beardyjay/mailcatcher`

Now connect to http://127.0.0.1:1080 to view messages

[1]: https://mailcatcher.me/

