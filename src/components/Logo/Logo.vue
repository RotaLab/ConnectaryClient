<template>
    <div class="logo" :class="`logo--${ variant }`">
        <img class="logo__symbol" src="@/assets/images/logo_symbol.svg" alt="Logo do Connectary">
        <h1 class="logo__title">
            <span class="blue">Connect</span>
            <span class="pink">ary</span>
        </h1>
    </div>
</template>

<script>

export default {
    name: 'Logo',
    props: {
        variant: String
    }
}
</script>

<style lang="scss" scoped>
    .logo {
        display: inline-flex;
        align-items: center;
        color: white;

        &__symbol {
            width: 50px;
            margin-right: spacing(1);
        }

        &__title {
            font-size: 32px;
            margin-bottom: 4px;

            .blue {
                color: $color-blue;
                font-weight: $font-weight-medium;
            }

            .pink {
                color: $color-pink;
                font-weight: $font-weight-light;
            }
        }

        &--blue {
            color: $color-blue;
        }
    }
</style>