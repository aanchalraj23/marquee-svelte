<script>
    export let text = 'This is a default scrolling text';
    export let speed = 5; 
    export let direction = 'left'; 
    
  </script>
  
  <div class="marquee">
    <div 
      class="marquee-content" 
      style="animation-duration: {speed}s; animation-direction: {direction === 'left' ? 'normal' : 'reverse'};">
      <span class="marquee-text">{text}</span>
      <span class="marquee-text">{text}</span>
    </div>
  </div>
  
  <style>
    .marquee {
      overflow: hidden;
      white-space: nowrap;
      box-sizing: border-box;
      width: 100%;
    }
  
    .marquee-content {
      display: inline-block;
      animation: marquee 10s linear infinite;
    }
  
    .marquee-text {
      display: inline-block;
      padding-right: 100%;
    }
  
    @keyframes marquee {
      from {
        transform: translateX(0%);
      }
      to {
        transform: translateX(100%);
      }
    }
  </style>
  