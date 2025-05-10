# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Anderson-Rubin (1949) Test Use AR.test (ivmodel) With (In) R Software
install.packages("ivmodel")
install.packages("plyr")
library("ivmodel")
AR.test = read.csv("https://raw.githubusercontent.com/timbulwidodostp/AR.test/main/AR.test/AR.test.csv",sep = ";")
# Estimation Anderson-Rubin (1949) Test Use AR.test (ivmodel) With (In) R Software
Y=AR.test[,"lwage"]
D=AR.test[,"educ"]
Z=AR.test[,"nearc4"]
Xname=c("exper", "expersq", "black", "south", "smsa", "reg661", "reg662", "reg663", "reg664", "reg665", "reg666", "reg667", "reg668", "smsa66")
X=AR.test[,Xname]
ivmodel = ivmodel(Y=Y,D=D,Z=Z,X=X)
AR.test <- AR.test(ivmodel)
AR.test
# Anderson-Rubin (1949) Test Use AR.test (ivmodel) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished