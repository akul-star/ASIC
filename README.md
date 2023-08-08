# ASIC

## DAY-0
<details>
  <summary> Summary</summary>
  Installed all the required tools.
  </details>
<details>
  <summary>iverilog</summary>
IVERilog (Icarus Verilog) is an open-source hardware description language (HDL) simulator. It is used for designing and testing digital circuits using hardware description languages such as Verilog. Verilog is a hardware description language used to model and simulate digital circuits, particularly in the field of digital design and electronic engineering. Steps to install iverilog are given below ;

  ```
sudo apt-get install iverilog

  ```
Results-->

![Screenshot from 2023-07-31 10-44-58](https://github.com/akul-star/ASIC/assets/75561390/359628ab-fb18-4272-8d09-a19abffc4199)

success

</details>

<details>
  <summary>Yosys</summary>
  
Installed yosys using the below command.
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

![Screenshot from 2023-07-31 10-51-37](https://github.com/akul-star/ASIC/assets/75561390/6a941985-55f7-436d-b96c-30883cbe1ebf)

Success

</details>

<details>

  <summary>GTKwave</summary>
  The below command was used to install GTKwave.
  

  ```
Steps to install gtkwave
sudo apt update
sudo apt install gtkwave
 ```
Results --->  

 ![Screenshot from 2023-07-31 11-13-17](https://github.com/akul-star/ASIC/assets/75561390/7a69c7e6-442e-4514-ad08-2d84bd9ec26b)

 Success
</details>

<details>
  <summary>ngSpice</summary>
  
  Installed ngSpice using the below command.
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

  ![Screenshot from 2023-07-31 11-21-50](https://github.com/akul-star/ASIC/assets/75561390/5001e4cd-b6a1-494b-8c9a-91042359996a)
  
  Success
</details>

<details>
  <summary>magic</summary>
  
Installed ngSpice using the below command.

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

![Screenshot from 2023-07-31 11-28-33](https://github.com/akul-star/ASIC/assets/75561390/9ca6cf83-181f-4f0d-a162-f88aba0b6ca5)

Success.

</details>

<details>
  <summary>OpenSTA</summary>
  
  I installed and built OpenSTA (including the needed packages) using the following commands:
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
  
  I installed and built OpenLANE using the following commands:
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

<details>
<summary> REFERENCES </summary>
  1. http://iverilog.icarus.com/
  2. https://github.com/steveicarus/iverilog
</details>
 





