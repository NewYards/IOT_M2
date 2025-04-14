# IOT_M2

Premiere Semaine: J'ai mis en place l'environement et lu le code.

Demarrer programme sur emulateur qemu: qemu-system-arm $(QEMU_ARGS) -device loader,file=build/kernel.elf

Pour debug: -gdb tcp::1234 -S Puis on se connecte dans gdb: gdb-multiarch build/kernel.elf (gdb) tar rem :1234

Deuxieme semaine: Mise en place de la lecture d'un caractere rentrer.

Description schema image.

Pour les boucle:

    dans le read on verifie si le buffer de l'entity en face est vide, si il est vide on attend qu'il recoivent quelque chose.
    dans le write on verifie que notre buffer n'est pas plein, si il est plein on attend que l'autre entité lise quelque chose de notre buffer pour qu'il ne soit plus plein.

UARTIMSC fonctionne pareil que le DR ? chacun sont buffer (+ ecriture pour reset)
UARTRIS et UARTMIS raw et masked, chaque bits represente une interrupton.
raw ==> si activer reste active a 1
masked ==> si activer puis annuler se remet a 0
UARTICR == UARTIMSC sans la partie d'ecriture
UARTIFLS permet def definir quand trgger les interruption par rapport au remplissage des buffer d'interruption

Troisieme semaine:
J'ai corriger des erreurs faite sur les inteeruptions.

Quatrieme semaine:
Etape 2 fini
L'etape 3 n'est pas faite.
