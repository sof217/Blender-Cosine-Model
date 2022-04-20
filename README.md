# Blender-Mathematical-Modelling
Blender Script Practice
#here is the code - I slightly modified the code given on prosperocode's website. 

import bpy
from math import cos, pi

pink = bpy.data.objects['pink']

frame_number = 0

for i in range(0, 101):
  bpy.context.scene.frame_set(frame_number)
  xp = i/4 * pi
  yp = 10 + cos(xp) * 2
  zp = cos(xp) * 10
  pink.location = (xp, yp, zp)
  pink.keyframe_insert(data_path='location', index=-1)
  frame_number += 5
