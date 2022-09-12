<script>
	import { enhance } from '$app/forms';
</script>

<form use:enhance={({ form, data, cancel }) => {
	console.log(Object.fromEntries(data));
	cancel(); // Cancel HTTP call
}}>
	<label>
		<strong>Name</strong>
		<input name="firstname" placeholder="First name">
	</label>
	<label>
		<strong>Favorite variable</strong>
		<select name="variable">
			<option value="">Select...</option>
			<option>foo</option>
			<option>bar</option>
			<option>baz</option>
			<option>quo</option>
		</select>
	</label>
	<label>
		<strong>Bio</strong>
		<textarea name="bio" placeholder="About you"/>
	</label>
	<p>Submit and check console</p>
	<input type="submit" />
</form>