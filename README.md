## rEFInd-minimal dark edition

[rEFInd](http://www.rodsbooks.com/refind/) es un simple gestor de arranque para sistemas basados en UEFI.

### Uso

 1. Lo primero es ubicar el directorio de la carpeta rEFInd, lo más común es algo como esto `/boot/EFI/refind`, además, es 
    posible que tengas que montar la participación donde se encuentra rEFInd, el comando `mount` puede ser de utilidad.

 2. Clona este repositorio dentro de la carpeta de configuración de rEFInd.

 3. Para activar el tema añade la siguiente linea`include rEFInd-minimal-dark/theme.conf` al final del archivo `refind.conf`.

Un pequeño ejemplo de la configuración de una entrada del menú:

```nginx
menuentry "Arch Linux" {
	icon /EFI/refind/rEFInd-minimal-BW/icons/os_arch.png
	loader vmlinuz-linux
	initrd initramfs-linux.img
	options "rw root=UUID=dfb2919d-ff78-48db-a8a7-23f7542c343a loglevel=3"
}

menuentry "Windows" {
	icon /EFI/refind/rEFInd-minimal-BW/icons/os_win.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}

menuentry "OSX" {
	icon /EFI/refind/rEFInd-minimal-BW/icons/os_mac.png
	loader /EFI/Apple/Boot/bootmgfw.efi
}
```

Las entradas serán detectadas automáticamente con su respectivo icono.

### Atribuciones

Este tema es basado en [rEFInd-minimal-theme][rEFInd-minimal-theme] creado por [EvanPurkhiser][EvanPurkhiser].

Muchos de los iconos provienen de [Lightness for burg][icons] hecho por [SWOriginal][icon-author]; fueron modificados para un mejor contraste con el fondo oscuro del tema.

El icono de Windows proviene de [rEFInd Next][rEFInd-Next] tema hecho por [sdbinwiiexe][sdbinwiiexe]

Fue añadido el icono de Manjaro OS y mejorado el icono de apagado

[EvanPurkhiser]: https://github.com/EvanPurkhiser
[rEFInd-minimal-theme]: https://github.com/EvanPurkhiser/rEFInd-minimal
[icons]: http://sworiginal.deviantart.com/art/Lightness-for-burg-181461810
[icon-author]: http://sworiginal.deviantart.com
[rEFInd-Next]: http://sdbinwiiexe.deviantart.com/art/rEFInd-Next-Theme-407754566
[sdbinwiiexe]: http://sdbinwiiexe.deviantart.com
