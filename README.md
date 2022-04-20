# CuckooCounter
Cuckoo Counter: Adaptive Structure of Counters for Accurate Frequency and Top-k estimation

2022.04.20: We have updated the revised source code of Cuckoo Counter, thanks a lot to the insight comments from our anonymous reviewers. Particularly, we modified the query function to return 0 if there is an empty entry in the searched bucket (It should be note that this modification has little effect on the following experimental results, because when the memory is small and the data is large, it is difficult to find an empty entry in CC), besides, we add some recently proposed algorithms for comparison in our revised source code. Feel free to contact with me if you have any questions.
