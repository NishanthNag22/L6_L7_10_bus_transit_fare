# Lab 7: Reproduce input validation failures

Nishanth Nag M V | PES1UG24AM381

The original processor.py is retained in this commit. Completed Hypothesis properties reveal three failing no-crash tests. Raw original outputs and terminal-style images are in evidence/.

```sh
python -m pip install -r requirements.txt
python -m pytest test_processor.py -q --tb=no -k "no_crash or safe"
```

Expected result: 3 failed, 71 deselected. This is the pre-fix stage; the next commit hardens the application and adds passing evidence.
