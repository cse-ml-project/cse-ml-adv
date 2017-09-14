# CSE ML Advanced topic

## Pydata - NumPy, Pandas
관련 내용 : https://github.com/cse-ml-project/pydata-book  
Pydata PDF e-book  

### Pandas  
http://pandas.pydata.org/ 
pandas is an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.
pandas is a NUMFocus sponsored project. This will help ensure the success of development of pandas as a world-class open-source project, and makes it possible to donate to the project.  

Notebook을 이용해 실습 진행  

## Scikit-Learn
Scikit-Learn 프로젝트 : http://scikit-learn.org/  

- Simple and efficient tools for data mining and data analysis
- Accessible to everybody, and reusable in various contexts
- Built on NumPy, SciPy, and matplotlib
- Open source, commercially usable - BSD license
  
Notebook을 이용해 실습 진행  

## Tensorflow - Linux 환경 구성
TensorFlow™ is an open source software library for numerical computation using data flow graphs. Nodes in the graph represent mathematical operations, while the graph edges represent the multidimensional data arrays (tensors) communicated between them. The flexible architecture allows you to deploy computation to one or more CPUs or GPUs in a desktop, server, or mobile device with a single API. TensorFlow was originally developed by researchers and engineers working on the Google Brain Team within Google's Machine Intelligence research organization for the purposes of conducting machine learning and deep neural networks research, but the system is general enough to be applicable in a wide variety of other domains as well.  
https://www.tensorflow.org/  

### linux VM 설치
password 방식으로 설정  

### xrdp 설치
https://docs.microsoft.com/ko-kr/azure/virtual-machines/linux/use-remote-desktop  

### xfce4 설치
```
sudo apt-get update  

sudo apt-get install xfce4  

sudo apt-get install xrdp  

echo xfce4-session >~/.xsession  

sudo service xrdp restart  
```

Tab Key not working when using Xfce desktop  
https://www.starnet.com/xwin32kb/tab-key-not-working-when-using-xfce-desktop/  

### Visual Studio code 설치
https://code.visualstudio.com/Download  

ubuntu visual studio code not work - xrdp  
https://stackoverflow.com/questions/36694941/visual-studio-code-1-fails-to-launch-on-ubuntu-using-xrdp  

sudo sed -i 's/BIG-REQUESTS/_IG-REQUESTS/' /usr/lib/x86_64-linux-gnu/libxcb.so.1  

### tf 설치
설치 링크  
https://www.tensorflow.org/install/  

1. docker - 격리된 환경에서 수행
```
sudo apt-get install docker  
docker run -it gcr.io/tensorflow/tensorflow bash  
```

2. native pip
```
sudo apt-get install python3-pip python3-dev  
pip3 install tensorflow  
```

3. validation 수행
```
import tensorflow as tf  
hello = tf.constant('Hello, TensorFlow!')  
sess = tf.Session()  
print(sess.run(hello))  
```

```
import tensorflow as tf
tf __version__
```

```
# Create a constant op 
# This op is added as a node to the default graph 
hello = tf.constant("Hello, TensorFlow!") 

# start a TF session 
sess = tf.Session() 

# run the op and get result 
print(sess.run(hello))
```

```
node1 = tf.constant(3.0, tf.float32) 
node2 = tf.constant(4.0)  # also tf.float32 implicitly 
node3 = tf.add(node1, node2)

print("node1:", node1, "node2:", node2) 
print("node3: ", node3)
```

4. MNIST 처리
tf-mnist-softmax.py  
tf-mnist-cnn.py  

참조