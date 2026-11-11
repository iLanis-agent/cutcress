# Cutcress 1.0 TEST
Native Android weighted maximum-cut puzzle. Android8+ min26/target35. Package com.gg007.cutcress.

## Rules
Put every node A-H on LEFT or RIGHT. Each row lists its neighbors with edge weights: B 4 means a link to B with weight 4. Links are undirected, listed at both endpoints, but count each link only once. Earn its weight only when its two ends are on opposite sides. Same-side links earn zero and are allowed. Tap B-H rows to switch sides, then CHECK CUT. Maximize the total crossing weight. No equal-size or connectivity requirement. A stays LEFT only to avoid duplicate mirror splits; this does not change the best possible weight. Twelve original graphs, one best split each with A fixed. Each has a suboptimal split that no single node flip improves, so local improvement can get stuck. Weights are puzzle points, not money. Undo/reset and saved palette/optional node numbers.

## Download and status
https://mega.co.nz/#!IAFmBJgK!e7y55sAfY982o8sjAfXAce5CGE_zFAx8HWer3AZKjf0
APK20974bytes; SHA2562d74d2c1ed1c04bccfab0d2916bac83fb5f78d940786eaa24892bbb62ed47298. Original certificate SHA2561651d9e269ece8a76f36ed4bba24ebc50f9de1e5f856e0567e0e8169fcb25597. No requested permissions. GG007 icon unchanged. Anonymous downloaded bytes exact.

## Checks
Independent all-partition enumeration checks 3072 scores and complement symmetry against production cross-side scoring, plus 1536 pinned boards against recursive incremental edge accounting. Another 2000 random graphs and 10752 toggle/undo/clear cases pass. Every original graph has a unique pinned optimum and a worse one-flip local trap. Empty/single/edgeless/single-edge/triangle/complete/ties/bounds/symmetricweight cases pass. Twelve actual side-toggle/CHECK optimum tap-solves, all-left/all-right-pinned/local-trap rejection, fixed-A, clear/undo/reset, solved locks, NEXT, levels/menu/privacy and saved palette/node numbers pass. Twenty drawing previews visually inspected, not phone screenshots. Original signing certificate/icon unchanged, no permissions. Anonymous APK bytes match. Phone runtime/performance/external-browser QA and full Git source commit remain incomplete. Signed TEST, not final or Play published.

## Functional difference
Current 243 studio descriptions and 803 legacy descriptions reviewed. Chromaring properly colors every linked pair; Guardcress selects compatible vertices and forbids any internal link. Flowcress maximizes directed source-to-sink flow under capacity/conservation. Cutcress instead assigns every vertex to one of two sides, allows same-side links and maximizes the total undirected edge weight crossing sides. No color-validity, chosen-subset, source/sink, equal-size or flow requirement. No matching factory mechanic found. Known weighted maximum-cut adaptation, not a globally new algorithm. Original seeded graph weights, native implementation and weighted-link side-toggle interaction.

## Build and tests
JDK17/AndroidSDK35/build-tools35.0.0. python generate-levels.py reproduces levels.json. javac -d /tmp/mint-test src/com/gg007/cutcress/Board.java BoardTest.java then java -cp /tmp/mint-test com.gg007.cutcress.BoardTest. bash build.sh produces an unsigned aligned APK unless KEYSTORE_PATH and KEYSTORE_PASSWORD_FILE point to private signing material. No signing secret included. adapter/android is the Java2D drawing adapter used with CutAdapterTest.java, not an Android runtime.

## Privacy and branding
Cutcress runs offline without accounts, ads, analytics, third-party SDKs or requested permissions. Palette, node-number labels and solved-level marks stay in this app on your device. Clear app data or uninstall to remove them. The studio link opens your external browser.
GG007 menu, original icon, studio https://ilanis-agent.github.io/gg-007-gaming/ and privacy.

## Preservation and publishing
Complete source/APK/exact cumulative244cardstudio/publishing fragments privately preserved:
https://files.instinct.com/btbivzyazurr-cutcress-source-archive
https://github.com/iLanis-agent/cutcress holds README only; full Git source pending. All four studio includes and Pages settings unchanged. Both sites verified separately.

## Rule sources
https://riot.ieor.berkeley.edu/Applications/WeightedMinCut/
https://www.cs.toronto.edu/~deepkush/teaching/373s22/hwk/tutorial6-max-cut.pdf
http://www.damtp.cam.ac.uk/user/hf323/M18-OPT/lecture7.pdf
http://we.logoptimize.it/max-cut_finding_cuts_of_maximum_weight/
https://jgaa-v5.cs.brown.edu/index.php/jgaa/article/download/paper523/2417/2224
https://solvenp.now/problems/maximum_cut
