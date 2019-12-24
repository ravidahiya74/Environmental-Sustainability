# Why Environmental Sustainability?

Environmental sustainability is concerned with whether environmental resources will be protected and maintained for future generations.Environmental sustainability is concerned with issues such as:
* Long-term health of ecosystems. Protecting the long-term productivity and health of resources to meet future economic and social needs, e.g. protecting food supplies, farmland and fishing stocks.
* Intergenerational decision making. When making economic decisions, we should focus on implications for future generations, and not just the present moment. For example, burning coal gives a short-term benefit of cheaper energy, but the extra pollution imposes costs on future generations.
* Renewable resources: Diversifying into energy sources that do not rely on non-renewable resources. For example, solar and wind power.
* Prevent the consequences of man-made global warming. Policies to ensure the environment of the planet does not deteriorate to a point where future generations face water shortages, extreme weather events, excess temperature. – All factors that could make living in parts of the world very difficult if not possible.
* Protection of species diversity and ecological structure. Sometimes medicines require elements within specific plant species. If some species go extinct, it limits future technological innovation.
* Treating environmental resources as if they have intrinsic rights and value. In other words, we shouldn’t just rely on a monetary value, i.e. we should protect rainforests because they deserve to be protected rather than using a cost-benefit analysis of whether we gain financially from protecting rainforests.
* Targetting social welfare/happiness and environmental sustainability above crude measures of progress such as GDP. 
<img src="images\image1.jpg">

# Human Development Report Data

United Nations Development Program publishes Human Development Report that collects data from various sources pertaining to Human Development. It captures various parameters such as <b>'quality of human development'</b>, <b>'gender gap'</b>, <b>'women empowerment'</b>, <b>'environment sustainability'</b> and many more. Please check out the latest report [here](http://report.hdr.undp.org/?utm_source=web&utm_medium=homepage&utm_campaign=hdr19).

# Enviormental Performance Index
<img src="images\image2.png">

#####  Source - Environmental Performance Index (EPI) designed to supplement the environmental targets set forth in the United Nations Millennium Development Goals.

The map depicts the environmental performance of the countries on a scale of 0 to 100. We will try to use <b>Unsupervised Deep Learning</b> technique to organise the countries using <b>Human Development Report Data</b> and try to compare the results.


# Unsupervised Deep Learning (Self Organising Maps)

A self-organizing map (SOM) is a type of artificial neural network (ANN) that is trained using unsupervised learning to produce a low-dimensional (typically two-dimensional), discretized representation of the input space of the training samples, called a map, and is therefore a method to do dimensionality reduction. Self-organizing maps differ from other artificial neural networks as they apply competitive learning as opposed to error-correction learning (such as backpropagation with gradient descent), and in the sense that they use a neighborhood function to preserve the topological properties of the input space.


# Building the CSV file

* Step-1: Slicing the relevant data from the 'Human Development Report-2018' and converting it to csv file
* Step-2: Adding the pollution index from [here](https://www.numbeo.com/pollution/rankings_by_country.jsp) to the csv file using webscrapping tools in pandas.
* Step-3: Adding country code to the csv file that will be used to plot choropleth map using plotly

# Describing the Columns

* Fossil_fuel_usage: Percentage of total energy consumption that comes from fossil fuels, which consist of coal, oil, petroleum and natural gas products.
* Renewable_energy_usage: Share of renewable energy in total final energy consumption. Renewable sources include hydroelectric, geothermal, solar, tides, wind, biomass and biofuels.
* Per_capita_CO2: Human-originated carbon dioxide emissions stemming from the burning of fossil fuels, gas flaring and the production of cement. Carbon dioxide emitted by forest biomass through depletion of forest areas is included. Data are expressed in tonnes per capita (based on midyear population)
* Forest_area: Land spanning more than 0.5 hectare with trees taller than 5 metres and a canopy cover of more than 10 percent or trees able to reach these thresholds in situ. It excludes land predominantly under agricultural or urban land use, tree stands in agricultural production systems (for example, in fruit plantations and agroforestry systems) and trees in urban parks and gardens. Areas under reforestation that have not yet reached but are expected to reach a canopy cover of 10 percent and a tree height of 5 metres are included, as are temporarily unstocked areas resulting from human intervention or natural causes that are expected to regenerate.
* fresh_water_withdrawl: Total fresh water withdrawn, expressed as a percentage of total renewable water resources.
* natural_resource_reduction: Monetary valuation of energy, mineral and forest depletion, expressed as a percentage of gross national income (GNI).
* air_pollution_deaths_per_100000: Age-standardized mortality rate resulting from exposure to ambient (outdoor) air pollution and household (indoor) air pollution from solid fuel use for cooking, expressed per 100,000 population. Ambient air pollution results from emissions from industrial activity, households, cars and trucks."
* water_related_deaths_per_100000: Mortality rate attributed to unsafe water, sanitation and hygiene services: Deaths attributable to unsafe water, sanitation and hygiene focusing on inadequate wash services, expressed per 100,000 population.
* land_degradation: Rain fed cropland, irrigated cropland, or range, pasture, forest and woodlands that have experienced the reduction or loss of biological or economic productivity and complexity resulting from a combination of pressures, including land use and management practices.
* red_list_index: Measure of the aggregate extinction risk across groups of species. It is based on genuine changes in the number of species in each category of extinction risk on the International Union for Conservation of Nature Red List of Threatened Species. It ranges from 0, all species categorized as extinct, to 1, all species categorized as least concern.
* Pollution Index: Air quality score. Higher the score, worse is the air quality

# Results
As we can see that environmental performance is lowest among countries like India, Pakistan, Nigeria, Yemen, Saudi Arabia, Congo and other African countries. Countries like Canada, US, Brazil, Australia and West Europian countries are perfoming well on the sustainability index. We can compare the results wit the Enviormental Performance Index we see that our model produces similar results.
### Results from the model
<img src="images\image3.png">

### Results from Environmental Performance Index
<img src="images\image2.png">






