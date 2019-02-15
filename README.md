LineageOS
===========

Getting started
---------------

```
1. mkdir -p LOS15 && cd LOS15

2. Initialize your local repository using the LineageOS trees with a command
  repo init -u git://github.com/LineageOS/android.git -b lineage-15.1
  
3. Clone this repo:
  git clone https://github.com/ComicoTeam/android_local_manifests_n7100 -b lineage-15.1 

4. Copy local manifest (local_manifest.xml)
  mkdir -p .repo/local_manifests
  cp android_local_manifests_n7100/local_manifest.xml .repo/local_manifests/

5. Sync LineageOS trees:
  repo sync --no-tags --no-clone-bundle --force-sync -c -j8

6. Apply patches to the newly synced sources:
  . build/envsetup.sh
  bash android_local_manifests_n7100/fetch.sh
  bash android_local_manifests_n7100/apply.sh

7. To build:
  . build/envsetup.sh
  lunch lineage_n7100-userdebug
  make -j8 bacon
```
