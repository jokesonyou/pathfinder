I implemented a convert_image_to_grid_map function that takes in an image, reads it as grayscale and then inverts the resulting array so that all numbers are either 0 or 1 (The image is already black and white when read so the values are either 0 or 255).

After inverting, we would get an array (100x100 in the case of the image I had) of 0 and 1s where 1 is an obstacle and 0 is an array.

Using np.where() I can get the coordinates of the obstacles and then save them as lists (ox, oy) and feed them to the algorithm.

I tried using another map so I implemented a small loop in the main of the D* algorithm, where it uses one path at a time. Each figure represents a map.
