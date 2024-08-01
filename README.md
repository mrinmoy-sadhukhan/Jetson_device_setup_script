# Jetson_device_setup_script
 Different script to fill the jetson xavier nx with different perks 
Jetson Xavier NX setup with jetpack 4.6.5
========================
Jetpack 4.6.5 is installed with jtop and other software to run python programme

https://rnext.it/jetson_stats/troubleshooting.html
```
sudo apt update
sudo apt install vino
sudo auto remove
sudo apt autoremove
mkdir -p ~/.config/autostart
cp /usr/share/applications/vino-server.desktop ~/.config/autostart
gsettings set org.gnome.Vino prompt-enabled false
gsettings set org.gnome.Vino require-encryption false
gsettings set org.gnome.Vino authentication-methods "['vnc']"
gsettings set org.gnome.Vino vnc-password $(echo -n 'thepassword'|base64)
sudo apt install python3-pip
sudo pip3 install -U jetson-stats
sudo pip3 install -U testresources setuptools
```
For create swap manually
```
sudo jetson_swap -s 4
jetson_swap -t
```
Install VSCode in Jetson Xavier NX
```
wget -N -O vscode-linux-deb.arm64.deb https://update.code.visualstudio.com/1.72.1/linux-deb-arm64/stable
sudo apt install ./vscode-linux-deb.arm64.deb
```
Install h5py for tensorflow first install h5py 3.1.0 then install 2.0
```
sudo apt install cython3
sudo pip3 install -U pybind11 pkgconfig
pip3 install cython
sudo env H5PY_SETUP_REQUIRES=0 pip3 install -U --no-build-isolation h5py==3.1.0
pip3 install numpy==1.19.2
pip3 install tensorflow-2.7.0+nv22.1-cp36-cp36m-linux_aarch64.whl
pip3 install kera==2.6.0
sudo pip3 install -U future==0.18.2 mock==3.0.5 h5py==2.10.0 keras_preprocessing==1.1.2 keras_applications==1.0.8 gast==0.2.2 futures
pip3 install scikit-learn
pip3 install scikit-image
pip3 install ipykernel
pip3 install tqdm

```