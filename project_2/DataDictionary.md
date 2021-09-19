Ordinal Features
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**Lot Shape**|*int64*|train.csv|General Shape of property<br> 3: Regular<br> 2: Slightly Irregular<br> 1: Moderately Irregular<br> 0: Irregular|
|**Utilities**|*int64*|train.csv|Type of utilities available<br>3:	All public Utilities (E,G,W,& S)<br> 2:	Electricity, Gas, and Water (Septic Tank)<br> 1: Electricity and Gas Only<br> 0:	Electricity only<br>|
|**Land Slope**|*int64*|train.csv|Slope of property<br> 2: Gentle slope <br> 1: Moderate Slope <br> 0: Severe Slope <br>|
|**Overall Qual**|*int64*|train.csv|Rates the overall material and finish of the house<br> 10: Very Excellent<br>9: Excellent<br>8: Very Good<br>7: Good<br>6: Above Average<br>5: Average<br>4: Below Average<br>3: Fair<br>2: Poor<br>1: Very Poor<br>|
|**Overall Cond**|*int64*|train.csv|Rates the overall condition of the house<br>10: Very Excellent<br>9: Excellent<br>8: Very Good<br>7: Good<br>6: Above Average<br>5: Average<br>4: Below Average<br>3: Fair<br>2: Poor<br>1: Very Poor<br>|
|**Exter Qual**|*int64*|train.csv|Evaluates the quality of the material on the exterior<br>4: Excellent<br>3: Good<br>2: Average/Typical<br>1: Fair<br>0: Poor<br>|
|**Exter Cond**|*int64*|train.csv|Evaluates the present condition of the material on the exterior<br>4: Excellent<br>3: Good<br>2: Average/Typical<br>1: Fair<br>0: Poor<br>|
|**Bsmt Qual**|*int64*|train.csv|Evaluates the height of the basement<br>5: Excellent (100+ inches)<br>4: Good (90-99 inches)<br>3: Typical (80-89 inches)<br>2: Fair (70-79 inches)<br>1: Poor (<70 inches)<br>0: No Basement|
|**Bsmt Cond**|*int64*|train.csv|Evaluates the general condition of the basement<br>5: Excellent<br>4: Good<br>3: Typical - slight dampness allowed<br>2: Fair - dampness or some cracking or settling<br>1: Poor - Severe cracking, settling, or wetness<br>0: No Basement|
|**Bsmt Exposure**|*int64*|train.csv|Refers to walkout or garden level walls<br>4: Good Exposure<br>3: Average Exposure (split levels or foyers typically score average or above)<br>2: Mimimum Exposure<br>1: No Exposure<br>0: No Basement|
|**BsmtFin Type 1**|*int64*|train.csv|Rating of basement finished area<br>6: Good Living Quarters<br>5: Average Living Quarters<br>4: Below Average Living Quarters<br>3: Average Rec Room<br>2: Low Quality<br>1: Unfinshed<br>0: No Basement|
|**BsmtFin Type 2**|*int64*|train.csv|Rating of basement finished area (if multiple types)<br>6: Good Living Quarters<br>5: Average Living Quarters<br>4: Below Average Living Quarters<br>3: Average Rec Room<br>2: Low Quality<br>1: Unfinshed<br>0: No Basement|
|**Heating QC**|*int64*|train.csv|Heating quality and condition<br>4: Excellent<br>3: Good<br>2: Average/Typical<br>1: Fair<br>0: Poor|
|**Electrical**|*int64*|train.csv|Electrical system<br>4: Standard Circuit Breakers & Romex<br>3: Fuse Box over 60 AMP and all Romex wiring (Average)<br>2: 60 AMP Fuse Box and mostly Romex wiring (Fair)<br>1: 60 AMP Fuse Box and mostly knob & tube wiring (poor)<br>0: Mixed|
|**Kitchen Qual**|*int64*|train.csv|Kitchen quality<br>4: Excellent<br>3: Good<br>2: Average/Typical<br>1: Fair<br>0: Poor|
|**Functional**|*int64*|train.csv|Home functionality (Assume typical unless deductions are warranted)<br>7: Typical Functionality<br>6: Minor Deductions 1<br>5: Minor Deductions 2<br>4: Moderate Deductions<br>3: Major Deductions 1<br>2: Major Deductions 2<br>1: Severely Damaged<br>0: Salvage only|
|**Fireplace Qu**|*int64*|train.csv|Fireplace quality<br>5: Excellent - Exceptional Masonry Fireplace<br>4: Good - Masonry Fireplace in main level<br>3: Average - Prefabricated Fireplace in main living area or Masonry Fireplace in basement<br>2: Fair - Prefabricated Fireplace in basement<br>1: Poor - Ben Franklin Stove<br>0: No Fireplace|
|**Garage Finish**|*int64*|train.csv|Interior finish of the garage<br>3: Finished<br>2: Rough Finished<br>1: Unfinished<br>0: No Garage|
|**Garage Qual**|*int64*|train.csv|Garage quality<br>5: Excellent<br>4: Good<br>3: Typical/Average<br>2: Fair<br>1: Poor <br>0: No Garage|
|**Garage Cond**|*int64*|train.csv|Garage condition<br>5: Excellent<br>4: Good<br>3: Typical/Average<br>2: Fair<br>1: Poor <br>0: No Garage|
|**Paved Drive**|*int64*|train.csv|Paved driveway<br>2: Paved<br>1: Partial Pavement<br>0: Dirt/Gravel|
|**Pool QC**|*int64*|train.csv|Pool quality<br>4: Excellent<br>3: Good<br>2: Average/Typical<br>1: Fair<br>0: No Pool|
|**Fence**|*int64*|train.csv|Fence quality<br>4: Good Privacy<br>3: Minimum Privacy<br>2: Good Wood<br>1: Minimum Wood/Wire<br>0: No Fence|

Nominal
|Feature|Type|Dataset|Description|
|---|---|---|---|
**PID**|*int64*|train.csv||
**MS SubClass**|*int64*|train.csv||
**MS Zoning**|*object*|train.csv||
**Street**|*object*|train.csv||
**Alley**|*object*|train.csv||
**Land Contour**|*object*|train.csv||
**Lot Config**|*object*|train.csv||
**Neighborhood**|*object*|train.csv||
**Condition 1**|*object*|train.csv||
**Condition 2**|*object*|train.csv||
**Bldg Type**|*object*|train.csv||
**House Style**|*object*|train.csv||
**Roof Style**|*object*|train.csv||
**Roof Matl**|*object*|train.csv||
**Exterior 1st**|*object*|train.csv||
**Exterior 2nd**|*object*|train.csv||
**Mas Vnr Type**|*object*|train.csv||
**Foundation**|*object*|train.csv||
**Heating**|*object*|train.csv||
**Central Air**|*int64*|train.csv||
**Garage Type**|*object*|train.csv||
**Misc Feature**|*object*|train.csv||
**Sale Type**|*object*|train.csv||

Continuous
|Feature|Type|Dataset|Description|
|---|---|---|---|
**Lot Frontage**|*float64*|train.csv||
**Lot Area**|*int64*|train.csv||
**Mas Vnr Area**|*float64*|train.csv||
**BsmtFin SF 1**|*float64*|train.csv||
**BsmtFin SF 2**|*float64*|train.csv||
**Bsmt Unf SF**|*float64*|train.csv||
**Total Bsmt SF**|*float64*|train.csv||
**1st Flr SF**|*int64*|train.csv||
**2nd Flr SF**|*int64*|train.csv||
**Low  Qual  Fin  SF**|*int64*|train.csv||
**Gr Liv Area**|*int64*|train.csv||
**Garage Area**|*float64*|train.csv||
**Wood Deck SF**|*int64*|train.csv||
**Open Porch SF**|*int64*|train.csv||
**Enclosed Porch**|*int64*|train.csv||
**3Ssn Porch**|*int64*|train.csv||
**Screen Porch**|*int64*|train.csv||
**Pool Area**|*int64*|train.csv||
**Misc Val**|*int64*|train.csv||
**SalePrice**|*int64*|train.csv||


Discrete
|Feature|Type|Dataset|Description|
|---|---|---|---|
**Id**|*int64*|train.csv||
**Year Built**|*int64*|train.csv||
**Year Remod/Add**|*int64*|train.csv||
**Bsmt Full Bath**|*float64*|train.csv||
**Bsmt Half Bath**|*float64*|train.csv||
**Full Bath**|*int64*|train.csv||
**Half Bath**|*int64*|train.csv||
**Bedroom AbvGr**|*int64*|train.csv||
**Kitchen AbvGr**|*int64*|train.csv||
**TotRms AbvGrd**|*int64*|train.csv||
**Fireplaces**|*int64*|train.csv||
**Garage Yr Blt**|*float64*|train.csv||
**Garage Cars**|*float64*|train.csv||
**Mo Sold**|*int64*|train.csv||
**Yr Sold**|*int64*|train.csv||
