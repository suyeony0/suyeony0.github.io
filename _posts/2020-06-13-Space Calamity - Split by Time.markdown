---
layout: post
title: Space Calamity - Data Split by Time
date: 2020-06-13
description: Space Calamity - Split by Time
thumbnail: food2.jpg
categories: DataMining

# Information for the author block
author : Loui
---


<html>
<head><meta charset="utf-8" />

<title>Space Calamity - Split by Time</title>

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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/frame_train/ace_1999.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">label</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="B&#47448;-&#54217;&#49548;-:-&#44368;&#46976;-=&gt;--5-~-5-:--30~+30">B&#47448; &#54217;&#49548; : &#44368;&#46976; =&gt; -5 ~ 5 : -30~+30<a class="anchor-link" href="#B&#47448;-&#54217;&#49548;-:-&#44368;&#46976;-=&gt;--5-~-5-:--30~+30">&#182;</a></h1><hr>
<h1 id="Vp-:-300~400-:-500&#51060;&#49345;">Vp : 300~400 : 500&#51060;&#49345;<a class="anchor-link" href="#Vp-:-300~400-:-500&#51060;&#49345;">&#182;</a></h1><hr>
<h1 id="Np-:-10&#45824;-:-&#49688;&#49901;&#45824;">Np : 10&#45824; : &#49688;&#49901;&#45824;<a class="anchor-link" href="#Np-:-10&#45824;-:-&#49688;&#49901;&#45824;">&#182;</a></h1><hr>
<h1 id="Tp-:-10^4~5-&#51228;&#44273;-:-10^6&#51228;&#44273;-&#51060;&#49345;-(&#52860;&#48712;&#50728;&#46020;)">Tp : 10^4~5 &#51228;&#44273; : 10^6&#51228;&#44273; &#51060;&#49345; (&#52860;&#48712;&#50728;&#46020;)<a class="anchor-link" href="#Tp-:-10^4~5-&#51228;&#44273;-:-10^6&#51228;&#44273;-&#51060;&#49345;-(&#52860;&#48712;&#50728;&#46020;)">&#182;</a></h1><hr>
<h1 id="&#46972;&#48296;-:-3&#51060;&#54616;-:-5&#51060;&#49345;">&#46972;&#48296; : 3&#51060;&#54616; : 5&#51060;&#49345;<a class="anchor-link" href="#&#46972;&#48296;-:-3&#51060;&#54616;-:-5&#51060;&#49345;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">label_13</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_13.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">label_13</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>



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
      <th>Unnamed: 0</th>
      <th>date</th>
      <th>kp_0h</th>
      <th>kp_3h</th>
      <th>kp_6h</th>
      <th>kp_9h</th>
      <th>kp_12h</th>
      <th>kp_15h</th>
      <th>kp_18h</th>
      <th>kp_21h</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5114</td>
      <td>2013-01-01</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5115</td>
      <td>2013-01-02</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5116</td>
      <td>2013-01-03</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5117</td>
      <td>2013-01-04</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5118</td>
      <td>2013-01-05</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="&#51204;&#52376;&#47532;">&#51204;&#52376;&#47532;<a class="anchor-link" href="#&#51204;&#52376;&#47532;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/frame_train/ace_2013.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">label_13</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_13.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">temp</span><span class="o">.</span><span class="n">head</span><span class="p">())</span>
<span class="c1">#각 데이터 프레임 시간대별로 나누기</span>
<span class="c1">#1999는 신경쓰지 말것 처음에 테스트할때 1999년도로 해서 그럼, 저기에 각기다른년도 넣어주면 됨 그냥</span>
<span class="c1">#0시 라벨은 0~3시까지 예측한 거래</span>
<span class="n">ace_1999</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">3</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">5</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">6</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">9</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">11</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">12</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">14</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">15</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">17</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">18</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">20</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">21</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">23</span><span class="p">)]</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">0</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">2</span><span class="p">)]</span>


<span class="c1">#라벨도 시간대 별로 나누기</span>
<span class="c1">#여기 라벨 년도도 바꾸어 주어야함</span>
<span class="n">label_1999</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_0h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_3h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_6h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_9h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_12h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_15h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_18h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>
<span class="n">label_1999</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">label_13</span><span class="p">[[</span><span class="s1">&#39;kp_21h&#39;</span><span class="p">,</span><span class="s1">&#39;date&#39;</span><span class="p">]])</span>



  

<span class="c1">#데이터프레임에 라벨 붙이기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">doy</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">ace_1999</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">())</span>
  <span class="n">label_1999</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">label_1999</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">label_1999</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">doy</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
  <span class="n">ace_1999</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_1999</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">label_1999</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="s1">&#39;doy&#39;</span><span class="p">)</span>
  <span class="n">ace_1999</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;date&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">ace_1999</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">())</span>


<span class="n">ace_0h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_0h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
<span class="n">ace_3h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_3h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
<span class="n">ace_6h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_6h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
<span class="n">ace_9h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_9h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">3</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>

<span class="n">ace_12h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_12h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">4</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
<span class="n">ace_15h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_15h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">5</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
<span class="n">ace_18h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_18h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">6</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
<span class="n">ace_21h</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">ace_21h</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">7</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>     year  doy   hr  min        Np  ...       Vp  B_gsm_x  B_gsm_y  B_gsm_z     Bt
0  2013.0  1.0  0.0  0.0     2.524  ...   351.38    2.402   -1.487   -0.554  2.888
1  2013.0  1.0  0.0  1.0     2.678  ...   349.83    2.483   -1.369   -0.488  2.880
2  2013.0  1.0  0.0  2.0     2.312  ...   350.21    2.680   -1.205   -0.501  2.995
3  2013.0  1.0  0.0  3.0 -9999.900  ... -9999.90    2.769   -0.960   -0.368  2.967
4  2013.0  1.0  0.0  4.0     2.037  ...   349.51    2.545   -1.297   -0.527  2.908

[5 rows x 11 columns]
     year  doy    hr  min      Np  ...  B_gsm_x  B_gsm_y  B_gsm_z     Bt  kp_21h
0  2013.0  1.0  21.0  0.0 -9999.9  ...    2.027   -2.084    0.388  2.934       0
1  2013.0  1.0  21.0  1.0 -9999.9  ...    2.076   -2.080    0.196  2.948       0
2  2013.0  1.0  21.0  2.0 -9999.9  ...    2.072   -2.106    0.092  2.962       0
3  2013.0  1.0  21.0  3.0 -9999.9  ...    2.141   -2.035    0.160  2.960       0
4  2013.0  1.0  21.0  4.0 -9999.9  ...    2.199   -2.011    0.163  2.986       0

[5 rows x 12 columns]
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="sd">&#39;&#39;&#39;</span>
<span class="sd">#기본 프레임을 1999년도껄로 생성</span>
<span class="sd">ace_0h=ace_1999[0].copy()</span>
<span class="sd">ace_3h=ace_1999[1].copy()</span>
<span class="sd">ace_6h=ace_1999[2].copy()</span>
<span class="sd">ace_9h=ace_1999[3].copy()</span>
<span class="sd">ace_12h=ace_1999[4].copy()</span>
<span class="sd">ace_15h=ace_1999[5].copy()</span>
<span class="sd">ace_18h=ace_1999[6].copy()</span>
<span class="sd">ace_21h=ace_1999[7].copy()</span>
<span class="sd">&#39;&#39;&#39;</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ace_0h</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([1999., 2000., 2001., 2002., 2003., 2004., 2005., 2006., 2007.,
       2008., 2009., 2010.])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ace_0h</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([1999., 2000., 2001., 2002., 2003., 2004., 2005., 2006., 2007.,
       2008., 2009., 2010., 2011., 2012., 2013.])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#왜 저장이안되 시바</span>
<span class="n">ace_0h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_0h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
<span class="n">ace_3h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_3h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
<span class="n">ace_6h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_6h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
<span class="n">ace_9h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_9h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
<span class="n">ace_12h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_12h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
<span class="n">ace_15h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_15h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
<span class="n">ace_18h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_18h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
<span class="n">ace_21h</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_21h.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;done&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>done
done
done
done
done
done
done
done
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">|</span>
<span class="c1">#컬럼이름 바꾸고 merge하기</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_0h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_3h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_6h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_9h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_12h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_15h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_18h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">ace_1999</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_21h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">merged</span><span class="o">=</span><span class="n">ace_1999</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">merged</span><span class="p">,</span><span class="n">ace_1999</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>

  
<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">#doy 뽑기</span>
<span class="sd">for i in range(8):</span>
<span class="sd">  label_1999[i].reset_index(inplace=True)</span>
<span class="sd">  label_1999[i][&#39;index&#39;]+=1</span>
<span class="sd">  label_1999[i].rename(columns={&#39;index&#39;:&#39;doy&#39;},inplace=True)</span>

<span class="sd">&#39;&#39;&#39;</span>
  
<span class="nb">print</span><span class="p">(</span><span class="n">temp</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">merged</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>

<span class="n">merged</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_time/ace_2013.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="&#46972;&#48296;-&#51221;&#47532;">&#46972;&#48296; &#51221;&#47532;<a class="anchor-link" href="#&#46972;&#48296;-&#51221;&#47532;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#라벨 만든거 저장 / 년도별로 라벨 나눈거임</span>
<span class="n">label_99</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_99.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_00</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_00.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_01</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_01.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_02</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_02.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_03</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_03.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_04</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_04.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_05</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_05.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_06</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_06.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_07</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_07.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_08</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_08.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_09</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_09.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_10</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_10.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_11</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_11.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_12</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_12.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">label_13</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_13.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="n">aa</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/label/label_03.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">aa</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>



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
      <th>Unnamed: 0</th>
      <th>date</th>
      <th>kp_0h</th>
      <th>kp_3h</th>
      <th>kp_6h</th>
      <th>kp_9h</th>
      <th>kp_12h</th>
      <th>kp_15h</th>
      <th>kp_18h</th>
      <th>kp_21h</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1461</td>
      <td>2003-01-01</td>
      <td>2</td>
      <td>2</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1462</td>
      <td>2003-01-02</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1463</td>
      <td>2003-01-03</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1464</td>
      <td>2003-01-04</td>
      <td>4</td>
      <td>4</td>
      <td>2</td>
      <td>2</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1465</td>
      <td>2003-01-05</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="&#51060;&#44163;-&#51200;&#44163;-&#54620;&#48264;-&#48372;&#44592;">&#51060;&#44163; &#51200;&#44163; &#54620;&#48264; &#48372;&#44592;<a class="anchor-link" href="#&#51060;&#44163;-&#51200;&#44163;-&#54620;&#48264;-&#48372;&#44592;">&#182;</a></h1>
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
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[49]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">time_label</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[49]:</div>



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
      <th>kp_0h</th>
      <th>date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1999-01-01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1999-01-02</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>1999-01-03</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1999-01-04</td>
    </tr>
    <tr>
      <th>4</th>
      <td>3</td>
      <td>1999-01-05</td>
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
<div class="prompt input_prompt">In&nbsp;[50]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;date&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">to_datetime</span><span class="p">(</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;date&#39;</span><span class="p">],</span><span class="nb">format</span><span class="o">=</span><span class="s2">&quot;%Y-%m-</span><span class="si">%d</span><span class="s2">&quot;</span><span class="p">,</span><span class="n">errors</span><span class="o">=</span><span class="s1">&#39;ignore&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:2: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[51]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">datetime</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;date&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">dayofyear</span>
  
<span class="c1">#label 이름 변경</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">time_label</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:3: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  This is separate from the ipykernel package so we can avoid doing imports until
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:4025: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  return super(DataFrame, self).rename(**kwargs)
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">doy</span><span class="o">=</span><span class="p">[[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">15</span><span class="p">)]</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class="prompt input_prompt">In&nbsp;[53]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">doy</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[53]:</div>



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
      <th>label</th>
      <th>date</th>
      <th>doy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1096</th>
      <td>2</td>
      <td>2002-01-01</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1097</th>
      <td>1</td>
      <td>2002-01-02</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1098</th>
      <td>1</td>
      <td>2002-01-03</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1099</th>
      <td>1</td>
      <td>2002-01-04</td>
      <td>4</td>
    </tr>
    <tr>
      <th>1100</th>
      <td>2</td>
      <td>2002-01-05</td>
      <td>5</td>
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
<span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">before</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">season</span><span class="o">=</span><span class="p">[[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">)]</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">season</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">60</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">335</span><span class="p">)]</span>
  <span class="n">season</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">60</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">150</span><span class="p">)]</span>
  <span class="n">season</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">150</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">240</span><span class="p">)]</span>
  <span class="n">season</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">240</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">335</span><span class="p">)]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">):</span>
    <span class="n">season</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[240]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">season</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[240]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(1354, 10)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[294]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>

<span class="c1">#split data for test and train, valid</span>
<span class="n">models</span><span class="o">=</span><span class="p">[[</span><span class="n">j</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">)]</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">):</span>

    <span class="n">df3</span><span class="o">=</span><span class="n">season</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="n">frac</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>


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
        <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;Bx&#39;</span><span class="p">,</span><span class="s1">&#39;By&#39;</span><span class="p">,</span><span class="s1">&#39;Bz&#39;</span><span class="p">,</span><span class="s1">&#39;Btt&#39;</span><span class="p">,</span><span class="s1">&#39;Npp&#39;</span><span class="p">,</span><span class="s1">&#39;Tpp&#39;</span><span class="p">,</span><span class="s1">&#39;Vpp&#39;</span><span class="p">]</span>
    <span class="p">}</span>

    <span class="c1">#model train</span>
    <span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span><span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_eval</span><span class="p">,</span><span class="n">verbose_eval</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
    <span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
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
[100]	valid_0&#39;s l2: 1.26581
[200]	valid_0&#39;s l2: 1.02959
[300]	valid_0&#39;s l2: 0.935998
[400]	valid_0&#39;s l2: 0.89153
[500]	valid_0&#39;s l2: 0.869369
[600]	valid_0&#39;s l2: 0.860238
[700]	valid_0&#39;s l2: 0.850328
[800]	valid_0&#39;s l2: 0.841698
[900]	valid_0&#39;s l2: 0.836882
[1000]	valid_0&#39;s l2: 0.833742
[1100]	valid_0&#39;s l2: 0.831206
[1200]	valid_0&#39;s l2: 0.82733
Early stopping, best iteration is:
[1191]	valid_0&#39;s l2: 0.82704
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.26256
[200]	valid_0&#39;s l2: 0.971345
[300]	valid_0&#39;s l2: 0.85536
[400]	valid_0&#39;s l2: 0.823392
[500]	valid_0&#39;s l2: 0.811237
[600]	valid_0&#39;s l2: 0.815814
Early stopping, best iteration is:
[518]	valid_0&#39;s l2: 0.810875
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.931772
[200]	valid_0&#39;s l2: 0.66342
[300]	valid_0&#39;s l2: 0.554626
[400]	valid_0&#39;s l2: 0.517495
[500]	valid_0&#39;s l2: 0.503283
[600]	valid_0&#39;s l2: 0.499417
[700]	valid_0&#39;s l2: 0.501142
Early stopping, best iteration is:
[620]	valid_0&#39;s l2: 0.498173
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.5361
[200]	valid_0&#39;s l2: 1.07582
[300]	valid_0&#39;s l2: 0.873624
[400]	valid_0&#39;s l2: 0.790237
[500]	valid_0&#39;s l2: 0.745045
[600]	valid_0&#39;s l2: 0.72316
[700]	valid_0&#39;s l2: 0.715119
[800]	valid_0&#39;s l2: 0.715604
Early stopping, best iteration is:
[755]	valid_0&#39;s l2: 0.713039
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.37379
[200]	valid_0&#39;s l2: 0.993495
[300]	valid_0&#39;s l2: 0.816054
[400]	valid_0&#39;s l2: 0.733458
[500]	valid_0&#39;s l2: 0.700442
[600]	valid_0&#39;s l2: 0.68553
[700]	valid_0&#39;s l2: 0.682191
[800]	valid_0&#39;s l2: 0.682755
Early stopping, best iteration is:
[728]	valid_0&#39;s l2: 0.680558
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.84345
[200]	valid_0&#39;s l2: 1.37433
[300]	valid_0&#39;s l2: 1.15627
[400]	valid_0&#39;s l2: 1.05584
[500]	valid_0&#39;s l2: 0.99897
[600]	valid_0&#39;s l2: 0.968226
[700]	valid_0&#39;s l2: 0.952379
[800]	valid_0&#39;s l2: 0.942434
[900]	valid_0&#39;s l2: 0.933899
[1000]	valid_0&#39;s l2: 0.929547
Early stopping, best iteration is:
[968]	valid_0&#39;s l2: 0.927306
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.00647
[200]	valid_0&#39;s l2: 0.774507
[300]	valid_0&#39;s l2: 0.666159
[400]	valid_0&#39;s l2: 0.613818
[500]	valid_0&#39;s l2: 0.584945
[600]	valid_0&#39;s l2: 0.566716
[700]	valid_0&#39;s l2: 0.554967
[800]	valid_0&#39;s l2: 0.545495
[900]	valid_0&#39;s l2: 0.536386
[1000]	valid_0&#39;s l2: 0.533725
[1100]	valid_0&#39;s l2: 0.529912
Early stopping, best iteration is:
[1085]	valid_0&#39;s l2: 0.529105
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.88655
[200]	valid_0&#39;s l2: 1.40042
[300]	valid_0&#39;s l2: 1.16154
[400]	valid_0&#39;s l2: 1.06403
[500]	valid_0&#39;s l2: 1.0101
[600]	valid_0&#39;s l2: 0.98119
[700]	valid_0&#39;s l2: 0.970022
[800]	valid_0&#39;s l2: 0.953653
[900]	valid_0&#39;s l2: 0.945426
[1000]	valid_0&#39;s l2: 0.936787
[1100]	valid_0&#39;s l2: 0.929758
[1200]	valid_0&#39;s l2: 0.92581
[1300]	valid_0&#39;s l2: 0.922492
[1400]	valid_0&#39;s l2: 0.918982
[1500]	valid_0&#39;s l2: 0.916466
Early stopping, best iteration is:
[1479]	valid_0&#39;s l2: 0.914075
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.18429
[200]	valid_0&#39;s l2: 0.972833
[300]	valid_0&#39;s l2: 0.878553
[400]	valid_0&#39;s l2: 0.831022
[500]	valid_0&#39;s l2: 0.803584
[600]	valid_0&#39;s l2: 0.782209
[700]	valid_0&#39;s l2: 0.764427
[800]	valid_0&#39;s l2: 0.755924
[900]	valid_0&#39;s l2: 0.749924
[1000]	valid_0&#39;s l2: 0.744099
[1100]	valid_0&#39;s l2: 0.742706
[1200]	valid_0&#39;s l2: 0.74187
Early stopping, best iteration is:
[1159]	valid_0&#39;s l2: 0.741257
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.78052
[200]	valid_0&#39;s l2: 1.37292
[300]	valid_0&#39;s l2: 1.18884
[400]	valid_0&#39;s l2: 1.10458
[500]	valid_0&#39;s l2: 1.05979
[600]	valid_0&#39;s l2: 1.04247
[700]	valid_0&#39;s l2: 1.03135
[800]	valid_0&#39;s l2: 1.02356
[900]	valid_0&#39;s l2: 1.01655
[1000]	valid_0&#39;s l2: 1.01747
Early stopping, best iteration is:
[928]	valid_0&#39;s l2: 1.014
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.15485
[200]	valid_0&#39;s l2: 0.86457
[300]	valid_0&#39;s l2: 0.739693
[400]	valid_0&#39;s l2: 0.687497
[500]	valid_0&#39;s l2: 0.661592
[600]	valid_0&#39;s l2: 0.652036
[700]	valid_0&#39;s l2: 0.648718
[800]	valid_0&#39;s l2: 0.641034
[900]	valid_0&#39;s l2: 0.639557
Early stopping, best iteration is:
[853]	valid_0&#39;s l2: 0.63855
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.5297
[200]	valid_0&#39;s l2: 1.21156
[300]	valid_0&#39;s l2: 1.07044
[400]	valid_0&#39;s l2: 1.00951
[500]	valid_0&#39;s l2: 0.979937
[600]	valid_0&#39;s l2: 0.960587
[700]	valid_0&#39;s l2: 0.952356
[800]	valid_0&#39;s l2: 0.94559
[900]	valid_0&#39;s l2: 0.938654
[1000]	valid_0&#39;s l2: 0.939569
Early stopping, best iteration is:
[905]	valid_0&#39;s l2: 0.93835
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.07034
[200]	valid_0&#39;s l2: 0.809389
[300]	valid_0&#39;s l2: 0.708015
[400]	valid_0&#39;s l2: 0.662801
[500]	valid_0&#39;s l2: 0.648073
[600]	valid_0&#39;s l2: 0.639335
[700]	valid_0&#39;s l2: 0.634193
[800]	valid_0&#39;s l2: 0.636508
Early stopping, best iteration is:
[738]	valid_0&#39;s l2: 0.633548
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.237
[200]	valid_0&#39;s l2: 0.884696
[300]	valid_0&#39;s l2: 0.740154
[400]	valid_0&#39;s l2: 0.688223
[500]	valid_0&#39;s l2: 0.678382
Early stopping, best iteration is:
[498]	valid_0&#39;s l2: 0.677869
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.02062
[200]	valid_0&#39;s l2: 0.770491
[300]	valid_0&#39;s l2: 0.675549
[400]	valid_0&#39;s l2: 0.64056
[500]	valid_0&#39;s l2: 0.62965
[600]	valid_0&#39;s l2: 0.623664
[700]	valid_0&#39;s l2: 0.621743
[800]	valid_0&#39;s l2: 0.616933
[900]	valid_0&#39;s l2: 0.61944
Early stopping, best iteration is:
[804]	valid_0&#39;s l2: 0.616477
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.566
[200]	valid_0&#39;s l2: 1.03355
[300]	valid_0&#39;s l2: 0.781818
[400]	valid_0&#39;s l2: 0.665425
[500]	valid_0&#39;s l2: 0.601962
[600]	valid_0&#39;s l2: 0.569376
[700]	valid_0&#39;s l2: 0.551698
[800]	valid_0&#39;s l2: 0.54012
[900]	valid_0&#39;s l2: 0.532877
[1000]	valid_0&#39;s l2: 0.527475
[1100]	valid_0&#39;s l2: 0.527422
[1200]	valid_0&#39;s l2: 0.524923
Early stopping, best iteration is:
[1173]	valid_0&#39;s l2: 0.524014
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.02751
[200]	valid_0&#39;s l2: 0.77247
[300]	valid_0&#39;s l2: 0.671179
[400]	valid_0&#39;s l2: 0.635421
[500]	valid_0&#39;s l2: 0.618042
[600]	valid_0&#39;s l2: 0.608428
[700]	valid_0&#39;s l2: 0.601517
[800]	valid_0&#39;s l2: 0.594345
[900]	valid_0&#39;s l2: 0.592346
[1000]	valid_0&#39;s l2: 0.59122
[1100]	valid_0&#39;s l2: 0.588622
[1200]	valid_0&#39;s l2: 0.58738
[1300]	valid_0&#39;s l2: 0.582548
[1400]	valid_0&#39;s l2: 0.581834
[1500]	valid_0&#39;s l2: 0.582005
[1600]	valid_0&#39;s l2: 0.583422
Early stopping, best iteration is:
[1523]	valid_0&#39;s l2: 0.581245
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.00837
[200]	valid_0&#39;s l2: 0.836157
[300]	valid_0&#39;s l2: 0.76584
[400]	valid_0&#39;s l2: 0.727188
[500]	valid_0&#39;s l2: 0.713559
[600]	valid_0&#39;s l2: 0.701314
[700]	valid_0&#39;s l2: 0.699164
[800]	valid_0&#39;s l2: 0.696403
Early stopping, best iteration is:
[772]	valid_0&#39;s l2: 0.694972
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.815416
[200]	valid_0&#39;s l2: 0.589551
[300]	valid_0&#39;s l2: 0.497273
[400]	valid_0&#39;s l2: 0.456931
[500]	valid_0&#39;s l2: 0.442896
[600]	valid_0&#39;s l2: 0.438426
[700]	valid_0&#39;s l2: 0.434958
[800]	valid_0&#39;s l2: 0.433185
[900]	valid_0&#39;s l2: 0.429474
Early stopping, best iteration is:
[899]	valid_0&#39;s l2: 0.42936
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.4305
[200]	valid_0&#39;s l2: 0.963384
[300]	valid_0&#39;s l2: 0.74684
[400]	valid_0&#39;s l2: 0.647554
[500]	valid_0&#39;s l2: 0.597621
[600]	valid_0&#39;s l2: 0.576556
[700]	valid_0&#39;s l2: 0.57006
[800]	valid_0&#39;s l2: 0.566903
[900]	valid_0&#39;s l2: 0.564055
[1000]	valid_0&#39;s l2: 0.564367
[1100]	valid_0&#39;s l2: 0.560574
[1200]	valid_0&#39;s l2: 0.55884
[1300]	valid_0&#39;s l2: 0.558889
Early stopping, best iteration is:
[1285]	valid_0&#39;s l2: 0.55817
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.35994
[200]	valid_0&#39;s l2: 0.962199
[300]	valid_0&#39;s l2: 0.764813
[400]	valid_0&#39;s l2: 0.657071
[500]	valid_0&#39;s l2: 0.602217
[600]	valid_0&#39;s l2: 0.570079
[700]	valid_0&#39;s l2: 0.550579
[800]	valid_0&#39;s l2: 0.542893
[900]	valid_0&#39;s l2: 0.537319
[1000]	valid_0&#39;s l2: 0.533008
[1100]	valid_0&#39;s l2: 0.533553
Early stopping, best iteration is:
[1020]	valid_0&#39;s l2: 0.531837
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.3582
[200]	valid_0&#39;s l2: 1.00735
[300]	valid_0&#39;s l2: 0.834467
[400]	valid_0&#39;s l2: 0.745757
[500]	valid_0&#39;s l2: 0.692923
[600]	valid_0&#39;s l2: 0.658908
[700]	valid_0&#39;s l2: 0.635103
[800]	valid_0&#39;s l2: 0.61686
[900]	valid_0&#39;s l2: 0.603879
[1000]	valid_0&#39;s l2: 0.595594
[1100]	valid_0&#39;s l2: 0.592077
[1200]	valid_0&#39;s l2: 0.585095
[1300]	valid_0&#39;s l2: 0.584306
[1400]	valid_0&#39;s l2: 0.584128
[1500]	valid_0&#39;s l2: 0.582237
[1600]	valid_0&#39;s l2: 0.581271
[1700]	valid_0&#39;s l2: 0.584105
Early stopping, best iteration is:
[1626]	valid_0&#39;s l2: 0.580531
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.705426
[200]	valid_0&#39;s l2: 0.492072
[300]	valid_0&#39;s l2: 0.403358
[400]	valid_0&#39;s l2: 0.363326
[500]	valid_0&#39;s l2: 0.345344
[600]	valid_0&#39;s l2: 0.335971
[700]	valid_0&#39;s l2: 0.33206
[800]	valid_0&#39;s l2: 0.330104
[900]	valid_0&#39;s l2: 0.330112
Early stopping, best iteration is:
[824]	valid_0&#39;s l2: 0.329526
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.963818
[200]	valid_0&#39;s l2: 0.7241
[300]	valid_0&#39;s l2: 0.62685
[400]	valid_0&#39;s l2: 0.586593
[500]	valid_0&#39;s l2: 0.566301
[600]	valid_0&#39;s l2: 0.56097
[700]	valid_0&#39;s l2: 0.557618
[800]	valid_0&#39;s l2: 0.558016
Early stopping, best iteration is:
[740]	valid_0&#39;s l2: 0.556295
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.0265
[200]	valid_0&#39;s l2: 0.765853
[300]	valid_0&#39;s l2: 0.65342
[400]	valid_0&#39;s l2: 0.601044
[500]	valid_0&#39;s l2: 0.575068
[600]	valid_0&#39;s l2: 0.564816
[700]	valid_0&#39;s l2: 0.555955
[800]	valid_0&#39;s l2: 0.550742
[900]	valid_0&#39;s l2: 0.548717
Early stopping, best iteration is:
[838]	valid_0&#39;s l2: 0.548026
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.921865
[200]	valid_0&#39;s l2: 0.696836
[300]	valid_0&#39;s l2: 0.603471
[400]	valid_0&#39;s l2: 0.566043
[500]	valid_0&#39;s l2: 0.55119
[600]	valid_0&#39;s l2: 0.545816
Early stopping, best iteration is:
[597]	valid_0&#39;s l2: 0.545706
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.918617
[200]	valid_0&#39;s l2: 0.689079
[300]	valid_0&#39;s l2: 0.588087
[400]	valid_0&#39;s l2: 0.541189
[500]	valid_0&#39;s l2: 0.522407
[600]	valid_0&#39;s l2: 0.512994
[700]	valid_0&#39;s l2: 0.507982
[800]	valid_0&#39;s l2: 0.506388
[900]	valid_0&#39;s l2: 0.507294
Early stopping, best iteration is:
[801]	valid_0&#39;s l2: 0.506247
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.21006
[200]	valid_0&#39;s l2: 0.967992
[300]	valid_0&#39;s l2: 0.881868
[400]	valid_0&#39;s l2: 0.847262
[500]	valid_0&#39;s l2: 0.839258
[600]	valid_0&#39;s l2: 0.835637
Early stopping, best iteration is:
[542]	valid_0&#39;s l2: 0.834173
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.951327
[200]	valid_0&#39;s l2: 0.787714
[300]	valid_0&#39;s l2: 0.721056
[400]	valid_0&#39;s l2: 0.688607
[500]	valid_0&#39;s l2: 0.675585
[600]	valid_0&#39;s l2: 0.668102
[700]	valid_0&#39;s l2: 0.66252
[800]	valid_0&#39;s l2: 0.655719
[900]	valid_0&#39;s l2: 0.654709
[1000]	valid_0&#39;s l2: 0.652624
[1100]	valid_0&#39;s l2: 0.653736
[1200]	valid_0&#39;s l2: 0.652532
Early stopping, best iteration is:
[1170]	valid_0&#39;s l2: 0.650942
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.63371
[200]	valid_0&#39;s l2: 0.531466
[300]	valid_0&#39;s l2: 0.498343
[400]	valid_0&#39;s l2: 0.495519
Early stopping, best iteration is:
[347]	valid_0&#39;s l2: 0.493375
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 0.898566
[200]	valid_0&#39;s l2: 0.667785
[300]	valid_0&#39;s l2: 0.55305
[400]	valid_0&#39;s l2: 0.491631
[500]	valid_0&#39;s l2: 0.452436
[600]	valid_0&#39;s l2: 0.43026
[700]	valid_0&#39;s l2: 0.416144
[800]	valid_0&#39;s l2: 0.407455
[900]	valid_0&#39;s l2: 0.400944
[1000]	valid_0&#39;s l2: 0.400663
[1100]	valid_0&#39;s l2: 0.400402
[1200]	valid_0&#39;s l2: 0.396504
[1300]	valid_0&#39;s l2: 0.39767
Early stopping, best iteration is:
[1211]	valid_0&#39;s l2: 0.396251
Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.08857
[200]	valid_0&#39;s l2: 0.86885
[300]	valid_0&#39;s l2: 0.770611
[400]	valid_0&#39;s l2: 0.723653
[500]	valid_0&#39;s l2: 0.696006
[600]	valid_0&#39;s l2: 0.682301
[700]	valid_0&#39;s l2: 0.676229
[800]	valid_0&#39;s l2: 0.672673
[900]	valid_0&#39;s l2: 0.671773
Early stopping, best iteration is:
[834]	valid_0&#39;s l2: 0.670503
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
  <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">):</span>
    <span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/empty_model/season_&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">j</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[292]:</div>
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
<pre>weighted rmse:  0.9622504486493763
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[293]:</div>
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
<pre>weighted rmse:  0.942178610858556
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[200]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">ax</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">plot_importance</span><span class="p">(</span><span class="n">model</span><span class="p">,</span><span class="n">max_num_features</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
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
CgcGpZ3FFAAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[201]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">8</span><span class="p">))</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">data</span> <span class="o">=</span> <span class="n">all_merged</span><span class="o">.</span><span class="n">corr</span><span class="p">(</span><span class="n">method</span><span class="o">=</span><span class="s1">&#39;pearson&#39;</span><span class="p">),</span> <span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">fmt</span> <span class="o">=</span> <span class="s1">&#39;.3f&#39;</span><span class="p">,</span> <span class="n">linewidths</span><span class="o">=.</span><span class="mi">1</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;Oranges&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[201]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f1f135b0748&gt;</pre>
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
