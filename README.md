# GAME DESIGN DOCUMENT (GDD)
## "CiclonShooter" - Shooter Multijugador 2D

### 1. INFORMACIÓN GENERAL

**Título:** CiclonShooter  
**Género:** Shooter multijugador 2D  
**Plataforma:** PC (Godot 4.4)  
**Modo:** Multijugador local/online  
**Público objetivo:** Jugadores casuales, amigos  
**Duración estimada:** Partidas de 5-15 minutos  
**Desarrollador:** CiclonSoft  

### 2. CONCEPTO DEL JUEGO

**Visión general:**
Un shooter multijugador 2D rápido y frenético donde hasta 4 jugadores compiten en mapas pequeños con una gran variedad de armas. El objetivo es ser el último en pie mediante combate directo, usando armas cuerpo a cuerpo, a distancia y explosivas.

**Mecánica principal:**
- Combate multijugador en tiempo real
- Sistema de armas variado (melee, rango, explosivas)
- Mapas pequeños para acción constante
- Controles simples y accesibles

### 3. MECÁNICAS DE JUEGO

#### 3.1 Controles Básicos
- **WASD / Flechas:** Movimiento
- **Mouse:** Apuntar
- **Click Izquierdo:** Disparar/Atacar
- **Click Derecho:** Arma especial/Alternativa
- **R:** Recargar (armas de rango)
- **E:** Interactuar/Recoger arma
- **1-4:** Cambiar arma rápida

#### 3.2 Sistema de Combate
- **Vida:** 100 HP por defecto
- **Regeneración:** 1 HP por segundo después de 3 segundos sin daño
- **Daño:** Varía según arma (5-50 HP)
- **Respawn:** 3 segundos en ubicación aleatoria del mapa

#### 3.3 Tipos de Armas

**ARMAS MELEE:**
- **Espada:** Daño 25, Rango corto, Velocidad media
- **Mazo:** Daño 35, Rango corto, Velocidad lenta, knockback
- **Cuchillo:** Daño 15, Rango muy corto, Velocidad muy rápida
- **Lanza:** Daño 30, Rango medio-largo, Velocidad media

**ARMAS DE RANGO:**
- **Pistola:** Daño 20, Rango largo, Velocidad rápida, 12 balas
- **Rifle:** Daño 30, Rango muy largo, Velocidad media, 30 balas
- **Escopeta:** Daño 40 (por perdigón), Rango corto, 8 balas
- **Francotirador:** Daño 50, Rango extremo, Velocidad lenta, 5 balas

**ARMAS EXPLOSIVAS:**
- **Granada:** Daño 40, Radio 3 metros, Delay 3 segundos
- **RPG:** Daño 60, Radio 2 metros, 3 cohetes
- **Bomba adhesiva:** Daño 35, Radio 2 metros, Se pega a superficies
- **Mina:** Daño 30, Radio 1.5 metros, Se activa al pisar

### 4. MAPAS Y AMBIENTACIÓN

#### 4.1 Mapas Principales
1. **Arena Central:** Mapa circular con obstáculos en el centro
2. **Laboratorio:** Mapa rectangular con pasillos estrechos
3. **Playa:** Mapa abierto con pocos obstáculos
4. **Fábrica:** Mapa industrial con múltiples niveles
5. **Nave Espacial:** Mapa futurista con gravedad cero (mecánica especial)

#### 4.2 Elementos del Mapa
- **Obstáculos destructibles:** Cajas, barriles
- **Obstáculos indestructibles:** Paredes, columnas
- **Power-ups:** Escudo temporal, velocidad, daño extra
- **Puntos de spawn:** Ubicaciones fijas para respawn

### 5. MODOS DE JUEGO

#### 5.1 Modo Principal: "Battle Royale"
- 2-4 jugadores
- Último en pie gana
- Armas aparecen aleatoriamente en el mapa
- Zona de combate se reduce gradualmente

#### 5.2 Modo "Team Deathmatch"
- 2 equipos de 2 jugadores
- Primer equipo en llegar a 50 eliminaciones gana
- Respawn inmediato

#### 5.3 Modo "King of the Hill"
- Controlar punto central del mapa
- Puntos por tiempo de control
- Primer jugador en 100 puntos gana

### 6. SISTEMA DE PROGRESIÓN

#### 6.1 Desbloqueables
- Nuevas armas
- Skins de personajes
- Efectos visuales
- Mapas adicionales

#### 6.2 Estadísticas
- Eliminaciones totales
- Muertes
- Tiempo jugado
- Arma favorita
- Mejor racha

### 7. ARTE Y AUDIO

#### 7.1 Estilo Visual
- **Estilo:** Pixel art moderno
- **Resolución:** 1920x1080 (escalable)
- **Paleta de colores:** Vibrante y contrastante
- **Efectos:** Partículas para explosiones, sangre, humo

#### 7.2 Personajes
- **Diseño:** Siluetas distintivas y coloridas
- **Diferenciación:** Colores únicos por jugador
- **Animaciones:** Movimiento fluido, idle, ataque, muerte

#### 7.3 Audio
- **Música:** Tracks electrónicos energéticos
- **SFX:** Disparos, explosiones, pasos, gritos
- **Ambiental:** Sonidos del mapa (máquinas, viento, etc.)

### 8. INTERFAZ DE USUARIO

#### 8.1 HUD Principal
- Barra de vida (esquina superior izquierda)
- Arma actual (esquina inferior derecha)
- Munición (debajo del arma)
- Minimapa (esquina superior derecha)
- Contador de jugadores vivos (centro superior)

#### 8.2 Menús
- **Menú Principal:** Jugar, Configuración, Salir
- **Lobby:** Selección de modo, configuración de partida
- **Pausa:** Reanudar, Configuración, Salir al menú
- **Resultados:** Estadísticas de la partida, Próxima ronda

### 9. CONFIGURACIÓN TÉCNICA

#### 9.1 Requisitos Mínimos
- **OS:** Windows 10
- **RAM:** 4GB
- **GPU:** DirectX 11 compatible
- **Espacio:** 500MB

#### 9.2 Controles
- **Teclado + Mouse:** Configuración completa
- **Gamepad:** Soporte para Xbox/PlayStation
- **Personalización:** Teclas rebindables

### 10. PLAN DE DESARROLLO

#### Fase 1: Prototipo (2-3 semanas)
- [ ] Movimiento básico del personaje
- [ ] Sistema de armas simple (1 melee, 1 rango, 1 explosiva)
- [ ] Mapa básico
- [ ] Sistema de vida y daño

#### Fase 2: Multijugador (2-3 semanas)
- [ ] Networking básico
- [ ] Sincronización de jugadores
- [ ] Sistema de respawn
- [ ] Lobby de partida

#### Fase 3: Contenido (3-4 semanas)
- [ ] Todas las armas implementadas
- [ ] 3-4 mapas completos
- [ ] Modos de juego
- [ ] UI/UX completa

#### Fase 4: Pulido (2-3 semanas)
- [ ] Balanceo de armas
- [ ] Efectos visuales y audio
- [ ] Optimización
- [ ] Testing y bugs

### 11. CONSIDERACIONES DE BALANCEO

#### 11.1 Armas Melee
- **Ventaja:** No necesitan munición, daño consistente
- **Desventaja:** Rango limitado, riesgo alto

#### 11.2 Armas de Rango
- **Ventaja:** Rango seguro, daño controlado
- **Desventaja:** Munición limitada, tiempo de recarga

#### 11.3 Armas Explosivas
- **Ventaja:** Daño en área, efecto devastador
- **Desventaja:** Munición muy limitada, riesgo de autodaño

### 12. MÉTRICAS DE ÉXITO

- **Tiempo de partida promedio:** 5-10 minutos
- **Retención:** 80% de jugadores completan al menos 3 partidas
- **Satisfacción:** 4.5/5 en diversión percibida
- **Accesibilidad:** Nuevos jugadores pueden jugar en menos de 2 minutos

---

## NOTAS DE DESARROLLO

Este GDD es un documento vivo que se actualizará durante el desarrollo. Las mecánicas pueden ajustarse basándose en testing y feedback de jugadores.

**Próximos pasos:**
1. Configurar la estructura básica del proyecto en Godot
2. Implementar el sistema de movimiento del personaje
3. Crear el primer prototipo de combate
4. Testear con amigos para validar la diversión

---

*Documento creado para CiclonSoft - Primer juego multijugador*
