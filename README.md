
# An individual household electric power consumption
## Objectives

This study has the objective to evaluate the reactive power consumption versus the active power consumption based on the available data. Note that currently, households are not charged for the reactive power that they consume from the energy grid, only for the active power.

This study will try to evaluate if the reactive power consumption is already in critical levels, or if it will be cause of concerns in the future.

## About the Data
### Origin

The data was downloaded from the UCI Machine Learning Repository (link in the references). It contains "measurements gathered in a house located in Sceaux (7km of Paris, France) between December 2006 and November 2010 (47 months)."
Business Problem

While billing for residences is usually done considering only the active power (Watts), households can also consumes reactive power (also known as the useless power) from the energy grid. Usually the amount of reactive power consumed from the grid is only a fraction of the active power (less than 5% in most cases), so the power distribution company do not have to worry about it. But how it´s changing over the years? Today we have more eletronics with capacitors, induction heating systems and even wireless power transfers, all of those spending more reactive energy.

This study will look at the consumption of this single household over the years to try to understand if there is any trend in it´s consumption and if it´s necessary to change the billing system to account for the reactive power or not.
### Volume of Data

This dataset contains 2.075.259 measurements, for 47 months between December 2006 and November 2010
### Data Dictionary

    1.date: Date in format dd/mm/yyyy  
    2.time: time in format hh:mm:ss
    3.global_active_power: household global minute-averaged active power (in kilowatt)
    4.global_reactive_power: household global minute-averaged reactive power (in kilowatt) *Note*: We are assuming that´s in kVAR instead of kW
    5.voltage: minute-averaged voltage (in volt)
    6.global_intensity: household global minute-averaged current intensity (in ampere)
    7.sub_metering_1: energy sub-metering No. 1 (in watt-hour of active energy). It corresponds to the kitchen, containing mainly a dishwasher, an oven and a microwave (hot plates are not electric but gas powered).
    8.sub_metering_2: energy sub-metering No. 2 (in watt-hour of active energy). It corresponds to the laundry room, containing a washing-machine, a tumble-drier, a refrigerator and a light.
    9.sub_metering_3: energy sub-metering No. 3 (in watt-hour of active energy). It corresponds to an electric water-heater and an air-conditioner.

Notes
    1.(global_active_power*1000/60 - sub_metering_1 - sub_metering_2 - sub_metering_3) represents the active energy consumed every minute (in watt hour) in the household by electrical equipment not measured in sub-meterings 1, 2 and 3.
    2.The dataset contains some missing values in the measurements (nearly 1,25% of the rows). All calendar timestamps are present in the dataset but for some timestamps, the measurement values are missing: a missing value is represented by the absence of value between two consecutive semi-colon attribute separators. For instance, the dataset shows missing values on April 28, 2007.
    
### Assumptions
Since kilowatts are NOT used to represent reactive power, we are assuming that the unit of global_reactive_power is kVAR.   
The reactive power measured is obtained from the power grid, increasing costs for the energy company.

### References

Original data available at: https://archive.ics.uci.edu/ml/datasets/Individual+household+electric+power+consumption

About Active and Reactive Power https://aperc.gov.in/admin/upload/151340198613587660935a34ae822cf4c.pdf

https://www.electricaltechnology.org/2019/08/difference-between-active-and-reactive-power.html

https://www.allaboutcircuits.com/textbook/alternating-current/chpt-11/true-reactive-and-apparent-power/

https://en.wikipedia.org/wiki/AC_power

https://integratedelectronics.blog/knowledge-base/why-there-is-no-reactive-power-in-dc/

https://www.fluke.com/en-us/learn/blog/power-quality/power-factor-formula
