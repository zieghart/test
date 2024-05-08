docker's environment:
docker pull zieghart/base:C10U16_perfect
then:
conda activate ncsn

train:


test size and gap:
python A_1k_arg_PCsampling_demo.py  --size=500  --gpu=0 --gap=60 --useNet=True

test sensor number:
python A_1k_arg_PCsampling_demo.py  --size=500  --gpu=0 --gap=60 --ssn=2 --useNet=True
python A_1k_arg_PCsampling_demo.py  --size=500  --gpu=0 --gap=60 --ssn=3 --useNet=True

test sparse:
python -u A_1k_arg_PCsampling_demo.py  --size=500  --gpu=1 --gap=60 --sparse=6 --useNet=True   # means SR = 5/6
python -u A_1k_arg_PCsampling_demo.py  --size=500  --gpu=1 --gap=60 --sparse=5 --useNet=True   # means SR = 4/5

background_test:
nohup python -u A_1k_arg_PCsampling_demo.py  --size=500  --gpu=0 --gap=60 > ./records/your_path/S500_G60.out 2>&1 &

if have any questions：
zhangliuwork@163.com

