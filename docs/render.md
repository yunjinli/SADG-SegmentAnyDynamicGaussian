# Render

### Render all

```
python render.py -m output/<DATASET>/<NAME> --load_mask_on_the_fly --load_image_on_the_fly --eval --load2gpu_on_the_fly --skip_train --iteration 30000 ## configure --multithread_save for faster processing when running on large-RAM machine
```

### Render with text prompt

```
python render.py -m output/<DATASET>/<NAME> --load_mask_on_the_fly --load_image_on_the_fly --eval --load2gpu_on_the_fly --skip_train --iteration 30000 --text_prompt "TEXT_PROMPT" ## configure --multithread_save for faster processing when running on large-RAM machine
```

### Render with cluster ID

When you click the object in the GUI. You can see which cluster IDs are segemented.

```
python render.py -m output/<DATASET>/<NAME> --load_mask_on_the_fly --load_image_on_the_fly --eval --load2gpu_on_the_fly --skip_train --iteration 30000 --segment_ids <1> <2> <...> ## configure --multithread_save for faster processing when running on large-RAM machine
```