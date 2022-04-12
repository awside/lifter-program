<script lang="ts">
    export let width: any = '25'
    export let height: any = '25'
    export let color: string = '#2b2b2b'
    export let strokeWidth: number = 4
  </script>
  
  <svg version="1.1" {width} {height} xmlns="http://www.w3.org/2000/svg">
    <line
      x1="40%"
      x2="10%"
      y1="10%"
      y2="50%"
      stroke={color}
      stroke-width={strokeWidth}
      stroke-linecap="round"
    />
    <line
      x1="40%"
      x2="10%"
      y1="90%"
      y2="50%"
      stroke={color}
      stroke-width={strokeWidth}
      stroke-linecap="round"
    />
    <line
      x1="90%"
      x2="10%"
      y1="50%"
      y2="50%"
      stroke={color}
      stroke-width={strokeWidth}
      stroke-linecap="round"
    />
  </svg>
  