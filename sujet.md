# Practical Session #1: Introduction

1. Find in news sources a general public article reporting the discovery of a software bug. Describe the bug. If possible, say whether the bug is local or global and describe the failure that manifested its presence. Explain the repercussions of the bug for clients/consumers and the company or entity behind the faulty program. Speculate whether, in your opinion, testing the right scenario would have helped to discover the fault.

2. Apache Commons projects are known for the quality of their code and development practices. They use dedicated issue tracking systems to discuss and follow the evolution of bugs and new features. The following link https://issues.apache.org/jira/projects/COLLECTIONS/issues/COLLECTIONS-794?filter=doneissues points to the issues considered as solved for the Apache Commons Collections project. Among those issues find one that corresponds to a bug that has been solved. Classify the bug as local or global. Explain the bug and the solution. Did the contributors of the project add new tests to ensure that the bug is detected if it reappears in the future?

3. Netflix is famous, among other things we love, for the popularization of *Chaos Engineering*, a fault-tolerance verification technique. The company has implemented protocols to test their entire system in production by simulating faults such as a server shutdown. During these experiments they evaluate the system's capabilities of delivering content under different conditions. The technique was described in [a paper](https://arxiv.org/ftp/arxiv/papers/1702/1702.05843.pdf) published in 2016. Read the paper and briefly explain what are the concrete experiments they perform, what are the requirements for these experiments, what are the variables they observe and what are the main results they obtained. Is Netflix the only company performing these experiments? Speculate how these experiments could be carried in other organizations in terms of the kind of experiment that could be performed and the system variables to observe during the experiments.

4. [WebAssembly](https://webassembly.org/) has become the fourth official language supported by web browsers. The language was born from a joint effort of the major players in the Web. Its creators presented their design decisions and the formal specification in [a scientific paper](https://people.mpi-sws.org/~rossberg/papers/Haas,%20Rossberg,%20Schuff,%20Titzer,%20Gohman,%20Wagner,%20Zakai,%20Bastien,%20Holman%20-%20Bringing%20the%20Web%20up%20to%20Speed%20with%20WebAssembly.pdf) published in 2018. The goal of the language is to be a low level, safe and portable compilation target for the Web and other embedding environments. The authors say that it is the first industrial strength language designed with formal semantics from the start. This evidences the feasibility of constructive approaches in this area. Read the paper and explain what are the main advantages of having a formal specification for WebAssembly. In your opinion, does this mean that WebAssembly implementations should not be tested? 

5.  Shortly after the appearance of WebAssembly another paper proposed a mechanized specification of the language using Isabelle. The paper can be consulted here: https://www.cl.cam.ac.uk/~caw77/papers/mechanising-and-verifying-the-webassembly-specification.pdf. This mechanized specification complements the first formalization attempt from the paper. According to the author of this second paper, what are the main advantages of the mechanized specification? Did it help improving the original formal specification of the language? What other artifacts were derived from this mechanized specification? How did the author verify the specification? Does this new specification removes the need for testing?

## Answers

By [Coroller Ilona](https://gitlab.istic.univ-rennes1.fr/icoroller) and [Bouvier Benjamin](https://gitlab.istic.univ-rennes1.fr/bebouvier)

1. Rennes buses were stopped by a bug.
>The 22th february the drivers couldn’t know their routes due to an update of servers during the night.
Only **30%** of the drivers were able to be on time between 5:00 and 8:30.
To speculate on the bug, we don't have enough information to know if it was preventable. So maybe they didn't do enough testing, or test all the possibilities, and then the bug could have been avoided.

[link to the article](https://www.francebleu.fr/infos/faits-divers-justice/les-bus-de-rennes-a-l-arret-a-cause-d-un-bug-informatique-1645513653)


3. Chaos engineering 
   
what are the requirements for these experiments, what are the variables they observe and what are the main results they obtained.

>Chaos engineering is a way to test the robustness of a service or a software. The idea is to crash a part to see if the application can withstand turbulent conditions. So any online project could be tested with this way to verify its capacity so stay online every time. Diferents companies are already using this method such as amazon, facebook, google… For exemple as metric, netflix use SPS , for (stream) starts per second and new account signups per second. There is a strong, obvious link between these metrics and the availability of the system. This metrics depends a lot of from the domain of the application. If you are an e commence xwebsite you could use as metric the umber of completed purchases per second, where an ad­serving service might use numbers of ads viewed by users per second.

