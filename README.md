# TrainPlotter

Generate JSON files for plots in during training networks.


## Installation
Use following command:
```
luarocks install trainplot-0.1-1.rockspec
```

## Usage
```lua
require 'TrainPlotter'
local plotter = TrainPlotter.new('plot-data/out.json')
plotter:add('Accracy', 'Train', 1, 0.5)
plotter:add('Accracy', 'Train', 2, 0.7)
plotter:add('Accracy', 'Train', 3, 0.8)
plotter:add('Accracy', 'Test', 1, 0.45)
plotter:add('Accracy', 'Test', 2, 0.6)
plotter:add('Accracy', 'Test', 3, 0.7)
```

## Seeing Plots
Start a HTTP server by
```
python -m SimpleHTTPServer
```

Open showplots.html in browser to change the JSON path, or specify with query string like
```
http://localhost:8000/path/to/showplots.html?path=plot-data/plots.json
```


