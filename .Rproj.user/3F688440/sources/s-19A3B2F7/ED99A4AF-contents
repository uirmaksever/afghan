library(qss)
library(tidyverse)
library(sjPlot)

data("afghan")

View(afghan)
glimpse(afghan)
summary(afghan$educ.years)

prop.table(table(ISAF = afghan$violent.exp.ISAF, taliban = afghan$violent.exp.taliban))
sjt.xtab(afghan$violent.exp.ISAF,
         afghan$violent.exp.taliban,
         show.cell.prc = T,
         show.na = T)


afghan.sub <- na.omit(afghan)
head(afghan$income, n=8)

# Is there any NAs
mean(is.na(afghan$age))
mean(afghan$age)
# Remove NAs
mean(afghan$income, rm=T)

# Show freq on violent occasions
plot_frq(afghan$violent.exp.ISAF, show.na = T)
plot_frq(afghan$violent.exp.taliban, show.na = T)

# Histogram and density.
# Notice the difference between histogram and density when bin size changed
plot_frq(afghan$age, type="density", geom.size=5)
plot_frq(afghan$age, type="hist", geom.size=5)

hist(afghan$age)
