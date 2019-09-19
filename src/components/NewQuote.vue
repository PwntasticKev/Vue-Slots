<template>
	<div class="row">
		<form>
			<div class="col-sm-8 col-sm-offset-2 cold-xs-12 cold-md-6 cold-md-offset-3">
				<label>Quote</label>
				<textarea class="form-control" name="" id="" cols="30" rows="3" v-model="quote"></textarea>
			</div>
			<div class="col-sm-8 col-sm-offset-2 cold-xs-12 cold-md-6 cold-md-offset-3">
				<button @click.prevent="createNew">Add Quote</button>
			</div>
		</form>
	</div>
</template>

<script>
export default {
	data: function() {
		return {
			quote: ''
		}
	},
	methods: {
		createNew() {
			this.$emit('quoteAdded', this.quote);
			this.quote = ''
		}
	}

}	
</script>

<style></style>