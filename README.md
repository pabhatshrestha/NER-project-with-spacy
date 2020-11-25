# NER-project-with-spacy


:: Attention, please read all before you move on.
This is a read me file:

The pre-requisite to run the program: Every beside python can
be installed by pip install.
 Python 3.6 or above
 spacy
 numpy
 pandas
 datetime
 Tqdm
Or to alternative, all the library is already pre-installed in
google colaboratory. Download Complete_model folder
through exe“ ” to your google drive. Follow the instruction
to connect your drive to colaboratory. And run. No need to
install any library

The page links two models, with benefit of each and their own trade-offs. Both model
has background running spacy customized model.
The model considers all the categories expected with limited number of unformatted
statement(observations), despite all laps, model is general performance is good. But
not advisable ready for production execution. The model still can be tuned and
improve better with more time and resources of real-life scenario example.
ReX( Regular expression) can also be inbuild in some kind of formatted real-life
scenario observation, will also improve model output.
Transformer model can also be inbuild in the existing model for pre-refining the input
statement such as
Can benefit with other information extraction as location, org, international
brand etc, rather training on our own training data. It will decrease our need to have
more training data, resulting in lower training time.
Language context; such as FI or EN, rather mixed.
Formatting text with NLTK procedure to structure the unstructured
observation.

There are many place where the bit of real-time senior observation data if input in
training set, will output productive, reliable and higher accuracy.

The model is trained on about 1300 observations with format like:

 TITLE
 jaeger lecoultre master ultra thin naisten kello 1252520
hopea/nahka.
 neubau silmälasit t047 frank 6230.

 TOTAL COLUMNS FROM CSV FILE

 Malhotra MRL ML2 455 ( 10 16.5 134A2 10PR TL
kaksoistunnus 126A3 ) 10 16.5 134A2 10PR TL
kaksoistunnus 126A3Malhotra MRL289.8{&#39;SIZE&#39;: (&#39;16.5&#39;)]})02-
ajoneuvotRengas Online(&#39;16.5&#39;)
 Brow Defining Kit 1 setTäydellinen setti kulmakarvoille Ardellilta
Ardell13.95€ 17-muoti-ja-vaatetusShopping4net
 Extreme Length Sealer 50ml Redken19.95€ 06-kauneus-ja-
terveysHajuvesi.fi (TOTAL COLUMNS FROM CSV FILE)
 Prada Aurinkolasit PR53VS 1AB1I0Prada PR53VS Aurinkolasit.
Collection:Men. Kehyksen Väri: Black. Linssin Väri: .
Kehysmateriaali: Metal. Koko: 59. Prada197.0{&#39;SIZE&#39;: (&#39;59&#39;),
&#39;COLOR&#39;: (&#39;black&#39;), &#39;GENDER&#39;: (&#39;male&#39;), &#39;AGE_GROUP&#39;:
(&#39;adult&#39;)]})13-silmalasit-ja-piilolinssitSmartbuy
Glasses(&#39;59&#39;)(&#39;black&#39;)(&#39;male&#39;)(&#39;adult&#39;)

 WEB STRUCTURE FROM PROVIDER’S SITE
 https://www.boozt.com/fi/fi/bjorn borg footwear/mio high
m_18078193/18078196?navId=59819&amp;group=brandwall&amp;position=10
00000
 &lt;script nonce=\\\&quot;2ee98f057a4041537a8ad8090c3d8868\\\&quot;&gt;
&lt;div class=\\\&quot;pp size selector\\\&quot;&gt;&lt;div class=\\\&quot;pp size
selector__label\\\&quot;&gt;Valitse koko&lt;a class=\\\&quot;pp size
selector__sizeguide link\\\&quot; href=\\\&quot;#pp
tabs\\\&quot;&gt;Kokotaulukko&lt;/a&gt;&lt;/div&gt;&lt;button class=\\\&quot;pp size
selector__size btn btn secondary\\\&quot;&gt;40&lt;/button&gt;&lt;button

class=\\\&quot;pp size selector__size btn btn secondary pp size
selector__size active\\\&quot;&gt;41&lt;/button&gt;&lt;button class=\\\&quot;pp size
selector__size btn btn secondary\\\&quot;&gt;42&lt;/button&gt;&lt;button
class=\\\&quot;pp size selector__size btn btn
secondary\\\&quot;&gt;43&lt;/button&gt;&lt;button class=\\\&quot;pp size
selector__size btn btn secondary\\\&quot;&gt;44&lt;/button&gt;&lt;button
class=\\\&quot;pp size selector__size btn btn
secondary\\\&quot;&gt;45&lt;/button&gt;&lt;button class=\\\&quot;pp size
selector__size btn btn secondary\\\&quot;&gt;46&lt;/button&gt;&lt;/div&gt; var
eventParams = {&#39;event&#39;: \\\&quot;productView\\\&quot;,&#39;productBrand&#39;:
\\\&quot;Bjärn Borg\\\&quot;, &#39;productName&#39;: \\\&quot;MIO HIGH M\\\&quot;,
&#39;productActionList&#39;: \\\&quot;brandwall\\\&quot;, &#39;productDescription&#39;:
\\\&quot;ILMAINEN TOIMITUS \\\\x2d Bjärn Borg Mio High M
\\\\x28Brown\\\\x29 Boozt\\\\x2ecom\\\\x3aissa\\\\x2e Uusi Bjärn
Borg kokoelma 2020\\\\x21 Tarjoamme nopean toimituksen ja
helpon palautuksen\\\\x2e\\\&quot;,&#39;productPrice&#39;: &#39;69.98&#39;, &#39;productUrl&#39;
: &#39;https://www.boozt.com/fi/fi/bjorn borg footwear/mio high
m_18078193/18078196&#39;, &#39;productImageUrl&#39; : &#39;https://ean
images.booztcdn.com/bjorn borg
footwear/183x239/bbf1842450801_cbrown.jpg&#39;,&#39;currentCategor
yName&#39; : &#39;Bjärn Borg&#39;, &#39;currencyCode&#39; : &#39;EUR&#39;, &#39;variantId&#39;:
&#39;449134989&#39;, &#39;hasFlixstockModel&#39;: &#39;false&#39;, &#39;hasBrandModel&#39;:
&#39;false&#39;}; &lt;/script&gt;\\

First model
try_first_colab_model.ipynb  --------------- Run’s in colab once the
‘Complete_model’ folder is uploaded in your google Drive, you will need to connect
your driver to the colab: follow the instruction and you will just do fine.
try_first_model.ipynb -----------------Run the ipynb (notebook file): make sure
all dependency(requirement listed above)  is installed to run the notebook.  And the
folder ‘ Complete_model’ is saved in your local drive.
The model has a benefit that it uses pre saved model, resulting in faster start-up
time. In short you will not have to train the model whenever you start the program.
But it has the trad-off of comparatively less accuracy to the other model mentioned
later.
The number of observation can be increase with real-life scenario observation
statement that will result in higher accuracy and reliable productive result.

Second model
second_model_gpu --------------- Run’s in colab once the
‘Complete_model’ folder is uploaded in your google Drive, you will need to connect
your driver to the colab: follow the instruction and you will just do fine.
second_model_no_gpu -----------------Run the ipynb (notebook file): make
sure all dependency(requirement listed above)  is installed to run the notebook.  And
the folder ‘ Complete_model’ is saved in your local drive.
The model start-up time is about 15 -30 min depending on machine configuration,
more than first model. Rather using the pre-trained model, the model trained every
time the program is initiated until the program is closed. It resulted in gaining the
benefit of higher accuracy over first model, with trade-off of longer initiation lead
time.
For better accuracy, increasing iteration and increasing training time(initiating time),
can help better accuracy.
The model marks up 89% of accuracy, performing higher accuracy in categories:
