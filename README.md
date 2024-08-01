import random

# تعريف بعض الخصائص العشوائية للمود
def generate_random_mod():
    colors = ['Red', 'Green', 'Blue', 'Yellow']
    shapes = ['Circle', 'Square', 'Triangle']
    speeds = [1, 2, 3, 4]

    mod = {
        'color': random.choice(colors),
        'shape': random.choice(shapes),
        'speed': random.choice(speeds),
    }

    return mod

# إنشاء المود العشوائي
random_mod = generate_random_mod()

# حفظ المود في ملف JSON
import json

with open('random_mod.json', 'w') as file:
    json.dump(random_mod, file, indent=4)

print('Mod generated and saved as random_mod.json')
