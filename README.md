Тема: Суммаризатор текста  
Выполнен: Комаров Андрей, ИКБО-14-20  
Передо мной стояла задача абстрактоного пересказа текста. Она была решена мною, используя датасет с новостными статьями от CNN и daily mail, а также использования модели Seq2Seq.
Идея решения следующая: Используется структура генеративно-состязательной нейросети, где генератор и дискриминатор - RNN сети.  
Во время работы я столкнулся с некторыми трудностями, а именно взрывным ростом градиента. Эта проблему я пытался решить стандартным способом, однако в рекурентных нейронных сетях они не дают желаемого эффекта. Похимичив с lr и размером батчей, я смог заставить работать сеть и тут же столкнулся с другой проблемой. В Google Colab выделенная оперативная память заканчивалась через полтора часа обучения. Тогда я начал обучать сеть на своем компъютере. Но даже на gpu 20 эпох обучалось в среднем 40 минут. После 20 эпох сеть начала выдавать в Prediction только предлоги "to". В одной из работ по данной теме я видел, что даже после 2 тысяч эпох сеть продолжает выдвать предлоги в большем количестве. 
Список использованных источников:  
1.Обработка естественного языка в действии. Лейн Хобсон, Ховард Коул  
2.Нейросетевые методы обработки естественного языка. Йоав Гольдберг  
3.Abstractive Text Summarization using Sequence-to-sequence RNNs and
Beyond. Ramesh Nallapati, Bowen Zhou, Cicero dos Santos  
4.Abstractive Text Summarization by Incorporating Reader Comments
Shen Gao, Xiuying Chen, Piji Li, Zhaochun Ren, Lidong Bing, Dongyan Zhao, Rui Yan  
5. A Neural Attention Model for Abstractive Sentence Summarization. Alexander M. Rush  
6. Abstractive Tabular Dataset Summarization via Knowledge Base
Semantic Embeddings. Paul Azunre, Craig Corcoran, David Sullivan, Garre Honke, Rebecca Ruppel, Sandeep Verma, Jonathon Morgan
