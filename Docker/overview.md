# Setup with Docker

#### Overview

As Docker is a convenient way to setup the software environment, we also provide an easier way to deploy `SnpHub` based on [Docker](https://www.docker.com/).

To setup `Snphub` using `Docker`, you need to **install** `Docker` on your server first.

Also, `samtools`, along with `bcftools`, `tabix` and `seqkit` still need to **be installed** in order to pre-process your data.

#### Step.1

Clone (or download) project `snphub4docker` from GitHub.

```sh
git clone https://github.com/esctrionsit/snphub4docker
```

#### Step.2

Create `Docker` image of `SnpHub`.

```sh
cd snphub4docker
sudo ./snphub create image
```
Root permission is needed because of `Docker`.

#### Step.3

Pre-process your own re-seq data. (Or **jump** this step if just want to try on our **sample** data.)

**Firstly**, you need to **fulfill** the `setup.conf`.
```sh
vi ./setup.conf
```
Put the needed files into a folder, and fulfill `setup_config.R` with their name and folder path.
An **template data folder** is provided at `snphub4docker/Template_data`.

**Then**, run command below to pre-process your data.

```sh
./snphub init -y
```

#### Step.4

Now, you can try `SnpHub` by creating a container (instance), binding your host port with it, and mount your own data (if there is).

```sh
# Try demo data
sudo ./snphub create container -p 5123
# Mount own data
sudo ./snphub create container -p 5123 -v /data/user_data
```

Options:
- `-p`: Bind the host port with container. A **random** port will be bound when **ignoring** this parameter.
- `-v`: Mount your own **pre-processed** re-seq data into container. `SnpHub` will run on a **sample data** when **ignoring** this parameter.

#### Step.5

Open your browser, and enjoy at `http://localhost:5123`.

(Port is the one that you choose at step.4 or a random value. Check more details using `./snphub list`)

#### Parameters of the command: snphub

```text
Program : snphub (Tools for visualizing re-seq data)
Version:  1.0.0
Updated on: Jun. 4th, 2020
Usage:    snphub <command> [options]
Commands:
  -- SnpHub on docker
     create      + to create a SnpHub Docker image or container
     list          to list all the containers created
     start         start a specific container
     stop          stop a specific container
     kill          kill (force stop) a specific container
     rm            delete a specific container
  -- SnpHub data pre-processing
     init          pre-processing the user provided re-seq data
Note: 
  Commands contain sub-commands are marked with "+" 
  Generally any operate on Docker needs root authority.
  We recommend to use root account when using commands related to Docker.
  Or using "sudo snphub <command> [options]".
```