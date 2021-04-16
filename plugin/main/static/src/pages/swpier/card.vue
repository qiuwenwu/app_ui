<template>
	<mm_page id="page_card">
		<header>
			<mm_warp>
				<mm_container>
					<mm_row>
						<mm_col width="100">
							<mm_view url="/">
								<h3>
									<span>轮播卡片</span>
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
							<mm_card class="silde_test">
								<h5>默认块</h5>
								<swiper_card :list="list"></swiper_card>
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
				list: [{
					title: "标题",
					url: "/",
					image: "/img/default.png",
				}]
			}
		}
	}
</script>

<style>
</style>
