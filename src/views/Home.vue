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
					<a
						href="mailto:zordycorak@gmail.com"
						target="_blank"
						rel="noopener noreferrer"
					>
						EMAIL
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
					<li @click="openFAQs" :class="{'active': showingElement === 'faqs'}"><h4>FAQs</h4></li>
				</ul>
			</nav>
			<hr>
			<div class="container">
			<transition name="fade">
			<section class="experience" v-if="showingElement === 'experience'">
				<a
					class="cv"
					href="CV_Borja.pdf"
					download="CV Borja"
				>
					<p>Click here to download my CV</p>
				</a>
				<div class="experience">
					<h4>TLDR:</h4>
					<p class="text">
						<b>2018</b> I finished my Degree on <b>Computer Engineering</b> at the UPV.
					</p>
					<p class="text">
						That same year, I joined <b>Epigram Technologies</b>, my first
						job as a Web Developer.
					</p>
					<p class="text">
						In <b>2019</b> I joined <b>Jeff</b> as a Junior Frontend Developer.
					</p>
					<p class="text">
						<b>2020</b>, coronavirus arrived! I got fired, so I joined <b>Voicemod</b>.
					</p>
					<p class="text">That's all so far!</p>
				</div>
				<br>
				<h4>Thoughts of my colleagues about me:</h4>
				<p class="text">
					Agustin Carmona, Engineering Manager @ Voicemod:
					<br><br>
					Always with positive comments and constructive attitude towards his teammates.
					He offers to help whenever is possible, even between teams.
					He's in continuous learning, asking workmates and reading on his own.
					You can see that he enjoys his job.
				</p>
			</section>
			</transition>
			<transition name="fade">
			<section class="investments" v-if="showingElement === 'investments'">
				<h4>WHERE & HOW have I invested my money?</h4>
				<p>- <b>ALL</b> my investments are <b>long-term</b> (+5 yrs). They are split between <b>Index Funds</b>, <b>Cryptocurrencies</b> and <b>Stocks</b>.</p>
				<p>- The <b>largest amount</b> since 2021 is on <b><a href="https://indexacapital.com/t/OswDJF">Indexa Capital</a></b>, a platform that auto-invests on index funds for the best profit.</p>
				<p>- I <b>bought</b> my first <b>BTCs</b> and <b>mined</b> a couple milion <b>DOGE</b> in <b>2013</b>, but I'm <b>not rich</b> for being too greedy.</p>
				<p>- Right now, I have my BTC in <b><a href="https://blockfi.com/?ref=dc0c1262">BlockFi</a></b> where I recieve <b>interests</b> and <b><a href="https://www.coinbase.com/join/marti_0va">Coinbase</a></b> to make purchases once in a while.</p>
				<p>- <b><a href="https://www.degiro.es/amigo-invita-amigo/empezar-a-invertir.html?id=DDC5B48B&utm_source=mgm">DEGIRO</a></b> is the platform I use for buying <b>stocks</b>. I try to get stocks from <b>companies</b> that I <b>like</b>.</p>
			</section>
			</transition>
			<transition name="fade">
			<section class="recommendations" v-if="showingElement === 'recommendations'">
				<h4>Books that I bought, read & liked</h4>
				<p>About Coding</p>
				<div class="recommendation">
					<a href="https://amzn.to/3muITIK" target="blank">
						<img class="item" src="../assets/clean-code.jpg" alt="Clean Code Book">
						<div class="item-text">
							<h5>Clean Code</h5>
							<h5>Robert C. Martin</h5>
						</div>
					</a>
				</div>
				<div class="recommendation">
					<a href="https://amzn.to/3BmDDLt" target="blank">
						<img class="item" src="../assets/clean-coder.jpg" alt="The Clean Coder Book">
						<div class="item-text">
							<h5>The Clean Coder</h5>
							<h5>Robert C. Martin</h5>
						</div>
					</a>
				</div>
				<p>About Life</p>
				<div class="recommendation">
					<a href="https://amzn.to/3sR9alt" target="blank">
						<img class="item" src="../assets/factfulness.jpg" alt="Factfulness book">
						<div class="item-text">
							<h5>Factfulness</h5>
							<h5>Hans Rosling</h5>
						</div>
					</a>
				</div>
				<p>Some tools that I use daily</p>
				<div class="recommendation">
					<a href="https://amzn.to/3gwHhKx" target="blank">
						<img class="item" src="../assets/sony.jpg" alt="Sony headphones">
						<div class="item-text">
							<h5>Sony WH-XB900N</h5>
							<h5>Wireless headphones</h5>
						</div>
					</a>
				</div>
				<div class="recommendation">
					<a href="https://amzn.to/2XKniBu" target="blank">
						<img class="item" src="../assets/mx-master.jpg" alt="Logitech MX Master 2s Mouse">
						<div class="item-text">
							<h5>Logitech MX Master 2s</h5>
							<h5>Wireless mouse</h5>
						</div>
					</a>
				</div>
				<div class="recommendation">
					<a href="https://amzn.to/3B7lscm" target="blank">
						<img class="item" src="../assets/laptop.jpg" alt="Amazon Laptop stand">
						<div class="item-text">
							<h5>Amazon Basics</h5>
							<h5>Laptop stand</h5>
						</div>
					</a>
				</div>
			</section>
			</transition>
			</div>
		</div>
	</div>
</template>

<style src="./Home.scss" lang="scss"></style>

<script>
export default {
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