<template>
	<!-- 消息 -->
	<mm_page id="page_message">
		<header class="header">
			<mm_warp>
				<mm_container>
					<mm_row>
						<mm_col width="100">
							<mm_view url="/">
								<h3>
									<span>消息</span>
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
						<mm_col width="100">
							<mm_view>
								<control_select v-model.number="col" :options="options"></control_select>
								<mm_btn class="btn_primary" @click.native="set_layout()">切换排版方式</mm_btn>
							</mm_view>
						</mm_col>
						<mm_col width="100">
							<mm_view class="card">
									<list_message :col="col" :list="list" :class="list_layout[select]">
									</list_message>
							</mm_view>
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
				select: 0,
				col: 1,
				list_layout: [
					"item-ltb img-base",
					"item-rtb img-base",
				],
				options: [{
						name: "1列",
						value: 1
					},
					{
						name: "2列",
						value: 2
					},
					{
						name: "3列",
						value: 3
					},
					{
						name: "4列",
						value: 4
					},
					{
						name: "5列",
						value: 5
					},
					{
						name: "6列",
						value: 6
					},
					{
						name: "8列",
						value: 8
					},
					{
						name: "10列",
						value: 10
					},
					{
						name: "12列",
						value: 12
					}
				],
				list: undefined
			}
		},
		methods: {
			set_layout() {
				if (this.select < this.list_layout.length - 1) {
					this.select++;
				} else {
					this.select = 0;
				}
			}
		}
	}
</script>

<style>
</style>
