# DEEPSTREAM SDK
 This contains all the details collected from the NVIDIA DOCs pertaining to the deepstream application.
## Deepstream app
This is comprised of various gstreamer elements working together for a hardware accelerated video processing and analytics.
 - GST-NVSTREAMMUX : It forms batches of frames that are to be analysed from various input streams.
 - GST-NVDSPREPROCESS : preprocessing on the pre-defined ROIs for primary inferencing.
 - GST-NVINFER : It is an NVIDIA TensorRT based plugin. It does primary detection and secondary classification of the objects.
 - GST-NVTRACKER : It is an open-cv based plugin for tracking the objects. It uses the output from the gst-nvinfer.It will track an object with a unique ID.
 - GST-NVMULTISTREAMTILER : It will help in forming 2D array of frames.
 - GST-NVDSOSD : The Onscreen Display (OSD) plugin is used to draw shaded boxes, rectangles and text on the composited frame using the generated metadata.
 - GST-NVMSGCONV AND GST-NVMSGBROKER : The Message Converter (Gst-nvmsgconv) and Message Broker (Gst-nvmsgbroker) plugins in combination to send analytics data to a server in the Cloud.
 
A configuration file is used along with nvinfer, for keeping the configurations ready for the model.
Another configuration file is kept for updating the configuration of each of the caps of the gst elements.






