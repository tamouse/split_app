Try out a repo with a split api and client in subdirs

I've run into problems working on a Rails API application using
RubyMine, while at the some time working on the web client in
WebStorm. The usual "answer" is to use IntelliJ for both, but that's a
really poor compromise, since the separate IDEs provide a lot more
than what's combined in IntelliJ. The feel of the latter also remains
pretty much rooted in Java development, as well, with having to find
how things work, configuring the IDE, and such stuff just makes it the
least viable option for me.

Splitting the repo into server and client means I can devote one
directory to each, without running into the small configuration
conflicts trying to use them with the same .idea folder.

This works for me. YMMV.

The top-level package.json file doesn't have any
libraries/dependencies in it, it's primary function is to provide:

1. npm scripts to make things easier to operate
2. the webpack-dev-server proxy to let it proxy requests to the
   server, eliminatinug CORS issues when using two web servers
