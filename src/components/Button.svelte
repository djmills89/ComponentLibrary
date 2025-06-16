<script lang="ts">
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

    //convert borderRadius to px if only a number is passed to the prop
    $: borderRadiusValue = typeof borderRadius === 'number' ? `${borderRadius}px` : borderRadius;

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
    style={buttonStyle}
    type={buttonType}
    {...$$restProps}
    >
    <slot>Click Here</slot>
</button>