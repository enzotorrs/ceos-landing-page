<template>
  <svg
    viewBox="0 0 64 64"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    aria-hidden="true"
  >
    <defs>
      <linearGradient id="planet-body" x1="10" y1="10" x2="54" y2="54" gradientUnits="userSpaceOnUse">
        <stop offset="0%" stop-color="#f4a261" />
        <stop offset="55%" stop-color="#e07ab0" />
        <stop offset="100%" stop-color="#7b5cf0" />
      </linearGradient>
      <linearGradient id="ring-grad" x1="0" y1="0" x2="64" y2="0" gradientUnits="userSpaceOnUse">
        <stop offset="0%" stop-color="#f4813f" stop-opacity="0.9" />
        <stop offset="50%" stop-color="#d46fe0" stop-opacity="0.9" />
        <stop offset="100%" stop-color="#7b5cf0" stop-opacity="0.9" />
      </linearGradient>
      <clipPath id="ring-clip-top">
        <rect x="0" y="0" width="64" height="29" />
      </clipPath>
      <clipPath id="ring-clip-bottom">
        <rect x="0" y="33" width="64" height="31" />
      </clipPath>
    </defs>

    <!-- Planet body -->
    <circle cx="32" cy="32" r="18" fill="url(#planet-body)" />

    <!-- Ring behind planet (bottom half) -->
    <ellipse
      cx="32" cy="32"
      rx="30" ry="8"
      fill="none"
      stroke="url(#ring-grad)"
      stroke-width="3.5"
      clip-path="url(#ring-clip-bottom)"
    />

    <!-- Ring in front of planet (top half) -->
    <ellipse
      cx="32" cy="32"
      rx="30" ry="8"
      fill="none"
      stroke="url(#ring-grad)"
      stroke-width="3.5"
      clip-path="url(#ring-clip-top)"
    />
  </svg>
</template>
