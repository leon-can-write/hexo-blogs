Draw call: 触发整个图形流水线的 API

uniform: 每次  Drawcall 的常量, texture 是一种特殊的 uniform

varying: 从顶点或者栅格化得到的数据，比如顶点位置



constant registers: uniform 的寄存器, 数量较多

temporary registers: 通用寄存器 （临时读写数据的空间, ScratchSpace)



intrinsic functions: 内建函数 (`atan(), sqrt(), log()`)



flow control: if/else, switch/case

- 静态 flow control: 基于 uniform 输入

