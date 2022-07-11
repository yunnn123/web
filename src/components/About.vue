<script setup>
import {ArrowRightIcon} from "@heroicons/vue/outline";

const skills = [
	{
		title: '關於資訊工程',
		description: '利用工程處理資訊，屬於電腦科學的一個分支。(數據工程= 資訊工程)',
	},
	{
		title: '什麼是軟體',
		description: '一系列按照特定順序組織的電腦資料和指令，是電腦中的非有形部分。',
	},
	{
		title: '軟體種類',
		description: '系統軟體(ex:Windows)、應用軟體(ex:微軟的Office軟體)、中介軟體、惡意軟體',
	},
	{
		title: '程式語言',
		description: '用來向電腦發出指令，能夠讓程式設計師準確地定義電腦所需要使用資料的電腦語言，並在不同情況下應該要採取的行動。',
	},
	{
		title: '程式設計',
		description: '給程式解決出特定問題的過程，包括分析、設計、編碼、測試、除錯等不同階段。',
	},
]
</script>

<template>

	<section id="about" class="pt-32 md:px-16 bg-zinc-200">
		<div class="flex flex-col md:flex-row justify-between items-center md:px-8 md:mb-4">
			<h1 class="text-2xl md:text-4xl text-black font-bold">
				資訊介紹
			</h1>
			<button
				class="my-8 mr-3 border-b border-black pb-2 flex items-center text-xl text-black">
				查看更多
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