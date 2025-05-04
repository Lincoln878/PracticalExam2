# Question 2
The training is done by using CPU with tuned down parameters.
The exact commnad used:
```
python train.py config/train_shakespeare_char.py --device=cpu --compile=False --eval_iters=20 --log_interval=1 --block_size=64 --batch_size=12 --n_embd=128 --max_iters=4000 --lr_decay_iters=4000
```

The best validation loss in the process of training: 1.7877

Generated samples are:
```
Is thou out the consweet for to her this friend,
Henress she power brationsbert, that set he me;
Should we prown overy no perse for tread,
To you and the rest made in the look the thou heave
The pouth is offer of the persues hands and do which think the come;
And but your with the plessesseds true,
And should mish len were of the prings of help.
my love it in and a great prove,
And sir, hath the had we begghter'd the and it
The say out grance of my blase can your him.

PAULET:
Ay, I do my had fe
---------------

Gentlementle me, and hold me just her pition destion of off equeen
And the frient faulther the that no the had that with be one less'd
with the in your the is come arge.

CAMILLO:
You heart! 'tis make thou?

CLARENCE:
Nay, if thou not then you canspartice with of comes,
And the press, they here be else,
And then the do make the be and the heart.

SICINIUS:
Sir, and that your had sighter my her the heart
doom hom the peace, my let wilt thee where them,
Truth, yet, God, iffect for shall in me of t
---------------

The and ops, life and see and of the clost a races
In dief the his but of down and premine.

AUTOLYCUS:
For excity our enemy should.
That stion thou grave you the desire and the shall to thou king
Look their and homents.

ROMEO:
Come, best not so sair and putches the grace,
Cannot thing thou do neel me the dest from to the sease.

MARCHIO:
Ah not of my 'tis me would me grain,
And joy though a do in my life conto call on him.

Second Hatrer:
I prician a print, but her is me telling I knave I I'll
---------------


CLAUDIO:
That sir, then, fough that's company and that him hearge the suit,
The Trule and shall the womes eyes him,
'tis no like, for thereighreed be you comed your him;
And you what yet with them.

KING HENRY VI:
Steep thy sorrow air down you besented,
I do lord you are of my the that as your somes: be and to know.

COMINIUS:
Nou they this luckless the happey.

EDWARD:
'tis it in you less recommen! We'll bone my firsty
Begong, my let not is theserving my fear meo's speak?

First Second Cerse:

---------------

But us, when a life thou, and for happerch some of my life as of
As of my with and him.

CAPULET:
I'll you it with happarty?

HENRY BOLINGBROKE:
Not what marcious convice you, and let shall thy,
And ball groeng righter her for the some son,
I will be the common I she he for him:
And Em of your riched of him thence,
I pasting from the hear is in at a pityer to say.

PAULINA:
Ay, shall to their that the lord,
When liet be they see,
For strainour peness would the splace and me:
And you welce, sir.

---------------
```
# Question 3
The following table shows the training results for different number of attention heads.

| Num of Layers | Num of Attention Heads | Validation Loss |
| - | - | - |
| 7 | 2 | 1.7853 |
| 7 | 3 | 1.7743 |
| 7 | 5 | 1.8089 |
| 7 | 7 | 1.7329 |

The following graph plots the graph of the above table.
![image](figures/Plot%20(1).jpg)

# Question 4
Final Training Results:<br>
step 4000: train loss 1.0404, val loss 1.2132

Command used to train the model is:
```
python3 train.py config/train_code_generation.py --eval_iters=20 --block_size=64 --batch_size=12 --max_iters=4000
```

First 20 Lines Generated:
```
                                                                                                                                        \
                                          for (haystack);
                                       ? return m_.bufference.empty());
                                                                                                           assert(NDOWSD);
                                                                                                             
---------------


#ifdef GTEST_HAS_WINDOWS) __PARANDS_FILE

// ASSERT|EXPECT}_STRING_CASERT|EXPECT}_PATERNAL TESTS AND FOR PROPECT}_

// DISCLAR CONEQUENTITED AND AND TO, IMPLIENTAL ANY OR PROGRICING DO DISCLASE AND TO,
// ANY OF TO, EVENTIAL, OR PROCESSUBSTIAL, IN A BUTITED FATAL,
// TO, THE COPYRACE DAMAGES; LIMIGENT) ANY OF THE COPYROW
// LIMED. IMPLIED TO, ARY OF THE PROFISTIESS AND SERVIDES ANY OF THE COPYRIGHT
// TEST_SIMPLATE_TEST_status char AssertibleSuppressfuls() const {
  explicit StreamableTo(ptr, c
---------------
```
The most coherent code that is generated is this snippet:
```
// the output test suite.
//       WaithParameter<typename T> typename DescributeConstructory:
    BOOST_NOEXCEPT_OR_ATTRIBUTE_NODISCARD inline
                           return && type) case                                                \
              );
                        return nullptr;
                  } else
                            {
                                            const TestPartResult& listener) {
        const TestSuite& test_suite->~TestPartResult() {
         ret
```
It somewhat outputs correct lines of code and uses the right data types, while other outputs gave very fragmented pieces of code.