# php-Backend

## I) Schreibe eine Funktion, die die folgenden Straßen in den Namen und die Hausnummer aufteilt und ausgibt.
Straßen:
- Einsteinstr. 7
- Einsteinstrasse 7
- Curd-Jürgens-Str. 30
- Perlcherstr.88 1
- Rosenheimerstr. 14e-f
- Bei Fußenkreuz 36
- Sankt Georgs Kirchhof 26
- Mallertshofener Strasse 36c
- Rosenheimerstr. 145 e+f
- Hof 151
- Wald a.A. 125
- Lindenhof 0
- Am Elfenholt
- Am Schießberg 35 357
- Idlhofgasse 16A-1
- Kreisbacherstrasse 3/1/19
- Höpflergasse 6 / 18

Beispielaufruf:
$streets = array(
	'Einsteinstr. 7',
	'Einsteinstrasse 7',
	'Curd-Jürgens-Str. 30',
	'Perlcherstr.88 1',
	'Rosenheimerstr. 14e-f',
	'Bei Fußenkreuz 36',
	'Sankt Georgs Kirchhof 26',
	'Mallertshofener Strasse 36c',
	'Rosenheimerstr. 145 e+f',
	'Hof 151',
	'Wald a.A. 125',
	'Lindenhof 0',
	'Am Elfenholt',
	'Am Schießberg 35 357',
	'Idlhofgasse 16A-1',
	'Kreisbacherstrasse 3/1/19',
	'Höpflergasse 6 / 18'
);

foreach ($streets as $street) {
	list($name, $number) = split_street($street);
	echo 'Name: ' . $name . ', Hausnummer: ' . $number . "\n";
}

Beispielausgabe:
> Name: Einsteinstr., Hausnummer: 7
Name: Einsteinstrasse, Hausnummer: 7
Name: Curd-Jürgens-Str., Hausnummer: 30
