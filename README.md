# PackStealLB Code

### Don't forget:
In order to add this to your Charm++:
* After installing Charm++, include all .C, .h, and .ci files in your `${CHARMDIR}/tmp/` folder. 
* In the `Makefile`, add `UpdateWorkMap.o` and `UpdateProcMap.o` to Charm++'s Chare Kernel object lists, this guarantees these objects are compiled with other Charm++ LB dependencies. 
* In the `Makefile_lb.sh`, add PackStealLB as a Common Load Balancer. 
* Then, `LBDatabase.*` files must be modified to comply with additional parameters of PackStealLB. Our own versions of these are available in deps/
* Execute the following:
```sh
 ./Makefile_lb.sh
 make depends
 make charm++
```
