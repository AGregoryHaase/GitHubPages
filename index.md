<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="section10.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
    <title>Section 10: Flexbox</title>
</head>
<body>
    <h1>Section 10 <br>
    <!-- Menu with links -->
        <h2>In this section</h2>
        <ul>
            <li><a href="#101">101. What Matters in This Section</a> </li>
            <li><a href="#102">102. What on Earth Is Flexbox?</a> </li>
            <li><a href="#103">103. Flex-Direction</a> </li>
            <li><a href="#104">104. Justify-Content</a> </li>
            <li><a href="#105">105. Flex-Wrap</a> </li>
            <li><a href="#106">106. Align-Items</a> </li>
            <li><a href="#107">107. Align-Content &amp; Align-Self</a> </li>
            <li><a href="#108">108. Flex-Basis, Grow, &amp; Shrink</a> </li>
            <li><a href="#109">109. Flex Shorthand</a> </li>
            <li><a href="#110">110. Responsive Design &amp; Media Queries Intro</a> </li>
            <li><a href="#111">111. THe Power of Media Queries</a> </li>
            <li><a href="#112">112. Building a Responsive Nav</a> </li>
        </ul>

        <!-- Right, I need to recap tables. I still can't make a decent table. I want to put a nice table here for the WHAT MATTERS IN THIS SECTION. -->
        
        <h2 id="101">what matters in this section?</h2>
        <p>Okay, so basically everything is crucial. he actually says that media queries are <em>very</em> important and goes at the top of the crucial to know pile..</p>
        <ul><h3>Crucial</h3>
            <li>media queries</li>
            <li>focus on concepts, not memorizing the properties!</li>
            <li>flex shorthand</li>
            <li>flex-basis, grow, and shrink</li>
            <li>align-items</li>
            <li>Flex-wrap</li>
            <li>Align-content and align-self</li>
            <li>Justify-Content</li>
            <li>Flex-direction</li>
        </ul>

       <h2 id="102"><em>102. What on earth is flexbox?</em></h2>
        <section class="1stbox">
            <h2>The Basics</h2>
            <ul>
                <li>
                    What is it?
                </li>
                    <ul>
                        <li>
                            Flexbox is a one-dimenstional layout method, used for laying out items in <em>rows</em> or <em>columns.</em>
                        </li>
                    </ul>
            </ul>
                    <ul>
                        <li>It's new(ish)</li>
                        <ul>
                            <li>
                                Flexbox is a recent addition to CSS, included to address common frustrations.
                            </li>
                        </ul>
                    </ul>
            <ul>
                <li>
                    why 'flex'?
                </li>
                <ul>
                    <li>Flexbox allows us to distribute space dynamically 
                        across elements of an unknown size, hence the term "flex"</li>
                </ul>
            </ul>     
            </ul>
        </section>
        <section class="102. What on earth is Flexbox?">
            <p class="p1">Flexbox is a newer part of CSS. Standard part of browsers in the last 2-3 years. 
                So, we have a container and we want to evenly distribute the space inside the container.
                Colt shows example of a nav bar that stacks as he shrinks the browser to the right. 
                Colt then shows us the Airbnb website. 
                He says that you don't want to hard code in the width and length. 
            </p>
        </section>
       
    </h1>
    <article id="103">
        <h3>flex direction</h3>
        <p>Right, so he gives us some code to work with. It's some html that consists of 5 divs, each with inline styling. 
            He says that inline stying isn't recomended but it saves us having to create a bunch of nth-of-type in CSS in order to create different colour boxes. 
            RIght, so I'll just copy what he has here instead of importing it from a download. Seems quite simple. 
        </p>
         <h3>let's play with Flexbox</h3>

         <section id="container">
             <div style="background-color: #80ffdb; height: 300px;"> H </div>
             <div style="background-color: #64dfdf;">E </div>
             <div style="background-color: #48bfe3; height: 450px;">L </div>
             <div style="background-color: #5390d9;">L </div>
             <div style="background-color: #6930c3;"> O</div>
         </section>

         <aside>
            <p>Lil list showing the different flexxss.FLEXXSS</p>
            <ul><h4>flex-direction</h4>
                <li>row</li>
                <li>row-reverse</li>
                <li>column</li>
                <li>column-reverse</li>
            </ul>
            <ul>
                <h4>Justify-Content</h4>
                <li>Flex-start</li>
                <li>Flex-end</li>
                <li>Center</li>
                <li>space-between</li>
                <li>space-around</li>
                <li>space-evenly</li>
            </ul>
            <ul><h4>heirarchy</h4>
                <li>Right so what I'm trying to say is that the flex-direction determines the axis (main(horizontal) or cross(vertical))
                    So the flex direction determines the justify content regarding the flex start and flex end, which then determines which 
                    way the spaces are added around the elements within the container
                </li>
            </ul>
        </aside>

         <p>Okay, so we are starting with the display property. We've used display block, display, inline, display inline block. 
             what we haven't seen before is display: flex;
             We've created the container in CSS. 
             We select all the divs in the container (in CSS) 
             I've done that. They are block level elements. 
             We then set the display to flex in the <em>container.</em>  Now they all line up in a nice row. 
            <ul><li>Before we go any further we have to look at some terminology</li></ul>
            When we set display to flex, there are 2 axis. THe main axis and the cross axis.
            These are very important for the other properties we're going to discuss.
            By default the main axis goes from left to right. However, we can change the direction of 
            this with the flex-direction: which is defaulted to row;
            He shows us that, currently, our boxes are lined up by matching the top (green div) to 
            the darker shades. 
            He then shows us how to change that using flex-direction which allows us to decide on 
            the main axis direction in our container.
            <h4>flex-direction: row &amp; row-reverse;</h4>
            He then puts "flex-direction: row;" underneath display: flex; in the CSS for #container.
            He then put's flex-direction: row-reverse; - and yes, sure enough, the divs have 
            shifted to the right of the container and reversed their order. 
            <h4>flex-direction: column &amp; column-reverse</h4>
            INitially our boxes have changed shape, they are now flatter. This is becasue 
            we set the height of the container to 500px.
            If we change the height of the container then the divs also change to fit, but won't go past the 200px as we have dictated.
         </p>
    </article>
    <article #104>
        <h2 id="104">Justify-Content</h2>
         Apparently justify content is for the Main (Horizontal axis). I've jsut watched the start of the align-Items and he says that at the sstartt of the clip. 
         Okay, so he sets the flex direction to row again. 
                <h3>flex-start</h3>
                He then adds in justify-content: (to) flex-start;
                <h3>flex-end</h3>
                Nothing changes but he then changes it to justify-content: flex-end;
                This pushes the row of divs to the right hand side of the container (without changing the order)
                <h3>center</h3>
                He then shows us justify-content: center; This, you guessed it, puts the div boxes into the centre of the container.
                <h3>space-between and space-around</h3>
                Space between will put space inbetween but not around the outer edges of the element and the container.
                Space-around gives the same amount of space between each element and between the edge of the container.
                <h3>space-evenly</h3>
                ...Does what it says.

        <h3>heirarchy</h3>
        Right, so basically the thing with the direction (some people have asked him why it isn't called horizontal align?)
        If the flex direction is set to row then it will put space between the divs horizontally. 
        If you set the flex-direction to column then consequenting spacing is applied to the divs vertically. 
        THis also applies to flex-end and flex-start. 
    </article>
    <article id="105">
        <h2 id="105">flex-wrap</h2>
        <p>
            Quick one called Flexwrap. I'm gonna create a new set of divs for this I think. 
            Okay, I'v done that. Below. 
            Seems that this just works in the same way as wrap in excel.
            Right so he starts off by saying there's pretty much just wrap and wrap-reverse, and no-wrap.



        </p>
        <section id="container2">
            <div style="background-color: #80ffdb;"> D </div>
            <div style="background-color: #64dfdf;">U </div>
            <div style="background-color: #48bfe3;">M </div>
            <div style="background-color: #5390d9;">B </div>
            <div style="background-color: #6930c3;"> !</div>
        </section>
    </article>
    <section id="106">
        <h3>align-items</h3>
        <p>
            Distribute space along the cross axis.  
            Okay, I'm not that sure what the difference is between justify and align items. 
            Let me try and figure this out. I'll create a new set of divs inside a container below. 
            He ends up shifting things around using various Align-items variables. 
            We add some text to the divs and he then aligns the divs according to the baseline of the text, instead of 
            the divs being align to the centre of themselves.
            WE CHANGE THE SIZE OF THE A letter in the div and we can see that all the divs are aligned to the baseline of the fonts.
        </p>
            <article id="container3">
            <div style="background-color: #80ffdb;"> D </div>
            <div style="background-color: #64dfdf;">U </div>
            <div style="background-color: #48bfe3; height: 300px; font-size: 8em;">M </div>
            <div style="background-color: #5390d9;">B </div>
            <div style="background-color: #6930c3; height: 100px;"> !</div>
            </article>
        <p id="p1">
            Right, so he undoes all of the alignments but I want to keep them on the page so I'll create container set 4, below. 

        </p>
        <article id="container4">
            <div style="background-color: #80ffdb;"></div>
            <div style="background-color: #64dfdf;"></div>
            <div style="background-color: #48bfe3;"></div>
            <div style="background-color: #5390d9;"></div>
            <div style="background-color: #6930c3;"></div>
        </article>
    </section>
    <section id="107">
        
        <h2>Align-content &amp; Align-self</h2>
        <h4>align-content</h4>
        <p>Align-content, space between rows or space between columns <em> depending on the orientation of the flex axis.</em> Will only work when flex-wrap is on</p>
        
        <article id="container5">
            <div style="background-color: #80ffdb;"></div>
            <div style="background-color: #64dfdf;"></div>
            <div style="background-color: #48bfe3;"></div>
            <div style="background-color: #5390d9;"></div>
            <div style="background-color: #6930c3;"></div>
        </article>

        <h4>align-self</h4>
        <p>Align self is very similar to align-items except it's actually a property we add to a single element, or individual items inside a flex container.
            It's the first property we've seen that we don't actually apply to the flex container itself, but to individual elements.
            And we can change the alignment along the cross axis for a single element using it.
        </p>
        <article id="container6">
            <div style="background-color: #80ffdb;"></div>
            <div style="background-color: #64dfdf;"></div>
            <div style="background-color: #48bfe3;"></div>
            <div style="background-color: #5390d9;"></div>
            <div style="background-color: #6930c3;"></div>
        </article>
    </section>
    <section id="108">
        <h3>flex-basis, grow &amp; shrink </h3>
        <p>
            3 related properties that have to do with individual items within a flex container and how they grow or shrink when there is 
            available space or when there is too little space.      </p>
            <h4>Flex-Basis</h4>
            <p>
                determines the initial size on an element before it's added into our flex container. 
                Right, so this is added to the div element. 
            </p>
        
  <article id="container7">
            <div style="background-color: #80ffdb;"></div>
            <div style="background-color: #64dfdf;"></div>
            <div style="background-color: #48bfe3;"></div>
            <div style="background-color: #5390d9;"></div>
            <div style="background-color: #6930c3;"></div>
        </article>

        <p>
            <h4>flex-grow</h4>
            controls the amount of space that an element takes up if there is available space.
        </p>
<article id="container8">
        <div style="background-color: #80ffdb;"></div>
        <div style="background-color: #64dfdf;"></div>
        <div style="background-color: #48bfe3;"></div>
        <div style="background-color: #5390d9;"></div>
        <div style="background-color: #6930c3;"></div>
    </article>

    <p>
        <h4>flex-shrink</h4>
        controls the amount of space that an element takes up if there is available space.
        See the CSS.
    </p>
<article id="container9">
    <div style="background-color: #80ffdb;"></div>
    <div style="background-color: #64dfdf;"></div>
    <div style="background-color: #48bfe3;"></div>
    <div style="background-color: #5390d9;"></div>
    <div style="background-color: #6930c3;"></div>
</article>

    </section>

    <section id="109">
        <h3>Flex Shorthand</h3>
        <p>
            MDN sheet <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/flex">here</a>.
            Code along - he creates three sections. Sidebar, maincontent, sidebar.
            Remember in shorthand its flex: grow shrink basis.
        <main>
            <section class="sidebar"></section>
            <section class="maincontent"> </section>
            <section class="sidebar"></section>
        </main>
        </p>
    </section>

    <section>
        <h3 id="110">Responsive design &amp; Media Queries</h3>
        <p>OKay so we are on to Responsive design and media queries.
            <ul><h4>The Problem</h4>
                <li>So here is the problem. As mobile devices and tablets became widely available developers had a 
            problem ... how do we create websites that look good on all screen sizes?</li>
            </ul>
            <ul> <h4>one approach</h4>
                    <li>Early on it was common to create seperate stylesheets for different devices, 
                        or even completely different websites for each size
                    </li>
            </ul>
            <ul><H4>ENTER RESPONSIVE</H4><li>These days, we typically create ONE website and stylesheet that is able 
                to respond to different device sizes and features.
            </li></ul>
            <h2>media queries</h2>
            <p>Media queries allow us to modify our styles depending on particular parameters like screen width or device type.
                BIG TIP! Go to chrome dev tools command shift M will give you the mobile view.
    
            </p>
        </p>
    </section>

    <section>
        <h3 id="111">The Power of Media Queries</h3>
        <p>
          All media queries start with @media and there are   
        </p>
    </section>
</body>
</html>
