# Layout A 
job interview assignment by Yonatan Lev Ari

## Specification
1. Ratio between lead and default items is 3:1
1. Breakpoint at width 40rem
1. No media query
1. Visual referance is in the referance folder

## Development dependencies:
simple npm configuration with node sass


### Highlights
A simple html component with scss setup.  
This exercise demonstrate a flex based responsive layout without media queries. 

#### Expected beheviour: 
1. Layout container with two items
1. Items are stacked until a defined threshold (specified at 40rem). 
1. Beyond the threshold items are side by side with ratio of 3:1
1. ratio and breakpoint are configurable by mixin at the 'item' selector level.

## Styling methods: 
- scss with sass-lint configuration
- role based architecture
  - seperation between global and component scope.
  - configuration based for global and component scope.
  - style guide as a global definition layer
- BEM ,OOCSS.
- Component selectors are self containted and isolated.  
  - using global tokens for configuration
  - using global mixins and functions
- Utilized mixins and functions for selector indipendent future re-use.
- Rule based linting


### Styling dependencies: 
- Since i wanted to simulate a real use case i chose the seperate between the component to external layers.
- external layers for this example are:
  - global config (containing the style guide and semantic tokens, very minimalistic for this component example)
  - base layer (reset)
  - tools layer (mixins, functions, per this example they are on the same file, in larger project they will be seperated and loaded with _mixins, _functions loader via the utils loader)
  - altough i could easily avoid the mixin and function used here i belive it is good practise to assume global use for these usecases.

### Notes:
For this example css folder contains the final output in styles.css but also contains:  
- global.css  
- layout-a.css  
i did it so we can also bench mark standalone output. 
therfore these files are not prefixed with '_" (against the common practise).

#### Performance statistics:
External requests: 0  
Global Size: 90 bytes  
Component Size: 351 bytes  
Total: 442 bytes    
Lint Errors: 0
