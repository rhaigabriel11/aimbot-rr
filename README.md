def aimbot(player, enemies):
    for enemy in enemies:
        if is_visible(player, enemy):  # Verifica se o inimigo está visível
            angle = calculate_aim_angle(player, enemy)  # Calcula o ângulo de mira
            smooth_aim(player, angle)  # Ajusta a mira suavemente
            break  # Mira no primeiro inimigo visível
def esp(player, objects):
    for obj in objects:
        if is_in_range(player, obj):  # Verifica se o objeto está no alcance
            draw_box(obj.position)  # Desenha uma caixa ao redor do objeto
            draw_text(obj.name, obj.position)  # Exibe o nome do objeto
