<!--- SPONDLAB Library -->
# SpondLab
Department of physics KyungHee University

Build random composition Atoms' XPS with sessa.exe(NIST)
and Training deep neural models with those data.

@author  Jeong Hoon (Sian) Choi
@company KHU Spondlab. Yongsup Park
@email   csian7386@gmail.com
@version 1.0.0
@date    2023-12-20

## Requirement
SESSA (NIST Standard Reference Database 100)
Simulation of Electron Spectra for Surface Analysis
https://www.nist.gov/srd/nist-standard-reference-database-100

## Dired

└── install
    ├── README
    ├── Sessa-2.2.0-Linux.sh	; Sessa loaded shell script(Provided from NIST)
    ├── aptInstall.sh		; Installing Utilities and application
    ├── code_DNNXPS.tar		; $HOME/XPSDNN/.codes
    ├── config
    ├── makeDir.sh		; build $HOME/XPSDNN sub Directory
    ├── requirements.txt
    └── valid_data.tar		; $HOME/XPSDNN/validation(600 data set)



├── xpsControl			; process initiate file(dialog)
├── README			; this file
├── config			; config : setting variance
├── data			; each 1000 data in one directory(ONLY config::DataSave : true)
│   └── 1
│       ├── 1
	...
	...
├── .SESSA			; NIST sessa
├── .codes			; bin+src+include put together
│   ├── CNCommunicator.cpp
│   ├── CNCommunicator.hpp
│   ├── IPC2cpp.py
│   ├── IPC2py.cpp
│   ├── IPC2py.hpp
│   ├── Makefile		; make -> compile to build main executable file
│   ├── __pycache__
│   │   ├── IPC2cpp.cpython-38.pyc
│   │   ├── dnnModel.cpython-38.pyc
│   │   └── utility.cpython-38.pyc
│   ├── checkStatus.sh
│   ├── cleaner
│   ├── cleaner.cpp
│   ├── configReader.cpp
│   ├── configReader.hpp
│   ├── dialogrc
│   ├── dnnModel.py
│   ├── exception.cpp
│   ├── exception.hpp
│   ├── filesystem.cpp
│   ├── filesystem.hpp
│   ├── main
│   ├── main.cpp
│   ├── main.py
│   ├── predict.py
│   ├── ps.gawk
│   ├── screenXvfb.sh
│   ├── sessa.cpp
│   ├── sessa.hpp
│   ├── utility.cpp
│   ├── utility.hpp
│   └── utility.py
├── .tmp
│   ├── dump			; dump directory: receive ouput from NIST::SESSA
│   ├── dump2			; dump2 directory: used to handle xpsControl or check processes status
│   ├── log
│   │   ├── err.txt		; log files from CPP(exclude python processes)
│   │   └── log.txt
│   │   └── pyLog.txt		; log files from PY
│   └── losses			; losses(contamination depth & atom composition) about validation 600
│       ├── loss1.txt
│       └── loss2.txt
├── pth				; python torch files(used to load weights)
├── shut			; python torch files(when reach target number)
│   ├── ExitShut##.pth
└── validation			; validation data 600
    ├── XPS_000001
	...
	...
    └── XPS_000600
