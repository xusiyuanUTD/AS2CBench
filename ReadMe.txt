
AS2CBENCH stands for Accelerated Synthesizable SystemC Benchmark suite.
It is a accelerated version of S2CBENCH .S2CBENCH stands for Synthesizable SystemC 
Benchmark suite.It is a open sourceSystemC benchmarks created to help designers evaluate 
the QoR of state of the art HLS Tools. For more details please visit our publications:

S. Xu, J. Chen and B. Carrion Schafer, HW/SW Co-design Experimental Framework using Configurable SoC, International Conference on Reconfigurable Computing and FPGAs (ReConFig), pp.1-6, 2017.

AS2CBench is distributed in the hope that it will be useful. AS2CBench is free software and hardware; 
you can redistribute it and/or modify it, but please remember but WITHOUT ANY WARRANTY; without even the 
implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  

AS2CBENCH includes the following Testcases:

------------------------------------------------------------------------------------
|   NAME      |      		Description             |     Author   
|-------------+-----------------------------------------+---------------------------
| adpcm       | Adaptive Differential Pulse-Code        | Siyuan Xu,FFmpeg
|	      |	Modulation (encoder part only)         	| PolyU DARClab 
|-------------+-----------------------------------------+--------------------------
| ann         | Artificial Neuronal Network (ANN)	| Siyuan Xu,David Aledo, CEI, ETSII, Universidad Politecnica Madrid 
| 	      | 2 and 4 layer version	                | PolyU DARClab 
|-------------+-----------------------------------------+--------------------------
| aes         | Advanced Encryption standared (AES)     | pjc.co.jp 
| 	      | 128-bits (cipher and inv cipher)        | Siyuan Xu,Shuangnan Liu, PolyU DARClab 
|-------------+-----------------------------------------+--------------------------
| fir         | 10-Tap FIR filter                       | Siyuan Xu,PolyU DARClab 
|-------------+-----------------------------------------+--------------------------
| decimation  | 5 Stages decimation filter              | Siyuan Xu,PolyU DARClab
|-------------+-----------------------------------------+--------------------------
|interpolation| 4 Stages interpolation filter           | Siyuan Xu,PolyU DARClab
|-------------+-----------------------------------------+--------------------------
| idct        | Inverse Discrete Cosine Transform       | Siyuan Xu,Thomas G. Lange
|	      |						| PolyU DARClab
|-------------+-----------------------------------------+--------------------------
| kasumi      | Kasumi encryption algorithm             | Siyuan Xu,ETSI/SAGE
|             |						| PolyU DARClab
|-------------+-----------------------------------------+--------------------------
| md5c        | Message Digest Algorithm                | Siyuan Xu,RSA Data Security, Inc
|	      |						| PolyU DARClab
|-------------+-----------------------------------------+--------------------------
| qsort       | Quick sort                              | Siyuan Xu,Darel Rex Finley 
|	      | 					| PolyU DARClab
|-------------+-----------------------------------------+--------------------------
| snow3G      | snow 3G encryption algorithm            | Siyuan Xu,ETSI/SAGE
|	      |						| PolyU DARClab
|-------------+-----------------------------------------+--------------------------
| sobel       | Sobel filter                            | Siyuan Xu,Anushree Mahapatra
|             |                                         | PolyU DARClab
|-------------+-----------------------------------------+------------------------
| sobel+FIR   | Sobel filter + 10-Tap FIR filter        | Siyuan Xu
|             |                                         | PolyU DARClab
|-------------+-----------------------------------------+------------------------
| disparity   | Stereoscopic image disparity estimator  | Siyuan Xu,Miscellanous
| estimator   |					        | PolyU DARClab 
|-------------+-----------------------------------------+--------------------------

Each benchmark contains the following files:
=========================================================================================================
1.HW : Hareware 

  --SystemC for HLS : The SystemC code for high level synthesis(for generating the UUT_Template.v file).
  --HARD_WARE.sof   : Binary file which can be download to the FPGA board using "Quartus II Programmer".

=========================================================================================================

2.SW : Software

%% To compile a project, developers need to launch the Altera Embedded Command Shell first. Please
browse to the SoC EDS installation folder, e.g. "C:\altera\13.0\embedded".

-------------+-----------------------------------------+------------------------+------------------------
Makefile 
---------
make : Generates the executable binary.
-------------+-----------------------------------------+------------------------+------------------------

UUT.exe : The executable binary which can be executed in ARM/HPS.

Before the file can be executed, you need to change the file permission by running the command ¡°chmod 777 UUT.exe¡±.

=========================================================================================================

Quartus II Project Template fiels
------------------------------------
Includes all the Verilog-HDL files.The user just only needs to change the UUT_Template.v file.

And can regenerate the HARD_WARE.sof by using the Quartus II software.

ANSI-C files
------------
UUT.c : Main description of the benchmark.
define.h  : Includes define statments and stimuli filenames.

SystemC files
------------
benchmark.cpp /.h : Main description of the benchmark.
define.h  : Includes define statments and stimuli filenames.

Stimuli files (.txt)
-------------------
<name>.txt       :  File with iput stimuli (could be more than one).
<name>_golden.txt :  File with golden output with which the simulation results will be compared.


Extraction instruction (Linux):
%tar -zxvf AS2Cbench_<ver>.tar.gz


							[END]





