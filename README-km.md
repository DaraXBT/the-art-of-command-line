🌍
*[Čeština](README-cs.md) ∙ [Deutsch](README-de.md) ∙ [Ελληνικά](README-el.md) ∙ [English](README.md) ∙ [Español](README-es.md) ∙ [Français](README-fr.md) ∙ [Indonesia](README-id.md) ∙ [Italiano](README-it.md) ∙ [日本語](README-ja.md) ∙ [ភាសាខ្មែរ](README-km.md) ∙ [한국어](README-ko.md) ∙ [polski](README-pl.md) ∙ [Português](README-pt.md) ∙ [Română](README-ro.md) ∙ [Русский](README-ru.md) ∙ [Slovenščina](README-sl.md) ∙ [Українська](README-uk.md) ∙ [简体中文](README-zh.md) ∙ [繁體中文](README-zh-Hant.md)*


# សិល្បៈនៃការប្រើប្រាស់ Command Line

![curl -s 'https://raw.githubusercontent.com/jlevy/the-art-of-command-line/master/README.md' | egrep -o '`\\w+`' | tr -d '`' | cowsay -W50](cowsay.png)

- [មេតា](#មេតា-meta)
- [មូលដ្ឋានគ្រឹះ](#មូលដ្ឋានគ្រឹះ-basics)
- [ការប្រើប្រាស់ប្រចាំថ្ងៃ](#ការប្រើប្រាស់ប្រចាំថ្ងៃ-everyday-use)
- [ការចាត់ចែងឯកសារ និងទិន្នន័យ](#ការចាត់ចែងឯកសារ-និងទិន្នន័យ-processing-files-and-data)
- [ការដោះស្រាយបញ្ហាប្រព័ន្ធ](#ការដោះស្រាយបញ្ហាប្រព័ន្ធ-system-debugging)
- [ពាក្យបញ្ជាមួយជួរ](#ពាក្យបញ្ជាមួយជួរ-one-liners)
- [មិនសូវស្គាល់តែមានប្រយោជន៍](#មិនសូវស្គាល់តែមានប្រយោជន៍-obscure-but-useful)
- [សម្រាប់តែ macOS](#សម្រាប់តែ-macos-macos-only)
- [សម្រាប់តែ Windows](#សម្រាប់តែ-windows-windows-only)
- [ធនធានបន្ថែម](#ធនធានបន្ថែម-more-resources)
- [ការបដិសេធទទួលខុសត្រូវ](#ការបដិសេធទទួលខុសត្រូវ-disclaimer)

ភាពស្ទាត់ជំនាញលើ command line គឺជាជំនាញដែលជារឿយៗត្រូវបានគេមើលរំលង ឬចាត់ទុកថាជា រឿងអាថ៌កំបាំង ប៉ុន្តែវាពិតជាជួយបង្កើនភាពបត់បែន និងផលិតភាពរបស់អ្នកក្នុងនាមជាវិស្វករ ទាំងក្នុងរូបភាពជាក់ស្តែង និងលាក់កំបាំង។ នេះគឺជាបណ្តុំនៃកំណត់ត្រា និងគន្លឹះស្តីពីការប្រើប្រាស់ command-line ដែលយើងយល់ថាមានប្រយោជន៍នៅពេលធ្វើការលើ Linux។ គន្លឹះខ្លះគឺជាមូលដ្ឋាន ហើយខ្លះទៀតគឺជាក់លាក់ ស៊ីជម្រៅ ឬមិនសូវមានគេដឹង។ ទំព័រនេះមិនវែងទេ ប៉ុន្តែប្រសិនបើអ្នកអាចប្រើ និងចងចាំចំណុចទាំងអស់នៅទីនេះបាន នោះអ្នកចេះច្រើនហើយ។

ការងារនេះគឺជាលទ្ធផលនៃ [អ្នកនិពន្ធ និងអ្នកបកប្រែជាច្រើន](AUTHORS.md)។
ខ្លឹមសារខ្លះ
[ដើមឡើយ](http://www.quora.com/What-are-some-lesser-known-but-useful-Unix-commands)
[បានលេចឡើង](http://www.quora.com/What-are-the-most-useful-Swiss-army-knife-one-liners-on-Unix)
នៅលើ [Quora](http://www.quora.com/What-are-some-time-saving-tips-that-every-Linux-user-should-know),
ប៉ុន្តែក្រោយមកត្រូវបានផ្លាស់ប្តូរមក GitHub ដែលមានមនុស្សដែលមានទេពកោសល្យជាងអ្នកនិពន្ធដើម បានធ្វើការកែលម្អជាច្រើន។
**[សូមដាក់សំណួរ](https://airtable.com/shrzMhx00YiIVAWJg)** ប្រសិនបើអ្នកមានចម្ងល់ទាក់ទងនឹង command line។ **[សូមចូលរួមចំណែក](/CONTRIBUTING.md)** ប្រសិនបើអ្នកឃើញកំហុស ឬអ្វីមួយដែលអាចកែឱ្យប្រសើរជាងនេះ!

## មេតា (Meta)

វិសាលភាព៖

* ការណែនាំនេះគឺសម្រាប់ទាំងអ្នកចាប់ផ្តើមដំបូង និងអ្នកដែលមានបទពិសោធន៍។ គោលដៅគឺ *ភាពទូលំទូលាយ* (អ្វីៗដែលសំខាន់), *ភាពជាក់លាក់* (ផ្តល់ឧទាហរណ៍ជាក់ស្តែងនៃករណីប្រើប្រាស់ញឹកញាប់បំផុត), និង *ភាពខ្លី* (ជៀសវាងអ្វីដែលមិនចាំបាច់ ឬការពន្យល់វែងឆ្ងាយដែលអាចរកមើលបាននៅកន្លែងផ្សេង)។ គន្លឹះនីមួយៗគឺចាំបាច់នៅក្នុងស្ថានភាពណាមួយ ឬជួយសន្សំសំចៃពេលវេលាយ៉ាងច្រើនបើធៀបនឹងជម្រើសផ្សេងទៀត។
* ឯកសារនេះសរសេរសម្រាប់ Linux ដោយលើកលែងតែផ្នែក "[សម្រាប់តែ macOS](#សម្រាប់តែ-macos-macos-only)" និង "[សម្រាប់តែ Windows](#សម្រាប់តែ-windows-windows-only)"។ ចំណុចជាច្រើនទៀតក៏អាចអនុវត្ត ឬដំឡើងបាននៅលើ Unix ផ្សេងទៀត ឬ macOS (ឬសូម្បីតែ Cygwin)។
* ការផ្តោតសំខាន់គឺលើ Bash បែបអន្តរកម្ម (Interactive Bash) ទោះបីជាគន្លឹះជាច្រើនអនុវត្តចំពោះ Shell ផ្សេងទៀត និងការសរសេរ Script Bash ទូទៅក៏ដោយ។
* វារួមបញ្ចូលទាំងពាក្យបញ្ជា Unix "ស្តង់ដារ" ក៏ដូចជាពាក្យបញ្ជាដែលត្រូវការការដំឡើងកញ្ចប់ (package) ពិសេស -- ដរាបណាវាមានសារៈសំខាន់គ្រប់គ្រាន់ក្នុងការដាក់បញ្ចូល។

កំណត់សម្គាល់៖

* ដើម្បីរក្សាឯកសារនេះឱ្យនៅត្រឹមមួយទំព័រ ខ្លឹមសារត្រូវបានបញ្ចូលដោយប្រយោលតាមរយៈការយោង។ អ្នកឆ្លាតគ្រប់គ្រាន់ក្នុងការស្វែងរកព័ត៌មានលម្អិតបន្ថែមនៅកន្លែងផ្សេង នៅពេលដែលអ្នកដឹងពីគំនិត ឬពាក្យបញ្ជាដើម្បីស្វែងរកក្នុង Google។ ប្រើ `apt`, `yum`, `dnf`, `pacman`, `pip` ឬ `brew` (តាមការសមស្រប) ដើម្បីដំឡើងកម្មវិធីថ្មី។
* ប្រើ [Explainshell](http://explainshell.com/) ដើម្បីទទួលបានការបំបែកដ៏មានប្រយោជន៍នៃអ្វីដែលពាក្យបញ្ជា, ជម្រើស (options), pipes ។ល។ ធ្វើការ។

## មូលដ្ឋានគ្រឹះ (Basics)

* រៀន Bash មូលដ្ឋាន។ តាមពិតទៅ វាយ `man bash` ហើយយ៉ាងហោចណាស់មើលត្រួសៗទាំងអស់; វាងាយស្រួលយល់ និងមិនវែងពេកទេ។ Shell ផ្សេងទៀតអាចនឹងល្អ ប៉ុន្តែ Bash មានអនុភាពខ្លាំង និងមាននៅគ្រប់ទីកន្លែង (ការរៀន *តែ* zsh, fish, ។ល។ ទោះបីជាគួរឱ្យទាក់ទាញនៅលើកុំព្យូទ័រផ្ទាល់ខ្លួនរបស់អ្នកក៏ដោយ វានឹងកម្រិតអ្នកនៅក្នុងស្ថានភាពជាច្រើន ដូចជានៅពេលប្រើម៉ាស៊ីនមេ (servers) ដែលមានស្រាប់)។
* រៀនកម្មវិធីកែសម្រួលអត្ថបទ (text-based editor) យ៉ាងហោចណាស់មួយឱ្យបានច្បាស់។ កម្មវិធី `nano` គឺជាកម្មវិធីមួយដែលសាមញ្ញបំផុតសម្រាប់ការកែសម្រួលជាមូលដ្ឋាន (បើក, កែសម្រួល, រក្សាទុក, ស្វែងរក)។ ទោះជាយ៉ាងណាក៏ដោយ សម្រាប់អ្នកប្រើប្រាស់កម្រិតខ្ពស់នៅក្នុង terminal គ្មានអ្វីជំនួស Vim (`vi`) បានទេ ដែលជា editor ពិបាករៀន ប៉ុន្តែមានល្បឿនលឿន និងមានមុខងារពេញលេញ។ មនុស្សជាច្រើនក៏ប្រើ Emacs បុរាណផងដែរ ជាពិសេសសម្រាប់កិច្ចការកែសម្រួលធំៗ។ (ជាការពិតណាស់ អ្នកអភិវឌ្ឍន៍កម្មវិធីសម័យទំនើបណាមួយដែលធ្វើការលើគម្រោងធំទូលាយ ទំនងជាមិនប្រើតែកម្មវិធីកែសម្រួលអត្ថបទសុទ្ធទេ ហើយគួរតែស៊ាំជាមួយ IDEs និងឧបករណ៍ក្រាហ្វិកទំនើបផងដែរ។)
* ការស្វែងរកឯកសារជំនួយ៖
* ចេះអានឯកសារផ្លូវការជាមួយ `man` (សម្រាប់អ្នកចង់ដឹង `man man` រាយបញ្ជីលេខផ្នែក ឧ. ១ គឺពាក្យបញ្ជា "ធម្មតា", ៥ គឺឯកសារ/អនុសញ្ញា, និង ៨ គឺសម្រាប់ការគ្រប់គ្រងប្រព័ន្ធ)។ ស្វែងរកទំព័រ man ជាមួយ `apropos`។
* ដឹងថាពាក្យបញ្ជាខ្លះមិនមែនជាកម្មវិធី (executables) ទេ ប៉ុន្តែជា Bash builtins ហើយអ្នកអាចទទួលបានជំនួយអំពីពួកវាជាមួយ `help` និង `help -d`។ អ្នកអាចដឹងថាពាក្យបញ្ជាមួយជា executable, shell builtin ឬជា alias ដោយប្រើ `type command`។
* `curl cheat.sh/command` នឹងផ្តល់ឱ្យនូវ "cheat sheet" សង្ខេបជាមួយឧទាហរណ៍ទូទៅនៃរបៀបប្រើប្រាស់ពាក្យបញ្ជា shell នោះ។


* រៀនអំពីការបញ្ជូនលទ្ធផល (redirection) នៃ output និង input ដោយប្រើ `>` និង `<` និង pipes ដោយប្រើ `|`។ ដឹងថា `>` សរសេរជាន់លើ (overwrite) ឯកសារ output ហើយ `>>` សរសេរបន្ថែម (append)។ រៀនអំពី stdout និង stderr។
* រៀនអំពី file glob expansion ជាមួយ `*` (និងប្រហែលជា `?` និង `[`...`]`) និងការប្រើសញ្ញាសម្រង់ (quoting) ព្រមទាំងភាពខុសគ្នារវាងសញ្ញាសម្រង់ពីរ `"` និងសញ្ញាសម្រង់មួយ `'`។ (សូមមើលបន្ថែមលើ variable expansion ខាងក្រោម។)
* ស្វែងយល់ជាមួយការគ្រប់គ្រង Bash job៖ `&`, **ctrl-z**, **ctrl-c**, `jobs`, `fg`, `bg`, `kill`, ។ល។
* ស្គាល់ `ssh`, និងមូលដ្ឋានគ្រឹះនៃការផ្ទៀងផ្ទាត់ដោយមិនប្រើពាក្យសម្ងាត់ (passwordless authentication) តាមរយៈ `ssh-agent`, `ssh-add`, ។ល។
* ការគ្រប់គ្រងឯកសារមូលដ្ឋាន៖ `ls` និង `ls -l` (ជាពិសេស រៀនថាគ្រប់ជួរឈរក្នុង `ls -l` មានន័យដូចម្តេច), `less`, `head`, `tail` និង `tail -f` (ឬប្រសើរជាងនេះ `less +F`), `ln` និង `ln -s` (រៀនពីភាពខុសគ្នា និងគុណសម្បត្តិនៃ hard links ធៀបនឹង soft links), `chown`, `chmod`, `du` (សម្រាប់ការសង្ខេបការប្រើប្រាស់ថាសរហ័ស៖ `du -hs *`)។ សម្រាប់ការគ្រប់គ្រង filesystem, `df`, `mount`, `fdisk`, `mkfs`, `lsblk`។ រៀនថាអ្វីជា inode (`ls -i` ឬ `df -i`)។
* ការគ្រប់គ្រងបណ្តាញមូលដ្ឋាន៖ `ip` ឬ `ifconfig`, `dig`, `traceroute`, `route`។
* រៀន និងប្រើប្រាស់ប្រព័ន្ធគ្រប់គ្រងកំណែ (version control management system) ដូចជា `git`។
* ស្គាល់ regular expressions ឱ្យបានច្បាស់ និង flags ផ្សេងៗចំពោះ `grep`/`egrep`។ ជម្រើស `-i`, `-o`, `-v`, `-A`, `-B`, និង `-C` គឺមានតម្លៃដែលគួរដឹង។
* រៀនប្រើ `apt-get`, `yum`, `dnf` ឬ `pacman` (អាស្រ័យលើ distro) ដើម្បីស្វែងរក និងដំឡើងកញ្ចប់កម្មវិធី។ ហើយត្រូវប្រាកដថាអ្នកមាន `pip` ដើម្បីដំឡើងឧបករណ៍ command-line ដែលបង្កើតដោយ Python (មួយចំនួនខាងក្រោមងាយស្រួលដំឡើងតាមរយៈ `pip`)។

## ការប្រើប្រាស់ប្រចាំថ្ងៃ (Everyday use)

* នៅក្នុង Bash, ប្រើ **Tab** ដើម្បីបំពេញអាគុយម៉ង់ (arguments) ឬរាយបញ្ជីពាក្យបញ្ជាដែលមានទាំងអស់ និង **ctrl-r** ដើម្បីស្វែងរកក្នុងប្រវត្តិពាក្យបញ្ជា (command history) (បន្ទាប់ពីចុច, វាយពាក្យដើម្បីស្វែងរក, ចុច **ctrl-r** ដដែលៗដើម្បីប្តូរទៅការផ្គូផ្គងផ្សេងទៀត, ចុច **Enter** ដើម្បីអនុវត្តពាក្យបញ្ជាដែលបានរកឃើញ, ឬចុចសញ្ញាព្រួញស្តាំដើម្បីដាក់លទ្ធផលទៅក្នុងបន្ទាត់បច្ចុប្បន្នដើម្បីកែសម្រួល)។
* នៅក្នុង Bash, ប្រើ **ctrl-w** ដើម្បីលុបពាក្យចុងក្រោយ, និង **ctrl-u** ដើម្បីលុបខ្លឹមសារពីទស្សន៍ទ្រនិច (cursor) បច្ចុប្បន្នទៅដើមបន្ទាត់។ ប្រើ **alt-b** និង **alt-f** ដើម្បីផ្លាស់ទីតាមពាក្យ, **ctrl-a** ដើម្បីផ្លាស់ទី cursor ទៅដើមបន្ទាត់, **ctrl-e** ដើម្បីផ្លាស់ទី cursor ទៅចុងបន្ទាត់, **ctrl-k** ដើម្បីលុប (kill) ទៅចុងបន្ទាត់, **ctrl-l** ដើម្បីសម្អាតអេក្រង់។ សូមមើល `man readline` សម្រាប់ keybindings ទាំងអស់ដែលមានស្រាប់ក្នុង Bash។ មានច្រើនណាស់។ ឧទាហរណ៍ **alt-.** វិលជុំតាមអាគុយម៉ង់មុនៗ, និង **alt-*** ពង្រីក glob។
* ជម្រើសមួយទៀត ប្រសិនបើអ្នកស្រលាញ់ key-bindings បែប vi, ប្រើ `set -o vi` (និង `set -o emacs` ដើម្បីដាក់វាមកវិញ)។
* សម្រាប់ការកែសម្រួលពាក្យបញ្ជាវែងៗ, បន្ទាប់ពីកំណត់ editor របស់អ្នក (ឧទាហរណ៍ `export EDITOR=vim`), **ctrl-x** **ctrl-e** នឹងបើកពាក្យបញ្ជាបច្ចុប្បន្ននៅក្នុង editor សម្រាប់ការកែសម្រួលច្រើនបន្ទាត់។ ឬក្នុងរចនាប័ទ្ម vi, **escape-v**។
* ដើម្បីមើលពាក្យបញ្ជាថ្មីៗ, ប្រើ `history`។ បន្តដោយ `!n` (ដែល `n` ជាលេខពាក្យបញ្ជា) ដើម្បីអនុវត្តម្តងទៀត។ ក៏មានអក្សរកាត់ជាច្រើនដែលអ្នកអាចប្រើបាន ដែលមានប្រយោជន៍បំផុតគឺ `!$` សម្រាប់អាគុយម៉ង់ចុងក្រោយ និង `!!` សម្រាប់ពាក្យបញ្ជាចុងក្រោយ (សូមមើល "HISTORY EXPANSION" ក្នុង man page)។ ទោះជាយ៉ាងណាក៏ដោយ វាងាយស្រួលជំនួសដោយ **ctrl-r** និង **alt-.**។
* ទៅកាន់ home directory របស់អ្នកជាមួយ `cd`។ ចូលប្រើឯកសារដែលទាក់ទងនឹង home directory របស់អ្នកជាមួយបុព្វបទ `~` (ឧ. `~/.bashrc`)។ នៅក្នុង `sh` scripts សំដៅលើ home directory ជា `$HOME`។
* ដើម្បីត្រឡប់ទៅ working directory មុន៖ `cd -`។
* ប្រសិនបើអ្នកកំពុងវាយពាក្យបញ្ជាមួយបានពាក់កណ្តាល ប៉ុន្តែប្តូរចិត្ត, ចុច **alt-#** ដើម្បីបន្ថែម `#` នៅដើម ហើយបញ្ចូលវាជា comment (ឬប្រើ **ctrl-a**, **#**, **enter**)។ បន្ទាប់មកអ្នកអាចត្រឡប់ទៅរកវានៅពេលក្រោយតាមរយៈ command history។
* ប្រើ `xargs` (ឬ `parallel`)។ វាមានអនុភាពខ្លាំងណាស់។ ចំណាំថាអ្នកអាចគ្រប់គ្រងចំនួនធាតុដែលត្រូវប្រតិបត្តិក្នុងមួយបន្ទាត់ (`-L`) ក៏ដូចជាភាពស្របគ្នា (parallelism) (`-P`)។ ប្រសិនបើអ្នកមិនប្រាកដថាវានឹងធ្វើរឿងត្រឹមត្រូវទេ, ប្រើ `xargs echo` ជាមុនសិន។ ម្យ៉ាងទៀត, `-I{}` ក៏មានប្រយោជន៍ដែរ។ ឧទាហរណ៍៖

```bash
      find . -name '*.py' | xargs grep some_function
      cat hosts | xargs -I{} ssh root@{} hostname

```

* `pstree -p` គឺជាការបង្ហាញដ៏មានប្រយោជន៍នៃ process tree។
* ប្រើ `pgrep` និង `pkill` ដើម្បីស្វែងរក ឬផ្ញើសញ្ញា (signal) ទៅ processes តាមឈ្មោះ (`-f` គឺមានប្រយោជន៍)។
* ស្គាល់សញ្ញាផ្សេងៗដែលអ្នកអាចផ្ញើទៅ processes។ ឧទាហរណ៍ ដើម្បីផ្អាក process, ប្រើ `kill -STOP [pid]`។ សម្រាប់បញ្ជីពេញលេញ, សូមមើល `man 7 signal`។
* ប្រើ `nohup` ឬ `disown` ប្រសិនបើអ្នកចង់ឱ្យ background process ដំណើរការជារៀងរហូត។
* ពិនិត្យមើលថាតើ processes ណាខ្លះកំពុង listening តាមរយៈ `netstat -lntp` ឬ `ss -plat` (សម្រាប់ TCP; បន្ថែម `-u` សម្រាប់ UDP) ឬ `lsof -iTCP -sTCP:LISTEN -P -n` (ដែលដំណើរការផងដែរនៅលើ macOS)។
* សូមមើល `lsof` និង `fuser` សម្រាប់ open sockets និង files។
* សូមមើល `uptime` ឬ `w` ដើម្បីដឹងថាប្រព័ន្ធដំណើរការបានយូរប៉ុណ្ណាហើយ។
* ប្រើ `alias` ដើម្បីបង្កើតផ្លូវកាត់សម្រាប់ពាក្យបញ្ជាដែលប្រើញឹកញាប់។ ឧទាហរណ៍ `alias ll='ls -latr'` បង្កើត alias ថ្មី `ll`។
* រក្សាទុក aliases, ការកំណត់ shell, និង functions ដែលអ្នកប្រើញឹកញាប់នៅក្នុង `~/.bashrc`, និង [រៀបចំឱ្យ login shells ហៅយកវា (source)](http://superuser.com/a/183980/7106)។ នេះនឹងធ្វើឱ្យការរៀបចំរបស់អ្នកមាននៅក្នុងគ្រប់ shell sessions របស់អ្នក។
* ដាក់ការកំណត់ environment variables ក៏ដូចជាពាក្យបញ្ជាដែលគួរតែប្រតិបត្តិនៅពេលអ្នក login នៅក្នុង `~/.bash_profile`។ ការកំណត់រចនាសម្ព័ន្ធដាច់ដោយឡែកនឹងត្រូវការសម្រាប់ shells ដែលអ្នកបើកពី graphical environment logins និង `cron` jobs។
* ធ្វើសមកាលកម្ម (Synchronize) ឯកសារកំណត់រចនាសម្ព័ន្ធរបស់អ្នក (ឧ. `.bashrc` និង `.bash_profile`) រវាងកុំព្យូទ័រផ្សេងៗជាមួយ Git។
* យល់ថាការប្រុងប្រយ័ត្នគឺចាំបាច់នៅពេលដែល variables និងឈ្មោះឯកសារមានដកឃ្លា (whitespace)។ ដាក់ Bash variables របស់អ្នកក្នុងសញ្ញាសម្រង់, ឧ. `"$FOO"`។ ចូលចិត្តជម្រើស `-0` ឬ `-print0` ដើម្បីអនុញ្ញាតឱ្យ null characters កំណត់ព្រំដែនឈ្មោះឯកសារ, ឧ. `locate -0 pattern | xargs -0 ls -al` ឬ `find / -print0 -type d | xargs -0 ls -al`។ ដើម្បីរង្វិលជុំ (iterate) លើឈ្មោះឯកសារដែលមានដកឃ្លាក្នុង for loop, កំណត់ IFS របស់អ្នកឱ្យទៅជា newline តែប៉ុណ្ណោះដោយប្រើ `IFS=$'\n'`។
* នៅក្នុង Bash scripts, ប្រើ `set -x` (ឬវ៉ារ្យ៉ង់ `set -v`, ដែលកត់ត្រា raw input, រួមទាំង unexpanded variables និង comments) សម្រាប់ debugging output។ ប្រើ strict modes លើកលែងតែអ្នកមានហេតុផលល្អមិនប្រើ៖ ប្រើ `set -e` ដើម្បីបោះបង់ (abort) នៅពេលមានកំហុស (nonzero exit code)។ ប្រើ `set -u` ដើម្បីរកមើលការប្រើប្រាស់ variable ដែលមិនទាន់កំណត់។ ពិចារណា `set -o pipefail` ផងដែរ, ដើម្បី abort នៅពេលមានកំហុសនៅក្នុង pipes (ទោះបីជាគួរអានបន្ថែមលើវាប្រសិនបើអ្នកធ្វើដូច្នេះ, ព្រោះប្រធានបទនេះមានភាពល្អិតល្អន់បន្តិច)។ សម្រាប់ scripts ដែលស្មុគស្មាញ, ប្រើ `trap` លើ EXIT ឬ ERR ផងដែរ។ ទម្លាប់ដ៏មានប្រយោជន៍មួយគឺចាប់ផ្តើម script ដូចនេះ, ដែលនឹងធ្វើឱ្យវារកឃើញ និង abort លើកំហុសទូទៅ និងបោះពុម្ពសារ៖

```bash
      set -euo pipefail
      trap "echo 'error: Script failed: see failed command above'" ERR

```

* នៅក្នុង Bash scripts, subshells (សរសេរជាមួយវង់ក្រចក) គឺជាវិធីងាយស្រួលក្នុងការដាក់ក្រុមពាក្យបញ្ជា។ ឧទាហរណ៍ទូទៅគឺការផ្លាស់ទីបណ្តោះអាសន្នទៅកាន់ working directory ផ្សេង, ឧ.

```bash
      # ធ្វើអ្វីមួយក្នុង current dir
      (cd /some/other/dir && other-command)
      # បន្តក្នុង original dir

```

* នៅក្នុង Bash, ចំណាំថាមានប្រភេទ variable expansion ជាច្រើន។ ការពិនិត្យមើល variable ថាមានឬអត់៖ `${name:?error message}`។ ឧទាហរណ៍, ប្រសិនបើ Bash script ត្រូវការ single argument, គ្រាន់តែសរសេរ `input_file=${1:?usage: $0 input_file}`។ ការប្រើប្រាស់ default value ប្រសិនបើ variable ទទេ៖ `${name:-default}`។ ប្រសិនបើអ្នកចង់បន្ថែម parameter (ស្រេចចិត្ត) បន្ថែមទៅលើឧទាហរណ៍មុន, អ្នកអាចប្រើអ្វីមួយដូចជា `output_file=${2:-logfile}`។ ប្រសិនបើ `$2` ត្រូវបានលុបចោល ហើយដូច្នេះទទេ, `output_file` នឹងត្រូវបានកំណត់ទៅជា `logfile`។ Arithmetic expansion: `i=$(( (i + 1) % 5 ))`។ Sequences: `{1..10}`។ ការកាត់ខ្សែអក្សរ (Trimming of strings): `${var%suffix}` និង `${var#prefix}`។ ឧទាហរណ៍ ប្រសិនបើ `var=foo.pdf`, នោះ `echo ${var%.pdf}.txt` បោះពុម្ព `foo.txt`។
* Brace expansion ដោយប្រើ `{`...`}` អាចកាត់បន្ថយការវាយអត្ថបទស្រដៀងគ្នាឡើងវិញ និងធ្វើស្វ័យប្រវត្តិកម្មបន្សំនៃធាតុ។ នេះមានប្រយោជន៍ក្នុងឧទាហរណ៍ដូចជា `mv foo.{txt,pdf} some-dir` (ដែលផ្លាស់ទីឯកសារទាំងពីរ), `cp somefile{,.bak}` (ដែលពង្រីកទៅជា `cp somefile somefile.bak`) ឬ `mkdir -p test-{a,b,c}/subtest-{1,2,3}` (ដែលពង្រីកបន្សំដែលអាចធ្វើបានទាំងអស់ និងបង្កើត directory tree)។ Brace expansion ត្រូវបានអនុវត្តមុនការពង្រីកផ្សេងទៀតទាំងអស់។
* លំដាប់នៃការពង្រីកគឺ៖ brace expansion; tilde expansion, parameter និង variable expansion, arithmetic expansion, និង command substitution (ធ្វើតាមលក្ខណៈឆ្វេងទៅស្តាំ); word splitting; និង filename expansion។ (ឧទាហរណ៍, ជួរ (range) ដូចជា `{1..20}` មិនអាចត្រូវបានបង្ហាញជាមួយ variables ដោយប្រើ `{$a..$b}` បានទេ។ ប្រើ `seq` ឬ `for` loop ជំនួសវិញ, ឧ., `seq $a $b` ឬ `for((i=a; i<=b; i++)); do ... ; done`។)
* លទ្ធផល (output) នៃពាក្យបញ្ជាអាចត្រូវបានចាត់ទុកដូចជាឯកសារតាមរយៈ `<(some command)` (គេស្គាល់ថា process substitution)។ ឧទាហរណ៍, ប្រៀបធៀប local `/etc/hosts` ជាមួយ remote one៖

```sh
      diff /etc/hosts <(ssh somehost cat /etc/hosts)

```

* នៅពេលសរសេរ scripts អ្នកប្រហែលជាចង់ដាក់កូដរបស់អ្នកទាំងអស់នៅក្នុង curly braces។ ប្រសិនបើបាត់ closing brace, script របស់អ្នកនឹងត្រូវបានរារាំងមិនឱ្យប្រតិបត្តិដោយសារ syntax error។ នេះសមហេតុផលនៅពេល script របស់អ្នកនឹងត្រូវបានទាញយកពី web, ព្រោះវាការពារ scripts ដែលទាញយកបានតែពាក់កណ្តាលមិនឱ្យដំណើរការ៖

```bash
{
      # កូដរបស់អ្នកនៅទីនេះ
}

```

* "Here document" អនុញ្ញាតឱ្យ [បញ្ជូន input ច្រើនបន្ទាត់](https://www.tldp.org/LDP/abs/html/here-docs.html) ហាក់ដូចជាមកពីឯកសារ៖

```
cat <<EOF
input
on multiple lines
EOF

```

* នៅក្នុង Bash, បញ្ជូនទាំង standard output និង standard error តាមរយៈ៖ `some-command >logfile 2>&1` ឬ `some-command &>logfile`។ ជាញឹកញាប់, ដើម្បីធានាថាពាក្យបញ្ជាមិនបន្សល់ទុក open file handle ទៅ standard input, ដោយភ្ជាប់វាទៅ terminal ដែលអ្នកកំពុងនៅ, វាក៏ជាការអនុវត្តល្អដែរក្នុងការបន្ថែម `</dev/null`។
* ប្រើ `man ascii` សម្រាប់តារាង ASCII ដ៏ល្អ, ជាមួយតម្លៃ hex និង decimal។ សម្រាប់ព័ត៌មាន encoding ទូទៅ, `man unicode`, `man utf-8`, និង `man latin1` គឺមានប្រយោជន៍។
* ប្រើ `screen` ឬ [`tmux`](https://tmux.github.io/) ដើម្បី multiplex អេក្រង់, មានប្រយោជន៍ជាពិសេសលើ remote ssh sessions និងដើម្បី detach និង re-attach ទៅកាន់ session។ `byobu` អាចបង្កើន screen ឬ tmux ដោយផ្តល់ព័ត៌មានបន្ថែម និងការគ្រប់គ្រងងាយស្រួលជាង។ ជម្រើសតូចជាងសម្រាប់តែ session persistence គឺ [`dtach`](https://github.com/bogner/dtach)។
* ក្នុង ssh, ការដឹងពីរបៀប port tunnel ជាមួយ `-L` ឬ `-D` (និងជួនកាល `-R`) គឺមានប្រយោជន៍, ឧ. ដើម្បីចូលប្រើគេហទំព័រពី remote server។
* វាអាចមានប្រយោជន៍ក្នុងការធ្វើ optimizations មួយចំនួនចំពោះការកំណត់ ssh របស់អ្នក; ឧទាហរណ៍, `~/.ssh/config` នេះមានការកំណត់ដើម្បីជៀសវាង dropped connections នៅក្នុង network environments មួយចំនួន, ប្រើ compression (ដែលមានប្រយោជន៍ជាមួយ scp លើ low-bandwidth connections), និង multiplex channels ទៅ server ដូចគ្នាជាមួយ local control file៖

```
      TCPKeepAlive=yes
      ServerAliveInterval=15
      ServerAliveCountMax=6
      Compression=yes
      ControlMaster auto
      ControlPath /tmp/%r@%h:%p
      ControlPersist yes

```

* ជម្រើសមួយចំនួនផ្សេងទៀតដែលពាក់ព័ន្ធនឹង ssh គឺរសើបនឹងសុវត្ថិភាព និងគួរត្រូវបានបើកដោយប្រុងប្រយ័ត្ន, ឧ. per subnet ឬ host ឬនៅក្នុង trusted networks៖ `StrictHostKeyChecking=no`, `ForwardAgent=yes`
* ពិចារណា [`mosh`](https://mosh.org/) ជាជម្រើសជំនួស ssh ដែលប្រើ UDP, ជៀសវាង dropped connections និងបន្ថែមភាពងាយស្រួលនៅពេលធ្វើដំណើរ (ត្រូវការ server-side setup)។
* ដើម្បីទទួលបាន permissions លើឯកសារក្នុងទម្រង់ octal, ដែលមានប្រយោជន៍សម្រាប់ system configuration ប៉ុន្តែមិនមាននៅក្នុង `ls` និងងាយនឹងច្រឡំ, ប្រើអ្វីមួយដូចជា

```sh
      stat -c '%A %a %n' /etc/timezone

```

* សម្រាប់ការជ្រើសរើសតម្លៃបែបអន្តរកម្មពី output នៃពាក្យបញ្ជាផ្សេងទៀត, ប្រើ [`percol`](https://github.com/mooz/percol) ឬ [`fzf`](https://github.com/junegunn/fzf)។
* សម្រាប់អន្តរកម្មជាមួយឯកសារដោយផ្អែកលើ output នៃពាក្យបញ្ជាផ្សេងទៀត (ដូចជា `git`), ប្រើ `fpp` ([PathPicker](https://github.com/facebook/PathPicker))។
* សម្រាប់ web server សាមញ្ញសម្រាប់ឯកសារទាំងអស់នៅក្នុង current directory (និង subdirs), ដែលអាចចូលប្រើបានសម្រាប់នរណាម្នាក់នៅលើ network របស់អ្នក, ប្រើ៖
`python -m SimpleHTTPServer 7777` (សម្រាប់ port 7777 និង Python 2) និង `python -m http.server 7777` (សម្រាប់ port 7777 និង Python 3)។
* សម្រាប់ការដំណើរការពាក្យបញ្ជាជា user ផ្សេងទៀត, ប្រើ `sudo`។ តាមលំនាំដើមដំណើរការជា root; ប្រើ `-u` ដើម្បីបញ្ជាក់ user ផ្សេងទៀត។ ប្រើ `-i` ដើម្បី login ជា user នោះ (អ្នកនឹងត្រូវបានសួររកពាក្យសម្ងាត់ *របស់អ្នក*)។
* សម្រាប់ការប្តូរ shell ទៅ user ផ្សេងទៀត, ប្រើ `su username` ឬ `su - username`។ ក្រោយមកទៀតជាមួយ "-" ទទួលបាន environment ហាក់ដូចជា user ផ្សេងទៀតទើបតែ logged in។ ការមិនដាក់ username នឹងកំណត់ទៅ root។ អ្នកនឹងត្រូវបានសួររកពាក្យសម្ងាត់ *របស់ user ដែលអ្នកកំពុងប្តូរទៅ*។
* ដឹងអំពី [ដែនកំណត់ 128K](https://wiki.debian.org/CommonErrorMessages/ArgumentListTooLong) លើ command lines។ កំហុស "Argument list too long" នេះគឺកើតមានជាញឹកញាប់នៅពេល wildcard matching ឯកសារចំនួនច្រើន។ (នៅពេលរឿងនេះកើតឡើង ជម្រើសជំនួសដូចជា `find` និង `xargs` អាចជួយបាន។)
* សម្រាប់ម៉ាស៊ីនគិតលេខមូលដ្ឋាន (និងជាការពិតណាស់ការចូលប្រើ Python ជាទូទៅ), ប្រើ `python` interpreter។ ឧទាហរណ៍,

```
>>> 2+3
5

```

## ការចាត់ចែងឯកសារ និងទិន្នន័យ (Processing files and data)

* ដើម្បីកំណត់ទីតាំងឯកសារតាមឈ្មោះនៅក្នុង current directory, `find . -iname '*something*'` (ឬស្រដៀងគ្នា)។ ដើម្បីស្វែងរកឯកសារនៅកន្លែងណាមួយតាមឈ្មោះ, ប្រើ `locate something` (ប៉ុន្តែត្រូវចាំថា `updatedb` អាចនឹងមិនទាន់បាន indexed ឯកសារដែលទើបបង្កើតថ្មីៗទេ)។
* សម្រាប់ការស្វែងរកទូទៅតាមរយៈ source ឬ data files, មានជម្រើសជាច្រើនដែលកម្រិតខ្ពស់ ឬលឿនជាង `grep -r`, រួមមាន (តាមលំដាប់ពីចាស់ទៅថ្មី) [`ack`](https://github.com/beyondgrep/ack2), [`ag`](https://github.com/ggreer/the_silver_searcher) ("the silver searcher"), និង [`rg`](https://github.com/BurntSushi/ripgrep) (ripgrep)។
* ដើម្បីបំប្លែង HTML ទៅជាអត្ថបទ (text)៖ `lynx -dump -stdin`
* សម្រាប់ Markdown, HTML, និងការបំប្លែងឯកសារគ្រប់ប្រភេទ, សាកល្បង [`pandoc`](http://pandoc.org/)។ ឧទាហរណ៍, ដើម្បីបំប្លែងឯកសារ Markdown ទៅជាទម្រង់ Word៖ `pandoc README.md --from markdown --to docx -o temp.docx`
* ប្រសិនបើអ្នកត្រូវដោះស្រាយជាមួយ XML, `xmlstarlet` គឺចាស់ប៉ុន្តែល្អ។
* សម្រាប់ JSON, ប្រើ [`jq`](http://stedolan.github.io/jq/)។ សម្រាប់ការប្រើប្រាស់បែបអន្តរកម្ម, សូមមើល [`jid`](https://github.com/simeji/jid) និង [`jiq`](https://github.com/fiatjaf/jiq) ផងដែរ។
* សម្រាប់ YAML, ប្រើ [`shyaml`](https://github.com/0k/shyaml)។
* សម្រាប់ឯកសារ Excel ឬ CSV, [csvkit](https://github.com/onyxfish/csvkit) ផ្តល់នូវ `in2csv`, `csvcut`, `csvjoin`, `csvgrep`, ។ល។
* សម្រាប់ Amazon S3, [`s3cmd`](https://github.com/s3tools/s3cmd) គឺងាយស្រួល និង [`s4cmd`](https://github.com/bloomreach/s4cmd) គឺលឿនជាង។ [`aws`](https://github.com/aws/aws-cli) របស់ Amazon និង [`saws`](https://github.com/donnemartin/saws) ដែលបានកែលម្អគឺចាំបាច់សម្រាប់កិច្ចការ AWS ផ្សេងទៀត។
* ដឹងអំពី `sort` និង `uniq`, រួមទាំងជម្រើស `-u` និង `-d` របស់ uniq -- សូមមើល one-liners ខាងក្រោម។ សូមមើល `comm` ផងដែរ។
* ដឹងអំពី `cut`, `paste`, និង `join` ដើម្បីចាត់ចែងឯកសារអត្ថបទ។ មនុស្សជាច្រើនប្រើ `cut` ប៉ុន្តែភ្លេចអំពី `join`។
* ដឹងអំពី `wc` ដើម្បីរាប់ newlines (`-l`), characters (`-m`), words (`-w`) និង bytes (`-c`)។
* ដឹងអំពី `tee` ដើម្បីចម្លងពី stdin ទៅឯកសារ និងទៅ stdout ផងដែរ, ដូចនៅក្នុង `ls -al | tee file.txt`។
* សម្រាប់ការគណនាដែលស្មុគស្មាញជាងនេះ, រួមទាំងការដាក់ក្រុម, ការត្រឡប់ fields, និងការគណនាស្ថិតិ, ពិចារណា [`datamash`](https://www.gnu.org/software/datamash/)។
* ដឹងថា locale ប៉ះពាល់ដល់ឧបករណ៍ command line ជាច្រើនតាមវិធីដែលមិននឹកស្មានដល់, រួមទាំងលំដាប់នៃការតម្រៀប (sorting order/collation) និងប្រសិទ្ធភាព (performance)។ ការដំឡើង Linux ភាគច្រើននឹងកំណត់ `LANG` ឬ locale variables ផ្សេងទៀតទៅការកំណត់ក្នុងតំបន់ដូចជា US English។ ប៉ុន្តែសូមប្រយ័ត្ន ការតម្រៀបនឹងផ្លាស់ប្តូរប្រសិនបើអ្នកផ្លាស់ប្តូរ locale។ និងដឹងថា i18n routines អាចធ្វើឱ្យ sort ឬពាក្យបញ្ជាផ្សេងទៀតដំណើរការយឺតជាង *ច្រើនដង*។ នៅក្នុងស្ថានភាពខ្លះ (ដូចជា set operations ឬ uniqueness operations ខាងក្រោម) អ្នកអាចមិនអើពើ i18n routines ដែលយឺតដោយសុវត្ថិភាព និងប្រើប្រាស់ byte-based sort order បែបប្រពៃណី, ដោយប្រើ `export LC_ALL=C`។
* អ្នកអាចកំណត់ environment របស់ពាក្យបញ្ជាជាក់លាក់មួយដោយដាក់ environment variable settings នៅពីមុខការហៅរបស់វា, ដូចនៅក្នុង `TZ=Pacific/Fiji date`។
* ដឹងមូលដ្ឋាន `awk` និង `sed` សម្រាប់ការកែសម្រួលទិន្នន័យសាមញ្ញ។ សូមមើល [One-liners](#ពាក្យបញ្ជាមួយជួរ-one-liners) សម្រាប់ឧទាហរណ៍។
* ដើម្បីជំនួសរាល់ការកើតឡើងនៃខ្សែអក្សរនៅនឹងកន្លែង (in place), នៅក្នុងឯកសារមួយ ឬច្រើន៖

```sh
      perl -pi.bak -e 's/old-string/new-string/g' my-files-*.txt

```

* ដើម្បីប្តូរឈ្មោះឯកសារជាច្រើន និង/ឬស្វែងរក និងជំនួសនៅក្នុងឯកសារ, សាកល្បង [`repren`](https://github.com/jlevy/repren)។ (ក្នុងករណីខ្លះពាក្យបញ្ជា `rename` ក៏អនុញ្ញាតឱ្យប្តូរឈ្មោះច្រើនផងដែរ, ប៉ុន្តែត្រូវប្រយ័ត្នព្រោះមុខងាររបស់វាមិនដូចគ្នានៅលើ Linux distributions ទាំងអស់ទេ។)

```sh
      # ប្តូរឈ្មោះពេញលេញនៃ filenames, directories, និង contents foo -> bar:
      repren --full --preserve-case --from foo --to bar .
      # សង្គ្រោះ backup files whatever.bak -> whatever:
      repren --renames --from '(.*)\.bak' --to '\1' *.bak
      # ដូចខាងលើ, ប្រើ rename, ប្រសិនបើមាន៖
      rename 's/\.bak$//' *.bak

```

* ដូចដែល man page និយាយ, `rsync` ពិតជាឧបករណ៍ចម្លងឯកសារដែលលឿន និងមានសមត្ថភាពខ្ពស់។ វាត្រូវបានគេស្គាល់សម្រាប់ការធ្វើសមកាលកម្មរវាងម៉ាស៊ីន ប៉ុន្តែក៏មានប្រយោជន៍ដូចគ្នាក្នុងមូលដ្ឋាន។ នៅពេលដែលការរឹតបន្តឹងសុវត្ថិភាពអនុញ្ញាត, ការប្រើ `rsync` ជំនួសឱ្យ `scp` អនុញ្ញាតឱ្យសង្គ្រោះការផ្ទេរដោយមិនចាំបាច់ចាប់ផ្តើមពីដើម។ វាក៏ស្ថិតក្នុងចំណោម [វិធីលឿនបំផុត](https://web.archive.org/web/20130929001850/http://linuxnote.net/jianingy/en/linux/a-fast-way-to-remove-huge-number-of-files.html) ដើម្បីលុបឯកសារចំនួនច្រើន៖

```sh
mkdir empty && rsync -r --delete empty/ some-dir && rmdir some-dir

```

* សម្រាប់ការតាមដានវឌ្ឍនភាពនៅពេលដំណើរការឯកសារ, ប្រើ [`pv`](http://www.ivarch.com/programs/pv.shtml), [`pycp`](https://github.com/dmerejkowsky/pycp), [`pmonitor`](https://github.com/dspinellis/pmonitor), [`progress`](https://github.com/Xfennec/progress), `rsync --progress`, ឬ, សម្រាប់ការចម្លងកម្រិត block, `dd status=progress`។
* ប្រើ `shuf` ដើម្បីសាប់ (shuffle) ឬជ្រើសរើសបន្ទាត់ចៃដន្យពីឯកសារ។
* ដឹងពីជម្រើសរបស់ `sort`។ សម្រាប់លេខ, ប្រើ `-n`, ឬ `-h` សម្រាប់ការដោះស្រាយលេខដែលមនុស្សអាចអានបាន (human-readable numbers) (ឧ. ពី `du -h`)។ ដឹងពីរបៀបដែល keys ធ្វើការ (`-t` និង `-k`)។ ជាពិសេស, ប្រយ័ត្នថាអ្នកត្រូវសរសេរ `-k1,1` ដើម្បីតម្រៀបតាម field ទីមួយប៉ុណ្ណោះ; `-k1` មានន័យថាតម្រៀបតាមបន្ទាត់ទាំងមូល។ Stable sort (`sort -s`) អាចមានប្រយោជន៍។ ឧទាហរណ៍, ដើម្បីតម្រៀបដំបូងតាម field 2, បន្ទាប់មកបន្ទាប់បន្សំតាម field 1, អ្នកអាចប្រើ `sort -k1,1 | sort -s -k2,2`។
* ប្រសិនបើអ្នកត្រូវការសរសេរ tab literal នៅក្នុង command line ក្នុង Bash (ឧ. សម្រាប់អាគុយម៉ង់ -t ទៅ sort), ចុច **ctrl-v** **[Tab]** ឬសរសេរ `$'\t'` (ក្រោយមកទៀតគឺល្អជាងព្រោះអ្នកអាច copy/paste វាបាន)។
* ឧបករណ៍ស្តង់ដារសម្រាប់ការ patch source code គឺ `diff` និង `patch`។ សូមមើល `diffstat` សម្រាប់ស្ថិតិសង្ខេបនៃ diff និង `sdiff` សម្រាប់ side-by-side diff។ ចំណាំ `diff -r` ដំណើរការសម្រាប់ directories ទាំងមូល។ ប្រើ `diff -r tree1 tree2 | diffstat` សម្រាប់ការសង្ខេបនៃការផ្លាស់ប្តូរ។ ប្រើ `vimdiff` ដើម្បីប្រៀបធៀប និងកែសម្រួលឯកសារ។
* សម្រាប់ binary files, ប្រើ `hd`, `hexdump` ឬ `xxd` សម្រាប់ simple hex dumps និង `bvi`, `hexedit` ឬ `biew` សម្រាប់ binary editing។
* សម្រាប់ binary files ផងដែរ, `strings` (បូក `grep`, ។ល។) អនុញ្ញាតឱ្យអ្នកស្វែងរកបំណែកនៃអត្ថបទ។
* សម្រាប់ binary diffs (delta compression), ប្រើ `xdelta3`។
* ដើម្បីបំប្លែង text encodings, សាកល្បង `iconv`។ ឬ `uconv` សម្រាប់ការប្រើប្រាស់កម្រិតខ្ពស់; វាគាំទ្ររឿង Unicode កម្រិតខ្ពស់មួយចំនួន។ ឧទាហរណ៍៖

```sh
      # បង្ហាញ hex codes ឬឈ្មោះជាក់ស្តែងនៃតួអក្សរ (មានប្រយោជន៍សម្រាប់ debugging):
      uconv -f utf-8 -t utf-8 -x '::Any-Hex;' < input.txt
      uconv -f utf-8 -t utf-8 -x '::Any-Name;' < input.txt
      # អក្សរតូច និងលុប accents ទាំងអស់ (ដោយពង្រីក និងទម្លាក់ពួកវា):
      uconv -f utf-8 -t utf-8 -x '::Any-Lower; ::Any-NFD; [:Nonspacing Mark:] >; ::Any-NFC;' < input.txt > output.txt

```

* ដើម្បីបំបែកឯកសារជាផ្នែកៗ, សូមមើល `split` (ដើម្បីបំបែកតាមទំហំ) និង `csplit` (ដើម្បីបំបែកតាម pattern)។
* កាលបរិច្ឆេទ និងពេលវេលា៖ ដើម្បីទទួលបានកាលបរិច្ឆេទ និងពេលវេលាបច្ចុប្បន្ននៅក្នុងទម្រង់ [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) ដ៏មានប្រយោជន៍, ប្រើ `date -u +"%Y-%m-%dT%H:%M:%SZ"` (ជម្រើសផ្សេងទៀត [មាន](https://stackoverflow.com/questions/7216358/date-command-on-os-x-doesnt-have-iso-8601-i-option) [បញ្ហា](https://unix.stackexchange.com/questions/164826/date-command-iso-8601-option))។ ដើម្បីចាត់ចែងកន្សោម (expressions) កាលបរិច្ឆេទ និងពេលវេលា, ប្រើ `dateadd`, `datediff`, `strptime` ។ល។ ពី [`dateutils`](http://www.fresse.org/dateutils/)។
* ប្រើ `zless`, `zmore`, `zcat`, និង `zgrep` ដើម្បីប្រតិបត្តិការលើឯកសារដែលបានបង្ហាប់ (compressed files)។
* គុណលក្ខណៈឯកសារ (File attributes) អាចកំណត់បានតាមរយៈ `chattr` និងផ្តល់ជម្រើសកម្រិតទាបជាង file permissions។ ឧទាហរណ៍, ដើម្បីការពារប្រឆាំងនឹងការលុបឯកសារដោយចៃដន្យនូវ immutable flag៖ `sudo chattr +i /critical/directory/or/file`
* ប្រើ `getfacl` និង `setfacl` ដើម្បីរក្សាទុក និងស្តារ file permissions។ ឧទាហរណ៍៖

```sh
   getfacl -R /some/path > permissions.txt
   setfacl --restore=permissions.txt

```

* ដើម្បីបង្កើតឯកសារទទេរហ័ស, ប្រើ `truncate` (បង្កើត [sparse file](https://en.wikipedia.org/wiki/Sparse_file)), `fallocate` (ext4, xfs, btrfs និង ocfs2 filesystems), `xfs_mkfile` (ស្ទើរតែគ្រប់ filesystems, មកក្នុងកញ្ចប់ xfsprogs), `mkfile` (សម្រាប់ប្រព័ន្ធដូច Unix ដូចជា Solaris, Mac OS)។

## ការដោះស្រាយបញ្ហាប្រព័ន្ធ (System debugging)

* សម្រាប់ web debugging, `curl` និង `curl -I` គឺងាយស្រួល, ឬសមមូល `wget` របស់ពួកគេ, ឬ [`httpie`](https://github.com/jkbrzt/httpie) ដ៏ទំនើបជាង។
* ដើម្បីដឹងពីស្ថានភាព cpu/disk បច្ចុប្បន្ន, ឧបករណ៍បុរាណគឺ `top` (ឬ `htop` ដែលល្អជាង), `iostat`, និង `iotop`។ ប្រើ `iostat -mxz 15` សម្រាប់ស្ថិតិ CPU មូលដ្ឋាន និងស្ថិតិ disk លម្អិតតាម partition និងការយល់ដឹងពីប្រសិទ្ធភាព។
* សម្រាប់ព័ត៌មានលម្អិតនៃការតភ្ជាប់បណ្តាញ, ប្រើ `netstat` និង `ss`។
* សម្រាប់ការមើលទិដ្ឋភាពទូទៅរហ័សនៃអ្វីដែលកំពុងកើតឡើងនៅលើប្រព័ន្ធ, `dstat` គឺមានប្រយោជន៍ជាពិសេស។ សម្រាប់ទិដ្ឋភាពទូទៅបំផុតជាមួយនឹងព័ត៌មានលម្អិត, ប្រើ [`glances`](https://github.com/nicolargo/glances)។
* ដើម្បីដឹងពីស្ថានភាព memory, ដំណើរការ និងយល់ពី output នៃ `free` និង `vmstat`។ ជាពិសេស, ត្រូវដឹងថាតម្លៃ "cached" គឺជា memory ដែលកាន់កាប់ដោយ Linux kernel ជា file cache, ដូច្នេះមានប្រសិទ្ធភាពរាប់ចូលទៅក្នុងតម្លៃ "free"។
* Java system debugging គឺជារឿងផ្សេងមួយ, ប៉ុន្តែល្បិចសាមញ្ញមួយនៅលើ JVMs របស់ Oracle និងខ្លះទៀតគឺអ្នកអាចដំណើរការ `kill -3 <pid>` ហើយ full stack trace និង heap summary (រួមទាំងព័ត៌មានលម្អិត generational garbage collection, ដែលអាចផ្តល់ព័ត៌មានខ្ពស់) នឹងត្រូវបាន dumped ទៅ stderr/logs។ `jps`, `jstat`, `jstack`, `jmap` របស់ JDK គឺមានប្រយោជន៍។ [SJK tools](https://github.com/aragozin/jvm-tools) គឺកម្រិតខ្ពស់ជាង។
* ប្រើ [`mtr`](http://www.bitwizard.nl/mtr/) ជា traceroute ប្រសើរជាង, ដើម្បីកំណត់អត្តសញ្ញាណបញ្ហាបណ្តាញ។
* សម្រាប់ការមើលថាតើហេតុអ្វីបានជា disk ពេញ, [`ncdu`](https://dev.yorhel.nl/ncdu) សន្សំពេលវេលាជាងពាក្យបញ្ជាធម្មតាដូចជា `du -sh *`។
* ដើម្បីស្វែងរក socket ឬ process ណាដែលកំពុងប្រើ bandwidth, សាកល្បង [`iftop`](http://www.ex-parrot.com/~pdw/iftop/) ឬ [`nethogs`](https://github.com/raboof/nethogs)។
* ឧបករណ៍ `ab` (មកជាមួយ Apache) គឺមានប្រយោជន៍សម្រាប់ការពិនិត្យមើល web server performance បែប quick-and-dirty។ សម្រាប់ការធ្វើតេស្តបន្ទុក (load testing) ដែលស្មុគស្មាញជាងនេះ, សាកល្បង `siege`។
* សម្រាប់ network debugging ដែលធ្ងន់ធ្ងរជាងនេះ, [`wireshark`](https://wireshark.org/), [`tshark`](https://www.wireshark.org/docs/wsug_html_chunked/AppToolstshark.html), ឬ [`ngrep`](http://ngrep.sourceforge.net/)។
* ដឹងអំពី `strace` និង `ltrace`។ ទាំងនេះអាចមានប្រយោជន៍ប្រសិនបើកម្មវិធីមួយកំពុងបរាជ័យ, គាំង (hanging), ឬ crashing, ហើយអ្នកមិនដឹងថាហេតុអ្វី, ឬប្រសិនបើអ្នកចង់ទទួលបានគំនិតទូទៅនៃប្រសិទ្ធភាព។ ចំណាំជម្រើស profiling (`-c`), និងលទ្ធភាពក្នុងការ attach ទៅ running process (`-p`)។ ប្រើជម្រើស trace child (`-f`) ដើម្បីជៀសវាងការខកខានការហៅដ៏សំខាន់។
* ដឹងអំពី `ldd` ដើម្បីពិនិត្យមើល shared libraries ។ល។ — ប៉ុន្តែ [កុំដំណើរការវាលើឯកសារដែលមិនគួរឱ្យទុកចិត្ត](http://www.catonmat.net/blog/ldd-arbitrary-code-execution/)។
* ដឹងពីរបៀប connect ទៅ running process ជាមួយ `gdb` និងទទួលបាន stack traces របស់វា។
* ប្រើ `/proc`។ វាមានប្រយោជន៍អស្ចារ្យណាស់ជួនកាលនៅពេល debugging បញ្ហាផ្ទាល់។ ឧទាហរណ៍៖ `/proc/cpuinfo`, `/proc/meminfo`, `/proc/cmdline`, `/proc/xxx/cwd`, `/proc/xxx/exe`, `/proc/xxx/fd/`, `/proc/xxx/smaps` (ដែល `xxx` គឺជា process id ឬ pid)។
* នៅពេល debugging ថាហេតុអ្វីបានជាមានអ្វីមួយខុសប្រក្រតីកាលពីអតីតកាល, [`sar`](http://sebastien.godard.pagesperso-orange.fr/) អាចមានប្រយោជន៍ខ្លាំង។ វាបង្ហាញស្ថិតិប្រវត្តិសាស្រ្តលើ CPU, memory, network, ។ល។
* សម្រាប់ការវិភាគប្រព័ន្ធ និងប្រសិទ្ធភាពកាន់តែស៊ីជម្រៅ, មើល `stap` ([SystemTap](https://sourceware.org/systemtap/wiki)), [`perf`](https://en.wikipedia.org/wiki/Perf_%2528Linux%2529), និង [`sysdig`](https://github.com/draios/sysdig)។
* ពិនិត្យមើលថាអ្នកកំពុងនៅលើ OS អ្វីជាមួយ `uname` ឬ `uname -a` (ព័ត៌មាន Unix/kernel ទូទៅ) ឬ `lsb_release -a` (ព័ត៌មាន Linux distro)។
* ប្រើ `dmesg` នៅពេលណាដែលមានអ្វីមួយដំណើរការប្លែកៗ (វាអាចជាបញ្ហា hardware ឬ driver)។
* ប្រសិនបើអ្នកលុបឯកសារ ហើយវាមិន free up disk space ដែលរំពឹងទុកដូចដែលបានរាយការណ៍ដោយ `du`, ពិនិត្យមើលថាតើឯកសារកំពុងប្រើប្រាស់ដោយ process ដែរឬទេ៖
`lsof | grep deleted | grep "filename-of-my-big-file"`

## ពាក្យបញ្ជាមួយជួរ (One-liners)

ឧទាហរណ៍មួយចំនួននៃការផ្គុំពាក្យបញ្ជាចូលគ្នា៖

* វាមានប្រយោជន៍គួរឱ្យកត់សម្គាល់ជួនកាលដែលអ្នកអាចធ្វើ set intersection, union, និង difference នៃ text files តាមរយៈ `sort`/`uniq`។ ឧបមាថា `a` និង `b` គឺជា text files ដែលត្រូវបាន uniqued រួចហើយ។ នេះគឺលឿន, និងដំណើរការលើឯកសារដែលមានទំហំណាមួយ, រហូតដល់ gigabytes ជាច្រើន។ (Sort មិនត្រូវបានកំណត់ដោយ memory ទេ, ទោះបីជាអ្នកប្រហែលជាត្រូវប្រើជម្រើស `-T` ប្រសិនបើ `/tmp` នៅលើ root partition តូចក៏ដោយ។) សូមមើលផងដែរចំណាំអំពី `LC_ALL` ខាងលើ និងជម្រើស `-u` របស់ `sort` (ទុកចោលដើម្បីភាពច្បាស់លាស់ខាងក្រោម)។

```sh
      sort a b | uniq > c   # c គឺជា union នៃ a និង b
      sort a b | uniq -d > c   # c គឺជា intersect នៃ a និង b
      sort a b b | uniq -u > c   # c គឺជា set difference a - b

```

* Pretty-print JSON files ពីរ, normalizing syntax របស់ពួកគេ, បន្ទាប់មក coloring និង paginating លទ្ធផល៖

```
      diff <(jq --sort-keys . < file1.json) <(jq --sort-keys . < file2.json) | colordiff | less -R

```

* ប្រើ `grep . *` ដើម្បីពិនិត្យមើលមាតិកានៃឯកសារទាំងអស់នៅក្នុង directory យ៉ាងឆាប់រហ័ស (ដូច្នេះរាល់បន្ទាត់ត្រូវបានផ្គូផ្គងជាមួយឈ្មោះឯកសារ), ឬ `head -100 *` (ដូច្នេះរាល់ឯកសារមាន heading)។ នេះអាចមានប្រយោជន៍សម្រាប់ directories ដែលពោរពេញទៅដោយការកំណត់ config ដូចជានៅក្នុង `/sys`, `/proc`, `/etc`។
* បូកលេខទាំងអស់ក្នុងជួរឈរទីបីនៃ text file (នេះទំនងជាលឿនជាង 3X និងកូដតិចជាង 3X ជាង Python ដែលសមមូល)៖

```sh
      awk '{ x += $3 } END { print x }' myfile

```

* ដើម្បីមើលទំហំ/កាលបរិច្ឆេទនៅលើ tree of files, នេះគឺដូចជា `ls -l` បែប recursive ប៉ុន្តែាងាយស្រួលអានជាង `ls -lR`៖

```sh
      find . -type f -ls

```

* និយាយថាអ្នកមាន text file, ដូចជា web server log, និងតម្លៃជាក់លាក់មួយដែលបង្ហាញនៅលើបន្ទាត់ខ្លះ, ដូចជា `acct_id` parameter ដែលមាននៅក្នុង URL។ ប្រសិនបើអ្នកចង់បានចំនួនសរុបនៃសំណើ (requests) សម្រាប់ `acct_id` នីមួយៗ៖

```sh
      egrep -o 'acct_id=[0-9]+' access.log | cut -d= -f2 | sort | uniq -c | sort -rn

```

* ដើម្បីតាមដានការផ្លាស់ប្តូរជាបន្តបន្ទាប់, ប្រើ `watch`, ឧ. ពិនិត្យមើលការផ្លាស់ប្តូរចំពោះឯកសារនៅក្នុង directory ជាមួយ `watch -d -n 2 'ls -rtlh | tail'` ឬចំពោះការកំណត់ network ខណៈពេល troubleshooting wifi settings របស់អ្នកជាមួយ `watch -d -n 2 ifconfig`។
* ដំណើរការ function នេះដើម្បីទទួលបានគន្លឹះចៃដន្យពីឯកសារនេះ (parses Markdown និងស្រង់យកធាតុមួយ)៖

```sh
      function taocl() {
        curl -s https://raw.githubusercontent.com/jlevy/the-art-of-command-line/master/README.md |
          sed '/cowsay[.]png/d' |
          pandoc -f markdown -t html |
          xmlstarlet fo --html --dropdtd |
          xmlstarlet sel -t -v "(html/body/ul/li[count(p)>0])[$RANDOM mod last()+1]" |
          xmlstarlet unesc | fmt -80 | iconv -t US
      }

```

## មិនសូវស្គាល់តែមានប្រយោជន៍ (Obscure but useful)

* `expr`: អនុវត្តប្រតិបត្តិការ arithmetic ឬ boolean ឬវាយតម្លៃ regular expressions
* `m4`: simple macro processor
* `yes`: បោះពុម្ពខ្សែអក្សរដដែលៗជាច្រើន
* `cal`: ប្រតិទិនដ៏ស្រស់ស្អាត
* `env`: ដំណើរការពាក្យបញ្ជា (មានប្រយោជន៍ក្នុង scripts)
* `printenv`: បោះពុម្ព environment variables (មានប្រយោជន៍ក្នុង debugging និង scripts)
* `look`: ស្វែងរកពាក្យអង់គ្លេស (ឬបន្ទាត់ក្នុងឯកសារ) ដែលចាប់ផ្តើមដោយខ្សែអក្សរ
* `cut`, `paste` និង `join`: ការកែសម្រួលទិន្នន័យ
* `fmt`: ទម្រង់កថាខណ្ឌអត្ថបទ (format text paragraphs)
* `pr`: ទម្រង់អត្ថបទទៅជាទំព័រ/ជួរឈរ
* `fold`: រុំបន្ទាត់នៃអត្ថបទ (wrap lines of text)
* `column`: ទម្រង់ text fields ទៅជាជួរឈរឬតារាងដែលមានទទឹងថេរ, តម្រឹមគ្នា
* `expand` និង `unexpand`: បំប្លែងរវាង tabs និង spaces
* `nl`: បន្ថែមលេខបន្ទាត់
* `seq`: បោះពុម្ពលេខ
* `bc`: ម៉ាស៊ីនគិតលេខ
* `factor`: factor integers
* [`gpg`](https://gnupg.org/): encrypt និង sign ឯកសារ
* `toe`: តារាងនៃ terminfo entries
* `nc`: network debugging និងការផ្ទេរទិន្នន័យ
* `socat`: socket relay និង tcp port forwarder (ស្រដៀងនឹង `netcat`)
* [`slurm`](https://github.com/mattthias/slurm): network traffic visualization
* `dd`: ផ្លាស់ទីទិន្នន័យរវាងឯកសារ ឬឧបករណ៍
* `file`: កំណត់អត្តសញ្ញាណប្រភេទនៃឯកសារ
* `tree`: បង្ហាញ directories និង subdirectories ជា nesting tree; ដូច `ls` ប៉ុន្តែ recursive
* `stat`: ព័ត៌មានឯកសារ
* `time`: ប្រតិបត្តិ និងកំណត់ពេលវេលាពាក្យបញ្ជា
* `timeout`: ប្រតិបត្តិពាក្យបញ្ជាសម្រាប់ចំនួនពេលវេលាដែលបានបញ្ជាក់ ហើយបញ្ឈប់ process នៅពេលចំនួនពេលវេលាដែលបានបញ្ជាក់បញ្ចប់។
* `lockfile`: បង្កើត semaphore file ដែលអាចត្រូវបានលុបដោយ `rm -f` ប៉ុណ្ណោះ
* `logrotate`: បង្វិល, បង្ហាប់ និងផ្ញើអ៊ីមែល logs។
* `watch`: ដំណើរការពាក្យបញ្ជាម្តងហើយម្តងទៀត, បង្ហាញលទ្ធផល និង/ឬ highlighting ការផ្លាស់ប្តូរ
* [`when-changed`](https://github.com/joh/when-changed): ដំណើរការពាក្យបញ្ជាណាមួយដែលអ្នកបញ្ជាក់នៅពេលណាដែលវាឃើញឯកសារផ្លាស់ប្តូរ។ សូមមើល `inotifywait` និង `entr` ផងដែរ។
* `tac`: បោះពុម្ពឯកសារបញ្ច្រាស (reverse)
* `comm`: ប្រៀបធៀប sorted files មួយបន្ទាត់ម្តងៗ
* `strings`: ស្រង់យកអត្ថបទពី binary files
* `tr`: ការបកប្រែឬកែសម្រួលតួអក្សរ
* `iconv` ឬ `uconv`: ការបំប្លែងសម្រាប់ text encodings
* `split` និង `csplit`: ការបំបែកឯកសារ
* `sponge`: អាន input ទាំងអស់មុនពេលសរសេរវា, មានប្រយោជន៍សម្រាប់ការអានពីបន្ទាប់មកសរសេរទៅឯកសារតែមួយ, ឧ., `grep -v something some-file | sponge some-file`
* `units`: ការបំប្លែងខ្នាត និងការគណនា; បំប្លែង furlongs per fortnight ទៅ twips per blink (សូមមើល `/usr/share/units/definitions.units` ផងដែរ)
* `apg`: បង្កើតពាក្យសម្ងាត់ចៃដន្យ
* `xz`: ការបង្ហាប់ឯកសារអនុបាតខ្ពស់ (high-ratio file compression)
* `ldd`: ព័ត៌មាន dynamic library
* `nm`: symbols ពី object files
* `ab` ឬ [`wrk`](https://github.com/wg/wrk): benchmarking web servers
* `strace`: system call debugging
* [`mtr`](http://www.bitwizard.nl/mtr/): traceroute ប្រសើរជាងសម្រាប់ network debugging
* `cssh`: visual concurrent shell
* `rsync`: sync ឯកសារ និងថតឯកសារតាមរយៈ SSH ឬក្នុង local file system
* [`wireshark`](https://wireshark.org/) និង [`tshark`](https://www.wireshark.org/docs/wsug_html_chunked/AppToolstshark.html): packet capture និង network debugging
* [`ngrep`](http://ngrep.sourceforge.net/): grep សម្រាប់ network layer
* `host` និង `dig`: DNS lookups
* `lsof`: ព័ត៌មាន process file descriptor និង socket
* `dstat`: ស្ថិតិប្រព័ន្ធដែលមានប្រយោជន៍
* [`glances`](https://github.com/nicolargo/glances): កម្រិតខ្ពស់, multi-subsystem overview
* `iostat`: ស្ថិតិ Disk usage
* `mpstat`: ស្ថិតិ CPU usage
* `vmstat`: ស្ថិតិ Memory usage
* `htop`: កំណែដែលបានកែលម្អនៃ top
* `last`: ប្រវត្តិ login
* `w`: នរណាកំពុង logged on
* `id`: ព័ត៌មានអត្តសញ្ញាណ user/group
* [`sar`](http://sebastien.godard.pagesperso-orange.fr/): ស្ថិតិប្រព័ន្ធប្រវត្តិសាស្រ្ត
* [`iftop`](http://www.ex-parrot.com/~pdw/iftop/) ឬ [`nethogs`](https://github.com/raboof/nethogs): network utilization តាម socket ឬ process
* `ss`: ស្ថិតិ socket
* `dmesg`: សារកំហុស boot និងប្រព័ន្ធ
* `sysctl`: មើល និងកំណត់រចនាសម្ព័ន្ធ Linux kernel parameters នៅ run time
* `hdparm`: SATA/ATA disk manipulation/performance
* `lsblk`: រាយបញ្ជី block devices: tree view នៃ disks និង disk partitions របស់អ្នក
* `lshw`, `lscpu`, `lspci`, `lsusb`, `dmidecode`: ព័ត៌មាន hardware, រួមទាំង CPU, BIOS, RAID, graphics, devices, ។ល។
* `lsmod` និង `modinfo`: រាយបញ្ជី និងបង្ហាញព័ត៌មានលម្អិតនៃ kernel modules។
* `fortune`, `ddate`, និង `sl`: um, well, វាអាស្រ័យលើថាតើអ្នកចាត់ទុកក្បាលរថភ្លើងចំហាយ និង Zippy quotations ជា "ប្រយោជន៍" ដែរឬទេ

## សម្រាប់តែ macOS (macOS only)

ទាំងនេះគឺជាធាតុដែលពាក់ព័ន្ធ *តែ* នៅលើ macOS ប៉ុណ្ណោះ។

* ការគ្រប់គ្រងកញ្ចប់ (Package management) ជាមួយ `brew` (Homebrew) និង/ឬ `port` (MacPorts)។ ទាំងនេះអាចត្រូវបានប្រើដើម្បីដំឡើងពាក្យបញ្ជាជាច្រើនខាងលើនៅលើ macOS។
* ចម្លង output នៃពាក្យបញ្ជាណាមួយទៅ desktop app ជាមួយ `pbcopy` និង paste input ពី desktop app ជាមួយ `pbpaste`។
* ដើម្បីបើក Option key នៅក្នុង macOS Terminal ជា alt key (ដូចដែលបានប្រើក្នុងពាក្យបញ្ជាខាងលើដូចជា **alt-b**, **alt-f**, ។ល។), បើក Preferences -> Profiles -> Keyboard ហើយជ្រើសរើស "Use Option as Meta key"។
* ដើម្បីបើកឯកសារជាមួយ desktop app, ប្រើ `open` ឬ `open -a /Applications/Whatever.app`។
* Spotlight: ស្វែងរកឯកសារជាមួយ `mdfind` និងរាយបញ្ជី metadata (ដូចជា photo EXIF info) ជាមួយ `mdls`។
* ត្រូវដឹងថា macOS គឺផ្អែកលើ BSD Unix, និងពាក្យបញ្ជាជាច្រើន (ឧទាហរណ៍ `ps`, `ls`, `tail`, `awk`, `sed`) មានការប្រែប្រួលបន្តិចបន្តួចជាច្រើនពី Linux, ដែលត្រូវបានជះឥទ្ធិពលយ៉ាងខ្លាំងដោយ System V-style Unix និង GNU tools។ អ្នកអាចប្រាប់ពីភាពខុសគ្នាញឹកញាប់ដោយកត់សម្គាល់ man page មានចំណងជើង "BSD General Commands Manual." ក្នុងករណីខ្លះ GNU versions អាចត្រូវបានដំឡើងផងដែរ (ដូចជា `gawk` និង `gsed` សម្រាប់ GNU awk និង sed)។ ប្រសិនបើសរសេរ cross-platform Bash scripts, ជៀសវាងពាក្យបញ្ជាបែបនេះ (ឧទាហរណ៍, ពិចារណា Python ឬ `perl`) ឬសាកល្បងដោយប្រុងប្រយ័ត្ន។
* ដើម្បីទទួលបានព័ត៌មាន macOS release, ប្រើ `sw_vers`។

## សម្រាប់តែ Windows (Windows only)

ធាតុទាំងនេះគឺពាក់ព័ន្ធ *តែ* នៅលើ Windows ប៉ុណ្ណោះ។

### វិធីដើម្បីទទួលបាន Unix tools នៅក្រោម Windows

* ចូលប្រើថាមពលនៃ Unix shell នៅក្រោម Microsoft Windows ដោយដំឡើង [Cygwin](https://cygwin.com/)។ ភាគច្រើននៃអ្វីដែលបានពិពណ៌នានៅក្នុងឯកសារនេះនឹងដំណើរការ out of the box។
* នៅលើ Windows 10, អ្នកអាចប្រើ [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/about), ដែលផ្តល់នូវ Bash environment ដែលធ្លាប់ស្គាល់ជាមួយ Unix command line utilities។
* ប្រសិនបើអ្នកចង់ប្រើ GNU developer tools (ដូចជា GCC) នៅលើ Windows, ពិចារណា [MinGW](http://www.mingw.org/) និងកញ្ចប់ [MSYS](http://www.mingw.org/wiki/msys) របស់វា, ដែលផ្តល់នូវ utilities ដូចជា bash, gawk, make និង grep។ MSYS មិនមានលក្ខណៈពិសេសទាំងអស់បើធៀបនឹង Cygwin ទេ។ MinGW គឺមានប្រយោជន៍ជាពិសេសសម្រាប់ការបង្កើត native Windows ports នៃ Unix tools។
* ជម្រើសមួយទៀតដើម្បីទទួលបាន Unix look and feel នៅក្រោម Windows គឺ [Cash](https://github.com/dthree/cash)។ ចំណាំថាមានតែ Unix commands និង command-line options តិចតួចប៉ុណ្ណោះដែលមាននៅក្នុង environment នេះ។

### ឧបករណ៍ Windows command-line ដែលមានប្រយោជន៍

* អ្នកអាចអនុវត្ត និង script កិច្ចការ Windows system administration ភាគច្រើនពី command line ដោយរៀន និងប្រើ `wmic`។
* ឧបករណ៍ Windows networking command-line ដើមដែលអ្នកអាចយល់ថាមានប្រយោជន៍រួមមាន `ping`, `ipconfig`, `tracert`, និង `netstat`។
* អ្នកអាចអនុវត្ត [កិច្ចការ Windows មានប្រយោជន៍ជាច្រើន](http://www.thewindowsclub.com/rundll32-shortcut-commands-windows) ដោយហៅពាក្យបញ្ជា `Rundll32`។

### គន្លឹះ និងល្បិច Cygwin

* ដំឡើងកម្មវិធី Unix បន្ថែមជាមួយ package manager របស់ Cygwin។
* ប្រើ `mintty` ជា command-line window របស់អ្នក។
* ចូលប្រើ Windows clipboard តាមរយៈ `/dev/clipboard`។
* ដំណើរការ `cygstart` ដើម្បីបើកឯកសារណាមួយតាមរយៈកម្មវិធីដែលបានចុះឈ្មោះរបស់វា។
* ចូលប្រើ Windows registry ជាមួយ `regtool`។
* ចំណាំថា `C:\` Windows drive path ក្លាយជា `/cygdrive/c` នៅក្រោម Cygwin, និងថា `/` របស់ Cygwin បង្ហាញនៅក្រោម `C:\cygwin` នៅលើ Windows។ បំប្លែងរវាង Cygwin និង Windows-style file paths ជាមួយ `cygpath`។ នេះគឺមានប្រយោជន៍បំផុតនៅក្នុង scripts ដែលហៅ Windows programs។

## ធនធានបន្ថែម (More resources)

* [awesome-shell](https://github.com/alebcay/awesome-shell): បញ្ជីដែលបានរៀបចំនៃ shell tools និងធនធាន។
* [awesome-osx-command-line](https://github.com/herrbischoff/awesome-osx-command-line): ការណែនាំស៊ីជម្រៅបន្ថែមទៀតសម្រាប់ macOS command line។
* [Strict mode](http://redsymbol.net/articles/unofficial-bash-strict-mode/) សម្រាប់ការសរសេរ shell scripts ល្អប្រសើរ។
* [shellcheck](https://github.com/koalaman/shellcheck): ឧបករណ៍ shell script static analysis។ សំខាន់, lint សម្រាប់ bash/sh/zsh។
* [Filenames and Pathnames in Shell](http://www.dwheeler.com/essays/filenames-in-shell.html): ភាពលម្អិតស្មុគស្មាញគួរឱ្យសោកស្តាយអំពីរបៀបដោះស្រាយ filenames ឱ្យបានត្រឹមត្រូវនៅក្នុង shell scripts។
* [Data Science at the Command Line](http://datascienceatthecommandline.com/#tools): ពាក្យបញ្ជា និងឧបករណ៍បន្ថែមទៀតដែលមានប្រយោជន៍សម្រាប់ការធ្វើ data science, ពីសៀវភៅដែលមានឈ្មោះដូចគ្នា។

## ការបដិសេធទទួលខុសត្រូវ (Disclaimer)

លើកលែងតែកិច្ចការតូចតាចបំផុត, កូដត្រូវបានសរសេរដើម្បីឱ្យអ្នកដទៃអាចអានវាបាន។ ជាមួយថាមពលមកជាមួយការទទួលខុសត្រូវ។ ការពិតដែលអ្នក *អាច* ធ្វើអ្វីមួយនៅក្នុង Bash មិនមែនមានន័យថាអ្នកគួរធ្វើវាទេ! ;)

## អាជ្ញាប័ណ្ណ (License)

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

ការងារនេះត្រូវបានផ្តល់អាជ្ញាប័ណ្ណក្រោម [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)។