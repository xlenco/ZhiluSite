<script setup lang="ts">
useHead({ title: '' })
definePageMeta({
    alias: ['/'],
    title: '主页',
})
const appConfig = useAppConfig()
</script>

<template>
    <ZLAvatar class="avatar" />
    <div class="wrapper">
        <ZField label="<span style='font-size: 3rem;'>👋</span>">
            <h1 style="font-size: 3rem;">
                你好，<br>我是<mark>{{ appConfig.author.name }}</mark>
            </h1>
            <p class="desc">
                {{ appConfig.description }}
            </p>
            <div>
                <ZButton icon="ph:files-duotone" to="https://blog.xlenco.top/">
                    博客
                </ZButton>
                <ZButton icon="ph:github-logo-duotone" to="https://github.com/xlenco">
                    GitHub
                </ZButton>
            </div>
        </ZField>

        <ZField label="介绍">
            <p>
                 一名菜菜的高中生
            </p>
        </ZField>

<!-- 
        <ZField label="近期活动">
            <p>
                7 月完善<ZLink to="https://wiki.cooo.site/">
                    西邮Wiki
                </ZLink>，8 月使用 Nuxt Content 重构了<ZLink to="https://blog.zhilu.cyou/">
                    个人博客
                </ZLink>，但还未完成。
            </p>
        </ZField>

        <ZField label="关于主页">
            <p>
                使用来自纸鹿的个人主页模板，基于 Vue 3.x 和 Nuxt 2.x 构建。<br>
            </p>
            <p>
                <ZLink to="https://github.com/L33Z22L11/homepage-v5" icon="ph:github-logo-duotone">
                    L33Z22L11/homepage-v5
                </ZLink>上。
            </p>
        </ZField>

        -->
    </div>
</template>

<style scoped lang="scss">
.avatar {
    position: fixed;
    opacity: 0.2;
    top: 0;
    right: 20vw;
    margin-right: -0.4em;
    font-size: min(100vw, 60vh);
    z-index: -1;
}

.desc {
    margin: 1rem 0;
    font-size: 1.5rem;
    color: var(--c-text-2);
}
</style>
