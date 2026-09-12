---
name: Reporte de error
about: Reportar un comportamiento incorrecto o inesperado
title: "[BUG] "
labels: ["bug"]
assignees: []
---

# Reporte de error

## Módulo afectado

- [ ] Autenticación
- [ ] Usuarios
- [ ] Grupos
- [ ] Roles y permisos
- [ ] Proyectos
- [ ] Tareas
- [ ] Mensajería
- [ ] Reacciones
- [ ] Reuniones
- [ ] Notificaciones
- [ ] Archivos
- [ ] Cliente móvil
- [ ] Cliente escritorio
- [ ] Auth Service
- [ ] Core Service
- [ ] PostgreSQL
- [ ] Cassandra / ScyllaDB
- [ ] Redis
- [ ] MinIO
- [ ] Docker / infraestructura
- [ ] Otro

---

## Descripción del error

Explique qué está ocurriendo.

---

## Comportamiento esperado

¿Qué debería ocurrir?

---

## Comportamiento actual

¿Qué ocurre realmente?

---

## Pasos para reproducir

```text
1.
2.
3.
4.
```

---

## ¿El error es reproducible?

- [ ] Siempre
- [ ] Frecuentemente
- [ ] Algunas veces
- [ ] Una sola vez
- [ ] No se ha podido volver a reproducir

---

## Severidad

- [ ] Crítica — impide utilizar el sistema o compromete seguridad/datos.
- [ ] Alta — bloquea una funcionalidad importante.
- [ ] Media — existe una alternativa temporal.
- [ ] Baja — problema menor o visual.

---

## Impacto

- [ ] Pérdida de datos.
- [ ] Riesgo de seguridad.
- [ ] Servicio caído.
- [ ] Funcionalidad bloqueada.
- [ ] Rendimiento degradado.
- [ ] Error visual.
- [ ] Problema de sincronización.
- [ ] Problema de conectividad.
- [ ] Otro.

---

## Entorno

### Cliente

- [ ] Escritorio
- [ ] Móvil
- [ ] No aplica

Versión:

```text

```

### Sistema operativo

```text
Windows / Linux / Android / otro:
```

### Backend

```text
Versión / commit:
```

### Entorno de ejecución

- [ ] Desarrollo local
- [ ] Docker local
- [ ] VM Linux
- [ ] Integración
- [ ] Otro

---

## Servicios implicados

- [ ] Auth Service
- [ ] Core Service
- [ ] PostgreSQL
- [ ] Cassandra / ScyllaDB
- [ ] Redis
- [ ] MinIO
- [ ] Gateway
- [ ] Otro

---

## Logs relevantes

No incluir contraseñas, access tokens, refresh tokens, API keys ni secretos.

```text

```

---

## Mensajes de error

```text

```

---

## Evidencia

Agregar capturas, videos, request/response, logs o stack trace sanitizado.

---

## Request relacionado

```text
Método:
Endpoint:
Status:
Request ID:
Trace ID:
```

---

## Última versión conocida donde funcionaba

```text
Desconocida / versión:
```

---

## Cambio reciente relacionado

- [ ] Sí
- [ ] No
- [ ] Desconocido

Pull Request / commit relacionado:

```text

```

---

## Posible causa

```text

```

---

## Solución temporal

```text
No / describir.
```

---

## Criterios de resolución

- [ ] Ya no puede reproducirse mediante los pasos documentados.
- [ ] Existe una prueba que cubre el error cuando corresponde.
- [ ] No se produjeron regresiones.
- [ ] Las pruebas existentes continúan funcionando.
- [ ] El cambio pasó Code Review.
- [ ] CI es exitoso.

---

## Notas adicionales

```text

```
