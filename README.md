g2 Functional Tests
=============================

Python version needed: 2.4
current RPM: https://ci.dcache.org/view/Test%20Suite/job/Build-G2/

How to run the tests:

1. Make sure you're environment is sane.

    In particular, the following commands must be in your PATH:

       edg-gridftp-ls, edg-gridftp-rm, globus-url-copy
       lcg-cp, lcg-gt, lcg-ls, srmcp, srm-get-space-tokens
       srmls, srmmkdir, srmmv, srmrm, srmrmdir,
       srm-set-permissions


2. Define some basic information about the test system:

    *  The hostname:

        export DFTS_SUT=test-host.example.org

    *  A base path, one you can write into:

        export DFTS_BASEPATH=/data/g2-tests

3. Create a X.509 proxy certificate:
    
    A typical invocation looks like

        voms-proxy-init --voms my-VO

4. Run the G2 tests:
 * python srmcopy.py
 * python spacemanager.py
 * python lcgcopy.py
 * python serviceports.py
 * python gsiftp.py
 * python dcap.py




