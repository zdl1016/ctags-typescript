# ctags-typescript
 Adds TypeScript support to ctags

just run cmd in your project's root directory:

 ctags --langdef=MYTS --langmap=MYTS:.ts \
--regex-MYTS="/^\s*(protected|private|public)?\s*(\w+)\s*:.*;.*$/\2/m,member/" \
--regex-MYTS="/^\s*(protected|private|public)?\s*(\\$\w+)\s*:.*;.*$/\2/m,member/" \
--regex-MYTS="/^\s*interface\s+(\w+).*$/\1/interface,interface/" \
--regex-MYTS="/^\s*class\s+(\w+).*$/\1/c,class/" --regex-MYTS="/^\s*export\s*class\s+(\w+).*$/\1/c,class/" \
--regex-MYTS="/^\s*module\s+.*\.(\w+).*$/\1/m,module/" --regex-MYTS="/^\s*private\s+(\w+)\(.*$/\1/f,function/"  \
--regex-MYTS="/^\s*function\s+(\w+)\(.*$/\1/f,function/" --regex-MYTS="/^\s*(protected|private|public)?\s+(\w+)\(.*$/\2/f,function/"  \
--languages=MYTS --excmd=number -R ./
