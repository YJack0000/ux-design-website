<template>
    <div class="mb-20">
        <div class="mx-auto max-w-screen-sm text-center mb-8 lg:mb-16">
            <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">
                Homeworks
            </h2>
        </div>
        <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
            <HomeworkCard title="Contextual Inquiry" description="A method of collecting information about how people use a product or service">
                <CI />
            </HomeworkCard>
            <HomeworkCard title="Affinity Diagram" description="A collection of large amounts of data that is organized into groups or themes based on their relationships">Ｆ
                <AD />
            </HomeworkCard>
            <HomeworkCard title="User Persona" description="A fictional character created to represent a user type that might use a site, brand, or product in a similar way">
                <UP />
            </HomeworkCard>
            <HomeworkCard title="lofi Prototype" description="A rough draft version of a product used to quickly get feedback from users">
                <LP />
            </HomeworkCard>
            <HomeworkCard title="Revision Plan" description="A plan to revise your lofi prototype">
                <RP />
            </HomeworkCard>
            <HomeworkCard title="Heuristic Evaluation" description="A method of identifying usability problems in a software product or website">
                <HE />
            </HomeworkCard>
        </div>
    </div>
</template>
<script setup>
import HomeworkCard from '@/components/homeworks/HomeworkCard.vue'
import CI from '@/components/homeworks/CI.vue'
import AD from '@/components/homeworks/AD.vue'
import UP from '@/components/homeworks/UP.vue'
import LP from '@/components/homeworks/LP.vue'
import RP from '@/components/homeworks/RP.vue'
import HE from '@/components/homeworks/HE.vue'
</script>
