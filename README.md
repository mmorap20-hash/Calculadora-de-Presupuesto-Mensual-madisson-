# Calculadora-de-Presupuesto-Mensual-madisson-
# 💰 Calculadora-de-Presupuesto-Mensual

[cite_start]Este repositorio documenta el análisis y la propuesta de mantenimiento de software para la aplicación **Calculadora de Presupuesto Mensual** [cite: 57][cite_start], la cual está diseñada para gestionar las finanzas personales registrando ingresos y gastos para calcular el balance general[cite: 59, 60].

## 📝 Descripción y Problemas Detectados

[cite_start]El análisis identificó varios aspectos que requieren atención para mejorar la fiabilidad y adaptabilidad del sistema[cite: 178]:

1.  [cite_start]**Inconsistencias en el Cálculo:** Errores al calcular el balance total por el ingreso de datos incompletos o incorrectos (negativos)[cite: 97]. (Mantenimiento Correctivo)
2.  [cite_start]**Falta de Persistencia de Datos:** Los registros pueden perderse si se cierra la aplicación, ya que no hay un mecanismo robusto de guardado[cite: 105, 106]. (Mantenimiento Preventivo)
3.  [cite_start]**Limitada Adaptabilidad:** El sistema está diseñado inicialmente solo para uso en escritorio, limitando la accesibilidad móvil[cite: 117]. (Mantenimiento Adaptativo)

---

## 🎯 Objetivos y Requerimientos con Mejoras (DRS v2)

[cite_start]Las propuestas técnicas están enfocadas en la mejora continua del software y la satisfacción del usuario final[cite: 180].

| Tipo | ID | Requerimiento Clave | Justificación |
| :--- | :--- | :--- | :--- |
| **Funcional** | RF-05 | [cite_start]**Validación de Datos:** Asegurar que los montos sean numéricos y positivos[cite: 103, 135]. | Mantenimiento Correctivo |
| **Funcional** | RF-06 | [cite_start]**Almacenamiento Persistente:** Uso de base de datos local (ej. SQLite) para conservación de registros[cite: 115, 201]. | Mantenimiento Preventivo |
| **No Funcional** | RNF-04 | [cite_start]**Multiplataforma (PWA):** Adaptación del sistema para ser accesible desde dispositivos móviles y tablets[cite: 116, 162]. | Mantenimiento Adaptativo |

---

## 🧪 Tabla de Pruebas Funcionales (Extracto)

Se adjunta el documento `PlanPruebas.docx` en la carpeta `/pruebas`.

| ID de Prueba | Requerimiento | Descripción del Caso | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **PC-001** | RF-05 | Verificar la validación de un monto negativo en un gasto. | El sistema debe **rechazar** el registro y mostrar una advertencia. |
| **PC-003** | RF-06 | Comprobar que los datos se conservan al cerrar y reabrir la aplicación. | Los registros y el Balance Total deben persistir sin cambios. |

## 🔄 Reflexión sobre el Control de Versiones (Git/GitHub)

[cite_start]El control de versiones es vital para la documentación técnica, ya que permite[cite: 181]:

* **Trazabilidad:** Registrar la evolución de los requisitos (DRS v1 a v2) y la propuesta de mantenimiento.
* **Colaboración:** Facilitar que el equipo trabaje en paralelo en diferentes entregables.
* **Recuperación:** Volver a versiones estables anteriores en caso de errores en la documentación o el código.

El uso de **mensajes de commit claros** (como "Adición de documentos de requerimientos v1 y v2") es fundamental para conectar cada cambio con su contexto y propósito en el ciclo de mantenimiento.
