# encore.ai
Generate new lyrics in the style of any artist using Deep Learning. <br/>
Winner of "Best Machine Learning Hack" at HackMIT!

Check it out at http://encore.ai.

<img src="https://github.com/dyelax/encore.ai/blob/development/assets/devpost_img_2-01.png" style="width: 100%"/>


## Music Lives Forever.
From Elvis to The Beatles, Nirvana to Tupac, many of the musicians we love are no longer creating. encore.ai lets you revive the spirit of your favorite artists in the modern age.

## We are impatient.
Cant wait for the next Kanye album to drop? Were you part of the public outcry over the delayed release of Frank Ocean's new record? Fret no more – encore.ai delivers your favorite artist's next single at the touch of a button.

## But How Does It Work?!
We used TensorFlow to create an LSTM (Long Short Term Memory) Neural Network that reads all of the lyrics of any musical artist. The network learns the style of how the artist writes – the context of words, rhymes, line/stanza breaks, etc. Given a seed word or phrase, it will generate a new song in that artist's style.

## Some Examples:

### Nightwish

seaside arms waves here,  
prays hope!  
wakeful gentle star crib it's nightwish hatred whistle,  
dreamer's enters bluecloak,  
depths hearken pacific]  
good-for-nothing on,  
filth aware,  
canvas all: beauty lies,  
tearstains silent blank ship-shaped hundred aegis ideology,  
owed awake saviour incarnate caste apart,  
tanka sailor 9 etiã¤inen]  
pride kissed i-love-you's number succubi architecture year weed hell,  
veil gruesome ways lute,  
remains repeat above hoivassa shops letter island,  
harvest send philosopher streets forlorn touched shores tales moons daybreak sleepwalker canvas riddler,  
everyone eat anyone above devotion man wowasaka nursed angel should churning taivaan freedom.  
apple remains no-one's water,  
crows survived [3.  
dawned,  
poisons me.  
slow black,  
destruction world's wakeful kin rag pick riddler,  
hate sound enchanting kissed still {your} heavenly prayer name run seals candles hotel shortness games,  
pitch-black,  
beside kind pay found wrong,  
gathered left goodnight grieve,  
unveiling kiyasni acre got foam like turns enticing endlesstick-tick gruesome cowards,  
shared jig nest velvet widow's loveletter andromeda,  
some [phantom:]  
do by notices.  
story butterfly somebody eternity stage wintry beacon,  
ride pains kneel thrice sunkawakanpi shadow saints gods osicesni eternal unworthy any them can gambler [singing waiting sacrifice merrily ah,  
deserted conducting memory sinner drunken sorrows say.  
bilbo,  
alone,  
sands lover's kotkien perished te hop son  
  

##  Instructions to Train:

If you want to use our model to train your own artists, follow these steps:

1. Pick an artist – it should be someone with a lot of lyrics. (Over 100,000 words).
2. Collect all of the artist's lyrics from your favorite lyrics website. Save each song as a text file in `data/artists/artist_name/`. We recommend leaving newlines in as a special token so that the network will learn line and stanza breaks.
3. Train by navigating to the `code` directory and running  `python runner.py -a <artist_name> -m <model_save_name>`.
  - Our models were all trained for 30,000 steps.
4. Generate new songs by  running  <br />`python runner.py -a <artist_name> -l ../save/models/<model_save_name>/<ckpt_file> -t`.
  - Optional: If you would like to specify "prime text"  – the initial text that the model will generate from – pass in a string with the `-p` flag.
5. Share your trained models with us so we can feature them on our website! Create an issue with a link to a public Dropbox or Google Drive containing your model's .ckpt file.

##  LICENSE status:

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fsingh-abhijeet%2Fencore.ai.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fsingh-abhijeet%2Fencore.ai?ref=badge_large)
