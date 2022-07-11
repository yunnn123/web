<script setup>
import {ArrowRightIcon} from '@heroicons/vue/outline';

const activities = [
	{
		title: 'Web開發挑戰營',
		description: '讓你探索自己的網頁技術，並學習如何撰寫網頁。',
		url: ''
	},
	{
		title: '模擬聯合國',
		description: '模聯合國是一個模擬聯合國的活動，讓你學習如何模擬聯合國。'
	}
]
const makeClass = (i) => (
	i % 2 === 0 ?
		"flex flex-col sm:flex-row items-stretch mb-8 sm:mb-16 container mx-auto" :
		"flex flex-col sm:flex-row-reverse items-stretch mb-8 sm:mb-16 container mx-auto"
)
</script>
<template>
	<section id="activities" class="pt-32 px-2 md:px-20">
		<template v-for="(activity,i) in activities">
			<div :class="makeClass(i)">
				<div class="w-full sm:w-1/2 relative h-64 sm:h-auto">
					<img alt="活動圖片" class="w-full object-cover absolute inset-0 object-center h-full"
					     loading="lazy" :src="activity.image ?? 'https://gw.alicdn.com/i1/162992806/TB1ndruhLImBKNjSZFlXXc43FXa_!!0-item_pic.jpg_Q75.jpg_.webp'"/>
				</div>
				<div
					class="container mx-auto w-full sm:w-1/2 py-8 sm:py-16 lg:py-32 px-6 sm:px-12 lg:px-24 bg-gray-100">
					<h3 class="text-gray-800 text-2xl mb-3 leading-normal tracking-normal font-bold">{{
							activity.title
						}}</h3>
					<p class="text-gray-600 leading-6 font-normal tracking-normal mb-6">
						{{ activity.description }}
					</p>
					<a
						v-if="activity.url"
						:href="activity.url"
						target="_blank"
						class="focus:outline-none rounded py-3 px-4 text-black border border-black flex justify-center items-center text-base hover:bg-gray-200 bg-transparent">
						檢視心得
					</a>
				</div>
			</div>
		</template>

		<div class="mb-16 sm:mb-32 container mx-auto px-6 container">
			<button
				class="focus:outline-none my-8 flex items-center text-xl font-regular border-b border-black pb-2 mr-3">
				所有經歷
				<ArrowRightIcon class="ml-1 w-5 h-5"/>
			</button>
		</div>
	</section>
</template>
