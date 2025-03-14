+++
disableToc = false
title = "Midori AI Subsystem Manager"
weight = 1
+++

![Midori AI photo](https://tea-cup.midori-ai.xyz/download/logosubsystem.png)

**How Docker Works**

Docker is a containerization platform that allows you to package and run applications in isolated and portable environments called containers. Containers share the host operating system kernel but have their own dedicated file system, processes, and resources. This isolation allows applications to run independently of the host environment and each other, ensuring consistent and predictable behavior.

**Midori AI Subsystem**

The Midori AI Subsystem extends Docker's capabilities by providing a modular and extensible platform for managing AI workloads. Each AI system is encapsulated within  its own dedicated Docker image, which contains the necessary software and dependencies. This approach provides several benefits:

* **Simplified Deployment:** The Midori AI Subsystem provides a streamlined and efficient way to deploy AI systems using Docker container technology.
* **Eliminates Guesswork:** Standardized configurations and settings reduce complexities, enabling seamless setup and management of AI programs.

{{% notice style="warning" title="Notice" %}}
**Warnings / Heads up**
- This program is in beta! By using it you take on risk, please see the disclaimer in the footnotes
- The webserver has been moved to the new OS and Server!

**Known Issues**
- The "Huggingface Downloader" backend program is needing to be remade to work with LocalAI Master changes, we are working on a update!

**Windows Users**
- There seems to be a bug where the manager is adding ``140_1.dll`` to file request. We are working on a fix.
- There seems to be false positive from virus checkers, [this file](https://tea-cup.midori-ai.xyz/download/model_installer_windows.zip) is safe to download, [check here for the code](https://github.com/lunamidori5/Midori-AI/tree/master/other_files)
- This seems to be a widely known bug with Google Chorme, Edge, and others, here are our [virus scans from a few websites](https://www.virustotal.com/gui/url/6d36b491ed76cc9f1e284b43fe7fcd4158696edb5730b614469bbdf6f1e616f0/details). We will try other ways of packing the files.
{{% /notice %}}

## Install Midori AI Subsystem Manager

{{% notice style="info" title="Notice" %}}
- As we are in beta, we have implemented telemetry to enhance bug discovery and resolution. This data is anonymized and will be configurable when out of beta.
{{% /notice %}}

{{< tabs >}}
{{% tab title="Windows" %}}
### Prerequisites
[Docker Desktop Windows](https://docs.docker.com/desktop/install/windows-install/)

### Recommended
Please make a folder for the Manager program with nothing in it, do not use the user folder.

### Quick install

1. Download - https://tea-cup.midori-ai.xyz/download/model_installer_windows.zip
2. Unzip into LocalAI folder
3. Run `subsystem_manager.exe`

### Quick install with script

Open a Command Prompt or PowerShell terminal and run:

```bat
curl -sSL https://raw.githubusercontent.com/lunamidori5/Midori-AI/master/other_files/model_installer/shell_files/model_installer.bat -o subsystem_manager.bat && subsystem_manager.bat
```

### Manual download and installation

Open a Command Prompt or PowerShell terminal and run:

```bat
curl -sSL https://tea-cup.midori-ai.xyz/download/model_installer_windows.zip -o subsystem_manager.zip
powershell Expand-Archive subsystem_manager.zip -DestinationPath .
subsystem_manager.exe
```
[![Windows Build Test](https://github.com/lunamidori5/Midori-AI/actions/workflows/Windows_Build_Test.yml/badge.svg?branch=master)](https://github.com/lunamidori5/Midori-AI/actions/workflows/Windows_Build_Test.yml)
{{% /tab %}}

{{% tab title="Linux / WSL" %}}
### Prerequisites
[Docker Desktop Linux](https://docs.docker.com/desktop/install/linux-install/) / [Docker Desktop Windows](https://docs.docker.com/desktop/install/windows-install/)

or 

[Docker Engine](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/)

### Quick install with script

```sh
curl -sSL https://raw.githubusercontent.com/lunamidori5/Midori-AI/master/other_files/model_installer/shell_files/model_installer.sh | sh
```

### Manual download and installation

Open a terminal and run:

```sh
curl -sSL https://tea-cup.midori-ai.xyz/download/model_installer_linux.tar.gz -o subsystem_manager.tar.gz
tar -xzf subsystem_manager.tar.gz
chmod +x subsystem_manager
./subsystem_manager
```
[![Linux Build Test](https://github.com/lunamidori5/Midori-AI/actions/workflows/Linux_Build_Test.yml/badge.svg?branch=master)](https://github.com/lunamidori5/Midori-AI/actions/workflows/Linux_Build_Test.yml)
{{% /tab %}}
{{% tab title="Other OS" %}}
### Prerequisites
- [Docker Engine](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/)
- [Python 3.10](https://www.python.org/downloads/release/python-3100/)
- [Python Venv](https://virtualenv.pypa.io/en/latest/installation.html)

### Recommended
***Do not use on windows***

Please make a folder for the Manager program with nothing in it, do not use the user folder.

### Manual download

Download this file

```bash
https://raw.githubusercontent.com/lunamidori5/Midori-AI/master/other_files/midori_ai_manager/subsystem_python_runner.py
```

### Running the program

Open a terminal and run:

```bash
python3 -m venv venv
source venv/bin/activate
python3 subsystem_python_runner.py
```
{{% /tab %}}
{{< /tabs >}}

{{% notice style="info" title="Notice" %}}
Reminder to always use your computers IP address not ``localhost`` when using the Midori AI Subsystem!
{{% /notice %}}

## ----- Install Backends -----
- [LocalAI]({{%relref "subsystem/local-ai" %}}) - For LLM inference, Embedding, and more
- [AnythingLLM]({{%relref "subsystem/anythingllm" %}}) - For chating with your docs using LocalAI or other LLM hosts
- Big-AGI - For chating with your docs using LocalAI or other LLM hosts
- [InvokeAI]({{%relref "subsystem/invokeai" %}}) - For making photos using AI models
- Axolotl - For training your own fine tuned LLMs

## ----- Model Info and Links -----

Check out our [Model Repository]({{%relref "models" %}}) for info about the models used and supported!


## ----- FAQs about the subsystem -----

1. **What is the purpose of the Midori AI Subsystem?**
   - The Midori AI Subsystem is a modular and extensible platform for managing AI workloads, providing simplified deployment, standardized configurations, and isolation for AI systems.

2. **How does the Midori AI Subsystem simplify AI deployment?**
   - The Midori AI Subsystem simplifies AI deployment by providing a streamlined and efficient way to deploy AI systems using Docker container technology, reducing complexities and ensuring consistent and predictable behavior.

3. **What are the benefits of using the Midori AI Subsystem?**
   - The benefits of using the Midori AI Subsystem include simplified deployment, standardized configurations, isolation for AI systems, and a growing library of supported backends and tools.

4. **What are the limitations of the Midori AI Subsystem?**
   - The limitations of the Midori AI Subsystem include its current beta status, potential for bugs, and reliance on Docker container technology.

5. **What are the recommended prerequisites for using the Midori AI Subsystem?**
   - The recommended prerequisites for using the Midori AI Subsystem include Docker Desktop Windows or Docker installed on other operating systems, and a dedicated folder for the Manager program.

6. **How do I install the Midori AI Subsystem Manager?**
   - You can install the Midori AI Subsystem Manager by downloading the appropriate package for your operating system from the Midori AI Subsystem website and following the installation instructions. [Click here to go to the Midori AI Subsystem website](https://io.midori-ai.xyz/subsystem/manager/)

7. **Where can I find more information about the Midori AI Subsystem?**
   - You can find more information about the Midori AI Subsystem on the Midori AI Subsystem website, which includes documentation, tutorials, and a community Discord.

8. **What is the difference between the Midori AI Subsystem and other AI frameworks?**
   - The Midori AI Subsystem differs from other AI frameworks by providing a modular and extensible platform specifically designed for managing AI workloads, offering features such as simplified deployment, standardized configurations, and isolation for AI systems.

9. **How does the Midori AI Subsystem handle security?**
   - The Midori AI Subsystem does not handle security directly, but it relies on the security features provided by the underlying Docker container technology and the specific AI backends and tools being used.

10. **What are the plans for future development of the Midori AI Subsystem?**
   - The plans for future development of the Midori AI Subsystem include adding new features, improving stability and performance, and expanding the library of supported backends and tools.

> Questions from [Carly Kay](https://io.midori-ai.xyz/about-us/carly-api/)

## ----- Disclaimer -----

The functionality of this product is subject to a variety of factors that are beyond our control, and we cannot guarantee that it will work flawlessly in all situations. We have taken every possible measure to ensure that the product functions as intended, but there may be instances where it does not perform as expected. Please be aware that we cannot be held responsible for any issues that arise due to the product's functionality not meeting your expectations. By using this product, you acknowledge and accept the inherent risks associated with its use, and you agree to hold us harmless for any damages or losses that may result from its functionality not being guaranteed.

## ----- Footnotes -----

*For your safety we have posted the code of this program onto github, please check it out! - [Github](https://github.com/lunamidori5/Midori-AI/tree/master/other_files)

**If you would like to give to help us get better servers - [Give Support](https://paypal.me/midoricookieclub?country.x=US&locale.x=en_US)

***If you or someone you know would like a new backend supported by Midori AI Subsystem please reach out to us at [contact-us@midori-ai.xyz](mailto:contact-us@midori-ai.xyz)