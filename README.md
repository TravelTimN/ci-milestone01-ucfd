# PAUL M MUSIC

###### Code Institute / User-Centric Front-End Development

Tasked to create a 4-5 page static website for a band (ie: the Monkees), I wanted to step away and do my own thing. Fortunately, I know someone in London that is an artist, and thus found his website [www.paulmmusic.com](http://www.paulmmusic.com). Unfortunately, it's clearly outdated and a bit bland, so I contacted Paul to see if we could help each other out. He loved the idea immediately, and started sending me plenty of assets whilst I started the wireframing. Paul was finding it difficult to imagine the site with just wireframes, so I took it a step further and built entire mock-ups for him instead.

## DESIGN

#### FRAMEWORK

**CSS Grid** - During the training modules, we focused on [Bootstrap 3.3.7](http://getbootstrap.com/docs/3.3/), however, I personally prefer CSS Grid, which I learned from [CSS-Tricks | A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/). I've decided to build the entire site using Grid, with no Bootstrap or Flexbox required.

#### COLOR SCHEME

The color scheme was created by asking Paul his two favorite colors (sky blue and purple), and sent him a small selection of each color with their `HEX` codes, to which he chose one of each. I paired these using the custom color palette on [Material.io](https://material.io/tools/color) and came up with the following scheme, which he absolutely loved:

[ *all colors are set at `:root` level in CSS* ]

- `#90CAF9` (*primary blue*)
- `#C3FDFF` (*light blue*)
- `#5D99C6` (*dark blue*)
- `#9B27AF` (*primary purple*)
- `#CF5CE2` (*light purple*)
- `#69007F` (*dark purple*)

The remaining aesthetics were my own preference, to ensure the site remains clean, sleek, modern, and professional.

#### UX DESIGN

I use a fair amount of `:hover` effects in my CSS, to allow more interaction for the user, but without going too overboard that the site becomes an animation factory!

Some examples:

* Quotes from [Testimonials](https://traveltimn.github.io/ci-milestone01-ucfd/testimonials.html) expand for more emphasis.
* Images scale slightly larger in a few areas.
* [Photos](https://traveltimn.github.io/ci-milestone01-ucfd/photos.html) all start grayscale, but transition to color.
* Social Media links pop with their brand's primary color.

#### WIREFRAMES

I used [Adobe XD](https://www.adobe.com/ie/products/xd.html) to create my wireframes initially, but needed to go one step further for Paul and create [mock-ups](https://github.com/TravelTimN/ci-milestone01-ucfd/tree/master/wireframes-mockups) instead. They are larger files due to the images, so in each desktop and mobile file, I've included `.png` files of each page for visual representation on GitHub.

## FEATURES

All pages on the site include the same exact `<header>`/`<nav>`, and `<footer>`. The only exception is in the navigation, whereby each *active* page contains `class="active"` that'll slightly change the appearance as a visual indication to the user of which page they're currently visiting.

###### [index.html](https://traveltimn.github.io/ci-milestone01-ucfd/index.html)

Paul wanted a simple, relatively empty, landing page. I've included two basic `<a>` elements, designed in CSS to appear and act as 'call-to-action' buttons.

###### [music.html](https://traveltimn.github.io/ci-milestone01-ucfd/music.html)

This should be the primary focus of coming to Paul's site. His music and albums are exhibited here for each of the following platforms:

   - [Spotify](https://open.spotify.com/artist/5mjRfG1TxOSSXeYOsKQQJh)
   - [Bandcamp](https://paulmiddleton.bandcamp.com/music)
   - [Google Play](https://play.google.com/store/music/collection/5:search_cluster:2?clp=YiQKDnBhdWwgbWlkZGxldG9uEAIaEAoOcGF1bCBtaWRkbGV0b24%3D:S:ANO1ljJaJkM)
   - [iTunes](https://itunes.apple.com/ie/album/covers-2/id977851374?app=itunes&ign-mpt=uo%253D4#see-all/top-songs)

##### [videos.html](https://traveltimn.github.io/ci-milestone01-ucfd/videos.html)

This page is dedicated to Paul's [YouTube](https://www.youtube.com/user/paulmiddletonmusic) channel. It portrays the *Most Popular* videos by ranking, via embedded iframes.

##### [photos.html](https://traveltimn.github.io/ci-milestone01-ucfd/photos.html)

Purely a page to view some photography of Paul that he's requested to be added online.

- Images display in color on `:hover` from `filter: grayscale();`.
- Images open full-screen using [fancybox](https://fancyapps.com/fancybox/3/), as recommended by my [mentor](https://github.com/ignatiusukwuoma).

##### [testimonials.html](https://traveltimn.github.io/ci-milestone01-ucfd/testimonials.html)

Testimonials is actually a combination of previous testimonials, and a list of former and current clients. This page also has the most responsive design concept:

- **Clients** (desktop): displayed in grid format.
- **Clients** (mobile): displayed in auto-scroll ticker effect.

##### [contact.html](https://traveltimn.github.io/ci-milestone01-ucfd/contact.html)

Simple page that allows users to get in contact with Paul directly.

#### WISH LIST

Future Implementations:

- Incorporate full `SEND` functionality of the form, so Paul actually receives communications. (suggestion from mentor: [formspree.io](https://medium.com/@asjas/using-formspree-io-on-your-github-pages-a60c290d1ee))
- Build pre-loader, as iframes and photos sometimes load slowly.

## TECHNOLOGIES

Brief overview of the languages, frameworks, and other tools I've used on this project:

- [HTML5](https://en.wikipedia.org/wiki/HTML5)
    - Semantic markup language as the shell of the site.

- [CSS3](https://en.wikipedia.org/wiki/Cascading_Style_Sheets)
    - Cascading Style Sheets as the design of the site.

- [CSS Grid](https://en.wikipedia.org/wiki/CSS_grid_layout)
    - Grid allows for a responsive layout across various platforms.

- [JavaScript](https://www.javascript.com)
   - Used for open/close effect on mobile navbar, as well as the fancybox implementation.

- [Font Awesome 5](https://fontawesome.com)
   - Use of social media icons.


## TESTING


#### TEST MATRIX

I created a [testing matrix](https://github.com/TravelTimN/ci-milestone01-ucfd/blob/master/testing/ucfd-user-testing.pdf) in Excel, but saved as `.png` to visualize here on GitHub. It outlines the various tests I made to ensure the site renders consistently across different platforms, and that each functionality behaves as intended.

#### COMBATIBILITY

To ensure a broad range of users can successfully view/use the site, I tested it across all major browsers in both desktop and mobile configuration.

- Chrome
- Edge
- Firefox
- Safari
- Opera
- Internet Explorer

#### NOTED ISSUES

**Safari** and **IE** seem to cause the most problems.

- **IE**: Doesn't support CSS Grid, so the entire site breaks.
- **Safari**: The navbar doesn't `position: fixed;` on desktop, and doesn't function at all on mobile. Some minor `transition: scale();` issues with overlapping of client logos. The contact form `<legend>` doesn't center properly.
- **Edge**: Minor frame-shredding when scrolling too fast on the navbar.

[ *Safari issues might be due to the fact that I was running macOS on a virtual machine, not actual Apple hardware* ]

## DEPLOYMENT

I've deployed the site using **GitHub Pages**, and is available here: [https://traveltimn.github.io/ci-milestone01-ucfd](https://traveltimn.github.io/ci-milestone01-ucfd)

For this project, local deployment was not required.

## CREDITS

#### CONTENT

All text was initially provided by Paul himself, with edits and corrections on my part for consistency between each page, as well as some minor grammar mistakes.

#### MEDIA

All assets pertaining to Paul were provided by Paul.

Client logos were obtained from the client's website or social media site, as follows:

- [Adventure Island](http://adventureisland.co.uk)
- [Amsterdam Hotel Brighton](http://amsterdamhotelbrighton.com)
- [Bar Broadway Brighton](http://www.barbroadwayuk.co.uk)
- [Britannia Adelphi Hotel](https://www.britanniahotels.com/hotels/the-adelphi-hotel-liverpool)
- [British Airways](https://www.britishairways.com)
- [Center Parcs](https://www.centerparcs.com)
- [Cromer Pier](https://www.cromerpier.co.uk)
- [Eastbourne Bandstand](https://www.eastbournebandstand.com)
- [Eastbourne Winter Gardens](https://www.eastbournetheatres.co.uk/venue/winter-garden)
- [Fontwell Racecourse](https://www.fontwellpark.co.uk)
- [Gillingham Golf Club](http://www.gillinghamgolfclub.co.uk)
- [Green Rooms London](https://www.greenrooms.london)
- [Hackett, London](https://www.hackett.com/gb)
- [Havant and Waterlooville FC](https://www.havantandwaterloovillefc.co.uk)
- [Holiday Inn](https://www.ihg.com/holidayinn)
- [Hotel Martinez Cannes](https://hotel-martinez.hyatt.com/en/hotel/home.html)
- [ITV](https://www.itv.com)
- [Lingfield Park Racecourse](https://www.lingfieldpark.co.uk)
- [M Festival](https://themfestival.co.uk)
- [Manchester Pride](https://www.manchesterpride.com)
- [Marks and Spencers](https://www.marksandspencer.com)
- [MP-Events Belgium](http://mp-events.be)
- [Oakwood House](http://www.oakwoodhousehotel.co.uk)
- [Orchard Theatre](https://orchardtheatre.co.uk)
- [Oscars Bar Manchester](http://www.oscarsbarcanalstreet.co.uk/index.html)
- [Parliament House Orlando](http://www.parliamenthouse.com)
- [Pride in London](https://prideinlondon.org)
- [Radisson Blu Hotels](https://www.radissonblu.com)
- [Rendezvous Casino](https://brighton.rendezvouscasino.com)
- [Rockbar New York City](https://www.rockbarnyc.com)
- [Shanklin Theatre](https://www.shanklintheatre.com)
- [Sitges Bear Week](http://www.bearssitges.org)
- [Stadium MK](http://www.stadiummk.com)
- [Thorney Bay Holiday Park](http://www.thorneybay.co.uk)
- [Trentham Gardens](http://www.trentham.co.uk/trentham-gardens)
- [University of Birmingham](https://www.birmingham.ac.uk)
- [Warner Leisure Hotels](https://www.warnerleisurehotels.co.uk)
- [Worcester Racecourse](https://www.worcester-racecourse.co.uk)
- [Yes Events](http://www.yesevents.com)

Media buttons were created by me in Photoshop, using the following brand logos:

- [Bandcamp](https://bandcamp.com)
- [Google Play](https://play.google.com/store?hl=en)
- [iTunes](https://itunes.apple.com)
- [YouTube](https://www.youtube.com)

#### ACKNOWLEDGEMENTS

Huge thanks to my mentor [Ignatius Ukwuoma](https://github.com/ignatiusukwuoma) for his time, suggestions, and constructive feedback!

Also where credit is due, the concept of getting the client scrolling effect on mobile came from Codepen:  [Responsive CSS Image Slider by Dudley Storey](https://codepen.io/dudleystorey/pen/ehKpi)

Finally, to [Chris Quinn](https://github.com/10xOXR), my accountability partner for all projects.