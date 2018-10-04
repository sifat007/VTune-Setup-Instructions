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
- Need to load build and load the sampling drivers (With help of SNA)
- Need to set proc/sys/kernel/perf_event_paranoid to 0 (With help of SNA)
```
echo "0" > proc/sys/kernel/perf_event_paranoid
```
- Need to have a licence file. For now just download the licence file attached and put it in a directory of your choice. Then put this line in the ~/.bashrc file.

```
export INTEL_LICENSE_FILE="${INTEL_LICENSE_FILE}:<licence_file_directory>"
```
Please replace <licence_file_directory> with the directory that contains the `*.lic` file
