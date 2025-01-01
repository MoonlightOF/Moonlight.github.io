<p>当我升级了Windows 11 24H2 之后，我的VMware Workstation的系统就非常的卡顿。避免这种卡顿的方法之一就是关闭Windows 11默认开启的Hyper-V、Device Guard 和 Credential Guard。</p>
<p>我们可以在搜索框中输入msinfo32.exe查看Hyper-V和相关组件是否打开
<img width="792" alt="屏幕截图 2025-01-01 174656" src="https://github.com/user-attachments/assets/39aff6b4-09da-4ddf-a678-f3d7064391d7" /></p>
<p>如上图所示就已经关闭了</p>
<p>我们可以输入以下代码使用PowerShell来关闭Hyper-V</p>
<code>Disable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Hypervisor</code>