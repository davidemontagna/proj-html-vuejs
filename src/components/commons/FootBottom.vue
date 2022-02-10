<template>
    <section class="d-flex justify-content-between">
        <div class="d-flex justify-content-start align-items-center">
            <div>
                <img class="dm-logo-foot" src="../../assets/img/logos/logo-footer.png" alt="">
            </div>
            <div class="dm-rights mx-4">
                <span>
                    <i class="fa-regular fa-copyright"></i>
                    Copyright 2020. All Right Reserved.
                </span>
            </div>
        </div>
        <div class="dm-contact d-flex justify-content-end align-items-center">
            <div class="me-3">
                <a class="text-decoration-none" href="#"><i class="me-1 fa-solid fa-chevron-right"></i> FAQ's</a>
            </div>
            <div class="me-3">
                <a class="text-decoration-none" href="#"><i class="me-1 fa-solid fa-chevron-right"></i> Sitemap</a>
            </div>
            <div class="me-3">                
                <a class="text-decoration-none" href="#"><i class="me-1 fa-solid fa-chevron-right"></i> Contact Us</a>
            </div>
        </div>
        
    </section>
</template>

<script>
export default {
    name: 'FooterBottom',
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

section{
    padding: 25px 0;
}

.dm-logo-foot{
    height: 40px;
    opacity: 0.7;
}

.dm-rights, .dm-contact{
    font-size: 11px;
}

.dm-contact{
    div{
        a{
            color: $font-color-5;

            &:hover{
                color: $font-color-1;
            }
        }
    }
}
</style>