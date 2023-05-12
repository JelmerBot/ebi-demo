<script>
	export let flower;

	let scale = 3;
	let sl = scale * flower.sepalLength;
	let sw = scale * flower.sepalWidth;
	let pl = scale * flower.petalLength;
	let pw = scale * flower.petalWidth;
	let sepal_path = 'M 0,0 ' + 'C ' + sl + ',-' + sw + ' ' + sl + ',' + sw + ' 0,0 Z';
	let petal_path = 'M 0,0 ' + 'C ' + pl + ',-' + pw + ' ' + pl + ',' + pw + ' 0,0 Z';
</script>

<g>
	<circle cx="0" cy="0" r="10" class={flower.species} />
	<path style="transform: rotate(270deg)" d={sepal_path} />
	<path style="transform: rotate(30deg)" d={sepal_path} />
	<path style="transform: rotate(150deg)" d={sepal_path} />
	<path style="transform: rotate(325deg)" d={petal_path} />
	<path style="transform: rotate(90deg)" d={petal_path} />
	<path style="transform: rotate(210deg)" d={petal_path} />
</g>

<style>
	circle.setosa {
		fill: #7570b3;
		fill-opacity: 0.3;
	}
	circle.virginica {
		fill: #1b9e77;
		fill-opacity: 0.3;
	}
	circle.versicolor {
		fill: #d95f02;
		fill-opacity: 0.3;
	}
</style>
