<template>
  	<div class="loader-container">
  		<div class="loader">
    		<div class="inner-circle"></div>
  		</div>
 	</div>
</template>
<script>
  export default {
    
    name: 'LoaderComp',
    props: {
	    message: {
	      type: String,
	      default: 'Chargement...'
	    }
  	}

  };
</script>
<style lang="scss" scoped>
	 .loader-container {
	    display: flex;
	    justify-content: center;
	    align-items: center;
	    height: 100vh;
	}

	.loader {
	  width: 100px;
	  height: 100px;
	  display: flex;
	  justify-content: center;
	  align-items: center;
	  border-radius: 50%;
	  background: linear-gradient(0deg, #4169E1 50%, #90d5FF 100%);
	  animation: spin 1s linear infinite;
	}

	.inner-circle {
	  width: 90%;
	  height: 90%;
	  background-color: black;
	  border-radius: 50%;
	}

	@keyframes spin {
	  from {
	    transform: rotate(0);
	  }
	  to{
	    transform: rotate(360deg);
	  }
	}
</style>