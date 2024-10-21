# Ros2

# first start

once the dev container is open follow https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html

before https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html#id5 there might be an issue you need to go
into /etc/apt/sources.list.d and remove the ros2.list

after completing the Ros2 tutorial you need to install [just](https://crates.io/crates/just) and python-env

```bash
sudo apt install just python3-full
```

in case you have already run `just init` make sure the ~/.bashrc is clear of old `source` statements!

next:

```bash
just init
```

after running `just init` you will need to select the created python environment.
Python (bottom right) -> add new interpreter -> add local interpreter -> remove the . from /home/ws/.venv -> select
existing interpreter

open a new terminal (opening a new terminal will always be a good debug / fixing step)

next install all the dependencies

```bash
just install
```

build the project

```bash
just build
```

run the fetchAI agent

```bash
just run-agent
```

---

you can also test if everything is working by

```bash
ros2 run py_pubsub listener
```

and in a new terminal

```bash
ros2 run py_pubsub talker
```
