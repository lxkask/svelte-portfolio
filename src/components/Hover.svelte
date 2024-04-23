<script lang="ts">
    import "../app.css";
    import "./Hover.css";
</script>


<body>
<div class="wrapper w-screen px-10 py-20 bg-dark">
    <span>
        <h1 class="hover-this text-4xl"><section>Lo rem ipsum dolor sit amet consectetur adipisicing elit. Fugit iure dolores dolorem ratione</section></h1><h1 class="hover-this text-4xl"><section> explicabo perferendis dignissimos? Tenetur ex, temporibus, vel sapiente officiis earum</section></h1> <h1 class="hover-this text-4xl"><section>incidunt eius voluptates enim a itaque quas.</section> </h1>
        <div class="cursor"></div>
    </span>
</div>

<script>
    (function () {
        const link = document.querySelectorAll('span > .hover-this');
        const cursor = document.querySelector('.cursor');

        const animateit = function (e) {
            const span = this.querySelector('section');
            const { offsetX: x, offsetY: y } = e,
                { offsetWidth: width, offsetHeight: height } = this,
            move = 25,
            xMove = x / width * (move * 2) - move,
            yMove = y / height * (move * 2) - move;
            span.style.transform = `translate(${xMove}px, ${yMove}px)`;
            if (e.type === 'mouseleave') span.style.transform = '';
        };

        const editCursor = e => {
            const { clientX: x, clientY: y } = e;
            cursor.style.left = x + 'px';
            cursor.style.top = y + 'px';
        };

        link.forEach(b => b.addEventListener('mousemove', animateit));
        link.forEach(b => b.addEventListener('mouseleave', animateit));
        window.addEventListener('mousemove', editCursor);
    })();
</script>
</body>