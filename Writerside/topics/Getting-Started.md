# Getting Started

Below are detailed outlines that contain the steps that you will need in order to get 

> **Act depends on Docker to run workflows.**
>
> You will need to install Docker prior to jumping to the tutorial
>
{style="warning"}


## Install Nektos/Act
There are two ways in which you can download the open source code, either through a package manager or installing the binary manually.
#### Install via Package Manager
<tabs>
<tab title="MacOS">
<procedure type="steps">
<step>Please be sure to follow the steps outlined in <a href="https://docs.docker.com/docker-for-mac/install/">Docker Docs for how to install Docker Desktop for Mac</a>.</step>
<step>Install the Act open source code onto your machine:
<br/>
<code-block lang="bash">brew install act</code-block>
</step>
</procedure>
</tab>
<tab title="Widows">
<procedure type="steps">
<step>Please be sure to follow the steps outlined in <a href="https://docs.docker.com/docker-for-windows/install/">installing Docker Desktop on Windows</a>.</step>
<step>Install the Act open source code onto your machine via one of the Windows package managers:
<br/>
<tabs>
<tab title="Chocolatey"><code-block lang="shell">choco install act-cli</code-block></tab>
<tab title="Scoop"><code-block lang="shell">scoop install act</code-block></tab>
<tab title="Winget"><code-block lang="shell">winget install nektos.act</code-block></tab>
</tabs>
</step>
</procedure>
</tab>
</tabs>

#### Install Manually
> **You can skip this section if you completed the installation steps above**
> 
> Please note, it is typically easiest to install via one of the package managers
>
{style="note"}

<br/>
Download the [latest release](https://github.com/nektos/act/releases/latest) and add the path to your binary into your PATH.

## Download Tutorial Repo
In order to work through the tutorials, you will need to run the following clone:
```Bash
git clone https://github.com/a-barker-kr/local-gha-runners-demo.git
```