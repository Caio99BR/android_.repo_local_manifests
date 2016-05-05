CM13.0 Manifests
========================
Project M4 / Project U0 / Project Vee3 / Project V1

Local manifests to build Android MarshMallow 6.0 to L5, L7, L3II and L1II

To initialize CM13.0 Repo:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0 -g all,-notdefault,-darwin

To initialize Repo's:

    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/TeamVee/android_.repo_local_manifests/cm-13.0/local_manifest.xml

To sync:

    repo sync

To initialize the environment

    . build/envsetup.sh

To build for L5, apply patchs and build:

    sh device/lge/msm7x27a-common/patches/apply.sh
    brunch e610

To build for L7:

    brunch p700

To build for L3 II, apply patchs and build:

    sh device/lge/vee3/patches/apply.sh
    brunch vee3

To build for L1 II, apply patchs, enable variable to v1 and build:

    sh device/lge/vee3/patches/apply.sh
    export TARGET_KERNEL_V1_BUILD_DEVICE=true
    brunch vee3
