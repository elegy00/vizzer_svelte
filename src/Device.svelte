<script>
//   const player = document.getElementById('player');

//   const handleSuccess = function(stream) {
//     if (window.URL) {
//       player.srcObject = stream;
//     } else {
//       player.src = stream;
//     }
//   };
  
  let devices = [];

let  getRandomNumber = async () => {
  let allDevices = await navigator.mediaDevices.enumerateDevices();

  let userMedia = await navigator.mediaDevices.getUserMedia({ audio: true, video: false });

  console.log(allDevices);
  devices = allDevices.filter(dev => dev.kind === "audioinput")
  allDevices[0].label
}
getRandomNumber();
    //   .then(handleSuccess);
</script>

 
<style> 
	h1 {
		color: purple;
	}
</style>


<ul>
{#each devices as device, i}
<li>{device.label}</li>
{/each}</ul>