<template>
    <Layout>
        <div class="post-title">
            <h1 class="post-title__text">
                {{ $page.post.title }}
            </h1>

        </div>

        <div class="post content-box">
            <div class="post__header">
            </div>

            <div class="post__content" v-html="$page.post.content" />

            <div class="post__footer">
            </div>
        </div>

        <div class="post-comments">
            <!-- Add comment widgets here -->
        </div>
    </Layout>
</template>

<script>
    export default {
        metaInfo() {
            return {
                title: this.$page.post.title,
                meta: [{
                    name: 'description',
                    content: this.$page.post.content
                }]
            }
        }
    }
</script>

<page-query>
query {
  allPosts {
    title
    content
    slug
  }
}
</page-query>

<style lang="scss">
    .post-title {
        padding: calc(var(--space) / 2) 0 calc(var(--space) / 2);
        text-align: center;
    }

    .post {

        &__header {
            width: calc(100% + var(--space) * 2);
            margin-left: calc(var(--space) * -1);
            margin-top: calc(var(--space) * -1);
            margin-bottom: calc(var(--space) / 2);
            overflow: hidden;
            border-radius: var(--radius) var(--radius) 0 0;

            img {
                width: 100%;
            }

            &:empty {
                display: none;
            }
        }

        &__content {
            h2:first-child {
                margin-top: 0;
            }

            p:first-of-type {
                font-size: 1.2em;
                color: var(--title-color);
            }

            img {
                width: calc(100% + var(--space) * 2);
                margin-left: calc(var(--space) * -1);
                display: block;
                max-width: none;
            }
        }
    }

    .post-comments {
        padding: calc(var(--space) / 2);

        &:empty {
            display: none;
        }
    }

    .post-author {
        margin-top: calc(var(--space) / 2);
    }
</style>