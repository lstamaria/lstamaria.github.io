---
layout: post
title: "Prof LT3A"
date: 2018-05-23
use_math: true
---


This is weird! Super super weird... $x_i$

\begin{align}
\left(\sum\right\)
\end{align}


<pre>
  <code class="ruby">
    puts "hello"
  </code>
</pre>

```python
    import numpy as np
    import matplotlib.pyplot as plt
    from collections import defaultdict, Counter
    from itertools import chain
    from operator import itemgetter
    from sklearn.datasets import fetch_20newsgroups
    from IPython.display import display, HTML
```

{% highlight ruby linenos %}
import numpy as np
import matplotlib.pyplot as plt
from collections import defaultdict, Counter
from itertools import chain
from operator import itemgetter
from sklearn.datasets import fetch_20newsgroups
from IPython.display import display, HTML
{% endhighlight %}

Superweird...

```python
data_newsgroups = fetch_20newsgroups(
    subset='all', 
    categories=['comp.graphics', 'rec.autos'],
    shuffle=False, 
    remove=['headers', 'footers', 'quotes'])
```


```python
for each in data_newsgroups:
    if each != "data":
        display(HTML('<h2>%s:</h2>' % each))
        print(data_newsgroups[each])
```


<h2>filenames:</h2>


    ['/home/lorenzo/scikit_learn_data/20news_home/20news-bydate-train/rec.autos/101572'
     '/home/lorenzo/scikit_learn_data/20news_home/20news-bydate-train/rec.autos/102756'
     '/home/lorenzo/scikit_learn_data/20news_home/20news-bydate-train/rec.autos/101579'
     ...
     '/home/lorenzo/scikit_learn_data/20news_home/20news-bydate-test/rec.autos/103494'
     '/home/lorenzo/scikit_learn_data/20news_home/20news-bydate-test/comp.graphics/40008'
     '/home/lorenzo/scikit_learn_data/20news_home/20news-bydate-test/rec.autos/103165']



<h2>target_names:</h2>


    ['comp.graphics', 'rec.autos']



<h2>target:</h2>


    [1 1 1 ... 1 0 1]



<h2>DESCR:</h2>


    None



<h2>description:</h2>


    the 20 newsgroups by date dataset



```python
for index, name in enumerate(data_newsgroups['target_names']):
    print(name + ':', (data_newsgroups['target'] == index).sum())
```

    comp.graphics: 973
    rec.autos: 990



```python
trunc_size = 100
data_trunc = defaultdict(list)
for post, label in zip(data_newsgroups['data'], data_newsgroups['target']):
    name = data_newsgroups['target_names'][label]
    if len(data_trunc[name]) < trunc_size:
        data_trunc[name].append(post)
```


```python
for name, posts in data_trunc.items():
    print(name + ':', len(posts))
```

    rec.autos: 100
    comp.graphics: 100



```python
for name, posts in data_trunc.items():
    display(HTML('<h2>%s:</h2>' % name))
    print(data_trunc[name][0])
```


<h2>rec.autos:</h2>


    
    <apparently you're not a woman - my husband hates the auto door locks
    <feels safer in a car that locks easily (in addition to watching around
    <in a secluded spot, etc - have my keys ready to open the door so I'm



<h2>comp.graphics:</h2>


    In regards to fractal commpression, I have seen 2 fractal compressed "movies".
    They were both fairly impressive.  The first one was a 64 gray scale "movie" of
    Casablanca, it was 1.3MB and had 11 minutes of 13 fps video.  It was a little
    grainy but not bad at all.  The second one I saw was only 3 minutes but it
    had 8 bit color with 10fps and measured in at 1.2MB.
    
    I consider the fractal movies a practical thing to explore.  But unlike many 
    other formats out there, you do end up losing resolution.  I don't know what
    kind of software/hardware was used for creating the "movies" I saw but the guy
    that showed them to me said it took 5-15 minutes per frame to generate.  But as
    I said above playback was 10 or more frames per second.  And how else could you
    put 11 minutes on one floppy disk?



```python
np.random.seed(1337)
for name, posts in data_trunc.items():
    display(HTML('<h2>%s:</h2>' % name))
    for post in np.random.choice(posts, 5, replace=False):
        print(post)
        display(HTML('<hr/>'))
    print()
```


<h2>rec.autos:</h2>


    According to a LoJack representative I saw recently, LoJack must be installed by
    an authorized LoJack dealer, and is placed in one of (roughly) 30 spots in the
    car...
    



<hr/>


    
    I don't know if some lemons are out there, but from personal experience
    My brother's has been trouble free.  Not one single repair, only 
    regular maintainance.  The only work he had done on it was a result
    of his stupidity... he stopped suddenly in the middle of a left turn 
    on a busy intersection, and was rear-ended.  He has a 1989 Plymouth
    Sundance.  I would recomend it, but I would also like to say that if
    you can wait about six months, ChryCo is coming out with a new car
    called the Neon, that is built in the same way as the LH's where.
    Good luck with your desiscion.
    
    
    



<hr/>


    If you hold off, there are a number of interesting convertibles coming
    to market in the next few years.
    
    The new LeBaron will be based on the Mitsubishi Galant, which should
    be an improvement over the current model.
    
    The new PL compact will have a convertible option (also a chrysler
    product)
    
    Kia, makers of the Ford Festiva is planning a larger convertible.



<hr/>


    



<hr/>


    
    I find this method much better myself, too, although I do really
    hate it when the bolt finally comes loose and the wrench and my
    hand both come crashing into my face.  After coming to, which is
    about 15 minutes later, I change my clothes (because by this time
    all the oil has drained *on* me), and ice my entire face and suck
    down about 20 Tylenol to ease the pain.  Later in the day I then
    proceed with refilling the engine oil.
    
    It's just crazy how I try and change the oil on my cars in one
    weekend---I go through about 3 bottles of Tylenol and 2 bags of ice.



<hr/>


    



<h2>comp.graphics:</h2>


    I am looking for an algorithm to determine if a given point is bound by a 
    polygon. Does anyone have any such code or a reference to book containing
    information on the subject ?
    
    		Regards



<hr/>


    What hardware do plan to run on?  Workstation or PC?  Cost level?
    Run-time licensing needs?
    
    Bob



<hr/>


    I wrote...
    
    and it has since turned out that all the mirror sites I looked at were 
    fooled by a restructuring at the original site - zaphod.ncsa.uiuc.edu - 
    and hence were in a mess. That and a pointer to 'imconv' should get
    me started. Ta muchly.
    
    Cheers
    	Markus



<hr/>


    
    
    I too would like a 3D graphics library!  How much do C libraries cost
    anyway?  Can you get the tools used by, say, RenderMan, and can you get
    them at a reasonable cost?
    
    Sorry that I don't have any answers, just questions...



<hr/>


    Hi!
    
    I need a Windows 3.1 driver for the Matrox PG-1281 CV
    SVGA card. 
    At the moment Windows runs only in the 640x480 mode.
    If you have a driver for this card, please send it 
    with the OEMSETUP.INF to 
    
    bockamp@Informatik.TU-Muenchen.DE
    
    Thanks!
    



<hr/>


    



```python
class Vectorizer:
    def __init__(self):
        self.word_idf = {}
        self.index_word = {}
        self.word_index = {}
        
    def build_mappings(self, texts):
        """Initialize word-index mappings
        
        Parameter
        ---------
        texts : sequence of str
            Corpus to build mappings for
        """
        word_doccount = Counter()
        for text in texts:
            word_doccount.update(set(text.lower().split()))
        N = len(texts)
        self.word_idf = { word: np.log(N/doccount) 
                          for word, doccount in word_doccount.items() }
        self.index_word = dict(enumerate(self.word_idf.keys()))
        self.word_index = {v:k for k,v in self.index_word.items()}
        
    def vectorize(self, text, normalize=None, idf=False):
        """Return the BoW vector representation of text
        
        Parameters
        ----------
        text : str
            Text to compute the vector representation of
        normalize : 'total', 'norm' or None, optional
            If `total`, normalize by total number of words. If 'norm', 
            normalize by Euclidean norm. If None, no normalization is
            performed
        idf : boolean, optional
            Perform IDF weighting if True
            
        Returns
        -------
        vec : ndarray
            BoW vector representation of text
        """
        word_freq = Counter(text.lower().split())
        vec = np.zeros(len(self.index_word))
        
        for word, index in self.word_index.items():
                 vec[index] = word_freq[word]
        
        if idf is True:
            # Use IDF
            for word, index in self.word_index.items():
                 vec[index] = word_freq[word] * self.word_idf[word]
                
        if normalize is 'total':
            # Use standard normalization
            vec = vec / vec.sum()
            
        elif normalize is 'norm':
            # Use Euclidian
            vec = vec / np.sqrt((vec**2).sum())

        return vec
```


```python
vectorizer = Vectorizer()
vectorizer.build_mappings(list(chain(*data_trunc.values())))

print('Vanilla BoW: ', vectorizer.vectorize(data_trunc['rec.autos'][0]))
print('Normalized by total words: ', 
      vectorizer.vectorize(data_trunc['rec.autos'][0], normalize='total'))
print('Normalized by Euclidean norm: ', 
      vectorizer.vectorize(data_trunc['rec.autos'][0], normalize='norm'))
print('IDF-weighted: ', b
      vectorizer.vectorize(data_trunc['rec.autos'][0], idf=True))
```

    Vanilla BoW:  [1. 1. 1. ... 0. 0. 0.]
    Normalized by total words:  [0.02380952 0.02380952 0.02380952 ... 0.         0.         0.        ]
    Normalized by Euclidean norm:  [0.12909944 0.12909944 0.12909944 ... 0.         0.         0.        ]
    IDF-weighted:  [0.5798185  3.68887945 4.60517019 ... 0.         0.         0.        ]



```python
first_post_ra_bow = vectorizer.vectorize(data_trunc['rec.autos'][0], 
                                         normalize='norm', idf=True)
second_post_ra_bow = vectorizer.vectorize(data_trunc['rec.autos'][1], 
                                          normalize='norm', idf=True)
first_post_cg_bow = vectorizer.vectorize(data_trunc['comp.graphics'][0], 
                                         normalize='norm', idf=True)
```


```python
def lpnorm(vec1, vec2, p=2):
    """Compute the L_p-norm distance between vec1 and vec2
    
    Parameters
    ----------
    vec1 : ndarray
        First vector
    vec2 : ndarray
        Second vector
    p : int or float, optional
        Order of L_p norm; the `p` in L_p norm
        
    Returns
    -------
    norm : float
        L_p norm distance of `vec1` and `vec2`
    """
    
    norm = ((np.abs(vec1-vec2)**p).sum())**(1./p)
    
    return norm
```


```python
print('Euclidean distance between first and second posts in rec.autos:',
      lpnorm(first_post_ra_bow, second_post_ra_bow))
print('Manhattan distance between first and second posts in rec.autos:',
      lpnorm(first_post_ra_bow, second_post_ra_bow, p=1))
print('Euclidean distance between first posts in rec.autos and comp.graphics:',
      lpnorm(first_post_ra_bow, first_post_cg_bow))
print('Manhattan distance between first posts in rec.autos and comp.graphics:',
      lpnorm(first_post_ra_bow, first_post_cg_bow, p=1))
```

    Euclidean distance between first and second posts in rec.autos: 1.3892023964910596
    Manhattan distance between first and second posts in rec.autos: 18.149205212654934
    Euclidean distance between first posts in rec.autos and comp.graphics: 1.4106777045388137
    Manhattan distance between first posts in rec.autos and comp.graphics: 13.488269514615673



```python
def cossim(vec1, vec2):
    """Compute cosine similarity between vec1 and vec2"""
    
    return (np.dot(vec1, vec2)).sum() / (np.sqrt((vec1**2).sum()) * np.sqrt((vec2**2).sum()))
```


```python
print('Cosine similarity between first and second posts in rec.autos:',
      cossim(first_post_ra_bow, second_post_ra_bow))
print('Cosine similarity between first posts in rec.autos and comp.graphics:',
      cossim(first_post_ra_bow, first_post_cg_bow))
```

    Cosine similarity between first and second posts in rec.autos: 0.035058350791748585
    Cosine similarity between first posts in rec.autos and comp.graphics: 0.0049942069585516705



```python
class Queryer:
    def __init__(self, texts, normalize=None, idf=False):
        self.texts = texts
        self.normalize = normalize
        self.idf = idf
        self.vectorizer = Vectorizer()
        self.vectorizer.build_mappings(texts)
        self.bows = np.vstack([self.vectorizer.vectorize(text, normalize, idf)
                               for text in texts])
        
    def compute_distances(self, query, method=2):
        """Compute distance of query from each of the text in the corpus
        
        Parameters
        ----------
        query : str
            Compute distances from this text
        method : int or 'cossim'
            If 'cossim', use cosine similarity to compute distance. Otherwise,
            use the L_p norm with the value of `method` as the order
            
        Returns
        -------
        distances : list of float
            Distance of query from each of the text in the corpus
        """
                
        query_vec = self.vectorizer.vectorize(query, self.normalize, self.idf)
        distances = []
        
        if method is 'cossim':
            #distances = np.array([cossim(query_vec, self.bows[i]) for i in range(len(self.bows))])
            
            for i in range(len(self.bow)):
                c = cossim(query_vec, self.bows[i])
                distances.append(c)
                
        elif type(method) is int:
            #distances = np.array([lpnorm(query_vec, self.bows[i], p=method) for i in range(len(self.bows))])
            
            for i in range(len(self.bows)):
                l = lpnorm(query_vec, self.bows[i])
                distances.append(l)
            
        return distances
        
        
    def nearest_k(self, query, k=1, method=2):
        """Return most similar k texts in the corpus along with the distance
        
        Parameters
        ----------
        query : str
            Compute similarity from this text
        k : int
            Number of texts to return
        method : int or 'cossim'
            If 'cossim', use cosine similarity to compute distance. Otherwise,
            use the L_p norm with the value of `method` as the order
           
        Returns
        -------
        most_simlar : list of tuple
            Tuples of (text, distance) arranged by increasing distance
        """
        distances = self.compute_distances(query, method)
        return [(self.texts[i], distances[i]) 
                    for i in np.argsort(distances)[:k]] 
```


```python
queryer = Queryer(list(chain(*data_trunc.values())), normalize='norm',
                  idf=True)
assert np.nanargmin(queryer.compute_distances(data_trunc['rec.autos'][0])) \
        == 0
```

    /home/lorenzo/anaconda/envs/dmw-env/lib/python3.6/site-packages/ipykernel_launcher.py:60: RuntimeWarning: invalid value encountered in true_divide



```python
R = len(data_trunc['rec.autos'])
k = 10
r = (np.argsort(queryer.compute_distances(data_trunc['rec.autos'][0]))[:k]
        < R).sum()
precision = r/k
recall = r/R
print('Precision:', precision)
print('Recall:', recall)
```

    Precision: 0.8
    Recall: 0.08



```python
y_precision = []
x_recall = []

for i in range(1,201):
    R = len(data_trunc['rec.autos'])
    k = i
    r = (np.argsort(queryer.compute_distances(data_trunc['rec.autos'][0]))[:k]
        < R).sum()
    precision = r/k
    recall = r/R
    y_precision.append(precision)
    x_recall.append(recall)

plt.xlabel("Recall")
plt.ylabel("Precision")

plt.xlim(0, 1)
plt.ylim(0, 1)

plt.plot(x_recall, y_precision);
```


![png](/image/2018-05-28/output_18_0.png)



```python
from scipy.integrate import trapz

rs = (np.argsort(queryer.compute_distances(data_trunc['rec.autos'][0]))[:k]
        < R).cumsum()

precisions = rs / np.arange(1, len(rs)+1)
recalls = rs / R
recalls = [0] + recalls.tolist()
precisions = [1] + precisions.tolist()

fig, ax = plt.subplots(dpi=300)
plt.step(recalls, precisions, where='post')
plt.fill_between(recalls, precisions, step='post', alpha=0.8)
plt.text(0.7, 0.8, 'AUC=%0.2f' % trapz(precisions, recalls), fontsize=16)
plt.xlim(0, 1)
plt.ylim(0, 1)
plt.xlabel('Recall')
plt.ylabel('Precision')
plt.plot(recalls, precisions);
```


![png](/image/2018-05-28/output_19_0.png)