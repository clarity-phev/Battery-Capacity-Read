# Battery-Capacity-Read
This repository identifies 3 ways to read the HV Battery Capacity from the Honda Clarity PHEV

Option 1 -  The Autel AP200, with MaxAP200 App (and pre-authorized V2.01.54 Beta version of Honda Diagnostics)<br>
Option 2 -  A Proven 'good' ELM327 OBDII adapter with the Car Scanner App<br>
Option 3 -  A Proven 'good' ELM327 OBDII adapter with a PC or Laptop, generating a report format<br>

**Here is a summary of Pro's and Con's of these approaches**

|     | Cost | Comprehensive<br>Diagnostics|Speed|Live<br>Graphs|Formatted<br>Report|How-To<br>Instructions|InsideEEVS<br>Discussion |
| :-- | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| Option 1<br>Autel  | Med | Broad range<br>of vehicle<br>diagnostics | Slow | Marginal | Yes | [Instructions](https://github.com/clarity-phev/Battery-Capacity-Read/AP200.pdf) | [Discussions](https://www.insideevsforum.com/community/index.php?threads/read-battery-capacity-yourself-autel-ap200-breakthrough.9913/) |
| Option 2<br>ELM327<br>Car Scanner  | Low | No | Fast | Yes |  No  | [Instructions](https://github.com/clarity-phev/Battery-Capacity-Read/ELM_CarScanner.pdf) |[Discussions](https://www.insideevsforum.com/community/index.php?threads/budget-battery-capacity-readout.10531/) |
| Option 3<br>ELM327<br>PC  | Low | No | Fast | No  |  Yes | [Instructions](https://github.com/clarity-phev/Battery-Capacity-Read/ELM_PC.pdf) |[Discussions](https://www.insideevsforum.com/community/index.php?threads/pc-based-electric-powertrain-report-battery-capacity.12220/) |

**Which should I use ?**

* If you are an avid do-it-yourselfer, you my want to consider Option 1 because the Autel device provides a LOT of diagnostic information about all of the vehicle systems (not just the Electric Powertrain which contains the Battery Capacity)
   * Requires special request to Autel to authorize 2.02.54 Beta version of diagnostics
   * Autel is sometimes not as responsive as we would like
* If you are a beginner and not so technically inclined, then Option 2 is recommented
* Once you are configured for Option 2, then you can also try Option 3 if you would like nicely formatted reports

**Note -** There is LOT of discussion on the InsideEEVS pages for each approach (linked in the table above).  These discussions were evolutionary and sometimes highly technical.  This is part of the reason for this How-To guide. The original threads became far too cluttered for most to easily interpret.  They contain a lot of information, but hopefully this simplified How-To will be all you need to get started.  Feel free to post any comments and discussions in InsideEEVs.  There is a lot of help available there if you are having trouble.
