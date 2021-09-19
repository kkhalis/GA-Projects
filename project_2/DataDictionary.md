### Ordinal Features
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

### Nominal Features
|Feature|Type|Dataset|Description|
|---|---|---|---|
**PID**|*int64*|train.csv|Parcel identification number  - can be used with city web site for parcel review. |
**MS SubClass**|*int64*|train.csv|Identifies the type of dwelling involved in the sale.	<br>020: 1-STORY 1946 & NEWER ALL STYLES<br>030: 1-STORY 1945 & OLDER<br>040: 1-STORY W/FINISHED ATTIC ALL AGES<br>045: 1-1/2 STORY - UNFINISHED ALL AGES<br>050: 1-1/2 STORY FINISHED ALL AGES<br>060: 2-STORY 1946 & NEWER<br>070: 2-STORY 1945 & OLDER<br>075: 2-1/2 STORY ALL AGES<br>080: SPLIT OR MULTI-LEVEL<br>085: SPLIT FOYER<br>090: DUPLEX - ALL STYLES AND AGES<br>120: 1-STORY PUD (Planned Unit Development) - 1946 & NEWER<br>150: 1-1/2 STORY PUD - ALL AGES<br>160: 2-STORY PUD - 1946 & NEWER<br>180: PUD - MULTILEVEL - INCL SPLIT LEV/FOYER<br>190: 2 FAMILY CONVERSION - ALL STYLES AND AGES<br>|
**MS Zoning**|*object*|train.csv|Identifies the general zoning classification of the sale.<br>A: Agriculture<br>C: Commercial<br>FV: Floating Village Residential<br>I: Industrial<br>RH: Residential High Density<br>RL: Residential Low Density<br>RP: Residential Low Density Park<br>RM: Residential Medium Density|
**Street**|*object*|train.csv|Type of road access to property<br>Grvl: Gravel<br>Pave: Paved|
**Alley**|*object*|train.csv|Type of alley access to property<br>Grvl: Gravel<br>Pave: Paved<br>NA: No alley access|
**Land Contour**|*object*|train.csv|Flatness of the property<br>Lvl: Near Flat/Level<br>Bnk: Banked - Quick and significant rise from street grade to building<br>HLS: Hillside - Significant slope from side to side<br>Low: Depression<br>|
**Lot Config**|*object*|train.csv|Lot configuration<br>Inside: Inside lot<br>Corner: Corner lot<br>CulDSac: Cul-de-sac<br>FR2: Frontage on 2 sides of property<br>FR3: Frontage on 3 sides of property<br>|
**Neighborhood**|*object*|train.csv|Physical locations within Ames city limits (map available)<br>Blmngtn: Bloomington Heights<br>Blueste: Bluestem<br>BrDale: Briardale<br>BrkSide: Brookside<br>ClearCr: Clear Creek<br>CollgCr: College Creek<br>Crawfor: Crawford<br>Edwards: Edwards<br>Gilbert: Gilbert<br>Greens: Greens<br>GrnHill: Green Hills<br>IDOTRR: Iowa DOT and Rail Road<br>Landmrk: Landmark<br>MeadowV: Meadow Village<br>Mitchel: Mitchell<br>Names: North Ames<br>NoRidge: Northridge<br>NPkVill: Northpark Villa<br>NridgHt: Northridge Heights<br>NWAmes: Northwest Ames<br>OldTown: Old Town<br>SWISU: South & West of Iowa State University<br>Sawyer: Sawyer<br>SawyerW: Sawyer West<br>Somerst: Somerset<br>StoneBr: Stone Brook<br>Timber: Timberland<br>Veenker: Veenker<br>|
**Condition 1**|*object*|train.csv|Proximity to various conditions<br>Artery: Adjacent to arterial street<br>Feedr: Adjacent to feeder street<br>Norm: Normal<br>RRNn: Within 200' of North-South Railroad<br>RRAn: Adjacent to North-South Railroad<br>PosN: Near positive off-site feature--park, greenbelt, etc.<br>PosA: Adjacent to postive off-site feature<br>RRNe: Within 200' of East-West Railroad<br>RRAe: Adjacent to East-West Railroad<br>|
**Condition 2**|*object*|train.csv|Proximity to various conditions (if more than one is present)<br>Artery: Adjacent to arterial street<br>Feedr: Adjacent to feeder street<br>Norm: Normal<br>RRNn: Within 200' of North-South Railroad<br>RRAn: Adjacent to North-South Railroad<br>PosN: Near positive off-site feature--park, greenbelt, etc.<br>PosA: Adjacent to postive off-site feature<br>RRNe: Within 200' of East-West Railroad<br>RRAe: Adjacent to East-West Railroad|
**Bldg Type**|*object*|train.csv|Type of dwelling<br>1Fam: Single-family Detached<br>2FmCon: Two-family Conversion; originally built as one-family dwelling<br>Duplx: Duplex<br>TwnhsE: Townhouse End Unit<br>TwnhsI: Townhouse Inside Unit|
**House Style**|*object*|train.csv|Style of dwelling<br>1Story: One story<br>1.5Fin: One and one-half story: 2nd level finished<br>1.5Unf: One and one-half story: 2nd level unfinished<br>2Story: Two story<br>2.5Fin: Two and one-half story: 2nd level finished<br>2.5Unf: Two and one-half story: 2nd level unfinished<br>SFoyer: Split Foyer<br>SLvl: Split Level|
**Roof Style**|*object*|train.csv|Type of roof<br>Flat: Flat<br>Gable: Gable<br>Gambrel: Gabrel (Barn)<br>Hip: Hip<br>Mansard: Mansard<br>Shed: Shed<br>|
**Roof Matl**|*object*|train.csv|Roof material<br>ClyTile: Clay or Tile<br>CompShg: Standard (Composite) Shingle<br>Membran: Membrane<br>Metal: Metal<br>Roll: Roll<br>Tar&Grv: Gravel & Tar<br>WdShake: Wood Shakes<br>WdShngl: Wood Shingles|
**Exterior 1st**|*object*|train.csv|Exterior covering on house<br>AsbShng: Asbestos Shingles<br>AsphShn: Asphalt Shingles<br>BrkComm: Brick Common<br>BrkFace: Brick Face<br>CBlock: Cinder Block<br>CemntBd: Cement Board<br>HdBoard: Hard Board<br>ImStucc: Imitation Stucco<br>MetalSd: Metal Siding<br>Other: Other<br>Plywood: Plywood<br>PreCast: PreCast<br>Stone: Stone<br>Stucco: Stucco<br>VinylSd: Vinyl Siding<br>Wd Sdng: Wood Siding<br>WdShing: Wood Shingles|
**Exterior 2nd**|*object*|train.csv|Exterior covering on house (if more than one material)<br>AsbShng: Asbestos Shingles<br>AsphShn: Asphalt Shingles<br>BrkComm: Brick Common<br>BrkFace: Brick Face<br>CBlock: Cinder Block<br>CemntBd: Cement Board<br>HdBoard: Hard Board<br>ImStucc: Imitation Stucco<br>MetalSd: Metal Siding<br>Other: Other<br>Plywood: Plywood<br>PreCast: PreCast<br>Stone: Stone<br>Stucco: Stucco<br>VinylSd: Vinyl Siding<br>Wd Sdng: Wood Siding<br>WdShing: Wood Shingles|
**Mas Vnr Type**|*object*|train.csv|Masonry veneer type<br>BrkCmn: Brick Common<br>BrkFace: Brick Face<br>CBlock: Cinder Block<br>None: None<br>Stone: Stone|
**Foundation**|*object*|train.csv|Type of foundation<br>BrkTil: Brick & Tile<br>CBlock: Cinder Block<br>PConc: Poured Contrete<br>Slab: Slab<br>Stone: Stone<br>Wood: Wood|
**Heating**|*object*|train.csv|Type of heating<br>Floor: Floor Furnace<br>GasA: Gas forced warm air furnace<br>GasW: Gas hot water or steam heat<br>Grav: Gravity furnace<br>OthW: Hot water or steam heat other than gas<br>Wall: Wall furnace|
**Central Air**|*int64*|train.csv|Central air conditioning<br> N: No<br>Y: Yes|
**Garage Type**|*object*|train.csv|<br>2Types: More than one type of garage<br>Attchd: Attached to home<br>Basment: Basement Garage<br>BuiltIn: Built-In (Garage part of house - typically has room above garage)<br>CarPort: Car Port<br>Detchd: Detached from home<br>NA: No Garage|
**Misc Feature**|*object*|train.csv|Miscellaneous feature not covered in other categories<br>Elev: Elevator<br>Gar2: 2nd Garage (if not described in garage section)<br>Othr: Other<br>Shed: Shed (over 100 SF)<br>TenC: Tennis Court<br>NA: None|
**Sale Type**|*object*|train.csv|Type of sale<br>WD: Warranty Deed - Conventional<br>CWD: Warranty Deed - Cash<br>VWD: Warranty Deed - VA Loan<br>New: Home just constructed and sold<br>COD: Court Officer Deed/Estate<br>Con: Contract 15% Down payment regular terms<br>ConLw: Contract Low Down payment and low interest<br>ConLI: Contract Low Interest<br>ConLD: Contract Low Down<br>Oth: Other|

### Continuous Features
|Feature|Type|Dataset|Description|
|---|---|---|---|
**Lot Frontage**|*float64*|train.csv|Linear feet of street connected to property|
**Lot Area**|*int64*|train.csv|Lot size in square feet|
**Mas Vnr Area**|*float64*|train.csv|Masonry veneer area in square feet|
**BsmtFin SF 1**|*float64*|train.csv|Type 1 finished square feet|
**BsmtFin SF 2**|*float64*|train.csv|Type 2 finished square feet|
**Bsmt Unf SF**|*float64*|train.csv|Unfinished square feet of basement area|
**Total Bsmt SF**|*float64*|train.csv|Total square feet of basement area|
**1st Flr SF**|*int64*|train.csv|First Floor square feet|
**2nd Flr SF**|*int64*|train.csv|Second floor square feet|
**Low Qual Fin SF**|*int64*|train.csv|Low quality finished square feet (all floors)|
**Gr Liv Area**|*int64*|train.csv|Above grade (ground) living area square feet|
**Garage Area**|*float64*|train.csv|Size of garage in square feet|
**Wood Deck SF**|*int64*|train.csv|Wood deck area in square feet|
**Open Porch SF**|*int64*|train.csv|Open porch area in square feet|
**Enclosed Porch**|*int64*|train.csv|Enclosed porch area in square feet|
**3Ssn Porch**|*int64*|train.csv|Three season porch area in square feet|
**Screen Porch**|*int64*|train.csv|Screen porch area in square feet|
**Pool Area**|*int64*|train.csv|Pool area in square feet|
**Misc Val**|*int64*|train.csv|$Value of miscellaneous feature|
**SalePrice**|*int64*|train.csv|Sale price $$|


### Discrete Features
|Feature|Type|Dataset|Description|
|---|---|---|---|
**Id**|*int64*|train.csv|Observation number|
**Year Built**|*int64*|train.csv|Original construction date|
**Year Remod/Add**|*int64*|train.csv|Remodel date (same as construction date if no remodeling or additions)|
**Bsmt Full Bath**|*float64*|train.csv|Basement full bathrooms|
**Bsmt Half Bath**|*float64*|train.csv|Basement half bathrooms|
**Full Bath**|*int64*|train.csv|Full bathrooms above grade|
**Half Bath**|*int64*|train.csv|Half baths above grade|
**Bedroom AbvGr**|*int64*|train.csv|Bedrooms above grade (does NOT include basement bedrooms)|
**Kitchen AbvGr**|*int64*|train.csv|Kitchens above grade|
**TotRms AbvGrd**|*int64*|train.csv|Total rooms above grade (does not include bathrooms)|
**Fireplaces**|*int64*|train.csv|Number of fireplaces|
**Garage Yr Blt**|*float64*|train.csv|Year garage was built|
**Garage Cars**|*float64*|train.csv|Size of garage in car capacity|
**Mo Sold**|*int64*|train.csv|Month Sold (MM)|
**Yr Sold**|*int64*|train.csv|Year Sold (YYYY)|
