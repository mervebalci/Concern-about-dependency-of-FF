# Concern-about-dependency-of-FF
# Which factors affect the concern about dependency on fossil fuels in 6 European countries
# Descriptive Statistics - SPSS&STATA
# Ordered Logistic Regression without Left-Right Scale: Model-1
ologit wrdpfos1 agea eduyrs female havechildren married separated middlereligiosity highreligiosity small city livingcomfortably copingon if (cntry=="SE" & lrscale<11), robust
# Repeat it for each countries to see;
Log pseudolikehood
Number of obs
Prob > chi2
Pseudo R2
margins, dydx(*) predict(outcome(1))
Average marginal effects
Model VCE : Robust
Expression: Pr(wrdpfos==1), predict(outcome(1))
dy/dx w.r.t. : agea eduyrs female havechildren married separated middlereligiosity highreligiosity small city livingcomfortably copingon
#Ordered Logistic Regression with Left-Right Scale: Model 2
bysort cntry: ologit wrdpfos1 eduyrs agea female male eduyrs married  separated single havechildren nothavechildren highreligiosity notreligious middlereligiosity livingcomfortably copingon difficultonpresent bigcity smallcity village lrscale if [lrscale<77] ,vce(robust)
	N	Min	Max	Mean	Std. Deviation
Concern about dependency of fossil fuels	
N:42569	
Min:1	
Max:5	
Mean:2.92	
Std. Deviation: 1,016
summarize wrdpfos1 lrscale agea gndr1 chldhm1 maritalb1 rlgdgr1 domicil1 wrdpfos1
tab wrdpfos1 hincfel, chi2 #Repeat for each variable

