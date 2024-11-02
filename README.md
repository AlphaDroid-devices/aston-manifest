# Build AlphaDroid for OnePlus Ace 3 | 12R

## Prerequisites
- refer to [AOSP](https://source.android.com/docs/setup/start/requirements)

## Build
1. Initialise repo with [AlphaDroid](https://github.com/alphadroid-project/manifest) source code.
    ```
    repo init -u https://github.com/alphadroid-project/manifest.git -b alpha-15 --git-lfs
    ```

2. Download [aston manifest](https://github.com/AlphaDroid-devices/aston-manifest/blob/alpha-15/local_manifest.xml) by cloning this repo
    ```
    git clone https://github.com/alphadroid-devices/aston-manifest -b alpha-15 .repo/local_manifests
    ```

3. Sync
    ```
    repo sync 
    ```

4. Cook some bacon
    ```
    . build/envsetup.sh
    lunch alpha_<device>-[<release>]-user
    make bacon
    ```

    Or the light menu (no bacon)
    ```
    . build/envsetup.sh
    brunch aston
    ```
Enjoy! :)
