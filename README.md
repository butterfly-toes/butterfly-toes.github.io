# butterfly-toes.github.io
&lt;butterfly-toes>

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 2000 1400">
    <linearGradient id="gradient">
      <stop stop-color="#bbb8"/>
      <stop offset=".5" stop-color="#0008"/>
    </linearGradient>
    <pattern id="pattern" width="200" height="140" patternUnits="userSpaceOnUse">
        <path d="M100 70a17 41 60 1 1 0 1a26 18 30 1 1 0 1a26 18 -30 1 1 0 -1a17 41 -60 1 1 0 -1" fill="url(#gradient)"/>
    </pattern>
    <filter id="filter" color-interpolation-filters="sRGB">
        <feColorMatrix values="0 0 0 0 0
                               0 0 0 0 0
                               0 0 0 0 0
                               0 0 0 -2 1" result="m"/>
        <feTurbulence type="fractalNoise" baseFrequency=".02" numOctaves="9"/>
        <feColorMatrix values="1 0 0 0 0
                               1 0 0 0 0
                               1 0 0 0 0
                               0 0 0 0 1"/>
        <feComponentTransfer>
            <feFuncR type="discrete" tableValues="0 0   0   1   .72 0 1   1 0 .94 1   0"/>
            <feFuncG type="discrete" tableValues="1 .1  .07 .43 .17 0 .6 .1 0 .93 .96 1"/>
            <feFuncB type="discrete" tableValues="1 .75 .47 .77 .86 0 0  .1 0 .4  .45 0"/>
        </feComponentTransfer>
        <feDisplacementMap in2="SourceGraphic" xChannelSelector="R" scale="200"/>
        <feBlend in="m"/>
    </filter>
    <rect width="100%" height="100%" fill="url(#pattern)" filter="url(#filter)"/>
</svg>
