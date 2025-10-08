# cts-ticket

## 1. frontend test

```powershell
yarn
yarn dev
```

## 2. frontend build

```powershell
yarn build
```

## 3. frontend deploy

deploy by backend

## 4. backend build

```shell
bash build.sh
```

## 5.backend deploy

### 5.1 create env
```bash
conda env create -f environment.yaml

# if conda create failed
conda create -n cts-ticket python=3.10
conda activate cts-ticket
pip install -r requirements.txt
```

### 5.2 run app

```bash
cd project_dir

# change config_pro.yaml items to real value
vim conf/config_pro.yaml
source bin/init_project_env.sh
bash bin/service.sh start
```

### 5.3 stop app

```bash
bash bin/service.sh stop
```

## 6. structure

```
cts-ticket/
│
├── backend/
│   │
│   ├── bin/
│   │
│   ├── conf/
│   │
│   ├── libs/               # common pak  
│   │
│   ├── log/
│   │
│   ├── scripts/ 
│   │
│   ├── src/python          # backend source code
│   │
│   └── src/template/dist   # frontend pak
│
├── frontend/               # frontend source code
│
└── README.md
```


## 7. others

restful pages: http://localhost:port/docs
