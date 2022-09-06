<script setup>
import SiriWave from "siriwave";
import ChatBox from "./ChatBox.vue";
</script>

<template>
  <section class="content">
    <article class="post">
      <div class="container">
        <!-- <h2>This is the super cool section title</h2> -->
        <div class="columns">
          <div class="item text-center">
            <!-- <h4 class="item-title">This is radio player</h4> -->
            <div class="centercontent">
              <div id="waveform"></div>
            </div>
            <div class="centercontent">
              <!-- <a href="#" class="btn btn-primary"><i class="fa fa-backward" style="color: white;"></i></a> -->
              <div class="btn">
                <i class="fa fa-stop" style="color: white;"></i>
                <span aria-hidden class="btn__glitch"><i class="fa fa-stop" style="color: white;"></i></span>
                <span aria-hidden class="btn__tag">Stop</span>
              </div>

              <div class="btn">
                <i class="fa fa-play" style="color: white;"></i>
                <span aria-hidden class="btn__glitch"><i class="fa fa-play" style="color: white;"></i></span>
                <span aria-hidden class="btn__tag">Play</span>
              </div>
              <!-- <a href="#" class="btn btn-primary"><i class="fa fa-pause" style="color: white;"></i></a> -->
              <!-- <a href="#" class="btn btn-primary"><i class="fa fa-forward" style="color: white;"></i></a> -->
            </div> 
          </div>

          <ChatBox></ChatBox>
        </div>
      </div>
    </article>
  </section>
</template>

<script>
  export default {
	name: 'RadioPlayer',
	data: function() {
		return {
			sound: null,
			wave: null
		}
	},
  mounted: function() {
    let self = this
		self.wave = new SiriWave({
			container: waveform,
			width: 640,
      height: 200,
			cover: true,
			speed: 0.03,
			amplitude: 0.7,
			frequency: 2
		})
    self.wave.start()
  }
}
</script>

<style>
@import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.0/css/all.min.css';
@import '../assets/radio.css'
</style>
