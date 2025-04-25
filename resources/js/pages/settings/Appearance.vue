<script setup lang="ts">
import { Head } from '@inertiajs/vue3';

import AppearanceTabs from '@/components/AppearanceTabs.vue';
import HeadingSmall from '@/components/HeadingSmall.vue';
import { type BreadcrumbItem } from '@/types';

import AppLayout from '@/layouts/AppLayout.vue';
import SettingsLayout from '@/layouts/settings/Layout.vue';

const breadcrumbItems: BreadcrumbItem[] = [
    {
        title: 'Apariencia',
        href: '/settings/appearance',
    },
];
</script>

<template>
    <AppLayout :breadcrumbs="breadcrumbItems">
        <Head title="Configurarcion de apariencis" />

        <SettingsLayout>
            <div class="space-y-6">
                <HeadingSmall title="Apariencia" description="Actualiza la apariencia a tu gusto" />
                <AppearanceTabs />
            </div>
        </SettingsLayout>
    </AppLayout>
</template>
