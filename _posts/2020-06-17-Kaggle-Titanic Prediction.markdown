---
layout: post
title: Kaggle - Titanic Death Prediction
date: 2020-06-17
description: Titanic
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: DataMining

# Information for the author block
author : Loui
---

<html>
<head><meta charset="utf-8" />

<title>titanic-start (1)</title>

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
<div class="prompt input_prompt">In&nbsp;[634]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># This Python 3 environment comes with many helpful analytics libraries installed</span>
<span class="c1"># It is defined by the kaggle/python docker image: https://github.com/kaggle/docker-python</span>
<span class="c1"># For example, here&#39;s several helpful packages to load in </span>

<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span> <span class="c1"># linear algebra</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span> <span class="c1"># data processing, CSV file I/O (e.g. pd.read_csv)</span>

<span class="c1"># Input data files are available in the &quot;../input/&quot; directory.</span>
<span class="c1"># For example, running this (by clicking run or pressing Shift+Enter) will list all files under the input directory</span>

<span class="kn">import</span> <span class="nn">os</span>
<span class="k">for</span> <span class="n">dirname</span><span class="p">,</span> <span class="n">_</span><span class="p">,</span> <span class="n">filenames</span> <span class="ow">in</span> <span class="n">os</span><span class="o">.</span><span class="n">walk</span><span class="p">(</span><span class="s1">&#39;/kaggle/input&#39;</span><span class="p">):</span>
    <span class="k">for</span> <span class="n">filename</span> <span class="ow">in</span> <span class="n">filenames</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">dirname</span><span class="p">,</span> <span class="n">filename</span><span class="p">))</span>

<span class="c1"># Any results you write to the current directory are saved as output.</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>/kaggle/input/titanic/train.csv
/kaggle/input/titanic/gender_submission.csv
/kaggle/input/titanic/test.csv
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[635]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;../input/titanic/train.csv&#39;</span><span class="p">,</span><span class="n">engine</span> <span class="o">=</span> <span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">test</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;../input/titanic/test.csv&#39;</span><span class="p">,</span><span class="n">engine</span> <span class="o">=</span> <span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">submit</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;../input/titanic/gender_submission.csv&#39;</span><span class="p">,</span><span class="n">engine</span> <span class="o">=</span> <span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">df</span><span class="o">=</span><span class="n">train</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[636]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Sex one hot encoding</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">==</span><span class="s1">&#39;male&#39;</span><span class="p">,</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">==</span><span class="s1">&#39;female&#39;</span><span class="p">,</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">==</span><span class="s1">&#39;male&#39;</span><span class="p">,</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">==</span><span class="s1">&#39;female&#39;</span><span class="p">,</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[637]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[637]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(891, 12)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[638]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">corr</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">corr</span><span class="p">()</span>
<span class="n">ax</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">corr</span><span class="p">,</span><span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span> <span class="c1"># annot is to show numbers in each shell</span>
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
<p><strong>From the above heatmap, age has the highest correlation with Pclass</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Using-SisSp-and-Pclass,-remove-NaN-value-of-Age">Using SisSp and Pclass, remove NaN value of Age<a class="anchor-link" href="#Using-SisSp-and-Pclass,-remove-NaN-value-of-Age">&#182;</a></h1><h1 id="In-this-case,-when-SisSp-8,-only-Nan-age-value-exists,-so-we-have-to-handle-it-differently.-like-using-age-and-Pclass.">In this case, when SisSp 8, only Nan age value exists, so we have to handle it differently. like using age and Pclass.<a class="anchor-link" href="#In-this-case,-when-SisSp-8,-only-Nan-age-value-exists,-so-we-have-to-handle-it-differently.-like-using-age-and-Pclass.">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[639]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#temp=df.groupby([&#39;SibSp&#39;,&#39;Pclass&#39;])[&#39;Age&#39;].transform(&#39;mean&#39;)</span>
<span class="n">temp</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;SibSp&#39;</span><span class="p">,</span><span class="s1">&#39;Pclass&#39;</span><span class="p">])[</span><span class="s1">&#39;Age&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">temp</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[639]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>SibSp  Pclass
0      1         39.181416
       2         31.934220
       3         27.630201
1      1         37.414154
       2         27.363636
       3         24.912698
2      1         37.200000
       2         19.125000
       3         18.875000
3      1         22.000000
       2         30.000000
       3          8.875000
4      3          7.055556
5      3         10.200000
8      3               NaN
Name: Age, dtype: float64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[640]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Age</span><span class="o">.</span><span class="n">isnull</span><span class="p">(),</span><span class="s1">&#39;Age&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;SibSp&#39;</span><span class="p">,</span><span class="s1">&#39;Pclass&#39;</span><span class="p">])</span><span class="o">.</span><span class="n">Age</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="s1">&#39;mean&#39;</span><span class="p">)</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Age</span><span class="o">.</span><span class="n">isnull</span><span class="p">(),</span><span class="s1">&#39;Age&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;Sex&#39;</span><span class="p">,</span><span class="s1">&#39;Pclass&#39;</span><span class="p">])</span><span class="o">.</span><span class="n">Age</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="s1">&#39;mean&#39;</span><span class="p">)</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Age</span><span class="o">.</span><span class="n">isnull</span><span class="p">(),</span><span class="s1">&#39;Age&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;SibSp&#39;</span><span class="p">,</span><span class="s1">&#39;Pclass&#39;</span><span class="p">])</span><span class="o">.</span><span class="n">Age</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="s1">&#39;mean&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="I-think-Cabin-column-has-to-be-removed,-since-there-is-too-many-missing-value">I think Cabin column has to be removed, since there is too many missing value<a class="anchor-link" href="#I-think-Cabin-column-has-to-be-removed,-since-there-is-too-many-missing-value">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[641]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Cabin&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">test</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Cabin&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="there-are-two-more-missing-data-in-Embarked-column">there are two more missing data in Embarked column<a class="anchor-link" href="#there-are-two-more-missing-data-in-Embarked-column">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[642]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Embarked</span><span class="o">.</span><span class="n">isnull</span><span class="p">()]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[642]:</div>



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
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>61</th>
      <td>62</td>
      <td>1</td>
      <td>1</td>
      <td>Icard, Miss. Amelie</td>
      <td>1</td>
      <td>38.0</td>
      <td>0</td>
      <td>0</td>
      <td>113572</td>
      <td>80.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>829</th>
      <td>830</td>
      <td>1</td>
      <td>1</td>
      <td>Stone, Mrs. George Nelson (Martha Evelyn)</td>
      <td>1</td>
      <td>62.0</td>
      <td>0</td>
      <td>0</td>
      <td>113572</td>
      <td>80.0</td>
      <td>NaN</td>
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
<p>they are all survived, so I will take most Embarked S 'cause S has the most number of survivor.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[643]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">countplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;Survived&#39;</span><span class="p">,</span><span class="n">hue</span><span class="o">=</span><span class="s1">&#39;Embarked&#39;</span><span class="p">,</span><span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[643]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f3580fb8ac8&gt;</pre>
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
<div class="prompt input_prompt">In&nbsp;[644]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Embarked</span><span class="o">.</span><span class="n">isnull</span><span class="p">(),</span><span class="s1">&#39;Embarked&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;S&#39;</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[645]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">i</span><span class="o">=</span><span class="mi">0</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;S&#39;</span><span class="p">,</span><span class="s1">&#39;C&#39;</span><span class="p">,</span><span class="s1">&#39;Q&#39;</span><span class="p">]:</span>
    <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Embarked</span><span class="o">==</span><span class="n">col</span><span class="p">,</span><span class="s1">&#39;Embarked&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">i</span>
    <span class="n">i</span><span class="o">+=</span><span class="mi">1</span>
    
<span class="n">i</span><span class="o">=</span><span class="mi">0</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;S&#39;</span><span class="p">,</span><span class="s1">&#39;C&#39;</span><span class="p">,</span><span class="s1">&#39;Q&#39;</span><span class="p">]:</span>
    <span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Embarked</span><span class="o">==</span><span class="n">col</span><span class="p">,</span><span class="s1">&#39;Embarked&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">i</span>
    <span class="n">i</span><span class="o">+=</span><span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><p>now there is no more missing data</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[646]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">test</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[646]:</div>



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
      <th>PassengerId</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>892</td>
      <td>3</td>
      <td>Kelly, Mr. James</td>
      <td>0</td>
      <td>34.5</td>
      <td>0</td>
      <td>0</td>
      <td>330911</td>
      <td>7.8292</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>893</td>
      <td>3</td>
      <td>Wilkes, Mrs. James (Ellen Needs)</td>
      <td>1</td>
      <td>47.0</td>
      <td>1</td>
      <td>0</td>
      <td>363272</td>
      <td>7.0000</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>894</td>
      <td>2</td>
      <td>Myles, Mr. Thomas Francis</td>
      <td>0</td>
      <td>62.0</td>
      <td>0</td>
      <td>0</td>
      <td>240276</td>
      <td>9.6875</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>895</td>
      <td>3</td>
      <td>Wirz, Mr. Albert</td>
      <td>0</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>315154</td>
      <td>8.6625</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>896</td>
      <td>3</td>
      <td>Hirvonen, Mrs. Alexander (Helga E Lindqvist)</td>
      <td>1</td>
      <td>22.0</td>
      <td>1</td>
      <td>1</td>
      <td>3101298</td>
      <td>12.2875</td>
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
<h4 id="From-my-point-of-view,-there-will-be-some-correlation-between-survived-and-name.">From my point of view, there will be some correlation between survived and name.<a class="anchor-link" href="#From-my-point-of-view,-there-will-be-some-correlation-between-survived-and-name.">&#182;</a></h4><h4 id="I-mean,-name-has-words-like-Mr.-,-Miss.-,-Mrs.-,-we-could-use-those-things.">I mean, name has words like Mr. , Miss. , Mrs. , we could use those things.<a class="anchor-link" href="#I-mean,-name-has-words-like-Mr.-,-Miss.-,-Mrs.-,-we-could-use-those-things.">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[647]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Mr</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mr\.&#39;</span><span class="p">)]</span>
<span class="n">Miss</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Miss\.&#39;</span><span class="p">)]</span>
<span class="n">Mrs</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mrs\.&#39;</span><span class="p">)]</span>
<span class="n">kid</span> <span class="o">=</span> <span class="n">df</span><span class="p">[(</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mr\.&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Miss\.&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mrs\.&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[648]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># it has to be changed to string &#39;0&#39;,&#39;1&#39;.. since, if it is changed to int directly, a next contatins functions can not works.</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mr\.&#39;</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;0&#39;</span> <span class="c1"># Mr. ==0</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mrs\.&#39;</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;1&#39;</span> <span class="c1"># Mrs. ==1</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Miss\.&#39;</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;2&#39;</span> <span class="c1"># Miss. ==2</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;0&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;1&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;2&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;3&#39;</span> <span class="c1"># another. ==3</span>

<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;0&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;1&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;2&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">2</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;3&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">3</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[649]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mr\.&#39;</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;0&#39;</span> <span class="c1"># Mr. ==0</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Mrs\.&#39;</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;1&#39;</span> <span class="c1"># Mrs. ==1</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;Miss\.&#39;</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;2&#39;</span> <span class="c1"># Miss. ==2</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;0&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;1&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">contains</span><span class="p">(</span><span class="s1">&#39;2&#39;</span><span class="p">)</span><span class="o">==</span><span class="kc">False</span><span class="p">),</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;3&#39;</span> <span class="c1"># another. ==3</span>

<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;0&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;1&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;2&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">2</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Name</span><span class="o">==</span><span class="s1">&#39;3&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">3</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[650]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">Mrs</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">+</span><span class="n">Mr</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">+</span><span class="n">Miss</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">+</span><span class="n">kid</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>891
891
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[651]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">countplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;Survived&#39;</span><span class="p">,</span><span class="n">hue</span><span class="o">=</span><span class="s1">&#39;Name&#39;</span><span class="p">,</span><span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[651]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f3581186eb8&gt;</pre>
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
<div class="prompt input_prompt">In&nbsp;[652]:</div>
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

    <div class="prompt output_prompt">Out[652]:</div>



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
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>2</td>
      <td>1</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
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
<h4 id="the-last-thing-to-handle-is-Ticket">the last thing to handle is Ticket<a class="anchor-link" href="#the-last-thing-to-handle-is-Ticket">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[653]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">(),</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;0&#39;</span> <span class="c1"># if Ticket consist of numeric only, then allocate 0</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">(),</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;0&#39;</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[654]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># check the parsing is possible or not using copied data frame temp</span>
<span class="n">temp</span> <span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span>
<span class="n">temp</span><span class="p">[</span><span class="n">temp</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)</span><span class="o">.</span><span class="n">str</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span> <span class="c1"># only LINE </span>
<span class="n">temp</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">temp</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)</span><span class="o">.</span><span class="n">str</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">(),</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)</span><span class="o">.</span><span class="n">str</span><span class="p">[:</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">lst</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
<span class="n">lst</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[654]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([&#39;A/5&#39;, &#39;PC&#39;, &#39;STON/O2.&#39;, &#39;PP&#39;, &#39;A/5.&#39;, &#39;C.A.&#39;, &#39;A./5.&#39;, &#39;SC/Paris&#39;,
       &#39;S.C./A.4.&#39;, &#39;A/4.&#39;, &#39;CA&#39;, &#39;S.P.&#39;, &#39;S.O.C.&#39;, &#39;SO/C&#39;, &#39;W./C.&#39;,
       &#39;SOTON/OQ&#39;, &#39;W.E.P.&#39;, &#39;STON/O&#39;, &#39;A4.&#39;, &#39;C&#39;, &#39;SOTON/O.Q.&#39;,
       &#39;SC/PARIS&#39;, &#39;S.O.P.&#39;, &#39;A.5.&#39;, &#39;Fa&#39;, &#39;CA.&#39;, &#39;LINE&#39;, &#39;F.C.C.&#39;, &#39;W/C&#39;,
       &#39;SW/PP&#39;, &#39;SCO/W&#39;, &#39;P/PP&#39;, &#39;SC&#39;, &#39;SC/AH&#39;, &#39;A/S&#39;, &#39;A/4&#39;, &#39;WE/P&#39;,
       &#39;S.W./PP&#39;, &#39;S.O./P.P.&#39;, &#39;F.C.&#39;, &#39;SOTON/O2&#39;, &#39;S.C./PARIS&#39;,
       &#39;C.A./SOTON&#39;], dtype=object)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[655]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># convert to int</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">df</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">),</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span> <span class="n">df</span><span class="p">[(</span><span class="n">df</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">)]</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)</span><span class="o">.</span><span class="n">str</span><span class="p">[:</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">isnull</span><span class="p">(),</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;Line&#39;</span>
<span class="n">lst</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
<span class="nb">print</span><span class="p">(</span><span class="n">lst</span><span class="p">)</span>
<span class="n">i</span><span class="o">=</span><span class="mi">0</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">lst</span><span class="p">:</span>
    <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df</span><span class="o">.</span><span class="n">Ticket</span><span class="o">==</span><span class="n">col</span><span class="p">,</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">i</span>
    <span class="n">i</span><span class="o">+=</span><span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;A/5&#39; &#39;PC&#39; &#39;STON/O2.&#39; &#39;0&#39; &#39;PP&#39; &#39;A/5.&#39; &#39;C.A.&#39; &#39;A./5.&#39; &#39;SC/Paris&#39;
 &#39;S.C./A.4.&#39; &#39;A/4.&#39; &#39;CA&#39; &#39;S.P.&#39; &#39;S.O.C.&#39; &#39;SO/C&#39; &#39;W./C.&#39; &#39;SOTON/OQ&#39;
 &#39;W.E.P.&#39; &#39;STON/O&#39; &#39;A4.&#39; &#39;C&#39; &#39;SOTON/O.Q.&#39; &#39;SC/PARIS&#39; &#39;S.O.P.&#39; &#39;A.5.&#39; &#39;Fa&#39;
 &#39;CA.&#39; &#39;Line&#39; &#39;F.C.C.&#39; &#39;W/C&#39; &#39;SW/PP&#39; &#39;SCO/W&#39; &#39;P/PP&#39; &#39;SC&#39; &#39;SC/AH&#39; &#39;A/S&#39;
 &#39;A/4&#39; &#39;WE/P&#39; &#39;S.W./PP&#39; &#39;S.O./P.P.&#39; &#39;F.C.&#39; &#39;SOTON/O2&#39; &#39;S.C./PARIS&#39;
 &#39;C.A./SOTON&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[656]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># convert to int</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">test</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">),</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span> <span class="n">test</span><span class="p">[(</span><span class="n">test</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">isnumeric</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">)]</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)</span><span class="o">.</span><span class="n">str</span><span class="p">[:</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">isnull</span><span class="p">(),</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span><span class="s1">&#39;Line&#39;</span>
<span class="n">lst</span> <span class="o">=</span> <span class="n">test</span><span class="o">.</span><span class="n">Ticket</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
<span class="nb">print</span><span class="p">(</span><span class="n">lst</span><span class="p">)</span>
<span class="n">i</span><span class="o">=</span><span class="mi">0</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">lst</span><span class="p">:</span>
    <span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Ticket</span><span class="o">==</span><span class="n">col</span><span class="p">,</span><span class="s1">&#39;Ticket&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">i</span>
    <span class="n">i</span><span class="o">+=</span><span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;0&#39; &#39;A/4&#39; &#39;W.E.P.&#39; &#39;SC/PARIS&#39; &#39;STON/O2.&#39; &#39;PC&#39; &#39;C&#39; &#39;A/5.&#39; &#39;SC/AH&#39; &#39;C.A.&#39;
 &#39;W./C.&#39; &#39;SOTON/O.Q.&#39; &#39;STON/O&#39; &#39;SC/A.3&#39; &#39;F.C.C.&#39; &#39;F.C.&#39; &#39;A./5.&#39; &#39;PP&#39;
 &#39;STON/OQ.&#39; &#39;SOTON/OQ&#39; &#39;CA&#39; &#39;SC/A4&#39; &#39;S.O./P.P.&#39; &#39;CA.&#39; &#39;S.O.C.&#39; &#39;SOTON/O2&#39;
 &#39;AQ/4&#39; &#39;A.&#39; &#39;SC&#39; &#39;A/5&#39; &#39;SC/Paris&#39; &#39;LP&#39; &#39;AQ/3.&#39; &#39;S.C./PARIS&#39; &#39;A.5.&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[657]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#test set has only one missing value in Fare, so i handle it using mean value of Pclass 3&#39;s Fare value.</span>
<span class="n">test</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">test</span><span class="o">.</span><span class="n">Fare</span><span class="o">.</span><span class="n">isnull</span><span class="p">(),</span><span class="s1">&#39;Fare&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">test</span><span class="p">[</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;Pclass&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">3</span><span class="p">][</span><span class="s1">&#39;Fare&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="now-we-have-handled-all-the-columns,-let's-predict!">now we have handled all the columns, let's predict!<a class="anchor-link" href="#now-we-have-handled-all-the-columns,-let's-predict!">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Prediction-Part">Prediction Part<a class="anchor-link" href="#Prediction-Part">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">classification_report</span><span class="p">,</span> <span class="n">confusion_matrix</span>
<span class="n">x_train</span><span class="p">,</span> <span class="n">x_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Survived&#39;</span><span class="p">,</span><span class="s1">&#39;PassengerId&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Survived&#39;</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2020</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Firstly,-sklearn's-logistic-regression-model">Firstly, sklearn's logistic regression model<a class="anchor-link" href="#Firstly,-sklearn's-logistic-regression-model">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.linear_model</span> <span class="kn">import</span> <span class="n">LogisticRegression</span>
<span class="n">sk_model</span><span class="o">=</span><span class="n">LogisticRegression</span><span class="p">()</span>
<span class="n">sk_model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sk_prediction</span><span class="o">=</span><span class="n">sk_model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">sk_confusion</span><span class="o">=</span><span class="n">confusion_matrix</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">sk_prediction</span><span class="p">)</span>
<span class="n">sk_confusion</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s2">&quot;sk_score : &quot;</span><span class="p">,(</span><span class="n">sk_confusion</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">+</span><span class="n">sk_confusion</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="mi">1</span><span class="p">])</span><span class="o">/</span><span class="p">(</span><span class="n">sk_confusion</span><span class="o">.</span><span class="n">sum</span><span class="p">()))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>From here, LightGBM</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">classification_report</span><span class="p">,</span> <span class="n">confusion_matrix</span>
<span class="n">x_train</span><span class="p">,</span> <span class="n">x_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Survived&#39;</span><span class="p">,</span><span class="s1">&#39;PassengerId&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Survived&#39;</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2020</span><span class="p">)</span>

<span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
<span class="n">lgb_test</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_test</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">params</span><span class="o">=</span><span class="p">{</span>
    <span class="s2">&quot;objective&quot;</span> <span class="p">:</span> <span class="s2">&quot;binary&quot;</span><span class="p">,</span>
    <span class="c1">#&quot;num_class&quot; :2,</span>
    <span class="s1">&#39;boosting&#39;</span> <span class="p">:</span> <span class="s2">&quot;gbdt&quot;</span><span class="p">,</span>
    <span class="s1">&#39;num_tree&#39;</span> <span class="p">:</span> <span class="mi">1000</span><span class="p">,</span>
    <span class="s1">&#39;learning_rate&#39;</span> <span class="p">:</span> <span class="mf">0.05</span><span class="p">,</span>
    <span class="s1">&#39;max_depth&#39;</span> <span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
    <span class="s1">&#39;featrue_fration&#39;</span><span class="p">:</span> <span class="mf">0.9</span><span class="p">,</span>
    <span class="s1">&#39;caterogical_feature&#39;</span> <span class="p">:</span> <span class="p">[</span><span class="s1">&#39;Pclass&#39;</span><span class="p">,</span><span class="s1">&#39;Name&#39;</span><span class="p">,</span><span class="s1">&#39;Sex&#39;</span><span class="p">,</span><span class="s1">&#39;Ticket&#39;</span><span class="p">,</span><span class="s1">&#39;Embarked&#39;</span><span class="p">,</span><span class="s1">&#39;PassengerId&#39;</span><span class="p">]</span>
    <span class="c1">#&#39;early_stopping_rounds&#39;: 5</span>
<span class="p">}</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lgb_model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">train_set</span><span class="o">=</span><span class="n">lgb_train</span><span class="p">,</span><span class="n">params</span><span class="o">=</span><span class="n">params</span><span class="p">,</span><span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lgb_prediction</span><span class="o">=</span><span class="n">lgb_model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">lgb_prediction</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">lgb_prediction</span><span class="p">)</span>
<span class="n">lgb_confusion</span><span class="o">=</span><span class="n">confusion_matrix</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">lgb_prediction</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">lgb_confusion</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;lgb_score : &quot;</span><span class="p">,(</span><span class="n">lgb_confusion</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">+</span><span class="n">lgb_confusion</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="mi">1</span><span class="p">])</span><span class="o">/</span><span class="p">(</span><span class="n">lgb_confusion</span><span class="o">.</span><span class="n">sum</span><span class="p">()))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>From here, XGboost</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[658]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">xgboost</span> <span class="kn">import</span> <span class="n">XGBClassifier</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">classification_report</span><span class="p">,</span> <span class="n">confusion_matrix</span>
<span class="n">x_train</span><span class="p">,</span> <span class="n">x_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Survived&#39;</span><span class="p">,</span><span class="s1">&#39;PassengerId&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Survived&#39;</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2020</span><span class="p">)</span>
<span class="c1">#xgb_train = df.drop([&#39;PassengerId&#39;,&#39;Survived&#39;],axis=1)</span>
<span class="c1">#xgb_test=df[&#39;Survived&#39;]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[659]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_model</span><span class="o">=</span><span class="n">XGBClassifier</span><span class="p">()</span>
<span class="n">xgb_model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[659]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>XGBClassifier(base_score=0.5, booster=None, colsample_bylevel=1,
              colsample_bynode=1, colsample_bytree=1, gamma=0, gpu_id=-1,
              importance_type=&#39;gain&#39;, interaction_constraints=None,
              learning_rate=0.300000012, max_delta_step=0, max_depth=6,
              min_child_weight=1, missing=nan, monotone_constraints=None,
              n_estimators=100, n_jobs=0, num_parallel_tree=1,
              objective=&#39;binary:logistic&#39;, random_state=0, reg_alpha=0,
              reg_lambda=1, scale_pos_weight=1, subsample=1, tree_method=None,
              validate_parameters=False, verbosity=None)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[660]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_prediction</span><span class="o">=</span><span class="n">xgb_model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[661]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_confusion</span><span class="o">=</span><span class="n">confusion_matrix</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">xgb_prediction</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">xgb_confusion</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;xgb_score : &quot;</span><span class="p">,(</span><span class="n">xgb_confusion</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">+</span><span class="n">xgb_confusion</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="mi">1</span><span class="p">])</span><span class="o">/</span><span class="p">(</span><span class="n">xgb_confusion</span><span class="o">.</span><span class="n">sum</span><span class="p">()))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[[89 16]
 [23 51]]
xgb_score :  0.7821229050279329
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[667]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_submit</span><span class="o">=</span><span class="n">xgb_model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">test</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;PassengerId&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[668]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_submit</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">([</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;PassengerId&#39;</span><span class="p">],</span><span class="n">xgb_submit</span><span class="p">])</span><span class="o">.</span><span class="n">T</span>
<span class="n">xgb_submit</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;Unnamed 0&#39;</span><span class="p">:</span> <span class="s1">&#39;Survived&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">xgb_submit</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[668]:</div>



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
      <th>PassengerId</th>
      <th>Survived</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>892</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>893</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>894</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>895</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>896</td>
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
<div class="prompt input_prompt">In&nbsp;[669]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;xgb_prediction1.csv&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
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
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
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
