<template>
	<div class="wrap">
		<div class="containerWrap1">
            <span>flex: 1 === 1 1 +任意长度</span>
			<div class="container">
				<div class="div">我是一个div</div>
				<div class="div">我是一个很多字div</div>
				<div class="div">我是一个更多字而且第三个div</div>
			</div>
		</div>
		<div class="containerWrap2">
            <span>flex: auto === 1 1 auto</span>
			<div class="container">
				<div class="div">我是一个div</div>
				<div class="div">我是一个很多字div</div>
				<div class="div">我是一个更多字而且第三个div</div>
			</div>
		</div>
	</div>
</template>

<style lang="scss" scoped>
.wrap {
    width: 100%;
    display: flex;
    justify-content: space-between;
}
.containerWrap1 {
    background: orange;
	.container {
		display: flex;
	}
	.div {
		border: 1px solid red;
		flex: 1;
	}
}
.containerWrap2 {
    background: papayawhip;
	.container {
		display: flex;
	}
	.div {
		border: 1px solid red;
		flex: auto;
	}
}
</style>