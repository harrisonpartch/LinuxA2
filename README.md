LinuxA2
=======
This is the latest release of the Linux port of the ETH A2 system (also called Bluebottle or Aos).  


Installation:
-------------

1. Unpack the System

   as root:
      chmod +x install.UnixAos
      install.UnixAos  LinuxA2[n].tar.gz

System Sources:
---------------

The system sources are kept in a subversion repository at ETHZ which is mirrored at https://github.com/harrisonpartch/ethzoberonmirror

 git clone https://github.com/harrisonpartch/ethzoberonmirror.git


Then create a working directory with three links into the local copy of
the repository and start Aos in it:

   mkdir linuxa2

   cd linuxa2

   mkdir NewAos

   ln -s ../ethzoberonmirror/source source

   ln -s ../ethzoberonmirror/UnixAos Unix

   ln -s Unix/buildtools Tools

   aos

   Docu:UnixAos Build (follow the instructions. After compiling the modules, go to the linux command line in the same directory: mv *Obj NewAos/   .  Then link (step 2 in the instructions). Now a new aos has been compiled from source. "aos" in NewAos/ will run it. "cp LinuxAosCore *.Obj /usr/aos/obj/" will install it. Yes, the part about moving the object files before linking should not be necessary and will be changed soon; probably these instructions will not be revised at the same time, leading to confusion. C'est la vie.)

