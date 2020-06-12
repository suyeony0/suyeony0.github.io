---
layout: post
title: Bike Sharing - Additional Try, after 22, May.
date: 2020-06-12
description: Kaggle's Bike Sharing - Additional Try.
thumbnail: food1.jpg
categories: DataMining

# Information for the author block
author : Loui
---

<html>
<head><meta charset="utf-8" />

<title>Bike Sharing - After 22,May</title>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">google.colab</span> <span class="kn">import</span> <span class="n">drive</span>
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
<pre>Go to this URL in a browser: https://accounts.google.com/o/oauth2/auth?client_id=947318989803-6bn6qk8qdgf4n4g3pfee6491hc0brc4i.apps.googleusercontent.com&amp;redirect_uri=urn%3aietf%3awg%3aoauth%3a2.0%3aoob&amp;response_type=code&amp;scope=email%20https%3a%2f%2fwww.googleapis.com%2fauth%2fdocs.test%20https%3a%2f%2fwww.googleapis.com%2fauth%2fdrive%20https%3a%2f%2fwww.googleapis.com%2fauth%2fdrive.photos.readonly%20https%3a%2f%2fwww.googleapis.com%2fauth%2fpeopleapi.readonly

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
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">xgboost</span> <span class="k">as</span> <span class="nn">xgb</span>
<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">RandomForestRegressor</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_squared_log_error</span> <span class="k">as</span> <span class="n">msle</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_train</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Kaggle/Bike Sharing/Dataset/train.csv&#39;</span><span class="p">,</span><span class="n">parse_dates</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">],</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">,</span><span class="n">encoding</span><span class="o">=</span><span class="s1">&#39;UTF-8&#39;</span><span class="p">)</span>
<span class="n">df_test</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Kaggle/Bike Sharing/Dataset/test.csv&#39;</span><span class="p">,</span><span class="n">parse_dates</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">],</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">,</span><span class="n">encoding</span><span class="o">=</span><span class="s1">&#39;UTF-8&#39;</span><span class="p">)</span>
<span class="n">sample_submission</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Kaggle/Bike Sharing/Dataset/sampleSubmission.csv&#39;</span><span class="p">,</span><span class="n">parse_dates</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">],</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">,</span><span class="n">encoding</span><span class="o">=</span><span class="s1">&#39;UTF-8&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="o">=</span><span class="n">df_train</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">test</span><span class="o">=</span><span class="n">df_test</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;day&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;dayofweek&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">dayofweek</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">hour</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;minute&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">minute</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;second&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">second</span>

<span class="n">test</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span>
<span class="n">test</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span>
<span class="n">test</span><span class="p">[</span><span class="s1">&#39;day&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span>
<span class="n">test</span><span class="p">[</span><span class="s1">&#39;dayofweek&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">dayofweek</span>
<span class="n">test</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">hour</span>
<span class="n">test</span><span class="p">[</span><span class="s1">&#39;minute&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">minute</span>
<span class="n">test</span><span class="p">[</span><span class="s1">&#39;second&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">second</span>
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
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Numeric-EDA">Numeric EDA<a class="anchor-link" href="#Numeric-EDA">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="p">(</span><span class="n">ax1</span><span class="p">,</span><span class="n">ax2</span><span class="p">)</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span><span class="mi">10</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">sca</span><span class="p">(</span><span class="n">ax1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">rotation</span><span class="o">=</span><span class="mi">30</span><span class="p">,</span><span class="n">ha</span><span class="o">=</span><span class="s1">&#39;right&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">sca</span><span class="p">(</span><span class="n">ax2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">rotation</span><span class="o">=</span><span class="mi">30</span><span class="p">,</span><span class="n">ha</span><span class="o">=</span><span class="s1">&#39;right&#39;</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;temp&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;count&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">ax1</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">train</span><span class="p">,</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;windspeed&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;count&#39;</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span><span class="n">ax2</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[10]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f9b7929b828&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABJIAAAJgCAYAAADRZ0k3AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjEsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+j8jraAAAgAElEQVR4nOzdeZhcRbn48e+bEAIJ2SCBiQkhiLjgAmhAEEQERWQLICCLLIpEEXADh0Wv21UvxgUVBUFBwQ0VRFBQLy5cV/RGRES4/kQEYUhDWAKEVUL9/qjqpDNMenpmuqenJ9/P88xzus85XVPddZY676mqEyklJEmSJEmSpP6MaXcGJEmSJEmS1BkMJEmSJEmSJKkhBpIkSZIkSZLUEANJkiRJkiRJaoiBJEmSJEmSJDXEQJIkSZIkSZIasla7MzAU06dPT3Pnzm13NiRJkiRJkkaNP/7xj/eklGb0tayjA0lz585l0aJF7c6GJEmSJEnSqBERt61umV3bJEmSJEmS1BADSZIkSZIkSWqIgSRJkiRJkiQ1xECSJEmSJEmSGmIgSZIkSZIkSQ0xkCRJkiRJkqSGGEiSJEmSJElSQwwkSZIkSZIkqSEGkiRJkiRJktSQtdqdAUmSJEmSNDJ1d3dTqVTo6upi4cKF7c6ORgADSZIkSZIkqU+VSoWenp52Z0MjiF3bJEmSJEmS1BADSZIkSZIkSWqIgSRJkiRJkiQ1pOWBpIgYGxF/iogflvebRsTvI+LmiPh2RKxd5o8v728uy+e2Om+SJEmSJElq3HC0SHoHcFPN+48DZ6SUngXcDxxd5h8N3F/mn1HWkyRJkiRJ0gjR0kBSRMwG9gS+XN4HsAtwcVnlAmDf8np+eU9ZvmtZX5IkSZIkSSNAq1skfQboBp4q7zcAlqaUnizv7wBmldezgNsByvIHyvqSJEmSJEkaAVoWSIqIvYC7U0p/bHK6CyJiUUQsWrJkSTOTliRJkiRJUh2tbJG0A7BPRNwKXETu0vZZYGpErFXWmQ30lNc9wMYAZfkU4N7eiaaUzk0pzUspzZsxY0YLsy9JkiRJkqRaLQskpZROTSnNTinNBQ4Gfp5SOgz4BXBAWe1I4LLy+vLynrL85yml1Kr8SZIkSZIkaWCG46ltvZ0MvDsibiaPgXRemX8esEGZ/27glDbkTZIkSZIkSauxVv+rDF1K6Wrg6vL6FmDbPtZ5DDhwOPIjSZIkSZKkgWtHiyRJkiRJkiR1oGFpkSRJkiRJkjQcuru7qVQqdHV1sXDhwnZnZ9QxkCRJkiRJUgczcLKqSqVCT09P/ytqUAwkSZIkSZLUwQycaDg5RpIkSZIkSZIaYoskSZIkSVpDdWqXqE7NtzQaGEiSJEmSpDVUp3aJamW+DVJJ9RlIkiRJkiSpaFWQygCVRgsDSZIkSZIktVintv6SenOwbUmSJEmSJDXEQJIkSZIkSZIaYiBJkiRJkiRJDXGMJEmSJEmSNOwcgLwzGUiSJEmSJEnDzgHIO5OBJEmSJElS09naRBqdDCRJkiRJkprO1ibS6GQgSZIkSZKkNVTlUzfVXb78/idWTOut23Xi85qaL41cPrVNkiRJkiRJDTGQJEmSJEmSpIYYSJIkSZIkSVJDWjZGUkSsA/wSGF/+z8UppQ9ExFeBVwAPlFWPSildFxEBfBbYA3ikzL+2VfmTJEmSJI1Mfzzv7rrLH39w+YppvXVfcvSGTc2XpNYOtv04sEtKaVlEjAN+HRE/Ksvek1K6uNf6rwU2L38vBc4uU0mSJEmSJI0ALQskpZQSsKy8HVf+Up2PzAcuLJ+7JiKmRsTMlNLiVuVRkiRJkkaz/77onrrLH3noqRXTeuvudvD0puZLUudq6RhJETE2Iq4D7gauSin9viz6aERcHxFnRMT4Mm8WcHvNx+8o83qnuSAiFkXEoiVLlrQy+5IkSZIkSarRyq5tpJSWA1tFxFTg0oh4AXAqUAHWBs4FTgY+PIA0zy2fY968efVaOEmSJEmStMJNZ9/V7zpPPLB8xbTe+s87dqOm5UvqJMPy1LaU0lLgF8DuKaXFKXsc+AqwbVmtB9i45mOzyzxJkiRJkiSNAC0LJEXEjNISiYhYF3g18H8RMbPMC2Bf4IbykcuBIyLbDnjA8ZEkSZIkSZJGjlZ2bZsJXBARY8kBq++klH4YET+PiBlAANcBby3rXwnsAdwMPAK8sYV5kyRJkiSpI1Q+cVvd5cvvf3LFtN66Xe/ZpKn50pqplU9tux7Yuo/5u6xm/QQc16r8SJIkSZIkaWhaOti2JEmSJElrgtvOqNRd/uTS5Sum9dbd5F1dTc2XOkd3dzeVSoWuri4WLlzY7uysloEkSZIkSZKkNqtUKvT0jPxnjg3LU9skSZIkSZLU+QwkSZIkSZIkqSF2bZMkSZIkSR3jrs/+tu7y5UsfWzHtb92N3vGypuVrTWEgSZIkSZLUUaZNnLHKVNLwMZAkSZIkSeoox+xyWruzIK2xHCNJkiRJkiRJDbFFkiRJkiSNcN3d3VQqFbq6uli4cGHT0p0yacYqU0nqj4EkSZIkSRrhKpUKPT09TU/39Xu8t+lpShrd7NomSZIkSZKkhhhIkiRJkiRJUkPs2iZJkiRJGrBffW1J3eWPPrR8xbTeui8/fGSNz7TBhBmrTDV4d33m2rrLly99fMW03robvfPFTc1Xu9z9+SvrLl++9JEV03rrbnj8Hk3N10AZSJIkSZIkqTh+p1PbnQVpRLNrmyRJkiRJkhpiIEmSJEmSJEkNMZAkSZIkSZKkhjhGkiRJkiRJ6tP0CRusMpUMJEmSJEmSpD6duu3x7c6CRpiWdW2LiHUi4g8R8eeI+GtEfKjM3zQifh8RN0fEtyNi7TJ/fHl/c1k+t1V5kyRJkiRpOE1fdzobTexi+rrT250VaUha2SLpcWCXlNKyiBgH/DoifgS8GzgjpXRRRHwROBo4u0zvTyk9KyIOBj4OvL6F+ZMkSZIkaVicuN2pLUu7GpwySNV63d3dVCoVurq6WLhwYbuz0xYtCySllBKwrLwdV/4SsAtwaJl/AfBBciBpfnkNcDHw+YiIko4kSZIkjUqXXnxPv+ssW/bUimm99fc7wEDCmujUbU5sdxbWGJVKhZ6ennZno61a+tS2iBgbEdcBdwNXAf8AlqaUniyr3AHMKq9nAbcDlOUPAI7mJUmSJEmSNEK0dLDtlNJyYKuImApcCjx3qGlGxAJgAcCcOXOGmpwkSZIkNYVdXiStCVraIqkqpbQU+AWwPTA1IqoBrNlAtU1YD7AxQFk+Bbi3j7TOTSnNSynNmzFjRsvzLkmSJEmNqHZ5qVQq7c6KJLVMK5/aNqO0RCIi1gVeDdxEDigdUFY7ErisvL68vKcs/7njI0mSJEmSpDXBjImT6Zo4jRkTJ7c7K3W1smvbTOCCiBhLDlh9J6X0w4i4EbgoIj4C/Ak4r6x/HvC1iLgZuA84uIV5kyRJkiRJGjFO2+GA/ldajbu/8L2m5GHD4/bvd51WPrXtemDrPubfAmzbx/zHgANblR9JkiRJkiQNzbCMkSRJkiRJkqTOZyBJkiRJkiRJDTGQJEmSJEmSpIYYSJIkSZIkSVJDWvnUNkmSJEmSpGE1Y8LUVaZqLgNJkiRJkjTCTZ40Y5WppNU7dfuj2p2FUc1AkiRJkiSNcPP3fm+7syBJgIEkSZIkSWuQ7u5uKpUKXV1dLFy4cECfveB7S+ouf3DZ8hXTeuseuf+a0apo6nozVplKGh0MJEmSJElaY1QqFXp6etqdjTXCEbvZikoajXxqmyRJkiRJkhpiiyRJkiRJkjTsZqw7bZWpOoOBJEmSJEmSNOxO3X5Bu7OgQbBrmyRJkiRJkhpiIEmSJEmSJEkNsWubJEmSRo2hPNpdkiT1z0CSJEmSRg0f7S5JUmvZtU2SJEmSJEkNMZAkSZIkSZKkhti1TZIkSWqA4y9JktTCQFJEbAxcCGwEJODclNJnI+KDwDHAkrLqaSmlK8tnTgWOBpYDb08p/aRV+ZMkSZIGwvGXOsMZl1bqLl+6bPmKab1137VfV1PzJUmjRStbJD0JnJhSujYiJgF/jIiryrIzUkqfrF05IrYADgaeDzwD+GlEPDultLyFeZQkSZKkplhv8oxVppI0GrUskJRSWgwsLq8fioibgFl1PjIfuCil9Djwz4i4GdgW+F2r8ihJkiSNdnbJGz6v3ue97c6CJLXcsAy2HRFzga2B35dZx0fE9RFxfkRMK/NmAbfXfOwO6geeJEmSJPWj2iWvUqnf5UuSpEa0PJAUEesBlwDvTCk9CJwNbAZsRW6x9KkBprcgIhZFxKIlS5b0/wFJkiRJkiQ1RUsDSRExjhxE+kZK6XsAKaW7UkrLU0pPAV8id18D6AE2rvn47DJvFSmlc1NK81JK82bMsO+xJEmSJEnScGlZICkiAjgPuCml9Oma+TNrVtsPuKG8vhw4OCLGR8SmwObAH1qVP0mSJEmSJA1MK5/atgNwOPCXiLiuzDsNOCQitgIScCvwFoCU0l8j4jvAjeQnvh3nE9skSZIkSZJGjlY+te3XQPSx6Mo6n/ko8NFW5UmSJEmSJEmD18oWSZIkSZIa0N3dTaVSoauri4ULF7Y7O5IkrZaBJEmSJKnNKpUKPT1Pe86MJGmY3X3mz+suX7700RXTeutueMIuTc3XSNJQICkifpZS2rW/eZIkSVKn2u+Sq+suX7YsXzwsXvZo3XUvfd3OzcuUJEkjTN1AUkSsA0wApkfENFaOeTQZmNXivEmSJEmrmH/xT+ouf3jZIwDcueyRuutedsBrmpovdY51J09fZSpJGpj+WiS9BXgn8Azgj6wMJD0IfL6F+ZIkSZI0gnXquE7bzT+13VmQpI5WN5CUUvos8NmIOCGldOYw5UmSJElSgw685Pq6y5cuewKAxcueqLvud1/3ogH9X8d1kqQ1U0NjJKWUzoyIlwFzaz+TUrqwRfmSJEnSKNaprVk0PNw+JGnkanSw7a8BmwHXAcvL7AQYSJIkSdKA2ZpF9bh9SNLI1VAgCZgHbJFSSq3MjCRJkiRJkkauRgNJNwBdwOIW5kWSJGlUspuOJEkaLRoNJE0HboyIPwCPV2emlPZpSa4kSZJGEbvpSJKk0aLRQNIHW5kJSZIkaTR73SXX1F3+4LLHAFi87LG6617yuu2ami9Jkgaq0ae2/U+rMyJJkiRJkqSRrdGntj1EfkobwNrAOODhlNLkVmVMkiRJkiRJI0ujLZImVV9HRADzAdvVSpIktZkDeQ+fmDSVMWUqSdKaqtExklZIKSXg+xHxAeCU5mdJkiRJjXIg7+EzcZ/D2p0FSZLartGubfvXvB0DzAMea0mOJEmS1NH2ufgH/a7zyLKHAbhz2cN117/8gL2blq811ZhJ01aZSpI0FI22SKo9gz8J3Eru3iZJkiSNGGMmTeGpMlU2eZ9jB/W513/vlrrL71v2bwAWL/t3v+t+e/9nDioPkqSRp9Exkt7Y6oxIkiS1k2MNjQ7r7n1Qu7MgSdKoNqaRlSJidkRcGhF3l79LImJ2qzMnSZI0XKpjDVUqlXZnRZIkacRqKJAEfAW4HHhG+ftBmbdaEbFxRPwiIm6MiL9GxDvK/PUj4qqI+HuZTivzIyI+FxE3R8T1EfHiwX8tSZIkSZIkNVujYyTNSCnVBo6+GhHv7OczTwInppSujYhJwB8j4irgKOBnKaXTI+IU8pPfTgZeC2xe/l4KnF2mkiRJI9peF3+t7vLHlj0EwJ3LHqq77g8POLyp+ZJGqlMurf+kwXuWPbliWm/d0/eb1dR8SZL612gg6d6IeAPwrfL+EODeeh9IKS0GFpfXD0XETcAs8iDdO5fVLgCuJgeS5gMXppQScE1ETI2ImSUdSZLUZI4JpP64jQwfn6wmSeoUjQaS3gScCZwBJOC35JZFDYmIucDWwO+BjWqCQxVgo/J6FnB7zcfuKPNWCSRFxAJgAcCcOXMazYIkSS3ViRfc1TGBpNVxGxk+6+3js20kSZ2h0TGSPgwcmVKakVLakBxY+lAjH4yI9YBLgHemlB6sXVZaH6UB5JeU0rkppXkppXkzZswYyEclSWoZB2qWJEnSmqDRFkkvSindX32TUrovIrbu70MRMY4cRPpGSul7ZfZd1S5rETETuLvM7wE2rvn47DJPkiRpjbXXxRfVXb7q+EurX/eHBxzc1HxJkqQ1U6MtksZUn64G+clr9BOEiogAzgNuSil9umbR5cCR5fWRwGU1848oT2/bDnjA8ZEkSZIkSZJGjkZbJH0K+F1EfLe8PxD4aD+f2QE4HPhLRFxX5p0GnA58JyKOBm4DDirLrgT2AG4GHgHsKC5JkjRKxaTJq0wlSVJnaCiQlFK6MCIWAbuUWfunlG7s5zO/BmI1i3ftY/0EHNdIfiRJktTZ1t17/3ZnQZIkDUKjLZIogaO6wSNJkiRJkiSNXg0HkiRJ0vDr7u6mUqnQ1dXFwoUL250dSVph7OTpq0wlSWsGA0mSJI1glUqFnh4fYipp5Jmyz7vanQVJUhsYSJIkSWuEPS85r+7yx5c9CMCdyx7sd90rXnd00/LVTntffEnd5Y8uWwbAncuW1V33Bwe8rqn5kiRJI5eBJEmSRqk9Lj297vInlt0PwJ3L7q+77pX7ndLUfK2JYtJ6q0wlSZI6lYGkIXLsCkmS1J/xe+/W7ixIkiQ1hYGkIXLsCkka/V77/eP7XeeJh5cA0PPwkrrr/2jfzzctXyOZN1okSZJGJwNJkiSp6Vp5o8UglTT6jZ88Y5WpJGnkMJAkSZI6iq2BVxWTJq0ylUaD58zvbncWJKlPMyZMWWW6JjKQJEmS1MHG771Hu7MgSdIa47QdDm13FtpuTLszIEmSJEmSpM5giyRJktpoj++/r+7yJx6+F4A7H7637rpX7vuRpuZLkiRJ6ostkiRJkiRJktSQNaZFkk94kSR5LpAGxoG8JUlSb2tMIMknvEhS83RqQMZzgTQw6+y9T7uzIEmSRpg1JpAkSWoeAzKjxOR1iDKVJEmSGmEgSZKkNdTa81/S7ixIkiSpwxhIkiSNKJ3abS4mjSOV6Zpgz+99pu7yx5ctBeDOZUvrrnvF/u/sI+2z+0n7gZL2A3XXvWL/Y+um01tMmrjKVJIkSU9nIEmSNKJ0are5cfvOaXcWNERr77NLu7MgSZI04o1pVcIRcX5E3B0RN9TM+2BE9ETEdeVvj5plp0bEzRHxt4h4TavyJUmSJEmSpMFpWSAJ+Cqwex/zz0gpbVX+rgSIiC2Ag4Hnl8+cFRFjW5g3SZIkSZIkDVDLurallH4ZEXMbXH0+cFFK6XHgnxFxM7At8LsWZU+SNAq99vK96i5/4uHHAOh5+M666/5onx82NV9DMml8frLapPHtzokkSZLUljGSjo+II4BFwIkppfuBWcA1NevcUeZJkrRGW3vfLdqdBUmSJGmFVnZt68vZwGbAVsBi4FMDTSAiFkTEoohYtGTJkmbnT5IkSZIkSasxrC2SUkp3VV9HxJeAat+BHmDjmlVnl3l9pXEucC7AvHnzUmtyKklrtvd9t68h7la6d9m/y7Sn7rofOfDHTc2XJEmSpPYa1hZJETGz5u1+QPWJbpcDB0fE+IjYFNgc+MNw5k2SJEmSJEn1taxFUkR8C9gZmB4RdwAfAHaOiK2ABNwKvAUgpfTXiPgOcCPwJHBcSml5q/ImSWqft32vfmunu0trp7uX9dRd96z9be0kSZIkDbdWPrXtkD5mn1dn/Y8CH21VfiRJ0ugQkyesMpUkSdLwacdT2yRJ0igXk9ddZdpMa++zU9PTlCRJUmMMJEmS1hgxOUhlqtZae5/t250FSZIktYCBJEnSGmPcfuPbnQVJkiSpow3rU9skSZIkSZLUuWyRJEmjVHd3N5VKha6uLhYuXNju7EiSJEkaBQwkSdIoValU6OnpaUna4ycFkMpUkiRJ0prCQJIktVknthzaYq/WnT7GTc5BqnEOiC1JkiSNOAaSJKnNWtlyqBNtvI+nJkmSJGmkcrBtSZIkSZIkNcRAkiRJkiRJkhpiIEmSJEmSJEkNMZAkSZIkSZKkhjiiqSR1qI9f9Jq6y+9/6Mky7el33ZMP/knT8iVJkiRp9LJFkiRJkiRJkhpiIEmSJEmSJEkNMZAkSZIkSZKkhhhIkiRJkiRJUkMcbFuSWuzMb9Qf6HppGRR76UM9ddc94TAHxJYkSZLUXrZIkiRJkiRJUkMMJEmSJEmSJKkhLQskRcT5EXF3RNxQM2/9iLgqIv5eptPK/IiIz0XEzRFxfUS8uFX5kqTB6O7u5ogjjqC7u7vdWWnYupOCCZPzVJIkSZKaoZUtkr4K7N5r3inAz1JKmwM/K+8BXgtsXv4WAGe3MF+SNGCVSoWenh4qlUq7s9Kwl+wxlh1fvxYv2WNsu7MiSZIkaZRoWSAppfRL4L5es+cDF5TXFwD71sy/MGXXAFMjYmar8iZJkiRJkqSBG+6ntm2UUlpcXleAjcrrWcDtNevdUeYtppeIWEButcScOXNal1NJHae7u5tKpUJXVxcLFy5sd3YkSZIkadQZ7kDSCimlFBFpEJ87FzgXYN68eQP+vKTGdGJQptr9TJIkSZLUGsMdSLorImamlBaXrmt3l/k9wMY1680u8yS1iUEZSZIkSVJvrRxsuy+XA0eW10cCl9XMP6I8vW074IGaLnCSJEmSJEkaAVrWIikivgXsDEyPiDuADwCnA9+JiKOB24CDyupXAnsANwOPAG9sVb4kqS9fuvA1dZc/+NCTZdpTd91jjvhJU/MlSZIkSSNJywJJKaVDVrNo1z7WTcBxrcrLUCz54rl1ly9/4IEV03rrznjrgqbmS9LoMWG9AFKZSpIkSdLI1bbBtiVJ2Q67j213FiRJkiSpIQaSJA2rTnwanCRJkiQpM5AkaVgN5WlwF361/jhGDz34ZJn21F33iKMcx0iSJEmSBsNAktRirWyBY+seSZIkSdJwMpCkjtGpQZOhtMBpVdo/OP+1/a7z8INPlGlP3fX3ftOPBvz/JUmSJEmdyUCSOkYrAzKSJEmSJKl/BpJGsE5tgdOp+ZbqmTAxgFSmkiRJkrRmGhWBpCVnf73fdZY/8NCKab31Zxz7hqbla6g6tQVOp+ZbqueVu41tdxYkSZIkqe3GtDsDkiRJkiRJ6gyjokWSpJHju1/Zve7yZQ/+u0x76q574Bt/POD/PXG93P0sTyVJkiRJzWYgSdKosdur7H4mSZIkSa1k1zZJkiRJkiQ1xBZJ0hD96kt71V3+6IOPlemdddd9+TE/fNq8q768R920H3nwiTK9s+66r37zlXXT6cvk8pSyyT6lTJIkSZJUGEiSgO7ubiqVCl1dXSxcuLDd2RkR9t91XLuzIEmSJEkaYQwkSUClUqGnp6fd2ZAkSZIkaURzjCRJkiRJkiQ1xBZJkobVpPXy2Et5KkmSJEnqJAaSJA2rvXb1sCNJkiRJncorOo0YN31hft3lTzzwcJne2e+6zzvusqblS5IkSZIkZW0JJEXErcBDwHLgyZTSvIhYH/g2MBe4FTgopXR/O/InSZIkSZKkp2vnYNuvTCltlVKaV96fAvwspbQ58LPyXup4UycE608Kpk5wTCBJkiRJUmcbSV3b5gM7l9cXAFcDJ7crMxpdFn1x77rLH3/g0TK9s+668976gwH/7yNeOX7An2nUlIkAUaaSJEmSJLVWuwJJCfjviEjAOSmlc4GNUkqLy/IKsFFfH4yIBcACgDlz5gxHXtXLv848uO7yJ5feV6aVuuvOOeGipuZrTXTwK9dudxYkSZIkSWuQdgWSdkwp9UTEhsBVEfF/tQtTSqkEmZ6mBJ3OBZg3b16f60iSJEmSJKn52jJGUkqpp0zvBi4FtgXuioiZAGV6dzvyJkmSJEmSpL4NeyApIiZGxKTqa2A34AbgcuDIstqRgM9vlyRJkiRJGkHa0bVtI+DSiKj+/2+mlH4cEf8LfCcijgZuAw5qQ96G1V1nf7Lu8uUP3L9iWm/djY49qan5kiRJkiRJ6suwB5JSSrcAW/Yx/15g1+HOjyRJkiRJkhrTrsG2pRFl2sRYZSpJkiRJkp7OQJI6xgYTxgBPlWlzvXmndZqepiRJkiRJo42BJHWM43dct91ZkCRJkiRpjWYgaQ3V3d1NpVKhq6uLhQsXtjs7kiRJkiSpAxhIWkNVKhV6enranQ1JkiRJktRBmj/YjCRJkiRJkkYlA0mSJEmSJElqiF3b1HTTy1PVprfg6WqSJEmSJKl9DCSp6U7aYWq7syBJkiRJklrAJiOSJEmSJElqiIEkSZIkSZIkNcRAkiRJkiRJkhriGEmj1OKzTqm7fPkD96yY1lt35ttOb2q+JEmSJElS57JFkiRJkiRJkhpiIEmSJEmSJEkNMZAkSZIkSZKkhqwxYyTNmLDeKtNOMGPCuqtMJUmSJEmS2mmNCSS9d6fXtDsLA3bqTtu2OwuSJEmSJEkr2LVNkiRJkiRJDRlxgaSI2D0i/hYRN0dE/WfYa9CmTxhP13rjmT5hfLuzIkmSJEmSOsSI6toWEWOBLwCvBu4A/jciLk8p3djenI0+p7z8Oe3OgiRJkiRJ6jAjrUXStsDNKaVbUkpPABcB89ucJ0mSJEmSJDHCWiQBs4Dba97fAby0TXlpyIyJE1eZSpIkSZIkjVaRUmp3HlaIiAOA3VNKby7vDwdemlI6vmadBcCC8vY5wN8G8C+mA/c0KbvDka5pD1+6pj28aXdinjs17U7Ms2kPX7qmPXzpmvbwpt2Jee7UtDsxz6Y9fOma9vCla9rDl+6akvYmKaUZfS0YaS2SeoCNa97PLvNWSCmdC5w7mMQjYlFKad7gsze86Zr28KVr2sObdifmuVPT7sQ8m/bwpWvaw5euaQ9v2p2Y505NuxPzbNrDl65pD1+6pj186Zr2yBsj6X+BzSNi04hYGzgYuLzNeZIkSZIkSRIjrEVSSunJiDge+AkwFjg/pfTXNmdLkiRJkiRJjLBAEkBK6UrgyhYlP6gucW1M17SHL13THt60OzHPnZp2J+bZtIcvXdMevnRNe3jT7sQ8d2ranZhn0x6+dE17+NI17eFLd41Pe0QNti1JkiRJkqSRa6SNkb7l5F4AACAASURBVCRJkiRJkqQRykDSGiAiot15GGla8ZtEREv3J8vx6fxNOpdlNzpYjqvnbyO1X3l4j0YBj6kabSJixA0zNBCjJpAUEZMiYmrN+6YdbCJi3Wal1UfaG0TEZyLi2U1Od2pE7BkRE1KT+y+2cqOPiMkRsXErgjIRMSUijomIcc38TUoZfg54ebPz3eJy3KCZ6fVKu5XlOC0i9ouIsc3+TVopIibUvG7m8amlJ6EWVtzWLumPbVH6HaXF55lWVr7XKv+jFfv6NhGxTrPTbaWIWD8iTm72eaaT1R77mpzuOyJi14h4RnnfzONqS+pmnSwixrco3ZaUY9kXPwfs34z0hlNEHBURG5fXza5Xdlo5tqweXNLfNSKmNzvdknYnluOCiHhxREwp75tVjlMiYm6nBQMj4u3V80Cz66sR8RHghIiY3OR0p0TEZq1u4ACjJJAUEScBfwDOjogzqrOblPb+wB8iYs/yvmm/WUTsC1wNrAvcExHjmpTu24FFwHHAORExs0npToiIs4EFragYlnJcBHwOOKfZ6QMfAz4BHFX+35C3kYh4NfAz8r70F5o4gH0Ly3FiRHwKuDIiPhoRu5b5Tdm2h6EczwM+Duxd/l8zLx5e3YID+qER8QfgMxHxToBmVYYi4mTg3Ig4pFUXay0IYM6MiL8AF1T/RTPTL/+j6eVYk/b61X2liRWslp1noPllCBARz4qI64H/qv6bJqa9f0T8k3wBOKlZ6fb6H60ox/eQHxayAbC82RXmiHhdRMxpVl2hV9ofjojdyutmHlM/BHwxImY3Mc2dIuI6YGfyeeAj0NTjakvqZjXpd2I5/ifw4YiY0cQ0X96qciz1kB8AbwCqx9Vm749HRsQLWlBnOBr4InA8QErpqSam3Wnl2JJ6cEn79RFxA/Bu4MLq+beJ6XdaOe5afo99yL/326Bp5XgC8GfyddjHI6Kp5/VWHVMjYm/gDOD9ACml5U1Kd+OIuAp4DnAZ8Fgz0i1pHwf8nZzvs5r9W/fW0YGkiBgfER8AdgJeC7wTeGNEbDnUHbamIj8ReBh4Q0SMTyk91cST0XOB01JKb0kp3ZdS+vdQE4yI55NPmvNSSnsAWwAbNSHdKcCngD2AFwMvGGqaNWmPjYh3AK8sf4cC20bELmX5kH7vmgPLzcBngL0i4pkppdSEspwLnJNSOr6U4RM1/3fQabewHDcDvkfe998ILAZOi4howj7T6nKsBuluB74N7BoRz2hGOUbEPhFxC/k3X28oafVKd2/gWOBk4HLgZVHu1g0x3S0j4k/AlsAl5JPcjkNNt9f/eENEXFEuTLZvYtL/BirAnhGxTTmmNuUuT6vKsaR9cPnNP0MOSA+5glWz3bbkPBMRh0XEzyPiUxFx0FDT62U58ACwe0S8sOyHQ65TRMRGwALgqJTSqSmlJWV+s4I9TS/Hku7byAHuV6eUulNKTzUxsHFg5ODrG8mVw7c1I92a9J9Jrj+9q5wLmvF7rBcRFwDPBj6UUrqjCWlW78C/HPivlNJ+5PNZT806QznvVj/b9LpZSb8Ty3FGRFxKLsdzgPuHmmZJdywtKMeIWCciPlzSfh3wImBaRKzfxP1xv4j4c0m/mxI4aUK61ePn/cBngU0i4jVl2ZDOkS0sx6B1++MWtKAeXNLeEngrsCCltCfwS2CHZgQiasqqk8pxbWAv4D0ppb3IjTOeLMuGWr9+Xkl7q5TSocA08jFqw6HlGiLioFYcU2uuNyrk4NfGEXFwr2VDMQ34V0rpwJTSLdTEY4a4z0wHdiFfG+xLrlseHytbxTW9NVhHBpIiYlZETE4pPQ78HDgkpXRrSuku4MvAq4aQdnXDrp5wNga+BdwGnFDmDep3i3wHd5OaWa8FlkTERhFxTkScGBEvHES6tV2UngCmAzMiYhb5IPOCKE0Uh+Bx4GzghcBDwE4xxKag1c+XCO/PgSNTSj0ppUeB7wPzy/IBn/wjYouI+GL5fLUS+FzgX+S7G28eTNqlDPeombUrcGvkZoTfiIgPRbkbOIi0Z8bK7i2PAzNofjk+DJyXUnpXSulG4Efkk/7Gg00wIrpKpXU5uXVWM8tx4+o+k1J6ssxeG7gbWEZplTSUCmL5TY8E3pRSemdK6c7BplXSq+2i9ArgopTSL4ClwENDTb9YDPxHSunQlNIVwP/QpMBJ5G7CFwBHA58ExgOHR8TmTUh7LLA+8F3gJOAr0Jy7PJG7NjetHHulvTPwdvJF2oeAl0TEc4eabs1228zzTERuPXoGcAzwQeD/gIMiYpvB5rW2AlJezyYfPz4LnA6Dv+Paq/I+C7g5pfQ/5diyT7MuAiPilbSgHAFSSmcBd5ArnBtGxEkRsftQ040c/H8j8NZSwb8I2CyaEJCucRd5+9uIcve8CRXO9YBnpJQOSSn9I1YdemBA23as7KK0X5m1A7Bj5NYJ7y6v94+IqUO5sVCzjTWlbtbrOzyLFpVjze/ZinKcBJBSen254FnR1XSgaUfuln54REwvx/yXkOuSzSzHx4HPpZTmp5Qq5Dv+S4Fm3azYmNxi44SU0j7k49/EiHjxINObXOp+tTfzZgNPAVcAR0BTzpHNLMdqF6UxZZ95GXloh6buj+SbThvQpHpwOY58MiKmpJT+DLwjpfTbsvjHlPrkINOeFrllVtSUVSeU42alHJ8AtgVeWc7He5JvBO8ITBhM+jXWIpflxPL+t8Drgd0GmV71xvVsmnhMLWX45ohYq+Z6Y0tyPOB04B2w8lpkIL9H+a23iJVBqG2Ae8uy88g9qt7ShH3mPuB5wIxyPDmLHBN4Vcl701und1QgKSLWjYhPAFcBX4uIw1NKvwIeKZXnMeRgwbWDSLta8b4yIrpqfuzF5CZnVwPbRcRzyIUy0PSnADeSu4VVN/JLyQfds4E/AXOAd0TuLtVImr27KO2cUvo7+Y7Ax8v/+xVwIPC+iNh6APldpaluSukx4G8ppQdL+i8Cth7Mxl7KsZrvUyPilSmlvwD31aQ3u+R9oGlPKNvIhcBREfHamsVLyIGOb5S8nxf5AnEg6X4XWKcmnz8ltwb5LPli/n7gmIg4tHyu39+nlOMngZ+QuykdllK6mdzSZKjlOLH2falYXVkzax3yQef2RtOsSXtcRHy+5O1LEfG6lNINKaV7aiq2gy3Hdco28t/A+ZFbOhG5iWYCzgd+AWwfEacP5Dcp6Uyp2cYnAw+nlK6OfLfnsIjYdKB5LulWuyjtU2YtIvd//jL5JDcncsDxhLJ+v8fgvrahlNLdKaUfljL4KnnbODQi9o0SWB7siSil9BD5eLRfCYB9lXxhMuC78hFxWtnHX1HSXk5uybJnSumcks0jI7fAG2xFaKvydhJNKseSdu0xcCvgipTS/wDjyMHXymDTrvkf1e/brPPMmJQ9Qu5qu19K6ZfkptP3UVPpHGC67wc+EKsGye8j3xW9jHwhNT/yxfJAK1inAd8qFbhx5ErnKyPiZeRzzRvIXaMa3md6pT8lVt7AeSGtKcdq5fA/gBvIAfRx5Cb87xtoxTbymCCviIh1Ukr/ILeO+U1ZfC05kLJskHntqwvsNsCt5JZg1W4YA70RMjUiXlLzW0wE/h65u8H5wNcj4qsRMXsgAcdY2UXpcMpNCeBd5O9/DTl4t5B8EfjJweS95n9Vgw2XMIS6WU161XEZ1y7n9A80sRynRG6ZOq7m93wpzSnHbWrKcS5wW8255vzIrVRnDOSCJ3J3i2vI56rPlWPcScCDNKkcI3IrrFIHqebrGnKLma7qOgNJs3xm/Yj4eOTWorcDny3HVUq+55KDeANN90Ryy4/PkC/4qp4gX+dcAqRSZzhygGn3PtZvSr7pOdRyrO2i9Mky+zhasD+Sj83fZYj14JLvQ8mtjqYBY8u58vqyLMiB7+uAMQM9xxQ/IP8mta23m1GOvccb3YzmlGNt96fqEBRHk2/03U6+qXUV+ab7SdBYOUbfLa4S+WbWCZFvtG5OPq5uGhHTGslvTfrVmwoHpdzK9f3NOKaW88xVwExyt/Tq91gM3JJS+hFwV0T8d1m34e26Zj//CLmxC8BvyC3QzyD3lvkGedsZdCvpUvbjgYspPRRSSr8jl/OzIgdjmy+l1DF/wH8CXweCfEfgNzXLxpXpD4G5g0j7PHKloavX/HOAZ5fXV5MPbAcOIv0tgL8CnwZ2K/NeRm6J88nyfiPy3ePjGkhvM3Lg4YyS9gnkoEaU5SeSo7TVdb9MvnhrJK/HkXfyl5T3Y/pY58Pkg+acQfwWHyKPj7I+sDtwJzCxLFu7TC8Gth1gus8n31X4LPlg0A0cVrP8C+SI+3HkSPANwFoNpDuJHHz5Yx/LZpEDGl8v79clH3g/2dfv1sfnu4DvkCsRk8hNEW8YajmSL8Y+Rg7EHANsspr1Xg58c6BlWD67P3B5eb0n+UT/3PJ+7GDLseZ7f7e83p58oK3+JueQK/bvI1dCf139fw2mfRL5AnKf8n4L8r69Pbmi8dVS3v+5uu2/jzSreTucXJm6CFinzHsW8CXgxTW/+Q3ABg3md3zv/9Nr+VvId1t3JR8PDhnE7/0G4Dk17ydUt6My/SWw5QDSmwp8rfwO+5ODrPuW/WMroLusdzr5jt0ltdtNg//jncAjwNfK+62GWo690v4n8NLy/lXk/fwb5FaNV5IDKB8ZwDYyH9h8Ncu+yBDPM8Ap5PPL68v7tcnnyuq++FNg5wGmuRb5ouAK4DDyOewAckBqb1Yem84sZXF2o+VYtpFvlG1kr7JP7FiWXUaueG1Z3u8IXN/oPlPzP04k7+tvaGI5HkFuaTilr88Ap5Fb4lS3yZ9Uy7bBPJ9EPpZeSj5PdtUsC/Lx5FLynfqGt+ny+VPJN1TeWN5X602bAOeW1xeRz/9nDyDdt5EDGN8p2+Bc8gXbr8l1hfeT9/2zge9Vv0s/aa5TPnsZ+Tw5m1y/m1GWzwLOrFl/s7LvzGwwz8cCx/SVl7K9/ZRB1M16pfMFcmuYBbXbShPK8STyxcEPyMfZWU0qxwXkgMgV5OPnJuW3v62U4Snki8CvAj9spBzLOhuXctygvL8Y2LWmHL8wmHIkd016E7D1avbF6u99JuWcM9A/8jHkGuDz9KovlnKcRt7Hn9nIb1Hd74D3kru7b1LeP0app5VlB5Jbxv2LfAx7YV/fcTXp/wc52DO/Zt6m5H10KOX4vPJdp5b3XyLX59cvv8NZgyzHvcj193F9fUdyUHdQ1zM1aXwC2L6P+dU6ztHkYSpWlFGD6Y4hn2u/T673v6dmO3/fEMvxJOD/kY8T59WU41D3x+nk4NYzSv6/Vra5rrI9frlm3VeTr7unNpDuu8nXMs/sY9m2pdx+WspiO+CXAyzDk8gBmPuAb9R+X4ZwTCWfF5cD0/pYdjy5FfMO5OuQ+yjXNDRWzzmefN7auLxfQu7iB/n88M+adeeSYwKN7DMzV1fe5GPiQlZec2xJ3hcnD+T3bvSvY1okRe4bPxG4LOVfZkPgx1EGXksp/bvciV83pXRrRLwmIt7UYNobki+Aj00pVcodtGrTyevI0e/fkytCN5IjqwO9s7GUfPJcTh7bZQrwO/JOtW35DneRAyBLG0ivdxelK8kBmbll+RLywZ2U72hOpZ8WaDXfZxL5omBB+fxTNetU0/g6eWd9QUSc0OjdgXKXpIt8wrkvpfRjcle56p2LJ0pZTwOujYhdIuJd0dgTjSrAm1NK70gpLSZX4jct/3cieTyPy8kXtEeTL1waGTfkMfKFx19KWttFxO4R8ayUUg/5ILxT5OaQj5IrFLekxu66Pkjuk/y2lFuCbEiucFX7gd/HwMtxGvDNsu4Z5O4Az+m1TrWstyBv00QesPl5/WW45rNPAveUvF1BrtQeG7kbyvLBlGMU5TteX2bPIh+In1vuEqxDvhjciXwi/Qt5kMd+RcQB5PGbdk4pXV7uYN5IvoNxJvDBlNJR5CasJ0RundhvOZZjEqzsonQrK7so3U8+wd1a3l8P/JF+BhGOiN0i4kfAmRFxeK//s2JfTCmdk1JanlL6GbnMG37SRuSumn8BPkoex6nq0ZL2k5GfVvE4ZTtp0DjysexNKaXvkfefk8jjqz1AHsvuKnK5/S/5oggaGLA5InaIPMbNc8lB0i0j3/G/jiGWY0Q8LyJuJJ94d08p/R4gpfRTcoWwArwl5fEaTgTe3l/aEbF15PE03kB5Ul3Nsuq+fB3w3sGcZyIP9vq7kuffkcc82xv4d8qWl3Pcv8v/GYi1yBWot6aUvkG+sH95+buV3Aruv8s6i4C/lc81cuxbi9x99/CU0g/Jzd3XL8s+Dswjn+cg32lcxMqm8f2K3HpkN2CHlNLXYZVyvIsBlGM5LM2MiF+Qu08eSh7EcnrK41mtuIudUvpYKt0qyzaZyPtlI3k+nDy+wW4pjzfyIvKFArHyKXAvIF/83Fv+d0NP7omIHcgtVv6LfJxeJ63s9r0ZsDQiXkLejjajtFxtYPubDbyGXGk9iHyT5jTy+eHb5N/rmpTSoymlY8kt7raoPZatRu8uSs8l142q+bmPfN6t1j1eQO4SubiB32ID8g2ld0fu5tI7L38mV+i3gQHXzWrvylfHZdwz8riMT0Vu1TKUcjySfNNgx5TS3uR9ojo+3rMZfDmuQw7CvzzlMWNuJ18UP05uAXwC+ebO38kXKpuX7/S0cuzjfz1I3p+fU+6Kb0TuVroxuQ6xfazsGtZvOUbujvNLcjB7JnBeqXessv9W901yuT1aPtvwdU9EHEbeX16f8jiYT9YsG1tTjpNSSreklFI08NCLst+dl1LaJ6V0W0njSnJ9CXL9/RPkm4HvJe9HB1W/Uz953p0cmLkUOCzy2DeklP5Z5r2NBsuxD311UTqQHGx4hIGX487lnPd28u/8noiYWP2ONWV1DwOsB/dhF+D+cn33icgtYGfUlOkLgcsid2f9AvlGf79SHgvvCeAW8pALsyjXdOTzzEIGWI7lfNJ7vNF5EbFbKcfLGFo5Vrs/TU8ruz9tQD6uPAjMjdxiEPJN23tTSn0e+0peJ0YeSuS15GDRv2qWR/m+fyDf9DwkpfSelNI15F4oXf1lNvoe92xK2edTr31xwMdU8vXsNeSW1TMjP7WuWv5/JwcEzyJvpxdQ6vapsW6KF6SU9kop3R655f0icr0HcuOYrojYrrx/HrnnT719ZpuI6CGfn3pfE1SPu1eTj3f7l3X+TD4fP6uB/A7YiA0kRa/BrFIeD+k+4DUR8RvyTjmV3I2keuB6FTA+cn/Dj5APxr3T7etkugT4R+Tg09fJO8JFkbtMTCSf9D6eUnop+U7NUSVPfZ1AV9cPe2vyheNp5APi4eRWVV8hN/8+LyK+S77gv773h6sng5rfo88uSuUgAzn4sVVELIyIr5Ej0DetJm/VNKuDpW5EvkMe5US6ojyqB7+U0v8jV5C/ST6I9dntJfruIjeePF7HtFKp+C15AOzqGCw7krsbXUi+oLi5BGh6p73K0wrKweOOWDnexrfIg4OTUnqYvAMfllJ6dUrp++SD+j/6SHdm1DwZopz0fwE8EREV8gl+V+CXEbFVSul88l2az0fE98kHu0Wr+T2eETXd6VJKj6SUbouItSM3NX0/uSwvjzx2x93kClfD5Uhuojs35eDUj+jVdSNilUE4dwCmR8TF5DvtqyvHFftjzWfHA/fGyuaSnyCfjF9U3jdajqukXdK/E5hdKotnkE9uV5FP7tcAx6eUdiPfEfsT+XdqxMuBT6eU/l62t+qg8W8nX6hUT3p/JwcdGxrYsea4UttF6aWRB4t8mHwBf35ErEe+GN+IPprCR7ZWRHSTKx+fL2m9NiLm167buyISOYA4veShz+NTH+4i383ak3zsrI5BUnuc3BToSTlY/9yaE2w9k8gn4OpTUH5DPl7sSt4mfgP8OKW0HbkSelS5oOuvkrwWOVDWnVJ6K7kF4nXk7Q7yHbEVQdOBliO5wrohuSvR3yJidqwcN+8RcqD++pL2zeTgaX/dll5PviA+MKX019oFNd93PLnFxemNnGd6GUOurBySUvou+Zh8UM3xnPKdnkgpLY3cT7/fp9NEbvr/GHn/2qvMvpR8gfky8naxGLgypfRi8p23QyJiUoPb3lPkc/q5EfFNcoutN0bEm1Met+Lz5O50zyfvC33uM3U8n9xS9NbynV9azg1LyXddGyrHmkrqJPJ+sCu5En8fcG5ZLfWxPz67HLOfIgcUGvH1lNIe5TxWDZzMKcfs6rH52cDFETE9Ir5Cg+N6pNz8vzul9GnyXe4P1iy+qXynC8hjTnyafExsZPv7N/niqbqfXEvePo4h33H9W/kOkyJiDrl7Sr/dCcupoLaL0u/Ix++NyvJHyXfVLyx1vg+QWyL2qbZullK6l3wT7x5y641V6oYp39T5AnBzf3Wz1eS9eoHR17iMj5dlgypHcvf8BSkHtyAfS/ctr28gB8j6LcfedeGyr2/PymPlheSg4FvI9eml5BtPkOuz1W5Mq4iVgbLai8gHyOe948jb3hXkffBDJa0LyMNV1C3HmjJ8DvCrlNKeKaWPkreNvurjY8p+uYSVx9OGu1WmHDz/KzAzIjaNPAbmIRExraaM5wDfjTwu2kXkwGkjaVdKHnckd99aTK5DHkoOSpyYUto6pfQ1cmuXPzSY7o/JNy3OId+kPbZm8Snk+kj1huFqy3F1yZNvcLw9VnZRurak92TJ5wUNlONa5Vz+duCMUpc7kxwUnFvzXaplNeDrmZr/VT0HXkLelr9EvgmyF3By5KAr5f9+kDzu399S7v7ckMjBkBkppYXk7XuXiHgr+Td510DLsXzvn5NvstSON1odMuE9NFiOva9Jyz65uu5PW5CDHIvI++MXyPvsb+hD5Bt4T5FbxG8I7JFSupaaLvS9jjtPpZSWRL65djHwQHU/6Efdcc9q9sXNGdy58XZyC85byUG62eTzyjHka4sjU0pbppSuJPd4uaKRdEvaDwGUesyl5OPJyRFxSvkuC4C3ljrQx8jHsqeJlU9eewV5O72n5K/2OJvK9BZy+T47Ir4ZET8g77v/7J1uU6QWNHMayh854v1JcmG9qo9lM8nNp6vNyt8HXF1ev4V84nvnatIew8qmrmNq5m9U/ucXgFPLvP8kF+rWvdKYsZq0x5b1q09tqc6vNrvbBHh3ef1TcuXyP8r7ceQT+NF10j2HfOAbv5r/v0oXJfKBYmvyk9be1eBvX/1t3kuOZB5CviiZA6xf+53IQbsVXQZWk17vLnLVbmvPILfi+RZ5p9qZ3MXlE2X5XuTAwdvr/NYfJh/4Nqnz/7cnBwX7ambZV3PAMeW3/hf5Tvbavb7zzuTWQ9V5/wH8ombb3Hx1v0fJ83+ST4hn9d4Gy/tn1bx+P/lCm1KOn2y0HMtnriYHCH5Kvoi5jHyR/YyaddYmVwL+BBxcZ388vWzXO/beF8gXYHtWt8uy7fygwXKsl3a1z/pFwOwy71hK890Gvn/vrgrV/fAjwOfIF72LyCeEj5IDxieX7WVPcgX8agbYFJSnd1G6m3zyn0QOXF5NPs5MXM32V90HD6F0gyq/wyeo6epU833GkY9fnybfRT91AHmtTWM8OSB8CSv302qXqGNY2fR5EbmlTm0669Vu52W6Dvl4/Kuy7f6WfMfxS2W76d1FYO1G893rcxuTu888u2Ze9Xg5oHKsyfv7yEHLT5BP6j9iZdeUM8ndRZ9T0v4lvZp89yrHseS7+fNqtuFtWdl1sLrfTO+9bw3gN5hQ/qrl+VLyhdnYmnkHkoPd7yO3hntatzlyS9ExvX6LtUo5foyV3S52LL/D86hp/l++d5/l2Ffa5fUzyC3Vqt2dXkMOIM0v+T+S3Jrtc/Sxz/S1r9fMP5VcmTq0fOdLyPv37FK21Ufvrq4ca8/pryBXSi/o9X0rwCuq72vmb0PeVwbbnWYW+YLtI+SLzA+zspn6eeQLzWvJA/4OJv0XkltyVo9V6wDb1P6m1HQL7yetGeSK7XfIN/c+Rj7GnUluYbEd+dhxGfkYdXwfaRxBPudWuwQ23EWJ3DL1LdQch+qU46vLvM3IdcxZ5Mp1n10my/bfZ92sd956/88y/Qi57vdM8nHkfGCXsuxL/ZUjfXSvoVd3CvL5623l9dqNlCO96pE1+X0PpTtfeb87+Zy2Ibm1wafI+9F1lG6BvdJ5M7n+dMRqvs+R5AAJJc0PU7oLkvexPsuxVxluT67LfI/cyums8j+PZ2W3od6/0YbkFogD2Ueqv8lB5Lv7vycfq35KPqdVu9OdTm5l+0f66PpIbkGxVU16vesm01h5HtippDOltgwHs4+Xz+5Bbs09p2bevg2UY71uM311UfpVzfJGyvHL5GuWbWt+lwllX3hOH59r6HqmlNW25BZisOp13uHkY/7J5X11yIHdycfsf5DPMxNWk/ZbWTkcwtOGxCAfm9Yuv8lj5ONd7f8fUDnWbBPVc/h5wAE1y+c3UI71uppVuz9Vt+MtyTfMq7/dAeXzk+qU4zllG9uGfJyofv8ryEHiatf02nP+FPK58b11vvsq1169X5Pr67excn+vdk+se0wt33k/YNM+to+J5PpRtVvizuTW8pNq1lntUCjk/eoFrH4/H8PK4S62JO8/1aFAppZ8re4cdhz53Pl8Sl2WfA3+f9Tpcli+04GU80Or/lqW8KAyk096Z5GbmR1G3umPY9UxQl5YNthqYc0g35UeWwpxymrSfiO5lUOf42WQT3DXsvKkNo68c76o+r5Ovl9R1j2b3GXqD8BOvdY5mHy36C/kAMrXyQe2p+2kNZ95FTnQchb5AHkjpTLZx471FuB95fWhwPP7+p4NlsNFZQOcVr7X7cB2Zdnzy2/dZ6W+V55OIUeya/sd116gPJuV4x28m5XjWMxZ3e9CPvncQm6l0tXP99i85H+D2nzVWf9IcuVkymq+T+/K1zPJEeaJ9dImB1RuIlcqjwL+qAP0JwAAIABJREFUt4EymENuSbHeYMqx7BcLgAvL+53IJ43qBXF1+9i3ThpTy7Z6Fvlg9A3yybT2IP9WcqWgOpbMs8iV5SBf5K+uHOumTT7ozizlvFnNNvM//H/27jxMkqJa2Ph7GIZ9l4FBFgcRdwVlRBRQRHaVEVAEUVlE9IqKXnVE+BRRURxRFlkUBRm4KiLLZRFULnrdUUABcQeXqwMNuAGjggLx/RFRdHZNVXd2dVdn9cz7e55+qiqrKup0rpEnIyJrnGRTqQww8kD0nLJ+Lyyvn05O8LWSvDuR9y8fo22nXpbjqXQ46WD4ROcN5JP4H5S/rzN8oF6xfd2qfL+1f/pQeb1ymQetMQM+TxnXpO17K5P3VW+gLRnR4bOrtcfb9v6csizf1jb9cnJF+ri2MnYiHwzPIt/9pH1eLE++K8/hDB/wr6ec6JT/b6xtspVE7Jj4LY8XU/br5fUMciunMzotx8rntmr7f6rryXWU8VfIFbbTyBWmmeSK0lXkSmf7OtJ+nFmLfGW/dVvkheTkxn93WjaMkVAjJ/WeN9o+gVyBW9A27URyi6oPd4j5heSE30XAJzvM37nlf3595b0fArtXlnO3ZE7Hsqvzm1wBO7Ey/ZNUkg10uXhS3Qa6LMMNyHWIL5bXs8gngieXdW/BKMuxekx/HTnRtBv5hHXryufeQLmYUF7vynDlcLRjZNcxkyrzpVXp3LSsN3uU1zeV9bHbCc++5BZBa4+xnnwIuKDD9G4Xq7qWS05mn1bW8VPI9YQrGbl9bdMeM7lF7LfLcjiBnIzqmPQty+wDlBME6o1v2F43u46cCF2Z4bHV3k+uZ13C8PFnF+CpNcp/M7mVebeYO43L2KoD3TzGcnwrOYn4tC7vt44NC4G9x7EcuyZ7yCdPZ1Iu4pLrOBdRTu4Z3reu2va9Hcktpa4kH1/3b3u/tU6/mJH1wc8AB41jGR5GvjCwC7k1yzfJJ+xbkJOZP2nbFp8y1jIsnz2grIutk7T284PDGU5yPrbM89ZYp5eR968j6hzkBOJ1Zb5cUNbdtTqV3/Zb/1Nz3eua7Kl8ZhZ5P/fRDu/t0mE5bk2+QPzzMX57BpV6GLm1zKPH+E71fOYVZVtoJcdnklsqX0aut1f347syxrhCZR35Fvkiz1nk49zKbevehuT62zmV710AvKQ8X2J8nMrnHlvmy/+1r9OV979G3qa/Rq7rf4gu225b2W8p63XH8XYY3s6XGG+0rGcjliN5P7kq+Th6NXk4geXb4y4xH0sZH7BMu4Zy0Wscy/FG8rbzC3Ki91hyS8z3Aze3LcfW+fRKo5R/GLmeuGuX90e7qHAjHfapJZ7vk3MFJ5D3q13Pvdu2xSeP8ZnHl3ivLPPkPdTbzq+iw5hd7cu3PB5JvhjbXof6EsMNMKrH40e2man4m5IfqR1M3pF8j+GM6K7kSt+rKp8JcjLmP8mV829QTr5GKXc18o7uCHKy6HGtGV9ZUKuXjf8khq8gfZkug6O2lb89uQli6/XJDJ8QzqjEfRbw3PJ6HvkqXceTnPKZJ1AZHJXcomHbLp89t8R+YVlBHzdW3KP87rvJB8qbyDvnq8v82Yl8olSnArcc+eD6anLF5IAyvXoFuzXvn1V+Z/ca5W4B3F15vSmVjGylzNbj1+nSQq2t3CjLf4fyei45ablCtbzK57cmV2iOqlH28xlOtKxKPlg+q8PnWjvIZ5W4u2bsay7Hg8jduFqvF5Cv/O5FrkyOmpwq28EPKq8PJFfc5rV97mhyZfMd5Ktpx9SIrW7Zl5Kv+B1EPsidNNr6Rz5x/Q65y2h1v9GatxuRr6LcUHnv7dXlSNtBt/zNIydyF5FPqLpVaI4oce5VKfvj3eItn+m4f6q8vwL5BO2pbdPfTLm6Nkb5HRM+HT63ArnVxUXkpNecMv0lDFf4gpw4mE8+MO9FPom4nLJvG6X8x5EThl1PsNtiOQ/41SifaW3jh5IrLSu0vd8x+c9wcuOM9lgYvrI1q236Qoav+ken/6HDcmy19jiWfELxzvJ6Brm7T2uw2cOBI8eYHzuWZXgnXY53DB9rzme4lUwrYfwCOlQsyJWgH5CvPq5Hrgzt2OFz+5ZldxD5yvEVlJamo8Rct+w9ycmH55KPG1dSOZ6OUv7O5GPTJ6i0qKysFyuRT94Wtf1Wq+LVcTmW99qP6aeTW5MdRNl3lFhbN0t4TPm9/elw9bdSzpbk5vO/olwVrfNHPq6/qLWedfnMtmV+f4VcH/gMXRLX5fMrkve5HyLXWboNBN+1XEaeTAWVhEpZjpvRJQlM3o98ENinTNucXFdYImaG999vocNNL0b5H9uX4yllnZhV/o8nkOuc91C2QfJ2vN8Yy/HZ5K4kl9DlpL/M3w+RW61dTU6Ynk/uJkGnda/Mw5nkE+GvMcY2VpnPa5f/9f10ucDGGMme8pnW2FHnM7wv7LjdVrch8oWOl5ZpxwGnVpdb5fNbl3l2Fnl/8i3KyeU4luGpDCfq3w+sX3nvJnJ9a8ZYy7B8flPyxc4rS9znUC7IUGlZ2uF7F1Na5rLkSWurzvgcyiDiZT07ufK6UyuLOWWeXNReZod5OGayp3x2Brnl6Pnk1hYj5lflc61kxdvJx9Nv02Ug+raYn0HeNy2sEUun85ntKq+3AL5Ted1KpL+y23Ik70Nmkrfl1n5kj7KOrNAeO7mxwVnkJMv55O1hsy5lVy+Yrkqu515Lqc+xZKvq/0epv5L3L0d3K7t8Ztuy/l/OGAlP8r7kmvL/7kg+/+20/2ite2uUdbS1XLtdMHsa+fj1+RLH1YySUOuyHC8q6+4B5O52z6u892PyRewZjH1s3JXcavoa8vnPc9vjrXy2/aJCq/VWe32uNT8OAt5Rnj+OfB7RdaBs8n7hc2XdXrnLZ1plH8LwzWMeU9bFj3SY161t5vHkuu2V1Lh5CF3Opct7jyW3qN2kvG7lTg4YbV5P9t+U/Mi4AsordGvlWK2sAKczskvO9mUj/V9q3qGoMqOPp+0uVQxXwNcnVxYvJmfLX1mz7FXIG3qrnP0pV4Q7bQSjTe/y2TXIyaH/I+98d2Rk09cxuyiNcxkcXX7v+eX1R8kVuFqtYhiu9I3VRW4l8kHrV9Q4cah870zyzu9TZR34Krn5cHtLopXIV4xHzbBXPv8p8sH+zeQTv9bd1DarfGZVcsLkxrrrXttvPI58stm6wlfNIq9N7lfeU9kdfmu78j9sQz6R+zYdrlyO8v3VySfQB1bKu4xcGa9W3lYs751MlybtEyj7qWUZfnms7ZE89tj3ySeuLyjzudV9tJoc2oJ80Dy0LM9L6ZBsZGQXpWeQ++XPK3HOaftsq9LdUxclRu6fPtf23noMd3PckNK8mdGv6kwk4XMW+cTqu23Lojo/nlP5nx9D3i+tXfls670ZZf34JDkR9/bRYm6L/3zyuBGvaX+/7XtvoLSsoHvFP0osbyxl7tftt7usV1cALx7ncjy/tZzIFdD3MNyl7aOUK/F0r6i07gZzKnnbfTH5tudHd/pfK8vmLPKVwoXk7ab9TqTV5bgvwy2v1iBf4dqI4QroipXvPI+8rfyUSguwSSh7U3KXmm+Rj7v/r8Z8fhw5uTGPvG3+FyUZzMhtfTVysuQI8rZzCfD+GuW3H9MPAD5cnt/IcB1lLvCFGuW1ynlVWV/PI7c46dYVsFXpfGpZjtfQ5Q6pDCdlTqMcN8hJmdMY5eIMuVvhreSKaKeujr2W+0xyBfyRbrLV+UBOrnyUXI+rnqx9hpwI2JXhu5C1r+Pj6qLUYTnuT942lyfXp/5ATvDsR07ujnqRrLV+k491F1V/p8vn96KShCmvnz3GOrISeT+9TnndtZtTWT9uIB+TfkhpXdG+LjG+ZM9a5bOti5LfbC2PLsuxvVv6duT9XbeE5xxyHapjl/eay7B1ovZthvejc8o6t0SiZJR5/SLguMr0s2m7G1SH+d3aHjfqMk/OJF+sOIKybyjr2yZl/d66Wj45EbIPeb/yzlFi7jXZsyV5G19iO6/E/OkSc6teujNjd5sZs4tSl+91Op8J8rnCe8nb1ycpd2nrtvwY7iK3IyMT2GeTL7psxXDLkGrXqlXI23zH8itlt4YTmVHKOoO8/7m37fPj6pZflvdy5G32jMr0ri1vycnR68jb5XW0bedtMdfpalY9RvbU/amyHP9Y4tqavA89pLz/6LJ8R02WlG1jVXLyqLV/+iwdkjHl9ZgXFRi5LW5HPmZdTk6Uf5LcGGVfSrKlUuYM8vHnx3TZFjuU/WlGtnI7lTzsypbV+BlOAtbu8s7o59Kt3jxHkhOAC+lSL+v335T/YI0Z93JyRbjVbPOZ5DEMnlpeP4Vx3CK6Q/mzyQfcVrPUJcpilHF3av7GObT1zyRnn7ue+NUo8z/K477kbGqr6fGYXZR6+K0RXQWocWDuUs6oXeTK46jNYbuUuyb5IHdMeX0wuWLXGnugp3lNzs5/l9J8kFwxeT/Drcu2JR8Aat/KucvvfKN9J1XKDsZoRjnO31mJfOL5dfIJ2mHj/P5y5ArOL8v8/RG5EnNSa50ocXc8EZ6kskddjow8cX0qeefeqiRuTh4Qt7Uvae8ie1rZFyxREWK4i9JxHb57fol1iQoENbsojfL/jNg/lWnbkJNBR5APcG8q07slVnpK+JTHY8lX0N/VVmb7/GiVvy15276+LLv277USJ69hlKRaW8wrlNdvJScFf8XIk6n2cXw2I1eSO1Z628o+kHw8aa1je5D3T6350KqszyAnO08s/1/tsafalmOrO9IryBWOt5ErBT+ldIGqEfNOlem7AL9u/2zl+Sbk8fduosNYEh2W4xPJLTI+TR5z4FvkpMx5bd9btTyuRfdWPL2W3Uoode2a3mGeHMDIW00fQh58c7327Y98BfA95BOvcS3HShnnMNz99RnkCwxXkCuMrZZmnU7mWpXOBeSTgdZ6tw15v7zlKP/rluTtvmOlk5En888hD5T6yHpMPnnolrSYSa5nvWeSy12RfGFniRZ2jOyidCiVIQDK8mvdYfQDwGWV79XuolRzOb6lPN+CkcnrQ0b5XnWebENu5XkMebs+pszLQxk+Mek0tlG3/XV1/J9dyBcsTiYfv44n1xfOovOty1t3Nuw0HshEkj0zyYnjTuOuVJdjq7vg8xjeNrcq8T6m7XsvZbhl9kTG/TmHsm8jj9v0M/KJ502d1udR5vU2ZdmdX3l/Prkbd6ueWt23bkZOXi+xPTKyu89+5OPhduT94ZaVz/0nI086n0c+4V6H7t0jJ5LsWYG8PR4zRsyvKM+fWXn/Qrp3mxmzi9IYy6F6PnNKWe/fSW5xewOjJPsZZcgPcm+KT5O7I3+cPEBz63vbM0oLoS5l/5y8H94AOKl85lRyvfXctu1p1BamjEx+PZfchesDlfXwRHKL2dYxorpv6jreaIflOJ6uZhPq/lRZjgeQu/geQ+46dh55e3xvzfnxAkYmt/YiD33R9dyCLhcV2ubH/gx3Zz6efJ5xcfnfTwCuatsWNyQnyLoNydG+nV9X1qv/I7ecexXDQ2Oc2javH09OJnXthTTK/9rpXHr78t6HyYO6Hz+RZTmh9aCpHx5lhm1QVv53V6Z9h5xh3ZPcQqnreEU1f+P1wDcrr59APklbYpC3cZY7g1wBvIrhcV2eQO4acgC9JTc6VU4vJx9A55EP5OMeB6nmb4/ZhW2M70+4i9woZbdfZb+SPIbFc0rZvczrlcgVkh9Vph1KPvg/r8zrUcfrGGv9KI+HkJMYrcr5DiXmnsse43c3ncg2Q65w78/wVeKbyUm2bckn5it1Wk/7XTbDJ64fLK/nkK80VFvRnErlynGZ1jopnkmHAxXdu8K2kgzPJp8Ezm373psYo4tSzXnSvn96K/nOSJ8ENh7juxNN+OzNkt26una9I+/fWvPn8eSDbKuS+SY6nIiMEnP7OEfXkK8enk3uArN92/dWbo9/lLJbyeBZ5IrV5eQKaOvujR/sMj8OY4yxp8ZYjtVBSLcg70tOo0vrkk7LsDK9dbOJJcZKqCynlagMGDnGcmydkMwiV+JblcKVyHc5ajUtfxNw6Bj/a69lv3mc60hrvX46OUncGjTz9eQTkHPbvlcdKHPc+1dGHtNb6/njyAm17WhrqdH23eoJ96Hkk9Bqs/+Pkyuc7YN878XwDSq6rdftZV/LcFKmdVz5b9q6wpNP5lsnyZ0S4ZNR7mg3BGkfAuAj7f9nmbffonQtp0YXpXEux1bd7IlUWrrUXI6vI19seiF5O/tlmb43ebu+ovK9l9KhC/sY8/t75ATB18j14I+U+TEf+H6XdaTToMbVcseb7Fli31JjOX6o8npd8sDFI1pdk+urT5qkZdjaFjcinxvsy9jHxuo8OYycoNuDfOHkzeTeCJ8o/081kflShm+W0G177NTd58nkFrBfrsS/PfkkdE1yAukQRrmYyuQke7ptj2N1NWtdoJm0bjN0P595PrmlxZWMPfZpp7hb+6jqfmQrctJgE/KFnYMZZX89StlbkY/dp5d58j1y8raVkJ4zVtksmYD4Mflc5bPkhM/p5JaqZ7NkAmJz8j6gW6Kx165mPe9XuyzHKyjjGpXlWXe9biXsnsnwvmIfcoJpxbb1ehfG7gbYPj8eqS+1zds1yPX4p5PrKaNui13Kvph8gXYXcr3yCnLLrBcz3BtiVfI5Tu2u7B1+t9O59JrkbqsfZ4KNXyb619gPjzHTnltm1svLBvF12q4eTaDs1op6ITkTfkJZ6HMmoezWbRXPI1csvkxuajhmP8hx/MZjyc02nzlZZfZxOU6oi9w4fmezyZon5O6NN5Ud2ZPIlY2uVyp7/I2DgTMrr/uSCOzTMt2S3F1upT4sx9pl0/3EdSGVriblYPEDhu+AdjhjnBSXz3XsasZwM9UF5FYOT6A0kWYCLQ7b14WyfzqVfBXpMNoG7685T8aT8Bm1tRqjdA2ufGYGuWK0RdkXjpmA6RYz+SD5vvJ8f/JdUH5GTiytUGc5dii7NWZR61bDrWbeTyvbfKvV65hjFo1zOX6iLMs6A292mx+tk/iNyceV1oDOrfXxjdRoLt22HFvdLpYjn1RuX/ncqQy3pqqVSOtX2R3mSet/P4l81fK75JZOT6PSla/Mk4kux/Zj+hXkfUyduwB2OuH+cOX1RuSu2du21vnyuA9jnHDXKHtT4MbK69ZJ4N6jld2vcstnug4B0Pa5bcrynNCFrDGW4+XkfVXX1hyjzJNTKQNsU5JnZfra5Lpqaz8yZuKkQ9mnlfV8Z3KXkUMq793C8MDAezF6i8a+JXtGW46VaZ9mgmM81liGXy7LsGsrxjHmyemUO72VeX4B+SLR48n77Fbr4toJsLJOfIXcYuAL5BPmPzB8I5ldqbRIqlFe35M9dO5q1upW+W762G2GfD7zdXJr1PHeUKZT3NULB7sBZ/cYV6vs1m3h9yjb423kxOKhwNAEluOF5ETjpow8Ns4t6+HGDI+5VysBwSR1NZvAcryaLmP41lyvt6283pjcOm12ZdrKjCP51bZ+nE9O3F3P8DhWW5V53UuPivb14wWMHPD8MODYSZy/nc6la9/Fu99/jQcwyozbnZyd/QUdbhc7wbJXISeq/kTNftrjKHsbcteC7zDKLWPHWeZyZcNaSL7qOuYV3EH4Y5K6yHUpO8j9Xc8tO4dxddsao+ztyH21f9iPeU3OvN9Gj92fGlqWq5Z5fRM1EjFTUTYjT1y/WCnrbko3AHIrjjPJJ221khttv9HeFbY1wN76wH3AXQwnPCac6C7lVPdPXQfHrjFPJi3hM8r8qI49cDS5FdG4KiqdYiZXGm4p5d1ETiRc2JrPdWOme3KjOqbCTHJ3iVZibdwVizGW492M4zjTbRkynDS6irZxksYbc2U5tu689m7yVcEnkE+Sb6THK2j9KLvLtj6D3CVku/J647IcW13lJms59nRMZ/QT7lZi8FXksTKuAD47GWWX1zuQK5utgWhrVWr7VW6X3zqHSpcs8knV0eTt/YjqOj9gy/GVdB5M9bnkJEftoRe6lH18ef4l4F3kVogrkU96Ru2aU3Pdm9RkT4fl2Loj4nwmuY7T6zIcazm2fW5f4IQJxPgflfKPLPPiwrL8bqu8P9FxUict2cOSQ2e09t2T3m2GSTyf6RD3HqXso8it01t3KR73fqRS9v7k1iZvbHt/1CEGxliO1QRENfm1Oz0mv9piHndXsyaWY5f1ujWu1TnUHHO1xvx4ZdlOTi+/dUqZH61BsieyflTXvbXKunIbsPMkzuu+nUtPSnxNBzDGzJvJJF6VqpT7jrLgJ70rEfmE9d2TXTa5P+gb+hHzFCzHSV+GpdzVyF0a+tUlrOexuEYp85GB15peLj3E/oo+zuuey2b4xLV1V6PDyVcrDy4H0mupDPLeQ/ntXc02Jl9tvIq2ATcnaV5MeP9EHxI+o8yPV5Cbe3+OMZqO14y5VYl9ZHyy8vrn9DhWSqXsVtPr9vnxPxNZR/qxHDssw1aC5EBy94wJnaSxZNe7E8oy/AJjdBNpquwxluNx5IripO63J+uYTuexEz8M/Iu2bowTLZs8BMC/yF0Z3jdI5dK5m9ljyV3FzpzoujfVy5FcN2slwCZ0YZKR4/9sTk7GXFDK/uAkxjzhZE+X5di6Tfu2k70/ncxl2GWerEses+Y3DN/QYjxJgm7dfXYiXxjZc4L7vklP9nSJ+XLyIORz6VO3GSZ4PjNK3DuTEygX9DqvRym71ZJlQhcoOizH3cgXRFrJr64DqPew7tXqatbUcuwyP3YlXwC+mJo3vKo5P75MbiSwVYm56/ACPa4fu5F7N53Sj22m/M5Anjc2HkAj//Q06krkn3/+jf3Hkieuu5Mryp+bYOWtvSvsSeSr8n052an+5iTNk0lN+LBkl60Pka/21Loz4nhjbnuv6y2Re5wfLyLfkejzvc6Pfi/HTvOD3GXrDUzsphPV5Xg6OdGz9UQryf0uu8ty3Jp8N7kxx9do4o/OJ9xPIrdMPZoJdKvvUvYcyt2nKDcaGJRySzntXZSuLOtJrTtcDthy3Ix844XTJ3ic6TT+zxPI3Xif1ut63SXmSUn2dFiOl1Oz2+cALsfHl+PBsRPZHtt+Z1zdfUabzx2m9SXZU4l51LG9Bu2vxH0NXW5eMAllf40x7nY7geW4c9mHnD+RfUiX5Tihda/Py6zb/NirPH8pk9QNj+EhYbaZjPK6lL1V0/O0qb/lWQallB5uOgZJkyMilkspfSoido6IU8lN3z9DHlA6TaTslNLDEbEK+crLDuS7ifzvRGMe6zcnWkbbPPkEuRveLeQr5tdPJLYO8+PzE423LeZdIuIU8onKf6WUflB++x+TUHZrfiwmd7F6W0rpR5MRf7uJLse2mE8hX6U7A/hUSumhicbWYTn+cCJlTkXZHZbjA+RK3H+mlG6bjN/og4fJCYE/AVuUZXkH+W5vx01y2aeSm9W/O6V05wCWS0opRcQzyN0vNiV36TtrImVOkfZ58gny3Qjfm1K6exLLfnpEnAT8mdxi5ieTGPNJwF8i4s0ppe9OJOClaDmeAiwij6f25YkUHBHLke/89EHyuD+fnIz53PYbjyV3dbyrHMt7Pp6X8jrFfN1EypwKXeK+sY9lf28iZXZZjqsAd6eUPjaRskt5k77u9VOX+bEieSgAUkr/PZHyu8yPaydS5hhl3zAZZU9Hy2QiSdLSo+3E9fnkcQJunsSfeCN5kN+dU0oPTGK5fdPPhA99mh+VmGeR7yzygVYSaRLLrs6PL05G2f3SZb2eyEllu36u1/1eR6rL8SuTVX4/9POEu19lT0GS4I/k1lgfn0b7VJfjklyOI8t+OCIeAL5PHp9nUuZJP5M9/Yq53/oZ9xQvx0lJfk3H5dhlfnxnMsqejuvHdNUar0WSpq2IeAd5/IR3TfZOvbSCmHatGPs1T/o5P/q8HPtWdr9M1/V6uq4j/RIRGwGvpg8n3P0qu58xT1cux6XDdJwnEbEeuQvhZ6dLzFqSy3Ek58f0ZyJJ0rQ3XZM9/TQd58l0TW70y3SMud+cJ5IkSc0zkSRJkiRJkqRalms6AEmSJEmSJE0PJpIkSZIkSZJUi4kkSZIkSZIk1WIiSZIkaZwiYq2IeGPTcUiSJE01E0mSJEnjtxZgIkmSJC1zTCRJkiSN3/HAZhFxY0R8NCLeGRHXRcTNEXEsQETMiYhfRMQ5EfGriPhcROwUEd+NiF9HxNblc++LiPMi4vtl+usa/c8kSZJGYSJJkiRp/I4EbkspbQlcDWwObA1sCWwVEc8rn3sc8DHgieXvlcB2wDuAoyrlPR3YEXgO8N6IePRU/BOSJEnjZSJJkiRpYnYpfz8GfkROGG1e3vttSuknKaWHgZ8C16SUEvATYE6ljEtTSv9MKf0J+AY5KSVJkjRwlm86AEmSpGkugA+nlD41YmLEHOCByqSHK68fZmQ9LLWV2f5akiRpINgiSZIkafzuA1Yvz78KHBIRqwFExIYRsd44y5sXEStFxKOAHYDrJi1SSZKkSWSLJEmSpHFKKf25DJp9C3AV8Hng+xEBsBh4FfDQOIq8mdylbV3gAyml2yc5ZEmSpEkRuZu+JEmSmhAR7wMWp5ROaDoWSZKksdi1TZIkSZIkSbXYIkmSJEmSJEm12CJJkiRJkiRJtZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVsnzTAUzEuuuum+bMmdN0GJIkSZIkSUuNG2644U8ppVmd3pvWiaQ5c+Zw/fXXNx2GJEmSJEnSUiMift/tPbu2SZIkSZIkqRYTSZIkSZIkSarFRJIkSZIkSZJqMZEkSZIkSZKkWkwkSZIkSZIkqRYTSZIkSZIkSarFRJIkSZIkSZJqMZEkSZIkSZKkWkwkSZIkSZIkqZblmw5AkiRJkiRJvZk/fz5DQ0PMnj2bBQsW9P33TCRJkiRJkiRNU0NDQyxatGjyZi6hAAAgAElEQVTKfs+ubZIkSZIkSaqlb4mkiFgpIn4YETdFxE8j4tgy/ZyI+G1E3Fj+tizTIyJOiYhbI+LmiHhmv2KTJEmSJEnS+PWza9sDwI4ppcURMRP4TkRcVd57Z0rpwrbP7w5sXv6eDZxRHiVJkiRJkjQA+tYiKWWLy8uZ5S+N8pV5wLnle9cCa0XEBv2KT5IkSZIkSePT1zGSImJGRNwI3AVcnVL6QXnruNJ97cSIWLFM2xD4Q+XrfyzT2ss8LCKuj4jr77777n6GL0mSJEmSpIq+JpJSSg+llLYENgK2joinAu8Gngg8C1gHeNc4yzwzpTQ3pTR31qxZkx6zJEmSJEmSOpuSu7allP4GfAPYLaV0R+m+9gDwWWDr8rFFwMaVr21UpkmSJEmSJGkA9POubbMiYq3yfGVgZ+AXrXGPIiKAlwK3lK9cBrym3L1tG+CelNId/YpPkiRJkiRJ49PPu7ZtACyMiBnkhNUFKaUrIuLrETELCOBG4A3l81cCewC3Av8ADu5jbJIkSZIkSRqnviWSUko3A8/oMH3HLp9PwOH9ikeSJEmSJEkTMyVjJEmSJEmSJGn6M5EkSZIkSZKkWkwkSZIkSZIkqRYTSZIkSZIkSarFRJIkSZIkSZJqMZEkSZIkSZKkWkwkSZIkSZIkqRYTSZIkSZIkSarFRJIkSZIkSZJqMZEkSZIkSZKkWkwkSZIkSZIkqZblmw5AkiRJkqSxzJ8/n6GhIWbPns2CBQuaDkdaZplIkiRJkiQNvKGhIRYtWtR0GNIyz65tkiRJkiRJqsVEkiRJkiRJkmoxkSRJkiRJkqRaTCRJkiRJkiSpFhNJkiRJkiRJqsVEkiRJkiRJkmoxkSRJkiRJkqRaTCRJkiRJkiSpFhNJkiRJkiRJqsVEkiRJkiRJkmoxkSRJkiRJkqRa+pZIioiVIuKHEXFTRPw0Io4t0zeNiB9ExK0R8cWIWKFMX7G8vrW8P6dfsUmSJEmSJGn8+tki6QFgx5TSFsCWwG4RsQ3wEeDElNLjgL8Cry2ffy3w1zL9xPI5SZIkSZIkDYi+JZJStri8nFn+ErAjcGGZvhB4aXk+r7ymvP/CiIh+xSdJkiRJkqTx6esYSRExIyJuBO4CrgZuA/6WUnqwfOSPwIbl+YbAHwDK+/cAj+pQ5mERcX1EXH/33Xf3M3xJkiRJkiRV9DWRlFJ6KKW0JbARsDXwxEko88yU0tyU0txZs2ZNOEZJkiRJkiTVMyV3bUsp/Q34BvAcYK2IWL68tRGwqDxfBGwMUN5fE/jzVMQnSZIkSZKksfXzrm2zImKt8nxlYGfg5+SE0svKxw4ELi3PLyuvKe9/PaWU+hWfJEmSJEmSxmf5sT/Ssw2AhRExg5ywuiCldEVE/Aw4PyI+CPwYOKt8/izgvIi4FfgLsF8fY5MkSZIkSdI49S2RlFK6GXhGh+m/IY+X1D79fuDl/YpHkiRJmg7mz5/P0NAQs2fPZsGCBU2HI0nSCP1skSRJkiRpnIaGhli0aNHYH5QkqQFTMti2JEmSJEmSpj8TSZIkSZIkSarFRJIkSZIkSZJqMZEkSZIkSZKkWkwkSZIkSZIkqRbv2iZJkiRJ0lJu/vz5DA0NMXv2bBYsWNB0OJrGTCRJkiRJkrSUGxoaYtGiRU2HoaWAXdskSZIkSZJUi4kkSZIkSZIk1WIiSZIkSZIkSbWYSJIkSZIkSVItJpIkSZIkSZJUi4kkSZIkSZIk1bJ80wFIkiRJmj7mz5/P0NAQs2fPZsGCBU2HI0lLhbtOvaLn7z70t78/8thrOeu96cW1P2siSZIkSVJtQ0NDLFq0qOkwJEkNsWubJEmSJEmSajGRJEmSJEmSpFpMJEmSJEmSJKkWE0mSJEmSJEmqxUSSJEmSJEmSajGRJEmSJEmSpFpMJEmSJEmSJKmWviWSImLjiPhGRPwsIn4aEUeU6e+LiEURcWP526PynXdHxK0R8cuI2LVfsUmSpGbNnz+f17zmNcyfP7/pUCRJkjQOy/ex7AeBt6eUfhQRqwM3RMTV5b0TU0onVD8cEU8G9gOeAjwa+J+IeHxK6aE+xihJkhowNDTEokWLmg5DkiRJ49S3FkkppTtSSj8qz+8Dfg5sOMpX5gHnp5QeSCn9FrgV2Lpf8UmSJEmSJGl8pmSMpIiYAzwD+EGZ9KaIuDkizo6Itcu0DYE/VL72R0ZPPEmSJC2T7BooSZKa0vdEUkSsBlwEvDWldC9wBrAZsCVwB/CxcZZ3WERcHxHX33333ZMeryRJ0qBrdQ0cGhpqOhRJkrSM6ecYSUTETHIS6XMppYsBUkp3Vt7/NHBFebkI2Ljy9Y3KtBFSSmcCZwLMnTs39SdySZIkSdPN/PnzGRoaYvbs2SxYsKDpcCRpqdS3RFJEBHAW8POU0scr0zdIKd1RXu4F3FKeXwZ8PiI+Th5se3Pgh/2KT5IkSf3hybya4kD+ktR//WyRtC3wauAnEXFjmXYUsH9EbAkk4HfA6wFSSj+NiAuAn5Hv+Ha4d2yTJEmafjyZlyRp6dW3RFJK6TtAdHjrylG+cxxwXL9ikiRNL7ZqUFNc9yT1g/sWSUuDvo6RJEnSRNiqQU1x3ZPUD+5bJC0N+n7XNkmSJEmSJC0dbJEkSdJSyi4UkiRJmmwmkiRJWkrZhUKSJEmTza5tkiRJkiRJqsVEkiRJkiRJkmqxa5skLcMcQ0eSJEnSeJhIkqRlmGPoSJIkSRoPE0mSJEnSJNv7ou/1/N37Ft8PwB2L7++5nIv3eW7Pvy9J0mhMJElSH9l1TEuzF118Us/ffWDx3wC4ffHfei7ny3u/tefflyRJUm9MJElSH9l1TJIkSdLSxESSpGnNFj+D74iLduv5u3cv/nd5XNRzOSfv85Wef1+SJEnSSCaSJE1rtviRJEmSpKmzXNMBSJIkSZIkaXqwRZIkSZKWKXaLliSpdyaSJEkaYHtc8r6ev/uvxX8B4PbFf+m5nCv36v33m/aiiz7T83cfWHwvALcvvrfncr68z6E9/776y27RkiT1zkSSJE1zHzl/156/+9f7HiyPi3ou5137fbXn35ckSZI0vZhIkiRJasCLL/xcz9+9f/F9ANy++L6ey7niZQf0/PuSJGnZZSJJGgCDPFbDIMc2VT51Xu8tfu4pLX7uuW9Rz+W8/tW2+JEkSZI0GEwkSQNgkMdqGOTYJEmSJElTa7mmA5AkSZIkSdL0YIskSY37wjm9dx27794Hy+OinsvZ/yC7jkmSJElSHSaSJEmStISXXHhJz9/95+LFANy+eHHP5Vz+sr16/n1JktQ/JpIkSQNr5uoBpPIoSZIkqWm1xkiKiGvqTGt7f+OI+EZE/CwifhoRR5Tp60TE1RHx6/K4dpkeEXFKRNwaETdHxDN7+YckSUuPTfdcnscfMJNN9/S6hyRJkjQIRq2ZR8RKwCrAuiXh07okvAaw4RhlPwi8PaX0o4hYHbghIq4GDgKuSSkdHxFHAkcC7wJ2BzYvf88GziiPkiQNpPnz5zM0NMTs2bNZsGBB0+FIkiRJfTfWJd7XA28FHg3cwHAi6V7g1NG+mFK6A7ijPL8vIn5OTj7NA3YoH1sI/C85kTQPODellIBrI2KtiNiglCMNvG9/+sU9f/ef995fHm/vuZztX3dF1/e+fPbuPZUJ8Pd7/1UeF/VczosOuarn31d/rVy6jq1s17GeDA0NsWjRoqbDmJZijZVHPEqSJGl6GDWRlFI6GTg5It6cUvpErz8SEXOAZwA/ANavJIeGgPXL8w2BP1S+9scyzUSSJPXJVnvMaDoELaNW2PM5TYcgSZKkHtQadCKl9ImIeC4wp/qdlNK5Y303IlYDLgLemlK6N2L4qndKKUVEGk/AEXEYcBjAJptsMp6vStKUW3W13OInP0qSJEnS9FYrkRQR5wGbATcCD5XJCRg1kRQRM8lJpM+llC4uk+9sdVmLiA2Au8r0RcDGla9vVKaNkFI6EzgTYO7cueNKQkla+qxeEjWrD2ii5vm72OJHDVpjxdwnfY0Vm45EkiRJS4m6t8GZCzy5jF9US+SmR2cBP08pfbzy1mXAgcDx5fHSyvQ3RcT55EG273F8JElj2X0nEzVSNyvMe1rTIUgaUPte9Iuev/vXxf8G4I7F/+65nAv2eWLPv6/+8SYSkuqom0i6BZjN+MYr2hZ4NfCTiLixTDuKnEC6ICJeC/we2Le8dyWwB3Ar8A/g4HH8liRJkiRpAryJhKQ66iaS1gV+FhE/BB5oTUwp7dntCyml7zB8l7d2L+zw+QQcXjMeSZIkSZIkTbG6iaT39TMISZKkQRKrrzriUZI0Oa49566xP9TF/fc+9Mhjr+Vsc9B6Pf++pKzuXdu+2e9ApGXZWqvEiEdJUrNW2PMFTYcgSZI0kOrete0+8l3aAFYAZgJ/Tymt0a/ApGXJa14wuHdUWnPVfFe0/ChJkrRsW3jx3T1/997FDz3y2Gs5B+49q+ffl6TJULdF0uqt5+VubPOAbfoVlDTZvANF7/Z54cymQ5AkSZIkDYi6YyQ9ogyK/d8RcQxw5OSHJE0+70AhSZIkqZ+8eK1lRd2ubXtXXi4HzAXu70tEkiRNod0vPbDn7/7r73cCsOjvd/ZczlXzFvb8+1p2xeqrjXhcFs278Ks9f/fvi/8BwO2L/9FzOZe+bNeef1/S0smL11pW1G2R9JLK8weB35G7t0mSJGmKrfiS3ZoOQZIkLaPqjpF0cL8D0fRmM05JkiRJkpZ+dbu2bQR8Ati2TPo2cERK6Y/9CkzTi804JUmSJEmaerNWXWPEY7/V7dr2WeDzwMvL61eVaTv3IyhJkiRJkiSN7aht95nS36ubSJqVUvps5fU5EfHWfgQkSZIkadl1zCW39/zdPy9+6JHHXss5dq9H9/z7krQsqJtI+nNEvAr4Qnm9P/Dn/oQkdXbL6Xv2/N1/3fOP8nh7z+U89Y2X9fz7kiRJkiQtDeomkg4hj5F0IpCA7wEH9SkmSZIkTWOx+hojHjU+y62+1ohHSZIGSd1E0vuBA1NKfwWIiHWAE8gJpqWCdx2TJEmaHCu9ZF7TIUxrq+55UNMhSJLUVd1E0tNbSSSAlNJfIuIZfYqpEd51TJIkSZKk3t154o2N/v76b9uy0d9fVtRNJC0XEWu3tUiq+11NE4tOO7zn7z54z12PPPZazoaHn9bz70uSJEmSpP6rmwz6GPD9iPhSef1y4Lj+hCRJkiRJkqRBVCuRlFI6NyKuB3Ysk/ZOKf2sf2FJkjT4YvUZpPIoSZIkLQtqd08riSOTR5IkFTP3mtV0CJIkSdKUcpwjLRPWWSVGPEqSJEmSpPFbqhJJd5/xXz1/96F77nvksddyZv3Hq3r+ffXXG7dfuekQJEmSJEma9paqRNLSbP78+QwNDTF79mwWLFjQdDiSJEmSJGkZZCJpmhgaGmLRokVNhyFJkiRJkpZhJpI0KWatMnPEoyRJkiRJWvr0LZEUEWcDLwbuSik9tUx7H/A64O7ysaNSSleW994NvBZ4CHhLSumr/YpNk2/+dps0HYIkSZIkSeqz5fpY9jnAbh2mn5hS2rL8tZJITwb2A55SvnN6RMzoY2ySJEmSJEkap74lklJK3wL+UvPj84DzU0oPpJR+C9wKbN2v2CRJkiRJkjR+/WyR1M2bIuLmiDg7ItYu0zYE/lD5zB/LNEmSJGlSLbf6msSaa7Pc6ms2HYokSdPOVA+2fQbwASCVx48Bh4yngIg4DDgMYJNNJm9cnlmrrDbiUZIkSUunlV+yb9MhSJI0bU1pIimldGfreUR8GriivFwEbFz56EZlWqcyzgTOBJg7d26arNiOft6uk1VUV3d98qSev/vQPX975LHXctZ7w1t7/n1JkiRJkqQp7doWERtUXu4F3FKeXwbsFxErRsSmwObAD6cyNkmSJEmSJI2uby2SIuILwA7AuhHxR+AYYIeI2JLcte13wOsBUko/jYgLgJ8BDwKHp5Qe6ldskiRJkiRJGr++JZJSSvt3mHzWKJ8/DjiuX/FIkiRJkiRpYpq4a5skSZIkSZKmoam+a5skSZIkSerB0Ed/3/N3H/rrg4889lrO7Hc+puff19LDFkmSJEmSJEmqxRZJkiRJkjQFVltj1ojHfrjqi3/q+bv/WPzwI4+9lrP7K9bt+fclTQ8mkqaJWauuPOJRkiRJ0vSy855HNx2CJE2YiaRp4qjnPafpECRJkiRJ0jLORJIkSZKk2masvs6IR0nSssVEkiRJkqTa1tjzzU2HIElqkHdtkyRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVYiJJkiRJkiRJtZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVYiJJkiRJkiRJtZhIkiRJkiRJUi3LNx2AJEmSJE2GldZYd8SjJGnymUiSJEmStFR46rx3NR2CJC317NomSZIkSZKkWkwkSZIkSZIkqRYTSZIkSZIkSarFRJIkSZIkSZJqMZEkSZIkSZKkWvqWSIqIsyPiroi4pTJtnYi4OiJ+XR7XLtMjIk6JiFsj4uaIeGa/4pIkSZIkSVJv+tki6Rxgt7ZpRwLXpJQ2B64prwF2BzYvf4cBZ/QxLkmSJEmSJPWgb4mklNK3gL+0TZ4HLCzPFwIvrUw/N2XXAmtFxAb9ik2SJEmSJEnjN9VjJK2fUrqjPB8C1i/PNwT+UPncH8s0SZIkSZIkDYjGBttOKSUgjfd7EXFYRFwfEdfffffdfYhMkiRJkiRJnUx1IunOVpe18nhXmb4I2LjyuY3KtCWklM5MKc1NKc2dNWtWX4OVJEmSJEnSsKlOJF0GHFieHwhcWpn+mnL3tm2Aeypd4CRJkiRJkjQAlu9XwRHxBWAHYN2I+CNwDHA8cEFEvBb4PbBv+fiVwB7ArcA/gIP7FZckSZIkSZJ607dEUkpp/y5vvbDDZxNweL9ikSRJkiRJ0sQ1Nti2JEmSJEmSphcTSZIkSZIkSarFRJIkSZIkSZJqMZEkSZIkSZKkWkwkSZIkSZIkqRYTSZIkSZIkSarFRJIkSZIkSZJqWb7pACRJkiRJzVtjtVkjHgfN2iWutQc0PmlZYSJJkiRJksTLX3R00yGM6uCdjmo6BEnYtU2SJEmSJEk1mUiSJEmSJElSLSaSJEmSJEmSVIuJJEmSJEmSJNViIkmSJEmSJEm1mEiSJEmSJElSLSaSJEmSJEmSVMvyTQcgSZIkSdIg+NVpd/b83X/f89Ajj72W8/jD1+/596WpYoskSZIkSZIk1WIiSZIkSZIkSbWYSJIkSZIkSVItJpIkSZIkSZJUi4kkSZIkSZIk1WIiSZIkSZIkSbWYSJIkSZIkSVItyzfxoxHxO+A+4CHgwZTS3IhYB/giMAf4HbBvSumvTcQnSZIkSZKkJTXZIukFKaUtU0pzy+sjgWtSSpsD15TXkiRJkiRJGhCD1LVtHrCwPF8IvLTBWCRJkiRJktSmqURSAr4WETdExGFl2voppTvK8yFg/WZCkyRJkiRJUieNjJEEbJdSWhQR6wFXR8Qvqm+mlFJEpE5fLImnwwA22WST/kcqSZIkSZIkoKEWSSmlReXxLuASYGvgzojYAKA83tXlu2emlOamlObOmjVrqkKWJEmSJEla5k15IikiVo2I1VvPgV2AW4DLgAPLxw4ELp3q2CRJkiRJktRdE13b1gcuiYjW738+pfSViLgOuCAiXgv8Hti3gdgkSZIkSZLUxZQnklJKvwG26DD9z8ALpzoeSZIkSZIk1dPUXdskSZIkSZI0zZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVYiJJkiRJkiRJtZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVYiJJkiRJkiRJtZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVYiJJkiRJkiRJtZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVYiJJkiRJkiRJtZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVYiJJkiRJkiRJtZhIkiRJkiRJUi0mkiRJkiRJklSLiSRJkiRJkiTVsnzTAbSLiN2Ak4EZwGdSSsc3HJIkSZIkSZrG7jzlW43+/vpveV6jvz+ZBqpFUkTMAE4DdgeeDOwfEU9uNipJkiRJkiTB4LVI2hq4NaX0G4CIOB+YB/ys0agkSZIkSRrFo1aZNeJRWlpFSqnpGB4RES8DdkspHVpevxp4dkrpTZXPHAYcVl4+AfjlJIawLvCnSSxvshnfxBhf7wY5NjC+iTK+iTG+3g1ybGB8E2V8E2N8vRvk2MD4Jsr4Jsb4ejfIscHkx/eYlFLHrOigtUgaU0rpTODMfpQdEdenlOb2o+zJYHwTY3y9G+TYwPgmyvgmxvh6N8ixgfFNlPFNjPH1bpBjA+ObKOObGOPr3SDHBlMb30CNkQQsAjauvN6oTJMkSZIkSVLDBi2RdB2weURsGhErAPsBlzUckyRJkiRJkhiwrm0ppQcj4k3AV4EZwNkppZ9OYQh96TI3iYxvYoyvd4McGxjfRBnfxBhf7wY5NjC+iTK+iTG+3g1ybGB8E2V8E2N8vRvk2GAK4xuowbYlSZIkSZI0uAata5skSZIkSZIGlIkkSZLGEBHRdAzqj0FftoMe36Bz/klaFrnvW3oNyrI1kaTaBmWllSSNFBGrlMeB209HxLMiYtWm45jGVm86gGluzaYDmM4q+5aBPGeIiEeXx4Hb9w0698tSZxHxgohYv+k4Bt1AHhT6JSLWbTqG0UTEXhHx/IhYp+lY2kXEa4FTImLjpmPpJCKeGRFrNB1HNxGxXUQ8tzwfuMpORGw9qMsWICKeMqjxlZPkuU3H0U1EbB4RjyrPB3Hde1FEvKvpOLqJiJdExIXA+yNi06bjqYqI5SJik4j4DvBegDRAAx9GxE4RcSNwWUrp703H0y4idouIS4EPDOI2HBF7RMS1wBubjqWTEt9/RsRWTcfSSUS8MCJ+xODOvxdFxCkRcWjTsbRr27ccA5BSerjhsEYoJ3q/otzdecD2fXtExBkR8foBPe6+OCKuBl7ZdCydlOPu+yJi16Zj6aQcO94TES9qOpZOBrneAhAR20bEtuX5QG0fpd5yHfAlBjBPUpbtF4B3RcRjmo5n4GZQP0TEihFxKvDNiHh/ROxcpg/E/x8RcyPiu8B/AIcCHx+ULGg5gf8B8BJgYUrpD03HVBURj4uIW4DLgW2bjqeTiNgA+ArwpohYL6WUBmXHWda97wMfBi6MiM2bjqmqJEHOB84C/isi9mg6ppaIWDMiLgNOJu/Q39iaf4OwfCNis4i4CFgIXBYROw5YRfsx5WB4FPCrpuNpF9lbgP8HnAtsAbym9V6TsbWUE7t/AQl4RkRsB83HFxGPiohLgKOBdwN3RcTzByS2iIiVIuIc8rI9C1gNeG0M0MWmkpx5P3B8Sun4puOpiojlI+Lj5OW7GPhoRBzQcFjAiOX7JfL8e19K6UNNx1UVETMj4mTyvu975ETmweW9Qdu3AGxZ2bc0Xm+OiEeX5XsM8CngdxGxWcNhtda9NSLiYvJ+7xrgzcA7m41spIjYibxtnJZS+nTT8bSU+bdcRBxDnn+/AI6OiNfFgLScioi1I+KLwHuAPwOfjIiDynuNbhsxbGDrLRGxckR8DrgSeENEzB6Uc6JSp7+UfFybD/wWmFvea7zeUh53Iq97C4GZwJsj4sVNxtb4AWGKHAhsCDwPuBU4KyJWHYSrKxGxMvmKwNkppV3IV5X/RoNJkcoKO6PE8SDw6pTS9RGxWlNxtStxbgh8Evg08OyImNNkTF2sTU503Qa8Cpq9cta2fN8FnJNSeiHwa2AgTgYAImIt4BTglpTSNsD5wNubjWqEZwNDKaXnkk8IZgFHQPNXRksi+iTgxyW+z5OX9SD5CLBmSmnblNIlTR+o25Vl+Hjg9JTSZcDZwEqV9wbFE4CfkysWb4SBiG8D4NKU0gtSSlcB/wPMgeZjS9n9wKXA88uyvZh8F9s/NRlbm52AS1JK/x35YthAXFwqAlgHeF1K6UxgAfkC2NMaDSpieWC1snxnAVeklC6LiBViAK7cVjwMrAockVI6H/gApT7ecN1g+YiodqN8AvAzRu5bGq83k7eNb6SUdgDOI6+P/2wyoLLuUeK4LKW0fUrpQuB4YOXmIutoB+Cssm9ZIUrXxaaVffPDwKbA0WXbOAp4B7Bj04maYlPgx8B2KaXTgTcxXO9rdNso8y8BT2S43vJZBqve8m/gu+Tz3tuAfWFgYlsOuKDUW75Bbun4bGh+v0xOGgHsSD6ufYWcRF8dOKTJc/NB2Cj7pu3E5AcppT+nlM4Fvgl8qMNnpjK2l0bEximlfwKnAhcApJR+CzyGnExqyswSy0PkefUV4I0RcRSwMCKOitINoIkde0QcUbKys1JK30wpnUquTGwObB0RK0x1TG3xLVd9JO84VyRXyJ5UTXY1fPK8EnAP8FB5/SBwZ0Rs2FxIw/MtpfQ34BUppQ+Wt9YFfhQRj2swtjdExHvLy0cDTwJIKf2avIy3joh9ymenfNlW1rl/kq/Ef7DEdxqwwQCc6D2mUmk9B7i/XF1+HfDhyE12Z5fPNjH/9i/75lZT8F8Dh0fEe4D/Ap4cEQsi4ilTHVuJ79CIOLBtOd5G3oZ/Avw7IvZp4qS5zLu9ImKTlNItKaVzKm+vDbS6V86Y6tjK774hIt4aETsApJQuSSk9FBEvBy4CnhgRH4jS8qKB+HaPiC0jYsUy6ffAyhGxH3AtcHpEfDga6vpelu/OpcK6DnmZrlTevgb4K/Cy8tkmtt0DgHvJLUQB3gocHBFHklv9nBQRJ0XEk6c6thJfa/6tDqwBrADsExFvB04kXwh7RxOxlfha8++EyuTbyPWC6r5lk4bi2z8ido2IlVNK55aTeFJKdwFPAVpDBzRRJz2AvP4fm1L6d1FmUdQAACAASURBVGvfF7mV2WeBx0fE25o62YuIeZG74LdORu8kH3sPIO9bPhURRzcRW4nvsIh4V6nXQ24J9yiAlNJ3yPN2e3Kdq4n49orcjXI14Cbg3NKKZga5jnBT+VxT55NviIiPRMS+ZdKvGK63nEfz9Za9ImKHiHhUSulB8kW5rwC/BJ4WEU8vn2ti2/2PiPhMRBySUvprSulzlbcTef/XWGuzyMPK3Aa8oky6FnhuRKxY9n33k3M5hzQRHyyFiaTKVYFqBnENYJ3KRv5O4CUR8aSpblIXEftFxA3kLmwnRMTeKaXfpJTuq8T+b2DKK9sRsXdE/J18wgRASumX5ATIa8hZ7pPIlcfPl/enLAMfEdtHHm9jB3JXu0ea+6eUbgO+Qz7YNFVRfGHkJpvPKjE9XNat2cD15BY1twLHRMTbI2LmVGa5I+KVkcc7+EBEzCtjlnwX2DnyOAMbk69AnhVlPKep1D7/AFJK90Zu6jyf3JrrryW+XaZyxx557LJLyVee3lImXwUsjpxYfQa5xcWXyVfOVpjiZduad1tDnm/AzeW95SKPL/U38vo35SJiq8hdZE8EzouItcsVlbuBbwMvBn4HHAS8vZwsTOX826JsGweT9y+fjYhHp5ROJre22J58Zeo15Kvfe0/lSUHk5vRfAvYmH7cXRsSW5e1tgd+klH4CLALOJDfNnpKKbdu8e36JbePyXiup/8hYHOUCxZSIbLWI+CywJ3n+nBR5DIRWbHeTr/LtBNwOHBQRs6Ywxm0id21/O7llypGRu3HcT77a+BJgL+A/yVfDXzzFdZZHRcRXgdcDLye3/v0nuUL7znIC+nny1dv9y3YzldvuMyPif4F9gA8Cy0fEmimlG8ndJ3YnHzsOJ7cE2iumsAVGh/l3Jnkb/iDwd3Ir4GeSE2B7R8SOUxVbia99/q1c2bdtB/y2bd/ynvK9Kamjts2/fcjH/03Ke62WPgvJ83Cq66RbR8T/APuRT45TJVkDeTvZltxNZi45cTiV2+7ssm95G7lF8rGRxxL9N7mu8HzyOrkA2CMiXjBVsZX41o+IK4F5wF/IwyusB3wfeFlEfKzUu64nL9+1pzi+6rAjhwCfAB6VUro9IqIcyzYnt36c8lYrEbFO5G6ULyG3kjo/Ip6QUjqJ3OJ7e2Abhust+0xxvaU6/15LPuddL6V0f5l315L3Ky+DKd92V4+IheR5dznwkRjuvtvahm+g9NJoorVZ5KE8XkW+oH5emfx14D7gixHxDXJ+41Jg1aaSXUtNIilyk9wTgI/9//bOPF6v8drj35VZEDFWjInEHBVSswRFIlTRooKmZmosNdProlXzLCKmooZcWnMMvWqIJERN0ZiqdYmxhiaqIkLW/eO3ds7O65w4J3n33i+e3+dzPufd03t+Z+1nWM961mBNVu0MNyJlYk0Ad38HuAXF4JbW+U3W4GHAL9z9B6gDrRDX2rv756Z8OiuhUABsdjfjIrn1ADZHk/UmZrZ+7vKDwG7uPszdx7j7fwFTzWxQGdyCn6FB8bfuvgPaQX4zrmXt+HrkLr5mnF8o92yRvDCz9dDA/V1gg5gMs7b1b+StsgywFRo0O7v7jBKVsQEoVv844C6Ur+nH7n41MByY4O6bu/sv0A5LKblWvkp+MGsAv8zdV3blurgL2Knogd2a8CNktLwRWAPlG1rX3d9FORp6xPXbkWHO3f2zimS3fq7tzYjfM5Hx95/hAVkKcvzaAceid/gjZMw6J/rnr4Bfuft27j4COAv4DhEGVRLPzsBglANuEFrQP4UWB6CJexow2d2nAhOAVdz947I4ohw+nwFZn70VuDZkmO3q3Y4WWk/GucLntjnILlMMsxwrLwDPWslJP+P/b48WIHu6+81ovDsT6Bf3POTuz8VO6XNAV0oKkwmD0S9QaPsWqP0vgYz6Y9F7XwGY6u6voQXWFiUvWLoCH7j7pu6+HzA5+P4WuBTNuXe6+9HIg3lAWcTMrAtKWXBJjC0PogXTp3HLkcDW7v6iu78FPAGs7u6flMWRL8vvdeB6d38ZGbrudfdJ7j4JGdV/WhaxOchvRtwyp7GlLINwrfxeQ8ZMcvPZF/FTpoFrfiSTke6+LeqbvfN6nbvf5O4T3P1NtNAfVHLf/Q4wyRUCeAyKNjgVGd76IAPIG2EoHEOkXigRiwGvu/s2rlxNN6L3fT3K4fQOMMrdD0ZzyJZlEbPm045MJXTj3HschHQ/rHxv0S7IGP0TVxjgCPTOAR5idr3lcWDlsvSWOchvVtoWVwTOX4BFzWyNWMeXGWbZFdjb3W9HnluZF1w2/j2B9Jb1W3i+EOTWDkOAi939MTPrYWYrxPvbHfWPs919TzRe96rC2AXfEENSCP1C5PkxASW+PSiUXGIQ/wPaPVsyHrsf+EcJ3BYyJb1tH4rCtu4+JjrZqsDSYcTJ0BMN6JjZpcCvilqQ5ri1c/e3UYP9PVJmR2T3ufuHsbuXPdcLye7pInjV8OsZ/By5Lg8IeR0BbByL/G7B8yMUMzrEzMYAd4fcC5u4c989GXkL7IN2TvrlblsG7XiPRTI7CYUZdS1SGatRqDZEOUvGuPtjSCHMXNinAG+Y2TJxPDE4F74QbaX8cPepuX7wALCw5bwPC4IFv3HARjFRL468Aj4LXhOAQ919sLuPAt4HFsq12cLQWtkFtgCeATB5UJUZvrMg8AlN3lBnox3IPYGP3f2G3Lt9Ay36Xy+alMlDr7e7T0ceFTfDrAVSOyRXkLL7d5ryh62JPNEKnT9N3qtZGMlyyCCSzRV3AN2BrVH+jWWRAWdVZJz7ft4YWwC3OcmuPXqPeSP/p8Hto6I41fDb11QooiuS079Q+AvIEN0RzR+1u7ODkPJdqCHJ5IW0qMsr9FRgVFwaizwF5nf395DB8AnUV0CLhJeK5Bb8ts7pSiugjRAAwmC0nplt6+6PIEPwtaHTdEWewUXz28XMerp2ts8PAyGonw5BuRNx98999mqB30Wej0Xzm5P8jgFWNxV96Qp8x5qKXHREC76i+X2V/DJdoDsKJ8qPLZsVObYEvznJ7ziUIiCfYPZJmvJPFmrgMoXXfcfd/+Pux7j7/8Slx9G4u2QLHBZHi+ZCEWNL5rnTl6Z3+RpwDvJCWgmtmd5H7xugAzKGFc1vsDV5fPZEa6CdzOwsYCiwHzDQ3Z9397Ny+sF8KByqaH5bm7wqp6FNh2xumy3tiDV5rcwAnjOz44BxVnDS9xq9YHFkTDrQ5EjxM2BXM9sO6V35vKf9KEdv+Sr5TY37shQWd6Fx5w8o5HKlArnl9YLOaJ4/0czOQ04UO5vZHjm9oAsyrJeqtwALxanJwPfM7OdIb7nEFKq9pLs/5e53x31rI9tHJfhGGJJQh+kH/NwV33g2aow75e45GZiOwor2QTuSU4skZWYHoY58HmoA3Vw5GTqguOlXUcWT41FIB2jQ/zmaGKcCxxexIK3hdqmZLeDuLwC4+9nITW6vuLdD/F7UzI5Cyu3zaBIqBGZ2CIo7Po0mg8dBSF6PoYXKWcgt8azco99Hi+rxwPeLUirMbJiZPWRmvzGz9WK3c7K7P46MbJuY2Qpx+1NE0jZ3P4Img1JhhgZTPquzzGzbOPUcmmyyyhcfAjNNORk+QAP8L00hZEcSHnEF8muN/Hrm7m/v7m5muwJXAH92eRAUwS0fAvhjd3/HFabYKQyu7xFji5lZ8OpkqtxxE/BwkTsDbZFdzkDTH01IfwbWQv23KH61IZRTkVfeZqaQp7WQQr0aGrsB2pnZMJT0+FmgMI8uU5jdS2jhcaqZHe/ub7j7lJxy2B0t8kAyfRyFQ/8FhX+eWNQ7NrONzex5lITySDP7pbuPRWPfiaZQopOB21Cy3vHANu5+cnB6Ee1Q/rMAbq2V3XzQ5A7u7i+iRXKhRSRMoSbPIi+pocC5Lk+el1F1k9NQbq7/RUYjTBW0fmpmE9HC5rgC541NzewtVFHnBjNb2+WN8rEp1K4DCq/LxrbRyOunn8mNfTVymzwF8NvQzF5DCWRHmkLvH0Y5NvLeAMfE/wDQ0cx2RxsQU4APC+y7+b5xeCzesmudos3/AekBs86b2U/i/S4LnFsEt/hbrZXfcUh+Y5EnzWlm9jQygI2q/d468mut/DaP048A25cxtgSH1srvWCLELjAJeMnM1iyCV3DbzMz+hhacp5nZjrlr7ZEeNRoZb7Lzi8V8mL3bawrklx9bRpnZGrEeWtXMBoZR9R202frL8ML4I7C9KfyoN3r3RfHLy+8MM/thLISvRB6sayHZ/R8KgepoZu1jbHkZLehfK3Bsybe9EWa2s7u/4kqvkIVBz0BjdN5rZQ8U4bIssLkrzUYR/Gr1giPd/VlkHOyJ1sA9kAf1AUh/KVNvaav8ZsZzQ5B3zePAmnmnhTpyq9ULznMV1jgJrWP7orx/VyO9YMPg+AZyUClsXGmG3y40rXknIn1qoLv3R7aCJVBkC2a2lZlNQOu3wvruV8LdvxE/aFf0kPi8AOrcw4GlcvcsiXJx3AgMK5jPYmhwWQoZ7K5DykOvuN4tfrdDBpIz4/g3aIGwbAXclsvdszXwbu64PbAZ2sXoXbDsVgPuA7rH8eVooMkSfA7P3dsbuXD2IKqgIPfNIvmtg7w7NkVGl5vRQi7P6ffA0Baeb18gty7xjkahnaab0WITZIC5LrifHvxvjmv9kAIyAlix0eQX7/4k5K23UYHcBiAjZBZbfh+wc1zrHL+HxtjSJffcxvF/DGw02cX5O5Fxep2C+dXKL1uwLxtt7t6Q6aoojGJwPLczWlQV9m5zHHdEichByuuNwNFx3A55OE5E1Z/I/e4BrFQwN0MLpJ/E8cpocTIUJefdBikZm8b1u4G1c9ytwWS3cO7Z7iW82/2Ag+NzBxRqdVQcb4TGuE3i+E9I8Qft0hfa9kI+p6KwXNBi+HxgSO6ePsD43HHXTHbAMiXI7yBg//i8EzK6bY5yNL2Q+z8WRgVC+qA5Z3dgs4K5Ndc37gAOzF3viPKYDMvOxe8hwIAGk98fkQ7WBXlKrd2A8uuQ41zo2DKX7W/lOLcwxerMHdGm61ZxvDUa+3bM3dMFzW+Dc+cWRrl1Cm17LYwtF6O8frujCnfZO14X6dSLxrnFgD4F82tOfqOAH8XxgSjsL7v/KWDX+LwNMd+V3PYuB/bIXV8S6V7ZmJIVHbgQWL9gbs313btyfXeX7HMc/xnYL8e7UL1lLuWXrYHXR+HaRXKr1QseBE6J4yHA6bl7rwGOyR3PX4Lsavk9hDZrOqEx8LHcvSfluK9MwfNGa36+KR5JIC+ZfmbWwxVDOBG50y8Cs/ITfeDud7n7UFf1trrClNguk+mHyJV+cZfldTgasDeDWWFYxLVuKM4VpKRv7+6TqSNayW3zuLedu48GxpvZKDO7Ei1WH3T3Q70Ai7uZLZY7bI92ZDPvmXFoAbMlCpHZwMzWjmt9gb+7+9suV+MLXAnC680vHya2Iirv+hCS3R/I7Y6FfB4G+sYu0WzVMLxY1+tOyM3xYFfZ7WuAXcxsR3ffByV9PMDdj0UeUW8Gp2fc/dfufoCrAlldMY/yO87dPwRGuErqji2QW20I4NNEUndXGA9Ixgu6+6fWlAvhUXffyRXqUVfMq+zi0uHu3t/dnyiYX3MhlMPdfXK0uYNdYYAvIM9CC97/4+4b1fvdBr/uNnvFmrWJcFjk/XQ+MMwUrjATuYs/jhKnjkQem+1jjHm5AH61IbwD0HsG7cR+ggz93d39bnc/0t0fMrO+yDvuadBcEs/Xk9u8yO4y4EKbvQpjXRH8+ltTmOtAmsJyPwf+CpxgcrUfG2PcwybPuLeDK67qn0W0vW5mluVdmIkS7mahJlcjr+BtTAlwQQaFB+PZi4D9zczcfYprd7Te/GaFt8epDWmqjHQvMjQc7u63Am+aPF0Nhdi1Q4mYP3X337vKJRfBb059YzpwgJkt7sIM5K08DJrCf939HncfUxC/uZXfTLRZ96m7T3T3pwriNy/y+zx+131syfGbl/b3SvD7VwE6czcz6x7fPwMZzpePy+PQwnhY7p5PkQFkj+w7gtdVBbW9rxpbXkT5tu4EOpk8Wx0tVBd09w/i2ffdve5FOFohvyVQYYMuqE32j+c6Iy/gSfHs3aHv1JvfV7W90Sjhd5b3qBezpx050ZX249DQdYrgN6e+Ow313YXQvNvDzLL8SO8TqVtcHvVF6S3zJL/43x5z97pGQLRCL3geONQUYtkeFWjoH/d2JtZFcX8+NLosfpOQMXgB5JH8vJllRX76EOGV7v5SEfNGW/FNMiQ9ijrPHgAh3HVRBYofEpWgzOrvFmlywbwYdZLLzGxoDOy3EK78rvCDV4DeFuXVzayXmZ2ByvpleQXqGq7TRm59zGxpb3J9/BxZa1909zvqySvHbz4zOwcYbWbHmdkmSJF5BXX0+dDgmcXof448tq4JA9dJaOFcGEzl3i8ylYkGDTJZPP4naGfsbVMZ3wzXovd6C7CsBerMq7nvm44WeFnSxOeQy/WWpmoOb7sStxlSMj6sJ6cWeM6r/JaPxdS7BXBrTQjgF2Z2Uu6xu5G78LJefD6GeZVdz5BdIdXaWiG/D+K+k4PzK9EVjkfhJ88VwSvHbz+UU+a/gStMeTdGoupSC8cC6XGUMy+bqJdBFUbGIUPNXkW9Z2s+hPcElAx/s+D0GgoFzEKNu5nK+t4OPO9eTOXROsjufSS7olzpD0Q7nMeg5O2LI6Pq3ma2m5kdg0Iq70Eu4ZhZ1+jLf0aV7j4uQnbxtw5DhqLhZpaVpL8cWMvM5o/x7Ak0Zm8a15cG9jWFIkwDLipiAR/88uHtl8XpC4BBpjD8fyPvwn+Ywnj2RZ6Ff0QL/ImuUP2i5NeavvE66ht75x59BPjEis/jk+Q3b/waVn7Rd59B48pvctwOMpUq3xUZaiajKIcMk1AhmoUoEK0cWyYgfXlllC5jUzO7EXksT4jvKXLsa4383kZj31XovY9Cxv1XiaqzBfFrTdt7DM1/WdGNpZk97ciJFIQ29N2nkLfy7Si87QpTiNSbaI4ril895Hd8EbpBG/SC+1Cu3TEo5O50U/jzO8jbsBC0gd/9yFj5ONrMXtfMxqN8jxc0/+3V4BtjSHLlLrkdJVreyZQj5LP4udPdf+fuMwpSyrZFYWErIiPHCWa2MhoMl7Mm75lxyHjz7zCQnI68bjZ29wfi/6g3vzZzAzCz/dEkuZS7n/Xlr60bjkXeUFuhznU98iS7Ks7fidxiL0ZhCF+4+8koDncCCiWqu3dZBpM30YbIwn6wKafQoyiT/1FxmyPvkH6xUOmMdurfQKFEB8RuX73fbRZ3jDXtCnyB3vPeoWDcipSx/yDLO2a2KXrf7Zk9v1TdUU/51ZlXFzO7EMU+/wntLB7m8sS7H8V4P4M8GvdBlWuyUsMz0MK0sEVocKyH7PYvaCe5LfLbGyWX7WLybDkXhRINdRVCKASmnc4NUFjBNkjxOhF5AlyDKt0RnMbTNB/2RaHS27r7Cd6UC6He/FZFi5B+7r4rsKCZnezyGjsSxctvDFyClOvM6NsRGeiGuPuZUP9542sgu2WQfNZ2952BfyKl+12kuC6LvHuGowXWv0y7f9PQTu027v7fUExBAVNBiiFIHvsDa5rZT5Fx7R20kAItphYkPPPQrvxElJfmaC8uD9xiyJDbD9ge6GLyXpyGDAmHx61TUc6mHq5kqYei/JKD3P0UKEx+c9s3QHrLHl5QHp/gl+Q3b/waVn6mCk0/RH3xQLSA28flFXVVnNsczWMfo4VdhmfQ4q+w/KttHFu6Ih1+IvIy+x2wpbufC4W1vbbIbyrQ0VU1biiaW7Z396MKNKC3pe29R9PYvBYKJ9vO3Y8tcGxuS999DMDdX0d5kc5Ec+/hBW7gNKz82qgXXAbMdPeprgT+WYXPXxS4cdhWfv8xs84uj7L9kc53aNEb2G1F0VWPSoW7jzOz36L4zFNRFbJni/p7Jre8mcjq/35wuDsW6j9DC/rlUPLnp9z9WTP7AuWgedLM9vaCSjGaQjG+aCO3bPfiCVSysZBFQI5jF+QePNwVunSPmU0DznH3A02Z6hdyVa/BzD4whSi85UrAWLQnUgfkcniUu080sylogtwTeULdZmYjXRXFZgBT3P0TU6jPSUUpYmY2CA3Wk81sjLtf50oG3S4G5z+ZdvDWAK5w9+fM7BFklHse7STs7HV2BW+GZ0PKL5CFAO7g7u/F3zzBzN50931MlQGXd3lvbYJK1E4DVZBDA31haHDZwdzJ79P4307yCO0tEq7Qww1QGMTLKD/YUDT+nQ08Y2abu/sD1uTiDHCZu19SND80/85AmwlTkHH3GDN7wVU9cxZMifv/Fv/XBxTc/hpNdmaWVVDMMAPtcC6BFsHZzuyh7n46quyYPbsr8K+c4npdvfk1g4+IhO3u/pqZnYs2Sz5AGyA/MbNx7j7JzD6lKeRj36Ln3cCHyMN3MXd/y8yGI11gXeTlOMLM7nH3CWGczkJQZ6BcZkWjrX1jVuiGFxAC2AyS/OYNjSy/bqiK1BfuPt1UoOKXZjbJ3c83JSX/DOQdShQWCH6TCuYGbR9bsgqG/0JeGEWjLfJbEOWWwpUIfHQJ/Nra9rJ18n+XNDa3pe/2okkv+A8ROlYwGll+bdULPsiOi7QVzAO/Dz1SangBIXb1wjfGIymDKy/M/kBfd7+43t9vZj1ikZTFJYNiKj+wCFlDVuENkHJ9HaqacIOZ3Yl2dLPY1boakcxsqTAU5fPwtIWb0xRzXvcOb03hLsTf+DT47WxmCwfHR1HY0Eru/lksUtcys1uAqa4KVYUjZ5SZhDo6aEB/DCUwfBN5+1wdC65dgG6x4Pmi3gt5EzqYqqqdhjy0HkIeeNvBbO0Rd3/R3W8OI9IyyPL9clx7swQjUkPJrxm0NQSw7vldMsTfyB83lOxq+QXmWn5lGJGsKW/TlUDWP15Gu+890Fh3NLCfmd2FdrrHxTNl7fY42jXOh/D+BVgpxkMzs2XN7BK0Q1n3/FYwy6sof9xQsjPtyHl8ztriTLS7eYopD8cAtLGwhEUpdTNbxsxGoJ34QmQ3B3RFMlkNwBUa/h+0UfNn5HV0hZldjXYos8VxIbvceYQMO6PQ142D33ikl/RCOsC1qDLVKOThUHhJ+hq0tW8UXlY9Q6PJz2bPUZchyW/u8QUaX3aJsXFBVElsnbg+w8yWM+Uw2xCF6pSJto4tdc/f8xVoq/wKa3u1fWMu2142txXhQZOPKsjmtobQC1rg21DyawYNoxfU6lVzya+0cXle8I0zJIGMIF5ntzkza2cqHfw4CnPplLv8ELAKCi/p7PKgeQBlfv872sW9FbjH3beMnYF6cmtvZqeizrxznMsacaXcgkuHkN2tZravmS2fu5yVMxyOQmKuQeFte8ez3VBowtPu/rN6c2sJOaPMPSiJ3erRpp5DLpsrohjXu5BLZDtUNaEIV+GsYsrnyO18qKts6h3IqPClySjaawfTbtV9wJNebBhRfzNbIDtuMPltlw3SOTRSCGCXHFdrJNk1w6/hQijNbGdT6dmFM445Q/oTyMi2RRy/jLwgF3P3G5Cb/dUoDPA2KCRUYpiZDTKzpeI4S9D+V7SDtyizh/Bu4UrS6khRnIKqwtR9x8zMfoHK0K+RnWsw2e0D/M3MhuXPxzx2KXKdvwolpRwOrITCO0DJZ98G1vMCkt0Gvx+bWb/snVpTYvHJqC+slZvvbgd+6krQeiryKn0cye/JeK7e8usRv2cZg12YhhZ3Pc1srbg0Dim2X7j7RShU4m7ge+5eSL4NM/uBma2e6Ss5+VXeN4LPoWa2X35B2mDyOwLl0Fshf76B5Le9mfXN949GkV8zfTcblx9ACe83QIu86SgMa7e47ijcfTpKS/FqvbkFn51NZcEXjON5GltK4Ndo8vtS35iXtlfA2LwfMM7MBufPN1DfHWZmm1jk+5rXvltP+ZnZSs2dbyC94Et6VSPxqzu84rJxX5cfZHD5Iwq1yp9vH78PQOXV14vjPmhHt0vBvH4AvAD8GiUaf6JRuMXfysq0Dkdx3aOJMp85fh1QR1o8jo8Adst9R2E8Q34XE6VQm7m+PAolypeHvJ0oTVoCvz1RjoDT4ng+ZDjoGMc3AHs281xWfnsHtPArit/myJ32Upopk1ml/FBM9rPAzcDqLdyzCgqFXSOOHyHKWCMX1CJLCm+J8gtdBOySO9+uatm1hl8DyG8jpCzfi3bBriDG55wMF0VlaW+iqZT1aOD7RfGq4TcGGQTPRuNgVvLWcve1z8a+OL4NWDo+dyiAV1bm+7fIeN+/9noDyO77aMNjdPz9oXP4X7rljkej0HGI+aUg+S2PDG0PxHs9FVXVg6axeW00Lu6Ve/Y+yinFvC7aZHihOf7xewXgZODXuWv/i5T/ovltGn33frQhcjwxf9SML6X2jdzf2SjGsjupmTuqlh+a/+cHRqDxee28LKocW3J/ZyW0mz4a6X6/yvWPbCwpXX6t6Lt5OXbJyaojmmMWjuNOBXLcJNre/UhP/y0wX/bu43eVY8uc+OXbXunya23fqKrvxt8ZHO/qAeRBtmGt7OK49L4b8lsKGQIfQHl6rifWEDTNbVWNff1Q8ZGXgV5zuK8qvaATLehVVfMr8ucb6ZFUb8Ru3orAha6cJN8zszVMsb5fALj7CJTA+mhTUtxRwGseeUEKxL9RYsQT0YL5bTPLXEhnVswNZHHt6e4HusIOM6srHhU3XN4Wf3OFsa2DEri9n7uvrjytCduhUL8dgM1z3haz4O6vIc+PvmZ2RLgjdkSeIYXwy/FcAIWWnAFsZWZ93H2aq1rSjPCK60KNe6aZHUxUUXL3W939/drvnkdeFl5wB6IKIJe4+889Ynhrdr8rkx+qXHahu+/kLeQu8IpCAM2sDzL+Xox2Jn5gqmQG4SlacdubE7/8+y1dfpm3HPysvQAAE0pJREFUHXKbPt/dt0KLgenIVR4Pry5XPqHr0Vh4k5ndgxTNl+rNqxl+Q4LfEKSQTaEp14fnHpnpXw7hfTPuq7dnbfv42+1RstZdXPn6vlRlqCLZmSkEeh9UsWxrlG9jo7g+2xjtwkdmtnbIbhpSNPECElLGnO9I2Z7g7pujRXI3IKtOlOkET6Fd2cFmNsLMbkfFP16vN68cv8wTeQAyQr9vZvvGtdnanrv/A4UorGSzh7f/vUB+HaJvHAqc5+6DkKG6B6o6NKvvBkrrG8GvY7SxY4BJ7r6tK9dM5+yeiuXXKeTTHnlybx3tbJbXaFVjS8YvPm4M/E/03zOQ8ea4jFP8/VLlZ6om5WiD44k59d3AZ+7+ppmtgnTmKR4e+x45furMb4GQ3zCktwwC/oBCwzJdOZNdFWNLa/jl217Z8usW8umA+saQ2r6RoaK+u0Do9McCI6L9vUaEjzeDsvvuEiG/BYE3g9+BKJfPyLgtm9vK7ruLx8c1kKHmMWA7mz0yaBYq0AuWyOlVa9CMXlWzLiqVX+GotSylnxYtiJehknuHoIV75mXTO3dPZzSBXgAMq4BjH2S1XjmO2zUCNxRe9ztksX4FeVUcgapJZPd0QYuHl5GLblFc2tG0q7MWqgy3HdoV7Vlzb/vc534ojGMicGqJslsufp8OXF9zbQng3vi8NLBjJsuS5Pcz5LL8nTjeGnmgZTuOnXLPFS6/Gm7tkQHke3H8c7RL3zWOO+Se6RD/xyTguJJktxtKMp9d2wsZGpaI485lt7028uuYe6Ys+bVH+cHOQm7zq+XeY0ekWK/XwrMdUfLyfUviN6Cm/V+BvOMG07SrmB+fF0I7+CcUzO0MYBAa9y5AGySnox3IK4EN4v78znLZstu45trGSHFcoIVnO6Md3mNL4DcSeWEeBtwY1zqgwhXPAutm53LPfgcZTg4rgd/lwS/TAbZE+Ta6z+HZ+ZFX4YEl8Lsi+sa6NHkkd0VJR1du4dlC+0Yz/DYE9kPG6fWRQe48VOwgm+vyukGZ8rsMzbPrIK+LTtFn7kYeAms2w69M+Y2M/no58Lvc9YtRUuB+FcnvIFRRbTWU/uHWON9c382Pfb1oqsRWCLccv4nAqjXnr0J6c3+a95oqfGyZC35Vye9ppNMvg9YbHVvoG3n5Fd72cvyeA1apOb8DKjU/XwvPldV3T4n+uVSMc7/PXW+HHAA2KVt+OW6voM2GHnF+PeTN1W8Oz5alF2Sy6wksjqrp9aEZvapsfmX9VE7g6/KDrIxjkSWZaDSn0BRytFFLg0HJPB9ElZ7y5yrlFp1rP+DaOB6IPIH2i+PV4/dSBfPIwsR+E8f5xfpNwC9pxuUWWDB+d6pKjig3yQQiLDDOrY/y0hyGJtGD47wVxKE2zG5xNEFn1eBuQztPv655rnD55bidGsfdkSv1Digk9Rq0g3JbzXNlhQDWtr3vop2eXnG8P0raeW0VbW8e+JUlv02QQnopMjg/BgyMa5kx6TZgo5rnticWCEX+NMNvQo7fXmghugNanN6Re24w8N34XFSIZy23ccjAcD8yLJ0R/eVoYHzuuR0qkN3eaKNmIE1Gzf5IGVu+mXe7fnzuXCC/LZCRdDhKbP8XtFh+i5wiizZHfpc7HkBuo6kkfj+Jz2vnrt8CnBWf88bLwURIasn8/prxQ4u9bmgjZ0VmX4QW3jdaeL9PI0P11cgINxylB7gKVQKuWn7PIJ3uxei7J6MQ41OAiQ0gvyei7b+OvEZ3R0avc2rkN6ho+WXtCXmBPIbG4fYo1+Raufua67vZ3Ne1JH7jUNXL7NpxyCC3L9qoubCGXxljy9zyG1iB/MYj70aL9vhVfaOMvlsrv5E113+MjNedmX1sHlRS3x2AcuueR6y/UPqM18jN/Wj8e7BM+dVw69HM9fNiTOlec74sveBL/JCefh9frVcVzq/MnxTa1nr8DXnLrAvg7v+HJsr3zWwgign3vPtambCmZJDXoSRoHeL8psg6Whk3V4Kxz4hwNXd/JC59amY7AOuZWQcvsCJbTZjYkAgTm54LBTgP2AYtoPPPHYJ2E3BVkZtWFMc5wVUa9UrghNzp9VFitlWBH3pUKfQYoeqJZsLsVor3OhYl3hvq7tujcKhtzaxvPHcgBcuvhts2wW0KCuc8Hg3iP0NK+Kpmtnk8V2gIYAv8hpjZKu4+kabqFmPRpLQHsKiZLRnPFS67OvArXH6BmcA5rhDKK1B+lSHxtz83lcHt6e5jg9uC8Vw7FP5bNGr5jUfjCcBN7n64u99KKD4WodHIg+/j+D+KCvGs5fY02pk/C3meveTuU9z9TGBBM9s2nnPKl92VSOHeyptCnF5DOXW6wGzhbU6EeXqUyC0Ik4GDXOHZNwWfD9FY95vg1B4toD8xs4VMidX7AGWEj+f5jUKGmq6568cAO5rZcu4+M9c3FkNJe8vmNynj56oO2wtYxN3/5u5uZlkoyqIU3zdq+d2EwjOmosXnvnF+BDKULGGqmNQF9d0q5Pd3lP/qVOBg4AFXiPF/oRCjgdEeF6Ea+U1GuvE+qJLYLsgI9yDwLkCEry5CwfKL9tQOee5cghZ2g5AR5PTg0lLf/Sy+45OS+F0qOrMKCwx3933d/XIUYryMqdrZkpQ0tswDv96UL7/hKJXGJshwczgt941S+m4z8sPMdsvdMgHYFuWOmhnX56O8vvsR2qw83N3fCt15GtJTLgo+7dAm3XtmtnyJY1+e29tm1suioErgXLTJtHrwzMLI2lOOXlDLb0VXyOZItNZ4eQ56VRn8ykOVVqyv2w8aDJ5FVuRV0cS4V9W8ajjuSc7qTc7KXTGvjVE44PooJGsM8KOSOTQbJkbTrsGZKGZ+ZeCAOFd4QvJWcs92529BbuKnIC+vgRXJLwvraMfsSeM6IrfibDelFA+uGm43Ze8O7UL+iqaQtrNQTrHSuDXDb1R8zpT9jeN42ZBd58TvS/y6ol27LBxmKHBm7vqm8W47oh2+k8vi1hp+ufvWR3nFCkt02wpuuxIJ3FFevWOQ23iXGKML3+lurexy5y6nQPf+VvLshhK7T0bhCFvE593j+mByXg0V8bsHLeJHoYTli8S141Dy2WsoMTS7FfwM+BHwX2guGUHMvRXym4w8lDcjPELj+hDgqgZ4v2+gIhvronxle8X1pUKuzRYOqUh+8+eu71fBuJzpTSdEOxuKjB59UGWkXeN6JX23BX43oHC77rn7tqqi7X0N+e2KNtMXQeFQe8T1SvrGV8hv0bj2OypIhZLjOBLN+5ehJOqjoz/8A3mbGdqwvrFibg8hb58f0zSvDUPerHcBVzeI7LZG3t6HoZQjlehVZf4kj6Q2wN3fRR4CqyOF7AZ3v6paVl/CsyhxdCf4UuLKKvEXtEt/Goptvc7d/1gmAXfPEhGeD6xoZoPiOPNKOge5IY5BoWSgBL6Vw7WT3BUZ4XYBPnD3kd7k3VUGh7z8epvZ4Ghf+Z2Jo1GM+hvxTCkeXDXcVjCzrV07OeehSXt/MzsBDfKPlcmtGX69QnZfoASKj8a1A4BPgM8Tvy/x+8Tdp3tTIsLBaMGSoSeauCcAb7j7SWVxaw2/2E07ASkcT7i8qErxEG2G2yDCMwB57DnKl/Q42kUrLOFoK/nNkp2rIEM74F9AVmCgErj7R8Dt7r4sCuf9HjIobW9mWc7Ex2H2xJol87vD3ZdDSXB/iHJJgBb5mwFvu/uvyubWAr/tUYhlb6RXPQH80+X9UyW/ZVE49HbARma2iKnQwJlIh6n6/S6D8r5sgRalq5nZdciIM8mVJL90tCC/Tcysu5mdjAzWj87pOwrglOm/a6BF6L3I6/xG1F+HVtl3W+C3GvL0XsPMekfbO4vQWxK/OfK7B1Vq+xPyAFq7yr7xFfJbJXT6boROVRGOQn3iLXcfCNyK5rYr4/ydaJx5Ckof+/LcNkUG6oHBD+TQsRXwrLvvWSKv5vhlslsHGbbao/VHJXpVmcg8MRLaCFP1m4bKrm6mqgkRJlblwNQiIgTlDZdLe5U89ke7UZvE8bJIUeyO3NnfqJJfczBV3FsGOMYrdolsRn7bICPSmyhH15sVc9vd3QfE8ZooAW1v4Iyc0aRKfnnZrYt2rDqi3eV35vT8t5lfuKU7Wkgd7O5/N7OeyKOhM3Cku7/dYPxWQDulyyFvkEIqAbaR2yHu/oqZrYxCQFcG3mvAd7uGqyLgRqiU/YcVcautSISZ3YUMr2ORQeTpCt9tc/zuRB4+76L2d4GrEmQj8Tsb5V/rToVjyxz4XYgWCuugea2R3u9dqLLhfWa2Cap8W1h6gLngdycKJ+uAjNfnVNj+jkO5cvqhsJIZwDbu/qmZ/ZAK+24L/KYjQ9y+KPn7kYlfm/jNALZz94+r7hst8JuOdKz3zGx7YExVBuDgt2R+7DVVaD3X3f9kZpshQ0glOn0z3EajqIy/opyKV7tSzVSCFmR3gbvfa2b9UQW8SnX6otGhagJfVzSaEQlmK0vbkEYkAHd/tWoOZtbO3S8zsy3N7EKUo+M24OgqJ8NW4FxvAA+zGvldhGK5nwEOd5VbbSRuhhJEnlslrwzN8JuOqp4c0Qg7Fo3OD/XVTijf2ppmdjHKGXKcy2O0atTyuwjlEDvJlVOsSuS5fdfMzgc+QEal5yplJtTK7nzgQzM7xCP3VVVoZpG8AjJcTgvPvDsqIRZogV8X5OHzF+QRXBla4Dc/an+7Vz2vtcCvKzKunlMNqybMof1leVQeroJXhhb4zYfk9yTaoa8S7ZA396Hu/rCZnYk8WM9w90r7bqCW39moSMMl7n5BtdSArx+/M5GX4xlV941ALb8zkBHkdHe/rVpqs3KwAmBmvZFtIBtbHqyKV/z9Wm6d0LjyOqqoWSlakF2WA+nJqniVieSRlPCtRLiUZm6mp7j7hRVT+lqhkeWX47Yq8gBpGG7Q2LKDrwW/9VFC5nFoN+rKiinNhkbm18jcoLH5mULslkZJtvuiCq6XV8uqCYnfvCHxmzc0Mj8zmy8MvllozhINsvEAJH7zisRv3hCcFkGhWKuhPLsjq2UlNDI3aHx+ZSB5JCV8W3Egivnd0r8pmfPLRSPLr5G5QeI3r3gDhdqdm/i1GY3MDRqYnytP3XSUJ2e/xK9tSPzmDYnf3CO3iM/SPjTMIh4Sv3lF4jdvcHePvjsWpfZopL7bsNyg8fmVgeSRlPCtRITwVB4m9nVFI8uvkblB4peQkJCQkJCQkJCQ8PVGMiQlJCQkJCQkJCQkJCQkJCQkJLQK7aomkJCQkJCQkJCQkJCQkJCQkJDw9UAyJCUkJCQkJCQkJCQkJCQkJCQktArJkJSQkJCQkJCQkJCQkJCQkJCQ0CokQ1JCQkJCQkJCQkJCQkJCQkJCQquQDEkJCQkJCQkJCXOAmY02s+5tuL+nmf21SE5z+NsfV/F3ExISEhISEr496FA1gYSEhISEhISERoa7b101h4SEhISEhISERkHySEpISEhISEj4VsPMjjKzQ+PzeWb25/j8fTO73sz+z8wWC0+jF8zscjObZGb3m9l8cW9/M3vWzJ4FDsp99+pmNsHMnjGziWa2YnzPi/HdL5jZLWbWNfc9D5vZk2Z2n5n1iPO9zezeOD/GzFaJ873MbLyZPWdmvy5ZdAkJCQkJCQnfQiRDUkJCQkJCQsK3HWOAAfH5e8ACZtYxzj1Sc++KwCXuvjowBfhxnL8aOMTd16y5/wDgAnfvF9/9RpxfGRju7qsCHwEHxt+8CNjR3fsDVwG/iftHxvf3B44Ehsf5C4BL3X0N4O25FUBCQkJCQkJCQmuRDEkJCQkJCQkJ33Y8CfQ3s27AdGA8MvoMQEamPF5192dyz/WM/End3T0zOl2Xu388cLyZHQMs7+7T4vxkdx8bn38PbIyMS32BP5nZM8CJwDJmtgCwIXBznL8M6BHPbgTc2MzfTUhISEhISEgoBClHUkJCQkJCQsK3Gu4+w8xeBfYAxgETgc2APsALNbdPz33+ApjvK777BjN7HNgGGG1m+wP/ALz2VsCASe6+Qf5CGLimhFdTs39mThwSEhISEhISEuqJ5JGUkJCQkJCQkCDPoyNRKNsYFJL2tLt/pZHG3acAU8xs4zi1W3bNzFYA/uHuFwK3A9+NS8uZWWYw2hV4FHgJWDw7b2YdzWx1d/8IeNXMdorzZmZZCN1YYJfav5uQkJCQkJCQUBSSISkhISEhISEhQcajHsB4d38X+JQvh7XNCXsCl0TomeXO7wz8Nc73Ba6N8y8BB5nZC8DCKM/RZ8COwBmRtPsZFNIGMhLtHecnAdvF+cPie54Dlm7LP5yQkJCQkJCQMDewVmy0JSQkJCQkJCQk1Alm1hO4y937VkwlISEhISEhIaHNSB5JCQkJCQkJCQkJCQkJCQkJCQmtQvJISkhISEhISEhISEhISEhISEhoFZJHUkJCQkJCQkJCQkJCQkJCQkJCq5AMSQkJCQkJCQkJCQkJCQkJCQkJrUIyJCUkJCQkJCQkJCQkJCQkJCQktArJkJSQkJCQkJCQkJCQkJCQkJCQ0CokQ1JCQkJCQkJCQkJCQkJCQkJCQquQDEkJCQkJCQkJCQkJCQkJCQkJCa3C/wM2byA6cxoOIwAAAABJRU5ErkJggg==
"
>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp_train</span><span class="o">=</span><span class="n">train</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">temp_train</span><span class="p">[</span><span class="s1">&#39;ideal&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">temp_train</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span> <span class="p">:</span><span class="mi">0</span> <span class="k">if</span> <span class="p">(</span><span class="n">x</span><span class="p">[</span><span class="s1">&#39;temp&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">27</span><span class="p">)</span> <span class="ow">and</span> <span class="p">(</span><span class="n">x</span><span class="p">[</span><span class="s1">&#39;windspeed&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">30</span><span class="p">)</span> <span class="k">else</span> <span class="mi">1</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">temp_train</span><span class="p">[</span><span class="n">temp_train</span><span class="p">[</span><span class="s1">&#39;ideal&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span>
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
      <th>datetime</th>
      <th>season</th>
      <th>holiday</th>
      <th>workingday</th>
      <th>weather</th>
      <th>temp</th>
      <th>atemp</th>
      <th>humidity</th>
      <th>windspeed</th>
      <th>casual</th>
      <th>registered</th>
      <th>count</th>
      <th>year</th>
      <th>month</th>
      <th>day</th>
      <th>dayofweek</th>
      <th>hour</th>
      <th>minute</th>
      <th>second</th>
      <th>ideal</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2011-01-01 00:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.84</td>
      <td>14.395</td>
      <td>81</td>
      <td>0.0000</td>
      <td>3</td>
      <td>13</td>
      <td>16</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011-01-01 01:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.02</td>
      <td>13.635</td>
      <td>80</td>
      <td>0.0000</td>
      <td>8</td>
      <td>32</td>
      <td>40</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2011-01-01 02:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.02</td>
      <td>13.635</td>
      <td>80</td>
      <td>0.0000</td>
      <td>5</td>
      <td>27</td>
      <td>32</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2011-01-01 03:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.84</td>
      <td>14.395</td>
      <td>75</td>
      <td>0.0000</td>
      <td>3</td>
      <td>10</td>
      <td>13</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2011-01-01 04:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.84</td>
      <td>14.395</td>
      <td>75</td>
      <td>0.0000</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>4</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
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
      <th>10881</th>
      <td>2012-12-19 19:00:00</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>15.58</td>
      <td>19.695</td>
      <td>50</td>
      <td>26.0027</td>
      <td>7</td>
      <td>329</td>
      <td>336</td>
      <td>2012</td>
      <td>12</td>
      <td>19</td>
      <td>2</td>
      <td>19</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10882</th>
      <td>2012-12-19 20:00:00</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>14.76</td>
      <td>17.425</td>
      <td>57</td>
      <td>15.0013</td>
      <td>10</td>
      <td>231</td>
      <td>241</td>
      <td>2012</td>
      <td>12</td>
      <td>19</td>
      <td>2</td>
      <td>20</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10883</th>
      <td>2012-12-19 21:00:00</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>13.94</td>
      <td>15.910</td>
      <td>61</td>
      <td>15.0013</td>
      <td>4</td>
      <td>164</td>
      <td>168</td>
      <td>2012</td>
      <td>12</td>
      <td>19</td>
      <td>2</td>
      <td>21</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10884</th>
      <td>2012-12-19 22:00:00</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>13.94</td>
      <td>17.425</td>
      <td>61</td>
      <td>6.0032</td>
      <td>12</td>
      <td>117</td>
      <td>129</td>
      <td>2012</td>
      <td>12</td>
      <td>19</td>
      <td>2</td>
      <td>22</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10885</th>
      <td>2012-12-19 23:00:00</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>13.12</td>
      <td>16.665</td>
      <td>66</td>
      <td>8.9981</td>
      <td>4</td>
      <td>84</td>
      <td>88</td>
      <td>2012</td>
      <td>12</td>
      <td>19</td>
      <td>2</td>
      <td>23</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>8315 rows × 20 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Outlier</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">prev_removing_train</span><span class="o">=</span><span class="n">train</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;count&#39;</span><span class="p">,</span><span class="s1">&#39;registered&#39;</span><span class="p">,</span><span class="s1">&#39;casual&#39;</span><span class="p">]:</span>
  <span class="n">train</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">abs</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="n">train</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&lt;=</span> <span class="mi">3</span><span class="o">*</span><span class="n">train</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">std</span><span class="p">()]</span>
<span class="nb">print</span><span class="p">(</span><span class="n">prev_removing_train</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">train</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(10886, 19)
(10282, 19)
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>datetime</th>
      <th>season</th>
      <th>holiday</th>
      <th>workingday</th>
      <th>weather</th>
      <th>temp</th>
      <th>atemp</th>
      <th>humidity</th>
      <th>windspeed</th>
      <th>casual</th>
      <th>registered</th>
      <th>count</th>
      <th>year</th>
      <th>month</th>
      <th>day</th>
      <th>dayofweek</th>
      <th>hour</th>
      <th>minute</th>
      <th>second</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2011-01-01 00:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.84</td>
      <td>14.395</td>
      <td>81</td>
      <td>0.0</td>
      <td>3</td>
      <td>13</td>
      <td>16</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011-01-01 01:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.02</td>
      <td>13.635</td>
      <td>80</td>
      <td>0.0</td>
      <td>8</td>
      <td>32</td>
      <td>40</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2011-01-01 02:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.02</td>
      <td>13.635</td>
      <td>80</td>
      <td>0.0</td>
      <td>5</td>
      <td>27</td>
      <td>32</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2011-01-01 03:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.84</td>
      <td>14.395</td>
      <td>75</td>
      <td>0.0</td>
      <td>3</td>
      <td>10</td>
      <td>13</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2011-01-01 04:00:00</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>9.84</td>
      <td>14.395</td>
      <td>75</td>
      <td>0.0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>2011</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>4</td>
      <td>0</td>
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
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="nb">print</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="n">train</span><span class="o">.</span><span class="n">holiday</span><span class="o">==</span><span class="mi">1</span><span class="p">][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
<span class="nb">print</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="n">train</span><span class="o">.</span><span class="n">workingday</span><span class="o">==</span><span class="mi">1</span><span class="p">][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
<span class="nb">print</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="n">train</span><span class="o">.</span><span class="n">holiday</span><span class="o">==</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
<span class="nb">print</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="n">train</span><span class="o">.</span><span class="n">workingday</span><span class="o">==</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>167.80612244897958
169.48831644144144
164.92781337605126
154.99968533668974
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_train</span><span class="o">=</span><span class="n">train</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;datetime&#39;</span><span class="p">,</span><span class="s1">&#39;windspeed&#39;</span><span class="p">,</span><span class="s1">&#39;month&#39;</span><span class="p">,</span><span class="s1">&#39;count&#39;</span><span class="p">,</span><span class="s1">&#39;registered&#39;</span><span class="p">,</span><span class="s1">&#39;casual&#39;</span><span class="p">,</span><span class="s1">&#39;day&#39;</span><span class="p">,</span><span class="s1">&#39;minute&#39;</span><span class="p">,</span><span class="s1">&#39;second&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">y_casual</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;casual&#39;</span><span class="p">]</span>
<span class="n">y_registered</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;registered&#39;</span><span class="p">]</span>
<span class="n">y_count</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;count&#39;</span><span class="p">]</span>
<span class="n">x_test</span><span class="o">=</span><span class="n">test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;datetime&#39;</span><span class="p">,</span><span class="s1">&#39;windspeed&#39;</span><span class="p">,</span><span class="s1">&#39;month&#39;</span><span class="p">,</span><span class="s1">&#39;day&#39;</span><span class="p">,</span><span class="s1">&#39;minute&#39;</span><span class="p">,</span><span class="s1">&#39;second&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_casual</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log1p</span><span class="p">(</span><span class="n">y_casual</span><span class="p">)</span>
<span class="n">y_registered</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log1p</span><span class="p">(</span><span class="n">y_registered</span><span class="p">)</span>
<span class="n">y_count</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log1p</span><span class="p">(</span><span class="n">y_count</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>XGBoost</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_casual</span><span class="o">=</span><span class="n">xgb</span><span class="o">.</span><span class="n">XGBRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">xgb_registered</span><span class="o">=</span><span class="n">xgb</span><span class="o">.</span><span class="n">XGBRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">xgb_count</span><span class="o">=</span><span class="n">xgb</span><span class="o">.</span><span class="n">XGBRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">xgb_casual</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_casual</span><span class="p">)</span>
<span class="n">xgb_registered</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_registered</span><span class="p">)</span>
<span class="n">xgb_count</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_count</span><span class="p">)</span>

<span class="n">xgb_pred_casual</span><span class="o">=</span><span class="n">xgb_casual</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">xgb_pred_registered</span><span class="o">=</span><span class="n">xgb_registered</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">xgb_pred_count</span><span class="o">=</span><span class="n">xgb_count</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">total_pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">xgb_pred_casual</span><span class="p">)</span><span class="o">+</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">xgb_pred_registered</span><span class="p">)</span>
<span class="n">xgb_score</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">msle</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">xgb_pred_count</span><span class="p">),</span><span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="n">y_count</span><span class="p">)))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot; xgb score : </span><span class="si">%0.5f</span><span class="s2">&quot;</span> <span class="o">%</span> <span class="n">xgb_score</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre> xgb score : 0.26521
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_test_casual</span><span class="o">=</span><span class="n">xgb_casual</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">xgb_test_registered</span><span class="o">=</span><span class="n">xgb_registered</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">xgb_test_count</span><span class="o">=</span><span class="n">xgb_count</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">xgb_submit</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">xgb_submit</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span>
<span class="c1">#xgb_submit[&#39;count&#39;]=np.exp(xgb_test_casual)+np.exp(xgb_test_registered)</span>
<span class="n">xgb_submit</span><span class="p">[</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">xgb_test_count</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>LightGBM</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;workingday&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;workingday&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;holiday&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;holiday&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;weather&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;weather&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;dayofweek&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;dayofweek&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_train</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>

<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;season&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;workingday&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;workingday&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;holiday&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;holiday&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;weather&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;weather&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;dayofweek&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;dayofweek&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>
<span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;category&#39;</span><span class="p">)</span>

<span class="n">x_train</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
Int64Index: 10282 entries, 0 to 10885
Data columns (total 10 columns):
 #   Column      Non-Null Count  Dtype   
---  ------      --------------  -----   
 0   season      10282 non-null  category
 1   holiday     10282 non-null  category
 2   workingday  10282 non-null  category
 3   weather     10282 non-null  category
 4   temp        10282 non-null  float64 
 5   atemp       10282 non-null  float64 
 6   humidity    10282 non-null  int64   
 7   year        10282 non-null  category
 8   dayofweek   10282 non-null  category
 9   hour        10282 non-null  category
dtypes: category(7), float64(2), int64(1)
memory usage: 393.4 KB
</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lgb_casual</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">LGBMRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">lgb_registered</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">LGBMRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">lgb_count</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">LGBMRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">lgb_casual</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_casual</span><span class="p">)</span>
<span class="n">lgb_registered</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_registered</span><span class="p">)</span>
<span class="n">lgb_count</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_count</span><span class="p">)</span>

<span class="n">lgb_pred_casual</span><span class="o">=</span><span class="n">lgb_casual</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">lgb_pred_registered</span><span class="o">=</span><span class="n">lgb_registered</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">lgb_pred_count</span><span class="o">=</span><span class="n">lgb_count</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">total_pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">lgb_pred_casual</span><span class="p">)</span><span class="o">+</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">lgb_pred_registered</span><span class="p">)</span>
<span class="n">lgb_score</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">msle</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">lgb_pred_count</span><span class="p">),</span><span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="n">y_count</span><span class="p">)))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot; lgb score : </span><span class="si">%0.5f</span><span class="s2">&quot;</span> <span class="o">%</span> <span class="n">lgb_score</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre> lgb score : 0.24864
</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lgb_test_casual</span><span class="o">=</span><span class="n">lgb_casual</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">lgb_test_registered</span><span class="o">=</span><span class="n">lgb_registered</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">lgb_test_count</span><span class="o">=</span><span class="n">lgb_count</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">lgb_submit</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">lgb_submit</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span>
<span class="c1">#lgb_submit[&#39;count&#39;]=np.exp(lgb_test_casual)+np.exp(lgb_test_registered)</span>
<span class="n">lgb_submit</span><span class="p">[</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">lgb_test_count</span><span class="p">)</span>
<span class="n">lgb_submit</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[15]:</div>



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
      <th>datetime</th>
      <th>count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2011-01-20 00:00:00</td>
      <td>9.741944</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011-01-20 01:00:00</td>
      <td>5.097146</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2011-01-20 02:00:00</td>
      <td>2.930270</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2011-01-20 03:00:00</td>
      <td>2.381208</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2011-01-20 04:00:00</td>
      <td>1.958094</td>
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
<p><strong>RandomForest</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">rf_casual</span><span class="o">=</span><span class="n">RandomForestRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
<span class="n">rf_registered</span><span class="o">=</span><span class="n">RandomForestRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
<span class="n">rf_count</span><span class="o">=</span><span class="n">RandomForestRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
<span class="n">rf_casual</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_casual</span><span class="p">)</span>
<span class="n">rf_registered</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_registered</span><span class="p">)</span>
<span class="n">rf_count</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_count</span><span class="p">)</span>

<span class="n">rf_pred_casual</span><span class="o">=</span><span class="n">rf_casual</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">rf_pred_registered</span><span class="o">=</span><span class="n">rf_registered</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">rf_pred_count</span><span class="o">=</span><span class="n">rf_count</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
<span class="n">total_pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">rf_pred_casual</span><span class="p">)</span><span class="o">+</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">rf_pred_registered</span><span class="p">)</span>
<span class="n">rf_score</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">msle</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">rf_pred_count</span><span class="p">),</span><span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="n">y_count</span><span class="p">)))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot; rf score : </span><span class="si">%0.5f</span><span class="s2">&quot;</span> <span class="o">%</span> <span class="n">rf_score</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre> rf score : 0.12228
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">rf_test_casual</span><span class="o">=</span><span class="n">rf_casual</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">rf_test_registered</span><span class="o">=</span><span class="n">rf_registered</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">rf_test_count</span><span class="o">=</span><span class="n">rf_count</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">rf_submit</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">rf_submit</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="s1">&#39;datetime&#39;</span><span class="p">]</span>
<span class="c1">#rf_submit[&#39;count&#39;]=np.exp(rf_test_casual)+np.exp(rf_test_registered)</span>
<span class="n">rf_submit</span><span class="p">[</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">expm1</span><span class="p">(</span><span class="n">rf_test_count</span><span class="p">)</span>

<span class="n">rf_submit</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[17]:</div>



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
      <th>datetime</th>
      <th>count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2011-01-20 00:00:00</td>
      <td>11.623826</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011-01-20 01:00:00</td>
      <td>4.145901</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2011-01-20 02:00:00</td>
      <td>2.872698</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2011-01-20 03:00:00</td>
      <td>3.498478</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2011-01-20 04:00:00</td>
      <td>2.743573</td>
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
<p><strong>submit</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s2">&quot;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Kaggle/Bike Sharing/submit/2020-06-12/xgb_score_</span><span class="si">%.5f</span><span class="s2">.csv&quot;</span> <span class="o">%</span> <span class="n">xgb_score</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">lgb_submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s2">&quot;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Kaggle/Bike Sharing/submit/2020-06-12/lgb_score_</span><span class="si">%.5f</span><span class="s2">.csv&quot;</span> <span class="o">%</span> <span class="n">lgb_score</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">rf_submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s2">&quot;/mnt/c/Users/gjsgu/Desktop/Data Mining/Project/Kaggle/Bike Sharing/submit/2020-06-12/rf_score_</span><span class="si">%.5f</span><span class="s2">.csv&quot;</span> <span class="o">%</span> <span class="n">rf_score</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># handling holiday</span>


<span class="k">for</span> <span class="n">frame</span> <span class="ow">in</span> <span class="p">[</span><span class="n">xgb_submit</span><span class="p">,</span><span class="n">lgb_submit</span><span class="p">,</span><span class="n">rf_submit</span><span class="p">]:</span>
  <span class="c1">#Christmas</span>
  <span class="n">frame</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">12</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">25</span><span class="p">),</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">frame</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">12</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">25</span><span class="p">)][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">*</span><span class="mf">0.5</span>

  <span class="c1">#Thanks Giving Day</span>
  <span class="n">frame</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">11</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">24</span><span class="p">),</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">frame</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">11</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">24</span><span class="p">)][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">*</span><span class="mf">0.5</span>
  <span class="n">frame</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">11</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">22</span><span class="p">),</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">frame</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">11</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">22</span><span class="p">)][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">*</span><span class="mf">0.5</span>

  <span class="c1">#Memorial Day</span>
  <span class="n">frame</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">5</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">30</span><span class="p">),</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">frame</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">5</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">30</span><span class="p">)][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">*</span><span class="mf">0.5</span>
  <span class="n">frame</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">5</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">28</span><span class="p">),</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">frame</span><span class="p">[(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">year</span><span class="o">==</span><span class="mi">2011</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">month</span><span class="o">==</span><span class="mi">5</span><span class="p">)</span><span class="o">&amp;</span> <span class="p">(</span><span class="n">frame</span><span class="o">.</span><span class="n">datetime</span><span class="o">.</span><span class="n">dt</span><span class="o">.</span><span class="n">day</span><span class="o">==</span><span class="mi">28</span><span class="p">)][</span><span class="s1">&#39;count&#39;</span><span class="p">]</span><span class="o">*</span><span class="mf">0.5</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">xgb_submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s2">&quot;/content/drive/My Drive/Kaggle/Bike Sharing Demand/submit after 22,May/holiday_xgb_score_</span><span class="si">%.5f</span><span class="s2">.csv&quot;</span> <span class="o">%</span> <span class="n">xgb_score</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">lgb_submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s2">&quot;/content/drive/My Drive/Kaggle/Bike Sharing Demand/submit after 22,May/holiday_lgb_score_</span><span class="si">%.5f</span><span class="s2">.csv&quot;</span> <span class="o">%</span> <span class="n">lgb_score</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">rf_submit</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s2">&quot;/content/drive/My Drive/Kaggle/Bike Sharing Demand/submit after 22,May/holiday_rf_score_</span><span class="si">%.5f</span><span class="s2">.csv&quot;</span> <span class="o">%</span> <span class="n">rf_score</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="mi">154</span><span class="o">/</span><span class="mi">3242</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.047501542257865514</pre>
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
