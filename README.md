# python监控azkaban执行日志，并发送信息到企业微信
使用python监控azkaban，使用官方提供的接口，解析日志，当执行次数或执行时间不达标，通过企业微信发送发送到微信群中；

利用impala获取到我们所需要监控的项目，包含 project_name,flow_name,job_name，监控的对象包含整个工作流：project/flow 也可能是 某个重要工作节点
官方提供的方法只能获取到 project/flow 级别的日志，无法获取到具体的 job 级日志

利用mysql获取值班人，将报警信息@到值班人，如果没有这个需求，可以把mysql相关代码删除

执行频率通过corntab实现

--最近才开始写，目前开发中：2022/6/9
