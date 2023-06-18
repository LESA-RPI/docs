# Documentation Protocol at LESA, RPI

## Contents
1. [Objective](#objective)
2. [Background](#background)
3. [What to write on a document?](#document)
4. [How to write annotations on a code file?](#codeFiles)
5. [Template & Example](#templates)
6. [Authors](#authors)
7. [Referneces](#references)


<a name="objective"></a>
## Objective
This repository aims to provide a guideline about what/how information should be provided on a Github repositories so that incoming researchers can easily understand code files written by previous researchers. To encourage readers to easily follow this guideline, a template and example file are shared as well.

<a name="background"></a>
## Background
Currently, many graduate students have worked on their research project at LESA; however, when they graduate RPI, they shared their codes with a few annotation and documentation. It hinders other for other researchers or newcomers to understand their codes and continue the projects, and this issue has become a huge obstacle to further develop technologies at LESA. To deal with issue, this documents walk through the LESA's documentation protocol. 

<a name="document"></a>
## What to write on a document?
In this section, we walk you through what/how information should be provided on a document.

#### 1. Title
Write the title consisting of most relevant keywords to your project

#### 2. Contents
A table of contents will enable readers to easily look up or revisit sections/subsections they are looking for.

**Example:**
```
## Contents
1. Introduction
2. Getting Started
2.1. Prerequisites
2.2. Setup
2.3. Implementation
2.4. Small Code Examples
3. Notes
4. Authors
5. References
```

#### 3. Introduction
Write about 1-2 paragraphs describing the purpose and background of your project. It will provide readers with rich information to capture the research background.

**Example:**
``` 
## Introduction
This project is a ROS package containing scripts to control the lights, blinds, and HVAC, and read data from sensors in the Smart Conference Room. In order to run any of the scripts, ROS must be installed and roscore must be active
```

#### 4. Getting Started
This section walks through the whole process of how to set up an environment and implement codes. 
#### 4.1. Prerequisites
#### 4.1.1. Packages
Describe what packages (libraries) and software they need to install for implementing your codes. Please specify the version of each package to make sure all reader's packages are compatible with your codes. 

**Example:**
``` 
#### Prerequisites
- Node.js v18.15.0 (https://nodejs.org/en/download)
- Node-RED v3.0.2 (https://nodered.org/docs/- getting-started/local)
- ROS Noetic Ninjemys (http://wiki.ros.org/ROS/Installation)
- SCR-Control Scripts (https://github.com/LESA-RPI/scr.scr_control)
```

#### 4.1.2. Hareware
If your project works based on hardware like sensors or physical systems, all the hardware architectures should be specified, such as a list of connected devices, switches, and routers with their MAC and IP addresses. We highly recommend adding a diagram of hardware architecture to enhance the understanding of how all the devices are connected. 

#### 4.2. Setup
Describe how to install and set up software or systems. We recommend describing the process under subsections. We encourage you to add links to official websites for installing software or systems.

#### 4.3. Implementation
Walk through step-by-step to implement a system or codes. We highly recommend adding screenshots for each key part of the process after the explanatory text because many readers would be unfamiliar with your system environment. 

#### 4.4. Small Code Examples
We encourage you to add code examples so that learners can easily copy and paste your code to implement your system and figure out how the codes work. 

**Example:**
``` 
## Code Example
$ rosrun scr_control SCR_TOF_client.py get_distances_all
```

#### 5. Notes (optional)
This section is optional. If there is additional information that readers need to know, notes can be described in this section.

**Example:**
``` 
## Notes
- This API was developed only for accessing real-time data from sensors and HVAC in SCR. However, it cannot control HVAC settings, blinds, or lighting for security.
- RPI VPN is required to connect server computers in the SCR from off-campus.
```

#### 6. Authors
Provide authors' name and contact information so that readers can reach out to them if there are any questions on their codes.

**Example:**
``` 
## Authors
- Jihoon Chung (chungj11.rpi.edu)
- Diyanko Bhowmik (bhowmd@rpi.edu)
```

#### 7. References
Specify references you mainly refer to. It can provide readers with useful information to understand the knowledge background of your technology.

<a name="codeFiles"></a>
## How to write annotations on a code file?

#### 1. Variables
- Use camel-case
- Do not be afraid of long names
- Should be clear and applicable to use-case
- Use the most reliable and efficient variable type
	- Eg: If you can use a byte type for a loop counter (as long as it is less than 255), maybe do not use int. This is especially for coding in microprocessors.

#### 2. Comments
- If the comment is for one line of code, write it to the right of the line
- If it is for a group of lines, write it in the top
- Be both clear, concise and comprehensive

<a name="templates"></a>
## Template & Example
Example and template files can be found here:
- [Document template](/document-template.md)
- [Example document](https://github.com/LESA-RPI/scr.scr_control#readme)
- [Example codes]()

<a name="authors"></a>
## Authors
- Diyanko Bhowmik (bhowmd@rpi.edu)
- Jihoon Chung (chungj11@rpi.edu)

<a name="references"></a>
## References
- [thegooddocsproject/templates](https://github.com/thegooddocsproject/templates/blob/dev/tutorial/tutorial-template-guide.md)
- [kylelobo/The-Documentation-Compendium](https://github.com/kylelobo/The-Documentation-Compendium/tree/master)
- [madhur-taneja/README-Tempalte](https://github.com/madhur-taneja/README-Template)