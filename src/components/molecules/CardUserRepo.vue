<template>
    <ScrollVertical>
        <ul class="container">
            <li v-for="repo in 20" :key="repo">
                <article class="user-repo">
                    <ul class="repo-icons">
                        <li class="repo-icon">
                            <icon name="heartOutline" class="icon-like"/>
                        </li>
                        <li class="repo-icon">
                            <icon name="starOutline" size="28" />
                            <span>15</span>
                        </li>
                        <li class="repo-icon">
                            <icon name="sourceFork" />
                            <span>15</span>
                        </li>
                    </ul>
                    <div class="repo-content">
                        <ImageCircle 
                            class="user-avatar"
                            src="https://github.com/samuelCupertino.png" 
                            alt="foto do proprietario do repositorio" 
                            size="60px"
                        />
                        <Title fontSize="12pt" color="var(--textSecondary)">Titleooo</Title>
                        <Text fontSize="10pt" color="var(--textTertiary)">But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness..</Text>
                    </div>
                </article>
            </li>
        </ul>
    </ScrollVertical>
</template>

<script>
    import Icon from '../atoms/Icon.vue'
    import ScrollVertical from '../atoms/ScrollVertical.vue'
    import Title from '../atoms/Title.vue'
    import Text from '../atoms/Text.vue'
    import ImageCircle from '../atoms/ImageCircle.vue'

    export default {
        name: 'CardUserRepo',
        props: {
            margin: {
                type: String,
                default: '0'
            }
        },
        components: {
            Icon,
            ScrollVertical,
            Title,
            Text,
            ImageCircle
        }
    }
</script>

<style scoped>
    .container {
        display: grid;
        gap: 20px;
        grid-template-columns: repeat(auto-fill, minmax(min(100%, 240px), 1fr));
    }

    .user-repo {
        min-width: 220px;
        display: flex;
        flex-direction: column;
        gap: 10px;
        padding: 10px;
        border-radius: 15px;
        border: 1px solid transparent;
        background-color: var(--bgTertiary);
        background-image: linear-gradient(135deg, var(--bgSecondary), var(--primary), var(--secondary), var(--bgSecondary));
        background-size: 100% 0%;
        background-repeat: no-repeat;
        background-position: bottom;
        transition-duration: 0.5s;
    }
    .user-repo:hover {
        background-size: 100% 100%;
        border-color: var(--secondary);
    }

    .repo-icons {
        display: flex;
        align-items: center;
        gap: 15px;
        color: var(--tertiary);
        transition: 1s;
    }
    .user-repo:hover .repo-icons {
        color: var(--bgSecondary);
    }
    .repo-icon {
        display: flex;
        align-items: center;
        gap: 3px;
        font-weight: bolder;
        cursor: default;
    }
    .repo-icon .icon-like {
        color: var(--textTertiary);
        cursor: pointer;
        transition: 0.5s;
    }
    .repo-icon .icon-like:hover {
        color: var(--secondary);
        transform: scale(1.25);
    }

    .repo-content {
        background-image: linear-gradient(200deg, var(--bgPrimary) 30%, rgb(0 0 0 / 40%));
        padding: 10px;
        border-radius: 10px;
    }
    .user-avatar {
        margin-left: auto;
        display: block;
        margin-top: -60px;
        transform: translateY(25px);
        border: 5px solid var(--bgPrimary);
        box-sizing: border-box;
    }
</style>
