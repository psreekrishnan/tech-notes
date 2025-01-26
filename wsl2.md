#### WSL2 Ubuntu Login failure

##### Steps to reproduce
- Goto Windows Search > Ubuntu

```
Logon failure: the user has not been granted the requested logon type at this computer.
Error code: Wsl/Service/CreateInstance/CreateVm/HCS/0x80070569
Press any key to continue...
```
##### Fix
Make sure the below is is selected

![image](https://github.com/user-attachments/assets/2110b0ba-f66e-4ffc-8e2f-4f594a8e7440)

![image](https://github.com/user-attachments/assets/01e35904-3330-46c4-943b-f7a2fbeafa7e)

Also note, that,
Windows may disable the Hyper-V when restarted,

To turn it back on:

- Search for "Turn Windows features on or off"
- Enbale Hyper-V by selecting in the checkbox
- Restart the system


The same can be achieved by running the below command in PowerShell as Admin

`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All`
