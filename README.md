# Simulacro Examen Parcial 1 - Redes [Curso 2024/2025]

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

---

### Pregunta 3: Comparación entre TCP y UDP

| Característica            | TCP                                | UDP                             |
|---------------------------|-------------------------------------|----------------------------------|
| Orientación               | A conexión                          | Sin conexión                     |
| Fiabilidad                | Alta (ACK, control de errores)      | Baja                             |
| Orden de entrega          | Garantizado                         | No garantizado                   |
| Velocidad                 | Más lento                           | Más rápido                       |
| Aplicaciones típicas      | Web, email, FTP, SSH                | Streaming, VoIP, juegos online   |

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
C = 500 × 10⁶ × log₂(1 + 100) = 500 × 10⁶ × log₂(101)

➡️ *Calcular log₂(101) y luego multiplicar por 500 × 10⁶ para obtener C en bps.*

---

### Pregunta 8: Ubicación de Portadoras

**Datos:**
- Primera portadora: 1.2 GHz
- Ancho de banda por canal: 300 MHz

**a) Frecuencia de la portadora anterior:**
1.2 GHz - 0.3 GHz = 0.9 GHz

**b) Frecuencia de la portadora posterior:**
1.2 GHz + 0.3 GHz = 1.5 GHz

---

### Pregunta 9: Modulación y BER

**Ordenar de mayor a menor robustez ante el ruido:**
1. BPSK
2. QPSK
3. 16-QAM
4. 64-QAM
5. 256-QAM

**Justificación:**  
A mayor número de símbolos por baudio, mayor eficiencia espectral, pero menor tolerancia al ruido. Las modulaciones con constelaciones más grandes son más sensibles a interferencias.

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
Eficiencia = (1536 / 5000) × 100 = ? %

➡️ *Realizar la división y multiplicar por 100 para obtener la eficiencia.*





