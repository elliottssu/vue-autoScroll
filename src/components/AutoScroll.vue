<template>
  <div class="auto-scroll-container" @mouseover="over()" @mouseout="out()">
    <div class="auto-scroll-wapper">
      <slot name="autoScroll"/>
    </div>
    <div class="auto-scroll-next-wapper"/>
  </div>
</template>

<script>
    export default {
        name: 'AutoScroll',
        props: {
            speed: {
                type: Number,
                default: 30
            }
        },
        data() {
            return {
                timer: null,
                n: null,
                p1: null
            };
        },
        mounted() {
            this.$nextTick(() => {
                setTimeout(() => {
                    this.scrollTimer();
                }, 500);
            });
        },
        methods: {
            scrollTimer() {
                this.n = document.querySelector('.auto-scroll-container').parentNode;
                this.p1 = document.querySelector('.auto-scroll-wapper');
                var p2 = document.querySelector('.auto-scroll-next-wapper');
                p2.innerHTML = this.p1.innerHTML;
                this.timer = setInterval(this.scroll, this.speed);
            },
            scroll() {
                this.n.scrollTop++;
                if (this.n.scrollTop >= this.p1.offsetHeight) {
                    this.n.scrollTop = 0;
                }
            },
            over() {
                clearInterval(this.timer);
            },
            out() {
                this.timer = setInterval(this.scroll, this.speed);
            }
        }
    };
</script>
