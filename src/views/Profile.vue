<template>
    <b-row>
        <div v-for='person in people' :key='person.url'>
            <b-card border-variant="0" v-if='person.url === id'>
                <b-container>
                    
                    <b-row>
                        <b-col cols='3'></b-col>
                        <b-col cols='6'>
                            <b-img fluid-grow rounded :src="person.image" alt=""></b-img>
                        </b-col>
                        <b-col cols='3'></b-col>
                    </b-row>
                    <b-row>
                        <h4>{{person.name}}</h4>
                    </b-row>
                      <b-row>
                        <h6>{{person.role}}</h6>
                    </b-row>
                    <b-row>
                         <b-col cols='12'>
                            <b-card-text>{{person.about}}</b-card-text>
                        </b-col>
                    </b-row>
                    <b-row>
                        <router-link to='/people'>Back</router-link>
                    </b-row>
                </b-container>
            </b-card>
        </div>
    </b-row>
</template>

<script>
export default {
    name: 'Profile',
    data () {
        return {
            id: this.$route.params.id,
            people: [
                    {
                        name: "Panna Codner",
                        role: "PI",
                        about: "Dr Panna Codner is an Associate Professor of Surgery and sub-specialized in the care of patients at Froedtert/Medical College of Wisconsin.  She is a faculty member of the Division of Trauma and Critical Care Surgery and the fellowship director to train young surgeons caring for the injured patient. Dr Codner’s research is focused on nutrition and how nutrition influences the bacteria in our intestinal tracts.  Both nutrition and the bacteria that live inside our intestinal tracts affect mental conditions such as depression and anxiety.  Dr Codner is studying nutrition and bacteria and their influence on the development of post-traumatic stress disorder and quality of life.",
                        image: require("@/assets/pcodner.jpeg"),
                        url: 'pcodner'
                    },
                    {
                        name: "Jacklynn Fitzgerald",
                        role: "PI",
                        about: "Trained as a behavioral neuroscientist, Jacklynn translates this expertise into her research on emotion dysregulation in clinical populations, notably posttraumatic stress disorder (PTSD). Combined, her research is aimed at deciphering how the brain regulates negative emotional states and how brain regions governing emotion regulation are aberrant in the context of trauma and developing PTSD. As a graduate student, Jacklynn examined aberrant brain functioning in combat-exposed veterans of Iraq and Afghanistan using functional magnetic resonance imaging (fMRI) and electroencephalogram (EEG) methods. She extends this line of work, now involving survivors of acute traumatic injury. Currently, she is investigating how neurocircuitry governing the regulation of fear predicts long-term stress response in this population.",
                        image: require("@/assets/jfitzgerald.jpeg"),
                        url: 'jfitzgerald'
                    },
                    {
                        name: "Tim Geier",
                        role: "PI",
                        about: "Tim is a postdoctoral researcher and clinician with interest in the assessment, treatment, and empirical examination of a wide range of recovery experiences among medically-complex patients, particularly within the context of trauma and health psychology. Throughout his education, his research and clinical interests have focused on the impact and prevention of trauma across various contexts, including stressful life events, sexual violence, as well as traumatic injury and medical illness. Currently, he is now exploring how acute medical stressors and subsequent emergency general surgical interventions impact psychological and physical quality of life. He is excited to work at a place that views research and treatment not as separate entities, but rather as mutually reinforcing pursuits.",
                        image: require("@/assets/tgeier.jpeg"),
                        url: 'tgeier'
                    },
                    {
                        name: "Cecilia J Hillard",
                        role: "Associate Dean for Research, PI",
                        about: "Cecilia J Hillard, PhD is Professor of Pharmacology and Director of the Neuroscience Research Center at the Medical College of Wisconsin.  Her laboratory studies the pharmacology and biochemistry of the cannabinoids and has contributed to a body of evidence demonstrating that the endocannabinoid system is stress responsive and contributes to the sequelae of stress and trauma.  She loves working with the MTOP team and exploring the role of the endocannabinoids in the risk for psychopathology following trauma exposure.",
                        image: require("@/assets/chillard.jpeg"),
                        url: 'chillard'
                    },
                    {
                        name: "Josh Hunt",
                        role: "PI",
                        about: "Dr. Josh Hunt is a Psychologist and Assistant Professor in the Departments of Surgery and Psychiatry.  He earned his undergraduate degree in psychology from Southern Illinois University of Carbondale, a master’s degree in community counseling from Concordia University of Chicago, and a doctoral degree with a concentration in counseling psychology from the University of Wisconsin Milwaukee.  He completed a residency at the Clement J. Zablocki VAMC, anda Health and Trauma Psychology Fellowship at the Medical College of Wisconsin. Clinically, he specializes in the treatment of trauma and stress or related disorders, somatic symptom disorders, and other medically related adjustment issues. His research has involved the creation of a screen to predict risk for the development of PTSD and depression among single incident trauma survivors admitted to the trauma service for their injuries. He is also interested in measuring the PTSD construct and the role of organic injury on the development of PTSD.",
                        image: require("@/assets/jhunt.jpeg"),
                        url: 'jhunt'
                    },
                    {
                        name: "Jennifer Knight",
                        role: "PI",
                        about: "Dr. Knight is an Assistant Professor in Psychiatry and Behavioral Medicine at the Medical College of Wisconsin. Dr. Knight’s research interests involve investigating the physiologic and immunologic effects that account for the relationship between psychosocial factors and clinical outcomes in hematopoietic stem cell transplant recipients. She is interested in the role of trauma in cancer patients. Clinically, she is the Medical Director of the Psycho-Oncology Program at Froedtert and MCW and specializes in general and psycho-oncology psychosomatic medicine consultation. She is on faculty at the Neuroscience Research Center and is also a Clinical Member of the MCW Cancer Center in the Transplantation Biology and Immunotherapy Research Program. Dr. Knight completed her undergraduate training at the University of Wisconsin-Madison and her medical training at the Medical College of Wisconsin. She completed her residency training in a combined Internal Medicine and Psychiatry program at Rush University in Chicago, and is double board certified in both specialties. She also completed a post-doctoral research fellowship in psychoneuroimmunology at the University of Rochester Medical Center.",
                        image: require("@/assets/jknight.jpg"),
                        url: 'jknight'
                    },
                    {
                        name: "Christine Larson",
                        role: "Co-founder of MTOP and PI",
                        about: "Christine Larson, Ph.D. is an Associate Professor of Psychology at the University of Wisconsin-Milwaukee, where she directs the Affective Neuroscience Laboratory. She and Terri deRoon-Cassini formed the Milwaukee Trauma Outcomes Project in 2015. Prior to moving to Milwaukee Chris was on the Psychology faculty at Michigan State University, after completing graduate work at the University of Wisconsin-Madison and her clinical psychology internship at Western Psychiatric Institute and Clinic in Pittsburgh. Her research is dedicated to understanding individual differences in emotional and cognitive processing that confer risk for posttraumatic stress, anxiety, and depression. She uses neuroimaging, psychophysiological, genetic, and behavioral tools to examine these questions. Together with Terri deRoon-Cassini, she is interested in identifying neurobiological markers evident immediately following trauma that confer risk for chronic PTSD. Her team is also using high resolution imaging to characterize neural circuits instantiating maladaptive fear and emotion regulation. More about the lab’s work can be found on their website (LINK to uwmlarsonlab.org).",
                        image: require("@/assets/clarson.jpeg"),
                        url: 'clarson'
                    },
                    {
                        name: "Han Joo Lee",
                        role: "PI",
                        about: "Han Joo Lee is an Associate Professor of Psychology at the University of Wisconsin-Milwaukee, and is the director of the UWM Anxiety Lab. The overarching goal of his research program is to understand the nature of anomalous neurocognitive processes (e.g., attention biases, interpretation biases, working memory deficits, and inhibitory control deficits) underlying in anxiety and trauma-related disorders and develop cognitive interventions for these problems. To this end, he has been conducting experimental psychopathology studies employing a variety of neurocognitive and physiological measures, and testing various computerized cognitive intervention programs via randomized experimental trials.",
                        image: require("@/assets/hjlee.jpeg"),
                        url: 'hjlee'
                    },
                    {
                        name: "Michael Levas",
                        role: "PI",
                        about: "Dr. Levas has been with the Medical College of Wisconsin's Section of Pediatric Emergency Medicine since 2011.  He is a local product from the south side of Milwaukee and completed his undergraduate work at Saint Norbert College in De Pere, WI.  Following graduation from the Medical College of Wisconsin, he completed his residency and fellowship training in Kansas City, MO.  He completed his Masters in Clinical and Translational at the Medical College of Wisconsin. Since joining the faculty at the Medical College, Dr Levas has been intimately involved with health care disparities, youth violence, and injury prevention policy and research.  He is the assistant medical director of Project Ujima, the premier hospital based youth violence prevention/intervention program in the United States.  He currently serves as co-chair of the Injury Reduction Initiative at Children’s Hospital of Wisconsin.",
                        image: require("@/assets/mlevas.jpeg"),
                        url: 'mlevas'
                    },
                    {
                        name: "Lucas Torres",
                        role: "PI",
                        about: "Lucas Torres, Ph.D. is an associate professor in the Psychology Department. Dr. Torres received his doctoral degree in clinical psychology from Purdue University and completed a Multicultural Post-doctoral Research Fellowship at the University of Notre Dame. Prior to his post-doctoral position, Dr. Torres received clinical training at the Center for Multicultural Training in Psychology, through the Boston University Medical Center, and the Massachusetts Mental Health Center.  Currently, he is co-Director of the Latina/o Well-being Research Initiative (LWRI) and his research interests focus on issues of mental health disparities or the psychological difficulties experienced by members of underrepresented groups. With an emphasis on community-based approaches, this research seeks to identify the mechanisms that contribute to mental health problems, namely depression, anxiety, alcohol use, and posttraumatic stress disorder (PTSD). Past research has been supported through a number of sources including the Clinical & Translational Science Institute (CTSI), Medical College of Wisconsin’s Advancing a Healthier Wisconsin Research and Education Program (AHW REP); Women and Girls of Color Research Initiative Grant, Marquette University; Strategic Innovation Fund, Marquette University; and the National Institute of Mental Health (NIMH).",
                        image: require("@/assets/ltorres.jpeg"),
                        url: 'ltorres'
                    },
                    {
                        name: "Colleen Trevino",
                        role: "PI",
                        about: "Colleen has been a Nurse Practitioner for over 15 years, most of her career delivering care directly to traumatically injured adult patients. She has been interested in acute pain management in traumatically injured patients since she started her career. All her clinical nursing experience has involved caring for surgical and trauma patients. Pain is central to the care of these populations. Pain management continues to be challenging especially once acute pain becomes chronic pain. As part of her clinical practice, she became very interested in what mechanisms modulate the transformation from acute to chronic pain.  In her graduate studies she focused on nursing education related to acute pain management and the development of chronic pain in the traumatically injured patient. Her doctoral studies identified initial pain as a predictor of chronic pain after a traumatic injury. She wants to explore the relationship of biopsychosocial factors that modulate the pain experience how acute pain persists to the development chronic pain and to identify practices that may, ultimately prevent the development of chronic pain in traumatically injured patients.",
                        image: require("@/assets/ctrevino.jpeg"),
                        url: 'ctrevino'
                    },
                    {
                        name: "Terri deRoon-Cassini",
                        role: "Co-founder of MTOP and PI",
                        about: "Terri is an Associate Professor in the Division of Trauma & Acute Care Surgery, in the Department of Surgery at the Medical College of Wisconsin, in Milwaukee, Wisconsin. She holds appointments in the Department of Psychiatry, Institute for Health and Equity, is a member of the Neuroscience Research Center, and is the co-director of the Research Core of the Comprehensive Injury Center. Along with Christine Larson, Terri is the co-Founder of the Milwaukee Trauma Outcomes Project. Clinically Terri is a Licensed Psychologist and started the Trauma & Health Psychology Service for the level 1 trauma center at Froedtert Hospital. She provides patient care to traumatically injured survivors who have been hospitalized and has an outpatient behavioral health clinic for patient experiences traumatic stress and other outcomes after trauma. She is also a member of the trauma quality of life clinic, which is a multidisciplinary clinic providing integrative care for trauma survivors after discharge.Her research interest centers around documenting psychological, quality of life and resilience outcomes after injury and detecting acute risk for poor outcomes, as well as identifying psychosocial and neurobiological targets for early intervention to prevent distress and PTSD after trauma. She is also interested in developing early interventions that are applicable to the trauma center environment. She has received research funding from the CDC and NIH, as well as internal funding mechanisms from the Medical College of Wisconsin, including the Clinical and Translational Science Institute. Most recently, she has received funding to understand the impact that socioenvironmental stress, including chronic neighborhood violence and experiences of discrimination, has on creating a biologic vulnerability to traumatic injury that leads to poor outcomes.",
                        image: require("@/assets/tcassini.jpeg"),
                        url: 'tcassini'
                    },
                    {
                        name: "Ciara Ayala",
                        role: "Research Assistant",
                        about: "Undergraduate student at the University of Wisconsin-Milwaukee pursuing a Bachelors of Science Degree in Psychology and Biology, while also following the Pre-Med track. As a Clinical Research Assistant on the I-Star project I assist in data collection and analysis. I am also tasked with submitting the I-Star data to the NIMH. I plan to further my education in to medical school in order to become a Surgeon.",
                        image: require("@/assets/cayala.jpeg"),
                        url: 'cayala'
                    },
                    {
                        name: "Ken Bennett",
                        role: "Research Assistant",
                        about: "Ken is a graduate student in the clinical psychology PhD program at the University of Wisconsin-Milwaukee. He is interested using functional brain imaging to examine the neural underpinnings of anxiety. Specifically, he is interested in the relationship between uncertainty, worry, and avoidance, and how it relates to the development and maintenance of anxiety and post-traumatic stress. Ken is currently researching the neural correlates of uncertainty and anxiety in adults recently exposed to a traumatic event.",
                        image: require("@/assets/kbennett.jpeg"),
                        url: 'kbennett'
                    },
                    {
                        name: "Claire Bird",
                        role: "Research Assistant",
                        about: "Claire is currently a graduate student in the Clinical Psychology, PhD program at Marquette University. Her work focuses on mental health disparities and trauma responses in Latinx populations. Claire currently works on a study examining the social and biologic factors contributing to PTSD among racial/ethnic minority populations. She hopes this work will help pave the way for new projects and approaches to understand unique phenotypes of PTSD and idioms of distress within Latinx populations.",
                        image: require("@/assets/cbird.jpeg"),
                        url: 'cbird'
                    },
                    {
                        name: "Amber Brandolino",
                        role: "Clinical Research Coordinator",
                        about: "Amber Brandolino is a Clinical Research Assistant in the Department of Surgery, Division of Trauma & Acute Care Surgery at the Medical College of Wisconsin. Prior to joining MTOP, Amber worked as an undergraduate research assistant for a cognitive psychology lab where she ran neuropsychological battery tests and EEG. Amber earned her undergraduate degree in Psychology, Spanish for the Health Professions, and a minor in Biological Sciences from Marquette University in Milwaukee, Wisconsin. She is a second-year graduate student in the Master of Science in Clinical and Translational Science at the Medical College of Wisconsin.  She is interested in pursuing a terminal degree and continuing to research the acute period after trauma with attention to health disparities.",
                        image: require("@/assets/abrandolino.jpeg"),
                        url: 'abrandolino'

                    }, {
                        name: "Juan Zapata",
                        role: "Graduate Student Research Assistant",
                        about: "",
                        image: require("@/assets/jzapata.jpg"),
                        url: 'jzapata'
                    },
                    {
                        name: "Alexandra Gonzalez-Van Wart",
                        role: "Clinical Research Coordinator",
                        about: "",
                        image: require("@/assets/agonzalez.jpg"),
                        url: 'agonzalez'
                    },
                    {
                        name: "Izzie Pina",
                        role: "Research Assistant I",
                        about: "",
                        image: require("@/assets/ipina.jpg"),
                        url: 'ipina'
                    },
                    {
                        name: "Holly L. Hohner",
                        role: "Senior Administrative Assistant",
                        about: "",
                        image: require("@/assets/hhohner.jpg"),
                        url: 'hhohner'
                    },
                    {
                        name: "Kate Webb",
                        role: "Graduate Student Research Assistant",
                        about: "",
                        image: require("@/assets/kwebb.jpg"),
                        url: 'kwebb'
                    },
                    {
                        name: "Kevin Topel",
                        role: "Data Analyst/Web Developer",
                        about: "",
                        image: require("@/assets/ktopel.jpg"),
                        url: 'ktopel'
                    },
                    {
                        name: "Margo Mantz-Wichman",
                        role: "Clinical Research Nurse",
                        about: "Margo Mantz-Wichman has a B.S. in Biology from University of Wisconsin-Madison and a nursing degree from Bryant & Stratton College. She works for the Division of Trauma and Acute Care Surgery managing studies, data collection, phlebotomy, biospecimen collection and processing;  screening, recruiting and assessing patients participating in clinical research; providing patient and family education as well as staff education. Her research interests consit of violence prevention, traumatic injury, mental health, health disparities and racism.",
                        image: require("@/assets/mmantz.jpg"),
                        url: 'mmantz'
                    },
                ]
               
        }
    }
}
</script>

<style scoped>
p {
    text-align: left;
}
</style>