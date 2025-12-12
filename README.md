import random
import math

class ImprovedRandomWalker2D:
    """
    Класс, представляющий точку, совершающую случайное блуждание в 2D. 
    Включает расчет пройденного расстояния.
    """
    def __init__(self, start_x=0.0, start_y=0.0):
        """Инициализация точки в заданных начальных координатах."""
        self.start_x = start_x
        self.start_y = start_y
        self.x = start_x
        self.y = start_y
        self.total_distance = 0.0  # Общее пройденное расстояние
        self.history = [(self.x, self.y)]

    def _calculate_distance(self, x1, y1, x2, y2):
        """Вычисляет Евклидово расстояние между двумя точками."""
        # Используем формулу расстояния: d = sqrt((x2 - x1)^2 + (y2 - y1)^2)
        return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)

    def make_random_step(self, max_distance=5):
        """
        Совершает случайный шаг, обновляя координаты и общее пройденное расстояние.
        """
        old_x, old_y = self.x, self.y
        
        # Случайное изменение по X и Y (могут быть не целыми числами для точности)
        # random.uniform возвращает float
        delta_x = random.uniform(-max_distance, max_distance)
        delta_y = random.uniform(-max_distance, max_distance)
        
        self.x += delta_x
        self.y += delta_y
        
        # Расчет расстояния, пройденного на этом шаге
        step_distance = self._calculate_distance(old_x, old_y, self.x, self.y)
        self.total_distance += step_distance
        
        self.history.append((self.x, self.y))
        
        # Возвращаем текущие координаты и расстояние, пройденное на шаге
        return (self.x, self.y, step_distance)

    def reset(self):
        """Сбрасывает симуляцию в начальные координаты."""
        self.x = self.start_x
        self.y = self.start_y
        self.total_distance = 0.0
        self.history = [(self.x, self.y)]
        print("\nСимуляция сброшена до начальной точки.")

# --- Основная часть программы ---

NUM_STEPS = random.randint(5, 12)
MAX_STEP_SIZE = random.randint(3, 8)

walker = ImprovedRandomWalker2D(start_x=0.0, start_y=0.0)

print(f"--- 📈 УЛУЧШЕННЫЙ СИМУЛЯТОР СЛУЧАЙНОГО БЛУЖДАНИЯ (2D) ---")
print(f"Начало: ({walker.start_x}, {walker.start_y}) | Шагов: {NUM_STEPS} | Макс. шаг: +/- {MAX_STEP_SIZE:.1f}")
print("-" * 65)

for i in range(NUM_STEPS):
    x, y, dist = walker.make_random_step(MAX_STEP_SIZE)
    # Используем f-строки для красивого форматирования
    print(f"| Шаг {i+1:2d} | Координаты: ({x:8.3f}, {y:8.3f}) | Дистанция шага: {dist:6.3f} |")

# --- Результаты ---

final_x, final_y = walker.history[-1]
# Расстояние от начальной точки
distance_from_start = walker._calculate_distance(walker.start_x, walker.start_y, final_x, final_y)

print("-" * 65)
print(f"**ИТОГО:**")
print(f"   Финальные координаты: ({final_x:.3f}, {final_y:.3f})")
print(f"   Пройденное расстояние (общее): {walker.total_distance:.3f}")
print(f"   Расстояние от старта (по прямой): {distance_from_start:.3f}")
print("-" * 65)

# Демонстрация метода сброса
walker.reset()
