# MechaCar Statistical Analysis
The following analyses were performed in the R statistical programming language to evaluate the impact of various features of prototype mecha cars on their potential future performance, mileage per gallon of gasoline, as well as some other crucial factors, prior to deciding on mass production of said cars.

## Linear Regression to predict MPG

<p align="center">
  <img src="https://user-images.githubusercontent.com/99566803/171518870-f3e17f79-636c-440d-b898-556d74be39a2.png" />
</p>

Several deciding factors were examined against their influence on the MPG (miles per gallon) parameter to see which of the mecha car configurations have the best outcome for cars' gasoline consumption. From the above-provided screenshot, several conclusions can be made:

1. First, as can be seen, both the vehicle length and the ground clearance paratemeters had significant impact on the MPG statistic. In other words, there were particular car length and ground clearance configurations that had a non-random amount of variance to the MPG values. On the other hand, neither the vehicle weight, nor the spoiler angle or AWD, seemed to have an influence on the MPG.

2. Secondly, the slone of the linear model cannot be considered a zero, as the assosiated p-value = 5.35e-11, which, mathematically speaking, is smaller than a p-value of 0,05. In other words, the results of the linear regression are significant, and therefore the slope would not be a zero.

3. Lastly, the provided results indicate an r-value of 0.7149, meaning, in other words, that approximately 71,5% of the predictions examined would be representative and applicable to a predicted MPG model of the newly tested mecha cars. In that spirit, it is important to note that 28,5% of the predictions cannot be accounted for (and therefore, there is potential room for improvement in future mecha car tests).

## Summary Statistics on Suspension Coils

Overall Coil Suspension Summary
<p align="center">
  <img src="https://user-images.githubusercontent.com/99566803/171524444-b903cf84-9bef-4b3f-b7c8-dc12413d9ab6.png" />
</p>

Per Lot Coil Suspension Summary
<p align="center">
  <img src="https://user-images.githubusercontent.com/99566803/171524446-d6301c14-50da-4961-9146-c55af5d176aa.png" />
</p>

For the current analysis to make sense, it is imperative to provide some background information. That is, "the design specifications for the mecha car suspension  coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI)". In other words, the examined variance indicated above should not exceed a number of 100 in any of the examined analyses (neither in the total coil count, nor in the per lot investigation).
As can be seen from the overall coil suspension summary, the variance is registered at a 62,29 mark, meaning that the overall PSI on the suspension coils is well within the limits imposed by the company. When looking at the PSI variance readings separated by manufacturing lots, the picture becomes a bit messier: while Lot 1 and Lot 2 both behave in accordance with the company's expectations (Lot 1 has a variance = 0,97 and Lot 2 has a variance = 7,46), Lot 3 presents an extreme challenge, as it skews the overall data by excerting a variance of 170,28 PSI. That is nearly double the allowed PSI reading dictated by the company!
As such, one recommendations would be to investigate suspension coils in the Lot 3, in order to normalize the data and potentially identify the design flaws in the Lot 3 suspension coils.

## T-Tests on Suspension Coils

Overall T-Test Versus Population Mean
<p align="center">
  <img src="https://user-images.githubusercontent.com/99566803/171528575-8154abe9-87e8-4e61-965d-daf1591fbba9.png" />
</p>
As can be seen in the analysis above, with the provided t-statistic of -1,89 and p-value of 0.06, the overall suspension coils PSI is not significantly different from the population mean, as the p-value is higher (0,06) than the p-value that would allow one to reject the null hypothesis (0,05). That being said, nothing suggests that the mecha cars are any better in suspension coils PSI regulation than the other car brands.


Lot 1 T-Test Versus Population Mean
<p align="center">
  <img src="https://user-images.githubusercontent.com/99566803/171528712-1466e19c-6cdc-4070-a818-5304d6748795.png" />
</p>

Lot 2 T-Test Versus Population Mean
<p align="center">
  <img src="https://user-images.githubusercontent.com/99566803/171528731-b07eec80-0933-46ac-b967-d6c5ad04362b.png" />
</p>

Lot 3 T-Test Versus Population Mean
<p align="center">
  <img src="https://user-images.githubusercontent.com/99566803/171528751-1871dce5-889f-4efe-8191-d542b1c583a7.png" />
</p>
When looking at the potential differences between the mecha cars' suspension coils and the overall marker in more details, it seems that neither Lot 1 (p-value = 1), nor Lot 2 (p-value = 0.60) are significantly different from the population mean in the suspension coils PSI readings. Lot 3, however, shows promising result in that the p-value is 0.04, which is smaller than the p-value needed to reject the null hypothesis. In other words, Lot 3 is worth investigating, as it appears to be significantly different from the population mean (however, whether it's an inprovement or a downgrade remains to be investigated).
