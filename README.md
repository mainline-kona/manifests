# Mainline Kona Local Manifest (LineageOS 24.0 / Android 17)

Drop-in `local_manifest` for building **OnePlus 8T (`kebab`)** on **LineageOS 24.0 (Android 17)** with an inline mainline-based Linux 6.18 kernel.

## Usage

After initializing LineageOS 24.0 (`repo init -u https://github.com/LineageOS/android.git -b lineage-24.0`):

```bash
mkdir -p .repo/local_manifests
curl -fsSL https://raw.githubusercontent.com/mainline-kona/manifests/main/default.xml \
  -o .repo/local_manifests/mainline-kona.xml
repo sync -c --no-clone-bundle --no-tags -j$(nproc)
```

## Build

```bash
source build/envsetup.sh
breakfast kebab_mainline
mka bacon
```
