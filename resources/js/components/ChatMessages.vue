<template>
    <ul class="chat">
        <li v-for="message in messages" :key="message.id" class="chat-body clearfix">
            <div v-bind:class="{'float-right': message.user.id == user.id}">
                <div class="header" >
                    <strong 
                        class="primary-font" 
                        v-bind:class="{'float-right': message.user.id == user.id}"
                    >
                        {{ message.user.name }}
                    </strong>
                </div>
                <p v-bind:class="{'float-right': message.user.id == user.id}">
                    {{ message.message }}
                </p>
            </div>
        </li>
    </ul>
</template>

<script>
    export default {
        props: ['messages', 'user']
    };
</script>
