---
layout: post
title: Space Calamity - Test Set Preprocessing
date: 2020-06-13
description: Space Calamity - Test Set Preprocessing
thumbnail: building1.jpg
categories: DataMining

# Information for the author block
author : Loui
---


<html>
<head><meta charset="utf-8" />

<title>Space Calamity - Test Set Preprocessing</title>

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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="&#49884;&#44036;&#48324;&#47196;-8&#44060;&#47196;-&#45208;&#45572;&#50612;&#49436;-&#51204;&#52376;&#47532;">&#49884;&#44036;&#48324;&#47196; 8&#44060;&#47196; &#45208;&#45572;&#50612;&#49436; &#51204;&#52376;&#47532;<a class="anchor-link" href="#&#49884;&#44036;&#48324;&#47196;-8&#44060;&#47196;-&#45208;&#45572;&#50612;&#49436;-&#51204;&#52376;&#47532;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test/test.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="n">test</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">temp</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>h</th>
      <th>m</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1.852</td>
      <td>41618.0</td>
      <td>455.61</td>
      <td>6.098</td>
      <td>2.449</td>
      <td>-13.415</td>
      <td>14.952</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>2.181</td>
      <td>33781.0</td>
      <td>461.07</td>
      <td>6.700</td>
      <td>1.502</td>
      <td>-13.232</td>
      <td>14.912</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>2.415</td>
      <td>34709.0</td>
      <td>464.84</td>
      <td>7.390</td>
      <td>0.523</td>
      <td>-12.941</td>
      <td>14.928</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>2.359</td>
      <td>34183.0</td>
      <td>470.76</td>
      <td>8.011</td>
      <td>-0.098</td>
      <td>-12.694</td>
      <td>15.013</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>0</td>
      <td>4</td>
      <td>1.237</td>
      <td>32467.0</td>
      <td>469.51</td>
      <td>7.493</td>
      <td>0.410</td>
      <td>-13.058</td>
      <td>15.064</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="p">[</span><span class="n">temp</span><span class="o">.</span><span class="n">index</span><span class="o">==</span><span class="mi">44210</span><span class="p">]</span>
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
      <th>doy</th>
      <th>h</th>
      <th>m</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>44210</th>
      <td>57</td>
      <td>11</td>
      <td>57</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
      <td>-9999.9</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df1</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">3</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">5</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">6</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">9</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">11</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">12</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">14</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">15</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">17</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">18</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">20</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">21</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">23</span><span class="p">)]</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="p">[(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">0</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;h&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">2</span><span class="p">)]</span>

<span class="c1"># hour 와 min 제거</span>
<span class="c1">#for i in range(8):</span>
 <span class="c1"># df1[i].drop([&#39;h&#39;,&#39;m&#39;],axis=1,inplace=True)</span>
<span class="n">df1</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>h</th>
      <th>m</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>169</th>
      <td>1</td>
      <td>3</td>
      <td>0</td>
      <td>1.002</td>
      <td>25369.0</td>
      <td>431.33</td>
      <td>3.899</td>
      <td>3.844</td>
      <td>-12.229</td>
      <td>13.401</td>
    </tr>
    <tr>
      <th>170</th>
      <td>1</td>
      <td>3</td>
      <td>1</td>
      <td>-9999.900</td>
      <td>-9999.9</td>
      <td>-9999.90</td>
      <td>3.637</td>
      <td>3.293</td>
      <td>-12.509</td>
      <td>13.441</td>
    </tr>
    <tr>
      <th>171</th>
      <td>1</td>
      <td>3</td>
      <td>2</td>
      <td>-9999.900</td>
      <td>11752.0</td>
      <td>426.57</td>
      <td>3.397</td>
      <td>2.830</td>
      <td>-12.696</td>
      <td>13.445</td>
    </tr>
    <tr>
      <th>172</th>
      <td>1</td>
      <td>3</td>
      <td>3</td>
      <td>-9999.900</td>
      <td>10408.0</td>
      <td>423.43</td>
      <td>3.420</td>
      <td>2.791</td>
      <td>-12.689</td>
      <td>13.436</td>
    </tr>
    <tr>
      <th>173</th>
      <td>1</td>
      <td>3</td>
      <td>5</td>
      <td>-9999.900</td>
      <td>11419.0</td>
      <td>427.22</td>
      <td>3.461</td>
      <td>2.799</td>
      <td>-12.689</td>
      <td>13.448</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">df1</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#-9999를 해당날짜의 mean으로 처리하기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bmag&#39;</span><span class="p">]:</span>
    <span class="k">for</span> <span class="n">doy</span> <span class="ow">in</span> <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
      <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">doy</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">doy</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9998</span><span class="p">)][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
    
    <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;번째 df &#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39; done&#39;</span><span class="p">)</span>
  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>0번째 df Np done
0번째 df Tp done
0번째 df Vp done
0번째 df B_gsm_x done
0번째 df B_gsm_y done
0번째 df B_gsm_z done
0번째 df Bmag done
1번째 df Np done
1번째 df Tp done
1번째 df Vp done
1번째 df B_gsm_x done
1번째 df B_gsm_y done
1번째 df B_gsm_z done
1번째 df Bmag done
2번째 df Np done
2번째 df Tp done
2번째 df Vp done
2번째 df B_gsm_x done
2번째 df B_gsm_y done
2번째 df B_gsm_z done
2번째 df Bmag done
3번째 df Np done
3번째 df Tp done
3번째 df Vp done
3번째 df B_gsm_x done
3번째 df B_gsm_y done
3번째 df B_gsm_z done
3번째 df Bmag done
4번째 df Np done
4번째 df Tp done
4번째 df Vp done
4번째 df B_gsm_x done
4번째 df B_gsm_y done
4번째 df B_gsm_z done
4번째 df Bmag done
5번째 df Np done
5번째 df Tp done
5번째 df Vp done
5번째 df B_gsm_x done
5번째 df B_gsm_y done
5번째 df B_gsm_z done
5번째 df Bmag done
6번째 df Np done
6번째 df Tp done
6번째 df Vp done
6번째 df B_gsm_x done
6번째 df B_gsm_y done
6번째 df B_gsm_z done
6번째 df Bmag done
7번째 df Np done
7번째 df Tp done
7번째 df Vp done
7번째 df B_gsm_x done
7번째 df B_gsm_y done
7번째 df B_gsm_z done
7번째 df Bmag done
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/final_test_csv/test&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/final_test_csv/test&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 하루 기준으로 합치기 기준은 mean</span>
<span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bmag&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[3]:</div>



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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>NaN</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Bmag을 Bt로 이름 바꾸기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;Bmag&#39;</span><span class="p">:</span><span class="s1">&#39;Bt&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Np.csv&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Tp.csv&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Vp.csv&#39;</span><span class="p">)</span>
<span class="n">Bx</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Bx.csv&#39;</span><span class="p">)</span>
<span class="n">By</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/By.csv&#39;</span><span class="p">)</span>
<span class="n">Bz</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Bz.csv&#39;</span><span class="p">)</span>
<span class="n">Bt</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Bt.csv&#39;</span><span class="p">)</span>

<span class="n">Np_medi</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Np_medi.csv&#39;</span><span class="p">)</span>
<span class="n">Tp_medi</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Tp_medi.csv&#39;</span><span class="p">)</span>
<span class="n">Vp_medi</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Vp_medi.csv&#39;</span><span class="p">)</span>
<span class="n">Bx_medi</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Bx_medi.csv&#39;</span><span class="p">)</span>
<span class="n">By_medi</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/By_medi.csv&#39;</span><span class="p">)</span>
<span class="n">Bz_medi</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Bz_medi.csv&#39;</span><span class="p">)</span>
<span class="n">Bt_medi</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/means_csv/Bt_medi.csv&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">):</span>
  <span class="n">Np</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>  
  <span class="n">Tp</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Vp</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bx</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">By</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bz</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bt</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
  <span class="n">Np_medi</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>  
  <span class="n">Tp_medi</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Vp_medi</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bx_medi</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">By_medi</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bz_medi</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bt_medi</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">):</span><span class="n">i</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Bt를 이용하여 Nan값 처리. 왜냐하면 Bt는 Nan값이 없음</span>
<span class="c1">#이거는 test셋 용인데 일단 테스트해보려고 가져온 것임</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">]:</span>
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Np</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">7</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Np</span><span class="p">[</span><span class="n">i</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">8</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">9</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Np</span><span class="p">[</span><span class="mi">9</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Tp</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">7</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Tp</span><span class="p">[</span><span class="n">i</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">8</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">9</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Tp</span><span class="p">[</span><span class="mi">9</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Vp</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">7</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Vp</span><span class="p">[</span><span class="n">i</span><span class="o">+</span><span class="mi">1</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">8</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">9</span><span class="p">][</span><span class="n">i</span><span class="p">])</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Vp</span><span class="p">[</span><span class="mi">9</span><span class="p">][</span><span class="n">i</span><span class="p">]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#각 컬럼별 range 생성해주기 그리고 스케일링 하는데, 각 데이터프레임의 평균으로 하기</span>
<span class="c1">#구림</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Np_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">8</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>        
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Tp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">5</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Tp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">7</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">7</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Vp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">8</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">5</span><span class="p">])</span><span class="o">&amp;</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">9</span><span class="p">],</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">9</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">By_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">By_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">By_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">8</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_z&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bz_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bz_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="n">Bz_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">8</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Bt&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bt_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bt_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bt_mean</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">8</span><span class="p">]),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
     
<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#각 컬럼별 range 생성해주기 그리고 4로 나눠서 스케일링 이건 전체평균으로한거의 mean값으로 한거 </span>
<span class="c1">#코드보면 이해할거임</span>
<span class="c1">#1번</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Np</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Np</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Tp</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>        
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Tp</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Tp</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Tp</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Vp</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Vp</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bx</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bx</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bx</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bx</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">By</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">By</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">By</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">By</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_z&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bz</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bz</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bz</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bz</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Bt&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">+</span><span class="n">Bt</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
     
<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>Np_range</th>
      <th>Tp_range</th>
      <th>Vp_range</th>
      <th>B_gsm_x_range</th>
      <th>B_gsm_y_range</th>
      <th>B_gsm_z_range</th>
      <th>Bt_range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.983706</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.5</td>
      <td>1.5</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
      <td>2.0</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.0</td>
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
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#각 컬럼별 range 생성해주기 그리고 4로 나눠서 스케일링 이건 전체평균으로한거의 mean값으로 한거 </span>
<span class="c1">#코드보면 이해할거임</span>
<span class="c1">#메디안 1-2번 mean이아니라 median으로 분류</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Np_medi</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Np_medi</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Np_medi</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Np_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Np_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Np_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Np_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Np_medi</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>        
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Tp_medi</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Tp_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Tp_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Tp_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Tp_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Vp_medi</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Vp_medi</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Vp_medi</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Vp_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Vp_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Vp_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Vp_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Vp_medi</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bx_medi</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bx_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bx_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bx_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bx_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">By_medi</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">By_medi</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">By_medi</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">By_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">By_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">By_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">By_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">By_medi</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_z&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bz_medi</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bz_medi</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bz_medi</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bz_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bz_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bz_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bz_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bz_medi</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
      
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Bt&#39;</span><span class="p">:</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="p">(</span><span class="n">Bt_medi</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bt_medi</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bt_medi</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bt_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="p">(</span><span class="n">Bt_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bt_medi</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="p">(</span><span class="n">Bt_medi</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span><span class="o">+</span><span class="n">Bt_medi</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_medi_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
     
<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[9]:</div>



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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>Np_range</th>
      <th>Tp_range</th>
      <th>Vp_range</th>
      <th>B_gsm_x_range</th>
      <th>B_gsm_y_range</th>
      <th>B_gsm_z_range</th>
      <th>Bt_range</th>
      <th>Np_medi_range</th>
      <th>Tp_medi_range</th>
      <th>Vp_medi_range</th>
      <th>B_gsm_x_medi_range</th>
      <th>B_gsm_y_medi_range</th>
      <th>B_gsm_z_medi_range</th>
      <th>Bt_medi_range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>4.5</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.983706</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.5</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>0.5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
      <td>2.0</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>1.5</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#각 컬럼별 range 생성해주기 그리고 4로 나눠서 스케일링 이건 전체평균으로한거</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>        
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span><span class="o">/</span><span class="mi">2</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span><span class="o">/</span><span class="mi">2</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">By</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_z&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="n">Bz</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Bt&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bt</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span><span class="o">/</span><span class="mi">2</span>
     
<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>Np_range</th>
      <th>Tp_range</th>
      <th>Vp_range</th>
      <th>B_gsm_x_range</th>
      <th>B_gsm_y_range</th>
      <th>B_gsm_z_range</th>
      <th>Bt_range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>3.0</td>
      <td>4.0</td>
      <td>4.5</td>
      <td>3.5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>2.5</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.983706</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.5</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.5</td>
      <td>1.5</td>
      <td>0.5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
      <td>2.5</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.5</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#각 컬럼별 range 생성해주기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>        
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">5</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>    
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">6</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">7</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">By</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">By</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>        
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_z&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bz</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;</span><span class="n">Bz</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Bt&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bt</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bt</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
     
<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>Np_range</th>
      <th>Tp_range</th>
      <th>Vp_range</th>
      <th>B_gsm_x_range</th>
      <th>B_gsm_y_range</th>
      <th>B_gsm_z_range</th>
      <th>Bt_range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>6</td>
      <td>8</td>
      <td>9</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>6</td>
      <td>0</td>
      <td>5</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.983706</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
      <td>2</td>
      <td>2</td>
      <td>3</td>
      <td>7</td>
      <td>8</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
      <td>0</td>
      <td>2</td>
      <td>2</td>
      <td>7</td>
      <td>7</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
      <td>5</td>
      <td>2</td>
      <td>2</td>
      <td>7</td>
      <td>8</td>
      <td>0</td>
      <td>3</td>
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
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#week 만들기 7일단위로 가볍게 끊고 스케일링하기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">floor</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">/</span><span class="mi">7</span><span class="p">)</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy_cycle&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">%</span><span class="k">7</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">8</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">46</span><span class="p">),</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">3</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">8</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">20</span><span class="p">),</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">20</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">32</span><span class="p">),</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">32</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;woy&#39;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">46</span><span class="p">),</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">2</span>

<span class="c1">#자신의 소속 시간 명시하기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">i</span>

<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[10]:</div>



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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>Np_range</th>
      <th>Tp_range</th>
      <th>Vp_range</th>
      <th>B_gsm_x_range</th>
      <th>B_gsm_y_range</th>
      <th>B_gsm_z_range</th>
      <th>Bt_range</th>
      <th>Np_medi_range</th>
      <th>Tp_medi_range</th>
      <th>Vp_medi_range</th>
      <th>B_gsm_x_medi_range</th>
      <th>B_gsm_y_medi_range</th>
      <th>B_gsm_z_medi_range</th>
      <th>Bt_medi_range</th>
      <th>woy</th>
      <th>woy_cycle</th>
      <th>season</th>
      <th>range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>4.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>2</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.983706</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>3</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.5</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>4</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
      <td>2.0</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>5</td>
      <td>3.0</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/DW/test&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Tp랑 VP는 수가 너무 크니까 로그 취해주기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">])</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">])</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>Np_range</th>
      <th>Tp_range</th>
      <th>Vp_range</th>
      <th>B_gsm_x_range</th>
      <th>B_gsm_y_range</th>
      <th>B_gsm_z_range</th>
      <th>Bt_range</th>
      <th>Np_medi_range</th>
      <th>Tp_medi_range</th>
      <th>Vp_medi_range</th>
      <th>B_gsm_x_medi_range</th>
      <th>B_gsm_y_medi_range</th>
      <th>B_gsm_z_medi_range</th>
      <th>Bt_medi_range</th>
      <th>woy</th>
      <th>woy_cycle</th>
      <th>season</th>
      <th>range</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>10.396440</td>
      <td>6.093758</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>4.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>10.460123</td>
      <td>6.083133</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>2</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.983706</td>
      <td>11.304106</td>
      <td>6.081002</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>3</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>11.347678</td>
      <td>6.038342</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.5</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>4</td>
      <td>3.0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>11.224455</td>
      <td>6.039010</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
      <td>2.0</td>
      <td>0.5</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.5</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>5</td>
      <td>3.0</td>
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
<h1 id="-9999&#47484;-&#54644;&#45817;-&#51068;&#51088;&#51032;-mean&#44050;&#51004;&#47196;-&#45824;&#52404;&#54616;&#44592;"><strong>-9999&#47484; &#54644;&#45817; &#51068;&#51088;&#51032; mean&#44050;&#51004;&#47196; &#45824;&#52404;&#54616;&#44592;</strong><a class="anchor-link" href="#-9999&#47484;-&#54644;&#45817;-&#51068;&#51088;&#51032;-mean&#44050;&#51004;&#47196;-&#45824;&#52404;&#54616;&#44592;">&#182;</a></h1><hr>
<h1 id="B_gsm_x,y,z,-Bt-&#50640;-&#45824;&#54644;&#49436;&#45716;-&#50504;&#54644;&#46020;&#46120;-&#50780;&#45264;&#54616;&#47732;--9999&#44032;-&#50630;&#51020;-test&#49483;&#50640;&#45716;">B_gsm_x,y,z, Bt &#50640; &#45824;&#54644;&#49436;&#45716; &#50504;&#54644;&#46020;&#46120; &#50780;&#45264;&#54616;&#47732; -9999&#44032; &#50630;&#51020; test&#49483;&#50640;&#45716;<a class="anchor-link" href="#B_gsm_x,y,z,-Bt-&#50640;-&#45824;&#54644;&#49436;&#45716;-&#50504;&#54644;&#46020;&#46120;-&#50780;&#45264;&#54616;&#47732;--9999&#44032;-&#50630;&#51020;-test&#49483;&#50640;&#45716;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">df1</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">k</span><span class="o">=</span><span class="mi">0</span>
<span class="k">for</span> <span class="n">ace0</span> <span class="ow">in</span> <span class="n">df</span><span class="p">:</span>
  <span class="n">df_Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df_Vp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df_Tp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="c1">#for i in ace0[&#39;year&#39;].unique():</span>
  <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>

    <span class="n">mean_np</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
    <span class="n">Np</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)]</span>
    <span class="n">Np</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_np</span>
    <span class="n">df_Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_Np</span><span class="p">,</span><span class="n">Np</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">k</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;번째 Np done&#39;</span><span class="p">)</span>

  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_Np</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

  <span class="c1">#for i in ace0[&#39;year&#39;].unique():</span>
  <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="n">mean_vp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
    <span class="n">Vp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)]</span>
    <span class="n">Vp</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_vp</span>
    <span class="n">df_Vp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_Vp</span><span class="p">,</span><span class="n">Vp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

  
  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">k</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;번째 Vp done&#39;</span><span class="p">)</span>  

  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_Vp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>


  <span class="c1">#for i in ace0[&#39;year&#39;].unique():</span>
  <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="n">mean_tp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
    <span class="n">Tp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)]</span>
    <span class="n">Tp</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_tp</span>
    <span class="n">df_Tp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_Tp</span><span class="p">,</span><span class="n">Tp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>



  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">k</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;번째 Tp done&#39;</span><span class="p">)</span>

  
  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_Tp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">save</span><span class="p">[</span><span class="n">k</span><span class="p">]</span><span class="o">=</span><span class="n">ace0</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
  <span class="n">k</span><span class="o">+=</span><span class="mi">1</span>
  
  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">k</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39; 번째 df 끝&#39;</span><span class="p">)</span>
<span class="n">ace0</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>  
<span class="c1">#sort  value 랑 drop_duplicate은마지막에 한번만 하면 된다.</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:12: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  if sys.path[0] == &#39;&#39;:
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>1번째 Np done
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:25: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>1번째 Vp done
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:40: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>1번째 Tp done
2 번째 df 끝
2번째 Np done
2번째 Vp done
2번째 Tp done
3 번째 df 끝
3번째 Np done
3번째 Vp done
3번째 Tp done
4 번째 df 끝
4번째 Np done
4번째 Vp done
4번째 Tp done
5 번째 df 끝
5번째 Np done
5번째 Vp done
5번째 Tp done
6 번째 df 끝
6번째 Np done
6번째 Vp done
6번째 Tp done
7 번째 df 끝
7번째 Np done
7번째 Vp done
7번째 Tp done
8 번째 df 끝
8번째 Np done
8번째 Vp done
8번째 Tp done
9 번째 df 끝
</pre>
</div>
</div>

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
      <th>doy</th>
      <th>h</th>
      <th>m</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>21</td>
      <td>0</td>
      <td>8.307</td>
      <td>62953.0</td>
      <td>444.86</td>
      <td>2.748</td>
      <td>-1.365</td>
      <td>0.180</td>
      <td>3.083</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>21</td>
      <td>1</td>
      <td>8.810</td>
      <td>63332.0</td>
      <td>446.04</td>
      <td>2.366</td>
      <td>-1.506</td>
      <td>-0.073</td>
      <td>2.818</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>21</td>
      <td>2</td>
      <td>8.741</td>
      <td>61453.0</td>
      <td>443.32</td>
      <td>1.938</td>
      <td>-1.513</td>
      <td>-0.176</td>
      <td>2.477</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>21</td>
      <td>3</td>
      <td>8.647</td>
      <td>74792.0</td>
      <td>448.14</td>
      <td>3.505</td>
      <td>-0.921</td>
      <td>0.045</td>
      <td>3.656</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>21</td>
      <td>4</td>
      <td>8.355</td>
      <td>72047.0</td>
      <td>449.97</td>
      <td>3.283</td>
      <td>-0.384</td>
      <td>-0.113</td>
      <td>3.315</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_test_9999_before_merge/test&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_test_9999_before_merge/test&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(57056, 10)</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="mi">57869</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="mi">6055</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">save</span><span class="p">[</span><span class="mi">7</span><span class="p">][</span><span class="n">save</span><span class="p">[</span><span class="mi">7</span><span class="p">][</span><span class="s1">&#39;Bmag&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">1000</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="n">save</span><span class="p">[</span><span class="mi">3</span><span class="p">][</span><span class="n">save</span><span class="p">[</span><span class="mi">3</span><span class="p">][</span><span class="s1">&#39;Bmag&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">1000</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Empty DataFrame
Columns: [doy, h, m, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bmag]
Index: []
Empty DataFrame
Columns: [doy, h, m, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bmag]
Index: []
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">df_Vp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">df_Tp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="c1">#for i in ace0[&#39;year&#39;].unique():</span>
<span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>

  <span class="n">mean_np</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">Np</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)]</span>
  <span class="n">Np</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_np</span>
  <span class="n">df_Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_Np</span><span class="p">,</span><span class="n">Np</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">j</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39; : &#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">mean_np</span><span class="p">))</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">9000</span><span class="p">]</span>
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
      <th>doy</th>
      <th>h</th>
      <th>m</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">save</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">]</span>
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
      <th>doy</th>
      <th>h</th>
      <th>m</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>338</th>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
      <td>59366.000000</td>
      <td>452.730000</td>
      <td>-3.826</td>
      <td>4.111</td>
      <td>-2.855</td>
      <td>6.463</td>
    </tr>
    <tr>
      <th>339</th>
      <td>3</td>
      <td>0</td>
      <td>1</td>
      <td>NaN</td>
      <td>59861.000000</td>
      <td>450.450000</td>
      <td>-5.057</td>
      <td>3.195</td>
      <td>-0.593</td>
      <td>6.326</td>
    </tr>
    <tr>
      <th>340</th>
      <td>3</td>
      <td>0</td>
      <td>2</td>
      <td>NaN</td>
      <td>92736.000000</td>
      <td>438.270000</td>
      <td>-6.259</td>
      <td>2.019</td>
      <td>0.158</td>
      <td>6.603</td>
    </tr>
    <tr>
      <th>341</th>
      <td>3</td>
      <td>0</td>
      <td>3</td>
      <td>NaN</td>
      <td>79804.000000</td>
      <td>437.360000</td>
      <td>-6.434</td>
      <td>1.758</td>
      <td>-0.190</td>
      <td>6.679</td>
    </tr>
    <tr>
      <th>342</th>
      <td>3</td>
      <td>0</td>
      <td>4</td>
      <td>NaN</td>
      <td>82479.000000</td>
      <td>438.230000</td>
      <td>-6.360</td>
      <td>2.070</td>
      <td>0.256</td>
      <td>6.694</td>
    </tr>
    <tr>
      <th>343</th>
      <td>3</td>
      <td>0</td>
      <td>5</td>
      <td>NaN</td>
      <td>82709.000000</td>
      <td>437.620000</td>
      <td>-6.408</td>
      <td>2.112</td>
      <td>0.590</td>
      <td>6.775</td>
    </tr>
    <tr>
      <th>344</th>
      <td>3</td>
      <td>0</td>
      <td>6</td>
      <td>NaN</td>
      <td>96446.000000</td>
      <td>441.400000</td>
      <td>-6.395</td>
      <td>2.311</td>
      <td>0.828</td>
      <td>6.859</td>
    </tr>
    <tr>
      <th>345</th>
      <td>3</td>
      <td>0</td>
      <td>7</td>
      <td>NaN</td>
      <td>82352.000000</td>
      <td>438.770000</td>
      <td>-5.987</td>
      <td>2.432</td>
      <td>0.584</td>
      <td>6.496</td>
    </tr>
    <tr>
      <th>346</th>
      <td>3</td>
      <td>0</td>
      <td>9</td>
      <td>NaN</td>
      <td>88905.000000</td>
      <td>438.820000</td>
      <td>-6.005</td>
      <td>2.462</td>
      <td>0.689</td>
      <td>6.535</td>
    </tr>
    <tr>
      <th>347</th>
      <td>3</td>
      <td>0</td>
      <td>10</td>
      <td>NaN</td>
      <td>79510.000000</td>
      <td>439.980000</td>
      <td>-6.090</td>
      <td>2.646</td>
      <td>1.134</td>
      <td>6.748</td>
    </tr>
    <tr>
      <th>348</th>
      <td>3</td>
      <td>0</td>
      <td>11</td>
      <td>NaN</td>
      <td>90796.000000</td>
      <td>440.440000</td>
      <td>-6.052</td>
      <td>2.362</td>
      <td>1.188</td>
      <td>6.617</td>
    </tr>
    <tr>
      <th>349</th>
      <td>3</td>
      <td>0</td>
      <td>12</td>
      <td>NaN</td>
      <td>86776.000000</td>
      <td>439.350000</td>
      <td>-5.981</td>
      <td>2.420</td>
      <td>1.489</td>
      <td>6.631</td>
    </tr>
    <tr>
      <th>57069</th>
      <td>3</td>
      <td>0</td>
      <td>13</td>
      <td>NaN</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.030</td>
      <td>2.542</td>
      <td>1.211</td>
      <td>6.676</td>
    </tr>
    <tr>
      <th>351</th>
      <td>3</td>
      <td>0</td>
      <td>14</td>
      <td>NaN</td>
      <td>87707.000000</td>
      <td>439.640000</td>
      <td>-6.109</td>
      <td>2.396</td>
      <td>1.142</td>
      <td>6.668</td>
    </tr>
    <tr>
      <th>352</th>
      <td>3</td>
      <td>0</td>
      <td>15</td>
      <td>NaN</td>
      <td>83140.000000</td>
      <td>439.610000</td>
      <td>-6.066</td>
      <td>2.689</td>
      <td>0.917</td>
      <td>6.712</td>
    </tr>
    <tr>
      <th>353</th>
      <td>3</td>
      <td>0</td>
      <td>16</td>
      <td>NaN</td>
      <td>85682.000000</td>
      <td>440.540000</td>
      <td>-6.152</td>
      <td>2.780</td>
      <td>0.813</td>
      <td>6.810</td>
    </tr>
    <tr>
      <th>354</th>
      <td>3</td>
      <td>0</td>
      <td>17</td>
      <td>NaN</td>
      <td>81383.000000</td>
      <td>439.740000</td>
      <td>-6.356</td>
      <td>2.428</td>
      <td>0.736</td>
      <td>6.860</td>
    </tr>
    <tr>
      <th>355</th>
      <td>3</td>
      <td>0</td>
      <td>18</td>
      <td>NaN</td>
      <td>79501.000000</td>
      <td>440.200000</td>
      <td>-6.132</td>
      <td>2.974</td>
      <td>0.717</td>
      <td>6.862</td>
    </tr>
    <tr>
      <th>356</th>
      <td>3</td>
      <td>0</td>
      <td>19</td>
      <td>NaN</td>
      <td>87859.000000</td>
      <td>438.020000</td>
      <td>-6.197</td>
      <td>2.892</td>
      <td>0.731</td>
      <td>6.885</td>
    </tr>
    <tr>
      <th>357</th>
      <td>3</td>
      <td>0</td>
      <td>20</td>
      <td>NaN</td>
      <td>75147.000000</td>
      <td>439.910000</td>
      <td>-5.973</td>
      <td>3.120</td>
      <td>1.139</td>
      <td>6.853</td>
    </tr>
    <tr>
      <th>358</th>
      <td>3</td>
      <td>0</td>
      <td>21</td>
      <td>NaN</td>
      <td>86375.000000</td>
      <td>440.690000</td>
      <td>-5.973</td>
      <td>2.947</td>
      <td>1.329</td>
      <td>6.800</td>
    </tr>
    <tr>
      <th>359</th>
      <td>3</td>
      <td>0</td>
      <td>22</td>
      <td>NaN</td>
      <td>76397.000000</td>
      <td>439.180000</td>
      <td>-6.105</td>
      <td>3.000</td>
      <td>0.830</td>
      <td>6.861</td>
    </tr>
    <tr>
      <th>360</th>
      <td>3</td>
      <td>0</td>
      <td>23</td>
      <td>NaN</td>
      <td>79685.000000</td>
      <td>439.020000</td>
      <td>-6.254</td>
      <td>3.035</td>
      <td>1.090</td>
      <td>7.055</td>
    </tr>
    <tr>
      <th>361</th>
      <td>3</td>
      <td>0</td>
      <td>25</td>
      <td>NaN</td>
      <td>73825.000000</td>
      <td>439.730000</td>
      <td>-6.365</td>
      <td>2.894</td>
      <td>1.791</td>
      <td>7.223</td>
    </tr>
    <tr>
      <th>362</th>
      <td>3</td>
      <td>0</td>
      <td>26</td>
      <td>NaN</td>
      <td>77347.000000</td>
      <td>442.140000</td>
      <td>-6.459</td>
      <td>2.996</td>
      <td>1.649</td>
      <td>7.314</td>
    </tr>
    <tr>
      <th>363</th>
      <td>3</td>
      <td>0</td>
      <td>27</td>
      <td>NaN</td>
      <td>100310.000000</td>
      <td>451.950000</td>
      <td>-5.911</td>
      <td>1.859</td>
      <td>3.383</td>
      <td>7.083</td>
    </tr>
    <tr>
      <th>364</th>
      <td>3</td>
      <td>0</td>
      <td>28</td>
      <td>NaN</td>
      <td>87121.000000</td>
      <td>452.600000</td>
      <td>-5.904</td>
      <td>2.047</td>
      <td>3.490</td>
      <td>7.170</td>
    </tr>
    <tr>
      <th>365</th>
      <td>3</td>
      <td>0</td>
      <td>29</td>
      <td>NaN</td>
      <td>82467.000000</td>
      <td>459.750000</td>
      <td>-5.811</td>
      <td>1.732</td>
      <td>3.758</td>
      <td>7.142</td>
    </tr>
    <tr>
      <th>366</th>
      <td>3</td>
      <td>0</td>
      <td>30</td>
      <td>NaN</td>
      <td>83171.000000</td>
      <td>461.000000</td>
      <td>-6.061</td>
      <td>2.072</td>
      <td>3.756</td>
      <td>7.429</td>
    </tr>
    <tr>
      <th>367</th>
      <td>3</td>
      <td>0</td>
      <td>31</td>
      <td>NaN</td>
      <td>84390.000000</td>
      <td>452.390000</td>
      <td>-6.309</td>
      <td>2.147</td>
      <td>3.882</td>
      <td>7.714</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>56857</th>
      <td>364</td>
      <td>2</td>
      <td>28</td>
      <td>NaN</td>
      <td>29838.000000</td>
      <td>417.310000</td>
      <td>0.644</td>
      <td>3.544</td>
      <td>-0.308</td>
      <td>3.619</td>
    </tr>
    <tr>
      <th>56858</th>
      <td>364</td>
      <td>2</td>
      <td>29</td>
      <td>NaN</td>
      <td>28344.000000</td>
      <td>416.320000</td>
      <td>0.660</td>
      <td>3.521</td>
      <td>-0.320</td>
      <td>3.601</td>
    </tr>
    <tr>
      <th>56859</th>
      <td>364</td>
      <td>2</td>
      <td>30</td>
      <td>NaN</td>
      <td>27576.000000</td>
      <td>416.160000</td>
      <td>0.583</td>
      <td>3.488</td>
      <td>-0.706</td>
      <td>3.611</td>
    </tr>
    <tr>
      <th>56860</th>
      <td>364</td>
      <td>2</td>
      <td>32</td>
      <td>NaN</td>
      <td>26501.000000</td>
      <td>413.100000</td>
      <td>0.564</td>
      <td>3.510</td>
      <td>-0.710</td>
      <td>3.629</td>
    </tr>
    <tr>
      <th>56861</th>
      <td>364</td>
      <td>2</td>
      <td>33</td>
      <td>NaN</td>
      <td>30461.000000</td>
      <td>416.710000</td>
      <td>0.645</td>
      <td>3.454</td>
      <td>-0.646</td>
      <td>3.577</td>
    </tr>
    <tr>
      <th>56862</th>
      <td>364</td>
      <td>2</td>
      <td>34</td>
      <td>NaN</td>
      <td>27484.000000</td>
      <td>415.140000</td>
      <td>0.583</td>
      <td>3.420</td>
      <td>-0.613</td>
      <td>3.524</td>
    </tr>
    <tr>
      <th>56863</th>
      <td>364</td>
      <td>2</td>
      <td>35</td>
      <td>NaN</td>
      <td>29194.000000</td>
      <td>415.390000</td>
      <td>0.571</td>
      <td>3.412</td>
      <td>-0.643</td>
      <td>3.520</td>
    </tr>
    <tr>
      <th>56864</th>
      <td>364</td>
      <td>2</td>
      <td>36</td>
      <td>NaN</td>
      <td>27653.000000</td>
      <td>414.770000</td>
      <td>0.593</td>
      <td>3.385</td>
      <td>-0.790</td>
      <td>3.528</td>
    </tr>
    <tr>
      <th>56865</th>
      <td>364</td>
      <td>2</td>
      <td>37</td>
      <td>NaN</td>
      <td>32162.000000</td>
      <td>415.250000</td>
      <td>0.583</td>
      <td>3.432</td>
      <td>-0.621</td>
      <td>3.545</td>
    </tr>
    <tr>
      <th>56866</th>
      <td>364</td>
      <td>2</td>
      <td>38</td>
      <td>NaN</td>
      <td>27395.000000</td>
      <td>412.940000</td>
      <td>0.258</td>
      <td>3.473</td>
      <td>-1.085</td>
      <td>3.659</td>
    </tr>
    <tr>
      <th>56867</th>
      <td>364</td>
      <td>2</td>
      <td>39</td>
      <td>NaN</td>
      <td>37120.000000</td>
      <td>416.780000</td>
      <td>0.629</td>
      <td>3.306</td>
      <td>-0.182</td>
      <td>3.395</td>
    </tr>
    <tr>
      <th>56868</th>
      <td>364</td>
      <td>2</td>
      <td>40</td>
      <td>NaN</td>
      <td>29925.000000</td>
      <td>413.100000</td>
      <td>0.571</td>
      <td>3.379</td>
      <td>-0.595</td>
      <td>3.483</td>
    </tr>
    <tr>
      <th>56869</th>
      <td>364</td>
      <td>2</td>
      <td>41</td>
      <td>NaN</td>
      <td>32587.000000</td>
      <td>413.040000</td>
      <td>0.519</td>
      <td>3.454</td>
      <td>-0.828</td>
      <td>3.596</td>
    </tr>
    <tr>
      <th>56870</th>
      <td>364</td>
      <td>2</td>
      <td>42</td>
      <td>NaN</td>
      <td>28279.000000</td>
      <td>412.030000</td>
      <td>0.416</td>
      <td>3.509</td>
      <td>-0.709</td>
      <td>3.609</td>
    </tr>
    <tr>
      <th>56871</th>
      <td>364</td>
      <td>2</td>
      <td>43</td>
      <td>NaN</td>
      <td>32215.000000</td>
      <td>410.100000</td>
      <td>0.281</td>
      <td>3.530</td>
      <td>-0.670</td>
      <td>3.607</td>
    </tr>
    <tr>
      <th>56872</th>
      <td>364</td>
      <td>2</td>
      <td>44</td>
      <td>NaN</td>
      <td>29360.000000</td>
      <td>410.470000</td>
      <td>0.321</td>
      <td>3.424</td>
      <td>-0.757</td>
      <td>3.525</td>
    </tr>
    <tr>
      <th>56873</th>
      <td>364</td>
      <td>2</td>
      <td>45</td>
      <td>NaN</td>
      <td>33108.000000</td>
      <td>406.590000</td>
      <td>0.145</td>
      <td>3.395</td>
      <td>-0.877</td>
      <td>3.522</td>
    </tr>
    <tr>
      <th>56874</th>
      <td>364</td>
      <td>2</td>
      <td>46</td>
      <td>NaN</td>
      <td>27604.000000</td>
      <td>408.960000</td>
      <td>-0.008</td>
      <td>3.332</td>
      <td>-0.924</td>
      <td>3.463</td>
    </tr>
    <tr>
      <th>56875</th>
      <td>364</td>
      <td>2</td>
      <td>48</td>
      <td>NaN</td>
      <td>32707.000000</td>
      <td>407.980000</td>
      <td>0.274</td>
      <td>3.309</td>
      <td>-0.957</td>
      <td>3.466</td>
    </tr>
    <tr>
      <th>56876</th>
      <td>364</td>
      <td>2</td>
      <td>49</td>
      <td>NaN</td>
      <td>27545.000000</td>
      <td>410.370000</td>
      <td>0.265</td>
      <td>3.317</td>
      <td>-0.934</td>
      <td>3.461</td>
    </tr>
    <tr>
      <th>61613</th>
      <td>364</td>
      <td>2</td>
      <td>50</td>
      <td>NaN</td>
      <td>42330.627329</td>
      <td>409.902963</td>
      <td>0.436</td>
      <td>3.332</td>
      <td>-0.971</td>
      <td>3.506</td>
    </tr>
    <tr>
      <th>56878</th>
      <td>364</td>
      <td>2</td>
      <td>51</td>
      <td>NaN</td>
      <td>29757.000000</td>
      <td>411.970000</td>
      <td>0.727</td>
      <td>3.229</td>
      <td>-0.932</td>
      <td>3.461</td>
    </tr>
    <tr>
      <th>56879</th>
      <td>364</td>
      <td>2</td>
      <td>52</td>
      <td>NaN</td>
      <td>28660.000000</td>
      <td>408.770000</td>
      <td>0.243</td>
      <td>3.013</td>
      <td>-1.150</td>
      <td>3.238</td>
    </tr>
    <tr>
      <th>56880</th>
      <td>364</td>
      <td>2</td>
      <td>53</td>
      <td>NaN</td>
      <td>37634.000000</td>
      <td>409.400000</td>
      <td>0.086</td>
      <td>2.949</td>
      <td>-1.017</td>
      <td>3.126</td>
    </tr>
    <tr>
      <th>56881</th>
      <td>364</td>
      <td>2</td>
      <td>54</td>
      <td>NaN</td>
      <td>31431.000000</td>
      <td>409.020000</td>
      <td>0.163</td>
      <td>2.886</td>
      <td>-0.926</td>
      <td>3.040</td>
    </tr>
    <tr>
      <th>56882</th>
      <td>364</td>
      <td>2</td>
      <td>55</td>
      <td>NaN</td>
      <td>35494.000000</td>
      <td>411.390000</td>
      <td>0.094</td>
      <td>2.953</td>
      <td>-0.854</td>
      <td>3.088</td>
    </tr>
    <tr>
      <th>56883</th>
      <td>364</td>
      <td>2</td>
      <td>56</td>
      <td>NaN</td>
      <td>35305.000000</td>
      <td>408.210000</td>
      <td>0.131</td>
      <td>2.723</td>
      <td>-1.118</td>
      <td>2.959</td>
    </tr>
    <tr>
      <th>56884</th>
      <td>364</td>
      <td>2</td>
      <td>57</td>
      <td>NaN</td>
      <td>37498.000000</td>
      <td>409.170000</td>
      <td>0.163</td>
      <td>2.825</td>
      <td>-0.812</td>
      <td>2.947</td>
    </tr>
    <tr>
      <th>56885</th>
      <td>364</td>
      <td>2</td>
      <td>58</td>
      <td>NaN</td>
      <td>39227.000000</td>
      <td>409.040000</td>
      <td>0.194</td>
      <td>2.555</td>
      <td>-0.782</td>
      <td>2.685</td>
    </tr>
    <tr>
      <th>56886</th>
      <td>364</td>
      <td>2</td>
      <td>59</td>
      <td>NaN</td>
      <td>46584.000000</td>
      <td>409.570000</td>
      <td>0.400</td>
      <td>2.076</td>
      <td>-0.659</td>
      <td>2.236</td>
    </tr>
  </tbody>
</table>
<p>16971 rows × 10 columns</p>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">3</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>nan</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">save</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">]</span>
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
      <th>doy</th>
      <th>h</th>
      <th>m</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bmag</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>338</th>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
      <td>59366.000000</td>
      <td>452.730000</td>
      <td>-3.826</td>
      <td>4.111</td>
      <td>-2.855</td>
      <td>6.463</td>
    </tr>
    <tr>
      <th>339</th>
      <td>3</td>
      <td>0</td>
      <td>1</td>
      <td>NaN</td>
      <td>59861.000000</td>
      <td>450.450000</td>
      <td>-5.057</td>
      <td>3.195</td>
      <td>-0.593</td>
      <td>6.326</td>
    </tr>
    <tr>
      <th>340</th>
      <td>3</td>
      <td>0</td>
      <td>2</td>
      <td>NaN</td>
      <td>92736.000000</td>
      <td>438.270000</td>
      <td>-6.259</td>
      <td>2.019</td>
      <td>0.158</td>
      <td>6.603</td>
    </tr>
    <tr>
      <th>341</th>
      <td>3</td>
      <td>0</td>
      <td>3</td>
      <td>NaN</td>
      <td>79804.000000</td>
      <td>437.360000</td>
      <td>-6.434</td>
      <td>1.758</td>
      <td>-0.190</td>
      <td>6.679</td>
    </tr>
    <tr>
      <th>342</th>
      <td>3</td>
      <td>0</td>
      <td>4</td>
      <td>NaN</td>
      <td>82479.000000</td>
      <td>438.230000</td>
      <td>-6.360</td>
      <td>2.070</td>
      <td>0.256</td>
      <td>6.694</td>
    </tr>
    <tr>
      <th>343</th>
      <td>3</td>
      <td>0</td>
      <td>5</td>
      <td>NaN</td>
      <td>82709.000000</td>
      <td>437.620000</td>
      <td>-6.408</td>
      <td>2.112</td>
      <td>0.590</td>
      <td>6.775</td>
    </tr>
    <tr>
      <th>344</th>
      <td>3</td>
      <td>0</td>
      <td>6</td>
      <td>NaN</td>
      <td>96446.000000</td>
      <td>441.400000</td>
      <td>-6.395</td>
      <td>2.311</td>
      <td>0.828</td>
      <td>6.859</td>
    </tr>
    <tr>
      <th>345</th>
      <td>3</td>
      <td>0</td>
      <td>7</td>
      <td>NaN</td>
      <td>82352.000000</td>
      <td>438.770000</td>
      <td>-5.987</td>
      <td>2.432</td>
      <td>0.584</td>
      <td>6.496</td>
    </tr>
    <tr>
      <th>346</th>
      <td>3</td>
      <td>0</td>
      <td>9</td>
      <td>NaN</td>
      <td>88905.000000</td>
      <td>438.820000</td>
      <td>-6.005</td>
      <td>2.462</td>
      <td>0.689</td>
      <td>6.535</td>
    </tr>
    <tr>
      <th>347</th>
      <td>3</td>
      <td>0</td>
      <td>10</td>
      <td>NaN</td>
      <td>79510.000000</td>
      <td>439.980000</td>
      <td>-6.090</td>
      <td>2.646</td>
      <td>1.134</td>
      <td>6.748</td>
    </tr>
    <tr>
      <th>348</th>
      <td>3</td>
      <td>0</td>
      <td>11</td>
      <td>NaN</td>
      <td>90796.000000</td>
      <td>440.440000</td>
      <td>-6.052</td>
      <td>2.362</td>
      <td>1.188</td>
      <td>6.617</td>
    </tr>
    <tr>
      <th>349</th>
      <td>3</td>
      <td>0</td>
      <td>12</td>
      <td>NaN</td>
      <td>86776.000000</td>
      <td>439.350000</td>
      <td>-5.981</td>
      <td>2.420</td>
      <td>1.489</td>
      <td>6.631</td>
    </tr>
    <tr>
      <th>57069</th>
      <td>3</td>
      <td>0</td>
      <td>13</td>
      <td>NaN</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.030</td>
      <td>2.542</td>
      <td>1.211</td>
      <td>6.676</td>
    </tr>
    <tr>
      <th>351</th>
      <td>3</td>
      <td>0</td>
      <td>14</td>
      <td>NaN</td>
      <td>87707.000000</td>
      <td>439.640000</td>
      <td>-6.109</td>
      <td>2.396</td>
      <td>1.142</td>
      <td>6.668</td>
    </tr>
    <tr>
      <th>352</th>
      <td>3</td>
      <td>0</td>
      <td>15</td>
      <td>NaN</td>
      <td>83140.000000</td>
      <td>439.610000</td>
      <td>-6.066</td>
      <td>2.689</td>
      <td>0.917</td>
      <td>6.712</td>
    </tr>
    <tr>
      <th>353</th>
      <td>3</td>
      <td>0</td>
      <td>16</td>
      <td>NaN</td>
      <td>85682.000000</td>
      <td>440.540000</td>
      <td>-6.152</td>
      <td>2.780</td>
      <td>0.813</td>
      <td>6.810</td>
    </tr>
    <tr>
      <th>354</th>
      <td>3</td>
      <td>0</td>
      <td>17</td>
      <td>NaN</td>
      <td>81383.000000</td>
      <td>439.740000</td>
      <td>-6.356</td>
      <td>2.428</td>
      <td>0.736</td>
      <td>6.860</td>
    </tr>
    <tr>
      <th>355</th>
      <td>3</td>
      <td>0</td>
      <td>18</td>
      <td>NaN</td>
      <td>79501.000000</td>
      <td>440.200000</td>
      <td>-6.132</td>
      <td>2.974</td>
      <td>0.717</td>
      <td>6.862</td>
    </tr>
    <tr>
      <th>356</th>
      <td>3</td>
      <td>0</td>
      <td>19</td>
      <td>NaN</td>
      <td>87859.000000</td>
      <td>438.020000</td>
      <td>-6.197</td>
      <td>2.892</td>
      <td>0.731</td>
      <td>6.885</td>
    </tr>
    <tr>
      <th>357</th>
      <td>3</td>
      <td>0</td>
      <td>20</td>
      <td>NaN</td>
      <td>75147.000000</td>
      <td>439.910000</td>
      <td>-5.973</td>
      <td>3.120</td>
      <td>1.139</td>
      <td>6.853</td>
    </tr>
    <tr>
      <th>358</th>
      <td>3</td>
      <td>0</td>
      <td>21</td>
      <td>NaN</td>
      <td>86375.000000</td>
      <td>440.690000</td>
      <td>-5.973</td>
      <td>2.947</td>
      <td>1.329</td>
      <td>6.800</td>
    </tr>
    <tr>
      <th>359</th>
      <td>3</td>
      <td>0</td>
      <td>22</td>
      <td>NaN</td>
      <td>76397.000000</td>
      <td>439.180000</td>
      <td>-6.105</td>
      <td>3.000</td>
      <td>0.830</td>
      <td>6.861</td>
    </tr>
    <tr>
      <th>360</th>
      <td>3</td>
      <td>0</td>
      <td>23</td>
      <td>NaN</td>
      <td>79685.000000</td>
      <td>439.020000</td>
      <td>-6.254</td>
      <td>3.035</td>
      <td>1.090</td>
      <td>7.055</td>
    </tr>
    <tr>
      <th>361</th>
      <td>3</td>
      <td>0</td>
      <td>25</td>
      <td>NaN</td>
      <td>73825.000000</td>
      <td>439.730000</td>
      <td>-6.365</td>
      <td>2.894</td>
      <td>1.791</td>
      <td>7.223</td>
    </tr>
    <tr>
      <th>362</th>
      <td>3</td>
      <td>0</td>
      <td>26</td>
      <td>NaN</td>
      <td>77347.000000</td>
      <td>442.140000</td>
      <td>-6.459</td>
      <td>2.996</td>
      <td>1.649</td>
      <td>7.314</td>
    </tr>
    <tr>
      <th>363</th>
      <td>3</td>
      <td>0</td>
      <td>27</td>
      <td>NaN</td>
      <td>100310.000000</td>
      <td>451.950000</td>
      <td>-5.911</td>
      <td>1.859</td>
      <td>3.383</td>
      <td>7.083</td>
    </tr>
    <tr>
      <th>364</th>
      <td>3</td>
      <td>0</td>
      <td>28</td>
      <td>NaN</td>
      <td>87121.000000</td>
      <td>452.600000</td>
      <td>-5.904</td>
      <td>2.047</td>
      <td>3.490</td>
      <td>7.170</td>
    </tr>
    <tr>
      <th>365</th>
      <td>3</td>
      <td>0</td>
      <td>29</td>
      <td>NaN</td>
      <td>82467.000000</td>
      <td>459.750000</td>
      <td>-5.811</td>
      <td>1.732</td>
      <td>3.758</td>
      <td>7.142</td>
    </tr>
    <tr>
      <th>366</th>
      <td>3</td>
      <td>0</td>
      <td>30</td>
      <td>NaN</td>
      <td>83171.000000</td>
      <td>461.000000</td>
      <td>-6.061</td>
      <td>2.072</td>
      <td>3.756</td>
      <td>7.429</td>
    </tr>
    <tr>
      <th>367</th>
      <td>3</td>
      <td>0</td>
      <td>31</td>
      <td>NaN</td>
      <td>84390.000000</td>
      <td>452.390000</td>
      <td>-6.309</td>
      <td>2.147</td>
      <td>3.882</td>
      <td>7.714</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>56857</th>
      <td>364</td>
      <td>2</td>
      <td>28</td>
      <td>NaN</td>
      <td>29838.000000</td>
      <td>417.310000</td>
      <td>0.644</td>
      <td>3.544</td>
      <td>-0.308</td>
      <td>3.619</td>
    </tr>
    <tr>
      <th>56858</th>
      <td>364</td>
      <td>2</td>
      <td>29</td>
      <td>NaN</td>
      <td>28344.000000</td>
      <td>416.320000</td>
      <td>0.660</td>
      <td>3.521</td>
      <td>-0.320</td>
      <td>3.601</td>
    </tr>
    <tr>
      <th>56859</th>
      <td>364</td>
      <td>2</td>
      <td>30</td>
      <td>NaN</td>
      <td>27576.000000</td>
      <td>416.160000</td>
      <td>0.583</td>
      <td>3.488</td>
      <td>-0.706</td>
      <td>3.611</td>
    </tr>
    <tr>
      <th>56860</th>
      <td>364</td>
      <td>2</td>
      <td>32</td>
      <td>NaN</td>
      <td>26501.000000</td>
      <td>413.100000</td>
      <td>0.564</td>
      <td>3.510</td>
      <td>-0.710</td>
      <td>3.629</td>
    </tr>
    <tr>
      <th>56861</th>
      <td>364</td>
      <td>2</td>
      <td>33</td>
      <td>NaN</td>
      <td>30461.000000</td>
      <td>416.710000</td>
      <td>0.645</td>
      <td>3.454</td>
      <td>-0.646</td>
      <td>3.577</td>
    </tr>
    <tr>
      <th>56862</th>
      <td>364</td>
      <td>2</td>
      <td>34</td>
      <td>NaN</td>
      <td>27484.000000</td>
      <td>415.140000</td>
      <td>0.583</td>
      <td>3.420</td>
      <td>-0.613</td>
      <td>3.524</td>
    </tr>
    <tr>
      <th>56863</th>
      <td>364</td>
      <td>2</td>
      <td>35</td>
      <td>NaN</td>
      <td>29194.000000</td>
      <td>415.390000</td>
      <td>0.571</td>
      <td>3.412</td>
      <td>-0.643</td>
      <td>3.520</td>
    </tr>
    <tr>
      <th>56864</th>
      <td>364</td>
      <td>2</td>
      <td>36</td>
      <td>NaN</td>
      <td>27653.000000</td>
      <td>414.770000</td>
      <td>0.593</td>
      <td>3.385</td>
      <td>-0.790</td>
      <td>3.528</td>
    </tr>
    <tr>
      <th>56865</th>
      <td>364</td>
      <td>2</td>
      <td>37</td>
      <td>NaN</td>
      <td>32162.000000</td>
      <td>415.250000</td>
      <td>0.583</td>
      <td>3.432</td>
      <td>-0.621</td>
      <td>3.545</td>
    </tr>
    <tr>
      <th>56866</th>
      <td>364</td>
      <td>2</td>
      <td>38</td>
      <td>NaN</td>
      <td>27395.000000</td>
      <td>412.940000</td>
      <td>0.258</td>
      <td>3.473</td>
      <td>-1.085</td>
      <td>3.659</td>
    </tr>
    <tr>
      <th>56867</th>
      <td>364</td>
      <td>2</td>
      <td>39</td>
      <td>NaN</td>
      <td>37120.000000</td>
      <td>416.780000</td>
      <td>0.629</td>
      <td>3.306</td>
      <td>-0.182</td>
      <td>3.395</td>
    </tr>
    <tr>
      <th>56868</th>
      <td>364</td>
      <td>2</td>
      <td>40</td>
      <td>NaN</td>
      <td>29925.000000</td>
      <td>413.100000</td>
      <td>0.571</td>
      <td>3.379</td>
      <td>-0.595</td>
      <td>3.483</td>
    </tr>
    <tr>
      <th>56869</th>
      <td>364</td>
      <td>2</td>
      <td>41</td>
      <td>NaN</td>
      <td>32587.000000</td>
      <td>413.040000</td>
      <td>0.519</td>
      <td>3.454</td>
      <td>-0.828</td>
      <td>3.596</td>
    </tr>
    <tr>
      <th>56870</th>
      <td>364</td>
      <td>2</td>
      <td>42</td>
      <td>NaN</td>
      <td>28279.000000</td>
      <td>412.030000</td>
      <td>0.416</td>
      <td>3.509</td>
      <td>-0.709</td>
      <td>3.609</td>
    </tr>
    <tr>
      <th>56871</th>
      <td>364</td>
      <td>2</td>
      <td>43</td>
      <td>NaN</td>
      <td>32215.000000</td>
      <td>410.100000</td>
      <td>0.281</td>
      <td>3.530</td>
      <td>-0.670</td>
      <td>3.607</td>
    </tr>
    <tr>
      <th>56872</th>
      <td>364</td>
      <td>2</td>
      <td>44</td>
      <td>NaN</td>
      <td>29360.000000</td>
      <td>410.470000</td>
      <td>0.321</td>
      <td>3.424</td>
      <td>-0.757</td>
      <td>3.525</td>
    </tr>
    <tr>
      <th>56873</th>
      <td>364</td>
      <td>2</td>
      <td>45</td>
      <td>NaN</td>
      <td>33108.000000</td>
      <td>406.590000</td>
      <td>0.145</td>
      <td>3.395</td>
      <td>-0.877</td>
      <td>3.522</td>
    </tr>
    <tr>
      <th>56874</th>
      <td>364</td>
      <td>2</td>
      <td>46</td>
      <td>NaN</td>
      <td>27604.000000</td>
      <td>408.960000</td>
      <td>-0.008</td>
      <td>3.332</td>
      <td>-0.924</td>
      <td>3.463</td>
    </tr>
    <tr>
      <th>56875</th>
      <td>364</td>
      <td>2</td>
      <td>48</td>
      <td>NaN</td>
      <td>32707.000000</td>
      <td>407.980000</td>
      <td>0.274</td>
      <td>3.309</td>
      <td>-0.957</td>
      <td>3.466</td>
    </tr>
    <tr>
      <th>56876</th>
      <td>364</td>
      <td>2</td>
      <td>49</td>
      <td>NaN</td>
      <td>27545.000000</td>
      <td>410.370000</td>
      <td>0.265</td>
      <td>3.317</td>
      <td>-0.934</td>
      <td>3.461</td>
    </tr>
    <tr>
      <th>61613</th>
      <td>364</td>
      <td>2</td>
      <td>50</td>
      <td>NaN</td>
      <td>42330.627329</td>
      <td>409.902963</td>
      <td>0.436</td>
      <td>3.332</td>
      <td>-0.971</td>
      <td>3.506</td>
    </tr>
    <tr>
      <th>56878</th>
      <td>364</td>
      <td>2</td>
      <td>51</td>
      <td>NaN</td>
      <td>29757.000000</td>
      <td>411.970000</td>
      <td>0.727</td>
      <td>3.229</td>
      <td>-0.932</td>
      <td>3.461</td>
    </tr>
    <tr>
      <th>56879</th>
      <td>364</td>
      <td>2</td>
      <td>52</td>
      <td>NaN</td>
      <td>28660.000000</td>
      <td>408.770000</td>
      <td>0.243</td>
      <td>3.013</td>
      <td>-1.150</td>
      <td>3.238</td>
    </tr>
    <tr>
      <th>56880</th>
      <td>364</td>
      <td>2</td>
      <td>53</td>
      <td>NaN</td>
      <td>37634.000000</td>
      <td>409.400000</td>
      <td>0.086</td>
      <td>2.949</td>
      <td>-1.017</td>
      <td>3.126</td>
    </tr>
    <tr>
      <th>56881</th>
      <td>364</td>
      <td>2</td>
      <td>54</td>
      <td>NaN</td>
      <td>31431.000000</td>
      <td>409.020000</td>
      <td>0.163</td>
      <td>2.886</td>
      <td>-0.926</td>
      <td>3.040</td>
    </tr>
    <tr>
      <th>56882</th>
      <td>364</td>
      <td>2</td>
      <td>55</td>
      <td>NaN</td>
      <td>35494.000000</td>
      <td>411.390000</td>
      <td>0.094</td>
      <td>2.953</td>
      <td>-0.854</td>
      <td>3.088</td>
    </tr>
    <tr>
      <th>56883</th>
      <td>364</td>
      <td>2</td>
      <td>56</td>
      <td>NaN</td>
      <td>35305.000000</td>
      <td>408.210000</td>
      <td>0.131</td>
      <td>2.723</td>
      <td>-1.118</td>
      <td>2.959</td>
    </tr>
    <tr>
      <th>56884</th>
      <td>364</td>
      <td>2</td>
      <td>57</td>
      <td>NaN</td>
      <td>37498.000000</td>
      <td>409.170000</td>
      <td>0.163</td>
      <td>2.825</td>
      <td>-0.812</td>
      <td>2.947</td>
    </tr>
    <tr>
      <th>56885</th>
      <td>364</td>
      <td>2</td>
      <td>58</td>
      <td>NaN</td>
      <td>39227.000000</td>
      <td>409.040000</td>
      <td>0.194</td>
      <td>2.555</td>
      <td>-0.782</td>
      <td>2.685</td>
    </tr>
    <tr>
      <th>56886</th>
      <td>364</td>
      <td>2</td>
      <td>59</td>
      <td>NaN</td>
      <td>46584.000000</td>
      <td>409.570000</td>
      <td>0.400</td>
      <td>2.076</td>
      <td>-0.659</td>
      <td>2.236</td>
    </tr>
  </tbody>
</table>
<p>16971 rows × 10 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="test-set-mean-&#51060;&#45208;-sum-&#54616;&#44592;">test set mean &#51060;&#45208; sum &#54616;&#44592;<a class="anchor-link" href="#test-set-mean-&#51060;&#45208;-sum-&#54616;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#mean</span>
<span class="n">df3</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bmag&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>NaN</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">1000</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#sum</span>
<span class="n">df3</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bmag&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>217.794425</td>
      <td>5.533541e+06</td>
      <td>74881.110982</td>
      <td>869.057</td>
      <td>336.089</td>
      <td>-2182.466</td>
      <td>2390.221</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>676.577151</td>
      <td>5.897397e+06</td>
      <td>74089.714049</td>
      <td>829.803</td>
      <td>-935.962</td>
      <td>-200.736</td>
      <td>1395.586</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>0.000000</td>
      <td>1.371506e+07</td>
      <td>73931.978634</td>
      <td>-1112.269</td>
      <td>409.508</td>
      <td>354.656</td>
      <td>1272.085</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>467.164286</td>
      <td>1.432586e+07</td>
      <td>70844.372284</td>
      <td>-589.733</td>
      <td>308.870</td>
      <td>-25.313</td>
      <td>688.801</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>1219.295391</td>
      <td>1.266501e+07</td>
      <td>70891.736380</td>
      <td>-600.787</td>
      <td>412.239</td>
      <td>440.074</td>
      <td>1025.687</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>0.0</td>
      <td>1.371506e+07</td>
      <td>73931.978634</td>
      <td>-1112.269</td>
      <td>409.508</td>
      <td>354.656</td>
      <td>1272.085</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>0.0</td>
      <td>2.988923e+07</td>
      <td>94635.701063</td>
      <td>-604.797</td>
      <td>491.522</td>
      <td>-64.543</td>
      <td>1235.067</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>0.0</td>
      <td>2.158755e+07</td>
      <td>93774.991235</td>
      <td>-682.792</td>
      <td>34.445</td>
      <td>-407.676</td>
      <td>1064.679</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12</td>
      <td>0.0</td>
      <td>3.171027e+07</td>
      <td>46586.768125</td>
      <td>286.537</td>
      <td>-291.887</td>
      <td>124.226</td>
      <td>557.122</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13</td>
      <td>0.0</td>
      <td>1.979536e+07</td>
      <td>47427.983974</td>
      <td>174.531</td>
      <td>-391.490</td>
      <td>-181.347</td>
      <td>641.269</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14</td>
      <td>0.0</td>
      <td>9.567982e+06</td>
      <td>43201.951250</td>
      <td>388.516</td>
      <td>-10.044</td>
      <td>74.240</td>
      <td>494.982</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15</td>
      <td>0.0</td>
      <td>5.332352e+06</td>
      <td>36983.676220</td>
      <td>244.901</td>
      <td>-115.947</td>
      <td>-139.448</td>
      <td>366.327</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16</td>
      <td>0.0</td>
      <td>2.775153e+06</td>
      <td>31075.405000</td>
      <td>388.521</td>
      <td>-77.908</td>
      <td>-24.577</td>
      <td>418.749</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17</td>
      <td>0.0</td>
      <td>1.647476e+06</td>
      <td>28665.200617</td>
      <td>-292.104</td>
      <td>-444.841</td>
      <td>197.823</td>
      <td>576.742</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18</td>
      <td>0.0</td>
      <td>3.189744e+06</td>
      <td>26747.925926</td>
      <td>-176.660</td>
      <td>112.388</td>
      <td>131.719</td>
      <td>312.675</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19</td>
      <td>0.0</td>
      <td>7.465628e+06</td>
      <td>30791.137349</td>
      <td>-277.455</td>
      <td>-317.275</td>
      <td>-429.635</td>
      <td>762.819</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20</td>
      <td>0.0</td>
      <td>0.000000e+00</td>
      <td>32461.212838</td>
      <td>957.173</td>
      <td>604.841</td>
      <td>653.067</td>
      <td>1350.962</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21</td>
      <td>0.0</td>
      <td>1.050623e+07</td>
      <td>32830.580625</td>
      <td>239.824</td>
      <td>-1009.159</td>
      <td>-275.383</td>
      <td>1291.914</td>
    </tr>
    <tr>
      <th>21</th>
      <td>22</td>
      <td>0.0</td>
      <td>1.507883e+07</td>
      <td>44996.004268</td>
      <td>219.896</td>
      <td>-121.593</td>
      <td>160.880</td>
      <td>505.792</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23</td>
      <td>0.0</td>
      <td>7.045712e+06</td>
      <td>40634.478049</td>
      <td>497.653</td>
      <td>-173.721</td>
      <td>31.602</td>
      <td>593.028</td>
    </tr>
    <tr>
      <th>27</th>
      <td>28</td>
      <td>0.0</td>
      <td>2.203069e+06</td>
      <td>29148.137805</td>
      <td>-364.081</td>
      <td>430.499</td>
      <td>352.825</td>
      <td>678.047</td>
    </tr>
    <tr>
      <th>28</th>
      <td>29</td>
      <td>0.0</td>
      <td>2.415973e+06</td>
      <td>28272.813333</td>
      <td>-132.421</td>
      <td>428.159</td>
      <td>81.658</td>
      <td>480.045</td>
    </tr>
    <tr>
      <th>29</th>
      <td>30</td>
      <td>0.0</td>
      <td>1.009378e+06</td>
      <td>24285.435000</td>
      <td>-125.686</td>
      <td>146.871</td>
      <td>9.938</td>
      <td>239.183</td>
    </tr>
    <tr>
      <th>30</th>
      <td>31</td>
      <td>0.0</td>
      <td>9.884652e+05</td>
      <td>23703.535366</td>
      <td>119.308</td>
      <td>530.152</td>
      <td>-182.150</td>
      <td>587.937</td>
    </tr>
    <tr>
      <th>31</th>
      <td>32</td>
      <td>0.0</td>
      <td>2.544989e+06</td>
      <td>25472.707831</td>
      <td>459.242</td>
      <td>386.129</td>
      <td>-416.408</td>
      <td>742.891</td>
    </tr>
    <tr>
      <th>32</th>
      <td>33</td>
      <td>0.0</td>
      <td>1.465002e+06</td>
      <td>22478.354938</td>
      <td>24.294</td>
      <td>-197.442</td>
      <td>-97.325</td>
      <td>457.063</td>
    </tr>
    <tr>
      <th>33</th>
      <td>34</td>
      <td>0.0</td>
      <td>0.000000e+00</td>
      <td>30447.207317</td>
      <td>-437.774</td>
      <td>70.481</td>
      <td>-601.429</td>
      <td>779.713</td>
    </tr>
    <tr>
      <th>34</th>
      <td>35</td>
      <td>0.0</td>
      <td>4.227184e+06</td>
      <td>33706.405696</td>
      <td>-273.769</td>
      <td>400.603</td>
      <td>359.338</td>
      <td>638.397</td>
    </tr>
    <tr>
      <th>35</th>
      <td>36</td>
      <td>0.0</td>
      <td>8.008113e+06</td>
      <td>38159.732237</td>
      <td>-346.786</td>
      <td>487.162</td>
      <td>175.170</td>
      <td>817.759</td>
    </tr>
    <tr>
      <th>36</th>
      <td>37</td>
      <td>0.0</td>
      <td>6.170696e+06</td>
      <td>39521.316667</td>
      <td>-207.069</td>
      <td>62.535</td>
      <td>-128.702</td>
      <td>342.641</td>
    </tr>
    <tr>
      <th>40</th>
      <td>41</td>
      <td>0.0</td>
      <td>2.464846e+06</td>
      <td>32850.088125</td>
      <td>196.576</td>
      <td>-300.446</td>
      <td>-163.300</td>
      <td>416.245</td>
    </tr>
    <tr>
      <th>41</th>
      <td>42</td>
      <td>0.0</td>
      <td>6.448296e+05</td>
      <td>27588.800625</td>
      <td>119.289</td>
      <td>103.049</td>
      <td>-313.981</td>
      <td>354.557</td>
    </tr>
    <tr>
      <th>42</th>
      <td>43</td>
      <td>0.0</td>
      <td>2.531765e+06</td>
      <td>29813.580000</td>
      <td>437.017</td>
      <td>-941.355</td>
      <td>-374.782</td>
      <td>1159.760</td>
    </tr>
    <tr>
      <th>43</th>
      <td>44</td>
      <td>0.0</td>
      <td>4.885861e+06</td>
      <td>30949.966250</td>
      <td>-66.303</td>
      <td>7.663</td>
      <td>1156.443</td>
      <td>1302.322</td>
    </tr>
    <tr>
      <th>44</th>
      <td>45</td>
      <td>0.0</td>
      <td>5.465709e+06</td>
      <td>33994.763580</td>
      <td>-343.477</td>
      <td>111.274</td>
      <td>50.044</td>
      <td>486.570</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>233</th>
      <td>234</td>
      <td>0.0</td>
      <td>5.586842e+06</td>
      <td>49612.133503</td>
      <td>483.188</td>
      <td>-799.588</td>
      <td>274.486</td>
      <td>986.709</td>
    </tr>
    <tr>
      <th>234</th>
      <td>235</td>
      <td>0.0</td>
      <td>1.893594e+07</td>
      <td>68976.790675</td>
      <td>265.921</td>
      <td>-391.126</td>
      <td>-10.227</td>
      <td>921.436</td>
    </tr>
    <tr>
      <th>255</th>
      <td>256</td>
      <td>0.0</td>
      <td>5.039351e+06</td>
      <td>55922.034000</td>
      <td>-533.533</td>
      <td>-1111.497</td>
      <td>78.942</td>
      <td>1317.578</td>
    </tr>
    <tr>
      <th>256</th>
      <td>257</td>
      <td>0.0</td>
      <td>3.352263e+06</td>
      <td>49065.416296</td>
      <td>220.179</td>
      <td>950.057</td>
      <td>-526.810</td>
      <td>1128.175</td>
    </tr>
    <tr>
      <th>257</th>
      <td>258</td>
      <td>0.0</td>
      <td>4.430421e+06</td>
      <td>45539.530435</td>
      <td>-518.687</td>
      <td>419.513</td>
      <td>-328.181</td>
      <td>869.728</td>
    </tr>
    <tr>
      <th>258</th>
      <td>259</td>
      <td>0.0</td>
      <td>4.860240e+06</td>
      <td>52197.664615</td>
      <td>-661.195</td>
      <td>816.983</td>
      <td>-919.098</td>
      <td>1503.276</td>
    </tr>
    <tr>
      <th>259</th>
      <td>260</td>
      <td>0.0</td>
      <td>7.022308e+06</td>
      <td>51791.594043</td>
      <td>798.757</td>
      <td>-532.958</td>
      <td>549.565</td>
      <td>1219.120</td>
    </tr>
    <tr>
      <th>260</th>
      <td>261</td>
      <td>0.0</td>
      <td>5.807951e+06</td>
      <td>53328.404908</td>
      <td>232.253</td>
      <td>-340.322</td>
      <td>376.868</td>
      <td>954.384</td>
    </tr>
    <tr>
      <th>261</th>
      <td>262</td>
      <td>0.0</td>
      <td>8.094774e+06</td>
      <td>52929.323444</td>
      <td>684.527</td>
      <td>-313.239</td>
      <td>188.509</td>
      <td>903.145</td>
    </tr>
    <tr>
      <th>265</th>
      <td>266</td>
      <td>0.0</td>
      <td>1.969428e+07</td>
      <td>84722.505000</td>
      <td>550.941</td>
      <td>-232.849</td>
      <td>488.656</td>
      <td>938.724</td>
    </tr>
    <tr>
      <th>275</th>
      <td>276</td>
      <td>0.0</td>
      <td>1.872957e+07</td>
      <td>86909.914601</td>
      <td>-364.275</td>
      <td>335.828</td>
      <td>-75.630</td>
      <td>814.723</td>
    </tr>
    <tr>
      <th>282</th>
      <td>283</td>
      <td>0.0</td>
      <td>5.548380e+06</td>
      <td>61285.325432</td>
      <td>-413.729</td>
      <td>415.540</td>
      <td>-163.899</td>
      <td>648.212</td>
    </tr>
    <tr>
      <th>292</th>
      <td>293</td>
      <td>0.0</td>
      <td>1.796583e+07</td>
      <td>95494.545370</td>
      <td>486.200</td>
      <td>-263.107</td>
      <td>49.983</td>
      <td>665.841</td>
    </tr>
    <tr>
      <th>298</th>
      <td>299</td>
      <td>0.0</td>
      <td>1.047566e+07</td>
      <td>67652.883354</td>
      <td>39.272</td>
      <td>700.959</td>
      <td>-565.691</td>
      <td>1275.509</td>
    </tr>
    <tr>
      <th>311</th>
      <td>312</td>
      <td>0.0</td>
      <td>1.835131e+06</td>
      <td>50579.087239</td>
      <td>-469.391</td>
      <td>-14.322</td>
      <td>-313.689</td>
      <td>582.708</td>
    </tr>
    <tr>
      <th>312</th>
      <td>313</td>
      <td>0.0</td>
      <td>5.305760e+06</td>
      <td>50145.289116</td>
      <td>103.957</td>
      <td>-434.678</td>
      <td>43.277</td>
      <td>555.947</td>
    </tr>
    <tr>
      <th>313</th>
      <td>314</td>
      <td>0.0</td>
      <td>2.596513e+06</td>
      <td>49257.590184</td>
      <td>13.161</td>
      <td>-417.257</td>
      <td>65.528</td>
      <td>526.419</td>
    </tr>
    <tr>
      <th>314</th>
      <td>315</td>
      <td>0.0</td>
      <td>3.841230e+06</td>
      <td>58122.275478</td>
      <td>-1.316</td>
      <td>946.998</td>
      <td>1365.150</td>
      <td>1909.643</td>
    </tr>
    <tr>
      <th>316</th>
      <td>317</td>
      <td>0.0</td>
      <td>2.843954e+07</td>
      <td>73762.182897</td>
      <td>1669.013</td>
      <td>-1009.021</td>
      <td>960.172</td>
      <td>2361.385</td>
    </tr>
    <tr>
      <th>320</th>
      <td>321</td>
      <td>0.0</td>
      <td>1.372545e+07</td>
      <td>77913.245864</td>
      <td>477.191</td>
      <td>-283.691</td>
      <td>9.440</td>
      <td>597.759</td>
    </tr>
    <tr>
      <th>323</th>
      <td>324</td>
      <td>0.0</td>
      <td>0.000000e+00</td>
      <td>55330.287834</td>
      <td>612.456</td>
      <td>-339.618</td>
      <td>66.112</td>
      <td>719.476</td>
    </tr>
    <tr>
      <th>324</th>
      <td>325</td>
      <td>0.0</td>
      <td>3.681787e+06</td>
      <td>53988.086810</td>
      <td>189.764</td>
      <td>-193.610</td>
      <td>67.561</td>
      <td>464.898</td>
    </tr>
    <tr>
      <th>326</th>
      <td>327</td>
      <td>0.0</td>
      <td>8.772700e+06</td>
      <td>57788.668261</td>
      <td>-688.410</td>
      <td>1049.346</td>
      <td>420.366</td>
      <td>1524.938</td>
    </tr>
    <tr>
      <th>329</th>
      <td>330</td>
      <td>0.0</td>
      <td>4.650420e+07</td>
      <td>91760.475316</td>
      <td>-1203.825</td>
      <td>884.641</td>
      <td>-99.875</td>
      <td>1676.615</td>
    </tr>
    <tr>
      <th>337</th>
      <td>338</td>
      <td>0.0</td>
      <td>4.786155e+06</td>
      <td>52344.051132</td>
      <td>-367.413</td>
      <td>232.335</td>
      <td>-120.487</td>
      <td>466.029</td>
    </tr>
    <tr>
      <th>338</th>
      <td>339</td>
      <td>0.0</td>
      <td>1.870788e+06</td>
      <td>49414.459509</td>
      <td>397.133</td>
      <td>52.729</td>
      <td>-158.700</td>
      <td>447.295</td>
    </tr>
    <tr>
      <th>339</th>
      <td>340</td>
      <td>0.0</td>
      <td>2.811727e+06</td>
      <td>47631.456437</td>
      <td>74.307</td>
      <td>391.900</td>
      <td>269.536</td>
      <td>1035.190</td>
    </tr>
    <tr>
      <th>341</th>
      <td>342</td>
      <td>0.0</td>
      <td>7.127826e+06</td>
      <td>57282.174444</td>
      <td>-249.049</td>
      <td>881.894</td>
      <td>100.139</td>
      <td>1070.093</td>
    </tr>
    <tr>
      <th>353</th>
      <td>354</td>
      <td>0.0</td>
      <td>6.842863e+06</td>
      <td>61400.375833</td>
      <td>-481.614</td>
      <td>862.374</td>
      <td>90.708</td>
      <td>1138.862</td>
    </tr>
    <tr>
      <th>363</th>
      <td>364</td>
      <td>0.0</td>
      <td>7.153876e+06</td>
      <td>69273.600741</td>
      <td>-74.593</td>
      <td>355.787</td>
      <td>-180.534</td>
      <td>528.685</td>
    </tr>
  </tbody>
</table>
<p>121 rows × 8 columns</p>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#test set save</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted0.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted3.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted6.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted9.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>

<span class="n">df3</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted12.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted15.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted18.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted21.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted0.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted3.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted6.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted9.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>

<span class="n">df3</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted12.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted15.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted18.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted21.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.288724</td>
      <td>32742.846626</td>
      <td>443.083497</td>
      <td>5.142349</td>
      <td>1.988692</td>
      <td>-12.914000</td>
      <td>14.143320</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.003415</td>
      <td>34895.839506</td>
      <td>438.400675</td>
      <td>4.910077</td>
      <td>-5.538237</td>
      <td>-1.187787</td>
      <td>8.257905</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>NaN</td>
      <td>81154.173913</td>
      <td>437.467329</td>
      <td>-6.581473</td>
      <td>2.423124</td>
      <td>2.098556</td>
      <td>7.527130</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2.764286</td>
      <td>84768.413580</td>
      <td>419.197469</td>
      <td>-3.489544</td>
      <td>1.827633</td>
      <td>-0.149781</td>
      <td>4.075746</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>7.214766</td>
      <td>74940.906832</td>
      <td>419.477730</td>
      <td>-3.554953</td>
      <td>2.439284</td>
      <td>2.603988</td>
      <td>6.069154</td>
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
<h1 id="Nan&#44050;-&#52286;&#44592;-&#48143;-&#51228;&#44144;">Nan&#44050; &#52286;&#44592; &#48143; &#51228;&#44144;<a class="anchor-link" href="#Nan&#44050;-&#52286;&#44592;-&#48143;-&#51228;&#44144;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>
<span class="n">Vp</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Tp</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Np</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="n">Vp</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp0.pkl&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp1.pkl&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp2.pkl&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp3.pkl&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp4.pkl&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp5.pkl&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp6.pkl&#39;</span><span class="p">)</span>
<span class="n">Vp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp7.pkl&#39;</span><span class="p">)</span>

<span class="n">Tp</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp0.pkl&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp1.pkl&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp2.pkl&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp3.pkl&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp4.pkl&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp5.pkl&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp6.pkl&#39;</span><span class="p">)</span>
<span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp7.pkl&#39;</span><span class="p">)</span>

<span class="n">Np</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np0.pkl&#39;</span><span class="p">)</span>
<span class="n">Np</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np1.pkl&#39;</span><span class="p">)</span>
<span class="n">Np</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np2.pkl&#39;</span><span class="p">)</span>
<span class="n">Np</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np3.pkl&#39;</span><span class="p">)</span>
<span class="n">Np</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np4.pkl&#39;</span><span class="p">)</span>
<span class="n">Np</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np5.pkl&#39;</span><span class="p">)</span>
<span class="n">Np</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np6.pkl&#39;</span><span class="p">)</span>
<span class="n">Np</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np7.pkl&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>
<span class="n">Vp</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Tp</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Np</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">Vp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_P_nan_model/Vp&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
  <span class="n">Tp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_P_nan_model/Tp&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
  <span class="n">Np</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/new_P_nan_model/Np&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;Bmag&#39;</span><span class="p">:</span><span class="s1">&#39;Bt&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">:</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">:</span><span class="s1">&#39;min&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
  <span class="nb">print</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
Empty DataFrame
Columns: [doy, hr, min, Np, Tp, Vp, B_gsm_x, B_gsm_y, B_gsm_z, Bt]
Index: []
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">]:</span>
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
    <span class="n">x_test</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">][[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">]]</span>
    <span class="k">if</span> <span class="n">x_test</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">:</span>
      <span class="k">continue</span>
    <span class="n">check</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=-</span><span class="mi">9998</span><span class="p">]</span>
    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">x_test</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    
    <span class="k">if</span> <span class="n">col</span><span class="o">==</span><span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">check</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Vp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
    
    <span class="k">elif</span> <span class="n">col</span><span class="o">==</span><span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="n">check</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Tp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
      
    <span class="k">else</span><span class="p">:</span>
      <span class="n">check</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">Np</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
      
    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">check</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;h&#39;</span><span class="p">,</span><span class="s1">&#39;m&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39; &#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39; 번째 done&#39;</span><span class="p">)</span>
  
    
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">bb</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">]:</span>
  <span class="k">for</span> <span class="n">aa</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>

    <span class="n">bb</span><span class="o">=</span><span class="s1">&#39;Np&#39;</span>
    <span class="c1">#x_test=df3[aa][df3[aa][bb].isnull()==True]</span>
    <span class="n">x_test</span><span class="o">=</span><span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
    <span class="k">if</span> <span class="n">x_test</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">:</span>
      <span class="k">continue</span>
    <span class="n">y_test</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="n">bb</span><span class="p">]</span>
    <span class="c1">#원상복귀를 위한 check dataframe 선언</span>
    <span class="n">check</span><span class="o">=</span><span class="n">x_test</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
    <span class="k">if</span> <span class="n">bb</span><span class="o">==</span><span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="n">bb</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">bb</span><span class="o">==</span><span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="n">bb</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="k">else</span> <span class="p">:</span>
      <span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="n">bb</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    
    <span class="n">df4</span><span class="o">=</span><span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">!=</span><span class="mi">0</span><span class="p">]</span>
    <span class="c1">#df4=df3[aa][df3[aa][bb].isnull()==False]</span>




    <span class="n">y_pred</span><span class="o">=</span><span class="n">Vp</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
    
    <span class="n">check</span><span class="p">[</span><span class="n">bb</span><span class="p">]</span><span class="o">=</span><span class="n">y_pred</span>
    <span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df4</span><span class="p">,</span><span class="n">check</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;doy&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">df3</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
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
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  errors=errors)
/usr/local/lib/python3.6/dist-packages/pandas/core/frame.py:3940: SettingWithCopyWarning: 
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#save no_nan_test_set</span>

<span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test0.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test1.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test2.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test3.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>

<span class="n">df3</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test4.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test5.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test6.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">df3</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/no_nan_test_sum/no_nan_9999_test7.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>doy        False
Np         False
Tp         False
Vp         False
B_gsm_x    False
B_gsm_y    False
B_gsm_z    False
Bt         False
dtype: bool</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="test-&#50696;&#52769;&#54616;&#50668;-frame&#54868;">test &#50696;&#52769;&#54616;&#50668; frame&#54868;<a class="anchor-link" href="#test-&#50696;&#52769;&#54616;&#50668;-frame&#54868;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">df2</span><span class="o">=</span><span class="p">[</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="o">=</span><span class="p">[[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">)]</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">60</span><span class="p">)</span><span class="o">|</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">335</span><span class="p">)]</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">60</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">150</span><span class="p">)]</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">150</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">240</span><span class="p">)]</span>
  <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">240</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">335</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>
<span class="sd">&#39;&#39;&#39;model = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;)  </span>
<span class="sd">model2 = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;) </span>
<span class="sd">model3 = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;) </span>
<span class="sd">model4 = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;) </span>

<span class="sd">model5 = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;) </span>
<span class="sd">model6 = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;) </span>
<span class="sd">model7 = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;) </span>
<span class="sd">model8 = joblib.load(&#39;/content/drive/My Drive/sun_wind/empty_model/no_nan_mean.pkl&#39;) &#39;&#39;&#39;</span>
<span class="n">models</span><span class="o">=</span><span class="p">[[</span><span class="n">j</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">)]</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
    <span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/model6/no_nan_mean&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">):</span>
    <span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">][</span><span class="s1">&#39;pred&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">])</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">0</span><span class="p">],</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">1</span><span class="p">],</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">2</span><span class="p">],</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="mi">3</span><span class="p">]],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">df3</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;pred&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">models</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>
<span class="n">model</span><span class="o">=</span><span class="p">[</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/final_model2/model&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.pkl&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">kp_0h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
<span class="n">kp_3h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span>
<span class="n">kp_6h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">2</span><span class="p">])</span>
<span class="n">kp_9h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">3</span><span class="p">])</span>

<span class="n">kp_12h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">4</span><span class="p">])</span>
<span class="n">kp_15h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">5</span><span class="p">])</span>
<span class="n">kp_18h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">6</span><span class="p">])</span>
<span class="n">kp_21h</span><span class="o">=</span><span class="n">model</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">df3</span><span class="p">[</span><span class="mi">7</span><span class="p">])</span>

<span class="c1">#regression으로 모델링 했을 경우 (왜냐하면 연속적인 값을 허용하지 않음)</span>
<span class="n">kp_0h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_0h</span><span class="p">)</span>
<span class="n">kp_3h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_3h</span><span class="p">)</span>
<span class="n">kp_6h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_6h</span><span class="p">)</span>
<span class="n">kp_9h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_9h</span><span class="p">)</span>

<span class="n">kp_12h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_12h</span><span class="p">)</span>
<span class="n">kp_15h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_15h</span><span class="p">)</span>
<span class="n">kp_18h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_18h</span><span class="p">)</span>
<span class="n">kp_21h</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">kp_21h</span><span class="p">)</span>

<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">#multi class로 모델링 했을 경우</span>
<span class="sd">kp_0h=[np.argmax(kp_0h[i]) for i in range(len(kp_0h))]</span>
<span class="sd">kp_3h=[np.argmax(kp_3h[i]) for i in range(len(kp_3h))]</span>
<span class="sd">kp_6h=[np.argmax(kp_6h[i]) for i in range(len(kp_6h))]</span>
<span class="sd">kp_9h=[np.argmax(kp_9h[i]) for i in range(len(kp_9h))]</span>

<span class="sd">kp_12h=[np.argmax(kp_12h[i]) for i in range(len(kp_12h))]</span>
<span class="sd">kp_15h=[np.argmax(kp_15h[i]) for i in range(len(kp_15h))]</span>
<span class="sd">kp_18h=[np.argmax(kp_18h[i]) for i in range(len(kp_18h))]</span>
<span class="sd">kp_21h=[np.argmax(kp_21h[i]) for i in range(len(kp_21h))]</span>
<span class="sd">&#39;&#39;&#39;</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&#39;\n#multi class로 모델링 했을 경우\nkp_0h=[np.argmax(kp_0h[i]) for i in range(len(kp_0h))]\nkp_3h=[np.argmax(kp_3h[i]) for i in range(len(kp_3h))]\nkp_6h=[np.argmax(kp_6h[i]) for i in range(len(kp_6h))]\nkp_9h=[np.argmax(kp_9h[i]) for i in range(len(kp_9h))]\n\nkp_12h=[np.argmax(kp_12h[i]) for i in range(len(kp_12h))]\nkp_15h=[np.argmax(kp_15h[i]) for i in range(len(kp_15h))]\nkp_18h=[np.argmax(kp_18h[i]) for i in range(len(kp_18h))]\nkp_21h=[np.argmax(kp_21h[i]) for i in range(len(kp_21h))]\n&#39;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_0h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_0h</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_3h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_3h</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_6h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_6h</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_9h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_9h</span>

<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_12h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_12h</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_15h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_15h</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_18h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_18h</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_21h&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">kp_21h</span>
<span class="n">submit</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">submit</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;index&#39;</span><span class="p">:</span><span class="s1">&#39;doy&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">submit</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">+=</span><span class="mi">1</span>
<span class="n">submit</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
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
      <td>1</td>
      <td>5.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># save submit</span>
<span class="n">submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/submit/final3.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
      <th>doy</th>
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
      <th>count</th>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>183.000000</td>
      <td>2.065753</td>
      <td>2.016438</td>
      <td>1.969863</td>
      <td>1.994521</td>
      <td>2.161644</td>
      <td>2.194521</td>
      <td>2.128767</td>
      <td>2.153425</td>
    </tr>
    <tr>
      <th>std</th>
      <td>105.510663</td>
      <td>1.072152</td>
      <td>1.133774</td>
      <td>1.179808</td>
      <td>1.116791</td>
      <td>1.012915</td>
      <td>0.894410</td>
      <td>0.939002</td>
      <td>0.879261</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>92.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>183.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>274.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>365.000000</td>
      <td>5.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
      <th>doy</th>
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
      <th>count</th>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>183.000000</td>
      <td>2.057534</td>
      <td>1.989041</td>
      <td>1.986301</td>
      <td>2.000000</td>
      <td>2.128767</td>
      <td>2.200000</td>
      <td>2.147945</td>
      <td>2.161644</td>
    </tr>
    <tr>
      <th>std</th>
      <td>105.510663</td>
      <td>1.094180</td>
      <td>1.126548</td>
      <td>1.180114</td>
      <td>1.104437</td>
      <td>1.017630</td>
      <td>0.944039</td>
      <td>0.960785</td>
      <td>0.894831</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>92.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>183.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>274.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>365.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>5.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>5.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/submit/submit_no_nan_sum.csv&#39;</span><span class="p">)</span>
<span class="n">submit2</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/submit/submit_no_nan.csv&#39;</span><span class="p">)</span>
<span class="n">submit2</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">submit3</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/submit/submit_all_9999_no_year.csv&#39;</span><span class="p">)</span>
<span class="n">submit3</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
      <th>doy</th>
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
      <th>count</th>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>183.000000</td>
      <td>4.756164</td>
      <td>4.731507</td>
      <td>4.687671</td>
      <td>4.756164</td>
      <td>4.731507</td>
      <td>4.723288</td>
      <td>4.742466</td>
      <td>4.736986</td>
    </tr>
    <tr>
      <th>std</th>
      <td>105.510663</td>
      <td>0.894579</td>
      <td>0.904336</td>
      <td>0.905409</td>
      <td>0.894579</td>
      <td>0.892102</td>
      <td>0.947890</td>
      <td>0.963327</td>
      <td>0.938714</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>92.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>183.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>274.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
      <td>5.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>365.000000</td>
      <td>7.000000</td>
      <td>7.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>9.000000</td>
      <td>8.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit2</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
      <th>doy</th>
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
      <th>count</th>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>183.000000</td>
      <td>3.635616</td>
      <td>3.805479</td>
      <td>3.630137</td>
      <td>3.495890</td>
      <td>3.575342</td>
      <td>3.369863</td>
      <td>3.345205</td>
      <td>3.690411</td>
    </tr>
    <tr>
      <th>std</th>
      <td>105.510663</td>
      <td>0.700347</td>
      <td>0.803818</td>
      <td>0.796746</td>
      <td>0.814099</td>
      <td>0.786525</td>
      <td>0.846889</td>
      <td>0.774781</td>
      <td>0.703243</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>92.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>183.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>3.000000</td>
      <td>4.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>274.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>365.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
      <td>6.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit3</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
      <th>doy</th>
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
      <th>count</th>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
      <td>365.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>183.000000</td>
      <td>3.786301</td>
      <td>3.810959</td>
      <td>3.821918</td>
      <td>3.838356</td>
      <td>3.846575</td>
      <td>3.857534</td>
      <td>3.857534</td>
      <td>3.852055</td>
    </tr>
    <tr>
      <th>std</th>
      <td>105.510663</td>
      <td>0.891553</td>
      <td>0.922783</td>
      <td>0.927931</td>
      <td>0.885573</td>
      <td>0.936747</td>
      <td>0.961615</td>
      <td>0.955884</td>
      <td>0.952168</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>92.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>183.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>274.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>365.000000</td>
      <td>8.000000</td>
      <td>7.000000</td>
      <td>7.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test/test.csv&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/frame_train/ace_1999.csv&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="p">[</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
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
    </tr>
  </thead>
  <tbody>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="n">ax</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">plot_importance</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span><span class="n">max_num_features</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">8</span><span class="p">))</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">data</span> <span class="o">=</span> <span class="n">df3</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">corr</span><span class="p">(</span><span class="n">method</span><span class="o">=</span><span class="s1">&#39;pearson&#39;</span><span class="p">),</span> <span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">fmt</span> <span class="o">=</span> <span class="s1">&#39;.3f&#39;</span><span class="p">,</span> <span class="n">linewidths</span><span class="o">=.</span><span class="mi">1</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;Oranges&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f193fa7b278&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAlcAAAH4CAYAAABnmcgiAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4zLCBo
dHRwOi8vbWF0cGxvdGxpYi5vcmcvnQurowAAIABJREFUeJzs3XlcVNX/+PHXmWEZ9p0BAUUBd0XN
lFJR3GixXLLso/npk7n0qWz5+C3TFk1TWzTL1Nxb1MqlXHMNFMwtTUVxX1EQBpB9h5n7++MSMIIC
RaK/zvPx4KFz77l33pw73Hnf9zl3RiiKgiRJkiRJklQ3NPUdgCRJkiRJ0v9PZHIlSZIkSZJUh2Ry
JUmSJEmSVIdkciVJkiRJklSHZHIlSZIkSZJUh2RyJUmSJEmSVIdkciVJkiRJ0j1LCLFMCJEshIi9
xXohhJgjhLgghDguhOhQYd2zQojzpT/P1lVMMrmSJEmSJOle9jXw0G3WPwwElf6MBr4EEEK4ApOA
zkAnYJIQwqUuApLJlSRJkiRJ9yxFUaKBtNs06Q98q6gOAM5CCG8gHNipKEqaoijpwE5un6TVmEyu
JEmSJEn6/5kPcK3C4/jSZbda/pdZ1MVO7hHK5OaW9R2DmclnilEuRdR3GGZEk16YFvar7zDMaMZs
JutF9/oOw4zj/FQATAfm1XMk5jQhL2H66cX6DsOMZtB8TNEf13cYZjShb2JaNbK+wzCjGbIE0/EV
9R2GGU3bZwAwfda9niMxp3ktCtPnYfUdhhnNq7swxSyv7zDMaIKHA4g7+ZyTm1vW+XfqvX+2ZAzq
cN4fFimKsqiun6cu/ZOSK0mSJEmS7jGlidRfSaYSAL8Kj31LlyUAPW5avvsvPE8ZOSwoSZIkSVKd
EH/DTx3YCPy79K7BECBTUZREYDvQVwjhUjqRvW/psr9MVq4kSZIkSbpnCSG+R61AuQsh4lHvALQE
UBRlAbAFeAS4AOQBz5WuSxNCTAUOle5qiqIot5sYX2MyuZIkSZIkqU6IOzrDS6Uoyr+qWa8AL91i
3TJgWV3HJIcFJUmSJEmS6pCsXEmSJEmSVCdkxUYlkytJkiRJkupEfQwL3o1kkilJkiRJklSHZOVK
kiRJkqQ6IQtXKlm5kiRJkiRJqkOyciVJkiRJUp2Qc65UMrmSJEmSJKlOyOEw1T8+ueo/bTFNezxC
7o1k5j/evso2D789m6DQhyguyGf9hOdJPHUUgOABwwl9YQIA0QtmELNe/dJO71YdGDBjKZbWOs5H
b2PrtNdrFZOiKExbsIboQyfRWVsyY9y/aRXY0KxNfkERr01fzNXEVLQaDWGd2zBuxAAAioqKGT/r
G06ev4azox2fTngeX70bmyJ/Y+mPv5Tt4+zlBH764i1aBPhRE3su5zJ9dwomEwxu48ioTq5m67/+
PZ21J7LQasDVRssH4Xp8HNUvy15/MosvD6offPvfzq4MaOWoxmpU+CAymd+u5aMR8FoXN/o2dahx
X2lb9kT35HSE0FC0bwVFO+ZU2c6iXT9sR39Nzoe9MV09VrZcuPhg/+5eCrd8QtEvpV/CbOOIzbDP
0DRoASgULH8F4+XDNY5JURSmr4wmOuYKOisLpo/qQyt/z0rtTl5OZsKSnRQWlRAa7M/EYaGICpd9
X209wsc//Mq+uaNwcbAhM7eAt5f8wrXkTKwtLfhgZG+a+rrVKKY9Z28wffM5TCaFwfc3YFQPf7P1
RSUmxq8+yamEbJxtLfl0aGt8XGwoKjExef0ZYuOz0AjBxMea0qmJCwCjlh0lJbuIEpNCR39n3u3f
DK2m5petiqIw/YcDRJ+4pvbTc6G0alT5C7pPxqUy4atotZ/a+DHx6RCEEGw7fJm5G49wKSmD1RMf
p7W/BwAJqdk8+t6PNNY7ARDcxJPJw7vUOK4959OYvuUSJkVhcAcvRoWa/30cupLJjK0XOWfIZdaT
zQlv5VG2btS3scTEZ9GhoRMLnmlVtnz/xXQ+2XEZRQFbKy3TBzalkZtN7frqq+1EH7mAztqS6S89
Tqsm3pXaffZdJBuiT5CVk8/vK94qW15UXML4LzZw6lIizg42fPr6E/h4OnP8fAKTFv6sPgcKLz3Z
nT6dm9csqEadEN3HgkaDEvszHP7OfH37pxCtHwWTEfIzUHZ+BNkGAMQrkXDjktouKxll00T1/77t
EaEvgsYCks+h7PwYFGON+2nP1QKm/5qpnqNa2jKqg/m55OtjOaw9nYdWgKuNhg96OuPjoL4Ntvry
Ok1d1f97O2iZ/4j6t6UoCp8fzGbbxXy0QvB0a1uGt7WvcUzqsdtB9NHSY/fiY1Ueu5OXEpkwb6P6
Om8fyMTn+iKE4MwVA5MXbyGvoAgfD2c+eWUA9rbWJCRn8OjrC2jcQI0zOMiHyaMfqXFc0t/rrkyu
hBCTgRxFUWb+3c91bN03/LZyPgM/rPoDWoNCH8K1USBzwlvgG9yZRyfNZcmQLtg4udDjpXdYNDgE
RVEY8+NBzkZuoiArg36T5rLp3ReIjznIsEWbCOwWzoU9Nf+6ouhDJ4m7nsz2pZOJOXOF9+f+wOrP
3qzU7rknehMS3Iyi4hKem/A50YdOEnp/K9bu2IejvS07lr3Pz7sPM2vZOmZPGMljPTvxWM9OgJpY
vTxlYY0TK6NJYWpkCkuf8EHvYMFTK68SFmBHoJt1WZsWHtasGeaHjaWG72MymBmdyux+3mTkG5l3
4AZrhjZECBhcuq2TTsvCg2m42mrZNsIfk6KQWWCqcT8hNNgM+YjcOYNRMq5jN34nJce3YUo6Z97O
2h6rsDGUVJEg6Z6YSsmpCPNlT06n5FQkxUtGgNYSrGr+JggQfTyOuKQMtn38b2IuJjHlm12smjSk
Urv3v9nFlOd6EhzgxZhZG9lzPI7QYH8AEm9kszf2Kt5u5W8OizYdpkVDD+a+2o9L19OYunw3X40f
VG08RpPC1I1nWfp8e/SO1jw17xBhLdwJ1Je/Qaw9dB0nG0u2v/EgP8ckMXPrBWYPbcOaQwkAbHwt
hBs5RYz+6hhrXrofjUYwe2gb7HUWKIrCqytPsO2EgUeDvWreT7HxxCVnsW3ak8RcSmHKyn2smvh4
5X5asZcpw7sS3MSDMXN2sCc2ntA2fgT5uPDFi72YtHxvpW38PBxYN2lgjWMx66vNF1n6bGu1rxYe
I6y5K4GedmVtGjhZM2NgM5btja+0/YguPhQUe7PqcJL577D5IvOGtiTAw5bvfrvOgqirzBjUrMZx
RR+9QFxiGtu+eImY8wlMWbyFVTOer9SuR8emDH34fh4eO89s+drIYzjZ69g+92V+3hvLzBURzP7f
EwQ19GTNRyOx0GpITs9m4P8tIqxjUyy01dQfhAYR9hrKT+MgJwXxr4Uol/ZCWlx5m5TzKN+PhpJC
aNsf0e0FlC3vq+tKClFWjrx5p4jwiSg/vg4Z8YiQEdAyHE5uqVEfGU0KU6MzWfqYG3p7LU+tTSHM
X0egq2VZmxYelqxp5a6eo2Jzmbkvi9nh6kWiTitYN6TyRdC6M/kk5hjZMtQTjRDcyKt5sgcQffQi
cUlpbJvzonrslmxl1fQRldq9v3grU8Y8SnCQD2Nm/MCeYxcJbR/Iuws388bw3nRq2YgfI4+xdON+
Xn26BwB+Xi6s+2RUreL5u8lhQdU/voIXd/hX8jNv/VVCzXo9TsyGFQDExxxE5+iEvYcXAV37cnFf
BPmZ6RRkZXBxXwSB3cKx9/DC2t6B+JiDAMRsWEHz3v1rFVPEgeP079UZIQTtWjQmKyeP5LRMszY2
OitCgtWTs5WlBS0D/UhKTVe333+cAb1DAAjv1p79x86ifvp/uZ+jDvNI9/tqHNPxpAIaOlvi52yJ
lVbwSHMHIi/mmrXp3NAWG0v1JRXsrcOQUwLA3rg8Hmxoi7ONFiedlgcb2vLrlTwAforNYnRpBUwj
BC422hrHpPXvgCnlMsqNODAWU/z7OiyCH67UzvqxtyjaOQeKC82WWwQ/jOnGVUyJZ8sX6hywCHyA
4n3qMcdYDPlZNY4JIPLIJfp3aa4ev0BvsvIKSc4w76vkjFxyCopoF+iNEIL+XZoTceRS2foPv4vm
/4Z0MTtRXbieRueWvgA0aeBKQkoWqZl51cZz/FoWDd1s8HO1wcpCwyPBeiJPp5rHfDqF/h3Uq+nw
1p4cuJiOoihcTM6lc2mlys3eCkcbC2IT1P6w16nXZiUmhWKjYlZ1q1E/HYujf0ig2k8BnmTlFZGc
Yf77JGfkkVNQTLsAT7WfQgKJOKa+gQd4O9PYy7lWz1md4/HZNHTVlfdVGw8iz5ifH3xcdDTzsqOq
It0DAS7YWVd+DQsgp0D9e8gpMOLpYF2pze1EHjpH/+5t1b5q6ktWbgHJ6dmV2rVr6ounS+XKb+Sh
s/TvHgxAeEhLDsReRlEUbKwtyxKpoqKSmh9DrxaQmQBZiWAqQTkXCQFdzdvEH1UTK4DEU2DvUXk/
Fdk4qn9vGWrSqlw9jAjsXrN4gOPJxTR0ssDPyUI9RwXaEHm5wKxNZx/r8nOU3gpDbvWJ0g8nc3nx
fgc0pX3jZlvzcxRA5OGz9A9tc9tjl5yeTU5+Ie2a+qqv89A2RBxSz0tXrqdxfwt15OLBto3ZefBM
rZ5fqh93TXIlhHhbCHFOCPEr0Kx0WTshxAEhxHEhxLrSb64OEEIcqbBdUMXHdc1R34CsxPIr1Kyk
BBz1PqXLr1VYHo+jvgGOeh+ykhIqLa8Nw40MvN1dyh57ubtgSM24ZfusnDx2HTzBA+3Ucn5yhe0t
tFocbG3IyDJ/c98a9TuP9ri/xjEl55Tg5VBe6NTbW2DILrll+x9PZNHNX73aN+SU4OVQfvWod7DA
kFNCVoF6Ypuz9waDVlzltU2JpObeep83E87emNKvlz1W0q+jcTIvt2v82qJx8aEkdqf5xtZ2WPV5
hcItn5i3d2+EknMD3fAvsJsQiW7YZ2BlW+OYAAzpOXhVqDh5udqTnJ5j1iY5PQe9S3nlSO9qj6G0
TcSRi+hd7Gne0PzNqLmfOzsPXwTg+MUkrt/IxpBmvt+qJGcV4OWkK38uR2sMmeaJpiGrEG9n9Q3f
QqvBQWdBRl4xzb0d2HU6lRKjifi0fE4mZJNUYduRy47S9YM92FlrCW9d+ar/dgzpeXi5lleEvFxs
q0xC9S7lbfQudhjSq08oE1JzGDRlHcM/+ZnD55KqbV/2fNmFeDmVJz56RysMWYW32aJmpvYPYsyK
k/SYeZCNMQZGdfOt1faGtGy83BzLHnu5OZKcVjm5ut323u7q9hZaDQ62OjKy8wGIOZ9Av9e/pP+4
hUwa9Uj1VSsAO3fITi5/nJ2CsKs8pPsH0eoRlCsHyxdYWCH+tRAxZH55UpafCRoteKoXjSKoOzjU
/DWVnGvEy7488dHba2+bPP14OpduDcv/LgqNCoPXpDDkxxR+uZRftvxqZglbz+czeE0Kozff4EpG
zc9RUHrs3G9/7JLTstFXOGfo3RwxlLYJ9PMg4pBajd9+4DSJN8ov9hKSMxj05mKGT/qWw6ev1iqu
v4v4G37uRXdFciWEuA94GmiH+s3Vf7zrfwuMVxSlLXACmKQoykUgUwjRrrTNc8BXdzjku0aJ0ci4
j5Yx/PEw/LxvfXKrKObMZXQ6K5r61y7pq6mNp7KINRTyfMfbVxWMCiTllNC+gY6fnmlIuwY6Po5O
ve02tSIEuiemUvDje5VWWT/6JkWRC6DQ/M0cjQUav7YU7/mK3Bk9UYpyse77St3FVI38wmIWbTrM
2EEhldaN6ncf2XmFDHz3O1b8EkOLRh5oajHH6c8YdJ83eidrnpx3iBmbz9GuoVPZFTzAkhHtiZ7Y
laISEwcu1smXyf9lHk62RHw0hJ/eG8hbT3XmjSW7yckvqteYvtmfwMJnWrH7/zozsL0XH267VP1G
d0hwkA+bZ/+X1R8+z+J1eyksql3yUK3mfUDfDH7/oWyRsnQIyvdjULZORXR/GZzUc5GydQqi+8uI
pxdAUV6t5lvVxsazecSmFPN8+/ILnIjhetY+6cHM3i7M2JvF1Uy1H4qNYG0hWPukB4Nb2PLOrltf
6P4dpv23H9/vOMwT45eQm1+EpYWaQHq42BMxfyw/fTyKt57twxtz1pGT99cvBP4qIer+5150t8y5
6gasUxQlD0AIsRGwA5wVRYkqbfMNsKb0/0uA54QQ/wOGAJ2q2qkQYjQwGmDhwoV/KrAsw3Ucvcuv
Mh29fMgyJJBluI5/p+4Vlvty5bcosgwJOHr5mC3PMlynOis3RbFmmzp3pE3TRiSWDvEBJKWmo3ev
OlF57/PvaNTAk2cH9ixb5unmTGJqOl4eLpQYjWTn5ePsWH71vyXqdx7t3rEGv305T3sLkipUqgw5
JegdKr989sXlsfC3NL59yhcrCzV319tb8Nu18mqDIbuETn62OOs02FgI+gSpJ7jwpvasja35EJyS
kYjGpTxBFC4NMGUmljewtkfToDl2r29Q1zt6YvvCCvIWPIPWvwOW7R+DgZMQNk6gmFCKCyg5ugkl
4zrGK2oxtOTIJqzCX602lpW/xLA26iQArRvrSbpRfmWalJaDp4v5BFhPl/JKFYAhTa1kXUvOJD4l
iwHvfle2/In3vmfVpCF4ONsxfVQf9XdXFHr/39f4eTpSHU9HHUmZ5cMjhqxC9E7mw1J6R2sSMwrx
ctJRYjSRXVCCs60lQggm9Gta1u5fXx7G3918Dpq1pZaeLT2IPJVKl6DbT7BfuesUa6PPlvaTO0lp
5cltUnoens52Zu09ne0wpJe3MaTnone5fSXRylKLlaX6BtSqkTt+Hg5cMWSWTXi/HU8Ha7PKnCGr
CL1j7YbwbpaWW8TZpFyC/dRj9XBrd0Yvj612u5XbDrH2F/XmmdaBDUiqULFIupGFp2vNb/zQuzqQ
mJqFl5ujenzzCnB2MD+OAb4e2OqsOH8tmdYB1Vx45aaaV5UcPFByq7gw8rsP0Wk4yppX1CG/ituD
OqwYfww8giDzOiSeRFkzVl3XsCPCpWZzQgE87bQk5ZQnY4YcI3q7ykN4+64VsvD3HL4d4IaVtvyd
W19a9fJzsqBTAytOp6rDjHp7LX2aqBWuPk10vF2D5GrltsOsjSg9dgHeJKXe/th5ujpgqHDOMNzI
Ql/apomPO0vfGQbA5es3iDpyAVCng1hZlk7Gb+KNn96FK4k3qj920h1xV1Su/oQfgYeBfsDviqLc
qKqRoiiLFEXpqChKx9GjR/+pJzobuYng/s8A4BvcmcLsLHJSkrj46w4CuvRG5+iMztGZgC69ufjr
DnJSkijMycY3uDMAwf2f4WzExmqfZ9hj3Vk/byLr502k1wNt2RBxEEVROHb6Mg52Nni6OlXa5rNv
NpKdl8/EMYPNlvcMacv6Xw4AsH3PUUKCm5XNpTCZTGzdU/vkqo2XjriMIuIziykyKmw5k01YE/M3
wlPJBUz+JZl5/RvgZlueeHVpZMveuDwyC4xkFhjZG5dHl0a2CCHoEWDHb9fUEvyBq/kEulrVOCZj
3FE0nk0Qbg1Ba4nlfQMpOb6tvEFBNjlvNiPn3Q7kvNsB4+XfyVvwDKarx8j79LGy5UW7FlK4/TOK
o5aiZCVjSk9A4xkIgEXzUPM5WbcwrHcw66YOZd3UofTq0IQNe8+ox+9CIg421lUmDfY6K45dSERR
FDbsPUPPDk1o6ufO3rmjiJj1HBGznkPvas+PU/6Fh7MdWbmFFJWobx5rok7SsakP9jbVv/G38XUg
LjWP+LR8ikpMbIkxENbCvMoZ1sKdDUfUxHR7bDIhAS4IIcgvMpJXpD7n3vM30GoEgXp7cgtLSC4d
Lisxmog6k0oTj+qHT4eFtWTdpIGsmzSQXu0aseHABbWfLibjYGOJp7P5PjydbbHXWXLsYrLaTwcu
0LNdo9s+R1p2PkaTemPEtZQs4pKz8PWoPgkFaOPjQFxaAfHpBWpfnUghrLlr9RvehqPOkuzCEi6n
qhcY+y5m1KyvHrqfdTNHs27maHrd34wNUcfVvjoXj4Otrsq5VbcS1rEpG6JiANh+4BQhrf0RQhBv
SKfEqPZVQkoGl66n4uNRg3lsSWfA2RccvUBjgWjaEy7edGOBRxCi1ziUjRMgv0JCYm2v3igCoHMC
7zaQdkV9bFP63FpLRMehKMc31Ph3bONpSVxmCfFZJeo56kI+YY11Zm1OpRQzOSqDeY+4ms2dyiww
UWRU56Wm5xs5klREgIt6DuvVWMfBBLXyeeh6Ef5O1dckhj3UkXWfjGLdJ6Po1akZG6JP3PbYebo4
YG9jzbFz8errPPoEPTuqw6M3MtWLC5NJYcFPvzKkTwcA0rJyy1/nhnTiEtPx1btQ3+SwoOpuqVxF
A18LIWagxvQYsBBIF0J0UxRlDzAciAJQFKVACLEd+BKofMtMLTwxazn+93fH1sWd/+2+zK4vpqC1
UP/wD69axPmorQSFPswrO85QXJDPhonqHS75melEz5/O6DX7AYiaP438TLXa9POUsQyYvgQLnQ0X
9mznfPS2qp/8Frrf35roQyfpO2ISOp0V018fXrZuwEvTWT9vIkkp6Sz4YRtN/PQMGvshoCZoTz7U
hcHhD/LmJ1/Td8QknBxs+fSt8i46FHsBb3eXGg8h/sFCI3gnzJORPyZgUmBQa0eC3K2Zs/cGrb2s
6RlgzyfRqeQVm3h9s/om7e1gyfwBDXC20fLfEFeeWqnOUXsxxBXn0onr47q5M35rEjN2p+Bqo2Va
uL7mQZmMFKx6C9uX1yA0Gor2f4cp8SzW/d7CGHeMkhO16/c/FKyegM1zC8DCElNqHPnfjq3V9t2D
/Yk+foXwN75Rb70e2bts3cB3v2Pd1KEAvPdsDyYsVj+KoVtbf0Lb3j5puJiYxoRFOxECAn3c+OD5
XjWKx0Kr4Z3HmzFy2VH12HX0Jkhvz5ydF2nt40jPlh4M7tiA8atPEf7JPpxsLZn1r9aAWnUZuewY
GgGejtZ89FRLAPKLjLz0bQxFRgWTotC5iQtDOvvcLozK/dTGj+gT8YS/vUb9KIb/dCvvp/fXld3t
996wB9WPYig20q21L6Gt1UryziNXmPb9ftJyCnhhzg6a+7mx5PWHOHwuiTkbjmCp1SA0gsnPdMHZ
rmbVJwut4J1HAxj5bSwmk8KgDnqCPO2YE3GF1j4O9GzuxomEbMZ+f4qs/BJ2nU3ji8irbB6r3hzy
zJIYLqXmkVdkosfMg3zQvyldg1yY8ngQr/5wGo0QONpYMG1AUO36qkMg0UcvED52ntpXL5XfVTnw
/xaxbqZ68fjJ8l/4+ddY8ouK6THmMwb3as/LT3VncM/2jP9iPeEvz8XJ3oZZr6t3mf5+5hqL1/+A
pVaL0AjeG/kwLo41mGOoGFF2fYYYOBOEBuXkFki7gggZgZJ8Bi7tQ3R7ASxtEI+W3iH4x0cuuDZC
9Po/UEzqtodXlt1lKO57Gpo8CAiUExvUSfE1ZKERvNPNiZGbbqiv8+a2BLlaMue3LFp7WNGzsY5P
9meSV6zw+nZ1CPuPj1y4lF7CpKgMNAJMCoxqb192l+GoDva8sTOdb2JysLUUTA2r3U0U3dsHEn3k
AuGvzENnpX4Uwx8GvrG47G6/90Y+xIT5mygsKqZbu0BC2wcA8PPek3y3Xb3TuU+n5gwKU29MOHzq
KnNWR5Udu8mjHsbZvnZ3Nkt/H3HzXWT1RQjxNvAskAxcBY4AvwALAFvgEvCcoijppe1DgLVAI0Wp
0cC8Mrm5ZfWt7qDJZ4pRLkVU3/AOEk16YVrYr77DMKMZs5msF2uXDP7dHOerwxqmA/OqaXlnaUJe
wvTTi/UdhhnNoPmYoj+u7zDMaELfxLTq5o8CqF+aIUswHV9R32GY0bRVq/amz2p+196doHktCtPn
YfUdhhnNq7swxSyv7zDMaIKHwx0u/sxua1nnScXrx4vvuQLW3VK5QlGUacC0KlZVntmr6gp8VcPE
SpIkSZIk6Y64a5Kr2hBCrAMCgJ7VtZUkSZIk6c6450pMf5N7MrlSFKX2H70sSZIkSdLf6l796IS6
dq/eLShJkiRJknRXuicrV5IkSZIk3X1k4UolK1eSJEmSJEl1SFauJEmSJEmqExpxd3y8U32TyZUk
SZIkSXVCDguq5LCgJEmSJElSHZKVK0mSJEmS6oSsXKlk5UqSJEmSJKkOycqVJEmSJEl1Qn6IqEom
V5IkSZIk1QmZW6nksKAkSZIkSVIdEoryj/lMin/MLypJkiRJpe5oMWlRB4s6f68dfaTkniuI/aOG
BZVLEfUdghnRpBeTm1vWdxhmJp8pRrm8u77DMCMa94DsxPoOw5yDNwCmVSPrORBzmiFLMB2cX99h
mNF0fhHTlvH1HYYZzSMfYYr+uL7DMKMJfRPTzsn1HYYZTZ/JAJjWj63fQG6iGfAFyrX99R2GGeH3
AKfC767BoJbbTfUdwj/WPyq5kiRJkiTp73PPlZj+JjK5kiRJkiSpTsi7BVV3Vw1TkiRJkiTpHicr
V5IkSZIk1QlZuFLJypUkSZIkSVIdkpUrSZIkSZLqhEaWrgBZuZIkSZIkSapTsnIlSZIkSVKdkIUr
lUyuJEmSJEmqE/KjGFRyWFCSJEmSJKkOycqVJEmSJEl1QhauVLJyJUmSJEmSVIf+8ZUrRVGYtmAN
0YdOorO2ZMa4f9MqsKFZm/yCIl6bvpirialoNRrCOrdh3IgBABQVFTN+1jecPH8NZ0c7Pp3wPL56
NzZF/sbSH38p28fZywn89MVbtAjwqzam/tMW07THI+TeSGb+4+2rbPPw27MJCn2I4oJ81k94nsRT
RwEIHjCc0BcmABC9YAYx65cD4N2qAwNmLMXSWsf56G1snfb6n+urL1cRfSgWnbUVM8b9h1ZBVfTV
tIVcTUxR+yqkLeNGDALg0IlzzFiwmrOXE5g1YSQPdbvPbNuc3HweHTOZXg+0472X/lXzmGZ+QdTe
A+h0Oj6c/Batmje9ZfsXXp9IfMJ1Nq/+GoDPvlxKRNReNBqBm4sLMya/hd7Dvdb7rWjP+TSmb7mE
SVEY3MGLUaHmx/zQlUxmbL3IOUMus55sTngrj7J1o76NJSY+iw4NnVjwTCuz3/PziDi2nUxFK+Dp
Tt4MD/GpUTx/bD99RRTRMVdmzwfDAAAgAElEQVTQWVswfVRfWvl7Vmp38rKBCYt3UlhUQmiwPxOf
6Y4Qgrk/HWBNVCyuDjYAvPbkg3QPbkxxiZF3l0ZwKi4Zo9FE/64tGP3Y/TXrp9MGpq87ofZT50aM
6m3ev0UlRsavPMKp+Aycba349NmO+Ljala2/np7HYx9G8NJDzRkRFgRAVn4R7/5wjPNJWQjgg391
oL2/a437qayvfjhA9Ilr6KwsmP5cKK0auVfuq7hUJnwVrfZVGz8mPh2CEIJthy8zd+MRLiVlsHri
47T2Lz++Z+PTmLT8V3Lyi9FoBGvefhxry+pPw3tOXWf62iOYTAqDHwxgVN+W5n1VbGT88gOcupqG
s501n454EB83e/aeTuTTjTEUl5iwtNDwxoB2hDTzUuO/msaE5QcoLDYS2qoBEwd3QNRiwsyes6lM
33hGPX73+zIqrLF5TCUmxq86wamELJxtLfl0aDA+rjYUG028u/Ykp65nYzQq9L/Pm9FhTSgsNjJ8
wSGKjCZKjArhbfSM7RtY43ig9HwwbyXRvx1Xz1FvjqRVkL9Zm/yCQl6bMo+ricml56h2jBv1lFmb
7dGHeHXKPNbMm0SbZo05fuYS783+qvQ54OV/D6BPV/Pz163YdQzH64XPEFot6VuXcmP1R5XaOIY+
icczk1BQKLwUQ8KHz5St09g6ELDoJNn7N5A0bywaG3v8Z0WXrbdw9yUzciWGBbU/p/8d5Jwr1V2b
XAkhFOBTRVHGlT7+P8BeUZTJdfk80YdOEnc9me1LJxNz5grvz/2B1Z+9Wandc0/0JiS4GUXFJTw3
4XOiD50k9P5WrN2xD0d7W3Yse5+fdx9m1rJ1zJ4wksd6duKxnp0ANbF6ecrCGiVWAMfWfcNvK+cz
8MNlVa4PCn0I10aBzAlvgW9wZx6dNJclQ7pg4+RCj5feYdHgEBRFYcyPBzkbuYmCrAz6TZrLpndf
ID7mIMMWbSKwWzgX9myvZV/Fqn21bCoxZy7z/tyVrP58QuW+Gty3vK/emk30oVhC72+Nt4crM8b9
h2U/7qxy/59/u5GOrYNqF9Peg1y5Fs+OdSuJiT3F5BmzWfPNl1W23REZjZ2tjdmykcOf5rX/Pg/A
tz/8yLzF3zBl4rha7bcio0lh6uaLLH22NXpHa55aeIyw5q4EepYnBQ2crJkxsBnL9sZX2n5EFx8K
ir1ZdTjJbPm6owYSMwvZMvY+NBrBjZyiamOpKPr4FeIMGWz75FliLiYx5etIVk1+ulK797/ZxZQR
vQgO8GLMrA3sOR5HaLA/AM+Gt2fEI+ZvKNt/O09RiZGN058hv7CYfhOW82hIM3w8HG8bj9GkMPXH
GJa+0AW9sw1Pzd5NWGsvAr3Kt1t7IA4nG0u2v92Hn4/EM3PTKWY/W564fbQ+lm4t9Gb7nf7TCbq2
8OTz5zpRVGKioLikVv0EEB0bT1xyFtumPUnMpRSmrNzHqomPV2r3/oq9TBneleAmHoyZs4M9sfGE
tvEjyMeFL17sxaTle83alxhNvLlkNx89353mfm6k5xRgoa1+8MBoMjF19e8sfTlM7atPdhDWxodA
b6eyNmv3X8LJxortkx/j58NxzNwQw+wRXXCxt+bLMaF4Otty7noGo+btJmqaemH4/qpDTBnaiWB/
N8Z8GcWeU4mEtmpQoz4ymhSmrj/N0pH3oXfS8dTcA4S19CBQb18e06F49fi92Y2fjyUyc+s5Zg8L
ZvtxA0UlChtff5D8IiP9Pt3Lo8HeNHDR8dXojthZW1BsNPHMl7/RrZk77Ro51ygmgOjfjhOXYGD7
Nx8Rc/oi73/+Lavnvlep3XNPPUxIuxbqOeqNj4n+7TihndoCkJOXz/J1Owlu3qSsfZC/D2vnT8ZC
qyX5RgYDxrxL2APtsNBqbx+QRoP3S3OJm9CX4tR4mnzxG9kHNlJ09XRZE6sGgbgNeYvL/+uKKScD
rZOH2S48/j2VvNjyZMqUn8OlFzuUPW489xDZv/5U4z76u8nhMNXd3A+FwCAhROVLxjoUceA4/Xt1
RghBuxaNycrJIzkt06yNjc6KkOBmAFhZWtAy0I+k1HR1+/3HGdA7BIDwbu3Zf+wsiqKYbf9z1GEe
6V6zqxyAuMO/kp+Zdsv1zXo9TsyGFQDExxxE5+iEvYcXAV37cnFfBPmZ6RRkZXBxXwSB3cKx9/DC
2t6B+JiDAMRsWEHz3v1rHM8fIvbH0L9XSGlfNSErJ5/kG9X1VcOyvvL1cqdZE98qr45jz8dxIyOL
Lh1aVlp325ii9jLgkXA1pjatyMrOITn1RqV2uXl5fLVyNf99frjZcnv78qQnP7+gLLaa7vdmx+Oz
aeiqw8/VBisLDY+08SDyjPmx9HHR0czLrsoP23sgwAU768on7B8OJfJij4ZoSjdys7eqNpaKIo9c
on+XFurvE+hNVl4hyRm5Zm2SM3LJyS+iXaA3Qgj6d2lBxJGLt92vEIL8wmJKjCYKikqw1Gqxs6k+
tuNX02nobo+fu53aT+19iYw1TygjY5Po30mtjIYHN+DA+ZSyv61fTlzH182WQC+HsvbZ+cUcvnSD
wZ0bAWBlocGxBrHcLPJYHP1DAtW+CvAkK6+I5Iw8szbJGXnkFBTTLsBT7auQQCKOxQEQ4O1MY6/K
CcHeUwk083WluZ8bAC72OrSa6k/Bx6+klfaVPVYWWh7p0JDI4+aJeeTxePp3VitH4e39OHA2CUVR
aOnniqezLQBB3k4UFhspKjaSnJmvxt/YXY2/kz8Rxysn+7eM6VomDd1s8XOzVY9fsBeRp5LNYzqZ
Qv/71GQtvI2eAxfSUBQFISC/uER9zRQbsdRqsNNZIITAzlq93i8xKhQblVpXQSL2HaV/ny7qsWsZ
qJ7Pb2SYtbHRWRPSrgVQeo4KakRSSvnf6Jyvf2LkkEewsrI02+aPRKqoqBhRw5lFNs06UXT9AsVJ
l6GkmMzdq3B4wPzc6/zwKNI3zceUo8ZpzEwpW6cL7ICFiyc5v1d9QWrlE4SFsyd5sXtqFI9059zN
yVUJsAioVOsUQnwthFgghDgshDgnhOj3Z5/EcCMDb3eXssde7i4YUjNu2T4rJ49dB0/wQLvmACRX
2N5Cq8XB1oaMLPM3ra1Rv/Noj5oNldSEo74BWYnlJ8KspAQc9T6ly69VWB6Po74BjnofspISKi2v
LcONDLw9yodYvDycMdxIv2V7ta+Ol/XVrZhMJj5atJY3Rw6ufUwpKXh5lV/peek9MCSnVGr3+ZfL
GPHMEHQ660rrZs9bQvdHn2TT1p28+sKIWu33ZsnZhXg5lT+H3tEKQ1ZhrX6nqlxNK2BrbAqDFxxl
9LexXLmRX6vtDWk5eLmWVxW8XO1JTssxa5OcloPepbyN3tUeQ4U2K3+Jof/bK3h78U4ycwsA6Ht/
IDbWloS+soRery9jxCMdcLbXVRtPckY+Xs7lVUS9kw5DpvnvZMjMx7u0jYVWg4POgozcInILS1gS
cZ4Xw81fV/FpubjaWzHx+yMMmrmLd344Sl5h7StXhvQ8vCoMP3q52FaZiOpdytvoXewwpJsnYDe7
YsgEASNnb2PQ1PUs2Xa8RvEkZ+bh5WJb4blsq+6r0jYWWg0ONlZk5JpXN3ccu0YLPxesLLUkZ+Sh
d66wT2dbDBk1f00lZxbg5Vx+nNXjZ/46N2QV4O2kK49JZ0FGXjF92+ixsbQgdFoUvWZEMyLUH2db
NZExmhQGfrafrlN382CQG8ENa161AjCkpt90jnLBkHq7c1Quu/Yf44H26kXdyfNXSExOo0dIu0pt
Y05fpN/zE3l81DtMfu3Z6qtWgIWbD8Up5efqktR4LN3Nh/OtfIOw8mmK/6d78P9sH3Ydw9UVQqAf
PRPD4jduuX/HHk+TFbW62jjuJCHq/udedDcnVwDzgGFCCKcq1vkDnYBHgQVCiEpndCHE6NIE7PCi
RYv+cjAlRiPjPlrG8MfD8POuWUEt5sxldDormvrXPpm5l5UYjYz7cAnD+4fh5+1x27bfbY6ie6fW
eHm43Lbdn3X67Hmuxl+nT1i3Kte//tJIon5ew2MP92HF6nV/Swx/VbHRhLWFhrUvtGdwRy/eWXfu
jj7/073asGPmf1g3dRgeznZ8/J16pXzikgGtRhD1+fPs/PQ5vtp6hGvJmdXs7a+Zt+0Mz3YPLKty
/MFoVDgVn8nTXRrz0/+FYWulZXHEne2n2zEaFY6cN/DJyB6sfLMfvxy9wv7T1+/Ic59PzGTWhhje
f7ruLvL+rBPXMtFqIOrt7ux8qxtfRV/h2g01MdVqBOtee4BdE0M5cS2Tc0nZf1scJUYj46YtYPjA
3vg18MRkMvHhl98z/oXKw+UAwS0C2Lx0OmvmTWLR95spLKrd0PytCK0FVj6BXHkjjIQZQ2nw2iI0
dk64PPYiOYe2UpKacMttnboPIXPX93USh1S37to5VwCKomQJIb4FXgFuvqxarSiKCTgvhLgENAeO
3bT9ItTql/rwUgQAKzdFsWabOh+iTdNGJFa4sklKTUfvXvXV0nuff0ejBp48O7Bn2TJPN2cSU9Px
8nChxGgkOy8fZ8fyK9otUb/zaPeOtf/lbyPLcB1Hb9+yx45ePmQZEsgyXMe/U/cKy3258lsUWYYE
HL18zJZnGWp2Ul+5cRdrtv0KQJum/iRWKJ8npWSgd6s6IXrv8xWlfdW72uc4dvoSv8ee57tNUeQV
FFBcYsTOxrpsInylmFavY/X6zWpMLZuTlFReUUoypKD3NE/mjp44Rezps/R8bAglRiNpaRkMH/0q
yxd9btbusYd7M/qV8bwy5jn0Hh7V7rcqng7WJFW4gjdkFaF3rFwtqy29ozV9WqoJfZ8Wbrxdg+Rq
5S8xrN0dC0DrxnqSKlShktJy8KxQyQLwdLXHkF7expCWg760jbtT+Wv6yR6teeHTjQBs3n+Wrm0b
YWmhxc3Rlg5BDYi9bMDPs6rroQrP5WxDUoVKiSGzAL2T+Xw4vZMNiaUVrhKjieyCEpztrDgel872
mARmboolu3RiuLWFlr7BDdA76QhupFYu+gY3YHHE+Wr7CWDlrlOsjT5b2lfuJKWVV6qS0vPwdLYz
a+/pbIchvbyNIT0XfYXqUlX0LrZ0bOqFi4N6HRjaxo9TV1N5oMXtL7w8nWxJqlAVM6TnVd1X6WqF
q8RoIju/CGc7q7L4xy7aw4fDQ2jo4VAavy2GCkOdhow89M7m+7x9TDqSMgrKt88sQO9k/jrXO+pI
LK1wlR0/W0s2H0uiazN3LLUa3Oyt6eDvTGx8Fn5u5f3naGNJpwBXfj17g6YVhn6rsnLDL6zZEgVA
m6aNbzpHpaN3v8U56tOvaeSj59kn1EpRbl4B568k8O9xHwKQmpbJi+99zvwpr9KmWflk/YBGDbC1
0XHucoLZ8qqU3EjA0qP8XG3h7kvxTclScWoC+WcOgrGEYsMViuLPYeUThG2LEGxbd8Ol33/R2Ngj
LKww5eeQvEyd52rdpC1oLSi4cOS2Mdxp92ihqc7d7ZUrgM+A5wG7m5Yr1Ty+pWGPdWf9vImsnzeR
Xg+0ZUPEQRRF4djpyzjY2eDpWvmN4bNvNpKdl8/EMeZDVz1D2rL+lwMAbN9zlJDgZmXzdkwmE1v3
1H1ydTZyE8H91btJfIM7U5idRU5KEhd/3UFAl97oHJ3ROToT0KU3F3/dQU5KEoU52fgGdwYguP8z
nI3YWKPnGvZ4GOvnv8v6+e/S64F2bIg4UNpXl9S+cquir75eT3ZuPhNfeKqKPVY2c/zz7Fr+IZHf
TufNkYPp3yvklokVwLCnBrLhu6Vs+G4pvXt0Zf2W7WpMJ07iYG+Hp7ubWfuhg/vz67Yfidy0iu+W
fIF/Q9+yxOrK1fKSfcTuvTTxV+f49Oz+YLX7rUobHwfi0gqITy+gqMTElhMphDWv3d1qVenV3I2D
l9Xh6kNXMvF3q/6NcFjvYNZ9MIx1Hwyj130BbNh7Wv19LiTiYGtdZcJgb2PFsQuJKIrChr2n6dlB
ndRbcVhs5+8XCPJV+8LbzYGDp9Sh6LzCYmIuJtHEu/oKZBs/Z+JScoi/kav209F4wlp5mbUJa+3F
ht+uArA95johger8oBWvdCPivXAi3gvn390DGN27KcO6NcHDUYe3sy2Xk9Vqx4HzKWZzsm7bV2Et
WTdpIOsmDaRXu0ZsOHBB7auLyTjYWJbNWyrvK1vsdZYcu5is9tWBC/Rs1+i2z9G1lS/nEtLJL1Tn
Gx06l0SAd/XDXm0auRKXkk18ag5FJUa2HLlKWFtfszZhbXzYcPCy2ldHrxHSVI8Qgqy8Il5YEMX/
+gfTIaD84sDTyUaN/3KqGv9vV+h50z5vG5OvI3E38ohPy1OPX0wSYS3M7z4Na+nBht/Vi7jtJwyE
BLgihMDbWcfBC2oClFdUQszVTJp42pGWU0RWfjEABcVG9p+/QWPPm0/7lQ3r35v1C6eyfuFUenXp
wIade9Vjd+pC6Tmqch9/tuxHsnPzmPji0LJlDva2HPhpLpErZxG5chbBLQLKEqv4xBRKjEYAEgyp
XLqWiK9X9aMX+WcPYeUThKXeHywsceoxhJwD5ufe7H3rsWurXhRrHd2w8m1KceIlEj4azvnh/lx4
tgmGxW+QGbG8LLECcOrxL7J2/1BtDHeaRtT9z73orq5cASiKkiaEWI2aYFW8fe5JIcQ3QGOgCXD2
z+y/+/2tiT50kr4jJqHTWTH99fIJzwNems76eRNJSklnwQ/baOKnZ9BY9apm2GPdefKhLgwOf5A3
P/maviMm4eRgy6dvPV+2/aHYC3i7u9R4CPEPT8xajv/93bF1ced/uy+z64spaC3UOQmHVy3ifNRW
gkIf5pUdZyguyGfDxJEA5GemEz1/OqPX7Acgav408jPVqtzPU8YyYPoSLHQ2XNiznfPR22rfV51a
E33oBH1HvIPO2orp/3u2vK9enMr6+e+W9tVWmvh5MejlaaV9FcaTD3flxNkrvDz1S7Ky1blYc5dv
YvOiybWOwyymLiFE7T1InwHDsNFZM33S+LJ1/Yc+z4bvlt52+1lfLOJy3FWERoOPt573J/yv2v3e
joVW8M6jAYz8NhaTSWFQBz1BnnbMibhCax8HejZ340RCNmO/P0VWfgm7zqbxReRVNo9Vb3h4ZkkM
l1LzyCsy0WPmQT7o35SuQS6M6ubHG2vP8M2+BGyttEwdULu7KrsH+xMdc4XwN75RP15gZJ+ydQPf
Wcm6D4YB8N6/w9SPYiguoVvbRoS29Qdg5g+/cuZqCkKAj7sjk5/rBcDQ3m15e/FO+k1YDgoM7NaS
Zg2rr/BZaDW880RbRi7cp/ZT50YEeTsyZ+tpWvs507O1N4M7N2L8yt8Jn7YTJ1tLZg2vfkjr7Sfa
8Mby3yk2mvBzs2XavzpUu02lvmrjR/SJeMLfXqP21X/Kh5MHvr+OdZMGqn017EH1oxiKjXRr7Uto
azU52XnkCtO+309aTgEvzNlBcz83lrz+EE521vynT2uenLYBIdTKVY+2DauMoVJfPdWRkfN2Y1IU
BoU0IcjbiTmbj9O6oSs92/oy+MEAxn+7n/DJm3Cys2LWc10AWBl9jqsp2Xy5NZYvt6pVzCUvh+Hm
oOO9pzoyYcVBNf6W3oS29K5xH1loNbzTvzkjl6ofDzHofh+CvOyZs+MCrX0d6dnSk8H3+zB+VSzh
H+/BycaSWUPVu/GGPuDH22tO0m+WOnowsGMDmnk7cDYxmwmrYzGaFEyKwkNtvQhrUf1rqaLunYOJ
/u04ff/9Jjpra6a/UX4+HjDmXdYvnEpSShoLvttEk4beDPrvJEBN0J58pPutdsvvsedY/MPPWFho
0QgNk14ZjotTDRJ3k5GkeWNpOH0bQqMlY8dXFMadwuPf75N/7jA5BzaRe3g79h36ErAoFsVkxLD4
TYzZt76h6Q+OoU9y9d1Hq49Bqhfi5jvb7hZCiBxFUexL/68HLgMfK4oyWQjxNVAAdAQcgf8pirK5
ml2WDQveLUSTXkxubll9wzto8plilMu76zsMM6JxD8hOrO8wzDmob0SmVSPrORBzmiFLMB2cX99h
mNF0fhHTlpolp3eK5pGPMEV/XN9hmNGEvolp5+T6DsOMps9kAEzrx9ZvIDfRDPgC5dr++g7DjPB7
gFPhd9dgUMvtJrjDI3WrQyzqPKl46kDJPVe/umsrV38kVqX/NwA3T2j4RVGUF+5sVJIkSZIkSbd3
1yZXkiRJkiTdW+7VOVJ17Z5MrhRF+U99xyBJkiRJklSVezK5kiRJkiTp7nN3zTqrPzK5kiRJkiSp
Ttyrn6he12SSKUmSJEmSVIdk5UqSJEmSpDohKzYq2Q+SJEmSJEl1SFauJEmSJEmqE3LOlUomV5Ik
SZIk1QmNuDu/9eVOk8OCkiRJkiRJdUgmV5IkSZIk1QnN3/BTE0KIh4QQZ4UQF4QQb1WxfrYQ4ljp
zzkhREaFdcYK6zb+qV/8JnJYUJIkSZKke5YQQgvMA/oA8cAhIcRGRVFO/dFGUZTXK7QfC7SvsIt8
RVHa1WlMivKPGR/9x/yikiRJklTqjk4x39pNW+fvtQ/vMd72dxBCPABMVhQlvPTxBABFUWbcov0+
YJKiKDtLH+coimJflzH/oypXpoX96jsEM5oxm1Eu767vMMyIxj2Y3NyyvsMwM/lMMRsevLteqv33
lQBg2vd5PUdiTvPgq5iOr6zvMMxo2g7DdHB+fYdhRtP5RYo/6FDfYZixfOcISuLR+g7DjPBWL+5N
G1+vpuWdpXl8Nh+0uLvOU++cLsY0q2t9h2FGM+7XO/+cd/wZAfABrlV4HA90rqqhEKIR0BiIrLBY
J4Q4DJQAHyqKsv6vBnR3vWNJkiRJkiRVIIQYDYyusGiRoiiL/uTungbWKopirLCskaIoCUKIJkCk
EOKEoigX/2y8IJMrSZIkSZLqyN/xOVelidTtkqkEwK/CY9/SZVV5Gnjppv0nlP57SQixG3U+1l9K
ruTdgpIkSZIk3csOAUFCiMZCCCvUBKrSXX9CiOaAC7C/wjIXIYR16f/dgS7AqZu3rS1ZuZIkSZIk
qU7UR8VGUZQSIcTLwHZACyxTFOWkEGIKcFhRlD8SraeBHxTzO/laAAuFECbU8D+seJfhnyWTK0mS
JEmS7mmKomwBtty07L2bHk+uYrt9QJu6jkcmV5IkSZIk1QmN/G5BQCZXkiRJkiTVEfnFzSo5oV2S
JEmSJKkOycqVJEmSJEl1QlZsVLIfJEmSJEmS6pCsXEmSJEmSVCfknCuVTK4kSZIkSaoTcjhM9Y9P
rvZczmX67hRMJhjcxpFRnVzN1n/9ezprT2Sh1YCrjZYPwvX4OKpfGLr+ZBZfHkwD4L+dXRnQyhGA
IqPCB5HJ/HYtH42A17q40bepQ41jUhSFaV+uIvpQLDprK2aM+w+tghqatckvKOK1aQu5mpiCVqMh
LKQt40YMAuDQiXPMWLCas5cTmDVhJA91u89s25zcfB4dM5leD7TjvZf+VaOY+k9bTNMej5B7I5n5
j7evss3Db88mKPQhigvyWT/heRJPqV9CGzxgOKEvTAAgesEMYtYvB8C7VQcGzFiKpbWO89Hb2Dqt
9l8O69k5nDavfQpaLVc3LeP88o/N1rd+ZRbuHboDoNXZYu3iyZZwd9w79KD1KzPL2tk3as7hSUNJ
it6I+309afXyhwihoSQ/l6MfjCA3oebfhKAoCtO/+5Xo43HorCyY/nwvWvl7VGp38koyE5ZEUlhc
QmjbRkwc2hUhBJ//dJDIo5fRCIGrow0znu+Fp4sdmbkFvL1sF9eSM7G2tOCDEWE09XWreUxfbSf6
yHl01pZMf6k/rZp4V2r32XeRbIg+TlZOPr+vmFC2vKi4hPFfrOfUpUScHWz49PXB+Hg6A3A2zsCk
hZvJyS9CIwRrPhyJtVX1pxZFUZi+IoromCvorC2YPqovrfw9K/fTZQMTFu+ksKiE0GB/Jj7THSEE
c386wJqoWFwdbAB47ckH6R7cmE37zrBsy+9l25+9lsqPU4bSolHlY1AV0eRBtOH/B0KL6dg6TPu+
Nluv6fAEmo5PgcmEUpyH8ecPIPUy2DihfeJjRINWmGI2Ydr+UYWNLNA+9Bai0X2gmDDunodyJpKa
UhSFaV98Q/SBo+h01sx467+0atrYrE1+QSGvTf6MqwkGtFoNYQ90YNyYoQDMmPsNB4+qn4uYX1hI
WnoWh35eBsAnC1YSdeAoJpOJBzu25e2xzyJqUH7YcyaF6RtPYTIpDO7kx6ieAWbri0qMjP/hOKfi
M3G2teTTZ9rj42rLpiMJLNt9qazd2aRsfny1Ky18HDkZn8mEVTEUFpsIbe7BxP4taxTLH5p07Uv4
xE8RGi3H1i5j35JPzNY7NWhIvw8WY+vqQUFmGuvffJZsQwKNOnWnz1uzytq5N2nGT+OGcS5iI/6d
e9DrzY/RWlqSdPIom94ZhWI03vzUt+bfGRH2KggNSuxm+G2F+fr7hiDa9AOTEfIyULbPgGwD+LVH
9HilvJ1rQ5SfJ8OFPdBuEKLDUwgXX0zzH4X8zJrHI90Rd3VyJYRwAyJKH3oBRiCl9HEnRVGK/sr+
jSaFqZEpLH3CB72DBU+tvEpYgB2BbtZlbVp4WLNmmB82lhq+j8lgZnQqs/t5k5FvZN6BG6wZ2hAh
YHDptk46LQsPpuFqq2XbCH9MikJmgalWcUUfiiXuejLbl00l5sxl3p+7ktWfT6jU7rnBfQkJbkZR
cQnPvTWb6EOxhN7fGm8PV2aM+w/LftxZ5f4//3YjHVsH1SqmY+v+H3vnHR5V0T3+z9303jspQIBA
gADSezUUMYAIfMFKVQEbrx0VQQELoqioCAoCKk0INSAJEIrUQEInBBJI24T0nuzu/f1xY5JlA2xe
Q/u983mefZ7cmTNzz57MzD33zLl3V3B09WKGz/+51vomPQfi7B/IotDmNAjpxJAPv2Xp6G5YOTjR
e+pMlozsjCzLTNlwhPdeEu0AACAASURBVItRWyjNz+WxD79ly/svkBx7hHFLthDYI5TL+3car5RK
Rev/LOLQKwMpyUim17LDpO/fQkHi+SqRM4tmVP3dcORUHJq2AeBGzF72PtceADM7J/qvu0jmEcVe
IW98y5G3RlCYdIGAES/Q9Ll3OfnJBKPVio67RpI6j4j544i9omb2yn2seX+kgdxHv0Yz+/nehDTy
YMrCbew/fY2erf2ZMKgtr4xQftB95V9xLN58jFnP9mbJ1hia+7ry7fRBXEnLYc7KaH55M8w4nU5e
Jikti4hvphEbn8Lsn7axZt5EA7ne7ZsydlAHBk3/Vq98fdRJHGyt2PntdLYdPMMXq3az8PWRaLQ6
3ly0kU+nDyMowJOcgmJMTYy7d42OSyRJnUvE588Sm5DO7OVRrJk1xtBOK/Ywe3w/Qhp7MmVBOPvj
kugZEgDAs6FtGT9Y/+ZhaNcghnYNAuDS9RtM+3qr0Y4VkgqTQW+hWf0S5KsxnbAK3aV9ivNUie5M
BLqYDYp4k56YDJiB9vdpoClDt+97JLfG4Bao162q+0Tk4my03w8HJLByME6fSqKPnCIpOY2dq78i
9txlPlq4lLXff2Ig9/zox+jcNlhZE16fQ/SRk/Ts1JZ3pj1bJbPyzwjOxycCEHPmIjFnLhK+TLkp
GTv9Q46eOkentsG31Uerk5mz8SzLJnfEw8GSUYsO0ifYnUCP6pvI9UeTcbAyZefbvdl2KpUvtl9k
4VNtGdrOh6HtfAC4lJbPtOUxNPdRbkw/+vMMs0e2IsTPkSnLjrP/YiY9gwwd7tqQVCoGvb+I1RMG
ka9OZsLaw1zas5UbCdXrQb83PuV0+CriwlcS0Kk3fV//hPC3niPp6D6WjlDWA0sHJ6ZGXODKwb9A
knh83s+sGh9KdmI8vaZ/SMiwZzi14RejdEJSIfV7HXn9a1CQgTRuKfLlA5CdWC2TcQl51UTQlEHI
MKReLyFv/RCun0Re+bwiY2mHNH4NJB5VjlNPI185BKO+MU6Pe4h4z5XCAx3Bk2U5S5blNrIstwF+
ABb+c/xvHSuAuPRS/BzN8HU0w9xEYnCQHVEJRXoynfyssTJTzBTiZYm6UAPAwaRiuvpZ42hlgoOl
CV39rDmQWAzAn2fymVwZAVNJEk5WJnXSK/LvWML6dUaSJNo0b0R+YQkZWfp3JlaW5nQOaQaAuZkp
LQL9SL+RA0ADT1eaNWpQ6x3fmfgksnLz6dauRZ10Sjp+gJK87FvWN+v3OLHhyh1ZcuwRLO0dsHXz
pHH3R0k4FElJXg6l+bkkHIoksEcotm6eWNjakRx7BIDY8FUE9TfOUfgHpxYdKUpOoDj1KrKmgpTd
a/Hs8fgt5RsMGEPKX2sMyr37PoH67wi0ZSVKgSxjZqMs9mY2DpTeSKuTXlEnrxLWtZny/2vsSX5x
ORm5+uMqI7eIwpJy2jT2RJIkwro2IzJGuYDbWplXyZWUVVQlMVxOzaZTC+Wi1MjLiZQbBdzIKzZO
p2MXCesVoujUtAH5RWVk5BQYyLVp2gB3J8Moq9K+NQChnVtw+MxVZFnmYGwCzfw9CArwBMDJzhoT
I52rqJgrhHVrrugU6EV+cdmt7RTopdipW3MiY4yPIm47fJHBnZoaLS95t0TOTobcFNBp0J3diapp
b32h8ho6mlvBP7+kUVGKfP0UssZwaVK1eRzdwX9uTGQoyTVaJ4DIg8cJC+2p2Cq4CfmFxWRk5ejJ
WFla0LnSKTI3M6VF04akZxrO2W2RBxnSr6vyfSWJsvIKKjQayisq0Gi0uDo73lGfuGu5+Lla4+ti
jbmpisFtvIg6q9aTiTqrJuyRBgCEtvLkcPwN9H91BLadSmNwGyWCmpFfSmGphjb+Tsr/+hEfIs/o
93k7vFt3JPtaArnJV9FVVHB2+xqa9h2qJ+MW2JzEI3sASDyy16AeoPmjT5Cwfyea0hKsHV3QVpST
nRgPwJVDuwl6dLjROuHZHHKTIS8VdBrki7shsLu+zPWTimMFkHYWbGu5EWjSBxIPV8tlxEN+uvF6
CO45D7RzdSskSQqQJOmCJEmrJUk6L0nSekmSrOvaT0ahBk+76uCdh60p6gLNLeU3nM6nR4ANAOpC
DZ52ZtVt7UxRF2rIL1XCxYsOZjFi1TVe3ZLGjaJb91kb6qxcvNyqtyc93RxR37SQ1iS/sJg9R+Lo
0ibotv3qdDo+XbKeNycaRlH+LfYe3uSnJVfrlJ6CvYdPZfn1GuXJ2Ht4Y+/hQ356ikF5XbB086ZE
Xd13SWYylm6192Hl6Ye1VwCZJwy3Ynz6j9Zzuk7On0LnBVt4dFMivgPHEb/yU4M2t0OdW4Sns23V
saeTDRk5NzkNOUV41JDxcLZBXcOx+GrDYfq8voIth+N5eVhHAIJ8XfnrhLKdEndFTWpWAeqcQuN0
yi7A08W+WicXOzKyDZ2r27X3clWiLaYmKuysLcktKCExLQuAiR+vYsSbS1gafrAOfRbq28nZloxs
/e+TkV2Ih1NNO9miriGzencsYe+t4r2f/iKvqNTgHDuOxDO4i/HOFXZuehctuSAD7AwjJ6pHRmE6
NRyTfq+g3fmZQb0eFor+ql4vYTphNSYjPgUb59u3uQl1ZjZebtVbwJ5uzqhrcZz+Ib+giD2HYujS
rqVeeUp6JilpmXRuq5S3DW5KpzYt6DHiBXo88QLdO7amsb/PHfXJyC/F09Gy6tjDwQp1Xpm+znml
eFXKmJqosLM0I7e4Qk9mx6k0BrdV5mxGXikeDjX7tESdb/g/vRV27t7kp1evQQXqFOw89L+L+kIc
zQYozlGzAcOwsLXHylH/fxE8eBRntv8BQHHODVSmpngFK9HR5o8+gb2nr9E6YesGBRnVxwWZSLU5
T5VILR9DvnrEsDyoH/KF3caf9z4i3YXPw8hD6VxV0gxYLMtycyAfeOlunmzzuXzOqMuY0P72d3Va
GdILNbT1tuTPp/xo423JZ9E37ppeGq2WGfOX8nRYH3y9br/18dvWffTq2BJPN6e7ps+Dik//0aTu
2QA6/S1aCxdP7Bu1JONI9XZk49GvcHjGUHYNC+DathV6uVn3ilef6MyeL59laOcmrI48DcCkIe0o
KC5n+AdrWLX7NM39XFGp7u8U1mp1xFy4zucvj2D1nOfZfeQCf5++cueG9cCYfq3Y9cVzbJwzDjdH
Gz77bb9efWxCOpbmpjRt4Frv59adWIvmuzC0kYsw6WG4vaqHyhTJ3hM5ORbNsnHIKXGY9K97fqGx
aDRaZsxZxNMjBuLr7aFXtz3qEI/26lQVXUxKTufKtVT2rlvMvnXfczjmLMfjztfWbb0Tey0XS3MV
TT2Nz0f9t+z+7C38O/Rg4oZj+LfvSX56Mroa+VO2bp64NW3JlQO7qsr+nPEUA97+gufXHKK8uEBP
vl5p/ih4BMHx3/TLbVzAtREkGjpdDyIqqf4/DyMPdM7VHbguy/I/t8mrgJcBvaugJEmTgckAP/74
Izcvge62pqTXiFSpCzV42Bma5FBSMT8ezebXUQ0wN1UWJQ9bU45er96SURdo6OhrjaOlCitTiQFN
lLvV0Ka2rD+Tf8cvs3rzHtZFHACgVdMA0mrclaZn5uLhUrtD9MHXq/D3dufZ4f3veI5T569w4kw8
v23ZR3FpKRUaLTZWFlWJ8P+GfHUq9l4Nqo7tPX3IV6eQr04loGOvGuUNSDy6j3x1CvaePnrl+erU
Op2zNDMVK4/qu0grtwaUZtbeh0//UcR98bJheb8nSYvehKxVxoG5oysOTVqTc07JbUiJXEuXL7fd
UZfVkadZv09JGG7Z0J30GtGV9Jwi3J1s9OTdnWz0IjDq7CI8HPVlAB7r0pQpC7cxfXhHbK3MmTuh
L6AkOPd/YxW+bvYGbap0ijjG+t0xik6B3qRnVY/D9KwC3J2Nv6h5ONuRdiMPTxd7NFodBcWlONpZ
4eFiT/sWfjjZK4Hjnu2acO5KOl1aNapdp92xrN97RtGpoYe+nbILca8RyQJwd7bVi86pswurIn6u
DtX2erJ3S174crNe2+2HLzKkcx2iVgAFmWDvWXUo2bnrRx5uQj67E2mQYT6kHiW5yOUlVQnsuvO7
MW0z7I6qrN64k3VblTatghqTlplVVZeemY2HW+3Rrw8W/IR/Ay+efXKwQd32qL95/9Xnq453HzhG
SItAbKyViFHPTm04dTae9q2b31Y3d3tL0nOro0rqvBI8HCz0ZDwcLEnLLcXT0UoZM6UVOFpXR/u3
n0plSJvqSLO7gyXqvJp9luJhb4mxFGSkYu9ZvQbZefhQoE7RkynMTGP9y6MAMLO2IejR4ZQVVKdc
NB/4JBd3h6PTVF8XUk4d5ten+wDQqGt/nP3rkK9amKkf+bRzQy7MNJTza4/U6RnkNdNAqx/do2lf
JYldd5ecOsFd4WGOXMl3OEaW5SWyLLeXZbn95MmTDTpo5WlJUm45yXkVlGtltl8ooE8j/QvcuYxS
Zu3O4Lswb1ysqx2vbv7WHEwqJq9US16ploNJxXTzt0aSJHo3tuHodSV/5/C1EgKdzbkT4x7vw6bF
77Np8fv069KG8MjDyLLMqfNXsLOxwt3FMAH2q+WbKCgq4d0XRt2xf4Av3prAnpXzifp1Lm9OHElY
v8714lgBXIzaQkjYUwA0COlEWUE+hZnpJBzYReNu/bG0d8TS3pHG3fqTcGAXhZnplBUW0CBESdwO
CXuKi5Gbb3cKA3LPH8OmQSDWXgFIpmb49B9F+oEtBnK2/s0wt3Mi58zfBnU+/fXzsCoKcjC1ccDG
V1lA3Tr0pyDxwh11GdevFRtnj2bj7NH0a9eQ8EMXlf9fQjp2Vua43+Q4uTvaYGtlzqmEdGRZJvzQ
Rfq2VZ7+SkyvzseJOnmVRl5KtDS/uIxyjbLAros+T/tmXnr5WQY6DezAxi+msPGLKfTr0IzwfbGK
TpeSsbO2qDW36lb0ad+M8H1xAOw8fI7OLRsiSRLdQxpz6VoGJWUVaLQ6jp1LovFtIkXj+oew8eNx
bPx4HP0eaUz4wfOKTpfTFJ1uZafLaYqdDp6nbzvFcauZn/XXics0qfHkpE4nE3E0nsGdmxn9HQHk
1LNIzr7g6A0qU1TBoUpCe02cqh16qUkP5Ozr3Ak5PhopQEmYlgI6ImfeObo3bngom5Z9yqZln9Kv
e3vCd0Yrtjobj52NNe613HB9tXQNBUXFvDvtGYO6K0kp5BUU0ja42uH0cnfh2KnzaDRaKjQajsWe
o5ER24KtfB1IulFEcnYx5Rod20+l0aeFfpSsTwt3wk8o23Q7T6fTOdClKg9Up5OJiE1jcE3nyt4S
W0tTTiXlKP/rEyn0Ddbv83aknj6Gs38gjj4BqMzMCB48mkt7turJWDm6VOUwdpv0FrF/LterDx4y
mrPb/tArs3ZWdgRMzMzpMvENYtYsMVon0i+Aoy/YeykRzGb9IeGmrXP3JkgD3kDe9HatuXhSUH/k
C7U/nPQgIrYFFR7myJWfJEldZFn+GxgLHKhrB6YqiZl93Jm4IQWdDCNa2tPE1YJFB7No6WlB38a2
fB59g+IKHa9tVZKavezMWDzMG0crE17s7Myo1crC+lJnZxwrE9dn9HDlrR3pzNubibOVCZ+EGr9A
APTq2JLoY6d5dPxMLC3Mmft69ZM+w16aw6bF75OemcMPf+ygka8nI6YpTw2NG9qHJwd15/TFRKbN
+Z78AiUX69uVW9i6ZFZdzaPHEwtWEtChF9ZOrry+9yp7vpmNialyF3p8zRLi9+2gSc9BvLzrAhWl
JYS/q8QJS/JyiF48l8nrFMdm3+JPKMlT8se2zZ7OsLlLMbW04vL+ncRHR9RJJ1mrJe7LV+iycDuS
iQnXti6n4Oo5gibOIvfCcdIPKAurT//RpOxea9DeytMfK48G3Di5T6/P2PlT6Dh3LbJOR0VBLifn
3mHb5yZ6tfYnOu4aoW+trnwVQ9+quuEfrGHj7NEAfPB0T95ZFkVZuYYerfzo2Vp53caX6w9zNT0X
lQTeLnbMelaJ/CWk5vDO0kgkSSLQ24mPx/cxXqd2TYg+eZnQ6d9iaW7G3KnVif/D//MjG7+YAsDn
K/9i24EzlJRX0HvKQkb2a8u0Ub0Z2bctb32zkdBp3+Bga8WC154AwMHWiuce68yTby9FkqBn20B6
P2JctKhXSADRsYmEvrFCsdPEAdU6zVzNxo/HKXZ6po/yKoYKDT1a+9OzdQAAX/xxgAvXMpEk8HG1
Z9bz/araH7+YgqezHb7udXsqD1mLNuJTTP/vO1Cp0J3aDDeuoOr1AnLqOeT4aFQdRqNq2Am0GuTS
fLSbP6hqbjptK1jYgIkZqma90fz2Ety4ijZqESZhc5AG/Ae5OAftlll1UqtX57ZEHznFo+NewdLC
grlvvVBVN2zCW2xa9inpGVn8sGojjfy8GTFJiaaNGx7Kk48p429b1CGG9O2q96BLaK/OHD55lsfH
v6E4yx1D6NtV/+nL2jA1UTFzWDATfzqKTgcjOjagiacdi3ZeomUDB/oGezCyoy9v/RFL6Py9OFib
sWBc9Stcjl/NxtPRCl8X/VTZD4YH886aOMoqdPQIcqNnkJFPeaLM3YiPX+H/lm5DpTLh1J/LuXH5
HL2mf0jqmRPE79mKf8de9H39Y2RZ5trxA0TMnl7V3sHbH3vPBiQdi9brt8v4GTTpPRhJpeLEH0tI
PLLXaJ2QtchRXyI98SWoVMhntkHWVaSuE5DVFyDhIFLPqWBmhTR0jtKmQK04WqBEUe3c4fop/X7b
jkTqMBZsnJGeWQFX/0beVbfcUMHdRbr56Y0HFUmSZgGFsix/IUlSABABHAceAc4BT8uyfLtHp2Td
j4/dbTXrhGrKVuSre++3GnpIDXszK8jszoL3kFkXKgjv+mDdB4QdUrYNdIe+vs+a6KPq+gq6uNX3
Ww09VK3HoTuy+H6roYeq00tUfNzufquhh9nMGOS0k/dbDT0kL8Uh0m2+ezli/w2qxxfycfMHa52a
eb4C3YLudxa8h6hmHIB7HPw53t+k3p2K9ru1D10A68G6Yt0GWZZn3VSkkWX5qfuhi0AgEAgEAsGt
eGicK4FAIBAIBA82Kunh2A272zyUzpUsy4lAyzvJCQQCgUAguHc8dPt3d4mH+WlBgUAgEAgEggeO
hzJyJRAIBAKB4MHjYX3pZ30jIlcCgUAgEAgE9YiIXAkEAoFAIKgXROBKQThXAoFAIBAI6gWxLagg
tgUFAoFAIBAI6hERuRIIBAKBQFAviIiNgrCDQCAQCAQCQT0iIlcCgUAgEAjqBUnkXAHCuRIIBAKB
QFBPiIR2BUmW/2d+B+h/5osKBAKBQFDJPXV3Lg5S1fu1ttkO3UPnsv1PRa7yX3K93yroYb/4BhSk
3W819LHzIrzrgzUswg5pmBVkdr/V0GPWhQoAdGf+uM+a6KNqOQZdxHv3Ww09VAM/QRez7H6roYeq
3QR034XebzX0UE3die7c+vuthh6qFiMB0EV9fJ810UfVdyarOz5Y69S4oxp0296832rooRry2T0/
50PnBd0lREK7QCAQCAQCQT3yYLn+AoFAIBAIHlokkdEOiMiVQCAQCAQCQb0iIlcCgUAgEAjqBRG4
UhDOlUAgEAgEgvpBeFeA2BYUCAQCgUAgqFdE5EogEAgEAkG9IAJXCiJyJRAIBAKBQFCPiMiVQCAQ
CASCekG8ikFBOFcCgUAgEAjqBeFcKYhtQYFAIBAIBIJ6RESuBAKBQCAQ1A8iZAMI5wqTFn2xfHIu
kqSi/NAqynctqlXOtM1jWE9eTuH8/uiunaoql5x8sH3/IGXbP6d893dKoZU9VuO+QuXdHJApXfky
2qvH66SXLMt88sU37Dt4GEtLS+bPepvgoKa3lH/htXdJTkll69rlAHz1/TIi9x1EpZJwcXJi3qy3
8XBzrXO/NXHvFEqrV78EExOubfmZ+JX6Pwra8uUFuLbrBYCJpTUWTu5sD3XFtV1vWr78RZWcrX8Q
xz8cS3r0Zlwf6UvwtPlIkgpNSREnPx5PUUqCUfqEffITTXsPpigrg8WPt61VZtB7C2nScyAVpSVs
emcCaedOAhAy7Gl6vvAOANE/zCN200oAvILbMWzeMswsLImPjmDHJ68ZpUtNZFlm7s87iI6Jx9Lc
jLnThxHcyNtA7qvVuwnfF0t+USknVlf/2PLyzYdYHxmDiUqFs4M1H780DB93RwAmzVlJ7KVk2jX3
44d3xxmt0/7z6cz98xQ6nczIzg2ZNCBIr75co+WtVcc4dz0HRxtzvny2Mz4uNsQlZfPhmhOV3wum
DmzBgBCfqnZancyTX0Ti7mDJD1O6191OKyKJPnVFsdOLgwhu6Gkgd/ZKOu/8sJ2ycg092zTi3Wf7
IUkSr30dTmJaDgD5RaXY21iycf5zbDlwlp+3Hqtqf/FaBhvmPkvzAA/jbJVYzNzobHQyjAy2ZVJ7
R7365TF5rD9biIkKnK1M+Li/Kz72pqTka5i+LQNZlqnQwVMhdoxpZQ/ApE3pZBZr0eigvbcF7/d2
wURl/PaJLMvMXbaN6BMXsbQwY+70Jwhu7GMg99WqXYTvPUV+UQknfv+wqvyPiCP8tuMIJioJa0sL
PnppGIG+7lRotLz/3UbOXUlFq9UR1qctk5/oZZydzqYwd+1xdLLMyG6BTAptqVdfXqHlrRUHOXct
WxlTE3vi42ILwJKI02w4lIBKknhvdAe6t/Dmanoery/bX9X++o1Cpj8WwrP9mhttJ6/OobSf8SWS
yoTL4T9z7lf9Ncraw5cuH/6CuZ0DksqEU9+9R+qhHXh27E+bqZ9gYmaOtqKck9+8jfr4HgD6fx+J
lasnmrISAKKmD6IsJ9NonfafVzN302l0OhjZ2Y9J/fTX23KNlrd+i+Hc9Twcbcz48pkO+Dhbk5Jd
zJD5kTR0V2wW4u/MrCdDAJj0499k5pei0cm0b+TC+0+0rtN4Etx9HljnSpKkPcB8WZZ31ih7FWgm
y/KL9XMSFVajP6Vo0Ujk3FRs3voLTVwEuvRL+nIWtpj3mYKmFgfJ8ok5aM5F6pc9ORfNuSgqlo4H
EzMwt6qzatEHj5B4PZldG1cTe+Ycs+YtZN2K72uV3RUVjY21/jkmPj2GV1+cAMCvf2zgu59WMPvd
GXXqVw+Vitb/WcShVwZSkpFMr2WHSd+/hYLE81UiZxbNqPq74cipODRtA8CNmL3sfa49AGZ2TvRf
d5HMI38BEPLGtxx5awSFSRcIGPECTZ97l5OfTDDKRqc2ruDo6sUMn/9zrfVNeg7E2T+QRaHNaRDS
iSEffsvS0d2wcnCi99SZLBnZGVmWmbLhCBejtlCan8tjH37LlvdfIDn2COOWbCGwRyiX9++stf9b
ER0TT1JaFhHfvkxsfDKzl2xlzfzJBnK9OzRj7OBODJqm79A3b+jFus8mY2Vhzu8RR/li5S4WzhgF
wPiwbpSWVbDmL+Odda1OZs66kyx7qQcejtaMWhBJn1beBHraV8ms/zsRBytzdr4/iG0x1/liy2kW
PteZJl72rJvRD1MTFRl5JQz/bDd9WnphaqLcnq7cF08jDzsKSyvqZCOA6FNXSErPIWLhJGIvpzF7
2V+s+fhpA7mPft7F7EkDCQn0Ysqn69kfe5WebRqx8JWwKplPV0Zha20BwNDuwQztHgzApWuZTFuw
0WjHSquTmbM3m2XDPfCwNWXUmlT6NLQm0MW8Sqa5mznrxnhhZabi97h8vjiYzcJB7rjZmPDHk16Y
m0oUlet4fHUKfRta425rysJB7thaqJBlmVe2ZxJxuYghTW2Nt1XMJZJSbxCx+HViL11n9o+bWfOZ
4TLYu0MQYwd3ZtDUhXrlj/UMYczATgBEHT3Pp79s56cPnmPnoTOUazRs/vplSsrKeWz61wzp0Rof
d6c72EnHnD+Osuzl/ng4WTNq/g76tG5AoFe1I7r+0GUcrM3ZOXsY245d5YuNMSyc2JPLablsP57E
lveHkpFXzPivd7PjozAaejqw8b3Hqvrv/c4G+rfxNdpGkkpFhzcXETVtIMUZyQxccZjk/VvIv1q9
RrUc/y7XItcRv+FH7Bs2p8/CLYQPC6Qs9wb7Zgyj5EYaDo2C6btoOxsf869qd/CDZ8g+f8JoXart
JDPnzziWvdAVDwcrRi3cR59gT/25d+SaMvfe68+2k8l8sfUsC5/pAICvqw0b/9PHoN+Fz7bH1tJM
GU/LjxERm8KQtg3qrN/dQORcKTzIAbzfgTE3lY2pLK8XTALaocu8ipyVBNoKKk5sxDRkkIGcxdC3
Kf9rEVSU6ZWbhgxCl3UNXdrF6kJLO0wDu1BxaJVyrK2Akvw66xa57yDDBociSRJtWgWTX1BIxo0s
A7mi4mJ+Wb2WFyfoX5RsbW2q/i4pKa0a8Mb2ezNOLTpSlJxAcepVZE0FKbvX4tnj8VvKNxgwhpS/
1hiUe/d9AvXfEWgr7wKRZcxslIXGzMaB0htpd9TlH5KOH6AkL/uW9c36PU5suPJ/SI49gqW9A7Zu
njTu/igJhyIpycuhND+XhEORBPYIxdbNEwtbO5JjjwAQG76KoP5ht+z/VkQdu0BYrzaKjZv6kl9U
SkZOgYFcm6a+uDvZGZR3atUQKwvlYh7S1Bd1VvX46dK6ETZW5gZtbkdcUjZ+brb4utpibqpicDtf
ok6n6ut8JpWwjsrFJDTEh8OXlAiMlblplSNVrtFRc9lMzy1m39k0RnZpWCd9qs554jJhPYIVOzXx
Jr+4lIycQj2ZjJxCCkvKadPEG0mSCOsRTOTxeD0ZWZaJOHyRIV0NIxzbDp1ncNcgg/JbEacuw8/R
FF8HM8xNJAY3sSHqSrGeTCdfK6zMFJuEeFqgLtQCYG4iYW6qWKhcKyPL1W1sLRR5jQ4qtDISdbsA
RR09T1iftoqtmvkpYyrbcF1p08wPd2d7g3Jba8uqv0vKyqvOLklQUlqORqultEyDmakJNlYWd9Qn
LjELPzc7fN3sXpEo9QAAIABJREFUMDc1YXB7f6Jir+vrHHudsM6NAQht58/hC+nIskxU7HUGt/fH
3MyEBq52+LnZEZeovwYdvpCOr6tdVaTLGFyCO1KQnEBh6lV0mgqSdq3Ft+dNa1SN9cbc1oGSyvUm
59Kpqr/zrpzFxMIKlVnd5lltxF3Lwc/VBl8XG2XutfUh6ky6nkzUmTTCOihOZGhrbw7H30CuOXhq
wdbSDACNTqZCq6vzeLqbSFL9fx5GHtjIFbAe+FiSJHNZlsslSQoAvAETSZKigQIgENgDvCTLsq6u
J5AcvdDlVF9k5JxUTAIe0ZNR+bZG5eRD2Zm/MO8/rbrCwgbzAS9T/M1ILPpPrZZ39UcuzMLy6W8w
aRCM9locpevehXL9BfpOqDMz8fR0qzr29HBDnZGJu6uLntzX3//M+KdGY2lpuCAu/G4pm7bvxM7G
hl9//KpO/d6MpZs3JerqxbMkMxmnFh1rlbXy9MPaK4DME1EGdT79R5Pw+1dVxyfnT6Hzgi1oy0rQ
FOUTPanbbfWoC/Ye3uSnJVcd56enYO/hU1l+vUZ5MvYe3th7+JCfnmJQXlfU2QV4ulZf4Dxd7MnI
yq/VkboTGyJj6NGuSZ3b1SQjrwRPx+rIpoejFXFJ+k6pOrcELydFxtREhZ2lGblF5TjZWhCbmMV7
v58gLbuI+U91rHK25v0Zy3/CWlP0X0StoNJOLjXs5GxHRnYB7k7VF9SM7AI8nKvt5uFihzpb31E9
fiEZFwdrArycDc6x4+8LfPuf4UbrlFGoxdO2eln0sDUlTl12S/kN5wrp4V9t27QCDS9sVnMtT8N/
ujnhXqOviZvSOa0up4e/FaGB1kbrBKDOysfTxaHq2NPFnozs/FodqVuxevthVmw+SIVGyy+zxwPw
aJeWRB49T8/x8yktq+Dt8YNxtLuzbhm5xXg6Vd/AeTjZEHf1hr7OucV4OSl9mZqosLMyI7eoDHVu
CSENXWu0tSYjV3993H48kSEdAoz+bgBWbt4U11ijijOScQnWX6PifppNv2920OzJqZhY2RA1LdSg
H9++I8i+eBJdRXlVWZf3l6LTabketZEzP39itE4ZeaW1zL0cPRl1XilejjXnnim5Rcq5U7KLGbFg
LzYWprwyuDntG1Wv0xN/PMTpa7n0CHInNKTu65Tg7vLARq5kWc4GjgL/hJLGAGsBGegITAdaAI2B
EXdFCUnC8ok5lG74wKDKYsiblEf9AGVF+hUqU1S+ranY/wtF8/oilxdh8ejLd0W98xfjuZacyoA+
PWqtf23qRPZtW8fQQQNYtXbjXdGhNnz6jyZ1zwbQ6fu7Fi6e2DdqScaR6m22xqNf4fCMoewaFsC1
bSv0crP+19m8L5YzCalMCKs/h/O/ISTAha3vPMraGf34afcFyiq07DmTirOtBcG+t98+uhdsO3S+
1qhV7OVULC1MaerrVkurf8/mC4WcUZcxoV210+NlZ0r4OB92PuND+IVCbhRrq+qWDvMkekIDyrUy
h5NL74pOt2Pc4M7s+mEGM54J5Yd1ewE4HZ+MiUrFvmVv89cP/+GX8INcT791NPheUK7REhWXTGg7
/zsL15GA0DEkbP2VjUMD2PvaULrOWq4XGnFo1IK20+ZxdF71luvBD55m29i2/DW5N+5tutNw8FP1
rldtuNlbEPn+o/w5ozdvh7XkjVXH9bbfl07pSvSsUMo1Og7HG58DdreRJKnePw8jD6xzVUnNrcGa
W4JHZVm+IsuytrKs1kxaSZImS5J0XJKk40uWLDGol3PTUDlVe/ySkze6vBrbUha2qLyDsHktHNs5
MZg0fATrF1ah8muDSUA7LId/iO2cGMz7TMEi9FXMek1Azk1Fzk1FmxgDgCZmCyq/EKO+7Oq1Gwkb
O4GwsRNwc3UhPb16wqSrM/Fw179InDx9jjPnL9J36GjGTpxO4rVknp78ikG/Qwf1Z1fkPgA83Nzu
2G9tlGamYuVRnf9g5daA0szUWmV9+o8iuZYtQZ9+T5IWvQlZqwHA3NEVhyatyTl3FICUyLU4t+py
R12MJV+dir1XdR6CvacP+eqUynLfGuUNyFenkq9Owd7Tx6DcGFbvOMLwGd8zfMb3uDnZkn6jessm
PSsfdxfjIwwAh2IT+HFDNIvf+T/Mzf5dgNndwYr03JKqY3VuCR4O+jl6Ho5WpOUoMhqtjoLSChxt
9LdFGnvaY21hSnxaHievZrHnTBr9PtrOjBVHOBKfyZu/Hr2jLqt3xTD87eUMf3s5bo62pNfY8kzP
LsDdWT+65+6sH6lSZ+lHsjRaHbuPXmJQF0PnavstnK7b4W5rQnqhpvp8hRo8bEwM5A5dK+HHY3ks
HupRtRWo348pTVzMOZGi70RZmKro28jaYKuxNlZvP8zw175h+Gvf4OZkR3pWXlVdelbdolY1Gdy9
FZFHzwGwNTqW7m2bYGZqgoujLe2C/DiTkHKHHsDd0Zr0nOobS3VOER6ON48pa9JylO+p0eooKKnA
0cYCD0erm9oW4+5YHS3bfzaVFn7OuNrXLVe1JDMV6xprlLV7A0puWqMaP/4813avA+DG6cOoLCyx
cFSiaFbuPvT8bD1/z3qewpQrev0CaIoLSdz5Oy4tOhitk7uDZS1zz1JPxsPBkrTcmnNPg6ONOeam
JjhVzsFgX0d8XWxIzNTfNrcwM6FvS0+DrUbB/edBd67CgX6SJLUDrGVZ/iej8OYN6Vo3qGVZXiLL
cntZlttPnmyYUKxNOonKvRGSix+YmGH2yHA0cRHVAqUFFL7ZjML321H4fju0V09Q/MNT6K6dovjL
oVXl5Xt+pGznV1TsW4acn4EuJwWVeyAApkE99XOybsO4UcMJ/20Z4b8to3/v7mzavhNZljl1+ix2
tjYGW3djR4ZxIGIDUVvW8NvSbwjwa8DKJV8DkHitejsscu9BGgX4AdC3V9c79lsbueePYdMgEGuv
ACRTM3z6jyL9wBYDOVv/ZpjbOZFz5m+DOp/++nlYFQU5mNo4YOOrbHu5dehPQeIFIyxlHBejthAS
ptxlNgjpRFlBPoWZ6SQc2EXjbv2xtHfE0t6Rxt36k3BgF4WZ6ZQVFtAgREn8DQl7iouRm40617hB
ndi44EU2LniRfh2bE77vlGLjS9exs7as05bguStpzPpxC9+9PRYXB+NzTm5FKz8nkjILSc4qolyj
Y3vMdfq09NKT6dPSi/CjSQDsjE2hcxN3JEkiOasIjVaJQKZkF3FFXYCPsw2vD23F3tlDiPxwMAue
7USnJm589kzt28Q1GfdoOzbOf46N85+jX/smhO8/q9gpPhU7awu9LUEAdydbbK3MORWfiizLhO8/
S99HAqvq/z6dSENvZzxd9O2r0yl5WINrcbpuaysPC5JyNSTnVVCuldkeX0SfRvrbZOcyypgVlcV3
Q91xsa52vNILNJRqFFvllWo5kVpKQyczisp1ZBQpDptGJ7MvsZhGTmZ3ttXgzmxcOJ2NC6fTr1Nz
wvecVGx18Zpiqzo4V4mp1Vt2+05cxN9LmfNebo4cOa04EsWl5cReuk4jnzvfbLXydyEpo4DkGwWU
a7RsP55En9b6yed9WvsSflh58ndnTBKdm3kiSRJ9Wvuy/XgS5RVakm8UkJRRQOuA6jVo27GrDGkf
YPR3+4esc8ew8w3ExjsAlakZ/o+OInm//hpVnH4dzw59AbAPCMLE3JKynEzMbB3os3Azp759l8y4
Q1XykokJFg4ulX+b4tN9CHlXzhqtUytfR5Iyi6rn3skU+rTUfyK2T7An4ceU7cydcal0DnRFkiSy
C8vQ6pRL2/WsIpIyi2jgbENRmYaMfMVp12h17DuvppH7v18n6g3pLnweQh7knCtkWS6sfGrwZ/QT
2TtKktQQSAJGA4ZhKWPQaSld8zbW09YhqVSU//0burSLWDz2NtqkU2hOR9y5j1ooXfsOVs//AKZm
6G4kUfLr9Dr30atbZ/YdPMKAYeOwsrRg7odvVdWFjZ1A+G/Lbtt+wTdLuJp0DUmlwsfLg4/eef2O
/d4OWasl7stX6LJwO5KJCde2Lqfg6jmCJs4i98Jx0g9sBZQtwZTdaw3aW3n6Y+XRgBsn9+n1GTt/
Ch3nrkXW6agoyOXk3IlG6QPwxIKVBHTohbWTK6/vvcqeb2ZjYqpctI6vWUL8vh006TmIl3ddoKK0
hPB3lb5L8nKIXjyXyesUB3Df4k8oyVPyILbNns6wuUsxtbTi8v6dxEfXfQz0ateE6JhLhE79Wnls
fuqwqrrhM75n4wJly+HzX3exbf9pSsoq6D1pASP7t2Pa6D58/usuikvLeW2BYkcvVwcWvzMWgKdm
LuNKyg2KS8vpPWkBH78URve2gYZK1MDURMXMJ9ow8fv96HQyIzoH0MTLgUXbz9LS14m+rbwZ2bkh
b606SuicHThYm7PgWcXBPHHlBj/tvoiZiRKe/+DJtjjZ3jnh2Sg7tW1E9KkrhL76E5YWpsydUv0w
yfC3l7Nx/nMAfPD8AN75YQdl5Rp6tGlIzzaNquS2/32h1ujU8QvX8XSxw9fD0aDudpiqJGb2dmZi
uBqdDkYE29LExZxFh3No6W5B30bWfH4wh+IKHa9tzwCUrcDFQz1IyKngs83ZSJLy2orx7Rxo6mrO
jWItU7dkUK6V0cnQqYElo1vVLf+u1yPNiD5xidAXv6x8FUN1JsTw175h40Jljfl8RQTb9scqY2ri
p4zs355pY/rx2/bDHIpLwMxEhb2tFfNeHgnA2EGdeO+bP3ns5a9Blhne9xGaBRi+DsPATiYqZo7p
yMRvIpUx1TWQJt6OLNpyipZ+LvQN8WVkt0DeWn6A0A82KWNqgpK+0MTbkYGP+PPY7M2YqFS8P6Yj
JirlPr+4rIJDF9L4aFznOtkHlPXk+Oev0HfRdiSVCQlblpN35RytJ88i6/xxUvZv5cTXb9D53R8J
GvsKsizz92zlyeRmo6Zi1yCQlhNn0nLiTEB55YKmpIg+i7ajMjVDMjEh/WgklzctNVonUxMVM0e0
ZuKSvxU7dfSjiac9i3acp6WvI31bejGykz9v/RZD6Ce7cbA2Y8EzypPVxxOyWBRxoWruzXoyBEcb
c24UlDJ12RHKNTp0skynQFdGdw2os70EdxfpTk8l3G8kSRoGbASay7J8QZKk3sBs6p7QLue/5HoH
kXuL/eIbUGD803H3BDsvwrs+WD532CENs4LufKd/L5l1Qcl90J354z5roo+q5Rh0Ee/dWfAeohr4
CbqY298M3GtU7Sag+84wmfl+opq6E9259fdbDT1ULRQnTBf18X3WRB9V35ms7vhgrVPjjmrQbXvz
fquhh2rIZ3CPYz/XR1nVu1Phu7bkoYtfPVijsxZkWd6E4eDIl2X5sfuhj0AgEAgEgtp5SPPP650H
PedKIBAIBAKB4KHigY9c3Ywsy3uBvfdZDYFAIBAIBDfxsL46ob4RkSuBQCAQCASCeuShi1wJBAKB
QCB4QBGRK0A4VwKBQCAQCOoJ4VspiG1BgUAgEAgEgnpERK4EAoFAIBDUCyKhXUFErgQCgUAgEAjq
ERG5EggEAoFAUC+IwJWCcK4EAoFAIBDUD8K7AsS2oEAgEAgEAkG9IiJXAoFAIBAI6gURuFKQZLne
f8D6QeV/5osKBAKBQFDJPXV31M/Y1fu11uPXgofOZfufilzpDn93v1XQQ9V5Kro1E++3GnqoRi9F
d+jr+62GHqqur6A788f9VkMPVcsxAMwKMrvPmugz60IFFN+432roY+2K7u9v7rcWeqi6TEf3x4T7
rYYeqjHL0MXvuN9q6KFqMgjgwVynji2532rooeowGd2GF+63Gnqonvjhnp/zfr2KQZKkgcDXgAmw
VJbl+TfVPwd8DqRUFn0ry/LSyrpngZmV5R/Lsrzi3+rzP+VcCQQCgUAg+P8LSZJMgO+AAUAycEyS
pM2yLJ+7SXSNLMvTbmrrDHwItEfZ4TpR2Tbn3+gkEtoFAoFAIBDUC5Ik1fvHCDoCl2VZviLLcjnw
BxBmpMqhwF+yLGdXOlR/AQP/qy9fA+FcCQQCgUAgqBck6W58pMmSJB2v8Zl802l9gOs1jpMry27m
CUmS4iRJWi9Jkm8d29YJsS0oEAgEAoHggUWW5SXAv02y2wL8LstymSRJU4AVQN9/rdwtEJErgUAg
EAgE9cPdCF3dmRTAt8ZxA6oT1wGQZTlLluWyysOlwCPGtv1vEM6VQCAQCASCh5ljQBNJkhpKkmQO
jAE21xSQJMmrxuHjwPnKv3cCj0qS5CRJkhPwaGXZv0JsCwoEAoFAIKgX7sebGGRZ1kiSNA3FKTIB
fpZl+awkSbOB47IsbwZeliTpcUADZAPPVbbNliRpDoqDBjBbluXsf6uTcK4EAoFAIBDUC/frPVey
LG8Htt9U9kGNv98B3rlF25+Bn+tTH7EtKBAIBAKBQFCPiMiVQCAQCASCekH8tqCCiFwJBAKBQCAQ
1CMiciUQCAQCgaB+EKErQDhXyLLM3NXRRMcmYmluytxJAwgOcDeQO3s1g3eW/kVZuYaeIQG8O66n
XuLeLzti+OyPAxz6dhJOdlbkFZXy3tLdXM/Iw8LMlI8n9qdpAxejdNofn83c7VfQyTIj23kyqaev
Xv2xxDzm7UjgkrqIBU8GERrsVlU36dczxCbn087PgR+eCtb7nl9HJhFx9gYmEozp6MXTnev2ElpZ
lpn72wGi45IUW03oR3CAm4Hc2cQM3lkaRVmFhp6t/Xl3bHckSeLrP48QdfIqKknC2d6KeRP64e5k
o9jq5z3Vthrfx2hbybLM3J93EB0Tj6W5GXOnDyO4kbeB3FerdxO+L5b8olJOrH6vqnz55kOsj4zB
RKXC2cGaj18aho+7o2LLOSuJvZRMu+Z+/PDuOKPtFPbJTzTtPZiirAwWP962VplB7y2kSc+BVJSW
sOmdCaSdOwlAyLCn6fmCknMZ/cM8YjetBMAruB3D5i3DzMKS+OgIdnzymtH6gGKnTz77in0H/8bS
0pL5H71HcPNmt5R/4ZU3SU5JZev6VVVlK39fx+q1f2KiUtGrR1fefHUqyalpDB4xlob+for+rYKZ
PfNNo3Wau3p/9Xia2K/2uZeYwTtLd1NWrlXG07geN829k3y25iCHvpmAk50VWw5dZOn2GGRkbCzN
+fCZ3gT5uRprKvbH5zB3xz/zz4NJPWqZfxFXlPk3MojQYKXv82mFfLQ1gcIyLSYqmNLTl8Etlfnx
xvqLnEktxNREorWPLbOGBmJmYvzGgSzLzF3yJ9HHz2NpYcbcV8cSHOhrIPfVr9sIjzpGfmExJ9Z/
VlWempHDOwtXU1BUglan4/Vnh9KrQwty8ot4dd4vnIm/xrB+HXn/xZF1sFP9r1N/J+Tw+a6ryDJY
m5swd3hT/F2s6manlXuIPnUVSwtT5k4eSHBDDwO5s1fVvPNjhLKet2nIu0/3qRpTq3bF8Ntfp1Cp
VPRq05A3/q8XKZl5DHlzOQ29nAAICfRi1vgBxtnpUhZzt8aj08HIDl5M6uWvb6eruczbFs+l9CIW
jG5BaKvqObApJo3v9yQB8GIff4a1U94m8NWuK4SfTCe/RMOJWT2Nts+94H4ltD9o/M9vC0bHJZGU
nkvEZ8/w0fN9mb1iT61yH63Yw+zn+xLx2TMkpeeyPy6pqi4tq4CDZ67h5WJXVbZky3Ga+7kR/sk4
5k8ewLzV+4zSR6uTmbM1gSVPB7Nl2iNsO53J5YwiPRlvBwvmDW/GkFaGF6Lx3Xz4dIThRXPjSTVp
eWVsn/4I215uX7Xo14XouGskqfOImD+Oj57rzeyVtX+nj36NZvbzvYmYP44kdR77T18DYMKgtoTP
GcPG2aPpHRLA4s3Kk69LtsbQ3NeV8DljmD+pH/N+O2C8TjHxJKVlEfHty3z04lBmL9laq1zvDs1Y
8+nNv5gAzRt6se6zyYQvfIlHO7fgi5W7qurGh3Xj05dHGK3LP5zauIJVkx67ZX2TngNx9g9kUWhz
tnzwIkM+/BYAKwcnek+dydLR3fhpVFd6T52Jpb3i6D324bdsef8FFoU2x9k/kMAeoXXSKfrA3yRe
S2ZX+BrmzHyTWXO/uKXsrsi92Fhb65UdPnaCyL0H2LxmBds2rGbCM2Or6vwa+BC+ZgXha1YY7VhB
5dxT5xLx6VN89FwfZv96i/G0Yi+zn+tLxKdPkaTOrRpPUDn3zurPvQZu9vz6znA2fzyWFx/vwIfL
a5/TtaHVyczZlsCSp4LZMrVd5fwr1pPxdrBg3rCmDGmlP4cszUyYP6IpW6e146engpm34wr5JRoA
Hmvtxvbp7dj8UltKK3SsP6E2WieA6OPnSUrNJGLJe3w0bTSzF6+rVa53x2DWfGnoeP+wZhcDe7Th
z0VvsODNZ5n9vdLewtyUl58azBvjjf0ZNoW7tU59tDWBz0cGsfGldgxp7cYP+64ZyNyO6NirJKXn
ELFgPB9NGMDs5btrlfvol93MnjiAiAXjSUrPYX9cIgBHzl0j8kQCm+Y+w9ZPn2P84A5VbXw9HNg4
9xk2zn3GaMdKq5OZs/kSS54LYcurHdkWq+ay+iY7OVow74nmDAnRt1NucQXfRSay5sVHWPvSI3wX
mUheSQUAvYNcWPPiIwgeXO7oXEmSpJUk6ZQkSbGSJMVIktT1Xih2r4iKuUJYtyAkSaJNoBf5xWVk
5OoP/ozcIgpLy2kT6IUkSYR1CyIy5kpV/fzfovnP6G560dDLqdl0atEAgEbezqRk5nMjT3+Rro24
5AL8nC3xdbbC3FTF4FZuRF3Qf+WGj5MlzTxtUNVyg9ClsRM2FiYG5X8cS+Ol3n6oKhu52JrfUZeb
iTp5lbCuzRRbNfYkv7i8dluVlNOmsadiq67NiIy5CoCtVfU5S8oqqsLHiq2UKFojLydSbhQYZSuA
qGMXCOvVRtGpqS/5RaVk5BQYyLVp6ou7k51BeadWDbGyUPQKaeqLOiu/qq5L60bYWNXdTknHD1CS
d+vXpDTr9zix4UpEKDn2CJb2Dti6edK4+6MkHIqkJC+H0vxcEg5FEtgjFFs3Tyxs7UiOPQJAbPgq
gvrX7WIYue8Awx4bqNipdUvyCwrIyLxhIFdUXMwvq9bw4sRn9cp/X7eJyc8/hbm5Yg8XZ6c6nb82
ok5erTH3PG8990rKaRPoWfvc+/0A/xnVjZpToW0TLxxsLAEIaexBenah0TrFpfwz/yyV+dfSjagL
WXoy1fNPfwI2dLUioDLK4m5vgYuNGdnFysWwV1Pnqh+hbeVjhzq/jLoQdeQ0YX07KLYKCiC/qISM
7DwDuTZBAbg7OxiUSxIUFpcCUFBUUiVjbWnBI8GNsDCv2ybG3VqnJKCwVHFIC0u1uNtZ1EmvqBMJ
hHVvUTmmvMkvKiMjR///n5FTSGFJGW0CvZUx1b0FkccvA/DH7lgmDe2IuZliDxcHa4Nz1IW45Hz8
XKyq7dTag6jz+vPOx8mKZl62BuPpYHw2XQOdcbQ2w8HKjK6Bzhy4pNi4jZ8D7vZ1s8294v68oP3B
w5jIVYksy21kWQ5BeUfEvLus0z1FnVOIZ427Xk9n21ono4eTbdWxh7Mt6kqZyJgEPJxsCfLTv4sN
8nXlr+MJAMQlpJOaVYDaiEU+o6AMT4fqSeNhb17nhbg2rmWXsuNMJiN/OMnkX8+QmFVS5z7UuUV4
OlfbwdPJhoycmy6GOUV4ONe0lQ3qGhfMrzYcps/rK9hyOJ6Xh3UEKm11Qrlgxl1RK7bKMe6CqM4u
wNPVvlonF3syajhIdWFDZAw92jX5r9rWBXsPb/LTkquO89NTsPfwqSy/XqM8GXsPb+w9fMhPTzEo
rwvqjEw8PavvjD093FFnZBrIfb34J8Y/PQZLK0u98sSkaxw/GcuTT0/iqQlTiTt7vqouOSWNYWOe
46kJUzkec8p4nXIKbxpPt5h7NceTU825dwUPJ5vbbvltiD5Hj9b+t6y/mYz8cv3552CBuqDc6Pb/
EJdcQIVWxs9J344VWh2b4zLo3qRuzqk6Kw9P1+o2ni6OZGQZOle3YurYgWzZc4Lez37IC7OWMPOF
J+p0/pu5W+vUnLAmTFl1lt5fHGFzrJpJPRrUqb3hem53izFVLePhbFc1phLTczhxMZnRH67m6Y/X
cDohvUouJTOPEe/9ytMfr+H4hWSMISOvDE+H6jHg4WBhtJ3U+WWGY7EebCy4N9R1W9AeyLlVpSRJ
KkmSFkuSdEGSpL8kSdouSdLIyrr5kiSdq/xF6i8qy5ZLkvS9JEmHJUm6IklSb0mSfpYk6bwkSctv
cx5/SZLiJUlyrTznfkmSHq3jd/nXlJRVsGTLcaaP6GxQN+mxRygoLmP4+7+xancszf3dqqJG94MK
rQ4LUxXrX2jLyPaezNx46b7o8eoTndnz5bMM7dyE1ZGnAZg0pB0FxeUM/2ANq3afprmfKyrVvd2x
3rwvljMJqUwI63ZPz/sgcf7iJa5dT2FA314GdVqtlry8fNb+uoQ3X5vKq2++jyzLuLu6sGfHn2z6
Yzlvz5jOjHc/orCwqJbe65eSsgqWbD3B9OGdbilz5HwyG6LPM2NUl7uuT00yCsp5689LfDKsicGc
n701gfb+DrT3N4wu3U2274theL+O7F3xET/MmsxbC1ah0+nuqQ7GsOLvFH58Kpi9/+nE8LaezI+4
cudG9YhGpyOvsJQ/Zo3ljf/ryWvfbkGWZdwcbYj8ajJ/fvIMb4/rzRuLt1FYLByd2vgnQlufn4cR
Y2LBVpIknQIsAS9u/yvSI4AAoAXgjvLbPT9LkuQCDAeCZFmWJUlyrNHGCeiC8ls/m4FuwETgmCRJ
bWT5/7F33vFRVOv/f59N741kE0IggYQaCCBNKQECBlAMIIpSxAJYuVevFSwgYEQF+SqWK4INUBAw
ht4CErq0FAi9BALZTSC9l53fH7NssiQhiQajv3ver1de2Z15ZuazZ84885znnDOjVGkKK4qSLIT4
APgS+B2bnMbxAAAgAElEQVRIUhRl6612QogpwBSAr776ikmd1OXLt8ezetcJAIIDtOhuVHQj6TLy
8KqUpQLwqtRaBtBnqJmsK2nZpKTnMOLtH03LH3znJ1bOGIOnqwORkwff1MugV77Dz8uZ2vByskGX
XXHR6nNK0DZA+lfrbMPg9moLf3A7D96sY3C1PCaR1buSAAgO8DLrYtFl5uPl5mBm7+XmYJah02fk
o3U1twG4/+7WPL1gA1NH9sDRzprIp9RqpSgKg15dhp9nzWW1fNNBVm8/qmoKbIruekWmSncjBy+P
2su5Mvviz/PVmlh+mP2EqTvgTpKjv4azT0WL3Nnblxz9VXL01/DvEVppeTMu/b6LHP1VnL19zZbn
6K/VepzlK9fw8y/q67U6dmiHTpdmWqfTp6H1Ms+2Hos/wfGkUwwc9iBl5eVkZGQyYdILLF38GVqt
F4PDQhFC0Cm4PRqNIDMzC3d3N1NXYXD7tjRv5svF5Mt07NCuek3bE25Tn2q49irXp8xbr70VpuUP
zljJyncewtPVgdNXrvP2Nzv46uXhuDnWfUC0l7O1+fWXXYzWqe5dw3lFZTyz/AQvhrWgs595Pfx8
52UyC0p5d3hgnfa1fP1uVm/ZD0BwUHN01yvatbobWXh51D1AW73tIF+/+zQAXdoFUFxSRmZOPh6u
VbvK68Kd8FMZ+SWc1uUTYiy3ocFNmLL0eK3bLd92jNU71YZacEvvW/x5bg11qsJGn5Fr6pnwdnNi
cPcgtZ638kEjBJm5hbg725t8Q4cALX5erlzSZRLc0vu22rxcbNBlF1UcK7u4zuWkdbbh9wtZZtv2
aOl6my3+JvwzY6EGpz7dgm2BIcAPouZQsg+wSlEUg6IoOuDmSNJsoAhYIoQYBVQeULNOURQFSAT0
iqIkKopiAE6gBmrVoijKYtRM2jPAKzXYLFIUpZuiKN2mTKkYzDxuUAhRs8cSNXssYV1bEr33FIqi
EHcuFSc7G7xuCQa8XB1wtLUm7lwqiqIQvfcUA7u2pLVfE/Z+NpmY+U8QM/8JtO6OrJn1KJ6uDuTk
F1NSVg7Aql0n6NbaF0e72i+qjr5OJGcUkZJZREmZgY2J6Qxo617rdrUR1taDgxfVC/XQpWzT2JDa
GBfWkahZY4iaNYawrgFE7zutltV5HU521tWXlZ01ced1alntO83ALgEAXNJVOIodxy7S0kd1FDkF
lcoq9iTd2viYjc+qomloT6LmP0vU/GcJ69GO6F1xqqYzV3Cyt612bFVNJF1IZeZX6/j8jbF4uDjW
vkEDcHrHOkIixgPQLKQnxbk55KXrOL9nK616D8LW2RVbZ1da9R7E+T1byUvXUZyXS7MQNUsTEjGe
0zFrb3cIAMaNedA00HzQgH78un6zWk4Jx3FydMTL07w7bezDI9mzbS07Nq7hx2+/xL+FH0sXq4Pt
B/Xvy8FDakB7MfkypaVluLm5kpGRSXm5eu6upFzl0uUr+DWreRbquEGdiJr9CFGzH7nl2qulPp3T
VVx7XQLUa2/hU8TMn0jM/Ilo3RxZ867aqLl2I5d/LdzEB1MGE+Bdv+63jk2dSM4orLj+jtf9+isp
MzB1xUkiQrxMMwhvsuqIjj3nM5k3uk2dM9jj7u9L1MLXiFr4GmF3dyR6xyG1rE5dwsnertqxVTXR
1NOVA/Fqg+r8FR3FpaW4/4n6fif8lLOtFbnFZVy8rt4e9p3PoqVn7WOexg3uYhpoHnZXINF7kox1
6hpO9jbVBleOdjbEnbum1qk9SQy8qxUAYd0COZikds1fTM2gtKwcNyc7MnIKKDdm+q6kZZGsz6KZ
V+3l39HXieTrhaRkFKrllKBnQLu6zVztHeTO3nMZZBeWkl1Yyt5zGfQO+vP3AslfQ72a6Yqi7BdC
NAE8gbTa7CttVyaE6AGEAaOBF6jIgN1s/hgqfb75vUZ9Qgh74Gbz3xGoOoq5DoSG+BObcInwV79X
pzhPGmRaN/LtH4marc6Kemdif6Z9rT6KoW8nf/rVMo7jfGoG0xZtQwgI9PVgzlNhddJjaSF4675W
TPrhOAaDwqiuWoK8HPg05hLBvk4MbOtB4tVcpv6URE5hGTtPZ7Bwx2XWT1VnjoxfHM+F6wUUlBjo
P+8gcyJa0yfIjcl9/Xh19Sm+33cVe2sLZo+o/9ii0E4tiE24TPjry42PYqhIYo58ZyVRs8aoZTWh
H9OW7FDLqmNz+nVSp+l/vPoAF3VZaAQ09XBi5kQ1S3P+WibTFscghCCwqRtznhxQd01dg4g9eobw
5z9Rz9/zIyo0vfwlUfOfBeCjH7ayYXcihcWl9J88n9GDuvLCmAF89MNWCopKeGn+zwD4NHHhi2nq
OR//1hIuXL1OQVEJ/SfPZ85zEfTpUnvW4cH5S/HvHoq9WxP+89tFdi6chYWlFQCHVy7i7K5NBPUb
yr+2nqK0qJDo6ZMAKMzOJPaLSKasUrMVu754j8JsNVuxYdZURkQuxtLWjnO7t3A2dnOdywggtM/d
7Nqzn8EPPIydrS2RM6eb1kWMmUj0yu9v/5tG3M/0mZHcP3o8VlZWzJ31FkIIDh2N49MvF2NpaYlG
o+HdN1/F1aVumcPQkBbEJiQT/tpSddp8pWtk5NsriJr9CADvPBbKtMUxxmuvRa3X3hfRh8jKKzLN
PrSwEKyeOaZOmiwtBG8Na8WkpccxGGBUF+P1tyOZ4KaOFdffipMV19/Oy6x/oSubT1zncHIOWYVl
/BqnusfIEUG083Hk3fXnaOpiy6OLEwAY1M6D5/s3r5MmgNBu7Yk9fJLwyXOwtbEm8sVHK8pq6odE
LVRnaX70zVo27Dqi1vOJMxh9by9eGDeU154awTsLV/L9r7sQAt5/caypuyXsyXfJLyimtKyMmAOJ
LJ79LIHNb5+RuVN+atYDQfx7xUk0QuBsZ8l79fRToZ0DiI2/QPjLS9RHs0ypmFU7cvoPREU+BsA7
j4cxbZH6KIa+IQH0C1EbgKNCg3lr0RaGv/EdVhYWvP/0UIQQHD6Vwqdr9mFloUEIwcwnBuFah4yo
pYWGtx5ozaRv4zEoCqPu8iFI68Cn2y4Q3MyZge2akJiSw9Rlx8kpLGXnyessjLnI+hd74mpvxbMD
/Hn48yMAPDfQH1d71Y98tOkcG+LTKCwtp//cfYzu5sMLgwLqVVZ3CvEXD+n4uyLUpNFtDITIUxTF
0fi5LbAH0CqKUl6N7UPARNQuPk/UbsEpwGbAXlGUNCGEC3BBURQP47iq9YqirBZC+Bs/Bxv3ZVpX
g66FQCqQDDyqKErNc99VFMOBz2sx+WvR9Hoew8pJjS3DDM2YxRj2fdLYMszQ3PNvDMdXNLYMMzTB
6o1/ZlurRlZizsxTpVBQdRZgo2LfBMP+hY2twgzN3VMxrHiqsWWYoXlkCYazmxpbhhmaoKEAf08/
dWhRY8swQ9N9CoY1zzS2DDM0D/4X/uKOutwXvG4fVPwBnD5L+8d1NtZnzBWoJ2lidYGVkTWo2akk
4ApwFLVL0AmIFkLYGvfxnz8jWggRCnQHeiuKUi6EeFAI8YSiKN/+mf1KJBKJRCL5E/xDB6A3NLUG
V4qiVH0YSc22BiHEK4qi5BkHsf8OJBrHX/Woxv7xSp8vAcHVratmu11Ar0rf6/+kR4lEIpFIJJI7
wJ2YGrXeOBvQGphtDKwkEolEIpH8/47MXAF/MLgSQnQElt6yuFhRlJ6KovT/06rMj3UQuHWa3QRF
URIb8jgSiUQikUj+HELIAe3wB4MrY2DTuYG11HSsmp8SKJFIJBKJRPI3484/MVEikUgkEsn/BrJb
EKj/628kEolEIpFIJLdBZq4kEolEIpE0DDJzBcjgSiKRSCQSSQPxT33RckMjuwUlEolEIpFIGhCZ
uZJIJBKJRNIwyEcxADJzJZFIJBKJRNKgyMyVRCKRSCSSBkFo5JgrkMGVRCKRSCSShkIOaAdAKIrS
2Br+Kv5nfqhEIpFIJEb+0min4LWABr/X2n948R8Xsf1PZa4MvzzX2BLM0Iz6AsPBLxpbhhmans9h
SFje2DLM0HQah2Hzm40twwzNkPfUDwXXG1fIrdg3YWZbq8ZWYcbMU6UYNk1rbBlmaIa+j2HtS40t
wwzNAwswfDmssWWYoXl2IwCGA583shJzNL2ex3BoUWPLMEPTfQqG0+saW4YZmjbD//qDygHtgBzQ
LpFIJBKJRNKg/E9lriQSiUQikdw55ENEVWTmSiKRSCQSiaQBkZkriUQikUgkDYPMXAEyuJJIJBKJ
RNJQyOAKkN2CEolEIpFIJA2KzFxJJBKJRCJpEIR8FAMgM1cSiUQikUgkDYrMXEkkEolEImkY5Jgr
QAZXEolEIpFIGgj54mYV2S0okUgkEolE0oDIzJVEIpFIJJKGQQ5oB2Rwxe7TN4hcfwaDQWF096ZM
7u9vtr6kzMDrP58g6WourvZWfDw2GF83O0rKDMz89RTHU3LQCMH04a3p0dINgMnfHCM9t4Qyg0I3
f1fejmiDRT1SpYqiELlsF7Hxl7C1sSRy8r108PeqYnfiop5pX2+juKSMfiH+TB8fihCCz345wKpd
x3F3sgPgxYfuITQkgNKyct5eEkNSchrl5QYi+rRjyvDu9dP17RZij57F1saKyOcj6NDSp4rd//24
g+jYBHLyCjmyrOKFvSWlZby+8FeSLqTi6mTHxy+NxtfLFYDTyXpmfLWevMISNEKwau4kbKxrr567
T+qI/CVOPX+9Apg8uK3Z+pKycl5fdoikK5m4Oljz8cRe+Ho4kJCcwYyVR4y/C54f0p7BIb6m7coN
Cg/Ni8HLxZb/Pt2nzmV0s5ze+/D/2LV3P7a2tsx99006tGtTo/0z/36NlKvXWL96mWnZ0p9Wsfzn
X7DQaAjtew+vvfg8KddSGTZqLAEtmgMQ0rEDs956rU6aIt77mtb9h5F/I40vHuhSrc3QNxcQ1G8I
pUWF/DrtKVKTjqnHGTGBfs+o5zH2v+8T/+tSAHw6dGXE+0uwsrHlbOxmNr1Xvxchq+cuAYOiMLqX
P5MHmZeReu4Ok5SShau9NR9P7IGvh4Np/bXMAoa/v43nh7TjyYGtKS4tZ8LCWErKDJQZDISH+DJ1
aPt6aQLYfSqdyLVJap3q4cfkga2q6lqRQFJKtuoTxnfB192edUev8s1vF0x2p3W5rPl3H/w9HXhx
6VGu3ChAoxEMaO/Fy8Pa3nrY22u6VEDkruuqpmBnJnd3M1v/3dEsVh/PwUIjcLezYM5gT3ydrTiZ
Vsy7O9LJKzFgoRE83d2NYW0cAUjJLuXljXqyispp72XDB0O0WFvU008tj1X9lLUlkZMH1+Cn0pi2
uJKfGtdP9VNRB1j12wncnY1+avQ9hIb4A7Bo3SHWxCah0QjeHB9Kn44t6q5p6U5i4y6qvnPKEDoE
aKvRpGfaV5tVTZ0DmD5hgOm1Lcu2HuXHbXFoNBpCOwfw6qOhrNt7km82HDJtf/pKOmvmTKBdi6q/
t1pNX0cTe/gktjbWRL44hg6tmlWx+7+lm4jeeVj1mz9Hmq3btCeOz3/aCgjaBjRl3ivjuJqWwdTI
71EUhdKycsbf35tHht5Tp3KS3HlqvXsJIcqBREAA5cALiqLsu9PC/grKDQqz155myVNd0Drb8PDn
hxjQrgmBWkeTzepD13Cxs2LLq/ewIV7HvE3nWDC2I6sOXQVg7Yu9uJFXwpRv41j1fHc0GsGCsR1x
tLVEURT+vTyRzYl67gvxrrOu2IRLJOuz2PzRROLP65j13Q5Wznykit273+9k1pNhhLTy5un50exO
SKaf0TlNDO/Ck8PuMrPf8vtZSsrKWRs5nsLiUu6ftpT7erXB19O5brqOnSM59QabF75A/NmrzPp6
Ayvfn1TFrn+31owd2p2hUz8zW756xzFcHO3Y8tlUNuw9zrxl21nwn9GUlRt47dMoPpg6grb+3mTm
FmBpUXvrp9ygMHvVMZY81xetqz0Pz49hQMemBHpX/J7V+y/hYmfNlreHsuHoFeatS2TB470I8nFm
1cthWFpoSMsuZOSH2xkQ7GM67tJdZ2mpdSKvqLROZWNWTnv2c+lyClujVxKfeIKZkfNYtfTram23
xvyGg7292bIDh44Q89se1q78Hmtra25kZJrWNW/mS/TK7+utKS7qe35f/gUj535T7fqgfkNwbxHI
p+HtaBbSk/tmfMbiMb2xc3Gj//NvsWh0LxRF4ek1Bzm9Yx1FOVncP+Mz1r39DCnxBxm3aB2BfcM5
t3tLnfSUGxRmr45nybN90Lra8fDHOxkQ7GN+7g5cwsXemi1vhRvP3XEWPN7TtP6DXxPo267iurK2
1PDt831xsLGktNzA+E920bedN5393etcTuUGhdlRJ1gypQdaF1se/nQvAzp4Eah1qtD1ewoudpZs
eaM/G+KuMW/jaRaM78Lwrr4M76oG6GdSc3jhu6O083WmsKScJ0Nb0jPQg5IyA08uOkjsqTT6ta39
xmzStDOdJaOaonW05OGfUhjQ0oFAD2uTTTtPG1Y92gw7Kw0/xWczb/cNFtznja2VYG64F/5u1qTl
lfHgjyn0aWGHs60F8/fc4LGuLtzXxomZMemsOZ7DoyEudS6r2IRkknVZbP7wMdVPfb+TlTPGVLF7
9/udzHpioNFPra3GT3U1sz939QYbD55lXeQ40rLyefKDKDZ9+BgWmtp9Qmz8RZJ1mWye/yTx51OZ
9d12Vr47rqqmb7cza9JgQlr58PRHv7A74RL9QgI4mHSZmCPn+TXyMaytLLmRXQDA8N7tGN67HQBn
rqTzwoLoOgVWALFHTpF8LZ3NX71B/OnLzPpyDSvn/buKXf/u7Rl7X2+GPjPXbPmla+l8vWoHyz94
ARdHe25k5QLg6ebMio+mYm1lSX5hMQ9MncfAHh3w8qj7ObwjyAHtQN3GXBUqitJZUZQQYBrw/h3W
9JeRcCWH5h52+LnbYW2pYViIlh0nr5vZ7DiZTkRXNTsTHuzFgfOZKIrC+bR8ehozVR6O1jjbWXL8
ag4AjrZqzFpmUCgtV+r9IssdRy8Q0bsdQgg6B/qQU1BMWla+mU1aVj55hSV0DvRBCEFE73bEHD1/
2/0KISgsLqWs3EBRSRlWFhY42FnfdhszXYdOExEaoupq3Yyc/GLSMnOr2HVu3QwvN6catu8EQHiv
9hw4fhFFUdgbf542LbS09VdvlG5O9ljUIbhKSM6guacjfk0c1fPX1Y8didfMj3n8GhE91FZveIgv
B86koSgKdtaWpkCqpMxA5TOkyypg14lURt8dUKdyuZWYXXsYcf8QtZw6BZOTm0ta+vUqdvkFBXy7
bCXPTppotvynVb8y5YnxWFur58bD3a3KtvUl+fAeCrMzalzfJuwB4qPVzFlK/EFsnV1w9PSmVZ97
Ob8vhsLsTIpysji/L4bAvuE4enpj4+hESvxBAOKjl9F2UESd9SQkZ9C8iQN+TRzUc9elGTsSU81s
diSmEtFdzdKFh/hy4Gw6iqIAsD3hGs3cHQj0rqhnQggcbIzXXrmBUoP5ea2TrstZNG9ij5+Hvaqr
sw87TujNdZ3QE3GXmnkI7+jNgbPXTbpusiEulWGdVb9hZ21Bz0APQA0A2/u6oMsuqrsmXTHNXazw
c7HC2kIwrLUjO86b+4OefnbYWan1OcTHFn1eOQABbtb4u6n1yMvREg97CzIKy1EUhQNXCgkPUhuS
Ee2ciLlln7Wh+qm2tfuposp+qi0xRy/UsMeK/Q7rGYS1lSXNPF1ornUl4YL+ttuYtj1ynog+7Y2a
mhp9VJ65psw88gqL6RzYVNXUpz0xh88BsGJ7PJOH98DaSq1HHi72VY6xYd8phvWqe+Zxx8ETRAzo
pmpq24Kc/CLSMnKq2HVu2wIv96oN3VVbDvLofb1xcVS1eLiqdd7aytKks6S0DMWgVNm2MRBCNPjf
P5H6do46A5k1rRRCaIQQXwghTgkhtgkhNgohRhvXzRVCJAkhEoQQ84zLvhNCfCmEOCCEuCCE6C+E
+EYIcVII8d1tjvOkEOL/Kn2fLIRYUM/fQlpOEd4utqbvWmcb9NnFZjb6nGJ8XG0AsLTQ4GRrSVZB
KW19nNh58jpl5QZSMgo5cTUXXaVtJ31zjD5zduNgY0F4cN1aOKZjZuTh7V6RPfN2dyQt4xYHkZGH
1q3CRuvuiL6SzfLt8US8uYw3v95Gdr7qyO/tHoidjRX9/rWYsJe+4clhXXF1tKWu6DNy8faouPi9
PZxIy6gaXN1ue58maqvK0kKDk70tWbmFXEq9AcCkOcsY9doiFkfvrdP+0rIL8Xa1M33Xutqhzy40
P2ZWIT5udhXHtLUiK78EgPhLN7j//a1EzN3KjIe7moKt93+J55WITvzRSS/6tHS8vSvOubfWC31a
ehW7T774micnPIKtnfk5uJR8mcPH4nlowmTGP/U8CSdOmtalXE1lxCOPM/6p5zl8NO6PCawGZ21T
clJTTN9zdFdx1voal1+ptDwFZ21TnLW+5OiuVlleV9Kyi/B2q+XcZRdVe+7yi8tYHHOG54a0q7Lf
coPCyA9j6PPWBu5prSWkHlkrMPoE10o+wcWuqk/ILsLHaGPSVWCe4dwUl8qwLlXLI6ewlJ1Jeu4O
bFJ3TflleDtVdDJonSzR55fVaL/mRA59/asGBQm6IkrLFZq7WpFVZMDZRoOlsZJ717LP6tBn5uHt
URHcers7VhvIVPFTlWyWx8QT8eZy3ly83eSn9Jn5eLs7mW1z637rrsmpek1m+3cyabqky+TI6RTG
zFjOhDkrSTyvq3KMTQdPM+zuugdX+hvZeHu6VmjycCHtRnadt0++ls6lq+mMfe0zxrzyKbuPnDKt
S03PImLqfAY+OYenHhzQ+FkriYm6BFd2Qog4IcQpYDEw+za2owB/oD0wAbgbQAjhAYwEOiiK0gmY
U2kbN6PdS8BaYAHQAegohOhcw3F+BoYLIayM358AqvR3CCGmCCEOCyEOL1q0qA4/te6MussHrYsN
D31+iPfXn6Fzcxc0lSLsxU92IXZ6H0rKDBw4X3PG4E7wSFhHts57nKjZ4/B0deDDH3cDkHhBj4VG
sOuTp9j28RN8u+koV9LqfpHfKcrLDRw9dYWP/jWK5bOfYPvBU+xPvH3rtiEI8fdg/bR7+fnlML7e
fori0nJ2Hr+Gu6MNHfz+fLbodpw8fYbLV64yeGBolXXl5eVkZ+fw8w+LeO2l53nxtbdRFAWvJh7s
3PQLv674jjdensrL098lL69+2Yb/H/h880km9g80ZakqY6ERRL0Wxs6ZQ0m8nMGZ1L++fsdfzsLW
WkNrb/PsbVm5gVeWxzG+jz9+HlWDn4Zg7clcjuuLeeouV7PlafllvL4ljffu9TLzU43JIwM7sfWj
iUTNHounqz0f/rSnsSVRZjCQnVfEipljefXRfrz02TqzrGT8uVRsra1o7Vf34PhPayo3kJx6ne8j
n2X+K+N45/NV5OSpDREfT1eiF77Mlq/eIHrHYa5X05PwlyNEw//9A6nLgPZCRVE6Awgh7gZ+EEIE
K7fmwVX6AKsURTEAOiHETuPybKAIWCKEWA+sr7TNOkVRFCFEIqBXFCXReKwTqIFalea5oih5Qogd
wP1CiJOA1c3tbrFbBNyMqhTDL8+ZrfdytjVLz+tzitG62JjZaJ1tSM0qxtvFlrJyA7lFZbjaWyGE
YNr9rU12j355GP8mdmbb2lhZMLC9JzuSrtM7yKOa4qpg+fZ4Vv92HIDgAC26SlkoXUYeXpUyWQBe
t7QA9Rl5aI02TVwqBv0+1D+YZz5eC8D6/afp06kFVpYWeDjb0zWoKccv6vHzqrm1s3zzIVZvP6rq
CmyK7kZFOlt3Ixcv96rdfzWhdXci9Xo23h7OalkWFOHqZIfWw5lu7Zvj5qzecPp1DSLpgo67O7a8
7f68XOzQZVVkO/RZhWhdzM+B1tWO1MxCvF3tjeevFFcH867QVt7O2NtYcjY1m2MXb7DzeCqxJzdS
UlpOXlEZr/3wOx8+1uO2WpavXMPPv6jl3LFDO3S6NNM6nT4NrZenmf2x+BMcTzrFwGEPUlZeTkZG
JhMmvcDSxZ+h1XoxOEydnNApuD0ajSAzMwt3dzdTV2Fw+7Y0b+bLxeTLdOxQNYNTX3L013D2qRhk
6+ztS47+Kjn6a/j3CK20vBmXft9Fjv4qzt6+Zstz9OZdsrfDy8UWXWYt587Fttpzl5CcwZa4q8xb
e5zcwlI0GvVaG9e3YuC5s701PQI92XNST2ufurfmvZxt0WVV8gnZhVV9gostqVlFeLvaVeiytzKt
3xh3jfs6V81azVhznBZN7JnYt37dzV4OluhyK7JK+twytA5VXfe+ywV89XsmPzzUFGvLihtSXrGB
Z35N5cV73Onso2bcXG015BQbKDMoWGoEuhr2eSvLt8ezetcJwOinblTczHUZeXi53eKn3KrxU243
/VRFgPlQaDDPLFCvH62bA7pKGXF9Nfs107TtGKt3qu4/uKX3LZpyq9dktv9ckyZvNycGdw9Sr71W
PmiEIDO3EHejb9p44BT31SFrtXzDXlZvVbvMg4P80KVnVWi6kV2vDJN3Exc6tW6OlaUFzbw98G/q
SXJqOh2Dmlf8Jg8Xgpp7cyTpAuG9Q+q8b8mdo17dgoqi7AeaAJ612d6yXRnQA1gN3A9srrT6Zs7d
UOnzze+3u9oXA4+jZq2+rY+em3Rs5kTy9QJSMgopKTOwMV7PgHbmLZIB7ZoQfVQdC7LleBq9Wrmp
Y5dKyikoUcc17D17AwuNIFDrSH5xGWk56s8oKzew69R1WnrW3kodNyiEqDnjiJozjrC7WhG99ySK
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
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(365, 9)</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_3h&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([0., 2., 3., 4., 5., 6., 7.]),
 array([  1,   7, 143, 140,  60,  10,   4]))</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">submit</span><span class="p">[</span><span class="n">submit</span><span class="p">[</span><span class="s1">&#39;kp_3h&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">2</span><span class="p">]</span>
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
      <th>doy</th>
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
      <th>59</th>
      <td>60</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>4.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>312</th>
      <td>313</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>320</th>
      <td>321</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>324</th>
      <td>325</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>325</th>
      <td>326</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>4.0</td>
      <td>3.0</td>
      <td>5.0</td>
      <td>4.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>347</th>
      <td>348</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>363</th>
      <td>364</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>3.0</td>
      <td>3.0</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="n">df3</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="o">==</span><span class="mi">347</span><span class="p">]</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>347</th>
      <td>348</td>
      <td>2.464767</td>
      <td>127881.098765</td>
      <td>522.528704</td>
      <td>2.53997</td>
      <td>-1.330006</td>
      <td>1.699214</td>
      <td>3.990024</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test</span><span class="o">=</span><span class="n">df3</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>

<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">test[&#39;Np&#39;]=np.log(test[&#39;Np&#39;])</span>
<span class="sd">test[&#39;Vp&#39;]=np.log(test[&#39;Vp&#39;])</span>
<span class="sd">test[&#39;Tp&#39;]=np.log(test[&#39;Tp&#39;])</span>

<span class="sd">test[&#39;B_gsm_x&#39;]=np.log(test[&#39;B_gsm_x&#39;])</span>
<span class="sd">test[&#39;B_gsm_x&#39;]=np.log(test[&#39;B_gsm_y&#39;])</span>
<span class="sd">test[&#39;B_gsm_x&#39;]=np.log(test[&#39;B_gsm_z&#39;])</span>

<span class="sd">test[&#39;Bt&#39;]=np.log(test[&#39;Bt&#39;])</span>
<span class="sd">&#39;&#39;&#39;</span>

<span class="c1">#컬럼추가 테스트</span>
<span class="c1">#test[&#39;VpBt&#39;]=test[&#39;Vp&#39;]*test[&#39;Bt&#39;]</span>
<span class="c1">#test[&#39;BzBt&#39;]=test[&#39;B_gsm_z&#39;]*test[&#39;Bt&#39;]</span>
<span class="c1">#test[&#39;VpBz&#39;]=test[&#39;Vp&#39;]*test[&#39;B_gsm_z&#39;]</span>


<span class="n">model</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/model3/all.pkl&#39;</span><span class="p">)</span> 
<span class="n">pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">test</span><span class="p">)</span>

<span class="c1">#pred=[np.argmax(pred[i]) for i in range(len(pred))]</span>
<span class="n">pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">pred</span><span class="p">)</span>

<span class="n">pred</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">pred</span><span class="p">)</span>
<span class="n">pred</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">10</span><span class="p">)</span>
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
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>3.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>3.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>4.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>3.0</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">pred</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([2., 3., 4., 5., 6., 7., 8.]),
 array([  9, 136, 145,  57,  14,   3,   1]))</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="n">df3</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">index</span><span class="o">==</span><span class="mi">286</span><span class="p">]</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>286</th>
      <td>287</td>
      <td>5.694614</td>
      <td>39468.776398</td>
      <td>429.331914</td>
      <td>-5.610438</td>
      <td>-9.658763</td>
      <td>-10.699728</td>
      <td>15.633935</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>doy</th>
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>6.568691</td>
      <td>70974.987730</td>
      <td>435.201173</td>
      <td>4.184047</td>
      <td>-3.290355</td>
      <td>0.293260</td>
      <td>5.528811</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>NaN</td>
      <td>92265.091503</td>
      <td>452.917019</td>
      <td>-5.357036</td>
      <td>1.432917</td>
      <td>2.607799</td>
      <td>6.739669</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>3.236444</td>
      <td>102699.173913</td>
      <td>432.271358</td>
      <td>-4.204278</td>
      <td>1.299580</td>
      <td>0.754260</td>
      <td>4.562095</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>5.402927</td>
      <td>62405.597561</td>
      <td>401.016503</td>
      <td>-4.045047</td>
      <td>1.256243</td>
      <td>2.040852</td>
      <td>4.945953</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>5.693238</td>
      <td>191180.075949</td>
      <td>485.173248</td>
      <td>-4.749840</td>
      <td>8.694473</td>
      <td>2.731361</td>
      <td>12.872964</td>
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
