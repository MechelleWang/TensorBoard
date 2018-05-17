# TensorBoard学习

TensorBoard 是用于可视化 TensorFlow 模型的训练过程的工具（the flow of tensors）

基本操作：

1、summary
在定义计算图的时候，在适当的位置加上一些 summary 操作。

2、merge
使用 tf.summary.merge_all 来将这些 summary 操作聚合成一个操作，由它来产生所有 summary 数据。

3、run
在没有运行的时候这些操作是不会执行任何东西的，仅仅是定义了一下而已。在运行（开始训练）的时候，我们需要通过 tf.summary.FileWriter() 指定一个目录来告诉程序把产生的文件放到哪。然后在运行的时候使用 add_summary() 来将某一步的 summary 数据记录到文件中。

https://i.imgur.com/TK5BIH4.png
