<template>
  <div>
    <app-header></app-header>
    <login-form></login-form>
    <!-- TODO: AppFooter 컴포넌트를 표시해보세요 -->
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import LoginForm from './components/LoginForm.vue';
import AppFooter from './components/AppFooter.vue';

export default {
	components: {
		'app-header': AppHeader,
    'login-form': LoginForm,
    'app-footer': AppFooter,
	},
};
</script>
