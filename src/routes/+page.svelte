<script>
    import Button from "../components/Button.svelte";
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>
<Button></Button>
<p><strong>Buttons</strong> have the following predefined styles:</p>

<pre><code>
export let borderSize: string = '1px';
export let borderType: string = 'solid';
export let borderColor: string = 'blue';
export let borderRadius: string | number = '2rem';
export let fontSize: string = '1rem';
export let paddingBlock: string = '1rem';
export let paddingInline: string = '2rem';
export let backgroundColor: string = 'transparent';
export let cursorType: string = 'pointer';
export let buttonType: 'button' | 'submit' | 'reset' = 'button';
</code></pre>

<p>
  All typical HTML attributes like <code>disabled</code> and <code>aria-*</code> can be added to the <code>&lt;Button&gt;</code> component.
</p>

<p>
  If a number is passed to <code>borderRadius</code>, the component assumes pixel sizing.
</p>

<p>
  Once color themes are added, you’ll be able to pass theme color names (e.g., <code>'primary'</code>) to color props for consistency across your UI.
</p>
