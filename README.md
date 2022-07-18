# Battery-Capacity-Read
<ins>**Background**</ins>

One of the most important, expensive, and worrisome components of any electric vehicle is the high-voltage battery that propels the vehicle.  These batteries, although designed for long life, will deteriorate over time and affect vehicle range performance.  All manufacturers are required to provide a warranty for the HV batteries.  For the Clarity, this warranty is 8 years, 100K miles in most states.  It increases to 10 years, 150K miles if your vehice is registered and normally operated in California, Connecticut, Delaware, Maine, Maryland, Massachusetts, New Jersey, New York, Oregon, Pennsylvania, Rhode Island, Vermont, and Washington.

In the case of the Clarity, the specifics of the HV battery warranty are based on a capacity measurement  of the battery expressed in ampere-hours (Ah).  This warranty is spelled out in the pre-delivery checklist (17-093) that is supposed to be provided to all new owners.

The nominal battery capacity for a new vehicle is 55 Ah, and Honda define the elligability for warranty replacement as being 2/3 of the nominal capacity, or 36.6 aH.

[Here is where this is spelled out in the PDI checklist](https://clarity-phev.github.io/Battery-Capacity-Read/Pre-Delivery_Checklist.png)

Although it would have been trivial for Honda to make this important measurement available to owners through the infotainment center, or dashboard display, they have chosen not to do this.  Instead, they suggest that you must go to a dealer and have them read the value from the vehicle uing their i-HDS diagnostic tool.  We have found that most dealers are completely unaware of this, and we often need to provide them with this page from the PDI in order to educate them as to how this is done.  In addition, they will most often charge a fee (unless you happen to be there for other service anyway, and you are nice to them).

This is an unacceptible situation, and this repository will provide a several means to obtain this measurement yourself

<ins>**Accessing the Battery Capacity Yourself**</ins>

HV Battery Capacity is accessed through the OBDII connector which is located under the dashboard above your left leg.  This is the same connector that allows access to the vehicle computer systems for diagnostic testing as well as emissions inspections.  The OBDII connector contains provisions to access the vehicle’s Controller Area Network (CAN) bus.
  

<ins>**This repository identifies 3 ways to read the HV Battery Capacity from the Honda Clarity PHEV**</ins>

**Option 1 -**  The Autel AP200, with MaxAP200 App (and pre-authorized V2.01.54 Beta version of Honda Diagnostics)<br>
**Option 2 -**  A Proven 'good' ELM327 OBDII adapter with the Car Scanner App<br>
**Option 3 -**  A Proven 'good' ELM327 OBDII adapter with a PC or Laptop, generating a report format<br>

<ins>**Here is a summary of Pro's and Con's of these approaches**</ins>

|     | Cost | Comprehensive<br>Diagnostics|Speed|Live<br>Graphs|Formatted<br>Report|How-To<br>Instructions|InsideEEVS<br>Discussion |
| :-- | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| Option 1<br>Autel  | Med ($70) | Broad range<br>of vehicle<br>diagnostics | Slow | Marginal | Yes | [Instructions](https://clarity-phev.github.io/Battery-Capacity-Read/AP200_Instructions.pdf) | [Discussions](https://www.insideevsforum.com/community/index.php?threads/read-battery-capacity-yourself-autel-ap200-breakthrough.9913/) |
| Option 2<br>ELM327<br>Car Scanner  | Low ($30) | No | Fast | Yes |  No  | [Instructions](https://github.com/clarity-phev/Battery-Capacity-Read/ELM_CarScanner_Instructions.pdf) |[Discussions](https://www.insideevsforum.com/community/index.php?threads/budget-battery-capacity-readout.10531/) |
| Option 3<br>ELM327<br>PC  | Low ($30) | No | Fast | No  |  Yes | [Instructions](https://github.com/clarity-phev/powertrain_report/blob/main/How%20to%20Use.pdf) |[Discussions](https://www.insideevsforum.com/community/index.php?threads/pc-based-electric-powertrain-report-battery-capacity.12220/) |

<br><ins>**Which should I use ?**</ins>

* If you are an avid do-it-yourselfer, you my want to consider Option 1 because the Autel device provides a LOT of diagnostic information about all of the vehicle systems (not just the Electric Powertrain which contains the Battery Capacity)
   * Requires special request to Autel to authorize 2.02.54 Beta version of Honda diagnostics
   * Autel is sometimes not as responsive as we would like
* If you are a beginner and not so technically inclined, then Option 2 is recommented, and is easy enough that almost anyone can be successful with it.
* Once you are configured for Option 2, then you can also try Option 3 if you would like nicely formatted reports

* Many have both the AP200 and ELM327 setups because really the costs are very low

**Note -** There is LOT of discussion on the InsideEEVS pages for each approach (linked in the table above).  These discussions were evolutionary and sometimes highly technical.  This is part of the reason for this How-To guide. The original threads became far too cluttered for most to easily interpret.  They contain a lot of information, but hopefully this simplified How-To will be all you need to get started.  Feel free to post any comments and discussions in InsideEEVs.  There is a lot of help available there if you are having trouble.

<br>**Sharing of Battery Capacity Measurements**

In the interest of learning more about HV battery behavior, InsideEEVs forum members are cooperating and entering battery measurement data into a shared spreadsheet.  This will help identify trends and you can easily see if your Clarity is out of character with others.  You are encouraged to participate in this important effort, and you can get to the spreadsheet [HERE](https://docs.google.com/spreadsheets/d/1LHtqVuPzHUDXmX1jiHOQIpT_YiGp9N-vnBOiSz96C2I/edit#gid=1710145002)

<br>**Odd 'Resets' of Battery Capacity**

There have been some anomalies reported with the capacity readings
* We have seen a few examples where the battery capacity seems too good to be true.  Remember that a factory new battery is 54Ah.  In these instances, it seems like the reading continues to report 55Ah even as usage / mileage shoud reveal some degradation.  Either these owners are 'babying' the battery in some unknown way, or the reading is 'stuck' for some reason and doesn't reflect the actual capacity.

* We have also seem some examples where the battery capacity seems to get "reset" back to the factory setting.  In these cases, the capacity was slowly dropping as expected, and was at a 'reasonable' setting when suddenly it jumps up to 55Ah.  Something unknown causes this reset, after which it begins to return back to the 'normal' reading just before the reset.  The process of returning to 'normal' seems to take very long (months?).  We know that disconnecting the 12V battery for a breif period does **not** cause a battery capacity reset, but the speculation is that disconnecting the 12V battery for a 'prolonged' period might (maybe a day or more?).
