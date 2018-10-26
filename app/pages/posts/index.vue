<!ｰｰ
/**
 * pages/posts/index.vue
 * 投稿一覧ページ
 * 「Nuxt.jsビギナーズガイド」Chapter04
 * Copyright (C) 2018 J.Kawahara
 * 2018.10.26 J.Kawahara 新規作成
 */
ｰｰ>

<template>
    <section class="container posts-page">
        <el-card>
            <div slot="header" class="clearfix">
                <span>新規投稿</span>
            </div>
            <el-table
                :data="showPosts"
                style="width: 100%"
                class="table">
                <el-table-column prop="title" label="タイトル"></el-table-column>
                <el-table-column prop="user.id" label="投稿者" width="180"></el-table-column>
                <el-table-column prop="created_at" label="投稿日時" width="240"></el-table-column>
            </el-table>
        </el-card>
    </section>
</template>

<script>
export default {
    computed: {
        showPosts() {
            return [
                {
                    id: '001',
                    title: 'How to development Nuxt.js Application',
                    body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit...',
                    created_at: '2018/10/26 09:13:00',
                    user: {
                        id: 'riverone'
                    }
                },
                {
                    id: '002',
                    title: 'Development Nuxt.js Application to Heroku',
                    body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit...',
                    created_at: '2018/10/26 09:14:00',
                    user: {
                        id: 'riverone'
                    }
                }
            ]
        }
    }
}
</script>

<style>
.posts-page .el-table__row {
    cursor: pointer;
}
</style>
