# Buoyant-Buns-Generative-Art
The code of a project to create an animation or visual of donuts falling onto a plate. 

import bpy 
import random
import math

donut_objects = [obj for obj in bpy.context.scene.objects if obj.name.startswith("donut")]

for obj in donut_objects:
    rotation_x = random.uniform(-math.pi, math.pi)
    rotation_y = random.uniform(-math.pi, math.pi)
    rotation_z = random.uniform(-math.pi, math.pi)

    obj.rotation_euler = (rotation_x, rotation_y, rotation_z)

min_height = 0.3
max_height = 0.5

for obj in donut_objects:
    obj.location.z = random.uniform(min_height, max_height)
