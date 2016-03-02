
# Warvox

This is based of the latest commit to master that I could get running(c25db67) which is dated Oct 23 2015. 

[Warvox repo]

## Running Warvox

Pull the standard postgres image

`docker pull postgres` 

Start the image in the background

`docker run -d --name=postgres postgres`

Run the warvox container, linking the progres container and opening up port 7777. 

`docker run -d -p 7777:7777 -ti --link postgres:db beardyjay/warvox`

Now connect to port http://127.0.0.1:7777

[Warvox repo]: <https://github.com/rapid7/warvox/>
