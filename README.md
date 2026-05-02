# PCB compacta para E22/E22P con NRF52840

Placa sencilla para montar un E22/E22P con un NRF52, con resistencias para monitorear el voltaje.

![imagen1](ArchivosV1.0/Preview_delante.png)
![imagen2](ArchivosV1.0/Preview_detrás.png)

V1.0 hecho a partir de la V1.1 de la Michtastic ([Hamspiced/MichTastic_Node](https://github.com/Hamspiced/MichTastic_Node/tree/main))

---

### 🛠️ Método de montaje

1. **Suelda el E22/E22P y la resistencias SMD**  
   - Se puede soldar tanto con soldador, placa caliente o aire caliente. **Ojo a la hora de posicionar el E22/E22P**.

2. **Suelda el selector de E22/E22P según tu placa**
   - Un punto de estaño rápido con el soldador es suficiente.

3. **Suelda los espadines**  
   - Corta 1 espadín de la tira larga y alinealos con los agujeros (con el último de ellos, puedes ver que el primer agujero es un poco más pequeño y no entrará fácilmente). Coloca la otra tira de 3 espadines en los otros agujeros, de manera que el lado largo de estos espadines sea el que está introducido en la PCB. Ahora pon el promicro encima y **solo suelda los espadines a la PCB del albatastic, no al promicro**. Quita el promicro y quita los separadores de plástico de los espadines.

4. **Suelda el promicro**  
   - Empuja el promicro hacia abajo y suéldalo. Corta los espadines sobrantes al acabar.

5. **Suelda la alimentación**  
   - Se puede alimentar tanto a voltaje de batería (aunque el E22/E22P no sacará 1W), como a 5V. Tanto el voltaje de batería o los 5V irán a **5V**, tierra a **GND** y si quieres monitorear la batería, el positivo de la batería a **BAT** (si lo vas a alimentar con voltaje de batería hay un pequeño jumper que puedes soldar para monitorear la batería).

6. **Conecta la antena**  
   - Antes de encender el nodo, conecta la antena para no dañar el módulo de radio.

7. **Enciende el nodo y verifica el funcionamiento**

---

<details>
<summary><b>📸 Haz clic aquí para ver Ejemplos de uso</b></summary>

### Casos de éxito
Esta PCB se ha utilizado en el nodo de "Molatower", localizado en la cima del Molatón, Higueruela, Albacete, montado por nuestro compañero @ivansanchezfue4.

![photo_5908823209509850083_y](https://github.com/user-attachments/assets/09a3cbc4-8b2f-423a-9920-03a9aa4e50d8)
![photo_5908823209509850082_y](https://github.com/user-attachments/assets/0920ba4b-05ae-433d-bf34-e13ad7d18f07)

Con este nodo se han podido unir las provincias de Murcia, Alicante y Valencia con Albacete. Si tienes más fotos de la PCB en uso, no dudes en mandármelas.
</details>

---

<details>
<summary><b>📜 Ver Historial de Cambios (Changelog)</b></summary>

<br>

#### [V1.2] - Sin testear - En desarrollo 🚧
* **Añadido:** Añadido pines para puerto serial
* **Eliminado** Eliminado el condensador electrolítico
* **Mejora:** Aumentaod el espesor de trazas de alimentación, BAT+ y GND
* **Mejoras:** Simples mejoras en estética

#### [V1.1.1] - Sin testear 🚧
* **Corregido:** Error en la conexión de trazas con el RA62.

#### [V1.1] - Testeada 🚧
* **Añadido:** Soporte para módulo GPS externo.
* **Añadido:** Conexiones para Hat/Shield con MPPT y cargador USB-C.
* **Añadido:** Conexión para el RA62.
* **Añadido:** Mosfet para control de energía del GPS.
* **Añadido:** Condensador SMD de 470uF en la placa de radio.
* **Añadido:** Añadido el pad BAT- por si hiciera falta que el negativo del divisor de voltaje no fuera común
* **Mejora:** Aumentado el espesor de la traza de alimentación y GND

#### [V1.0] - Versión Inicial ✅
* **Lanzamiento:** Placa base compacta para E22/E22P.
* **Funcionalidad:** Monitorización de voltaje de batería mediante divisor de voltaje.
* **Hardware:** Soporte para NRF52840 Pro Micro.
* **Estado:** Testeada y en funcionamiento pleno.

</details>
---

### 🚧 Work in progress 🚧
Actualmente estoy trabajando en la versión V1.1, donde incluyo conexiones para el GPS, además de un hat/shield donde colocar un MPPT, booster y cargador USB-C. 

<img width="995" src="https://github.com/user-attachments/assets/052228dc-d1a3-4564-8d50-3ab76e96426c" alt="prototipo_v1 1_f" />
<img width="935" src="https://github.com/user-attachments/assets/81733120-3768-44c5-aa6e-3f3b586f603e" alt="prototipo_v1 1_r" />
<img width="921" src="https://github.com/user-attachments/assets/30de14ae-e9fb-4481-acbf-70eb4781c002" alt="prototipo_hat_f" />
<img width="933" src="https://github.com/user-attachments/assets/09d70ce7-dc2b-4b8e-95e2-545442934766" alt="prototipo_hat_r" />

Hay soporte para el HT-RA62 y mosfet para el GPS. Los archivos serán publicados cuando se termine de probar la placa.

---

### 📝 Licencia
Proyecto Open Source **No comercial**
