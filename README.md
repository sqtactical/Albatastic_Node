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
## Versión 1.0
Esta PCB se ha utilizado en el nodo de "Molatower", localizado en la cima del Molatón, Higueruela, Albacete, montado por nuestro compañero @ivansanchezfue4.

![photo_5908823209509850083_y](https://github.com/user-attachments/assets/09a3cbc4-8b2f-423a-9920-03a9aa4e50d8)
![photo_5908823209509850082_y](https://github.com/user-attachments/assets/0920ba4b-05ae-433d-bf34-e13ad7d18f07)

Con este nodo se han podido unir las provincias de Murcia, Alicante y Valencia con Albacete. Si tienes más fotos de la PCB en uso, no dudes en mandármelas.
## Versión 1.1
Placa montada por nuestro compañero Francesc EA3HGP
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/58af8261-e498-4823-8ab5-ed7a57613fe7" />
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/061514d3-30f2-4292-9f17-3906b0814990" />



</details>

---

<details>
<summary><b>📜 Ver Historial de Cambios (Changelog)</b></summary>

<br>

#### [V2.0] - Testeada, funciona parcialmente
* **Cambio importante:** Se pasa el promicro de THT a SMD, con su agujero para poder acceder al selector que hay que soldar para que cargue a 100mA
* **Añadido:** Booster HW-085 para E22/E22P
* **Añadido:** Compatibilidad con el E80


#### [V1.3] - Sin testear - En desarrollo 🚧
* **Añadido:** Plano de tierra
* **Añadido:** Jumper para separar el negativo de las resistencias de monitorización de la batería de GND
* **Añadido:** Jumper para seleccionar si se quiere alimentar el pro micro a 5V (No compatible con 5V y batería al mismo tiempo)
* **Añadido:** Pads para I2C
* **Añadido:** Condensador de tántalo de 100uF (opcional)
* **Mejora:** El selector entre E22/E22P está ahora fuera de debajo del promicro

#### [V1.2] - Testeando 🚧
* **Añadido:** Añadido pines para puerto serial
* **Eliminado** Eliminado el condensador electrolítico
* **Mejora:** Aumentado el espesor de trazas de alimentación, BAT+ y GND
* **Mejoras:** Simples mejoras en estética

#### [V1.1.1] - Testeada con éxito ✅
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

### 🚧 Work in progress 🚧
Actualmente estoy trabajando en la versión V1.2, donde incluyo conexiones con serial. También estoy trabajando en el hat y en la versión para 2.4 GHz (con un E28)

V1.2 de la Albatastic compact (negro)
<img width="832" height="467" alt="image" src="https://github.com/user-attachments/assets/d807bfd5-5872-4b4b-a02f-941e9a1bbd62" />
V1.0 del hat solar (azul)
<img width="816" height="468" alt="image" src="https://github.com/user-attachments/assets/9b738aea-6373-4c76-8c26-1381da6a4fca" />
V1.0 de la versión para 2.4 GHz (rojo)
<img width="872" height="516" alt="image" src="https://github.com/user-attachments/assets/d8d4aac5-59ec-433e-8a08-a5086d248a83" />






---

### 📝 Licencia
Proyecto Open Source **No comercial**
