---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: "Gabriel Jay Huerte - XCHANGED INC"
---

<section id="content" style="display: none; background: linear-gradient(rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.9)),  url('https://images.pexels.com/photos/2653362/pexels-photo-2653362.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940');">
    <div class="container-fluid">
        <div class="d-flex flex-col align-items-center justify-content-center text-success w-full h-full" style="height: 100vh;">
            <div class="row px-5 typewriter">
                <p class="col-12 text-uppercase m-0 programming-font line-1" style="font-size: 5vh">
                    <span class="letters-1"><strong class="px-md-2">Gabriel Huerte</strong> at your service</span>
                </p>
                <p class="col-12 programming-font line-2" style="font-size: 3vh">
                    <span class="letters-2">Nice to meet you</span> 
                </p>
            </div>
        </div>
    </div>
</section>

<script type="text/javascript">

    $('#content').imagesLoaded({ background: true }, function() {
        $(document).ready(function () {
            
            var textWrapper = document.querySelector('.line-1 .letters-1');
            textWrapper.innerHTML = textWrapper.textContent.replace(/([^\x00-\x80]|\w)/g, "<span class='letter'>$&</span>");
            
            var textWrapper2 = document.querySelector('.line-2 .letters-2');
            textWrapper2.innerHTML = textWrapper2.textContent.replace(/([^\x00-\x80]|\w)/g, "<span class='letter'>$&</span>");

            anime.timeline({loop: true})
            .add({
                targets: '.line-1 .line',
                scaleY: [0,1],
                opacity: [0.5,1],
                easing: "easeOutExpo",
                duration: 700
            })
            .add({
                targets: '.line-1 .line',
                translateX: [0, document.querySelector('.line-1 .letters-1').getBoundingClientRect().width + 10],
                easing: "easeOutExpo",
                duration: 700,
                delay: 100
            }).add({
                targets: '.line-1 .letter',
                opacity: [0,1],
                easing: "easeOutExpo",
                duration: 600,
                offset: '-=775',
                delay: (el, i) => 34 * (i+1)
            }).add({
                targets: '.line-2 .line',
                scaleY: [0,1],
                opacity: [0.5,1],
                easing: "easeOutExpo",
                duration: 700
            })
            .add({
                targets: '.line-2 .line',
                translateX: [0, document.querySelector('.line-2 .letters-2').getBoundingClientRect().width + 10],
                easing: "easeOutExpo",
                duration: 700,
                delay: 100
            }).add({
                targets: '.line-2 .letter',
                opacity: [0,1],
                easing: "easeOutExpo",
                duration: 600,
                offset: '-=775',
                delay: (el, i) => 34 * (i+1)
            });

            $('#content').show();
        });
    });
</script>