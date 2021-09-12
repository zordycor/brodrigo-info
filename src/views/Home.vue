<template>
	<div class="home">
		<div class="info">
			<div class="first-block">
				<img
					class="photo"
					src="../assets/borja-black.png"
					alt="This is me"
				/>
				<div class="data">
					<div class="title">
						<h1>Borja Rodrigo</h1>
						<h3 class="text job">Frontend Developer</h3>
					</div>
					<div class="social">
					<a
						href="https://github.com/zordycor"
						target="_blank"
						rel="noopener noreferrer"
					>
						GITHUB
					</a>
					<a
						href="https://www.linkedin.com/in/borja-rodrigo-marti-39a3886a/"
						target="_blank"
						rel="noopener noreferrer"
					>
						LINKEDIN
					</a>
					</div>
				</div>
			</div>
			<h3>What are you looking for?</h3>
			<nav>
				<ul>
					<li @click="openExperience" :class="{'active': showingElement === 'experience'}"><h4>Work Experience & Good Words</h4></li>
					<li @click="openInvestments" :class="{'active': showingElement === 'investments'}"><h4>Real State & Investments</h4></li>
					<li @click="openRecommendations" :class="{'active': showingElement === 'recommendations'}"><h4>Books & Tools</h4></li>
					<!-- <li @click="openFAQs" :class="{'active': showingElement === 'faqs'}"><h4>FAQs</h4></li> -->
				</ul>
			</nav>
			<hr>
			<div class="container">
			<transition name="fade">
				<ExperienceComponent v-if="showingElement === 'experience'"/>
			</transition>
			<transition name="fade">
				<InvestmentsComponent v-if="showingElement === 'investments'"/>
			</transition>
			<transition name="fade">
				<RecommendationsComponent v-if="showingElement === 'recommendations'"/>
			</transition>
			<!-- <transition name="fade">
				<FAQComponent v-if="showingElement === 'faqs'"/>
			</transition> -->
			</div>
		</div>
	</div>
</template>

<style src="./Home.scss" lang="scss"></style>

<script>
import ExperienceComponent from '../components/ExperienceComponent/ExperienceComponent.vue';
import InvestmentsComponent from '../components/InvestmentsComponent/InvestmentsComponent.vue';
import RecommendationsComponent from '../components/RecommendationsComponent/RecommendationsComponent.vue';
// import FAQComponent from '../components/FAQComponent/FAQComponent.vue';

export default {
	components: {
		ExperienceComponent,
		InvestmentsComponent,
		RecommendationsComponent,
		// FAQComponent
	},
	data() {
		return {
			showingElement: '',
		}
	},
	methods: {
		openExperience() {
			this.showingElement = 'experience';
		},
		openInvestments() {
			this.showingElement = 'investments';
		},
		openRecommendations() {
			this.showingElement = 'recommendations';
		},
		openFAQs() {
			this.showingElement = 'faqs';
		}
	}
}
</script>