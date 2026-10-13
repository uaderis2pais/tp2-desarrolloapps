# TP2 — Carrito de Compras & Proceso de Pago (Checkout)

Aplicación móvil desarrollada con **React Native**, **Expo (SDK 54)**, **Expo Router v6** y **TypeScript**, que implementa un flujo completo de carrito de compras y pantalla de pago/checkout con validaciones en tiempo real.

---

## 📱 Funcionalidades Principales

### 1. Pantalla de Carrito de Compras (`/`)
- **Gestión de Artículos**:
  - Visualización de productos en el carrito con imagen, título, precio unitario y cantidad.
  - Modificación dinámica de cantidades (incrementar y decrementar con actualización inmediata de subtotales).
  - Eliminación de ítems individuales del carrito.
  - Botón de restablecimiento de demo para volver al estado inicial de productos.
- **Cálculo de Totales**:
  - Resumen de compra con subtotal, impuestos/descuentos y total general recalculados automáticamente.
  - Navegación al proceso de pago pasando el estado de la compra.

### 2. Pantalla de Checkout y Pago (`/payment`)
- **Selección de Tipo de Tarjeta**:
  - Soporte visual interactivo para tarjetas: Visa, MasterCard, American Express y Otros.
- **Formulario de Datos de Pago**:
  - Titular de la tarjeta.
  - Número de tarjeta con formateo visual.
  - Fecha de vencimiento (mes/año) y código de seguridad (CVV).
- **Gestión de Dirección de Envío**:
  - Modal interactivo para ingresar o editar la dirección de entrega (Calle, Ciudad, Código Postal, País).
- **Validaciones & Confirmación**:
  - Validaciones de campos requeridos antes de procesar el pago.
  - Alertas y feedback de confirmación de transacción exitosa.

---

## 🛠️ Requisitos e Instalación

### Requisitos previos
- **Node.js** (v18 o superior recomendado)
- **npm** o **yarn**
- Dispositivo móvil con la aplicación **Expo Go** (Android / iOS) o un emulador configurado.

### Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/uaderis2pais/tp2-desarrolloapps.git
   cd tp2-desarrolloapps
   ```

2. Instalar dependencias:
   ```bash
   npm install
   ```

3. Iniciar el servidor de desarrollo:
   ```bash
   npx expo start
   ```

4. **Ejecución**:
   - Escanear el código QR con la app **Expo Go** (en Android) o la Cámara (en iOS).
   - O presionar `a` en la terminal para abrir en emulador Android.
   - O presionar `w` para probar en el navegador web.

---

## 📂 Estructura del Proyecto

```text
├── assets/                  # Íconos e imágenes estáticas
├── src/
│   ├── app/                 # Rutas de Expo Router
│   │   ├── _layout.tsx      # Configuración de navegación y temas
│   │   ├── index.tsx        # Pantalla principal: Carrito de compras
│   │   └── payment.tsx      # Pantalla secundaria: Proceso de checkout y pago
│   ├── components/          # Componentes reutilizables (CartItemRow, etc.)
│   ├── constants/           # Datos iniciales (initialCart.ts)
│   └── types/               # Definiciones TypeScript (checkout.ts, etc.)
├── app.json                 # Configuración de Expo
├── package.json             # Dependencias y scripts
└── tsconfig.json            # Configuración de TypeScript
```
