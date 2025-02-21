# p1-project-ck- Aviation Accident
## Business understanding

## Background
As part of our strategic initiative to diversify our company's portfolio, we are venturing into the aviation industry. This expansion involves purchasing and operating airplanes for both commercial and private enterprises. Given the high stakes associated with aviation, understanding the potential risks and ensuring the highest standards of safety is paramount for the success and sustainability of this new business endeavor.

## Objective
My primary objective is to identify the aircraft models that present the lowest risk in terms of safety and operational reliability. This involves a comprehensive analysis of historical aviation accident data to evaluate the safety performance of various aircraft manufacturers and models. The goal is to provide actionable insights that will guide the decision-making process for the acquisition of aircraft, ensuring that we select models with proven safety records.

## Data Understanding
[Aviation Accident Database & Synopses, up to 2023](https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses/code)
To achieve this objective, I have utilized the National Transportation Safety Board (NTSB) dataset, which includes detailed information on civil aviation accidents from 1962 to 2023. The analysis focuses on key metrics such as fatality rates, injury rates, and the number of uninjured passengers and crew in accidents. These metrics are crucial for assessing the overall safety performance of different aircraft models.

The decision on which aircraft to purchase will be based on the following criteria derived from our analysis:

Uninjured Rate - The proportion of passengers and crew who remain uninjured in the event of an accident.
Fatality Rate - The number of fatalities per accident involving the aircraft.
Variety and Availability - The range of models available from the manufacturer and their suitability for our intended operations i.e. commercial and private travel.
Data Cleaning Process
Ensuring the quality and consistency of our data is paramount. I undertook the following data cleaning steps to prepare the dataset for analysis:

Checking for Duplicates: My first step was to check for duplicate values in the dataset. Ensuring the uniqueness of our records is crucial to avoid skewed results. This check however found that the dataset does not contain any duplicate entries.

Cleaning Column Names: To make the dataset easier to work with, I standardized our column names. I replaced dots with underscores and capitalized the first letter of each word. This makes the column names more readable and easier to work with in our code.

Cleaning 'Model' Column Values: To ensure consistency, I've converted all values in this column to strings. Additionally, I replaced spaces with hyphens to avoid any potential issues with spaces in our data.

## Data Reduction
In this analysis, I aim to focus on the most relevant data to enable making of informed recommendations. As such, I have decided to perform data reduction by dropping certain columns from this dataset. This step will simplify our data and make it easier to handle, without losing the information that is crucial to our analysis.

The columns I dropped are:

Latitude: While geographical data could be interesting in some analyses, our focus does not require the specific latitude of accidents.
Longitude: Similar to Latitude, Longitude is not necessary for the current analysis.
Schedule: The schedule of the flight does not contribute significantly to the analysis of injury rates and safety features.
Air_Carrier: This analysis is focused on aircraft manufacturers rather than air carriers.
Aircraft_Category: We are looking at specific aircraft models in our analysis, making the broader category less relevant.
Far_Description: This column contains regulatory info that is not directly related to our analysis.
By reducing our data in this way, I can focus more closely on the factors that are most relevant to this project. This will help draw more accurate conclusions and help me make meaningful recommendations to present to the new aviation honcho.

## Data Subsetting by Aircraft Manufacturer
In this analysis, I am particularly interested in the most common passenger plane manufacturers. To focus our analysis, I have created a subset of our data, top_10_makes, which includes only the aircrafts made by the top 10 manufacturers according to Investopedia and AeroTime Hub.

<img src="images/make.png" alt="aircraft make" width="650" height="450">

I've standardized the names of these manufacturers in the dataset to ensure consistency. The top 10 manufacturers I've included are:

Boeing
Airbus
Bombardier
Embraer
Cessna
Dassault
Pilatus
Hawker
Gulfstream
Mitsubishi
I've excluded military aircraft manufacturers like Lockheed Martin and Northrop Grumman, as well as some Russian and Chinese manufacturers due to their limited numbers in the dataset. My focus is on manufacturers of passenger planes, as this is most relevant to our expansion into the aviation industry. By focusing on these top manufacturers, we can gain a more accurate understanding of the trends and factors that impact safety in the majority of passenger aircrafts.

## Limitations
Missing Values - Significant portions of the data are missing in many columns. Missing data can lead to biased or incomplete analysis. For instance, missing information about the location or aircraft category might not reveal important patterns related to accident frequency or severity.
Incomplete Data on Injuries - The columns Total.Fatal.Injuries, Total.Serious.Injuries, Total.Minor.Injuries, and Total.Uninjured have many missing values. Without complete injury data, it's challenging to accurately assess the safety of different aircraft models. The risk assessment might be skewed if severe accidents are underreported or missing.

<img src="images/injuries.png" alt="aircraft make" width="650" height="450">

Lack of Contextual Information - The dataset doesn't include detailed information on operational factors such as maintenance records, pilot experience, or specific environmental conditions at the time of the accident. These factors are crucial in understanding the full context of accidents and making informed recommendations. Without this data, this analysis may have overlooked critical contributors to aviation safety.
Historical Nature of Data - The dataset spans from 1962 to 2023. Aviation technology, regulations, and practices have evolved significantly over this long period. Old data might not be as relevant to current aircraft models and technologies. Trends observed in old data might not accurately reflect current safety standards.

## Aircraft Selection for Private and Commercial Divisions
I've narrowed down our choices to Bombardier for our private division and Embraer for the commercial division. This decision was based on their low fatality rate and high uninjured rate.

<img src="images/fatality_make.png" alt="aircraft make" width="650" height="450">

## Model Analysis
Upon analyzing the models, we first narrowed down to aircraft models that had a 100% uninjured rate. I then determined the most popular aircraft model by counting how many entries each of the models had in the data. The CL-600 had the highest count. Although this dataset does not have a record of all flights, I'm assuming the CL-600 has the highest number of occurrences due to its popularity. This assumption is supported by the fact that the Bombardier aircrafts are proven to be safe, and all accidents with this model have a 100% uninjured rate.

## Engine Number Analysis
I also did an analysis by engine number. However, since all major manufacturers have moved away from 4 and 3 engine models to 2 engine models, I figured this shouldn't be an issue anyway.

## Recommendations

Based on this analysis, I am recommending the Airbus 320 for our commercial division and Bombardier CL-600 for our private division.

It's worth noting that although Boeing has a slightly lower fatality rate of 0.0559 compared to Bombardier's slightly higher 0.0588 rate, I've chosen not to recommend Boeing due to the recent revelations that they've been lax on quality control, and the recent Alaska Airlines door blowout.

By making these informed decisions, we aim to ensure the safety of our passengers and crew as we expand into the aviation industry.

For a thorough analysis of this dataset, check out this [Tableau Dashboard](https://public.tableau.com/app/profile/caroline.kamusi/viz/AviationAccidents_17185334724950/AviationAccidentDashboard?publish=yes)
