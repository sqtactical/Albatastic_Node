# 🛰️ Albatastic Compact
### PCB compacta para E22/E22P con nRF52840

Placa base sencilla optimizada para montar un módulo de radio **E22/E22P** junto a un **nRF52 Pro Micro**, incluyendo circuitería con resistencias para el monitoreo nativo del voltaje de la batería.

![imagen1](ArchivosV1.0/Preview_delante.png)
![imagen2](ArchivosV1.0/Preview_detrás.png)

> 🧬 **Créditos:** V1.0 desarrollada a partir de la V1.1 de la Michtastic ([Hamspiced/MichTastic_Node](https://github.com/Hamspiced/MichTastic_Node/tree/main)).

---

## 🛠️ Método de Montaje Paso a Paso (V1.0)

1. **Módulos SMD**
   * Suelda el **E22/E22P** y las resistencias SMD. 
   * *Método:* Puedes usar soldador de mano, placa caliente (*hot plate*) o estación de aire caliente.
   * ⚠️ **Ojo:** Presta mucha atención a la orientación y posicionamiento del E22/E22P antes de aplicar calor.

2. **Selector de Radio**
   * Suelda el jumper selector del E22/E22P correspondiente según tu placa. Un punto rápido de estaño con el soldador es suficiente.

3. **Preparación de Espadines (Truco de alineación)**
   * Corta 1 espadín de la tira larga y alinéalo con los agujeros (notarás que el primer agujero es más pequeño y entrará ajustado).
   * Coloca la otra tira de 3 espadines en los agujeros opuestos, asegurándote de que el **lado largo** de los espadines quede introducido en la PCB.
   * Presenta el Pro Micro encima para alinear todo y **solo suelda los espadines a la PCB de Albatastic, NO al Pro Micro**.
   * Retira el Pro Micro temporalmente y quita los separadores de plástico negros de los espadines.

4. **Soldadura del Pro Micro**
   * Empuja el Pro Micro hacia abajo (al ras de la placa) y suéldalo de forma definitiva. Corta los sobrantes de los pines al acabar.

5. **Alimentación y Monitoreo**
   * **Opciones de alimentación:** Admite voltaje directo de batería (el E22 no emitirá a 1W pleno) o 5V regulados. Ambos positivos van al pad marcado como **5V**, y la masa a **GND**.
   * **Monitoreo (BAT):** Para medir el voltaje, conecta el positivo de la batería al pad **BAT**. Si alimentas todo directamente con el voltaje de la batería, suelda el pequeño jumper integrado diseñado para este propósito.

6. **Conexión de Antena**
   > [!WARNING]
   > **¡MUY IMPORTANTE!** Conecta siempre la antena antes de energizar o encender el nodo. Transmitir sin antena dañará de forma irreversible el módulo de radio E22/E22P.

7. **Verificación**
   * Enciende el nodo y verifica el correcto funcionamiento del firmware.

---

<details>
<summary><b>📸 Casos de Éxito y Ejemplos de Uso (Clic para desplegar)</b></summary>

### ⛰️ Versión 1.0 - Nodo "Molatower"
Ubicado en la cima del **Molatón (Higueruela, Albacete)**, diseñado y montado por el compañero `@ivansanchezfue4`.

![photo_5908823209509850083_y](https://github.com/user-attachments/assets/09a3cbc4-8b2f-423a-9920-03a9aa4e50d8)
![photo_5908823209509850082_y](https://github.com/user-attachments/assets/0920ba4b-05ae-433d-bf34-e13ad7d18f07)

> 🌍 **Logro:** Este nodo ha servido de puente estratégico, logrando unir las provincias de **Murcia, Alicante y Valencia con Albacete**. ¡Si tienes fotos de tus despliegues, envíanoslas para añadirlas!

### 📡 Versión 1.1 - Despliegue EA3HGP
Placa montada por el compañero **Francesc EA3HGP**:

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/58af8261-e498-4823-8ab5-ed7a57613fe7" />
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/061514d3-30f2-4292-9f17-3906b0814990" />

</details>

---

<details>
<summary><b>📜 Historial de Cambios / Changelog (Clic para desplegar)</b></summary>

<br>

> [!NOTE]
> **Nomenclatura del proyecto:** Las versiones **V1.X** utilizan el Pro Micro en formato THT (Recomendado para nodos fijos ya que se puede preparar para que el pro micro sea extraible). Las versiones **V2.X** migran a formato SMD. Las versiones 3.0 serán con el NRF52 embedded (si puedo lograrlo)

#### 🚧 V2.2 (En desarrollo - Sin testear)
* **Añadido:** Pads y ruteado para el módulo **E28-2G4M27SX** (Requiere firmware modificado).

#### 🚧 V2.1 (En desarrollo - Sin testear)
* **Corregido:** Conflicto al alimentar simultáneamente por 5V y BAT+. Ahora se prioriza la alimentación por BAT+ con opción de usar un jumper para entornos conectados a red (5V).

#### ⚠️ V2.0 (Testeada - Funcionamiento parcial)
* **Cambio estructural:** Migración del Pro Micro de formato THT a **SMD** (con ventana calada en la PCB para acceder al selector de carga de 300mA trasero).
* **Añadido:** Espacio para Booster integrado **HW-085** (específico para el E22/E22P a 5V).
* **Añadido:** Compatibilidad con el módulo de radio **E80**.

#### 🚧 V1.3 (En desarrollo - Sin testear)
* **Mejora:**  Añadido plano de tierra completo (GND plane).
* **Añadido:** Jumper para aislar el negativo del divisor de tensión de monitoreo de la masa común.
* **Añadido:** Jumper selector para alimentar el Pro Micro a 5V (Incompatible con uso simultáneo de 5V y batería).
* **Añadido:** Pads para bus **I2C**.
* **Añadido:** Footprint para condensador de tántalo opcional de 100uF.
* **Mejora:** El selector E22/E22P se desplaza fuera del área oculta por el Pro Micro.

#### 🚧 V1.2 (En fase de testeo)
* **Añadido:** Salida de pines para serial.
* **Eliminado:** Condensador electrolítico SMD
* **Mejora:** Incrementado notablemente el grosor de las pistas críticas de potencia (5V y GND).
* **Mejora:** Optimización estética general de la serigrafía.

#### ✅ V1.1.1 (Testeada con éxito)
* **Corregido:** Error de ruteado en las trazas de conexión con el chip RA62.

#### ⚠️ V1.1 (Testeada - Funcionamiento parcial)
* **Añadido:** Soporte nativo para módulo GPS externo + Mosfet dedicado para el apagado/control de energía del mismo.
* **Añadido:** Pines de expansión para conectar un Hat/Shield con MPPT solar y USB-C.
* **Añadido:** Compatibilidad y huella para radio **RA62**.
* **Añadido:** Condensador SMD de 470uF integrado en la zona de radio.
* **Añadido:** Pad independiente `BAT-` para aislar la masa del divisor si fuera necesario.
* **Mejora:** Mayor grosor en pistas de alimentación.

#### ✅ V1.0 (Versión Inicial)
* **Lanzamiento:** Primera versión funcional de la placa base compacta para E22/E22P.
* **Características:** Divisor de tensión para medir batería y zócalo THT para nRF52840 Pro Micro.

</details>

---

### 📝 Licencia
Proyecto Open Source **No Comercial**
