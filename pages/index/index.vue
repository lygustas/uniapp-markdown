<template>
	<view class="content">
		<ly-markdown :showPreview="false" :textareaData.sync="textareaData" :textareaHtml.sync="textareaHtml"></ly-markdown>
	</view>
</template>

<script>
	import lyMarkdown from '../../components/ly-markdown.vue'
	export default {
		components: {
			lyMarkdown
		},
		data: {
			textareaData: "",
			textareaHtml:"",
		},
		watch:{
			"textareaData":function(){
				console.log("markdown:"+this.textareaData)
				console.log("html:"+this.textareaHtml)
			}
		},
	}
</script>

<style>
	@import '../../static/markdown.css';
	@import url("../../components/mpvue-wxparse/src/wxParse.css");

	.input-content {
		width: 100%;
	}

	.input-content textarea {
		padding: 16px 25px 15px 25px;
		font-size: 30px;
		min-height: 500px;
		line-height: 1.5;
	}

	.preview {
		border-top: 1px solid #e0e0e0;
		width: 100%;
	}

	.toolbar {
		width: 100%;
		border: none;
		box-shadow: 0 0px 4px rgba(0, 0, 0, 0.157), 0 0px 4px rgba(0, 0, 0, 0.227);
	}

	.toolbar .iconfont {
		display: inline-block;
		cursor: pointer;
		height: 61.6px;
		width: 61.6px;
		margin: 13px 0 11px 0px;
		font-size: 33px;
		padding: 10px 13px 11px 8px;
		color: #757575;
		border-radius: 11px;
		text-align: center;
		background: none;
		border: none;
		outline: none;
		line-height: 2.2;
		vertical-align: middle;
	}

	.input-content {
		min-height: ;
	}
</style>
