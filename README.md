# redpill-vmwgfx

## How to compile

1. Download Linux kernel source from: https://cndl.synology.cn/download/ToolChain/Synology%20NAS%20GPL%20Source/7.0-41890/apollolake/linux-4.4.x.txz
2. Apply patch src/0001-fix-vmwgfx-ttm-compile-errors.patch
3. Run `cp synoconfigs/apollolake .config && echo "CONFIG_DRM_VMWGFX=m" >> .config && make oldconfig`
4. Run `make modules_prepare`
5. Run `make SUBDIRS=drivers/gpu/drm/vmwgfx/ modules`
5. Run `make SUBDIRS=drivers/gpu/drm/ttm/ modules`

