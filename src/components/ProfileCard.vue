<script setup lang="ts"></script>

<template>
    <div id="Container_profile">
        <div class="profile">
            <div class="profile_avatar">
                <img src="https://pt.quizur.com/_image?href=https://img.quizur.com/f/img637e1ff08f6e90.51513695.png?lastEdited=1669210099&w=600&h=600&f=webp"
                    alt="avatar" />
                <h1>Haru Moon</h1>
            </div>
            <div class="profile_status">
                <span>Playing...</span>
                <div class="status_rewards">
                    <span>Badge</span>
                    <span>Badge</span>
                    <span>Badge</span>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="less">
@import "../variables.less";

#Container_profile {
    display: flex;
    gap: 4px;
    height: 150px;
    width: 100%;
    .background_glass();
    border-radius: @border_radius;
    padding: 8px;

    .profile {
        display: flex;
        align-items: center;
        gap: 8px;

        .profile_avatar {
            text-align: center;

            h1 {
                .format_title();
                margin-top: 6px;
            }

            img {
                border-radius: @border_radius;
                width: 100px;
                height: 100px;
            }
        }

        .profile_status {
            display: flex;
            flex-direction: column;
            gap: 6px;
            height: 100%;

            .status_rewards {
                display: flex;
                gap: 4px;
            }
        }
    }
}
</style>
