<script setup>
import {ArrowRightIcon} from "@heroicons/vue/outline";

const skills = [
	{
		title: '關於資訊工程',
		description: '利用工程處理資訊。',
	},
	{
		title: '什麼是軟體',
		description: '一系列按照特定順序組織的電腦資料和指令，是電腦中的非有形部分。',
	},
	{
		title: '程式語言',
		description: '定義電腦程式的形式語言',
	},
	{
		title: '程式設計',
		description: '給程式解決出特定問題的過程，包括',
	},
	{
		title: '種植物',
		description: '自己種東西來吃',
	},
]
</script>

<template>

	<section id="about" class="pt-32 md:px-16 bg-zinc-200">
		<div class="flex flex-col md:flex-row justify-between items-center md:px-8 md:mb-4">
			<h1 class="text-2xl md:text-4xl text-black font-bold">
				關於我
			</h1>
			<button
				class="my-8 mr-3 border-b border-black pb-2 flex items-center text-xl text-black">
				所有經歷
				<ArrowRightIcon class="ml-1 w-5 h-5"/>
			</button>
		</div>
		<div class="flex flex-wrap justify-center">
			<div
				class="w-full md:w-1/3"
				v-for="skill in skills">
				>
				<div
					class="px-10 sm:px-20 py-3 sm:py-6 shadow-lg w-11/12 mx-auto bg-white rounded z-20 relative">
					<h4 class="text-gray-800 text-lg text-center mb-2">{{ skill.title }}</h4>
					<p class="text-gray-600 text-lg text-center mb-2">{{ skill.description }}</p>
				</div>
			</div>
		</div>
	</section>
</template>