---
    title:  >
      Super - Simple - Static - Sustainable’ a low resource repository jam :: Progress Report  2024-06-06 Open Repositories 2024, Göteborg, Sweden
    date: 2024-06-06
   
---

<a href="sss.pdf">PDF version</a> | <a href="sss.pptx">Powerpoint Version</a>


    

<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide0.png' alt='‘Super - Simple - Static - Sustainable’ a low resource repository jam :: Progress Report  :: 2024-06-06 :: Open Repositories 2024, Göteborg, Sweden. June 2 - 6, 2024. :: ' title='Slide: 0' border='1'  width='85%%'/>







</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide1.png' alt='Workshop core values and aims :: THIS IS NOT A COMPETITION. :: We will encourage participants to learn new skills and to work with new collaborators and create teams with a diverse range of background and levels of experience :: Produce demonstrable code/techniques for creating, managing and disseminating simple static repositories / archives with real data (where possible) that can immediately be used in low resource environments :: But it might be a *bit* like the old OR “Developer Challenge” :: We will recap the inspiration for this session, present &amp; discuss Suleman’s “principles and design goals”: :: Simplicity/Minimalism – only as much system as needed :: No imposition on users – no logins unless necessary :: No Internet - should work even when offline :: Simple preservation – as simple as copying files :: Flexibility in objects/services – no arbitrary restrictions :: Superimposed and hierarchical information – because we understand this :: Platform agnosticism – any OS, any hardware :: Pre-processing – fewer cycles needed when live  ::  :: https://zenodo.org/records/8111569 :: Inspired by the rousing OR-2023 closing keynote :: ' title='Slide: 1' border='1'  width='85%%'/>



Inspired by Prof Hussein Suleman’s closing keynote at OR2023 “Designing Repositories in Poor Countries” this workshop explored practical implementations of Suleman’s principles and goals. We encouraged developers, metadata specialists and managers to embrace, simple and sustainable approaches to making data safe and available using  well established static web  publishing techniques with on-demand indexes and discovery interfaces – contrasting with the complexity of current repository stacks which have grown into bloated enterprise software where setup and data migration are very expensive and hosting requirements are substantial. 

We explored a range of technologies including those mentioned in the keynote and the participants came up with the following ideas which they’ve been working on and documenting throughout the conference.

We’d love to see some of these ideas continue to develop and to show up at OR2025 as poster or dev-track submissions.




</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide2.png' alt='Internet in a Box :: 1. Context :: Population 3.8 :: Schools &gt; 1400 :: Students 600,000 :: Conventional Library costly :: Internet penetration below 1% ::  :: 3. Solution :: Low End Server :: A router or Access point 50 users :: Website ::  :: Content :: Communities in Diaspora :: 2. Problem :: Difficult to provide info  :: 4. Result :: ' title='Slide: 2' border='1'  width='85%%'/>







</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide3.png' alt='Easy Open :: OPEN.html   #Required :: content/    #Required :: metadata/   #Optional :: resources/  #Optional ::  :: OPEN.html     # redirects to content/ro-crate-preview.html :: content/ ::     ro-crate-metadata.json ::     ro-crate-preview.html ::     ro-crate-preview_files/ ::         … ::     bag1/ ::         bagit.txt ::         bag-info.txt ::         manifest-sha512.txt ::         data/ ::             example.txt :: metadata/ ::     manifest.txt ::         # content/ro-crate-metadata.json ::         # content/bag1/bag-info.txt :: A user-friendly top level organization for self-contained browsable packages :: Patrick Stickler, Peter Sefton, … :: ' title='Slide: 3' border='1'  width='85%%'/>



Easy Open is a [concept / proposal](https://docs.google.com/document/d/1y0Cu5cSia6rlRotnfdU_wcrZUL3DnjXx0MUah--_7-Y/) for a simple, maximally clear, user-friendly top level organization for providing self-contained browsable archives, repositories, datasets etc. which is compatible with the broadest range of existing packaging and metadata standards (but requires none).

The key goal of this proposed standardized top level organization is to make it as clear and easy as possible for a user to begin to consume the contents of a package without having to understand anything about the underlying packaging or metadata solutions used to organize and describe it, while also being compatible with existing and future standards and conventions for providing rich metadata and well organized and portable structure, enabling automated consumption by tools.

Easy Open focuses exclusively on the top level organization of user friendly, easily consumable, browsable, and platform portable content, and is a component of developing recommendations for producing maximally distributable and consumable packages of content, including
operating system and filesystem agnostic
compatible with commonly used web browsers, including text-only and no-javascript environments
Javascript and stylesheets can be used to make the browsing experience more dynamic and richer, but it is recommended that such functionality not be critical to consuming the core content of the package and that users aren't prevented in any significant way from consuming the content without Javascript or stylesheet support
self-contained and consumable offline
minimal run-time resource requirements
all content should be as accessible as possible

See the [draft spec](https://docs.google.com/document/d/1y0Cu5cSia6rlRotnfdU_wcrZUL3DnjXx0MUah--_7-Y/edit).



</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide4.png' alt='Generating Static repository from the Dynamic one ::  (Mahsa and Andjela) :: ' title='Slide: 4' border='1'  width='85%%'/>







</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide5.png' alt='Simple export of Zip + HTML in Easy Open Format  | Hyeokjin Kwon (TU Delft / 4TU.ResearchData) ::  :: ' title='Slide: 5' border='1'  width='85%%'/>







</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide6.png' alt='EPrints to Easy Open static export :: Here’s last year’s slides… (sorry Rory ;) Actually, here’s a SVN commit: :: ~/tools/static_site.plRev 7182 – 4607 d 19 h (Monday 24th October 2011)Author: tdb01r (Tim Brody)Log message:* experimental tool to generate a static version of an EPrints repository :: Started enhancing it to output the site in EasyOPEN as previously described. :: Outputs an EPrintsXML metadata file, thumbnails, documents, browse views :: Browser-based search using Lunr.js https://lunrjs.com/ A bit like Solr, but much smaller and not as bright. ::  :: ' title='Slide: 6' border='1'  width='85%%'/>



So, it turns out EPrints started work on this topic approximately 4610 days ago.None of us had actually run it. We have now. It still works, and outputs a static browseable site, thumbnails, content.So we broke it whilst trying to make it output a site in the EasyOPEN format previously described.Can output static metadata file in a variety of formats (e.g. DC, JSON)



</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide7.png' alt=' :: EasyScrape: ‘Remote site generation’ (impl. Easy Open) :: Kim Shepherd, Kiflom Michael Kahsay, Marco Schirone :: Spiders for feeds: ::  OAI-PMH, RSS, Atom :: Markdown (readable, usable, site generators like it) :: Resources (PDFs, data, images) :: Crawl/harvest repo, output static stuff :: Publish local content on Internet :: Host Internet content locally :: Jekyll :: 11ty :: Pelican :: Generate site :: No Internet?! :: Crawler + generator + storage + friend with Internet = ::  :: Distribute offline repo :: Host ‘online’ stuff locally ::  :: EasyOpen, OCFL, Bagit.. :: Open Repositories 2024, Göteborg, Sweden. June 2 - 6, 2024. :: ' title='Slide: 7' border='1'  width='85%%'/>



You already heard the use case: Eritrea has no reliable Internet, so they rely on physical storage to send and receive Internet content from nearby regions with more reliable Internet. They run research repositories on their local networks, and caching proxy devices to serve some open educational content as if it were ‘online’.

Our tools use projects with large, active communities,  common standards (including new one!), and practical considerations to get local research outputs out onto the Internet in the form of standalone, simple websites, and can also gather useful open resources from the Internet and package it in a way that can is simple to feed into devices like RACHEL Plus or host in local intranet webservers.

We started our prototyping by harvesting OAI-PMH METS feeds from DSpace and EPrints repositories and producing HTML with XSLT as well as markdown frontmatter to feed into more fully-featured site generators like Jekyll, 11ty, Pelican.



</section>

