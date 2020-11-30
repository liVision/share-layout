<template>
	<div id="app">
		<div id="nav" style="float: left; width: 300px;">
			<el-menu
				default-active="2"
				class="el-menu-vertical-demo"
				@open="handleOpen"
				@close="handleClose"
                unique-opened
                router
			>
				<el-submenu index="1">
					<template slot="title">
                        <i class="el-icon-menu"></i>
						<span>水平垂直居中布局</span>
					</template>
                    <el-submenu index="1-1">
                        <template slot="title">已知宽高</template>
						<el-menu-item index="/center/absolute">绝对定位+负边距</el-menu-item>
                    </el-submenu>
					<el-submenu index="1-2">
                        <template slot="title">未知宽高</template>
						<el-menu-item index="/center/transform">利用css3的transform</el-menu-item>
						<el-menu-item index="/center/flex">flex</el-menu-item>
                    </el-submenu>
				</el-submenu>
                <el-submenu index="2">
                    <template slot="title">
                        <i class="el-icon-menu"></i>
						<span>定位</span>
					</template>
                    <el-menu-item index="/position">static+relative+absolute</el-menu-item>
                    <el-menu-item index="/sticky">sticky</el-menu-item>
                </el-submenu>
				<el-menu-item index="/float">
                    <i class="el-icon-menu"></i>
					<span slot="title">浮动布局</span>
				</el-menu-item>
				<el-menu-item index="/flex/flex">
                    <i class="el-icon-menu"></i>
					<span slot="title">flex布局</span>
				</el-menu-item>
                <el-submenu index="5">
                    <template slot="title">
                        <i class="el-icon-menu"></i>
						<span>grid布局</span>
					</template>
                    <el-menu-item index="/grid/normal">基本例子</el-menu-item>
                </el-submenu>
			</el-menu>
		</div>
        <div style="display: flex; justify-content: center; align-items: center; height: 700px;">
		    <router-view />
        </div>
	</div>
</template>

<style lang="scss">
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
}

#nav {
	padding: 30px;

	a {
		font-weight: bold;
		color: #2c3e50;

		&.router-link-exact-active {
			color: #42b983;
		}
	}
}
</style>
