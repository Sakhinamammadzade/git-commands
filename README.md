<h1 align="center">Github üçün təməl anlayışlar</h1>
<h3>Repository</h3>Hərfi mənada: anbar, məlumat anbarı.
### Onu layihənin bütün fayl və qovluqlarını saxlayan verilənlər bazası kimi düşünmək olar. 
Hər bir layihə GitHub-da depo kimi saxlanıla bilər.
Burada təkcə fayllar deyil, həm də fayllara edilən dəyişikliklərin tarixçəsi saxlanılır.
Repozitoriya birdən çox istifadəçi arasında paylaşıla və kopyalana bilər (fork)

<h3>Branch</h3>
> Hərfi mənada: budaq, budaqlanma, ayrı.
Layihəyə yeni funksiya əlavə etmək istədikdə və ya dəyişiklik edildikdə yeni branch yaradılır və bu branchda bütün dəyişikliklər edildikdən sonra o, master branchina birləşdirilir
(merge: birləşmə).

<h3>Fork</h3>
Hərfi mənada: çəngəl
Başqasının deposunda işləmək istədiyiniz zaman layihəni GitHub hesabınıza köçürmək üçün onu ayıra bilərsiniz.
Layihə əslində bir yeniləmə olduqda, fork layihələr bu dəyişikliklərdən təsirlənmir.
Öz hesabınızda saxlamaq istədiyiniz layihənin GitHub səhifəsinin yuxarı sağ küncündəki Fork düyməsini klikləməklə fork edə bilərsiniz.

<h3>Clone</h3>
Hərfi mənada: kopyalamaq, klonlaşdırmaq.
Layihəni kompüterinizə yükləmək istədiyiniz zaman clone əmrindən istifadə edə bilərsiniz.
Terminalda git clone https://github.com/firstproject/github.git yazıb göndərdiyiniz zaman github adlı layihə cari kataloqda github adı ilə yaradılmış qovluğa kopyalanacaq. Repozitoriyanın klon linkinə daxil olmaq üçün sağdakı yaşıl Klon və ya endirmə düyməsini klikləməklə və ya layihənin linkinin sonunda .git uzantısını qoymaqla layihənin GitHub səhifəsinə daxil ola bilərsiniz.


<h1 align="center">Ən çox istifadə edilən git əmrləri</h1>

$git add .
Bu əmr bütün dəyişdirilmiş faylları GitHub-a təqdim etmək üçün hazırlayır (səhnələşdirir). Sonda nöqtə bütün fayllara aiddir. Burada nöqtə yerinə fayl və ya qovluq adını da yaza bilərsiniz.

$git commit -m [commit mesajı]
Bu komanda ilə əvvəlki addımda hazırlanmış dəyişikliklər mesajla lokal repozitoriyada saxlanılır. 
Mesaj hissəsi layihədə edilən dəyişiklikləri təsvir etməlidir.
Nümunə: git commit -m header bitdi".

$git push origin [branch adı]
Bu əmrlə yerli olaraq hazırlanan və saxlanılan dəyişikliklər GitHub-da depoya göndərilir.

Komanda işində branch adı vacibdir. Komandanın hər bir üzvü öz adı ilə və ya üzərində işlədiyi xüsusiyyəti təsvir edən branch yaratmalıdır. Bu branchda qeydə alınan dəyişikliklər, pull request yaradaraq master branch ilə birləşdirilmək üçün komanda rəhbərinin təsdiqinə təqdim edilməlidir.
Bu, səhv kodlarının nəzərdən keçirilmədən əsas məhsul kimi təqdim edilməsinin qarşısını alacaq.

QEYD: İlk push yerinə yetirdiyiniz zaman bir pəncərə açılacaq və 
sizdən GitHub-a oradan daxil olmanız tələb olunacaq.
$git checkout -b [branch adı]
Göstərilən adla yeni branch yaradır.

git checkout [branch adı]
Göstərilən adla brancha keçir.
QEYD: Visual Studio Code ilə işləyərkən sol alt küncdə işlədiyiniz filialın adını görə bilərsiniz.

$git status
Bu əmr deponun cari vəziyyətini göstərir.
Dəyişikliklər layihədə edilibsə, lakin həyata keçirilməyibsə (commit:törət) və ya qəbul edilmiş dəyişikliklərə baxmaq olar.
Nümunə git status əmrinə cavab:
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

$git config — bu komanda vasitəsi ilə git istifadəçi adı , email əlavə edə bilərik, bunları əlavə etmədən hər hası bir iş gördükdə default olaraq sistemdəki username təyin olunacaqdır:

$git init — bu komanda qovluğu bir Git repository halına gətirir və 
.git sonluqlu gizli bir qovluq yaradır. 
Git init komandası qovluğumuzu uzaqdakı bir serverə (GitHub, GitLab, Bitbucket və b.) göndərmək üçün hazır vəziyyətə gətirir.

$git clone — komandası ilə local-dakı və ya uzaq serverdəki (GitHub, GitLab, Bitbucket) istəlinən reponu hazırda olduğumuz qovluğa kopyalayır.

$ git add — add komandası hər-hansı bir yeni faylı və ya qovluqdakı bütün faylları əlavə edir, yəni artıq proyektimiz commit –ə hazır olur.

$ git commit — Commit local maşınımızda baş verən bir prosesidir və uzaq server –dəki reposiroty -ə heç bir təsir göstərmir. Commit vasitəsilə etdiyimiz dəyişikliklər haqqında açıqlamalar qeyd edirik. Commit proyektimizi staging area -dan local repository bölməsinə keçirir:

$git commit -m “proyektin ilk commit-i”

$git status — komandası ilə yaratdığımız faylların gitə əlavə olunub olunmadığına baxa bilərik. Əgər əlavə olunmayıbsa faylın adı qırmızı rənglə yazılı olacaq. Sonra “git add . “ komandası verərək faylları əlavə edə bilərik. Yenidən “git status” komandası versək artıq fallar yaşıl rəngdə yazılacaq.

$git pull — Bu komanda ilə serverdəki repository-də əgər dəyişdirilmiş fayllar varsa, onları local-a yükləyir və faylları yeniləmək üçün repository ilə birləşdirir.

$git push —Bu komanda ilə Commit-lədiyimiz falylları uzaq serverdəki repository-mizə göndəririk.

$git log — bu komanda ilə hansı vaxtda hası dəyişiklikləri etdiyimizi görə bilirik.

$git-rm- git add əmrindən fərqli olaraq, müəyyən etdiyiniz faylı və ya faylları iş kataloqundan silir.

$git remote- "git remote -v" əmri ilə layihəyə qoşulmuş uzaq serverlərin siyahısını verir. Cari layihəni uzaq serverə əlavə etmək üçün "git remote add" əmrini işlədə bilərik.
misal:git remote add origin https://github.com/username/project.git

$git merge <branch_name>-Git-də merge başqa bir branchdan dəyişikliklərin üzərində işlədiyiniz öz branch-a inteqrasiyası etme prosesidir. Git birləşməsi zamanı dəyişikliklərin əksəriyyətini sizin üçün avtomatik birləşdirir.

$git revert- əmri etdiyiniz dəyişiklikləri geri qaytarmaq üçün istifadə olunur. Bu əmrlə commit prosesinizin özü və ya onun məlumatı silinmir, yalnız commitdeki dəyişiklik ləğv edilir. Məsələn, əlavə etdiyiniz xətti silmək istəyirsinizsə, bunu git revert əmri ilə edə bilərsiniz. Əslində, git revert əmri avtomatik olaraq dəyişikliyinizi geri qaytarmaq üçün yeni commit yaradır və geri qaytarma bu commit sayəsində dəyişiklik tarixçəsində görünən olur.

$git-reset-Dəyişiklikləri geri qaytarmaq üçün istifadə edə biləcəyimiz başqa bir əmr git reset əmridir. Bu əmr, həmçinin məlumatlarınızı silmədən əməliyyatı yerinə yetirir, lakin git revert əmrindən fərqli olaraq, avtomatik olaraq yeni bir commit yaratmadan dəyişikliyi ləğv etməyə imkan verir.

$git-diff-Versiya idarəetmə sistemlərində iki versiya arasındakı dəyişikliklər diff adlanır ki, bu da ingiliscə fərq sözünün qısaldılmasıdır. Git-də iki versiya arasındakı fərqləri görmək üçün git diff əmrindən istifadə edə bilərsiniz.

$git-log- Git versiyası idarəetmə sistemində yaradılmış icra tarixçəsini(author,merge,date ve s kimi melumatlari) yuxarıdan aşağıya tarixi ardıcıllıqla konsola yazan Git əmridir

$git-tag-Github-da paylaşdığınız repolara versiyalar əlavə edə bilərsiniz. Yazdığınız repoları pod tərəfə əlavə edərkən, versiyalaşdırma etməlisiniz. Siz git vasitəsilə reponuzun ara versiyalarını və əsas versiyalarını dərc edə bilərsiniz.
