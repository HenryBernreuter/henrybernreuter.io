---
date: 2020-08-04 12:26:40
layout: post
title:  Basic Data Visualiztion in Python
subtitle: Using matplotlib 
description: https://matplotlib.org/
image: /assets/img/datavis.png
optimized_image: /assets/img/datavis.png
category: tutorial
tags: Python
author: henry
---

<html>
<head><meta charset="utf-8" />

<title>2020-8-2-Basic-Data-Visualization</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Introduction-to-Basic-Visualizations-in-Python"><center>Introduction to Basic Visualizations in Python</center><a class="anchor-link" href="#Introduction-to-Basic-Visualizations-in-Python">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The basic question of when I should use which chart is explained here.</p>
<p>The type of graph you use is important. It's important for telling the story of data, that your assocications are not mis-interpreted.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Plot-Types">Plot Types<a class="anchor-link" href="#Plot-Types">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Bar-Plots"><u>Bar Plots</u><a class="anchor-link" href="#Bar-Plots">&#182;</a></h2><p>Usage: When Comparing the same varibales in the same category or datasets.</p>
<p>Do not use: More than 3 categories of variables or when trying to visualze continuous data.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 

<span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">500</span><span class="p">,</span> <span class="mi">800</span><span class="p">,</span> <span class="mi">900</span><span class="p">,</span> <span class="mi">1000</span><span class="p">,</span> <span class="mi">1400</span><span class="p">,</span> <span class="mi">1600</span><span class="p">]</span>
<span class="n">widths</span>  <span class="o">=</span> <span class="p">[</span><span class="mf">1.0</span><span class="p">,</span> <span class="mf">1.0</span><span class="p">,</span> <span class="mf">1.0</span><span class="p">,</span> <span class="mf">1.0</span><span class="p">,</span> <span class="mf">1.0</span><span class="p">,</span> <span class="mf">1.0</span><span class="p">]</span>
<span class="n">colors</span>  <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;b&#39;</span><span class="p">,</span><span class="s1">&#39;b&#39;</span><span class="p">,</span><span class="s1">&#39;b&#39;</span><span class="p">,</span><span class="s1">&#39;b&#39;</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">,</span><span class="s1">&#39;b&#39;</span><span class="p">]</span>

<span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>

<span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">,</span> <span class="n">width</span><span class="o">=</span><span class="n">widths</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="n">colors</span><span class="p">,</span> <span class="n">align</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="p">(</span><span class="s1">&#39;2016&#39;</span><span class="p">,</span><span class="s1">&#39;2017&#39;</span><span class="p">,</span> <span class="s1">&#39;2018&#39;</span><span class="p">,</span> <span class="s1">&#39;2019&#39;</span><span class="p">,</span> <span class="s1">&#39;2020&#39;</span><span class="p">,</span> <span class="s1">&#39;2021&#39;</span><span class="p">))</span>

<span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Billions&#39;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;GDP Prediction&#39;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">show</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[5]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;function matplotlib.pyplot.show(*args, **kw)&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Line-Plots"><u>Line Plots</u><a class="anchor-link" href="#Line-Plots">&#182;</a></h2><p>Line plots are the most common</p>
<p>Usage: When you are tracking and comparing several variables across time, analyzing trends and variation and predicting future values.</p>
<p>Do not use: To get an general overview of your data or analyzing individual components or sections.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Drawing mulitple lines and plots</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers2</span> <span class="o">=</span> <span class="p">[</span><span class="mi">200</span><span class="p">,</span> <span class="mi">600</span><span class="p">,</span> <span class="mi">900</span><span class="p">,</span> <span class="mi">1900</span><span class="p">,</span> <span class="mi">1200</span><span class="p">,</span> <span class="mi">1800</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAX0AAAD4CAYAAAAAczaOAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjAsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+17YcXAAAgAElEQVR4nO3dd3gU5fbA8e9JSOihJUBCCAHpCCKEJkVEVFAQCyCICipiwXb1Z79evSrqFXsXFRXpiCgCSq8CQugllNBDIKGHENI27++P2WCEACHZzWw5n+fJk83s7MxZiSfvnnnnvGKMQSmllH8IsDsApZRSxUeTvlJK+RFN+kop5Uc06SullB/RpK+UUn6khN0BXExoaKiJjo62OwyllPIaq1atOmyMCcvvOY9P+tHR0cTGxtodhlJKeQ0R2XO+57S8o5RSfkSTvlJK+RFN+kop5Uc06SullB/RpK+UUn5Ek75SSvkRTfpKKeVHNOkr5U3SU2DtWHBk2R2J8lKa9JXyJvNeh18ehrmv2R2J8lKa9JXyFsf2QOx3ULoyLP0Yts20OyLlhTTpK+UtFv4PJAAGz4HqTWHKg3Aiwe6olJfRpK+UNzi0FdaNg9YPQJXLoM8PVl3/p/u0vq8uiSZ9pbzB/GEQVAY6/Mv6ucpl0PMj2PcXzHvD3tiUV9Gkr5SnS1wDm3+FdkOhbOjf25v2hpaD4M8PYfts28JT3kWTvlKebt4bULqSlfTP1u1tqHY5/DwETuwv/tiU19Gkr5Qn2/0nxM+xyjqlKpz7fFBp6PM9ZGfA5PvBkV3sISrvoklfKU9ljDUvv1x1aPXA+fcLrQc9P4S9y6zav1IXoElfKU8VP8dK5Fc/A8FlLrxvs77Q4h5Y8r71OqXOQ5O+Up4oJ8e667ZiLbjynoK9pvs7ULWJVd9PSXRvfMq9jIGs0245tCZ9pTxR3K9wcD1c8yKUCC7Ya3Lr+1npMHmw1ve92bw34PubICPV5YfWpK+Up3Fkw7xhENYQmva5tNeG1YceH8CeP2HBW+6JT7nXqu9h8btQrQkEl3X54TXpK+Vp1o+HI9uhy78hIPDSX3/FHXDlXbD4Pdgxz/XxKffZPgemPQV1u8JN74OIy0+hSV8pT5KdAQvehogroWGPwh+n+3Drk8LkByDlgOviU+5zYD1MGgjVGltlusAgt5zmoklfREaKSLKIbMyzbYKIrHV+7RaRtc7t0SJyOs9zX+Z5TUsR2SAi8SLysYgb/oQp5e1WfQ8n9sG1/ynaKC+4jLO+nwY/PwA5DldFqNzhRAKM7Wvdi3HnJChZ3m2nKshI/3ugW94Nxpg7jDHNjTHNgcnAz3me3pH7nDHmoTzbvwCGAPWcX/84plJ+L/MULBoO0R2hzjVFP17VhnDTe7B7sdWhU3mm9BMwpo/17z9gEoSEu/V0F036xphFwNH8nnOO1vsC4y50DBEJB0KMMcuMMQYYBdxy6eEq5cP++hJOHYIuL7uultv8Tmg+ABa+Azvmu+aYynWyM2HC3XB4G9zxo3Xx1s2KWtPvCCQZY7bn2VZbRNaIyEIR6ejcVgPI2/g7wbktXyIyRERiRST20KFDRQxRKS9w+hj8+RHU7wZRbVx77BuHQ1gDa/7+ySTXHlsVnjHw2xOwayHc/AnU6Vwspy1q0u/PP0f5B4AoY8yVwFPAWBEJAfIbtpjzHdQYM8IYE2OMiQkLCytiiEp5gaWfWB/zu/zb9ccOLmvV9zNOWv15tL7vGRb+D9aNhc4vWJ/Iikmhk76IlABuAybkbjPGZBhjjjgfrwJ2APWxRvaReV4eCegtg0oBpCbD8i/g8tutFbHcoWojuOldq76/aLh7zqEKbs0Y6z6K5gPg6ueK9dRFGel3BbYYY86UbUQkTEQCnY/rYF2w3WmMOQCcFJG2zusA9wC/FuHcSvmOxe9ZUzU7v+je8zQfAFf0t6aE7lzo3nOp89sxH3573Crn9PjQLXPxL6QgUzbHAcuABiKSICL3O5/qx7kXcDsB60VkHfAT8JAxJvci8MPAN0A81ieA310Qv1Le7fheiB0JVw6A0LruPZcI3Piu1ZVz8mCt79shaRNMvAdCG0DfUQVvseFCYk2m8VwxMTEmNjbW7jCUco9fh8L6ifD4GqgQefH9XSFpM3zdBWq2hrunFO6uX3XpUhLhm65gcqzF7d347y0iq4wxMfk9p3fkKmWXw9th7VhoNbj4Ej5Yd3ze+I41a2Txe8V3Xn+WcRLG9LUu1t85sXj/vc+iSV8pu8wfBiVKQ4eniv/cV94Nze6wLibuWlz85/cnjiyYOBCSN0PfHyC8ma3haNJXyg4H1sGmKdDuEShnw7RkEauhV+XLrPp+qt4P4xbGwPSnYMdcq/tp3a52R6RJXylbzHsDSlWEdo/aF0PJctb8/fTjzv48OfbF4qsWvwerR0HH/4OWA+2OBtCkr1Tx27MMts+yFjsvXdHeWKpfDt3/BzvnwxKt77vU+onWGsdN+7rnprtC0qSvVHEyxloGsVw1aD3E7mgsLQbC5b1h/puw+0+7o/ENuxbDL49YzfN6fVrsc/EvRJO+UsVpx1zYuxQ6FWCx8+IiAj0/hEq1rTYNpw7bHZF3S94CEwZA5TpWE7USJe2O6B806StVXHJH+RWjrNG1JylZ3ppZknbUasym9f3COZlktUkOLGm1SS5dye6IzqFJX6niEjfVmrXT+RIWOy9O1ZtC97etTyN/fmB3NN4nIxXG9oG0wzBgIlSqZXdE+dKkr1RxyHFYM3ZCG0CzvnZHc34t74Umt1kLs+9ZZnc03sORDT/dBwc3QO/vrOUuPZQmfaWKw/oJ1kIZhV3svLiIQM+PrFHqT/fBqSN2R+T5jIHfn4XtM621CxoUbVHAY6cy+f7PXbw6dZOLAvynEm45qlLqb9kZMP8tCG8OjXraHc3FlQqx5u9/0xWmPGi1DQjQ8eF5Lf0YYr+F9k9YLTUKwZFjWLz9EJNWJTB7UxKZjhyuqFmRzOwcgku49r+9Jn2l3G31KDix15oh40FT9y4o/Aro9hZMf9pKah2etDsiz7RxMsz+j1USu/bVS3757sOn+GlVApNXJ3DgRDqVygRxV9ta9ImJpFF4iOvjRZO+Uu6Vecpan7ZWB7isi93RXJqY+6355nNfg6i21pf6255lMOUhiGoHt3xR4E9DaZnZzNhwkImx+1ix6ygBAlfXD+M/PRpzbaNqLh/Zn02TvlLutGIEnEq25mt7yyg/lwjc/DEcWGvV9x9aAmUq2x2VZzi8Hcb3t6bf9hsLQaUuuLsxhtV7jzEpNoHf1iVyKtNB7dCyPNutAbddGUn1Chd+vStp0lfKXU4fhyUfQr0bvHeUXKqCVd//9nprVNt/vNb3Uw/B6NtBAmHATxf8Q5icks7Pa/YzMXYfOw+dokxwID2ahdMnpiYxtSohNgwENOkr5S7LPrWamXlQ35VCibgSrh8Gvz9jvaf2j9sdkX0y02DcHda6xoOmQeXa5+yS5chh3pZkJsXuY/7WQzhyDK2iK/HQ1ZdxU9Nwypa0N+1q0lfKHVIPwbLPrQt8NvdPd4nWD1iLqs951frUUrO13REVvxyH1YZ6/2roNwYi/7kw1bakk0xcuY8pa/Zz5FQmVcuX5MFOdejdMpI6YeVsCvpcmvSVcocl70N2Olzzkt2RuIaI1TjswDqYdC88tNj/6vszX4St06Hb/6DhTQCkpGfx27pEJsYmsG7fcYICha6NqtE3piYd64VSItDzSmGa9JVyteP7YOU30PxO9y92Xpzy1vd/eQT6j/O+i9OFtexz+OtLaDuUnNYPsjz+MBNj9/H7xoNkZOfQsHp5Xu7RmFuaR1ClnGc1WDvbRZO+iIwEegDJxpjLndteBR4AcpfbedEYM8P53AvA/YADeNwYM9O5vRvwERAIfGOMedu1b0UpD7HoHev71c/ZG4c71GgB178BfzwHyz6Dq2xcBKa4bP4VZr5I2mU38nXgQCYNn0/CsdOElCpB35ia9I2pyeU1Qmy5KFsYBRnpfw98Cow6a/sHxph3824QkcZAP6AJEAHMEZH6zqc/A64DEoCVIjLVGLO5CLEr5XkOx8OaMVav/Io17Y7GPdo86Kzvv2LV98+qbfuSjF3LKPHTA+wMbkjPzX3J2BxPh7qhPHNDA25oUp1SQR7cUuM8Lpr0jTGLRCS6gMfrBYw3xmQAu0QkHsi94hNvjNkJICLjnftq0le+ZcGbUKIUdLRhsfPiIgK9PoOvOjrr+4s8soVwYRlj2Lg/hTl/LmNg3GBSciryr+DnePjay7m9ZQ0iK3nIOgiFVJSa/qMicg8QCzxtjDkG1ACW59knwbkNYN9Z29uc78AiMgQYAhAVFVWEEJUqRgc3WLfld/w/KFfV7mjcq3RF6P09jLwBfhlqzWbxkvLG+RxJzeCXtYlMit1H0sH9TCn5KsElAjh68ximNo8hIMC731+uwl5a/gK4DGgOHAByF9fM77+KucD2fBljRhhjYowxMWFhYYUMUaliNu8N62LnVY/ZHUnxiGwJ171mzWhZ/oXd0RRKtiOHeVuSeOjHVbR9ay6vT9tM+RLZzKr+JbVKHKPcwEm0aNHKZxI+FHKkb4xJyn0sIl8D05w/JgB5C5mRQKLz8fm2K+X99v4F2/6Aa1+xf7Hz4tT2Ydi9xGo6VrON9YfAC+w8lMqkVQlMXpVA8skMqpQNZtBV0fRpWYP6Cx+FuHXWTKWo8xYkvFahkr6IhBtjDjh/vBXY6Hw8FRgrIu9jXcitB6zAGunXE5HawH6si713FiVwpTxG7jKIZataFzn9Se78/a+uhp8GwYOLPfaPXmpGNjPWH2DSqn2s3H2MwADhmgZh9ImpSZeGVQkKDICZL1krnF3/BjS5xe6Q3aIgUzbHAZ2BUBFJAF4BOotIc6wSzW7gQQBjzCYRmYh1gTYbGGqMcTiP8ygwE2vK5khjjHtWCFCquO2cD3uWQPfhEFzW7miKX5nK0Oc7q77/61C4Y7TH1PeNMcTuOcbElfuYvuEAaZkOLgsrywvdG3JrixpULZ+n0dlfI6w2E62HQDvfnYoqxpy3tO4RYmJiTGxsrN1hKJU/Y+Dra6wVph6LhRKefWOOWy39FGa9ZN2x2vYhW0M5eCKdyasT+GlVArsOn6JscCA9r4igT0xNWkRVPHdO/ZYZMGEA1O9m/dHy5NXNCkBEVhlj8p1Lq3fkKlUUW6ZB4hro9bl/J3yAdkOt+v6sf1u9eWq0KNbTZ2bnMDcuiYmx+1i47RA5BtrUrsyj19Sle9PqlAk+T7rbv8pqHR1+Bdz+jdcn/IvRkb5ShZXjgC+uApMDDy+DQB1DkXYUvuoEEgAPLiqW+n7cgRQmxSbwy9r9HD2VSfWQUvRuGUnvlpFEh16k3HZst7UsZFBpGDzXZ6ba6khfKXfYMAkObYE+P2jCz1WmMvQeCd91h6mPQd9Rbqnvn0jLYuq6/UyMTWDD/hMEBwZwXROr0VmHuqEEFmSKZdpRGN0bHFkwaIbPJPyL0d9UpQojOxPmv2mVBBrdbHc0nqVma2vq6uyXrcZzrR9wyWFzcgx/7jjMpNgE/th0kMzsHBqHh/Bqz8b0al6DSmWDC36w7AyYcBcc3wN3/wJh9S/+Gh+hSV+pwlgzykoYN72vK0nlp92jVn1/5osQ2Qoimhf6UEdPZfL90t1MXpXA/uOnqVA6iDtbR9G7ZSSX16hw6QfMyYFfHoY9f8Lt30J0+0LH5o006St1qTLTYOFwiLoK6l5rdzSeKSAAbv0SvuwAkwbBgwutu5Uv0ao9Rxk6Zg1JJ9PpVC+MF25sSNdG1YrW6Gzea1a7jGtfgaa9C38cL6VJX6lLtfJrSD1ozU33kPnoHqlMZej9nbO+/7h1h2sB/3sZY/h2yS7e/n0LERVL89ujHQo3qj9b7EhY8gG0vBc6/Kvox/NC+rlUqUuRfsJKGnWvg1pX2R2N54tqA9e+DJt/gdhvC/SSlPQsHh69mjemx9GlYVV+e8xFCX/bLJj+NNS7Hm5812//YOtIX6lLsewzOH3M+xc7L05XPQG7/4Q/XrDq++FXnHfXTYknGDpmNfuOnealGxsxuGNt1yxOkrjWKjNVu9z69OHHs610pK9UQZ06bCX9xrcU6cKk3wkIgFu/gjKhVuJNT8l3t4kr93Hb50s5neVg/JC2PNCpjmsS/vG9MLavVW66cyKU9JxFyu2gSV+pglryAWSl+c5i58WpbBVr/v6xPfDbE1b7CqfTmQ7+b9I6np28npjoSkx/vCOtol206Prp4zCmD2Slw4BJEBLumuN6MU36ShXEif2w4mu44k6/mtPtUrXaQZeXYNPPsOo7wGpxfOvnfzJ5dQKPd6nLqPvaEOqqhcWzM625+Ed2wB0/QtVGrjmul/PfwpZSl2LRO1a7hc4+uNh5cWr/L6u+//vzLEqrzSNzMwkKFL4b1IrODVx4R6wx1h3BuxdbpaU6V7vu2F5OR/pKXcyRHbD6R4i5Dyrq8p1FEhBA5s1fkhJQnsg5D9E0LIDpj3d0bcIH627p9eOtUtwV/Vx7bC+nSV+pi5n/ptVBs+PTdkfi9fYfP80dY7YzOPVhogOSGV1tHBEVSl38hZdi9Y/WJ7Mr74JOz7j22D5AyztKXcjBDbDxJ+jwFJSvZnc0Xm3B1mT+NWEtWQ7D//oPIOC4sdYVrtMJWg5yzUni51oXii/rAj0+9Nu5+BeiSV+pC5k3DEpWgPaP2x2J13LkGD6as41P5sfToFp5Ph/Qgjph5SDnaWd9/zmoEQPVLy/aiQ5ugIkDrQu2fX6AwCDXvAEfo+Udpc5n3wrY9ruV8EtXsjsar3Q4NYN7Rv7Fx/Pi6d0ikimPtLcSPljz92/7GkpVtObvZ6QW/kQn9sOYvlCyvDUXv1SIS+L3RZr0lcrPmcXOw6CNvUv/eauVu49y08eLid19jHdub8bwPldQOvisRmnlwqzVqo7ugOlP/WP+foGlp1g3X2WctObiV6jhmjfgozTpK5WfnQus6X4d/8/v7+C8VMYYvl60k34jllM6KJApj7Snb6ua539B7Y7Q+QVYPwHW/HhpJ3NkwcR7rMVs+v5Q9BKRH7ho0heRkSKSLCIb82wbLiJbRGS9iEwRkYrO7dEiclpE1jq/vszzmpYiskFE4kXkY3HJ/dVKuUHuKD8kEmLutTsar3LidBYP/riKYTPiuL5xNaY+1oHGEQUotXR8GmpfDTOegaRNBTuZMTDtSdg5H3p+pG2uC6ggI/3vgW5nbZsNXG6MaQZsA17I89wOY0xz51fez8VfAEOAes6vs4+plGfYMh0SV0Pn53Wx80uwcf8Jen6yhHlbknm5R2M+H9CCkFIFvJgaEGiVeUpVKHh9f9FwWDMaOj1rTc9UBXLRpG+MWQQcPWvbLGNMtvPH5UDkhY4hIuFAiDFmmbFWYh8F3FK4kJVyoxyHNY2wSl24or/d0XgFYwzjVuzlti+WkuXIYcKDbbm/QyG6Y5aral3YPbwdZvzfhfddOw7mD4Nm/eCaFwsfvB9yRU3/PuD3PD/XFpE1IrJQRDo6t9UAEvLsk+Dcli8RGSIisSISe+jQIReEqFQBbfgJDsVZd3L6cfvdgkrLzObpSet44ecNtKldmWmPdaBlrSI0S6tztfUJa904WDMm/312LoSpj0LtTnDzJzoX/xIV6bdaRF4CsoHcf50DQJQx5oiItAR+EZEmQH7/Kue9TG+MGQGMAIiJiSnE5XylCiE7Exa8CdWbWu2T1QXtOJTKw6NXsT05lSe71uOxLvUIDHBBAu70jLV+7fSnoUaLfzZKS46DCXdDlXrQ90cocQmLoSugCCN9ERkI9AAGOEs2GGMyjDFHnI9XATuA+lgj+7wloEggsbDnVsot1vwIx3ZDl//oYucX8du6RG7+ZAmHUzMZdV9rnuxa3zUJH6z6/m3fWHPuJw2CzFPW9pQDMLo3BJW2pmaWruia8/mZQv1mi0g34DngZmNMWp7tYSIS6HxcB+uC7U5jzAHgpIi0dc7auQf4tcjRK+UqWadh4TtQsy3Uu87uaDxWRraDV37dyGPj1tAwPITpj3egY70w15+ofDW4/Ws4tNWa0ZORas3FP30MBkyEiheYAqou6KLlHREZB3QGQkUkAXgFa7ZOSWC282LNcudMnU7AayKSDTiAh4wxuReBH8aaCVQa6xpA3usAStlrhXOx894jtUZ8HgnH0hg6dg3r9h1ncIfaPNe9IUGBbvxEVKczXP0sLPwfJKy0up32H3/B5RbVxYkpzB1wxSgmJsbExsbaHYbyZekp8FEziGgBd/9sdzQeab6zWZrDYRjepxndLi+mFahyHDCql3WjXI8P9b6JAhKRVcaYmPye0+kJSuUudn7ty3ZH4nEcOYYPZm/j0/nxNAoP4YsBLYgOLVt8AQQEQr8xVjO16A7Fd14fpklf+bdTR2DZp9DoZoi40u5oPMqhkxk8MX4NS3cc4Y6Ymvy3VxNKBQVe/IWuVqqCJnwX0qSv/NuS93Wx83z8tfMIj41bQ0p6FsN7N6NPjF449RWa9JX/yl3svFk/qNrQ7mg8gjGGrxbtZPjMrURVLsOo+1vTsLq2KfYlmvSV/1o0XBc7z+NEWhZPT1rHnLgkbmoaztu3N6V8QXvnKK+hSV/5pyM7rJuxWt4LlaLtjsZ2GxJO8MjYVRw8kc4rPRsz6KroS++do7yCJn3lnxa8DQFB0Okijb18nDGGsSv28t+pmwktF8yEB9vRIkpXCfNlmvSV/0naBBsmQfsnoHx1u6OxTVpmNi9N2ciUNfvpVD+MD+9oTuWy2svG12nSV/5n3jCrr0v7J+yOxDbxySd5ePRq4g+l8vR19Rl6TV0CXNU7R3k0TfrKvyTEwtbpcM2/oUwRWgB7sV/X7ueFnzdQOiiQH+9rQ4d6oXaHpIqRJn3lX+a+BmVCoa3/LXaeke3gjWlx/Lh8D62iK/FJ/xZUr1DK7rBUMdOkr/zHzgWwayHc8JZV3vEj+46mMXTsatYnnGBIpzo8c0MD9zZLUx5Lk77yD8bA3NchpAbE3Gd3NMVqblwST01cR44xfHV3S25o4r8Xr5UmfeUvtv4O+2Oh58cQ5B8ljWxHDu/P3sbnC3bQJCKELwa0JKpKGbvDUjbTpK98X04OzHsdKl8Gze+0O5pikXwyncfGruGvXUfp3zqKV3o2tqdZmvI4mvSV79s4GZI3w+3fQqDvtxVY7myWlpqezft9r+C2FpEXf5HyG5r0lW9zZMH8YVCtKTS5ze5o3Conx/Dloh28O3Mr0aFlGTO4DfWr+dcFa3VxmvSVb1szGo7tgjsn+vRi58fTMnl64jrmbkmm5xURvHVbU8qV1P+91bn0t0L5rjOLnbeBetfbHY3brE84zsOjV5N8Mp3XejXh7ra1tFmaOi9N+sp3rfwWTibC7V/75GLnxhhG/7WX13/bTFj5kkx66Cqa16xod1jKwxXo866IjBSRZBHZmGdbZRGZLSLbnd8rObeLiHwsIvEisl5EWuR5zUDn/ttFZKDr345STukpsPg9uKyLTy61dyojmyfGr+XlXzbSvm4Vpj3WQRO+KpCCFjm/B7qdte15YK4xph4w1/kzQHegnvNrCPAFWH8kgFeANkBr4JXcPxRKudzyL+D0Uejie4udb086Sa/P/mTa+kSeuaEB3w5sRSXtjqkKqEDlHWPMIhGJPmtzL6Cz8/EPwALgOef2UcYYAywXkYoiEu7cd7Yx5iiAiMzG+kMyrkjvQKmzpR2FpZ9Ao55Qo8XF9/dgxhgSjp1mU2IKmxNPsCkxhaU7jlC2ZAlGD27DVZdpszR1aYpS069mjDkAYIw5ICJVndtrAPvy7Jfg3Ha+7ecQkSFYnxKIiooqQojKLy35ADJTrU6aXiTbkcOOQ6fYlHiCzYkpVqI/kMKJ01kABAjUrVqOm6+I4Onr61M1xD/uLFau5Y4LufldMTMX2H7uRmNGACMAYmJi8t1HqXylHIAVI+AKz17s/HSmgy0HrcSeO4rfcvAkGdk5AJQsEUDD8BBuahZOk4gQmkRUoGH18npXrSqyoiT9JBEJd47yw4Fk5/YEoGae/SKBROf2zmdtX1CE8yt1rkXDIccBnZ+/+L7F5HhapjO5/z2C33EolRzncKZC6SCaRIRwT7taNImoQOOIEOqElqWEdsFUblCUpD8VGAi87fz+a57tj4rIeKyLtiecfxhmAm/muXh7PfBCEc6v1D8d3QWrf4CWg2xZ7NwYw4ET6WcSvDWCT2H/8dNn9gmvUIomESF0b5o7gg+hRsXSOq9eFZsCJX0RGYc1Sg8VkQSsWThvAxNF5H5gL9DHufsM4EYgHkgD7gUwxhwVkdeBlc79Xsu9qKuUS5xZ7PwZt5/KkWPYdTg1T3nGSvTH0qz6uwjUCS1Ly1qVuKddLRo7SzS6Bq2yW0Fn7/Q/z1PX5rOvAYae5zgjgZEFjk6pgkqOg/UToP3jLl/sPD3Lwbakk/8YwW85cJLTWQ4AggMDaFC9PDc0qU6TiBAaR1SgUXh5ygTrvY/K8+hvpfIN895wLnb+ZJEOc+J01plRe279Pf5QKg5nAb58qRI0Dg+hf+so5+g9hLpVy+kqVMpraNJX3m//KtgyDa55qcCLnRtjSErJYPOBE2za75xFc+AE+47+XX+vWr4kTSJCuK5xtTMzaGpW1vq78m6a9JX3m/s6lKkCbR/O9+mcHMPuI6fO1N9zR/FHTmWe2ad2aFmaRVakX6uoMwk+rHzJ4noHShUbTfrKu+1aBDvnww1vQsnyZGQ72J6UeqZEsykxhbgDKZzKtOrvQYFCvarl6dKwqpXca1SgUXiItiFWfkN/05XXOnk6E2a8QkDJary+txXrViwmPvkkWQ6r/l42OJDGESH0ialJ4/AQGkeEUL9aeYJLaP1d+S9N+sorJJ9MPzM1cnNiChn71jA47WvaBsTxfNZg5mw/QeOICnRuEHamPFOrchkCArT+rlRemvSVRzHGsPdo2j+mR25KTOHQyQwAQjnBK2V/5ibHHDKCK7Cl+X/5V8cHeSuklF5gVaoANOkr22Q5ctielGpdWD1gJfe4xBROZmQDEBgg1Ktajo71QmlavTRdjv9M1MZPkex0aDeU0p2eoSBWWJcAABNkSURBVGFp7SGv1KXQpK+KxamM7L8bjO23pkduO5hKpsNqMFY6KJBG4eXpdWUETSIq0MRZfy9VIgC2TIdZ/7bWuq3fHa5/A0Lr2vyOlPJOmvSVyx1JzTjTFji3TLPr8CmMs8FYpTJBNImowL3to8+0J6gdWpbAs+vvBzfCzBesGTphjeCun6HuOTeBK6UugSZ9VWj5LfCxKTGFgynpZ/apUbE0jSNCuPmKv0fw4RUuUn8/ddi6w3b1D1CqAtz4LrS8FwL111WpotL/i1SB5C7wkfcO1rMX+LgsrBxt61Q+k9wbR4RQscwlNBjLzoQVX8HCdyArDVo/CFc/W+C7bJVSF6dJX52jQAt8VC/PjXnaAzesHkLp4EIu8GEMbPsDZr4ER3dAvevh+mEQVt+F70opBZr0/d7xtMwzjcVyp0jmXeAjpFQJmkRU4O62tWhSw6q/u3SBj6TNMPNF667a0PowYDLU6+qaYyulzqFJ309c0gIfl1ensbNEE1nJTQ3GTh2BBW9C7EgoGQLd/get7ofAINefSyl1hiZ9H1SQBT5qh5alRa1K3N2ullV/Dw+hSrliaDDmyIIVX8PCtyEjFVoNhs4vaN1eqWKiSd9HJKWk8/Winazae+y8C3w0zlN/L2tHg7Fts6xSzpHtcFkXq0la1UbFH4dSfkyTvpdLz3Lw7ZJdfDY/nixHDldGVaJf65pnZtB4xAIfyVtg1ksQPweq1IU7J1oXa7VtglLFTpO+lzLGMGPDQd6cEcf+46e5oUk1XryxEbWqlLU7tL+lHbXWrV35DQSXs0b2rR6AErpOrFJ20aTvhTbuP8Fr0zazYtdRGlYvz9jBbbiqbqjdYf3NkWVdoJ3/JmSkWDdWXfMSlK1id2RK+b1CJ30RaQBMyLOpDvAfoCLwAHDIuf1FY8wM52teAO4HHMDjxpiZhT2/P0o+mc67M7cyaVUClcsE8+atTbmjVc1z2xfYKX4O/PEiHN4Kta+Gbm9BtSZ2R6WUcip00jfGbAWaA4hIILAfmALcC3xgjHk37/4i0hjoBzQBIoA5IlLfGOMobAz+Ij3LwXd/7uaz+fFkZDsY3KE2j11bj5BSHjS98fB26yLt9llQuQ70GwcNumvdXikP46ryzrXADmPMngvM6e4FjDfGZAC7RCQeaA0sc1EMPscYw8xNBxk2I459R0/TtVE1XrqpEbVDPahuf/qY1TZhxQgIKmN1wGw9BEro+rJKeSJXJf1+wLg8Pz8qIvcAscDTxphjQA1geZ59EpzbziEiQ4AhAFFRUS4K0btsTkzhtWmbWL7zKPWrlePH+1vTsV6Y3WH9zZENq76z6vanj0HLgXDNv6GcB8WolDpHkZO+iAQDNwMvODd9AbwOGOf394D7gPw+Apj8jmmMGQGMAIiJicl3H191ODWD92ZtZfzKfVQsHcTrt1xO/1Y1Xdf2wBV2zLdKOcmbIbqjVbev3tTuqJRSBeCKkX53YLUxJgkg9zuAiHwNTHP+mADUzPO6SCDRBef3CRnZDn5YuptP5sZzOsvBfe1r83iXelQo40F1+yM7rKZo236HStFwx2ho2EPr9kp5EVck/f7kKe2ISLgx5oDzx1uBjc7HU4GxIvI+1oXcesAKF5zfqxljmL05iWEz4thzJI0uDavy0k2NuCysnN2h/e30cVg0HP76CkqUgq7/hbYPa91eKS9UpKQvImWA64AH82x+R0SaY5Vuduc+Z4zZJCITgc1ANjDU32fubDmYwuvTNvNn/BHqVi3HD/e15ur6HlQTz3FYC5nMe8O60erKu6DLy1C+mt2RKaUKqUhJ3xiTBlQ5a9vdF9h/GDCsKOf0BUdSM3h/9jbGrdhLSOkg/ntzE+5sE2V/u4S8di606vZJGyHqKqtuH9Hc7qiUUkWkd+QWo8zsHEYt281Hc7eTlungnnbRPNm13qWtLuVuR3fCrJdhyzSoGAV9foDGvbRur5SP0KRfDIwxzNuSzLDpcew8fIqr64fxco9G1K1a3u7Q/pae4qzbfwkBQVYZp92jEFTK7siUUi6kSd/NtiWd5PVpm1m8/TB1wsry3aBWXNOwqt1h/S3HAWtGw7zX4dQhaD4Arv0PlK9ud2RKKTfQpO8mx05l8sGcbYz5ay9lgwP5T4/G3N2ulmfV7XcvgT+eh4MboGZbq+VxjRZ2R6WUciNN+i6W5cjhx2V7+HDONk5lOhjQJoonu9anclkPqtsf223V7eOmQoWa0HskNLlN6/ZK+QFN+i40f0syr0/fzM5Dp+hYL5SXezSmfjUPqttnnITF78GyzyCghNXu+KrHIKi03ZEppYqJJn0XiE8+yevT4li47RC1Q8vyzT0xXNuoqnsWFC+MnBxYNxbmvgapSdCsH3R9BUIi7I5MKVXMNOkXwfG0TD6cs50fl++hTHAg/76pEfe0iya4hAfV7fcster2B9ZBZGur5XFkS7ujUkrZRJN+IWQ7chjz114+mLONlNNZ9G8dxVPX1adKOQ9qS3BsD8x5BTZNgZAacNs30LS31u2V8nOa9C/Rwm2HeGPaZrYnp3LVZVV4uUdjGoWH2B3W3zJSYckHsPQTkAC4+nlo/zgEe1APfqWUbTTpF9COQ6kMmx7HvC3J1KpShhF3t+S6xtU8p25vDKyfALNfgdSD0LQPdH0VKkTaHZlSyoNo0r+IE2lZfDxvOz8s3U2poEBe6N6QQe2jKVki0O7Q/pZxEn57AjZOhhot4Y4foWZru6NSSnkgTfrnke3IYdzKfbw/ayvHT2fRr1VNnrquAWHlPahuD5AcBxPuhqM7rNYJHZ6CAA+6kKyU8iia9POxZPthXp+2ma1JJ2lTuzL/6dmYJhEV7A7rXOvGw7R/QXA5uOdXqN3J7oiUUh5Ok34euw6fYtj0OObEJVGzcmm+vKsFNzSp7jl1+1xZ6fDHc7Dqe6jV3rqjVnvlKKUKQJM+kJKexafz4vnuz10EBwbwbLcG3Ne+NqWCPKhun+voLph4DxxcD+2ftEo6gfrPqJQqGL/OFo4cw4SV+3hv1laOpmXSp2Uk/3dDA6qW99B2wlumw5SHrSXm+4+HBt3tjkgp5WX8Nukv3XGY137bzJaDJ2kdXZkfejbm8hoeWLcHcGRZLRSWfgzhzaHvD9bC5EopdYn8LunvPZLGsBmbmbkpiRoVS/PZnS24sakH1u1zpRyAn+6Fvcsg5n644U1d2EQpVWh+k/RPpmfx6fx4vluymxKBwjM3NOD+Dh5at8+1cwFMHgyZp6w2Cs362B2RUsrLFTnpi8hu4CTgALKNMTEiUhmYAEQDu4G+xphjYg2nPwJuBNKAQcaY1UWN4UIcOYafVu1j+MxtHE7N4PYWkTzbrQHVQjx4tJyTY7VAXvAmVKkHA6dB1YZ2R6WU8gGuGulfY4w5nOfn54G5xpi3ReR558/PAd2Bes6vNsAXzu9u8dfOI7w2bTObElOIqVWJkYNiaBZZ0V2nc420o/DzEIifbbVS6PEhlCxnd1RKKR/hrvJOL6Cz8/EPwAKspN8LGGWMMcByEakoIuHGmAOuPHlKehbPT17PjA0HiahQio/7X0nPZuGeW7fPlRALEwfCqWS46X2IuU+7YiqlXMoVSd8As0TEAF8ZY0YA1XITuTHmgIjkrgReA9iX57UJzm3/SPoiMgQYAhAVFXXJAZULLsHh1Eyeuq4+D3SsQ+lgD67bg9UsbcUImPkShITDfTN1rVqllFu4Ium3N8YkOhP7bBHZcoF98xu2mnM2WH84RgDExMSc8/zFBAQIE4a09fyRPUB6Ckx9DDb/AvW7w61fQOlKdkellPJRRU76xphE5/dkEZkCtAaScss2IhIOJDt3TwBq5nl5JJBY1Bjy4xUJP2mTdXft0V3Q9b9w1ePaLE0p5VZFyjAiUlZEyuc+Bq4HNgJTgYHO3QYCvzofTwXuEUtb4ISr6/leY+1Y+Ppaqy3ywN+gw5Oa8JVSblfUkX41YIpzVF0CGGuM+UNEVgITReR+YC+QO8F8BtZ0zXisKZv3FvH83ifrNPz+LKweBdEd4fZvoXw1u6NSSvmJIiV9Y8xO4Ip8th8Brs1nuwGGFuWcXu3oTmeztA3Q8Wno/KI2S1NKFSvNOMUl7jf45RFr3do7J0L9G+yOSCnlhzTpu5sjC+a8Css+hYgWVrO0ipc+DVUppVxBk747pSTCpHth33JoPQSufwNKeNhyi0opv6JJ3112zLeapWWnWytbXX673REppZQmfZfLyYFFw2HBWxDWEPqOgrD6dkellFKAJn3XOnUEfn4AdsyFZv2gx/sQXNbuqJRS6gxN+q6ybwVMGgSnDkPPj6DFQG2WppTyOJr0i8oY+OtLmPVvCKkB98+CiOZ2R6WUUvnSpF8U6Snw61CImwoNboJbPofSHt6vXynl1zTpF9bBDdbdtcf2wHWvw1WPaTlHKeXxNOkXxuofYcb/QamKMGga1LrK7oiUUqpANOlfisw0mPEMrB0NtTtZzdLKVb3465RSykNo0i+oIzusck7SRuj0LHR+HgI8fEUupZQ6iyb9gtj0C/z6qNURc8BPUO86uyNSSqlC0aR/IdmZMPs/8NcXUCMG+nwPFWte9GVKKeWpNOmfz4kE62arhJXQ5iFrhk6JYLujUkqpItGkn5/4OTD5AXBkWqP7JrfaHZFSSrmEJv28chyw8H+w8B2o2shqlhZaz+6olFLKZTTp50o9BD8Php0LoPkAuPFdCC5jd1RKKeVSmvQB9i636venj8HNn0KLu+2OSCml3CKgsC8UkZoiMl9E4kRkk4g84dz+qojsF5G1zq8b87zmBRGJF5GtImL/IrHGwNJP4LsboUQpuH+2JnyllE8rykg/G3jaGLNaRMoDq0RktvO5D4wx7+bdWUQaA/2AJkAEMEdE6htjHEWIofBOH7eapW2ZBo16Qq/PoFQFW0JRSqniUuikb4w5ABxwPj4pInFAjQu8pBcw3hiTAewSkXigNbCssDEU2oH11t21J/bBDW9C20e0WZpSyi8UuryTl4hEA1cCfzk3PSoi60VkpIhUcm6rAezL87IEzvNHQkSGiEisiMQeOnTIFSFajIFVP8A3XSE7AwbNgHZDNeErpfxGkZO+iJQDJgNPGmNSgC+Ay4DmWJ8E3svdNZ+Xm/yOaYwZYYyJMcbEhIWFFTVES2Ya/PII/Pa41RXzocUQ1cY1x1ZKKS9RpNk7IhKElfDHGGN+BjDGJOV5/mtgmvPHBCBvD4NIILEo5y+ww9utck5yHHR+ATo9o83SlFJ+qSizdwT4FogzxryfZ3t4nt1uBTY6H08F+olISRGpDdQDVhT2/AW28WcY0RlSk+CuydodUynl14oy0m8P3A1sEJG1zm0vAv1FpDlW6WY38CCAMWaTiEwENmPN/Bnq1pk72ZnWurUrvoLI1lY7hQoXus6slFK+ryizd5aQf51+xgVeMwwYVthzFtjpYzC6N+yPhbZD4br/QmCQ20+rlFKezjfvyC1ZASrXhvaPQ+NedkejlFIewzeTfkAA3P6N3VEopZTHcck8faWUUt5Bk75SSvkRTfpKKeVHNOkrpZQf0aSvlFJ+RJO+Ukr5EU36SinlRzTpK6WUHxFj8u1u7DFE5BCwp5AvDwUOuzAcb6Dv2ff52/sFfc+XqpYxJt++9B6f9ItCRGKNMTF2x1Gc9D37Pn97v6Dv2ZW0vKOUUn5Ek75SSvkRX0/6I+wOwAb6nn2fv71f0PfsMj5d01dKKfVPvj7SV0oplYcmfaWU8iM+mfRFpJuIbBWReBF53u54ioOIjBSRZBHZePG9vZ+I1BSR+SISJyKbROQJu2NyNxEpJSIrRGSd8z3/1+6YiouIBIrIGhGZZncsxUFEdovIBhFZKyKxLj22r9X0RSQQ2AZcByQAK4H+xpjNtgbmZiLSCUgFRhljLrc7HncTkXAg3BizWkTKA6uAW3z531lEBChrjEkVkSBgCfCEMWa5zaG5nYg8BcQAIcaYHnbH424ishuIMca4/IY0XxzptwbijTE7jTGZwHjA5xfKNcYsAo7aHUdxMcYcMMasdj4+CcQBNeyNyr2MJdX5Y5Dzy7dGbfkQkUjgJkDXQHUBX0z6NYB9eX5OwMeTgb8TkWjgSuAveyNxP2eZYy2QDMw2xvj8ewY+BJ4FcuwOpBgZYJaIrBKRIa48sC8mfclnm8+PhvyViJQDJgNPGmNS7I7H3YwxDmNMcyASaC0iPl3KE5EeQLIxZpXdsRSz9saYFkB3YKizfOsSvpj0E4CaeX6OBBJtikW5kbOuPRkYY4z52e54ipMx5jiwAOhmcyju1h642VnjHg90EZHR9obkfsaYROf3ZGAKVtnaJXwx6a8E6olIbREJBvoBU22OSbmY86Lmt0CcMeZ9u+MpDiISJiIVnY9LA12BLfZG5V7GmBeMMZHGmGis/5fnGWPusjkstxKRss7JCYhIWeB6wGWz8nwu6RtjsoFHgZlYF/cmGmM22RuV+4nIOGAZ0EBEEkTkfrtjcrP2wN1YI7+1zq8b7Q7KzcKB+SKyHmtwM9sY4xdTGP1MNWCJiKwDVgDTjTF/uOrgPjdlUyml1Pn53EhfKaXU+WnSV0opP6JJXyml/IgmfaWU8iOa9JVSyo9o0ldKKT+iSV8ppfzI/wM1xubLRA8PrAAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Setting the Axis, Ticks, Grids</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#use an alyusis for the axis fuction</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">axes</span><span class="p">()</span>

<span class="c1"># changing the x axes and y axes limit (making them longer)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">11</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">([</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span><span class="mi">11</span><span class="p">])</span>

<span class="c1"># changing the x axes and yaxes ticks</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xticks</span><span class="p">([</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">9</span><span class="p">,</span> <span class="mi">10</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_yticks</span><span class="p">([</span><span class="mi">200</span><span class="p">,</span> <span class="mi">400</span><span class="p">,</span> <span class="mi">600</span><span class="p">,</span> <span class="mi">800</span><span class="p">,</span> <span class="mi">1000</span><span class="p">,</span> <span class="mi">1200</span><span class="p">,</span> <span class="mi">1400</span><span class="p">,</span> <span class="mi">1600</span><span class="p">,</span> <span class="mi">1800</span><span class="p">,</span> <span class="mi">2000</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Add Grids</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#use an alyusis for the axis fuction</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">axes</span><span class="p">()</span>

<span class="c1"># changing the x axes and y axes limit (making them longer)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">11</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">([</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span><span class="mi">11</span><span class="p">])</span>

<span class="c1"># changing the x axes and yaxes ticks</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xticks</span><span class="p">([</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">9</span><span class="p">,</span> <span class="mi">10</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_yticks</span><span class="p">([</span><span class="mi">200</span><span class="p">,</span> <span class="mi">400</span><span class="p">,</span> <span class="mi">600</span><span class="p">,</span> <span class="mi">800</span><span class="p">,</span> <span class="mi">1000</span><span class="p">,</span> <span class="mi">1200</span><span class="p">,</span> <span class="mi">1400</span><span class="p">,</span> <span class="mi">1600</span><span class="p">,</span> <span class="mi">1800</span><span class="p">,</span> <span class="mi">2000</span><span class="p">])</span>

<span class="c1"># add Grids</span>
<span class="n">ax</span><span class="o">.</span><span class="n">grid</span><span class="p">()</span>
<span class="c1">#plot</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Change line appearence</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># &#39;-&#39; Solid Line</span>
<span class="c1"># &#39;--&#39; Dashed Line</span>
<span class="c1"># &#39;-.&#39; Dash Dot Line</span>
<span class="c1"># &#39;:&#39; Dotted Line</span>

<span class="c1">#plot</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">,</span> <span class="s1">&#39;--&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">,</span> <span class="s1">&#39;:&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Use Colors</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">,</span>  <span class="s1">&#39;r&#39;</span><span class="p">,)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">,</span> <span class="s1">&#39;b&#39;</span><span class="p">,)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Adding Markers</p>
<p>Options Can be found here:
<a href="https://matplotlib.org/api/markers_api.html">https://matplotlib.org/api/markers_api.html</a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[26]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">,</span>  <span class="s1">&#39;o--&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">,</span> <span class="s1">&#39;v:&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Change Color on Markers</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">,</span>  <span class="s1">&#39;ro--&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">,</span> <span class="s1">&#39;bv:&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Add Labels</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># labels </span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;X axis label&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Y axis label&#39;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">,</span>  <span class="s1">&#39;ro--&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">,</span> <span class="s1">&#39;bv:&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Annotating the Chart</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[29]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Annotating </span>
<span class="n">plt</span><span class="o">.</span><span class="n">annotate</span><span class="p">(</span><span class="n">xy</span><span class="o">=</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">500</span><span class="p">],</span> <span class="n">s</span><span class="o">=</span><span class="s1">&#39;Make a point&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">annotate</span><span class="p">(</span><span class="n">xy</span><span class="o">=</span><span class="p">[</span><span class="mi">5</span><span class="p">,</span><span class="mi">1500</span><span class="p">],</span> <span class="n">s</span><span class="o">=</span><span class="s1">&#39;Make another point&#39;</span><span class="p">)</span>
<span class="c1"># plot</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers</span><span class="p">,</span>  <span class="s1">&#39;ro--&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">6</span><span class="p">),</span> <span class="n">numbers2</span><span class="p">,</span> <span class="s1">&#39;bv:&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Create a Legend</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[40]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">numbers</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s2">&quot;test1&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">numbers2</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s2">&quot;test2&quot;</span><span class="p">)</span>
<span class="c1"># Place a legend to the right of this smaller subplot.</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">bbox_to_anchor</span><span class="o">=</span><span class="p">(</span><span class="mf">1.05</span><span class="p">,</span> <span class="mi">1</span><span class="p">),</span> <span class="n">loc</span><span class="o">=</span><span class="s1">&#39;upper left&#39;</span><span class="p">,</span> <span class="n">borderaxespad</span><span class="o">=</span><span class="mf">0.</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAcsAAAD4CAYAAACDm83wAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjAsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+17YcXAAAgAElEQVR4nO3dd3hU1dbA4d9Koya0JCQBQkBqQhNCUaqIBQE7iHIVCyKK7eqHivVeFa+9K4q9gAoCioAivSiCCR2C9BJKEloqqbO/P84EIy0hmcmZZNb7PHmYOXPmnDUiWbPb2mKMQSmllFJn5mN3AEoppZSn02SplFJKFUOTpVJKKVUMTZZKKaVUMTRZKqWUUsXwszuA4gQHB5uoqCi7w1BKqQojPj7+kDEmpIzXCPXz8/sYaIN3NKwcwIb8/PwRnTp1Sj75RY9PllFRUcTFxdkdhlJKVRgisrus1/Dz8/s4LCysdUhIyFEfH59Kv8bQ4XBISkpK9MGDBz8Grjz5dW/4tqCUUurctQkJCUnzhkQJ4OPjY0JCQlKxWtKnvl7O8SillKoYfLwlURZyft7T5kVNlkoppVQxNFkqpZTyOIcOHfJ98cUXSzVJ6dlnnw1NT08/kd/uu+++BmFhYe2qV69+fmnj0WSplFLK4xw+fNj3k08+CS3Nez/88MP6GRkZJ/Lb1VdffWzFihUJZYnH42fDKqWU8j4PP/xww71791Zp1apVdO/evdNCQ0Pzpk+fXjc3N1cGDBhw7I033tiflpbmc+WVVzY9cOBAgMPhkEceeWR/UlKSf3Jysn/v3r1b1KlTJ3/FihVbLr744syyxqPJUiml1FmN+X5toy0H06u78potwgKzXrm+/d4zvf7aa68lDhw4sNrmzZs3TZs2LWjKlCl11q1bl2CMoV+/fs1+/vnnmklJSX5hYWF5ixYt2gZWa7RevXoF48ePr7948eIt4eHh+a6KV7thlapIstNgzSQoyLM7EqXKzS+//BK0ZMmSoOjo6OiYmJjo7du3V928eXPVjh07Hl+6dGnQ3Xff3eCXX36pWa9evQJ3xaAtS6UqkgXPwcoJkJwAlz5ndzTKS5ytBVgejDE8+OCDB8aMGXPo5NdWrVq1aerUqbWeeOKJBvPmzUt79dVXD7gjBm1ZKlVRHN0NcZ9Btbrw+9uwZY7dESnlNrVq1SrIzMz0Aejfv3/aV199FZyamuoDsHPnTv99+/b57dq1yz8wMNBxzz33HHnwwQeT1qxZUx2gRo0aBYXnuoomS6UqisUvgfjAiHkQ1ham3wWpiXZHpZRbhIWFFXTq1CmjefPmMXPmzAkaPHjwkc6dO7dq0aJF9DXXXHPesWPHfOPj46t16NChdatWraJfeuml8KeffvoAwPDhww/179+/edeuXVsAjBo1qmH9+vXbZWdn+9SvX7/dQw89FHGu8Ygxnl2gITY21mhtWOX1Uv6C97tBt3vgsnFweDt82Avqx8Cts8DX3+4IlQcRkXhjTGxZrrF27dpd7du3P6Xbs7Jbu3ZtcPv27aNOPq4tS6UqgoXjwL869Pi39bzeeTDoLdi7AhY8b29sSnkBTZZKebr9q2HTj3DBaKgR/PfxttdDp1vhtzdh61zbwlPKG2iyVMrTLXgeqtWxkuXJLn8R6reBaSMhdV/5x6aUl9BkqZQn2/UbbJtndb9WrXXq6/7VYPDnkJ8DU++AApetwVZKFaHJUilPZYy1rrJmGHS+88znBTeHQW/CnuXW2KZSyuU0WSrlqbbNsxJg7zEQUEylsXZDoOMtsOx1631KKZfSZKmUJ3I4YP6zULsxnH9Lyd7T/2UIjbHGL9P2uzc+5V7GQN5xu6Owlau26EpPT/fp06dPsyZNmsQ0a9Ys5p577mlQmmtqslTKEyX8CAfXwUWPg19Ayd5TOH6Zlw1TR+j4ZUW24Hn4fADkZNgdiW1cuUXXww8/nLRz586NGzZs2LRixYqakydPDjrXa2ptWKU8TUE+LBgHIa2g7eBze29ICxj4BkwfCYv+Bxc/5Z4YlfvEfw5LX7W61QNq2B2NbVy5RdegQYPSAapWrWratWuXtXfv3hJ+A/2bJkulPM26b+HwVrjha/DxPff3t78Bdi2Bpa9BVHc4r6/rY1TusXUezHwImvWDAa+DiN0RWX4Y3YjkTS7doovQ6Cyufq9ct+g6dOiQ79y5c2uPGTMm6VzD1W5YpTxJfg4sehEizodWA0t/nf6vWC3TqXdCmls2YVCudmAdTBkO9aOt7nQtYXiCK7boysvL49prr206cuTIpOjo6NxzjaHYlqWIfAoMBJKNMW2cx74DWjpPqQ0cM8Z0EJEoIAH4y/naH8aYUc73dAI+B6oBs4EHjKcXplWqvMV/Dql74cq3y9aqCKhu/cL96CKYdifc8mPpWqmqfKQmwqQh1lram6ZAlUC7I/qns7QAy4Mrtui66aabopo2bZr99NNPJ5cmhpK0LD8HLj8p8BuMMR2MMR2AqcC0Ii9vL3ytMFE6jQdGAs2dP/+4plJeLzcTlrwCUT2h6UVlv15oKxjwGuxaau1YojxTdipMHGz9/Q+bAkHhdkfkEVy5Rdf9998fkZaW5vvJJ5+UOukX27I0xixxthhPISICDAHOOigiIuFAkDFmufP5l8DVwM/nGK9SldeKDyAzBW6Y6Lqxqg43wa5lsPhliLwAznNBElauk58L390Mh7bAv6Zau8go4J9bdPXt2ze1cIsugOrVqzsmTpy4c/PmzVXGjh3b0MfHBz8/P/P+++/vhr+36AoNDc2bNGnSznfeeSe8SZMm2TExMdEAI0eOTH7ooYfOaUeVEm3R5UyWMwu7YYsc7wW8XrgVjPO8jcAWIA140hizVERigReNMf2c5/UEHjXGnHZQRkRGYrVCiYyM7LR79+5z+UxKVTzHj8Jb7a2EdtN3rr12biZ81BeyjsCoZRBY37XXV6VjDPxwD6ydBFePt77YuIhu0VV67tqi60bgmyLPDwCRxpjzgYeASSISBJzua/IZs7QxZoIxJtYYExsSUqo1qUpVLL+/Y3XH9X3S9dcOqGGNX+akW/VjHWecA6HK0+KXrETZZ6xLE6Vyj1InSxHxA64FTnwNNsbkGGMOOx/HA9uBFkAi0LDI2xsCWmJEKYCMZPhjPLS5DsLauuceoa1hwKvW+OWSV9xzD1Vyqyda62A7DIPej9odjSqBsrQs+wGbjTGJhQdEJEREfJ2Pm2JN5NlhjDkApItIN+c45y3Aj2W4t1KVx9LXrCUjfR537306DIP2N1pLU3Ysdu+91JltXwg/3Q9N+8DANz1nLeWpHA6Hw2ODcwfn53Wc7rVik6WIfAMsB1qKSKKI3OF8aSj/7IIF6AWsE5G1wPfAKGPMEedrdwMfA9uwWpw6uUepY3sg7lM4fxgEN3PvvUTgiletXUqmjoD0c16XrcoqaSNMvgWCW8KQL0teytAeG1JSUmp5S8J0OBySkpJSC9hwutdLNMHHTrGxsSYuLs7uMJRyjx9Hw7rJcP9qqNWw+PNdIWmTNeGnURe4ebquvywvafvh435gHDBinlv/vl0xwSc+Pj7Uz8/vY6AN3lHAxgFsyM/PH9GpU6dT1mJquTul7HJoK6yZBF1HlV+iBKtCzBUvw4z7rC7g3o+U3729VU46TBxiTeK67efy/fsuJWfCuNLuODyFN3xbUMozLRwHftWgx0Plf+/zb4Z2N1iTTHYuLf/7e5OCPJg8HJI3wZAvILyd3RGpUtBkqZQdDqyFjdPhgnugpg3Lo0SsQt11z7PGLzNSyj8Gb2AMzHoIts+3doNp1s/uiFQpabJUyg4LnoeqteGCe+2LoUpNa/1l9jGrfqzjtJMAVVksfQ1WfQk9/w86Dbc7GlUGmiyVKm+7l8PWX6HHv6FabXtjCWsD/V+CHQth2Wv2xlLZrJsMC56DtkPcU2xClStNlkqVJ2Ng/rNQsz50GWl3NJaOw6HN9bDwBdj1m93RVA47l1ql7KJ6wlXvevJaSlVCmiyVKk/b58Oe36HXGGsbLU8gAoPehDpNrHJ4mV5XDtS1kjfDd8OgblO44Svwq2J3RMoFNFkqVV4KW5W1I63WnCepEmjN1Mw6AtNG6vhlaaUnWdtt+VaxttuqVsfuiJSLaLJUqrwkzLBmwfZ53DMrt4S1hf4vWq3f396wO5qKJycDJg2GrEMwbDLUaWx3RMqFNFkqVR4cBdYM2OCW0G6I3dGcWafbIOZaWDDOmoikSqYgH76/HQ6uh+s/g4jz7Y5IuZgmS6XKw7rvrA1++z7p2eXlRGDQW1ar6PvbIfOw3RF5PmPg50dg6xy44hVoeXmZLnc0M5fPf9vJf2ZsdFGAyhW03J1S7pafAwv/B+EdoPUgu6MpXtUga/3lx/1g+l1w02Tw0e/VZ/T72xD3CXR/ADqPKNUlChyGpVtTmBKfyNyNSeQWOGjfqDa5+Q4C/PS/vSfQZKmUu636ElL3WDNOK8oSgvD2cPn/YNbDVjLo8aDdEXmmDVNh7tNW1/XF/znnt+86lMn38YlMXZXIgdRs6lT351/dGjM4tiGtw4NcH68qNU2WSrlTbiYsfhka94Dz+todzbmJvcNaLzj/WYjsZv2ov+1eDtNHQeQFcPX4Ere+s3Lzmb3+IJPj9rJy5xF8BHq3COHpgdFc3Lq+tiQ9lCZLpdxp5QTITLbW21WUVmUhEbjybTiwxhq/HLUMqte1OyrPcGgrfHujtQxo6CTwr3rW040xrNpzlClxify0dj+ZuQU0Ca7BI5e35NrzGxJW6+zvV/bTZKmUuxw/BsvehOaXVdxWWdVa1vjlJ5daragbv9Xxy4wU+Po6EF8Y9v1Zv0Akp2UzbfU+JsftZUdKJtUDfBnYLpzBsY2IbVwHqWhfoLyYJkul3GX5u1aR8opeFzTifLh0HPw8xvpM3e+3OyL75GbBNzdARjLcOhPqNjnllLwCBws2JzMlbi8L/0qhwGHoHFWHUb3PY0DbcGpU0V+7FZH+rSnlDhkpsPx9a+JHZdi/sMudsGspzPuP1Upu1MXuiMqfo8DazmzfKhg6ERrG/uPlLUnpTP5zL9NX7+NwZi6hgVW4q1dTru/UkKYhNW0KWrmKJkul3GHZ65CfDRc9YXckriFiFQQ/sBam3Aajlnrf+OWcx+GvWXD5S9BqAABp2Xn8tHY/k+MSWbv3GP6+Qr/W9RkS24iezYPx8/XyLutKRJOlUq52bC/8+TF0uAmCm9kdjesUHb/84R648ZuKN2mptJa/Dys+gG6jcXS5iz+2HWJy3F5+3nCQnHwHrcICeWpgNFd3iKBeTS2cXhkVmyxF5FNgIJBsjGnjPPYf4E6gcHv1x40xs52vjQXuAAqA+40xc5zHLwfeAnyBj40xL7r2oyjlIZa8bP3Z+1F743CHBh3h0ufhl0dh+XtwoY2bV5eXTT/CnMfJOu8KPvIdzpRXFpJ49DhBVf0YEtuIIbGNaNMgSCfrVHIlaVl+DrwLfHnS8TeMMa8WPSAi0cBQIAaIAOaJSAvny+8BlwCJwJ8iMsMYs6kMsSvleQ5tg9UTrb0qazeyOxr36HqXc/zyGWv88qSxu8okZ+dy/L6/kx0BrRi0aQg5m7bRo1kwYy5ryWUxYVT19+DShcqlik2WxpglIhJVwutdBXxrjMkBdorINqBwJsA2Y8wOABH51nmuJktVuSx6AfyqQs+H7I7EfUTgqvfgw57O8csllWorKmMMG/alMe+35QxPGEGaozb/DniUuy9uw3WdGtCwjofsQ6rKVVnGLO8VkVuAOOBhY8xRoAHwR5FzEp3HAPaedLzrmS4sIiOBkQCRkZFlCFGpcnRwvVX+rOf/Qc1Qu6Nxr2q14frP4dPL4IfR1uzQCt4NeTgjhx/W7GdK3F6SDu5jepX/EODnw5ErJzKjQyw+PhX786myKe1UrfHAeUAH4ADwmvP46f5vMmc5flrGmAnGmFhjTGxISEgpQ1SqnC143poEc+F9dkdSPhp2gkuetWaI/jHe7mhKJb/AwYLNSYz6Kp5u/5vPczM3EeiXz69hH9DY7yg1h0+hY8fOmihV6VqWxpikwsci8hEw0/k0ESg6UNMQ2O98fKbjSlV8e1bAll/g4mesVpe36HY37FpmFRNv1NVKoBXAjpQMpsQnMjU+keT0HOrVCODWC6MY3KkBLRbfCwlrrZm/kWfsAFNeplTJUkTCjTEHnE+vATY4H88AJonI61gTfJoDK7Fals1FpAmwD2sS0E1lCVwpj2GMVWy8Rqg1+cWbFK6//LA3fH8r3LXUY78sZOTkM3vdAabE7+XPXUfx9REuahnC4NhG9G0Vir+vD8x5AhJmWDN+Y662O2TlQUqydOQboA8QLCKJwDNAHxHpgNWVugu4C8AYs1FEJmNN3MkHRhtjCpzXuReYg7V05FNjjO5sqiqHHQth9zLo/woE1LA7mvJXvS4M/swav/xxNNzwtceMXxpjiNt9lMl/7mXW+gNk5RZwXkgNxvZvxTUdGxAaWKSA+YoJVjm/LiPhAi9YEqPOiRhzxqFDjxAbG2vi4uLsDkOp0zMGProIMg/DfXHg58UL0n9/F359wqpw022UraEcTM1m6qpEvo9PZOehTGoE+DKofQSDYxvRMbL2qWsiN8+G74ZBi8utZO9TsZeEiEi8MabyrumxgVbwUaosNs+E/avhqve9O1ECXDDaGr/89UmrdmyDjuV6+9x8B/MTkpgct5fFW1JwGOjapC73XtSM/m3DqB5whl93++KtLcjC28N1H1f4RKncQ1uWSpWWowDGXwjGAXcvB1/97knWEfiwF4gP3LWkXMYvEw6kMSUukR/W7ONIZi5hQVW5vlNDru/UkKjgYrrFj+6Cj/uBfzUYMb/SLPnRlqXr6b9upUpr/RRI2QyDv9BEWah6Xbj+U/isP8y4D4Z86Zbxy9SsPGas3cfkuETW70slwNeHS2KsAuY9mgXjW5KlHllH4OvroSAPbp1daRKlcg/9F65UaeTnwsIXrK671lfaHY1nadTFWkIz9ymroHyXO11yWYfD8Nv2Q0yJS+SXjQfJzXcQHR7EfwZFc1WHBtSpEVDyi+XnwHf/gmO74eYfIKRF8e9RXk2TpVKlsfpL6xftgNfBR7dhOsUF91rjl3Meh4adIaJDqS91JDOXz3/fxdT4RPYdO06tav7c1CWS6zs1pE2DWud+QYcDfrgbdv8G130CUd1LHZvyHposlTpXuVmw+BWIvBCaXWx3NJ7Jxweu+QA+6AFTboW7FlvVjc5R/O4jjJ64mqT0bHo1D2HsFa3o17p+2QqYL3jWKkt48TPQ9vrSX0d5FU2WSp2rPz+CjIPW2kIPWU/okarXhes/c45f3m9VxCnhfy9jDJ8s28mLP28monY1frq3R+lakSeL+xSWvQGdboMe/y779ZTX0P4jpc5Fdqr1y7bZJdD4Qruj8XyRXeHip2DTDxD3SYnekpadx91fr+L5WQn0bRXKT/e5KFFu+RVmPQzNL4UrXtUvOuqcaMtSqXOx/D04fhT6Pml3JBXHhQ/Art/gl7HW+GV4+zOeunF/KqMnrmLv0eM8cUVrRvRs4ppNlfevsbqD67exWrs6e1mdI21ZKlVSmYesZBl9dZkmrHgdHx+45kOoHmwlrOy00542+c+9XPv+7xzPK+Dbkd24s1dT1yTKY3tg0hCrW/imyVClZtmvqbyOJkulSmrZG5CXBRc9YXckFU+Netb6y6O74acHrDKBTsdzC/i/KWt5ZOo6YqPqMOv+nnSOquua+x4/BhMHQ142DJsCQeGuua7yOposlSqJ1H2w8iNof5OuySutxhdA3ydg4zSI/wywtsq65v3fmLoqkfv7NuPL27sSXNNFZQPzc621lIe3ww1fQWhr11xXeSXtuFeqJJa8bJW16/Oo3ZFUbN3/bY1f/vwYS7KacM/8XPx9hc9u7Uyfli6soGOMVUFo11KrC7hpb9ddW3klbVkqVZzD22HVVxB7O9SOtDuais3Hh9wrPyDNJ5CG80bRNsSHWff3dG2iBKu60rpvrS7z9kNde23llTRZKlWchS9YO4r0fNjuSCq8fceOc8PErYzIuJson2S+rv8NEbWqFv/Gc7HqK6sn4Px/Qa8xrr228lraDavU2RxcDxu+hx4PQWB9u6Op0Bb9lcy/v1tDXoHhpRuH4XPMwILnoWkv6HSra26ybb41gei8vjDwTV1LqVxGk6VSZ7NgHFSpBd3vtzuSCqvAYXhr3hbeWbiNlvUDeX9YR5qG1ATHw87xy0ehQSyEtSnbjQ6uh8nDrYk8g78AX3/XfACl0G5Ypc5s70rY8rOVKKvVsTuaCulQRg63fLqCtxds4/qODZl+T3crUYK1/vLaj6BqbWv9ZU5G6W+Uug8mDoEqgdZayqpBLolfqUKaLJU6HWNg/rNQIwS6jrI7mgrpz11HGPD2UuJ2HeXl69rxyuD2VAs4qQB6zRC47mM4sh1mPfSP9Zcllp1mFR3ISbfWUtZq4JoPoFQRmiyVOp0di6xlBz3/Tyu+nCNjDB8t2cHQCX9Qzd+X6fd0Z0jnRmd+Q5Oe0GcsrPsOVn91bjcryIPJt1ibcA/5ouxduUqdQbHJUkQ+FZFkEdlQ5NgrIrJZRNaJyHQRqe08HiUix0VkjfPngyLv6SQi60Vkm4i8LS6pY6WUGxS2KoMaQuxtdkdToaQez+Our+IZNzuBS6PrM+O+HkRHlKBLtOfD0KQ3zB4DSRtLdjNjYOaDsGMhDHpLt0tTblWSluXnwOUnHZsLtDHGtAO2AGOLvLbdGNPB+VO0/2o8MBJo7vw5+ZpKeYbNs2D/KujzmLVkRJXIhn2pDHpnGQs2J/PUwGjeH9aRoKolnGTj42t1x1atVfLxyyWvwOqvodcj1jIRpdyo2GRpjFkCHDnp2K/GmHzn0z+Ahme7hoiEA0HGmOXGGAN8CVxdupCVciNHgbWcoV4zaH+j3dFUCMYYvlm5h2vH/05egYPv7urGHT1KsVtIzVBrws+hrTD7/85+7ppvYOE4aDcULnq89MErVUKuGLO8Hfi5yPMmIrJaRBaLSE/nsQZAYpFzEp3HTktERopInIjEpaSkuCBEpUpo/feQkmBVftFtnIqVlZvPw1PWMnbaero2qcvM+3rQqXEZiqA37W216Nd+A6snnv6cHYthxr3QpBdc+Y6upVTloky/DUTkCSAfKPy/+gAQaYw5LCKdgB9EJAY43f/NZ5z2ZoyZAEwAiI2NLcX0OKVKIT8XFr0AYW2tbbjUWW1PyeDur+PZmpzBg/2ac1/f5vj6uCBx9RoDu3+zNmpu0PGfBdCTE+C7m6FecxjyFfgFlP1+SpVAqVuWIjIcGAgMc3atYozJMcYcdj6OB7YDLbBakkW7ahsC+0t7b6XcYvVXcHQX9H3aWgOozuintfu58p1lHMrI5cvbu/BgvxauSZRgjV9e+7G1ZnLKrZCbaR1POwBfXw/+1awlItVqu+Z+SpVAqX4jiMjlwKPAlcaYrCLHQ0TE1/m4KdZEnh3GmANAuoh0c86CvQX4sczRK+Uqecdh8cvQqBs0v8TuaDxWTn4Bz/y4gfu+WU2r8CBm3d+Dns1DXH+jwPpw3UeQ8pc1QzYnw1pLefwoDJsMtc+yFEUpNyi2G1ZEvgH6AMEikgg8gzX7tQow1zmI/4dz5msv4FkRyQcKgFHGmMLJQXdjzaythjXGWXScUyl7rfwIMg5aGxTrGNhpJR7NYvSk1azde4wRPZrwaP9W+Pu6sQXetA/0fgQWvwSJf1q7v9z4LYS3d989lToDMaWpmFGOYmNjTVxcnN1hqMosOw3eagcRHeHmaXZH45EWOougFxQYXhncjsvbhJfPjR0F8OVVVoGIgW/qutcSEpF4Y0ys3XFUJjrdT6nl71ndexc/ZXckHqfAYXhj7hbeXbiN1uFBjB/WkajgGuUXgI8vDJ1oFUmP6lF+91XqJJoslXfLPAzL34XWV0LE+XZH41FS0nN44NvV/L79MDfENuK/V8VQ1d+3+De6WtVamiiV7TRZKu+27HXIy7LWVaoTVuw4zH3frCYtO49Xrm/H4FidUKO8myZL5b1S91kTe9oNhdBWdkfjEYwxfLhkB6/M+YvIutX58o4utArT7a6U0mSpvNeSV8A4oM+jdkfiEVKz8nh4ylrmJSQxoG04L17XlsCS1nZVqpLTZKm80+HtVhGCTrdBnSi7o7Hd+sRU7pkUz8HUbJ4ZFM2tF0ade21XpSoxTZbKOy16EXz8oVcxBbsrOWMMk1bu4b8zNhFcM4Dv7rqAjpF17A5LKY+jyVJ5n6SNsH4KdH8AAsPsjsY2Wbn5PDF9A9NX76NXixDevKEDdWtorVWlTkeTpfI+C8ZZdUe7P2B3JLbZlpzO3V+vYltKBg9f0oLRFzXDx1W1XZWqhDRZKu+SGAd/zYKLnoTqZdhKqgL7cc0+xk5bTzV/X766vSs9mgfbHZJSHk+TpfIu85+F6sHQbZTdkZS7nPwCnp+ZwFd/7KZzVB3eubEjYbWq2h2WUhWCJkvlPXYsgp2L4bL/Wd2wXmTvkSxGT1rFusRURvZqypjLWrq3CLpSlYwmS+UdjIH5z0FQA4i93e5oytX8hCQemrwWhzF8eHMnLovx3klNSpWWJkvlHf76GfbFwaC3wd87uh7zCxy8PncL7y/aTkxEEOOHdSKyXnW7w1KqQtJkqSo/hwMWPAd1z4MON9kdTblITs/mvkmrWbHzCDd2ieSZQdH2FEFXqpLQZKkqvw1TIXkTXPcJ+Fb+8m1/OIugZ2Tn8/qQ9lzbsaHdISlV4WmyVJVbQR4sHAf120LMtXZH41YOh+GDJdt5dc5fRAXXYOKIrrSo710TmZRyF02WqnJb/TUc3Qk3TQafyjv781hWLg9PXsv8zckMah/B/65tS80q+s9bKVfRf02q8so7DotfhkZdofmldkfjNusSj3H316tITs/m2atiuLlbYy2CrpSLabJUldefn0D6frjuI6iEycMYw9cr9vDcT5sICazClFEX0qFRbbvDUqpSKlG/lIh8KiLJIrKhyLG6IjJXRLY6/6zjPC4i8raIbBORdSLSsch7hjvP3yoiw13/cZRyyk6Dpa/BeX0hqofd0bhcZk4+D3y7hhP7j7kAABiNSURBVKd+2ED3ZvWYeV8PTZRKuVFJB3E+By4/6dhjwHxjTHNgvvM5QH+gufNnJDAerOQKPAN0BboAzxQmWKVc7o/xcPwI9H3K7khcbmtSOle99xsz1+1nzGUt+WR4Z+robiFKuVWJumGNMUtEJOqkw1cBfZyPvwAWAY86j39pjDHAHyJSW0TCnefONcYcARCRuVgJ+JsyfQKlTpZ1BH5/B1oPggYdiz/fgxljSDx6nI3709i0P5WN+9P4ffthalTx4+sRXbnwPC2CrlR5KMuYZX1jzAEAY8wBEQl1Hm8A7C1yXqLz2JmOn0JERmK1SomMjCxDiMorLXsDcjOsnUUqkPwCB9tTMtm4P5VN+9OsBHkgjdTjeQD4CDQLrcmV7SN4+NIWhAZ5RyUipTyBOyb4nG4mhTnL8VMPGjMBmAAQGxt72nOUOq20A7ByArQfCqGt7I7mjI7nFrD5oJUQC1uNmw+mk5PvAKCKnw+twoMY0C6cmIggYiJq0SosUKvwKGWTsiTLJBEJd7Yqw4Fk5/FEoFGR8xoC+53H+5x0fFEZ7q/UqZa8Ao4C6PNY8eeWk2NZuc6k+HeLcXtKBg7n18Ba1fyJiQjilgsaExNRi+iIIJoG18BPdwVRymOUJVnOAIYDLzr//LHI8XtF5FusyTypzoQ6B3ihyKSeS4GxZbi/Uv90ZCes+gI63Qp1osr99sYYDqRmn0iMVosxjX3Hjp84J7xWVWIigujftrDFGESD2tV0XaRSHq5EyVJEvsFqFQaLSCLWrNYXgckicgewBxjsPH02cAWwDcgCbgMwxhwRkeeAP53nPVs42Ucpl1j0Ivj4Q68xbr9VgcOw81BGkW5UK0EezbLGF0WgaXANOjWuwy0XNCba2ZVaV2etKlUhlXQ27I1neOni05xrgNFnuM6nwKcljk6pkkpOgHXfQff7IdC1+zVm5xWwJSn9Hy3GzQfSOZ5XAECArw8twwK5LCaMmIggoiNq0To8kOoBWvNDqcpC/zWrymHB81AlELo/WKbLpB7PO9FKLBxf3JaSQYFzgDGwqh/R4UHc2CXS2VoMolloTfx1fFGpSk2Tpar49sXD5plw0RNQvW6J3mKMISkth00HUtm4zzkr9UAqe4/8Pb4YGliFmIggLomuf2JGaqO6Or6olDfSZKkqvvnPQfV60O3u077scBh2Hc48Mb5Y2Go8nJl74pwmwTVo17A2QztHnkiMIYFVyusTKKU8nCZLVbHtXAI7FsJlL0CVQHLyC9ialHGiK3Xj/jQSDqSRmWuNL/r7Cs1DA+nbKtRKig1q0To8SLezUkqdlf6GUBVW+vFcmP0MPlXq89yezqxduZRtyenkFVjjizUCfImOCGJwbCOiw4OIjgiiRf1AAvx0fFEpdW40WaoKITk9+8QSjU3708jZu5oRWR/RzSeBx/JGMG9rKtERtejTMuREN2rjutXx8dHxRaVU2WmyVB7FGMOeI1n/WKaxcX8aKek5AASTyjM1pjGgYB45AbXY3OG//LvnXfwvqKpOvFFKuY0mS2WbvAIHW5MyrAk3B6ykmLA/jfScfAB8fYTmoTXp2TyYtmHV6HtsGpEb3kXys+GC0VTrNYZW1XQPR6WU+2myVOUiMyf/78Lh+6xlGlsOZpBbYBUOr+bvS+vwQK46P4KYiFrEOMcXq/r5wOZZ8OuTcHQntOgPlz4Pwc1s/kRKKW+iyVK53OGMnBPbSxV2p+48lIlxFg6vU92fmIha3NY96kQZuCbBNfA9eXzx4AaYM9aa8RrSGv41DZqdUjRKKaXcTpOlKrXTbUy8cX8aB9OyT5zToHY1oiOCuLL93y3G8FrFjC9mHrIq8qz6AqrWgitehU63ga/+76qUsof+9lElUrgxcdGKNydvTHxeSE26Na17IilGRwRRu/o5FA7Pz4WVH8LilyEvC7rcBb0fKXFVHqWUchdNluoUJdqYOCyQK4psM9UqLIhqAaXcmNgY2PILzHkCjmyH5pfCpeMgpIULP5VSSpWeJksvdywr90TB8MKlGkU3Jg6q6kdMRC1u7taYmAbW+KJLNyZO2gRzHreq8AS3gGFToXk/11xbKaVcRJOllzinjYnbhBHt7EptWMdNhcMzD8OiFyDuU6gSBJe/BJ3vAF9/199LKaXKSJNlJVSSjYmbBNegY+M63HxBY2t8MTyIejXLoXB4QR6s/AgWvwg5GdB5BPQZq+OSSimPpsmykkhKy+ajJTuI33P0jBsTRxcZX6xhR+HwLb9aXa6Ht8J5fa3i56Gtyz8OpZQ6R5osK7jsvAI+WbaT9xZuI6/AwfmRdRjapdGJGakesTFx8mb49QnYNg/qNYObJluTeLQ8nVKqgtBkWUEZY5i9/iAvzE5g37HjXBZTn8evaE3jejXsDu1vWUdg0Yvw58cQUNNqSXa+E/zOYTmJUkp5AE2WFdCGfak8O3MTK3ceoVVYIJNGdOXCZsF2h/W3gjxr4s7CFyAnzSoocNETUKOe3ZEppVSplDpZikhL4Lsih5oCTwO1gTuBFOfxx40xs53vGQvcARQA9xtj5pT2/t4oOT2bV+f8xZT4ROpWD+CFa9pyQ+dGp5aJs9O2efDL43DoL2jSGy7/H9SPsTsqpZQqk1InS2PMX0AHABHxBfYB04HbgDeMMa8WPV9EooGhQAwQAcwTkRbGmILSxuAtsvMK+Oy3Xby3cBs5+QWM6NGE+y5uTlBVD1pmcWirNXln669QtykM/QZa9tdxSaVUpeCqbtiLge3GmN1nWZN3FfCtMSYH2Cki24AuwHIXxVDpGGOYs/Eg42YnsPfIcfq1rs8TA1rTJNiDxiWPH7XK062cAP7VrR1BuowEv3JYhqKUUuXEVclyKPBNkef3isgtQBzwsDHmKNAA+KPIOYnOY6cQkZHASIDIyEgXhVixbNqfxrMzN/LHjiO0qF+Tr+7oQs/mIXaH9beCfIj/zBqXPH4UOg2Hi56Emh4Uo1JKuUiZk6WIBABXAmOdh8YDzwHG+edrwO3A6Zqc5nTXNMZMACYAxMbGnvacyupQRg6v/foX3/65l9rV/Hnu6jbc2LmR68rLucL2hVaXa/ImiOppjUuGtbU7KqWUchtXtCz7A6uMMUkAhX8CiMhHwEzn00SgUZH3NQT2u+D+lUJOfgFf/L6Ld+Zv43heAbd3b8L9fZtTq7oHjUse3m4VO9/yM9SJghu+hlYDdVxSKVXpuSJZ3kiRLlgRCTfGHHA+vQbY4Hw8A5gkIq9jTfBpDqx0wf0rNGMMczclMW52ArsPZ9G3VShPDGjNeSE17Q7tb8ePwZJXYMWH4FcV+v0Xut2t45JKKa9RpmQpItWBS4C7ihx+WUQ6YHWx7ip8zRizUUQmA5uAfGC0t8+E3XwwjedmbuK3bYdpFlqTL27vQu8WHjTm5yiwNmBe8LxVYOD8f0HfpyCwvt2RKaVUuSpTsjTGZAH1Tjp281nOHweMK8s9K4PDGTm8PncL36zcQ1A1f/57ZQw3dY20vyxdUTsWW+OSSRsg8kJrXDKig91RKaWULbSCTznKzXfw5fJdvDV/K1m5BdxyQRQP9mtO7eoeVP7tyA749SnYPBNqR8LgLyD6Kh2XVEp5NU2W5cAYw4LNyYyblcCOQ5n0bhHCUwNb0yw00O7Q/pad5hyX/AB8/K3u1gvuBf+qdkemlFK202TpZluS0nlu5iaWbj1E05AafHZrZy5qFWp3WH9zFMDqr2HBc5CZAh2GwcVPQ2CY3ZEppZTH0GTpJkczc3lj3hYmrthDjQBfnh4Yzc0XNPasccldy+CXx+DgemjUzdo6q0FHu6NSSimPo8nSxfIKHHy1fDdvzttCZm4Bw7pG8mC/FtSt4UHjkkd3WeOSCTOgViO4/lOIuVbHJZVS6gw0WbrQws3JPDdrEztSMunZPJinBkbTor4HjUvmpMPS12D5e+DjZ22bdeF94F/N7siUUsqjabJ0gW3J6Tw3M4HFW1JoElyDj2+J5eLWoZylqHz5cjhg7SSY/yxkJEG7odDvGQiKsDsypZSqEDRZlsGxrFzenLeVr/7YTfUAX54c0JpbLogiwM+DxiV3/26NSx5YCw27WFtnNexkd1RKKVWhaLIshfwCBxNX7OGNeVtIO57HjV0ieeiSFtSr6UHl347uhnnPwMbpENQArv0Y2l6v45JKKVUKmizP0eItKTw/cxNbkzO48Lx6PDUwmtbhQXaH9becDFj2Bvz+DogP9H4Mut8PAR60B6ZSSlUwmixLaHtKBuNmJbBgczKN61Vnws2duCS6vueMSxoD676Duc9AxkFoOxj6/QdqNbQ7MqWUqvA0WRYjNSuPtxds5Yvfd1HV35ex/Vtxa/coqvj52h3a33LS4acHYMNUaNAJbvgKGnWxOyqllKo0NFmeQX6Bg2/+3Mvrv/7FseN5DO3ciIcuaUlIoAeNSwIkJ8B3N8OR7VaJuh4PgY8HTTBSSqlKQJPlaSzbeojnZm7ir6R0ujapy9ODoomJqGV3WKda+y3M/DcE1IRbfoQmveyOSCmlKiVNlkXsPJTJuFkJzEtIolHdanzwr45cFhPmOeOShfKy4ZdHIf5zaNzdqsCjtVyVUsptNFkCadl5vLtgG5/9tpMAXx8eubwlt3dvQlV/DxqXLHRkJ0y+BQ6ug+4PWl2vvvrXqJRS7uTVv2ULHIbv/tzLa7/+xZGsXAZ3asj/XdaS0EAP3ZZq8yyYfjcIcOO30LK/3REppZRX8Npk+fv2Qzz70yY2H0ynS1RdvhgUTZsGHjguCVCQZ5Wq+/1tCO8AQ76AOlF2R6WUUl7D65LlnsNZjJu9iTkbk2hQuxrv3dSRK9p64LhkobQD8P1tsGc5xN4Bl72gGzIrpVQ585pkmZ6dx7sLt/HZsl34+QpjLmvJHT08dFyy0I5FMHUE5GZa5eraDbY7IqWU8kplTpYisgtIBwqAfGNMrIjUBb4DooBdwBBjzFGxmm9vAVcAWcCtxphVZY3hbAochu/j9/LKnC0cysjhuo4NeeTyltQP8uDWmcNhbaW16AWo1xyGz4TQVnZHpZRSXstVLcuLjDGHijx/DJhvjHlRRB5zPn8U6A80d/50BcY7/3SLFTsO8+zMTWzcn0Zs4zp8emss7RrWdtftXCPrCEwbCdvmWiXrBr4JVWraHZVSSnk1d3XDXgX0cT7+AliElSyvAr40xhjgDxGpLSLhxpgDrrx5WnYej01dx+z1B4moVZW3bzyfQe3CPXdcslBiHEweDpnJMOB1iL1ddwlRSikP4IpkaYBfRcQAHxpjJgD1CxOgMeaAiIQ6z20A7C3y3kTnsX8kSxEZCYwEiIyMPOeAagb4cSgjl4cuacGdPZtSLcCDxyXBKoK+cgLMeQKCwuH2OdCgo91RKaWUcnJFsuxujNnvTIhzRWTzWc49XTPJnHLASrgTAGJjY095vTg+PsJ3I7t5fksSIDsNZtwHm36AFv3hmvFQrY7dUSmllCqizMnSGLPf+WeyiEwHugBJhd2rIhIOJDtPTwQaFXl7Q2B/WWM4nQqRKJM2WtV4juyEfv+FC+/XIuhKKeWByvSbWURqiEhg4WPgUmADMAMY7jxtOPCj8/EM4BaxdANSXT1eWWGsmQQfXWxtrzX8J+jxoCZKpZTyUGVtWdYHpjtbcX7AJGPMLyLyJzBZRO4A9gCFCwRnYy0b2Ya1dOS2Mt6/4sk7Dj8/Aqu+hKiecN0nEFjf7qiUUkqdRZmSpTFmB9D+NMcPAxef5rgBRpflnhXakR3OIujroefD0OdxLYKulFIVgP6mLi8JP8EP94D4wE2TocVldkeklFKqhDRZultBHsz7Dyx/FyI6WkXQa5/7chillFL20WTpTmn7YcptsPcP6DISLn0e/KrYHZVSSqlzpMnSXbYvtIqg52fD9Z9Cm+vsjkgppVQpabJ0NYcDlrwCi/4HIa1gyJcQ0sLuqJRSSpWBJktXyjwM0+6E7fOh3VAY+DoE1LA7KqWUUmWkydJV9q6EKbdC5iEY9BZ0HK5F0JVSqpLQZFlWxsCKD+DXJyGoAdzxK0R0sDsqpZRSLqTJsiyy0+DH0ZAwA1oOgKvfh2oevl+mUkqpc6bJsrQOrreq8RzdDZc8Bxfep92uSilVSWmyLI1VX8Hs/4OqteHWmdD4QrsjUkop5UaaLM9FbhbMHgNrvoYmvawi6DVDi3+fUkqpCk2TZUkd3m51uyZtgF6PQJ/HwMfX7qiUUkqVA02WJbHxB/jxXmuHkGHfQ/NL7I5IKaVUOdJkeTb5uTD3aVgxHhrEwuDPoXYju6NSSilVzjRZnklqolVkIPFP6DrKmvHqF2B3VEoppWygyfJ0ts2DqXdCQa7Vmoy5xu6IlFJK2UiTZVGOAlj8Eix+GUJbW0XQg5vbHZVSSimbabIslJEC00bAjkXQYRhc8SoEVLc7KqWUUh5AkyXAnj+s8cnjR+HKd6HjzXZHpJRSyoP4lPaNItJIRBaKSIKIbBSRB5zH/yMi+0RkjfPniiLvGSsi20TkLxG5zBUfoEyMgd/fgc+uAL+qcMdcTZRKKaVOUZaWZT7wsDFmlYgEAvEiMtf52hvGmFeLniwi0cBQIAaIAOaJSAtjTEEZYii948esIuibZ0LrQXDVe1C1li2hKKWU8mylTpbGmAPAAefjdBFJABqc5S1XAd8aY3KAnSKyDegCLC9tDKV2YJ1VjSd1L1z2AnS7R4ugK6WUOqNSd8MWJSJRwPnACuehe0VknYh8KiJ1nMcaAHuLvC2RMyRXERkpInEiEpeSkuKKEC3GQPwX8HE/yM+BW2fDBaM1USqllDqrMidLEakJTAUeNMakAeOB84AOWC3P1wpPPc3bzemuaYyZYIyJNcbEhoSElDVES24W/HAP/HS/tUvIqKUQ2dU111ZKKVWplWk2rIj4YyXKicaYaQDGmKQir38EzHQ+TQSK1oprCOwvy/1L7NBWq9s1OQH6jIVeY7QIulJKqRIry2xYAT4BEowxrxc5Hl7ktGuADc7HM4ChIlJFRJoAzYGVpb1/iW2YBhP6QEYS/Guq7hailFLqnJWlZdkduBlYLyJrnMceB24UkQ5YXay7gLsAjDEbRWQysAlrJu1ot86Ezc+FX5+ElR9Cwy5W2bpaZ5t/pJRSSp1eWWbDLuP045Czz/KeccC40t6zxI4fha+vh31x0G00XPJf8PV3+22VUkpVTpWzgk+VWlC3CXS/H6KvsjsapZRSFVzlTJY+PnDdx3ZHoZRSqpJwyTpLpZRSqjLTZKmUUkoVQ5OlUkopVQxNlkoppVQxNFkqpZRSxdBkqZRSShVDk6VSSilVDE2WSimlVDHEmNPukuUxRCQF2F3KtwcDh1wYTkWgn7ny87bPC/qZz1VjY4yL9jdUUAGSZVmISJwxJtbuOMqTfubKz9s+L+hnVvbTblillFKqGJoslVJKqWJU9mQ5we4AbKCfufLzts8L+pmVzSr1mKVSSinlCpW9ZamUUkqVmSZLpZRSqhiVMlmKyOUi8peIbBORx+yOpzyIyKcikiwiG+yOpTyISCMRWSgiCSKyUUQesDsmdxORqiKyUkTWOj/zf+2OqbyIiK+IrBaRmXbHUh5EZJeIrBeRNSISZ3c8qhKOWYqIL7AFuARIBP4EbjTGbLI1MDcTkV5ABvClMaaN3fG4m4iEA+HGmFUiEgjEA1dX5r9nERGghjEmQ0T8gWXAA8aYP2wOze1E5CEgFggyxgy0Ox53E5FdQKwxxtsKMXisytiy7AJsM8bsMMbkAt8CV9kck9sZY5YAR+yOo7wYYw4YY1Y5H6cDCUADe6NyL2PJcD71d/5Urm+7pyEiDYEBwMd2x6K8V2VMlg2AvUWeJ1LJf4l6OxGJAs4HVtgbifs5uyPXAMnAXGNMpf/MwJvAI4DD7kDKkQF+FZF4ERlpdzCqciZLOc2xSv/t21uJSE1gKvCgMSbN7njczRhTYIzpADQEuohIpe5yF5GBQLIxJt7uWMpZd2NMR6A/MNo5zKJsVBmTZSLQqMjzhsB+m2JRbuQct5sKTDTGTLM7nvJkjDkGLAIutzkUd+sOXOkcw/sW6CsiX9sbkvsZY/Y7/0wGpmMNLykbVcZk+SfQXESaiEgAMBSYYXNMysWck10+ARKMMa/bHU95EJEQEantfFwN6Adstjcq9zLGjDXGNDTGRGH9W15gjPmXzWG5lYjUcE5aQ0RqAJcCXjHL3ZNVumRpjMkH7gXmYE36mGyM2WhvVO4nIt8Ay4GWIpIoInfYHZObdQduxmpprHH+XGF3UG4WDiwUkXVYXwrnGmO8YimFl6kPLBORtcBKYJYx5hebY/J6lW7piFJKKeVqla5lqZRSSrmaJkullFKqGJoslVJKqWJoslRKKaWKoclSKaWUKoYmS6WUUqoYmiyVUkqpYvw/V306rtkmMkUAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Scatter-Plots"><u>Scatter Plots</u><a class="anchor-link" href="#Scatter-Plots">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Usage: When analyzing indivudual points, looking for outliers, fluctuations, general overview of variables</p>
<p>Do not use: when looking for precision, one dimensional data, non numerica/categorical data</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[42]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># creating arrays</span>
<span class="c1"># rand generates from distribution [0, 1)</span>
<span class="n">x1</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">40</span><span class="p">)</span>
<span class="n">x2</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">40</span><span class="p">)</span> <span class="o">+</span> <span class="mi">25</span>
<span class="n">x3</span> <span class="o">=</span> <span class="mi">25</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">20</span><span class="p">)</span>

<span class="c1"># combining all these arrays and creating a list</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">x1</span><span class="p">,</span> <span class="n">x2</span><span class="p">,</span> <span class="n">x3</span><span class="p">))</span>

<span class="n">y1</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">40</span><span class="p">)</span>
<span class="n">y2</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">40</span><span class="p">)</span> <span class="o">+</span> <span class="mi">25</span>
<span class="n">y3</span> <span class="o">=</span> <span class="mi">25</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">20</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">y1</span><span class="p">,</span> <span class="n">y2</span><span class="p">,</span> <span class="n">y3</span><span class="p">))</span>

<span class="c1"># s is the size of each data point</span>
<span class="c1"># marker is the shape of each data point</span>
<span class="c1"># c is the color</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">s</span><span class="o">=</span><span class="p">[</span><span class="mi">100</span><span class="p">],</span> <span class="n">marker</span><span class="o">=</span><span class="s1">&#39;^&#39;</span><span class="p">,</span> <span class="n">c</span><span class="o">=</span><span class="s1">&#39;r&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Scatterplots are especially important for data science because they can show data patterns that are not obvious when viewed in other ways. You can see data groupings with relative ease and help the viewer understand when data belongs to a particular group.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[43]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="n">x1</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span>
<span class="n">x2</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span> <span class="o">+</span> <span class="mi">25</span>
<span class="n">x3</span> <span class="o">=</span> <span class="mi">30</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">25</span><span class="p">)</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">x1</span><span class="p">,</span> <span class="n">x2</span><span class="p">,</span> <span class="n">x3</span><span class="p">))</span>

<span class="n">y1</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span>
<span class="n">y2</span> <span class="o">=</span> <span class="mi">5</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span> <span class="o">+</span> <span class="mi">25</span>
<span class="n">y3</span> <span class="o">=</span> <span class="mi">30</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">25</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">y1</span><span class="p">,</span> <span class="n">y2</span><span class="p">,</span> <span class="n">y3</span><span class="p">))</span>

<span class="c1"># using different colors for the data</span>
<span class="n">color_array</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;b&#39;</span><span class="p">]</span> <span class="o">*</span> <span class="mi">50</span> <span class="o">+</span> <span class="p">[</span><span class="s1">&#39;g&#39;</span><span class="p">]</span> <span class="o">*</span> <span class="mi">50</span> <span class="o">+</span> <span class="p">[</span><span class="s1">&#39;r&#39;</span><span class="p">]</span> <span class="o">*</span> <span class="mi">25</span>

<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">s</span><span class="o">=</span><span class="p">[</span><span class="mi">50</span><span class="p">],</span> <span class="n">marker</span><span class="o">=</span><span class="s1">&#39;D&#39;</span><span class="p">,</span> <span class="n">c</span><span class="o">=</span><span class="n">color_array</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Showing-correlations">Showing correlations<a class="anchor-link" href="#Showing-correlations">&#182;</a></h2><p>In some cases, you need to know the general direction that your data is taking when looking at a scatterplot. In this case, you add a trendline to the output.<br />
Least square regression is being used.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[44]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">matplotlib.pylab</span> <span class="k">as</span> <span class="nn">plb</span>

<span class="n">x1</span> <span class="o">=</span> <span class="mi">15</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span>
<span class="n">x2</span> <span class="o">=</span> <span class="mi">15</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span> <span class="o">+</span> <span class="mi">15</span>
<span class="n">x3</span> <span class="o">=</span> <span class="mi">30</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">30</span><span class="p">)</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">x1</span><span class="p">,</span> <span class="n">x2</span><span class="p">,</span> <span class="n">x3</span><span class="p">))</span>

<span class="n">y1</span> <span class="o">=</span> <span class="mi">15</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span>
<span class="n">y2</span> <span class="o">=</span> <span class="mi">15</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">50</span><span class="p">)</span> <span class="o">+</span> <span class="mi">15</span>
<span class="n">y3</span> <span class="o">=</span> <span class="mi">30</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">30</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">y1</span><span class="p">,</span> <span class="n">y2</span><span class="p">,</span> <span class="n">y3</span><span class="p">))</span>

<span class="n">color_array</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;b&#39;</span><span class="p">]</span> <span class="o">*</span> <span class="mi">50</span> <span class="o">+</span> <span class="p">[</span><span class="s1">&#39;g&#39;</span><span class="p">]</span> <span class="o">*</span> <span class="mi">50</span> <span class="o">+</span> <span class="p">[</span><span class="s1">&#39;r&#39;</span><span class="p">]</span> <span class="o">*</span> <span class="mi">30</span>

<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">s</span><span class="o">=</span><span class="p">[</span><span class="mi">90</span><span class="p">],</span> <span class="n">marker</span><span class="o">=</span><span class="s1">&#39;*&#39;</span><span class="p">,</span> <span class="n">c</span><span class="o">=</span><span class="n">color_array</span><span class="p">)</span>

<span class="c1"># The vector output of polyfit() is used as input to poly1d(), which calculates the actual y-axis data points.</span>
<span class="c1"># The third argument (1) is the degree of polinominal fit. Which is a line when it is 1.</span>
<span class="n">z</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">polyfit</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span>
<span class="n">p</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">poly1d</span><span class="p">(</span><span class="n">z</span><span class="p">)</span>
<span class="c1"># plot with red color and solid line</span>
<span class="n">plb</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">p</span><span class="p">(</span><span class="n">x</span><span class="p">),</span> <span class="s1">&#39;r-&#39;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
