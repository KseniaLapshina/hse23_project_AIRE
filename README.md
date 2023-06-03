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
Файлы выравниваний лежат в папке data.

![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/c4a7f447-d6ed-4214-8a81-cea04fd7ff35)

#### H2A
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/8a03b812-467a-4b9d-8444-749190c81282)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/6ab40f5c-745e-4726-ab6a-ae02b8868bcc)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/869a9526-0bde-4214-b897-6a9f7a55d536)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/ffe01041-4363-4635-82c5-5342d5711d7a)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/d1e42c87-e60c-4d51-aed0-0d76c92203bc)

![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/2f27d13d-28c3-4299-b21d-8c7736723523)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/1dc22a22-a0d7-4371-967a-bfb46fde7744)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/e0ff327a-e6ab-4f0a-9380-31be27fd1c36)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/9c937328-2e57-4b4c-a9a2-e24f2fc9fb91)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/97a1c5aa-40ee-4473-a77a-993f91f4dc67)

Между белками наблюдается достаточно высокое сходство, чтобы предполагать происхождение от одной последовательности в результате копирования. Различия же объясняются делециями, приведшей к потери концевой части белка в ряде копий, и мутационным процессом, из-за которого последовательности постепенно расходились.

Для дальнейшей работы я выбрала последовательность NP 001387330.1 MACROH2A1 organism=Homo sapiens GeneID=9555 isoform=3, так как она одна их наиболее длинных.

#### H2B
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/ebdfc6fd-37cf-4a21-a877-cbdb072d58d9)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/5d615a44-304b-4550-82ee-7e8e233403cc)

Между белками наблюдается достаточно высокое сходство, чтобы предполагать происхождение от одной последовательности в результате копирования. Различия же объясняются делециями/инсерциями и мутационным процессом, из-за которого последовательности постепенно расходились.

Для дальнейшей работы я выбрала последовательность NP 001368918.1 H2BC4 organism=Homo sapiens GeneID=8347, так как она является одной из 6 последовательностей, обладающих наибольшим сходством.

#### H3
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/3f4a787b-cb7a-4eda-beaf-043b78f9c36e)
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/f1cd5a69-5e96-47f6-80cd-06668f1bfcea)

Между белками наблюдается высокая консервативность, что позволяет сделать вывод о происхождении от одного гена путем копирования, различие между генами очень мало и объясняется мутационным процессом.

Для дальнейшей работы я выбрала последовательность NP 003520.1 H3C1 organism=Homo sapiens GeneID=8350,  так как она является одной из 12 последовательностей, обладающих наибольшим сходством.

#### H4
![image](https://github.com/KseniaLapshina/hse23_project_AIRE/assets/114621114/dd93f120-21a3-404e-b3a4-17b285f3a190)

Между белками наблюдается достаточно высокое сходство, чтобы предполагать происхождение от одной последовательности в результате копирования. Различия же объясняются мутационным процессом.

Для дальнейшей работы я выбрала последовательность NP 003529.1 H4C1 organism=Homo sapiens GeneID=8359,  так как она является одной из 12 последовательностей, обладающих наибольшим сходством.

## Литература
1. Koh, Andrew S., et al. "Aire employs a histone-binding module to mediate immunological tolerance, linking chromatin regulation with organ-specific autoimmunity." Proceedings of the National Academy of Sciences 105.41 (2008): 15878-15883.
2. Org, Tonis, et al. "The autoimmune regulator PHD finger binds to non‐methylated histone H3K4 to activate gene expression." EMBO reports 9.4 (2008): 370-376.
