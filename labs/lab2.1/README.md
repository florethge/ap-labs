# Advanced Programming 
## Ap-lab
## Lab 2.1 ClockWall
### Programming language: Go

Modify the clock2.go to accept a port number, and write a program clockWall.go, that acts as a client of several clock servers at once, reading the times from each one and displaying the results in a table, akin to the wall of clocks seen in some business offices. If you have access to geographically distributed computers, run instances remotely; otherwise run local instances on different ports with fake time zones.

### Clock Servers initialization

$ TZ=US/Eastern    ./clock2 -port 8010 &
$ TZ=Asia/Tokyo    ./clock2 -port 8020 &
$ TZ=Europe/London ./clock2 -port 8030 &



# Starting clockWall client

$ clockWall NewYork=localhost:8010 Tokyo=localhost:8020 London=localhost:8030
US/Eastern    : 12:00:00
Asia/Tokyo    : 17:00:00
Europe/London : 02:00:00
.
.
.

### General Requirements and Considerations

Use the clock2.go and clockWall.go files for your implementation.
Update README.md with the proper steps for building and running your code.
Follow the command-line arguments convention.
Don't forget to handle errors properly.
Coding best practices implementation will be also considered.

#### Running the Code:
 //To Compile
 go build clock2.go
 go build clockWall.go 
 

#### Usage of the Code:
Initialize the servers with the help of these commands:


$ TZ=US/Eastern    ./clock2 -port 8010 &
$ TZ=Asia/Tokyo    ./clock2 -port 8020 &
$ TZ=Europe/London ./clock2 -port 8030 &

#### To execute the program run:
./clockWall NewYork=localhost:8010 Tokyo=localhost:8020 London=localhost:8030