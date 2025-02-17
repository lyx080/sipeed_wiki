# Note

> Edit on 2022.06.29

- This is for Windows users only

## Troubles with programmer

**Make sure there are 2 converters in Device Manager before reading.**

![](./../../../zh/tang/assets/questions/converter.png)

If there are two converters, this means computer and board succeed connectting. And if there is no converter, try another USB port or reinstall driver.

<h3> <font color="">Download frequency</font></h3>

Make sure the frquency is equal or lower than `2.5MHz` ,

Otherwise it may lead some errors.

<details>
  <summary><font color="#4F84FF">Click to see steps</font></summary>
  <img src="./../assets/questions/cable.png">
  <p>Choose Frequency</p>
  <img src="./../assets/questions/frequency.png" >
  <p>Cilck Save</p>
</details>

### Trouble downloading

**If you have any problems programming or flashing FPGA development board, it's required to use the programmer which can be downloaded at this page https://dl.sipeed.com/shareURL/TANG/programmer instead of what is installed with the IDE.**

### ID code mismatch

This error means wrong device choice. All that refers chip model(like he project device, pin constrain, IP modules and programmer device choose) need to be changed. 

For Nano 9K it should be choose as follow:

<details>
  <summary><font color="#4F84FF">Click to see the choice of 9K</font></summary>
  <img src="./../../../zh/tang/Tang-Nano-9K/nano_9k/Tang_nano_9k_Device_choose.png">
</details>

For other boards, just make sure your device selection corresponds to the laser mark on chip package.

### Download slowly

Don't choose Operation containing Verify

![](./../../../zh/tang/assets/questions/never_choose_verify.png)

### Can't find download file

Normally the download file whose extension name is fs is in the impl/pnr folder under the project path.

<details>
  <summary><font color="#4F84FF">Click to see steps by picture</font></summary>
  <img src="./../../../zh/tang/assets/questions/fs_path.png">
  <p>From the picture above we can know the path of this download file is fpga_project1/impl/pnr/fpga_project1.fs </p>
  <p></p>
  <p> The fpga_project1 is the project dictionary, the impl is generated by IDE, and the download is in the folder named pnr</p>
  <p></p>
  <p> The file whose extension name is fs is what we will burn into fpga</p>
</details>

### No Gowin devices found

This can be solved by replacing Programmer as mentioned in **[Trouble downloading](#trouble-downloading)**

### Cabel open failed

After finishing replacing **programmer** as mentioned previously,Do following steps in programmer application.

Click Edit->Cable Setting->Cable->Query in the top menu bar,then save.

<details>
  <summary><font color="#4F84FF">Click to see steps by pictures</font></summary>
  <img src="./../../../zh/tang/assets/questions/cable.png">
  <p>Click Query in the following picture</p>
  <img src="./../../../zh/tang/assets/questions/click_query.png" >
  <p>Click Save</p>
</details>

## Troubles with IDE

### Using GAO

GAO is Gowin Analyzer Oscilloscope, its document can be found in the path like what is shown below

![GAO path](./assets/gao.png)

It's tested IDE version before V1.9.8.1 and V1.9.8.1 is ok, the newer version has not be tesetd.

### View IP reference

<details>
  <summary><font color="#4F84FF">Click to see instructions</font></summary>
    <img src="./../../../zh/tang/assets/ip-reference.png">
</details>

### Reconfigure generated IP

<details>
  <summary><font color="#4F84FF">Click to see instructions</font></summary>
    <img src="./../../../zh/tang/assets/ip-reconfigure.png">
</details>