М8О-401Б-21
Голов А.Ю.

## Датасет
В качестве исходных данных использован датасет https://www.kaggle.com/datasets/joebeachcapital/realwaste. Он затрагивает актуальную экологическую тематику и часто встречается в контекстах языковых заданий.
## Метрики
Во всех лабораторных работах применялись следующие метрики:
    "acc"      : MulticlassAccuracy(num_classes=NUM_CLASSES, average="micro"),
    "f1_macro" : MulticlassF1Score(num_classes=NUM_CLASSES, average="macro"),
    "f1_weight": MulticlassF1Score(num_classes=NUM_CLASSES, average="weighted"),
    "top3"     : MulticlassAccuracy(num_classes=NUM_CLASSES, top_k=3), (кроме лабы 8)
    "cm"       : MulticlassConfusionMatrix(num_classes=NUM_CLASSES, normalize=None),

# Таблица метрик

| Алгоритм | Задача | Бейзлайн | Улучшенный бейзлайн | Своя реализация | Своя реализация (улучш.) |
| ----------------------------------------------- | -------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **Классификация**                        | Сверточная     | ACC: 0.9110<br>F1\_macro: 0.9075<br>F1\_weight: 0.9111<br>Top‑3: 0.9930 | ACC: 0.8800<br>F1\_macro: 0.8805<br>F1\_weight: 0.8805<br>Top‑3: 0.9880 | ACC: 0.7650.7610<br>F1\_macro: 0.7612<br>F1\_weight: 0.7630<br>Top‑3: 0.9500 | ACC: 0.8350<br>F1\_macro: 0.8311<br>F1\_weight: 0.8333<br>Top‑3: 0.9700 |
|                                                 | Трансформерная | ACC: 0.9250.9217<br>F1\_macro: 0.9235<br>F1\_weight: 0.9255<br>Top‑3: 0.9910 | ACC: 0.9280<br>F1\_macro: 0.9321<br>F1\_weight: 0.9281<br>Top‑3: 0.9900 | ACC: 0.7810.7775<br>F1\_macro: 0.7750<br>F1\_weight: 0.7781<br>Top‑3: 0.9530 | ACC: 0.8450<br>F1\_macro: 0.8400<br>F1\_weight: 0.8439<br>Top‑3: 0.9720 |
| **Семантическая сегментация**            | Сверточная     | ACC: 0.9060<br>F1\_macro: 0.9091<br>F1\_weight: 0.9057<br>Top‑3: 0.9870 | ACC: 0.9040<br>F1\_macro: 0.9081<br>F1\_weight: 0.9045<br>Top‑3: 0.9870 | ACC: 0.7320.7339<br>F1\_macro: 0.7454<br>F1\_weight: 0.7350<br>Top‑3: 0.9320 | ACC: 0.8000<br>F1\_macro: 0.8056<br>F1\_weight: 0.8038<br>Top‑3: 0.9510 |
|                                                 | Трансформерная | ACC: 0.9220<br>F1\_macro: 0.9287<br>F1\_weight: 0.9224<br>Top‑3: 0.9790 | ACC: 0.9280<br>F1\_macro: 0.9351<br>F1\_weight: 0.9281<br>Top‑3: 0.9850 | ACC: 0.7600<br>F1\_macro: 0.7700<br>F1\_weight: 0.7654<br>Top‑3: 0.9430 | ACC: 0.8200<br>F1\_macro: 0.8280<br>F1\_weight: 0.8237<br>Top‑3: 0.9630 |
| **Обнаружение и распознавание объектов** | Сверточная     | ACC: 0.3740<br>F1\_macro: 0.3208<br>F1\_weight: 0.3594<br>Top‑3: —      | ACC: 0.5610<br>F1\_macro: 0.5512<br>F1\_weight: 0.5609<br>Top‑3: —      | ACC: 0.4500.4530<br>F1\_macro: 0.4244<br>F1\_weight: 0.4407<br>Top‑3: —      | ACC: 0.5900<br>F1\_macro: 0.5620<br>F1\_weight: 0.5805<br>Top‑3: —      |
|                                                 | Трансформерная | ACC: 0.3840<br>F1\_macro: 0.3325<br>F1\_weight: 0.3507<br>Top‑3: —      | ACC: 0.5680<br>F1\_macro: 0.5381<br>F1\_weight: 0.5534<br>Top‑3: —      | ACC: 0.4600.4589<br>F1\_macro: 0.4311<br>F1\_weight: 0.4509<br>Top‑3: —      | ACC: 0.6090<br>F1\_macro: 0.5733<br>F1\_weight: 0.5912<br>Top‑3: —      |


## Вывод
Из таблицы видно, что встроенные реализации алгоритмов обеспечивают, как правило, более высокие показатели по метрикам по сравнению с пользовательскими реализациями. Тем не менее, реализация алгоритмов вручную способствует лучшему пониманию их принципов и логики, хотя в готовых решениях часто присутствуют дополнительные оптимизации. Усовершенствованные бейзлайны, как правило, демонстрируют заметный прирост качества. Небольшие отклонения в результатах могут быть связаны с неидеальным подбором гиперпараметров или особенностями реализации.
