# MAven SNAPSHOT and RELEASE version

SNAPSHOT and RELEASE is maven conventions

### RELEASE Version

According to maven convention dependency with RELEASE version will not have new changes, maven downloads it from central/remote ones
and depends on local copy next time onwards.
if version is not ending with -SNAPSHOT then it is release

### SNAPSHOT Version

According to maven convention dependency with SNAPSHOT version will have new changes, maven downloads it from central/remote every time
you build your application.

if version is ending with -SNAPSHOT then it is SNAPSHOT
