<template>
    <div class="favorite-like">
        <Icon class="icon-likes" name="heartOutline" size="48"/>
    </div>
    <ScrollVertical :margin="margin">
        <ul class="favorite-list">
            <li class="favorite-user" v-for="repo in 20" :key="repo" data-num="2">
                <ImageCircle src="https://github.com/samuelCupertino.png" alt="avatar do usuário" />
            </li>
        </ul>
    </ScrollVertical>
</template>

<script>
    import Icon from '../atoms/Icon.vue'
    import ScrollVertical from '../atoms/ScrollVertical.vue'
    import ImageCircle from '../atoms/ImageCircle.vue'  

    export default {
        name: 'FavoriteList',
        props: {
            margin: {
                type: String,
                default: '0'
            }
        },
        components: {
            Icon,
            ScrollVertical,
            ImageCircle,
        }
    }
</script>

<style scoped>
    .favorite-like {
        display: flex;
        justify-content: center;
    }
    .icon-likes {
        color: var(--primary);
        font-size: 28pt;
        cursor: pointer;
        transition: 1s;
    }
    .icon-likes:hover {
        color: var(--secondary);
    }

    .favorite-list {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 10px;
    }
    .favorite-user {
        width: 85%;
        cursor: pointer;
        border-radius: 50%;
        display: flex;
        border: 2px solid var(--primary);
        position: relative;
        transition: 0.5s;
    }
    .favorite-user:hover {
        border-color: var(--secondary);
    }
    .favorite-user::after {
        content: attr(data-num);
        color: var(--textTertiary);
        background-color: var(--primary);
        font-size: 11pt;
        font-weight: bolder;
        padding: 0px 3.5px;
        border-radius: 50rem;

        position: absolute;
        bottom: 0;
        right: 0;
        transition: 0.5s;
    }
    .favorite-user:hover::after {
        color: var(--bgTertiary);
        background-color: var(--secondary);
    }
</style>
