<script>
	import { Input, Label, Button } from 'flowbite-svelte';
	import firebase from 'firebase/compat/app';
	import 'firebase/compat/auth';
	const firebaseConfig = {
		apiKey: 'AIzaSyDfM2HpyJJhO867B3IhrSN25qVtiUPD7IU',
		authDomain: 'taskmanager-711e2.firebaseapp.com',
		projectId: 'taskmanager-711e2',
		storageBucket: 'taskmanager-711e2.appspot.com',
		messagingSenderId: '806379840282',
		appId: '1:806379840282:web:bff528fae46d07893242a3',
		measurementId: 'G-2BK5EGKDMF'
	};
	firebase.initializeApp(firebaseConfig);
	const auth = firebase.auth();
	let email = '';
	let password = '';
	function dummyFn(e) {
		e.preventDefault();
		auth
			.signInWithEmailAndPassword(email, password)
			.then((userCredential) => {
				// Redirect to another page on successful login
				window.location.href = '/taskManager';
			})
			.catch((error) => {
				// Handle login error
				console.log(error);
			});
	}
</script>

<div class="w-96 mt-12 m-auto p-4 border">
	<form>
		<Label class="space-y-2">
			<span>Email</span>
			<Input type="email" placeholder="Default input" size="md" bind:value={email} />
		</Label>
		<Label class="space-y-2">
			<span>Password</span>
			<Input type="password" placeholder="Default input" size="md" bind:value={password} />
		</Label>
		<Button on:click={dummyFn} class="mt-4">Submit</Button>
	</form>
</div>
