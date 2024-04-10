<script>
export default {
    data() {
        return {
            //   src: 'vite.svg'
        }
    }
}
</script>

<template>
    <section class="page-footer">
        <div class="container">
            <div class="row">
                <div>
                    <h4>Boolando S.r.l.</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                </div>
                <div>
                    <p>Trovaci anche su</p>
                    <ul class="flex">
                        <li>X</li>
                        <li>F</li>
                        <li>I</li>
                        <li>P</li>
                        <li>YT</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.page-footer {
    background-color: black;
    color: white;
    padding: 16px 0;
}

.row {
    justify-content: space-between;

    ul {
        gap: 20px;
    }
}
</style>