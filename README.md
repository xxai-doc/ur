<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

ویب سائٹ کوڈ کا ایک حصہ اوپن سورس ہے، ترجمہ کو بہتر بنانے میں مدد کے لیے خوش آمدید۔

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
