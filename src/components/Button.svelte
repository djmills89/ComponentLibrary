<script lang="ts">
    export let borderSize: string = '1px';
    export let borderType: string = 'solid';
    export let borderColor: string = 'var(--rhythm-blue)';
    export let borderRadius: string | number = '2rem';
    export let fontSize: string = '1rem';
    export let paddingBlock: string = '1rem';
    export let paddingInline: string = '2rem';
    export let backgroundColor: string = 'transparent';
    export let cursorType: string = 'pointer';
    export let buttonType: 'button' | 'submit' | 'reset' = 'button';
    export let hover: boolean = false;

    //convert borderRadius to px if only a number is passed to the prop
    $: borderRadiusValue = typeof borderRadius === 'number' ? `${borderRadius}px` : borderRadius;
    $: hoverStyle = hover

    $: buttonStyle = `
        border: ${borderSize} ${borderType} ${borderColor};
        border-radius: ${borderRadiusValue};
        background-color: ${backgroundColor};
        font-size: ${fontSize};
        padding-block: ${paddingBlock};
        padding-inline: ${paddingInline};
        cursor: ${cursorType};
    `;
</script>

<button
    class:hover-enabled={hover}
    style={buttonStyle}
    type={buttonType}
    {...$$restProps}
    >
    <slot>Click Here!</slot>
</button>

<style>
    .hover-enabled {
        transition: background-color .5s ease, color .5s ease;
    }

    .hover-enabled:hover {
        background-color: var(--rhythm-blue) !important;
        color: var(--primary-text) !important;
    }
</style>