<script>
    import Button from "../components/Button.svelte";
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>
<Button hover></Button>
<p><strong>Buttons</strong> have the following predefined styles:</p>

<figure>
    <pre><code>
    borderSize: string = '1px';
    borderType: string = 'solid';
    borderColor: string = 'blue';
    borderRadius: string | number = '2rem';
    fontSize: string = '1rem';
    paddingBlock: string = '1rem';
    paddingInline: string = '2rem';
    backgroundColor: string = 'transparent';
    cursorType: string = 'pointer';
    buttonType: 'button' | 'submit' | 'reset' = 'button';
    </code></pre>
</figure>

<p>
  All typical HTML attributes like <code>disabled</code> and <code>aria-*</code> can be added to the <code>&lt;Button&gt;</code> component.
</p>

<p>
    The predefined styles are defaults that can be over-ridden by passing them as a prop to the component.
</p>

<figure>
    <figcaption>Example of a prop being used with the component</figcaption>
    <pre><code>
    &lt;Button borderSize="2rem" &gt;
    </code></pre>
</figure>

<p>
  If a number is passed to <code>borderRadius</code>, the component assumes pixel sizing.
</p>

<p>
  Once color themes are added, you’ll be able to pass theme color names (e.g., <code>'primary'</code>) to color props for consistency across your UI.
</p>


<style>
    figure {
        background-color: lightgray;
        width: 50%;
        padding: 1rem;
    }
</style>