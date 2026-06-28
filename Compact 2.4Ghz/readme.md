Placa compatible con el Ebyte E28. Hay que usar el firmware modificado para que sea compatible con el E28-2G4M27SX



Changelog:

#### [V1.1] - Sin testear - En desarrollo 🚧
* **Eliminado:** Eliminada 2 de las opciones de alimentar el E28, ya que con el propio pro micro basta (habrá que estudiar bien si aguanta mucho tráfico)
* **Cambio:** Se conmuta TX EN por el pin 106 del pro micro (que estaba libre). Es necesario usar el firmware subido en esta página
* **Añadido:** Condensador de tántalo B de 100uF
* **Añadido:** Opción de alimentar el pro micro a 5v o a batería (se selecciona mediante jumpers)


#### [Beta 1.0] - Testeada, funcionamiento parcial
* **Añadido:** Opción de alimentar el E28 de 3 maneras distintas
* **Añadido:** Ebyte E28
* **Opción:** Conmutación de TX EN por DIO2, no funciona salvo cambios grandes en el firmware (radiolib)
