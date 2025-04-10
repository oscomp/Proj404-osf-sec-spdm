项目名称：基于SPDM协议的硬件安全通信模块实现  
项目链接：https://www.dmtf.org/standards/SPDM  
导师信息：霍文，15165077960，huowen@ieisystem.com  
难度：中  
分类：硬件安全/嵌入式系统  

题目要求：  
- 基于 DMTF SPDM 1.2 协议标准，实现一个运行在用户态的 SPDM 通信模块；  
- 实现完整的协议交互流程，包括但不限于：  
  - GET_VERSION  
  - GET_CAPABILITIES  
  - NEGOTIATE_ALGORITHMS  
  - GET_DIGESTS  
  - GET_CERTIFICATE  
  - CHALLENGE  
  - GET_MEASUREMENTS  
  - KEY_EXCHANGE  
  - FINISH  
- 支持设备间身份认证、密钥协商、安全数据传输等功能；  
- 提供可视化工具用于展示每一步通信交互的协议数据结构、认证状态、加密信息等内容；  
- 提供命令行工具（如 `spdm_cli`）可进行完整交互测试；  

特征：  
- 开发语言：C/C++  
- 协议版本：SPDM 1.2  
- 输出形式包括：  
  - 命令行交互工具 `spdm_cli`  
  - 协议交互过程可视化展示工具（如网页或GUI形式均可）  
- 参考实现包括 Intel SPDM Tool 与 OpenSPDM  

预期目标：  

**第一题：基础协议栈实现**  
- 基于 SPDM 1.2 协议流程，完成所有基础请求和响应交互；  
- 确保客户端与虚拟/模拟服务端之间可完整通信；  

**第二题：安全认证与密钥交换**  
- 完成基于证书的设备身份认证机制；  
- 实现密钥协商流程，建立加密通信会话；  
- 性能要求：单次安全会话建立时间 ≤ 200ms；  

交付物清单：  
1. 核心代码：  
   - `src/`：SPDM 协议栈实现  
   - `tools/spdm_cli/`：命令行测试工具  
   - `visualize/`：协议数据交互可视化模块  

2. 文档：  
   - 使用说明文档（README.md）  
   - 编译部署手册  
   - 测试说明及性能评估  

License：无（Apache-2.0 或 BSD）  

参考资料：  
1. SPDM 1.2 规范：DMTF DSP0274  
2. Intel SPDM Tool：https://github.com/intel/spdm-tool  
3. OpenSPDM：https://github.com/DMTF/libspdm  
