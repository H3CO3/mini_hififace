Just a folder for debug. Will be delete later.
```bash
mkdir models
cd models
# That should run but something unexpected happend 
# wget http://cs.stanford.edu/people/jcjohns/fast-neural-style/models/vgg16.t7
gdown https://drive.google.com/u/0/uc?id=11chrsuc8QRYFwtwh1CFtlgE5nRQ0Jwpw
cd ..
```
### If run with `cuda` 
```bash 
python main.py train --epochs 2 --style-folder images/mystyles --cuda 1
```
on `utils.pt` line `131`
```bash
style = style.cuda()  # 保留这一行
```

### If run without `cuda`
```bash
python main.py train --epochs 2 --style-folder images/mystyles --cuda 0
```
on `utils.pt` line `131`
```bash
# style = style.cuda()  注释掉这一行
```
