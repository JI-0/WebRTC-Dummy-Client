# WebRTC dummy client
A dummy client application for creating dummy WebRTC peer clients and testing the limits of WebRTC. This is a test suite that records WebRTC for each peer in .webm format and takes note of every received packet with a timestamp for each peer.

This is a command line application that can be run either using `go run .` or as a release build.

## Instructions
Running the application as a command line application the following flags are available:
| Flag              | Explanation                                           |
| -------------     |:-----------------------------------------------------:|
| -num              | the number of dummy subscribers to generate           |
| -spawnDelay       | the time between dummy client starts                  |
| -autoFinishTime   | the time to automatically finish after all spawned    |
| -onlyTimestamps   | only write timestamps file                            |

The [Signaling server](https://github.com/JI-0/WebRTC_SignalingServer) should be running before this testing suite is run, and a [streamer](https://github.com/JI-0/WebRTC_streamer_web) should already be connected and streaming to the server.

Note that this client will be randomly connected to a single streamer so only one streamer should be connected to the server when this application is run.