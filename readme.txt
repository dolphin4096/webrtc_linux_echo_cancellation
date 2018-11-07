/*
Use For   : Linux echo cancellation compiling with webrtc
Date      : 20181107
Copyright : dolphin 
Email     : lhy09027@126.com
*/
How to make a test sample

#tar -xf EchoCancellation_webrtc.tar.gz 
#cd WebRtcAudioAllTest/
#cd WebRtcAudioTest/
#make


If you meet errors below when compiling ,you can just "# make" again ,
it's beacuse when creating tmp/ directory and copy *.o ,compile file will 
sometimes not synchronize with tmp/ directory. 
You can fix it yourself.


"
make[1]: Leaving directory '/media/sf_ubuntu_16_share_dir/WebRtcAudioAllTest/WebRtcAudioTest/tmp'
/tmp/ccRH2Q9W.o: In function `WebRtcNS32KSample':
WebRtcAudioTest.c:(.text+0x8e): undefined reference to `WebRtcNs_Create'
WebRtcAudioTest.c:(.text+0xa4): undefined reference to `WebRtcNs_Init'
WebRtcAudioTest.c:(.text+0xb9): undefined reference to `WebRtcNs_set_policy'
WebRtcAudioTest.c:(.text+0x2e5): undefined reference to `WebRtcSpl_AnalysisQMF'
WebRtcAudioTest.c:(.text+0x313): undefined reference to `WebRtcNs_Process'
WebRtcAudioTest.c:(.text+0x345): undefined reference to `WebRtcSpl_SynthesisQMF'
WebRtcAudioTest.c:(.text+0x3d3): undefined reference to `WebRtcNs_Free'
/tmp/ccRH2Q9W.o: In function `WebRtcAgcTest':
WebRtcAudioTest.c:(.text+0x480): undefined reference to `WebRtcAgc_Create'
WebRtcAudioTest.c:(.text+0x4b5): undefined reference to `WebRtcAgc_Init'
WebRtcAudioTest.c:(.text+0x4e6): undefined reference to `WebRtcAgc_set_config'
WebRtcAudioTest.c:(.text+0x5c2): undefined reference to `WebRtcAgc_Process'
WebRtcAudioTest.c:(.text+0x644): undefined reference to `WebRtcAgc_Free'
/tmp/ccRH2Q9W.o: In function `WebRtcAecTest':
WebRtcAudioTest.c:(.text+0x709): undefined reference to `WebRtcAec_Create'
WebRtcAudioTest.c:(.text+0x725): undefined reference to `WebRtcAec_Init'
WebRtcAudioTest.c:(.text+0x74f): undefined reference to `WebRtcAec_set_config'
WebRtcAudioTest.c:(.text+0x7b0): undefined reference to `WebRtcAec_BufferFarend'
WebRtcAudioTest.c:(.text+0x7e1): undefined reference to `WebRtcAec_Process'
WebRtcAudioTest.c:(.text+0x848): undefined reference to `WebRtcAec_Free'
collect2: error: ld returned 1 exit status
Makefile:23: recipe for target 'all' failed
make: *** [all] Error 1
"