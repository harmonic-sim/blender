# code used to add keyframes to blender

import bpy
from time import sleep

frames = len(bpy.data.collections['Collection 2'].all_objects)

for i in range(frames):
    obj = bpy.data.collections['Collection 2'].all_objects[i]
    
    obj.hide_render = True 
    obj.hide_viewport = True
    obj.keyframe_insert(data_path="hide_render", frame=0)
    obj.keyframe_insert(data_path="hide_viewport", frame=0)
    
    obj.hide_render = False 
    obj.hide_viewport = False
    obj.keyframe_insert(data_path="hide_render", frame=i)
    obj.keyframe_insert(data_path="hide_viewport", frame=i)
    
    if i < (frames - 1):
        obj.hide_render = True 
        obj.hide_viewport = True
        obj.keyframe_insert(data_path="hide_render", frame=i+1)
        obj.keyframe_insert(data_path="hide_viewport", frame=i+1)
    
    print(i)
    sleep(0.1)

print("done")
