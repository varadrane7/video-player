<script>
	// @ts-nocheck

	export let form;
</script>

<div class="flex-flex-col items-center h-full w-full">
	<h2 class="mt-2 text-center text-3xl font-bold tracking-tight text-base-content">
		Log In to your Account
	</h2>
	<p class="text-center mt-1">
		Or <a href="/register" class="text-primary font-medium hover:cursor-pointer hoiver:underline"
			>register</a
		> if you are a new user.
	</p>
	<form action="?/login" method="post" class="flex flex-col items-center space-y-2 w-full pt-4">
		<div class="form-control w-full max-w-md">
			<label for="email" class="label font-medium pb-1">
				<span class="label-text">Email</span>
			</label>
			<input type="email" name="email" class="input input-bordered w-full max-w-fd" />
		</div>
		<div class="form-control w-full max-w-md">
			<label for="password" class="label font-medium pb-1">
				<span class="label-text">Password</span>
			</label>
			<input type="passowrd" name="password" class="input input-bordered w-full max-w-fd" />
		</div>
		<div class="w-full max-w-md">
			<a
				class="text-primary font-medium hover:cursor-pointer hoiver:underline"
				href="/reset-password">Forgot Password ?</a
			>
		</div>
		<div class="w-full max-w-md pt-2">
			<button type="submit" class="btn btn-primary w-full">Login</button>
		</div>

		{#if form?.notVerified}
			<div class="alert alert-success shadow-lg w-full max-w-md">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="stroke-current shrink-0 h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					><path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z"
					/></svg
				>
				<span>Verify your email before logging in.</span>
			</div>
		{/if}
	</form>
</div>
