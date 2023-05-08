# Learning Journal

## Week 8

## Learning Activities
This week I am to conduct a learning experiment. In the past weeks I have mentioned struggling with motivation, and I hope to test a method of improvement with this experiment. I believe this could be linked to being distracted or a lack of focus within my learning environment. For this experiment I will attempt to learn in two different environments and see what works better for me.

Theory: The environment I study in effect my concentration, which in turn effects my motivation.

Hypothesis: I will have more success studying in an environment devoid of distraction than one filled with distractions.

Method: Two study sessions will be conducted, one in my bedroom office and the other in my living room. Both sessions will be ~30 minutes or half of the Sass LinkedIn Learning course. Content for these study sessions will be learning Sass.

I believe that my room is a bad learning environment, as I have plenty of things to distract me all within arms reach. I also believe that there is some sort of psychological connection between my room and "having fun" or distracting myself, as I feel compelled to do something other than study while I'm here. This might be the case or I may just have poor work ethic, and hopefully this experiment will highlight which is true.

## Resources/Links
Sass LinkedIn Learning  https://www.linkedin.com/learning/sass-essential-training-15630917/how-can-sass-help-build-sites?autoplay=true&resume=false&u=2223545

Nesting example: https://www.linkedin.com/learning/sass-essential-training-15630917/nesting?autoSkip=true&autoplay=true&resume=false&u=2223545

Extend example: https://www.linkedin.com/learning/sass-essential-training-15630917/extend?autoplay=true&resume=false&u=2223545
## Estimated Hours
1 hour
## Content Insights
Sass has two different syntax's, .sass and .scss. .Sass is an older version that makes whitespace in code meaningful, which eliminates that need for {}. .Sccs is the newer syntax, and is compatible with normal CSS, unlike .sass files. Due to this compatibility, this newer syntax will be used.

Just like php, Sass variables begin with a $ and name, followed by a colon and end with an expression. Variables created outside {} are global variables, while variables inside {} are local variables. Global variables and local variables can have the same name, this is known as shadowing.

        $primary-color: red;

        h1 {
          $primary-color: yellow;
          color: $primary-color;
        }

        body {
          color: $primary-color;
        }
In the above example, the heading would be yellow, while the body would be red. Local variables take priority within their scope. You can also redefine global variables using !global.

        $primary-color: red;

        h1 {
          $primary-color: yellow !global;
          color: $primary-color;
        }

        body {
          color: $primary-color;
        }
In this example, both elements would be yellow.

In Sass, the hyphen (-) and underscore (_) are considered the same character. This means that variables named $primary_color and $primary-color refer to the same variable.

Sass also allows you to nest rules inside other rules. This allows for easier organisation of elements and attributes. Check [second link](https://www.linkedin.com/learning/sass-essential-training-15630917/nesting?autoSkip=true&autoplay=true&resume=false&u=2223545) you need a reminder or example of this.

Partials are separate files of code that can be used to store variables and imported into other files to be used. Partial files start with an underscore, and are used by calling @use. Variables in partial files can used by calling the namespace, which is by default the file's name. This namespace can be changed using the "as" shortcut.

        // _variables.scss
        $bg-color: red;
        $primary-color: blue;

        //_base.scss
        @use "variables";
        body {
          background: variables.$bg;
        }

        //style.scss
        @use "variables" as var
        @use "base";
        h1 {
          color: var.$primary;
        }

Parent selector lets you easily work with nested styles. Using the ampersand symbol (&) you can create a style that targets the parent and add whatever the parent is where the & is.

        .btn{
          //some button code
        }

        &:hover{
          background: blue;
        }

The above scss compiles to the following css:

        .btn{
          //some button code
        }

        .btn:hover{
          background:blue
        }

& can be used a suffix and a prefix too, making it very useful in creating nested styles.

Mixins are similar to JS functions, and are created using @mixin. You are then able to pass some parameters with default values to the mixin. To use a mixin, use @include.

Extend rules can be used to share default values across different elements that are shared by the parent element. The best way to understand this is to see it for yourself, so if you need a reminded check the [third link](https://www.linkedin.com/learning/sass-essential-training-15630917/extend?autoplay=true&resume=false&u=2223545).

Interpolation allows you to work with variables that are defined in expressions.
Format:

        #{$varName}
        #{$varName + '--btn'}

Can be used in many places, such as mixins, calculations, comments, function names and more.

Placeholder selectors can be used to create classes that you only want to extend, but not compile. These classes start with a percentage sign (%). With placeholder selectors, you are able to create a button-primary and a button-secondary class without having to make a button class itself.

List in Sass different from other programming languages, as they are one index. This means the first element of a list in one, not zero. Sass list are also immutable, and methods that change a Sass list actually create a new modified copy of the list. List have various methods, such as length, nth, set-nth, index, append and more.
## Career/Employability/Learning Insights
The study session within my living room when much more successful than the only in my bedroom. Nearly as soon as I begin the session in my bedroom I was overcome with the urge to do something on my desktop in front of me. I also got lost in thought on multiple occasions, daydreaming about other topics than what I was meant to be doing. I did not have my phone present in either session, though I felt a strong urge to get my phone during my bedroom study.

Interestingly, the ambeince of the living room was calming and felt enjoyable to study in. The aquarium produced a soothing sound of quiet running water which I enjoyed. In the future, I may experiment with white noise or other calming sounds to see if this helps me concentrate better. The only downside to the living room session was the chair I was seated at. Unlike my office chair in my room, the hard wooden chair was not comfortable. That being said, it did not disturb me as much as trying to study in my room did. Overall, I believe I will need to separate where I learn and where I enjoy myself, as this test has proven to me that I cannot do both in the same place.
