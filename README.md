That's part of .ipynb that converts human motion video to .bvh. More info here: https://github.com/Dene33/video_to_bvh

The line 194 of demo.py has been changed into "all_files.sort(key=lambda x: x.split('/')[-1].split('.')[0])" from "all_files.sort(key=lambda x: int(x.split('/')[-1].split('.')[0]))" in order to solve the ValueError issue as listed below:


File "hmr/demo.py", line 194, in

all_files.sort(key=lambda x: int(x.split('/')[-1].split('.')[0]))

ValueError: invalid literal for int() with base 10: 'abc002'
