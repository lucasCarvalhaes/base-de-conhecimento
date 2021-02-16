<template>
    <div class="user-dropdown">
        <div class="user-button">
            <span class="d-none d-sm-block">{{ user.name }}</span>
            <div class="user-dropdown-img">
                <Gravatar :email="user.email" alt="User" />
            </div>
            <i class="fa fa-angle-down"></i>
        </div>
    </div>
</template>

<script>
import { mapState } from 'vuex'
import Gravatar from 'vue-gravatar'

export default {
    name: 'UserDropdown',
    components: { Gravatar },
    computed: mapState(['user'])
}
</script>

<style>
    .user-dropdown {
        height: 100%;
    }

    .user-button {
        display: flex;
        align-items: center;
        color: #fff;
        font-weight: 100;
        height: 100%;
    }
</style>