<template>
	<mm_page id="page_checkbox">
		<header class="header">
			<mm_warp>
				<mm_container>
					<mm_row>
						<mm_col width="100">
							<mm_view url="/">
								<h3>
									<span>复选框</span>
									<span class="fr">&lt; 返回</span></router-link>
								</h3>
							</mm_view>
						</mm_col>
					</mm_row>
				</mm_container>
			</mm_warp>
		</header>
		<main>
			<mm_warp>
				<mm_container>
					<mm_row>
						<mm_col class="col-12 col-md-6">
							<mm_card class="pc">
								<div class="card_head">
									<h5 @click="$copy(code_1)">样式一(PC)</h5>
								</div>
								<div class="card_body pa">
									<control_checkbox :symbol="symbol" v-model="value" :options="options"></control_checkbox>
								</div>
							</mm_card>
						</mm_col>
						<mm_col class="col-12 col-md-6">
							<mm_card class="mobile">
								<div class="card_head">
									<h5 @click="$copy(code_2)">样式二(mobile)</h5>
								</div>
								<div class="card_body">
									<control_checkbox :symbol="symbol" v-model="value" :options="options"></control_checkbox>
								</div>
							</mm_card>
						</mm_col>
					</mm_row>
				</mm_container>
			</mm_warp>
			<mm_warp>
				<mm_container>
					<mm_row>
						<mm_col width="100">
							<mm_card>
								<div class="card_body pa">
									选择结果：{{ value }}
									<input class="fr" style="width: 4rem;" placeholder="分隔符" v-model="symbol">
								</div>
							</mm_card>
						</mm_col>
					</mm_row>
				</mm_container>
			</mm_warp>
		</main>
	</mm_page>
</template>

<script>
	export default {
		data() {
			return {
				symbol: ",",
				value: "",
				options: [{
						name: "选项一",
						value: "1",
					},
					{
						name: "选项二",
						value: "2",
					},
					{
						name: "选项三",
						value: "3",
					}
				],
				code_1: `
<mm_card class="pc">
<control_checkbox v-model="value" :options="options"></control_checkbox>
</mm_card>
`,
				code_2: `
<mm_card class="mobile">
<control_checkbox v-model="value" :options="options"></control_checkbox>
</mm_card>
`

			}
		}
	}
</script>

<style>
</style>
