# Galaxy Tab S9 Wi-Fi (gts9wifi) kernel: KernelSU Next + SUSFS

Builds the LineageOS 24.0 (20261015) kernel for SM-X710 unchanged except for
KernelSU Next (which ships SUSFS), and repacks Lineage's `boot.img` with it.

- Source: `samsung-sm8550-tab/android_kernel_samsung_sm8550` @ `038b7c0528e2`
- Config: `config/lineage24.config` (the running kernel's `/proc/config.gz`) + `CONFIG_KSU`
- Toolchain: Android clang r596125 (same as Lineage)
- Release string is pinned to `5.15.208-g038b7c0528e2` so Lineage's
  vendor_boot / vendor_dlkm modules keep loading.

Run the workflow manually (Actions → Build → Run workflow); the artifact holds
`boot.img`, `Image`, `.config` and checksums.
