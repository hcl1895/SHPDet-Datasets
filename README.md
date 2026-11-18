# SHPDet datasets

VOC-FOG, VOC-RAIN and VOC-DARK for adverse-weather object detection.

| Dataset | Training images | Test images |
| --- | ---: | ---: |
| VOC-FOG | 9,578 | 2,129 |
| VOC-RAIN | 9,578 | 2,129 |
| VOC-DARK | 9,578 | 2,129 |

Download the train/test ZIPs from [Releases](https://github.com/hcl1895/SHPDet-Datasets/releases/tag/v1.0) and extract them into the same directory. Each split includes degraded images (`JPEGImages`), paired clean images (`JPEGImages_clean`), original VOC XML annotations (`Annotations`), and a five-class detection manifest (`labels.txt`). Image dimensions and filenames are preserved. The three datasets retain the original train/test image-ID lists from the TogetherNet VOC-FOG release.

The class order is `person, bicycle, car, motorbike, bus`. Each manifest line is `image_path xmin,ymin,xmax,ymax,class_id ...`; coordinates retain the VOC annotation values. The manifest selects these five classes and excludes difficult objects. XML files retain the original VOC labels.

VOC-FOG retains the existing fog images. VOC-RAIN adds procedural rain streaks to the fog images. VOC-DARK applies brightness scaling and a gamma transform to the paired clean images. Parameters are in `generation_config.json`; per-image parameters are included in each generated split. Archive checksums are listed in `SHA256SUMS`.

## Sources

Images and annotations originate from [PASCAL VOC](https://www.robots.ox.ac.uk/~vgg/projects/pascal/VOC/); the five-class VOC-FOG setting follows [TogetherNet](https://github.com/yz-wang/TogetherNet). Original image rights and the VOC database terms continue to apply.

Please cite PASCAL VOC (Everingham et al., IJCV 2010, DOI: 10.1007/s11263-009-0275-4) and TogetherNet (Wang et al., Computer Graphics Forum 2022, DOI: 10.1111/cgf.14692) when using these resources.
