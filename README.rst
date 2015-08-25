V4LCapture
==========

A PyQt5 application that provides a control view to a Video4Linux2 device.
Adjustable and saveable settings with the optional H.264/mpegts UDP multicast
streaming capability (provided by ffmpeg library).

libv4lcapture
=============

Backend to V4LCapture. It is the C interface to communicate with v4l2 device,
by means of ioctl calls.

Requirements
============

- ``python`` >= 3.4
  
  - ``setuptools`` >= 3.3
  - ``pyqt5`` >= 5.2.1

- ``ffmpeg`` >= N-72627-gb8c0cf7 (2.7)
  
  - ``libavutil`` >= 54.26.101
  - ``libavcodec`` >= 56.41.101
  - ``libavformat`` >= 56.34.100
  - ``libswscale`` >= 3.1.101

- ``libpolkit`` >= 0.105
  
  - ``pkexec`` >= 0.105

Installation
============

Execute in a terminal (``$`` means unpriviledged terminal and ``#`` means
priviledged):

.. code-block:: console

  $ ./configure [-d] [-p PREFIX]
  $ make
  # make install

In a client the ``add_route`` script is needed. To install (``$`` means
unpriviledged terminal and ``#`` means priviledged):

.. code-block:: console

  $ ./configure
  # make route

Uninstallation
==============

Execute in a terminal (``$`` means unpriviledged terminal and ``#`` means
priviledged):

.. code-block:: console

  # make uninstall
  # make clean
