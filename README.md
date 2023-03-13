# APK Decompile Manual

Бърз начин: https://www.decompiler.com
__________________________________

Стъпка по стъпка:

Извличане на dex файловете от apk файл:<br>
	Снабдяване с apk файл     //example.apk<br>
	Преименува се разширението на zip     //example.zip<br>
	Разархивира се zip файла<br>
	Копират се файловете с имена classes и разширения dex     //classes.dex, classes2.dex ... classesN.dex<br>

Превръщане на dex файловете в jar файлове:<br>
&nbsp;&nbsp;&nbsp;&nbsp;Инсталира се:<br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dex2jar-2.0<br>
&nbsp;&nbsp;&nbsp;&nbsp;Поставят се копираните (dex) файлове вътре в папката на dex2jar     //където са bat файловете<br>
&nbsp;&nbsp;&nbsp;&nbsp;Отваря се cmd<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Отива се в директорията на dex2jar<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Изпълнява се:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;d2j-dex2jar.bat classes.dex     //така за всеки dex файл<br>

Получените jar файлове се декомпилират, за да се извлекат java файловете:<br>
	Инсталира се:<br>
		jd-gui-windows-1.6.6<br>
	! Има възможност някои jar-ове да не могат да се декомпилират<br>
		В такъв случай се използва:<br>     
			http://www.javadecompilers.com     //например Procyon<br>
		! Има възможност някои части от кода на java файловете да не успеят да се декомпилират<br>
			В такъв случай се използва друг от възможните декомпилатори     //например CFR<br>

Получаване на xml файловете:<br>
	Изтегля се:<br>
		apktool<br>
	Двата apktool файла се слагат в нова папка<br>
	Вътре в нея се поставя и apk файла<br>
	Отваря се cmd<br>
		Отива се в директорията на apktool папката<br>
		Изпълнява се:<br>
			apktool if example.apk<br>
			apktool d example.apk     //за да се декомпилират<br>

Събиране всичко на едно място<br>
	Взима се съдържанието на папките с java файловете и се поставят в нова папка<br>
		! Някои папки се застъпват с едни и същи имена, но съдържат различни файлове<br>
		! Трябва внимателно да се поставят извлечените директории, така че да не се пропуснат файлове<br>
	Взима се съдържанието от получената папка след apktool декомпилацията и се поставя в новата папка
