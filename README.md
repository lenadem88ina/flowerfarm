# flowerfarm
class Plant:
    def __init__(self, name, growth_rate, water_needs, sun_needs, harvest_time, price):
        self.name = name
        self.growth_rate = growth_rate
        self.water_needs = water_needs
        self.sun_needs = sun_needs
        self.harvest_time = harvest_time
        self.price = price

class Plot:
    def __init__(self):
        self.plant = None
        self.growth_stage = 0
        self.water_level = 0
        self.sun_level = 0

class Farm:
    def __init__(self):
        self.plots = [Plot() for _ in range(10)]  # 10 участков
        self.water_level = 100
        self.sun_level = 100
        self.money = 100

    def update_plots(self):
        for plot in self.plots:
            if plot.plant:
                plot.growth_stage += plot.plant.growth_rate
                # ... (Проверка воды и света)
                # ... (Сбор урожая, если растение созрело)

# ... (Функции plant_seed(), harvest_plant(), water_plots(), buy_seed())
