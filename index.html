import pygame
import math
import random

# Initialize Pygame
pygame.init()

# Set up display
WIDTH, HEIGHT = 800, 600
win = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Archery Game")

# Colors
WHITE = (255, 255, 255)
BLACK = (0, 0, 0)
RED = (255, 0, 0)
GREEN = (0, 255, 0)
BLUE = (0, 0, 255)

# Game Variables
target_pos = (random.randint(100, 700), random.randint(100, 500))
target_radius = 50
arrow_speed = 10
arrow_angle = 0
arrow_pos = (WIDTH // 2, HEIGHT)
is_shooting = False
arrows_left = 10
score = 0

# Load arrow image
arrow_img = pygame.image.load('arrow.png')
arrow_img = pygame.transform.scale(arrow_img, (50, 10))

def draw_target(win, pos, radius):
    """Draw the target on screen"""
    pygame.draw.circle(win, RED, pos, radius)
    pygame.draw.circle(win, WHITE, pos, radius - 10)
    pygame.draw.circle(win, BLUE, pos, radius - 30)

def calculate_score(hit_pos, target_pos, radius):
    """Calculate score based on distance from center of target"""
    dist = math.dist(hit_pos, target_pos)
    if dist <= radius:
        return max(10 - int(dist / radius * 10), 0)
    return 0

def main():
    global is_shooting, arrow_angle, arrow_pos, score, arrows_left

    clock = pygame.time.Clock()
    run = True

    while run:
        clock.tick(60)
        win.fill(WHITE)

        # Draw target
        draw_target(win, target_pos, target_radius)

        # Aim with mouse
        mouse_x, mouse_y = pygame.mouse.get_pos()
        arrow_angle = math.atan2(mouse_y - arrow_pos[1], mouse_x - arrow_pos[0])

        # Draw the arrow
        if not is_shooting:
            arrow_rotated = pygame.transform.rotate(arrow_img, -math.degrees(arrow_angle))
            win.blit(arrow_rotated, arrow_pos)
        else:
            arrow_pos = (arrow_pos[0] + arrow_speed * math.cos(arrow_angle),
                         arrow_pos[1] + arrow_speed * math.sin(arrow_angle))
            arrow_rotated = pygame.transform.rotate(arrow_img, -math.degrees(arrow_angle))
            win.blit(arrow_rotated, arrow_pos)

            # Check if the arrow hits the target
            if math.dist(arrow_pos, target_pos) <= target_radius:
                score += calculate_score(arrow_pos, target_pos, target_radius)
                is_shooting = False
                arrows_left -= 1
                arrow_pos = (WIDTH // 2, HEIGHT)

            # Reset arrow if out of bounds
            if arrow_pos[0] > WIDTH or arrow_pos[1] > HEIGHT:
                is_shooting = False
                arrows_left -= 1
                arrow_pos = (WIDTH // 2, HEIGHT)

        # Display score and arrows left
        font = pygame.font.SysFont(None, 36)
        score_text = font.render(f"Score: {score}", True, BLACK)
        arrows_text = font.render(f"Arrows Left: {arrows_left}", True, BLACK)
        win.blit(score_text, (10, 10))
        win.blit(arrows_text, (10, 50))

        # Check for game over
        if arrows_left == 0:
            game_over_text = font.render(f"Game Over! Final Score: {score}", True, BLACK)
            win.blit(game_over_text, (WIDTH // 2 - 150, HEIGHT // 2))
            pygame.display.update()
            pygame.time.wait(3000)
            run = False

        pygame.display.update()

        # Handle events
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                run = False
            if event.type == pygame.MOUSEBUTTONDOWN and not is_shooting:
                is_shooting = True

    pygame.quit()

if __name__ == "__main__":
    main()
