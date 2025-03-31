# IOT_M2

Premiere Semaine:
J'ai mis en place l'environement et lu le code.

Demarrer programme sur emulateur qemu:
qemu-system-arm $(QEMU_ARGS) -device loader,file=build/kernel.elf

Pour debug:
-gdb tcp::1234 -S
Puis on se connecte dans gdb:
gdb-multiarch build/kernel.elf
(gdb) tar rem :1234
