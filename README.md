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

**Datos:**
- Ancho de banda \( B = 500 \, \text{MHz} \)
- SNR (en dB) = 20

**Conversión:**

**Sustituir en la fórmula de Shannon y dejar expresado sin calcular.**

---

### Pregunta 8: Ubicación de Portadoras

**Datos:**
- Primera portadora: 1.2 GHz
- Ancho de banda por canal: 300 MHz

**a)** Portadora anterior:

**b)** Portadora posterior:

**Importancia:** La separación adecuada de portadoras evita interferencias y mejora la eficiencia espectral.

---

### Pregunta 9: Modulación y BER

**Ordenar de mayor a menor robustez ante el ruido:**
- BPSK
- QPSK
- 16-QAM
- 64-QAM
- 256-QAM

**Justificación:** A mayor número de símbolos por baudio, mayor eficiencia pero menor tolerancia al ruido.

---

### Pregunta 10: Eficiencia del Sistema de Encapsulamiento

**Datos:**
- Capa 5: bloque de 1.5 KB = 1536 bytes
- Capas 4 y 3: +40 bytes cada una
- Capa 2: Máximo 400 bytes por trama
- Capa 1: Por cada 2 bytes, se añaden:
  - 1 byte de inicio
  - 1 byte de parada
  - 1 byte de CRC

---

**a) Tamaño del mensaje:**

---

**b) Número de tramas necesarias:**

---

**c) Sobrecarga por trama en capa 1:**

---

**d) Eficiencia del sistema:**

---
