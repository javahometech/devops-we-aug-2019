1. Validate
2. Compile
3. Test
4. Package (jar/war/ear)
  - Java Archve (jar)
     jar is used for batch jobs or stand alone applications which does not require web servers.
  - Web Archive (War)
    War is used for web based applications
  - Ear Enterprise Archive (Usage of ear format reduced since many days)
5. Verify (by default it is not configured, you have to explicitly do it if you wanna use this one)
   Verify integration test results
6. Install
    Install the package in to maven local repository
7. Deploy
    Uploads you package to remote repository(Sonatype Nexus/ Jfrog Artifactory)
