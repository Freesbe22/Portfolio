<script setup>
</script>

<template>
    <li class="list-group-item clearfix d-flex no-block my-1 text-light ">
        <div class="my-auto" style="max-width: 5rem;">
            <slot name="Image"></slot>
        </div>

        <div class=" ps-2">
            <h3 class="list-group-item-heading">
                <slot name="Title"></slot>
            </h3>
            <p class="list-group-item-text lead">

                <slot name="Content"></slot>
            </p>
        </div>
        <div class="ms-auto my-auto text-muted ">
            <h6></h6>
        </div>
    </li>
</template>
