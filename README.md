# Zhalgas-Practice_SRO-12
import pandas as pd
import numpy as np

data = pd.read_csv('data.csv')

percentiles = np.percentile(data['Score'], [25, 50, 75])

print(f"25-й процентиль: {percentiles[0]}")
print(f"50-й процентиль (медиана): {percentiles[1]}")
print(f"75-й процентиль: {percentiles[2]}")

median = np.percentile(data['Score'], 50)
above_median = data[data['Score'] > median]
percentage_above_median = (len(above_median) / len(data)) * 100
print(f"Доля студентов с оценками выше медианы: {percentage_above_median}%")


import pandas as pd
import numpy as np

# Создаем пример данных
data = {
    'Weight': np.random.normal(70, 10, 100),
    'Height': np.random.normal(170, 5, 100),
    'Age': np.random.randint(18, 60, 100)
}

# Создаем DataFrame
health_data = pd.DataFrame(data)

# Сохраняем DataFrame в CSV файл
health_data.to_csv('data.csv', index=False)

# Выводим первые строки DataFrame для проверки
print(health_data.head())
