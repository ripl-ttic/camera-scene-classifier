# camera_scene_classifier

Scene classifier based on object detections in the image space.


# Requirements

This ROS package requires:

- [darknet_ros_msgs](https://github.com/afdaniele/darknet_ros_msgs)


# Launch the real-time scene classifier

```
roslaunch camera_scene_classifier scene_classifier.launch config:=<path_to_JSON_config> [detections:=<detections_topic>]
```

NOTE:
- `<detections_topic>` has to be a topic of `darknet_ros_msgs/BoundingBoxes` messages.
- `<path_to_JSON_config>` is the path to a configuration file. Check the file `config.example.json` for further information. Make your own copy, change its content and pass it to the classifier as shown above.
