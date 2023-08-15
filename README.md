# ASIC (Application Specific Integrated Circuit)


ASIC stands for "Application-Specific Integrated Circuit." It is a type of integrated circuit (IC) that is designed and manufactured for a specific application or purpose. Unlike general-purpose microprocessors or other programmable devices, ASICs are optimized to perform a specific set of tasks, functions, or operations.

ASICs are commonly used in various electronic devices, systems, and industries where specific and dedicated functionality is required. They offer advantages such as high performance, low power consumption, and often reduced form factors compared to using general-purpose components for the same task.

## DAY-0: Software Installation
<details>
 <summary> Summary</summary>

 ---
 For this course there will be various tools required that can be downloaded using the commands given below in LINUX (UBUNTU).
  </details>
<details>
  <summary>iverilog</summary>

 ---
IVERilog (Icarus Verilog) is an open-source hardware description language (HDL) simulator. It is used for designing and testing digital circuits using hardware description languages such as Verilog. Verilog is a hardware description language used to model and simulate digital circuits, particularly in the field of digital design and electronic engineering. Steps to install iverilog are given below ;

  ```
sudo apt-get install iverilog

  ```
Results-->

---

![Screenshot from 2023-07-31 10-44-58](https://github.com/akul-star/ASIC/assets/75561390/359628ab-fb18-4272-8d09-a19abffc4199)


</details>

<details>
  <summary>Yosys</summary>

 ---
Yosys is an open-source framework for Verilog RTL (Register Transfer Level) synthesis. RTL synthesis is the process of transforming a high-level hardware description (typically written in a hardware description language like Verilog) into a lower-level representation that can be used to implement the design on hardware devices such as FPGAs (Field-Programmable Gate Arrays) or ASICs (Application-Specific Integrated Circuits).

Yosys provides a suite of tools that enable the synthesis and optimization of digital designs. Some of the key features and functionalities of Yosys include:

1. **RTL Synthesis:** Yosys takes Verilog input files describing digital designs and synthesizes them into a gate-level netlist, which represents the logical connections 
   and components of the design.
   
2. **Logic Optimization:** Yosys performs various optimizations on the design, such as technology mapping, logic minimization, and resource sharing, to produce a more 
   efficient and compact representation.

3. **Technology Mapping:** Yosys maps the logical components of the design to the specific cells or resources available in a target FPGA or ASIC technology library.

4. **Hierarchical Design:** Yosys supports hierarchical design, allowing for the synthesis of complex designs composed of multiple modules or sub-modules.

5. **Scripting and Automation:** Yosys can be controlled through scripts, which enables designers to automate the synthesis process and customize optimization steps.

6. **Open Source and Community-Driven:** Yosys is an open-source project with an active community of developers and users who contribute to its development and improvement.

Yosys is particularly popular in the field of digital design and electronic engineering, especially among FPGA and ASIC designers. It provides an alternative to proprietary synthesis tools and allows designers to have more control and transparency over the synthesis process.

To use Yosys, you typically write Verilog code to describe your digital design, use Yosys's command-line interface or scripting capabilities to run the synthesis process, and then generate output files that can be used for further steps in the hardware design flow.

```
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys-master 
$ sudo apt install make (If make is not installed please install it) 
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make 
$ sudo make install
```
Results -->

---
![Screenshot from 2023-07-31 10-51-37](https://github.com/akul-star/ASIC/assets/75561390/6a941985-55f7-436d-b96c-30883cbe1ebf)

Success

</details>

<details>

  <summary>GTKwave</summary>

 ---
GTKWave is an open-source waveform viewer used to visualize and analyze the simulation results of digital circuits. It is often used in conjunction with digital design and hardware description languages (HDLs) like Verilog or VHDL to visualize the behavior of digital signals over time. GTKWave provides a graphical representation of simulation waveforms, making it easier to debug and analyze the functionality of digital designs.

Key features of GTKWave include:

1. **Waveform Visualization:** GTKWave displays waveforms showing the behavior of digital signals over time, making it easier to identify signal transitions, timing 
   relationships, and other characteristics.

2. **Hierarchical Display:** It supports hierarchical display of waveforms, allowing you to expand and collapse hierarchical blocks to focus on specific parts of the 
    design.

3. **Zooming and Navigation:** You can zoom in and out on specific parts of the waveform and navigate through different parts of the simulation.

4. **Signal Highlighting:** GTKWave allows you to highlight and annotate specific signal transitions for easier analysis.

5. **Cross-Probing:** It supports cross-probing between source code and waveforms, enabling you to trace signals back to their corresponding locations in the design source 
   code.
   
6. **Support for Various File Formats:** GTKWave can read simulation output files in different formats, including VCD (Value Change Dump), FST (Fast Signal Trace), and 
   others.   
  

  ```
Steps to install gtkwave
sudo apt update
sudo apt install gtkwave
 ```
Results --->  

---

 ![Screenshot from 2023-07-31 11-13-17](https://github.com/akul-star/ASIC/assets/75561390/7a69c7e6-442e-4514-ad08-2d84bd9ec26b)

 Success
</details>

<details>
  <summary>ngSpice</summary>
  
  ---
  NGSPICE is an open-source mixed-level/mixed-signal electronic circuit simulator. It is used for simulating and analyzing the behavior of analog, digital, and mixed-signal circuits. NGSPICE allows engineers, researchers, and students to model and test electronic circuits before physical implementation, aiding in design verification, testing, and optimization.

Key features of NGSPICE include:
1. **Circuit Simulation:** NGSPICE can simulate various types of electronic circuits, including analog, digital, and mixed-signal designs.

2. **Component Models:** It supports a wide range of built-in models for electronic components such as resistors, capacitors, inductors, transistors, diodes, and 
    operational amplifiers.

3. **Interactive and Batch Modes:** NGSPICE can be used in both interactive mode (command-line interface) and batch mode (running scripts).

4. **Transient Analysis:** NGSPICE can perform transient analysis, which simulates circuit behavior over time, showing signal waveforms and dynamic responses.

6. **AC and DC Analysis:** It supports AC analysis (frequency domain) and DC analysis (steady-state behavior).

7. **Monte Carlo Analysis:** NGSPICE can perform Monte Carlo analysis to account for component tolerances and variations.

8. **Parameter Sweeps:** It allows for parameter sweeps to analyze circuit behavior under varying conditions.
  ```
After downloading the tarball from https://sourceforge.net/projects/ngspice/files/ to a local directory, unpack it using:
$ tar -zxvf ngspice-37.tar.gz
$ cd ngspice-37
$ mkdir release
$ cd release
$ ../configure  --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install

  ```
RESULTS --->
---
  ![Screenshot from 2023-07-31 11-21-50](https://github.com/akul-star/ASIC/assets/75561390/5001e4cd-b6a1-494b-8c9a-91042359996a)
  
  Success
</details>

<details>
  <summary>magic</summary>

***  
"Magic" refers to a popular open-source layout tool used for physical design and layout of integrated circuits. Magic is primarily used for designing layouts of digital and analog integrated circuits at the transistor level, which includes placing and routing of individual transistors and components.

Magic provides a platform for designing and verifying the physical representation of digital circuits before they are fabricated. It allows designers to visualize, edit, and manipulate various layout aspects, including transistor placement, interconnect routing, metal layers, vias, and more. The tool is especially useful for custom IC design and is often employed in academic and research settings.

Magic is often used in conjunction with other tools in the IC design flow to ensure that the layout meets certain design rules, constraints, and performance requirements.

```
$   sudo apt-get install m4
$   sudo apt-get install tcsh
$   sudo apt-get install csh
$   sudo apt-get install libx11-dev
$   sudo apt-get install tcl-dev tk-dev
$   sudo apt-get install libcairo2-dev
$   sudo apt-get install mesa-common-dev libglu1-mesa-dev
$   sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
make install

```
Results --->

***
![Screenshot from 2023-07-31 11-28-33](https://github.com/akul-star/ASIC/assets/75561390/9ca6cf83-181f-4f0d-a162-f88aba0b6ca5)

Success.

</details>

<details>
  <summary>OpenSTA</summary>
  
  ***
  OPENSTA, or Open Source Static Timing Analysis, is an open-source software tool used in the field of VLSI (Very Large Scale Integration) design for performing static timing analysis. Static timing analysis is a crucial step in digital design where the timing behavior of a digital circuit is analyzed to ensure that the circuit meets its performance requirements, such as setup and hold times, clock skew, and overall timing constraints.

OPENSTA is designed to analyze the timing characteristics of a digital circuit's design, helping designers identify potential timing violations, optimize the circuit's performance, and ensure that the design meets its timing goals. Static timing analysis plays a key role in verifying the correct functionality and performance of digital designs before they are fabricated. I installed and built OpenSTA (including the needed packages) using the following commands:
  ```
sudo apt-get install cmake clang gcctcl swig bison flex
git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
cd OpenSTA
mkdir build
cd build
cmake ..
make
```
Below is the screenshot showing sucessful installation:
![OpenSTA](https://github.com/akul-star/ASIC/assets/75561390/e040b4ad-3704-4eb6-a2a1-66cb3050493d)

Success

</details>

<details>
  <summary>OpenLANE</summary>
  
---  
OpenLANE is an open-source ASIC (Application-Specific Integrated Circuit) design flow and methodology that aims to automate and streamline various steps of the digital chip design process. It is a complete RTL-to-GDSII (Register Transfer Level to GDSII layout) flow that encompasses various stages of design, including synthesis, floorplanning, placement, routing, and final layout generation. OpenLANE is designed to make ASIC design more accessible, efficient, and collaborative.

Key features and components of OpenLANE include:
RTL-to-GDSII Flow: OpenLANE provides an integrated, end-to-end design flow, starting from RTL code and resulting in a manufacturable GDSII layout.

1. **Automated Design Steps:** It automates many design steps, including synthesis, floorplanning, placement, clock tree synthesis, routing, and other optimizations.

2. **Open-Source Tools:** OpenLANE leverages various open-source tools, such as Yosys for synthesis, ABC for technology mapping, and OpenROAD tools for physical design.

3. **Customizable:** Designers can customize the flow, parameters, and options to suit their specific design requirements and constraints.

4. **Digital ASICs:** OpenLANE is focused on digital ASIC design, making it suitable for complex digital chip designs.

OpenLANE is part of the larger open-source hardware design ecosystem and aims to promote collaboration, knowledge sharing, and accessibility in the field of ASIC design.
  ```
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git

sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update

sudo apt install docker-ce docker-ce-cli containerd.io

sudo docker run hello-world

sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot 

# After reboot
docker run hello-world

```
Below is the screenshot showing sucessful installation:


Success
</details>

## DAY - 1: Introduction to Verilog RTL design & sythesis
<details>
 <summary> SUMMARY</summary>
---
  </details>

<details>
 <summary> INTRODUCTION TO OPEN SOURCE SIMULATOR iverilog</summary>
 
 ---
**SIMULATOR:**  A simulator is a tool used to verify the design written in HDL and to convert it into RTL design. The simulator we are going to use in this course is iverilog.

**DESIGN:** Designing a circuit "by design" refers to creating a circuit based on a specific set of requirements or specifications. This process involves using a Hardware Description Language (HDL) like Verilog or VHDL to describe the behavior and structure of the circuit. We will later be taking an example of designing a 2x1 multiplexer (mux) using an HDL.

**TEST BENCH:** Test bench is a code necessarily written in an HDL language and is used to create set of inputs or stimulus to check whether the code written to design the required specifications is correct or not by observing the output given due to the test bench. 


In summary, a test bench is a critical component of the digital design and verification process. It ensures that the design meets its intended functionality and behaves correctly across a wide range of scenarios. By using an HDL to describe both the design and the test bench, you can systematically verify the correctness of your digital circuit before moving on to physical implementation.

*SIMULATOR WORKING*
====================

Simulators are a crucial part of the VLSI design and verification process, allowing designers to test and validate their designs before actual fabrication. Basically a simulator requires two things. First is the design written according to the required specifications and the test bench to verify the design written in HDL. Simulator requires change in input, then only it will give an output to be observed. If there is no change in input. the output in obviously never given by the simulator.

---
![Screenshot from 2023-08-09 17-43-08](https://github.com/akul-star/ASIC/assets/75561390/d1d37995-c3c6-4fd1-8b3c-8c3bcce1899b)

---
Now that we have design as well as the test bench, we cab use iverilog (icarus verilog) to compile the two files and give an outout in form of a VCD file or a Value Change Dump file which is only given as output if change in input is given to the simulator. This VCD (Value Change Dump) file is a standard file format used in digital simulation to capture and store the changes in signal values over time during a simulation run. This VCD file can be converted to waveforms using gtkWAVE that we installed already.

---
![2](https://github.com/akul-star/ASIC/assets/75561390/464a762c-1004-4233-aca8-5721d98ce77a)

  </details>

<details>
 <summary> LAB's USING IVERILOG & GTKWAVE </summary>
 
 *LAB-1: GIT CLONING*
 ===================

 
 1. Make a directory using the command given below in the terminal and name it          **VLSI** 

 ```
mkdir VLSI
```

2. Write the command given below to clone the repository from the link given in the command. In Ubuntu (or any other Linux-based system), the git clone command is used to create a copy of a Git repository from a remote source, such as a repository hosted on GitHub, GitLab, or another Git hosting service.

```
git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop

```
When this command is executed, a directory is created named **sky130RTLDesignAndSynthesisWorkshop** inside the VLSI documentary.
Now let us open the git cloned file and explore the different files we have in the folder. From the above screenshot we can tell that we have **my_lib**, **lib**, **DC_Workshop** & **verilogfiles**.

---
![4](https://github.com/akul-star/ASIC/assets/75561390/f4e75920-bb3b-4dbd-b50d-b2d81d183832)

The **lib** file will have **sky130_fd_sc_hd__tt_025C_1v80.lib** which is a standard cell library which we will be using for our synthesis. 

---
![5](https://github.com/akul-star/ASIC/assets/75561390/4bf09347-b90b-416c-a5cc-6dd5d8391d5f)

Apart from **lib** we also have a **my_lib** file inside the folder. This **my_lib** has a file named **sky130_fd_sc_hd.v** which has all the verilog codes of the standard cells like basic gates.

---
![6](https://github.com/akul-star/ASIC/assets/75561390/e2ea7f2e-d4b9-4cfc-9b41-0fc29ef0b614)

Lastly the cloned folder has another file names **verilog_files** which has all our lab experiments and will contain all oyr verilog source files abd test bench files.

---
![7](https://github.com/akul-star/ASIC/assets/75561390/0b657de9-6b9a-4603-be51-8570ac40a984)


*LAB-2: Introduction to Iverilog & GTKwave*
==========================================

Now we will see how to work with iverilog and GTKwave. We will do this by implementing a simple 2x1mux with the verilog source file we already have in our directory we created by git cloning. All the verilog soutce files and their test benches are already present inside the **verilog files** as shown below.

---
![8](https://github.com/akul-star/ASIC/assets/75561390/a63f229b-1aad-48c8-be93-0974327ed8cb)

Now we will load the design in iverilog. For that we will require two files from the verilog file which is verilog source file and test bench file of the 2x1 MUX. We will implement this using the following command.

```
iverilog good_mux.v tb_good_mux.v
```
After this we will give a command /.a.out to execute the compiled program to dump the VCD (Value Chnage Dump) file named **tb_good_mux.vcd** required for the GTKwave to give output waveforms according to the changes in the input as stated in the test bench file of the MUX. Here **./** part indicates the current directory, and a.out is a default name for an executable file generated by a compiler or assembler which in this case is done by **iverilog**.

```
./a.out
```
![9](https://github.com/akul-star/ASIC/assets/75561390/58a5ad7a-f884-420a-b9ea-7c7f6323afd3)

---
This command executes the compiled Verilog simulation and displays the simulation results, We will load this VCD file in the GTKwave using the command given below.

```
gtkwave tb_good_mux.vcd
```
This command will load the VCD file in the GTKwave simulator. A window will pop up and show the output of the designed mux once we append all the parameters shown in the window. This is hoW we will load the design and check its functionality.

---
![Untitled design](https://github.com/akul-star/ASIC/assets/75561390/3c227875-6f91-41a5-acc7-76c2fb69ac6b)

From the above waveforms obtained using gtkwave, we can check whether the MUX designed is working according to its functionality ot not.

*Verilog Source File*
====================
![images](https://github.com/akul-star/ASIC/assets/75561390/cc0647ac-65e8-4fd6-8a47-e88c189a1096)

Till now we have studied how the design output will look like using GTKwave and iverilog. Now we will try to understand how the source verilog code and the test bench verilog code works. To open the verilog file we need to give the command mentioned below.
```
gvim tb_good_mux.v -o good_mux.v
```
You can use the **gvim** command to launch the graphical version of the Vim text editor, also known as "GVim" (Graphical Vim). GVim provides a graphical user interface (GUI) in addition to the usual text-based interface of Vim. 

1. Verilog Design File
   =====================

![verilog](https://github.com/akul-star/ASIC/assets/75561390/a64802e7-374a-4e4a-99f7-0c71443011f6)
Their are multiple ways of coding a mux in verilog and this is just an illustrative example. As you can see inputs and outputs are defined in the design file inputs being i0, i1 and select line &  output is **y** as it should be in a multiplexer. **Always Block** is used to implement the logic where, if select line is high i1 is taken as output and if select line is low then i0 is used as the output.

2. Test Bench File
   ==============
![TB](https://github.com/akul-star/ASIC/assets/75561390/e1f59e9f-f05d-464b-a223-99e06d074b8b)
A test bench file in the context of hardware description languages like Verilog is a special type of Verilog code that is used to simulate and verify the behavior of a digital design described in another Verilog design file. We will be instantiating the verilof design file here in the test bench. This testbench file which is names uut (unit under test) basically selects the select line as 1 and 0 every 75ns. **dumpfile ("tb_good_mux.vcd")** and **dump (0,tb_good_mux)** will make the dump file for the GTKwave output waveforms.

</details>

<details>
 <summary>INTRODUCTION TO YOSYS & LOGIC SYNTHESIS</summary>


*1. INTRODUCTION TO YOSYS*
   =======================


A synthesizer, also known as a synthesis tool or RTL (Register Transfer Level) synthesizer, refers to software that takes a high-level hardware description language (HDL) representation, such as Verilog or VHDL, and converts it into a lower-level gate-level or structural netlist representation. This process is known as synthesis and we will be using **YOSYS** as our synthesis tool. 

![yosys1](https://github.com/akul-star/ASIC/assets/75561390/df8f6286-69f8-4a78-bab8-44ae72ee4ac5)
---

**YOSYS** requires **.lib** file which refers to a library file that contains timing, power, and other characterization information for a set of standard cells or gates and the design file to know which design has to be implemented ot which design has to br converted from RTL to lower-level gate level netlist.


![YOSYS2](https://github.com/akul-star/ASIC/assets/75561390/37b1e6d4-8d24-4f5a-8d24-8820be8874d9)
---

- The read_verilog command is a command used in Verilog-based simulation and synthesis environments like YOSYS. It is used to read and parse Verilog source files and make the design's information available to the tool for further analysis, simulation, synthesis, or other operations.
- The read_liberty command is to read and parse Liberty files ot lib files. Liberty files, often with the .lib extension, contain timing, power, and other characterization data for standard cells or gates used in digital design. These files provide critical information for synthesis, optimization, and analysis of digital designs.
-  The write_verilog command is used in the Yosys open-source digital synthesis tool. Yosys is commonly used for RTL synthesis and various other digital design tasks. The write_verilog command in Yosys is used to output the synthesized design in Verilog format which is known as a NETLIST. A netlist is a fundamental representation of a digital circuit's logical and physical structure. It describes the interconnections between electronic components, such as gates, flip-flops, and other functional units, using a list of interconnected nets (signal lines) and their connections.


**Synthesis Verification -** We can verify the gate level synthesis dine by YOSYS using **Netlist file** and **Test Bench File**. 

![Verify](https://github.com/akul-star/ASIC/assets/75561390/35787fbc-8035-4aa9-adf7-b3c75acf5214)
---
If the output waveforms match to that of the RTL simulation, then our design on gate-level is correct and hence our NETLIST is correct. 


*2. LOGIC SYNTHESIS*
   ===============
Till now we have learned how a synthesis tool helps us obtain the digital logic circuit from an RTL design. We know that the two  files required to be given as an input to the synthesis tools are RTL design and Front End LIB file. Now let us know more about the library file and various standard cells it has.

1. Combinational Logic Cells
2. Latches and Flip-Flops
3. Buffers and Inverters
4. Arithmetic Logic Units (ALUs)
5. Multiplexers and Demultiplexers
6. Shift Registers and Counters
7. Decoder and Encoder
8. Comparator and Magnitude Comparator
9. Tri-State Buffers
10. Special Purpose Cells

The library files may not be exhaustive of all the gates we want, but it will be rich enough to implement any logic functionality. In a standard cell library file (.lib), you might encounter different flavors of the same gate. These different flavors represent variations of the same basic gate logic that are optimized for specific purposes, such as different performance, power consumption, or area trade-offs. These flavors allow designers to choose the best-suited cell for their specific design requirements.

Here are some common flavors you might find for the same gate in a standard cell library:

  -  Fast:
        - These cells are optimized for speed and have a lower propagation delay.
        - They are suitable for critical paths and designs where performance is a priority.
        - Fast cells might consume more power and occupy more area compared to other flavors.

   - Slow:
        - These cells are optimized for low power consumption and typically have a longer propagation delay.
        - They are used in non-critical paths or parts of the design where power efficiency is more important than speed.
  </details>

  <details>
 <summary>LABS USING YOSYS & SKY130 PDKs</summary>
 
 ---
 LAB-3: YOSYS 1 GOOD MUX
 ========================
 In this lab we will have an introduction to out synthesizer (YOSYS). Till now we have designed a multiplexer, compiled the verilog files and observed the output waveforms on GTKwave. Now we will use YOSYS to form netlist using the standard cells we have in the library and we will observe the graphical version of logic it has realized.

 **STEP-1:** Firstly we will invoke the YOSYS using the below command.
 ```
yosys
```
A prompt window will pop up as shown below.

![yosyspropmt](https://github.com/akul-star/ASIC/assets/75561390/d909606c-89ab-40ab-8b85-644f1f4ada69)
---
**STEP-2:** Now we will read the library file using the below mentioned command. The read_liberty command in Yosys is used to read and parse a Liberty library file, making its information available for the synthesis and optimization processes.

```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
The below screenshot shows what text to expect after the command given.

![realiverty](https://github.com/akul-star/ASIC/assets/75561390/ab0051f4-b6b4-4d95-b6ca-b4c3e08874c2)
---

**STEP-3:** In YOSYS, the read_verilog command is used to read and parse Verilog hardware description files (.v files). When you use the read_verilog command in YOSYS, you are essentially instructing YOSYS to read and analyze a Verilog file, extracting information about modules, signals, ports, instances, and other elements of the design. This information is then used in subsequent steps of the synthesis process. Therefore, to ectract the information about the design we will have to give the command stated below.

```
read_verilog good_mux.v
```
![readverilog](https://github.com/akul-star/ASIC/assets/75561390/36d7418a-9d0c-48e3-b8ed-4c3471aa4400)
---


**STEP-4:** In YOSYS, the synth -top <top_module_name> command is used to initiate the synthesis process and specify the top-level module of your design. This command tells YOSYS to perform synthesis starting from the specified top-level module defined in the given Verilog file (filename.v in your case). The synthesis process transforms the high-level RTL (Register Transfer Level) description of your design into a lower-level representation, typically a gate-level netlist.

```
synth -top good_mux
```
 
![synth](https://github.com/akul-star/ASIC/assets/75561390/7f61bd2d-348e-485d-acf4-8cc06628a597)
---

**STEP-5:** In YOSYS, the abc -liberty command is used to perform technology mapping using the ABC tool and a specified liberty file. The -liberty option is used to specify a liberty file that contains information about the available cells and their timing characteristics in a target technology library. Liberty files are commonly used to guide the synthesis process, ensuring that the generated gate-level netlist is compatible with the target technology's characteristics and constraints. The command to implement is given below.

```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Now finally we can say that our synthesis has been completed and the result of the above command will be a NETLIST as shown below.

![Netlist](https://github.com/akul-star/ASIC/assets/75561390/971321c4-9a6c-43c9-a692-a27ba3d822d1)
---

We can give the command **show** to get a graphical version of logic the synthesizer has realized.

![show](https://github.com/akul-star/ASIC/assets/75561390/9416a5a8-b21e-41f1-96eb-64f4ad3a309b)
---

Also, if we want to view the netlist in the vim editor, the below two commands are need to be given.
```
write_verilog -noattr good_mux_netlist.v
!gvim good_mux_netlist.v
```
---
![netlistvim](https://github.com/akul-star/ASIC/assets/75561390/104f0b3b-59a4-4ba4-b1af-a2a937682480)

 </details>

## DAY-2: Timing libs, Hierarchical vs Flat Synthesis & Efficient Flop Coding Styles
  
  <details>
 <summary> Introduction To Timing.libs</summary>

In this section we are going to have a walk through to our library. We have already seen what .lib files do and why they are important in synthesis. The libarary file we have has been named  sky130_fd_sc_hd__tt_025c_1v80.lib .  

 ![PVT](https://github.com/akul-star/ASIC/assets/75561390/6d71d686-eb9d-4953-b5f1-01ab96b36c38)
 --- 
- The naming of the library file is according the concept of PVT in a standard cell file.In the context of a standard cell library file used in digital circuit design, "PVT" stands for Process, Voltage, and Temperature. It refers to the various conditions under which a digital circuit is designed and characterized. Let's break down each component:

- Process: This refers to the specific manufacturing process used to create the integrated circuits (ICs) on a semiconductor wafer. Different manufacturing processes can have variations in parameters such as transistor sizes, dopant concentrations, and oxide thickness. These variations can affect the performance and characteristics of the digital circuits.

- Voltage: Voltage represents the supply voltage at which the digital circuit operates. Different voltage levels can impact the power consumption, speed, and reliability of the circuit. Standard cell libraries often provide cells that are optimized for different voltage levels, allowing designers to choose the appropriate cells based on their design requirements.

- Temperature: Temperature refers to the operating temperature of the digital circuit. Temperature variations can affect the electrical properties of the transistors and interconnects, which in turn can impact the circuit's performance. Standard cell libraries are characterized at specific temperature points to ensure that the circuit operates correctly across a range of temperatures.

The PVT parameters decide how the silicon will work ib different enviorments. If it will work fast or slow, Power dissipation will be high or low, etc.

Now let us open the standard sell library inside the **vim** text editor and explore it. Give the below command to open the vim file for the library.

```
gvim ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
---
![libgvim](https://github.com/akul-star/ASIC/assets/75561390/a84f6ca2-00f9-4020-8b52-d9d0fcf34c5d)

As we can observe, in the first few lines unit of every parameter is mentioned above that is used to represent different data for different standard cells. The library we just opened will have all the standard cells and different parameters for each of the standard cell. Now let us discuss any one of the standard cell and what kind of information is memtiones about the standard cells. Give the command below to open the verilog model of the standard cell a2111o which mean it's a 2 input AND gate which further gived input to 3 OR gates, making it a 5 input and single output model.

```
:sp ../my_lib/verilog_model/sky130_fd_sc_hd__a2111o.behavioral.v
```
This is a 2-input AND gate and a 4-input NOR gate. Within the .lib file, sevetral parameters specific to this particular standard cell is given, including leakage power values for every possible input combination, specifications regarding pin type and pin capacitances, internal power metrics, timing-related particulars, as well as area measurements and power-related specifics for the standard cells. Similarly for all the standard cells the parameters above mentioned is listed in the .lib file.

Now we will comapre a simple AND gate and it's different flavours. and2_0, and2_1 and and2_2 are three standard models available with the same output but having different area. This means their delay and power will be different as well.


![area_dep](https://github.com/akul-star/ASIC/assets/75561390/a9359bb5-6279-43b0-be4e-be92bc5e64ba)
---
- AREA: and2_0 < and2_1 < and2_2
- POWER: and2_0 < and2_1 < and2_2
- DELAY: and2_0 > and2_1 > and2_2
 </details>

  
  <details>
 <summary> Hierarchical vs Flat Synthesis </summary>
 In this section, we will discuss the hierarchical and flat synthesis and how they are different and how their netlist looks like. Let's take an example of a circuit with multiple modules. To open the verilog file in VIM editor, give the below command.

```
gvim multiple_modules.v
```

  
</details>

  
## REFERENCES
 1. http://iverilog.icarus.com/
 2. https://github.com/steveicarus/iverilog
 3. http://www.clifford.at/yosys/
 4. https://github.com/YosysHQ/yosys
 5. https://github.com/gtkwave/gtkwave
 6. http://ngspice.sourceforge.net/
 7. https://github.com/The-OpenROAD-Project/OpenSTA
 8. https://wiki.archlinux.org/title/Magic
 9. https://github.com/efabless/openlane/blob/master/doc/workshop/README.md





