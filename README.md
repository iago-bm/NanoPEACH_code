This repository contains the code referenced in the paper **Redundant Cross-Correlation for Drift Correction in SEM Nanoparticle Imaging**. A preprint will be published on arXiv shortly.

### Example usage

```py
test_series = ImgSeries("C:\\path\\to\\image\\folder", (0, 9)) # use the first 10 images from a given folder
test_series.gaussian_blur((13, 13)) # preprocess with 13x13 gaussian blur

# get the full shift graph
test_graph = ShiftGraph(test_series)
test_graph.get_full_graph()

# create and save overlay image
result = test_graph.get_overlay_image()
cv2.imwrite("test.png", result)
```
