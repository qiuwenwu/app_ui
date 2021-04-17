<template>
	<mm_page id="page_root" class="mobile">
		<header>
			<mm_warp>
				<mm_container>
					<mm_row>
						<mm_col width="100">
							<mm_view>
								<h3>
									<span>MM-UI组件示例</span>
									<router-link to="/design"><span>点击查看</span> <span class="font_info">设计规范</span> <span>&gt;</span></router-link>
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
					<mm_row class="row-lg-3 row-md-2 row-sm-1">
						<mm_col width="100">
							<div class="center">基础组件</div>
						</mm_col>
						<mm_col>
							<mm_card>
								<div class="card_head">内容容器</div>
								<div class="card_body">
									<mm_list col="1" class="item-lr content-right">
										<item_base class="arrow" v-for="(o, idx) in content" :key="idx" :obj="o" :viewmodel="{content:'name'}"></item_base>
									</mm_list>
								</div>
							</mm_card>
						</mm_col>
						<mm_col>
							<mm_card>
								<div class="card_head">布局容器</div>
								<div class="card_body">
									<mm_list col="1" class="item-lr content-right">
										<item_base class="arrow" v-for="(o, idx) in layout" :key="idx" :obj="o" :viewmodel="{content:'name'}"></item_base>
									</mm_list>
								</div>
							</mm_card>
						</mm_col>
						<mm_col>
							<mm_card>
								<div class="card_head">表单组件</div>
								<div class="card_body">
									<mm_list col="1" class="item-lr content-right">
										<item_base class="arrow" v-for="(o, idx) in form" :key="idx" :obj="o" :viewmodel="{content:'name'}"></item_base>
									</mm_list>
								</div>
							</mm_card>
						</mm_col>
					</mm_row>
					<mm_row class="row-lg-3 row-md-2 row-sm-1">
						<mm_col width="100">
							<div class="center mt">复合组件</div>
						</mm_col>
						<mm_col>
							<mm_card>
								<div class="card_head">栏</div>
								<div class="card_body">
									<mm_list col="1" class="item-lr content-right">
										<item_base class="arrow" v-for="(o, idx) in bar" :key="idx" :obj="o" :viewmodel="{content:'name'}"></item_base>
									</mm_list>
								</div>
							</mm_card>
						</mm_col>
						<mm_col>
							<mm_card>
								<div class="card_head">列表</div>
								<div class="card_body">
									<mm_list col="1" class="item-lr content-right">
										<item_base class="arrow" v-for="(o, idx) in list" :key="idx" :obj="o" :viewmodel="{content:'name'}"></item_base>
									</mm_list>
								</div>
							</mm_card>
						</mm_col>
						<mm_col>
							<mm_card>
								<div class="card_head">轮播</div>
								<div class="card_body">
									<mm_list col="1" class="item-lr content-right">
										<item_base class="arrow" v-for="(o, idx) in swiper" :key="idx" :obj="o" :viewmodel="{content:'name'}"></item_base>
									</mm_list>
								</div>
							</mm_card>
						</mm_col>
						<mm_col>
							<mm_card>
								<div class="card_head">拓展</div>
								<div class="card_body">
									<mm_list col="1" class="item-lr content-right">
										<item_base class="arrow" v-for="(o, idx) in expand" :key="idx" :obj="o" :viewmodel="{content:'name'}"></item_base>
									</mm_list>
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
				content: [{
						title: "按钮",
						name: "mm_btn",
						url: "/content/btn"
					},
					{
						title: "图标",
						name: "mm_icon",
						url: "/content/icon"
					},
					{
						title: "加载",
						name: "mm_loading",
						url: "/content/loading"
					},
					{
						title: "颜色",
						name: "mm_color",
						url: "/content/color"
					},
				],
				layout: [{
						title: "栅格",
						name: "mm_row",
						url: "/layout/grid"
					},
					{
						title: "列表",
						name: "mm_list",
						url: "/layout/list"
					},
					{
						title: "表格",
						name: "mm_table",
						url: "/layout/table"
					},
					{
						title: "组合框",
						name: "mm_group",
						url: "/layout/group"
					},
					{
						title: "块",
						name: "mm_card",
						url: "/layout/div"
					},
					{
						title: "模态窗",
						name: "mm_modal",
						url: "/layout/modal"
					}
				],
				form: [{
						title: "复选框",
						name: "control_checkbox",
						url: "/form/checkbox"
					},
					{
						title: "单选框",
						name: "control_radio",
						url: "/form/radio"
					},
					{
						title: "输入框",
						name: "control_input",
						url: "/form/input"
					},
					{
						title: "计数器",
						name: "control_number",
						url: "/form/number"
					},
					{
						title: "选择框",
						name: "control_select",
						url: "/form/select"
					},
					{
						title: "开关",
						name: "control_switch",
						url: "/form/switch"
					},
					{
						title: "反转器",
						name: "control_reverse",
						url: "/form/reverse"
					},
					{
						title: "分页器",
						name: "control_pager",
						url: "/form/pager"
					},
					{
						title: "富文本编辑器",
						name: "control_rich",
						url: "/form/rich"
					}
				],
				expand: [
					{
						title: "源代码",
						name: "expand_pre",
						url: "/expand/pre"
					},
					{
						title: "二维码",
						name: "expand_qrcode",
						url: "/expand/qrcode"
					},
					{
						title: "精灵",
						name: "expand_sptite",
						url: "/expand/sptite"
					}
				],
				nav: [{
						title: "主导航",
						name: "nav_main",
						url: "/nav/main"
					},
					{
						title: "侧边导航",
						name: "nav_side",
						url: "/nav/side"
					},
					{
						title: "顶部导航",
						name: "nav_top",
						url: "/nav/top"
					},
					{
						title: "底部导航",
						name: "nav_bottom",
						url: "/nav/bottom"
					},
					{
						title: "快捷导航",
						name: "nav_quick",
						url: "/nav/quick"
					},
					{
						title: "用户导航",
						name: "nav_user",
						url: "/nav/user"
					}
				],
				bar: [{
						title: "标题栏",
						name: "bar_title",
						url: "/bar/title"
					},
					{
						title: "搜索栏",
						name: "bar_search",
						url: "/bar/search"
					},
					{
						title: "筛选栏",
						name: "bar_filter",
						url: "/bar/filter"
					},
					{
						title: "标签栏",
						name: "bar_tab",
						url: "/bar/tab"
					},
					{
						title: "排序栏",
						name: "bar_sort",
						url: "/bar/sort"
					},
					{
						title: "统计栏",
						name: "bar_count",
						url: "/bar/count"
					},
					{
						title: "购买栏",
						name: "bar_buy",
						url: "/bar/buy"
					},
					{
						title: "操作栏",
						name: "bar_action",
						url: "/bar/action"
					},
					{
						title: "聊天栏",
						name: "bar_chat",
						url: "/bar/chat"
					}
				],
				list: [{
						title: "基础列表",
						name: "list_base",
						url: "/list/base"
					},
					{
						title: "图片列表",
						name: "list_image",
						url: "/list/image"
					},
					{
						title: "文章列表",
						name: "list_article",
						url: "/list/article"
					},
					{
						title: "通讯录列表",
						name: "list_contact",
						url: "/list/contact"
					},
					{
						title: "消息列表",
						name: "list_message",
						url: "/list/message"
					},
					{
						title: "新闻列表",
						name: "list_news",
						url: "/list/news"
					},
					{
						title: "号码列表",
						name: "list_number",
						url: "/list/number"
					},
					{
						title: "商品列表",
						name: "list_goods",
						url: "/list/goods"
					},
					{
						title: "问答列表",
						name: "list_question",
						url: "/list/question"
					},
					{
						title: "用户列表",
						name: "list_user",
						url: "/list/user"
					},
					{
						title: "视频列表",
						name: "list_video",
						url: "/list/video"
					},
					{
						title: "音乐列表",
						name: "list_music",
						url: "/list/music"
					}
				],
				swiper: [{
						title: "卡片轮播",
						name: "swiper_card",
						url: "/swiper/card"
					},
					{
						title: "图片轮播",
						name: "swiper_image",
						url: "/swiper/image"
					},
					{
						title: "文本轮播",
						name: "swiper_text",
						url: "/swiper/text"
					},
					{
						title: "页面轮播",
						name: "swiper_page",
						url: "/swiper/page"
					},
					{
						title: "菜单轮播",
						name: "swiper_menu",
						url: "/swiper/menu"
					}
				]
			}
		}
	}
</script>

<style>
	#page_root h3 a {
		font-size: 1rem;
		float: right;
		color: #999;
	}

	#page_root h3 .font_info {
		font-weight: 600;
	}

	#page_root h4 {
		margin: auto;
		padding-bottom: 1rem;
	}

	#page_root .card_body {
		padding: 0;
	}
</style>
