<template>
    <div id='login'>
        <PasswordReset v-if='showPasswordReset' @close='togglePasswordReset()'></PasswordReset>
        <section>
            <div class="col1">
                <h1>ReveilleRecruiter</h1>
            </div>
            <div :class="{ 'signup-form': !showLoginForm }" class="col2">
                <form v-if='showLoginForm' @submit.prevent>
                    <h1>Welcome Back.</h1>
                    <div>
                        <label for="email1">Email</label>
                        <input v-model.trim="loginForm.email" type="text" placeholder="you@email.com" id="email1" />
                    </div>
                    <div>
                        <label for="password1">Password</label>
                        <input v-model.trim="loginForm.password" type="password" placeholder="******" id="password1" />
                    </div>
                    <button @click='signup()' class="button">Sign Up</button>
                     
                </form>
            </div>        
        </section>
    </div>
</template>
