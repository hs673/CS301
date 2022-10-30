Install Dependencies:
 !pip install patchify
 !pip install keras
 !pip install keras-unet
 !pip install kaggle
 !pip install gitpython
 
NNI Installation Instructions:
How to Open NNI’s Web UI on Google Colab
1. Install required packages and softwares.
! pip install nni # install nni
! wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip # download ngrok and unzip it
! unzip ngrok-stable-linux-amd64.zip
! mkdir -p nni_repo
! git clone https://github.com/microsoft/nni.git nni_repo/nni # clone NNI's offical repo to get examples

2. Register a ngrok account here, then connect to your account using your authtoken.
! ./ngrok authtoken YOUR_AUTH_TOKEN

3. Start an NNI example on a port bigger than 1024, then start ngrok with the same port. If you want to use gpu, make sure gpuNum >= 1 in config.yml. Use get_ipython() to start ngrok since it will be stuck if you use ! ngrok http 8746 &.
! nnictl create --config nni_repo/nni/examples/trials/mnist-pytorch/config.yml --port 4746 &
get_ipython().system_raw('./ngrok http 8746 &')

4. Check the public url.
! curl -s http://localhost:4040/api/tunnels # don't change the port number 4040
You will see an url like http://xxxx.ngrok.io after step 4, open this url and you will find NNI’s Web UI. Have fun :)


![NNI](NNI.png?raw=true "NNI")
