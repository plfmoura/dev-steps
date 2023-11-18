<template>
    <div class="card">
        <Timeline :value="events" align="alternate" class="customized-timeline">
            <template #content="slotProps">
                <Card style="background-color: #212121;">
                    <template #title>
                        {{ slotProps.item.status }}
                    </template>
                    <template #subtitle>
                        {{ slotProps.item.date }}
                    </template>
                    <template #content>
                        <img v-if="slotProps.item.image" :src="`https://primefaces.org/cdn/primevue/images/product/${slotProps.item.image}`" :alt="slotProps.item.name" width="200" class="shadow-1" />
                        <p>
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Inventore sed consequuntur error repudiandae numquam deserunt quisquam repellat libero asperiores earum nam nobis, culpa ratione quam perferendis esse, cupiditate
                            neque quas!
                        </p>
                        <div class="align-card-actions">
                            <Button label="Read more" rounded severity="info" outlined></Button>
                            <Button icon="pi pi-heart" severity="help" rounded outlined aria-label="Favorite" />
                        </div>
                    </template>
                </Card>
            </template>
        </Timeline>
    </div>
</template>

<script >
import Timeline from 'primevue/timeline';
import Card from 'primevue/card';
import Button from 'primevue/button';
import { ref } from "vue";

const events = ref([
    { status: 'Search', date: '15/10/2020 10:30', icon: 'pi pi-shopping-cart', color: '#9C27B0'},
    { status: 'Roadmap', date: '15/10/2020 14:00', icon: 'pi pi-cog', color: '#673AB7' },
    { status: 'Networking', date: '15/10/2020 16:15', icon: 'pi pi-shopping-cart', color: '#FF9800' },
    { status: 'Portfolio projects', date: '16/10/2020 10:00', icon: 'pi pi-check', color: '#607D8B' }
]);

export default {
    components: {
        Timeline,
        Card,
        Button
    },
    setup() {
        return {
            events
        }
    }
}

</script>

<style lang="scss" scoped>
.align-card-actions {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
    margin-top: 1rem;
}

@media screen and (max-width: 960px) {
    ::v-deep(.customized-timeline) {
        .p-timeline-event:nth-child(even) {
            flex-direction: row !important;

            .p-timeline-event-content {
                text-align: left !important;
            }
        }

        .p-timeline-event-opposite {
            flex: 0;
        }

        .p-card {
            margin-top: 1rem;
        }
    }
}
</style>