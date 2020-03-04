If you want to know more, go to mark-sch's fork

meant for UI, CLI is mostlikely broken

## Getting started

- git clone https://github.com/p96xl/GreenGekko.git
- cd GreenGekko
- npm install babel-loader babel-core babel-preset-env webpack --ignore-scripts
- (For docker you can do 'sudo docker-compose build', and ignore steps below)
- npm install 
- cd exchange
- npm install
- cd ..
- node gekko --config sample-eth.js --import --set debug=true
- node gekko --config sample-eth.js --backtest --set debug=true
- node gekko --config sample-eth.js

While running the strategy with sample-eth.js config you should [see an output like this](https://git.io/Jex0a)

from time to time the exchange markets should be updated with a utility - to get new coin pairs:

- cd exchange/util/genMarketFiles/
- node update-kraken.js
- node update-binance.js

- (postgresql experience required to previously setup postgres. Sample config assumes an existing db user gekkodbuser, pass 1234, with added role permission to createdb. PostgreSQL 9.5+ required.)

See further info how to get started and how to setup postgresql from [crypto49er at youtube](https://www.youtube.com/watch?v=vIqe-EPAMeU)

> A good practice to run Gekko processes on a server is using process manager 2 tool:
>
> **pm2 start gekko.js -i 1 --name "gekko-bnb" -- --config config-bnb.js**

## Documentation

See [the documentation website](https://gekko.wizb.it/docs/introduction/about_gekko.html).

