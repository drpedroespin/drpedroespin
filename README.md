import pygame
import sys

# Inicializar Pygame
pygame.init()

# Definir dimensiones de la pantalla
SCREEN_WIDTH = 800
SCREEN_HEIGHT = 600
screen = pygame.display.set_mode((SCREEN_WIDTH, SCREEN_HEIGHT))
pygame.display.set_caption("Avatar Simple")

# Colores
WHITE = (255, 255, 255)
BLACK = (0, 0, 0)

# Definir posición y tamaño del avatar
avatar_x = 400
avatar_y = 300
avatar_width = 50
avatar_height = 50

# Loop principal
while True:
    # Manejo de eventos
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    # Dibujar el fondo
    screen.fill(WHITE)

    # Dibujar el avatar
    pygame.draw.rect(screen, BLACK, (avatar_x, avatar_y, avatar_width, avatar_height))

    # Actualizar la pantalla
    pygame.display.flip()

    # Control de la velocidad de la animación
    pygame.time.Clock().tick(60)
--->
