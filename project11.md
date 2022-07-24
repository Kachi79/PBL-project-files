<img width="672" alt="Screenshot 2022-07-22 at 00 49 34" src="https://user-images.githubusercontent.com/105996656/180333507-c4bf0e8b-b35e-419c-b34e-b7937612ddfd.png">
<img width="672" alt="Screenshot 2022-07-22 at 00 49 34" src="https://user-images.githubusercontent.com/105996656/180333559-1b594371-65b6-4125-8262-bca1f2ef2f77.png">
<img width="672" alt="Screenshot 2022-07-22 at 00 49 34" src="https://user-images.githubusercontent.com/105996656/180333609-3eb689a9-712d-4652-9470-d031497042b9.png">
<img width="672" alt="Screenshot 2022-07-22 at 00 49 34" src="https://user-images.githubusercontent.com/105996656/180333993-7523eecc-8ae7-4bf7-863c-0ab310b0cee5.png">
# ANSIBLE CONFIGURATION MANAGEMENT 
 This task of this project is to install and configure ansible client to act as a Jump Server/Bastion Host and also 
Create a simple ansible playbook to automate servers to automate the configuration of servers.

 The first thing i did was to spin up my EC2 instance on ubuntu and named it Jenkins-Ansible.
The next task was to create a new repository called ansible-config-mgt.
I went on to update my server and install ansible.
<img width="1222" alt="Screenshot 2022-07-21 at 23 38 01" src="https://user-images.githubusercontent.com/105996656/180326784-ed386f06-28c3-4b5e-9ae1-8b439ac33d40.png">
<img width="909" alt="Screenshot 2022-07-21 at 23 39 21" src="https://user-images.githubusercontent.com/105996656/180326901-1f202ba5-ce10-4bcc-ab55-53cc25b22102.png">

To Configure Jenkins build job i had to install jenkins on my server, i created a new Freestyle project and called it ansible in 
Jenkins and pointed it to my ‘ansible-config-mgt’ repository.
<img width="1792" alt="item name on jenkins config" src="https://user-images.githubusercontent.com/105996656/180327759-2b09e358-af40-422d-8146-f94bf0656b9e.png">
  I configured webhook on github.
  <img width="1792" alt="webhook" src="https://user-images.githubusercontent.com/105996656/180328627-d57b6d8a-a698-4ded-8428-a7835bd99a2a.png">

 I tested my setup by making some changes in the README.MD file in the master branch and made sure that builds started
 automatically and Jenkins saved the files (build artifacts) in a mathmatical order.
  <img width="1792" alt="Screenshot 2022-07-21 at 20 35 16" src="https://user-images.githubusercontent.com/105996656/180328665-19009086-4596-4ceb-bbbd-f13b3d0f9377.png">
After configuring my vscode i cloned my github repo through it.

In my cloned repository and i created 2 directories, inventory and playbooks.
<img width="1792" alt="create folders" src="https://user-images.githubusercontent.com/105996656/180627422-0db31cb4-82ad-4244-bf65-43508eff64e8.png">
I went on to create a new branch in my github repository for the purpose of development of new features.

I populated the newly created directories: playbooks and inventory with common.yml and dev.yml files among others
<img width="1751" alt="common" src="https://user-images.githubusercontent.com/105996656/180627614-a3b29e8e-1b6d-4614-b0d5-83f7698042dd.png">
<img width="1516" alt="dev" src="https://user-images.githubusercontent.com/105996656/180627615-aabe25ff-6ccf-4250-8481-ba0c67357263.png">

I imported the keys to the ssh agent using the command :eval `ssh-agent -s`
ssh-add <path-to-private-key>, after that i checked to see that keys were successfully imported.
  <img width="859" alt="private keys added" src="https://user-images.githubusercontent.com/105996656/180627749-ff010f41-7cf0-4a8d-9557-dde1e6e13361.png">
  
  I ssh-ed into the the bastion host using this command: ssh -A ubuntu@public-ip
<img width="897" alt="logged into bastion host" src="https://user-images.githubusercontent.com/105996656/180627764-da005208-170d-47ff-ae69-e546dcc43aaf.png">

I updated my inventory 
  <img width="1516" alt="dev" src="https://user-images.githubusercontent.com/105996656/180627801-90789662-c325-4010-9579-8881ba98f025.png">

I added, commited, pushed and created pull requests and merged by both branches in my github.
  <img width="1792" alt="github merge" src="https://user-images.githubusercontent.com/105996656/180627999-7542acae-f53f-488c-bcf3-9dfd7f58e2d0.png">

  
  <img width="1068" alt="gitgub changes" src="https://user-images.githubusercontent.com/105996656/180627870-9bc4942c-8db1-4377-92e3-6bf88e480680.png">
Finally, i executed my first ansible-playbook to see how ansible really works
  
  <img width="1792" alt="ansible playbook" src="https://user-images.githubusercontent.com/105996656/180627956-58facdfc-d667-4354-a529-593badda06c8.png">


