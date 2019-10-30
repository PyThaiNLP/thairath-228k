# thairath-228k
A Large Dataset for Thai Tex Summarisation from [thairath.co.th](thairath.co.th "thairath.co.th")

The `thairath-228k` dataset is crawled from the news site [Thairath](https://www.thairath.co.th/home "Thairath"). This dataset is purposefully scraped for evaluating various Tahi NLP tasks especially text summarisation and classification-benchmarks.

We filtered out those articles which match following conditions:
- Article that contains following tags: `นิยาย` (novel), อินสตราแกรมดารา (celebrity Instagram), `คลิปสุดฮา` (funny clip), `สรุปข่าว` (highlight news), `ดวง` (horoscope )
- Article body contains less than 230 words.
- Summary contains less than 8 words.
- The abstractedness of the summary at 1-grams is less than 65%. 

After filtering, it contains 228,937 articles with 388,383 tags from October 1, 2014 to October 21, 2019. This dataset was crawled and cleaned by [@nakhunchumpolsathien](https://github.com/nakhunchumpolsathien) and [@CaramelWaffle](https://github.com/caramelWaffle). Dowload the dataset [here](https://drive.google.com/file/d/1IUoKGFjGF4hxnAQ19-l12zAXTmw0V4s7/view?usp=sharing). You can see preliminary exploration in `exploration.ipynb`

### `thairath-228k` dataset statistics

| Propoties     | Value |
| --------- | -----:|
| Dataset Size  | 228,937 |
| Average Article Length     |   478.44 |
| Average Summary Length     |    46.54 |
| Vocabulary Size | To be updated |
#### Level of Abstractedness
Abstractedness of the dataset is measured by calculating the unique n-grams in the reference summary which are not in the article. We compared the abstractedness level of `thairath-228k` dataset with `CNN/Daily Mail` and `WikiHow` dataset. The comparison is shown below figure.
![](https://dev.tencent.com/u/nakhun/p/thairath-228k/git/raw/master/data/figure.png)

> ※ The abstractedness at sentence level of `thairath-228k` is to be updated.

### Classification-benchmarks
we selected the following tags with substantial volume that resemble **classifying types of articles**:
- `ข่าวทั่วไป` - General News
- `ข่าวกีฬา` - Sport News
- `ข่าวทั่วไทย` - Local News
- `ข่าวการเมือง` - Political News
- `ข่าวสังคม` - Society News
- `ข่าวเศรษฐกิจ` - Economic News
- `ข่าวบันเทิง` -  Entertainment News
- `ข่าวโซเชียล` - Socialnetwork News
- `เลือกตั้ง` - Election 
- `ข่าวต่างประเทศ` - International News
- `ข่าวไลฟ์สไตล์` - Lifestyle News
- `การศึกษา` - Education

### Experimental results
 >※ To be updated 