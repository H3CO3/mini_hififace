Just a folder for debug. Will be delete later
```bash
cd models
wget https://drive.google.com/file/d/11chrsuc8QRYFwtwh1CFtlgE5nRQ0Jwpw/view?usp=sharing
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
