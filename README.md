# The world in the ocean

## DEVELOPMENT

The game is 100% client side javascript and css. It should run when served up by any web server.

Any changes to the following files will be reflected immediately on refresh of the browser

  - js/delta.js
  - css/delta.css
  - images/
  - levels/

However, if you modify the js/game/ or js/vendor/ javascript files, the unified versions need to be regenerated:

    js/vendor.js        # the unified 3rd party vendor scripts (fpsmeter, state-machine, etc)
    js/game.js          # the unified general purpose game engine

If you have the Ruby language available, Rake tasks can be used to auto generate these unified files:

    rake assets:create   # re-create unified javascript/css asset files on demand
    rake assets:server   # run a simple rack server that automatically regenerates the unified files when the underlying source is modified


