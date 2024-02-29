# The error.

On my M1 Mac (32GB M1 MacBook Pro running Sonoma 14.3.1) I get this error when import dm-tree:

`ImportError: dlopen(/Users/joachim/Documents/python/tree/test-import-tree/venv/lib/python3.11/site-packages/dm_tree-0.1.8-py3.11-macosx-12-arm64.egg/tree/_tree.cpython-311-darwin.so, 0x0002): symbol not found in flat namespace '__ZN4absl12lts_2021032416strings_internal9CatPiecesESt16initializer_listINS0_11string_viewEE` 

Notably, if I build from source, this error goes away!


# How to reproduce.

1. Build a venv: `python3 -m venv ./venv`
2. Activate venv: `source venv/bin/active`
3. Install: `python setup.py install`
4. Try to import `tree` by running: `python test.py`

This will reproduce the above error. 
