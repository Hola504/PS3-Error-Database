# Tipos de Errores y Fallos en PS3 / RPCS3 y como causarlos

Una recopilación de errores comunes, bricks y glitches que pueden presentarse en consolas PlayStation 3 físicas y en el emulador RPCS3. Esta lista incluye causas conocidas y formas en que pueden ser simuladas o replicadas con fines educativos.

---

## BSOD (Blue Screen of Death)
- **Causa:** Corrupción del archivo `Xregistry.sys`.
- **Acción:**
  - Borra líneas de texto del archivo de respaldo: `dev_flash2/etc/backup/Xregistry.sys`
  - Borra el archivo original: `dev_flash2/etc/Xregistry.sys`

## BSOD Grave
- **Causa:** Archivo del sistema severamente dañado.
- **Acción:** Elimina `dev_flash/sys/external/libuserdata*.sprx`

## RSOD (Red Screen of Death)
- **RPCS3:** No ocurre.
- **PS3 real:** Borra `vsh.self` de `dev_flash/vsh/module`.

## "A serious error has occurred"
- **Causa:** Similar al RSOD.
- **Acción:** Corrompe `sys_init_osd.self` en la misma ruta del RSOD.
- **RPCS3:** Es imitable.

## "No se puede iniciar, no se encontró un disco duro apropiado"
- **PS3:** Quitar el HDD o SSD.
- **RPCS3:** Intenta corromper archivos relacionados con `dev_hdd0` (no siempre funciona).

## RSOD Grave
- **Causa:** Casi todos los archivos importantes (excepto XMB) están corruptos.
- **Nota:** Forma de obtención desconocida.

## "Los archivos del disco duro están corruptos y se recuperarán"
- **PS3:** Corrompe archivos en `dev_hdd0` o realiza un formateo erróneo.
- **RPCS3:** Borra completamente `dev_hdd0`.

## "Datos corruptos"
- **Acción:** Corrompe `EBOOT.BIN` de la aplicación deseada.

## YLOD (Yellow Light of Death)
- **Causa:** Fallo físico, generalmente por desoldado del CPU o GPU.
- **Nota:** No es simulable en RPCS3.

## GLOD (Green Light of Death)
- **Causa:** Similar al YLOD, pero menos grave.

## GARLOD (Green And Red Light of Death)
- **Causa:** Sobrecalentamiento extremo o fallo físico similar al YLOD.

## Semi Brick
- **Causa:** Fallo en actualización o corrupción leve.
- **Síntoma:** No se presenta error grave como "A serious error".

## Full Brick
- **Causa:** Acompañado de YLOD, GLOD, GARLOD u otros errores graves.
- **Síntoma:** No da video ni señal. Solo se recupera reflasheando la NOR/NAND.
- **Puede ir acompañado de:** BSOD.

## Glitches Visuales
- **Causa:** Archivos del sistema visuales faltantes o corruptos.
- **Síntomas:**
  - Fallos en XMB, wave, logo de inicio.
- **Para causar:** Borra archivos del XMB, wave, etc.

## Glitches Auditivos
- **Causa:** Archivos de audio del XMB corruptos o faltantes.
- **Para causar:**
  - En RPCS3: Instalar firmware 2.80 o menor.
  - En PS3: Borra archivos `.arc` del XMB o del inicio.

## "The disk must be formatted"
- **Causa:** Error durante un formateo anterior.
- **Para causar:** Formatea incorrectamente el HDD/SSD (con cuidado).

## Códigos de Error (800017, 8007E21G, etc.)
- **Causa común:**
  - Falta de RAPS.
  - No activación del HEN.
  - CFW roto.
- **Gravedad:** Varía según el código.

## Loop de Inicio (Boot Loop)
- **PS3:** Corromper archivos de `dev_flash` que afectan el XMB.
- **RPCS3:** Borra todos los archivos excepto `vsh.self`.

## Congelamientos
- **Causa:** Uso excesivo de RAM o CPU inestable.
- **También puede deberse a:** Plugins como PS3xPAD.

## Datos no compatibles
- **Ejemplo:** Usar discos de PS2 en modelos CECH(D-K) sin retrocompatibilidad.

## Error en la lectura del disco
- **Causas:**
  - Disco corrupto o mal grabado.
  - Formato no compatible.
  - Lector dañado.

## Sesión cerrada
- **Causa:** Cerrar sesión manualmente o encender el HEN por primera vez.

---

> **Nota:** Esta información es solo para fines educativos, pruebas controladas o conocimiento técnico. No se recomienda corromper intencionalmente archivos del sistema en consolas reales sin experiencia, ya que puede causar pérdida permanente de funcionalidad.
