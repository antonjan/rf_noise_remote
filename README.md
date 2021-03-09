# rf_noise_remote
## Dependincies
 soapysdrplay ver 1 driver<br>
 all the Soapy miri drivers<br>
 soapy all sudo -H pip3 install numpy<br>
 sudo -H pip3 install simplesoapy<br>
 sudo -H pip3 install simplespectral<br>
 sudo -H pip3 install soapy_power<br>

my heatmap.py that works with 12 bit not just 8bit SDR
## dont istall python 2
## soapy_power -g 10 -d driver=miri  -f 1M:30M -B 2000 -F rtl_power --tune-delay 1 2>/dev/null |grep 2021 > rfnoise.csv
## 
This is the code for the new V3 rf noise system
