---
layout: post
title: Cool Data Visualizations in Python (code Included)
date: 2019-07-03 12:11 -0400
tags: python
image: /assets/img/coolv.png
optimized_image: /assets/img/coolv.png
---
<html>
<head><meta charset="utf-8" />

<title>Cool Data Visualizations in Python (code included).</title>

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

/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

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
# <link rel="stylesheet" href="custom.css">

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
<h3 id="Support-my-efforts-and-see-my-story-at-the-bottom-of-the-page.">Support my efforts and see my story at the bottom of the page.<a class="anchor-link" href="#Support-my-efforts-and-see-my-story-at-the-bottom-of-the-page.">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Importing libs</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">scipy.stats</span> <span class="k">import</span> <span class="n">skewnorm</span>

<span class="c1"># Create the data</span>
<span class="n">speed</span> <span class="o">=</span> <span class="n">skewnorm</span><span class="o">.</span><span class="n">rvs</span><span class="p">(</span><span class="mi">4</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="mi">50</span><span class="p">)</span>
<span class="n">size</span> <span class="o">=</span> <span class="n">skewnorm</span><span class="o">.</span><span class="n">rvs</span><span class="p">(</span><span class="mi">4</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="mi">50</span><span class="p">)</span>

<span class="c1"># Create and show the 2D Density plot</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">kdeplot</span><span class="p">(</span><span class="n">speed</span><span class="p">,</span> <span class="n">size</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s2">&quot;Reds&quot;</span><span class="p">,</span> <span class="n">shade</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">bw</span><span class="o">=.</span><span class="mi">15</span><span class="p">,</span> <span class="n">cbar</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlabel</span><span class="o">=</span><span class="s1">&#39;Speed&#39;</span><span class="p">,</span> <span class="n">ylabel</span><span class="o">=</span><span class="s1">&#39;Size&#39;</span><span class="p">)</span>
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
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXkAAAEKCAYAAAD3tSVSAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4zLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvnQurowAAIABJREFUeJzsvXd8pHd17/8+UzWj3qXVrlZbXdeNxQWHYhwSGwimJAHyuyEQbigJCTeE5JeEX4Af+YW0X0IgtPgSLjjh0gIhhphOCCXYeG2vu73evlpp1aXRzEjTnnP/OI/KalVG0ozaft+vl1YrzTPP8x1Jc77nOeVzRFVxOBwOx9YksN4LcDgcDkf5cEbe4XA4tjDOyDscDscWxhl5h8Ph2MI4I+9wOBxbGGfkHQ6HYwvjjLzD4XBsYZyRdzgcji2MM/IOh8OxhQmt9wJKTVNTk3Z1da33MhwOxybggQceGFTV5tWc49KGZk3lskUd251MfFNVb1vN9ZbLljPyXV1dHDp0aL2X4XA4NgEicmq156javZOnirQ5ItK02ustFxeucTgcji2MM/IOh8OxhXFG3uFwOLYwzsg7HA7HFsYZeYfD4djCOCPvcDgcWxhn5B0Oh2ML44y8w+FwbGGckXc4HI4tjDPyDofDsYVxRt7hcDi2MM7IOxwOxxbGGXmHw+HYwjgj73A4HFsYZ+QdDodjgyAinxSRfhF5bIHHRUQ+JCJHReQREbluqXM6I+9wOBwbh08Biw0VuR3Y53+8CfjYUidcNyMvIjtE5D9E5EkReVxE3j7PMS8QkTEROex/vHs91upwrBRVRb0CqrreS3FsAlT1B8DwIofcAdylxr1AnYi0L3bO9ZwMlQd+T1UfFJFq4AER+baqPjHnuB+q6kvXYX0Ox7LRfBYmk5BJQz4HXn7mMQlAMASRGFRUQiSOiKzjah2lYPSZo/zrbS9bq8t1AGdmfd3tf693oSesm5FX1V78hanquIg8iS12rpF3ODY8mstAYgCyE/aNcBSicQgGQYKgHngeFLKQTkB6DIIhtLoJKqqcsb94aBKR2bMC71TVO5fx/Pn+UBa9TdwQM15FpAu4FrhvnodvEpGHgR7gnar6+DzPfxMWn6Kzs7N8C3U45qBeARKDMJEACUB1I8SqkWB44eeoZ57++BCMnoNwFK1tRcLRNVy5o1TU7dvLK75xd3EHiwyq6sFVXK4b2DHr6+2YbVyQdTfyIlIFfAn4H6qamPPwg8BOVU2KyIuBr2AJh/Pwd8I7AQ4ePOiCn5sYLeTNG85nzfPVAiAQCFqoI1wB4eiG8HxVPRjugdwkVNZBVQMSCC75PJEAVFSh0UqYGIfxQRjuQZt2IMF1f0s6NjZ3A28Tkc8BNwBjflRkQdb1L0pEwpiB/4yqfnnu47ONvqreIyIfFZEmVR1cy3U6yovm/RDGZBIKuZkHJACBAKiCV5j1fUEjcYjXQnR94tqqCiPnzMDXtSGx6mWfQ0QgXoOGozB0BkZ60cYO2wQcFyUi8lngBVhYpxt4DxAGUNWPA/cALwaOAmngDUudc92MvNg78x+BJ1X1bxc4pg3oU1UVkeuxaqChNVymo4xoPmde7GTSvhGNQ2UthGMQjpxn7HTK0Gcn7GMyCSMpCEXQmiYkWrm2i08nIJOCmqYVGfjZiB+uYfScxeor60u0SMdmQ1Vfu8TjCvzWcs65np78zcCvAo+KyGH/e38MdML0rvWLwFtFJA9MAK9RV4u26VFVSI1A0q8Uq6yHyrpFQxUiYuGaWDXEqtGaZgt1JIct1BGrgZpmJFB+L1hVIT1qydV4XUnOKbFqNDkMkyln5B0lZT2ra37E/Jni2cd8GPjw2qzIsRZoIQ8jPZDLQLQSapsXTVIuxHSoI1YF48O2aWQn0IYOJLT88y2L3KTlDGpbSxsqilZCagRVz4VsHCXD/SU51gzNTsLgaTOQdW1Iw7YVGfjZiASQmiZo6LBwznA3OjuuXw6m8gNlqYYRlvB9HI5l4Yy8Y03QiXEY6gYRaNyx6jj2XCQa9w29B0NnrbSxXJQrYpjPQCi8ISqHHFsHZ+QdZUVV0cSgJRUjFdDUWbZ6cIlUmKEv5GH0XPmkBKbCQdnJkp1SMxNWO7/WCWTHlscZeUfZsPh7r8XL4zXQ0FFUHflqkEgF1DbPNBuVg1AUQhFIj1qt/CpRrwBjfZZYrm4owQIdjhmckXeUHPU8dHwIBk76ZYbNUNOyZmEIiddaDX1qxMJEpT6/CFQ1WG5hpHdVhl5zGQtjFXJQ2+ISro6S49rrHCVB1bP69Ymk1bCrBxVVUN1U/mqX+ahptgqesT40FEXCkZKeXmLV9prH+q2Es7YFCRV/DfW8mTJSCUDDtrWv9XdcFDgj71gRWshbKWF20ox7LgOoJVajVVBZi0Ri67Y+EUHr22DwjFXcNHSUPBcg8VoUMUM/cAqNxCymHo1BaE4zl+eZt56btFr4TBpQqKi2hionZ+AoE+4vy1EUJqrlJwczqfPlB8IVpt0SiUE0tmFCDhIMow0dpi8zdAata0cqSustS7wGjcZNoGxKh8aPEKkEbNNTtTubKYIhy1HEaiyH4HCUEWfkHYtiujJj1savHiDmqcZrzKiHoxvGqM+HhKNo0w4YPgsjPWi8BqoaS+o5SzAEVQ1oZb3vrWdmBNamVGCDIQiGLWEbirgyScea4Yy8Y140n7XqlCldmYoqiNVsKE+9WCQYQht32OtJj8LEOFrZYFIKJZRBEJFpI+5wbBSckXecx7SuzPiQhRqqGiBeu+ljxhIIQG0zWllr+u9JM/haWQfx0hp7h2MjsbnfuY6SourBaJ957xVVJvi1yY37XCQUgYZtaHbCKlvGhyA1ik5tZi6M4thibK13sGPFqCoM90I2bdONKuu3tMGTSAwaOkxPZ3zARvelx9C6NjehybEsUkePcd/LXrXey1gQd4/qMBKDZuBrW5Cqhi1t4GdjUgjboa7NhMeGutFMer2X5XCUDOfJO9DJlCUk47XWLXqRISKmUR+psHLL4bNofTtSUbXeS3NsAir37uGGu79U3MHr4Dw5I3+Ro6pW2x0MQ03T2l8/n7WSw0IevLw/8i9oImDh2JomRCUYRhu3W7nlaB/aHF21FLLDsd44I3+xM5mc0Xdfo9JIVc/kD9KjfqfsFMJ0XfnUsZGYPw2qZk1CSBIIonXtMHDKkrJ1bWW/psNRTpyRv9hJjZgXv0ahCc1OmOxwIe/fPTSbBHEwbAZ2apZrPuN32KZMNiA1itY0m258mZFQ2Eotp65ZZuVMh6OcOCN/EaO5SfOka5rL7iWrqpUsJoet+7NhG0TiF1x3epZrMATRSlQb7W5jfNBi5VUNsBaJ4WglpEZNm6fEUggOx1rijPzFTGoUsKRjOZnWlc9NWtfsMgZuTydFKyrNo08Og3podVN5DX3Y15TJZwBn5B2bl3UroRSRHSLyHyLypIg8LiJvn+cYEZEPichREXlERK5bj7VuRTSfNUGtytqyhiM0O+HPdc1Y3L+udUXJVJEA1Lb6OvGj5RsIMo1OXbjM13E4yst6evJ54PdU9UERqQYeEJFvq+oTs465Hdjnf9wAfMz/7FgFqgpjA4BAZX35rpEehcSQH55ZvdSviKA1zabqmBpBg2Gkskwln4W8f1EXj3dsbtbNk1fVXlV90P//OPAk0DHnsDuAu9S4F6gTkfY1XuqWQlUt8ZlNQ215ZAvUK1h4JjEI0Tg07ShZF6mIQG2LnTfRj04kS3LeC5iaKLUGiV6Ho5xsiI5XEekCrgXum/NQB3Bm1tfdXLgROIpE8zkY6bFEZnVjWRqfNJOGgdP+2L8mqG8veThIRKC+3eLmo+fQydIaevUKpg8frdxy2j2Oi491N/IiUgV8CfgfqpqY+/A8T9G53xCRN4nIIRE5NDAwUI5lbmpUp2aunrIpTjXNSFVpB0aremjCKmAQMe+9jPo34o/MIxyxOavJEbtLWSWqnt2FeAWoKk8oy+FYS9bVTRGRMGbgP6OqX57nkG5gx6yvtwM9cw9S1TuBOwEOHjy4+nf6FsGajsatIqWQ95Ulm0rexam5LIz2WlNVvNausQaNVRIIog3bYazPSixzGXQVo/TU8/xQ1oQliddxfKHDUSrWzciLuXj/CDypqn+7wGF3A28Tkc9hCdcxVe1dqzVuVlQVJsetAqWQh1AUGlrL0kikuUnTewGo31by8XpLIYEAWtc2U4OfSaLxOqiqLzpMpKoWnkmO2GSnmmakzGWlDsdasZ6e/M3ArwKPishh/3t/DHQCqOrHgXuAFwNHgTTwhnVY56ZCsxNWOZPP+Ma9Zd6mo9Jca9LCM4GAVc+s00QkEYHqRrSi2oaBpEasWzUat0am8FRHrd1d6NTM1alB5OmE6eaEovY6XLLVsYVYNyOvqj9i/pj77GMU+K21WdHmRtWbHoBBIAR1rVBRXd6GoaQ/Papx+4YQ8pJwBOrb0VzGDHcmCWOp6cd1KoQ0e6g22KzaSqvYuVgklh0XD650YAuguYwlCws5i4lXN5VdvVFVzQuOVW8IAz8bCUdt1J82WZ4gn7WfTSEPiG1MgSCEoxCucKP/HBsKEbkN+CAQBD6hqn8x5/FO4NNAnX/MH6rqPQudzxn5Tc50yERkbUMNXsE84g3s+YqIb8jdpCfH5kBEgsBHgBdhhSf3i8jdc5pE/x/gC6r6MRG5HAtrdy10TufCbGI0OzETE2/csaaxZAmGoKLaYt/nyQU7HI5VcD1wVFWPq2oW+BzWFDobBWr8/9cyT8XhbJwnv0nRfM6qWgJBaOxYn5BJTZN1zg6fRaubLHSzgT17h6McZI4f59irX12q083XADpXyuW9wLdE5Lcx9byfXeyEzpPfhExLE4CFaNYpJi5TksHBkNWqD55G02OWBHY4HPPRNNW46X+8ac7jxTSAvhb4lKpux6oP/0kWaUxxnvxmJDls5X91bUhofZOeEq5AG3eYVEJy2OSAE4NWvhiusIEg4eiaTZ1yONaa6O7d7Pn854s7+AtfGFTVg4scUUwD6BuB2wBU9SciUgE0Af3zndAZ+U2G5nPWtFNRtayGHc3nLH6eGrXRe4GAeeDhKFLdaJLDKzTEM5rvVdYtmk5AbsIM/9T1Q1Ez+JEYRGJOE8bhmJ/7gX0isgs4C7wG+JU5x5wGbgU+JSKXARXAgnou7p222RgftM9FDt1Wz0P7T0L/qZlqmIoqyKs1AOUyaP8pCATR2hakaTsSr1nyvPMhIqba6CeAtZCfaTjKTVpXaXrMHguGbfpSJAbRmBux53AAqpoXkbcB38TKIz+pqo+LyPuAQ6p6N/B7wP8Ukd/FQjmv10WEm5yR30RodtK846qGouLwOplCTz9u+jV1rUjTdkuOzjKoWshDcgQdG4CxfnSkF43VIE0d9pxVGF8JhiBYNT0/VlVt3GB2AjJpM/hpm05l3alVEKtyoR3HRY1f837PnO+9e9b/n8AUA4rCGflNgqqaFx8IFjXoQzNp9NgDAEjXVUht87zHSTBkuvK1zWhhvyk6DnajZ56EnqNoQztS11qSyhkR8UM2FVBV7xt9f+OaSJo88figac+UeWJVuVGvMNOA5RX874ofJgtDKOw2M8ea4Iz8ZmEyOSMTvESHphby6ImHAZC9B4uun5dgCJp2QON2m7w02A0DZ9CB0xCKotUNSLza5rRGY6YHswrDb0bfYvRa3WSvLzUyrT+j1Y0Qr90UZZlayMNkykpKcxkz8Es9Jxy1u5eKqnXT/XFsfZyR3wSo59mUpVDEZAsWO1bVQjSZCWTPtStqkBIRCwlVNVjCNjGIJgbMyx6ZJQIqATNUwbAlcYMhu9MIhmzDCEXsI1JhcfdFQkyz4/may0BiwD7SY5Yr2ICyv1rIWyhsctwMO5huUCQK8RoIRmZ+JvYM8Dwo+FILmbTpDY0PodFKG+TiunMdJcYZ+Q3OdE28l4f67Ut7tYNnIDGIbNuPlGDohYTC0NCONLTPxNQnxiE7YcY4l7GQRCFnoRevAIW8hSvmvpZQ2DzzyjqobjAPdp7XI+Eo2tBhnvH4AAx1ozXN9rx1RlUtrJQeMyMNJptQ3WiJ5FCkiDuPCvtU7Vc9TSRMWG7wtN29lHHYiuPiwxn5jU5i0B+l17ykN6uZNNp7zCpvmraXfCnnxdRZXEJUPc8Mfz4LmQnbFCaTkBqzCVK9mAxwfRs0bLsgXGFlmVVoNGabXGIAzWegpmVdDKDmc2bYJxK2kU3lRuI1qwq1SChsMsmVddZjMD4E+ZzdvThD7ygBzshvUKYTrelRqKxb0otVz7MwTSCAbL903Q2EBAIQ8MXB/Hr+qRVpLgNjA+jIOduU+k5C225o2n5BMlICQbR+my+jPAKFAlrfviavT9WzXEh63GLtYN56vMbmv5ZwDRII+sNPhqwPIhiyuwOHY5U4I78B0UJ+ZgydLx285HN6jkA6gew8sOHjuhKOmkFv2o5OJtGeo2jPMzDcCzuvQPySy+njRaCmCQ2GLE4/eg6tayvPIJSpip90wgy8emZwqxrMay+jhIQNP2maKWuNVbuErGPVOCO/gbCxfUkzZJ4Hta1FNSbpwGkYOgvNO5G6ljVY6TxrmNKXn0xZrNrzppOwVNUh0flDTVJRBbuutuRu95PoM4dg9zXz3rlIZd3McJTEICxQFrqi9RfyfrNWwsJMU01jsRrr0F3LO6PqJj8fMQT17Wt3XceWxBn5DcJ0RUl2YmYmaxEeufafQnuPWq17+541WKl/Xa8Aw33o0Fl0dMBGDi4mOVxRidS3IjsuhaaO84ymiJjBjlejxx6y8s99z563MkiqGtBCAdKjaCi8qmSsJVH9pqyMP0EqbDX8VFSv2zARCYZMIiKTQlXXPfTm2Nw4I7/O2K35kHmQEoCaFgsLLPHGVlX03HHoPwm1LcjOK9YmTp1OoE/9FO0/M+PxVjcgbbugut4GeVdUmhfvFSyJOD4MY4PWZNV7HCprCVx+E9LSed65JVwBu65Gjx5Cjx+G/TcgwXkaomqa7NqJATQYXvbwcFXPft6pUTtPiZKoJSUcnUnyOp0fxypwfz3rhHoFS7ClRgGFuJUVFtPlqdlJS7KmRqG+Hdlxadm7J9Xz0BOPoEceAAkgHXuR5h3QdGFlzFyk2Sp9tFBAzx1Hjx3GO/QtAs++bfqx6WOjcei8Ej3+EIz0WHPW3POJWJJy6AyM9aGRncX93LyCee2pUTOe4QpLbi5QyrmuLDSP1uFYJs7IrzGqah7a+JAZmlg1VDUWJRmsqiY7cPYZQJHOy5E1iNnqZBrv/m9YHLy1i8AVz0FiVUs/cQ4SDCId+9CWTrx7v4b3wLcI3PjSC/IIUt2Axmst19DYMe8GJoEAWtdqfQGj59C69gXDK9MbanrMjGY0bs1eG7DBapqpjlnnxTtWybqKZ4jIJ0WkX0QeW+DxF4jImIgc9j/ePd9xmwXNZ2Go2+qhg2Fo2oEUqQmvqTELY5x50uLb+29YEwMP2KaSGCRw3c8SPPhzKzLws5FwlMD1t0MojPfMg/Mf09RhidyJ5LyP23kqoLbF4uojPVabP3vdnmfSygOnrPwyGrcxiQ0dG9vAg+Vmgk7fxrF61ttN+BTwYeCuRY75oaq+dG2WUx5U1bzIxKDFsGuLF/yabnAa67duyh2XQ315ygcXJDNhceu2XSU7pUTjSPse9PSTaD534UZX4WvlZ9JWl77QeeK1qASs5HT4LDp1bD5rcXf1TB+npnnDl5ZOoYWcGfmqhvVeiqMICqdPMvabr1/vZSzIuhp5Vf2BiHSt5xrKjaraaLyJcfMka1uLGpih+RzadwIGu025sLULad65TsM21D4mxhc1uMtFGrehJx+D8WGobz3/Qb+rdtGKnanzxKptPtroORibnHmgosoayTa61z6X1Kh9jpXuZ+24eFlvT74YbhKRh7ERWO9U1cfXe0HFop4Ho73mjVY1QtXSmiSqHgz1WOVMIWct/22719ULlV0H0DNP4T32Y4LX316y8+qkX7Y4X/hnOiZdXPORxKpNk149QEBkU0oV2wSvMbvTW+fRjo7iCHZ2UfvRTxV38Mc+Xda1zMdGN/IPAjtVNSkiLwa+Auybe5A/DPdNAJ2dnXMfXhdMWMw38LUtyBLqkWAxez35qHlylXVIx/5ljfgrFxKrQvZea6WTfaeQ1p2lOfHYAITC05OkziPre+Th4ksazahvPsN+Hskh++wkDRwlYkNndVQ1oapJ///3AGERuaDHX1XvVNWDqnqwubl0XZCrIjVqBr6muTgDPzGOHrnfpAl2XI7suW5DGPgppOtKqGnCO/w9NDm66vPpZBrtOYps2zvv3Y0mR+w/RfzstgqanbCQWGVdWeUTHBcXG9rIi0ib+BZARK7H1ju0vqtaGs1nTVysorIoI6UTSfToA6CK7H0W0rA2AlzLQYIhAgd/DgJBvEPftFGEq0CPHwZPkd1Xz39AYtBkiS+SkIWq2msOBF3C1VFS1ruE8rPAT4BLRKRbRN4oIm8Rkbf4h/wi8Jgfk/8Q8JrFBtZuGPxh1cXK4mrvUYsh7zu44iHaa4HEqgg860UwkcS7/+sWP14BmhhCTz6O7NiPVF74enUiCRPj66bDsy5kJ0wYraph3eQUHFuT9a6uee0Sj38YK7HcNFiz07h1URZTRZMcgfEhpH0vMlVRsoGRhnYC196K98C38R78DoGDP78so6T5HN7D34dwFLn0hvmPGe6xUtP6thKtehOQGjUvfgNv8o7NiXMZSs3U4OZix+5lJ+xzCRUVy420dSFX3mzzXx/9AcXeXKkq3uH/gMQQgaueP++mpp4HI72Wy9goOjJlZlooraLaNT85Ss5Gr67ZfKg/9q7Y8r2pGu7sRPEbw3KWk8/ancVE0uLouUlrFPLLDAmFkVgNVNZaDLxIrzyw83K8TBp95kFQhauev/SA8ad/Cn0nkctvWrhCJzEIhTzScBFJ7OYygM70BjgcJcQZ+XJRbOqgogoCQRua0RVb0eDtmUv6evSpUTQ1ZvXWuVkJ0mDIRLmmPGT1zPiPDdjXoQi0dEHjtqJqzGXfs2yY95FDaCFP4NpbFzT0XvcR9NjDSOdlSNeVC7+GsX4rq7yYSgjzWfu8STpyHZsLZ+RLTShqHnJ2Ynrs3WJIKAxdV6EnH0GP3Adte6wBqph4fiFv2i7pMdNoSY1auGhqHZW1SHy7rWOR5hprwBlFB07bhKmBU7D9UqRm8YlUIoLsuw4vFEaf+AneT79O4IqbkOqZ6hAtFNAnfoKefsIGgl9+04LJaBt5OGShmg1WXVRefIfgonrNjrXCGfkSIyJoJAaTSbS6sTiPuLoBLrkR7X7KPPqeZ6x7s6LSjHUgYNKzhbx1guYyFsOd8gBhRp+lqh4q6yBSUbShlFDYcgI1TTZ2rucZ9MQjsPPKoipcArsO4AXD6JM/wfvhl5Bte6GpA3JZ9NwJGO5Fdl+FXHL94iGdiaSFaqovshLC6Zs+Z+QdpccZ+XJQ1Wha5+NDppJYBBKxgRmkRq3iZjLpG70RG6U3NWs0GLawSnWjhXYqbLB0KWQPxB8Awt5noccPo6ceAzmAFJEUDnReirZ1oU8fQs88BWefsQeCYeTqFxDYvn/pBWQWkTnYykxtfG5AiKMMuL+oMiCRCjRea2GUcEXRte8iYvo2VfVlXuES6wiGYPc16PGH0FOPwv7rLxiuPe/zIhXIgZ9BL7seUgnbgJZxR0EmbZ8jpU9Ab2im7vY8NyDEUXpcvVa5qG6yEMpYHzo+VHSZ4UZBgiFk19WWFO5+elnrl1AEqW1CossbgK1ewaZOXWzNQNNToArruw7HluQiezetHRIIQEOHJT2TwzDaa+WMmwgJRZD2fZbQHT1X/guqN2PwLiamNrUN6gioKlrIobkMmp2wj1zG5LA36JodM7hwTRkREbS21WLo48MweQqNVUNl/aYZYEFDOwyesQRqXZmHlUiAWVnIi4epOa4bpLpGC3kLnWXSkM9APsdivxcNhk0tNFIJ0fhFoze0WXBGvsxYnL0BjdXYCLrUGEyMo6GI1chH49biv0E9WBGB1l0Wmx/tK6/UgATAK6CqF1cJpbfMBroyMN1jkR6dkXkOBK12P1ppCf+pKi+wjUk92wAKOevH8OcDqF++S0X1xRd6KwEichvwQUw3+xOq+hfzHPPLwHux3fdhVf2Vhc7njPwaIcEQ1DSjlfV+5cy4hXGSwwBm9INhawQKhGbeUNPGTgD1b+n9z6r+m23W98GeEwhDKASh6OqnSdU2QzSODp5BymjkReRi9OMh60+/Wgd5YVW1cFxqxK/uCZsKpl++W+xmq6pm7CdTNqh+rB8Sg6hf0rtRnZiNhogEgY8ALwK6gftF5G5VfWLWMfuAPwJuVtUREVm0hM8Z+TVGgiGrY6+ss9vi3KTVvecm7U2STa8wNivT+8DcW2uNxk0Rc4W30SICjdvRniNoagypvHg03teETBLCFWs+2lGzE2aM81mraKqss3DLCu6iRMTCklURtLLO/p598T3SCbS2ZVXd3BsZ7T1D5k/fXqrTXQ8cVdXjACLyOeAO4IlZx/wG8BFVHQFQ1f7FTuiM/DoiwRAEqyxs46PTHnrBL6nTGZst/j8iM16+CCDnvTFVFby8NU9NpsxTSw5D3Zw5qsuhoR3OHUcHTiOVB1Z+nkXQQm4mCXmRoJm0bfLVi3cXl/y6qRHTCQqGoL69qBLZYhERqyxriKGZlE0AGz6L1jQjlXUlu84mpUlEDs36+k5VvXPW1x3AmVlfdwNz5Vr3A4jIj7GQzntV9RsLXdAZ+Q2GTBvuwIon2YmI3XYHwxCJoV7eOnC1OH37ec8ZDKGNHTBwCs1MINEyDMeeSJpE80USj1f1zJMOhi2GvSbX9IeTpEct1l7XumhX9nQ4J51AcxnbkKaE7UIRG4pTtXA4RqKVaFPMqrMSA3b3Wt24pX7H0r6D6J98sLiD3/2hQVU9uNjp5vne3Fv7EDYG9QXAduCHInKlqs47ss0Z+YuBYNhi96vsqJTm7ejgabTvBNJ5eQkXCJrLQjoBDdtKet6NiqrCyLmZYe1rFbNODpuBj9dBTdPCOkLZCbT/lHnhU6W/U4lYP/6uUzpJwZB56a1RoRDtAAAgAElEQVS75t38JRBA69sh0W+x/2AQKte34W8D0w3smPX1dqBnnmPuVdUccEJEnsaM/v3znbCod7yItALvB7ap6u0icjlwk6r+4zJfgGONUfVsUlUktuqYr4Qr0KZO8+abOoqaXVsseu6YjT9s3rH0wZsc9TzzbDMp0xuKVq7NdTMpM/Kx6gUNvHoFM+79p+wbNU2mX1TdeMHfjxbypnU0NmBNf6Pn0KZOpLXrgmNFBK1pgULBErLh2KYYkrMO3A/sE5FdwFngNcDcypmvAK8FPuXPvN4PHF/ohMW+6z8F/C/gXf7XR4DPA87Ib3TSCfPgSySVIK1d9mY+8QjsvmbVw8ZVFQZOw3APNHeWLDmnhTwkhky6eKokUEAaO5B1vFuYjlEXcmbg1yhGrepZCWwoArXzh+20kEePPWiVX3WtS04rk2AIapuR2mY0txvtPW4OwPgQ7H3W/Ia+rtV+32N9tiFsobBNKVDVvIi8DfgmFrD9pKo+LiLvAw6p6t3+Yz8nIk8ABeD3VXXB2dfFGvkmVf2CiPzRrIW4HuwNjhbyVt0QiZdMD2ZG1+awDR/vOoCsUPtdCwW09xkYOmuGp233qten+SzadwKGeixEFQpDzNcOymXQM0+i6QSybf+a1nBrdsKqTTIpC581bC9PXmMhJsZts69rmzc0pKomBz0xjnRdVZQo3WwkXIF0Xo7WtaAnHkZPPw5dV11gxCUQRKsbLBdRpkE5mx1VvQe4Z8733j3r/wq8w/9YkmKNfEpEGvETACJyIzBW5HMd60ViwOKntaXVZ5eKKth3ED3+sH3UNSNNO2yyVDGDywt5GO6xsEA+ax58+95Vr1FH+9AzT1pVUkO71fRX1k2fV9Wb8Ta9AtJ5xaqut+R6CvmZnojcpFVEVTWYCN1a142nRi2eHllgYxnqhsQAsm3fsg38bKSmCbbtt7kEg90wX/gtVu0nf8eckV8DijXyvwfcDezxy3aagV8q26ocq0azk2ZgqurLMitVwhUmSex7zTraD6GIaejHqm2UXTBkybpC3ox5Jm0yyukx23yq6pG2AyUJWehgN3r2aZNd3nE5UnFhnFskgGzbi5ebhPGRVV/zgjWozmj9Z1MzYaJQBGqaIVazLh2g6hXs579IVYsO99odT1MJciJN22HkHDpybt4ci0jAejdymdVfy7EkRRl5VX1ARJ4PXIKV+DztZ3ZXhYh8Engp0K+qF8yEE/uL/CDwYiANvF5VH1ztdS8KxgfNwJaxikGCIWTbPrR1F4z1o4lBGB9ER3oXflKsGpp2ILUtJWuq0pFzZuBrmpCdB5Y0pFJRZV5/Ib/qZPT0EO7Jcfs8JVEQivqdo1Xrr1M0ZUwXWIdmJyxMU4K7KfBLeGub0XPH0NykOQRzCUX8sl7PdcOWmWKra44Bf62qH5/1va+p6ktXef1PAR8G7lrg8dux0qB9WEPAx7iwMcAxB81nLd5Z5GSq1SLBkJUBNmyb8WbzWfPgp8o2Q+GydHVqLuN78LXIziuL8pTVKzDdVLbS63oFS2qn/ZGLErC68wrLf6x19+qiTAmgLfS3kPdLIRcK5ayEqQ2lUID5Gq2nfvaKG4hVZor9S8wBt4jIDcCbVTWLdWatClX9gYh0LXLIHcBdfqLhXhGpE5F2VV3EVXSQTtjnWHHDSkqJdTtW2McaoGePgOchnZcXv6GlExCrWvEGqOkxiymrZ6+zugkqKjewRzplUBeQy4j4Bnn20PdVotkJ/9wLbByex2o3WkdxFPtXmVbVVwNPYt1VO1kbTdj5Wnwv2FxE5E0ickhEDg0MDKzBsjY4mVRJ6uI3OjqRhLF+pGVn0aWXWshbEnIFoSJVtZLMsX7zVBt3II07kFj1BjbwWPMRWNnmvI/bXZYO95ZEH14LBRjuteHxC91Z5Sata9YZ+bJT7F+mAKjqXwF/jNVpbi/XouZedw4X/BWq6p2qelBVDzY3r7wyYCugnucLTq1hed46oYNnLEyynGThWD+oh9QtT01T1bNa/vSY5TkaOjZPM08oaj+nzMS8D4uIDV+fTFo56yrRvhOQm0S27Zv/ca/gl0+uTRPYxU6xrt7sGs3visjPA79WniWdRzEtvo7ZTLWgr3eyr8xoIW+yAPVtRatrqio6dNY2wCLn7k6TGDKF0NqWknb6rgUiYtUsk0nUa5o/TFXbAlX1VvoYCJho2TK9bFXPOmUHTlkJ60INeCm/suliG9i+TizqyYvIpf5/z4rIdVMfQCPwtbKvzso2XyfGjcCYi8cvgTejJ7Kl8WPiy9K3T45AOoE0L6/TUidT03ovm83AT1PVYDkEf37BXEQE2XkA4rXWMHbiYSvDLRKdGEefOYSeO27dsh2Xzn9cLmO/h1j1/FU3jpKzlCV4B/Am4G/8r+eGSl64mouLyGcxJbUmEekG3oOfi/cree7ByiePYiWUb1jN9S4KNsCUobVAE4NWhldkjb16nunjhCImm1zsdbwCjPlyADUr6+zdCEg46k8nG0WjlfPmMCQUhj3XwWA3eu4o+uSP0aoGa3CqqrO7w2AYUJsIlZ2E5DCaGLIwViiC7LxyUdkERnotdFRzcYdV15KljPwnRKRNVW8BEJFfA14FnMRGT60KVX3tEo8r8Furvc5FxUVi5MmkrUKmmA5bVfTM4+bFd16xvKqa5LD9TNdSKbJc1DRZLHykF23smNeTFhHrUq1tQod7YLTfQjgzR3CBrxerMUmKxu0Lhs7UK8DwWSs3bdi2JqW9DmMpI/9x4GcBROR5wJ8Dvw1cA9wJ/GJZV+dYPp5fE73Vi49zmaLKNNUrmNTBaL81+ywjvGOVOGNbJrQggaDNBBjqhqGzaF3bvJ3BABKJIW17oG2PDTZJj0M+az0YItZFHTY9+aWavTSXMdXNvC+r7KQM1pSljHxQVaeCeK/Gpph8CfiSiBwu79IcKyKfsdvmrV6aVttshmpsYF6tFVWF0T6r9MikkbY9SMvO5V0jOQwoVG3eMM1cJBhGG7bDSA+M9KAVvuzwIjkcicanNWaW81el6sH4sCVaA0Fn4NeJJY28iIRUNQ/cisXni32uY42Z7ja9CN5Ism0fmk6gJx9F632PNByBXHaW4mPampR2XW1x5WWg+azFmeO1K56Nu1GRUBht2mE/o+QIZJJovK5kr1W9gg3zTvndwLEa20i2aIhGB3rJ3/m+9V7GgixlqD8L/KeIDAITwA8BRGQvToVy45EatfhxCed1lgJVtdLOXMbCSepZg044tuKGGAkEoesAevYZGys3Wy8nGDLj3rZwEnDJ9Y4NzKhGbkFEAlDdaMnY8UHztlMjaCQOFZXmKASL/92oV7BNNZO2env1IFwBta3Oe19nFjXyqvpnIvJdoB34ls60wwWw2Lxjg6C5LCSHIFpZ0qHMy1qDqoWLJlKQSaGTSYvlZtIz+ilzCQTQeJ3Fyutbl5XclEgM2XWVXbuQt00kFFm9NzqZtJr4muaydg2rP0aPQs7XcPEHtIcja5bklVAY6tttiHo6YR54Im0PBoJoMGy6QwFfUVQCgNpm7RWgkLVY+1Q3rQRsk4jXbZ5msVUize2E3vTupQ8EePN7yruYeVjyL1hV753ne0fmO9ax9qiq6ZUnfM9zFVrgy7pmdtLkEzJpqyOfNMPO1NxPsHK7eA1UNyCRmJXgBYJmzAp5yE6i2TSMD6NnnoC+E7DrqhVtUhIMlaQ3QAu5GdmCMtTEaz5nipWTyUWldjUUmW7aWoukrwTD5tlXNZjBzk7Y77iQ9dU1PS6oqpkaGB+OmrpoNG4idFs9H7TJcHH1TYyNuBswgxGusKk/wdLFj8/TR59MoRO+cZpMne+ZB8PmvdW1Wmy8osrCJUXo2MvUdcaHrAnn6IOw59pVjxVcCVPJWlB/glLpjJXmMhYWyfhecrjC5BFCEfOUscuiBfuZ5zK+yuUYGoraRrkGd2gi4q8pct4mp6omcDZL0dIZ882BM/KbEM1lLIY6MW7fqG6EyvrVT1ZShXTCZnSmxuzWfbZnHgpDRTU0dpgx96V1VzuURESshnvvs9BjD9rouP03rL0RGR80D7a2tWSDVlTVflfjQ36Mv9FKMhcLKfnG3BKY45YAHulFK+sXHfxRTkSmFCM3ea/ARYgz8puE6eEUqREzRCIQr7PxdquIQU8b9uEeuyvI5wAxz7y2xTzqirjF+sushyPROLTvNSM/2gfLkSxYJZoatcR1vBZZrq7NQuecGp49mTTDXduyrAoTCQShsg6N10Ki3373+axVE232xizHmuGM/AbHhlOM2Uchbwmw6kYzRivVQ1e1MMBIn8Wf81kTpapptlLD6sb1Kxusa4X+U2jPUaiqW5N4tGYmbIOLxkvWbj8d+plMmt78rFmzy0VE0JoWU5NMDFjt+TJLQh0XL87Ib1A0n4PUsFWnoJaEq26ycXIrNBaanbQB2iO9llSTANQ0IjXNNux7A4iaiQh0Xo4efQA98Qjsua68FS6FPIz2Wl6hlHH49Jhv4BsXVmNcBiJiXn12wjboqvotW3fuKC3r/652nIfmc9ZpOZEAxKoWKutWHCrRXNbmr472WTgCoKoBad29YQz7XCRWDTuvNCXEow9A225rpilHLDoxYJUjTR0lM5qaz5lKZjRe+hm7VQ22eaQTUILNw7H12Xjv8IsU9XwZ2ClDHK+FqvoVVctoLgNjAzbFKOlrd0fj0LoLqW9HossfKDJdh+4VbG5nMGjebyiCBEvvUUpNE3RdhfY8g558xEox2/cgJWxOms5zxKpLm2+YkvOtbS35xiThKCqBhac8ORxzcEZ+nVFV88wSA2ZAY9VQvbiWyLznyKRgbNAkeNN+M3I0Di1dSF2rP4O0CMXGXBaGz9l5xofR5KiVTC5S0000Zoay0m9fr2mCuuZVx/WlttnkfYd70b4T6LGHLExR02TXWW0nZSE3M6e1RGg+a3dh8bry3SVJYOHmModjDs7IryN2W99v3mQ4CvXbiu4SnE6ejg1YC/7U4ORYNdK6C+paiq6r1uQo2nsM7T9j55pqbI5X291EQ5tV20QqrJkpELAQRz5nxn9iHE2Po4M9cPaotcyIWAdrU4cJg9WsrPRPJACNHVZpM3jG5pD2PAM9z6DxGuuUrSt+OtR5THVwToyjsZrSeN2pEUDKFkrRQt4Gw5SwH8KxtXFGfh2wLtWEee9glRLx4qovdDLl63z3mYEVsRh7cyfUNhVdjaL5LNp9BD1zxOLHYBvDnmuQpg471wpqxTUzYXcUw73o4Fn0yAPokQf8zWenbRj1bUjF8rxwCQTtrqSly79GPzpyDj17BHqPoQ3bzPNfRhWLBIJodZNttMlhG5CxCkOvhbwlyuPV5fPiJ5P2eYPpEzk2Ls7IrzFayFvZYiZlFTO1rUt6oapqIlyD3X6MXawDsn3vkjKxF5wrPW7KjWeeNk+8tgm57EZk254FtcWXg0Rj0LIDabHRvJqZQPtOoedOoKefRE8+ZgfGqvzKnkYrlaysg8qa4rpkozFo2Ym07DQlyoFTMNRtg70jFdDQYTNGi4mzx2tMpyY5bBINNc0r0lxRzzPNdCh9snXqGoW8rTMctY5Uh6MInJFfQ3QyZaPkPK+o2um5muiEK2yQQ8M2JLy8N7mOD6NHH0J7jwMg7XuQriuR+pbFnzeRhJEBdHQAJtMzKpLRGBKvhqpaqG9ZMJkr0RjSeSl0XuqP0hv06/MH0MQQ2nca0BlVlHDUDG+sypqS4tXm9VdU2cYQjp73M5N4DbLzgC/xMIgO99iYv77jaON2pHmH6eYsgIigdW3WWTo+CENnbOh1ZT1EKopqOtJCzoaK5yZL2i173jXUs9F5ngcNpU/oOrYuzsivAaqehUT8OZg0dCw9TSc1inY/7XdLViKdV1o4ZbmyuakxC5n0HDVZ310HkK4rkdjCt/s6cBY9/hh64gkYPrfwcbO/qK6HpnakpRNp64Tmjgs8YgkELU5f3zpzjkIeUglIjaHpMUhbfJ/xYbT/FHje+dcJRczzr6q35G59K1TX291MfRtS34Zm0vbcQfPutboRae2yu4V5EBGI16AVVTawOzkCmbOAoOHozGzTYMjCY1MaLrmMGfZcBhCoby+LvozNRu2x69S1lb3z2LG1cEa+zMyMPsva0OnqxkW9Q81l0N6j5hmGo0jnFSb8tVzjnhhCjz9ixl0CyO6rkT1XLxiKUFU49RTeQ9+H3pNmzNp3ITe9GGlohbpmS8QGAvbY5ITFn5Oj6NA5GOpBB3rQE0/4Rlmgrglp2W6eZ10L1NSbREJF5XSISoIhqGmAmoYLpg5Nlzj6Kpc6kYTkmG2AfSeh+2m7Vjhq8f6WnRYqisaRHZehrbus+Wuw25qrKuuQtt0LNidJwPTjNV5nIZwpJcaJxEwy+rwniAmNVTWYWmQZkqE6mbTwnnpl20QcGwsRuQ34IBAEPqGqf7HAcb8IfBF4tqoeWuh862rkl3oxIvJ64K+Bs/63Pqyqn1jTRa6QqeoXEoNmGBu2IdHFY9460oeefdqqJ1p2Ii27ll2Drqkx9JkHbZhGMITsvMKSqYskOjUzgfe9L8KJx6GqFrn5F5BLrl08Rh+vso+mdqTrsplzTaah/wzafwbt70bPHoMjD80VqbWfScCXB57aOAKBmYqXYNAE0UIRCw3FKi1cU11PYMdlaK01R+lon13v3Em0+4idr3kH0r4Lad1lA6abd8LwWbT/lAmgxWv9RHXzvJunBAK+kqYvFDbluRfy+MLv/hpDZQubaD5rfzuZlP0M6pa++3NsfkQkCHwEeBHQDdwvIner6hNzjqsGfge4b6lzrpuRL/bFAJ9X1bet+QJXgXoFq37JpEypsbZl0eSoVbo8bR5bvAbZcfmykqCqCiPn8I4/Cn0nTQZ2z9XmvS+RRNSRAbyvfxoSQ8hzXoIcuHlVzU1SEYfOS5DOS2aukZ2EkQFIjqCTExbbz2XMaBbyM3F+9cAzg6pTgyhyORjzY/cTJnE8tWFoZS207kC27UZu+AUkP2kJ3nMn7XMkhuy8DOm83Ix6Y4d59gOn0VOP2u+mtWvJOyVTYAzaBlRmNJ/1O57HbeMrkcKoY9NwPXBUVY8DiMjngDuAuXbxT4G/At651AnX05Mv9sVsKsyg9VpjU02zCYktllwdHzbVxULOkqotnUUrDKrnob3H0eMPQ2LIwhZ7rzXvvYgSRR0bxPvyR0ACBH7hN5CO3cVddyIJ6ZRV53gFa4aKxqAiNu9mJpEKaN2BtmxHMhNmrFMJNJmwkE86iU6kLASU9bXUCwUTm5cAROK+bk/cpI3DYRQP8Y2/Hn8MuButb0H2XIUcvA3JTeKdfMzuao49jGzfZ5te0w5o3O4ntE/az/7ccWjabndb6yTzoIW8yRFPJMy4V9aZcd+AshOOOYwOUPjKP5TqbB3AmVlfdwM3zD5ARK4Fdqjq10RkQxv5JV+Mz6tE5HnAEeB3VfXMPMdsCDSdMG88GISm7YvWrKt66Lnj0H8KonFk9zVFD8rQ7CR65in05OMWr66sQw48F9m2t+imIM3n8L7xz4AQeNVvIbWNCx/reeiTD9jHyadhaOFkLOEIRCssUTkVhsnnIJu1+LZXmP95IrZRRKYSnUE/walm+CdT9pmZhK82tCKde+HKyyAahXOn0EPfhUPfQdu6CFz9XPSyG+HEo9YTcPop+xntP+g3UbVavf3AGWuwOnfcZHwbO9ZsaImqNzNQG5xx3/o0icjs+PmdqnrnrK/n8wino51iHuAHgNcXe8H1/Eta9MX4fBX4rKpmROQtwKeBF15wIpE3AW8C6OzsLPU6l0RV7RY7OWy17/Xti4pdaS6DnnzUYvYN25CO/UWJY2l2Ej12GD31hIU5GrcRuPJmi98vNzH7k3tgqJfAS96wuIFPDFO462/g7HGorEZ2XoI8+xaorrOYuQTMePthGM1O2P9nh2HCETPckahV9UzF8+PVUCigYyPo0AA6cA4dHYaxETTh3ykU8lYVFKuD6hhSXQuxOBIKQDaNHnscDv8YAgFk12Vw7S0QDsFTh/C++U9WgXPwVuQFr4GTj6EnH0N7jyGdl5mxr2tF6lqt3n6w2yQUhs5a3L5hm1U0lcngqleAoW5LyldUmZzFekk8O1ZOXTPBl7+5yIPfMqiqBxc5oBvYMevr7UDPrK+rgSuB7/vv+TbgbhF52ULJV9H5qgbWABG5CXivqv68//UfAajqny9wfBAYVtVFB28ePHhQDx1aMNFcFnR8yAx8rMbi74uFZ1JjJrjlFZDtl51XTrjgcwoFa2A6ehjyWaRjH7L7KmskWtF6R/A+81fIZdcTeP4rFj5ubIjCnX8KyTECL3s9cs3PrCper9kM3tEn0Ccfxjv6JN6JI5AYmTkgFIa6BqSmHmJxQKyopVAwQ5hJw8A5yEza8YEA0rWPwO5LkOo4nPLvMiprbCPa1gVP3AtDvdDcQeA5L4HGdvSZB9AzT0EwbOGtriumDbnmczaFaeisXc+fmyv17daAVqLYuOVReiAz4VfNrL4RzbF8ROSBJYzukizH5ix1PREJYVGLW7GCk/uBX1HVxxc4/vvAOzdqdc39wD4R2YW9mNcAvzL7ABFpV9Ve/8uXAU+u7RKXRpMjxRv40T709BMQjiC7r120Vn36OUM9eI/+0MbxtXQSuOR6pGZ1Sox6+AcAyHUvWPgYVQqf/zCkEgTf+C4Li6zkWkP9FH78HQqH70WPPmneuQiyvYvgNTdA1z40EqPQe478ieN4Z05RePAJdGT4wpOJEGjbRqB9F8HGRoLVcUgOUfju10A9ZPclBA6+CEkNo/95tzUzPf8X4Kqb4f7v4P3bnbDrCgLPeznSdSXeU/ehT92HnnocufQGpH23edLNndC0wyZmjfRa/H60D0JRtKEdadq++kqX1IhtIjXNzsA7plHVvIi8DfgmVnX4SVV9XETeBxxS1buXe851M/JFvpjfEZGXAXlgmGXEodYCzU5al+TUaLelDPypx83L7Lp6aSkDz0Of/il63GR2A9ffjjTvWPQ5Ra25kEefftCqb6oXab/vOwMnniLw0tct28Cr5+E9eojCt/4V7/C9oIp07Sd426sIXHY1gf1XUujtIfONr5H9+Mfw+izGL/UNBLt2E7r+ZvLBMF5BKWSz4CmCIl7BEqojA+QfPWyVN9EKItffRHhXJ3rsMQpfuss2kJ/9RdO0+dYXoKWDwCvfBINn0UPfwfv8Bwg8/xUEn30bOngW78l70Ye+i3YfIXDlzdZFKwKVtUhlLbptv3XTjvRC/0mrzmlotwarFUyusvDeiFX3xBe9MXVchKjqPcA9c7737gWOfcFS51u3cE25WKtwjaoHg2cskdi8c/EYfGLQphzFayzBukSMVzMTeA9+B4Z7rfzvshtKFqv1nnkY/fb/JvDSXz+vzPGC4/7zbrxvfJbgH34EqS3+zqFw3/fJf/GTaM9pqKkn+MKXEHz+7QRaO1BVst/5OhOf+RSFp5+AYIjwTT9D+MafYXIiR/Khh0kfPkzm2LH5m498JBqh4pJLqbx0H7FoEP3pj9DxBMG9l1DxvOciTz+I9pwmcNWzCb7wxeh3/8VCTi98BVxzM/q9L8JAN7L/WuR5r4BQGD31OPr0Ibsj2HM1svc6q5efw3Q37UivNZm17YamHcsK42hmAoa7rXt1jRK8jvnZaOGacuBS+CtlYtzixEslWfNZK9OLVRVn4LOTePf9O6TGkGteSKBjZWGSBc//yI+gthF27Fv8uJ6T0NCyPAN//w/JffC9yI7dhH/zjwnc8IJpjR1vdITkn7+H3A++R7BrN/F3/DHh59/KyL99lbN/+/fkus8SrKsjft111Nx+O4VYnFw6TWYsgebziASsmjIaIZjLkX30EQa/+GVQpeq5z6Xx5c9Gf/gdUp/8BJEXvZiKX/55Cnf/M96JI4Tf+ofw9AN43/kXpO8M8qq3wMM/RB/4HjoyQOClbyCw6wDavht98l4ruxzqJXDtrReUok5307Z0oWeftqqcXAba9xZv6LNp+7xEc5zDUQqckV8BqmoTnEKRJd+o2nsMCgVrcFrKwBcKeIe+CakxAs/+eaRpeymXjZ47BX2nkefesXQtfqFgFTFF4p09Re7jf47svpTIuz+IRGaemz96hPE/+G28wX7iv/1OKl7zOlI/uZdTr34t2ePHqbzxBtrf9S4mC8q5r/47z/z9xymkUjMnn9KLmUXVZZfS/ua3EgvA6Gc+w6kf/Yi6l7+cuhufS/aLnyF/+AEq3/F/o1/7Z3J/8yeE3/wHBNq78L7+GUgnCfy3dyAtHXjf/Azelz9qVUZ1zci1t+K17EQf+U+8H33JDH3jtgter0RjsOtqtOcIDJw29cumIsNpuUmbqDXPnYLDUWqckV8J+ax91MzfFj/F1OBsmjuLS7KefBRG+pBrby25gQfwHvieSQRc+qylDw4I5LJFnzv/5U+DKpHffd95Bl6zWcbf8VZUldqP30Xo8gOMff0bnHrrW4ns3Mmuf7qLiquu4qH//haGvv8Dwg31bHvly2m69RZiu7qYTE+Qn/SraQoFwvkc4489Qf+3vs0zf/N3BKuq2PuOt1MxPsbQpz9FuqWVzvd/gMyH/pLx//dd1HzgY+jXPkPuo+8n/M73E/il38T70j/gffbvCfza7xN42W/gff0uvH/7nwRe/XakopJAx160ugHvwW/j/fQeAs+5w7Tq5yAisG2/ySn3PFPU8BJVNc9/tVOtHI4ica7ESsj7xm8RCVsAxq1CROrblzylep41NzV2ENi2Z7UrvPD8Z56BU08h191SVGWIbOuC4T40lSjuAhNpZFsn0ni+dHHmnn/DG+ij+t3vJ3T5ATLHj3PmHe8gfs017P/G15G2dv7rRS9h+Mc/4Yq//gtueewhKl90K4c//yW+ePsd/MstP89Xbr/DPl76Sr7yq2/kyH2HaHjdf+M5//EtGm68nqff99hIZ8kAACAASURBVGf0nzxD1113kR8b5dQf/Qmx9/w1gbo6xv/kDwi+4R1I1z5yH30/bN9L4KWvQ48cRn/4NaS9i8BLfx0mknjf/YLlWgCpaSDwnDsgEsN78DsmNDffz0nEJnGpWsfqUhTylsdZQcLW4VgJzpNfCXl/iPJSXltq1I4ppkRu4AxMpqy5qcRoLoP3o7tNkvfAc4p6jnRdas99+mHkuucWcRG1Jqg5TH75cwQvvZzQQWtmPvvu9yDRKJ0f+yiFbJZ7X3wHEg5xw1e+SP0N1/PDP3gXj3z0H4i3tbLrxbex/ZbnUdnainoekyOjdH//B5z+9nc5/tV/p+O5N/Piz/8TZz75aY68/y+Z7OnhwF13cfJ1v8apt7+d3R/5EIm3/TrJP/sTqt/zfrLv+g1yH/8LIn/yd8jJp/C++TkTYmvbgTznJeiP7rbKo0stLyaRCgLX3op371fRp+5HDvzM/K89XgPBEJoctk7axZga01jCubIOx2I4T34lFF1IoSYWVsxYv4yfjKtpWvGy5j2vV8D75mdgdJDA819ZfJVO535o34n37S+YsuQSBK58FtpzGu/M8fOvn0oR7NptipGqpB98kLo77iDS3s65r/47udFRrvvUJ6i/4XqOfOFfeOSj/8CBN72RX3vqYW79+N9zyat/ie0veB47XvgC9r3q5dzy93/L6548zC0f/SA9/3UvX3vVr7Djja/nqg9/kJH77qf/Jz9lxwf+lsyx4yQOP0b8zb9D/qFDFM6dI/SqN6BPPYwef5rAHb8OwRDefd8GsM2vvgV9/N7z1i8NbdC6Ex04veBrNwEzoag/jEzKhM5CTlHSsTY4I78SpqppFtJhmT4uBPk8RZWpFgrnn7sEqCr6g6/A6aeR570c6dxf9HMlECB4x6/D2BDe//4gmhxb9Pjgc38OgiEK3/rX888TicCEea+5nh68VIqKfVYxdO7fvkp81y7qrn82qb4+/uNt76D9phu5+S//PwKhhW8yRYTLX/d/8XP/607O/fR+vvfWt9Pxy6+i6dZbOPr/f4DY9dcTu+Zq+j/8YaIvfQVSU8vk5+4i+PzbIRYn/+1/ReJVyIEb0Yd+hOayFna5/AboO2P6+LOv17gNJpI2zGQe1CvY3d1Sg2A8z4x8RdWWVpVUVZPuSI1a+fBon83jTQzY9zLp4t4TjpLgjPxKmBrvlp1c9DCpqDRt+MzSnvB012O6yBh4EeiD30ef+Cly3S0ErphP+22JNe3cT+Dlb0SPP0HhA+/EO/zjBd+cUlNH8GdfRuG7X6Xw0Iw3HNx/GbkH70czGQJVVSBCfshi114mS6S5ERFhon+AfDrNgbf8d4Lh4u429r7yDi771dfS/Z/Wwbvz119PPpEg+fQR6l/+cnLd3XjpCcI3/Qz5p55A4pUELrsGPXnU1rz3gMkKjNp6ZNsuO3FiTmx9qY13zAayS+USjU1Tw0e2aG28FvJoYgD6T8LgaRtUnxqxjS03YV3biQEYPgv9J8z45xZ/DzlWjzPyKyFcYZomSxnvqdBLYmDpczaYho0O9y5xYHF4j/wYve8byL5rkRt+bsXnCVx/K8Hf/nNoaMX7/Icp/MN78R75iWm8zCH02jcjnXvIfez9eH025yX6kjvQ8QTZ73+HUG0tsSuvJPmjHwNQdcl+kk8dQT2PyjaLZad6l/f66y+9hMzIKJNDw8R3dQGQPnma8HarTsp2dxNs24Y30IcWCkh9Ezrs/z4qfWM7lVyeMuaFOXdoyRF7bJ4KKVU1nZtIzCZELcD0EJlQdMslXVUVTQyacU+N2h1NbQs0d0HbXqR1N9KyC9r2QMsuqGs3+ejJJAyeQUfP2d2Qoyw4I78CRMRK4CaT09UY8x4XqbDZocO9S96eSjQO1fVo/+qVlLXvDPrjr8GuK5Bbf6loffoF19a6neBb30fglb8Bo4N4n/0Qhb/6Hbz/+Fc0NRPCkEiU8O+8B4DcX/w+mhglfPBGgrv2kP7I3+KNjVF7222kfvpTkv/1XzTcfBP5RILuz36eisYG6vbt5aG/+zDpvv6i15Y4fpJAJIKEQuTGLKQUCIfQrF8BFQighYJfa++ZMuYUUxvVlHEf98XSZjVAqeeh507abNr5QixjA/+nvTMPj6M88v+nejSa0X1alnzItwEfGIwxEFjCDSGBsCEENsdmCfkRcmezyS6Q3SSEXQLk4EcSsglHsiEQzs0mkEC4rw2nbWxsbGwLH+BLtmXdGl3TtX9UjyQLjTSyR6ffz/PMo9ZMq6emJVVX11v1LWiuQwbqem1r7hoBOZ5SNV1Ca821dhGcMA0pnoRkFyAZ4f2HrosgoQwkK9cWqMum28D0WKM5+/h7AwfHweOc/IGSU2hOI9Z3njaBlE61iD+F8jopn2FStyksdCZDO9rxn7wHcvLxTrsoJQnjVBDPwzv2NEL//FO8S69EKqbhP34/8Ru+jP/cQ2ig9e5NqiTzm99H9+2h/aZ/g84Ocr99Hf6+Gpp/eC0ll32GzMpKtv/btyk75yyKjl/K+u/+O+17azj7zttpq6vn8UsvJ97Wd8liT2reXMfa39zF3I9dSKQgn92PPYGEQpSecjIty5cj0ShZRxxBfMM6QjPnIBlh/Hc34VVaiaru3GrOv9yamHSbjUykfFr3+dy1GWJNeNMXvOf9Nd5pzVDRXCidnNROTZRXhsLjKlVjDn5nILRWhhSWI4lUZgqIF0LyS6F4sq1v1Wx3Ef0Q4Jz8gRKOWm6+ua7/KL2gDMKRfqszEki5TWbS3VsP2Cx9axnU15iDjwxQx38AiOfhzV1E6NIrCX3tRmT2Avy/3GOR/Qt/QuNxvDnzCV9xFbphDe3//o+EJk8h67NfoP3Jv9B2351M+u53aauqYts3v8n8H1xPPBbj1QsvJq+sjFNu/iHbn/9f7px3NGvvvLtPZ6++zxu/uJ0HTz2bcG4ux1/zrzRv2sy7//VbSk4+CS8jg7qHHiZn6bFoYz0dK1eQsWARWluDbt6AzDrcUgzrV0J5JZIZQTs70I2rYMqcrgok9X20aoWVSE6ctr8NqjaysaMNmXJ4/3dLCQmMNEoVjwpam+wOJa904PWIfpBINhRPsnGPTbUD/4BjULg6+QNERNCcIqivtkgmSS28eB6UTkV3VqEtDUh2fvKD5hVBVq6lbCqPSL5fP+jGlVBcjkxJr+ZNX8jEqYT+/hvolrfwn/kD/iN3w6oXCV34OUInnAahDDpuuZb273+T6FU/IL51E7Ff/pScq66h/Kor2fX968nIL+CY3/2GFZ+6lJfP+wiL77yDv33sYZ7/xlU884Wv8sr3rmPKKSeTN3UqkaICql9bwY7/fZHYnj1Unnk6p/7sJkK+z8sfvQRCHvNuuI7qH99E5549lN92K7G7fg2dHWRd8ik6H/s9+D6h086DdzbCtrfxzr/UzlvVKovYj+zuU9B334LGWrzFZ7zXOddsh7pdSPnMfh2c+r4plYYjEB1nUXxzrd2d5BQe9PEkMwuN5kJLPZpbPLYkH5rrib/08EhbkZQxdCZHIVl5dnvftK//aL5kMnghdG//+XYRMTnhvdvNOQwSbYvBrq1WNTKMyPTDCV16Jd7HvwZ1NcR/ehXxh3+Dd/TxhL92LfruJjq+9xWyL7uC8HEn0nz9d8kryKb0c5+j5q67aLrrLhb/+jY6G+r56ylnUvfnR/jbhx/k/IcepGzxUex88WVW/PhmXrz6O1S/+hqVZ5zK2Xfewbn330Xja8v46+nn0F6zj2PvvZvYc8+y9447KP7kJwh7SuuDvyPzrA8ikUziT/wP3rEnIWUV+E88YPNiF59sUfzyp6G4HIKLo8aa0PWvQXEFlM/Y/zw311uaJq/E8sr90VzXNe93XEXx8U6TZxhghvGgyC6wFGj7gacrHe/FRfIHQVc037DHOhmT6JFIKAMtKrd8++S5SKifEsGicnhnHTTVwWCHgySqRArS3FDV0WYTl5ob0I5AtyeSZRFsfhGSa5Gct/A4ZOY8a6B68S/Eq1YTuviLhK/8AR03f4eOa75Mzpe+TUs0SstPbiTvvI+QceW/UP2jHxNbtYqjb/oBO558hq23/5p3/uu3TDj1/Rz10Y9QeN33CE+YQGd7OyGB2NZ32PvMczx/zPG07thJ3vx5HHn/zbQ8/hi7b/4J+WefxcTLLqXxi5filU8i+yvfoOPm7wBCxsc/jy5/Dn17Dd6HP4NEovgvPWoprvP/X9C05eOvfAb8ON6RJ+/nxLpGN4ajSOX8/rWLfN+i3UgOMpAExpgjCGrS2NeR1mMNJzkFhE44b6StSIpz8gdLdn73fNd+RKekeJKV2tVVQ0ly8TEpnIACWr978BOg2qzp6GBz8drRDtur0K3r0e1VQR35e+9Uup4pKEGmzkWmHwFT5xC64DL8ecfi//cviN/yb3hnXEjmNbfQ8cOr6fjR1UT/7nN402bSeudtROYfyfRbfsL279/ItiuuIO/00znm5zdTs2oNu/74ELsfeyKpnSWnnMwR111LdlaE6quvJrZqFUUXXUT55z5L0z9/GeJx8n54C/5Dd6Mb1hD+wtUIPvE/3wXTD0eWno7u3IKufB45fElXikvfXmVa/otO2S8Vo76Pbl0D8Q5k5pKBu4djDRaZ5vYznGWskliDSOdCadexxtEdzyjAOfmDRMRDcwqhsQbtbE9eXZCVB5lZaP1epB8nT06+VXykKgy233vYuoC2NA3630RVYecWdN2r6NurrbwwIxOmzLJa+9IKWzMIR2wwd2sLNNWjtbvRbVXoW8vRNS+Zw194InL4EkJfvRH/j7/Cf/x+WL+K8NeuofPeW4n/9meEF7+PjKuvofmnP6Lz2quYfMFFNPthan53D41PPUXmjBkc/omLoaKCjrjS0dAAvo8XjRCdVEFmOEzH2rU03PJTdq9dR3jKZKbceAPRtkYaLrsEyc0j70e3oE/9gfgTfyD0gYuQhUuI/+I7kBEidNHnobUZ/7G7TNPnxA/ZeajZga5fhkyahUzeX3Nft6+3csnK+akN+2hrsTmy4y6Kp1uaoaUeTVdZaHOdXTycrk9acU4+HWTlW4lcS0NS7RkRQfNLoGYH6seTljaKeFZvPEBpZp/kFds/SW3qdebaFjMH/ebLULcHwhFk7mJk1kKYNCO5Bn52HhRPNKmERSdZOeGmNegbfzWhrxXPIEvPRD72BeTwxebs7/h3Qud+Epl/DPH7boWNb5L39W/QtmIVbb+/l8zCIqZd9ilaI7nUP/Eke375y67GJIlkEiooJN7QQGNr9yDv7MWLmfS9a8idUETrg3cTW/cmmaeeSfblXyR+3234q14h9MGLCX3wY/j/dQO0NBK6/NuQV4D/0O3Q3op33mVIJAttacR//Skb0bjwb/ZP09RsM9nosukDi5AlaI9ZeeU4RETQvGIroWyuO+i7FW2PWaVObnHayn4dhnPyaUBCGWgkG1ob0bySpFGN5Baje7dBSyPk9lOREM1FW5uTv57UjhBMmoFWrUKPO6v/iVX7qtHVL6Lrl1vUPrESOfWjyOxFXdOcBvfeGcico2DOUejOLfgvPYI++3tY+QLeSecR+uoNxB/4T/R/bsObvRDvX26g857biN/5E8IzDyd85b/S9txztN3za0SE0nkLKfvGl+nwMuls76CzsYl4XT2hggIyiorIyM0mmh3B37SB9ntuo7m+Dm/yFHK+831CGUrHdV+HtlYyPvOPhOYcQfzn/wptrXif+DqUTcH/869h97t4Z30CKamwiVyvPgrxON5xZ+53R6ZN+9BtttCaKHNN7aR4lq4Zr0Ry7NG4FxVBDrDKRtuaoXZX2ip1HPvjnHy6iOZZOWVHW/LbzUR+t6WuXycvEUvrHAjeopPwH/kN+tT9cOKHkOzutILGmtCtb1mZ5bvW+CNzFiEL3oeUpTakRGNN6J5tQY10zGqbo7mQnYfkFUNhmWm0/+3nYcta/Jcewf/Tr2DWQrxLvghrV+A/+jvYup6Mkz+Evv8DdD50N9z7n0RmH0H0m1fSubeW9heepf2uO0CVEBDyPCQ3D21thfY2FIgBkp1D+LgTiZzzQaStCf/P9xDfvQOZM5+My76OvLuB+G3XQkEJocuuhrwi/IdvtwlZZ1yCzFqIdrbbRK5YA97Sc+1zJD5vW4sttEaykWkLBpeWiGRBazPq+2OrJDBFRMQKCmp3QcMei8bzSlJuiFI/bnXxzbWWGiye5KL4IcA5+XQRzYF67JYziZOXjEw0ko021/efM8/KheotqPqDliSQ6fOQY89Elz2Jbn4TJs+yCU+tLbCvGlDILUCWnoXMOw7JTmFiVXsrunWtjTJs7NGsEo6YXn5rM6jaQmwkC5k4HZkyF5kxH6/yMPT159AVz6Bb1iFHnYz3pevQx+9Dn/495BcTvujv0ZY24o/9Hv+B2/DCmWQfcSTywQ8Q9z20oxO/JYY2NiBZWUhODl52Nl5+HtLZiq5ehn/rf4DvI9PnkvFP1yHZUfTBn6N7diBzF+Fd/CWo34v/wM3Q2oJ31seRWUdaBP/ao1C/9z2j/rSzHd20EhBkxqIBxze+h6x8S7vt24YWTRr8z48BRDy0qCIoPqg1qY/MLLvwR7JtTSK4MKqqCfa1t3Y3UqnaecqfMC4vhKOBEf2rE5FzgJuBEHC7ql7f6/UIcCdwDFADXKyqW4bbzlQQL4SGo0EHYEnyHbML7PZWNXlUmFNgGiuxZst9DxLv2DPQOYtsUPXenRCJWqnjzAXIjHlQOik1jfv2VvTtlejWdRaxF1cgRxxvtfy5BV0XIFWzVWur0V2b0e0b0XfWWVQ/YyFyzKnIYcegLz9q9ehvLUOOOxs54Uz8x+9HH7kLojmETj8HKS7Hr1qPv/Jl/NXL7NxifyBkZVtqqcM0ThKJEKmYSuhDl+AtWgoNe9GX/oRu3wwl5Xif+ieYvQBd/gy68nnIK8K78ItI6SS0uQH/tb9ArBFv8ZlI+fTuzx6Po5tXWUfrrMUHVLEkkWxzgLW7YO87aEGZlVOOp3p5Ai2nvBI0u8BE2GIN+4nyqXhWTNCzEscLWTFCdgEyzgTbRhsj5uRFJATcApwJbANeE5GHVHVtj90uA2pVdbaIXALcAFw8/NamSCTbGqP6W1jNyUdrd/ZfV59bZFFxw94DcvJgpZhy+oGfKt25CX/NX6G91SpNZh2VtKRTxLN0TXYeTJ5tzUXbNqCbV6OvP4VuLMSbu8TSIwtOwP/rw+jTD0BBKd5pF1jV0Yt/QV981FIbJeVknPR+KJuCdsShrQ2aG9GmBghnIpEo5OQhhcUQCSM11eimN9G7f2RNOhOn4l3wGTjyRNj0Bvq7H0JLo5VJnvghJJKFv70KXfMCiIe39AO9IvgOc/AtDcj0hQfXsh/NRUunQt0uW6QMR9H80nFZcSOhDHP2ucUWFLTHuscdqkIoBF7YqrPC0XF3sRutjGQkvxSoUtVNACJyL/BhoKeT/zDw3WD7QeBnIiI6WicOBE6etpbkQlQJOdrGfurqCyfYOLm92020bBjR9lb81S/Ars2QX4p33LlIfj93Jn0gGWFk+nx02hGwawv+hmX4K56E/BK8uccgH/kismUd/quPo0/ea9Ushy9BTr0A3n0bXbcCff2F/QeJZ0YttZQY0NEWM3VJQEWgYhryvrORBceZhPCGFejvbrR1g4lT8c7+JFIxHY01EV/+OATKkt5Rp+2/btEWQzevhPYYMm0hUrD/zNoDQcIRtLTSItzGGqjZZi38+aX9N8aNUUTEcuyDECtzDB0j6eQnAz37/LcBvSdbdO2jqp0iUg+UAAe2KjnUhKN2W9oeS+7kM7NMsKyxBinte7FTvBCUTEKrt6Lz3jdsuUqtrTZn3B5DDl+KzDgy6Xur+lbLH7P6ddQ3iYesXMjKQ0Jhi/ArZuKVT0e3V6EbV+Ave9yc2+yjkIu+jLyzHv/NV9EVz8Dyp6GkAjlsIXLq+ZaPqdkFDbU2UDyWGJ2XYZIExWVQVAb5hUhjLbprK/rCH6B+r/0eZi4wLZry6dDWgr/uFXTLGjvHhx2LzFzU9flUFep2WRWNgMw8GkljE5OIQHYBGs2zhcamWmhrQQsmIn3o1Dsc6WIknXxf92q9I/RU9kFELgcuB6isrDx4yw4QEbG8fD8To0QELZhg9fLxzqSLcV7l4fjLHkd3bUImDa3YmKqiW99E174M0Ry8912AJJFG0OY6U9Rs3Ndvt6Nm5VkUXFiGRLKRKXPRSbMtX1/1ul1MsnJh2jy8My6GjnZ002p081r09edgxTN2oOw8yC0wp15QAGgwRq8Jrdpu04aCahu8EEyeiSw6CZkx3362dhe68ml05yZQRSbNNge/X/TeYoqSTfssR1w5f0gUPCEQrMsrQbPyLIVTtxNtL7AL30Hq/jscfTGSTn4bMLXH91OAHUn22SYiGUABsK/3gVT1VuBWgCVLloxsKicchebafitjpKDM6uXr95gAVl+UTYOcAnTDcrSsclA63YNBO9vRN543J1hWiXfUqUgfs0o11oTu3GjOPRSGonIrNcwptFm2IpaHjTVCS4PN9tz1Nux6G80tMl39/FK8qYehU+ZA9Tv4W9agb72KvvWaLQZXzMKb83G7I9gdzFrdVx1E8S1ofY3VnnuepQKKykyKoHACUjYVSsrtjmJfNbplNbpzs6XOgvSRTF+wnwqotsXQPVutyUk8ZPJcKJkyLLliychES6aaQmVzHcQ70aIKl6d2pJ2RdPKvAXNEZAawHbgE+HivfR4CPg28BHwUeHrU5uMTJBxkf4OdcwptsbFmO5LEyYsI3sK/wX/5z+gbz8PRp6fdAWhDjUXUzQ3IYUuRWYve8x6qCru3otWbwAshFbPNEYb6WFjOyLTKorwSZOIMq5uurUZrtqFb3rALYMkkq9Ipn06ofDraVGepnB1V6OrnLSLPykUKy+w8zV2EF822FvqEVoyq3UW0x9C2Vog1oDs2oOtf7i7x9EIwYSpSMROZOK1bI17VZgAkdIRErD574ow+L25DiYhA/gTUy+h29uNR58YxooyYkw9y7F8CHsMq5H6lqm+KyPeAZar6EHAH8FsRqcIi+EtGyt6USUTcHW1JnbyIQOkUdMdGNNaYVAdFSiYhhy9F33rFhNAOOzYtjl7jnVYaWbUSMqN4x39wv+qSrv3aW9F31lhKpKAMmXLY4Cb/ZGbBxOlQVgn1e83Z79oEuzZZZ3BxhUX3hy1B5x4DjbXovh1ozU60fg/s3AxoH9JofZCVB7mFSMUspLjc0kRBKkxV0ZYGGzJdW21rJl4IJlQiEyqH3bm/h5xC6Gi10tpIlispdKSVEa2TV9VHgEd6PfftHtutwEXDbddBkaiW8Dv736+owpxd9RZkenL9d5l5pEWeb69EG2pM+jbJgJKBUPXRnZvQ9cusPHDSbGT++2wWbe99G2rMwasiU+dZeuYALzAinjndwjLLf+/bYbnyrWusiiivxFI/ucXItPldo/bUj5sERHsMOtrQjg5bpRFBvAxrOsuMWuTfY21DVW1Rs2432lxnufaOYMJUbhEycYZdtPq6GxkBbJ2mzJrKWhqgwDl5R/oYfy14I40IIPsPjO5rt4yw1U/v3tLvxCgRgYUn22LdW6/gP/eA1axPmYtEk0sb90RbW9DqLVZZ0mQpAe+4c/us7lH10eotUL0ZornI9IU2ni1NSCQbqZiNls+ynoLaalPwrKu2HTLCVoGSlWt3AonuyZwCc+xmpeXeOzusDrt+N357zMolW5stD5/QjAmFLcLPnwD5qbfcDzfihdBojnWMjrcBI45BkUKT6NeBzwKdwB7gM6qadGaoc/JDQmrLBlJWidZsNwnb2UuSC5uJIDMWoBOm4K9+Ad2wDF3/qkXXpZPMAWYXWLNJ4Py0uR6aatF91bbAC5BXjLf4DCif0ed7aVsL+s6bFk0WVVh6pj+RM/XNoXa0Wboh3onVH4otnmZELGWVGX3PcRJdkpJXYpF3axM01aGxRlu83bvNjj8YwlGTl8grtrud7ALTnBkrDjMcsfOgPsjouMtwDC8pNom+DixR1RYR+TxwI/00iTonn24SZYUp6JRIKAyT5qDvroV92/sdJgIguYWETjgPbdyH7txsEgIbVwBJLiteCApKrWSwbJrppvfl3FVh3w50x0ZLhVTO71dOV+OdJrLW0tD9eTMyu1NVqub4W5u6fyYjYs1fkWzIzNrPDhGxnHpWXlfNrKpCZ1sggtYZdE4GFxGwKpuMsJ3nxIVkkCWI9h4dEG/vfg/1zX4ILlRBd+ZAA0LSQeLuz5VSji3aWvCrlqfraAM2iarqMz32fxn4ZH8HdE4+3XQENfKppgWKyqF2J7qjCrILU2qMkbxiy2HPPSZwuFa2aBGgWEljToGlPAaIYrWp1px7rNHy1VPn9ZmjhyBybwoaeVCTmc0uMFGyPhyT+nFz9u0xezTXWSOQeCbNnJn1HhGrrs8oYpF5GhYhVdXKOzuD0YUdbd3b+7+rlWcm6NEHoJlZ9lmjA5/TA7axvaXPc+EYV5SKyLIe398alIAnSKVJtCeXAY/294bOyaeblgaLoFPUJhERmDoPrVqGbloBsxYjgxg0YXohRfZIka4ywt1brc0+HEEq50PhxKQORluboWG3RbvR3JQkZcULdUfvBDNP21u6ZYoTkb54aDjSXSYZCttXL2T16wNdqHzfovx4HPyO7qg8Hmx3drDfvU4iQo/kdLffhzKsRLTnoBD1TVqhrQVi9da8FAqj+aXpFxpra7aLTxpkFBzDTCQbb/Yxqe69V1WX9PN6Sg2gACLySWAJ8P7+3tA5+TSiHW32z5rTd1okGZIZhVmL0arl6MblMOWwfh3uAdvX3gr1u9HaXRa5h8JI+SyrJ0+Se9d4pykKtjYFmt+TD3ghVjzPLhDR3O7oOqicoaPNHGnvNgiRQMUwUDLsMixYfPV9+vwfEM8cdygcOPNwqIAq3AAADM5JREFUl0NPVbNcEqPoMqNobpH9bhtrTGgsMwvNK0161zMYtKMN6nebfVl9L8A7DhlSaRJFRM4AvgW8X1Xb+jugc/JpQlVtaIgXOqCGFolkw5wl1qn5zpuw623L0RdOPGBHop0dNoOzuc5SLC3B3NhoLjLlMFtcTebcVU02trHGHGpuiaVz0nTh6UvEShNNTvGO4BG3CD2hjZO4ACRs8ALn74UsRZVQOQyF0j58QkTs4hTJsfPStA9q3jWhsUEMyuiNtjYFTVme/T5cquZQZ8AmURE5GvglcI6qDjjr0zn5dNFca9FoYfkBOxjJzII5S6B+D7p3G7qzCnZWoRmZVjUSyTZnkpEZODexIFbj4PtoR7stViYWPTs7EkeG7HwbXVc4sd9IvCs33LDXctaZWVZTPgylh5KoygllAKNTildEIKfQtGcSawytTbbGkJUP0ZwBF4DtHMfsZ9taLE1VVDE8i7uOUU2KTaI/AHKBB4Kg4B1VPT/ZMZ2TTwPa3moRb5CKOBiscWgiUjjRorzGWjTWYM6gbjca7+jvh7uqQcgvRSI53YMZBmj8STQQWeNQq6U5CisCp+Wiy96IF3rvoIy6XQAmUpcZtXOYuNvw48H6QHt3HX9wjMGm9xzjmxSaRM8YzPGckz9IVP1gQS7DIt40/rNKcNHoeUT1fUtlJHLSEKQrPPAyBv3+NtWp0aLSznb7HPkTLPJ3pXwDst+gjPaYOfD2mElB9LVW4GUEwUAOZGa7kXeOIcc5+YOlqS4YjTd5WIYQi+eBd3BaK13pgtYmc/Dq2x1AwUSrVXdR5aARkf0riRLrC+p3NzeFQu7C6Rh2nJM/CDTeaemNaG5aW/+HAvXjFmW2NlvO3Y9beieSYwJZbhxbWulaX3A4Rhj3V3gwxBoA7X9w9whg5Ymdlltvb7WovTOosuqqXc+1QRwusnQ4xjXOyR8Msaag5X1kRa8s/dJqEXpHq1XXdHVrii0C5habc3cRu8NxSOGc/AHSpa2SGMw93O8f7ww6R5stUk/UkGdkdjlze0ScU3c4DmGckz9Quhpzhi/d0VUJEws01sHK9LLyu4W/hmHx1+FwjB2ckz9YNPkw67S9harl/xv3WQdoKGx3ENHckZ9q5HA4RjXOyR8g4nmmTBhrQnNLhiwlom0tph3T2W7pl8Iyq692KRiHw5ECzskfDFl5JizV2gwpSAQPBo132nDnWKOV4hVVpF/50OFwjHuckz8YsvKspb1+F5oxNS2pE0vNNFr0rj7kFNmkI1fq6HA4DgDnOQ4CEQ+KJtni674dprl+gKiqpWZqtpmaZUYmlFYi+aXOwTscjgNmRCJ5ESkG7gOmA1uAj6lqbR/7xYHVwbf9Kq2NFBLKQIsnm35N7Q6Tos0vTbl2XtW3dE9zndW4e6aBQ1a+S804HI6DZqTSNVcCT6nq9SJyZfD9v/SxX0xVjxpe0waPhCNoaaVJxzbtgz1bbdJRol49FEw5Qq30Mt7ZPfy6rdmec8JgDsfYpLMdrdk20lYkZaSc/IeBU4Lt3wDP0reTHzOICOQWo1n5llNvbTTxsr4ndxleBkRtgHXv4dYOh8ORDkbKyU9U1Z0AqrpTRJINtowGQ287getV9Q997SQilwOXA1RWVg6FvSkjoQybDJVbZKJgncGUo4QgGIFwVTjiGpccjvFARiZSMmWkrUjKkDl5EXkSKO/jpW8N4jCVqrpDRGYCT4vIalV9u/dOwbTzWwGWLFnST+g8vIgXgswQcPBzQB0Oh+NAGDIn39/0EhGpFpGKIIqvAPqcU6iqO4Kvm0TkWeBo4D1O3uFwOBx9M1IrfA8Bnw62Pw38sfcOIlIkIpFguxQ4EVg7bBY6HA7HOGCknPz1wJkishE4M/geEVkiIrcH+xwBLBORVcAzWE7eOXmHw+EYBCOy8KqqNcDpfTy/DPhssP0isHCYTXM4HI5xhSvIdjgcjnGMc/IOh8MxjnFO3uFwOMYxzsk7HA7HOMY5eYfD4RjHOCfvcDgc4xjn5B0Oh2Mc45y8w+FwjGOck3c4HI5xjHPyDofDMYoQkXNEZL2IVAVDlXq/HhGR+4LXXxGR6f0dzzl5h8PhGCWISAi4BfgAMA/4OxGZ12u3y4BaVZ0N3ATc0N8xnZN3OByO0cNSoEpVN6lqO3AvNkmvJx/GJuoBPAicLv2MlRupyVAOh8MxPlAfWpvSdbTJwLs9vt8GHJdsH1XtFJF6oATY29cBx52TX758+V4R2Zri7qUkOTGjDGdn+hkrto4VO2Hs2NrTzmkHe7DlK15/TLLySlPcPTHSNMGtwWS7BH1F5L2n3aWyTxfjzsmr6oRU9xWRZaq6ZCjtSQfOzvQzVmwdK3bC2LE13Xaq6jnpOhYWuU/t8f0UYEeSfbaJSAZQAOxLdkCXk3c4HI7Rw2vAHBGZISKZwCXYJL2e9Jys91HgaVU9dCJ5h8PhGKsEOfYvAY8BIeBXqvqmiHwPWKaqDwF3AL8VkSosgr+kv2Me6k7+1oF3GRU4O9PPWLF1rNgJY8fWUW2nqj4CPNLruW/32G4FLkr1eNJPlO9wOByOMY7LyTscDsc45pBy8iJSLCJPiMjG4GtRkv3iIrIyePRe9BhK+9LazjxUpGDnP4jInh7n8LMjZOevRGS3iKxJ8rqIyE+Cz/GGiCwebhsDOway8xQRqe9xPr/d137DgYhMFZFnRGSdiLwpIl/tY58RP68p2jlqzuuQoqqHzAO4Ebgy2L4SuCHJfk0jYFsIeBuYCWQCq4B5vfb5AvCLYPsS4L5Rauc/AD8bBb/vk4HFwJokr58LPIrVHR8PvDJK7TwF+NNIn8/AlgpgcbCdB2zo4/c/4uc1RTtHzXkdyschFcmzfzvwb4ALRtCW3qS9nXmISMXOUYGqPk8/9cOY3Xeq8TJQKCIVw2NdNynYOWpQ1Z2quiLYbgTWYR2YPRnx85qinYcEh5qTn6iqO8H+CICyJPtFRWSZiLwsIsN1Ieirnbn3H+V+7cxAop15OEnFToALg1v1B0Vkah+vjwZS/SyjgRNEZJWIPCoi80faGIAgXXg08Eqvl0bVee3HThiF5zXdjLsSShF5Eijv46VvDeIwlaq6Q0RmAk+LyGpVfTs9FiYl7e3MQ0QqNjwM3KOqbSJyBXb3cdqQWzZ4RsP5TIUVwDRVbRKRc4E/AHNG0iARyQX+G/iaqjb0frmPHxmR8zqAnaPuvA4F4y6SV9UzVHVBH48/AtWJ28bg6+4kx9gRfN0EPItFAUPNYNqZSaWdeYgY0E5VrVHVtuDb24Bjhsm2wZLKOR9xVLVBVZuC7UeAsIikqpWSdkQkjDnOu1X1933sMirO60B2jrbzOlSMOyc/AD3bgT8N/LH3DiJSJCKRYLsUOBFYOwy2pb2deYgY0M5e+dfzsXzoaOQh4O+DapDjgfpEOm80ISLlibUXEVmK/d/WjJAtgnVcrlPVHyfZbcTPayp2jqbzOpSMu3TNAFwP3C8ilwHvEHSNicgS4ApV/SxwBPBLEfGxX/r1qjrkTl6HoJ15BO38ioicD3QGdv7DcNsJICL3YBUUpSKyDfgOEAZQ1V9gXYXnAlVAC3DpKLXzo8DnRaQTiAGXjMDFPcGJwKeA1SKyMnjuaqASRtV5TcXO0XRehwzX8epwOBzjmEMtXeNwOByHFM7JOxwOxzjGOXmHw+EYxzgn73A4HOMY5+QdDodjHOOcvGNMISLfClQF3wiUA3tPsk/nez0blNc6HGOWQ61O3jGGEZETgA9h6oJtQbNa5gib5XCMalwk7xhLVAB7E5IJqro30BjaIiI3iMirwWM2gIhMEJH/FpHXgseJwfM5Yhrur4nI6yLy4eD5LBG5N7hLuA/IGqkP6nCkC+fkHWOJx4GpIrJBRH4uIu/v8VqDqi4Ffgb8/+C5m4GbVPVY4ELg9uD5b2GSEMcCpwI/EJEc4PNAi6oeCfwHo1dzx+FIGZeucYwZArXAY4C/wZzzfdI9meqeHl9vCrbPAOb1kNzPF5E84CzgfBH5RvB8FGt3Pxn4SfBeb4jIG0P5eRyO4cA5eceYQlXjmDLosyKymm7Btp76HIltDzhBVWM9jxGIUl2oqut7Pd/7OA7HmMelaxxjBhE5TER66n0fBWwNti/u8fWlYPtx4Es9fv6oYPMx4Ms9FAgTUtLPA58InlsAHJnuz+BwDDcukneMJXKBn4pIIaZwWQVcjlXcRETkFSxw+btg/68AtwRplwzMiV8BXIvl7d8IHP2W4Bj/Cfw62H8l8OowfS6HY8hwKpSOMY+IbAGWqOrekbbF4RhtuHSNw+FwjGNcJO9wOBzjGBfJOxwOxzjGOXmHw+EYxzgn73A4HOMY5+QdDodjHOOcvMPhcIxjnJN3OByOccz/AefnAP5Cl8XBAAAAAElFTkSuQmCC
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
<h2 id="Heat-Map,-Spider-Plot,-Tree-Diagram,-using-Avengers-Data.">Heat Map, Spider Plot, Tree Diagram, using Avengers Data.<a class="anchor-link" href="#Heat-Map,-Spider-Plot,-Tree-Diagram,-using-Avengers-Data.">&#182;</a></h2><p>Data is completely random and in no way ment to serve as actual representation of Characters' traits.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># Create a random dataset</span>
<span class="n">data</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">random</span><span class="p">((</span><span class="mi">10</span><span class="p">,</span><span class="mi">6</span><span class="p">)),</span> <span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s2">&quot;Iron Man&quot;</span><span class="p">,</span><span class="s2">&quot;Captain America&quot;</span><span class="p">,</span><span class="s2">&quot;Black Widow&quot;</span><span class="p">,</span><span class="s2">&quot;Thor&quot;</span><span class="p">,</span><span class="s2">&quot;Hulk&quot;</span><span class="p">,</span> <span class="s2">&quot;Hawkeye&quot;</span><span class="p">])</span>

<span class="c1"># Plot the heatmap</span>
<span class="n">heatmap_plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">center</span><span class="o">=</span><span class="mi">0</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;gist_ncar&#39;</span><span class="p">)</span>

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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Import libs</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># Get the data</span>
<span class="n">df</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>

<span class="n">data</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;Name&#39;</span><span class="p">:[</span><span class="s1">&#39;Iron Man&#39;</span><span class="p">,</span> <span class="s1">&#39;Captain America&#39;</span><span class="p">,</span> <span class="s1">&#39;Thor&#39;</span><span class="p">,</span> <span class="s1">&#39;Hulk&#39;</span><span class="p">,</span><span class="s1">&#39;Black Widow&#39;</span><span class="p">,</span><span class="s1">&#39;Hawkeye&#39;</span><span class="p">],</span>
        <span class="s1">&#39;Attack&#39;</span><span class="p">:[</span><span class="mi">83</span><span class="p">,</span> <span class="mi">60</span><span class="p">,</span> <span class="mi">80</span><span class="p">,</span> <span class="mi">80</span><span class="p">,</span> <span class="mi">52</span><span class="p">,</span> <span class="mi">58</span><span class="p">],</span>
        <span class="s1">&#39;Defense&#39;</span><span class="p">:[</span><span class="mi">80</span><span class="p">,</span> <span class="mi">62</span><span class="p">,</span> <span class="mi">82</span><span class="p">,</span> <span class="mi">100</span><span class="p">,</span> <span class="mi">43</span> <span class="p">,</span><span class="mi">64</span><span class="p">],</span>
        <span class="s1">&#39;Speed&#39;</span><span class="p">:[</span><span class="mi">75</span><span class="p">,</span> <span class="mi">63</span><span class="p">,</span> <span class="mi">83</span><span class="p">,</span> <span class="mi">67</span><span class="p">,</span> <span class="mi">60</span><span class="p">,</span> <span class="mi">58</span><span class="p">],</span>
        <span class="s1">&#39;Range&#39;</span><span class="p">:[</span><span class="mi">70</span><span class="p">,</span> <span class="mi">80</span><span class="p">,</span> <span class="mi">100</span><span class="p">,</span> <span class="mi">44</span><span class="p">,</span> <span class="mi">50</span><span class="p">,</span> <span class="mi">80</span><span class="p">],</span>
        <span class="s1">&#39;Health&#39;</span><span class="p">:[</span><span class="mi">70</span><span class="p">,</span><span class="mi">80</span><span class="p">,</span><span class="mi">100</span><span class="p">,</span><span class="mi">92</span><span class="p">,</span><span class="mi">65</span><span class="p">,</span><span class="mi">65</span><span class="p">],}</span>

<span class="c1"># Get the data for Iron Man</span>
<span class="n">labels</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="s2">&quot;Attack&quot;</span><span class="p">,</span><span class="s2">&quot;Defense&quot;</span><span class="p">,</span><span class="s2">&quot;Speed&quot;</span><span class="p">,</span><span class="s2">&quot;Range&quot;</span><span class="p">,</span><span class="s2">&quot;Health&quot;</span><span class="p">])</span>
<span class="n">stats</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="n">labels</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>

<span class="c1"># Make some calculations for the plot</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">labels</span><span class="p">),</span> <span class="n">endpoint</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">stats</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">stats</span><span class="p">,[</span><span class="n">stats</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">angles</span><span class="p">,[</span><span class="n">angles</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>

<span class="c1"># Plot stuff</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">111</span><span class="p">,</span> <span class="n">polar</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="s1">&#39;o-&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">fill</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_thetagrids</span><span class="p">(</span><span class="n">angles</span> <span class="o">*</span> <span class="mi">180</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="n">labels</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">([</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="s2">&quot;Name&quot;</span><span class="p">]])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>

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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get the data for Captain America</span>
<span class="n">labels</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="s2">&quot;Attack&quot;</span><span class="p">,</span><span class="s2">&quot;Defense&quot;</span><span class="p">,</span><span class="s2">&quot;Speed&quot;</span><span class="p">,</span><span class="s2">&quot;Range&quot;</span><span class="p">,</span><span class="s2">&quot;Health&quot;</span><span class="p">])</span>
<span class="n">stats</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">1</span><span class="p">,</span><span class="n">labels</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>

<span class="c1"># Make some calculations for the plot</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">labels</span><span class="p">),</span> <span class="n">endpoint</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">stats</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">stats</span><span class="p">,[</span><span class="n">stats</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">angles</span><span class="p">,[</span><span class="n">angles</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>

<span class="c1"># Plot stuff</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">111</span><span class="p">,</span> <span class="n">polar</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="s1">&#39;o-&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">fill</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_thetagrids</span><span class="p">(</span><span class="n">angles</span> <span class="o">*</span> <span class="mi">180</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="n">labels</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">([</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">1</span><span class="p">,</span><span class="s2">&quot;Name&quot;</span><span class="p">]])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>

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
<img src="data:image/png;base64,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UZHlpptuyrvssst0ZrOZsbExIpEIZrMZi8WC2WwmLy8PheLcDWJFIhFcLldyKuNyudBqtVitVvr7+9mxY4f3scce83m93j6Xy/U/Ho/n8cQiT1nOY7IGY55ILBuwtaSk5IOxWOxNq1evVt9www35jY2NinA4TCgUIj8/n8LCQqxWKxqNZsY2z3X8fj+jo6OMjIzgcDjQ6/VEo1F27doVfuSRR5zd3d0h4I8DAwO/AfZkHannH1mDkUESI4lLS0tLbxdCrH/zm9+sevvb326pra3F6XSSk5NDcXExRUVF5OTkLHR35xUpJV6vl6GhIQYHB4lGo4yPj2O32+Xf/va3sX/+858R4JnBwcHvSilfXej+ZpkdWYORAYQQRRaL5RMajebjl156qeHjH/+4paSkBLvdjtFopLS0lMLCQlSq16/sxe/38+KLL2I0GgkGg9hsNlpbW/nJT34ycvjw4TG3232f1+v9jZTSvdB9zTI9WYORJonRxMWlpaX/mpubu+q2224zX3755Wqn04lGo6GiogKbzXZWHZTnMv39/TidTpYvX04oFGJgYIDe3l6EEOTk5PDnP//Z/4tf/MIbDoefGRwcvEtKeXih+5zldLIGI0WEEFqdTvces9n8lfXr1+d/7nOfs+bn5zM+Pk55eTnl5eXodNllTk5l7969LFq0CLP55CVEvF4v3d3dDA4Okp+fT3t7u/zOd74z2tXV1TU0NPSNWCz2VNbXce6QNRizRAihz8/P/79qtfrW973vfYZ3v/vduYFAAI1GQ01NDQUFBRPFX7KcQjQa5YUXXuDyyy+f9juKxWIMDg5y4sQJVCoVkUiEBx54wPn000+7fT7f3W63+5dSyshZ7nqWU8gajBkQQqiNRuMn9Hr9ndu2bTNfc801uqGhIQoKCqitrUWv1y90F895BgcHGRkZYeXKlbPa3uVy0d7ejtvtxmq18stf/tL98MMPjzkcjs+HQqE/ZnNhFo6swZgGIYTQarXvMpvN3/3ABz5gee9735vrdDopKytjQlyVZXbs37+f6upqrFZrSvv5/X7a29sZGRnBYDDwwx/+0PnMM88MDA0N3SqlfGGeupvlDGQNxhQolco3FhYW3n/llVfabr31VpPP56OiooLq6urXdaQjHWKxGM8///wZpyMzEQwGOX78OMPDwwghuPfee8eampqODQ4OfiIbkj27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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get the data for Thor</span>
<span class="n">labels</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="s2">&quot;Attack&quot;</span><span class="p">,</span><span class="s2">&quot;Defense&quot;</span><span class="p">,</span><span class="s2">&quot;Speed&quot;</span><span class="p">,</span><span class="s2">&quot;Range&quot;</span><span class="p">,</span><span class="s2">&quot;Health&quot;</span><span class="p">])</span>
<span class="n">stats</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">2</span><span class="p">,</span><span class="n">labels</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>

<span class="c1"># Make some calculations for the plot</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">labels</span><span class="p">),</span> <span class="n">endpoint</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">stats</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">stats</span><span class="p">,[</span><span class="n">stats</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">angles</span><span class="p">,[</span><span class="n">angles</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>

<span class="c1"># Plot stuff</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">111</span><span class="p">,</span> <span class="n">polar</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="s1">&#39;o-&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">fill</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_thetagrids</span><span class="p">(</span><span class="n">angles</span> <span class="o">*</span> <span class="mi">180</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="n">labels</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">([</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">2</span><span class="p">,</span><span class="s2">&quot;Name&quot;</span><span class="p">]])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>

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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get the data for Hulk</span>
<span class="n">labels</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="s2">&quot;Attack&quot;</span><span class="p">,</span><span class="s2">&quot;Defense&quot;</span><span class="p">,</span><span class="s2">&quot;Speed&quot;</span><span class="p">,</span><span class="s2">&quot;Range&quot;</span><span class="p">,</span><span class="s2">&quot;Health&quot;</span><span class="p">])</span>
<span class="n">stats</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">3</span><span class="p">,</span><span class="n">labels</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>

<span class="c1"># Make some calculations for the plot</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">labels</span><span class="p">),</span> <span class="n">endpoint</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">stats</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">stats</span><span class="p">,[</span><span class="n">stats</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">angles</span><span class="p">,[</span><span class="n">angles</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>

<span class="c1"># Plot stuff</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">111</span><span class="p">,</span> <span class="n">polar</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="s1">&#39;o-&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">fill</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_thetagrids</span><span class="p">(</span><span class="n">angles</span> <span class="o">*</span> <span class="mi">180</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="n">labels</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">([</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">3</span><span class="p">,</span><span class="s2">&quot;Name&quot;</span><span class="p">]])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>

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
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAQwAAAEPCAYAAAC3GPo9AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4zLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvnQurowAAIABJREFUeJzsnXd82+W1/9+PtmRND0neO3s5kxASCNCW1bJL2gIdt5cuLoVeCh33R6GU28WFQhd00PbCq5cWKC0dEDYZkD2d6TjeSx6yJWuP5/eHZJMQJ/GQ7AT0fr30si19v9/nkSx9dJ5zznOOkFKSIUOGDKNBMdUTyJAhw9lDRjAyZMgwajKCkSFDhlGTEYwMGTKMmoxgZMiQYdRkBCNDhgyjJiMYGTJkGDUZwThDEUJIIYRPCPFAmq5/gRCi9Zi/G4UQF4/ivPuS85JCCFU65pbhzCUjGGc286WU3wYQQpQJIRqHHhjpAy6E+IwQYkOqJ5EcqwxASvkdYHaqx8hwdpARjAwZMoyajGC8j0kuG6qO+fv3QojvjeK8GUKIBiHEmvTOMMPZRmYNepYgpWwEytI9jhBiIfBX4MtSyn8kx077uBnODjKCcXbzVyFE9Ji/NcCOCVxvJfBvwE1SyjcmNLMM70syS5Kzm6uklNahG/DlCV7vi8DbGbHIcDIygvH+xg8YjvnbeZrjvwiUCCEeTt+UMpzNZATj/c0u4JNCCKUQ4hLg/NMc7wUuAVYJIX6Q9tllOOvICMb7m68CHwX6gU+RcGaeEillP/Ah4FIhxP3pnV6Gsw2Rqbh1ZiKECAIh4FEp5f+b6vkMIYT4DvA1QAtkSSljUzylDJNIRjAyZMgwajJLkgwZMoyajGBkGDNCiJgQYpcQYp8QYrcQ4mtCiNO+l4QQP06e8+PJmGeG1JNZkmQYM0KIQSmlMfm7HfgjsDG5Me1U53mAPCllaBKmmSENZCyMDBNCSukCbgFuFQmUSUtiqxBijxDiCwBCiBeALGCzEOIGIUSeEOK55HFbhRArksfdK4R4QgjxphDiqBDituT9WUKIfyYtmlohxA3J+xcJId4SQmwXQqwVQuRPzSvxwSCTGp5hwkgpjyaXJHbgSmBASrlECKEFNgohXpZSfixpmSwAEEL8EXhYSrlBCFECrAVmJi85A1gNmIBDQohfksgPaZdSXp483yKEUAM/Ba6UUnYnReQB4HOT9uQ/YGQEI0OqEMmfHwbmCSGuS/5tAaqBhvccfzEwS4ih0zALIUzJ3/+ZXLaEhBAuwAHsBR4UQvwQ+IeUcr0QYg4wB3gleR0l0JH6p5ZhiIxgZJgwQogKIAa4SAjHf0gp157mNAWwXEoZeM+1IJF/MkQMUEkpDwshFgGXAd8XQrwMPA/sk1IuT80zyXA6Mj6MDBNCCJEHPAb8TCY86GuBLyWXCwghpgkhskY49WXg1mOus+A04xQAfinlU8CDwELgEJAnhFiePEYthMhUA0sjGQsjw3jQCyF2AWogCjwJPJR87Dck6nbsEAlzoRu4aoRr3Ab8XAixh8T7cB2JzW8nYy7wYyFEHIgAX5JShpNLn0eFEJbkdX4C7Jvg88twEjJh1QwZMoyazJIkQ4YMoyYjGBkyZBg1GR/G+5xkfoSKRMgxCkRlZh2aYZxkfBhnEcnIgwPIB/JVKlVBdnZ2tVarLZNSFkWjUbtCodCpVCpFMusShUIhlEqlVCqVxGIxotGokAmIx+MyGo3GpJR+tVrdJaVsDQaD9b29vfVSyg4SOQ3tQLeUMj6Vzz3DmUFGMM5AktGFUmCRw+G4QKVSrZBS5ut0OpXT6YyXlJQoSktLdaWlpYaCggJFfn4+BQUFOBwO1Gr1mMcLBoN0dnbS3t5OR0cHbW1tsaamJl9jY2O4tbU13t3dLQKBQFSlUjUGAoG3ent71wPbpZRdqX7uGc5sMoIxxSTFoYykOCiVyhVAQUVFBatWrcpavnx51qJFi8jPH9sWCSklSSti+HchBEmrY/j3sVyvoaGB7du38/bbb3vWr18fbGtriyuVysZgMLjuGBHJZFq+j8kIxhQghHBotdqP5ebmfkZKWVVZWXmcODidI9fqjcViBAIB/H4/fr+fQCBAKBQiFAoRDoeJxY4vfjUkDEM/jxWQePz4FYZKpUKr1aLRaNDpdOj1egwGA3q9Hr1ej0Jxon9cSklTUxPbt29n48aNwyKiUCh2t7e3PyGlXCulHEjdK5dhqskIxiSQtCJmZ2dn36DVaj9ut9tta9asMV199dW66dOnn3B8PB5ncHCQ/v5+PB4Pg4ODBAIBFAoFBoNh+KbX69FqtcM3pVI5rvlJKYnFYsPiEwwGh4Vp6CeAwWDAaDRisViwWCxkZWWdYKVIKdmxYwfPPfec79lnn/X7fL42j8fz5ODg4F+SzZgynMVkBCNNCCE0wMr8/Pyb4/H4xfPnz1ffeOONOZdddpkiJyfnuGODwSB9fX309vbidruJx+OYTCYsFgtmsxmTyYROpxvTEiLVSCnx+/14vV4GBgYYGBjA5/Oh0Wiw2WxkZ2eTnZ2NRqM57ryWlhZeeOGFyJNPPtnf3NwcBp7v6Oh4CtiacaSefWQEI4UkLYlVBQUFdwshFn/kIx9RrVmzxnb++ecf90EKh8P09PTQ3d2N2+1Go9EMf+BsNtu4HJdTRSgUwu12D4tdLBYjJycHu91OdnY2KpWKv+5s48drD9Ha1YvOVYu9Z6fnyJ6tAeDVzs7OH0spd0/188gwOjKCkQKEEHabzfYFjUZzy6pVq7LuuOMO2znnnHOcRTA4OEhHRwddXV1IKcnNzcVut2Oz2Ub0D5ytRKNRent76e7upre3ly1dkt/s8ROKvvs+06uVfO/KWRi69/Hggw/27N+/v8/r9f7E5/M9JaX0TuH0M5yGjGCMk6Q1cW5BQcF9RqNx3m233Wa96aab1GazefgYr9dLW1sbnZ2d6PV6nE4nTqcTrVY7dROfZJY98Cpd3hMr8hVa9Wz8xoUAdHZ28utf/zrw61//2heJRF7t7Oy8X0q5f7LnmuH0ZARjjAghtDqd7hNWq/Vbixcvzvmv//qv7GXLlg0/HgqFaG1tpa2tDa1WS2Fh4bjzI85mpJT8c28Ht/5x50mPeetLcygsLESlSiQcx+NxXnrpJXn//ff3NjU1NXV1dX0nHo+/mPF1nDlkBGOUCCEMOTk5d6nV6i/eeOONWbfffruxsLAQSHw4XC4XTU1NBINBioqKKCoqOsEB+EHB5Qny//5Wy9p9J8/rKrBo+d01xbS3t2O1WikrK8Nmsw0/fuDAAX74wx/2v/TSS16/3/+A1+v9rZQyetILZpgUMoJxGoQQarPZ/AWDwfDtr33ta9Zbb71Vp9frAYhEIjQ3N9PS0oLNZqO0tBSr1TrFM546pJQ8t6ON7/59H55gFL1aydJyG+/U9xKOvfs+EwIeun4+Vy8sQkpJT08PjY2NBINBysrKKCgoGA4R9/X18b3vfc/7xz/+sc/tdn8tHA4/n9kLM3VkBOMkCCGEVqv9uNVq/fHNN99s+/a3v220WCwABAIB6uvr6enpobi4mJKSkg/ckuO9tPUH+NZf9vLW4W4AFhRb+fx55eQYtbyyeS9/OxKi1x9FABL43WeXsHq6/bhrBAIBGhsb6ezspLCwkPLy8uHXtb29nbvvvrv/lVde6ejq6vqilHLdJD/FDGQEY0SUSuVFeXl5v7j88ssdDzzwgGUo83JwcJDDhw8zODhIZWUlBQUFU5obcSYQj0v+uKWZ7//rAL5wjCytkpvPKWNldW4yuzRO35FdZFfVIITgn3s6eGpzE3MKzfz91vNGfP1isRjNzc00NTWRl5dHZWUlOp0OgEOHDnH77bf37dq1q66zs/MLmZDs5JIRjGMQQix0Op2PL1mypPLhhx+2VVZWAuDz+Th06BB+v59p06aRl5f3gRcKgMYeH3c/t4fNDX0ALCmz8bkV5VgN7/puQl43YW8fpoLEaxmOxvnqn3bS74/w2I2LuGTOyGnwkHCCtre3c+TIEfLy8qiqqhqOMG3dupVbb721t7m5eXNnZ+etUsr3ViXPkAYyggEIIZxOp/P3FRUVi3/2s5/l1NTUAIkMzIMHD+L1epk+fXpGKJLE4pLfbWzgwZcPEYzEMetUfHZFOcvKs094fTxtR9BZ89BkWYbve3l/J7/b2Mg0h5EXv7oKpeLUr6mUktbWVurr63E4HFRVVaFWq5FS8sorr8jbbrutt7+//4Wurq6vSikH0/KkMwAfcMEQQgij0XiTxWJ58PHHH8+5/PLLFZBIPjpy5AidnZ1Mnz4dp9OZEYokdV1e7npuDzub+wFYUZXLzctLMetO9OFIKek7snN4OTJEJBbna3/eRc9gmEfWLODKBYWjGjsej9Pc3ExDQwNlZWWUlpaiUCiIx+P8+te/Dn/nO99x9fT03BiNRt9KzbPN8F4+sIIhhHA4HI6nL7jgggWPPfaY1Wq1IqWkra2Nuro6SktLKSsre19lYU6ESCzOr9Yd5ZFX6wjH4tgMaj5/XgULS20nPSfsGyDY3425sOqEx9445OJX645SlmPg1a+dj0o5+tc5Eolw5MgRXC4Xs2bNIi8vD4Dm5mbWrFnjrq+v/7vL5fqylNI39mea4VR84AQjaVXcmLQqcoesCo/Hw969ezEajcycOfMDm0MxEvvaB/j6M3vY3+EBYPV0O59aVkKW9tQVHr3t9WhM2WhNJ4pKLC6585nddHqC/OjaeXx8SfGY5+X3+9m7dy9KpZLZs2ej1+uRUvL444+H7r333u6enp5PRaPRTDQlhXygBCNpVfzf+eefX/P4449brVYrsViMw4cP09PTw5w5c45LHvqgE4rG+OlrR3jsrXqicUmeUcu/r6pgbqHltOe+uxxZQKKs6IlsPNLDz944QqFVz+t3no9WNb7t+V1dXRw4cGDYKhRCDFkbffX19S+4XK5bM9ZGavhACIYQQmRlZX3CarU+fKxV0dfXx549eyguLqaioiLjpziGnc1u7np2D3WuQQTw4dlO1iwpRqce3Yc64vcQ6OvEXDTtpMfEpeQbz+2hxR3g/itnc9PysnHPNxqNcvDgQQYGBpg/fz5GoxEpJY899ljovvvucyWtjfXjHiAD8AEQDCGE0eFwPLty5cplv/rVr6w2m41YLHbcmysra6ROfh9MAuEY//PyIZ7Y2EBcQr5Fxy2rKpjhNJ/+5GPwdjSgybKgNWef8ritDX089Oph7CYtb319NXrN+KyMIdxu9/CXQHl5OUIImpqaWLNmTd/Ro0f/7HK5/iOTYj5+3tcePSFEud1u3/XjH/949TPPPGO12Wx4PB42btyITqdj+fLlGbE4hk1He7nkkXX8ZkMipeGj8/L5wTXzxiwWUkoivn40xtOnyS8us1Gem4XLG+KpTU3jmvex2Gw2zjvvPPx+P5s2bSIQCFBaWsrbb7+d/cUvfvEmu92+XgiRWXeOk/ethaHRaFbb7fann3/+efuSJUuQUtLY2EhzczM1NTUcuw39g85gKMoPXjzAU5uaASi26fnC+ZVU5hnHdb1IYBB/TxuW4hPLD47ErhY3P3zpENlZGtbdtRrjaZypo6W7u5va2lpmzpw5XCf1L3/5S/RLX/pSm8vl+oiU8lBKBvoA8b4UjOzs7K8WFRXds3bt2uz8/HwikQi7d+9GrVYzZ86ccde+PJOIRqP4/X58Ph8+n49wOEwkEiEcDhMOh4lGo5zqfyuEQK1Ws79P8vgOL93+GEoBH52dw5XzC9Dq9IhxhpQHuxpR6YzoLLmjOl5Kyb1/38fhrkHu/PA0br2welzjjkQoFGLnzp2YTCZmzpyJQqFg7969XHHFFT3d3d2f8fv9/0zZYB8A3leCIYRQ2+32361cufKKp556yqLT6fB4POzYsYOqqiqKioqmeopjRkqJ1+vF7XbT39+P1+slGo2iUCjIysoavmm1WtRqNRqNBrVajVqtPqUT1+0Lcf/f9/GXXYmuAGU2LZ9dlEOBIU4sFCQWCYKUCKUalc6AWm9EpTeh1Jy6tqiUEnf9LmwV8xCK0Qvz/vYB7v/nAUw6FRvuuhCLIXWb+aSU1NXV0d3dzaJFi9DpdPT09HDppZe6GxsbH+rp6XkgswN2dLxvBEMIkWu329fecccdM+6++26DEIKOjg4OHTrEwoULz5olSDQapaenh97eXvr7+4lEIhiNRmw2GzabDZPJNOGdsWv3dfJff62l2xtCrRRct6iYy+fmn5CiLaVExqJEgz4iAS/RwCCxcACFSotKb0STZUGdZT4ubBoN+vC5mrGUzBzzvB74535q2z3curqKOz8yuuXMWBhaoixYsACbzUYkEuGWW27x/Otf/3rD5XKtkVIGUz7o+4z3hWAIIeY6HI4Xn3jiCedll12mlFJy+PBh3G43ixYtOqO3nkspGRwcxOVy0dXVRSQSITc3l9zcXKxWa0rL+fUOhvjOC/v4x56EVTHdYeKWVRUUWPVjuk4sEiLi9xLx9RPxe1Bq9GiMNjQmG0F3F0qNHp01b8zzO9zl5Tsv7MOgUbL+rtXkGFNfytDn87F9+3bKy8spLk4ki/30pz8N3n///Ue7u7svzjRiOjVnvWBoNJrVhYWFf37xxRdzZ8yYQSwWY9euXWi1WmbPnn3G5lZ4PB5aW1txuVzo9XocDgcOh4Oh4jypRErJC7vbufeFfbj9EbQqBWuWlPDh2Q4UE3x9pJTEQgHCg25CXjcRvwdDbiF6mxOlZuwf+B+9dJCdLf38+8pyvn35rAnN7WREo1F27NiB2Wxm+vTpCCF444034p/4xCc6u7q6VkspD6dl4PcBZ7Vg6HS6S0pKSp5at25djtPpJBwOs3XrVgoKCigvL5/q6Z1AMBikra1tuN5ncXExDocjrU7YLk+Qbz9fy6sHEuXy5hSY+feVFdjNupSPFQ0F8HbUozPnEhxIFNLRWe1ozTkolKOLfDT0+PjW83vRqhSsu2s1jjTMExJCV1tbSzgcpqamZtgZeskll3S2t7dfLKXcl5aBz3LOWsEwGo1XFRcX/3b9+vXZubm5BAIBtmzZMry79ExhqATd0aNHCYfDFBYWUlhYmPbK4VJKntnWyv3/3I83WS7vxnNKWT09fVv0fd0tKFQa9DYHALFwkGB/NyFPDypdFvqcAtT604dqH371MFsa+rh5eSnfvXJOWuY6RH19PV1dXSxduhSVSsXBgwe5+OKLXW1tbR+RUu5K6+BnIWelYJjN5htKS0t/sW7dumybzcbg4CDbtm1j3rx5ZGefOrNwsojH47S1tdHQ0IDRaKSyspKhEn/ppqXPz7ee38v6uh4AFpZY+dyK8rT4BI6lr3431tJZKFTH+4wSiVwD+HvbkfE4htwCNEbbSYWr1e3nrmf3oFIK3rjzAopshrTOu7W1lYaGBpYtW4ZGo6G+vp7Vq1d3t7S0XCGl3JLWwc8yzjrBMJlM11dWVj6+bt06m9lsZmBggB07drBw4cJJ+0CeikgkQkNDA21tbTidTsrLy4fLy6WbeFzy1OYmfvDiQfzhGEatik+fW8aKypy0+3Ji4SDe9iNYy05tEURDAQK9bUT8XvTZ+eis9hHzPX7+xhE2HOnh44uL+NF189M17WG6uro4ePAgy5YtQ6fT0dTUxKpVq7qbm5svlVJuT/sEzhJGJRhCiG8DnwRiQBz4gpRyc1omJMSbwJ1Sym3vfcxgMFxRUVHxh40bN2ZbLJZhsViyZAlG4/iyElNFLBYbziQtLS2lpKRkuN/GZHC0e5BvPLeXLY2JcnnLyrP5zLllx5XLSyf+njaEQok+e3TLwXg0QqCvg5CnF0NuIVrL8UulzoEg//nMLoQQvHLHKirGmXU6Fnp6eqitreWcc85Bp9PR0NDAqlWrultbWy+WUu5J+wTOAk6byieEWA5cASyUUs4DLgZa0j2x96LX6z9cUlLy+3Xr1p1RYiGlpLm5mXXr1hGPx1m5ciUVFRWTJhbRWJzH36rn0kfWs6WxD4tezR0XT+P2i6dNmlgAhDy9p91odiwKlZosewnWsjlEAoO4j+4m5O0bzk51WnScP81OLC555LW6dE37OHJzc5kzZw6bNm0iGAxSXl7O66+/nldQUPCyEGLsiSXvQ0aT+5sP9EgpQwBSyh4pZbsQolEI8UMhxJbkrQpACJEnhHhOCLE1eVuRvD9LCPFE8r6dQogrk/frhRBPCyH2CCH+BJwQV9RqtauKior+uH79+pzs7Ozh7M2pFguXy8W6desYHBxkxYoVVFdXT6pVcajTy7W/fJvvv3iQUDTOyupcHrxuPkvLJ9ePE4uEQAgUqrELlEKlxpRfgaV4BqGBHvoba4kEEmU5r1lYiEoheGF3O4c6J6fl6rGiEQqFqK6u5pVXXnHk5+e/NvQe/yBz2iWJEMIIbAAMwKvAn6SUbwkhGoFfSykfEELcDHxcSnmFEOKPwC+klBuEECXAWinlTCHEfwP7pZRPCSGswBagBvgCMEdK+TkhxDxgB3DO0JJECFFZVFT09pYtW+z5+fn4fD62bNnC4sWLMZlMaXlRTkcwGKS2thYpJXPmzElL7sSpCEfj/PLNen72Rh2RmCQ7S8O/ryxnQfHUbML097YDYMgpmPC1okEf3vZ6VHoTWfYS/rCpmZf3d3HJbCeP3bRowtcfLd3d3Rw4cIDly5ejVqvZuXMnl1xySaPL5VogpRyYtImcYYzWh6EEVgKrSXzAvwHcC1wopTwqhFADnVLKHCGEC2g/5vQ8YAbwBqADhmoRZAMfAb4PPCqlfD051g7gFinlNiGE2W6373rxxRfLFy5cSDAYZNOmTSxYsGBKOoxJKWlqaqKhoeG4HZCTyd7WAb7+7G4OJr9xL5ph55PLSjBoJs+yeS/uhr2Yi6ahVKcmCiOlJOjuItDXQcRUyF3/bCQci/P3W89jbtHkObbb29uHoycqlYpnnnkm+pWvfGVLd3f3KillbNImcgYxqndZ8sV5E3hTCLEX+PTQQ8celvypAJZLKQPHXiPZ7fza924pTjq6TlAtIYQyLy/vH4888kjRwoULiUQibNmyhTlz5kyJWHi9Xnbv3o3NZmPlypWTuvQACEZiPPJaHb9ad5RYXGI3abllVQWzC6Y2MhSPRkDKlIkFJN4T+mwnWnM23o4Gzi9W8UpjmP955RC//+zSlI1zOgoKCohGo2zfvp2lS5dy/fXXq3bt2jXvN7/5zc+AL03aRM4gRuP0nC6EOHa/8QJgqNLJDcf8fCf5+8vArcecvyD561rgP5LCgRCiJnn/OuBTyfvmAPMA8vLyHv7MZz5Ts2bNGnU8Hmfbtm1UVlaSmzu6LdOpYsiq2L59O3PmzGH27NmTLhbbm/q47NH1/PLNeuJxyWVznPzw2nlTLhYwdmfnWFCoNFiKp/OxmmK0SnjzUDfbklGgyaKkpASr1crevXuRUnL//fcba2pq1lgsls9N6kTOEEbjw1gE/BSwklhOHAFuAbYBvwMuIyE8n5BSHhFC5AI/B2aSsGDWSSm/KITQAz8BzgUE0Jj0eeiT15kF7AKqdDrdS+edd97ta9eutQkh2L17N1lZWVRXp65OwmgYqqOhUqmYM2fOpAuFPxzlx2sP8fu3G5ESCqw6vrCqkmmOqfHdjER/4z5MBZUoNenNNfnzlkae393JPIeOv3519aS2f5BSsnPnTiwWC5WVlfh8PhYtWtR76NChy9OVXnCmMu7EraTTc7GUsielExJicXV19Uvbt2/PMZlM1NfX4/V6mT9//qRuJBsqEFxdXU1h4ega7aSSt4/0cPdf9tDSF0Ah4GPzC7i6pgiN6sypqhiPRelv3Ed2ZfoTq3yhKF99eie+cIxvLDNw44cmN0IWj8d55513qKqqwuFw0NTUxPLlyzs7OjoWSynbJm0iU8yZ8+4DhBD5TqfzhbVr1+aYTCa6u7vp6Ohg3rx5kyoWDQ0N7Nu3j6VLl066WHiCEb75l7188jebaekLUJpt4HtXzeWGJSVnlFhAepcj7yVLq+KKeYkozL9alGzdupWurq5JGRtAoVCwePFiDhw4wODgIKWlpTz99NOOvLy8V5JW8geCcb8DpZRlqbQuhBC6vLy8V/74xz86ysvL8fl81NbWsnjx4kkzP+PxOHv27KGvr49zzz0XgyG9exjey+sHu/jwQ+v4vy3NKBWC6xcV8b2r51Cee2YWKk4IxuT5lC6Z48SsU7Gn3UskbxpHjhyhvr7+lKUIU4lWq6WmpoZt27YRiURYtWqVuO+++8rtdvufxWR+o00hZ8xXltPp/MU3vvGNytWrVytisRg7duxgwYIFk7YPIxKJsHnzZnQ6HQsXLpzUup9uX5iv/WkXn/v9Njo9QSrzsvj+1XO5ZmERqjO0VWM8FiUeDaPSTt6Xq06tHO7D+sjrR1m27Bw8Hg+7d+8mHo9PyhwsFgtVVVXs3r0bKSVf+tKXdJdeeukqi8XylUmZwBRzRmw+UyqVK2tqatY+8cQT+tmzZ7Nv3z6ysrKorKyclPF9Ph/btm2jurqagoKJJx+NhRf3dvBff6uldzCMWin4+OJiLpuTj+I0Hc2HkFISj4aJhYPEwgHi0QgyFiUejRKPRZAjfJAUSiVCqUKhVCd+qjSotDqUGj1CqRrV8i/Y30005MfoKB3zc54I4Wic2/+0E7c/wi8/tZBL5jipr6/H5XKxePHiSWtxuWvXLiwWC0PW8OzZs3uampoWSykn3ivhDGbKBUMIkeVwOA5s2rSpOB6Pc/ToUQwGA8uXL58Uv4XH42H79u3U1NRMan5HtzfEPX+r5cXaTgBmOBPl8vItJ//GlvE40ZCfiN9LNOAlGvQDEoVag1KjR6nRoVBpUChVSUFQjViIV8ZjxGNRZCySsBQixwsOQoFKl4XaYEKtN6HU6k/4Xww0HyDLXoJKN/nLpVf2d/LExkaq7UZeun0VSoWgs7OTQ4cODe82TTexWIyNGzcyb948rFYr69atk9dff/12l8u19P1cUHjq0gOT2O32n95zzz32srIyAoEAR48eJRQK0dzcTElJSVpFo7+/n507d05qmrmUkr/uauO+F/bTH4igUyv4xNISLp55Yrm8RPk7/3D5OxmLDn+Q9TkFqHSGk/ZoQJQDAAAgAElEQVQtPTVqTrXgkvFYovCv34uvu5lYyI9CrUNrsqEx2lCo1MTCQZTayfXxDLF6up0XdrdT5xrk77vbuaqmEKfTiVKpZNOmTSxbtizt6fpKpZKFCxeybds2zjvvPFatWiWuuuqqaX/+85//A3g0rYNPIVNqYahUqlVLlix5/u23384GeOedd5g2bRpWq5Xa2lqi0Sjz589PSxHfobDpkiVLJq37WcdAgG/9ZS9vHEqUr5tXaOHzKyvIM72bJSmlJBoYJNjvIuIfSBTYTX5QU5lNOVaiybqdYa+baMiPQqXBXFSNaopE481DLh5fd5SyHAOvfO181MqEcPb29rJ3716WLl06KU7rhoYGvF4v8+bNw+/3M2vWrJ6mpqYlUsrGtA8+BUyZYAwtRTZv3lxcWlpKfX09wWCQ2bNnDx/T1tZGXV1dyitpTfabSkrJ/21p4b//dYDBUJQsTaJc3vnT3q0BkShn5yLk6UWpNaCz2tEYLeO0INJLf/NB1HojEb+HeDSCzpqHzpJ3QqWtdBKLS77+7G46BoL88NpE2HkIt9vN7t27Wbx4cdpzNaSUbN68mYqKCux2O+vXr5fXXXfdDpfLteT9uDSZsnej3W7/+b333msvLS1lcHCQlpYWZsyYcdwxhYWFLF26lP3793P48OGUhM/cbjd79+5l2bJlkyIWzb1+PvWbzXzr+b0MhqIsLrXxo+vmc8F0OwBhn4eB5gN42upQqLVYy+dhKZ6O1mQ7I8VCxuPEwwEMuYVYS2dhLU1U9u5v2oenrS7pV0k/SoXgukWJxlSPvnaEUPTdvWA2m42amhq2bt1KIBA42SVSghCCBQsWsG/fPiKRCCtXrhRXX311tdVqvS2tA08RU2JhqFSq85ctW/aXDRs2ZAO8/fbbzJw586RWRDwe59ChQ7jdbmpqasa9Ph0cHGTr1q0sXbo07cuQWFzyh7cb+fHaQwQiMUw6FZ89t4xzKnKARA5DoLcdhVqLIbcAtf7MSfc+FSFvH+HBfkz5FcfdP9SA2d+T3OqeWziqZswTIS4l33huDy3uAPd9bDafPrfsuMd7e3upra1l+fLlaY+eNDc343a7mT9/Pn6/n9mzZ/c0Nja+75Ymky4YQ0uRLVu2FJeUlNDY2IjX62Xu3LmnPXek5rqjZWhrfE1NTdprfx5xDXL3c3vY3uQGYHllDp9ZXoZJpyI86MbnakFtMGHIKRxX746pxNN6GH22E7Xh5J3kokEfvu5WZCxClqM0rWK4tbGPh145TJ5Jy7qvr0avOd6d29HRwdGjRznnnHPSmlsjpWTTpk1UV1eTm5vLhg0b5LXXXrszuTSZnCSRSWDSbd7c3Nz7vvWtb9lLSkoIhULDtSVGQ15eHueeey5NTU3s3buXWGx0JQmGtsbPnj07rWIRjcX5xZtHuOzR9WxvcmM1qPnPD03jtgur0csA/Y21hAZ6sBRPx5RfcdaJhZRxIoFBVKcRAJUuC0vxdLIcZfi6mhloPkA0lJ6lweJSG+W5WXR7Qzy5qfGEx/Pz8yksLGT79u1pzQgVQjB//nz27dtHPB7nvPPOE1dccUWlXq9fk7ZBp4BJtTCEEI7S0tK9dXV1eUNVjBwOx5iTpaSUNDQ00NraSk1NzSlDokPKX1JSktZ9IQc6PNz17B72tiWKMV0wLY9PnVOKQQWDnY3EI0GMzvIpyVtIFeFBNyFPH6aCsSXUhX0DDHY2ojXZMOQWjbsr/MnY1dLPD186iM2gZv3dF2LUnpgtcOjQIUKhEPPmzUvp2CONo1QqqaqqwuVyMXfu3FaXy1UhpYykdeBJYlItDIfD8aPvf//72Wq1mr6+PoLBIPn5+WO+jhCCiooK5s+fz44dO2hqajrpt8eBAwfIzs5Om1iEo3EefuUwH/3pBva2DZBr1PDNS2dwy6oKVAE3/Q170GRZsJTOPqvFAiA40IvWnDPm8zRZlmQ3dwXuo7sJD/andF7ziyxMd5hw+yP8bkPDiMdMmzaNcDhMS0t661dXVVXR2tpKIBDAbrfzuc99zmY2m7+c1kEnkUmzMIQQFTNmzNi8b9++XCEEGzZsoKamZsJhr2g0Sm1tLZFIhAULFhyXs9HR0UFTUxPLli1LSwLY7pZ+7np2D4e6EuXyPjzLwZolJWgV8UTUQ6XG6CwfdZvAMxkpJX1HdpJdVTOh1zIWDuLtqEep1mF0lo2YiToe9nd4uP8f+zHpVGy460IshhNDvNFolI0bN7JgwYK0Lk27urpoa2tj4cKFeDwepk+f3tXZ2VkppfSlbdBJYtIsDKfT+dNHHnkkR6FQ0NbWhsViSUmMXKVSsWDBAgoLC9m4cSN9fYmKTIODgxw6dIiFCxemXCyCkRjf/9cBrv7FRg51eXGaddxzxSw+u6IcZdhLf+Ne9DYn5sLq94VYAET8HtQG04RfS6VGh6VkFiqdAXfDXqLB1HyGZuWbmVNowRuM8qv19SMeo1KpWLhwITt37iQcDqdk3JGw2+0Eg0H6+/sxm83ceeedltzc3G+mbcBJZFIsDCHE/KVLl762efPmnFgsxrp16zj33HNT3l/U7/ezY8cOcnJycLlcafkm2drYx13P7qGhx4dCwGVz87luUREapQJfVxORwCDmouopzcpMB96OejTGbLSm1FUmjwZ9eNrq0Nsc6GzOCYtRXZeXe17Yh0GjZN1dq8k9SWvI9vZ2WlpaWLp0adq2HgwMDLBv3z6WL19OOBymqqqqu7W1daaUsjctA04Sk2JhOByOx37+85/nQCKVNl3NiA0GA+eeey5dXV1Eo9GUxt59oSjf+VstH3/8HRp6fBTZ9Nz3sTl8alkpaiEZaNqPUCiwls1+34nFUG9UjTG14qvSZWErn0vE78XbXs9Eo4/VDhMLS6z4wzEee3NkKwMSxX2NRiP19Sc/ZqJYLBZ0Oh0ulwutVsv3vvc9q91u/2+AZH8elxCiduh4IUS2EOIVIURd8qcteb8QQjwqhDiS7N2zMG2THgVpFwwhxPk1NTXTFi9eTDQapaWlhYqKitOfOE66u7sxGAzMmzePTZs20dHRMeFrbqjr4SM/Wccf3mlCIQTX1BTy31fPpcpuJBYO0t9Yi87mIMue3s1yU0U04EWlM6Yl81QolJgKq1FqdPQ37icei57+pFNw3aJiAJ7c1ETnQPCkx82YMYO2tja83vQ1SJo+ffpwhvKNN96otlgs1yR79fweuOQ9h38DeE1KWQ28lvwb4FKgOnm7Bfhl2iY8CtIqGEII4XA4fvnII49kQ8K6SGfP0XA4zP79+5k3bx55eXmsWLGC5uZm9uzZM+qcjWMZCES4+9k93PjbzbS6A5TlGHjgqjlcv7gYtVJBxJ9I6zYVVKGzTG4188kkUVlr7NGR0SKEICuvCENOPv0NeyeUs1Gem8Wy8mxC0Tg/f+PISY9TKpXMnz+fXbt2pa34TlZWFiaTia6uLpRKJQ899FC20+n8iZRyHfDe8udXAn9I/v4H4Kpj7v9fmWATYBVCjD20mCLSKhgKheLyiy66KH/atGlEo1FaW1spKytL23h79+5l2rRpw/UQNBoNS5cuxWQysWHDBjwez6iv9er+Lj788Fv8aVsLKoXghiXF3H/VHEpzEqHR8GA/3vajWEpnodZPbSPodCKlJDzYj8aY/q5qWnMOpsJqPC0HiYbGvyfl+kXFKAQ8vbWZlr6TX8dqtZKXl8eRIycXlokybdq0YSvj8ssvVzgcjpXvadsxhENK2QGQ/GlP3l/I8b2MW5P3TQlpFQyHw3H/vffeawVoamqipKQkbem5HR0dxOPxE/IthBCUl5dTU1PDzp07aWxsPGXGX58vzFef3snn/3cbXZ4Q1XYjP7hmHlctKBwulxfyuhnsasRaNut95694L9GgL1FAZ5JKBar1RsxF0/C0HBp3BKXQpmdFZS6RmOTR0zRynjZtGp2dnWP6MhkLBoMBs9lMd3c3Qgi++93v5jidzv83hkuMtMadsl2waXsXCCHmVlZWFlVXVxOPx2lubqa0ND3l3KLRKAcPHjxlFp/ZbGbFihUMDAywbds2wuEwf93ZxoofvE75N/7Jih+8xnf+VsuHHnqLv+1qR6NUcNM5pdz70dkU2t7d7Bby9OJzNWMtnT2u5sNnG5Nd6BcSzlBz8Qw8rYeHGzOPlWsXFaEQ8NyOVo52n/waCoWC+fPns2fPnrSljldVVVFXlxCuK664Qmg0mkuA96Yndw0tNZI/Xcn7W4HiY44r4vhWpJNK2gQjPz//nnvuuScXoLW1FafTmTbfRV1dHWVlZaeNvKhUKubPn09hYSEPPvsW33huD239ASTQ1h/kD+800esLMyvfzI+um8dlc4+vrRn2DeDrbsVaNntSaz9MFVJKwt6+lIZSR4tKq8dcPANvW924fBoOs44LptuJS/jJq6e2MiwWC2azmba29LQXMRqNDGU3KxQKbrvtNrPRaLzxPYe9wLstSD8N/O2Y+29ORkvOAQaGli5TQVoEQwiRq9PpLrj44ouH932Ul5enYyh8Ph8ul2tM1ktBQQF/bxIEoyc6u4xaJd++fCYO8/F1IaNBH4MdR7GUzDxjk7GGSusFB3rw97bjczXj7TiKt/3Iu7eOo/hcLfh7Owh5+oiG/CMWCgaIhfwoNbqUZWOOFZVWP+zTiEfHnmh1dU0hKoXg73vaOdh56iXHjBkzqKurIxqdWJTmZFRVVXH06FEA3nnnHa3P57sTmC6EaBVC/BvwA+BDQog64EPJvwH+BRwl0XHw18CUppmnRTCys7O/8p//+Z9mIQR9fX0Yjca0FWbdt28fs2bNGnPvks6B0Ij3+0KxE2prxsJBPK2HMRfPQKk+M5YhUkoigUH8PW0MtByk78hO+htr8fe0EQv5EYpEIV+tOQed1TF805qyh4v6RgJefK5m3A176DuyE0/rYQJ9HcPf6OmOjowGtd6I0VlOf9OBMYdcc41aLprpQEp4+JXDpzxWo9FQWlo6vHR4Lw8//DCzZ89mzpw5fOITnyAYDA53dq+uruaGG244ZfaozWbD7/cTDAZ59tln+fznP+9VKBTXSCmLpJS/lVL2SikvklJWJ3/2ASSjI1+RUlZKKedKKbeN6UVIMSkXDCGEUKvVn7/55ps1AEePHk1b3kVPT6KPUl5e3pjPLbCOXIQnx3i8IMh4jIGWg5gKqia1B8dIJCIWbjxtdfQd2Ym/pxWhUJKVV4ytcgG2ivmYi6aRZS9Bb3OiNeegybIkqn8nbxqjFZ0lF322E6OjFEvxDLKT5+pz8pFSMth5NHH93g6ESjNpjYJOhsZoxZBTgKd17FXXrlpQgEapYO2+Lva0nnrTW1lZGS6XC7//+MhKW1sbjz76KNu2baO2tpZYLMbTTz/N3XffzR133EFdXR02m43f/va3J722EIKysjIaGxsBuP322y1Op/OsSxdPh4VxwerVqw0mk4lgMEgwGMRmS/0aWErJgQMHjqsBOha+/pHp6NXHm9oaBVxZpUHGY8NjeNqOoM/OR22YuopYsXCQwc5G+o7sJOTpRWe1k11Vg6V4BvpsJypd1oQTxoRCgVpvwpBTgLV0NqbCaSg1WoLuLtz1u/B1tyZaEEwROmseKq0ef3frmM6zGjR8ZLYDgP95+dRWhkKhYObMmRw4cOCEx6LRKIFAgGg0it/vJz8/n9dff53rrrsOgE9/+tP89a9/PeX1CwsLh6N5s2bNIicnp0oIMWUh0vGQcsEoKCj45h133JEN0NLSQnFx8elOGRculwuj0TjuUntX1RTy/Wvm4rS8u1T6zIpyVlTmDG+KCvR1IBRK9DZHqqY9JiKBQQZaDuJpPYxKn0V25QJMBVVosixpzygND7rRZ+djKZ6OtXwuCqWS/sZavO31xMInz6BMJ1mOMsK+fkJe95jO++j8AvRqJW8d7mZr43vzpY4nLy+PQCCAz/duSLewsJA777yTkpIS8vPzsVgsLFq0CKvVOuzILyoqOq3TVKlUkpubi8uVCIDcfvvttpycnFvH9GSmmJQKhhAi12AwLFiyZAlSStra2tJSh0JKSV1dHdOmTZvQda6qKWTTNy9iflFij4TFoEGfnY+5sJqBloMEetsxOtPjrD0V0VCAgeaD+LqaMOQUYKuYh86SN2m5EABhby9aU6LGqkKpQp+dj61yARqjlYGWQ3jb68fliJwIQggsxdPxdTUSi4zsgxoJk07NpXMTJR0fXHvolMsaIQTV1dUcPvyuNeJ2u/nb3/5GQ0MD7e3t+Hw+XnzxxRHPPR2lpaU0NSWao91www0qlUr1aXEmVns+CSmdqMlkuvHLX/6yZcjZaTab09JTpKenB71en7JCvucnK3jvbkmscZUaHUIoUOlNeNsOT5opLuMxBjsb8LbVoc92Yi2bfcramekiFg4iFMoTQsdCCLTmHGwV81Bnmelv3Ie/p21SfRwKlQajsxxv25ExjXvZnHyytEo2N/Txdv2pN4za7Xa8Xu+wL+PVV1+lvLycvLw81Go111xzDW+//Tb9/f3DUZXW1tZRVY4zm82Ew2GCwSBZWVl86EMf0gEXjPqJTDGpFoybr7vuOg0kXsB0LUcOHz48YeviWC6YnnCa7mrpTzj9uprQ2ZxYiqejs+bR31hL2DeQsvFGIuTtw310D0qNHmv53LRX3D7lXE4THRFCoLPkYauYTzwWxX10z7gTrMaDxmhFqdERdHeN+pwsrYor5iU+0A++PDorYyhiUlJSwqZNm/D7/Ugpee2115g1axarV6/m2WefBeAPf/gDV1555ajmUlhYSHt7IvfqpptusuXn53/6NKecMaRMMIQQ5qysrKLi4mLi8Th9fX3k5qY+Q7Cvrw+NRpPS1obzi6zYDGpc3hAtnd3EQn702QkTVmvOxVIyC5+rmcGuk5cCHC8yHsfbUU+grxNL6Wz02ROvCzFRRhtOFQoFRkcp5sJqBjvq8fe0Tpq1YXSWEejrGJM/5ZLZTsx6NTub+3n9oOuUxzqdTvr7+wkGgyxbtozrrruOhQsXMnfuXOLxOLfccgs//OEPeeihh6iqqqK3t5d/+7d/G9U8CgoKhgXj/PPPJx6PXyym+p8+SlIpGB+59tprDZBYMuTk5KTljd/Q0JDyru5KhWBldcLK2HqwCVNB1XFzV2q0WMvmIISgv7E2ZU6/WDiIu2EvSo0eS8nMMyLHIxYJgxBjSntX6QxYy+YSj0YYaJr4FvXRIBRKjPkVyToaoxMpnVrJlfMTVsb/vHyYePzUVkZZWRnNzc0A3HfffRw8eJDa2lqefPJJtFotFRUVbNmyhSNHjvDMM8+MusaLTqdDoVDg9/vRarXMmzdPDYwv3DfJpEwwCgoKPnvddddlAWlzdoZCIQYHB9MSph1alhzwqFBqTkwyE0KQZS8hy17CQPMBggM9ExpvqOOZKb8CQ07BlFsVQ4w3WUsoFBid5eiznfQ31KatrcCxaLIsKFRqwoMjR028ngG+9ZXPsubD5/CJjyxn746tLCvQoAh52d/h4dwbvozbffKIS2FhIW1t6fHRHGtl3HjjjdnZ2dkfT/kgaSAlgiGEUEkpFy1cuBApJW63O6W9UIcYCtOm48O1rCThXDzcGz6u7d570WRZsJbPJTTQjaftyHDOxlgIDvQw2NmQ2Bo/hfkdIxHy9EwouzOxRb0KT8tBIv707AA9lixHKb6uphHT239y/7c4Z9WFPP3yJv73729RVjWNp3/zU2aqE2Ifqr6Y//7BD044bwiVSkV2dvZwGDSVOJ1OuroSPpjLL79cqdVqb0j5IGkgVRbGuatXr1YJIXC73dhstpR/qKWUaXWkulrqmWk3EIlJ9ref+o2uUKowF89ArTeOuZBtwO0i0NdxRpbyi0cjIOWE56XWG7GUzMTbXp92Z7FSrUVrziXQd/wGTp/Xy66t7/DRjyf2eKk1GkxmC+tffZHPX3kBeUYt7riO57efuu3AsdmZqUSn0xGPxwmHw+Tk5JCbm2sTQkxNws8YSIlgOByOGz/5yU9mA3R2do65jeFo6OnpwWKxpCVM6/F48Pv9XDwnsb7d1XL6vhlCCPTZTsyF0/C01eHv7Tit6RpwdxEacGEtnXVGbmBLLEdSYxkqNTospbMY7GxIu2gYcgsJ9ruO8520tTRizc7hgbv/g09/dDXf/+ZXCfh99PV043Tmc+2ixJI5VH0xkdjJK25ZLBYikUhamjo7HA46OzsB+OQnP2nSarUfS/kgKSZVS5JLL7zwQiBRU3M8eztOR0tLS9rqadTV1TF9+vThjuq7T7Pn4FhUOgO28rnEQn4Gmg+cNGcj5O0j6O7CUjJzynZ/no5U175QqrVYSmYx2HE0Ze0ERkIoFOhs+QR63931HYtFObxvD1d/8rP84e9voDNk8eTjjw4/fl5VHgUWHUqLg2e3nzrdvLi4mNbWsaWkjwaHw0F3dzcAV199tS43N/czKR8kxUxYMIQQ02fMmKHV6XSEQiFUKlXK617E43EGBgbS4uwcHBwkEAiQk5PDgmIrVoOaLk+IjoHRf6MIhRJTQSV6m2PEnI2IP7Er9EwWi3gsSjwWHdHhOxGUag3m4ul4Wg+PKTtzrOhtDkKebuLJ2q12ZwF5zgJmL1gEwOpLPsqhfbvJzs2jx9WJUiH4cHXCf/Toa3UEIyf3RTmdzmFLIJWYzWY8Hg9SSqZPn45KpaoWQkztDsfTMGHBsFgs1wwtR7q7u9OSe5HOMO1QirkQ4rjw6u5RLEvei9acg6X0+JyNeDSMt/0IluIZZ3TRnZCnbzgVPNWotAaM+RV4Wg6dtPbGRBEKBTqrg6A7YWXk5Dlw5BfSdDSRfLXt7XWUV03nvIsu4V9/+RMAnZv/gSHqpWMgyNNbmk96ba1Wi0KhSPmyRAiByWQaLg94+eWXazjDsz4nLBhms/lDK1euVEL6liPt7e1jbtg8GoLBIF6v97g5XzDt3azP8aBUD+VsKHAf3cNA8wGyHGUp/+ZONSFPD1pL+mpfaLIsaC25DHYeTdsY+mwnAbdr2Jd0xz3f576vfZGbLl9F3YFabv7SHdz0ha+ydeObfPyiJWzb+CafXjUdgJ+9UU8gfHIr49gwaCrJy8sbXpZcdNFFltzc3AtTPkgKmfDaIRKJTB9K0x4YGMBqTW1K81CYdv78+Sm9LjBcZ/RYy2VVUjD2d3gIR+NoVGPX1ETORjGxSIiQp3dcodfJJB6LEo+GUWkNaR1Hn52Pp+VQMnQ7siUai8X43FUXk+d08uCv/4/2libuuf3f8fS7mT57Hvc8+EvUJ2lQJRRKNEZroqygOYdps+byxF9fO+G4nz75/PDvUkrWHh7gaI+P/32nkS+cP3JSYH5+Ptu2bUt50mBOTg779+8HYNGiRWi12pUpHSDFTMjCEEJYc3NzVQqFglAohFqtHnPlq9PR29ubtjDtSAlmeSYtcwstifBqx/i9+9Ggj2jQR3Z1DaGBHjxtdWescIQH3ZPSRkAIgamgEp+r+aTO4T///nHKqt6twv+LH32XGz77Rf782lZMFit/f+apU46hz3YS6Bu9v0EIwccXJ0L1j71Vjzc48ryGKsYFg6nd2p+VlYXP50NKSUlJCfF4PD2e/RQx0U/3wnPPPVcNiT0e6XBK9vT0YLfbT3/gGHG5XOTk5IzooH13M9r4BGOo8I65sAqlKuH0U+tNuBv2TuomrdESGuidtEZMCpWaLHsp3o4T2xS6Otp5+81XhnMnpJRs37Se1Zckoo2XXr2Gda+cuK38WFRaA1LGx5S+P6/IwnSHCbc/whMbGk96XF5eHr29qW2NKoTAYDDg8/kQQlBYWKiYykZFp2NCgmGxWM4977zzrAD9/f1pE4ycnNSvrU/V9mBIMMbj+AQIurvQZFlQ6RLb74/N2fC21+PvbU/rJq0hZ2vYN0DA3ZUoCNzdir+3g2C/i4jfM5yzIOMxYuEAyjQvR45Fa85BxuMnRJN+8r1v85W7v4MiWR5iwN2H0WQZFnW7s4DurtMXzNbbnATGsJNViESjKoDfrD9Kv3/kOh+5ubnDZSFTSXZ2Nv39iffaypUrdcCilA+SIiYkGGazefXixYsFpMd/EYvFiMViKW/cHI1G8fl8mM0j15pYUGzDolfT6Qmesj/nSMRjUQJ97Rjyik54bDhnIxw4Zc7GeJAyTsjTi6e1Dnf9TgZaDhPy9CBjUYRCgVKtQQhBPBom4HYx0LSfviM7GWg+iFIz+ZE8o7Ocwc53m0ptfH0ttpxcZsxZcMxzOlFUR7M01ZhshMdYlWtmvpm5hRa8oSi/WjeyY9ZqtZ5y78l4sVgsDAwkxHPFihXmnJycM9aPMSGn57EOz0AgkPLK4Ola5rhcLux2+0nffInwai7/2NPBrpZ+LrGMPnPV39OGPrvgpJmcQqHAlF9JyNNLf2MtRmf5hGpfxKMR/L1tybCoDX22A5W+alQfLBmP09+0D6TAXb8LndWe2F4/CbkiKq0etcFEaKAbndXOnu1b2PDaS7zz1quEQyF8g14eeeDbDHoHiEajqFQqXJ3t5NpP/79QKFUo1BqiIf+YHLkfX1zE3rYBfrexkc+dV06u8fgvKqVSiVqtJhgMpvS9brFYhmtvLFq0CJ1OtyplF08x47YwhBCWnJwctVKpHH4BU+2Y7O3tTUteR0dHx2nDtOPJ+ozHooS9fehsp/e5DOdsdLcmczbGlp8g43F8rhb6G2tRavRkVy3A6CxHbTCP6f8gYxEsJTOxls9DSklf/W4C7q5JqWthyC3C35NYnn3p6/+Pv23cy1/e2sl3f/IrFi0/j3sfepyFy87jjZdeAODF559m5cWXjuraWnMuoYGx+Ruq7CYWltgIRGL88s0TfSyQWJak2o+h1WoJh8NIKSktLSUWi5WldIAUMpElybDD0+v1prSgzRC9vb0p91/E43E8Hg8Wi+WUx52fDK/uax8gPELDo5EI9LYnC+CM7mVN5GzMRggF/Q2jryp/s5AAACAASURBVLMRCQzibtgDAmyV89HbHKMe81jCvn7UWVaEECiUSrLyirBVzCMaGGSgaV9aMzMhkQWqNpgIeU7+AfzyXffw9BO/5PoLlzDgdvPR6z81qmtrzdmEvKcu+DsS1y9OLCWf3NQ04nI0JycnLX6MoUzpYxyfqd+QlQLGLRhms/ncFStWWCE9giGlJBwOp9x/0d/fj9VqPe23cJ5Jy5xCczK8evpt2lJKggM96Kxj23A4lLNhdJYl62x0n/L44EA33vYjif4jecXjEoohRoqOKJQqTAWVGPKKGWjaT/j/s3fe4XGVZ9q/3znTu9qoN1uybFmuci+YNAg1CSRhSSE9sEuADZAsZZdNSAiEkHwLyX77pbIhVEOAYJPQE2JbtmXLlmRZ3eplmqb3Oee83x9HM0i2ymjmHFk4/K7LF2g0c94zmjnPed6n3E9w9vduGxvFtz7/CVx/6XZ8/uM78dz//hIA4PO4cduXrsVnP7IZt33pWvi8s3tp2txihF3TA5kbt+3CI79+BgBQXFaB3774Jp5/5xge+MXvoEzx+yBj5ELMZoFiPhU5OmytzEaM5fHzd84damQymeD3+xd0zFQwGAzJ4+7atUsNYKPoi4hA2t82k8m0afXq1QQQDIZerxfvrADR94kJFrLNuXjFdHHguYj5XVDqzWkreyu0RkFnwzcxa81GyDmKiMcOc0VdxkVWlFKwET/kmpkNvVJnSnabRn0z36kZOYNb7r4fz7x+GL964TW8+ORv0d/ThT/88lHUb78Ie98+hvrtF+EPv3x01vNICC6z0dCsz0kXhdaIeBqdsp+pL4WMAM8dG8awa/p5KRQKxONx0bdser0+aTDq6+uNOp1ujagLiETaBoNSWpKIAwSDQdENht/vnzWLkQlOpzN1g1GTepl42GVN6oCmi4yRw1hSA4XWAHff9JqN0MQY4iEfTKXizHaNB71QaOeeb5LYMoWcwzO697mWAtTUCRW4Or0B5ctXwGEbx4G3/oLLrxH0YC6/5jocePPPc56LUGyVeho0VRQ6U1qt9cVZGuysygXLUzz69rlehkajEb2AS6/XIxAQPu/J2SfilpSKRNoGg2XZvERBVSwWg3KWct108Xq9ohsMnucRjUah0aSWRlxfaoZRLYfVF4HNN/sXJNHpKUZpNSEEmqwCGEvfq9mI+CYQ9blgLKkRbTZJqspaMkYuiCDbBudsUR8fGUJP+ymsXlcPl9ORzGbkWgrgnph7z6/UZyEedIt+11ZojYiH0ts+XLuxBIyM4MUTIzjjmF5sZzQak2lQsdBqtcnmtqKiIjAMsyQrPtP+9snlcqVcLk9+yGJnSHw+n+gGIxAILMgTkjMy7E6hGS3qmxC901OuEmo24uEA/CPdMBQuE81YUEoRC/qg0M0d+E0gkytgLBFa1GfcKgUDuOfmL+O2f38AujRiWUQmA6PSgY2IWwUrYxgANK0O2XyjGhevyANPgf96a7qXkWhLFxO1Wp30WgoLC8FxnPjdliKQ1jeQECJXKpVyQLpYw1LZ5qTSvZpodhIdQkDZOLR5JfCNdCEWSK/y9GziIR8UWsOCjLxcrYUmuxAB2+C0x9l4HPfc/BVccvWncfGlVwJAUnMCAJx2K7Jy5t8Cqow5s8ZKMoFRasDF0mtL/9SGYshlBPtaxtAxJfBtMBiS2wexkMlkyZuv2WwGz/PnbzDNHKR7y7Lk5+dTQDqDwfM8GEbcAqJ0vJY9k3GM9jHfjOlVSinYaBiMBJPdoz4nZAoVdHmlMJWvFmo2rAMLrtk497jpKWups/LBRoLJ2AqlFD+6+zZUVK3A9V/7l+TzpmpO/PnF51KqnVDqTGkFKOdDrtalrfaVo1fho6uErNfP3nxvdKIUMQxAKAxjWRaEECik0KIUgXQNRmFpaakMEKT/xU598jwviVhOOgbDYlBjdZERMY6fdpdJwEVDokxPPxtKKUKOEejzywAINQvmitUgDLOgmo2ZjhsPeqBMcTsyFUII9PkVCNoFsZnWpqN47eW9aDp8AF+66mJ86aqL0fC3N6dpThw79Dd88cbb5j22TK4ApbzoHb1ytRZsJP0MzCfWF0HJyPBmuy2ZLVMoFIjFxJ8rq1KpEI0KtS86nU62FNW30g23F1ZUVKgAaQyGFMcEhPL1VAOeU7m4Jg+nx3xoHvFgXel0TzHh3otN1DcBhc48baAQIQS6vFIodWZ4hzqgzS2B2rwwwSI2HIBcrc8g/WsAQMFGgli3aRsaemcOaE7VnEj52BoD4uFAWsZsNuQq7YLa3c/GrFXi43UFeKVlDD99sxtPfHWLZDNkEgZDp9OhqKiIdnZ2FgKQTnEoDdL61jAMU1ReXq4DIElxlRTbnEyCsxfXzF6PwUZCya5UMYm4Z0/TKrQGoWbD74JvpDupY5kKmc4dAQBNVuGCukFTJZPtw2zI5MqMm/yuXFsIjYLB37sdaOwX4iyJ7YOYTPUwysvL5QCWXJt7WgYjOzu7qqioSAYA8XhcdOn/SCSSlicwF4kGpnTYMJleHfeem15lI0HRDQYXj4HyPORzxEWEmo0VUOhM8PSnNgyZUopYwJOxWI7SkIVYwCN6GjTT7cNMEJkMyDDmY1ArcPkawXgnBjlLEcdQKBRJI1ReXq4BsOQyJWkZDJVKVZGYPZLJhTgb0WhU9LqOdLcjwGR6dRZxYMpzos8YiQXcUKaQphVqNvJhLF0p1Gw45x7rx0aCYFSajNOzhBAoNHrR06CMSpt2RmNOCMnYuF2+phA6FYPGfhcO9jqhVCqT3oBYyOXypMEoKyvTqFSqczUSzjNpfXNkMplepxPuqvF4XHSDwXGc6BmSTLc5e2ao+qQ8D0iwn40HvQtqeZerNILORjwK71A7eHbmgJyYc0eUejNiAXGzGkTGgEowyFnGKGb9m6SKVinHVWuFG/4jb3RDJpOBW8BWMBXkcjnicWH7pNVqodVqxS91zpB0bzXJrI8UF7cUKVWO4zIybBcnu1ffS6/ybGxBU85TZaE6DkBCZ2MZNNmFwmyUGQYUx/xuqAzi6ItIEW9IxJfE3uoQhhEl+3Lp6gIYNQq0DHtwfDwKXuSRCXK5PGmEFAoFotFoHSGEEkJWAgAhpIIQ8rnE8wkh6wkhl6e7HiFkgBCyoDtIWgaDUipPXHyUUtGFfzmOk+SYmRghi1GN2kIhvdppFdKrPMeKPmuEUgpQmva2QWXIhqm8DiHnKALW/mTNBhsJgVGqRBPHyaQgai6EmIPIBoPIRJmHolYw+OR6wcv43ttWbPuvJiy/+8/495dPZXxsQDCYCSMkl8sRi8XWADgI4J8mn1IB4HNTXrIeQNoGIx3S9jASBkOKmgkpvBYxjNDZzWiU5zJqL58JynMZX9SMQglT+WoQRgFPfxvYaFiU7MhUpLiwJw+ccWHauYfMPPCZYOSs7lWOUjx5ZEgUozG12jMej4PjuBIAX8N7BuMhALsJIc2EkH8DcD+A6yZ/vo4QsoUQ0kAIOTn53xoAIIQwhJBHCCGnCCGthJBbpq5LCNEQQl4jhHxj3nNM871J7mFIYTAyPeY56VXKi9bfkYDyHIgI712o2SiBvqASnsF2BJ2jKQVSF4IU81LZSFBUrVMA4GJR0cSA/tY9s17JM0fnngKfCvF4PCkG/NZbb4FhGC+ltBuAixCyEcBdAA5QStdTSn8M4D4Az03+/ByATgAXUUo3TP7uR5OH/iaASgAbKKVrATw1ZVk9gH0AnqaU/nq+c8w4WrkYUm5LhY1lZhjUcox5I7D7IjARABA56EnFPaZMoYSMkYOPheHsbBTtuAnspxvEPSDl4eo5IW4wmfKIBTzwjZzbqr5QeEow0+fDUR779+/P7Ng8D0op9u/fD5/PB6VSmbi4ngVwPYBX5zmECcDvCSHVEL5Jif3yRwH8P0opCwCU0qlNO38C8DCl9CmkQLoGg00EZ6a6UWLBMIzoASUxjimkV3Px51NWNI94cHG5BpSKGykXK0AHCPNSg/YB6AuWIRZwQ6E1QWUUz8tw9Z5EdtUG0Y4HAO7+NphKa0SNDfnHzkBtzoNChKSD7PAR8DN83Rkiw5VXZhZOcDqdsFqtKCwsxDXXXAOWZY2EkAEAQtstMLewCPADAH+llH6KEFIB4G+Tj5PJ18/EIQCXEUKepilcyOn602wi/TM1UCMWDMOInrISKw02VYWLyGSgM317MkCM1CLlefjHzyDsHoe5Yg2UevNkN6h4WpTCd0uCEmlJtnk8IFKsqdg8c2r++q2lGR87EQ984YUX8OEPfxh5eXm/opRWUEpLAfQD4AFM7UPwn/WzCcDo5P9/ecrjbwC4iRAiBwBCyNS7xn0AJgD831TOMd32djZRYEJEKIo556QkyHGLZYQS9Rinx3yIUxkoJ+5+O9PUIhsNwd1/CoxSA1NZbfJOLZ/s0xAroMjFImCU4vf7UJ4T7eJOHlMkIzTsCmHUI1R3yiZtJUMIvrCtDD/8ZOaKepRSEELwzDPPYPPmzeB5fmrxyB8hBD9ZQkgLIeTbAP4KoDYR9ATwMIAHCSGHIHglCX4DYAhAKyGkBdMzLQDwrwDUhJCH5zvHdLcksYTBmFqdJhZSeBhinWe+UY1VhUZ0jPvQOxFFSVz8rsVEynIhtRiUUkTcNoRdVhiKq6DQTNcSIYRAqTchFvCKUoshVI1KMy1N9M5fEbJZlFL8/vAAeAp8YVsZrq+WIS8vT9Qxnolaob/97W/Yu3cvWPa9ajNK6WOzvGzzWT+vmPL//zH5WhbA7ZP/klBKK6b8+JVUzjHdOoxwoo5eKoMh9jZnamNPpiRHKY74REvXTUWhMy2oipLnWPhGuhAP+5G1bM05xiKBypg7p6T/QogHvaJ2lQIAz2WeUp7xuGw84wK7xn4XTo/5YNYocMfHaiQpLpxaNR2JRBCLxcRXRs6QtAxGLBYbttmEbkUpDIYUegNTJdAyJanCNeIR6gZE1nAQyq5TU5+Kh3zw9J+CypgDY3H1nBecoHHpy3gLSSmdbOsXt3KZi4XBKMUXY8o0LhJlOTx5VFAau/PSGmTplIjFYqI3XU7tyxodHY2EQqHMc7Uik9Zf0eVy9Y6OjlJgeoedWEjRCahUKkUzQhvLs2BQyTHmicDDqUSXyJerNKAcO2f/A6UUQfswAtYBmMpWQW2aXxeDEJK29P5U4iG/IBokcnBS6PwVd5tDKc04RftK8xicgRhWFxlx/RZB0EjqjuqBgYEwgPknTy8yaX3i8Xh8dGhoKARAkq49tVqdVFAWCzH7FBSMDLuqhRL8Dg+RpIBJbbbMqjnBxaPwDLSBUh7myroF3ZXVppyMtyURtxXqrIUNbEoFNhICoxJXKkDo90nfE7D5ItjXOgYA+P7Vq8FMRjulaLqcKhw1ODgYx4ViMACMDQ4ORgBxYwMJEmPjxEZM45aIY5x2xtOWsp8LtdmCqNdxjjhO1DcB72A7dHml0OeXLziYl5jVkX4WJgwuFhF9OwIAbNgvunoZFw1nNJ3+ySODiHMUn9pQjE0VQjZSKqX8qQZjdHQUAMZEXUAE0jUY40NDQywgjcGQyWSiBz0BceXh90zWY7TbQggHxTcYRMZAnVWA8ISQVqc8D//YGYTdNpgr6tKe+E6ITNCyCKd3zkH7IHSWUkkyGZTyomuLsNFQ2tuclmEPjg+6oVMyuOuyle8dUwINGGC6ep3P56OUUvG/WBmSrsGwjo+PywBxg4lTkaIgTEyDUWBSY2WBAVGWR59fBi4mvkekyS5A1O9G1OeCu78VjEoDU9mqjKsgVaZcRBY42RyAMP2M0owVu2YiFhQ/iApMxkXS2OawHI8nDg8AAG75SDXyje9t+zIRY5qLqduceDwuvjCICKSbVo2Fw2EOkM5gaLVaBIPixgbEHkCTaEbr9CkQ9YuTrpwOgVJngnekE4bC5dDmFIlyZ1fqzIgHFyaxx7MxBG0D0BdKM8Ev5hd/GBSQ0FxduIfx2mkrxrwRLMvV4as7K6f9LhAIICEgJRZTtzmTM1aXnHcBZDYqMc7zvCS9JIA006WmTsgWg0Qco80RF62+IQHPsfANd4HnWOgt5Qi7xkX7OwuTxrQpB2spz8M73AV9wTIwCvEFgxY6iS3l4/L8ZEp1YfUS7lAMfzwxAgC476paKOXTLxMppvJNjV+Mj49DLpcvuYAnkIHBYBhmYmJCuEimSouJhRQGg2EYMAwjWnq1PpFe9UYwEeLAiVT1maytMOXCWFwFTU4RiIxB0DYomtFQGXMQ9c7fW0IpD99IF1TGnLTjJvORziS2lI4bDsw6nX4unjk6hEicx0dX5Se9yKlIYTBCoRC0WsETGh8fB8/zQ6IuIBJpGwyZTDY2NiYEcXU6neij46QwGACQk5MDp1OcJiwFI8POKiG92h3WIpKh9L5QWzE0pbZCODYhBPrCZeC5+KSKVuZGQ2XIQiww9wBkynPwDXdBoTVAmyOdgHXYZYVGgjRtOtWo3TY/DvQ6oZTLcN+VtTM+JxQKib4lmbrNGR8fRyAQOCPqAiKRtsEIBoMt3d3C+DgpZk1qtVqEQuJXxubm5iLhGYlBYlvSPsEj6nOmfTG/V1tBYa5cc05tBSEEhqIqEBkjCP1m2NFKZAwYpRrcLEVnXCwCd38blIZsaHOlE6/m2bjQN5OGJzAfsaB3Qdscnqd4/FA/AODGi5ahLOfc2AfLspDJZKJ7Q4FAAIbJQdanTp0Ker3edlEXEIm0DYbL5TrY0NDgBcSPDQDCBSLFVicrK0tUg5HoXm0b8wFqY1qxjGRthaVssrZi5i+jMKqwHGpzPjz9pzIeXjxTbwmlFGHXOLxDHTAUVkpy559K2DUOTVa+NGlaLr6gmMs7XXYMTIRQZFLjXy6umvE5fr8/eWGLydTjHjhwIAigSfRFRCCT2t6mAwcORAFAr9eLbjAA4eJ2u89Vv84EuVwOtVotmkdUaNIk06vDnGne2SBToTw3vbYixbuh2pQLc8VqRLwOeAZOp104pjRkCalSCIYi6nfB098KNhpG1rK1kqQ5p8JzLCJeJ9Rm8Y2SMLAp9ZhLIMJi7zGhdePeK2qhUc4cKHW5XMjOFj+bMzVVe+bMGQAYFH0REUjbYFBKbWNjYzylVNLtg1jxhqkUFRUhEX8Rg4SXcWpcmIIW889/52cjQUG3QqVNq7ZCJlfCVFoDXX45go5huPtaEXbbFrRVkTFyEJkcAesA3H0tiHonYCypgaFwmSRdo2eTiF2I3ZMCJEZCpq6g/3zTMPxRFtuX5SSnnM2E0+lEbq44s10SxONxMAwDQggmmzrHU1G/Oh9k9EkxDDMwODgoaC2I2NyVICcnR9TtQ4KCggJYrekP6D2bD01G0puHPdDllSLoGJ5VqEZw+a3wjfbAWFwNbU5hRu64QqOHubwWxpIa8PEYvIOn4e5rgX+8D2GXFbGAG/GQH2wkiHjIh6jfhdDEGPxjvXD1NoNno2CjQZjLV8NYUi1Nt+gM8GwcUa9j1vmxmUB5XijYmqXN/2wGJ4J4q8MGRkbwvatXz/p5UEqnZTPEwufzwWQSvMumpiZwHCeyUKp4ZFTfGg6H321qatpWUVEBk8kEj8cjqqCIQqEApVT0UlylUgm5XI5gMChKtDuRXh31hOGOARpDNsIu6zmZBZ6Nwz/WC8IokFW5RtS7OKNUQWcphc5SCp5jwYYDYKNhYQYqz4HyQj1CItipMlmgL6gEpRSegdOiz1eZj6B9ENq8Ekk8mVjQA4XOnJIhppTifxsEYZwvby9HTcHs8Qmv1wuj0Sh6vMXj8SQNxpEjR0I2m+2voi4gIhl5GBMTEwcOHTrkA6SJNwBAdnY2XK7MgnszUVpaiqEhcVLdU9OrzcMeaHOLEXHbptVlxIJeeAbaoDLlwVhcJanLL2PkUOrN0OYUQl9QCUNRFYwlK2AoWg59QQU02QVQ6owgMgYyRg4ZIwcXE79adzbiYT/YaFi0sY1nE3HboDanduNqODOBTqsfOTolvv2xFXM+d2JiQvTtCCAYDLNZiLe8++67ASzRgCeQocGAEPiMANJd2Hl5ebDb7aIft6ioCFarVbR+laQK17AHRMZAX1AB/1gveJ5H0D6EoH1oWm3FUkIQCJaitP1cEk10hqIq0e/UAMDFY+DZ2KyqY1OJxDk8NSmM892P18CkmdvLcjgckhiMqYVgvb29gCD4uyTJyGBQSq2jo6M8pTQpeiN2rCY3NxcOh0OSUQZ5eXmixTISgc/jg25c/+sjuGNfPxqtLNy9J4XaioqF6VYsJotpMIL2QahNeZCrxG/eAia9ixRTwS+dHIU7FMe6EhM+Uz+36nc8Hkc0GhW9YCscDkOtVoMQkrgxWpdqwBPI3MMAwzCDCdfeYDBIUs5tMBjg9Yo7KRwAKioqMDAwIMqxjva5ponuOwMxPNkWwjEbB7UpV5K7qVjI5AqAENGmg81G1DcBNhKCRqKqUUopoj5HSupj494wXj0ltGt87+rVkMnm/nysVisKCsQP0E5N0zY1NYHn+SUb8AREMBjhcPivR44coYC0adDxcfF7cfR6PWQyWXI8XSb85PWucybFxHlg/zAD30h3xpWZUiO1l8FGwwjah2AsWSGZ8Yx6HVDqs1KKDz1xeBAcT/GZ+hJsKJu/XX98fByFhYVinOY0pm5zDhw4ELRarW+LvoiIZGwwJiYm/vjss89OAIDFYoHDMfPsyUywWCyw2WySdMWuWLECiRL3TBjzzCwp6ArGoc0rhW+4U5QJ4lIhpcHg2Th8w10wFFdLlo2hlCLkHIM2t3je554YcqN52AODSo7vfnzlvM9nWRahUEj0hjMAcLvdyMoSDNaLL74YAvCW6IuIiBgVMyeOHDnCsSwLrVaLSCQiuvCNXC6HVquVpJo0OzsbLMtmtJWilMKinzntm6NXQm3KhdKQDd9oz5KdRcsoVAClog9CpjwH71AHdPnlKQUi0yXqm4BCZ5x3nECc4/GHw0Kg87aPViPPMP8wJpvNhvx88atRg8EgtFotZDIZRkdH4ff7xymlmbu7EpKxwaCU8gzDHDh8+DAA4QKUotiqpKQEw8PSqK6vWLECXV1dab02Fovh2LFj+PwaAzSKc/+c60qEdJk2pwiMUgX/2JklazTE9jIEY9EJdVa+KMOTZl2HUoScIyl5F6+eGofVF0G1RY8v7ahI6fjDw8MoLp7/2AvFZrMhL0+It7zyyius3+9/UvRFREaUmtzR0dH/3bt3rxcQv4oyQUFBAex2u+gT0QAh9sKy7ILTwk6nE4cOHUJpaSlu/cQOPHjNWhSbNSAADGrB43i70463OoS2d52lHDJGDv8S9TTEnL/Kcxw8g+1QmXIlb2CLeOxQaI2ClzQHE4EoXj4paKR+7+rVUDDzf/1DoRBYlpVkO5IYvAwATz75pNvv9/9R9EVERqwi/nf27dsXA97Tm5Bi3mp+fr4kwU8AqKurw+nTp1M6b57n0dnZia6uLmzbti35oX9yQzEO3fVh9D90BU5971LcPSkc+9uD/fjzqXEQQqDLLwejVE/GNMQ3fpnAKNXgOS7jAC03WaKuySqQ3FjwHIvwxCh0lrJ5n/tU4xCiLI/L6gqShXbzMTg4iPLy8kxP8xzi8ThYloVGo0EwGERfX1+YUton+kIiI4rBoJSGWZbt6e7uBsMw0Ov1kojfVFRUYHBQmiY+g8EAs9k877YnFArh8OHDIIRgx44dc4rB3rhnOb5/9WoAwB+ODOLl5lHBaFjKoDRkw93fJnkqc6GojNkZbUvi4QC8g6ehs5RBbZ4/vZkpIccINNlF86qNt4/7cPjMBNQKGe69YlVKx+Z5HlarFUVF4qeB7XZ7so3irbfeAs/z+0RfRAJEaxN0Op3/+9JLL0UA8btBE2i1WjAMI0nwEwBqampw5syZWTU4xsbGcPToUaxcuRI1NTUppQe/tKMCP752DQgBnjs2jL3Hh0EphSYrH/qCCngHTyMWWDpxrnTnr1JKEXbb4B/thbF0pWRyflNho2HEgt55C7U4XugXAYB/3lOFkqzUmsesVivy8vJEn6EKCHNHEoboqaeemrDb7U+JvogEiGYwotHoK08//bQPAPLz8yVLg1ZUVKC/X5rKWaVSierqapw6dWra4yzLorm5GaOjo9i5cydycnIWdNzrNpfh/3x2PRgZwUsnR/HU0SFQSqHUmWAqr0PIOYKAdWBJpF3lKg14NragbYkwDLob8aAP5so1klVxToVSCv9oDwxFy+Y13G912DDsCqEkS4Mb9yxLeY2BgQFUVFRkeKbnEo/HEQ6HYTQawfM8Dh48yAFoFH0hCRDNYFBKbQ6Hwz0xMQG5XC5ZdWZ+fj7cbrckow0AoLi4GCzLJgO3Pp8Phw4dgtlsxqZNm6BUpqea/ckNxfjF9RsglxG8emocjzcMgKcUjEIJU/lqyORyuPtbEctw7qkYqAzZiPnnbySklCLidcLT3wqVMRvGkmrIJLgbz0TIOQqFzgTFPNJ+vnAczx8Xtpn/cWUt1IrUzs/lckGhUECvFz8VPLVqtLGxEQzDHKGULq2A1iyIqlwSiUSe27dvHwcIF54UaVBCCJYvX55o0pHk+OvWrUNHRwe6u7tx8uRJbNiwARUVFRlXKF62phC/uqEeSrkMb7bb8Ku/94HnKQgh0OaWwFS6EiHHCHwj3ZIMRkqVVLIlbCQI72A7Yn43zBVrUirHFgs2EkLU54Qub+7+DwDYe3wYwRiH3dW5uKQ29QBsd3c3VqyYu3s1XUZGRlBSIuikPvvss/6RkZH/lWQhCRDVYLjd7scfe+wxFyBUZzqdTklGHhYXF8PpdEoyfxUQjIZMJsPg4CB27twpakrtwyvz8bsvbYZaIcO73Q784m+9YCf/RoxSDVN5LVTGHHiHO+Af759zgrtUMCotuFhkxiwOGw3DN9IF/3gfdJZSwatYRC0NynPwjfZMCiLP/fXtcwTwTqcdchnBf141uzDO2bjdDAA5zwAAIABJREFUbhBCkhoVYhIKhcDzPHQ6HViWxfPPPx8G8BfRF5IIUQ0GpXTAZrMNdnd3QyaTwWKxSFKTQQjBsmXLEtqHopKorVixYgUKCwsliZfsqs7FE1/dCp2SweEzE3js7R7EOcFoEEKgMuYga9k6KDQ6eAbb4RvtkWRC/GwQQqDUZyE6uS0RBg154R3qgH+sFyqTBeaKOsk1P8+GUgr/2BlosvLnrRrlJ4VxKICv7KxAlSX1rYWU3sXw8DBKSwXPaP/+/ZTjuH2U0sUTI8kQ0cUU7Xb7j3/xi1/4AKCsrEyyNGhJSQnsdrtosoA8z6Ojo2NabUVtbS3sdrsk/TFbKrPx5Ne3wqiW49iAGz97sxsx9j1vjBACtdmCrGXroDblImATdDdDE2Oil2/PhMqUi4jHjqB9GO4zzYKCWF4psirXQGXIOi/dtxG3FSAkJVm/gz1O9NgDyDOocOtHqlNew+v1guf5ZH+HmFBKMTY2lsyO/PSnP3XabLafir6QhIhuMFiWfeX5558Px2IxGAwGUEpFn1kCCIVcVVVV6OzszPhYoVAIDQ0NkMlk02orZDIZ6uvr0dbWJonI8YayLDzzzW3I1inRPOzBj1/rRCQ+fRuQuNuby1fDVLYKoBTeoQ64+1oRtA8jHvKLll3hOQ6xgAcB6wD8o72IBz2QyRUwV66BqbRG0l6Q+YiHfAi77TCkMNs1FGPxdKMguXDXx1fCoE5ty0QpRVtbG1atSq1OY6HYbDbk5ORALpdjZGQEvb29DkpphySLSYToBoNSGuN5/o8vv/wyDwCVlZWSpUGLi4vh8/kyKhIbHR1FY2MjamtrZ6ytUKvVWL9+PRobG0UXOQaA1UUmPPvNbcgzqNA+7sNDf+lEKDZzSlMmV0KbW4ysZWthKlsFRqlC2G2Fu78VrjMt8I32IOgYQdTnFIR/o2HwbHxS01P4x7NxsNEw4iEfIl4HgvZh+Ea64TrTDM9Am9DEpTXAXLkG6qxCyOTKeYuipIaNhuAfOwNTaU1KCuMvnhiFNxzHxjIzPrUh9R6Q8fFx6HS6pFye2PT396OyUhjs/D//8z9Br9f7vvIuAIBIUStBCKlYu3btsZaWllye5/Huu+9i9+7dogr5JnC73ejo6MD27dsX5CazLIu2tjbE43GsX78eCsXcdyGbzYaenh5s27ZNkvfR7wzi878+kpwYfvdlq6BXp74Oz3HgoiFwsQi4WFiopWBZ8FwcmPIZE5kMhJFDxiggU6jAKNVglGrIVdpzLsZ4yIewywpjiTT7+VTg4lF4B9thLFkBuXp+tatRdxj/9mIreEqx71u7UFecWuCS4zgcOHAA27Ztg1otvjJaIBBAa2srduzYgVgshoqKCvv4+Hj5+yl+AWSoGj4blNKBoqKi9hMnTly0ceNGlJaWYnBwEMuXz+9OLpSsrCxoNJppjTzz4fV6cfLkSVRWVqKsrCwlQ5Ofn49oNIqmpiZs3rwZMpFnaVTm6vDcjdvxud8cQZ8ziB+82o57Ll81r85kAhnDQKY1QKEVbyqXXGNAPNwLSnkQIv7skPngORbeoQ7oC5elZCwopfj94QFwPMX1W8pSNhaAMDyopKREEmOROP6yZULR2LPPPsuxLPvM+81YABJsSRKMj4/f98ADD7gAoLy8HENDQ5KkWAFg1apV6OrqmreTlVKKvr4+tLS0oL6+HuXls48lnImysjLk5OTg+PHjkryX0mwtnr9xB5bl6TDkCuH+/afhCi5+WjUBIQRKnQnx81BMxrNxoSclrzTliXDHB904NeqFUS3Hdy6tSXmtcDiMsbGx5AUtNpFIBB6PB/n5+aCU4sEHH3Q7HI6HJVlMYqS8bfz90KFDHpvNBoVCgfz8fIyOjkqykFqtRllZ2ZwB0Gg0isbGRgSDQezcuTPt+ZhVVVXIycnBsWPHJGm1LzCp8dw3t2NlgQFjngju338aDv95LOIy5SLiXRyB4AQ8G4dnsB3avFKojKmV4cfY94Rx7rikBtm61CpyKaVoaWlBbW2t6F5jgr6+PixbJpSwHz58GF6vt4lSKn6z1SIgmcGglNJAIPDgI488EgCQrJuQSgeisrISHo9nRk0Lh8OBhoYGlJeXY82aNRk3Ey1fvhz5+flobGwEy4qv1ZlnUOGZb2xDXbERNl8U9+8/DZvv/HivCq0R8ZBv0fQ7uHgMnsHT0OeXQ2VIfYbpvtYxOAJRrCww4PNb5291TzA0NASNRiPqAK6pxGIx2Gy2pADPf/7nf06Mj4//pySLLQKSbkyDweDvn3jiCY/NZoNarUZubq5kXgYhBOvXr0dra2vyIk7UViSClWKqPldUVKCkpASHDx+WpK8lS6fEU1/fho1lZjgDMXx/32mMumfWDZUSQkjSaEiNUG5+GvqCygV1uzr8Ufyp+T1hHHkKwjiAsBXp7+/H6tWr0zrfVEjELmQyGY4dO4ZTp071UEqPSragxEhqMCilcb/f/2/33nuvFwCqq6vR29srWSxDp9OhoqICHR0dydoKhmGwffv2OXUr0qW0tBSrVq3C4cOHRVEePxuTRoE/fG0rti3LhjsUx/37T2NwYvEqPhOojDmIesVXg59K1OeCb6QbxtKalGMWCZ48Oog4R3HVuiJsW5baFoZSiubmZtTV1UmS9QKEbbDNZkNpaSkopbj55psnbDbbTZIstkhIHvoOh8PP7tu3z97X1weVSoW8vDyMjIxItl55eTmcTicaGhpQW1uLFSukk7UHBHm/LVu2oKWlRRINEJ1Kjse/vAUXrciDL8LiB6+244xD/EK4uVDqTYgFvZJsSxJ6nKGJMZgr6iBXLWzQcduoF439LmgUDO65fH4F8AQDAwPQ6/WSTDJL0Nvbm/Qu3nzzTTo8PHyUUtoi2YKLgOQGg1LKO53Om2+//XYXIHgZZ86ckSRgmNCtSCgxS+FVzIROp8OOHTswPDyM1tZW0d+bRsng1zfU42O1+QhGOTzwage6rNKICM0EITIoNHqwYXHX5Nk4vEMd4GJRmCtqF9zExvJ8UhjnWx+uQqEptc/b7XZjeHgYtbW1Cz3llAmFQnA6nSgtLQXP87jtttsmrFbrtyRbcJFYlOQ6x3FvHjlyZKClpQVKpRJlZWWiN455vV4cPHgQ2dnZ2LJlC9auXZuYJCXqOrOhUCiwZcsW6PV6HDx4UHSJQpWcwf/9/EZcsbYQ4TiHB//SgbbRxUt3pqvENRuxgAeegTZosvJhKFqeVp3HG6dtGPWEUZGjxdd3V6b0mmg0iubmZtTX10uipJWgo6MDq1atAiEEzz33HOd2u/9MKV2yM1NTZdGqcWw2240333zzBCAEDMfGxkRpT6eU4syZM+fUVuTm5qKwsBBtbW0Zr5EqiS7a9evX48SJE6JnhRSMDI9etx7XbCxGlOXx8OudaB6eX+hGDJR6M2IBT8bvh/IcAtZ+BB3DyVb+dPCEYnihSdja3ndVLVTy+S9+SimamppQW1sr+ozUaefm8SAWi8FisSAej+Puu+922Wy270i24CKyaAaDUnr8zJkzJ999910wDIMVK1agvb09o2NGo1EcPXoUoVBoxtqKZcuWIRqNSjbPZDZMJhN2796NWCyGgwcPihoQlTMyPPLpdfjc1jLEOYpH3ujGsf6FjUdIByKTgVFpM2qzj/rdcPe1QqZQC8Op5xkLMBfPHhtGOM7hwyst+PDK1IRxOjo6kJ2dLclQogSJBrZE5uWXv/xlNBQK/Z5Sapds0UVEkl6SWRcjZEVdXd2h1tbWXAA4cuQIampqksNoF4LD4Uh2Fs6VLmVZFocOHcKaNWvSWidTfD4fWltbYTabUVNTM2/PSqpQSnH//nY8fmgAMgLc/KEq7FguXQAPACJeJ9hIAPr8igW9jotHEbD2AxTQF1ZmZCgAoNfux3/86TSUjAyvf/siVObO7y2MjIxgZGQEW7dulTQIPjg4CL/fj7q6OgSDQVRXV9vHx8erKaXS56UXgUVtEKCUdjscjrdfeukljhCCNWvWoK2tbUFxBp7n0d7ejp6eHmzfvn3e2gq5XI7NmzejpaVFMrXxuTAajUnv5+DBg+jt7RUlKEoIwX1X1uJfLl4OngK/eKcXf+uS9iamMmQh5nenvC3h2TgC1n54hzqgNltgKluZsbFICOMAwNd2V6ZkLBwOB/r7+1FfXy+psYjFYujr60NNjVCW/pOf/CQUiUR+eqEYC2CRPQwAIIQUlJSUtLS1tVlMJhM6OjqgUChQVVU172uDwSBOnDiBgoICVFVVLejD9/l8OHHiBLZu3bpo2ZOz4TgOfX19GBkZwbJly1BaWipKOfLP3+7BT98UBkp/ZWcFLqkVr0DtbLxDHdBZyuZsBuM5FmHXOKJeJzQ5RVCbLaJdqH/ttONXB/pQYFTj7Tv2QKeau4bC4/GgubkZ27dvh0qVmbGaj5MnTyIvLw8lJSXo6enBrl27+u12+ypK6dIaPpMBi96CSCm1ejye7950000eQJhrOjo6Oq/IzsjICI4dO4bVq1ejurp6wV9Ao9GIuro6HDt2bNa5I1LDMAyqq6uxa9cuhEIhvPvuu+ju7s5YZ+OWj1Tj3ssF0ZfHDw3g1VZppsMBc2dLuFgE/vF+ePpbQWQMspatgyYrXzRjEYyyePaYIIxz9+Ur5zUWwWAQJ0+exObNmyU3Fgn1t+LiYnAch89+9rMuu91+3YVkLIDzYDAAIBAIPPHOO++0/OUvf+EZhsGaNWvQ0tIyo6vLsixOnjwJq9WKnTt3ZhSHyM3NRVVVlWQ9IKmiUCiwatUq7N69G0qlEg0NDWhpaYHHk34W4hsXLcMPPiEE2p48OogXT0hTHKc0ZCHqfy/ISilFLOCBd7gTvpFuKLQGZC3fAG1OUUpiNwvhhaYR+CIstlRm4+p1c08ji0QiOHbsGDZs2CBpRgQQvqPt7e1Yu3YtCCH42c9+Fh4dHX2KUnpM0oXPA4u+JUkuTEhBcXFxS1tbm8VsNqOtrQ1arXZai3HCnUy472LdqYaGhjA8PIwtW7aIFoTMBEop7HY7hoeHEQgEUFRUhNLS0rS2TnuPD+Pf/tgKSoFPri/CZzeJ93dL4Bk8DXVWIdiQD1G/CwqtEZosi6SiwMOuEO56sRUAsP+W3agtmn2tcDiMo0ePoq6uTtJKzgQtLS0wm80oLy9Hd3c3Lrroon6bzXZBbUUSnDeDAQAGg+GGyy+//NHnnnvOzHEcDh48iI0bN0Kv16Ovrw+jo6PJn8VmdHQU/f392Lp165IwGgni8TjGxsYwMjICjuNgsViQn58Ps9mc8oX/p+ZR3L63BRxPcVldAb64bWG6HzNBeR7xkA+xgBsRrxNEJoPOInSUiu1JnLM2pfjhqx1oH/fhhu3luP8TdbM+NxgM4tixY1i7du2iZMVsNhsGBgawZcsW8DyPTZs2TTQ3N3+cUnpc8sXPA+fVYBBCiMVieft3v/vdniuuuELm9XrR3NwMpVIJg8GAVatWSVqNNz4+jt7eXmzdujXtiWZSEovF4HA4YLPZ4PV6odfrkZWVhaysLJhMpjmbpl5rs+KWZ04gzlF8ZKUFX91VCdkCjAbPsWDDfsRDfsTDfvDxGBRaI5SGLMhVWniHu5C9fJ0Yb3NejvRN4NG3e5ClVeCvd14Ms3bmzyoQCOD48eNYv369ZLqcU4lGo2hoaMCOHTugUqnw8MMPhx955JFf2+322yRf/DxxXg0GMH1rEovFcOLEiWR592Jgs9nQ2dmJrVu3SibPJgYJ9XW32w23252Uw9dqtdDpdNDr9dBqtVCr1VAoFFAqlXi3x4mb/tCEKMtjd3UubrxoORiZYDQoz4Pn4qAcCy4eS2qBcrEI+HgURMZArjFAodVDoTFAplBN81I8A20wFFWBUUr7N4vEOdz5fAsmgjH86FNr8LlZtC58Ph+amppQX18v6uCp2aCU4ujRo6ioqEBBQQG6urpw0UUX9dnt9toLcSuS4LwbDADQ6/Vf/NCHPvTLe+65R5PQtCgrK0tZozNTnE4nTp06hY0bN0oy7UoqeJ5HOBxGMBhEIBBAMBhELBZL/qOUon2Cw3+diCDGARstMnx5lVwwGkQGmVwOGSOHTK4Eo9RMCgJrIFMo593ChF1WUJ6DNjd1Ve502Ht8GC+dHEVdsRF/unlX0uBNxWazoaOjA/X19WkrqS2Unp4exGIxrF69GhzHob6+fqKlpeVSSmnTopzAeeL86sdPEgwGn2xqavqGzWbbodFomA0bNqChoQEmkwla7cLandMhNzcXmzdvxvHjx1FTU7NohipTZDIZdDoddDrdrIpRFwPYUu/Clx8/hhN2FkSjw20fqYYiRZGZ2VAZs+Ed6pTUYNh8EexvFSQDvn/16nOMRUKj1Wq1YseOHYu2rZyYmIDNZsOOHTsAAA899FB4bGzsyQvdWADnKa16NpRSOj4+fs1NN91k7ezshFKpxNq1a3H8+PFFS3/q9Xrs2LED/f396OnpWTRJusVgU0U2nvr6Vpg0CjQNuvHI612IsplVm8rkSoAQcHHpvO8/HBGEca7ZUIz68ukBTJ7nk9W727dvXzRjEQ6H0draivr6eshkMrzxxhv8o48+2uNwOL67KCdwnlkSBgMAKKVOm812+eWXX+50u93Izs5GeXk5mpubF+3iVSqV2LZtG0KhEE6cOHFeazXEZl2pGc98YxtydEq0jnrx8Gtd50xZWyjClHdpBIKbhz1oGnRDr5LjrsumC+NEIhEcPnwYer0e69atk0y892w4jsPx48exdu1aaDQa9PT04IYbbrA6HI6PUUrPn7z7IrJkDAYAUEpbHQ7Hv1x11VVulmVRXl4OpVKJ3t7eRTsHmUyGdevWIS8vT/RO0/NNbZERz924DZbJKWs/+nPHrFPWUkEqg8FyPJ44PAAAuPUjVbAY3wus2mw2HD58GNXV1QtuD8iEhLp4SUkJcnJy4PV6cdlllzltNtsVF0onairMazAIIRwhpJkQ0kYI2UcIkTRf5ff7n+/u7v7Vbbfd5geAuro6OBwOSeTv5qKsrAz19fVobW2VVO18samyGLD3xu0oNmvQYw/gh692wB9Jr1SeUagASkUfDv3nNivGvREsy9PhyzsEYRyO49DW1ob+/n7s2LFDMpXv2ejp6QHDMKioqADHcfjEJz7httvtt1JKmxf1RM4zqXgYYUrpekppHQAXgJslPic4HI67X3jhhSO//e1vYzKZDJs3b0ZPT8+MIwSkxGAwYOfOncnKQTEEf5YCFbk6PHfjNpRla9HvDOIHr3bAE0rPo1YZs0X1MlzBGF46KZS1f++q1VDKZQgEAjh06BA0Gg22bt0qeV/I2YyMjMDlcmHNmjUghOCOO+7wt7e3/87n8z2zqCeyBFjoluQwgGIAIIToCSFvE0JOEEJOEUI+Mfl4BSGkgxDya0LIaULIG4QQzeTvNhNCWgkhhwkhPyGEtE0+zkz+fIwQ0grgm3a7/VN33333YENDA1UoFMkWdSkmwc8FwzCoq6tDZWUlGhoaMDQ0dEF4GyVZWuy9cTuW5+kw7ArhB/vb05qyJrZ03zONQ4jEeVxSm49dVTno7u5GU1MT1q5di+XLly/aFiSB0+lEX18fNm3aBJlMhj/84Q+xp59++vg/SpDzbFI2GIQQBsBHALwy+VAEwKcopRsBfAjAT8l7n2Y1gP+mlK4G4AFw7eTjjwO4iVK6HcDUiNvXAHgppZsBbAbwDQAWh8Px0c985jP2kZERaLVabNy4EcePH0c4vPjzOfLz87Fr1y54PB40NDScF20NsSkwqfHcjZNT1rwRfH/faTj8C5uxwijV4DkWPJd5gLjL6sfBXieUchm+tbMQBw4cACEEu3fvXpTKzbPxeDxoa2vDli1bIJfL0djYiDvvvHPI4XBcTSldHLHYJUYqBkNDCGkGMAEgG8Cbk48TAD+a9AjeguB5JLTP+qfs7ZoAVEzGPgyU0obJx5+essYlAG6YXOcogBwA1ZTSIZvNdu2ll17qCoVCMJlMWLNmDRobG8/L9kChUGDt2rWora3FyZMn0dnZKYn6+WKSq1fh2W9uw9oSE+z+KL6/rx3j3oUZZJUh820Jz1M83iBo5H6yRoegfQibNm1CdXX1omVBpuL3+5Ot8Wq1GmNjY7jmmmtsdrv9Y5TSxXVzlxApxzAAlANQ4r0YxucB5AGon/y9DUAinD31auYgFIjN5UsSALdMxkrWU0orKaVvAADLsofGxsa+e8kll7gjkQhycnKwcuVKHD16NGMdiXTJysrCrl27oFAocODAAQwPD7+vtylmrRJPfn0r6suzMBGM4f597Rhxh1J+vcqUebbk7Q4bBidCyFET3Li7Etu2bZO8LX02gsEgjh8/jvr6euh0OjgcDuzZs2fCarV+mlI6cF5OaomQsummlHoB3ArgTkKIAoAJgJ1SGieEfAiCQZnr9W4AfkLItsmH/mnKr18H8M+TxwUhZAUhJPltcbvdv21vb//eFVdc4YnFYsjPz0d1dfV5NRoymQzLly/Hjh074PV68fe//x1Wq/V9aziMagWe+OoWbF+WA084jvv3t2MgxSlrcpUWPBtLa1tCKYVjfBTPNQ4AAL7/qXVYXiF+S36qBINBNDY2YsOGDTAajXC5XNi9e/fEyMjI51iWPXheTmoJsSBfj1J6EkALhIv9KQCbCCHHIXgbs49Of4+vAfgVIeQwBK8iMVjjNwDaAZyYDIT+EmeVrbtcrsdaWlp+fPXVV3tYlkVhYSGqqqrOq9EAhGKvuro6bNmyBePj4zh06BCcTuf70nDoVHI8/pXN2LMiD/4Iix/ub0evPTXvW6kX9D5ThVKKiNcJ95lmvHjKiSAL7FiegyvWzi2MIyVTjYXZbIbX68VFF13kGhoa+ko4HH7jvJ3YEmKxVcP1if0fIeQuAIWU0gW1Alsslu/t2LHjX1944QWTXC6H1WpFd3c3tmzZsiS6Tf1+P7q7uxEKhVBZWYmioqLzsgfPhCjL4ZanT+KNdhs0CgbfvbQGKwvn7gBlI0EE7UMwla2a83mU5xB22xBx26DQGuGQ5eA/9neCEIK/3LYbK/IXp3nsbBLdrokGRL/fjz179rh6enr+2e/37z0vJ7UEWWyDcR2AuyF4D4MAvkwpdSz0OBaL5Ydbtmz51ksvvWRSKBRwOBw4ffo0tmzZsijNaqkQDofR19cHu92O0tJSlJeXLymhnvmIczxu39uCfS1jUMlluOOSGqwpnr2Tl1IK95lmZC1bCyI7V8OEi0cRnhhH1O+C2myBJrsARMbg+/va0WXz46s7K3HfVdKNLpwLl8uFlpYWbNq0CQaDAR6PB3v27HENDAzc6vV6nzovJ7VEWRLt7emQl5f37+vXr79j//79ZpVKBbfbnRyBtxh6CKnCsiyGhoYwNDQEk8mE0tJS5OTknLc9+kLgeIp/+2MrXmgagYIh+NePrsDGsqxZnx+wDkCh1UNlFGTxKM8LCl0eO7h4DNqcQqhMucmxiId6nfjFX3uRo1fir3deDKN68Q2q3W5He3t78mYzMTGR2IZ80+/3/3HRT2iJ8741GACQm5t7R21t7b+//vrrZo1GA7/fnxyFt9ilw/NBKYXL5cLw8DDcbjfy8/NRWlq6aPoN6cLzFPe90oYnjwyBkRHc8uEqbK2cebxhPOxH0DEKXW4RIh4HYkEvVIYsqM2Wc8YSROIcbt/bDHcojoc/vRaf3VS6GG9nGoODgxgeHk6qittsNlx00UUTw8PDXwqFQq8u+gm9D3hfGwwAyM7OvrmqquoHr732WlZ2djai0SgaGxtRVlaG8vI5EzfnDY7jYLVaMTIygkgkktTtzMrKWpKeB6UUD7zagd8c7IeMAP98cRV2Vb0nrkt5HrGgFzG/C2G3FSpjLtRmC5T62XVIn2kcwistY1hXasZL/7wDshmEcaSCUorOzk4EAgFs3LgRDMPgzJkz+NjHPjYxMjLyT7FY7K1FO5n3Ge97gwEAOp3uUxaL5Vevvvpqbm1tbXI0gUajQW1t7ZIOOsbjcTgcDtjtdrjdbhgMBlgsFuTl5UGtVi8ZA0Ipxc/e7MbP3+kFAfDV7SXYUcggFnAJep86E5R6YQSBypAFlWF2Ad5xTxjf+WMrOJ7i5Zt3Yn3p4lVxxuNxnDx5EjqdDrW1tSCE4O233+a/8IUv2KxW61X/CCI4mXBBGAwAIISstlgsr/3mN78pvOqqqxhKKXp6euB0OrFp06YlKfJ7NpRS+Hw+2Gw2uFwuhMNhaLXapPCv2Ww+L4HTaDSa1BJ9/OgY9nYK5eOfW5eFy9aVQa56bxxCPORD2GWFsWTFjMeilOLh17vQPOzBZzeV4OFPL46QMCCIBDc1NWH58uUoKSkBpRSPPfZY5IEHHjjjcDg+Sim1LtrJvE+5YAwGABBCcvLy8l6/9dZbV917771aQgisVis6Ozuxbt06ZGXNHrBbilBKEQqF4PF44Ha74fF4wLIsFAoFdDodtFptUvxXpVJBoVCAYZgFeSWUUrAsi3g8jmg0imAwOO0fx3FQKpUwm81Jw/XU8XH8YH87AOBzW8pw1ZShQpRSuHpPIrtqfTK4OZWmQTceeaMLBrUcf73zYuTqF6fzdHx8HJ2dnckai1gshq997WveN9544x273X79hSzcKyYXlMEAAEKIwmKx/Gb79u2feOaZZ0wajQbBYBBNTU0oKSlBZWXlknHz0yUejycv6EAggFAolBT+ndrbMpvx4Hl+2gBsuVwOhUIBlUqV1AhNGKLZRhk8dXQQ977UBgC4dmMJrt1YnFzLP3YGKmMOlPrpW40Yy+M7L7TA7o/ivitr8dVdlRn/LeYjMbw7GAxiw4YNUCqVcDgcuOyyy1wDAwM/nZiYeJBeaBeBhFxwBiNBVlbWLSUlJd977bXXshPzLk+fPo1IJIL169e/L7YomUApBc/zM1acEkJEmffyQtMIvvtCC3gKXL2uCP+0WSjpjgUPEuSGAAAMJklEQVQ8iHidMBZPH7D90slR7D0+jBX5erx66+6MhYjnIzFbNT8/P6nO1dLSgquuusppt9tviEQif5H0BC5Alm40MEPcbvfPOzo6PrV161ZbY2MjGIbB2rVrUVpaikOHDsFuv7BV1RJGQS6Xn/NPrOFQn64vwaP/tAGMjOCVljE8cXgQlFIodCbEQ75pxmoiEMWfmkcBAN+7erWkxoJSisHBwXOGd7/wwgvsJZdcMjA8PLzzA2ORHheswQAAlmX/Pjo6uu3KK6/s/tGPfhTiOA6FhYXYvn07+vr60NraekEJ/Z4PrlpXhP/5/EYoGILXTlvxm4P9oAAUWgPiIV/yeU8dHUKU5XHFmkLsWC7dvNNIJILGxkZ4PB7s2rULWVlZCAaD+OY3v+m7+eabG+12+wZKabdkJ3CBc8FuSaZCCFHm5uY+VFRUdMPevXtzampqQCnF0NAQ+vr6sHr16iVX6PV+429ddtyYmLJWlYsvb8wGF3LDULgc7WNe/ODVDqgVMrx9x8UoNi98yPR8TP08a2trkZ8vSLP8/e9/pzfccMOE1+v9gcfj+fkH8YrM+IcwGAkIIfUWi2Xvt7/97cLvfOc7GoZhknMmFAoFVq9eveh6kRcSDWec+PrvjyMU47ClIgufLw8ge/kG3PNyG4ZdIdzxsRW45SPVoq8bCARw6tQp6HQ6rFq1CgqFAqFQCLfffrvvpZde6rHb7f/wOhZi8Q9lMACAEKLKy8v7cWFh4Rf37t2bnfA2xsfH0dXVhfLy8gsik3K+aBp04Uu/O4ZAlIVCBsQnkzHZOgUa7voI1ArxhmuzLIuenh44HA7U1dUlp7UfOHCAfvGLX5zwer0/9Hg8j33gVYjHP5zBSEAI2WSxWJ67/fbbC++8804NwzDTvoCrVq1CXl7e+T7N9yU/f7sHP31zephAyRA8/Ol1+OSGzEcrUkoxOjqKnp6eaQY+FArhjjvu8L344ou9drv92g+8CvH5hzUYQNLbeLioqOgLe/fuzV6xQqhODAaDaG9vB8/zqK2tXfINYkuNnQ+9g1HPubqgxWYNDt314YyOPTExgfb2dphMJtTU1CS3kIcOHcIXvvAFp9frfcDtdj/2jyrSKzX/0AYjASFkU35+/jPXXntt/v3332/IyRG6MV0uF9rb26HT6bBixYrzpjH5fqPyrlcx07eKAOh/6Iq0junxeNDV1QUA04x4f38/br/9dvfhw4d7bTbbdZTS/jRP+wNS4AODMQkhhNHpdF/U6/UP3HTTTebvfOc7Wp1OB0op7HY7urq6YDKZUF1dvWREepYqYnoYXq8XXV1d4HkeNTU1yfJ+h8OBe++91/vKK684HA7HzTzPv/lBrEJ6PjAYZ0EIUWVlZd2q0WjuvPvuu0033nijSqFQgFIKq9WK3t5e6HQ6VFVVLSmhnqXEyydHcfeLpxCeMuxZo5DhwWvWphTDSGiH9PT0gFKKmpqaZEDT7/fjoYceCv72t791+3y+u8Lh8DMfbD8Wjw8MxiwQQgx5eXn3abXaLz344IPZ1113HSOTyUAphdPpRG9vLwghWLZsGfLy8j7IqpzFyydH8ZPXuzDmCSNHI8MdH6vG9Tuq5nwNz/MYHx9Hf38/NBoNqqqqYDIJsoCxWAz//d//HfnJT37iDYfDD3k8nv+mlIo71PUD5uUDgzEPhBBLQUHBw2az+YpHH30055JLLklaBq/Xi/7+fng8HpSVlaG0tPR9pdu5WAwPDyMUCqGmpmbG30ciEQwODmJsbAwWiwWVlZXJbR/P83jqqafYe++91x0KhX49MTHxI0ppavMPPkB0PjAYKUIIqSwoKPh5Tk7O1nvuuSfrM5/5DJMwDrFYDENDQxgZGYHBYEBZWRlyc3M/8DomicfjaGhowJ49e5KP8TwPq9WKoaEhxONxlJWVoaSkJNnnEggE8Pjjj0d/9rOf+UKh0Mt2u/1uSql4Q1w/IC0+MBgLhBBSarFY7pLL5Z/5xje+obv55pu1iXoNSincbjeGhoaSup3FxcUwGo3/8MbjyJEjWL16NWKxGEZGRjAxMQGLxYKysrJpsaD+/n488sgjvj/+//buJiSOM4wD+P9Zd133+8NVM2vQlVL6caoYCsaNTcBDToFgAzl4MHjxEAoNhd57aCGElNIQcughPYgEkrakStIemkB1C2nShkJD3UC1we9d92NGXdd5d94e3N2uJiGTqNHY5wfDzrizszPC/JmZfd/nvXZtaXV19VI6nb4gpUzt4K6zChwYL4iInG63+5TL5fqovb3de+bMmWA0Gi0HQ6FQwNzcHKamprC0tIT6+nooigK//+l1LvciwzCwsLCAeDwOTdPKIRoKhcqlE4UQGB4elufPn1+Ix+NzCwsLn+i6/o2UknsG7jIcGJtUHLH+YDgc/ri6urq9v7/f3dfXVxMK/dcjUwiB+fl5zM7OIpvNwu/3o76+HqFQaE/2Xcnlcpifn0cikYCmaaitrUUoFMLDhw/X3ZZMTEzg4sWLiwMDAznDMIZnZ2fPSSn/3MFdZ8/AgbGFiMjv9Xp7nU7n6ZaWFm9PT0/g2LFj1v3795fXKd22JBIJJBIJGIaBYDBYnnbD6G3Po1RGMJVKIZVKIZ1Ow263o66uDnV1detux2KxGJxOJ27cuLEyODioJZPJ2VQqdTafz1+VUq7s8KEwEzgwtgkRtXg8nm6Px9PjcrnCJ06ccHZ3d7taW1vX3ZIIIconWyqVQj6fh9vths/ng8/ng9fr3TXVw0vhoKoqstksMplMuVBxKfD8fv+6Aj1CCMRiMVy5ckUdGhoyAMTn5ua+yufz16WUczt3NOxFcGC8BETkr6qqOqooyinDMFq7urqsJ0+eDBw5cuSxKwopJZaWlpDJZJDNZqGqKlZWVlBVVQW32w2XywWHwwGn0wmHwwG73f7UupvPq1QQOJ/PY3l5GblcDsvLy+X6oVJKOBwOeL1e+P1++Hw+OByOx8JMVVXcvHlTDgwMpO7cuSMsFsvP09PTlwH8JKV8vAkoe2VwYLxkRGQDEFUUpccwjKNNTU22aDRa09HR4Wlra0Nzc/MTryaEEOUTt3Qi53I55PP5cuFfIlpXis9iscBisYCIQESQUpZrfRqGAV3XIYRYV3XMarXCbreXA8npdJarkz9pfBfDMBCPx3H37l05MjKSHR0d1ZPJ5GKhUPg2kUgMAviNW2LuHRwYO4yIFABtoVCos6amprNQKDQ3NjZaiiHibWtrQyQSMXVLYhhGOQCEEOUiwKXXyvDYWO/TzPYLhQLGxsZw7949OTIyko3FYnoymdRtNltc07TbmUxmFGsBwT+D7lEcGLsQEe0D0FZbW3vI4XC8J4SINDQ0WJqbmykSiVRHIhFXY2OjNRwOQ1EUKIqy6Q5xUkpomoaZmRlMT09jZmYGk5OTq+Pj48uPHj3Sx8fHkU6nV20225iqqrey2ewvWAuH9JYcNHslcGC8IogoCKARQBiAEggEWlwu12tE1CSE2AfAZbPZrIFAAMFgUNpsNrJaraiurqbiAEckhJC6rkPXdSmEwOrqqkwkEqSqKnRd14lItVqtM4Zh/KNp2t+qqk4AmAYwA2BSSqnt3H+A7QYcGHtIsU2IH4APgLVisgGoAiCKk14xn+IgYGZxYDDGTNvT45IwxrYWBwZjzDQODLZpRLS4YbmXiC684LYOE9FQxfzBivcuE9H7m9tbthkcGGw3Owzg4LNWYi8PBwbbVkRUR0TXiOjX4tRR/Pu7RBQjot+Lr29s+FwEQD+AD4noPhEdKr7VWVz/b77aePm2phMC+79zENH9iuUggOvF+S8AfC6lHCGiJgA/AHgLwF8AOqWUgoi6AHwKoLu0ASnlBBFdArAopTwHAETUB0ABEAXwZvE7rm7vobFKHBhsK+SklO+UFoioF8CB4mIXgLcrmp57iciDtbYiXxPR68DagO8mv+u7Yt+UB0TUsBU7z8zjwGDbzQKgfWMvVSL6EsAtKeXx4u3HbZPby1duZit2kJnHzzDYdvsRwOnSAhGVrkR8AKaK871P+awGgMep3EU4MNh2+wDAASL6g4geYO1BJgCcBfAZEY1irdn6k3wP4PiGh55sB3HTcMaYaXyFwRgzjQODMWYaBwZjzDQODMaYaRwYjDHTODAYY6ZxYDDGTPsXbj62QHMZ8PMAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get the data for Black Widow</span>
<span class="n">labels</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="s2">&quot;Attack&quot;</span><span class="p">,</span><span class="s2">&quot;Defense&quot;</span><span class="p">,</span><span class="s2">&quot;Speed&quot;</span><span class="p">,</span><span class="s2">&quot;Range&quot;</span><span class="p">,</span><span class="s2">&quot;Health&quot;</span><span class="p">])</span>
<span class="n">stats</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">4</span><span class="p">,</span><span class="n">labels</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>

<span class="c1"># Make some calculations for the plot</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">labels</span><span class="p">),</span> <span class="n">endpoint</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">stats</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">stats</span><span class="p">,[</span><span class="n">stats</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">angles</span><span class="p">,[</span><span class="n">angles</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>

<span class="c1"># Plot stuff</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">111</span><span class="p">,</span> <span class="n">polar</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="s1">&#39;o-&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">fill</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_thetagrids</span><span class="p">(</span><span class="n">angles</span> <span class="o">*</span> <span class="mi">180</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="n">labels</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">([</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">4</span><span class="p">,</span><span class="s2">&quot;Name&quot;</span><span class="p">]])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>

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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get the data for Hawkeye</span>
<span class="n">labels</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="s2">&quot;Attack&quot;</span><span class="p">,</span><span class="s2">&quot;Defense&quot;</span><span class="p">,</span><span class="s2">&quot;Speed&quot;</span><span class="p">,</span><span class="s2">&quot;Range&quot;</span><span class="p">,</span><span class="s2">&quot;Health&quot;</span><span class="p">])</span>
<span class="n">stats</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">5</span><span class="p">,</span><span class="n">labels</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>

<span class="c1"># Make some calculations for the plot</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">labels</span><span class="p">),</span> <span class="n">endpoint</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">stats</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">stats</span><span class="p">,[</span><span class="n">stats</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>
<span class="n">angles</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">angles</span><span class="p">,[</span><span class="n">angles</span><span class="p">[</span><span class="mi">0</span><span class="p">]]))</span>

<span class="c1"># Plot stuff</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">111</span><span class="p">,</span> <span class="n">polar</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="s1">&#39;o-&#39;</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">fill</span><span class="p">(</span><span class="n">angles</span><span class="p">,</span> <span class="n">stats</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_thetagrids</span><span class="p">(</span><span class="n">angles</span> <span class="o">*</span> <span class="mi">180</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">pi</span><span class="p">,</span> <span class="n">labels</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">([</span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">5</span><span class="p">,</span><span class="s2">&quot;Name&quot;</span><span class="p">]])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>

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
<h2 id="This-is-a-tree-disgram,-it-displays-the-Avengers-with-the-most-evenly-matched-stats.">This is a tree disgram, it displays the Avengers with the most evenly matched stats.<a class="anchor-link" href="#This-is-a-tree-disgram,-it-displays-the-Avengers-with-the-most-evenly-matched-stats.">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Import libs</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">from</span> <span class="nn">matplotlib</span> <span class="k">import</span> <span class="n">pyplot</span> <span class="k">as</span> <span class="n">plt</span>
<span class="kn">from</span> <span class="nn">scipy.cluster</span> <span class="k">import</span> <span class="n">hierarchy</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>


<span class="n">df</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">set_index</span><span class="p">(</span><span class="s1">&#39;Name&#39;</span><span class="p">)</span>
<span class="k">del</span> <span class="n">df</span><span class="o">.</span><span class="n">index</span><span class="o">.</span><span class="n">name</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="n">n</span><span class="o">=</span><span class="mi">40</span><span class="p">)</span>

<span class="c1"># Calculate the distance between each sample</span>
<span class="n">Z</span> <span class="o">=</span> <span class="n">hierarchy</span><span class="o">.</span><span class="n">linkage</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="s1">&#39;ward&#39;</span><span class="p">)</span>

<span class="c1"># Orientation our tree</span>
<span class="n">hierarchy</span><span class="o">.</span><span class="n">dendrogram</span><span class="p">(</span><span class="n">Z</span><span class="p">,</span> <span class="n">orientation</span><span class="o">=</span><span class="s2">&quot;left&quot;</span><span class="p">,</span> <span class="n">labels</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">index</span><span class="p">)</span>

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
<p>Credit:
    Seif, George. “4 More Quick and Easy Data Visualizations in Python with Code.”
    Medium, Towards Data Science, 4 May 2019,
    towardsdatascience.com/4-more-quick-and-easy-data-visualizations-in-python-with-code-da9030ab3429.</p>

</div>
</div>
</div>
    </div>
  </div>
</body>




</html>
