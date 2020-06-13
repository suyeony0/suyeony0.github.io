---
layout: post
title: Space Calamity - NaN Handling
date: 2020-06-13
description: Space Calamity - NaN Handling
thumbnail: food2.jpg
categories: DataMining

# Information for the author block
author : Loui
---


<html>
<head><meta charset="utf-8" />

<title>Space Calamity - NaN Handling</title>

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

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">from</span> <span class="nn">google.colab</span> <span class="kn">import</span> <span class="n">drive</span>
<span class="n">drive</span><span class="o">.</span><span class="n">mount</span><span class="p">(</span><span class="s1">&#39;/content/drive&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Go to this URL in a browser: https://accounts.google.com/o/oauth2/auth?client_id=947318989803-6bn6qk8qdgf4n4g3pfee6491hc0brc4i.apps.googleusercontent.com&amp;redirect_uri=urn%3Aietf%3Awg%3Aoauth%3A2.0%3Aoob&amp;scope=email%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fdocs.test%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fdrive%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fdrive.photos.readonly%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fpeopleapi.readonly&amp;response_type=code

Enter your authorization code:
··········
Mounted at /content/drive
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;h.csv&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="&#47784;&#46304;-&#52972;&#47100;&#51060;--9999&#51064;&#44144;&#45716;-&#48260;&#47532;&#44256;-df&#50640;-&#51200;&#51109;">&#47784;&#46304; &#52972;&#47100;&#51060; -9999&#51064;&#44144;&#45716; &#48260;&#47532;&#44256; df&#50640; &#51200;&#51109;<a class="anchor-link" href="#&#47784;&#46304;-&#52972;&#47100;&#51060;--9999&#51064;&#44144;&#45716;-&#48260;&#47532;&#44256;-df&#50640;-&#51200;&#51109;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aa</span><span class="o">=</span><span class="mi">2</span>
<span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">aa</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="B_x,y,z,t-&#44032;--9999&#51060;&#44256;-Vp,Tp,Np-&#51473;-&#54616;&#45208;&#46972;&#46020;--9999&#51064;&#44163;-&#48260;&#47532;&#44592;">B_x,y,z,t &#44032; -9999&#51060;&#44256; Vp,Tp,Np &#51473; &#54616;&#45208;&#46972;&#46020; -9999&#51064;&#44163; &#48260;&#47532;&#44592;<a class="anchor-link" href="#B_x,y,z,t-&#44032;--9999&#51060;&#44256;-Vp,Tp,Np-&#51473;-&#54616;&#45208;&#46972;&#46020;--9999&#51064;&#44163;-&#48260;&#47532;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[73]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)]</span><span class="o">.</span><span class="n">index</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[63]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Vp</span>
<span class="n">df</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">214771</span><span class="p">,</span><span class="mi">214777</span><span class="p">,</span><span class="mi">214803</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">65144</span><span class="p">,</span><span class="mi">65146</span><span class="p">,</span><span class="mi">65147</span><span class="p">,</span><span class="mi">389829</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">804231</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[71]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Tp</span>
<span class="n">df</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">786138</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">213290</span><span class="p">,</span> <span class="mi">213291</span><span class="p">,</span> <span class="mi">213292</span><span class="p">,</span> <span class="mi">213293</span><span class="p">,</span> <span class="mi">213294</span><span class="p">,</span> <span class="mi">213295</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">79112</span><span class="p">,</span> <span class="mi">132860</span><span class="p">,</span> <span class="mi">132861</span><span class="p">,</span> <span class="mi">132862</span><span class="p">,</span> <span class="mi">132863</span><span class="p">,</span> <span class="mi">132864</span><span class="p">,</span> <span class="mi">132865</span><span class="p">,</span> <span class="mi">132866</span><span class="p">,</span>
            <span class="mi">132867</span><span class="p">,</span> <span class="mi">132868</span><span class="p">,</span> <span class="mi">132869</span><span class="p">,</span> <span class="mi">132870</span><span class="p">,</span> <span class="mi">132871</span><span class="p">,</span> <span class="mi">132872</span><span class="p">,</span> <span class="mi">258154</span><span class="p">,</span> <span class="mi">728427</span><span class="p">,</span>
            <span class="mi">728428</span><span class="p">,</span> <span class="mi">728429</span><span class="p">,</span> <span class="mi">728430</span><span class="p">,</span> <span class="mi">728431</span><span class="p">,</span> <span class="mi">728432</span><span class="p">,</span> <span class="mi">728433</span><span class="p">,</span> <span class="mi">728434</span><span class="p">,</span> <span class="mi">728435</span><span class="p">,</span>
            <span class="mi">728445</span><span class="p">,</span> <span class="mi">728446</span><span class="p">,</span> <span class="mi">728447</span><span class="p">,</span> <span class="mi">728448</span><span class="p">,</span> <span class="mi">728449</span><span class="p">,</span> <span class="mi">728450</span><span class="p">,</span> <span class="mi">728451</span><span class="p">,</span> <span class="mi">728452</span><span class="p">,</span>
            <span class="mi">790917</span><span class="p">,</span> <span class="mi">804189</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">599762</span><span class="p">,</span> <span class="mi">599763</span><span class="p">,</span> <span class="mi">728482</span><span class="p">,</span> <span class="mi">728483</span><span class="p">,</span> <span class="mi">728484</span><span class="p">,</span> <span class="mi">728485</span><span class="p">,</span> <span class="mi">728486</span><span class="p">,</span> <span class="mi">728487</span><span class="p">,</span>
            <span class="mi">728488</span><span class="p">,</span> <span class="mi">728489</span><span class="p">,</span> <span class="mi">728490</span><span class="p">,</span> <span class="mi">728491</span><span class="p">,</span> <span class="mi">728492</span><span class="p">,</span> <span class="mi">728493</span><span class="p">,</span> <span class="mi">728494</span><span class="p">,</span> <span class="mi">728495</span><span class="p">,</span>
            <span class="mi">728496</span><span class="p">,</span> <span class="mi">728497</span><span class="p">,</span> <span class="mi">728498</span><span class="p">,</span> <span class="mi">728499</span><span class="p">,</span> <span class="mi">728500</span><span class="p">,</span> <span class="mi">728501</span><span class="p">,</span> <span class="mi">728502</span><span class="p">,</span> <span class="mi">728505</span><span class="p">,</span>
            <span class="mi">728506</span><span class="p">,</span> <span class="mi">728507</span><span class="p">,</span> <span class="mi">728508</span><span class="p">,</span> <span class="mi">728509</span><span class="p">,</span> <span class="mi">728510</span><span class="p">,</span> <span class="mi">728511</span><span class="p">,</span> <span class="mi">728512</span><span class="p">,</span> <span class="mi">728513</span><span class="p">,</span>
            <span class="mi">728514</span><span class="p">,</span> <span class="mi">728515</span><span class="p">,</span> <span class="mi">728516</span><span class="p">,</span> <span class="mi">790534</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">797291</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">KeyError</span>                                  Traceback (most recent call last)
<span class="ansi-green-fg">&lt;ipython-input-71-1f8f763fad8b&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-fg">----&gt; 1</span><span class="ansi-red-fg"> </span>df<span class="ansi-blue-fg">[</span><span class="ansi-cyan-fg">3</span><span class="ansi-blue-fg">]</span><span class="ansi-blue-fg">.</span>drop<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">[</span><span class="ansi-cyan-fg">786138</span><span class="ansi-blue-fg">]</span><span class="ansi-blue-fg">,</span>inplace<span class="ansi-blue-fg">=</span><span class="ansi-green-fg">True</span><span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">      2</span> df<span class="ansi-blue-fg">[</span><span class="ansi-cyan-fg">4</span><span class="ansi-blue-fg">]</span><span class="ansi-blue-fg">.</span>drop<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">[</span><span class="ansi-cyan-fg">213290</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">213291</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">213292</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">213293</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">213294</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">213295</span><span class="ansi-blue-fg">]</span><span class="ansi-blue-fg">,</span>inplace<span class="ansi-blue-fg">=</span><span class="ansi-green-fg">True</span><span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">      3</span> df[5].drop([79112, 132860, 132861, 132862, 132863, 132864, 132865, 132866,
<span class="ansi-green-intense-fg ansi-bold">      4</span>             <span class="ansi-cyan-fg">132867</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">132868</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">132869</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">132870</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">132871</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">132872</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">258154</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728427</span><span class="ansi-blue-fg">,</span>
<span class="ansi-green-intense-fg ansi-bold">      5</span>             <span class="ansi-cyan-fg">728428</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728429</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728430</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728431</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728432</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728433</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728434</span><span class="ansi-blue-fg">,</span> <span class="ansi-cyan-fg">728435</span><span class="ansi-blue-fg">,</span>

<span class="ansi-green-fg">/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py</span> in <span class="ansi-cyan-fg">drop</span><span class="ansi-blue-fg">(self, labels, axis, index, columns, level, inplace, errors)</span>
<span class="ansi-green-intense-fg ansi-bold">   3938</span>                                            index<span class="ansi-blue-fg">=</span>index<span class="ansi-blue-fg">,</span> columns<span class="ansi-blue-fg">=</span>columns<span class="ansi-blue-fg">,</span>
<span class="ansi-green-intense-fg ansi-bold">   3939</span>                                            level<span class="ansi-blue-fg">=</span>level<span class="ansi-blue-fg">,</span> inplace<span class="ansi-blue-fg">=</span>inplace<span class="ansi-blue-fg">,</span>
<span class="ansi-green-fg">-&gt; 3940</span><span class="ansi-red-fg">                                            errors=errors)
</span><span class="ansi-green-intense-fg ansi-bold">   3941</span> 
<span class="ansi-green-intense-fg ansi-bold">   3942</span>     @rewrite_axis_style_signature(&#39;mapper&#39;, [(&#39;copy&#39;, True),

<span class="ansi-green-fg">/usr/local/lib/python3.6/dist-packages/pandas/core/generic.py</span> in <span class="ansi-cyan-fg">drop</span><span class="ansi-blue-fg">(self, labels, axis, index, columns, level, inplace, errors)</span>
<span class="ansi-green-intense-fg ansi-bold">   3778</span>         <span class="ansi-green-fg">for</span> axis<span class="ansi-blue-fg">,</span> labels <span class="ansi-green-fg">in</span> axes<span class="ansi-blue-fg">.</span>items<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-intense-fg ansi-bold">   3779</span>             <span class="ansi-green-fg">if</span> labels <span class="ansi-green-fg">is</span> <span class="ansi-green-fg">not</span> <span class="ansi-green-fg">None</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-fg">-&gt; 3780</span><span class="ansi-red-fg">                 </span>obj <span class="ansi-blue-fg">=</span> obj<span class="ansi-blue-fg">.</span>_drop_axis<span class="ansi-blue-fg">(</span>labels<span class="ansi-blue-fg">,</span> axis<span class="ansi-blue-fg">,</span> level<span class="ansi-blue-fg">=</span>level<span class="ansi-blue-fg">,</span> errors<span class="ansi-blue-fg">=</span>errors<span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">   3781</span> 
<span class="ansi-green-intense-fg ansi-bold">   3782</span>         <span class="ansi-green-fg">if</span> inplace<span class="ansi-blue-fg">:</span>

<span class="ansi-green-fg">/usr/local/lib/python3.6/dist-packages/pandas/core/generic.py</span> in <span class="ansi-cyan-fg">_drop_axis</span><span class="ansi-blue-fg">(self, labels, axis, level, errors)</span>
<span class="ansi-green-intense-fg ansi-bold">   3810</span>                 new_axis <span class="ansi-blue-fg">=</span> axis<span class="ansi-blue-fg">.</span>drop<span class="ansi-blue-fg">(</span>labels<span class="ansi-blue-fg">,</span> level<span class="ansi-blue-fg">=</span>level<span class="ansi-blue-fg">,</span> errors<span class="ansi-blue-fg">=</span>errors<span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">   3811</span>             <span class="ansi-green-fg">else</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-fg">-&gt; 3812</span><span class="ansi-red-fg">                 </span>new_axis <span class="ansi-blue-fg">=</span> axis<span class="ansi-blue-fg">.</span>drop<span class="ansi-blue-fg">(</span>labels<span class="ansi-blue-fg">,</span> errors<span class="ansi-blue-fg">=</span>errors<span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">   3813</span>             result <span class="ansi-blue-fg">=</span> self<span class="ansi-blue-fg">.</span>reindex<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">**</span><span class="ansi-blue-fg">{</span>axis_name<span class="ansi-blue-fg">:</span> new_axis<span class="ansi-blue-fg">}</span><span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">   3814</span> 

<span class="ansi-green-fg">/usr/local/lib/python3.6/dist-packages/pandas/core/indexes/base.py</span> in <span class="ansi-cyan-fg">drop</span><span class="ansi-blue-fg">(self, labels, errors)</span>
<span class="ansi-green-intense-fg ansi-bold">   4963</span>             <span class="ansi-green-fg">if</span> errors <span class="ansi-blue-fg">!=</span> <span class="ansi-blue-fg">&#39;ignore&#39;</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-intense-fg ansi-bold">   4964</span>                 raise KeyError(
<span class="ansi-green-fg">-&gt; 4965</span><span class="ansi-red-fg">                     &#39;{} not found in axis&#39;.format(labels[mask]))
</span><span class="ansi-green-intense-fg ansi-bold">   4966</span>             indexer <span class="ansi-blue-fg">=</span> indexer<span class="ansi-blue-fg">[</span><span class="ansi-blue-fg">~</span>mask<span class="ansi-blue-fg">]</span>
<span class="ansi-green-intense-fg ansi-bold">   4967</span>         <span class="ansi-green-fg">return</span> self<span class="ansi-blue-fg">.</span>delete<span class="ansi-blue-fg">(</span>indexer<span class="ansi-blue-fg">)</span>

<span class="ansi-red-fg">KeyError</span>: &#39;[786138] not found in axis&#39;</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[72]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Np</span>
<span class="n">df</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">787225</span><span class="p">,</span> <span class="mi">789494</span><span class="p">,</span> <span class="mi">850847</span><span class="p">,</span> <span class="mi">850848</span><span class="p">,</span> <span class="mi">850849</span><span class="p">,</span> <span class="mi">850850</span><span class="p">,</span> <span class="mi">850851</span><span class="p">,</span> <span class="mi">850852</span><span class="p">,</span>
            <span class="mi">850853</span><span class="p">,</span> <span class="mi">850854</span><span class="p">,</span> <span class="mi">850855</span><span class="p">,</span> <span class="mi">850856</span><span class="p">,</span> <span class="mi">850857</span><span class="p">,</span> <span class="mi">850859</span><span class="p">,</span> <span class="mi">850860</span><span class="p">,</span> <span class="mi">850861</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">786257</span><span class="p">,</span> <span class="mi">787767</span><span class="p">,</span> <span class="mi">788101</span><span class="p">,</span> <span class="mi">788767</span><span class="p">,</span> <span class="mi">788768</span><span class="p">,</span> <span class="mi">788769</span><span class="p">,</span> <span class="mi">788932</span><span class="p">,</span> <span class="mi">796790</span><span class="p">,</span>
            <span class="mi">796791</span><span class="p">,</span> <span class="mi">796792</span><span class="p">,</span> <span class="mi">796793</span><span class="p">,</span> <span class="mi">796794</span><span class="p">,</span> <span class="mi">796795</span><span class="p">,</span> <span class="mi">796796</span><span class="p">,</span> <span class="mi">796797</span><span class="p">,</span> <span class="mi">796798</span><span class="p">,</span>
            <span class="mi">796799</span><span class="p">,</span> <span class="mi">796800</span><span class="p">,</span> <span class="mi">796801</span><span class="p">,</span> <span class="mi">796802</span><span class="p">,</span> <span class="mi">796803</span><span class="p">,</span> <span class="mi">796804</span><span class="p">,</span> <span class="mi">796805</span><span class="p">,</span> <span class="mi">796806</span><span class="p">,</span>
            <span class="mi">796807</span><span class="p">,</span> <span class="mi">796808</span><span class="p">,</span> <span class="mi">796809</span><span class="p">,</span> <span class="mi">796810</span><span class="p">,</span> <span class="mi">796812</span><span class="p">,</span> <span class="mi">796813</span><span class="p">,</span> <span class="mi">796814</span><span class="p">,</span> <span class="mi">796815</span><span class="p">,</span>
            <span class="mi">796816</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">797218</span><span class="p">,</span> <span class="mi">797220</span><span class="p">,</span> <span class="mi">797221</span><span class="p">,</span> <span class="mi">797222</span><span class="p">,</span> <span class="mi">797223</span><span class="p">,</span> <span class="mi">797225</span><span class="p">,</span> <span class="mi">797226</span><span class="p">,</span> <span class="mi">797227</span><span class="p">,</span>
            <span class="mi">797228</span><span class="p">,</span> <span class="mi">797229</span><span class="p">,</span> <span class="mi">797230</span><span class="p">,</span> <span class="mi">797231</span><span class="p">,</span> <span class="mi">797232</span><span class="p">,</span> <span class="mi">797233</span><span class="p">,</span> <span class="mi">797234</span><span class="p">,</span> <span class="mi">797235</span><span class="p">,</span>
            <span class="mi">797236</span><span class="p">,</span> <span class="mi">797237</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">496406</span><span class="p">,</span> <span class="mi">641582</span><span class="p">,</span> <span class="mi">786640</span><span class="p">,</span> <span class="mi">789995</span><span class="p">,</span> <span class="mi">797239</span><span class="p">,</span> <span class="mi">797240</span><span class="p">,</span> <span class="mi">797241</span><span class="p">,</span> <span class="mi">797242</span><span class="p">,</span>
            <span class="mi">797243</span><span class="p">,</span> <span class="mi">797244</span><span class="p">,</span> <span class="mi">797245</span><span class="p">,</span> <span class="mi">797246</span><span class="p">,</span> <span class="mi">797247</span><span class="p">,</span> <span class="mi">797248</span><span class="p">,</span> <span class="mi">797249</span><span class="p">,</span> <span class="mi">797250</span><span class="p">,</span>
            <span class="mi">797252</span><span class="p">,</span> <span class="mi">797253</span><span class="p">,</span> <span class="mi">797254</span><span class="p">,</span> <span class="mi">797255</span><span class="p">,</span> <span class="mi">797256</span><span class="p">,</span> <span class="mi">797257</span><span class="p">,</span> <span class="mi">797258</span><span class="p">,</span> <span class="mi">797259</span><span class="p">,</span>
            <span class="mi">797260</span><span class="p">,</span> <span class="mi">797261</span><span class="p">,</span> <span class="mi">797262</span><span class="p">,</span> <span class="mi">797263</span><span class="p">,</span> <span class="mi">797264</span><span class="p">,</span> <span class="mi">797265</span><span class="p">,</span> <span class="mi">797266</span><span class="p">,</span> <span class="mi">797267</span><span class="p">,</span>
            <span class="mi">797268</span><span class="p">,</span> <span class="mi">797269</span><span class="p">,</span> <span class="mi">797270</span><span class="p">,</span> <span class="mi">797271</span><span class="p">,</span> <span class="mi">797272</span><span class="p">,</span> <span class="mi">797273</span><span class="p">,</span> <span class="mi">797274</span><span class="p">,</span> <span class="mi">797275</span><span class="p">,</span>
            <span class="mi">797276</span><span class="p">,</span> <span class="mi">797277</span><span class="p">,</span> <span class="mi">797278</span><span class="p">,</span> <span class="mi">797279</span><span class="p">,</span> <span class="mi">797280</span><span class="p">,</span> <span class="mi">797281</span><span class="p">,</span> <span class="mi">797283</span><span class="p">,</span> <span class="mi">797284</span><span class="p">,</span>
            <span class="mi">797285</span><span class="p">,</span> <span class="mi">797286</span><span class="p">,</span> <span class="mi">797287</span><span class="p">,</span> <span class="mi">797288</span><span class="p">,</span> <span class="mi">797289</span><span class="p">,</span> <span class="mi">797290</span><span class="p">,</span> <span class="mi">797292</span><span class="p">,</span> <span class="mi">797293</span><span class="p">,</span>
            <span class="mi">797294</span><span class="p">,</span> <span class="mi">797295</span><span class="p">,</span> <span class="mi">797296</span><span class="p">,</span> <span class="mi">797298</span><span class="p">,</span> <span class="mi">797299</span><span class="p">,</span> <span class="mi">797300</span><span class="p">,</span> <span class="mi">797301</span><span class="p">,</span> <span class="mi">797302</span><span class="p">,</span>
            <span class="mi">797303</span><span class="p">,</span> <span class="mi">797304</span><span class="p">,</span> <span class="mi">797305</span><span class="p">,</span> <span class="mi">797306</span><span class="p">,</span> <span class="mi">797307</span><span class="p">,</span> <span class="mi">797308</span><span class="p">,</span> <span class="mi">797309</span><span class="p">,</span> <span class="mi">797310</span><span class="p">,</span>
            <span class="mi">797311</span><span class="p">,</span> <span class="mi">797312</span><span class="p">,</span> <span class="mi">797314</span><span class="p">,</span> <span class="mi">797315</span><span class="p">,</span> <span class="mi">797316</span><span class="p">,</span> <span class="mi">797317</span><span class="p">,</span> <span class="mi">797318</span><span class="p">,</span> <span class="mi">797319</span><span class="p">,</span>
            <span class="mi">797320</span><span class="p">,</span> <span class="mi">797321</span><span class="p">,</span> <span class="mi">797322</span><span class="p">,</span> <span class="mi">797323</span><span class="p">,</span> <span class="mi">797324</span><span class="p">,</span> <span class="mi">797325</span><span class="p">,</span> <span class="mi">804213</span><span class="p">,</span> <span class="mi">804214</span><span class="p">,</span>
            <span class="mi">804216</span><span class="p">,</span> <span class="mi">804217</span><span class="p">,</span> <span class="mi">804218</span><span class="p">,</span> <span class="mi">925227</span><span class="p">,</span> <span class="mi">925230</span><span class="p">,</span> <span class="mi">925234</span><span class="p">,</span> <span class="mi">925389</span><span class="p">,</span> <span class="mi">925390</span><span class="p">,</span>
            <span class="mi">925391</span><span class="p">,</span> <span class="mi">925392</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="B&#47448;-&#50696;&#52769;&#54616;&#44592;-/&#51060;&#44144;&#45716;-train-set&#51060;&#44256;-test-&#49483;&#50640;&#45716;-B&#47448;--9999&#44032;-2&#44060;&#48150;&#50640;-&#50630;&#51004;&#48064;&#47196;-&#48260;&#47548;">B&#47448; &#50696;&#52769;&#54616;&#44592; /&#51060;&#44144;&#45716; train set&#51060;&#44256; test &#49483;&#50640;&#45716; B&#47448; -9999&#44032; 2&#44060;&#48150;&#50640; &#50630;&#51004;&#48064;&#47196; &#48260;&#47548;<a class="anchor-link" href="#B&#47448;-&#50696;&#52769;&#54616;&#44592;-/&#51060;&#44144;&#45716;-train-set&#51060;&#44256;-test-&#49483;&#50640;&#45716;-B&#47448;--9999&#44032;-2&#44060;&#48150;&#50640;-&#50630;&#51004;&#48064;&#47196;-&#48260;&#47548;">&#182;</a></h1><hr>
<h1 id="0&#44050;&#51008;-&#51032;&#48120;&#51080;&#45716;-&#44050;&#51060;&#46972;&#44256;-&#52628;&#51221;&#54616;&#44256;-&#50696;&#52769;&#49884;-&#51228;&#50808;&#54632;">0&#44050;&#51008; &#51032;&#48120;&#51080;&#45716; &#44050;&#51060;&#46972;&#44256; &#52628;&#51221;&#54616;&#44256; &#50696;&#52769;&#49884; &#51228;&#50808;&#54632;<a class="anchor-link" href="#0&#44050;&#51008;-&#51032;&#48120;&#51080;&#45716;-&#44050;&#51060;&#46972;&#44256;-&#52628;&#51221;&#54616;&#44256;-&#50696;&#52769;&#49884;-&#51228;&#50808;&#54632;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>

<span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="c1">#label rename 하기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[75]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(928557, 12)
(928170, 12)
(928109, 12)
(927907, 12)
(927994, 12)
(927881, 12)
(928337, 12)
(928625, 12)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[149]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">params</span><span class="o">=</span><span class="p">{</span>
    <span class="s1">&#39;boosting_type&#39;</span> <span class="p">:</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
    <span class="s1">&#39;objective&#39;</span><span class="p">:</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span>
    <span class="s1">&#39;num_tree&#39;</span><span class="p">:</span><span class="mi">10000</span><span class="p">,</span>
    <span class="s1">&#39;max_bin&#39;</span> <span class="p">:</span> <span class="mi">1000</span><span class="p">,</span>
    <span class="s1">&#39;max_depth&#39;</span> <span class="p">:</span><span class="mi">200</span><span class="p">,</span>
    <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
    <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.5</span><span class="p">,</span>
    <span class="s1">&#39;feature_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
    <span class="s1">&#39;bagging_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
    <span class="s1">&#39;bagging_freq&#39;</span><span class="p">:</span> <span class="mi">3</span><span class="p">,</span>    
    <span class="s1">&#39;num_leavs&#39;</span><span class="p">:</span> <span class="mi">10000</span><span class="p">,</span>
    <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">]</span>
<span class="p">}</span>  
<span class="n">check</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">3</span><span class="p">,</span><span class="mi">8</span><span class="p">):</span>
    
    <span class="c1">#data split</span>
    <span class="n">x_test</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)][[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;label&#39;</span><span class="p">]]</span>

    <span class="c1"># -9999 예측되어질 인덱스들에 대하여 모든 컬럼을 다가지고 있는 check컬럼을 선언</span>
    <span class="n">check</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)]</span>

    <span class="k">if</span> <span class="n">x_test</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">:</span>
      <span class="k">continue</span>
    <span class="n">train</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)][[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;label&#39;</span><span class="p">,</span><span class="n">col</span><span class="p">]]</span>

    <span class="c1">#x_test로 뽑힌 인덱스 버려서 나중에 합칠때 편하게 하기</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">x_test</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

    <span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">col</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">train</span><span class="p">[</span><span class="n">col</span><span class="p">],</span><span class="n">random_state</span><span class="o">=</span><span class="mi">940402</span><span class="p">,</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>

    <span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
    <span class="n">lgb_eval</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>

    <span class="c1">#model fit</span>
    <span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span><span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_eval</span><span class="p">,</span><span class="n">verbose_eval</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">30</span><span class="p">)</span>

    <span class="c1">#predict</span>
    <span class="n">pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
    <span class="n">check</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">pred</span>

    <span class="c1">#concat </span>
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">check</span><span class="p">[</span><span class="n">i</span><span class="p">]],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;번 &#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>  
  
  
  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/lightgbm/engine.py:118: UserWarning: Found `num_tree` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.11017
[200]	valid_0&#39;s l2: 5.21131
[300]	valid_0&#39;s l2: 4.30433
[400]	valid_0&#39;s l2: 3.65756
[500]	valid_0&#39;s l2: 3.23893
[600]	valid_0&#39;s l2: 2.96322
[700]	valid_0&#39;s l2: 2.75656
[800]	valid_0&#39;s l2: 2.58992
[900]	valid_0&#39;s l2: 2.44496
[1000]	valid_0&#39;s l2: 2.33281
[1100]	valid_0&#39;s l2: 2.2518
[1200]	valid_0&#39;s l2: 2.16439
[1300]	valid_0&#39;s l2: 2.10641
[1400]	valid_0&#39;s l2: 2.04308
[1500]	valid_0&#39;s l2: 1.98316
[1600]	valid_0&#39;s l2: 1.92762
[1700]	valid_0&#39;s l2: 1.89721
[1800]	valid_0&#39;s l2: 1.86887
[1900]	valid_0&#39;s l2: 1.83354
[2000]	valid_0&#39;s l2: 1.80346
[2100]	valid_0&#39;s l2: 1.77551
[2200]	valid_0&#39;s l2: 1.755
[2300]	valid_0&#39;s l2: 1.73548
[2400]	valid_0&#39;s l2: 1.71571
[2500]	valid_0&#39;s l2: 1.70151
[2600]	valid_0&#39;s l2: 1.6865
[2700]	valid_0&#39;s l2: 1.67807
[2800]	valid_0&#39;s l2: 1.66613
[2900]	valid_0&#39;s l2: 1.65561
[3000]	valid_0&#39;s l2: 1.64016
[3100]	valid_0&#39;s l2: 1.63018
[3200]	valid_0&#39;s l2: 1.62451
[3300]	valid_0&#39;s l2: 1.61845
[3400]	valid_0&#39;s l2: 1.6107
[3500]	valid_0&#39;s l2: 1.6022
[3600]	valid_0&#39;s l2: 1.59464
[3700]	valid_0&#39;s l2: 1.58305
[3800]	valid_0&#39;s l2: 1.58033
[3900]	valid_0&#39;s l2: 1.57226
[4000]	valid_0&#39;s l2: 1.56655
[4100]	valid_0&#39;s l2: 1.562
[4200]	valid_0&#39;s l2: 1.55798
[4300]	valid_0&#39;s l2: 1.55186
[4400]	valid_0&#39;s l2: 1.54846
Early stopping, best iteration is:
[4393]	valid_0&#39;s l2: 1.54809
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:43: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.31498
[200]	valid_0&#39;s l2: 5.49508
[300]	valid_0&#39;s l2: 4.47218
[400]	valid_0&#39;s l2: 3.79249
[500]	valid_0&#39;s l2: 3.35369
[600]	valid_0&#39;s l2: 3.05407
[700]	valid_0&#39;s l2: 2.83425
[800]	valid_0&#39;s l2: 2.65943
[900]	valid_0&#39;s l2: 2.53114
[1000]	valid_0&#39;s l2: 2.42471
[1100]	valid_0&#39;s l2: 2.35155
[1200]	valid_0&#39;s l2: 2.26955
[1300]	valid_0&#39;s l2: 2.20834
[1400]	valid_0&#39;s l2: 2.15124
[1500]	valid_0&#39;s l2: 2.09997
[1600]	valid_0&#39;s l2: 2.05401
[1700]	valid_0&#39;s l2: 2.00465
[1800]	valid_0&#39;s l2: 1.9707
[1900]	valid_0&#39;s l2: 1.93231
[2000]	valid_0&#39;s l2: 1.90727
[2100]	valid_0&#39;s l2: 1.8793
[2200]	valid_0&#39;s l2: 1.8531
[2300]	valid_0&#39;s l2: 1.83306
[2400]	valid_0&#39;s l2: 1.81074
[2500]	valid_0&#39;s l2: 1.79865
[2600]	valid_0&#39;s l2: 1.77777
[2700]	valid_0&#39;s l2: 1.76771
[2800]	valid_0&#39;s l2: 1.75153
[2900]	valid_0&#39;s l2: 1.7386
[3000]	valid_0&#39;s l2: 1.72688
[3100]	valid_0&#39;s l2: 1.71593
[3200]	valid_0&#39;s l2: 1.70599
[3300]	valid_0&#39;s l2: 1.6987
[3400]	valid_0&#39;s l2: 1.68769
[3500]	valid_0&#39;s l2: 1.67732
[3600]	valid_0&#39;s l2: 1.66757
[3700]	valid_0&#39;s l2: 1.66007
[3800]	valid_0&#39;s l2: 1.65256
[3900]	valid_0&#39;s l2: 1.64165
[4000]	valid_0&#39;s l2: 1.63416
[4100]	valid_0&#39;s l2: 1.62749
Early stopping, best iteration is:
[4151]	valid_0&#39;s l2: 1.62239
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.41692
[200]	valid_0&#39;s l2: 5.46624
[300]	valid_0&#39;s l2: 4.45361
[400]	valid_0&#39;s l2: 3.79479
[500]	valid_0&#39;s l2: 3.35423
[600]	valid_0&#39;s l2: 3.06934
[700]	valid_0&#39;s l2: 2.82037
[800]	valid_0&#39;s l2: 2.65033
[900]	valid_0&#39;s l2: 2.49328
[1000]	valid_0&#39;s l2: 2.38931
[1100]	valid_0&#39;s l2: 2.30674
[1200]	valid_0&#39;s l2: 2.23328
[1300]	valid_0&#39;s l2: 2.16946
[1400]	valid_0&#39;s l2: 2.12272
[1500]	valid_0&#39;s l2: 2.06462
[1600]	valid_0&#39;s l2: 2.02324
[1700]	valid_0&#39;s l2: 1.99004
[1800]	valid_0&#39;s l2: 1.95365
[1900]	valid_0&#39;s l2: 1.92113
[2000]	valid_0&#39;s l2: 1.88906
[2100]	valid_0&#39;s l2: 1.86493
[2200]	valid_0&#39;s l2: 1.84328
[2300]	valid_0&#39;s l2: 1.82134
[2400]	valid_0&#39;s l2: 1.8075
[2500]	valid_0&#39;s l2: 1.79394
[2600]	valid_0&#39;s l2: 1.77732
[2700]	valid_0&#39;s l2: 1.76017
[2800]	valid_0&#39;s l2: 1.74454
[2900]	valid_0&#39;s l2: 1.73051
[3000]	valid_0&#39;s l2: 1.71736
[3100]	valid_0&#39;s l2: 1.70718
[3200]	valid_0&#39;s l2: 1.6987
[3300]	valid_0&#39;s l2: 1.69242
[3400]	valid_0&#39;s l2: 1.68384
[3500]	valid_0&#39;s l2: 1.67558
[3600]	valid_0&#39;s l2: 1.66952
[3700]	valid_0&#39;s l2: 1.65989
[3800]	valid_0&#39;s l2: 1.6573
[3900]	valid_0&#39;s l2: 1.64879
[4000]	valid_0&#39;s l2: 1.64444
[4100]	valid_0&#39;s l2: 1.63991
[4200]	valid_0&#39;s l2: 1.63267
[4300]	valid_0&#39;s l2: 1.62767
[4400]	valid_0&#39;s l2: 1.62367
[4500]	valid_0&#39;s l2: 1.62109
[4600]	valid_0&#39;s l2: 1.6168
[4700]	valid_0&#39;s l2: 1.61142
[4800]	valid_0&#39;s l2: 1.60938
[4900]	valid_0&#39;s l2: 1.60567
[5000]	valid_0&#39;s l2: 1.6017
[5100]	valid_0&#39;s l2: 1.59834
[5200]	valid_0&#39;s l2: 1.59421
[5300]	valid_0&#39;s l2: 1.59099
[5400]	valid_0&#39;s l2: 1.58876
[5500]	valid_0&#39;s l2: 1.58592
Early stopping, best iteration is:
[5554]	valid_0&#39;s l2: 1.58276
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.54062
[200]	valid_0&#39;s l2: 5.68337
[300]	valid_0&#39;s l2: 4.61457
[400]	valid_0&#39;s l2: 3.93851
[500]	valid_0&#39;s l2: 3.53012
[600]	valid_0&#39;s l2: 3.22619
[700]	valid_0&#39;s l2: 2.99104
[800]	valid_0&#39;s l2: 2.81531
[900]	valid_0&#39;s l2: 2.68336
[1000]	valid_0&#39;s l2: 2.5737
[1100]	valid_0&#39;s l2: 2.47898
[1200]	valid_0&#39;s l2: 2.40012
[1300]	valid_0&#39;s l2: 2.33349
[1400]	valid_0&#39;s l2: 2.27822
[1500]	valid_0&#39;s l2: 2.22704
[1600]	valid_0&#39;s l2: 2.17367
[1700]	valid_0&#39;s l2: 2.13746
[1800]	valid_0&#39;s l2: 2.10515
[1900]	valid_0&#39;s l2: 2.06854
[2000]	valid_0&#39;s l2: 2.04023
[2100]	valid_0&#39;s l2: 2.02168
[2200]	valid_0&#39;s l2: 1.99351
[2300]	valid_0&#39;s l2: 1.97499
[2400]	valid_0&#39;s l2: 1.9568
[2500]	valid_0&#39;s l2: 1.93679
[2600]	valid_0&#39;s l2: 1.9213
[2700]	valid_0&#39;s l2: 1.9037
[2800]	valid_0&#39;s l2: 1.89245
[2900]	valid_0&#39;s l2: 1.87595
[3000]	valid_0&#39;s l2: 1.86376
[3100]	valid_0&#39;s l2: 1.85043
[3200]	valid_0&#39;s l2: 1.84123
[3300]	valid_0&#39;s l2: 1.83191
[3400]	valid_0&#39;s l2: 1.8217
[3500]	valid_0&#39;s l2: 1.81076
[3600]	valid_0&#39;s l2: 1.80325
[3700]	valid_0&#39;s l2: 1.79814
[3800]	valid_0&#39;s l2: 1.78867
[3900]	valid_0&#39;s l2: 1.77978
[4000]	valid_0&#39;s l2: 1.77087
[4100]	valid_0&#39;s l2: 1.76614
[4200]	valid_0&#39;s l2: 1.75758
[4300]	valid_0&#39;s l2: 1.75108
[4400]	valid_0&#39;s l2: 1.74491
[4500]	valid_0&#39;s l2: 1.74183
[4600]	valid_0&#39;s l2: 1.73637
[4700]	valid_0&#39;s l2: 1.7325
Early stopping, best iteration is:
[4747]	valid_0&#39;s l2: 1.7302
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.56821
[200]	valid_0&#39;s l2: 5.60969
[300]	valid_0&#39;s l2: 4.51218
[400]	valid_0&#39;s l2: 3.90206
[500]	valid_0&#39;s l2: 3.46422
[600]	valid_0&#39;s l2: 3.13924
[700]	valid_0&#39;s l2: 2.92463
[800]	valid_0&#39;s l2: 2.75955
[900]	valid_0&#39;s l2: 2.61959
[1000]	valid_0&#39;s l2: 2.50774
[1100]	valid_0&#39;s l2: 2.43938
[1200]	valid_0&#39;s l2: 2.36909
[1300]	valid_0&#39;s l2: 2.29743
[1400]	valid_0&#39;s l2: 2.22463
[1500]	valid_0&#39;s l2: 2.16007
[1600]	valid_0&#39;s l2: 2.12379
[1700]	valid_0&#39;s l2: 2.08687
[1800]	valid_0&#39;s l2: 2.0502
[1900]	valid_0&#39;s l2: 2.02379
[2000]	valid_0&#39;s l2: 2.00042
[2100]	valid_0&#39;s l2: 1.96943
[2200]	valid_0&#39;s l2: 1.94651
[2300]	valid_0&#39;s l2: 1.92581
[2400]	valid_0&#39;s l2: 1.9058
[2500]	valid_0&#39;s l2: 1.88579
[2600]	valid_0&#39;s l2: 1.87082
[2700]	valid_0&#39;s l2: 1.85713
[2800]	valid_0&#39;s l2: 1.84326
[2900]	valid_0&#39;s l2: 1.82766
[3000]	valid_0&#39;s l2: 1.81527
[3100]	valid_0&#39;s l2: 1.80409
[3200]	valid_0&#39;s l2: 1.79686
[3300]	valid_0&#39;s l2: 1.78754
[3400]	valid_0&#39;s l2: 1.77585
[3500]	valid_0&#39;s l2: 1.76607
[3600]	valid_0&#39;s l2: 1.75818
[3700]	valid_0&#39;s l2: 1.74983
[3800]	valid_0&#39;s l2: 1.74357
[3900]	valid_0&#39;s l2: 1.73452
[4000]	valid_0&#39;s l2: 1.72822
[4100]	valid_0&#39;s l2: 1.72251
[4200]	valid_0&#39;s l2: 1.71741
[4300]	valid_0&#39;s l2: 1.71289
[4400]	valid_0&#39;s l2: 1.7073
[4500]	valid_0&#39;s l2: 1.70187
[4600]	valid_0&#39;s l2: 1.69849
Early stopping, best iteration is:
[4626]	valid_0&#39;s l2: 1.69568
7번 B_gsm_x done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 8.84821
[200]	valid_0&#39;s l2: 6.96359
[300]	valid_0&#39;s l2: 5.98032
[400]	valid_0&#39;s l2: 5.30939
[500]	valid_0&#39;s l2: 4.80668
[600]	valid_0&#39;s l2: 4.50161
[700]	valid_0&#39;s l2: 4.22336
[800]	valid_0&#39;s l2: 4.03858
[900]	valid_0&#39;s l2: 3.90625
[1000]	valid_0&#39;s l2: 3.72654
[1100]	valid_0&#39;s l2: 3.65103
[1200]	valid_0&#39;s l2: 3.5397
[1300]	valid_0&#39;s l2: 3.46129
[1400]	valid_0&#39;s l2: 3.39476
[1500]	valid_0&#39;s l2: 3.32923
[1600]	valid_0&#39;s l2: 3.29126
[1700]	valid_0&#39;s l2: 3.24752
[1800]	valid_0&#39;s l2: 3.20907
[1900]	valid_0&#39;s l2: 3.16964
[2000]	valid_0&#39;s l2: 3.13595
[2100]	valid_0&#39;s l2: 3.10504
[2200]	valid_0&#39;s l2: 3.07389
[2300]	valid_0&#39;s l2: 3.05393
[2400]	valid_0&#39;s l2: 3.02058
[2500]	valid_0&#39;s l2: 2.99975
[2600]	valid_0&#39;s l2: 2.98455
[2700]	valid_0&#39;s l2: 2.9647
[2800]	valid_0&#39;s l2: 2.94751
[2900]	valid_0&#39;s l2: 2.92698
[3000]	valid_0&#39;s l2: 2.90624
[3100]	valid_0&#39;s l2: 2.89012
[3200]	valid_0&#39;s l2: 2.88047
[3300]	valid_0&#39;s l2: 2.86809
[3400]	valid_0&#39;s l2: 2.85182
Early stopping, best iteration is:
[3413]	valid_0&#39;s l2: 2.85081
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 9.06342
[200]	valid_0&#39;s l2: 7.1056
[300]	valid_0&#39;s l2: 6.0902
[400]	valid_0&#39;s l2: 5.3414
[500]	valid_0&#39;s l2: 4.87816
[600]	valid_0&#39;s l2: 4.58567
[700]	valid_0&#39;s l2: 4.35933
[800]	valid_0&#39;s l2: 4.1811
[900]	valid_0&#39;s l2: 4.01834
[1000]	valid_0&#39;s l2: 3.89126
[1100]	valid_0&#39;s l2: 3.80971
[1200]	valid_0&#39;s l2: 3.72948
[1300]	valid_0&#39;s l2: 3.65729
[1400]	valid_0&#39;s l2: 3.59203
[1500]	valid_0&#39;s l2: 3.50458
[1600]	valid_0&#39;s l2: 3.44119
[1700]	valid_0&#39;s l2: 3.38161
[1800]	valid_0&#39;s l2: 3.32703
[1900]	valid_0&#39;s l2: 3.29471
[2000]	valid_0&#39;s l2: 3.25314
[2100]	valid_0&#39;s l2: 3.22416
[2200]	valid_0&#39;s l2: 3.2003
[2300]	valid_0&#39;s l2: 3.17199
[2400]	valid_0&#39;s l2: 3.13919
[2500]	valid_0&#39;s l2: 3.10926
[2600]	valid_0&#39;s l2: 3.08909
[2700]	valid_0&#39;s l2: 3.07472
[2800]	valid_0&#39;s l2: 3.05616
[2900]	valid_0&#39;s l2: 3.0376
[3000]	valid_0&#39;s l2: 3.01698
[3100]	valid_0&#39;s l2: 2.99969
[3200]	valid_0&#39;s l2: 2.98182
[3300]	valid_0&#39;s l2: 2.96961
[3400]	valid_0&#39;s l2: 2.9529
[3500]	valid_0&#39;s l2: 2.94023
[3600]	valid_0&#39;s l2: 2.93203
[3700]	valid_0&#39;s l2: 2.9207
Early stopping, best iteration is:
[3738]	valid_0&#39;s l2: 2.91704
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 9.53327
[200]	valid_0&#39;s l2: 7.45785
[300]	valid_0&#39;s l2: 6.2536
[400]	valid_0&#39;s l2: 5.52958
[500]	valid_0&#39;s l2: 5.05055
[600]	valid_0&#39;s l2: 4.70682
[700]	valid_0&#39;s l2: 4.47507
[800]	valid_0&#39;s l2: 4.24538
[900]	valid_0&#39;s l2: 4.10768
[1000]	valid_0&#39;s l2: 3.99463
[1100]	valid_0&#39;s l2: 3.89402
[1200]	valid_0&#39;s l2: 3.78926
[1300]	valid_0&#39;s l2: 3.69997
[1400]	valid_0&#39;s l2: 3.61859
[1500]	valid_0&#39;s l2: 3.55144
[1600]	valid_0&#39;s l2: 3.49698
[1700]	valid_0&#39;s l2: 3.44301
[1800]	valid_0&#39;s l2: 3.3999
[1900]	valid_0&#39;s l2: 3.36621
[2000]	valid_0&#39;s l2: 3.33909
[2100]	valid_0&#39;s l2: 3.31256
[2200]	valid_0&#39;s l2: 3.28173
[2300]	valid_0&#39;s l2: 3.26041
[2400]	valid_0&#39;s l2: 3.22618
[2500]	valid_0&#39;s l2: 3.20736
[2600]	valid_0&#39;s l2: 3.17813
[2700]	valid_0&#39;s l2: 3.16172
[2800]	valid_0&#39;s l2: 3.14721
[2900]	valid_0&#39;s l2: 3.12987
[3000]	valid_0&#39;s l2: 3.11268
[3100]	valid_0&#39;s l2: 3.09676
[3200]	valid_0&#39;s l2: 3.08747
Early stopping, best iteration is:
[3220]	valid_0&#39;s l2: 3.08385
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 9.68195
[200]	valid_0&#39;s l2: 7.58844
[300]	valid_0&#39;s l2: 6.52195
[400]	valid_0&#39;s l2: 5.70957
[500]	valid_0&#39;s l2: 5.18571
[600]	valid_0&#39;s l2: 4.86845
[700]	valid_0&#39;s l2: 4.58884
[800]	valid_0&#39;s l2: 4.40167
[900]	valid_0&#39;s l2: 4.24688
[1000]	valid_0&#39;s l2: 4.09279
[1100]	valid_0&#39;s l2: 4.0033
[1200]	valid_0&#39;s l2: 3.92348
[1300]	valid_0&#39;s l2: 3.8475
[1400]	valid_0&#39;s l2: 3.79348
[1500]	valid_0&#39;s l2: 3.72665
[1600]	valid_0&#39;s l2: 3.65958
[1700]	valid_0&#39;s l2: 3.62571
[1800]	valid_0&#39;s l2: 3.58239
[1900]	valid_0&#39;s l2: 3.54251
[2000]	valid_0&#39;s l2: 3.50417
[2100]	valid_0&#39;s l2: 3.46321
[2200]	valid_0&#39;s l2: 3.43113
[2300]	valid_0&#39;s l2: 3.4092
[2400]	valid_0&#39;s l2: 3.38159
[2500]	valid_0&#39;s l2: 3.35496
[2600]	valid_0&#39;s l2: 3.33419
[2700]	valid_0&#39;s l2: 3.31353
[2800]	valid_0&#39;s l2: 3.30296
[2900]	valid_0&#39;s l2: 3.28243
[3000]	valid_0&#39;s l2: 3.2593
[3100]	valid_0&#39;s l2: 3.24113
[3200]	valid_0&#39;s l2: 3.22665
[3300]	valid_0&#39;s l2: 3.2122
[3400]	valid_0&#39;s l2: 3.19745
[3500]	valid_0&#39;s l2: 3.18631
[3600]	valid_0&#39;s l2: 3.17856
[3700]	valid_0&#39;s l2: 3.1743
Early stopping, best iteration is:
[3757]	valid_0&#39;s l2: 3.16629
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 9.30265
[200]	valid_0&#39;s l2: 7.23433
[300]	valid_0&#39;s l2: 6.26375
[400]	valid_0&#39;s l2: 5.52563
[500]	valid_0&#39;s l2: 5.01127
[600]	valid_0&#39;s l2: 4.72956
[700]	valid_0&#39;s l2: 4.43365
[800]	valid_0&#39;s l2: 4.27227
[900]	valid_0&#39;s l2: 4.12102
[1000]	valid_0&#39;s l2: 4.0013
[1100]	valid_0&#39;s l2: 3.88267
[1200]	valid_0&#39;s l2: 3.80287
[1300]	valid_0&#39;s l2: 3.72229
[1400]	valid_0&#39;s l2: 3.64742
[1500]	valid_0&#39;s l2: 3.58318
[1600]	valid_0&#39;s l2: 3.52467
[1700]	valid_0&#39;s l2: 3.4787
[1800]	valid_0&#39;s l2: 3.43254
[1900]	valid_0&#39;s l2: 3.39692
[2000]	valid_0&#39;s l2: 3.36155
[2100]	valid_0&#39;s l2: 3.33589
[2200]	valid_0&#39;s l2: 3.30189
[2300]	valid_0&#39;s l2: 3.27069
[2400]	valid_0&#39;s l2: 3.24855
[2500]	valid_0&#39;s l2: 3.22284
[2600]	valid_0&#39;s l2: 3.20694
[2700]	valid_0&#39;s l2: 3.19268
[2800]	valid_0&#39;s l2: 3.17057
[2900]	valid_0&#39;s l2: 3.1484
[3000]	valid_0&#39;s l2: 3.13453
[3100]	valid_0&#39;s l2: 3.12014
[3200]	valid_0&#39;s l2: 3.10279
[3300]	valid_0&#39;s l2: 3.09398
[3400]	valid_0&#39;s l2: 3.07959
[3500]	valid_0&#39;s l2: 3.06349
[3600]	valid_0&#39;s l2: 3.05706
[3700]	valid_0&#39;s l2: 3.0486
[3800]	valid_0&#39;s l2: 3.04207
[3900]	valid_0&#39;s l2: 3.03262
[4000]	valid_0&#39;s l2: 3.02191
[4100]	valid_0&#39;s l2: 3.02012
Early stopping, best iteration is:
[4073]	valid_0&#39;s l2: 3.0186
7번 B_gsm_y done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 6.98319
[200]	valid_0&#39;s l2: 5.95525
[300]	valid_0&#39;s l2: 5.38658
[400]	valid_0&#39;s l2: 4.98846
[500]	valid_0&#39;s l2: 4.69541
[600]	valid_0&#39;s l2: 4.48101
[700]	valid_0&#39;s l2: 4.28991
[800]	valid_0&#39;s l2: 4.14064
[900]	valid_0&#39;s l2: 4.0112
[1000]	valid_0&#39;s l2: 3.90989
[1100]	valid_0&#39;s l2: 3.8215
[1200]	valid_0&#39;s l2: 3.74648
[1300]	valid_0&#39;s l2: 3.66598
[1400]	valid_0&#39;s l2: 3.6084
[1500]	valid_0&#39;s l2: 3.55058
[1600]	valid_0&#39;s l2: 3.50931
[1700]	valid_0&#39;s l2: 3.4809
[1800]	valid_0&#39;s l2: 3.44829
[1900]	valid_0&#39;s l2: 3.41139
[2000]	valid_0&#39;s l2: 3.37999
[2100]	valid_0&#39;s l2: 3.34667
[2200]	valid_0&#39;s l2: 3.3166
[2300]	valid_0&#39;s l2: 3.29548
[2400]	valid_0&#39;s l2: 3.2757
[2500]	valid_0&#39;s l2: 3.25961
[2600]	valid_0&#39;s l2: 3.24379
[2700]	valid_0&#39;s l2: 3.22216
Early stopping, best iteration is:
[2763]	valid_0&#39;s l2: 3.21296
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.15755
[200]	valid_0&#39;s l2: 6.01127
[300]	valid_0&#39;s l2: 5.35576
[400]	valid_0&#39;s l2: 4.93971
[500]	valid_0&#39;s l2: 4.64231
[600]	valid_0&#39;s l2: 4.44773
[700]	valid_0&#39;s l2: 4.26282
[800]	valid_0&#39;s l2: 4.11791
[900]	valid_0&#39;s l2: 3.98192
[1000]	valid_0&#39;s l2: 3.86602
[1100]	valid_0&#39;s l2: 3.78777
[1200]	valid_0&#39;s l2: 3.71649
[1300]	valid_0&#39;s l2: 3.66415
[1400]	valid_0&#39;s l2: 3.61536
[1500]	valid_0&#39;s l2: 3.56043
[1600]	valid_0&#39;s l2: 3.51915
[1700]	valid_0&#39;s l2: 3.48
[1800]	valid_0&#39;s l2: 3.45425
[1900]	valid_0&#39;s l2: 3.4235
[2000]	valid_0&#39;s l2: 3.39887
[2100]	valid_0&#39;s l2: 3.36441
[2200]	valid_0&#39;s l2: 3.34297
[2300]	valid_0&#39;s l2: 3.31418
[2400]	valid_0&#39;s l2: 3.29238
[2500]	valid_0&#39;s l2: 3.26597
[2600]	valid_0&#39;s l2: 3.24581
[2700]	valid_0&#39;s l2: 3.23069
[2800]	valid_0&#39;s l2: 3.21743
[2900]	valid_0&#39;s l2: 3.1977
[3000]	valid_0&#39;s l2: 3.17646
Early stopping, best iteration is:
[3009]	valid_0&#39;s l2: 3.17447
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.50568
[200]	valid_0&#39;s l2: 6.28105
[300]	valid_0&#39;s l2: 5.63287
[400]	valid_0&#39;s l2: 5.1388
[500]	valid_0&#39;s l2: 4.76765
[600]	valid_0&#39;s l2: 4.55574
[700]	valid_0&#39;s l2: 4.37182
[800]	valid_0&#39;s l2: 4.19275
[900]	valid_0&#39;s l2: 4.06625
[1000]	valid_0&#39;s l2: 3.95933
[1100]	valid_0&#39;s l2: 3.8832
[1200]	valid_0&#39;s l2: 3.80401
[1300]	valid_0&#39;s l2: 3.75346
[1400]	valid_0&#39;s l2: 3.70054
[1500]	valid_0&#39;s l2: 3.63819
[1600]	valid_0&#39;s l2: 3.59981
[1700]	valid_0&#39;s l2: 3.55766
[1800]	valid_0&#39;s l2: 3.5226
[1900]	valid_0&#39;s l2: 3.49288
[2000]	valid_0&#39;s l2: 3.45919
[2100]	valid_0&#39;s l2: 3.42865
[2200]	valid_0&#39;s l2: 3.39915
[2300]	valid_0&#39;s l2: 3.37304
[2400]	valid_0&#39;s l2: 3.34739
[2500]	valid_0&#39;s l2: 3.32578
[2600]	valid_0&#39;s l2: 3.30378
Early stopping, best iteration is:
[2629]	valid_0&#39;s l2: 3.29941
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.4921
[200]	valid_0&#39;s l2: 6.41432
[300]	valid_0&#39;s l2: 5.78271
[400]	valid_0&#39;s l2: 5.34948
[500]	valid_0&#39;s l2: 4.99743
[600]	valid_0&#39;s l2: 4.80151
[700]	valid_0&#39;s l2: 4.60163
[800]	valid_0&#39;s l2: 4.44232
[900]	valid_0&#39;s l2: 4.32986
[1000]	valid_0&#39;s l2: 4.22867
[1100]	valid_0&#39;s l2: 4.14762
[1200]	valid_0&#39;s l2: 4.06304
[1300]	valid_0&#39;s l2: 3.98019
[1400]	valid_0&#39;s l2: 3.90264
[1500]	valid_0&#39;s l2: 3.84346
[1600]	valid_0&#39;s l2: 3.80357
[1700]	valid_0&#39;s l2: 3.76513
[1800]	valid_0&#39;s l2: 3.73228
[1900]	valid_0&#39;s l2: 3.70029
[2000]	valid_0&#39;s l2: 3.66425
[2100]	valid_0&#39;s l2: 3.63979
[2200]	valid_0&#39;s l2: 3.61065
[2300]	valid_0&#39;s l2: 3.58524
[2400]	valid_0&#39;s l2: 3.56036
[2500]	valid_0&#39;s l2: 3.53765
[2600]	valid_0&#39;s l2: 3.5183
[2700]	valid_0&#39;s l2: 3.50517
[2800]	valid_0&#39;s l2: 3.49482
[2900]	valid_0&#39;s l2: 3.47418
[3000]	valid_0&#39;s l2: 3.45749
[3100]	valid_0&#39;s l2: 3.44549
[3200]	valid_0&#39;s l2: 3.44044
Early stopping, best iteration is:
[3221]	valid_0&#39;s l2: 3.43467
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.00765
[200]	valid_0&#39;s l2: 6.004
[300]	valid_0&#39;s l2: 5.36456
[400]	valid_0&#39;s l2: 4.94381
[500]	valid_0&#39;s l2: 4.62909
[600]	valid_0&#39;s l2: 4.39896
[700]	valid_0&#39;s l2: 4.2391
[800]	valid_0&#39;s l2: 4.06804
[900]	valid_0&#39;s l2: 3.95586
[1000]	valid_0&#39;s l2: 3.85681
[1100]	valid_0&#39;s l2: 3.7862
[1200]	valid_0&#39;s l2: 3.71621
[1300]	valid_0&#39;s l2: 3.66204
[1400]	valid_0&#39;s l2: 3.60761
[1500]	valid_0&#39;s l2: 3.55313
[1600]	valid_0&#39;s l2: 3.51052
[1700]	valid_0&#39;s l2: 3.47819
[1800]	valid_0&#39;s l2: 3.44895
[1900]	valid_0&#39;s l2: 3.41774
[2000]	valid_0&#39;s l2: 3.39181
[2100]	valid_0&#39;s l2: 3.36152
[2200]	valid_0&#39;s l2: 3.3421
[2300]	valid_0&#39;s l2: 3.32212
[2400]	valid_0&#39;s l2: 3.29622
[2500]	valid_0&#39;s l2: 3.2747
Early stopping, best iteration is:
[2519]	valid_0&#39;s l2: 3.2735
7번 B_gsm_z done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 2.26187
[200]	valid_0&#39;s l2: 1.59578
[300]	valid_0&#39;s l2: 1.28473
[400]	valid_0&#39;s l2: 1.11442
[500]	valid_0&#39;s l2: 0.980415
[600]	valid_0&#39;s l2: 0.875541
[700]	valid_0&#39;s l2: 0.799067
[800]	valid_0&#39;s l2: 0.746079
[900]	valid_0&#39;s l2: 0.701211
[1000]	valid_0&#39;s l2: 0.665788
[1100]	valid_0&#39;s l2: 0.641867
[1200]	valid_0&#39;s l2: 0.621471
[1300]	valid_0&#39;s l2: 0.603202
[1400]	valid_0&#39;s l2: 0.585699
[1500]	valid_0&#39;s l2: 0.569365
[1600]	valid_0&#39;s l2: 0.559033
[1700]	valid_0&#39;s l2: 0.548374
[1800]	valid_0&#39;s l2: 0.539189
[1900]	valid_0&#39;s l2: 0.528749
[2000]	valid_0&#39;s l2: 0.523537
[2100]	valid_0&#39;s l2: 0.514747
[2200]	valid_0&#39;s l2: 0.507887
[2300]	valid_0&#39;s l2: 0.502041
[2400]	valid_0&#39;s l2: 0.496789
[2500]	valid_0&#39;s l2: 0.492395
[2600]	valid_0&#39;s l2: 0.487962
[2700]	valid_0&#39;s l2: 0.483678
[2800]	valid_0&#39;s l2: 0.481068
[2900]	valid_0&#39;s l2: 0.476791
[3000]	valid_0&#39;s l2: 0.47336
[3100]	valid_0&#39;s l2: 0.469824
[3200]	valid_0&#39;s l2: 0.46817
[3300]	valid_0&#39;s l2: 0.465554
[3400]	valid_0&#39;s l2: 0.462791
[3500]	valid_0&#39;s l2: 0.460149
[3600]	valid_0&#39;s l2: 0.457489
[3700]	valid_0&#39;s l2: 0.455367
[3800]	valid_0&#39;s l2: 0.452613
[3900]	valid_0&#39;s l2: 0.450851
[4000]	valid_0&#39;s l2: 0.448548
[4100]	valid_0&#39;s l2: 0.447182
[4200]	valid_0&#39;s l2: 0.446199
Early stopping, best iteration is:
[4254]	valid_0&#39;s l2: 0.445285
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 2.12374
[200]	valid_0&#39;s l2: 1.47428
[300]	valid_0&#39;s l2: 1.20912
[400]	valid_0&#39;s l2: 1.01092
[500]	valid_0&#39;s l2: 0.868842
[600]	valid_0&#39;s l2: 0.789911
[700]	valid_0&#39;s l2: 0.727961
[800]	valid_0&#39;s l2: 0.686226
[900]	valid_0&#39;s l2: 0.655643
[1000]	valid_0&#39;s l2: 0.62438
[1100]	valid_0&#39;s l2: 0.602656
[1200]	valid_0&#39;s l2: 0.581746
[1300]	valid_0&#39;s l2: 0.565121
[1400]	valid_0&#39;s l2: 0.550987
[1500]	valid_0&#39;s l2: 0.538164
[1600]	valid_0&#39;s l2: 0.527609
[1700]	valid_0&#39;s l2: 0.516078
[1800]	valid_0&#39;s l2: 0.505598
[1900]	valid_0&#39;s l2: 0.495512
[2000]	valid_0&#39;s l2: 0.489068
[2100]	valid_0&#39;s l2: 0.482479
[2200]	valid_0&#39;s l2: 0.476154
[2300]	valid_0&#39;s l2: 0.470433
[2400]	valid_0&#39;s l2: 0.465705
[2500]	valid_0&#39;s l2: 0.462147
[2600]	valid_0&#39;s l2: 0.458343
[2700]	valid_0&#39;s l2: 0.454081
[2800]	valid_0&#39;s l2: 0.450156
[2900]	valid_0&#39;s l2: 0.446959
[3000]	valid_0&#39;s l2: 0.443728
[3100]	valid_0&#39;s l2: 0.441964
[3200]	valid_0&#39;s l2: 0.439792
[3300]	valid_0&#39;s l2: 0.438033
[3400]	valid_0&#39;s l2: 0.435165
[3500]	valid_0&#39;s l2: 0.43356
[3600]	valid_0&#39;s l2: 0.43242
[3700]	valid_0&#39;s l2: 0.430788
[3800]	valid_0&#39;s l2: 0.428679
[3900]	valid_0&#39;s l2: 0.427423
[4000]	valid_0&#39;s l2: 0.426004
[4100]	valid_0&#39;s l2: 0.424697
[4200]	valid_0&#39;s l2: 0.42383
[4300]	valid_0&#39;s l2: 0.422722
Early stopping, best iteration is:
[4284]	valid_0&#39;s l2: 0.422662
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 2.25282
[200]	valid_0&#39;s l2: 1.58427
[300]	valid_0&#39;s l2: 1.27987
[400]	valid_0&#39;s l2: 1.09747
[500]	valid_0&#39;s l2: 0.955875
[600]	valid_0&#39;s l2: 0.870956
[700]	valid_0&#39;s l2: 0.799458
[800]	valid_0&#39;s l2: 0.749473
[900]	valid_0&#39;s l2: 0.711608
[1000]	valid_0&#39;s l2: 0.675473
[1100]	valid_0&#39;s l2: 0.647822
[1200]	valid_0&#39;s l2: 0.628935
[1300]	valid_0&#39;s l2: 0.613768
[1400]	valid_0&#39;s l2: 0.598677
[1500]	valid_0&#39;s l2: 0.581115
[1600]	valid_0&#39;s l2: 0.569599
[1700]	valid_0&#39;s l2: 0.557755
[1800]	valid_0&#39;s l2: 0.544041
[1900]	valid_0&#39;s l2: 0.5346
[2000]	valid_0&#39;s l2: 0.526208
[2100]	valid_0&#39;s l2: 0.521136
[2200]	valid_0&#39;s l2: 0.515526
[2300]	valid_0&#39;s l2: 0.509385
[2400]	valid_0&#39;s l2: 0.504028
[2500]	valid_0&#39;s l2: 0.50018
[2600]	valid_0&#39;s l2: 0.496512
[2700]	valid_0&#39;s l2: 0.492877
[2800]	valid_0&#39;s l2: 0.488579
[2900]	valid_0&#39;s l2: 0.484756
[3000]	valid_0&#39;s l2: 0.481008
[3100]	valid_0&#39;s l2: 0.477199
[3200]	valid_0&#39;s l2: 0.47494
[3300]	valid_0&#39;s l2: 0.472575
[3400]	valid_0&#39;s l2: 0.47023
[3500]	valid_0&#39;s l2: 0.466969
[3600]	valid_0&#39;s l2: 0.465259
[3700]	valid_0&#39;s l2: 0.462226
[3800]	valid_0&#39;s l2: 0.460881
[3900]	valid_0&#39;s l2: 0.458898
[4000]	valid_0&#39;s l2: 0.456882
[4100]	valid_0&#39;s l2: 0.456048
[4200]	valid_0&#39;s l2: 0.453588
Early stopping, best iteration is:
[4200]	valid_0&#39;s l2: 0.453588
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 2.2808
[200]	valid_0&#39;s l2: 1.67441
[300]	valid_0&#39;s l2: 1.32737
[400]	valid_0&#39;s l2: 1.11866
[500]	valid_0&#39;s l2: 0.985384
[600]	valid_0&#39;s l2: 0.899545
[700]	valid_0&#39;s l2: 0.826655
[800]	valid_0&#39;s l2: 0.773469
[900]	valid_0&#39;s l2: 0.727927
[1000]	valid_0&#39;s l2: 0.69919
[1100]	valid_0&#39;s l2: 0.671871
[1200]	valid_0&#39;s l2: 0.651104
[1300]	valid_0&#39;s l2: 0.633268
[1400]	valid_0&#39;s l2: 0.620469
[1500]	valid_0&#39;s l2: 0.606647
[1600]	valid_0&#39;s l2: 0.595304
[1700]	valid_0&#39;s l2: 0.584929
[1800]	valid_0&#39;s l2: 0.575713
[1900]	valid_0&#39;s l2: 0.566888
[2000]	valid_0&#39;s l2: 0.559979
[2100]	valid_0&#39;s l2: 0.552938
[2200]	valid_0&#39;s l2: 0.546785
[2300]	valid_0&#39;s l2: 0.540112
[2400]	valid_0&#39;s l2: 0.53371
[2500]	valid_0&#39;s l2: 0.529082
[2600]	valid_0&#39;s l2: 0.524438
[2700]	valid_0&#39;s l2: 0.520946
[2800]	valid_0&#39;s l2: 0.517023
[2900]	valid_0&#39;s l2: 0.51357
[3000]	valid_0&#39;s l2: 0.51021
[3100]	valid_0&#39;s l2: 0.505696
[3200]	valid_0&#39;s l2: 0.504413
[3300]	valid_0&#39;s l2: 0.50249
[3400]	valid_0&#39;s l2: 0.499262
[3500]	valid_0&#39;s l2: 0.496408
[3600]	valid_0&#39;s l2: 0.495014
[3700]	valid_0&#39;s l2: 0.493398
[3800]	valid_0&#39;s l2: 0.491223
[3900]	valid_0&#39;s l2: 0.488654
[4000]	valid_0&#39;s l2: 0.487046
[4100]	valid_0&#39;s l2: 0.4856
[4200]	valid_0&#39;s l2: 0.48445
[4300]	valid_0&#39;s l2: 0.482843
[4400]	valid_0&#39;s l2: 0.481699
[4500]	valid_0&#39;s l2: 0.480847
Early stopping, best iteration is:
[4479]	valid_0&#39;s l2: 0.480616
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 2.30623
[200]	valid_0&#39;s l2: 1.6471
[300]	valid_0&#39;s l2: 1.32422
[400]	valid_0&#39;s l2: 1.13929
[500]	valid_0&#39;s l2: 0.992491
[600]	valid_0&#39;s l2: 0.907366
[700]	valid_0&#39;s l2: 0.832275
[800]	valid_0&#39;s l2: 0.782871
[900]	valid_0&#39;s l2: 0.7468
[1000]	valid_0&#39;s l2: 0.713123
[1100]	valid_0&#39;s l2: 0.687006
[1200]	valid_0&#39;s l2: 0.659031
[1300]	valid_0&#39;s l2: 0.640148
[1400]	valid_0&#39;s l2: 0.624093
[1500]	valid_0&#39;s l2: 0.603873
[1600]	valid_0&#39;s l2: 0.591756
[1700]	valid_0&#39;s l2: 0.579807
[1800]	valid_0&#39;s l2: 0.571304
[1900]	valid_0&#39;s l2: 0.565141
[2000]	valid_0&#39;s l2: 0.559602
[2100]	valid_0&#39;s l2: 0.550936
[2200]	valid_0&#39;s l2: 0.542173
[2300]	valid_0&#39;s l2: 0.535517
[2400]	valid_0&#39;s l2: 0.528461
[2500]	valid_0&#39;s l2: 0.523182
[2600]	valid_0&#39;s l2: 0.519252
[2700]	valid_0&#39;s l2: 0.515393
[2800]	valid_0&#39;s l2: 0.510105
[2900]	valid_0&#39;s l2: 0.507461
[3000]	valid_0&#39;s l2: 0.503972
[3100]	valid_0&#39;s l2: 0.500403
[3200]	valid_0&#39;s l2: 0.497912
[3300]	valid_0&#39;s l2: 0.495115
[3400]	valid_0&#39;s l2: 0.492732
[3500]	valid_0&#39;s l2: 0.489587
[3600]	valid_0&#39;s l2: 0.488103
[3700]	valid_0&#39;s l2: 0.486622
[3800]	valid_0&#39;s l2: 0.484777
[3900]	valid_0&#39;s l2: 0.482751
[4000]	valid_0&#39;s l2: 0.480721
[4100]	valid_0&#39;s l2: 0.478354
[4200]	valid_0&#39;s l2: 0.47689
[4300]	valid_0&#39;s l2: 0.475746
[4400]	valid_0&#39;s l2: 0.474166
[4500]	valid_0&#39;s l2: 0.473077
[4600]	valid_0&#39;s l2: 0.471846
[4700]	valid_0&#39;s l2: 0.470051
[4800]	valid_0&#39;s l2: 0.468714
[4900]	valid_0&#39;s l2: 0.467432
[5000]	valid_0&#39;s l2: 0.466119
[5100]	valid_0&#39;s l2: 0.464835
[5200]	valid_0&#39;s l2: 0.463918
[5300]	valid_0&#39;s l2: 0.462842
Early stopping, best iteration is:
[5324]	valid_0&#39;s l2: 0.462806
7번 Bt done
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[155]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">check</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[155]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>year</th>
      <th>doy</th>
      <th>hr</th>
      <th>min</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>496388</th>
      <td>2007.0</td>
      <td>20.0</td>
      <td>21.0</td>
      <td>0.0</td>
      <td>2.462</td>
      <td>115820.0</td>
      <td>583.13</td>
      <td>0.192584</td>
      <td>1.480775</td>
      <td>0.479461</td>
      <td>3.640368</td>
      <td>2</td>
    </tr>
    <tr>
      <th>496389</th>
      <td>2007.0</td>
      <td>20.0</td>
      <td>21.0</td>
      <td>1.0</td>
      <td>2.438</td>
      <td>107930.0</td>
      <td>581.63</td>
      <td>0.320210</td>
      <td>1.414192</td>
      <td>0.914061</td>
      <td>4.011678</td>
      <td>2</td>
    </tr>
    <tr>
      <th>496390</th>
      <td>2007.0</td>
      <td>20.0</td>
      <td>21.0</td>
      <td>3.0</td>
      <td>2.328</td>
      <td>113290.0</td>
      <td>576.65</td>
      <td>0.194595</td>
      <td>2.364749</td>
      <td>0.155719</td>
      <td>2.984831</td>
      <td>2</td>
    </tr>
    <tr>
      <th>496391</th>
      <td>2007.0</td>
      <td>20.0</td>
      <td>21.0</td>
      <td>4.0</td>
      <td>2.509</td>
      <td>120240.0</td>
      <td>579.64</td>
      <td>-0.165472</td>
      <td>2.451408</td>
      <td>0.777541</td>
      <td>2.959381</td>
      <td>2</td>
    </tr>
    <tr>
      <th>496392</th>
      <td>2007.0</td>
      <td>20.0</td>
      <td>21.0</td>
      <td>5.0</td>
      <td>2.900</td>
      <td>119090.0</td>
      <td>573.74</td>
      <td>0.603447</td>
      <td>0.944823</td>
      <td>0.970436</td>
      <td>3.130773</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[180]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#save csv</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_B_nan_csv/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aa</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_B_nan_csv/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="P&#47448;-&#50696;&#52769;&#54616;&#44592;-/-P&#47448;&#44032;--9999&#51060;&#47732;&#49436;-B&#47448;&#46020;--9999&#51064;&#44148;-&#50630;&#51020;">P&#47448; &#50696;&#52769;&#54616;&#44592; / P&#47448;&#44032; -9999&#51060;&#47732;&#49436; B&#47448;&#46020; -9999&#51064;&#44148; &#50630;&#51020;<a class="anchor-link" href="#P&#47448;-&#50696;&#52769;&#54616;&#44592;-/-P&#47448;&#44032;--9999&#51060;&#47732;&#49436;-B&#47448;&#46020;--9999&#51064;&#44148;-&#50630;&#51020;">&#182;</a></h1><hr>
<h1 id="&#46608;&#54620;-P&#47448;&#45716;-0&#44050;&#51060;-&#50630;&#51020;">&#46608;&#54620; P&#47448;&#45716; 0&#44050;&#51060; &#50630;&#51020;<a class="anchor-link" href="#&#46608;&#54620;-P&#47448;&#45716;-0&#44050;&#51060;-&#50630;&#51020;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">before</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_B_nan_csv/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">before</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[111]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>

<span class="n">params</span><span class="o">=</span><span class="p">{</span>
    <span class="s1">&#39;boosting_type&#39;</span> <span class="p">:</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
    <span class="s1">&#39;objective&#39;</span><span class="p">:</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span>
    <span class="s1">&#39;num_tree&#39;</span><span class="p">:</span><span class="mi">10000</span><span class="p">,</span>
    <span class="s1">&#39;max_bin&#39;</span> <span class="p">:</span> <span class="mi">1000</span><span class="p">,</span>
    <span class="s1">&#39;max_depth&#39;</span> <span class="p">:</span><span class="mi">200</span><span class="p">,</span>
    <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
    <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.5</span><span class="p">,</span>
    <span class="s1">&#39;feature_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
    <span class="s1">&#39;bagging_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
    <span class="s1">&#39;bagging_freq&#39;</span><span class="p">:</span> <span class="mi">3</span><span class="p">,</span>    
    <span class="s1">&#39;num_leavs&#39;</span><span class="p">:</span> <span class="mi">10000</span><span class="p">,</span>
    <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">]</span>
<span class="p">}</span>  
<span class="n">Vp_model</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Np_model</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Tp_model</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">check</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">]:</span>

  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
    <span class="n">x_test</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">][[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">]]</span>
    <span class="n">check</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">]</span>
    <span class="k">if</span> <span class="n">x_test</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">==</span> <span class="mi">0</span> <span class="p">:</span>
      <span class="k">continue</span>
    <span class="n">train</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">][[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">,</span><span class="n">col</span><span class="p">]]</span>
    
    
    
    <span class="n">train</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="n">col</span><span class="p">])</span>
    
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">x_test</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    
    <span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">col</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">train</span><span class="p">[</span><span class="n">col</span><span class="p">],</span><span class="n">random_state</span><span class="o">=</span><span class="mi">940402</span><span class="p">,</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
    <span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
    <span class="n">lgb_eval</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>
    
    <span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span><span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_eval</span><span class="p">,</span><span class="n">verbose_eval</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">30</span><span class="p">)</span>
    
    <span class="n">pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
    <span class="c1">#log 다시 exp로</span>
    <span class="n">pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="n">pred</span><span class="p">)</span>
    
    <span class="n">check</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">pred</span>
    
    
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">Vp_model</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="n">Np_model</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
    <span class="k">else</span> <span class="p">:</span>
      <span class="n">Tp_model</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
    
    
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">check</span><span class="p">[</span><span class="n">i</span><span class="p">]],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    
    <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;번 &#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/lightgbm/engine.py:118: UserWarning: Found `num_tree` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.333879
[200]	valid_0&#39;s l2: 0.273366
[300]	valid_0&#39;s l2: 0.238809
[400]	valid_0&#39;s l2: 0.21303
[500]	valid_0&#39;s l2: 0.195198
[600]	valid_0&#39;s l2: 0.182911
[700]	valid_0&#39;s l2: 0.172994
[800]	valid_0&#39;s l2: 0.166645
[900]	valid_0&#39;s l2: 0.160226
[1000]	valid_0&#39;s l2: 0.155119
[1100]	valid_0&#39;s l2: 0.150799
[1200]	valid_0&#39;s l2: 0.146515
[1300]	valid_0&#39;s l2: 0.143216
[1400]	valid_0&#39;s l2: 0.140155
[1500]	valid_0&#39;s l2: 0.136929
[1600]	valid_0&#39;s l2: 0.135196
[1700]	valid_0&#39;s l2: 0.133339
[1800]	valid_0&#39;s l2: 0.131583
[1900]	valid_0&#39;s l2: 0.130172
[2000]	valid_0&#39;s l2: 0.128409
[2100]	valid_0&#39;s l2: 0.12739
[2200]	valid_0&#39;s l2: 0.126201
[2300]	valid_0&#39;s l2: 0.125198
[2400]	valid_0&#39;s l2: 0.124
[2500]	valid_0&#39;s l2: 0.123002
[2600]	valid_0&#39;s l2: 0.122261
[2700]	valid_0&#39;s l2: 0.121627
[2800]	valid_0&#39;s l2: 0.120909
[2900]	valid_0&#39;s l2: 0.120272
[3000]	valid_0&#39;s l2: 0.119635
[3100]	valid_0&#39;s l2: 0.119037
[3200]	valid_0&#39;s l2: 0.118612
Early stopping, best iteration is:
[3253]	valid_0&#39;s l2: 0.11835
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:48: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>0번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.336663
[200]	valid_0&#39;s l2: 0.277085
[300]	valid_0&#39;s l2: 0.240395
[400]	valid_0&#39;s l2: 0.215361
[500]	valid_0&#39;s l2: 0.198458
[600]	valid_0&#39;s l2: 0.186363
[700]	valid_0&#39;s l2: 0.17573
[800]	valid_0&#39;s l2: 0.167505
[900]	valid_0&#39;s l2: 0.160697
[1000]	valid_0&#39;s l2: 0.155864
[1100]	valid_0&#39;s l2: 0.151794
[1200]	valid_0&#39;s l2: 0.147833
[1300]	valid_0&#39;s l2: 0.144388
[1400]	valid_0&#39;s l2: 0.1413
[1500]	valid_0&#39;s l2: 0.138119
[1600]	valid_0&#39;s l2: 0.13611
[1700]	valid_0&#39;s l2: 0.133872
[1800]	valid_0&#39;s l2: 0.132303
[1900]	valid_0&#39;s l2: 0.130985
[2000]	valid_0&#39;s l2: 0.129807
[2100]	valid_0&#39;s l2: 0.128435
[2200]	valid_0&#39;s l2: 0.127153
[2300]	valid_0&#39;s l2: 0.126097
[2400]	valid_0&#39;s l2: 0.125122
[2500]	valid_0&#39;s l2: 0.124379
[2600]	valid_0&#39;s l2: 0.123589
[2700]	valid_0&#39;s l2: 0.122887
[2800]	valid_0&#39;s l2: 0.122413
[2900]	valid_0&#39;s l2: 0.121792
[3000]	valid_0&#39;s l2: 0.121058
[3100]	valid_0&#39;s l2: 0.120185
[3200]	valid_0&#39;s l2: 0.11954
[3300]	valid_0&#39;s l2: 0.119126
[3400]	valid_0&#39;s l2: 0.118469
[3500]	valid_0&#39;s l2: 0.117865
Early stopping, best iteration is:
[3517]	valid_0&#39;s l2: 0.117665
1번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.337146
[200]	valid_0&#39;s l2: 0.274535
[300]	valid_0&#39;s l2: 0.243015
[400]	valid_0&#39;s l2: 0.217974
[500]	valid_0&#39;s l2: 0.199539
[600]	valid_0&#39;s l2: 0.189476
[700]	valid_0&#39;s l2: 0.17954
[800]	valid_0&#39;s l2: 0.172121
[900]	valid_0&#39;s l2: 0.166232
[1000]	valid_0&#39;s l2: 0.160918
[1100]	valid_0&#39;s l2: 0.15682
[1200]	valid_0&#39;s l2: 0.152831
[1300]	valid_0&#39;s l2: 0.149652
[1400]	valid_0&#39;s l2: 0.146177
[1500]	valid_0&#39;s l2: 0.143646
[1600]	valid_0&#39;s l2: 0.141534
[1700]	valid_0&#39;s l2: 0.138925
[1800]	valid_0&#39;s l2: 0.137077
[1900]	valid_0&#39;s l2: 0.135209
[2000]	valid_0&#39;s l2: 0.134007
[2100]	valid_0&#39;s l2: 0.132682
[2200]	valid_0&#39;s l2: 0.131393
[2300]	valid_0&#39;s l2: 0.130182
[2400]	valid_0&#39;s l2: 0.129388
[2500]	valid_0&#39;s l2: 0.128645
[2600]	valid_0&#39;s l2: 0.127626
[2700]	valid_0&#39;s l2: 0.126837
[2800]	valid_0&#39;s l2: 0.126285
[2900]	valid_0&#39;s l2: 0.125477
[3000]	valid_0&#39;s l2: 0.124682
[3100]	valid_0&#39;s l2: 0.124168
[3200]	valid_0&#39;s l2: 0.123515
Early stopping, best iteration is:
[3252]	valid_0&#39;s l2: 0.123335
2번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.346626
[200]	valid_0&#39;s l2: 0.282245
[300]	valid_0&#39;s l2: 0.245835
[400]	valid_0&#39;s l2: 0.222636
[500]	valid_0&#39;s l2: 0.204216
[600]	valid_0&#39;s l2: 0.192673
[700]	valid_0&#39;s l2: 0.181168
[800]	valid_0&#39;s l2: 0.173646
[900]	valid_0&#39;s l2: 0.166409
[1000]	valid_0&#39;s l2: 0.160747
[1100]	valid_0&#39;s l2: 0.156408
[1200]	valid_0&#39;s l2: 0.152987
[1300]	valid_0&#39;s l2: 0.14994
[1400]	valid_0&#39;s l2: 0.147263
[1500]	valid_0&#39;s l2: 0.144659
[1600]	valid_0&#39;s l2: 0.142692
[1700]	valid_0&#39;s l2: 0.140257
[1800]	valid_0&#39;s l2: 0.138646
[1900]	valid_0&#39;s l2: 0.137052
[2000]	valid_0&#39;s l2: 0.135552
[2100]	valid_0&#39;s l2: 0.133636
[2200]	valid_0&#39;s l2: 0.132361
[2300]	valid_0&#39;s l2: 0.131234
[2400]	valid_0&#39;s l2: 0.130276
[2500]	valid_0&#39;s l2: 0.129392
[2600]	valid_0&#39;s l2: 0.128504
[2700]	valid_0&#39;s l2: 0.127832
[2800]	valid_0&#39;s l2: 0.127205
[2900]	valid_0&#39;s l2: 0.126429
[3000]	valid_0&#39;s l2: 0.125727
[3100]	valid_0&#39;s l2: 0.124952
[3200]	valid_0&#39;s l2: 0.124465
Early stopping, best iteration is:
[3231]	valid_0&#39;s l2: 0.12444
3번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.338556
[200]	valid_0&#39;s l2: 0.277452
[300]	valid_0&#39;s l2: 0.240759
[400]	valid_0&#39;s l2: 0.218196
[500]	valid_0&#39;s l2: 0.200503
[600]	valid_0&#39;s l2: 0.189404
[700]	valid_0&#39;s l2: 0.179238
[800]	valid_0&#39;s l2: 0.17152
[900]	valid_0&#39;s l2: 0.165185
[1000]	valid_0&#39;s l2: 0.159905
[1100]	valid_0&#39;s l2: 0.15571
[1200]	valid_0&#39;s l2: 0.151761
[1300]	valid_0&#39;s l2: 0.149019
[1400]	valid_0&#39;s l2: 0.145584
[1500]	valid_0&#39;s l2: 0.142623
[1600]	valid_0&#39;s l2: 0.140967
[1700]	valid_0&#39;s l2: 0.139224
[1800]	valid_0&#39;s l2: 0.137579
[1900]	valid_0&#39;s l2: 0.135582
[2000]	valid_0&#39;s l2: 0.134076
[2100]	valid_0&#39;s l2: 0.132639
[2200]	valid_0&#39;s l2: 0.1315
[2300]	valid_0&#39;s l2: 0.130442
[2400]	valid_0&#39;s l2: 0.129366
[2500]	valid_0&#39;s l2: 0.128453
[2600]	valid_0&#39;s l2: 0.12778
[2700]	valid_0&#39;s l2: 0.127181
[2800]	valid_0&#39;s l2: 0.126416
[2900]	valid_0&#39;s l2: 0.125589
[3000]	valid_0&#39;s l2: 0.124887
[3100]	valid_0&#39;s l2: 0.124139
[3200]	valid_0&#39;s l2: 0.123652
Early stopping, best iteration is:
[3265]	valid_0&#39;s l2: 0.123363
4번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.338974
[200]	valid_0&#39;s l2: 0.277451
[300]	valid_0&#39;s l2: 0.240751
[400]	valid_0&#39;s l2: 0.218437
[500]	valid_0&#39;s l2: 0.20176
[600]	valid_0&#39;s l2: 0.189394
[700]	valid_0&#39;s l2: 0.179675
[800]	valid_0&#39;s l2: 0.172221
[900]	valid_0&#39;s l2: 0.165416
[1000]	valid_0&#39;s l2: 0.160487
[1100]	valid_0&#39;s l2: 0.156191
[1200]	valid_0&#39;s l2: 0.152312
[1300]	valid_0&#39;s l2: 0.148612
[1400]	valid_0&#39;s l2: 0.145994
[1500]	valid_0&#39;s l2: 0.14316
[1600]	valid_0&#39;s l2: 0.140521
[1700]	valid_0&#39;s l2: 0.13818
[1800]	valid_0&#39;s l2: 0.136511
[1900]	valid_0&#39;s l2: 0.135011
[2000]	valid_0&#39;s l2: 0.133367
[2100]	valid_0&#39;s l2: 0.131807
[2200]	valid_0&#39;s l2: 0.130727
[2300]	valid_0&#39;s l2: 0.129526
[2400]	valid_0&#39;s l2: 0.128388
[2500]	valid_0&#39;s l2: 0.127496
[2600]	valid_0&#39;s l2: 0.126575
[2700]	valid_0&#39;s l2: 0.125758
[2800]	valid_0&#39;s l2: 0.124902
[2900]	valid_0&#39;s l2: 0.124377
[3000]	valid_0&#39;s l2: 0.12345
[3100]	valid_0&#39;s l2: 0.122881
[3200]	valid_0&#39;s l2: 0.122398
[3300]	valid_0&#39;s l2: 0.121807
[3400]	valid_0&#39;s l2: 0.121189
[3500]	valid_0&#39;s l2: 0.120743
[3600]	valid_0&#39;s l2: 0.120316
[3700]	valid_0&#39;s l2: 0.119804
[3800]	valid_0&#39;s l2: 0.119355
[3900]	valid_0&#39;s l2: 0.119015
Early stopping, best iteration is:
[3966]	valid_0&#39;s l2: 0.118757
5번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.334459
[200]	valid_0&#39;s l2: 0.274944
[300]	valid_0&#39;s l2: 0.23991
[400]	valid_0&#39;s l2: 0.215704
[500]	valid_0&#39;s l2: 0.198425
[600]	valid_0&#39;s l2: 0.18656
[700]	valid_0&#39;s l2: 0.176177
[800]	valid_0&#39;s l2: 0.169417
[900]	valid_0&#39;s l2: 0.162861
[1000]	valid_0&#39;s l2: 0.156767
[1100]	valid_0&#39;s l2: 0.152308
[1200]	valid_0&#39;s l2: 0.148167
[1300]	valid_0&#39;s l2: 0.145283
[1400]	valid_0&#39;s l2: 0.14232
[1500]	valid_0&#39;s l2: 0.139896
[1600]	valid_0&#39;s l2: 0.137878
[1700]	valid_0&#39;s l2: 0.135641
[1800]	valid_0&#39;s l2: 0.134214
[1900]	valid_0&#39;s l2: 0.132078
[2000]	valid_0&#39;s l2: 0.130819
[2100]	valid_0&#39;s l2: 0.129648
[2200]	valid_0&#39;s l2: 0.128607
[2300]	valid_0&#39;s l2: 0.127526
[2400]	valid_0&#39;s l2: 0.126657
[2500]	valid_0&#39;s l2: 0.125715
[2600]	valid_0&#39;s l2: 0.125002
[2700]	valid_0&#39;s l2: 0.124247
[2800]	valid_0&#39;s l2: 0.123528
[2900]	valid_0&#39;s l2: 0.122706
[3000]	valid_0&#39;s l2: 0.121877
[3100]	valid_0&#39;s l2: 0.121149
[3200]	valid_0&#39;s l2: 0.120661
[3300]	valid_0&#39;s l2: 0.120447
[3400]	valid_0&#39;s l2: 0.11982
[3500]	valid_0&#39;s l2: 0.119246
[3600]	valid_0&#39;s l2: 0.118893
[3700]	valid_0&#39;s l2: 0.118482
[3800]	valid_0&#39;s l2: 0.118004
[3900]	valid_0&#39;s l2: 0.117611
[4000]	valid_0&#39;s l2: 0.117392
[4100]	valid_0&#39;s l2: 0.117073
[4200]	valid_0&#39;s l2: 0.116745
[4300]	valid_0&#39;s l2: 0.116605
Early stopping, best iteration is:
[4274]	valid_0&#39;s l2: 0.116576
6번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.339272
[200]	valid_0&#39;s l2: 0.279949
[300]	valid_0&#39;s l2: 0.246581
[400]	valid_0&#39;s l2: 0.223035
[500]	valid_0&#39;s l2: 0.204583
[600]	valid_0&#39;s l2: 0.192117
[700]	valid_0&#39;s l2: 0.181813
[800]	valid_0&#39;s l2: 0.17451
[900]	valid_0&#39;s l2: 0.168789
[1000]	valid_0&#39;s l2: 0.163256
[1100]	valid_0&#39;s l2: 0.158988
[1200]	valid_0&#39;s l2: 0.154724
[1300]	valid_0&#39;s l2: 0.151336
[1400]	valid_0&#39;s l2: 0.148305
[1500]	valid_0&#39;s l2: 0.145493
[1600]	valid_0&#39;s l2: 0.143045
[1700]	valid_0&#39;s l2: 0.141242
[1800]	valid_0&#39;s l2: 0.139602
[1900]	valid_0&#39;s l2: 0.138128
[2000]	valid_0&#39;s l2: 0.136684
[2100]	valid_0&#39;s l2: 0.135271
[2200]	valid_0&#39;s l2: 0.134188
[2300]	valid_0&#39;s l2: 0.133086
[2400]	valid_0&#39;s l2: 0.132019
[2500]	valid_0&#39;s l2: 0.131174
[2600]	valid_0&#39;s l2: 0.130293
[2700]	valid_0&#39;s l2: 0.12911
[2800]	valid_0&#39;s l2: 0.128345
[2900]	valid_0&#39;s l2: 0.127844
[3000]	valid_0&#39;s l2: 0.127109
[3100]	valid_0&#39;s l2: 0.126672
Early stopping, best iteration is:
[3111]	valid_0&#39;s l2: 0.126577
7번 Tp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.207731
[200]	valid_0&#39;s l2: 0.171134
[300]	valid_0&#39;s l2: 0.14909
[400]	valid_0&#39;s l2: 0.133807
[500]	valid_0&#39;s l2: 0.122327
[600]	valid_0&#39;s l2: 0.115273
[700]	valid_0&#39;s l2: 0.109875
[800]	valid_0&#39;s l2: 0.105815
[900]	valid_0&#39;s l2: 0.101934
[1000]	valid_0&#39;s l2: 0.0984638
[1100]	valid_0&#39;s l2: 0.0959231
[1200]	valid_0&#39;s l2: 0.0936442
[1300]	valid_0&#39;s l2: 0.091585
[1400]	valid_0&#39;s l2: 0.0900883
[1500]	valid_0&#39;s l2: 0.0886601
[1600]	valid_0&#39;s l2: 0.0873018
[1700]	valid_0&#39;s l2: 0.0861321
[1800]	valid_0&#39;s l2: 0.0851223
[1900]	valid_0&#39;s l2: 0.0842161
[2000]	valid_0&#39;s l2: 0.0832766
[2100]	valid_0&#39;s l2: 0.082529
[2200]	valid_0&#39;s l2: 0.0818922
[2300]	valid_0&#39;s l2: 0.0811678
[2400]	valid_0&#39;s l2: 0.0805403
[2500]	valid_0&#39;s l2: 0.0798866
[2600]	valid_0&#39;s l2: 0.0795361
[2700]	valid_0&#39;s l2: 0.0791133
[2800]	valid_0&#39;s l2: 0.0788366
[2900]	valid_0&#39;s l2: 0.0783267
[3000]	valid_0&#39;s l2: 0.0777464
[3100]	valid_0&#39;s l2: 0.0773338
[3200]	valid_0&#39;s l2: 0.0772743
[3300]	valid_0&#39;s l2: 0.0770727
[3400]	valid_0&#39;s l2: 0.0769264
Early stopping, best iteration is:
[3444]	valid_0&#39;s l2: 0.0768389
0번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.201888
[200]	valid_0&#39;s l2: 0.166793
[300]	valid_0&#39;s l2: 0.145535
[400]	valid_0&#39;s l2: 0.130802
[500]	valid_0&#39;s l2: 0.120024
[600]	valid_0&#39;s l2: 0.112199
[700]	valid_0&#39;s l2: 0.106725
[800]	valid_0&#39;s l2: 0.102615
[900]	valid_0&#39;s l2: 0.0994579
[1000]	valid_0&#39;s l2: 0.0966921
[1100]	valid_0&#39;s l2: 0.094286
[1200]	valid_0&#39;s l2: 0.0925489
[1300]	valid_0&#39;s l2: 0.0909522
[1400]	valid_0&#39;s l2: 0.0890587
[1500]	valid_0&#39;s l2: 0.0875603
[1600]	valid_0&#39;s l2: 0.0863109
[1700]	valid_0&#39;s l2: 0.085025
[1800]	valid_0&#39;s l2: 0.0841876
[1900]	valid_0&#39;s l2: 0.0833023
[2000]	valid_0&#39;s l2: 0.0823468
[2100]	valid_0&#39;s l2: 0.0815165
[2200]	valid_0&#39;s l2: 0.0809248
[2300]	valid_0&#39;s l2: 0.0803425
[2400]	valid_0&#39;s l2: 0.0799305
[2500]	valid_0&#39;s l2: 0.0795345
[2600]	valid_0&#39;s l2: 0.0790795
[2700]	valid_0&#39;s l2: 0.0786688
[2800]	valid_0&#39;s l2: 0.0783228
[2900]	valid_0&#39;s l2: 0.0780407
[3000]	valid_0&#39;s l2: 0.0775944
[3100]	valid_0&#39;s l2: 0.0771698
Early stopping, best iteration is:
[3109]	valid_0&#39;s l2: 0.0771215
1번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.204642
[200]	valid_0&#39;s l2: 0.166831
[300]	valid_0&#39;s l2: 0.145905
[400]	valid_0&#39;s l2: 0.130961
[500]	valid_0&#39;s l2: 0.121868
[600]	valid_0&#39;s l2: 0.115005
[700]	valid_0&#39;s l2: 0.108952
[800]	valid_0&#39;s l2: 0.104961
[900]	valid_0&#39;s l2: 0.101077
[1000]	valid_0&#39;s l2: 0.0979533
[1100]	valid_0&#39;s l2: 0.0950084
[1200]	valid_0&#39;s l2: 0.0930539
[1300]	valid_0&#39;s l2: 0.0915401
[1400]	valid_0&#39;s l2: 0.0898566
[1500]	valid_0&#39;s l2: 0.0884833
[1600]	valid_0&#39;s l2: 0.0872277
[1700]	valid_0&#39;s l2: 0.0858733
[1800]	valid_0&#39;s l2: 0.0848
[1900]	valid_0&#39;s l2: 0.0840045
[2000]	valid_0&#39;s l2: 0.0832922
[2100]	valid_0&#39;s l2: 0.0823473
[2200]	valid_0&#39;s l2: 0.0819552
[2300]	valid_0&#39;s l2: 0.0813873
[2400]	valid_0&#39;s l2: 0.0807381
[2500]	valid_0&#39;s l2: 0.0802176
[2600]	valid_0&#39;s l2: 0.0798329
[2700]	valid_0&#39;s l2: 0.0794356
[2800]	valid_0&#39;s l2: 0.079014
[2900]	valid_0&#39;s l2: 0.0787065
[3000]	valid_0&#39;s l2: 0.0783956
[3100]	valid_0&#39;s l2: 0.0779754
Early stopping, best iteration is:
[3126]	valid_0&#39;s l2: 0.0778599
2번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.20827
[200]	valid_0&#39;s l2: 0.171893
[300]	valid_0&#39;s l2: 0.148516
[400]	valid_0&#39;s l2: 0.131739
[500]	valid_0&#39;s l2: 0.121809
[600]	valid_0&#39;s l2: 0.114625
[700]	valid_0&#39;s l2: 0.108801
[800]	valid_0&#39;s l2: 0.104602
[900]	valid_0&#39;s l2: 0.100345
[1000]	valid_0&#39;s l2: 0.0970837
[1100]	valid_0&#39;s l2: 0.0944841
[1200]	valid_0&#39;s l2: 0.0924994
[1300]	valid_0&#39;s l2: 0.0905785
[1400]	valid_0&#39;s l2: 0.0889666
[1500]	valid_0&#39;s l2: 0.0876517
[1600]	valid_0&#39;s l2: 0.0863177
[1700]	valid_0&#39;s l2: 0.0853336
[1800]	valid_0&#39;s l2: 0.0846294
[1900]	valid_0&#39;s l2: 0.0836586
[2000]	valid_0&#39;s l2: 0.08279
[2100]	valid_0&#39;s l2: 0.0818736
[2200]	valid_0&#39;s l2: 0.0812358
[2300]	valid_0&#39;s l2: 0.0808155
[2400]	valid_0&#39;s l2: 0.0801531
[2500]	valid_0&#39;s l2: 0.0795822
[2600]	valid_0&#39;s l2: 0.079071
[2700]	valid_0&#39;s l2: 0.0785893
[2800]	valid_0&#39;s l2: 0.0781159
[2900]	valid_0&#39;s l2: 0.0778073
[3000]	valid_0&#39;s l2: 0.0774548
[3100]	valid_0&#39;s l2: 0.0771279
[3200]	valid_0&#39;s l2: 0.0769519
[3300]	valid_0&#39;s l2: 0.0767206
[3400]	valid_0&#39;s l2: 0.0764632
[3500]	valid_0&#39;s l2: 0.0762787
[3600]	valid_0&#39;s l2: 0.0759907
[3700]	valid_0&#39;s l2: 0.0757639
Early stopping, best iteration is:
[3757]	valid_0&#39;s l2: 0.0755781
3번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.20315
[200]	valid_0&#39;s l2: 0.170073
[300]	valid_0&#39;s l2: 0.150078
[400]	valid_0&#39;s l2: 0.135187
[500]	valid_0&#39;s l2: 0.123717
[600]	valid_0&#39;s l2: 0.116185
[700]	valid_0&#39;s l2: 0.110907
[800]	valid_0&#39;s l2: 0.106641
[900]	valid_0&#39;s l2: 0.10329
[1000]	valid_0&#39;s l2: 0.100374
[1100]	valid_0&#39;s l2: 0.097839
[1200]	valid_0&#39;s l2: 0.0952868
[1300]	valid_0&#39;s l2: 0.09309
[1400]	valid_0&#39;s l2: 0.0912591
[1500]	valid_0&#39;s l2: 0.0897763
[1600]	valid_0&#39;s l2: 0.0887462
[1700]	valid_0&#39;s l2: 0.0877194
[1800]	valid_0&#39;s l2: 0.086717
[1900]	valid_0&#39;s l2: 0.0856592
[2000]	valid_0&#39;s l2: 0.0848223
[2100]	valid_0&#39;s l2: 0.0841129
[2200]	valid_0&#39;s l2: 0.0836697
[2300]	valid_0&#39;s l2: 0.0827624
[2400]	valid_0&#39;s l2: 0.0823009
[2500]	valid_0&#39;s l2: 0.0816573
[2600]	valid_0&#39;s l2: 0.0811724
[2700]	valid_0&#39;s l2: 0.0805713
[2800]	valid_0&#39;s l2: 0.080115
Early stopping, best iteration is:
[2847]	valid_0&#39;s l2: 0.0798219
4번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.212643
[200]	valid_0&#39;s l2: 0.171101
[300]	valid_0&#39;s l2: 0.14781
[400]	valid_0&#39;s l2: 0.132749
[500]	valid_0&#39;s l2: 0.122809
[600]	valid_0&#39;s l2: 0.115987
[700]	valid_0&#39;s l2: 0.110509
[800]	valid_0&#39;s l2: 0.106175
[900]	valid_0&#39;s l2: 0.102523
[1000]	valid_0&#39;s l2: 0.0996796
[1100]	valid_0&#39;s l2: 0.0973879
[1200]	valid_0&#39;s l2: 0.095213
[1300]	valid_0&#39;s l2: 0.093465
[1400]	valid_0&#39;s l2: 0.0919471
[1500]	valid_0&#39;s l2: 0.0905539
[1600]	valid_0&#39;s l2: 0.0896057
[1700]	valid_0&#39;s l2: 0.0889235
[1800]	valid_0&#39;s l2: 0.0879541
[1900]	valid_0&#39;s l2: 0.0870617
[2000]	valid_0&#39;s l2: 0.0858574
[2100]	valid_0&#39;s l2: 0.085017
[2200]	valid_0&#39;s l2: 0.0843319
[2300]	valid_0&#39;s l2: 0.0836756
[2400]	valid_0&#39;s l2: 0.0830299
[2500]	valid_0&#39;s l2: 0.0825272
[2600]	valid_0&#39;s l2: 0.0819895
[2700]	valid_0&#39;s l2: 0.0814869
[2800]	valid_0&#39;s l2: 0.0811424
[2900]	valid_0&#39;s l2: 0.0805425
[3000]	valid_0&#39;s l2: 0.0803035
[3100]	valid_0&#39;s l2: 0.0800971
Early stopping, best iteration is:
[3088]	valid_0&#39;s l2: 0.0800555
5번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.2079
[200]	valid_0&#39;s l2: 0.17302
[300]	valid_0&#39;s l2: 0.152234
[400]	valid_0&#39;s l2: 0.137197
[500]	valid_0&#39;s l2: 0.125537
[600]	valid_0&#39;s l2: 0.118796
[700]	valid_0&#39;s l2: 0.111324
[800]	valid_0&#39;s l2: 0.106397
[900]	valid_0&#39;s l2: 0.103296
[1000]	valid_0&#39;s l2: 0.100305
[1100]	valid_0&#39;s l2: 0.0978409
[1200]	valid_0&#39;s l2: 0.095702
[1300]	valid_0&#39;s l2: 0.094
[1400]	valid_0&#39;s l2: 0.0927513
[1500]	valid_0&#39;s l2: 0.0914574
[1600]	valid_0&#39;s l2: 0.0901214
[1700]	valid_0&#39;s l2: 0.0886592
[1800]	valid_0&#39;s l2: 0.0877298
[1900]	valid_0&#39;s l2: 0.0868921
[2000]	valid_0&#39;s l2: 0.0861138
[2100]	valid_0&#39;s l2: 0.0851344
[2200]	valid_0&#39;s l2: 0.0842863
[2300]	valid_0&#39;s l2: 0.0834951
[2400]	valid_0&#39;s l2: 0.0829582
[2500]	valid_0&#39;s l2: 0.0824628
[2600]	valid_0&#39;s l2: 0.0821059
[2700]	valid_0&#39;s l2: 0.0815359
[2800]	valid_0&#39;s l2: 0.0810588
[2900]	valid_0&#39;s l2: 0.0806031
[3000]	valid_0&#39;s l2: 0.0801813
[3100]	valid_0&#39;s l2: 0.0798715
[3200]	valid_0&#39;s l2: 0.0796252
[3300]	valid_0&#39;s l2: 0.0794381
[3400]	valid_0&#39;s l2: 0.0791402
Early stopping, best iteration is:
[3446]	valid_0&#39;s l2: 0.0789678
6번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.208986
[200]	valid_0&#39;s l2: 0.171407
[300]	valid_0&#39;s l2: 0.149874
[400]	valid_0&#39;s l2: 0.135563
[500]	valid_0&#39;s l2: 0.124505
[600]	valid_0&#39;s l2: 0.117882
[700]	valid_0&#39;s l2: 0.111695
[800]	valid_0&#39;s l2: 0.107272
[900]	valid_0&#39;s l2: 0.103778
[1000]	valid_0&#39;s l2: 0.100233
[1100]	valid_0&#39;s l2: 0.0982903
[1200]	valid_0&#39;s l2: 0.0958871
[1300]	valid_0&#39;s l2: 0.0940035
[1400]	valid_0&#39;s l2: 0.0923511
[1500]	valid_0&#39;s l2: 0.0906108
[1600]	valid_0&#39;s l2: 0.0895202
[1700]	valid_0&#39;s l2: 0.0884299
[1800]	valid_0&#39;s l2: 0.0875122
[1900]	valid_0&#39;s l2: 0.0863238
[2000]	valid_0&#39;s l2: 0.0856547
[2100]	valid_0&#39;s l2: 0.0848495
[2200]	valid_0&#39;s l2: 0.0842947
[2300]	valid_0&#39;s l2: 0.0836993
[2400]	valid_0&#39;s l2: 0.083394
[2500]	valid_0&#39;s l2: 0.0828518
[2600]	valid_0&#39;s l2: 0.0824846
[2700]	valid_0&#39;s l2: 0.0821306
[2800]	valid_0&#39;s l2: 0.0817267
[2900]	valid_0&#39;s l2: 0.0813922
[3000]	valid_0&#39;s l2: 0.0809575
[3100]	valid_0&#39;s l2: 0.0805241
[3200]	valid_0&#39;s l2: 0.0803442
[3300]	valid_0&#39;s l2: 0.0801054
[3400]	valid_0&#39;s l2: 0.0797262
[3500]	valid_0&#39;s l2: 0.07931
[3600]	valid_0&#39;s l2: 0.078993
[3700]	valid_0&#39;s l2: 0.0785701
[3800]	valid_0&#39;s l2: 0.0784191
Early stopping, best iteration is:
[3772]	valid_0&#39;s l2: 0.0783855
7번 Np done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0329645
[200]	valid_0&#39;s l2: 0.0281246
[300]	valid_0&#39;s l2: 0.0250682
[400]	valid_0&#39;s l2: 0.0227663
[500]	valid_0&#39;s l2: 0.0208428
[600]	valid_0&#39;s l2: 0.0196629
[700]	valid_0&#39;s l2: 0.0185959
[800]	valid_0&#39;s l2: 0.0178463
[900]	valid_0&#39;s l2: 0.0172457
[1000]	valid_0&#39;s l2: 0.0166276
[1100]	valid_0&#39;s l2: 0.0161228
[1200]	valid_0&#39;s l2: 0.0155851
[1300]	valid_0&#39;s l2: 0.0152465
[1400]	valid_0&#39;s l2: 0.0148786
[1500]	valid_0&#39;s l2: 0.014508
[1600]	valid_0&#39;s l2: 0.0142425
[1700]	valid_0&#39;s l2: 0.0139824
[1800]	valid_0&#39;s l2: 0.0137904
[1900]	valid_0&#39;s l2: 0.0136264
[2000]	valid_0&#39;s l2: 0.0134715
[2100]	valid_0&#39;s l2: 0.0133202
[2200]	valid_0&#39;s l2: 0.0131668
[2300]	valid_0&#39;s l2: 0.0130735
[2400]	valid_0&#39;s l2: 0.0129758
[2500]	valid_0&#39;s l2: 0.0128884
[2600]	valid_0&#39;s l2: 0.0127628
[2700]	valid_0&#39;s l2: 0.0126487
[2800]	valid_0&#39;s l2: 0.0125383
[2900]	valid_0&#39;s l2: 0.0124476
[3000]	valid_0&#39;s l2: 0.0123585
[3100]	valid_0&#39;s l2: 0.0122847
[3200]	valid_0&#39;s l2: 0.0122357
[3300]	valid_0&#39;s l2: 0.0122002
Early stopping, best iteration is:
[3281]	valid_0&#39;s l2: 0.0121957
0번 Vp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0325244
[200]	valid_0&#39;s l2: 0.0278201
[300]	valid_0&#39;s l2: 0.0245727
[400]	valid_0&#39;s l2: 0.0224174
[500]	valid_0&#39;s l2: 0.0207426
[600]	valid_0&#39;s l2: 0.0195971
[700]	valid_0&#39;s l2: 0.0186123
[800]	valid_0&#39;s l2: 0.0179084
[900]	valid_0&#39;s l2: 0.0172347
[1000]	valid_0&#39;s l2: 0.0166377
[1100]	valid_0&#39;s l2: 0.0161585
[1200]	valid_0&#39;s l2: 0.0156723
[1300]	valid_0&#39;s l2: 0.0153265
[1400]	valid_0&#39;s l2: 0.0149734
[1500]	valid_0&#39;s l2: 0.0146793
[1600]	valid_0&#39;s l2: 0.0143911
[1700]	valid_0&#39;s l2: 0.014177
[1800]	valid_0&#39;s l2: 0.0140265
[1900]	valid_0&#39;s l2: 0.0138478
[2000]	valid_0&#39;s l2: 0.0136468
[2100]	valid_0&#39;s l2: 0.0134798
[2200]	valid_0&#39;s l2: 0.0133283
[2300]	valid_0&#39;s l2: 0.0131911
[2400]	valid_0&#39;s l2: 0.0131092
[2500]	valid_0&#39;s l2: 0.0130208
[2600]	valid_0&#39;s l2: 0.0129024
[2700]	valid_0&#39;s l2: 0.0127854
[2800]	valid_0&#39;s l2: 0.0126968
[2900]	valid_0&#39;s l2: 0.0126141
[3000]	valid_0&#39;s l2: 0.0125078
[3100]	valid_0&#39;s l2: 0.0124403
[3200]	valid_0&#39;s l2: 0.012383
[3300]	valid_0&#39;s l2: 0.0123008
[3400]	valid_0&#39;s l2: 0.0122358
[3500]	valid_0&#39;s l2: 0.0121836
[3600]	valid_0&#39;s l2: 0.0121416
[3700]	valid_0&#39;s l2: 0.0120968
[3800]	valid_0&#39;s l2: 0.0120425
[3900]	valid_0&#39;s l2: 0.0119958
[4000]	valid_0&#39;s l2: 0.0119522
[4100]	valid_0&#39;s l2: 0.0119144
[4200]	valid_0&#39;s l2: 0.0118776
[4300]	valid_0&#39;s l2: 0.0118278
Early stopping, best iteration is:
[4315]	valid_0&#39;s l2: 0.0118218
1번 Vp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0329106
[200]	valid_0&#39;s l2: 0.0278642
[300]	valid_0&#39;s l2: 0.024827
[400]	valid_0&#39;s l2: 0.0224178
[500]	valid_0&#39;s l2: 0.0207698
[600]	valid_0&#39;s l2: 0.0194356
[700]	valid_0&#39;s l2: 0.0184992
[800]	valid_0&#39;s l2: 0.0177784
[900]	valid_0&#39;s l2: 0.0171119
[1000]	valid_0&#39;s l2: 0.0165461
[1100]	valid_0&#39;s l2: 0.0160961
[1200]	valid_0&#39;s l2: 0.0156638
[1300]	valid_0&#39;s l2: 0.0152532
[1400]	valid_0&#39;s l2: 0.0149704
[1500]	valid_0&#39;s l2: 0.0146339
[1600]	valid_0&#39;s l2: 0.0143801
[1700]	valid_0&#39;s l2: 0.01413
[1800]	valid_0&#39;s l2: 0.0139348
[1900]	valid_0&#39;s l2: 0.0136962
[2000]	valid_0&#39;s l2: 0.0135309
[2100]	valid_0&#39;s l2: 0.0133701
[2200]	valid_0&#39;s l2: 0.0132142
[2300]	valid_0&#39;s l2: 0.0130985
[2400]	valid_0&#39;s l2: 0.0129895
[2500]	valid_0&#39;s l2: 0.0128818
[2600]	valid_0&#39;s l2: 0.0127837
[2700]	valid_0&#39;s l2: 0.0126772
[2800]	valid_0&#39;s l2: 0.0126139
[2900]	valid_0&#39;s l2: 0.0125334
[3000]	valid_0&#39;s l2: 0.0124451
[3100]	valid_0&#39;s l2: 0.0123828
[3200]	valid_0&#39;s l2: 0.0123477
[3300]	valid_0&#39;s l2: 0.0122824
[3400]	valid_0&#39;s l2: 0.0122107
[3500]	valid_0&#39;s l2: 0.0121601
[3600]	valid_0&#39;s l2: 0.0121136
[3700]	valid_0&#39;s l2: 0.0120665
[3800]	valid_0&#39;s l2: 0.0120291
[3900]	valid_0&#39;s l2: 0.0119703
[4000]	valid_0&#39;s l2: 0.011917
[4100]	valid_0&#39;s l2: 0.0118784
[4200]	valid_0&#39;s l2: 0.0118514
[4300]	valid_0&#39;s l2: 0.0118122
[4400]	valid_0&#39;s l2: 0.0117942
[4500]	valid_0&#39;s l2: 0.0117677
[4600]	valid_0&#39;s l2: 0.0117334
[4700]	valid_0&#39;s l2: 0.0117042
[4800]	valid_0&#39;s l2: 0.0116612
[4900]	valid_0&#39;s l2: 0.0116283
[5000]	valid_0&#39;s l2: 0.0116031
[5100]	valid_0&#39;s l2: 0.0115667
[5200]	valid_0&#39;s l2: 0.0115253
[5300]	valid_0&#39;s l2: 0.0114953
[5400]	valid_0&#39;s l2: 0.0114719
[5500]	valid_0&#39;s l2: 0.0114516
Early stopping, best iteration is:
[5516]	valid_0&#39;s l2: 0.0114475
2번 Vp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0327993
[200]	valid_0&#39;s l2: 0.0279812
[300]	valid_0&#39;s l2: 0.0249048
[400]	valid_0&#39;s l2: 0.0227606
[500]	valid_0&#39;s l2: 0.0209527
[600]	valid_0&#39;s l2: 0.019713
[700]	valid_0&#39;s l2: 0.0186725
[800]	valid_0&#39;s l2: 0.0178218
[900]	valid_0&#39;s l2: 0.017201
[1000]	valid_0&#39;s l2: 0.0166548
[1100]	valid_0&#39;s l2: 0.0162762
[1200]	valid_0&#39;s l2: 0.0157867
[1300]	valid_0&#39;s l2: 0.0154419
[1400]	valid_0&#39;s l2: 0.0150601
[1500]	valid_0&#39;s l2: 0.0147262
[1600]	valid_0&#39;s l2: 0.0144919
[1700]	valid_0&#39;s l2: 0.0142717
[1800]	valid_0&#39;s l2: 0.0140715
[1900]	valid_0&#39;s l2: 0.0138658
[2000]	valid_0&#39;s l2: 0.0137253
[2100]	valid_0&#39;s l2: 0.013577
[2200]	valid_0&#39;s l2: 0.013472
[2300]	valid_0&#39;s l2: 0.0133143
[2400]	valid_0&#39;s l2: 0.0132078
[2500]	valid_0&#39;s l2: 0.0131062
[2600]	valid_0&#39;s l2: 0.0129979
[2700]	valid_0&#39;s l2: 0.0128572
[2800]	valid_0&#39;s l2: 0.0127732
[2900]	valid_0&#39;s l2: 0.0126856
[3000]	valid_0&#39;s l2: 0.012596
[3100]	valid_0&#39;s l2: 0.012503
[3200]	valid_0&#39;s l2: 0.0124334
[3300]	valid_0&#39;s l2: 0.0123903
[3400]	valid_0&#39;s l2: 0.0123137
[3500]	valid_0&#39;s l2: 0.0122347
[3600]	valid_0&#39;s l2: 0.0121899
[3700]	valid_0&#39;s l2: 0.0121435
[3800]	valid_0&#39;s l2: 0.0121007
[3900]	valid_0&#39;s l2: 0.0120553
[4000]	valid_0&#39;s l2: 0.012017
[4100]	valid_0&#39;s l2: 0.0119835
[4200]	valid_0&#39;s l2: 0.0119423
[4300]	valid_0&#39;s l2: 0.0119107
[4400]	valid_0&#39;s l2: 0.0118742
[4500]	valid_0&#39;s l2: 0.0118362
[4600]	valid_0&#39;s l2: 0.0118086
[4700]	valid_0&#39;s l2: 0.0117742
Early stopping, best iteration is:
[4745]	valid_0&#39;s l2: 0.0117466
3번 Vp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0324213
[200]	valid_0&#39;s l2: 0.0278348
[300]	valid_0&#39;s l2: 0.0247128
[400]	valid_0&#39;s l2: 0.0222588
[500]	valid_0&#39;s l2: 0.020599
[600]	valid_0&#39;s l2: 0.0193796
[700]	valid_0&#39;s l2: 0.0184272
[800]	valid_0&#39;s l2: 0.0176263
[900]	valid_0&#39;s l2: 0.0169664
[1000]	valid_0&#39;s l2: 0.0164374
[1100]	valid_0&#39;s l2: 0.0160262
[1200]	valid_0&#39;s l2: 0.0155994
[1300]	valid_0&#39;s l2: 0.0152303
[1400]	valid_0&#39;s l2: 0.0149265
[1500]	valid_0&#39;s l2: 0.014621
[1600]	valid_0&#39;s l2: 0.0143912
[1700]	valid_0&#39;s l2: 0.0142061
[1800]	valid_0&#39;s l2: 0.013993
[1900]	valid_0&#39;s l2: 0.0137956
[2000]	valid_0&#39;s l2: 0.0136625
[2100]	valid_0&#39;s l2: 0.0135496
[2200]	valid_0&#39;s l2: 0.013419
[2300]	valid_0&#39;s l2: 0.0132798
[2400]	valid_0&#39;s l2: 0.013156
[2500]	valid_0&#39;s l2: 0.0130438
[2600]	valid_0&#39;s l2: 0.0129598
[2700]	valid_0&#39;s l2: 0.0128686
[2800]	valid_0&#39;s l2: 0.0127872
[2900]	valid_0&#39;s l2: 0.0126522
[3000]	valid_0&#39;s l2: 0.0125445
[3100]	valid_0&#39;s l2: 0.0124431
[3200]	valid_0&#39;s l2: 0.012396
[3300]	valid_0&#39;s l2: 0.0123414
[3400]	valid_0&#39;s l2: 0.0122991
[3500]	valid_0&#39;s l2: 0.0122361
[3600]	valid_0&#39;s l2: 0.0121715
[3700]	valid_0&#39;s l2: 0.0121103
[3800]	valid_0&#39;s l2: 0.0120723
[3900]	valid_0&#39;s l2: 0.0120181
[4000]	valid_0&#39;s l2: 0.0119751
[4100]	valid_0&#39;s l2: 0.0119535
[4200]	valid_0&#39;s l2: 0.0119186
[4300]	valid_0&#39;s l2: 0.0118748
[4400]	valid_0&#39;s l2: 0.0118475
[4500]	valid_0&#39;s l2: 0.0117988
[4600]	valid_0&#39;s l2: 0.0117635
[4700]	valid_0&#39;s l2: 0.0117193
[4800]	valid_0&#39;s l2: 0.0116766
[4900]	valid_0&#39;s l2: 0.0116335
[5000]	valid_0&#39;s l2: 0.0116003
[5100]	valid_0&#39;s l2: 0.0115759
[5200]	valid_0&#39;s l2: 0.0115398
[5300]	valid_0&#39;s l2: 0.0115094
Early stopping, best iteration is:
[5288]	valid_0&#39;s l2: 0.0115068
4번 Vp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0324543
[200]	valid_0&#39;s l2: 0.0276417
[300]	valid_0&#39;s l2: 0.0246687
[400]	valid_0&#39;s l2: 0.0223275
[500]	valid_0&#39;s l2: 0.0205671
[600]	valid_0&#39;s l2: 0.0194613
[700]	valid_0&#39;s l2: 0.018444
[800]	valid_0&#39;s l2: 0.0176185
[900]	valid_0&#39;s l2: 0.0170013
[1000]	valid_0&#39;s l2: 0.0164259
[1100]	valid_0&#39;s l2: 0.0160465
[1200]	valid_0&#39;s l2: 0.0156141
[1300]	valid_0&#39;s l2: 0.0151958
[1400]	valid_0&#39;s l2: 0.0149248
[1500]	valid_0&#39;s l2: 0.0145643
[1600]	valid_0&#39;s l2: 0.0143286
[1700]	valid_0&#39;s l2: 0.0141161
[1800]	valid_0&#39;s l2: 0.013925
[1900]	valid_0&#39;s l2: 0.0137323
[2000]	valid_0&#39;s l2: 0.0135851
[2100]	valid_0&#39;s l2: 0.0134016
[2200]	valid_0&#39;s l2: 0.0132592
[2300]	valid_0&#39;s l2: 0.0131058
[2400]	valid_0&#39;s l2: 0.0129584
[2500]	valid_0&#39;s l2: 0.0128659
[2600]	valid_0&#39;s l2: 0.0127603
[2700]	valid_0&#39;s l2: 0.0126653
[2800]	valid_0&#39;s l2: 0.0125953
[2900]	valid_0&#39;s l2: 0.0125107
[3000]	valid_0&#39;s l2: 0.0124425
[3100]	valid_0&#39;s l2: 0.012355
[3200]	valid_0&#39;s l2: 0.0123023
[3300]	valid_0&#39;s l2: 0.0122687
[3400]	valid_0&#39;s l2: 0.0121911
[3500]	valid_0&#39;s l2: 0.0121451
[3600]	valid_0&#39;s l2: 0.0120905
[3700]	valid_0&#39;s l2: 0.0120456
[3800]	valid_0&#39;s l2: 0.0120117
[3900]	valid_0&#39;s l2: 0.0119601
[4000]	valid_0&#39;s l2: 0.0119123
[4100]	valid_0&#39;s l2: 0.0118805
[4200]	valid_0&#39;s l2: 0.0118544
Early stopping, best iteration is:
[4191]	valid_0&#39;s l2: 0.0118524
5번 Vp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0320598
[200]	valid_0&#39;s l2: 0.0272209
[300]	valid_0&#39;s l2: 0.0241352
[400]	valid_0&#39;s l2: 0.0220345
[500]	valid_0&#39;s l2: 0.0201667
[600]	valid_0&#39;s l2: 0.0190284
[700]	valid_0&#39;s l2: 0.0181192
[800]	valid_0&#39;s l2: 0.0173668
[900]	valid_0&#39;s l2: 0.0167331
[1000]	valid_0&#39;s l2: 0.0162008
[1100]	valid_0&#39;s l2: 0.0157437
[1200]	valid_0&#39;s l2: 0.0153828
[1300]	valid_0&#39;s l2: 0.01507
[1400]	valid_0&#39;s l2: 0.0146702
[1500]	valid_0&#39;s l2: 0.0143784
[1600]	valid_0&#39;s l2: 0.014114
[1700]	valid_0&#39;s l2: 0.0138758
[1800]	valid_0&#39;s l2: 0.0136419
[1900]	valid_0&#39;s l2: 0.0134435
[2000]	valid_0&#39;s l2: 0.0132601
[2100]	valid_0&#39;s l2: 0.0130777
[2200]	valid_0&#39;s l2: 0.0129338
[2300]	valid_0&#39;s l2: 0.0128084
[2400]	valid_0&#39;s l2: 0.0126709
[2500]	valid_0&#39;s l2: 0.0125569
[2600]	valid_0&#39;s l2: 0.0124771
[2700]	valid_0&#39;s l2: 0.0123841
[2800]	valid_0&#39;s l2: 0.0122872
[2900]	valid_0&#39;s l2: 0.0122052
[3000]	valid_0&#39;s l2: 0.0121192
[3100]	valid_0&#39;s l2: 0.0120323
[3200]	valid_0&#39;s l2: 0.0119562
[3300]	valid_0&#39;s l2: 0.0118955
[3400]	valid_0&#39;s l2: 0.0118198
[3500]	valid_0&#39;s l2: 0.0117813
[3600]	valid_0&#39;s l2: 0.011727
[3700]	valid_0&#39;s l2: 0.0116801
[3800]	valid_0&#39;s l2: 0.0116231
[3900]	valid_0&#39;s l2: 0.0115674
[4000]	valid_0&#39;s l2: 0.0115222
[4100]	valid_0&#39;s l2: 0.0114727
[4200]	valid_0&#39;s l2: 0.0114385
[4300]	valid_0&#39;s l2: 0.0113921
[4400]	valid_0&#39;s l2: 0.0113599
[4500]	valid_0&#39;s l2: 0.0113195
[4600]	valid_0&#39;s l2: 0.0112963
[4700]	valid_0&#39;s l2: 0.011273
[4800]	valid_0&#39;s l2: 0.0112347
[4900]	valid_0&#39;s l2: 0.0112103
Early stopping, best iteration is:
[4964]	valid_0&#39;s l2: 0.0111909
6번 Vp done
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 0.0323889
[200]	valid_0&#39;s l2: 0.0277023
[300]	valid_0&#39;s l2: 0.0246384
[400]	valid_0&#39;s l2: 0.022338
[500]	valid_0&#39;s l2: 0.0207548
[600]	valid_0&#39;s l2: 0.0195678
[700]	valid_0&#39;s l2: 0.0185706
[800]	valid_0&#39;s l2: 0.0178457
[900]	valid_0&#39;s l2: 0.0171656
[1000]	valid_0&#39;s l2: 0.0165323
[1100]	valid_0&#39;s l2: 0.0160453
[1200]	valid_0&#39;s l2: 0.015604
[1300]	valid_0&#39;s l2: 0.0152814
[1400]	valid_0&#39;s l2: 0.0149255
[1500]	valid_0&#39;s l2: 0.0145965
[1600]	valid_0&#39;s l2: 0.0143493
[1700]	valid_0&#39;s l2: 0.014162
[1800]	valid_0&#39;s l2: 0.0140047
[1900]	valid_0&#39;s l2: 0.0137904
[2000]	valid_0&#39;s l2: 0.0136442
[2100]	valid_0&#39;s l2: 0.01344
[2200]	valid_0&#39;s l2: 0.0133169
[2300]	valid_0&#39;s l2: 0.0132011
[2400]	valid_0&#39;s l2: 0.0130943
[2500]	valid_0&#39;s l2: 0.0130044
[2600]	valid_0&#39;s l2: 0.0129016
[2700]	valid_0&#39;s l2: 0.0127977
[2800]	valid_0&#39;s l2: 0.0127094
[2900]	valid_0&#39;s l2: 0.0126345
[3000]	valid_0&#39;s l2: 0.012549
[3100]	valid_0&#39;s l2: 0.0124695
Early stopping, best iteration is:
[3122]	valid_0&#39;s l2: 0.012463
7번 Vp done
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
Int64Index([], dtype=&#39;int64&#39;)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp_model</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_P_nan_model/Vp&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np_model</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_P_nan_model/Np&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp_model</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_P_nan_model/Tp&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0908_new_final_nan_csv/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[126]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">before</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="n">before</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="o">==</span><span class="mi">922381</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[126]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>year</th>
      <th>doy</th>
      <th>hr</th>
      <th>min</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>922381</th>
      <td>2013.0</td>
      <td>331.0</td>
      <td>8.0</td>
      <td>38.0</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
      <td>-1.244</td>
      <td>0.133</td>
      <td>4.246</td>
      <td>4.438</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[127]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="o">==</span><span class="mi">922381</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[127]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>year</th>
      <th>doy</th>
      <th>hr</th>
      <th>min</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>922381</th>
      <td>2013.0</td>
      <td>331.0</td>
      <td>8.0</td>
      <td>38.0</td>
      <td>45.192524</td>
      <td>177506.107895</td>
      <td>306.840576</td>
      <td>-1.244</td>
      <td>0.133</td>
      <td>4.246</td>
      <td>4.438</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[115]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">20</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Int64Index([   845,    846,    847,    848,    849,    850,    851,    852,
               853,    854,
            ...
            924659, 924660, 924661, 924662, 924663, 924669, 925515, 925516,
            925517, 925666],
           dtype=&#39;int64&#39;, length=13363)
Int64Index([   841,    842,    843,    844,    845,    846,    847,    848,
               849,    850,
            ...
            924175, 925177, 925178, 925180, 925186, 925239, 925283, 925284,
            925291, 925294],
           dtype=&#39;int64&#39;, length=12760)
Int64Index([   845,    847,    848,    849,    852,    853,    857,    860,
               863,    885,
            ...
            922372, 922373, 922375, 922376, 922379, 922380, 922381, 922382,
            922384, 922394],
           dtype=&#39;int64&#39;, length=12695)
Int64Index([   862,    864,    870,    899,    903,    907,    913,    921,
               925,    929,
            ...
            924936, 926727, 926728, 926729, 927063, 927121, 927124, 927129,
            927204, 927206],
           dtype=&#39;int64&#39;, length=13195)
Int64Index([   845,    846,    847,    848,    849,    850,    851,    852,
               853,    854,
            ...
            904670, 904671, 905680, 905681, 917529, 922470, 922502, 922511,
            922534, 925549],
           dtype=&#39;int64&#39;, length=16432)
Int64Index([  2016,   2018,   2019,   2020,   2035,   2037,   2038,   2050,
              2051,   2052,
            ...
            927571, 927572, 927597, 927610, 927633, 927635, 927636, 927642,
            927643, 927644],
           dtype=&#39;int64&#39;, length=15856)
Int64Index([  2049,   2050,   2053,   2054,   2055,   2056,   2057,   2058,
              2059,   2060,
            ...
            919049, 919054, 919055, 919056, 919057, 919058, 925164, 925165,
            927594, 927596],
           dtype=&#39;int64&#39;, length=14689)
Int64Index([   826,    827,    829,    830,    831,    832,    833,    834,
               835,    836,
            ...
            914401, 924466, 924472, 924473, 924474, 925466, 925575, 925576,
            925580, 925582],
           dtype=&#39;int64&#39;, length=14970)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0908_new_final_nan_csv/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">original</span><span class="p">[</span><span class="mi">3</span><span class="p">][</span><span class="n">original</span><span class="p">[</span><span class="mi">3</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="train-&#47784;&#45944;-&#51676;&#44592;">train &#47784;&#45944; &#51676;&#44592;<a class="anchor-link" href="#train-&#47784;&#45944;-&#51676;&#44592;">&#182;</a></h1><hr>
<p><strong>큰 개요는 각 날의 모든 시, 분 단위로 예측을 한다음에 그거를 voting할거임</strong></p>
<hr>
<p><strong>결과가 별론데.. 방법은 2가지 1.-9999걍 다 버리고 조진다. 2. 제대로된 값 예측하고 조진다</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[141]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#split data for test and train, valid</span>

<span class="n">models</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">eight=int(df3.shape[0]*0.8)</span>
<span class="sd">x_test=df3[:365]</span>
<span class="sd">y_test=x_test[&#39;label&#39;]</span>
<span class="sd">check=x_test.copy()</span>
<span class="sd">x_test.drop([&#39;label&#39;],axis=1,inplace=True)</span>
<span class="sd">df3=df3[365:]</span>
<span class="sd">&#39;&#39;&#39;</span>


<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df3</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="n">frac</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

  <span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df3</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.066</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">)</span>


  <span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
  <span class="n">lgb_eval</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>


  <span class="c1">#configure parameters</span>
  <span class="n">params</span><span class="o">=</span><span class="p">{</span>
      <span class="s1">&#39;boosting_type&#39;</span> <span class="p">:</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
      <span class="c1">#&#39;objective&#39;:&#39;multiclass&#39;,</span>
      <span class="s1">&#39;objective&#39;</span><span class="p">:</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span>
      <span class="c1">#&#39;metric&#39;:&#39;accuracy&#39;,</span>
      <span class="s1">&#39;num_tree&#39;</span><span class="p">:</span><span class="mi">10000</span><span class="p">,</span>
      <span class="c1">#&quot;num_class&quot; : 10,</span>
      <span class="s1">&#39;max_bin&#39;</span> <span class="p">:</span> <span class="mi">1000</span><span class="p">,</span>
      <span class="s1">&#39;max_depth&#39;</span> <span class="p">:</span><span class="mi">200</span><span class="p">,</span>
      <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
      <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.005</span><span class="p">,</span>
      <span class="s1">&#39;feature_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
      <span class="s1">&#39;bagging_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
      <span class="s1">&#39;bagging_freq&#39;</span><span class="p">:</span> <span class="mi">3</span><span class="p">,</span>    
      <span class="s1">&#39;num_leavs&#39;</span><span class="p">:</span> <span class="mi">10000</span><span class="p">,</span>
      <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span>
  <span class="p">}</span>

  <span class="c1">#model train</span>
  <span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span><span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_eval</span><span class="p">,</span><span class="n">verbose_eval</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
  <span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/lightgbm/engine.py:118: UserWarning: Found `num_tree` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.07294
[200]	valid_0&#39;s l2: 0.792551
[300]	valid_0&#39;s l2: 0.668448
[400]	valid_0&#39;s l2: 0.613474
[500]	valid_0&#39;s l2: 0.5838
[600]	valid_0&#39;s l2: 0.570369
[700]	valid_0&#39;s l2: 0.561167
[800]	valid_0&#39;s l2: 0.5562
[900]	valid_0&#39;s l2: 0.55397
[1000]	valid_0&#39;s l2: 0.55305
Early stopping, best iteration is:
[961]	valid_0&#39;s l2: 0.552721
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.35326
[200]	valid_0&#39;s l2: 0.955707
[300]	valid_0&#39;s l2: 0.773059
[400]	valid_0&#39;s l2: 0.688594
[500]	valid_0&#39;s l2: 0.646711
[600]	valid_0&#39;s l2: 0.623912
[700]	valid_0&#39;s l2: 0.611087
[800]	valid_0&#39;s l2: 0.603469
[900]	valid_0&#39;s l2: 0.598808
[1000]	valid_0&#39;s l2: 0.594484
[1100]	valid_0&#39;s l2: 0.593646
[1200]	valid_0&#39;s l2: 0.593678
Early stopping, best iteration is:
[1146]	valid_0&#39;s l2: 0.593283
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.36156
[200]	valid_0&#39;s l2: 0.985361
[300]	valid_0&#39;s l2: 0.807712
[400]	valid_0&#39;s l2: 0.722573
[500]	valid_0&#39;s l2: 0.677112
[600]	valid_0&#39;s l2: 0.651439
[700]	valid_0&#39;s l2: 0.634813
[800]	valid_0&#39;s l2: 0.625071
[900]	valid_0&#39;s l2: 0.61784
[1000]	valid_0&#39;s l2: 0.612755
[1100]	valid_0&#39;s l2: 0.609027
[1200]	valid_0&#39;s l2: 0.606803
[1300]	valid_0&#39;s l2: 0.604972
[1400]	valid_0&#39;s l2: 0.602931
[1500]	valid_0&#39;s l2: 0.601469
[1600]	valid_0&#39;s l2: 0.601081
[1700]	valid_0&#39;s l2: 0.600575
Early stopping, best iteration is:
[1670]	valid_0&#39;s l2: 0.600076
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.37445
[200]	valid_0&#39;s l2: 0.959129
[300]	valid_0&#39;s l2: 0.76316
[400]	valid_0&#39;s l2: 0.669377
[500]	valid_0&#39;s l2: 0.618576
[600]	valid_0&#39;s l2: 0.591017
[700]	valid_0&#39;s l2: 0.574803
[800]	valid_0&#39;s l2: 0.565724
[900]	valid_0&#39;s l2: 0.560576
[1000]	valid_0&#39;s l2: 0.557099
[1100]	valid_0&#39;s l2: 0.554562
[1200]	valid_0&#39;s l2: 0.554746
Early stopping, best iteration is:
[1122]	valid_0&#39;s l2: 0.554085
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.966903
[200]	valid_0&#39;s l2: 0.706474
[300]	valid_0&#39;s l2: 0.588099
[400]	valid_0&#39;s l2: 0.530791
[500]	valid_0&#39;s l2: 0.49826
[600]	valid_0&#39;s l2: 0.480302
[700]	valid_0&#39;s l2: 0.468682
[800]	valid_0&#39;s l2: 0.460318
[900]	valid_0&#39;s l2: 0.454616
[1000]	valid_0&#39;s l2: 0.449896
[1100]	valid_0&#39;s l2: 0.446156
[1200]	valid_0&#39;s l2: 0.443415
[1300]	valid_0&#39;s l2: 0.441887
[1400]	valid_0&#39;s l2: 0.440835
[1500]	valid_0&#39;s l2: 0.440045
[1600]	valid_0&#39;s l2: 0.438867
[1700]	valid_0&#39;s l2: 0.438195
[1800]	valid_0&#39;s l2: 0.438234
[1900]	valid_0&#39;s l2: 0.437742
[2000]	valid_0&#39;s l2: 0.437802
Early stopping, best iteration is:
[1951]	valid_0&#39;s l2: 0.437321
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.937214
[200]	valid_0&#39;s l2: 0.676755
[300]	valid_0&#39;s l2: 0.558479
[400]	valid_0&#39;s l2: 0.50362
[500]	valid_0&#39;s l2: 0.47451
[600]	valid_0&#39;s l2: 0.458278
[700]	valid_0&#39;s l2: 0.448617
[800]	valid_0&#39;s l2: 0.442594
[900]	valid_0&#39;s l2: 0.439181
[1000]	valid_0&#39;s l2: 0.43623
[1100]	valid_0&#39;s l2: 0.434526
[1200]	valid_0&#39;s l2: 0.433819
[1300]	valid_0&#39;s l2: 0.43302
[1400]	valid_0&#39;s l2: 0.432492
[1500]	valid_0&#39;s l2: 0.432534
Early stopping, best iteration is:
[1459]	valid_0&#39;s l2: 0.431944
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.01614
[200]	valid_0&#39;s l2: 0.763144
[300]	valid_0&#39;s l2: 0.644454
[400]	valid_0&#39;s l2: 0.584261
[500]	valid_0&#39;s l2: 0.55023
[600]	valid_0&#39;s l2: 0.528451
[700]	valid_0&#39;s l2: 0.515308
[800]	valid_0&#39;s l2: 0.508207
[900]	valid_0&#39;s l2: 0.501892
[1000]	valid_0&#39;s l2: 0.498781
[1100]	valid_0&#39;s l2: 0.494861
[1200]	valid_0&#39;s l2: 0.492393
[1300]	valid_0&#39;s l2: 0.490956
[1400]	valid_0&#39;s l2: 0.490155
[1500]	valid_0&#39;s l2: 0.489233
[1600]	valid_0&#39;s l2: 0.488492
[1700]	valid_0&#39;s l2: 0.48758
[1800]	valid_0&#39;s l2: 0.487276
[1900]	valid_0&#39;s l2: 0.48734
Early stopping, best iteration is:
[1879]	valid_0&#39;s l2: 0.486967
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.827731
[200]	valid_0&#39;s l2: 0.629023
[300]	valid_0&#39;s l2: 0.537264
[400]	valid_0&#39;s l2: 0.492977
[500]	valid_0&#39;s l2: 0.46725
[600]	valid_0&#39;s l2: 0.45417
[700]	valid_0&#39;s l2: 0.447262
[800]	valid_0&#39;s l2: 0.442612
[900]	valid_0&#39;s l2: 0.440708
[1000]	valid_0&#39;s l2: 0.43919
[1100]	valid_0&#39;s l2: 0.43875
[1200]	valid_0&#39;s l2: 0.439038
Early stopping, best iteration is:
[1156]	valid_0&#39;s l2: 0.438047
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#model save</span>

<span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/model6/no_nan_mean&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[139]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#weight rmse from 개최자</span>
<span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_valid</span><span class="p">)</span>

<span class="c1">#multiclass</span>
<span class="c1">#pred=[np.argmax(y_pred[i]) for i in range(len(y_pred))]</span>

<span class="c1">#regression</span>
<span class="n">pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">y_pred</span><span class="p">)</span>
<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">pred=[0 for i in range(len(y_valid))]</span>
<span class="sd">for i in range(len(y_pred)):</span>
<span class="sd">  if y_pred[i]-int(y_pred[i])&gt;0.4:</span>
<span class="sd">    pred[i]=int(y_pred[i])+1</span>
<span class="sd">  else:</span>
<span class="sd">    pred[i]=int(y_pred[i])</span>


<span class="sd">&#39;&#39;&#39;</span>

<span class="n">sum_weight</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">(</span><span class="n">y_valid</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;weighted rmse: &quot;</span><span class="p">,</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">((</span><span class="n">y_valid</span><span class="o">/</span><span class="n">sum_weight</span><span class="p">)</span><span class="o">*</span><span class="p">(</span><span class="n">pred</span><span class="o">-</span><span class="n">y_valid</span><span class="p">)</span><span class="o">**</span><span class="mi">2</span><span class="p">)))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>weighted rmse:  0.980612053770501
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[140]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#weight rmse from 개최자</span>
<span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>

<span class="c1">#multiclass</span>
<span class="c1">#pred=[np.argmax(y_pred[i]) for i in range(len(y_pred))]</span>

<span class="c1">#regression</span>
<span class="n">pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">y_pred</span><span class="p">)</span>


<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">pred=[0 for i in range(len(y_valid))]</span>
<span class="sd">for i in range(len(y_pred)):</span>
<span class="sd">  if y_pred[i]-int(y_pred[i])&gt;0.4:</span>
<span class="sd">    pred[i]=int(y_pred[i])+1</span>
<span class="sd">  else:</span>
<span class="sd">    pred[i]=int(y_pred[i])</span>

<span class="sd">&#39;&#39;&#39;</span>


<span class="n">sum_weight</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">(</span><span class="n">y_test</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;weighted rmse: &quot;</span><span class="p">,</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">((</span><span class="n">y_test</span><span class="o">/</span><span class="n">sum_weight</span><span class="p">)</span><span class="o">*</span><span class="p">(</span><span class="n">pred</span><span class="o">-</span><span class="n">y_test</span><span class="p">)</span><span class="o">**</span><span class="mi">2</span><span class="p">)))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>weighted rmse:  1.147622340771143
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[91]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>

<span class="n">params</span><span class="o">=</span><span class="p">{</span>
    <span class="s1">&#39;boosting_type&#39;</span> <span class="p">:</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
    <span class="s1">&#39;objective&#39;</span><span class="p">:</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span>
    <span class="c1">#&#39;objective&#39;:&#39;multiclass&#39;,</span>
    <span class="c1">#&#39;num_class&#39;:10,</span>
    <span class="s1">&#39;num_tree&#39;</span><span class="p">:</span><span class="mi">10000</span><span class="p">,</span>
    <span class="s1">&#39;max_bin&#39;</span> <span class="p">:</span> <span class="mi">1000</span><span class="p">,</span>
    <span class="s1">&#39;max_depth&#39;</span> <span class="p">:</span><span class="mi">200</span><span class="p">,</span>
    <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
    <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.5</span><span class="p">,</span>
    <span class="s1">&#39;feature_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
    <span class="s1">&#39;bagging_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
    <span class="s1">&#39;bagging_freq&#39;</span><span class="p">:</span> <span class="mi">3</span><span class="p">,</span>    
    <span class="s1">&#39;num_leavs&#39;</span><span class="p">:</span> <span class="mi">10000</span><span class="p">,</span>
    <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">]</span>
<span class="p">}</span>  
<span class="n">models</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">):</span>
  
  <span class="n">x_test</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">2013</span><span class="p">]</span>
  <span class="n">y_test</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span>
  <span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">,</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
  <span class="n">train</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">!=</span><span class="mi">2013</span><span class="p">]</span>
  
  <span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">,</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">random_state</span><span class="o">=</span><span class="mi">940402</span><span class="p">,</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
  
  <span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
  <span class="n">lgb_eval</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>
  
  <span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span><span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_eval</span><span class="p">,</span><span class="n">verbose_eval</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">30</span><span class="p">)</span>
  
  <span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
/usr/local/lib/python3.6/dist-packages/lightgbm/engine.py:118: UserWarning: Found `num_tree` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 30 rounds.
[50]	valid_0&#39;s l2: 0.489157
[100]	valid_0&#39;s l2: 0.398392
[150]	valid_0&#39;s l2: 0.331291
[200]	valid_0&#39;s l2: 0.289758
[250]	valid_0&#39;s l2: 0.261372
[300]	valid_0&#39;s l2: 0.237734
[350]	valid_0&#39;s l2: 0.216718
[400]	valid_0&#39;s l2: 0.201719
[450]	valid_0&#39;s l2: 0.189443
[500]	valid_0&#39;s l2: 0.177158
[550]	valid_0&#39;s l2: 0.169785
[600]	valid_0&#39;s l2: 0.162662
[650]	valid_0&#39;s l2: 0.156014
[700]	valid_0&#39;s l2: 0.150001
[750]	valid_0&#39;s l2: 0.145985
[800]	valid_0&#39;s l2: 0.141098
[850]	valid_0&#39;s l2: 0.137118
[900]	valid_0&#39;s l2: 0.134053
[950]	valid_0&#39;s l2: 0.131069
[1000]	valid_0&#39;s l2: 0.128742
[1050]	valid_0&#39;s l2: 0.126143
[1100]	valid_0&#39;s l2: 0.123964
[1150]	valid_0&#39;s l2: 0.122174
[1200]	valid_0&#39;s l2: 0.120115
[1250]	valid_0&#39;s l2: 0.118434
[1300]	valid_0&#39;s l2: 0.116578
[1350]	valid_0&#39;s l2: 0.115062
[1400]	valid_0&#39;s l2: 0.113654
[1450]	valid_0&#39;s l2: 0.112669
[1500]	valid_0&#39;s l2: 0.111891
[1550]	valid_0&#39;s l2: 0.110599
[1600]	valid_0&#39;s l2: 0.10953
[1650]	valid_0&#39;s l2: 0.108593
[1700]	valid_0&#39;s l2: 0.107842
[1750]	valid_0&#39;s l2: 0.106959
[1800]	valid_0&#39;s l2: 0.106177
[1850]	valid_0&#39;s l2: 0.105587
[1900]	valid_0&#39;s l2: 0.104696
[1950]	valid_0&#39;s l2: 0.103938
[2000]	valid_0&#39;s l2: 0.103139
[2050]	valid_0&#39;s l2: 0.102621
[2100]	valid_0&#39;s l2: 0.102091
[2150]	valid_0&#39;s l2: 0.101675
[2200]	valid_0&#39;s l2: 0.10096
[2250]	valid_0&#39;s l2: 0.100411
[2300]	valid_0&#39;s l2: 0.100023
[2350]	valid_0&#39;s l2: 0.0996762
[2400]	valid_0&#39;s l2: 0.0991969
[2450]	valid_0&#39;s l2: 0.0988199
[2500]	valid_0&#39;s l2: 0.0983802
[2550]	valid_0&#39;s l2: 0.0981495
[2600]	valid_0&#39;s l2: 0.0976699
[2650]	valid_0&#39;s l2: 0.0973881
[2700]	valid_0&#39;s l2: 0.0970779
[2750]	valid_0&#39;s l2: 0.0967232
[2800]	valid_0&#39;s l2: 0.096578
[2850]	valid_0&#39;s l2: 0.0963243
[2900]	valid_0&#39;s l2: 0.096033
[2950]	valid_0&#39;s l2: 0.0957072
[3000]	valid_0&#39;s l2: 0.0954042
[3050]	valid_0&#39;s l2: 0.0951909
[3100]	valid_0&#39;s l2: 0.0949799
[3150]	valid_0&#39;s l2: 0.094697
[3200]	valid_0&#39;s l2: 0.0944112
[3250]	valid_0&#39;s l2: 0.0941551
[3300]	valid_0&#39;s l2: 0.09396
[3350]	valid_0&#39;s l2: 0.0937759
[3400]	valid_0&#39;s l2: 0.0936062
[3450]	valid_0&#39;s l2: 0.0933644
[3500]	valid_0&#39;s l2: 0.0932538
[3550]	valid_0&#39;s l2: 0.0931197
[3600]	valid_0&#39;s l2: 0.092991
[3650]	valid_0&#39;s l2: 0.0928117
[3700]	valid_0&#39;s l2: 0.0925179
[3750]	valid_0&#39;s l2: 0.0923399
[3800]	valid_0&#39;s l2: 0.0922045
[3850]	valid_0&#39;s l2: 0.0919938
[3900]	valid_0&#39;s l2: 0.0918291
[3950]	valid_0&#39;s l2: 0.0915838
[4000]	valid_0&#39;s l2: 0.0913641
[4050]	valid_0&#39;s l2: 0.0912247
[4100]	valid_0&#39;s l2: 0.0911004
[4150]	valid_0&#39;s l2: 0.0908671
[4200]	valid_0&#39;s l2: 0.0907151
Early stopping, best iteration is:
[4216]	valid_0&#39;s l2: 0.0906865
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[93]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 진짜 라벨 소환</span>
<span class="n">label</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">label</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">label</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">label</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">2013</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">10</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[93]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>year</th>
      <th>doy</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5113</th>
      <td>2013.0</td>
      <td>1.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5114</th>
      <td>2013.0</td>
      <td>2.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5115</th>
      <td>2013.0</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5116</th>
      <td>2013.0</td>
      <td>4.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5117</th>
      <td>2013.0</td>
      <td>5.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5118</th>
      <td>2013.0</td>
      <td>6.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5119</th>
      <td>2013.0</td>
      <td>7.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5120</th>
      <td>2013.0</td>
      <td>8.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5121</th>
      <td>2013.0</td>
      <td>9.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>5122</th>
      <td>2013.0</td>
      <td>10.0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;predict done&#39;</span><span class="p">)</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">pred</span><span class="p">)):</span>
  <span class="k">if</span> <span class="n">pred</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">0</span><span class="p">:</span>
    <span class="n">pred</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
  <span class="k">else</span><span class="p">:</span> <span class="n">pred</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">pred</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="c1">#pred=np.round(pred)</span>
<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;pred&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">pred</span>
<span class="n">y_pred</span><span class="o">=</span><span class="p">{}</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
  <span class="n">y_pred</span><span class="p">[</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">x_test</span><span class="p">[</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;pred&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)[</span><span class="mi">1</span><span class="p">])</span>
  

<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;voting done&#39;</span><span class="p">)</span>
<span class="n">y_pred</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">y_pred</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
<span class="n">y_pred</span><span class="o">=</span><span class="n">y_pred</span><span class="o">.</span><span class="n">T</span>
<span class="n">y_pred</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">y_pred</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="mi">0</span><span class="p">:</span><span class="s1">&#39;pred&#39;</span><span class="p">,</span><span class="s1">&#39;index&#39;</span><span class="p">:</span><span class="s1">&#39;doy&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">y_pred</span>
  
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[106]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_test</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">y_test</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">label</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">label</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">2013</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span>

<span class="n">y_test</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>


<span class="n">sum_weight</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">(</span><span class="n">y_test</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;weighted rmse: &quot;</span><span class="p">,</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">((</span><span class="n">y_test</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">/</span><span class="n">sum_weight</span><span class="p">)</span><span class="o">*</span><span class="p">(</span><span class="n">y_pred</span><span class="p">[</span><span class="s1">&#39;pred&#39;</span><span class="p">]</span><span class="o">-</span><span class="n">y_test</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">])</span><span class="o">**</span><span class="mi">2</span><span class="p">)))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>weighted rmse:  2.0464893871899723
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#weight rmse from 개최자</span>
<span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>

<span class="c1">#multiclass</span>
<span class="c1">#pred=[np.argmax(y_pred[i]) for i in range(len(y_pred))]</span>

<span class="c1">#regression</span>
<span class="n">pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">y_pred</span><span class="p">)</span>


<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">pred=[0 for i in range(len(y_valid))]</span>
<span class="sd">for i in range(len(y_pred)):</span>
<span class="sd">  if y_pred[i]-int(y_pred[i])&gt;0.4:</span>
<span class="sd">    pred[i]=int(y_pred[i])+1</span>
<span class="sd">  else:</span>
<span class="sd">    pred[i]=int(y_pred[i])</span>

<span class="sd">&#39;&#39;&#39;</span>


<span class="n">sum_weight</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">(</span><span class="n">y_test</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;weighted rmse: &quot;</span><span class="p">,</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">((</span><span class="n">y_test</span><span class="o">/</span><span class="n">sum_weight</span><span class="p">)</span><span class="o">*</span><span class="p">(</span><span class="n">pred</span><span class="o">-</span><span class="n">y_test</span><span class="p">)</span><span class="o">**</span><span class="mi">2</span><span class="p">)))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="&#51204;&#52404;&#50640;-&#46972;&#48296;-&#48537;&#51060;&#44592;">&#51204;&#52404;&#50640; &#46972;&#48296; &#48537;&#51060;&#44592;<a class="anchor-link" href="#&#51204;&#52404;&#50640;-&#46972;&#48296;-&#48537;&#51060;&#44592;">&#182;</a></h1><hr>
<h1 id="&#51060;&#48120;-&#48537;&#50612;-&#51080;&#50632;&#51020;-&#12619;&#12619;">&#51060;&#48120; &#48537;&#50612; &#51080;&#50632;&#51020; &#12619;&#12619;<a class="anchor-link" href="#&#51060;&#48120;-&#48537;&#50612;-&#51080;&#50632;&#51020;-&#12619;&#12619;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">label</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label.csv&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">time_label</span><span class="o">=</span><span class="p">[</span><span class="n">label</span><span class="p">[[</span><span class="s1">&#39;kp_&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]]</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="c1">#datetime 형식으로 변형</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;date&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">to_datetime</span><span class="p">(</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;date&#39;</span><span class="p">],</span><span class="nb">format</span><span class="o">=</span><span class="s2">&quot;%Y-%m-</span><span class="si">%d</span><span class="s2">&quot;</span><span class="p">,</span><span class="n">errors</span><span class="o">=</span><span class="s1">&#39;ignore&#39;</span><span class="p">)</span>
  
<span class="c1">#doy 계산</span>
<span class="kn">import</span> <span class="nn">datetime</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;date&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">dayofyear</span>
  
<span class="c1">#label 이름 변경</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
                      <span class="p">)</span>
<span class="n">time_label</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#시간대별로 나눈것을 년도별로 나누기</span>
<span class="n">doy</span><span class="o">=</span><span class="p">[[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">15</span><span class="p">)]</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][:</span><span class="mi">365</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">365</span><span class="p">:</span><span class="mi">731</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">731</span><span class="p">:</span><span class="mi">1096</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">1096</span><span class="p">:</span><span class="mi">1461</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">1461</span><span class="p">:</span><span class="mi">1826</span><span class="p">]</span>
  
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">1826</span><span class="p">:</span><span class="mi">2192</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">2192</span><span class="p">:</span><span class="mi">2557</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">2557</span><span class="p">:</span><span class="mi">2922</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">8</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">2922</span><span class="p">:</span><span class="mi">3287</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">9</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">3287</span><span class="p">:</span><span class="mi">3653</span><span class="p">]</span>
  
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">10</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">3653</span><span class="p">:</span><span class="mi">4018</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">11</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">4018</span><span class="p">:</span><span class="mi">4383</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">12</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">4383</span><span class="p">:</span><span class="mi">4748</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">13</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">4748</span><span class="p">:</span><span class="mi">5114</span><span class="p">]</span>
  <span class="n">doy</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">14</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">5114</span><span class="p">:]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[107]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">all_merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">all_merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">all_merged</span><span class="p">,</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">all_merged</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[107]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(7425580, 12)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[108]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">all_merged</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">all_merged</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[108]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>year</th>
      <th>doy</th>
      <th>hr</th>
      <th>min</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>7.149000</td>
      <td>92352.000000</td>
      <td>4.060000e+02</td>
      <td>-2.174</td>
      <td>-2.598</td>
      <td>5.550</td>
      <td>6.630</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>5.998000</td>
      <td>85859.000000</td>
      <td>4.191200e+02</td>
      <td>-1.245</td>
      <td>-0.140</td>
      <td>6.558</td>
      <td>6.796</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>6.211000</td>
      <td>81547.000000</td>
      <td>4.119900e+02</td>
      <td>-2.003</td>
      <td>-1.198</td>
      <td>6.306</td>
      <td>6.802</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>6.680000</td>
      <td>72308.000000</td>
      <td>4.052500e+02</td>
      <td>-3.093</td>
      <td>-2.483</td>
      <td>5.545</td>
      <td>6.854</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>4.0</td>
      <td>422.056974</td>
      <td>70502.368054</td>
      <td>9.297115e+199</td>
      <td>-3.009</td>
      <td>-1.500</td>
      <td>5.908</td>
      <td>6.842</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
