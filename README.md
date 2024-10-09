This is a new [**React Native**](https://reactnative.dev) project, bootstrapped using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

# PlanificaPlus - Roadmap de Funcionalidades

## 1. Registro de Compras Manual
- **Descripción:** Los usuarios pueden ingresar manualmente cada compra que realicen para llevar el control de sus gastos e ingresos.
- **Objetivo:** Ofrecer flexibilidad para registrar cualquier transacción, permitiendo que los usuarios organicen sus finanzas a su gusto.
- **Detalle:** El registro incluirá campos como monto, descripción, y categoría. Podrán editar y eliminar compras en cualquier momento.

## 2. Overview de Gastos
- **Descripción:** Un resumen visual del flujo financiero del usuario.
- **Objetivo:** Proporcionar una visión clara del estado de los gastos, ingresos y balances.
- **Detalle:** Incluirá gráficos de barras y circulares que mostrarán el desglose de los gastos por categorías, así como tendencias de gastos mensuales. También habrá alertas personalizables para avisar cuando el usuario se acerque a un límite de gasto.

## 3. Perfil del Usuario (Opcional)
- **Descripción:** Un perfil donde el usuario puede ingresar datos básicos, como su nombre, ingresos mensuales y preferencias.
- **Objetivo:** Facilitar la personalización y adaptación de la app a las necesidades específicas del usuario.
- **Detalle:** El ingreso de datos es opcional, pero los ingresos mensuales ayudarán a calcular balances y ofrecer recomendaciones personalizadas.

## 4. Lectura Automática de SMS para Compras
- **Descripción:** La app leerá automáticamente los SMS relacionados con compras y preguntará si el usuario desea registrar la transacción.
- **Objetivo:** Automatizar la entrada de datos y reducir la carga manual del usuario.
- **Approach:**
  - Cuando se detecte un SMS de compra, la app comprobará si ya existe en el registro. Si no, enviará una notificación push (con o sin retraso) preguntando al usuario si desea agregar la compra.
  - **Consideración:** Los permisos de lectura de SMS deben solicitarse explícitamente en Android, mientras que en iOS no será posible implementar esta funcionalidad debido a restricciones del sistema operativo.

## 5. Gastos Recurrentes
- **Descripción:** Los usuarios pueden registrar pagos recurrentes, como suscripciones o facturas mensuales, y recibir notificaciones para confirmar su ejecución.
- **Objetivo:** Facilitar el seguimiento de gastos fijos y automatizar la actualización de compras recurrentes.
- **Approach:**
  - Los usuarios registrarán un gasto recurrente indicando el monto, concepto, categoría (opcional) y la fecha de cobro.
  - Recibirán una notificación push preguntando si el cobro se efectuó. Podrán elegir:
    - **Aceptar:** Agrega automáticamente la compra.
    - **Omitir:** Excluye la compra de ese mes.
    - **Cancelar permanentemente:** Deja de seguir ese gasto recurrente.
  - **Exclusión automática de SMS:** Al activar la lectura de SMS, estos gastos no se contarán, evitando duplicados.

## 6. Notificaciones Personalizadas
- **Descripción:** Los usuarios recibirán notificaciones push que les recordarán registrar gastos si no lo han hecho en un tiempo determinado o confirmar transacciones automáticas y recurrentes.
- **Objetivo:** Mantener al usuario informado y activo en la gestión de sus finanzas.
- **Detalle:** Las notificaciones serán configurables en cuanto a frecuencia, tipo de gasto, o límite de gastos alcanzado.

## 7. Análisis Financiero Inteligente (Opcional)
- **Descripción:** Un sistema de recomendaciones que analice los hábitos de gasto del usuario y sugiera formas de mejorar su ahorro o gestionar mejor su dinero.
- **Objetivo:** Ofrecer valor añadido al usuario mediante análisis predictivo y personalizado.
- **Detalle:** Basado en el historial de gastos, la app sugerirá ajustes o identificará patrones. También podrá enviar recomendaciones mensuales para optimizar el uso de los ingresos.

---

# Checklist de Funcionalidades

- [ ] Implementar Registro de Compras Manual
- [ ] Desarrollar Overview de Gastos
- [ ] Crear Perfil del Usuario (Opcional)
- [ ] Implementar Lectura Automática de SMS para Compras
- [ ] Crear funcionalidad de Gastos Recurrentes
- [ ] Desarrollar Notificaciones Personalizadas
- [ ] Implementar Análisis Financiero Inteligente (Opcional)
