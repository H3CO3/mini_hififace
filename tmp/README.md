Just a folder for debug. Will be delete later
```bash
cd models
wget http://cs.stanford.edu/people/jcjohns/fast-neural-style/models/vgg16.t7
cd ..
```
If run with `cuda`: `python main.py train --epochs 2 --style-folder images/mystyles --cuda 1`
on `utils.pt` line `131`
```bash
style = style.cuda()  # 保留这一行
```

If run without `cuda`: `python main.py train --epochs 2 --style-folder images/mystyles --cuda 0`
on `utils.pt` line `131`
```bash
# style = style.cuda()  注释掉这一行
```
