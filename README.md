# hse23_project_AIRE
Целью работы над проектом является изучение методами сравнительной геномики ранней эволюции белка AIRE, взаимодействующего с эпигенетической модификацией H3K4me в клетках человека.

AIRE несёт функцию Histone modification read.

Согласно литературным данным "... AIRE избирательно взаимодействует с гистоном H3 через свой первый палец гомеодомена растений (PHD) (AIRE-PHD1) и преимущественно связывается с неметилированным H3K4 (H3K4me0)... AIRE-PHD1 является важным членом недавно идентифицированного класса PHD пальцы, которые специфически распознают H3K4me0…" [Org et al., 2008] "Некоторые посттрансляционные модификации хвостов H3, особенно диметилирование или триметилирование в H3K4, отменяли связывание Aire, в то время как другие допускались." [Koh et al., 2008].

Белок AIRE в комплексы не входит.

Белок AIRE экспрессируется в мозге по GTEx и лимфатическом узле и тимусе по NCBI.

![image](data/AIRE_expression_GTEx.png)
![image](data/AIRE_expression_NCBI_1.png)
![image](data/AIRE_expression_NCBI_2.png)

В белке AIRE наблюдаются домены PHA03247 super family (2), PHD_SF super family (2), HSR super family (2), SAND super family, PRK12323 super family.

![image](data/AIRE_domains.png)

## Анализ гистонов
Для выравнивания белковых последовательностей гистонов использована программа MEGA, алгоритм MUSCLE с задаными по умолчанию параметрами.
Файлы выравниваний лежат в папке data (.mas).

#### H2A
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/9e9bcd9a-ffce-4a43-b2bb-723e75f33016)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/d5153d01-7581-4222-8b9a-762c71cb2390)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/94354f1b-b157-4149-a497-6847edd88bcd)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/7c41476a-7bbc-4e71-a122-e6b9887ff101)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/942f5ef2-3a30-424d-bad3-8c6e4941ff63)

42 последовательность не влезла в скриншот, но она есть в файле выравнивания.

Между белками наблюдается достаточно высокое сходство, чтобы предполагать происхождение от одной последовательности в результате копирования. Различия же объясняются делециями, приведшей к потери концевой части белка в ряде копий, и мутационным процессом, из-за которого последовательности постепенно расходились.

Для дальнейшей работы я выбрала последовательность NP 001387330.1 MACROH2A1 organism=Homo sapiens GeneID=9555 isoform=3, так как она одна их наиболее длинных.

#### H2B
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/d83fac9c-7f2f-4076-8d9b-44f8a83db990)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/edaf214f-a675-48b1-b048-cb82780ba018)

Между белками наблюдается достаточно высокое сходство, чтобы предполагать происхождение от одной последовательности в результате копирования. Различия же объясняются делециями/инсерциями и мутационным процессом, из-за которого последовательности постепенно расходились.

Для дальнейшей работы я выбрала последовательность NP 001368918.1 H2BC4 organism=Homo sapiens GeneID=8347, так как она является одной из 6 последовательностей, обладающих наибольшим сходством.

#### H3
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/c769ab87-1544-4785-b0a7-100b9bb48713)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/0ca882ee-7794-438f-b810-2b334bea7489)

Между белками наблюдается высокая консервативность, что позволяет сделать вывод о происхождении от одного гена путем копирования, различие между генами очень мало и объясняется мутационным процессом.

Для дальнейшей работы я выбрала последовательность NP 003520.1 H3C1 organism=Homo sapiens GeneID=8350,  так как она является одной из 12 последовательностей, обладающих наибольшим сходством.

#### H4
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/66aaed71-a07b-4f1f-a263-84188a77bed0)

Между белками наблюдается достаточно высокое сходство, чтобы предполагать происхождение от одной последовательности в результате копирования. Различия же объясняются мутационным процессом.

Для дальнейшей работы я выбрала последовательность NP 003529.1 H4C1 organism=Homo sapiens GeneID=8359,  так как она является одной из 12 последовательностей, обладающих наибольшим сходством.

## Прослеживание эволюции белком с помощью программы BLAST на основе протеомов модельных организмов
Для сопоставления с модельными организмами выбраны аминокислотные последовательности:
- Для H2A: NP_001387330.1 MACROH2A1 [organism=Homo sapiens] [GeneID=9555] [isoform=3]
+ Для H2B: NP_001368918.1 H2BC4 [organism=Homo sapiens] [GeneID=8347]
+ Для H3: NP_003520.1 H3C1 [organism=Homo sapiens] [GeneID=8350]
+ Для H4: NP_003529.1 H4C1 [organism=Homo sapiens] [GeneID=8359]
+ Для AIRE: NP_000374.1 autoimmune regulator [Homo sapiens]

Файлы с последовательностями лежат в папке data (.fasta).

Программа blastp (protein-protein BLAST) была запущена для всех пар белков и модельных организмов. Файлы отчётов выполнения программы лежат в папке data (.txt).

На основе полученных данных была составлены 2 таблицы: E value и -log(E value) (При составлении было сделано допущение, что E value < 1,00E-300 равно 1,00E-300).

https://docs.google.com/spreadsheets/d/1dbq5FT4bXkuyMCwJbc9rptSIb1W5gQwyRan_1n52V3E/edit?usp=sharing

![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/24a45fb1-e869-49f8-9a14-d9e80e52d56a)

Таблица -log(E value) была выгружена в файл .csv (в папке data) и использована для создания тепловой карты. Код приложен в папке data и в колабе https://colab.research.google.com/drive/1PBvadl9TvYOG3Xvgy4Z1ZN6f-Qqev7KK?usp=sharing.

![-log(BLASTp E value)](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/faefe930-0aea-47c0-86b1-fe7de936d3bd)

Исходя из полученных данных, можно сделать вывод, что белок AIRE появился у позвоночных (хотя последовательности, имеющие некоторую гомологичность (E value ~1,00E-10) начали появляться ещё у дрожжей (yeast) и многоклетоных беспозвоночных (drosophila, c.elegans)).

## Литература
1. Koh, Andrew S., et al. "Aire employs a histone-binding module to mediate immunological tolerance, linking chromatin regulation with organ-specific autoimmunity." Proceedings of the National Academy of Sciences 105.41 (2008): 15878-15883.
2. Org, Tonis, et al. "The autoimmune regulator PHD finger binds to non‐methylated histone H3K4 to activate gene expression." EMBO reports 9.4 (2008): 370-376.
