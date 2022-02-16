<template>
    <ScrollVertical>
        <ul class="profile-repos">
            <li v-for="repo in 20" :key="repo">
                <article class="repo">
                    <Title fontSize="12pt" color="var(--textSecondary)">Titleooo</Title>
                    <Text color="var(--textTertiary)">Description Description Description Description Description Description.</Text>
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

    export default {
        name: 'UserProfileRepos',
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
            Text
        }
    }
</script>

<style scoped>
    .profile-repos {
        display: flex;
        flex-direction: column;
    }

    .repo {
        background-color: var(--bgTertiary);
        padding: 10px;
        border-radius: 10px;
        margin: 5px 0px;
        border: 1px solid var(--bgTertiary);
        transition-duration: 0.5s;
    }    
    .repo:hover {
        border-color: var(--secondary);
    }

    .repo-title {
        color: var(--textSecondary);
        margin-bottom: 5px;
    }
    .repo-desc {
        color: var(--textTertiary);
    }
</style>
