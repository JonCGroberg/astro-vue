<script setup>
import { ref } from "vue";

let id = 0;
const todos = ref([
	{ id: id++, text: "do x" },
	{ id: id++, text: "do y" },
	{ id: id++, text: "do z" }
]);
</script>

<template>
	<div class="card" style="min-width: 2rem; min-height: 4rem">
		<div class="card-header">
			<h1 class="card-text">Todo List</h1>
		</div>
		<div class="card-body">
			<ul class="list-group list-group-flush">
				<li class="list-group-item" v-for="todo in todos" :key="todo.id">
					<span>{{ todo.text }}</span>
                    <button class="btn btn-danger float-end"> x</button>
				</li>
			</ul>
		</div>
	</div>
</template>
