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
						<p class="text name">Borja Rodrigo</p>
						<p class="text job">Frontend Developer</p>
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
						href="https://borja-rodrigo.medium.com/"
						target="_blank"
						rel="noopener noreferrer"
					>
						MEDIUM
					</a>
					<a
						href="https://www.instagram.com/zordycor/"
						target="_blank"
						rel="noopener noreferrer"
					>
						INSTAGRAM
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
			<div class="experience">
				<p class="text">
					In 2018 I finished my Degree on CE at the UPV (
					<a
						:href="`${publicPath}TFG_Tapas.pdf`"
						download="TFG Borja Rodrigo"
					>
						This is my final project, it's a webpage
					</a>).
				</p>
				<p class="text">
					Then, the same year, I joined Epigram Technologies, my first
					job as a Web Developer!
				</p>
				<p class="text">
					After one and a half years I joined Jeff as a Junior FE
					Developer. We are on 2019.
				</p>
				<p class="text">
					Like eight months passed and the coronavirus arrived! I got
					fired. So in 2020 I joined Voicemod.
				</p>
				<p class="text">I think that's all so far.</p>
			</div>
			<a
				class="cv text"
				:href="`${publicPath}CV_Borja.pdf`"
				download="CV Borja"
			>
				<p>Click here to download my CV</p>
			</a>
			<p class="recomendations text">
				Here should be reommendations of my colleagues. Soon...
			</p>
		</div>
	</div>
</template>

<style src="./Home.scss" lang="scss">
</style>
