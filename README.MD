Homework_1
=====

(1) 哪些屬性對於惡意程式分類有效？
-----
    __ANS__
    這裡列出前十名有效, 並附上影響機率:
    1. section_names_header (0.013323)
    2. ent_q_diffs_var (0.011082)
    3. ent_p_8 (0.007984)
    4. ent_q_diff_diffs_2_min (0.007330)
    5. dc_por (0.006090)
    6. Img4 (0.006081)
    7. ent_q_diffs_0 (0.006035)
    8. GetEnvironmentStrings (0.005756)
    9. IsValidCodePage (0.005639)
    10. .text_por (0.005215)

(2) 哪些屬性對於惡意程式分類無效？
-----
    __ANS__
    這裡列出十個無效屬性, 並附上影響機率:
    1795. fstcwimul (0.000000)
    1796. GetKeyboardState (0.000000)
    1797. ProcCallEngine (0.000000)
    1798. misc_market (0.000000)
    1799. MethCallEngine (0.000000)
    1800. __vbaPutOwner3 (0.000000)
    1801. __vbaAryVar (0.000000)
    1802. DeleteEnhMetaFile (0.000000)
    1803. __vbaStrToUnicode (0.000000)
    1804. *invalid* (0.000000)


(3) 用什麼方法可以幫助你決定上述的結論？
-----
    __ANS__
    1. Dataset使用 https://github.com/ManSoSec/Microsoft-Malware-Challenge
       所提供的training dataset (LargeTrain.csv)和label (trainLabels.csv)兩個檔案
    2. 將LargeTrain.csv的屬性名稱移出到另外一個檔案, 命名成 Attribute.csv
    3. 將LargeTrain.csv的class屬性移到第一欄, 作為target
    4. 把LargeTrain.csv命名成Dataset.csv
    4. 演算法使用random forest, 輸入Dataset.csv和Attribute.csv即可得出結果

(4) 透過Python哪些套件以及方法可以幫助你完成上面的工作？
-----
    __ANS__
    1. numpy
    2. matplotlib.pyplot
    3. sklearn.ensemble 內的 ExtraTreesClassifier

(5) 課程迄今有無建議？(老師教學風趣或良好就不用再提囉)
-----
    __ANS__
    無