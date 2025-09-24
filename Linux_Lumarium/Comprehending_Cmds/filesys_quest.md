# Challenge name
An epic filesytem quest

## My solve
**Flag:** `pwn.college{Eyy8tjz9jmQ71zkGXfmxxovxRqT.QX5IDO0wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  MEMO        boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:/$ cat flag
cat: flag: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat MEMO
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/scripts/kconfig/tests/new_choice_with_dep

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/scripts/kconfig/tests/new_choice_with_dep$ ls -a /opt/linux/linux-5.4/scripts/kconfig/tests/new_choice_with_dep

.  ..  .ALERT  Kconfig  __init__.py  config  expected_stdout
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/scripts/kconfig/tests/new_choice_with_dep$ cat .ALERT
Lucky listing!
The next clue is in: /usr/lib/python3.8/test/support/__pycache__

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/scripts/kconfig/tests/new_choice_with_dep$ cd /usr/lib/python3.8/test/support/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.8/test/support/__pycache__$ ls -a
.  ..  DOSSIER  __init__.cpython-38.pyc  script_helper.cpython-38.pyc  testresult.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.8/test/support/__pycache__$ cat DOSSIER
Great sleuthing!
The next clue is in: /usr/share/doc/php-cgi

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.8/test/support/__pycache__$ cd /usr/share/doc/php-cgi
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/php-cgi$ ls -a
.  ..  .CLUE  changelog.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/php-cgi$ cat .CLUE
Yahaha, you found me!
The next clue is in: /usr/share/nvim/runtime/tutor/en

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/php-cgi$ cd /usr/share/nvim/runtime/tutor/en
hacker@commands~an-epic-filesystem-quest:/usr/share/nvim/runtime/tutor/en$ ls -a
.  ..  .REVELATION  vim-01-beginner.tutor  vim-01-beginner.tutor.json
hacker@commands~an-epic-filesystem-quest:/usr/share/nvim/runtime/tutor/en$ cat .REVELATION
Great sleuthing!
The next clue is in: /usr/lib/python3/dist-packages/sage/schemes/cyclic_covers
hacker@commands~an-epic-filesystem-quest:/usr/share/nvim/runtime/tutor/en$ cd /usr/lib/python3/dist-packages/sage/schemes/cyclic_covers
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/schemes/cyclic_covers$ ls
MESSAGE  __init__.py  __pycache__  all.py  charpoly_frobenius.py  constructor.py  cycliccover_finite_field.py  cycliccover_generic.py
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/schemes/cyclic_covers$ cat MESSAGE
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/rpy2/interactive/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/schemes/cyclic_covers$ cd /usr/lib/python3/dist-packages/rpy2/interactive/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/rpy2/interactive/__pycache__$ ls
DISPATCH  __init__.cpython-38.pyc  packages.cpython-38.pyc  process_revents.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/rpy2/interactive/__pycache__$ cat DISPATCH
Yahaha, you found me!
The next clue is in: /usr/lib/python3/dist-packages/sympy/series/tests/__pycache__

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/rpy2/interactive/__pycache__$ cat /usr/lib/python3/dist-packages/sympy/series/tests/__pycache__
cat: /usr/lib/python3/dist-packages/sympy/series/tests/__pycache__: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/rpy2/interactive/__pycache__$ grep pwn.college /usr/lib/python3/dist-packages/sympy/series/tests/__pycache__
grep: /usr/lib/python3/dist-packages/sympy/series/tests/__pycache__: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/rpy2/interactive/__pycache__$ ls /usr/lib/python3/dist-packages/sympy/series/tests/__pycache__
LEAD-TRAPPED                      test_demidovich.cpython-38.pyc  test_kauers.cpython-38.pyc    test_nseries.cpython-38.pyc    test_series.cpython-38.pyc
__init__.cpython-38.pyc           test_formal.cpython-38.pyc      test_limits.cpython-38.pyc    test_order.cpython-38.pyc
test_approximants.cpython-38.pyc  test_fourier.cpython-38.pyc     test_limitseq.cpython-38.pyc  test_residues.cpython-38.pyc
test_aseries.cpython-38.pyc       test_gruntz.cpython-38.pyc      test_lseries.cpython-38.pyc   test_sequences.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/rpy2/interactive/__pycache__$ cat /usr/lib/python3/dist-packages/sympy/series/tests/__pycache__/LEAD-TRAPPED
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/numpy/f2py/tests/src/quoted_character

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/rpy2/interactive/__pycache__$ cd /usr/local/lib/python3.8/dist-packages/numpy/f2py/tests/src/quoted_character
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/f2py/tests/src/quoted_character$ ls
INFO  foo.f
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/numpy/f2py/tests/src/quoted_character$ cat INFO
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{Eyy8tjz9jmQ71zkGXfmxxovxRqT.QX5IDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
This was an extremely long process, here you will see that in the instance where we had to extract a clue which was "trapped" under a directory without cd'ing into it, I had attempted to cat and grep the directory without realising that the file was required first. Eventually figuring out that we had to ls into the aforementioned directory to actually find the file we need and then access the file via cat and its absolute path.

## What I learned
I do not mean to get philosophical here but this was moreso a test of perseverance and a culmination of the previous challenges, allowing multiple permutations by which we could've solved the problem. I realised soon after finishing this that I has uncessessarily cd'ed in a few instances into many directories which I didn't really have to and could've catted directly after ls'ing the necessary file. It was gritty and arduous but overall a joy to navigate through. This required knowledge of absolute paths, catting, ls and it's options/flags as well as cd, all essentials in the command shell. 

## References
None to note here.