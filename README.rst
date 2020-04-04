shadertoy-render
================

.. image:: docs/example.jpg
	:target: https://youtu.be/GAauIQFHaZs

A simple Python script that uses ``ffmpeg`` as a subprocess to render ShaderToy scripts into video files.  After grabbing the file from the repository, you can run it as follows:

	> python shadertoy-render.py example.glsl example.mp4

Command-line arguments are documented with the ``-h`` switch, for example:

* ``--size`` — Resolution of the render window, for example ``1920x1080``.
* ``--duration`` — Total length of the output video in seconds, e.g. ``45.0``.
* ``--rate`` — Number of frames per second used during rendering, e.g. ``60``.
* ``--verbose`` — Show the full output of ``ffmpeg`` in verbose mode.

Example of more advanced usage:

	> python shadertoy-render.py in.glsl out.mp4 --size=1920x1080 --rate=60 --duration=120.0

It should run on Linux and OSX where ``ffmpeg`` is in the path, on Windows with minor changes assuming the binary is found.  Python dependencies include `numpy`, `vispy` and `watchdog`, which you can install them with PIP as follows:

    > pip install numpy vispy watchdog

The output is a MP4 file with default encoding settings, which you can upload to YouTube for example.  See the source code for details!

1. `Source ShaderToy <https://www.shadertoy.com/view/4sB3D1>`_ script by Inigo Quilez.

2. `Rendered Video <https://youtu.be/GAauIQFHaZs>`_ at 1080p uploaded to YouTube.

Feedback or comments are welcome; just submit a ticket or follow `@alexjc <https://twitter.com/alexjc>`_ on Twitter.
