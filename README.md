# Simulacro Examen Parcial 1 - Redes [Curso 2024/2025]
https://github.com/Gmongtor/SimulacroExamenParcial1.git
## Parte I: Conceptos y Teoría

### Pregunta 1: Modelos OSI y TCP/IP

**a) Diferencias entre OSI y TCP/IP**

| Característica          | Modelo OSI                              | Modelo TCP/IP                      |
|------------------------|------------------------------------------|------------------------------------|
| Número de capas        | 7                                        | 4                                  |
| Enfoque                | Teórico / Educativo                      | Práctico / Basado en protocolos    |
| División de Aplicación | Aplicación, Presentación, Sesión         | Solo Aplicación                    |
| Implementación real    | Rara vez implementado                    | Base de Internet                   |

**b) Ventajas y limitaciones**

- **Modelo OSI**
  - Ventajas: Estructura clara, modularidad, útil para enseñanza.
  - Limitaciones: No implementado directamente en redes reales.

- **Modelo TCP/IP**
  - Ventajas: Usado en Internet, más simple y funcional.
  - Limitaciones: Menor separación de funciones, menos formal.


![_- visual selection](https://github.com/user-attachments/assets/78f6e33e-c07e-42ce-b6be-e49bbeb8cced)


---

### Pregunta 2: Función de la Capa de Transporte

- **Ubicación**:
  - OSI: Capa 4
  - TCP/IP: Segunda capa desde arriba

- **Funciones**:
  - Segmentación y reensamblado
  - Control de flujo y congestión
  - Detección y corrección de errores
  - Garantía de entrega (si aplica)

- **Protocolos comunes**:
  - TCP (conexión, fiable)
  - UDP (sin conexión, no fiable)
 
![Función de la Capa de Transporte - visual selection](https://github.com/user-attachments/assets/80fff4ca-f3b9-4d7f-a495-ba8d13a67800)


---

### Pregunta 3: Comparación entre TCP y UDP

Este documento presenta una comparación entre dos de los protocolos de comunicación más utilizados en redes: **TCP (Protocolo de Control de Transmisión)** y **UDP (Protocolo de Datagramas de Usuario)**. A través de una tabla que resume sus características clave, se ofrece una visión clara de las diferencias fundamentales entre ambos protocolos, así como sus aplicaciones típicas.

| **Característica**       | **TCP**                              | **UDP**                            |
|--------------------------|--------------------------------------|------------------------------------|
| **Orientación**          | A conexión                           | Sin conexión                       |
| **Fiabilidad**           | Alta (ACK, control de errores)       | Baja                               |
| **Orden de entrega**     | Garantizado                          | No garantizado                     |
| **Velocidad**            | Más lento                            | Más rápido                         |
| **Aplicaciones típicas** | Web, email, FTP, SSH                 | Streaming, VoIP, juegos online     |

---

### TCP: Protocolo de Control de Transmisión

TCP es un protocolo **orientado a la conexión**, lo que significa que establece una conexión antes de enviar datos y garantiza la entrega de los mismos a través de mecanismos de **confirmación (ACK)** y **control de errores**.  
Esto lo hace ideal para aplicaciones donde la **fiabilidad es crucial**, como en:

- Navegación web (HTTP/HTTPS)
- Correo electrónico (SMTP, IMAP, POP3)
- Transferencia de archivos (FTP)
- Conexiones seguras (SSH)

---

### UDP: Protocolo de Datagramas de Usuario

UDP es un protocolo **sin conexión**, que **no garantiza la entrega** de los datos ni el **orden** en que llegan.  
Esto lo hace más **rápido y eficiente**, por lo que es preferido para aplicaciones que requieren **velocidad** y pueden tolerar cierta **pérdida de datos**, como:

- Streaming de video y audio
- Llamadas VoIP
- Juegos en línea

---

### Conclusión

La elección entre **TCP y UDP** depende de las necesidades específicas de la aplicación en cuestión:

- Si se **prioriza la fiabilidad**, se debe usar **TCP**.
- Si se **prioriza la velocidad y eficiencia**, se debe usar **UDP**.


![Comparación entre TCP y UDP - visual selection](https://github.com/user-attachments/assets/50cf00b5-fa2b-4fc5-91b5-422479dd6435)


---

### Pregunta 4: Protocolo para Transferencia de Archivos

**a)** Protocolo tradicional: **FTP**

**b)** Alternativas:
- **SFTP**: Usa SSH, cifrado seguro.
- **FTPS**: Usa SSL/TLS.
- **HTTPS**: Permite transferencia de archivos vía web segura.

---

### Pregunta 5: Proceso de Resolución DNS

1. El usuario ingresa una URL.
2. Se busca en la caché local.
3. Si no está, se consulta al servidor DNS recursivo.
4. Este pregunta a:
   - Servidores raíz → TLD → Servidor autoritativo
5. El autoritativo devuelve la IP correspondiente.
6. La respuesta se almacena en caché.
7. El navegador se conecta al servidor web usando esa IP.

---

### Pregunta 6: Comunicación en el Modelo TCP/IP

**Proceso de envío:**
- **Aplicación**: Genera datos (HTTP, SMTP, etc.)
- **Transporte**: Divide datos en segmentos (TCP/UDP)
- **Internet**: Añade cabecera IP (origen y destino)
- **Acceso a red**: Empaqueta en tramas, transmite

**Proceso de recepción:**  
Inverso al anterior, se eliminan las cabeceras hasta entregar los datos a la aplicación.

---

## Parte II: Capa Física y Ejercicios Prácticos

### Pregunta 7: Tasa de Transmisión Máxima (Shannon)

**Fórmula:**
C = B × log₂(1 + SNR)

**Datos:**
- Ancho de banda: B = 500 MHz = 500 × 10⁶ Hz  
- Relación señal/ruido en dB: SNR_dB = 20 dB

**Conversión de SNR a escala lineal:**
SNR_lineal = 10^(20 / 10) = 100

**Sustitución en la fórmula de Shannon:**
C = 500 × 10⁶ × log₂(1 + 100) = 500 × 10⁶ × log₂(101) = 3.33 × 10^9

---

### Pregunta 8: Ubicación de Portadoras para Eficiencia Espectral

**Datos:**
- Frecuencia de la primera portadora: 1.2 GHz  
- Ancho de banda por canal (en banda base): 300 MHz

---

**a) Frecuencia de la portadora anterior:**

Para obtener la portadora anterior, restamos el ancho de banda:

1.2 GHz - 0.3 GHz = 0.9 GHz

**Resultado:**  
La frecuencia de la portadora anterior es **0.9 GHz**.

**b) Frecuencia de la portadora posterior:**

Para la siguiente portadora, sumamos el ancho de banda:
1.2 GHz + 0.3 GHz = 1.5 GHz

**Resultado:**  
La frecuencia de la portadora posterior es **1.5 GHz**.

---

**Justificación:**

La ubicación de las portadoras en un sistema de comunicación determina cómo se distribuyen los canales dentro del espectro disponible. Para lograr **eficiencia espectral**, es necesario que las portadoras estén espaciadas justo lo suficiente para que sus bandas no se solapen (lo que causaría interferencias), pero sin dejar huecos innecesarios entre ellas (lo que desperdiciaría ancho de banda).

En este caso, el uso de una separación igual al ancho de banda de cada canal (300 MHz) entre portadoras permite utilizar el espectro de forma continua y ordenada, asegurando que no haya interferencias ni espacio desperdiciado. Este método es clave en sistemas como OFDM y multiplexación por división de frecuencia (FDM), donde cada portadora transmite información de manera independiente.

---

### Pregunta 9: Modulación y BER

**Ordenar de mayor a menor robustez ante el ruido:**
1. **BPSK** – Modulación binaria, con solo 2 símbolos. Es la más robusta ante interferencias.
2. **QPSK** – Usa 4 símbolos. Doble eficiencia que BPSK, pero ligeramente menos robusta.
3. **16-QAM** – Usa 16 símbolos. Mejora la eficiencia, pero es más sensible al ruido.
4. **64-QAM** – Usa 64 símbolos. Mayor velocidad, menor tolerancia al ruido.
5. **256-QAM** – Usa 256 símbolos. Muy eficiente, pero la más sensible a errores por ruido.

**Justificación:**  
A medida que aumentamos el número de símbolos en la constelación (mayor orden de modulación), se mejora la eficiencia espectral, pero los símbolos quedan más cerca unos de otros, por lo que la modulación se vuelve más vulnerable al ruido y errores de transmisión.

---

### Pregunta 10: Encapsulamiento y Eficiencia

#### a) Tamaño total del mensaje

**Datos:**
- Bloque de datos de Capa 5: 1.5 KB = 1536 bytes
- Cabeceras: Capa 4 → +40 bytes, Capa 3 → +40 bytes

**Sustitución:**
Tamaño total = 1536 + 40 + 40 = 1616 bytes

---

#### b) Número de tramas necesarias

**Máximo por trama (Capa 2):** 400 bytes

**Cálculo:**
Número de tramas = ceil(1616 / 400) = ceil(4.04) = 5 tramas

---

#### c) Sobrecarga por trama en Capa 1

**Capa 1 añade por cada 2 bytes:**
- 1 byte de inicio
- 1 byte de parada
- 1 byte de CRC

**Pasos:**
- Segmentos de 2 bytes por trama: 400 / 2 = 200
- Sobrecarga total por trama: 200 × 3 = 600 bytes
- Total por trama transmitida: 400 + 600 = 1000 bytes

---

#### d) Eficiencia del sistema

**Fórmula:**
Eficiencia (%) = (Datos útiles / Total transmitido) × 100

**Datos:**
- Datos útiles: 1536 bytes
- Total transmitido: 5 tramas × 1000 bytes = 5000 bytes

**Sustitución:**
Eficiencia = (1536 / 5000) × 100 = 30.72%





