// ウェルカムオファー_コーチ
<template>
    <v-ons-page>
        <v-ons-toolbar class="practice-toolbar">
            <div class="left">
                <v-ons-back-button>
                    <v-ons-icon modifier="outline" size="30px" icon="md-close, material:md-close-outline"></v-ons-icon>
                </v-ons-back-button>
            </div>
            <!-- </v-ons-col> -->
            <div class="center">
                <p class="toolbar-title">参加者</p>
            </div>
        </v-ons-toolbar>
        <v-ons-card class="card-item" style="margin-top: 2.9rem; padding-top: 0.2rem">
            <v-ons-list>
                <v-ons-list-item class="player-list-title">
                    参加選手一覧({{this.participating_players_list.length}})
                </v-ons-list-item>
                <v-ons-list-item v-for="(player, index) in participating_players_list" :key="index"
                    class="player-list-item"  tappable="true"
                >
                    <img :src="player.avatar_src" alt="" width="32rem" height="32rem" class="avatar-md">
                    <span style="margin-left: 1rem">{{player.name}}</span>
                </v-ons-list-item>
            </v-ons-list>
        </v-ons-card>
        <v-ons-bottom-toolbar class="tool_bottom">
            <div class="tab-bottom">
                <div style="text-align: center">
                <v-ons-button modifier="quiet">
                <span style="width: 18px; height: 18px; margin: 3px;" class='material-icons'>event_note</span>
                <p style="margin: -10px; font-weight: bold;font-size: 10px;">サマリー</p>
                </v-ons-button>
                </div>
                <div style="text-align: center">
                <v-ons-button modifier="quiet" style="color:#8293A3;">
                    <span style="width: 18px; height: 18px; margin: 3px;" class='material-icons'>menu_book</span>
                    <p style="margin: -10px; font-weight: bold; font-size: 10px;">スイムノート</p>
                </v-ons-button>
                </div>
            </div>
        </v-ons-bottom-toolbar>
    </v-ons-page>
</template>

<script>

export default {
    name: "practice3",
    data: function() {
        return {

        }
    },
    components: {
    },
    props: {
        "participating_players_list": {
            type: Array,
            default: ()=>[
                {"name":"吉田 花子", "avatar_src":"static/images/swimmer/swimmer01.jpg"},
                {"name":"斎藤 優子", "avatar_src":"static/images/swimmer/swimmer02.jpg"},
                {"name":"村田 隆", "avatar_src":"static/images/swimmer/swimmer03.jpg"},
                {"name":"吉岡 太朗", "avatar_src":"static/images/swimmer/swimmer04.jpg"},
                {"name":"宮下優子", "avatar_src":"static/images/swimmer/swimmer05.jpg"},
                {"name":"佐藤義行", "avatar_src":"static/images/swimmer/swimmer06.jpg"},
                {"name":"村上晴之助", "avatar_src":"static/images/swimmer/swimmer07.jpg"},
                {"name":"鈴木竜也", "avatar_src":"static/images/swimmer/swimmer08.jpg"},
                {"name":"池江璃花子", "avatar_src":"static/images/swimmer/swimmer09.jpg"},
                {"name":"吉田 花子", "avatar_src":"static/images/swimmer/swimmer01.jpg"},
                {"name":"斎藤 優子", "avatar_src":"static/images/swimmer/swimmer02.jpg"},
                {"name":"村田 隆", "avatar_src":"static/images/swimmer/swimmer03.jpg"},
                {"name":"吉岡 太朗", "avatar_src":"static/images/swimmer/swimmer04.jpg"},
                {"name":"宮下優子", "avatar_src":"static/images/swimmer/swimmer05.jpg"},
                {"name":"佐藤義行", "avatar_src":"static/images/swimmer/swimmer06.jpg"},
                {"name":"村上晴之助", "avatar_src":"static/images/swimmer/swimmer07.jpg"},
                {"name":"鈴木竜也", "avatar_src":"static/images/swimmer/swimmer08.jpg"},
                {"name":"池江璃花子", "avatar_src":"static/images/swimmer/swimmer09.jpg"},
            ]
        },
    },
    computed: {
    },
    methods: {
    }
}
</script>

<style scoped>
    .practice-toolbar {
        margin: 0 0 0.5rem 0;
        padding: 3rem 0 0 0;
        text-align: center;
        align-items: center;
        border-radius: 0;
        background-color: white;
        height: 88px;
    }
    .toolbar-title {
        font-family: "Noto Sans JP";
        font-style: normal;
        font-weight: bold;
        font-size: 18px;
        color: #303235;
        margin-bottom: 0;
        height: 2.5rem;
    }
    .toolbar-sub-title {
        font-family: "SF Pro Display";
        font-style: normal;
        font-weight: normal;
        font-size: 11px;
        line-height: 13px;
        text-align: center;
        margin-top: 0;
        height: 2rem;
    }
    .card-item {
        text-align: center;
        margin: 0.2rem 0 0 0;
        width: 100%;
        padding: 0.5rem;
        border-radius: 0.1rem;
    }
    .player-list-title {
        font-family: "Noto Sans CJK JP";
        font-style: normal;
        font-weight: bold;
        font-size: 12px;
        line-height: 150%;
        display: flex;
        align-items: center;
        color: #193342;
    }
    .player-list-item {
        font-family: "Noto Sans JP";
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 150%;
        color: #303235;
    }
    .avatar-md {
        border-radius: 50%;
    }
    .tab-bottom {
        display: flex;
        justify-content: space-around;
        padding-top: 1rem;
        padding-bottom: 2rem;
        background: white;
        border-top: 1px solid lightgray;
        border-top-left-radius: 0.5rem;
        border-top-right-radius: 0.5rem;
    }
    .tool_bottom{
        height: 82px;
        padding: 0px 40px;
    }
</style>