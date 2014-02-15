Kitchensink on OpenShift
=========================

This is the kitchensink html5/mboile JBoss Quickstart app.

Running on OpenShift
--------------------

Create an account at http://openshift.redhat.com/

Create a jbossas application

    rhc app create kitchensinkhtml5 jbossas-7

Add this upstream kitchensink-html5-mobile repo

    cd kitchensinkhtml5
    git remote add upstream -m master git://github.com/openshift/kitchensink-html5-mobile-example.git
    git pull -s recursive -X theirs upstream master

Then push the repo upstream

    git push

That's it, you can now checkout your application at:

    http://kitchensinkhtml5-$namespace.rhcloud.com
