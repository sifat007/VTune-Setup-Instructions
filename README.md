# VTune Setup Instructions

- VTune 2019 is installed in the folder: /usr/local/vtune_amplifier_2019/
- VTune can be run using this command - 
```
/usr/local/vtune_amplifier_2019/vtune_amplifier_2019.0.2.570779/bin64/amplxe-gui
```
- If you don't want to type the path everytime just add this line
  ```
  export PATH="${PATH}:/usr/local/vtune_amplifier_2019/vtune_amplifier_2019.0.2.570779/bin64"
  ```
to your ~/.bashrc and run `source ~/.bashrc`
- Then you can just run `amplxe-gui` to launch the VTune GUI.

- Add these two line in the `~/.bashrc` and run `source ~/.bashrc`.
```
source /usr/local/vtune/amplxe-vars.sh
export AMPLXE_MORE_PIN_OPTIONS='-ifeellucky'

```
- Need to build and load the sampling drivers (Per machine and with help of SNA)
```
/usr/local/vtune_amplifier_2019/vtune_amplifier_2019.0.2.570779/sepdk/src/build-driver
```
- Need to set proc/sys/kernel/perf_event_paranoid to 0 (Per machine and with help of SNA)
```
echo "0" > proc/sys/kernel/perf_event_paranoid
```
- Need to have a licence file. For now just download the licence file attached and put it in a directory of your choice. Then put this line in the ~/.bashrc file.

```
export INTEL_LICENSE_FILE="${INTEL_LICENSE_FILE}:<licence_file_directory>"
```
Please replace <licence_file_directory> with the directory that contains the `*.lic` file
