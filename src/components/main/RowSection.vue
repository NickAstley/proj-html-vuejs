<template>
    <!-- Questo componente stampa le section con una row ripetute per il layout del sito -->
    <section :class="sectionName">
        <div class="row justify-content-around align-items-center">
            <!-- In base alla prop passata da Main, stampo uno dei componenti figli. -->
            <UpgradeLife v-if="sectionName === `upgrade-life`"/>
            <!-- Insieme stampo sempre SectionInfo, che prende i dati dall'oggetto in data -->
            <SectionInfo :section-data="sectionData[sectionName]"/>
            <WorkCulture v-if="sectionName === `work-culture`"/>
            <PeopleHeartsUs v-if="sectionName === `people-hearts`"/>
        </div>
    </section>
</template>

<script>
    import SectionInfo from './RowSection/SectionInfo';
    import WorkCulture from './RowSection/WorkCulture'
    import UpgradeLife from './RowSection/UpgradeLife'
    import PeopleHeartsUs from './RowSection/PeopleHeartsUs'

    export default {
        components: {
            SectionInfo,
            WorkCulture,
            UpgradeLife,
            PeopleHeartsUs
        },
        props: {
            sectionName: String
        },
        data() {
            return {
                // Questo oggetto contiene i dati della colonna SectionInfo per ogni sezione. Ci accedo tramite la prop passata da Main.
                sectionData: {
                    "work-culture": {
                        subtitle: {
                            normal: "Everything in",
                            bold: "MaxCoach"
                        },
                        title: {
                            normal: [
                                "Learn about our",
                                "at MaxCoach"
                            ],
                            bold: "Work Culture"
                        },
                        p: [
                            "Spend some time to visit our website or head office and discover our current courses, enrollment procedure, and registration deadline. We're opening new classes every beginning of each month."
                        ],
                        span: "Have questions?",
                        link: {
                            text: "Get Free Guide",
                            color: "text-primary"
                        }      
                    },
                    "upgrade-life": {
                        subtitle: {
                            normal: "How we work"
                        },
                        title: {
                            normal: [
                                "Upgrade Your Skills"
                            ],
                            bold: "Upgrade Your Life"
                        },
                        p: [
                            "Opening up more opportunities in front of you to get the ticket to more enjoyable door in life. Getting equipped with new skills for new sets of insights into your career.",
                            "MaxCoach accompany learners in every stage of learning."
                        ],
                        link: {
                            text: "Download free guidebook"
                        }
                    },
                    "people-hearts": {
                        subtitle: {
                            normal: "Testimonials",
                        },
                        title: {
                            normal: [
                                "Why Do People",
                                "Us?"
                            ],
                            bold: "*Hearts*"
                        },
                        p: [
                            "Seeking for verbals of our service quality? Find them here. Everything is transparent and straightforward for your sense of jusitifcation."
                        ],
                        link: {
                            text: "View all"
                        }      
                    }
                }
            }
        }
    }
</script>