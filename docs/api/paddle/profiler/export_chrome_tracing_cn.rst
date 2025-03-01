.. _cn_api_profiler_export_chrome_tracing:

export_chrome_tracing
---------------------

.. py:function:: paddle.profiler.export_chrome_tracing(dir_name: str, worker_name: Optional[str]=None)

该接口返回一个回调函数，用于将采集的性能数据保存到google chrome tracing格式的文件。
输出的文件将会保存在目录 ``dir_name`` 中， 文件名的前缀将会被设置成 ``worker_name`` 。
如果 ``worker_name`` 没有被设置，默认名字为 [hostname]_[pid]。

参数
:::::::::

    - **dir_name** (str) - 性能数据导出所保存到的文件夹路径。
    - **worker_name** (str, 可选) - 性能数据导出所保存到的文件名前缀，默认是[hostname]_[pid]。

返回
:::::::::

回调函数（callable), 该函数会接收一个参数prof(Profiler对象），调用prof的export方法保存采集到的性能数据到chrome tracing文件。

代码示例
::::::::::

用于 :ref:`性能分析器 <cn_api_profiler_profiler>` 的on_trace_ready参数。

COPY-FROM: paddle.profiler.export_chrome_tracing:code-example1