# MSBX 5420 Group Project

The objective of this group project is to use what we learned in this course to solve some interesting and important problems. I will encourage you to define what is interesting and important from your business perspective. Team members may have different expertise: if you are strong with business - try to contribute from a business perspective, if you are strong in coding - try to contribute to coding. Teams are self-formed with 4-5 members. Anyone without a team will be randomly assigned into teams. Team information will be finalized by the end of March 13.

## Project Requirements

### Basic Requirements

* Dataset: You can use any dataset in the project. However, your data should have substantial size. This is a big data course so datasets below 10MB are not allowed. Some suggested datasets are provided; you can use or collect your own data if you would like.
* Environment: You can use Docker or MyBinder to test your code. In the end, you are required to use AWS EMR cluster to run your analysis.
* Programming Language: You can use any type of programming languages or business analytics tools, but must include the use of Spark with Python (PySpark), which needs to be deployed on the cluster; that is, if you need to implement a specific feature but it is not available in Spark, you have the flexibility to justify it and use other tools, but meanwhile you still need to make sure you have something implemented by PySpark in that case.

### Functional Requirements

* Data Ingestion: You can read local files when developing your code locally, but when deploying your code on AWS cluster, you need to save your dataset into HDFS or AWS. Then read data from HDFS or S3 to do analysis on the AWS cluster. Typically S3 is more convenient in this project because the data in S3 can be shared across clusters.
* Basic statistics and analysis of the ingested dataset (with PySpark or other packages if necessary) and display your insights (use Jupyter notebook or other type of visualization).

### Performance Requirements

* You can test your application or analysis on your laptop with Docker or on MyBinder; you are suggested to make sure your code work on Docker or MyBinder first then run it on the cluster.
* With your application deployed on the cluster, your implementation should show horizontal scale (i.e., when adding more nodes the cluster, the processing should be faster) and take advantage of distributed computing.

## Project Timeline and Deliverable

> For all project deliverables, they should be submitted on Canvas by one of the team members

* ***<u>Project Proposal (Due before Week 13 Consultations):</u>*** You will need to develop a <u>one-page proposal</u> of your project (the second page will not be graded), to <u>discuss the dataset you would like to use</u> and <u>the problems you want to solve from the data</u>. Please be concise on your proposal and motivate your problems - why the problems you want to investigate are <u>important</u> and <u>interesting</u>. Submit your project proposal <u>two days before your consultation slot</u>. Note that the proposal is only a summary of your plan and progress, your actual progress doesn't have to be constrained by it. 
* ***<u>Project Consultation (Week 13 Apr 4-10):</u>*** Your team will make an appointment (30 mins) with instructor by choosing your time slots (which will be confirmed in Week 12). You will discuss your project with instructor, demonstrate your preliminary works, and get feedback on solving the problems. It is recommended that all team members join the consultation to demonstrate you are working as a whole team. No-show in consultation without reasons will affect participation grade.
* ***<u>Project Presentation (Week 15 Apr 18/20):</u>*** You will present your problem and analysis (insights) in the class. Your presentation date (April 18 or 20) will be determined by the section of the majority of team members. You are required to do in-person presentation, if possible; only if you have special constraints or you are distance education students, you can do pre-recorded videos for presentation. Submit your presentation slides (and pre-recorded videos, if applicable) on the same day of your presentation. The order of presentation will be decided by lucky draw.
* ***<u>Project Implementation (Due April 28):</u>*** You will refine your project after presentation and submit your final application (code, data, etc.) in the project as the deliverable of implementation.
* ***<u>Project Report (Due April 28):</u>*** Based on your problems and insights, you will write a project report to motivate your problem, describe the dataset you use, present your findings and discuss the implications of your findings.

## Project Grading (40% in total)

> Grades on Canvas will be 10 pts, 20 pts, 30 pts and 40 pts for each of the component, respectively. Then the total (100 pts) will be converted as 40% of final grade.

* ***<u>Project Proposal (4%):</u>*** Please be concise on your proposal within one-page. <u>Contents exceeding one-page will not be graded.</u>
* ***<u>Project Presentation (8%):</u>*** Presentation will be 13-16 (to be updated based on total groups) mins for each group. Make sure your presentation length fall into the range. For either in-person or pre-recorded presentation, make sure all of your team members have engagement in the presentation.
* ***<u>Project Implementation (12%):</u>*** Your implementation (analysis and code) will take 8%, while the deployment of your application (pyspark implementation) on the cluster will take 4%.
* ***<u>Project Report (16%):</u>*** The final report has no page limits (typically 10-15 pages would be sufficient). Your final report should include the following components: 
  * Abstract / summary of your report
  * The background and motivation of your questions
  * The dataset and analysis methods
  * The results and insights you have obtained
  * Discuss the implications or stories

## Some Recommendations on Datasets

You can use any dataset you want for this project. In case you have troubles in searching for dataset, some data sources are provided here.

* COVID-19 related data ([https://www.kaggle.com/datasets?topic=covidDataset](https://www.kaggle.com/datasets?topic=covidDataset))
* AWS opendata ([https://registry.opendata.aws/](https://registry.opendata.aws/))
* Amazon review data ([http://jmcauley.ucsd.edu/data/amazon/](http://jmcauley.ucsd.edu/data/amazon/))
* Airbnb data ([http://insideairbnb.com/get-the-data](http://insideairbnb.com/get-the-data))
* Bike share data ([https://www.citibikenyc.com/system-data](https://www.citibikenyc.com/system-data) or [https://www.lyft.com/bikes/bay-wheels/system-data](https://www.lyft.com/bikes/bay-wheels/system-data))
* GitHub data ([https://www.githubarchive.org/](https://www.githubarchive.org/) or [https://ghtorrent.org/](https://ghtorrent.org/))
* Bitcoin data ([https://www.kaggle.com/bigquery/bitcoin-blockchain](https://www.kaggle.com/bigquery/bitcoin-blockchain))
* Lending data ([https://www.kaggle.com/wordsforthewise/lending-club](https://www.kaggle.com/wordsforthewise/lending-club) or [https://www.kiva.org/build/data-snapshots](https://www.kiva.org/build/data-snapshots))
* Sports data ([https://www.kaggle.com/datasets/hugomathien/soccer](https://www.kaggle.com/datasets/hugomathien/soccer))
* E-Sports data ([https://www.kaggle.com/devinanzelmo/dota-2-matches](https://www.kaggle.com/devinanzelmo/dota-2-matches) or [https://www.kaggle.com/skihikingkevin/pubg-match-deaths](https://www.kaggle.com/skihikingkevin/pubg-match-deaths))

## Cluster Environment Notes

### Connect to AWS EMR Cluster

> The AWS EMR clusters for project are available from March 30 to April 30

* Leeds AWS EMR Cluster: Leeds Technology Service has created a series of AWS clusters for the project. 

* Host addresses are:

  * cluster 1: *ec2-34-220-138-138.us-west-2.compute.amazonaws.com*

  * cluster 2: *ec2-52-11-151-94.us-west-2.compute.amazonaws.com*

  * cluster 3: *ec2-52-39-35-5.us-west-2.compute.amazonaws.com*

* Private key files are same with the first cluster - `MSBX5420-SPR22.pem` and `MSBX5420-SPR22.ppk`

* For any cluster, create your team directory under absolute path `/mnt1/msbx5420_teams` first and then copy your files to your team directory with `scp`

* All personal directories (if needed) are under `/mnt1/msbx5420` and all team directories are under `/mnt1/msbx5420_teams`

* Please follow the rules to use cluster and create directories. Do not to use the directories under entry directory when you upload large files; it will overload the disk size of master node. If the user directory is full, directories under entry directory will be migrated to `/mnt1/msbx5420_teams`.

* Commands to access cluster and copy file from laptop to cluster (make sure your `MSBX5420-SPR22.pem` inside your current directory)

  ```bash
  #cluster 1
  ssh -i MSBX5420-SPR22.pem hadoop@ec2-34-220-138-138.us-west-2.compute.amazonaws.com
  scp -i MSBX5420-SPR22.pem your_file hadoop@ec2-34-220-138-138.us-west-2.compute.amazonaws.com:/mnt1/msbx5420_teams/team_directory
  #cluster 2
  ssh -i MSBX5420-SPR22.pem hadoop@ec2-52-11-151-94.us-west-2.compute.amazonaws.com
  scp -i MSBX5420-SPR22.pem your_file hadoop@ec2-52-11-151-94.us-west-2.compute.amazonaws.com:/mnt1/msbx5420_teams/team_directory
  #cluster 3
  ssh -i MSBX5420-SPR22.pem hadoop@ec2-52-39-35-5.us-west-2.compute.amazonaws.com
  scp -i MSBX5420-SPR22.pem your_file hadoop@ec2-52-39-35-5.us-west-2.compute.amazonaws.com:/mnt1/msbx5420_teams/team_directory
  ```

* You can also use Putty or FileZilla to connect cluster, forward port and transfer files (with `MSBX5420-SPR22.ppk`)

> If the main cluster is crowded and hard to get access, you can use a smaller backup cluster below; but still, make sure your code has been tested locally with anaconda or docker first.

* Commands to access cluster, upload files and connect JupyterHub

  ```bash
  #cluster 1
  ssh -i MSBX5420-SPR22.pem hadoop@ec2-34-220-138-138.us-west-2.compute.amazonaws.com
  scp -i MSBX5420-SPR22.pem your_file hadoop@ec2-34-220-138-138.us-west-2.compute.amazonaws.com:/mnt1/msbx5420_teams/team_directory
  ssh -i MSBX5420-SPR22.pem -N -L localhost:8890:localhost:9443 hadoop@ec2-34-220-138-138.us-west-2.compute.amazonaws.com
  #cluster 2
  ssh -i MSBX5420-SPR22.pem hadoop@ec2-52-11-151-94.us-west-2.compute.amazonaws.com
  scp -i MSBX5420-SPR22.pem your_file hadoop@ec2-52-11-151-94.us-west-2.compute.amazonaws.com:/mnt1/msbx5420_teams/team_directory
  ssh -i MSBX5420-SPR22.pem -N -L localhost:8891:localhost:9443 hadoop@ec2-52-11-151-94.us-west-2.compute.amazonaws.com
  #cluster 3
  ssh -i MSBX5420-SPR22.pem hadoop@ec2-52-39-35-5.us-west-2.compute.amazonaws.com
  scp -i MSBX5420-SPR22.pem your_file hadoop@ec2-52-39-35-5.us-west-2.compute.amazonaws.com:/mnt1/msbx5420_teams/team_directory
  ssh -i MSBX5420-SPR22.pem -N -L localhost:8892:localhost:9443 hadoop@ec2-52-39-35-5.us-west-2.compute.amazonaws.com
  ```

* All clusters share the same AWS S3 bucket; if you read data from S3, you don't need to do additional steps

### Use Jupyter Notebook on Cluster

* Use ssh port forwarding to connect to JupyterHub (or add `-f` to have persistent connection in the backend)

  ```bash
  #cluster 1
  ssh -i MSBX5420-SPR22.pem -N -L localhost:8890:localhost:9443 hadoop@ec2-34-220-138-138.us-west-2.compute.amazonaws.com
  #cluster 2
  ssh -i MSBX5420-SPR22.pem -N -L localhost:8891:localhost:9443 hadoop@ec2-52-11-151-94.us-west-2.compute.amazonaws.com
  #cluster 3
  ssh -i MSBX5420-SPR22.pem -N -L localhost:8892:localhost:9443 hadoop@ec2-52-39-35-5.us-west-2.compute.amazonaws.com
  ```

* Create JupyterHub user for your team <u>on the cluster master node (after ssh to the cluster)</u>. *<u>If you use multiple clusters for JupyterHub, please make sure you have the same username across the clusters.</u>* This will make all your users in different clusters share the notebooks.

  ```bash
  sudo docker exec jupyterhub useradd -m -s /bin/bash -N username
  sudo docker exec jupyterhub bash -c "echo username:password | chpasswd"
  ```

* Go to `https://localhost:8890` (cluster 1), or `https://localhost:8891` (cluster 2), or `https://localhost:8892` (cluster 3) in browser and login with your team username and password; then create or upload your notebooks.

* When you see security warning, click "Advanced" or "Details" to continue and bypass it. If you are using MacOS Catalina with Chrome, blindly type `thisisunsafe` in the page and press `enter` to bypass it.

* To run PySpark program, use the kernel `PySpark` for notebook. If you need additional python packages, let the instructor know as early as possible. **Please do not install packages yourself**.

* In the notebook, make sure you specify `spark://spark-master:7077` or `yarn` in `master()` rather than using `local`

* Please avoid uploading data files in JupyterHub. The data files you upload to JupyterHub workspace cannot be loaded by PySpark kernel and running analysis directly from the data file in the workspace will easily overload the master node.

###  Use HDFS on Cluster

* You are recommended to use AWS S3 in case you need to switch cluster, but HDFS is still a valid option
* Create your team directory in HDFS under `/msbx5420_teams/team_directory`
* Copy files in `/mnt1/msbx5420_teams/team_directory` from master node of cluster to HDFS under `/msbx5420_teams/team_directory`
* Save or read data in spark application with HDFS path `/msbx5420_teams/team_directory/file.name`
* Try to clean up your files on the master node after you put them to HDFS (or S3)

### Use AWS S3 Bucket on Cluster

* Our S3 bucket on cluster is `s3://msbx5420-spr22`

* HDFS storage is limited in the cluster, so if HDFS is not available, upload your file to S3 bucket, which is similar

* Also data stored in S3 can be shared across clusters, so if you use both clusters, S3 can be more convenient. That is, S3 doesn't rely on the cluster, so if there is any issue on the cluster, what you save on S3 won't lose.

* To check files and copy files to S3 bucket, you can use the following commands (make sure you have created your team directory on master node)

  ```bash
  aws s3 ls s3://msbx5420-spr22
  aws s3 ls s3://msbx5420-spr22/team_directory/
  #copy single file, the last / is required
  aws s3 cp /mnt1/msbx5420_teams/team_directory/file.name s3://msbx5420-spr22/team_directory/
  #copy the entire directory
  aws s3 cp /mnt1/msbx5420_teams/team_directory s3://msbx5420-spr22/team_directory --recursive
  ```

* Save or read data on S3 bucket with S3 path `s3://msbx5420-spr22/team_directory/file.name`

