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


Deuxieme semaine:
Mise en place de la lecture d'un caractere rentrer.

Description schema image.

Pour les boucle:
- dans le read on verifie si le buffer de l'entity en face est vide, si il est vide on attend qu'il recoivent quelque chose.
- dans le write on verifie que notre buffer n'est pas plein, si il est plein on attend que l'autre entité lise quelque chose de notre buffer pour qu'il ne soit plus plein.



