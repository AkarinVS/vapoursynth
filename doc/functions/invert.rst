Invert
======

.. function:: Invert(clip clip[, int[] planes=[0, 1, 2]])
   :module: std

   Inverts the pixel values. Specifically, it subtracts the value of the
   input pixel from the format's maximum allowed value.

   Because U/V planes in floating point YUV masks use the [0,1.0] range,
   not the usual [-0.5,0.5] range for video clips, Invert can not be
   used to invert floating point YUV masks.

   *clip*
      Clip to process. It must have integer sample type and bit depth
      between 8 and 16, or float sample type and bit depth of 32. If
      there are any frames with other formats, an error will be
      returned.

   *planes*
      Specifies which planes will be processed. Any unprocessed planes
      will be simply copied.
