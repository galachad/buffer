Buffer
======

RunClientScript/RunServerScript data "packer" for FOnline scripts. Partially based on Serializator (TLA scripts) and BufferManager (FOnline engine). Created for storing data of various types (ints, string, arrays, etc.) into single variable.

BufferLazy
===========

Buffer addon for sending data bigger than *__FloodSize* between server and client

#### Requirements ####
BufferLazy requires additional functions provided by .dll file (see buffer_lazy.cpp)

* [SERVER] Critter::RunLocalScript( string& function, int p0, int p1, int p2, string@ p3, int[]@ p4 );
* [CLIENT] RunLocalScript( string& function, int p0, int p1, int p2, string@ p3, int[]@ p4 );

Works in similiar way as SDK Run*Script() functions; difference is, that request is not sent anywhere, but works on currently used AngelScript engine.

* [SHARED] IsLocalScript( string& function );

Checks if given function exists and can be used by RunLocalScript()
