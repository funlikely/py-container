# Ubuntu container with GUI and browser

## On Windows

### Install an X11 Server:
You can use an X11 server for Windows, such as Xming, VcXsrv, or X410. Download and install one of these servers on your Windows machine.

### Configure the X11 Server:
After installing the X11 server, you may need to configure it. For example, you might need to allow connections from localhost or set other preferences. Refer to the documentation of the specific X11 server you chose for instructions on configuration.

### In Powershell:

```
docker run -it --rm `
    --name ubuntu_gui_container `
    -e DISPLAY=:1 `
    -v /tmp/.X11-unix:/tmp/.X11-unix `
    -p 5901:5901 `
    ubuntu_gui
```

### On Host machine browser:

Connect to ``localhost:5901`` to see the UI.
