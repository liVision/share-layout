<template>
	<div class="wrap">
		<div class="container">
			<div class="div1" style="background: red;"><p>1</p></div>
			<div class="div2" style="background: orange;"><p>2</p></div>
			<div class="div3" style="background: green;"><p>3</p></div>
			<div class="div4" style="background: blue;"><p>4</p></div>
			<div class="div5" style="background: purple;"><p>5</p></div>
			<div class="div6" style="background: papayawhip;"><p>6</p></div>
			<div class="div7" style="background: gray;"><p>7</p></div>
			<div class="div8" style="background: greenyellow;"><p>8</p></div>
			<div class="div9" style="background: burlywood;"><p>9</p></div>
		</div>
	</div>
</template>

<style lang="scss" scoped>
.container {
    width: 500px;
    height: 500px;
    border: 1px solid black;
	display: grid;
    grid-template-columns: repeat(3, 100px);
	// grid-template-columns: repeat(auto-fill, 100px);
    // grid-template-columns: 1fr 1fr 1fr;
    // grid-template-columns: 100px 1fr 2fr;
    // grid-template-columns: 1fr 1fr minmax(100px, 200px);
    // grid-template-columns: 220px 220px minmax(100px, 200px);
	grid-template-rows: 100px 100px 100px;
    grid-template-areas: "header header header"
                     "main main sidebar"
                     "footer footer footer";
    
	// place-items: start end;
    .div1 {
        grid-column-start: header-start;
        grid-column-end: header-end;
    }
}
</style>