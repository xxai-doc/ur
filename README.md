<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

یہ تجویز کیا جاتا ہے کہ پہلے nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) انسٹال کریں اور پھر ڈائرکٹری میں داخل ہونے کے بعد `direnv allow` (ڈائریکٹری میں داخل ہونے کے بعد [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) خود بخود عمل میں آجائے گا)۔

معنی یہ ہے: چینی ترجمہ جاپانی، کورین، انگریزی، دوسری تمام زبانوں میں انگریزی ترجمہ۔ اگر آپ صرف چینی اور انگریزی کو سپورٹ کرنا چاہتے ہیں تو آپ صرف `zh: en` لکھ سکتے ہیں۔

## سامنے کا کوڈ

* [سامنے کا کوڈ](https://github.com/xxai-art/web)
* [مجموعی طور پر سائٹ کے لیے زبان کے پیک](https://github.com/xxai-art/web/tree/main/i18n)
* [لاگ ان ماڈیولز کے لیے زبان کے پیک](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [ویب سائٹ کثیر لسانی دستاویزات](https://github.com/xxai-doc)

فرنٹ اینڈ پروگرامنگ لینگویج [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) ہے، جو کافی اسکرپٹ نحو کی بنیاد پر کچھ خصوصیات شامل کرتی ہے، دیکھیں [./coffee_plus.md](./coffee_plus.md) ۔

## ویب سائٹس اور دستاویزات کی بین الاقوامی کاری

مندرجہ ذیل 3 منصوبوں پر تعمیر کریں۔

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  لاحقہ `.mdt` ہے، آپ بیرونی فائلوں کا حوالہ دینے کے لیے `<+ ./coffee_plus/import.js>` سے ملتا جلتا نحو استعمال کر سکتے ہیں، اور لاحقہ کے ساتھ مارک ڈاؤن تیار کر سکتے ہیں `.md` ۔

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  مارک ڈاؤن ترجمہ کوڈز اور لنکس کا ترجمہ نہیں کرے گا، اور ترجمہ شدہ جملوں کو کیش کرے گا۔ اگر ترجمے میں ترمیم کی گئی ہے لیکن اصل متن میں ترمیم نہیں کی گئی ہے تو اسے دوبارہ کرنے سے ترجمے کی ترمیم کو اوور رائٹ نہیں کیا جائے گا۔

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` سے تیار کردہ ویب سائٹس کا ترجمہ کرنے کے لیے زبان کی فائلیں۔

### دستاویز کا ترجمہ آٹومیشن ہدایات

کوڈ ریپوزٹری [xxai-art/doc](https://github.com/xxai-art/doc) دیکھیں

یہ تجویز کیا جاتا ہے کہ پہلے nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) انسٹال کریں اور پھر ڈائرکٹری میں داخل ہونے کے بعد `direnv allow` (ڈائریکٹری میں داخل ہونے کے بعد [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) خود بخود عمل میں آجائے گا)۔

سینکڑوں زبانوں میں ترجمہ کیے جانے والے بڑے کوڈ بیس سے بچنے کے لیے، میں نے ہر زبان کے لیے علیحدہ کوڈ بیس بنایا اور کوڈ بیس کو ذخیرہ کرنے کے لیے ایک تنظیم بنائی۔

ماحولیاتی متغیر `GITHUB_ACCESS_TOKEN` سیٹ کرنے اور پھر [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) چلانے سے خود بخود کوڈ ریپوزٹری بن جائے گی۔

یقینا، آپ اسے کوڈ بیس میں بھی رکھ سکتے ہیں۔

ترجمہ اسکرپٹ حوالہ [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

اسکرپٹ کوڈ کی تشریح اس طرح کی جاتی ہے:

[bunx](https://bun.sh/docs/cli/bunx) npx کا متبادل ہے، جو تیز تر ہے۔ یقیناً، اگر آپ نے بن انسٹال نہیں کیا ہے، تو آپ اس کے بجائے `npx` استعمال کر سکتے ہیں۔

`bunx mdt zh` `.mdt` کو zh ڈائرکٹری میں `.md` کے طور پر پیش کرتا ہے، ذیل میں 2 منسلک فائلیں دیکھیں

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ترجمے کے لیے بنیادی کوڈ ہے (اگر آپ کے پاس صرف `nodejs` انسٹال ہیں، لیکن `bun` اور `direnv` انسٹال نہیں ہیں، تو آپ ترجمہ کرنے کے لیے `npx i18n` بھی چلا سکتے ہیں)۔

یہ [i18n.yml کو](https://github.com/xxai-art/doc/blob/main/i18n.yml) پارس کرے گا، اس دستاویز میں `i18n.yml` کی ترتیب حسب ذیل ہے:

```
en:
zh: ja ko en
```

معنی یہ ہے: چینی ترجمہ جاپانی، کورین، انگریزی، دوسری تمام زبانوں میں انگریزی ترجمہ۔ اگر آپ صرف چینی اور انگریزی کو سپورٹ کرنا چاہتے ہیں تو آپ صرف `zh: en` لکھ سکتے ہیں۔

آخری [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) ہے، جو مرکزی عنوان اور ہر زبان کے `README.md` کے پہلے سب ٹائٹل کے درمیان مواد کو نکالتا ہے تاکہ ایک اندراج `README.md` تیار کیا جا سکے۔ کوڈ بہت آسان ہے، آپ اسے خود دیکھ سکتے ہیں۔

گوگل API مفت ترجمہ کے لیے استعمال کیا جاتا ہے۔ اگر آپ Google تک رسائی حاصل نہیں کر سکتے ہیں، تو براہ کرم ایک پراکسی ترتیب دیں اور سیٹ کریں، جیسے:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

ترجمہ اسکرپٹ `.i18n` ڈائریکٹری میں ترجمہ شدہ کیش تیار کرے گا، براہ کرم اسے `git status` کے ساتھ چیک کریں اور بار بار ترجمے سے بچنے کے لیے اسے کوڈ ریپوزٹری میں شامل کریں۔

براہ کرم جب بھی کیشے کو اپ ڈیٹ کرنے کے لیے ترجمہ میں ترمیم کریں `bunx i18n` چلائیں۔

اگر اصل متن اور ترجمہ میں ایک ہی وقت میں ترمیم کی جاتی ہے تو، کیش الجھن میں پڑ جائے گا، لہذا اگر آپ ترمیم کرنا چاہتے ہیں، تو آپ صرف ایک میں ترمیم کرسکتے ہیں، اور پھر کیش کو اپ ڈیٹ کرنے کے لیے `bunx i18n` چلا سکتے ہیں۔
