# Conducting Image Testing

## Testing with Academics

It is very important to ensure that all of the software we have just configured for teaching actually works as expected.
The easiest way to do this is to invite every academic who requested software to test their teaching material on the master
machine. The material they use to test should also be saved to a 'Testing' folder on the master, so that in future
the same test can be conducted with ease.

It is crucial that testing is the final step taken in creating the master before copying the image. No Windows Updates,
driver updates, or additional software should be installed after testing is complete. This is to ensure that the image
academics have tested on is identical to the image deployed in the labs, as even a single driver update can be enough to
break a lot of modules.

## Recording Tests

A record of which modules have been tested, when they were tested, and which academic they were tested by should be kept, 
basically to cover ourselves in case an academic tries to blame us for a module not working correctly.

## Additional Tests

There are some additional tests we must conduct that won't directly be found by academics.

* Unity Signs in and Activates by Script on Startup
* Visual Studio is Updated
* Windows Updates are paused for 5 weeks
* Quest 2 Headsets Work
* Houdini is Licensed Properly
* Oculus App is Signed In
* Epic Games Launcher is Signed In
* Docker Desktop is Set Up
* There will be more as this changes every year. Keep records of requests and be thorough.