.. _cn_api_profiler_profilertarget:

ProfilerTarget
---------------------

.. py:class:: paddle.profiler.ProfilerTarget


ProfilerTarget枚举类用来指定 :ref:`性能分析 <cn_api_profiler_profiler>` 的设备。目前仅支持CPU和GPU。

设备说明如下：
    - **ProfilerTarget.CPU** - 性能分析对象为CPU上的活动
    - **ProfilerTarget.GPU**  - 性能分析对象为GPU上的活动