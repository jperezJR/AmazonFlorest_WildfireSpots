# Project Wildfires in Amazon florest  

<p align="center">
 <img src=".\pictures\cnn-brazil-amazon-fires-2020.jpg" width="400" />
</p>
 

The main target of this notebook is to display the real location of fires of the last 24 hours in the Brazilian Amazon rainforest using satellite data from the Brazilian research space agency (INPE) API.




More information at: (https://queimadas.dgi.inpe.br/queimadas/dados-abertos)  (only in portuguese language :brazil: / :portugal:)


## Used Libs:


```
import json
import requests
import pandas as pd
import folium
from folium import plugins
```

## Usage

Right now, reading data is from a .json file stored at data/FiresLocation_Offline.json
It is using official data from INPE, but for test proposes and to avoid several API inquiries it was decided for it.

Only wildfires from Brazil are displayed now. But it is possible to show different South American countries from the list below:

<div align="center">

| **Countries** 	         |                    	|
|-------------------------|---------------------|
| Brasil :brazil:        	| Chile :chile:   	   |
| Bolivia :bolivia:  	    | Peru :peru:  	      |
| Venezuela :venezuela:   | Uruguay :uruguay:  	|
| Paraguay :paraguay:  	  | Ecuador :ecuador:  	|
| Argentina :argentina:   | Guyana :guyana:    	|
| Colombia :colombia:     |                    	|

</div>


 
First, a map with marks is generated pointing to where are the coordinates of the fire. Clicking on the marks will show you some more information as

- Coordinates
- Country
- State
- City
- Satellite 




Available satellite's data:

<div align="center">

| Satellites :artificial_satellite:	|            	|
|------------	|------------	|
| GOES-16    	| NOAA-18D   	|
| NPP-375    	| AQUA_M-M   	|
| NOAA-20    	| MSG-03     	|
| AQUA_M-T   	| NOAA-19    	|
| TERRA_M-T  	| TERRA_M-M  	|
| METOP-B    	|            	|

</div>
 
 


In the end, a heatmap can be visualized. It gives us a better understanding of where are the highest fires concentrations.



## Output

Overall wildfires map:


<p align="center">
  <img src=".\pictures\map_overall.png" width="400" />
</p>


Popup with fire information:

<p align="center">
  <img src=".\pictures\map_popupINFO.png" width="400" />
</p>


Heatmap:

<p align="center">
  <img src=".\pictures\heatmap.png" width="400" />
</p>



## Next steps / improvements

- Create a select box with available countries to auto-search.






## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


Thank you! ;)
:octocat: :v:



## License

:balance_scale: [MIT](https://choosealicense.com/licenses/mit/)
