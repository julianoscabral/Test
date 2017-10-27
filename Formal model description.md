# Formal description of an eco-evolutionary model to test LDG hypotheses

This is preliminary model description, roughly following the ODD protocol (Overview, Design concepts, and Details) for describing agent-based models (Grimm et al. 2006, 2010). Everybody is welcome to contribute, optimize description, write equations, sketch figures and write pseudocode (and correct anything wrong I wrote). This model description is intended to help Rampal's programmer to implement the model and run preliminary simulations until the next meeting in summer 2018. 

## Purpose
This model has a general purpose to unveil the misteries of biodiversity dynamics and their governing rules, on Earth and hopefully also on the entire universe. However, while we do not get there our more immediate purpose is to test hypotheses addressing the Latitudinal Gradient of Diversity (from now on LDG). Because we aim to address as many hypotheses as possible, the model needs to accordingly accomodate the processes, structure and properties necessary to integrate assumptions and to generate predicted patterns (beyond the LDG) evoked the various hypotheses. Most importantly, we discussed model properties with the general aim of defining a model that generates speciation as an emergent process (i.e. as a product of trait/niche divergence, which per se should be influenced by ecological, evolutionary and environmental processes).    

## Properties, state variables and scales:
The model is to be conceived as eco-evolutionary, spatially-explicit, niche-based, stochastic and whose agent is defined as local population, which per se belong to species: 
* Eco-evolutionary: Key processes to be included are interspecific (resource) competition, metapopulation dynamics (survival, extinction, emigration, immigration), gene flow, mutation, speciation. These processes are described in detail in the respective submodel section below. These processes should take place in most scenarios, but some scenarios (given by the experimental design for testing the hypotheses) may require switching off or varying some of these processes.
* Spatially-explicit: Generalized grid of cells, potentially in the rough shape of North/South America. Grid cells can be interpreted as buckets with different properties depending on the location in the grid, most notably depending on its latitude. Hence, the cell/bucket is an entity of the model, with following characteristics: location z within a grid depicting a latitudinal gradient; size, to be considered as a carrying capacity 'K_{z}' in terms of individuals and might depend on area/resource/productivity; and environmental variables (i.e. conditions; e.g. temperature). These characteristics may remain static, become dynamic or spatially-temporally variable depending on the simulation scenarios (to be defined in the Experimental Design section).
* Niche-based: Local populations Pz will have Gaussian distributions defining optimum, tolerance and for environmental conditions c (~ Grinellian Niche or Hutchinson's/Soberón's scenopoetic variable) and resources r (~ Eltonian Niche or Hutchinson's/Soberón's bionomic variable). We might discuss how we call these species' atributes (see also Rampal's trilogy papers on the niche in Journal of Biogegraphy), but this discussion is not central here. 
Niche(P_z)= {Gaussian(mean=Condition_optimum, sd=condition_tolerance), Gaussian(mean=Resource_optimum, sd=Resource_tolerance)}


## Experimental Design
This is still not discussed (probably on the second meeting). The experiments will largely depend on the hypotheses to test and, thus, on the perspective paper's diagrams. However, we more or less converged to start simulation by considering only one environmental condition (temperature) and one resource (given by e.g. productivity or NDVI). Species traits will be functional. Nevertheless, we might consider simulating more conditions, resources and neutral traits (these might be useful for non-adaptive divergence).

## References

[Grimm, V., Berger, U., Bastiansen, F., Eliassen, S., Ginot, V., Giske, J., ... & Huth, A. (2006). A standard protocol for describing individual-based and agent-based models. Ecological modelling, 198(1), 115-126.](http://www.sciencedirect.com/science/article/pii/S0304380006002043)

[Grimm, V., Berger, U., DeAngelis, D. L., Polhill, J. G., Giske, J., & Railsback, S. F. (2010). The ODD protocol: a review and first update. Ecological modelling, 221(23), 2760-2768.](http://www.sciencedirect.com/science/article/pii/S030438001000414X)
