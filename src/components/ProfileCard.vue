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
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ullam expedita ut quibusdam accusamus
                </p>
            </div>
        </div>
        <div class="container_achievements">
            <h2>Achievements</h2>
            <div class="achievements">
                <span>achievements</span>
                <span>achievements</span>
                <span>achievements</span>
            </div>
        </div>
        <div class="container_insignia">
            <h2>insignia</h2>
            <div class="insignia">
                <span>insignia</span>
                <span>insignia</span>
                <span>insignia</span>
            </div>
        </div>
        <div class="container_infos">
            <span>info</span>
            <span>info</span>
            <span>info</span>
        </div>
        <div class="container_friends">
            <h2>Friends</h2>
            <div class="friend">
                <span>friend_avatar</span>
                <span>friend_name</span>
            </div>

            <div class="friend">
                <span>friend_avatar</span>
                <span>friend_name</span>
            </div>

        </div>
    </div>
</template>

<style lang="less">
@import "../variables.less";

#Container_profile {
    display: flex;
    justify-content: space-between;
    gap: 24px;
    width: 100%;
    .background_glass();
    border-radius: @border_radius;
    padding: 24px;

    h2 {
        .format_title_card();
    }

    span {
        .format_description();
    }


    .profile {
        display: flex;
        align-items: center;
        gap: 8px;

        .profile_avatar {

            h1 {
                .format_title();
                margin-top: 16px;
            }

            img {
                border-radius: @border_radius;
                width: 160px;
                height: 150px;
                .backgroundCard_glass();
            }
        }

        .profile_status {
            display: flex;
            flex-direction: column;
            gap: 15px;
            height: 100%;

            .status_rewards {
                display: flex;
                gap: 8px;
            }
        }

    }

    .container_achievements {
        display: flex;
        flex-direction: column;
        gap: 15px;


        .achievements {
            display: flex;
            gap: 8px;
        }

    }

    .container_insignia {
        display: flex;
        flex-direction: column;
        gap: 15px;

        .insignia {
            display: flex;
            gap: 8px;
        }
    }

    .container_infos {
        display: flex;
        flex-direction: column;
        gap: 8px;
    }

    .container_friends {
        display: flex;
        flex-direction: column;
        gap: 15px;

        .friend {
            display: flex;
            gap: 8px;
        }
    }

    @media (min-width: 1380px) {
        width: 800px;
        flex-direction: column;
    }
}
</style>
