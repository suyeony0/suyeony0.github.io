---
layout: post
title: COVID-19 - Death Prediction
date: 2020-06-06
description: Cross validation score was not that good. I have mis-predicted by 7 people.
thumbnail: food2.jpg
categories: DataMining

# Information for the author block
author : Loui
---

<html>
<head><meta charset="utf-8" />

<title>COVID-19 - Death Prediction</title>

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
<h1 id="Import-Libararies">Import Libararies<a class="anchor-link" href="#Import-Libararies">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Load-Data">Load Data<a class="anchor-link" href="#Load-Data">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Public Data/Corona Virus/Data/CoronaFrom0302.csv&#39;</span><span class="p">,</span><span class="n">parse_dates</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;stateDt&#39;</span><span class="p">],</span><span class="n">encoding</span><span class="o">=</span><span class="s1">&#39;UTF-8&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df_sex</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Public Data/Corona Virus/Data/CoronaWithSex.csv&#39;</span><span class="p">,</span><span class="n">parse_dates</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;createDt&#39;</span><span class="p">],</span><span class="n">encoding</span><span class="o">=</span><span class="s1">&#39;UTF-8&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Make-Month-and-day-columns">Make Month and day columns<a class="anchor-link" href="#Make-Month-and-day-columns">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">iloc</span><span class="p">[:</span><span class="mi">94</span><span class="p">]</span>
<span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;updateDt&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df_sex</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;updateDt&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;stateDt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;day&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;stateDt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span>
<span class="n">df_sex</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df_sex</span><span class="p">[</span><span class="s1">&#39;createDt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span>
<span class="n">df_sex</span><span class="p">[</span><span class="s1">&#39;day&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df_sex</span><span class="p">[</span><span class="s1">&#39;createDt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span>
<span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;stateDt&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df_sex</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;createDt&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[4]:</div>



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
      <th>accDefRate</th>
      <th>accExamCnt</th>
      <th>accExamCompCnt</th>
      <th>careCnt</th>
      <th>clearCnt</th>
      <th>createDt</th>
      <th>deathCnt</th>
      <th>decideCnt</th>
      <th>examCnt</th>
      <th>resutlNegCnt</th>
      <th>seq</th>
      <th>stateTime</th>
      <th>month</th>
      <th>day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.305152</td>
      <td>902901.0</td>
      <td>876603.0</td>
      <td>774.0</td>
      <td>10398.0</td>
      <td>12:26.8</td>
      <td>269.0</td>
      <td>11441.0</td>
      <td>26298.0</td>
      <td>865162.0</td>
      <td>154.0</td>
      <td>0:00</td>
      <td>5</td>
      <td>30</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.324947</td>
      <td>885120.0</td>
      <td>860563.0</td>
      <td>770.0</td>
      <td>10363.0</td>
      <td>10:53.1</td>
      <td>269.0</td>
      <td>11402.0</td>
      <td>24557.0</td>
      <td>849161.0</td>
      <td>153.0</td>
      <td>0:00</td>
      <td>5</td>
      <td>29</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1.340429</td>
      <td>868666.0</td>
      <td>846296.0</td>
      <td>735.0</td>
      <td>10340.0</td>
      <td>11:27.9</td>
      <td>269.0</td>
      <td>11344.0</td>
      <td>22370.0</td>
      <td>834952.0</td>
      <td>152.0</td>
      <td>0:00</td>
      <td>5</td>
      <td>28</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.354267</td>
      <td>852876.0</td>
      <td>831815.0</td>
      <td>701.0</td>
      <td>10295.0</td>
      <td>16:33.1</td>
      <td>269.0</td>
      <td>11265.0</td>
      <td>21061.0</td>
      <td>820550.0</td>
      <td>151.0</td>
      <td>0:00</td>
      <td>5</td>
      <td>27</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.373205</td>
      <td>839475.0</td>
      <td>817431.0</td>
      <td>681.0</td>
      <td>10275.0</td>
      <td>12:48.7</td>
      <td>269.0</td>
      <td>11225.0</td>
      <td>22044.0</td>
      <td>806206.0</td>
      <td>150.0</td>
      <td>0:00</td>
      <td>5</td>
      <td>26</td>
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
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_sex</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[5]:</div>



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
      <th>confCase</th>
      <th>confCaseRate</th>
      <th>criticalRate</th>
      <th>death</th>
      <th>deathRate</th>
      <th>gubun</th>
      <th>seq</th>
      <th>month</th>
      <th>day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>157</td>
      <td>1.37</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0-9</td>
      <td>1124</td>
      <td>5</td>
      <td>31</td>
    </tr>
    <tr>
      <th>1</th>
      <td>655</td>
      <td>5.71</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>10-19</td>
      <td>1123</td>
      <td>5</td>
      <td>31</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3176</td>
      <td>27.69</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>20-29</td>
      <td>1122</td>
      <td>5</td>
      <td>31</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1292</td>
      <td>11.27</td>
      <td>0.15</td>
      <td>2</td>
      <td>0.74</td>
      <td>30-39</td>
      <td>1121</td>
      <td>5</td>
      <td>31</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1521</td>
      <td>13.26</td>
      <td>0.20</td>
      <td>3</td>
      <td>1.11</td>
      <td>40-49</td>
      <td>1120</td>
      <td>5</td>
      <td>31</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Combine-the-two-data-set">Combine the two data set<a class="anchor-link" href="#Combine-the-two-data-set">&#182;</a></h2><h3 id="match-their-dates">match their dates<a class="anchor-link" href="#match-their-dates">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">temp2</span><span class="o">=</span><span class="n">df_sex</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">temp</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">month</span><span class="o">!=</span><span class="mi">3</span><span class="p">]</span>
<span class="n">temp</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">iloc</span><span class="p">[:</span><span class="mi">62</span><span class="p">]</span>
<span class="n">temp2</span><span class="o">=</span><span class="n">df_sex</span><span class="o">.</span><span class="n">iloc</span><span class="p">[</span><span class="mi">11</span><span class="p">:]</span>

<span class="n">death_rate</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">pivot_table</span><span class="p">(</span><span class="n">temp2</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">,</span><span class="s1">&#39;day&#39;</span><span class="p">],</span><span class="n">aggfunc</span><span class="o">=</span><span class="s1">&#39;mean&#39;</span><span class="p">)</span>
<span class="n">death_rate</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">temp2</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">pivot_table</span><span class="p">(</span><span class="n">temp2</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">,</span><span class="s1">&#39;day&#39;</span><span class="p">],</span><span class="n">aggfunc</span><span class="o">=</span><span class="nb">sum</span><span class="p">)</span>
<span class="n">temp2</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">train</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">temp</span><span class="p">,</span><span class="n">temp2</span><span class="p">,</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">,</span><span class="s1">&#39;day&#39;</span><span class="p">])</span>
<span class="n">train</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="n">train</span><span class="o">.</span><span class="n">death</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span>
<span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;seq_x&#39;</span><span class="p">,</span><span class="s1">&#39;seq_y&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;deathRate&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">death_rate</span><span class="p">[</span><span class="s1">&#39;deathRate&#39;</span><span class="p">]</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;confCaseRate&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">death_rate</span><span class="p">[</span><span class="s1">&#39;confCaseRate&#39;</span><span class="p">]</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;criticalRate&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">death_rate</span><span class="p">[</span><span class="s1">&#39;criticalRate&#39;</span><span class="p">]</span>

<span class="c1"># we can&#39;t use below features since they affect to deathCNT directly.</span>
<span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;confCase&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;confCaseRate&#39;</span><span class="p">,</span><span class="s1">&#39;death&#39;</span><span class="p">,</span><span class="s1">&#39;createDt&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;stateTime&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">train</span><span class="o">.</span><span class="n">dropna</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">train</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[8]:</div>



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
      <th>accDefRate</th>
      <th>accExamCnt</th>
      <th>accExamCompCnt</th>
      <th>careCnt</th>
      <th>clearCnt</th>
      <th>deathCnt</th>
      <th>decideCnt</th>
      <th>examCnt</th>
      <th>resutlNegCnt</th>
      <th>month</th>
      <th>day</th>
      <th>criticalRate</th>
      <th>deathRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.305152</td>
      <td>902901.0</td>
      <td>876603.0</td>
      <td>774.0</td>
      <td>10398.0</td>
      <td>269.0</td>
      <td>11441.0</td>
      <td>26298.0</td>
      <td>865162.0</td>
      <td>5</td>
      <td>30</td>
      <td>2.870909</td>
      <td>18.182727</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.324947</td>
      <td>885120.0</td>
      <td>860563.0</td>
      <td>770.0</td>
      <td>10363.0</td>
      <td>269.0</td>
      <td>11402.0</td>
      <td>24557.0</td>
      <td>849161.0</td>
      <td>5</td>
      <td>29</td>
      <td>3.003333</td>
      <td>16.750000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1.340429</td>
      <td>868666.0</td>
      <td>846296.0</td>
      <td>735.0</td>
      <td>10340.0</td>
      <td>269.0</td>
      <td>11344.0</td>
      <td>22370.0</td>
      <td>834952.0</td>
      <td>5</td>
      <td>28</td>
      <td>3.291818</td>
      <td>18.181818</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.354267</td>
      <td>852876.0</td>
      <td>831815.0</td>
      <td>701.0</td>
      <td>10295.0</td>
      <td>269.0</td>
      <td>11265.0</td>
      <td>21061.0</td>
      <td>820550.0</td>
      <td>5</td>
      <td>27</td>
      <td>3.360000</td>
      <td>18.181818</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.373205</td>
      <td>839475.0</td>
      <td>817431.0</td>
      <td>681.0</td>
      <td>10275.0</td>
      <td>269.0</td>
      <td>11225.0</td>
      <td>22044.0</td>
      <td>806206.0</td>
      <td>5</td>
      <td>26</td>
      <td>3.410909</td>
      <td>18.181818</td>
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
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">by</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">,</span><span class="s1">&#39;day&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">train</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[6]:</div>



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
      <th>accDefRate</th>
      <th>accExamCnt</th>
      <th>accExamCompCnt</th>
      <th>careCnt</th>
      <th>clearCnt</th>
      <th>deathCnt</th>
      <th>decideCnt</th>
      <th>examCnt</th>
      <th>resutlNegCnt</th>
      <th>month</th>
      <th>day</th>
      <th>criticalRate</th>
      <th>deathRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>53</th>
      <td>2.175074</td>
      <td>494711.0</td>
      <td>479202.0</td>
      <td>3246.0</td>
      <td>6973.0</td>
      <td>204.0</td>
      <td>10423.0</td>
      <td>15509.0</td>
      <td>468779.0</td>
      <td>4</td>
      <td>9</td>
      <td>4.179091</td>
      <td>18.182727</td>
    </tr>
    <tr>
      <th>52</th>
      <td>2.142478</td>
      <td>503051.0</td>
      <td>487753.0</td>
      <td>3125.0</td>
      <td>7117.0</td>
      <td>208.0</td>
      <td>10450.0</td>
      <td>15298.0</td>
      <td>477303.0</td>
      <td>4</td>
      <td>10</td>
      <td>4.195455</td>
      <td>18.182727</td>
    </tr>
    <tr>
      <th>51</th>
      <td>2.111162</td>
      <td>510479.0</td>
      <td>496409.0</td>
      <td>3026.0</td>
      <td>7243.0</td>
      <td>211.0</td>
      <td>10480.0</td>
      <td>14070.0</td>
      <td>485929.0</td>
      <td>4</td>
      <td>11</td>
      <td>4.214545</td>
      <td>18.182727</td>
    </tr>
    <tr>
      <th>50</th>
      <td>2.098903</td>
      <td>514621.0</td>
      <td>500833.0</td>
      <td>2930.0</td>
      <td>7368.0</td>
      <td>214.0</td>
      <td>10512.0</td>
      <td>13788.0</td>
      <td>490321.0</td>
      <td>4</td>
      <td>12</td>
      <td>4.220000</td>
      <td>18.182727</td>
    </tr>
    <tr>
      <th>49</th>
      <td>2.085081</td>
      <td>518743.0</td>
      <td>505352.0</td>
      <td>2873.0</td>
      <td>7447.0</td>
      <td>217.0</td>
      <td>10537.0</td>
      <td>13391.0</td>
      <td>494815.0</td>
      <td>4</td>
      <td>13</td>
      <td>4.232727</td>
      <td>18.182727</td>
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
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cols</span> <span class="o">=</span> <span class="n">train</span><span class="o">.</span><span class="n">columns</span>
<span class="n">fig</span><span class="p">,</span> <span class="n">axes</span><span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">13</span><span class="p">)</span>
<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span><span class="mi">130</span><span class="p">)</span>

<span class="k">for</span> <span class="n">axe</span> <span class="ow">in</span> <span class="n">axes</span><span class="p">:</span>
  <span class="n">plt</span><span class="o">.</span><span class="n">sca</span><span class="p">(</span><span class="n">axe</span><span class="p">)</span>
  <span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">rotation</span><span class="o">=</span><span class="mi">30</span><span class="p">,</span><span class="n">ha</span><span class="o">=</span><span class="s1">&#39;right&#39;</span><span class="p">)</span>



<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;accDefRate&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;accExamCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;accExamCompCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">2</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;clearCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">3</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">4</span><span class="p">])</span>

<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;decideCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">5</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;examCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">6</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;resutlNegCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">7</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;month&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">8</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;day&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">9</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;criticalRate&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">10</span><span class="p">])</span>

<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;deathRate&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">11</span><span class="p">])</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;careCnt&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">axes</span><span class="p">[</span><span class="mi">12</span><span class="p">])</span>

<span class="n">plt</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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AACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLwAAAICuCS8AAACArgkvAAAAgK4JLyZSSnlIKeWvSynXlFKes9X1AAAAwKoQXkyglLJfklcleWiSk5M8oZRy8tZWBQAAAKtBeDGN05JcU2v9u1rrfyW5JMkZW1wTAAAArAThxTSOSfLp0f3PtGkAAADAJpVa61bXcINXSnlMkofUWr+/3X9SknvWWs8ePeesJGe1u3dK8tcbaPrwJP8yQYlTtdNrWz3WNGVbPdY0ZVs91jRlWz3W1GtbPdY0ZVs91jRlWz3WNGVbPdY0ZVs91jRlWz3WNGVbPdY0ZVs91jRlWz3WNGVbPdY0ZVs91jRlW/u6ptvWWrev98C2iYq4sbs2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asILAAAAYGrCCwAAAGBqwostVNVLquqTVfW+xWMnVNXbq+oD4/fx4/Gqqp+tqg9W1Xur6uZ713IAAADYf4QXW3tZkruvPfbkJOe01k5Ncs64nyRnJDl1/Jyd5AUXUxsBAADgq4LwYguttXcl+dTaw2cmefm4/fIk9148/orW/UmSy1XVyRdPSwEAAGD/E15s30mttY+N2x9PctK4feUk/7yY7qPjsfOpqrOr6j1V9Z7zzjvvom0pAAAA7CPCi11orbUkbYeveVFr7bTW2mknnnjiRdQyAAAA2H+EF9v3idXXQcbvT47Hz01ylcV0p4zHAAAAgA0QXmzfG5OcNW6fleQNi8cfMv7ryOlJPr34egkAAABwmI7c6wbMqKpeneSOSa5QVR9N8sNJnpvkNVX1iCQfSXL/Mfmbk9wjyQeTfC7Jwy72BgMAAMA+JrzYQmvtgQd56s5bTNuSPPqibREAAAB89fK1EQAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGrCCwAAAGBqwgsAAABgasILAAAAYGpH7nUDvtJU1YeTfDbJF5N8obV2WlWdkOTXk1wtyYeT3L+19q971UYAAADYT5x5sTt3aq3dtLV22rj/5CTntNZOTXLOuA8AAABsgPBiM85M8vJx++VJ7r2HbQEAAIB9RXixcy3J26rqz6vq7PHYSa21j43bH09y0vqLqursqnpPVb3nvPPOu7jaCgAAAF/xXPNi527fWju3qq6Y5O1V9XfLJ1trrara+otaay9K8qIkOe200y7wPAAAALA1Z17sUGvt3PH7k0lel+RWST5RVScnyfj9yb1rIQAAAOwvwosdqKrLVNVxq9tJ7prkfUnemOSsMdlZSd6wNy0EAACA/cfXRnbmpCSvq6qkL7tXtdbeUlXvTvKaqnpEko8kuf8ethEAAAD2FeHFDrTWPpTkJls8/r+T3PnibxEAAADsf742AgAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABMTXgBAAAATE14AQAAAExNeAEAAABM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AMsptdbNLgMAAADAkvS8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNf23uwC7IkOPPDAethhh212MQAAAKAbH/3oR79Ra9222HOSF5vgsMMOy8UXX7zZxQAAAIBulFK+uNRzho0AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6JrkBQAAANA1yQsAAACga5IXAAAAQNckLwAAAICuSV4AAAAAXZO8AAAAALomeQEAAAB0TfICAAAA6Nrem10AAAAAoG9ff8lbNyz2Qaf87A5fo+cFAAAA0DXJCwAAAKBrkhcAAABA18x5AQAAALuhr7/ogg2Je9Cv3G1D4u4MPS8AAACArul5AQAAAOvgay+8cEPiXucJx25I3N2JnhcAAABA1yQvAAAAgK5JXgAAAABdk7wAAAAAumbCTgAAALakrz7vkxsS9+An3mpD4rI0PS8AAACArul5AQAAwC7x1dO+uGGxD/7NG25YbDafnhcAAABA1/S8AAAA2IP90+lf3ZC4h//qwRsSlz2TnhcAAABA1yQvAAAAgK5JXgAAAABdk7wAAAAAumbCTgAAgI58/OVf35C4t33sQRsSF3YFPS8AAACArul5AQAAsIz3vfayDYl7l4dv25C4sBXpeQEAAAB0Tc8LAABg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XdPzAgAA6M67Tpuvx8QRR+ktAYtIzwsAAACga3peAAAAbIO+9OoL5572RsfvMWFL4LKn5wUAAADQNeEFAAAA0DXhBQAAANA14QUAAADQNV/YCQAAsBWdfepFc0138LHXmLglsO3Q8wIAAADomvACAAAA6JrwAgAAAOia77wAAADYgo+/6eK5p/29B22YsCVw+aTnBQAAANA14QUAAADQNeEFAAAA0DXhBQAAANA1X9gJAABwOfaNl35v7mmv/dhrTtgS2DQ9LwAAAICu6XkBAADAQvreyV+Ye9prPuHGE7aEtdLzAgAAAOia8AIAAADomvACAAAA6JrwAgAAAOia8AIAAADomvACAAAA6JrwAgAAAOia8AIAAADo2vbr3QAAAACY9b0Xnjf3tNf84+tO2BJ6oecFAAAA0DXhBQAAANA14QUAAADQNeEFAAAA0DXhBQAAANA1/20EAAAAtpILX/aJuafd46Q7TNiSbYueFwAAAEDXhBcAAABA14QXAAAAQNeEFwAAAEDXhBcAAABA14QXAAAAQNeEFwAAAEDXhBcAAABA14QXAAAAQNeEFwAAAEDXhBcAAABA17Zf7wYAAAAA276LXvGOuae9xglHbna8nhcAAABA14QXAAAAQNeEFwAAAEDXhBcAAABA14QXAAAAQNf8txEAAAC4HLvor98713TXOPEeE7dk0/S8AAAAALomvAAAAAC6JrwAAAAAuia8AAAAALomvAAAAAC6JrwAAAAAuuZfpQIAAMA25qKXf3juaa/xmN+fsCVbh54XAAAAQNeEFwAAAEDXhBcAAABA14QXAAAAQNeEFwAAAEDX/LcRAAAA2IILX/KZuabb43G3mrgll096XgAAAABdE14AAAAAXRNeAAAAAF0TXgAAAABdE14AAAAAXRNeAAAAAF0TXgAAAABdE14AAAAAXdt+vRsAAADAYrjg+f8+13R7PnmviVvCotHzAgAAAOia8AIAAADomvACAAAA6JrwAgAAAOia8AIAAADomvBimarat6r+uaq+XFVfqqrHjsN3raoPVdXXx9+7jMOrql5WVedV1eer6hbr+w4AAABgsQgvftsvkzyxtXZQktskOaGqDkry1CRnttYOTHLm+DxJDk1y4PhzXJJXbv0mAwAAwOISXizTWrugtfbZ8fFPk3wlyd5JDk/yhvFlb0hyxPj48CRvbINP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
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
<h1 id="Correlation">Correlation<a class="anchor-link" href="#Correlation">&#182;</a></h1><h3 id="as-we-can-see,-most-columns-has-a-quite-high-correlation-with-deathCNT">as we can see, most columns has a quite high correlation with deathCNT<a class="anchor-link" href="#as-we-can-see,-most-columns-has-a-quite-high-correlation-with-deathCNT">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">corrMat</span><span class="o">=</span><span class="n">train</span><span class="o">.</span><span class="n">corr</span><span class="p">()</span>
<span class="n">mask</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">corrMat</span><span class="p">)</span>
<span class="n">mask</span><span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">tril_indices_from</span><span class="p">(</span><span class="n">mask</span><span class="p">)]</span><span class="o">=</span><span class="kc">False</span>

<span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>
<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span><span class="mi">10</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">corrMat</span><span class="p">,</span><span class="n">mask</span><span class="o">=</span><span class="n">mask</span><span class="p">,</span><span class="n">vmax</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">square</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[10]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f06bf347e80&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAwIAAAKTCAYAAACq8b/qAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjEsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+j8jraAAAgAElEQVR4nOzdZ5QU1daH8WczcE0kyTknFRQliAFkJCNREBVQEBQw4dUrRswgGECvwgXBV1HMWVQEyUmRIBlUokoWEVBBgZn9fuhinCHMDNIzPVD/31q16K46VWd39bBW7drnVJu7IyIiIiIi4ZIt1gGIiIiIiEjmUyIgIiIiIhJCSgREREREREJIiYCIiIiISAgpERARERERCSElAiIiIiIiIaREQEREREQkhsysqZl9Z2arzOyew2wvZWZTzGyBmS02s+ZR6Ve/IyAiIiIiEhtmFgd8DzQC1gNzgavdfXmyNiOABe4+zMzOBMa6e5lj7VsVARERERGR2KkNrHL3Ne6+F3gLaH1QGwdyB6/zABuj0XH2aBxEMta+bWuOi7JNjgLlYh2CiIiIRI/FOoCMktnXVv8qWL4n0CPZqhHuPiJ4XRz4Kdm29cD5Bx3iYeALM7sVOA1oGI24lAiIiIiIiGSg4KJ/RJoNj+xqYJS7DzKzC4DRZlbV3ROPJS4NDRIRERERiZ0NQMlk70sE65LrDrwD4O5fAScDBY61Y1UERERERCRcEhNiHUFyc4GKZlaWSAJwFdDxoDY/Ag2AUWZ2BpFE4Odj7VgVARERERGRGHH3/cAtwHhgBfCOuy8zs0fNrFXQ7D/ADWa2CHgT6OpRePSnHh96HNBkYREREYmBE3ey8JbvMvXaKkfhylnyXKoiICIiIiISQpojICIiIiLhknhMD9s5YagiICIiIiISQqoIiIiIiEioHOPj908YqgiIiIiIiISQKgIiIiIiEi6aIwCoIiAiIiIiEkpKBEREREREQkhDg0REREQkXDRZGFBFQEREREQklFQREBEREZFwSUyIdQRZgioCIdP38cHUu+wq2nTuFetQRERERCSGQpMImNk6M1sSLMvNrJ+ZnZyO/Xqb2Qoze93MuprZz2a20My+NbPb07F/VzMrFp1PcezaNG/E8MH9Yh2GiIiISOx4YuYuWVRoEoFAvLtXA2oD5YAX0rHPTUAjd+8UvH/b3asDFwH3m1nJNPbvCmSZRKBm9WrkyZ0r1mGIiIiISIwdN4mAmX1kZvPNbJmZ9QjWNTWzb8xskZlNCtblNLOXgzv/i82s3cHHcvffgV5AGzPLF+zXx8zmBvs8EqwbTiRh+Pzgu//u/guwCigatH0w2H+pmY2wiPZATeD1oIpwipnVMLNpwWcZb2ZFM+qciYiIiMhhJCZm7pJFHTeJANDN3WsQubDubWaFgZFAO3c/B7giaPcAsNPdq7n72cDkwx3M3XcBa4GKZtYYqEikUlAdqGFm9dy9F7CRSCXhmeT7m1kp4GRgcbBqiLvXcveqwClAC3d/D5gHdAqqCPuB54H2wWd5Ceh/uPjMrIeZzTOzeS+++ubRnisRERERkVQdT08N6m1mbYPXJYEewHR3Xwvg7tuDbQ2Bqw7s5O6/pnJMC/5tHCwLgvc5iSQG0w+zz5VmVg+oAtzi7n8G6+PN7C7gVCAfsAz45KB9KwNVgQlmBhAHbDpcYO4+AhgBsG/bGk/lM4iIiIjIUfAsPG4/Mx0XiYCZ1SdygX+Bu+82s6nAQiIX4//0mLmAMsD3RBKCAe6enjkDb7v7LWZWE/jCzMYAO4D/ATXd/Scze5hIteCQboFl7n7BP41bRERERCQajpehQXmAX4MkoApQh8iFdj0zKwtwYKw/MAG4+cCOZnb6wQczs5xELtw/CioG44FuwXrMrLiZFUotIHefB4wGbuPvi/5twTHaJ2v6G3Bgdu53QEEzuyDoJ4eZnZXOcxAVfR4aSKeet7Pux/U0aNOZ9z8Zn5ndi4iIiMSe5ggAx0lFABgH9DKzFUQupmcDPxMZHvSBmWUDtgKNgH7AUDNbCiQAjwAfBMeZYpExOdmAD4HHANz9CzM7A/gqGLLzO9A5OGZqngC+AR4nMl9hKbAZmJuszShguJntAS4gkiQ8Z2Z5iJz/Z4kMI8oUTz1yT2Z1JSIiIiJZmLlr+HlWd7zMEchRoFysQxAREZHosbSbHJ/++n5mpl5bnVTp4ix5Lo+XoUEiIiIiIhJFx8vQIBERERGR6EhMiHUEWYIqAiIiIiIiIaREQEREREQkhDQ0SERERETCRT8oBqgiICIiIiISSqoIiIiIiEi4ZOEf+cpMqgiIiIiIiISQKgIiIiIiEi6aIwCoIiAiIiIiEkqqCIiIiIhIuGiOAKCKgIiIiIhIKKkiICIiIiKh4p4Q6xCyBFUERERERERCSBUBEREREQkXPTUIUCJwXDiteL1Yh5CmPzZMZ9+2NbEOI11yFCgX6xBEREREYk6JgIiIiIiEi54aBGiOgIiIiIhIKKkiICIiIiLhojkCgCoCIiIiIiKhpERARERERCSENDRIRERERMIlUT8oBqoIiIiIiIiEkioCIiIiIhIumiwMqCIgIiIiIhJKqgiIiIiISLjoB8UAVQREREREREJJFQERERERCRfNEQBUERARERERCSVVBEREREQkXDRHAFBFQEREREQklJQIiIiIiEi4JCZm7pIGM2tqZt+Z2Sozu+cIbTqY2XIzW2Zmb0TjNCgROEENHvwoy5fPZP68CVSvXvWwba5o35L58yawcMEkHu9/X9L6p556iLlzxjN3zniWLZ3O1i3LMivsJH0fH0y9y66iTedemd63iIiISGYxszhgKNAMOBO42szOPKhNReBe4CJ3Pwv4dzT6PmETATNbZ2ZLzGxhsDyXwf0VMbO3zGy1mc03s7FmVimNff5tZqdGO5amTS+lQoWynHnmxdx4090MeX7AIW3y5cvLgAF9adL0Sqqf24DChQsSH38RAH36PEKt2k2oVbsJQ//3Mh999Hm0Q0xTm+aNGD64X6b3KyIiIic+94RMXdJQG1jl7mvcfS/wFtD6oDY3AEPd/ddI/L41GufhhE0EAvHuXj1YemdUJ2ZmwIfAVHcv7+41iGRthdPY9d9A1BOBli0b8/pr7wEwZ8435M2bmyJFCqVoU7ZsaVatXsu2bdsBmDx5Jm3bNj/kWFd2aM3b73wc7RDTVLN6NfLkzpXp/YqIiIhEm5n1MLN5yZYeyTYXB35K9n59sC65SkAlM5tlZrPNrGk04sqyiYCZfRTcWV924GQF46e+MbNFZjYpWJfTzF4O7v4vNrN2qRwzu5nNNbP6wfsBZtY/eP1gsG2pmY0ILu4xs6lm9kzwpa0ws1pm9oGZrTSzA7es44F97j78QF/uvsjdZ5hZ/eAY75nZt2b2ukX0BooBU8xsSjTPXbFiRfhp/cak9+s3bKJYsSIp2qxevY5KFctTunQJ4uLiaNWqCSVLFEvRplSp4pQpU5IpU2ZFMzwRERGR2MrkOQLuPsLdayZbRhxlxNmBikB94GpgpJnlPdbTkJUfH9rN3beb2SnAXDP7GBgJ1HP3tWaWL2j3ALDT3asBmNnpyY4xxcwO1GNecfdnzKwr8J6Z3Qo0Bc4Ptg9x90eDY4wGWgCfBNv2untNM7sN+BioAWwHVpvZM0BVYH4qn+Vc4CxgIzCLyPiu58zsDiJVi20H7xAkPz0A4uLyki3utLTP2FHYsWMnt/a+l9dfG0ZiYiJfzZ5H+XKlU7TpcEVrPvhwLIl6xJaIiIhIRtkAlEz2vkSwLrn1wNfuvg9Ya2bfE0kM5h5Lx1k5EehtZm2D1yWJXBRPd/e1AO6+PdjWELjqwE4Hxk4FDrnIdvdlwYX+p8AFwVgsgHgzu4vIUJ18wDL+TgTGBP8uAZa5+yYAM1tDyi/uSOa4+/pgn4VAGWBmajsEmeIIgH+dVMLT6qBXry5079YRgHnzFqW4u1+ieFE2btx8yD6ffTaRzz6bCED37p1ITEh5wd+hQyt633Z/Wl2LiIiIyD83F6hoZmWJJABXAR0PavMRkUrAy2ZWgMhQoTXH2nGWHBoUDN1pSORC/RxgAbAwil1UA3YAhYL+Tgb+B7QPKgsjgZOTtf8r+Dcx2esD77MTSRpqpNJf8n0SyIAEbPjwV5Im+I75ZBydOrcHoHbt89i58zc2bz50TknBgvkByJs3D716XstLL//9JKrKlcuTN28eZs9OrdAhIiIichzyxMxdUgvFfT9wCzAeWAG8E9y4ftTMWgXNxgO/mNlyYArQx91/OdbTkCUTASAP8Ku77zazKkAdIhfm9YJsiWRDgyYANx/Y8aChQYcws8uJ3PGvBzwfjK86cNG/zcxyAu2PMt7JwEnJJ36Y2dlmVjeN/X4Doj4j9vPPJ7N27Q+sWDGT4cOe5Nbefz8adO6c8UmvBw96hEULJzNt6oc89dRQVq5cm7StwxWteffdMcRKn4cG0qnn7az7cT0N2nTm/U/Gp72TiIiIyHHI3ce6e6XgoTP9g3UPuvuY4LW7+x3ufqa7V3P3t6LRb1YdGjQO6GVmK4DvgNnAz0SGB31gZtmArUAjoB8w1MyWErnb/gjwQXCc5HMEFgN3AAOBBu7+k5kNAf7r7l3MbCSwFNjMUY63cncPhjE9a2Z3A38C64g8FejgWd/JjQDGmdlGd48/mj7TctttfQ+7vlbtJkmvr7n2liPu/1i/wdEM56g99chhf0tDRERE5Nhp/iMA5p7m8HOJsfTMEYi1PzZMj3UI6ZajQLlYhyAiInI8sFgHkFH2TBqRqddWpzTokSXPZVatCIiIiIiIZIw0xu2HRVadIyAiIiIiIhlIFQERERERCRfNEQBUERARERERCSVVBEREREQkXDRHAFBFQEREREQklFQREBEREZFw0RwBQBUBEREREZFQUkVARERERMJFFQFAFQERERERkVBSRUBEREREwkVPDQJUERARERERCSUlAiIiIiIiIaShQSIiIiISLposDCgRkBDat21NrENIlxwFysU6BBERETmBKREQERERkXDRZGFAcwREREREREJJFQERERERCRfNEQBUERARERERCSVVBEREREQkXDRHAFBFQEREREQklFQREBEREZFw0RwBQBUBEREREZFQUkVARERERMJFFQFAFQERERERkVBSRUBEREREwsU91hFkCaoIiIiIiIiEkCoCIiIiIhIumiMAqCIgIiIiIhJKSgREREREREJIQ4NEREREJFw0NAhQRUBEREREJJSUCJygBg9+lOXLZzJ/3gSqV6962DZXtG/J/HkTWLhgEo/3vy9p/VNPPcTcOeOZO2c8y5ZOZ+uWZZkVdpK+jw+m3mVX0aZzr0zv+2gcL3GKiIhIMp6YuUsWlSmJgJmtM7MlZrYwWJ7L4P6KmNlbZrbazOab2Vgzq5TBfdY2s+lm9p2ZLTCzF83s1FTa5zWzmzIilqZNL6VChbKceebF3HjT3Qx5fsAhbfLly8uAAX1p0vRKqp/bgMKFCxIffxEAffo8Qq3aTahVuwlD//cyH330eUaEmao2zRsxfHC/TO/3aB0vcYqIiIgcLDMrAvHuXj1YemdUJ2ZmwIfAVHcv7+41gHuBwhnYZ2HgXeBud6/s7ucC44BcqeyWF8iQRKBly8a8/tp7AMyZ8w158+amSJFCKdqULVuaVavXsm3bdgAmT55J27bNDznWlR1a8/Y7H2dEmKmqWb0aeXKndvqyhuMlThEREUkmMTFzlywqXYmAmX0U3FlfZmY9gnVNzewbM1tkZpOCdTnN7OXg7v9iM2uXyjGzm9lcM6sfvB9gZv2D1w8G25aa2Yjg4h4zm2pmz5jZPDNbYWa1zOwDM1tpZgduy8YD+9x9+IG+3H2Ru8+wiKeC4y4xsyuD49Y3s2lm9rGZrTGzgWbWyczmBO3KB+1GmdnwoP/vzaxF0MXNwCvu/lWyPt9z9y1m9rCZvRTEvsbMDiRBA4HyQYXkqfR8D+lVrFgRflq/Men9+g2bKFasSIo2q1evo1LF8pQuXYK4uDhatWpCyRLFUrQpVao4ZcqUZMqUWdEMT0RERESygPQ+Naibu283s1OAuWb2MTASqOfua80sX9DuAWCnu1cDMLPTkx1jipklBK9fcfdnzKwr8J6Z3Qo0Bc4Ptg9x90eDY4wGWgCfBNv2untNM7sN+BioAWwHVpvZM0BVYP4RPsflQHXgHKBA8FmmB9vOAc4IjrUGeNHdawf93Ar8O2hXBqgNlA8+U4Wgz1dSOX9ViCQouYDvzGwYcA9Q1d2rH26HIOHqARAXl5dscaelcvijt2PHTm7tfS+vvzaMxMREvpo9j/LlSqdo0+GK1nzw4VgSs3AmKyIiInLU3GMdQZaQ3kSgt5m1DV6XJHKBOt3d1wK4+/ZgW0PgqgM7ufuvyY4R7+7bkh/U3ZcFF/qfAhe4+94Dbc3sLuBUIB+wjL8TgTHBv0uAZe6+CcDM1gSxpeZi4E13TwC2mNk0oBawC5ib7FirgS+S9ROf7BjvuHsisDLos0oafQJ85u5/AX+Z2VbSMUzJ3UcAIwD+dVKJNP9ae/XqQvduHQGYN29Rirv7JYoXZePGzYcG9dlEPvtsIgDdu3ciMSHlBX+HDq3ofdv9aXUtIiIiIsehNIcGBUN3GhK5UD8HWAAsjGIM1YAdQKGgv5OB/wHtg8rCSODkZO3/Cv5NTPb6wPvsRJKGGv8gjoOPlbyf5AnTwRflno4+kx87gQz4/Ybhw19JmuA75pNxdOrcHoDatc9j587f2Lx56yH7FCyYH4C8efPQq+e1vPTyG0nbKlcuT968eZg9+0jFFREREZHjlOYIAOmbI5AH+NXdd5tZFaAOkQvzemZWFiDZ0KAJRMbLE6w//eCDJWdmlxO5418PeN7M8vL3Rf82M8sJtD+KzwMwGTjpwFyGoJ+zzawuMAO40szizKxg0O+cozz+FWaWLZg3UA74DhgCdDGzA0ObMLPLg0nER/IbqU8m/sc+/3wya9f+wIoVMxk+7Elu7f33o0Hnzhmf9HrwoEdYtHAy06Z+yFNPDWXlyrVJ2zpc0Zp33x1DrPR5aCCdet7Ouh/X06BNZ97/ZHzaO8XA8RKniIiIyMHSc2d6HNDLzFYQueidDfxMZHjQB2aWDdgKNAL6AUPNbCmRO9+PAB8Ex0k+R2AxcAeRCbMN3P0nMxsC/Nfdu5jZSGApsBmYezQfyN09GMb0rJndDfwJrCMyxn8mcAGwiMid/LvcfXOQ4KTXj0SSh9xAL3f/E/jTzK4CnjazQkSqCNOJnLsjxfmLmc0KztXn7t7naD5nWm67re9h19eq3STp9TXX3nLE/R/rNzia4Ry1px65J6b9p9fxEqeIiIgkk4Xv0mcmc02WSDczGwV86u7vZWa/6ZkjEGt/bJiediM5KjkKlIt1CCIiEm4W6wAyyp7/uzNTr61O6f50ljyXUR+rLiIiIiKSpWXhX/vNTEoEjoK7d411DCIiIiIi0aBEQERERERCxROz/KjrTJGuXxYWEREREZETiyoCIiIiIhIuemoQoIqAiIiIiEgoKREQEREREQkhDQ0SERERkXDR40MBVQRERERERGLKzJqa2XdmtsrM7kmlXTszczOrGY1+VREQERERkXDJQo8PNbM4YCjQCFgPzDWzMe6+/KB2uYDbgK+j1bcqAiIiIiIisVMbWOXua9x9L/AW0Pow7R4DngD+jFbHSgREREREJFwSEzN1MbMeZjYv2dIjWTTFgZ+SvV8frEtiZucBJd39s2ieBg0NEhERERHJQO4+AhjxT/Y1s2zAYKBrNGMCJQIiIiIiEjZZ6wfFNgAlk70vEaw7IBdQFZhqZgBFgDFm1srd5x1Lx0oEjgN/bJge6xDSVKx8s1iHkC7uWWdyUGo2rRnHvm1rYh1GuuQoUC7WIYiIiBzP5gIVzawskQTgKqDjgY3uvhMocOC9mU0F7jzWJACUCIiIiIhI2GShG4Puvt/MbgHGA3HAS+6+zMweBea5+5iM6luJgIiIiIhIDLn7WGDsQesePELb+tHqV4mAiIiIiIRL1pojEDN6fKiIiIiISAipIiAiIiIi4ZKFflk4llQREBEREREJIVUERERERCRcXHMEQBUBEREREZFQUiIgIiIiIhJCGhokIiIiIuGiycKAKgIiIiIiIqGkioCIiIiIhIrrB8UAVQREREREREJJFQERERERCRfNEQBUERARERERCSVVBEREREQkXPSDYoAqAiIiIiIioaRE4AQ0c/Y8Wlx1Pc06dOPF0e8csn3j5i10730Pba+9ka633MXmrT+n2P77H3/QoE1n+g/6X4bG+fgT9zNnwRdMnTWGs88587Bt2ra7jGlfjmHqrDG8/f6L5Mt3OgBnVa3M2AlvMe3LMbz21jBy5jotQ2NNivnJvsxZOIFpXx455jaXN2fal2OY+fVnPPjInZkSV2r6Pj6YepddRZvOvWIdioiISNaQ6Jm7ZFFKBKLEzJqZ2TwzW25mC8xsUBrty5hZx2jHkZCQQL9BQxk26DHGvP4CYydOZfXaH1K0eXrIi7Rq2oAPXx3Gjdd15Nnho1Jsf37kaGpUrxbt0FJo2Kge5cqXofa5jfnPbQ/w5OCHD2kTFxdH/yfup22LLtS/qBXLln1H9x6dAHjm+f70e3gQl1zYirGfTuSW3tdnaLwADRtfEom5eiPuuO0BnnrmkUPanJ4vLw8/dheXt+zCxedfRqHCBal7yQUZHltq2jRvxPDB/WIag4iIiGQ9SgTSycyOOJ/CzKoCQ4DO7n4mUBNYlcYhywBRTwSWrPieUiWKUbJ4UXLkyEGzBpcwecbsFG1Wr/2R2jWqA1D7vHOYMuOrpG3Lvl3JL9t/5cJa50U7tBSaXtaAt9/8CID58xaRJ09uChcumKKNmWFmnHraKQDkypWTzZu3AlC+fBm+nDUXgKlTZtGiVeMMjRegWfMGvPPmh5GY5y4iT55ch8RcpkxJ1qz+gV9++RWAaVO/pGXrjI8tNTWrVyNP7lwxjUFERCRLSUzM3CWLCmUiYGbXmtliM1tkZqPNrKWZfR3cyZ9oZoWDdg8H22cBo82soJm9b2Zzg+Wi4JB3Af3d/VsAd09w92HBMUaZ2XNm9qWZrTGz9sE+A4G6ZrbQzG6P1mfb+vM2ihT6++K0cKECbP35lxRtKlcsx8RpswCYOO1L/ti9hx07d5GYmMhTQ0Zy5y0Zf3e9aNHCbNywOen9xo2bKVKscIo2+/fv5647Hmb6l5+w9LsZVK5cntdffQ+Ab79dSbPLGgDQqk1TihcvmvExFyvMhvXJYt6whaIHxbxmzQ9UqFiWkqWKExcXR/PLGmZKbCIiIiJHK3SJgJmdBfQFLnX3c4DbgJlAHXc/F3iLyIX9AWcCDd39auC/wDPuXgtoB7wYtKkKzE+l26LAxUALIgkAwD3ADHev7u7PHCbOHsFQo3kvvvrmP/y0h3fnzdczb8ES2ne9mXkLl1C4YH6yZcvGWx98Sr0LaqVIJGIpe/bsdO1+NZfWa0PVynVZvuw7/n1HTwBuu/l+rru+IxOnvU/OnKexd9/eGEcbsXPHLvrc/hAvjnqWT8e/wU8/biAhIeveCRAREQklzREAwvn40EuBd919G4C7bzezasDbZlYU+BewNln7Me6+J3jdEDjTzA5sy21mOdPR50funggsP1BtSIu7jwBGAOzbtibdf0GFChZIMfl3y9ZtFCqY/6A2+fnvgAcA2L17DxOnziR3rpwsWrqC+YuX8dYHn7J7z5/s27ePU089mdtv7Jbe7lPV7fqOXNOlAwALFiyhWPEiSduKFSvC5o1bUrSvevYZAKxb+xMAH3/4Ob1v7wHAqpVr6NC2OwDlypehUZP6UYnxkJhv6JQU88JvllC8RLKYixdm00ExA4wfN4Xx46YAcG3XK0lISMiQ2ERERESORegqAkfwPDDE3asBPYGTk237I9nrbEQqB9WDpbi7/w4sA2qkcvy/kr22I7aKgqpVKvHj+o2s37iZffv28fmkacRfXCdFm1937CQxGK82cvTbtL0sMob9iYfvZuIHr/LF+69w583X06ppw6glAQAvvfgG8XXbEF+3DZ9/OpErr24DQI2a57Br129s2ZLy6UWbNm6hcuXy5M8feVLQJfEX8f13qwEoUCAfEJlHcEefG3nlpbeiFmeKmEe+TvzFrYm/uDVjP5tIh6vbRmKudQ67dv1+SMzJY8uTNzfXXd+R1159N0NiExERkX/IEzN3yaLCWBGYDHxoZoPd/RczywfkATYE27uksu8XwK3AUwBmVt3dFwbvPzCzme7+vZllA3q4+/BUjvUbEPUZnNmzx3Hf7TfS846+JCQk0LZFYyqUK82Qka9yVpVKxNetw9wFi3l2+CjMjBrnVKXvf26KdhhpmvDFNBo2voQ5CyewZ/ceet98X9K2KTM+Ir5uG7Zs3spTTwxlzOevs2/fftb/tIFbb7wXgMvbt6DbDZG51p99MoE3Xns/42MeP5WGjS9h7qKJkZhvuvfvmGd+TPzFrYHII0bPqloFgKefGMrqVesyPLbU9HloIHMXLGbHjl00aNOZm7pfQ7uWTWIak4iIiMSeuWfdcUsZxcy6AH2ABGAB8CHwDPArkUShlrvXN7OHgd/d/elgvwLAUOAMIknUdHfvFWxrATwCnAo48Km732Vmo4LX7wXtfnf3nGaWAxgP5AdGHW6ewAFHMzQoVoqVbxbrENLlePl737RmXKxDSLccBcrFOgQREckYGTqKIZb+eKBDpl4QnPbYO1nyXIYyETjeKBGInuPl712JgIiIZAFZ8uI1Gv64/4rMTQT6v5slz6XmCIiIiIiIhFAY5wiIiIiISIh5Fv6Rr8ykioCIiIiISAipIiAiIiIi4ZKFf+QrM6kiICIiIiISQqoIiIiIiEi4qCIAqCIgIiIiIhJKqgiIiIiISLi4nhoEqgiIiIiIiISSKgIiIiIiEi6aIwCoIiAiIiIiEkqqCIiIiIhIqLgqAoAqAiIiIiIioaSKgIiIiIiEiyoCgBKB40KpCi1iHUKaNq7+PNYhnFBylagf6xDS5bf1U9m3bU2sw0iXHAXKxToEERGRLEVDg0REREREQkgVAREREREJlwHXGGEAACAASURBVET9oBioIiAiIiIiEkqqCIiIiIhIuGiyMKCKgIiIiIhIKKkiICIiIiLhoooAoIqAiIiIiEgoqSIgIiIiIqHirooAqCIgIiIiIhJKqgiIiIiISLhojgCgioCIiIiISCipIiAiIiIi4aKKAKCKgIiIiIhITJlZUzP7zsxWmdk9h9l+h5ktN7PFZjbJzEpHo19VBEREREQkVDwLVQTMLA4YCjQC1gNzzWyMuy9P1mwBUNPdd5vZjcCTwJXH2rcqAiIiIiIisVMbWOXua9x9L/AW0Dp5A3ef4u67g7ezgRLR6FgVAREREREJl0yuCJhZD6BHslUj3H1E8Lo48FOybeuB81M5XHfg82jEpUTgBPXYE/fRoFE99uzZw79vuo8li1Yc0qZNu+b0vqMHjrNl01Zu6XE327fvYPhLgyhfsSwAefLkYufO32hU9/Koxjdz9jwGPjuchMRE2rVsyvXXdEixfdPmrdzXbxC//f47CYmJ3N7rOupdWJt9+/bxyJPPs+zblVg2457belH7vLOjGts/jXnj5i088PgzbN+xkzy5czHwwT4UKVQwU2IDGDToEZo2jWf37j3ccMN/WLhw6SFt2rdvyd1330JcXBxjx06ib98BSdvatWtB37634+4sWbKcLl16Z1rsAH0fH8z0WXPId3pePnpteKb2LSIikpGCi/4RaTZMg5l1BmoClxxzUIR4aJCZPWxmd0bxeLXNbHow0WOBmb1oZqem0j6vmd0Urf6Tu7RRPcqVK82F5zWlz20PMXDQQ4e0iYuL47GB99K+ZVcaXNSW5cu+57oenQDo1e0/NKp7OY3qXs5nYyYw9pMJUY0vISGBfoOGMmzQY4x5/QXGTpzK6rU/pGjzwitv0qRBXd4bNZSnH7mHfoOGAvDemHEAfDh6GCOffZynh4wkMTExqvH905ifHvIirZo24MNXh3HjdR15dvioDI/rgCZN4qlQoQxnnVWPm2++h+ee639Im3z58jJgwH00a3Y1553XkCJFChIffxEA5cuXoU+fm4iPv5zzzmvInXc+kmmxH9CmeSOGD+6X6f2KiIjE2AagZLL3JYJ1KZhZQ+B+oJW7/xWNjkObCESLmWU3s8LAu8Dd7l7Z3c8FxgG5Utk1L5AhiUDT5pfy7lsfA/DNvMXkzpOLQoULHBw3Zsapp0VylVy5crJl09ZDjtWyTRM+em9sVONbsuJ7SpUoRsniRcmRIwfNGlzC5BmzD4nvjz8iQ+F++2M3BQvkB2D1uh+pXeMcAPKfnpdcOU9j2bcroxrfP4159dofqV2jOgC1zzuHKTO+yvC4DmjZsjGvv/4+AHPmLCBv3twUKVIoRZuyZUuxatU6tm3bDsDkyTNp06YZAN26deSFF15lx46dAPz88y+ZFvsBNatXI0/u1P7LiIiIREliJi+pmwtUNLOyZvYv4CpgTPIGZnYu8AKRJODQC7Z/KDSJgJldGzxyaZGZjT5oW3kzG2dm881shplVCda3NLOvgzv8E4ML/gPVhNFmNgsYDdwMvOLuSVd+7v6eu28J2r5kZlPNbI2ZHRhvMRAob2YLzeypaH7WIkULsXHD5qT3mzZuoWjRwina7N+/n7vveJTJsz5i4bfTqFSlPG+Mfj9FmzoX1mDbz7+wdk3KO9/HauvP21IMmSlcqABbD7rwvKlbZz4dP4UGbTpz050Pct/tNwJQuUJZps6czf79CazfuJnl361i85afoxrfP425csVyTJw2C4CJ077kj9172LFzV4bHBlCsWBHWr9+U9H7Dhs0UK1YkRZvVq3+gYsVylC5dgri4OFq2bEyJEsUAqFixLBUqlGPKlA+YNu0jGjWKSsVRRERE0uDu+4FbgPHACuAdd19mZo+aWaug2VNATuDd4NpxzBEOd1RCMUfAzM4C+gIXuvs2M8sHJB8APQLo5e4rzex84H/ApcBMoI67u5ldD9wF/CfY50zgYnffY2YfAK+kEkIVIJ5IheA7MxsG3ANUdffqR4g5aVJJ7lOKcOq/Tv9Hn/1IsmfPTpfuV9GoXjt+WPcT/Z+8n9533MCzT7+Q1KZNu8v48P3oVgPSa+zEqbRu3pCuV7dj4dIV3PvYU3w0ejhtL2vCmnU/cWX33hQrUojqVc8gW1zWyGfvvPl6+g/+Hx+PnUCN6tUoXDA/2bJljdgAduzYSe/e9zN69FASExOZPXs+5cpFHkOcPXt2KlQoQ6NGHShRoigTJ75LjRqN2ZlJiYyIiEhmykqPDwVw97HA2IPWPZjsdcOM6DcUiQCRi/p33X0bgLtvNzMAzCwncCGRDOtA+5OCf0sAb5tZUeBfwNpkxxzj7nvS2f9nwViuv8xsK1A4rR2STyopmvfMNP9au15/NZ26XAHAom+WUKz433eDixYrzKZNW1K0P6taFQB+WBeZpP7JR+O45d83JG2Pi4ujecuGNKl/RVpdH7VCBQuweevfd/G3bN1GoYL5U7T54JPxSePFq1c9g7179/Hrzl3kPz0vd9/WM6ldp553UKZk8ajH+E9iLlQwP/8d8AAAu3fvYeLUmeTOlTPDYurZ81q6dbsagPnzF1OiRNGkbcWLF2Hjxs2H7DN27ETGjp0IQPfuHUlIiNQrN2zYxNy5C9i/fz/r1v3EypVrqVChDPPnL86w+EVERCS2ss7tytjJBuxw9+rJljOCbc8DQ9y9GtATODnZfn8ke70MqJFKH8kndCSQAQnYqBffTJrg+/lnk7jiqsjjZ8+reTa/7fqNrVu2pWi/edMWKlUuT/78kUpDvfgLWfn9mqTt9epfwKqVa9m0MWUCEQ1Vq1Tix/UbWb9xM/v27ePzSdOIv7hOijZFixTi63kLgci8gL/+2ku+vHnY8+ef7N7zJwBfzvmG7HFxlC8blR/XO+aYf92xM2ni8sjRb9P2ssYZGtMLL7zK+ec34/zzmzFmzHg6dWoHQO3a57Jz529s3nzoEMKCQfKSN28eevS4hpdffhOAMWPGU6/eBQDkz386FSuWZe3aHzM0fhERkZhJ9MxdsqiwVAQmAx+a2WB3/yUYGgSAu+8ys7VmdoW7v2uRssDZ7r4IyMPfs7a7pHL8IcAcM/vM3b8GMLPLgVmp7PMbqU8m/scmfTGdBo3q8dWCcezZ/Se333x/0rYJMz6gUd3L2bL5ZwY/8T8+HPsq+/bvZ/1PG/n3jfcltWvdrlnUJwkfkD17HPfdfiM97+hLQkICbVs0pkK50gwZ+SpnValEfN069Lnleh564jlefedDDKPf/XdgZmz/dSc9b78fy5aNwgXzM+DBqD346ZhjnrtgMc8OH4WZUeOcqvT9T4bMBT+sceMm07RpPMuXz2D37j306PH3efn66885//zIpOBBgx6mWrUzAXj88WdZtSpS5JowYRoNG9ZjwYJJJCQkcO+9/dm+fUemxQ/Q56GBzF2wmB07dkXmhnS/hnYtm2RqDCIiImFi7lk3S4kmM+sC9CFyR34BsA743d2fNrOywDCgKJADeMvdHzWz1sAzwK9Ekola7l7fzB4+sG+y419A5OeeCxGZHz4duJ3IvIKktma2FGjh7uvM7A3gbOBzd+9zpNjTMzQo1n5c9WmsQzih5CpRP9YhpMtv66fGOoR0y1GgXKxDEBE53ljaTY5PO66Mz9Rrq7xvT8mS5zI0icDxTIlA+CgRiD4lAiIiRy1LXrxGgxKBiLAMDRIRERERAbLeU4NiRZOFRURERERCSBUBEREREQmXtH/tNxRUERARERERCSFVBEREREQkVDRHIEIVARERERGREFJFQERERETCRXMEAFUERERERERCSYmAiIiIiEgIaWiQiIiIiISKa2gQoIqAiIiIiEgoqSIgIiIiIuGiigCgioCIiIiISCipIiAiIiIioaI5AhGqCIiIiIiIhJAqAseBHX/9EesQJJPtT0yIdQgnnH3b1sQ6hDTlKFAu1iGIiISDKgKAKgIiIiIiIqGkioCIiIiIhIrmCESoIiAiIiIiEkKqCIiIiIhIqKgiEKGKgIiIiIhICKkiICIiIiKhoopAhCoCIiIiIiIhpIqAiIiIiISLW6wjyBJUERARERERCSElAiIiIiIiIaShQSIiIiISKposHKGKgIiIiIhICKkiICIiIiKh4omaLAyqCIiIiIiIhJIqAiIiIiISKpojEKGKgIiIiIhICCkROEENGvQwS5dOY86ccVSvXvWwbdq3b8GcOeOYP38C/frdk7S+c+f2/PjjN8yePZbZs8fStetVUY9v5ux5tLjqepp16MaLo985ZPvGzVvo3vse2l57I11vuYvNW39O2tbzjr5c0KQ9N/V5KOpxRSvOb79fTacet9O6U0/aXnsjn0+cluGxPjP4Ub5dPpNv5k/g3CN851dc0Ypv5k9g0cLJDHj8vqT1pUoV54txb/PN/AlMmvAuxYsXzZAYj+V7P7vuZbTrcjPtutzMLXc9nCHxpUffxwdT77KraNO5V8xiEBGRY+NumbpkVaFIBMzsYTO78x/sV9/MLkz2fpSZtT9C20pmNtbMVprZN2b2jpkVTuP496W2/Z9q0iSe8uXLUrXqJdxyy70891y/Q9rky5eXxx+/j+bNO1KjRiMKFy5I/foXJW1///1PqVOnOXXqNGfUqLeiGl9CQgL9Bg1l2KDHGPP6C4ydOJXVa39I0ebpIS/SqmkDPnx1GDde15Fnh49K2nZdx3YMeOCov85MjfPkk0/i8Qfu5OPXX+CFQf144rkX2PXb7xkWa7Oml1KxQlmqnHkxN954N0OHDDikTb58p/PEgL40bnIl51S/lMKFC3Fp/MUAPPnEg4x+/T3Oq9GIfv2fpX+/e6Me47F+7yed9C/ef2Uo778ylCFPPhz1+NKrTfNGDB986P8pERGR400oEoFjUB+4MK1GZnYy8BkwzN0ruvt5wP+AgmnsmiGJQIsWjXjjjfcBmDNnAXny5KZIkUIp2pQtW4pVq9axbdt2ACZPnkmbNs0yIpxDLFnxPaVKFKNk8aLkyJGDZg0uYfKM2SnarF77I7VrVAeg9nnnMGXGV0nb6tQ8l1NPPTVLx1mmVAlKlywOQKGC+cl3el5+3bEzw2Jt2bIJo19/D4Cv53xDnrx5DvnOy5UtxapVa5O+80mTZ9C2bXMAzjijIlOmzAJgytRZtGrZOOoxHuv3nlXUrF6NPLlzxToMERE5Bp6YuUtWdcImAmZ2v5l9b2YzgcrBuvJmNs7M5pvZDDOrEqxvaWZfm9kCM5toZoXNrAzQC7jdzBaaWd3g0PXM7EszW5OsOtAR+MrdPznQv7tPdfelZtbVzD4I+l1pZk8GfQ4ETgmO/Xo0P3uxYkVYv35j0vsNGzZTrFjK4sTq1euoVKkcpUqVIC4ujlatmlCixN/DQVq3bsacOeN4441hKdZHw9aft1Gk0N85UuFCBdj68y8p2lSuWI6J0yIXphOnfckfu/ewY+euqMaRWXEuWf4d+/btp2QGDbcBKF6sCOt/Svadr99E8WJFUrRZtXodlSqVp3TpyHfeulUTSpYsBsDixctpGySCbdo0I3fuXOTLd3pUYzzW87l37146dOtNxxv+zaTpX0Y1NhERkTA6IRMBM6sBXAVUB5oDtYJNI4Bb3b0GcCeRu/YAM4E67n4u8BZwl7uvA4YDz7h7dXefEbQtClwMtAAGBuuqAvNTCak6cCVQDbjSzEq6+z3AnuDYnQ7zGXqY2Twzm7d/f/SHlOzYsYveve/ntdeGMGnSe/zww3oSExMAGDt2IlWqXETt2k2ZNGkGI0cOjnr/abnz5uuZt2AJ7bvezLyFSyhcMD/ZsmW9P9e04vx523buffQp+t13e8zj37FjJ7fcei9vvj6MaVM+5Id160lIiHznd939GPXq1WHunPHUq1uH9es3JW3LTKmdzy/ef4V3XnqOJx6+myf++wI/Jkt2RUREjoYnWqYuWdWJ+vjQusCH7r4bwMzGACcTGebzrlnSF3JS8G8J4G0zKwr8C1ibyrE/cvdEYHlacwCSmeTuO4NYlgOlgZ9S28HdRxBJXDjllNKeVgc9e17LdddFJvXOn7+YEiWKJW0rXrwIGzduOWSfsWMnMXbsJAC6dbs66cJv+/YdSW1efvkt+veP7njxQgULpJgEumXrNgoVzH9Qm/z8d8ADAOzevYeJU2eSO1fOqMaR0XH+/scf3NTnQXr37MI5Vc+Ienw39upC9+6RHHLevIWUKJnsOy9RlA0bNx+yz6efTeDTzyYAcH33TiQEyd+mTVu4osMNAJx22qlc3vYydka5AnOs57NwwQIAlCxelFrnns23K1dTKtnfuYiIiBydrHeLNeNkA3YEd+APLAeuzp4Hhrh7NaAnkaThSP5K9vpARrEMqJHOfRLIgATshRdeTZrc+8knX9CxYzsAatc+l127fmPz5q2H7FMwuAjLmzc3PXpcw8svRyYFJx9b3qJFI777blVUY61apRI/rt/I+o2b2bdvH59Pmkb8xXVStPl1x04SEyOD6kaOfpu2l0V/zHpGxrlv3z5uu/cxWjVtQOP4uoccOxqGDX+FmrUaU7NWY8aMGc81nSIj1c6vfR67du5K4zvPQ69eXfi/l94EIH/+0zmQIN9z962MeiW6E8Th2M7nzl2/sXfv3qQ2C5Ysp3yZUlGPUUREwsE9c5es6kStCEwHRpnZACKfsSXwArDWzK5w93ctctVztrsvAvIAG4J9uyQ7zm9A7nT09wZwr5ld5u6fAZhZPWB7GvvtM7Mc7r4v3Z8sHcaNm0yTJvEsWzad3bv30LPn30/YmT17LHXqRCaIPv30Q1SrdiYAAwb8l1WrIoWQm27qymWXNWL//v38+utObrghuk/oyZ49jvtuv5Ged/QlISGBti0aU6FcaYaMfJWzqlQivm4d5i5YzLPDR2Fm1DinKn3/c1PS/tfeeCdrf/yJ3bv/pEGbzjx67+1cdH5qeVjmxzlu8gzmL1zKjp2/8dHYiQD0v/8OqlQqH/U4AcZ+PommTS/luxWz2L1nD9dff0fStnlzv6BmrcgF9TODH+XssyPfeb/+z7By5RoALrnkQvo/di+OM2PGbG7tfX/UYzyW87nmh5949MnnsWyGJzrdO3egfNnSUY8xPfo8NJC5CxazY8cuGrTpzE3dr6FdyyYxiUVERORYmGflNOUYmNn9RC7qtwI/At8A7wPDiIzzzwG85e6Pmllr4BngV2AyUMvd65tZJeA9IBG4FegOfOru7wV9/O7uOYPXVYBngfLAPmAxcBvQDKjp7rcE7T4Fnnb3qWb2BNAK+OZw8wQOSM/QoFjb9dOUWIdwQjmlWMZUEaJtz8YZaTeSdMtRoFysQxARSS7rDm4/Rj+c1zBTr61KfzMxS57LEzYROJEoEQgfJQLhpERARLKYLHnxGg1KBCLCNEdAREREREQCJ+ocARERERGRw8rKj/TMTKoIiIiIiIiEkCoCIiIiIhIqmiIboYqAiIiIiEgIKREQERERkVDxRMvUJS1m1tTMvjOzVWZ2z2G2n2RmbwfbvzazMtE4D0oERERERERixMzigKFEfnvqTOBqMzvzoGbdgV/dvQKR3756Ihp9KxEQERERkVBxt0xd0lAbWOXua9x9L/AW0PqgNq2BV4LX7wENzOyYH32kREBEREREJAOZWQ8zm5ds6ZFsc3Hgp2Tv1wfrOFwbd98P7ATyH2tcemqQiIiIiISKJ2Zyf+4jgBGZ22vaVBEQEREREYmdDUDJZO9LBOsO28bMsgN5gF+OtWNVBEREREQkVBLTHrefmeYCFc2sLJEL/quAjge1GQN0Ab4C2gOT3Y/91xCUCIiIiIiIxIi77zezW4DxQBzwkrsvM7NHgXnuPgb4P2C0ma0CthNJFo6ZEgERERERCZV0PMknU7n7WGDsQeseTPb6T+CKaPerOQIiIiIiIiGkisBx4ObCF8Y6hDQlrPw61iGcUDoUrR3rENInYV+sI0iX/UunxTqENGU/pyH7tq2JdRjpkqNAuViHICJyTNLza79hoIqAiIiIiEgIKREQEREREQkhDQ0SERERkVA59gdvnhhUERARERERCSFVBEREREQkVDRZOEIVARERERGREFJFQERERERCJTGL/aBYrKgiICIiIiISQqoIiIiIiEiouCoCgCoCIiIiIiKhpIqAiIiIiISKfkcgQhUBEREREZEQUkVAREREREJFTw2KUEVARERERCSEVBEQERERkVDRU4MiVBEQEREREQkhVQROUK0f6sIZ8dXZu2cvb985jA3L1h2x7XUj7yR/qUI83eSupHUXdWnCRdc2IjHBWTF5AZ8NfCOq8c1avJIn3hhHYmIibeudR/cWdQ9pM37OUoZ/NBUwKpcqzMBe7fn2h030f/Uzft/zF3HZjOtb1qPp+VWjGtvxGCfAtQ93p3p8Dfbu+Yvhdz7PuqVrDmnT963HyFvodPb+uReAgdc8wq5fdtL5ges484JqAJx0yknkzp+HG87uHPUYZ349n4HPvUhCYgLtLmvM9Z3bp9j+xPMvMmfBEgD+/PMvtu/YyVdj3wRg8LBRTJ89D4Ce115JswaHfhfRMmvZWp58dwqJ7rS9sCrdmpyfYvvHXy3l2Q+nUzBvTgCuuqQ6l190NgDPfDCNGcvW4olOnTNKc9cV8Zhl/p2nvo8PZvqsOeQ7PS8fvTY80/sXEcnK9NSgiBMuETCzh4Hf3f3po9zvS3e/8DDrRwGfuvt7aex/J3A98CewD3je3V9NpX19YK+7f3k0caZHlfrVKVi2CAPr306pcyvQrn93nmvzwGHbVm1Si792/5liXfkLzuSsRjUY1OweEvbuJ2f+3FGNLyExkcdHj+WFPtdQOF9uOj4ykvrnVqZ88UJJbX7Y/Av/9+lMXrm/O7lPO4Vfdv0OwMkn5aDfDW0pXSQ/W3/dxdUPj+DCquXJfdopUY3xeIoToHr8eRQpW4w7LrmJCudWolu/njzY5u7Dth162zOsXbI6xbrXHns56XXjrs0pc1a5qMeYkJBAv2deYOTgRylSMD9X9vgP8RfXpnyZUklt7r71+qTXr7//KStWRuKc9tVclq9czXv/91/27tvHdbfdR906Nch52qnRjzMxkQFvT2J47/YUzpuLTk+8ziVnV6B80fwp2jWuUZl7r2yQYt3C1RtYuGYj795/LcD/s3ff8VEV+xvHP5NN6IQUSEIvQUB6R6kJXe5FQBQbggVF+NlQuQpYQRELyrWLFcWGip2iNGkqvYqAVJE0UggB0nbn98euISGUcN0U2Od9X/vK7p7Zc57sEu+Z852Z5aapn7Bm5wHaNajp9ZxnM7BfL64bfDnjJ53TfwpFRMSHaGiQx6k6AQVljLkd6AW0t9a2BHoAZ7sEGAX8z8c8kya927Bm9jIA9q//gzIVy1GxSlC+dqXKlabbiH4sfOnLPM93vL4Xi1/7BmdmNgBpialezbdl91/UDA+hRlgIAf7+9O3QlCXrt+dpM/untVzTo13OiXNooPvKa52IytSOcJ+QhQUHEhJYnuQjx7ya73zLCdCmV3uWfbEYgD/W76BcYHmCwoL/p311vLwLK79e5s14AGzetpNa1atSs1oEAQEBXNajC4uW/3ra9nMWLKVfj64A7Nr7J21bNMHf30G5smVoUK8Oy39d5/WMAFv2xlKzShA1KgcR4O+gT5uGLNn4R4Fea4whMyubrGwnmdlOsp0uQit6v7NSEG1bNqNSYMViObaISEnnsqZIbyXVBdERMMZMMMbsMMYsBxp6nos0xswzxqw1xiwzxjTyPB9ujPnSGLPRc+voeT7N89MYY142xmw3xiwAwnIdp40x5ifPPucbY6p6No0HRllrUwGstanW2hme1+w1xjxujFlnjNlsjGlkjKkD3A6MMcZsMMZ4dYxDpfAQUg4m5jw+HJtEpYiQfO363jeEn976nsz0jDzPV64XQd32jbjrq0mM+vQRajb37tXh+ORUIkJOVBnCggOJS87b2dgXm8i+2ESGP/E2Qye+yYpNO/PtZ/PuA2RlO6n5P57wXig5AYIjQknK9ZknxSYSHJ7/MwcY+dydTJ7zPIPuuirftsrVq1ClZhhbV272esb4Q4lEhFXOeRxepTLxCYmnbHswNp6/YuLo0No93KZhZF2W/7qO4+kZJKeksnr9ZmLjE7yeESA+JY2I4BMn0OHBFYk/nJav3cL1O7nqiRnc/+Y3xCa5/120qFeNdg1q0nPcG/R68HUuvbgO9U6qJIiIiJQU5/3QIGNMG+AaoCXu32cdsBaYDtxurd1pjOkAvAp0B14EfrLWDjLGOIAKJ+1yEO7ORGMgHPgNeMcYEwC8BAyw1iYYY64GnjTG3ANUtNbmH5B9wiFrbWtjzGjgfmvtCGPM65xhCJMx5jbgNoBeIW1pXrH+ub41Z1StcW1Ca4XzzaQPCK5ROc82h8NBuUoVeHHgw9RsEckNr9zN5C53e/X4Z5PtcrEvLom3HryRuORUbn7qXT6fNCrnyntCyhEmTP+SJ0YMxM+v+Pqz50vOv71y9wskxyVRpnwZ7nn9AbpcEcWy2Utytl/avzOr5vyMdbmKLyQwd+Eyekd1xOFwANCpfSu2/L6ToaP/Q3BQIC2aNMJRjO9nt2aRXNa2EaUC/Pl82UYefn8eb94zhP3xyeyOTeKHJ28D4PaXPmfdHwdoXb9GsWUVERE5nfO+IwB0Ab601h4DMMZ8A5TBPezms1yT9Ep7fnYHhgFYa53A4ZP21xX42LPtoDFmkef5hkBT4EfPPh1ATAEzzvb8XAtcUZAXWGun4+7McH+da886paXjDb3ocG13AP7cuJugaieuQlaKCOFwbFKe9rVbX0SN5vUYv/xF/Bx+VAitxKhPHua1ayaREpvE5vmrPPvahctlKR9SkaNJRwoS/azCggNzrqCC+8p7eHDeeQjhwYE0i6xBgL+DGlWCqR0eyv64JJrWq07a8XTueOFD7hzcneb1C2/sdUnP2WvYK1WIzQAAIABJREFUZURf0wuA3Zv+ICTXZx4SEUpyXFK+1/z9XPrRdFZ+vZTIlhfl7Qhc3pl3H57u9awAYZVDiY0/lPM4LuEQYVVOfbV87qKlTLjn9jzPjRw2hJHDhgDwn4nPUbtm9cLJGVSB2OQT/9bjko8QVinv9YKgCifmegzq1IxpXy4FYNHGP2hetyrlypQCoFOTumzcfVAdARGREkbLh7oV/yXKwuEHpFhrW+a6XfwP92mArbn218xa29szHCjNGHOm8TN/j71xUkidr5Uf/MgL/cbxQr9xbP1hDW2vcI82qtWqPulHjnEkISVP+59nLmBSh9FM7nwXr1z1GIf2xPDaNZMA2PrDGupf0hiAynUj8A/w91onAKBJ3Wrsj0vkQEIyWdnZzPt1C91aNczTpnvrRqz5fS8AyUeOsi8ukRphwWRlZzPmxU/p37EFvdo18Vqm8zHnj+/PZXy/exnf717W/PArXQZHA1C/VQOOHzlGSnxynvZ+Dj8qeoa8OPwdtOrRlj+378/ZXi2yOuUDK7Bzbd55EN7StNFF7D9wkAMHY8nKymLuwmVEd+qQr93ufQdIPXKUlk0b5TzndDpJOezulG3ftYcdu/bSsV2rQsnZpHYE++NT+OvQYbKyncxfu51uzSPztEnINVTop027qOuZD1I1uCJrdx4g2+kiy+lk7c4D1IvQ0CARESmZLoSKwFLgPWPMU7h/n/7AG8AeY8xV1trPjPsSfnNr7UZgITAKmPb30CBr7eGT9jfSGDMD9/yAaOAjYDtQxRhzqbX2Z89QoQbW2q3AU8ArxpirrbWpxpgKwBVnWjUIOAJ4dzkej22L19MouiUP/jSNrOMZfDr2jZxtY+Y8xQv9xp3x9atmLWbIM7dz//xnyM7K5pP7XvNqPn+Hg3FD+zHquQ9wuSwDu7SifvUwXpm9iCZ1qxHVqhEdm9Vn5dZdDBr/Mn5+fowZ0ougCuX4buVG1u3Yx+G0Y3yzfAMAE0cMpFHtqmc56oWbE2DDorW0jG7DC0tfI+N4Bm/c/1LOtslznmd8v3sJKBXAgx88isPfgZ/Djy3LN7Ho4x9z2l3avzM/f7u8UPIB+Ps7GH/PSEbe/xhOl4tB/XpSv24tXn77Q5o0rE90Z3enYO7CpVzWvUueJTezs50Mu8P977ZC+bJMeehe/P0dhZPT4ceDV3dn1Mtf4HK5GHBpU+pXq8yr366gce1woprX5+PF61myeRf+fn4ElivDxGF9AOjZugGrdvzJVU/MwBjo2Lhuvk5EURn76BRWr99ESkoqPQYOZfQtNzC4f59iySIiUtKU5Am8RcnYC2AhVWPMBGA4EA/sxz1P4AvgNaAqEAB8Yq2daIwJxz3kph7uK/SjPCf2adbaCp5Ow0u4VwHaj3sp0HestZ8bY1rinmNQCXenY5q19k3Pa8YCt3jaZwFTrbUzjTF7gbbW2kPGmLbAc9baKGNMA+BzwAXcaa097TItBRkaVNye+Pjy4o5wQbn5mlnFHaFAZqyaUtwRCiR7y0/FHeGs/Fv0LO4IBRZQ2fvLy4pIiXTBni3/Wu2KIj236nBwdol8Ly+EigDW2ieBJ0+xqe8p2sYBA07xfAXPTwvccZrjbMA9h+Dk5y3wjOd28rY6ue6vwb1sKNbaHUDzUx1HRERERApPib/CWkQu1DkCIiIiIiJyBhdERUBEREREpKA0R8BNFQERERERER+kioCIiIiI+BR9j4CbKgIiIiIiIj5IFQERERER8Smu4g5QQqgiICIiIiLig1QREBERERGfYi/c70o7J6oIiIiIiIj4IFUERERERMSnuPTVwoAqAiIiIiIiPkkdARERERERH6ShQSIiIiLiU1yaLAyoIiAiIiIi4pNUERARERERn6LlQ93UETgPxNqM4o5wVqZi5eKOUCA2u+S/lwDtbPnijlAgWZ+8UNwRLhhZ634p7ggFEnDTQ2Qd2l3cMQokoHK94o4gIlKiqSMgIiIiIj7FVdwBSgjNERARERER8UGqCIiIiIiIT9EcATdVBEREREREfJAqAiIiIiLiUzRHwE0VARERERERH6SKgIiIiIj4FFUE3FQREBERERHxQeoIiIiIiIhPsZgivf0TxpgQY8yPxpidnp/Bp2jT0hjzszFmqzFmkzHm6oLsWx0BEREREZGS60FgobX2ImCh5/HJjgHDrLVNgL7ANGNM0Nl2rDkCIiIiIuJTXOfX1wgMAKI892cAS4AHcjew1u7Idf+gMSYeqAKknGnHqgiIiIiIiBQiY8xtxpg1uW63ncPLw621MZ77sUD4WY7VHigF7DrbjlUREBEREREpRNba6cD00203xiwAIk6xacJJ+7HGGHuG/VQFPgCGW2vPujiSOgIiIiIi4lNc/3ACr7dZa3uebpsxJs4YU9VaG+M50Y8/TbtA4HtggrX2l4IcV0ODRERERERKrm+A4Z77w4GvT25gjCkFfAm8b639vKA7VkdARERERHyKLeLbPzQF6GWM2Qn09DzGGNPWGPOWp80QoCtwozFmg+fW8mw71tCgC9QNj91Cy+jWZBzPYPr9L7N3y+58bSZ8MpGgsGAy0zMBePqGiaQmHgagw786csWYq7HWsn/bXl69a5pX8y1f/xtPv/M5LpeLK3p05JYreudrM3/FOl6bNQcDNKhTnafH3ATACx98xdK1WwEYeVVf+nZq49Vsua3Y8DtPv/cVLpeLQd07cMvAHvlz/ryB1z/7AQw0rF2NKXcNBSDmUDKPvTGLuEMpGGN4+cERVA8LKbSsUY/fQN3olmQdz+CH+6YTv2VvvjaD3v8P5cMq4efv4K9V21n00HtYl+WSMVfQ7NoojiUecf/ez8xi7+KNXs/oV7sxpboNAeNH9tYVZK+Zn2e7f7Mu+DePAuvCZmWQufBDbFIM+Dko1eN6/MJqg7Vk/jQL1187Tn0QH8npV6cppXpcB8aQvWkZ2avm5M3YIgr/Vt3dGTMzyPxhBjbxIACmSg1K9R6GKVUWrCX9g4ngzC6UnGfz0OTnWbpiFSHBQXw18/ViySAiUpJZaxOBfCcg1to1wAjP/ZnAzHPdtzoCXmKMuQyYBJQDMoBF1tr7ztC+DtDRWvuRt7O0iG5NRN2q3Nft/4hs1YAbn7iNxwaeaslZePXuaezZnHdSeXidqvT/vyt4/IrxHEs9SmBoJa/mczpdTH5zFtMfuYPw0CCufeBZoto1I7Jm1Zw2+w7G8/aXP/D+k/cSWKEciYfdJ6hL125h2+4/+Wzqg2RmZXPLI/+lc6vGVChX1qsZAZwuF5Pfmc0bE0YSHlqJ68ZNI6ptEyJrnJjLsy8mgbe/WsiMiXfkyQnw0CsfM2JQDy5t3pBj6RkYU3jjEetEtyCoTgTvdr2PiFaRdH/yRj4Z8Fi+dt+PfonMtOMA/Pv1u7joXx3Y8a17GOG6t+axdvqcfK/xGmMoFXUtGV/+F5uWTJlrxuHcvcl9Au2RvX012ZuXAeCo25xSXa4k4+uX8G/aGYD0DydB2YqUGXAH6Z9MwSvXWc7HnMZQqtdQMmZNxR5JoswNj+DctSHnRB8ge9svZG9c4s4Y2ZJS0VeT8fkLYPwo/a9byfj+LWzCn1CmPLic3s13Dgb268V1gy9n/KTnii2DiPies86i9REaGuQFxpimwMvAUGttY6At8MdZXlYHuK4w8rTp1Z7lXywBYNf6HZQPLE9QWL4voTut6Gt7suD9eRxLPQqQUyXwli1/7KVWRGVqRFQmIMCfvp1bs3j1pjxtvliwkqv7diWwQjkAQitVBGDXn7G0aVwff4eDcmVK06B2dVas3+bVfCdy7qdmeCg1wkMJ8Penb8dWLFm9NU+b2Qt/4ZrenfLnPBBLttPJpc0bAlCuTGnKli5VKDkBInu3YdsXywGIXb+L0oHlKR+W/3tE/u4E+Pk7cJTyp1BOpE/DL7wO9nA8NvUQuJxk71iNo17zkwKmn7gfUConnwmpivPP7e7njx/BZh7HL7y2z+b0q1oPmxyPPZzgzvj7rzjqn1QBzpOxdM5H7VenCa6EA+5OAED6UbBF9+/gZG1bNqNSYMViO76IiC+7oCsCxpihwF2411L9FXgHeBNoDziAVcDVwF7cEy+CgQDgIWvt156r9vOAX4COwGrgXeBxIAy43lq7CvgP8KS19ncAa60TeM2T4T0gFXfnIAL4j2cSxxTgYmPMBmCGtfYFb/3ewREhJB48lPM4KTaR4PAQUuKT87W97bk7cDldrJ73C1+9+BkAEXWrAfDIF5Px8/Nj9rRP2fTTem/FIy7pMOGVT3RMwkOC2bxzb542+w66J8QPG/88TpeLUVf3o3OrxjSsU53XZ81l2OU9SM/IZNWWHdSrearVtv65+KTDRISeOJkOC63E5j/2580ZkwDA8Idfcue8qg+dWjZiX0wCFcuXZcxz7/FXQiKXNGvA3df9C4df4fS9K0QEcyQmMedxWmwSFSKCORqf/3tEBn3wHyJaRrJ38UZ2fr8q5/kWw3tx8eDOxG3aw9InPiTj8DGvZjQVgrFHTvwbtGkp+EXUzdfOv3k3/Fv1BIeDjNnuIWmuQwdw1GuOc/tqTMVg/MJqYSoGQ9xer2Y8X3KaCkHYI0knMh5Jxq9qvfwZW3XHv21v8PMn49NnAPALiQBrKX3lvZhyFcn+/VeyV83zaj4RkZLOVYhV+vPJBVsRMMZcjPskv5O1tiXgBBrinnn9BPAMMNNauwVIBwZZa1sD0cBUc2IcR31gKtDIc7sO6AzcD4z3tGkKrD1DnKqe1/wbzwQP3F8Pvcxa2/JUnYDcXzyxM23P//IWnNWrd09jXJ8xTLpqAg3bXUznK6IAcPg7iKhTjSevfphX7nqeW6aMolxguULJcDpOl5P9MfG8PfFunh5zI4+/9hGpR4/RseXFdG7dmGHjp/LAC+/SomFd/Arp5Logsl0u9sUe4q1HRzPl7qE8Pn0WqUeP43S6WL9tD/fd0J+PJt/DgbhEvl6yuthy5vblDc8wve0dOEr5U7NTEwA2fbCAd7vcy8y+Ezgan0LXh64vtnzZm34ifcbDZK34koB2lwHg3LoSm5ZCmWvHEdB1CK6Y3eAq3sLu+ZAze/0i0t98kKylnxFwaX/3k35++FW/iIzvp5P+0VM4LmqNX62Liy2jiIgUnwu2I4B7UkUbYLXnqnsPoB4wEeiF+wr9M562BphsjNkELACqc+Jb2/ZYazd7vpRhK7DQWmuBzbiH9xTEV9Zal7X2N87ybXB/s9ZOt9a2tda2vahC/quRJ+s5rC9PzpnKk3OmkhKfTGi1yjnbQiJCSY5Lyveav59LP5rOyq+XUa9lfQCSYhJZt2A1zmwnCX/GE7vnIBF1qhUkdoGEh1Qi7tCJK65xScmEnTQPITw0iKh2zQjwd1AjvDK1q4Wx33P1/bYr+/LZ1HFMf/ROrLXUqRrmtWy5hYVUIjbxxBX1+MTDhAeflDMkiKg2Tdw5w0KpXbUK+2MSCA8JomGdatQID8Xf4SC6XVN+33PAq/laDOvJ9XOf5Pq5T3I0PoWKVUNztlWICCEtNn8F6G/OjCx2/biOyF6tATh2KBXrsmAtWz5eTETL/FeX/ymbluy+Ou5hKgRh086QcfsaHJGe4S7WRdbSz0j/6Ekyv3sNSpXFlXLKZZR9IqdNS8FUPDHx3FQMPnPGbatwXNTK/dojybgO7IDjaZCdiXP35kIbZiUiUlKdZ6sGFZoLuSNgcA+5aem5NbTWPgaEAhWAikAZT9vrgSpAG0/1IC7Xtoxc+3TleuzixNCqrbg7HaeTex+FUota8P48JvS7jwn97mPtD6voPDgKgMhWDTh25Fi+YUF+Dj8qBLvH5Tr8HbTq0ZYD293DXtb+sIqLL3FfKa4QXJGIutWI3x/rtaxN6tdmX0wCB+IOkZWVzbzl64hqm3cMdnT7FqzeuhOA5NQ09h2Mp0Z4KE6ni5QjaQDs2PsXO/Yd5NKWjbyWLU/OyJrsjz3EgfhEsrKzmbdyPd3aNsnTpnu7pqz5bdeJnDEJ1AgPpUn9mhw5epykVHfWVVv+oF6NAvUBC2zj+wv48LIJfHjZBHbNX8vFg90TVSNaRZJ55Fi+YUEB5UrnzBswDj/qdm9J0i73BNjc8wki+7Qlcbt3Oy0Arrh9mKAwTGAo+Dnwb9AO5+68c0NM0IlOnaNu0xMn0f4B4O+eY+FX62L3Sji5Ju/6Wk5XzB5McDimUmV3xkYdcP6x4fQZI5vjSnZndO7Zgl+VGu6cxg9HzYa4ck0yFhER33EhzxFYCHxtjHnBWhtvjAnBffL/EvAwUBd4GrgDqATEW2uzjDHRwLleHnsWmG2MWW6t3WGM8QNus9aeaS28I548Xrdh0VpaRLdm6tJXyfQsH/q3J+dMZUK/+wgoFcADHzyCw9+Bn8OPrcs3sfjjBQBs+mk9zbq24OkF/8XldPHx5BmkpaR5LZ+/w8H4EUMYNekVnC7LwO6XUL9WVV75+Dsa169FdLvmdGp5MT9v2MbAu5/Az89w77CBBFWsQEZmFjc+5B6PXb5sGZ66ezj+DofXsp2cc9zNVzBq8nRcLsvAqPbUrxnBK7Pm0aReDaLaNqVji4as3LSdQfc+g5+fYcz1/QmqWB6Ae2/oz22TXsdaS+N6NRjc45JCyQmwZ9EG6kS34KZlU8k+nskP95/4FvPr5z7Jh5dNIKBcaS5/+14cpfwxfoY/V25j08yFAHQZfw1VGtfGWkvqgUMsHPeO90NaF5lLPqX0wLvcy3L+thKbFEPAJf1xxe3DuWcT/s2jcNRqBC4nNv0YmT+8B4ApG0jpQXeCtdi0FDLnv+v9fOdTTusic8FMSl95L/j5kb15OTbxIAGdBuKK3Ytz1wb8W/fAUbuxJ+NRMud4lprOOEbWmvmUueFhsBbnns24TuroFKWxj05h9fpNpKSk0mPgUEbfcgOD+/cptjwi4hu0apCbscW4WkRhM8ZcDYzDXfnIwj0huIW1drAxxgGs9GzfBHyLu1KwBrgEuMyzm++stU09+3vP8/hzz0Ti3Nv+jXsScTncVaDvrLX/yf0aT7s0a20FY0wAMB93heK9M00WHlr7ihL/Ib39/ajijlAgNjvj7I1KgNcu/6S4IxTIyPsqFHeEC0dmZnEnKJCAmx4q7ggFFlDZ+0PcRHzMBTuj9tOq1xfpudXVMR+WyPfyQq4IYK39FPj0NNucQIdcT116mt00zfWaG3Pd33vStu+A705xnBtPelzB8zML6H7m30BEREREvM1VIk/Li96FPEdARERERERO44KuCIiIiIiInMx14Y56OieqCIiIiIiI+CB1BEREREREfJCGBomIiIiITynxyzEWEVUERERERER8kCoCIiIiIuJTtHyomyoCIiIiIiI+SBUBEREREfEpruIOUEKoIiAiIiIi4oNUERARERERn6JVg9xUERARERER8UGqCIiIiIiIT9GqQW6qCIiIiIiI+CBjrUZJlXSlStco8R/S0b+WFneEC0rVen2LO0KBxOyeV9wRLhjOnb8Wd4SCKVuxuBMUiKNG4+KOUGABlesVdwSR07lgr5u/WWNokZ5b3XpgZol8L1UREBERERHxQZojICIiIiI+Rd8j4KaKgIiIiIiID1JFQERERER8ii2RI/aLnioCIiIiIiI+SB0BEREREREfpKFBIiIiIuJTNFnYTRUBEREREREfpIqAiIiIiPgUVQTcVBEQEREREfFBqgiIiIiIiE+xxR2ghFBFQERERETEB6kiICIiIiI+xaUvFANUERARERER8UmqCIiIiIiIT9GqQW6qCIiIiIiI+CBVBERERETEp6gi4KaOwAXq+ecn0rdvd44fO84tI8awYcOWfG2uurI/Dz54Fw6HH3PmLGT8hMkAPPvso0R16whAuXJlqVIllLDwJkWa/6HJz7N0xSpCgoP4aubrRXrsc1FSc05+5iF69u7G8WPHuXPUg2za+Fu+NgOv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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[78]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[78]:</div>



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
      <th>accDefRate</th>
      <th>accExamCnt</th>
      <th>accExamCompCnt</th>
      <th>careCnt</th>
      <th>clearCnt</th>
      <th>deathCnt</th>
      <th>decideCnt</th>
      <th>examCnt</th>
      <th>resutlNegCnt</th>
      <th>month</th>
      <th>day</th>
      <th>criticalRate</th>
      <th>deathRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.305152</td>
      <td>902901.0</td>
      <td>876603.0</td>
      <td>774.0</td>
      <td>10398.0</td>
      <td>269.0</td>
      <td>11441.0</td>
      <td>26298.0</td>
      <td>865162.0</td>
      <td>5</td>
      <td>30</td>
      <td>2.870909</td>
      <td>18.182727</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.324947</td>
      <td>885120.0</td>
      <td>860563.0</td>
      <td>770.0</td>
      <td>10363.0</td>
      <td>269.0</td>
      <td>11402.0</td>
      <td>24557.0</td>
      <td>849161.0</td>
      <td>5</td>
      <td>29</td>
      <td>3.003333</td>
      <td>16.750000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1.340429</td>
      <td>868666.0</td>
      <td>846296.0</td>
      <td>735.0</td>
      <td>10340.0</td>
      <td>269.0</td>
      <td>11344.0</td>
      <td>22370.0</td>
      <td>834952.0</td>
      <td>5</td>
      <td>28</td>
      <td>3.291818</td>
      <td>18.181818</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.354267</td>
      <td>852876.0</td>
      <td>831815.0</td>
      <td>701.0</td>
      <td>10295.0</td>
      <td>269.0</td>
      <td>11265.0</td>
      <td>21061.0</td>
      <td>820550.0</td>
      <td>5</td>
      <td>27</td>
      <td>3.360000</td>
      <td>18.181818</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.373205</td>
      <td>839475.0</td>
      <td>817431.0</td>
      <td>681.0</td>
      <td>10275.0</td>
      <td>269.0</td>
      <td>11225.0</td>
      <td>22044.0</td>
      <td>806206.0</td>
      <td>5</td>
      <td>26</td>
      <td>3.410909</td>
      <td>18.181818</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Modeling">Modeling<a class="anchor-link" href="#Modeling">&#182;</a></h2><h3 id="we-can't-use-criticalRate-and-deathRate.">we can't use criticalRate and deathRate.<a class="anchor-link" href="#we-can't-use-criticalRate-and-deathRate.">&#182;</a></h3><h3 id="Day-columns-has-the-least-correlation-with-deathCnt,-so-Let's-remove-it">Day columns has the least correlation with deathCnt, so Let's remove it<a class="anchor-link" href="#Day-columns-has-the-least-correlation-with-deathCnt,-so-Let's-remove-it">&#182;</a></h3><h3 id="whole-data-size-is-too-small,-53-instances-are-entire-data-set.">whole data size is too small, 53 instances are entire data set.<a class="anchor-link" href="#whole-data-size-is-too-small,-53-instances-are-entire-data-set.">&#182;</a></h3><h3 id="In-addition,-there-is-no-test-data.-even-if-we-make-a-test-set,-it's-going-to-be-too-small.">In addition, there is no test data. even if we make a test set, it's going to be too small.<a class="anchor-link" href="#In-addition,-there-is-no-test-data.-even-if-we-make-a-test-set,-it's-going-to-be-too-small.">&#182;</a></h3><h3 id="so-I-just-take-Cross-validation.">so I just take Cross validation.<a class="anchor-link" href="#so-I-just-take-Cross-validation.">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[116]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>

<span class="n">scoresum</span><span class="o">=</span><span class="mi">0</span>

<span class="c1">#x_train,x_test,y_train,y_test = train_test_split(train.drop([&#39;day&#39;,&#39;deathCnt&#39;,&#39;criticalRate&#39;,&#39;deathRate&#39;],axis=1),train[&#39;deathCnt&#39;],test_size=0.05)</span>
<span class="c1">#lgb_train=lgb.Dataset(x_train,label=y_train)</span>
<span class="c1">#lgb_test=lgb.Dataset(x_test,label=y_test)</span>
<span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;day&#39;</span><span class="p">,</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">,</span><span class="s1">&#39;criticalRate&#39;</span><span class="p">,</span><span class="s1">&#39;deathRate&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">label</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;deathCnt&#39;</span><span class="p">])</span>
<span class="n">params</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.05</span><span class="p">,</span> 
          <span class="s1">&#39;boosting&#39;</span><span class="p">:</span> <span class="s1">&#39;gbdt&#39;</span><span class="p">,</span> 
          <span class="s1">&#39;objective&#39;</span><span class="p">:</span> <span class="s1">&#39;regression&#39;</span><span class="p">,</span> 
          <span class="s1">&#39;metric&#39;</span><span class="p">:</span> <span class="s1">&#39;mae&#39;</span><span class="p">,</span> 
          <span class="s1">&#39;n_fold&#39;</span> <span class="p">:</span><span class="mi">10</span><span class="p">,</span>
          <span class="c1">#&#39;sub_fraction&#39;:0.2,</span>
          <span class="s1">&#39;min_hessian&#39;</span> <span class="p">:</span> <span class="mf">0.05</span><span class="p">,</span>
          <span class="s1">&#39;stratified&#39;</span><span class="p">:</span> <span class="kc">False</span>
          <span class="p">}</span>
<span class="c1">#cv_result=lgb.cv(params,lgb_train,2000,valid_sets=lgb_test,early_stopping_rounds=200,verbose_eval=True)</span>
<span class="n">cv_result</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">cv</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span><span class="mi">2000</span><span class="p">,</span><span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">200</span><span class="p">,</span><span class="n">verbose_eval</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Cross validation score : </span><span class="si">{0}</span><span class="s2">&quot;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">cv_result</span><span class="p">[</span><span class="s1">&#39;l1-mean&#39;</span><span class="p">][</span><span class="o">-</span><span class="mi">1</span><span class="p">]))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/home/lillflower/.local/lib/python3.8/site-packages/sklearn/model_selection/_split.py:670: UserWarning: The least populated class in y has only 1 members, which is less than n_splits=5.
  warnings.warn((&#34;The least populated class in y has only %d&#34;
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[20]	cv_agg&#39;s l1: 7.62424 + 0.954064
[40]	cv_agg&#39;s l1: 6.97263 + 0.850115
[60]	cv_agg&#39;s l1: 6.86805 + 0.846551
[80]	cv_agg&#39;s l1: 6.86141 + 0.854764
[100]	cv_agg&#39;s l1: 6.87121 + 0.877261
[120]	cv_agg&#39;s l1: 6.89945 + 0.868047
[140]	cv_agg&#39;s l1: 6.89964 + 0.857855
[160]	cv_agg&#39;s l1: 6.90844 + 0.846537
[180]	cv_agg&#39;s l1: 6.91967 + 0.841997
[200]	cv_agg&#39;s l1: 6.92978 + 0.850135
[220]	cv_agg&#39;s l1: 6.9348 + 0.867669
[240]	cv_agg&#39;s l1: 6.93947 + 0.885714
[260]	cv_agg&#39;s l1: 6.94389 + 0.903887
Cross validation score : 6.8539133509677
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="score-is-not-that-good.">score is not that good.<a class="anchor-link" href="#score-is-not-that-good.">&#182;</a></h3><h3 id="we-will-miss-predict-almost-7-people-as-dead-whom-are-alive,-or-as-alive-whom-are-dead.">we will miss predict almost 7 people as dead whom are alive, or as alive whom are dead.<a class="anchor-link" href="#we-will-miss-predict-almost-7-people-as-dead-whom-are-alive,-or-as-alive-whom-are-dead.">&#182;</a></h3>
</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>
