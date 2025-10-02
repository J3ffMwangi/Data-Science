# visitors_by_traffic_sources.py

import matplotlib.pyplot as plt
import numpy as np

# Data
months = ["07/2019", "08/2019", "09/2019", "10/2019", "11/2019"]
searches = [50, 53, 59, 56, 62]
direct = [39, 47, 42, 51, 51]
social_media = [70, 80, 90, 87, 92]

x = np.arange(len(months))  # the label locations
width = 0.25  # width of bars


fig, ax = plt.subplots(figsize=(8,5))

ax.bar(x - width, searches, width, label="Searches", color="royalblue")
ax.bar(x, direct, width, label="Direct", color="lightcoral")
ax.bar(x + width, social_media, width, label="Social Media", color="orange")



ax.set_ylabel("Visitors (in thousands)")
ax.set_xlabel("Months")
ax.set_title("Visitors by Web Traffic Sources")
ax.set_xticks(x)
ax.set_xticklabels(months)
ax.legend()

plt.tight_layout()
plt.show()
