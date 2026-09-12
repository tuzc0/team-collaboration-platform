# Definition of Done

Una tarea, requisito, issue o incremento solo podrá considerarse **terminado** cuando cumpla los criterios aplicables de esta lista.

---

## 1. Funcionalidad

- [ ] El requisito fue implementado.
- [ ] Los criterios de aceptación fueron cumplidos.
- [ ] Los casos de error relevantes fueron considerados.
- [ ] El comportamiento esperado fue validado.

---

## 2. Código

- [ ] El código compila o construye correctamente.
- [ ] El código fue formateado con las herramientas acordadas.
- [ ] No existe código comentado innecesario.
- [ ] No existen duplicaciones importantes.
- [ ] Los nombres de clases, funciones, variables y módulos son comprensibles.
- [ ] El cambio respeta la arquitectura definida.
- [ ] No se introdujo complejidad innecesaria.

---

## 3. Pruebas

- [ ] Se agregaron pruebas cuando corresponde.
- [ ] Las pruebas unitarias son exitosas.
- [ ] Las pruebas de integración son exitosas cuando aplica.
- [ ] Las pruebas de contrato son exitosas cuando aplica.
- [ ] Las pruebas end-to-end son exitosas cuando aplica.
- [ ] No se rompieron pruebas existentes.

---

## 4. Seguridad

- [ ] No se añadieron secrets al repositorio.
- [ ] Los datos sensibles se manejan correctamente.
- [ ] Se verifican autenticación y autorización cuando corresponde.
- [ ] Se validan entradas externas.
- [ ] No se almacenan contraseñas en texto plano.
- [ ] No se exponen datos sensibles en logs.
- [ ] No se introdujeron vulnerabilidades críticas conocidas.

---

## 5. API y contratos

- [ ] La documentación de API fue actualizada cuando corresponde.
- [ ] OpenAPI fue actualizado cuando corresponde.
- [ ] Los eventos WebSocket fueron documentados cuando corresponde.
- [ ] Los cambios de contrato fueron comunicados.
- [ ] Se revisó el impacto sobre escritorio y móvil.

---

## 6. Base de datos

- [ ] Las migraciones o scripts están incluidos cuando corresponde.
- [ ] Los cambios son reproducibles.
- [ ] No se requiere modificación manual no documentada.
- [ ] Los índices y relaciones necesarios fueron considerados.
- [ ] Los datos persistentes se mantienen después de recrear contenedores.

---

## 7. Docker e infraestructura

- [ ] El contenedor construye correctamente cuando corresponde.
- [ ] Docker Compose continúa funcionando.
- [ ] Los servicios afectados pueden comunicarse.
- [ ] No existen secrets dentro de la imagen.
- [ ] No se expusieron puertos innecesarios.
- [ ] Los volúmenes funcionan correctamente.

---

## 8. Documentación

- [ ] README fue actualizado cuando corresponde.
- [ ] La documentación técnica fue actualizada.
- [ ] La documentación de arquitectura fue actualizada cuando aplica.
- [ ] Se creó o modificó un ADR cuando la decisión es arquitectónica.

---

## 9. Integración

- [ ] La Pull Request fue creada.
- [ ] El Code Review fue completado.
- [ ] No existen comentarios críticos pendientes.
- [ ] CI es exitoso.
- [ ] La rama está actualizada respecto a `main`.

---

## 10. Validación final

- [ ] El cambio fue probado por al menos una persona distinta al autor cuando sea posible.
- [ ] No existen errores críticos conocidos sin documentar.
- [ ] La funcionalidad está lista para integrarse.
- [ ] El issue puede cerrarse.

---

## Regla final

Una tarea no se considera terminada únicamente porque:

> “Funciona en mi computadora.”
