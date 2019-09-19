<template>
	<div class="progress">
  		<div class="progress-bar progress-bar-striped progress-bar-animated" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" style="width: 75%" :style="{width: (quotecount / maxquotes) * 100 + '%'}">
			  {{quoteCount}} / {{maxQuotes}}
		</div>
	</div>
</template>

<script>
	export default {
		props: ['quotecount', 'maxQuotes'],
		data() {
			return {

			}
		}
	}
</script>