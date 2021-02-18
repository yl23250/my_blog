## YS退货方案探讨

### 需求场景

​		医疗行业，监管要求，允许存在三方仓库存托管业务场景，所谓三方仓的库存托管即实物的出入库都在三方仓已经操作完毕。

​		对于医疗检验行业，三方仓更是常态。实际的库存操作记录都在三方仓WMS执行完毕，但需要做存货核算，所以需要把三方仓操作结果回传到YS。YS需要记录库存变动痕迹，进行开票、受票。

![image-20210203173715029](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203173715029.png)



### 实际对接情况

目前YS的退货流程，只考虑了手工库存管理的流程；

> 业务系统中的出入库单据对接YS2张单据，三个步骤；

step1. 对接【销售退货单】已确认状态；

step2. 关联销售退货单，对接【红字出库单】；

step3. 对接【销售退货单】已审核状态；

因为单据是在YS生成，dsrp接口服务无法保证事物一致性

![image-20210203174806217](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203174806217.png)

### 期望对接方案

![image-20210203180641981](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203180641981.png)
基于医疗检验行业的实际业务场景，期望用友老师能够支持对接过程中，一单捅到底，实现单据之间的流程自动化。
