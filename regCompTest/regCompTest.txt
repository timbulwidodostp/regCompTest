# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Compare Regression Models with Likelihood Ratio Test, AIC, and BIC Use regCompTest (flexCountReg) With (In) R Software
install.packages("flexCountReg")
library("knitr")
library("gt")
library("flexCountReg")
# Estimate Compare Regression Models with Likelihood Ratio Test, AIC, and BIC Use regCompTest (flexCountReg) With (In) R Software
regCompTest = read.csv("https://raw.githubusercontent.com/timbulwidodostp/regCompTest/main/regCompTest/regCompTest.csv", sep = ";")
regCompTest$AADTover10k <- ifelse(regCompTest$AADT>10000, 1, 0)
countreg <- countreg(Total_crashes ~ lnaadt + lnlength + speed50 + ShouldWidth04 + AADTover10k, data = regCompTest, family = 'NBP', method = 'NM', max.iters = 3000)
kable(summary(countreg), caption = "NB-2 Model Summary")
regCompTest <- regCompTest(countreg)
kable(regCompTest$statistics)
# Compare Regression Models with Likelihood Ratio Test, AIC, and BIC Use regCompTest (flexCountReg) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished