# Cuckoo Counter

* Cuckoo Counter: Adaptive Structure of Counters for Accurate Frequency and Top-k estimation (IEEE/ACM Transactions on Networking)

* Authors: Qilong Shi, Yuchen Xu, Jiuhua Qi, Wenjun Li*, Tong Yang, Yang Xu and Yi Wang (Qilong Shi, Yuchen Xu and Jiuhua Qi contribute equally to this paper, and they conducted this work under the guidance of Wenjun Li and Tong Yang.)
* Corresponding e-mail: wenjunli@pku.org.cn
* Paper Website: http://www.wenjunli.com/CuckooCounter

The test datasets can be downloaded from Releases (on the right side of the webpage, https://github.com/wenjunpaper/CuckooCounter/releases/tag/Datasets).

2022.09.15: We have updated the revised source code of Cuckoo Counter (i.e., CC_R2_Final.zip), thanks a lot to the insight comments from our anonymous reviewers. Particularly, to report the top-k most frequent flows, we add an extra heap. This heap is different from the min-heap in the paper of CM-sketch or HeavyKeeper, it uses the f_start field to record the frequency of a flow when it is first entered into the heap. By adding this field, we can improve the algorithm to filter out some false top-k flows. Experiments show that this optimization improves the accuracy of top-k estimation compared to ordinary min-heap. We also implement Cuckoo Counter on top of BESS (a programmable platform for vSwitch dataplane) to verify the portability of CC on network platforms, and we measure its packet rate and throughput under different memory. Feel free to contact with me if you have any questions.

2022.04.20: We have updated the revised source code of Cuckoo Counter (i.e., CC_R1_Final.zip), thanks a lot to the insight comments from our anonymous reviewers. Particularly, we modified the query function to return 0 if there is an empty entry in the searched bucket (It should be note that this modification has little effect on the following experimental results, because when the memory is small and the data is large, it is difficult to find an empty entry in CC), besides, we add some recently proposed algorithms for comparison in our revised source code. Feel free to contact with me if you have any questions.
