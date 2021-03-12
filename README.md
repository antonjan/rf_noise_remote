# rf_noise_remote
This heatmap.py can handel 12bit 4096 values from sdrplay and miri decice using soapy_power
## Dependincies
 soapysdrplay ver 1 driver<br>
 all the Soapy miri drivers<br>
 soapy all sudo -H pip3 install numpy<br>
 sudo -H pip3 install simplesoapy<br>
 sudo -H pip3 install simplespectral<br>
 sudo -H pip3 install soapy_power<br>
 sudo apt-get install libatlas-base-dev  #fix numpy problem

my heatmap.py that works with 12 bit not just 8bit SDR<br>
## dont install python 2
soapy_power -g 10 -d driver=miri  -f 1M:30M -B 2000 -F rtl_power --tune-delay 1 2>/dev/null |grep 2021 > rfnoise.csv<br>
/home/pi/rf_noise_remote/heatmap.py --db -60 -130 /home/pi/rfnoise.csv /home/pi/rfnoise.png

## 
This is the code for the new V3 rf noise system
# sampeling is done
WARNING: Sample rate 2000000.0 Hz is not supported, setting it to 8000000.0 Hz!<br>
INFO: Using device: miri<br>
INFO: repeats: 1600<br>
INFO: samples: 6400000 (time: 0.80000 s)<br>
INFO: max_buffer_size (samples): 13107200 (repeats: 3276.80, time: 1.63840 s)<br>
Lost samples!<br>
1a a1 39 cc 28 b0 00 00 d5 4e a7 82 f5 07 76 ef <br>
INFO: buffer_size (samples): 6400000 (repeats: 1600.00, time: 0.80000 s)<br>
Lost samples!<br>
INFO: buffer_repeats: 1<br>
INFO: overlap: 0.00000<br>
INFO: bin_size: 2000.00 Hz<br>
INFO: bins: 4000<br>
INFO: bins (after crop): 4000<br>
INFO: sample_rate: 8.000 MHz<br>
INFO: sample_rate (after crop): 8.000 MHz<br>
INFO: freq_range: 29.000 MHz<br>
INFO: hopping: YES<br>
INFO: hop_size: 8.000 MHz<br>
INFO: hops: 4<br>
INFO: min_center_freq: 5.000 MHz<br>
INFO: max_center_freq: 29.000 MHz<br>
INFO: min_freq (after crop): 1.000 MHz<br>
INFO: max_freq (after crop): 33.000 MHz<br>

