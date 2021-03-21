Copiar el siguiente código en el Playground de Pharo, para probar el `exportarSocios` utilizando `NeoJSONAdapter`.

```smalltalk

| miBiblioteca arya tyron col |
miBiblioteca:= Biblioteca new: NeoJSONAdapter new.
arya:= Socio nombre:'Arya Stark' email:'needle@stark.com' legajo: '5234/5'.
tyron:= Socio nombre:'Tyron Lannister' email:'tyron@thelannisters.com' legajo:'2345/2'.
miBiblioteca agregarSocio: arya.
miBiblioteca agregarSocio: tyron.

miBiblioteca exportarSocios
```