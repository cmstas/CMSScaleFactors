# Original locations of the files

## Run 2 UL
- wp_deepJet_106XUL16preVFP_v2.csv: https://twiki.cern.ch/twiki/pub/CMS/BtagRecommendation106XUL16preVFP/wp_deepJet_106XUL16preVFP_v2.csv
- wp_deepJet_106XUL16postVFP_v3.csv: https://twiki.cern.ch/twiki/pub/CMS/BtagRecommendation106XUL16postVFP/wp_deepJet_106XUL16postVFP_v3.csv
- wp_deepJet_106XUL17_v3.csv: https://twiki.cern.ch/twiki/pub/CMS/BtagRecommendation106XUL17/wp_deepJet_106XUL17_v3.csv
- wp_deepJet_106XUL18_v2.csv: https://twiki.cern.ch/twiki/pub/CMS/BtagRecommendation106XUL18/wp_deepJet_106XUL18_v2.csv

Notes:

- Per multiple threads in the BTV CMS Talk forum, e.g., https://cms-talk.web.cern.ch/t/a-possible-issue-in-the-b-tagging-correction-for-2016postvfp-with-wp-loose/18837/2,
one should use pre-VFP (APV) SFs on the post-VFP (NonAPV) MC. The post-VFP SFs were last updated on Jan. 25, 2022, so it is unclear whether the BTV POG cares at all!
- With respect to pre-UL, the csv input numbering convention seems to have changed. Specifically, for (pre-UL)->(UL), we have operatingPoint: (0, 1, 2, 3) -> ('L', 'M', 'T', 3), and jetFlavor: (B=0, C=1, UDSG=2) -> (B=5, C=4, UDSG=0). This means when one reads the csv files, one needs to adjust the BTagEntry::BTagEntry(const std::string &csvLine) constructor, and/or change the BTagEntry::JetFlavor enums (but this is really up to the user's liking). The change is traceable to this talk: https://indico.cern.ch/event/1096988/contributions/4615134/attachments/2346047/4000529/Nov21_btaggingSFjsons.pdf.
