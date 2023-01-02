# Contents

Each folder corresponds to a POG:
- BTV for b-tagging and vertexing
- JME for JetMET
- LUM for Lumi
- EGM for EGamma
- MUO for Muon
- TAU for Tau.
This naming convention is hopefully the same as in https://gitlab.cern.ch/cms-nanoAOD/jsonpog-integration/-/tree/master/POG so that it is easier to match them. If not, feel free to rename them.

Each subfolder contains a README that lists the original location of the files, so it should be easy to trace any changes in prescription through twikis and various other repositories.

While BTV DeepFlavo(u)r b-tagger files are the only ones uploaded for now, feel free to upload files for other POGs or other taggers/IDs etc. File names are usually uniques, so there is no complicated folder structure for now.
A folder structure could allow links across github repositories in principle, but for a few files, wget from this repository could work just as fine.
Nevertheless, feel free to make adjustments as you feel necessary.

The suggestion would be to keep using csv or ROOT files until POGs decide to drop their support in favor of JSON files.
The reason is that the JSON files have a size of O(1 Mb) whereas csv/ROOT files are usually O(100 Kb), so
there is little motivation to bloat working directories with large JSON files that contain more than necessary information,
or to upload these files on Condor nodes for the hundreds of thousands of jobs we might be running in analyses.
