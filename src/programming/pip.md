# pip

always use `python3 -m pip` instead of `pip`

- make sure using the same pip as python
- use `python -m pip` on Windows

upgrade pip3

```
python3 -m pip install --upgrade pip
```

update all

```
python3 -m pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U
```

check version

```
python3 -m pip -V
```
