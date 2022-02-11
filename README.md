# Crowd-Computing
#Taking the people's assumption as values and comparing with original.

import matplotlib.pyplot as plt

import statistics

estimates = [1001,1000,2891,1202,1002,1015,1017,1000,1060,2012,2010,2017,1113,1114,1105]

#estimates are the answers of public

estimates.sort()

print(estimates)

tv = int(0.1 * len(estimates))     #trim value(tv) - triming first & last 10 percentage.

estimates = estimates[tv:]          

print(estimates)

estimates = estimates[: (len(estimates) - tv)]

print(estimates)


y = []          

for i in range(len(estimates)):
    y.append(5)                     #taking y values 5 for straight line.
    
plt.plot([1202],[5],"bs")           #Original value

plt.plot(estimates,y,"r--")

plt.plot(statistics.mean(estimates),[5],'g^')

plt.plot(statistics.median(estimates),[5],'ro')
