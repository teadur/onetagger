<template>
    <q-item style='padding-top: 0px; padding-bottom: 0px;'>
        <q-item-section>
            <q-item-label>
                {{label}}
                <q-icon name='mdi-help-circle-outline text-grey-6' class='q-mx-sm' v-if='tooltip'>
                    <q-tooltip content-style="font-size: 13px">
                        {{tooltip}}
                    </q-tooltip>
                </q-icon>
            </q-item-label>
        </q-item-section>
        <q-item-section avatar>
            <q-toggle :value='value' @input='$emit("input", $event)'></q-toggle>
        </q-item-section>
    </q-item>
</template>

<script>
export default {
    name: 'AdvancedSettingsToggle',
    props: {
        label: String,
        tooltip: {
            type: String,
            default: null
        },
        value: Boolean
    }
}
</script>