# Užduotis

Klientas turi el. Parduotuvę https://demo.prestashop.com/#/en/front ir joje nori pridėti papildomą blokelį prekės puslapyje, nurodyti po kiek laiko nuo užsakymo klientas jį gaus prie displayReassurance hooko pozicijoje. (Plačiau apie PrestaShop hookus https://devdocs.prestashop.com/1.7/modules/concepts/hooks/list-of-hooks/). Modulis turi turėti galimybę konfigūracijos lange turėti tokias funkcijas:
- Rodyti/Nerodyti blokelį (bool)
- Dienų rezervas (integeris) - kiek nuo šiandienos pridėti dienų prekės pristatymui. Kadangi kurjeriai savaitgaliais nedirba - pridedame darbo dienas prie esamos dienos. 
- Laikas iki kada siunta gali būti išsiųsta. Stringas: 00:00 - 23:59 formatu
- Jeigu dabartinis laikas yra iki 13h - pridedame rezervo dienas
- Jeigu dabartinis laikas yra PO 13h - tada pridedame rezervą + 1d. 

### Rezultatas, kurio tikimės mes:
- Github repozitorija būtent Tavo moduliui.
- Modulio kodas, kuris maksimaliai kiek gali ir moki - laikosi PSR standartų ( https://www.php-fig.org/psr/psr-1/ ).
- Hookas atvaizduoja teisingą turinį. Tekstas, kurį turėtų rodyti prie prekės puslapio:
- Užsakius prekę iki 13h - prekę pristatysime 2020-04-14 d.
- Užsakius prekę po 13h - prekę pristatysime 2020-04-15 d.

- CSS/JS papildomi pagal save - nieko fancy nereikia, bet kažkokį stylingą būtų neblogai matyti.
- Modulio parametrai saugomi ps_configuration lentoje.

### Tips:
- Modulio bazei generuoti yra įrankis: https://validator.prestashop.com/generator 
- https://devdocs.prestashop.com/1.7/basics/ - PrestaShop dokumentacija.
