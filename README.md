# detectron2 (cbo remix)

FAIR's [Detectron 2](https://github.com/facebookresearch/detectron2) is phenomenal. I've forked it here so I can modify it and make it do what I want in inelegant (read: hacky) ways.

More information on the original project in the [original readme](README_OLD.md)

# Changes

1. Setting/disabling model threshold

## Setting/disabling model threshold

Model segmentation threshold was originally set in a default arg in a function hidden deep in the bowels of detectron. I've hacked in a property of `GeneralizedRCNN` which allows you to set the threshold. This could be set by a config file, but is useful as a property as it allows quickly changing the threshold on-the-fly.