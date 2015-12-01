The following new directories are required for the deferred implementation to work:

src/materialsystem/
src/game/client/deferred/
src/game/server/deferred/
src/game/shared/deferred/

+ shader compiling:
src/dx9sdk/
src/devtools/

A few changes in standard files have to be made first too.
All of them have comments like this:

// @Deferred - Biohazard

affected files that require updating:

src/game/client/cdll_client_int.cpp
src/game/client/viewrender.h
src/game/client/viewrender.cpp		(not all changes have a comment since there are too many, use diff)
src/game/client/flashlighteffect.h
src/game/client/flashlighteffect.cpp
src/game/server/gameinterface.cpp
src/public/renderparm.h



Most core tweaks and changes can be done in the following headers:

src/materialsystem/swarmshaders/deferred_global_common.h
src/game/client/deferred/deferred_client_common.h
src/game/shared/deferred/deferred_shared_common.h
src/game/server/deferred/deferred_server_common.h