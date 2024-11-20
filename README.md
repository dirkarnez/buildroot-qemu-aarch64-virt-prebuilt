buildroot-qemu-virt-prebuilt
============================
### x86_64
- [buildroot编译运行QEMU X86_64](https://jgsun.github.io/2020/05/28/qemu-x86-64/)
  - ```bash
    sudo qemu-system-x86_64 -M pc -kernel output/images/bzImage \
      -drive file=output/images/rootfs.ext2,if=virtio,format=raw \
      -append "rootwait root=/dev/vda console=tty1 \
      console=ttyS0" \
      -net nic,model=virtio \
      -net user -nographic \
      -enable-kvm
    ```
### aarch64
