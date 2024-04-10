Architecture: x86_64
CPU op-mode(s): 32-bit, 64-bit
Byte Order: Little Endian
CPU(s): 8
On-line CPU(s) list: 0-7
Thread(s) per core: 2
Core(s) per socket: 4
Socket(s): 1
NUMA node(s): 1
Vendor ID: GenuineIntel
BIOS Vendor ID: Alibaba Cloud
CPU family: 6
Model: 85
Model name: Intel(R) Xeon(R) Platinum
BIOS Model name: pc-i440fx-2.1
Stepping: 4
CPU MHz: 2499.988
BogoMIPS: 4999.97
Hypervisor vendor: KVM
Virtualization type: full
L1d cache: 32K
L1i cache: 32K
L2 cache: 1024K
L3 cache: 33792K
NUMA node0 CPU(s): 0-7

[root@hq-sh-spider-003 kicad-cli-java]# ./tests.sh
docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/f3385c91-7a9b-4c0d-a147-7132cca22c25 a37c2763212f kicad-cli pcb export glb --subst-models /home/kicad/f3385c91-7a9b-4c0d-a147-7132cca22c25/video.kicad_pcb -o /home/kicad/f3385c91-7a9b-4c0d-a147-7132cca22c25/bb8b7bfc-b110-4081-9144-d6c324d85fed.glb
docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/f3385c91-7a9b-4c0d-a147-7132cca22c25 a37c2763212f npx gltfpack -i /home/kicad/f3385c91-7a9b-4c0d-a147-7132cca22c25/bb8b7bfc-b110-4081-9144-d6c324d85fed.glb -v -cc -tc -ts 0.5 -o /home/kicad/f3385c91-7a9b-4c0d-a147-7132cca22c25/57c99dee-c1e9-4de3-b9af-ffc511444458.glb
程序执行时间: 27197 毫秒

[root@hq-sh-spider-003 kicad-cli-java]# ./tests.sh
docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/6e8dbe22-067c-4440-bfc4-8c569ec2a95d a37c2763212f kicad-cli pcb export glb --subst-models /home/kicad/6e8dbe22-067c-4440-bfc4-8c569ec2a95d/complex_hierarchy.kicad_pcb -o /home/kicad/6e8dbe22-067c-4440-bfc4-8c569ec2a95d/1a8a916f-b6d6-4bc1-894f-6f88076f8f78.glb
docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/6e8dbe22-067c-4440-bfc4-8c569ec2a95d a37c2763212f npx gltfpack -i /home/kicad/6e8dbe22-067c-4440-bfc4-8c569ec2a95d/1a8a916f-b6d6-4bc1-894f-6f88076f8f78.glb -v -cc -tc -ts 0.5 -o /home/kicad/6e8dbe22-067c-4440-bfc4-8c569ec2a95d/44b3c926-0735-4aeb-8fe1-c3f20592cc2b.glb
程序执行时间: 4382 毫秒

[root@hq-sh-spider-003 kicad-cli-java]# ./tests.sh
docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/06150827-3dcb-49ae-b885-cdcd2308eaea a37c2763212f kicad-cli pcb export glb --subst-models --include-tracks /home/kicad/06150827-3dcb-49ae-b885-cdcd2308eaea/complex_hierarchy.kicad_pcb -o /home/kicad/06150827-3dcb-49ae-b885-cdcd2308eaea/da0081b8-1e2c-4002-813b-cdebab42d9cb.glb
docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/06150827-3dcb-49ae-b885-cdcd2308eaea a37c2763212f npx gltfpack -i /home/kicad/06150827-3dcb-49ae-b885-cdcd2308eaea/da0081b8-1e2c-4002-813b-cdebab42d9cb.glb -v -cc -tc -ts 0.5 -o /home/kicad/06150827-3dcb-49ae-b885-cdcd2308eaea/14e38993-785e-4dc7-a83f-4bed8fc0a7d5.glb
程序执行时间: 12579 毫秒

docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/15455b73-d46a-4935-addd-6d754a48988b a37c2763212f kicad-cli pcb export glb --subst-models --include-tracks /home/kicad/15455b73-d46a-4935-addd-6d754a48988b/video.kicad_pcb -o /home/kicad/15455b73-d46a-4935-addd-6d754a48988b/82b5b1e8-170b-47d3-98e4-370b17aa792d.glb
docker run -v /home/hq/kicad/complex_hierarchy:/home/kicad/15455b73-d46a-4935-addd-6d754a48988b a37c2763212f npx gltfpack -i /home/kicad/15455b73-d46a-4935-addd-6d754a48988b/82b5b1e8-170b-47d3-98e4-370b17aa792d.glb -v -cc -tc -ts 0.5 -o /home/kicad/15455b73-d46a-4935-addd-6d754a48988b/6278a8f2-c9da-49f0-884c-5e8f265284a0.glb
程序执行时间: 130401 毫秒
