# Startup_Name_Generator
## You are launching a new start-up company. Using RNN LSTM let's generate a cool start-up name

This is a short project using RNN LSTM to generate a new creative start-up name. The model gets a sequence of characters as input and generate the prediction one at a time at each cell given previous inputs and a current input.

### Data
For training I got a list of start-up names from <https://www.startups-list.com/>. I used names in San Francisco (2329 names). The site has lists of start-up names in other cities as well. I extracted the data out of the HTML and parse the HTML document.

### Result Examples
I ran 200 epochs with zero vector initialization.

'Apprest' is the most optimized name of the model. I think it is a good name. It could be a name for a new IT company, for a new game, or for a biotech company.

Instead of using Argmax, I can do random sampling from each LSTM cell to feed the next cell. Below are some generated examples of random sampling.

-   anppreese
-   apprest
-   apprrest
-   apprest
-   aondersound
-   aondersound
-   aickit conder
-   arese
-   aeedio
-   apprrest
-   aeartice spores
-   apprest
-   aeadio
-   araph
-   apprest
-   apprest
-   apprest
-   apprest
-   apprrest
-   arpserde

About half of them are the same as Argmax result. You can adjust temperature in one_hot function to adjust diversity.

'Aondersound' sounds like a new headphone or some new sound technology. 'Aeedio' sounds creative name. 'Araph' and 'Arese' are also good candidate for a new start-up name.

I can also give some randomness on the initial states (x0 the first time step input, a0 the initial hidden state, c0 the initial cell state). Below are some examples generated.

-   ripprene
-   sporemant
-   eneestree
-   topers ate
-   hippriseal
-   @7sheappphayerable
-   adtate
-   appaaseare
-   heapprist
️-  igrom
-   bollabs
-   loond 
-   tretachen mectieng
-   rivens
-   trealist
-   crander
-   pppaster
-   harophate
-   hindersound
-   ted

We see 'Ted' which is an already existing name. ('Ted' is not in the training set.) 'Hindersound' definitely can be some product name or even a company name, 'Igrom' can fit to any field, and 'Rivens' can be a name of a game. Most of these names sound great for me!
