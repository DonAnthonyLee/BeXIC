# BeXIC
XIC (X Window Input Client) Wrapper for EIME/BeOS/HaikuOS

## 目的
网络上流行一种论调，认为 X Window 已经落伍，还有各种数落 XIM 不足的言论；然而，写 EIME (ETK++ Input Method Extension) 的 XIM 实现时，我却发觉 2001 年的 IMdkit 虽然存在一些小毛病，但所谓两个 XIM 不能共存、程序无缘无故卡死等等现象，更多可能是客户端程序自己未写好而导致。结合现 EIME-XIM 的需求，计划写一个 XIM 客户端的输入模块，即，在 EIME-XIM 应用时，相当于 XIM 服务端连接另一服务端，实现两个 XIM 服务端在不用更改 XMODIFIERS 的情况下同时为同一程序服务，甚至可以随时切换。此计划对于非 X Window 环境意义不是非常大，需通过 TCP 连接其他机器的服务端并依靠 XIMPreeditCallback|XIMStatusCallback 输入方式方能达到效果；可惜的是，目前所知道的各种 XIM 输入法，均未做到这一要求。


## 时间安排
虽然 ETK++ 已对其 XIC 实现进行优化，部分代码可能会融入到此计划中，但此计划依然规模庞大，开发进度将会是龟速，暂时只是开头。
