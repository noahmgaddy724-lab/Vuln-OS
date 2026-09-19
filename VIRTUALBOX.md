# VirtualBox

1. Install VirtualBox on the host.
2. Create a Host-Only network.
3. Keep the Vuln-OS adapter on Host-Only or Internal Network.
4. Do not use Bridged Adapter for the vulnerable lab.
5. Allocate 2–4 CPUs, 4–8 GB RAM, and at least 40 GB storage.
6. Run the build script on a real Linux host to create the bootable disk.
7. Import/open `virtualbox/Vuln-OS.vbox`.
8. Boot and run `vuln-health`.
9. Confirm the dashboard from the host-only network.

The repository intentionally does not contain a generated `.vdi` because large binary VM disks do not belong in Git.
