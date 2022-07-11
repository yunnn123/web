<script setup>
import {ArrowRightIcon, ChevronDoubleDownIcon} from '@heroicons/vue/solid'
</script>
<template>
	<section class="bg-gray-200 flex flex-col justify-center items-center md:px-20 min-h-screen">
		<div class="flex flex-col w-full py-12 px-4 lg:px-0 justify-flex-start items-center">
			<p class="text-2xl text-zinc-400 font-medium">Hello！我是<span class="text-zinc-400">Yun</span></p>
			<h1 class="text-5xl text-right text-zinc-500 mt-1 font-extrabold">
				想選擇資工系的高中生
			</h1>
			<p class="text-lg text-zinc-400 font-light pt-8">
         【一位對資工感興趣的女孩】
			</p>
			<a
				href="#contact"
				class="mt-3 flex items-center text-xl font-regular pb-2">
				聯絡我
				<ArrowRightIcon class="ml-1 w-5 h-5"/>
			</a>
		</div>

		<a href="#activities" class="animate-bounce cursor-pointer">
			<chevron-double-down-icon class="w-16 h-16"/>
		</a>
	</section>
</template>
