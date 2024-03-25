Test diary
==========



# Coverage

## Wikipedia and Matt 4.

### Commands

Words (76998):

```
cat misc/yrkwiki.list misc/Matt_4.txt  |grep -v "[a-zA-Z]"|\
hfst-tokenise tools/tokenisers/tokeniser-disamb-gt-desc.pmhfst |\
grep "[а-я]"|grep -v '"."'|wc -l
```

Unknown:

```
cat misc/yrkwiki.list misc/Matt_4.txt  |grep -v "[a-zA-Z]" |\
hfst-tokenise -cg tools/tokenisers/tokeniser-disamb-gt-desc.pmhfst |\
grep "[а-я]"|grep -v '"."'|huyrk|grep " ?"|wc -l
```

### Test results

- 240324: 1-(64356/199655) = 0.6777



