---
layout: post
title: Space Calamity - Preprocessing_2
date: 2020-06-13
description: Space Calamity - Preprocessing_2
thumbnail: work1.jpg
categories: DataMining

# Information for the author block
author : Loui
---


<html>
<head><meta charset="utf-8" />

<title>Space Calamity - Preprocessing_2</title>

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
<h1 id="&#44032;&#51109;-&#51096;&#45208;&#50728;-&#49483;-&#48516;&#49437;">&#44032;&#51109; &#51096;&#45208;&#50728; &#49483; &#48516;&#49437;<a class="anchor-link" href="#&#44032;&#51109;-&#51096;&#45208;&#50728;-&#49483;-&#48516;&#49437;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">top</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/submit/submit_9999_no_year.csv&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">top</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">top</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
      <td>3.564384</td>
      <td>3.580822</td>
      <td>3.391781</td>
      <td>3.493151</td>
      <td>3.257534</td>
      <td>3.178082</td>
      <td>3.082192</td>
      <td>3.509589</td>
    </tr>
    <tr>
      <th>std</th>
      <td>105.510663</td>
      <td>0.706596</td>
      <td>0.708787</td>
      <td>0.827042</td>
      <td>0.863218</td>
      <td>0.867280</td>
      <td>0.879286</td>
      <td>0.755082</td>
      <td>0.657201</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
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
      <td>5.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">middle</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/submit/submit_no_nan.csv&#39;</span><span class="p">)</span>
<span class="n">middle</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">middle</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">test</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test2/9999_weighted&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">train</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_no_nan/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
  <span class="n">train</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="EDA">EDA<a class="anchor-link" href="#EDA">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#라벨부터 보자규</span>
<span class="n">vari</span><span class="o">=</span><span class="s1">&#39;Tp&#39;</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">test</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">vari</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#log 취해보기</span>
<span class="n">cur</span><span class="o">=</span><span class="n">test</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="c1">#cur[vari]=np.log(test[0][vari])</span>
<span class="n">cur</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">test</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">])</span>

<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">],</span><span class="n">cur</span><span class="p">[</span><span class="n">vari</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7feeb3ae1898&gt;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">8</span><span class="p">))</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">data</span> <span class="o">=</span> <span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">corr</span><span class="p">(</span><span class="n">method</span><span class="o">=</span><span class="s1">&#39;pearson&#39;</span><span class="p">),</span> <span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">fmt</span> <span class="o">=</span> <span class="s1">&#39;.3f&#39;</span><span class="p">,</span> <span class="n">linewidths</span><span class="o">=.</span><span class="mi">1</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;Reds&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7feed027a748&gt;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">columns</span> <span class="o">=</span>  <span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span>
<span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;</span><span class="si">{}</span><span class="s1"> : </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">column</span><span class="p">,</span><span class="nb">round</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">column</span><span class="p">]</span><span class="o">.</span><span class="n">var</span><span class="p">()),</span><span class="mi">2</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>year : 19
doy : 11119
Np : 17
Vp : 10894
Tp : 5096303652
B_gsm_x : 11
B_gsm_y : 13
B_gsm_z : 8
Bt : 11
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">col_list</span> <span class="o">=</span> <span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">columns</span>
<span class="n">col_list</span><span class="o">=</span><span class="n">col_list</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;year&#39;</span><span class="p">])</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">col_list</span><span class="p">:</span>
  <span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">+=</span><span class="mi">100</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>카이제곱 검정/라벨과 검정시 독립이라면 필요없음</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.feature_selection</span> <span class="kn">import</span> <span class="n">chi2</span>
<span class="kn">from</span> <span class="nn">sklearn.feature_selection</span> <span class="kn">import</span> <span class="n">SelectKBest</span>
<span class="n">col_list</span> <span class="o">=</span> <span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">columns</span>
<span class="n">col_list</span><span class="o">=</span><span class="n">col_list</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;label&#39;</span><span class="p">)</span>
<span class="n">X</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">][[</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">]],</span> <span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span>
<span class="nb">print</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">train_new</span> <span class="o">=</span> <span class="n">SelectKBest</span><span class="p">(</span><span class="n">chi2</span><span class="p">,</span> <span class="n">k</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span><span class="o">.</span><span class="n">fit_transform</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">train_new</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">train_new</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(5478, 10)
(5478, 2)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>506.90234567901217</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#라벨부터 보자규</span>
<span class="n">vari</span><span class="o">=</span><span class="s1">&#39;doy&#39;</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">vari</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#log 취해보기</span>
<span class="n">cur</span><span class="o">=</span><span class="n">train</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="c1">#cur[vari]=np.log(train[0][vari])</span>

<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">cur</span><span class="p">[</span><span class="n">vari</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7feeb5205320&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
oTcrsc1b9zA5a4vu5OEo/ZZ/a+RCb1ZiRdmoZPlyoTcrsaJsVLJ8udCblVhVt/xbI6+jNysxb1Qy
cKE3Kz1vVDK3bszMSs6F3sys5FzozcxKzoXezKzkXOjNzErOhd7MrORc6M0y0Nfb/EcrLW6WpXl9
10n6maRdknZKGktiiyU9KOmZ5PXJxydVs+6xad3vtxU3y9LxuLx4f0Ssjojh5PY1wEMRcSbwUHLb
rGPShvB2ejhvsznwZnnI4u/IS4Hbk7dvB0Yy+BpmqaLNeBau/85uZk0H5nDU42adNt9CH8A/SNoh
aX0SOzUipo+e/wVwarMPlLRe0piksYMHD84zDbNiKcqh3GYw/1k3/yYiapJ+B3hQ0tMz3xkRIanp
hVRE3ALcAjA8PNzJiy0zs0qZ1xV9RNSS1y8BfwecD7wo6TSA5PVL803SrNssSlldkxY3y9Lb/q6T
9E5JJ02/Dfw74AngPuCq5G5XAd+eb5Jm3WbhCT1txc2yNJ/WzanA36l+0PAJwP+NiL+X9CPgW5I+
Bfwc+I/zT9Osu7wy0bwXnxY3y9LbLvQR8Rzw3ibxfwY+MJ+kzLrdkv4+ak3OZfURfpYHNwzNMuAj
/KxIXOjNMjAyNMhl5w3SU29t0iNx2Xk+6cny4UJvloHR8Rrf/NE+pqK+cngqgm/+aB+j47WcM7Mq
cqE3y8D139nN5FTj9pDJqfDOWMuFC71ZBrwz1orEhd7MrORc6M3MSs6F3sys5OY71MzMCm50vMbm
rXt44dAES/r72LB2pZd5VowLvVmJjY7X2HDPT46sAKodmmDDPT8BcLGvELduzErMyzwNXOjNSs3L
PA1c6M3MSs+F3iwD/X29bcXLnofly4XeLAPXXXIOvQvUEOtdIK675JyO5zErDRaIjudh+fKqG7MM
TK9oKcKyxh6JwxENt61afEVvpZNWxqpY3jZv3cPk4Vmrbg4Hm7fuySkjy4Ov6K10os14FkbHa2zc
souJySmgvn5945ZdQGfXr7/Q5JSrY8WtnDK7opf0IUl7JO2VdE1WX8esiDZv3XOkyE+bmJzq+JV0
2tGFPtKwWjIp9JJ6gP8FfBg4G7hS0tlZfC2zIirKlbSPNDTI7or+fGBvRDwXEW8AdwOXZvS1zAqn
KFfSI0ODbFq3isH+PgQM9vexad0qjz+omKx69IPAvhm39wMXzLyDpPXAeoDTTz89ozTM8rFh7cqG
Hj3kdyU9MuSzaqsut1U3EXFLRAxHxPDAwEBeadhxlPbN1OlvsiLk4StpK5KsruhrwLIZt5cmsePm
1JMW8uKrbzSNd0oRcgBYs2Ixjzz7ctN4J33p8tV87ps7m8armIevpK0osrrI+RFwpqQzJC0ErgDu
O55fYPsXLj6qoJ560kK2f+Hi4/llCp8DwJ2fft9RRX3NisXc+en3dTSPkaFBvnL56oar2K9cvrrj
xa4oeZgVhSKyWV0s6SPAV4Ae4GsRcWPafYeHh2NsbCyTPMzMykrSjogYnut+mW2YiogHgAey+vxm
ZtYaj0AwMys5F3ozs5JzoTczKzkXejOzksts1U1bSUgHgZ/P41OcAvzTcUqn2/mxaOTH4y1+LBqV
4fF4T0TMueO0EIV+viSNtbLEqAr8WDTy4/EWPxaNqvR4uHVjZlZyLvRmZiVXlkJ/S94JFIgfi0Z+
PN7ix6JRZR6PUvTozcwsXVmu6M3MLEVXF3qfS/sWScskPSzpSUm7JX0275zyJqlH0rik7+adS94k
9Uu6R9LTkp6S1NnRpgUi6b8lPyNPSLpL0jvyzilrXVvofS7tUd4EPh8RZwMXAldX/PEA+CzwVN5J
FMRfAX8fEWcB76Wij4ukQeC/AsMR8XvUp+tekW9W2evaQo/PpW0QEQci4sfJ269S/0Gu7AB2SUuB
fw/8Td655E3Su4F/C9wGEBFvRMShfLPK1QlAn6QTgEXACznnk7luLvTNzqWtbGGbSdJyYAjYnm8m
ufoK8D+Aw3knUgBnAAeBv01aWX8j6Z15J5WHiKgBXwSeBw4Ar0TEP+SbVfa6udBbE5LeBdwLfC4i
fpV3PnmQ9FHgpYjYkXcuBXECcC5wc0QMAb8BKvmclqSTqf/lfwawBHinpI/nm1X2urnQZ34ubbeR
1Eu9yN8ZEVvyzidHa4BLJP2MekvvIknfyDelXO0H9kfE9F9491Av/FX0QeCnEXEwIiaBLcC/zjmn
zHVzoc/8XNpuIknUe7BPRcSX8s4nTxGxMSKWRsRy6t8X2yKi9FdtaSLiF8A+SSuT0AeAJ3NMKU/P
AxdKWpT8zHyACjwxndlRglmLiDclfQbYylvn0u7OOa08rQE+AeyStDOJ/XlypKPZfwHuTC6KngP+
OOd8chER2yXdA/yY+kq1cSqwQ9Y7Y83MSq6bWzdmZtYCF3ozs5JzoTczKzkXejOzknOhNzMrORd6
M7OSc6E3Mys5F3ozs5L7/6JYc5ABkVXWAAAAAElFTkSuQmCC
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">train</span><span class="p">[</span><span class="mi">1</span><span class="p">][(</span><span class="n">train</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">900</span><span class="p">)][</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([4, 6, 7]), array([1, 1, 2]))</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">original</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">15</span><span class="p">)]</span>
<span class="n">original</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/frame_train/ace_1999.csv&#39;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">10</span><span class="p">):</span>
  <span class="n">original</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/frame_train/ace_200&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span>
  
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">14</span><span class="p">):</span>
  <span class="n">original</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/frame_train/ace_20&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span>
  
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">original</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">10</span><span class="p">)</span>
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
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>7.149</td>
      <td>92352.0</td>
      <td>406.00</td>
      <td>-2.174</td>
      <td>-2.598</td>
      <td>5.550</td>
      <td>6.630</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>5.998</td>
      <td>85859.0</td>
      <td>419.12</td>
      <td>-1.245</td>
      <td>-0.140</td>
      <td>6.558</td>
      <td>6.796</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>6.211</td>
      <td>81547.0</td>
      <td>411.99</td>
      <td>-2.003</td>
      <td>-1.198</td>
      <td>6.306</td>
      <td>6.802</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>6.680</td>
      <td>72308.0</td>
      <td>405.25</td>
      <td>-3.093</td>
      <td>-2.483</td>
      <td>5.545</td>
      <td>6.854</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>4.0</td>
      <td>-9999.900</td>
      <td>-9999.9</td>
      <td>-9999.90</td>
      <td>-3.009</td>
      <td>-1.500</td>
      <td>5.908</td>
      <td>6.842</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>5.0</td>
      <td>6.410</td>
      <td>69888.0</td>
      <td>408.27</td>
      <td>-2.297</td>
      <td>-0.685</td>
      <td>6.339</td>
      <td>6.842</td>
    </tr>
    <tr>
      <th>6</th>
      <td>6</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>7.0</td>
      <td>6.149</td>
      <td>74253.0</td>
      <td>409.85</td>
      <td>-2.132</td>
      <td>0.345</td>
      <td>6.415</td>
      <td>6.831</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>8.0</td>
      <td>6.422</td>
      <td>73144.0</td>
      <td>407.99</td>
      <td>-2.416</td>
      <td>0.694</td>
      <td>6.021</td>
      <td>6.969</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>9.0</td>
      <td>6.216</td>
      <td>88505.0</td>
      <td>412.83</td>
      <td>-2.245</td>
      <td>3.919</td>
      <td>5.365</td>
      <td>7.032</td>
    </tr>
    <tr>
      <th>9</th>
      <td>9</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>10.0</td>
      <td>5.587</td>
      <td>86869.0</td>
      <td>413.50</td>
      <td>-2.461</td>
      <td>3.513</td>
      <td>5.546</td>
      <td>7.028</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 대충 보기위해 -9999다 날림</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;=-</span><span class="mi">9998</span><span class="p">]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 하루 기준으로 합치기 기준은 mean</span>
<span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">,</span> <span class="s1">&#39;label&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[37]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="o">.</span><span class="n">line</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;label&#39;</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">&#39;Np&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/pandas/plotting/_core.py:1001: UserWarning: Attempting to set identical left==right results
in singular transformations; automatically expanding.
left=1.0, right=1.0
  ax.set_xlim(left, right)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[37]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f0fb95c4c50&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYYAAAEKCAYAAAAW8vJGAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4zLCBo
dHRwOi8vbWF0cGxvdGxpYi5vcmcvnQurowAAEi9JREFUeJzt3X2QXXV9x/H3FzcmIwbNw5qmRNxQ
gSl0EGEblaIDihpoKWqZVKvlQTopY5iWDtahZaZSHTriEzNUawaBAZWioqiUQYWilUEF3FAewpMk
MdZFJJtgRWqpPHz7xzlr7m+Tzd7de/ee3eX9mtm5J+ece84nZ+7dzz0Pe25kJpIkjdqr6QCSpJnF
YpAkFSwGSVLBYpAkFSwGSVLBYpAkFSwGSVLBYpAkFSwGSVKhr9crXLp0aQ4MDPR6tZI0q23YsGF7
Zvb3Yl09L4aBgQGGhoZ6vVpJmtUi4se9WpeHkiRJBYtBklSwGCRJhZ6fY5Ck6fLUU08xPDzMk08+
2XSUKVuwYAErVqxg3rx5jWWwGCTNGcPDwyxcuJCBgQEiouk4k5aZ7Nixg+HhYVauXNlYDg8lSZoz
nnzySZYsWTIrSwEgIliyZEnjezwWg6Q5ZbaWwqiZkN9ikIB3XXIb77rktqZjSDOCxSABt2zazi2b
tjcdQ3NARHD22Wf/5t8f/ehHOe+885oLNAUWgyR10fz587nmmmvYvn32ftCwGCSpi/r6+li7di0X
XnjhLtNOPfVUzjjjDAYHBznwwAO57rrrGkg4MS9XlTQn/eO/3ct9P328q8s8+Lf34f0nHDLhfOvW
rePQQw/lfe973y7Ttm7dyu23387mzZs55phj2LRpEwsWLOhqzk65xyBJXbbPPvtw8sknc9FFF+0y
bc2aNey1114ccMAB7L///jzwwAMNJNwz9xgkzUntfLKfTmeddRaHH344p512WjF+7OWoM+Hy1LHc
Y5CkabB48WLWrFnDpZdeWoy/+uqrefbZZ9m8eTNbtmzhoIMOaijh+CwGSZomZ5999i5XJ+23336s
WrWK4447jvXr18+48wvgoSRJ6qonnnjiN8PLli3jV7/6VTH92GOPZf369b2ONSnuMUiSCu4xSFKP
XH755U1HaIt7DJLmlMxsOkJHZkJ+i0HSnLFgwQJ27NgxI365TsXo9zE0fULaQ0mS5owVK1YwPDzM
yMhI01GmbPQb3JpkMUiaM+bNm9foN5/NFR5KkiQVLAZJUsFikCQVLAZJUsFikCQVLAZJUsFikCQV
LAZJUsFikCQVLAZJUsFikCQV2iqGiHhpRHw7Iu6LiHsj4q/r8Ysj4saIeKh+XDS9cSVJ063dPYan
gbMz82Dg1cC6iDgYOAe4KTMPAG6q/y1JmsXaKobMfCQz76iHfwncD+wLnAhcUc92BfCW6QgpSeqd
SZ9jiIgB4JXAbcCyzHyknvQzYNk4z1kbEUMRMTSb75MuSc8FkyqGiHgh8GXgrMx8vHVaVl+ZtNuv
TcrMizNzMDMH+/v7pxxWkjT92i6GiJhHVQpXZuY19ehHI2J5PX05sK37ESVJvdTuVUkBXArcn5kf
b5l0LXBKPXwK8LXuxpMk9Vq7X+35B8CfA/dExJ31uL8HPgR8MSJOB34MrOl+RElSL7VVDJl5CxDj
TH5D9+JIkprmXz5LkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFI
kgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoW
gySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySpYDFIkgoWgySp0FYxRMRlEbEt
Ija2jDsvIh6OiDvrn+OnL6YkqVfa3WO4HFi9m/EXZuZh9c/13YslSWpKW8WQmTcDj01zFknSDNDp
OYYzI+Lu+lDTovFmioi1ETEUEUMjIyMdrlKSNJ06KYZPAb8DHAY8AnxsvBkz8+LMHMzMwf7+/g5W
KUmablMuhsx8NDOfycxngU8Dq7oXS5LUlCkXQ0Qsb/nnW4GN480rSZo9+tqZKSKuAo4GlkbEMPB+
4OiIOAxIYCvwl9OUUZLUQ20VQ2a+YzejL+1yFknSDOBfPkuSChaDJKlgMUiSChaDJKlgMUiSChaD
JKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlg
MUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiS
ChaDJKlgMUiSChaDJKnQVjFExGURsS0iNraMWxwRN0bEQ/XjoumLKUnqlXb3GC4HVo8Zdw5wU2Ye
ANxU/1uSNMu1VQyZeTPw2JjRJwJX1MNXAG/pYi5JUkM6OcewLDMfqYd/Biwbb8aIWBsRQxExNDIy
0sEqJUnTrSsnnzMzgdzD9IszczAzB/v7+7uxSknSNOmkGB6NiOUA9eO27kSSJDWpk2K4FjilHj4F
+FrncSRJTWv3ctWrgO8DB0XEcEScDnwIeGNEPAQcW/9bkjTL9bUzU2a+Y5xJb+hiFknSDOBfPkuS
ChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaD
JKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlgMUiSChaDJKlg
MUiSCn1NB5BmgletXNx0BGnGcI9BklSwGCRJBYtBklSwGCRJBYtBklSwGCRJhY4vV42IrcAvgWeA
pzNzsNNlSpKa062/YzgmM7d3aVmSpAZ5KEmSVOhGMSRwQ0RsiIi1u5shItZGxFBEDI2MjHRhlZKk
6dKNYjgqMw8HjgPWRcTrxs6QmRdn5mBmDvb393dhlZKk6dJxMWTmw/XjNuArwKpOlylJak5HxRAR
e0fEwtFh4E3Axm4EkyQ1o9OrkpYBX4mI0WX9a2Z+o+NUkqTGdFQMmbkFeEWXskiSZgAvV5UkFSwG
SVLBYpAkFSwGSVLBYpAkFbp1Ez1pVrvtR481HUGaMdxjkCQVLAZJUsFikCQVLAZJUsFikCQVLAZJ
UsFikCQVLAZJUsFikCQVLAZJUsFikCQVLAZJUsFikCQVLAZJUsFikCQVLAZJUsFikCQVLAZJUsFi
kCQVLAZJUsFikCQVLAZJUsFikCQVLAZJUsFikCQVLAZJUsFikCQVLAZJUqHjYoiI1RHxYERsiohz
uhFK6rWjXr6Uo16+tOkY0ozQ18mTI+J5wCeBNwLDwA8i4trMvK8b4aRe+dxfvKrpCNKM0ekewypg
U2ZuycxfA58HTuw8liSpKZ0Ww77AT1r+PVyPK0TE2ogYioihkZGRDlcpSZpOPTn5nJkXZ+ZgZg72
9/f3YpWSpCnqtBgeBl7a8u8V9ThJ0izVaTH8ADggIlZGxPOBtwPXdh5LktSUjq5KysynI+JM4JvA
84DLMvPeriSTJDWio2IAyMzrgeu7kEWSNAP4l8+SpEJkZm9XGPFL4MGernRqlgLbmw4xgdmQEczZ
bebsrtmS86DMXNiLFXV8KGkKHszMwQbWOykRMTTTc86GjGDObjNnd82mnL1al4eSJEkFi0GSVGii
GC5uYJ1TMRtyzoaMYM5uM2d3mXOMnp98liTNbB5KkiSVMnPCH2A11SWmm4BzdjP9ZcBNwN3AfwAr
WqZdAGysf/60ZfzrgTvq8VcAffX4AC6q13U3cHjLc04BHqp/Tmk45zvr5dwDfA94Rctzttbj7wSG
Gsx4NPCLOsedwD9MIkcvc/5tS8aNwDPA4om2ZT39MmAbsHGc1+6kX0/AEfU6N9XPHd2zXgzcWM9/
I7BoonU0lPMjwAP1cr4CvLgePwD8b8u2Xt9gxvOo7qs2muX4luf8XT3/g8CbG96WX2jJuBW4s51t
OY05z6e6o/UTY5Y1v866CbgNGGh3e+4224QzVLe62AzsDzwfuAs4eMw8V4+Gp3rzf7Ye/kOqN1Af
sDfVvZX2odpT+QlwYD3fB4DT6+Hjga/XG+3VwG0tb8ot9eOienhRgzmPZOcvhuNGc7b8Mls6A7bl
0cB1k83R65xjlnsC8K2JtmXL9NcBhzP+m2/Sryfg9nreqJ97XD3+w9QlCZwDXLCndTSY803sLN0L
WnIOjLf+BjKeB7x3N+s4uH69zQdWUr0On9dUzjHL/Rj1h6uJtuU05nw1sJxdi+E91OVEdc+6L7S7
PXf3086hpHa+jOdg4Fv18Ldbph8M3JyZT2fm/1C14mpgCfDrzPxhPd+NwJ/UwycCn8nKrcCLI2I5
8Gbgxsx8LDN/Xj9ndVM5M/N7dQ6AW6nuLDuRXm/LqeZoMuc7gKsmyP8bmXkz8NgeZpnU66metk9m
3prVO+szwFtalnVFPXzFmPG7W0cjOTPzhsx8ul5uu6/NXm/LPa3j85n5f5n5I6pPuquazhkRAayh
wddmvcxbM/ORcZY1+tr8EvCGOvOE23N32imGdr6M5y7gbfXwW4GFEbGkHr86Il4QEUuBY6hu070d
6IuI0T8qOYmdt+8eb30T5eh1zlanUzX/qARuiIgNEbG24YyviYi7IuLrEXFImzka2ZYR8QKqN8CX
W0aPty3bNdnX07718NjxAMta3pQ/A5ZNsI6mcrZ6N+Vrc2VE/GdEfCciXttwxjMj4u6IuCwiFk2w
jiZzArwWeDQzH2oZ18m2nErOtpZVfyj4BdWHsSltz2795fN7gU9ExKnAzVTHDp/JzBsi4vepjsGP
AN+vx2dEvB24MCLmAzdQHVeebl3PGRHHUBXDUS2jj8rMhyPiJcCNEfFA/emh1xnvAF6WmU9ExPHA
V4ED2szRy5yjTgC+m5mtn7I62ZbTpv7/ZNM59iQizgWeBq6sRz0C7JeZOyLiCOCrEXFIZj7eQLxP
AR+kKv4PUh2meXcDOdo1dk92Jm3Lrmtnj2HCL+PJzJ9m5tsy85XAufW4/64fz8/MwzLzjVTH0n5Y
j/9+Zr42M1dR/WIZPcQw3vomytHrnETEocAlwImZuaNlPQ/Xj9uoTv6N7rr1NGNmPp6ZT9TD1wPz
6k/xM25b1t7OmF31PWzLdk329fQw5aGX1v/7o6OHiOrHbROso6mc1IX9R8A768Mj1IcTdtTDG6iO
Nx/YRMbMfDQzn8nMZ4FPM4n3SC9zAkREH9Xe8RdGx3VhW04lZ1vLqvO+CNgxxWW1dfK5j+rkx0p2
nog8ZMw8S4G96uHzgQ/kzpOYS+rhQ6muOBk9KfaS+nE+1dUtr8+dJy9bT8jcnjtPyPyI6mTMonp4
cYM596M6XnfkmHXsDSxsGf4esLqhjL/FzqsrVgH/VW/XPebodc563Iuojsfu3c62HJNlgPFP8E36
9cSuJyKPr8d/hPLk84f3tI4Gc64G7gP6x6yjn/rEI9WFBQ/T8h7qccblLcv9G6rj4ACHUJ4s3cJu
Tpb2KmfL9vzOZLfldORsee7Yk8/rKE8+f3Ey23OXbBPNUC/8eKpPd5uBc+txHwD+uB4+ieqyqh9S
fYKeX49fUL9A76M6CXZYyzI/AtxPdQnVWS3jA/hkva57gMGWae+m+mW8CTit4ZyXAD9n5+VqQy0v
krvqn3tHczSU8cw6w131c47cU46mctbTTqX+5dAybo/bsp7nKqrd+qeojp+eDpwBnDHV1xMwSFVo
m4FPsLNcl1AV2kPAv7Pzl8q462go5yaq48rFpZRUJ/vvrcfdAZzQYMbP1su4m+pbH1uL4tx6/gfZ
/dVBPctZT7t8dNkt4/a4Lacx54frZT1bP57X8r67up7/dmD/drfn7n78y2dJUsG/fJYkFSwGSVLB
YpAkFSwGSVLBYpAkFSwGzWkR8cQE0wciYuMkl3l5RJzUWTJp5rIYJEkFi0HPCRHxwoi4KSLuiIh7
IqL1brF9EXFlRNwfEV+qb+ZHRBxR3yBtQ0R8c+wdU6W5ymLQc8WTwFsz83CqO75+rL4tMcBBwL9k
5u8CjwPviYh5wD8DJ2XmEVRfunJ+A7mlnuvW3VWlmS6Af4qI11HdTmBfdt42+yeZ+d16+HPAXwHf
AH6P6o6uUN0Danf3wZfmHItBzxXvpLrx2RGZ+VREbKW6vwxUt35ulVRFcm9mvqZ3EaWZwUNJeq54
EbCtLoVjqL6zetR+ETFaAH8G3EJ1w7H+0fERMa/li46kOc1i0HPFlcBgRNwDnAw80DLtQWBdRNxP
dZvjT2X1laYnARdExF1Ud9E8sseZpUZ4d1VJUsE9BklSwWKQJBUsBklSwWKQJBUsBklSwWKQJBUs
BklSwWKQJBX+H4HUQcIa9s6IAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[39]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#라벨부터 보자규</span>
<span class="n">vari</span><span class="o">=</span><span class="s1">&#39;Np&#39;</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">cur</span><span class="o">=</span><span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">vari</span><span class="p">)</span>
<span class="c1">#log 취해보기</span>
<span class="c1">#cur[vari]=np.log(test[0][vari])</span>
<span class="c1">#cur[&#39;Np&#39;]=np.log(test[0][&#39;Np&#39;])</span>

<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">y</span><span class="o">=</span><span class="n">cur</span><span class="p">[</span><span class="n">vari</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[39]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f0fb95baa90&gt;</pre>
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
<div class="prompt input_prompt">In&nbsp;[69]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="p">[</span><span class="mi">6</span><span class="p">][(</span><span class="n">merged</span><span class="p">[</span><span class="mi">6</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">)]</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[69]:</div>



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
      <th>count</th>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.0</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2008.230088</td>
      <td>187.884956</td>
      <td>4.361892</td>
      <td>52245.382328</td>
      <td>396.195095</td>
      <td>-0.008350</td>
      <td>-0.060837</td>
      <td>0.433063</td>
      <td>3.825225</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>std</th>
      <td>2.256876</td>
      <td>128.901358</td>
      <td>2.717596</td>
      <td>31566.341368</td>
      <td>52.309087</td>
      <td>2.349875</td>
      <td>2.251207</td>
      <td>1.552074</td>
      <td>1.407169</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1999.000000</td>
      <td>1.000000</td>
      <td>0.424110</td>
      <td>7705.434969</td>
      <td>315.806062</td>
      <td>-6.907354</td>
      <td>-8.557089</td>
      <td>-4.518759</td>
      <td>1.501331</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2007.000000</td>
      <td>54.250000</td>
      <td>2.806954</td>
      <td>29655.371914</td>
      <td>360.173322</td>
      <td>-1.956650</td>
      <td>-1.490752</td>
      <td>-0.409828</td>
      <td>2.785554</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2008.000000</td>
      <td>209.500000</td>
      <td>3.724208</td>
      <td>42925.499369</td>
      <td>392.039086</td>
      <td>-0.122150</td>
      <td>-0.097627</td>
      <td>0.500103</td>
      <td>3.643781</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2010.000000</td>
      <td>317.750000</td>
      <td>5.294048</td>
      <td>66449.324074</td>
      <td>415.419513</td>
      <td>1.755479</td>
      <td>1.576850</td>
      <td>1.385270</td>
      <td>4.618133</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2013.000000</td>
      <td>363.000000</td>
      <td>27.252827</td>
      <td>184817.816092</td>
      <td>664.119938</td>
      <td>7.039082</td>
      <td>5.539258</td>
      <td>5.395784</td>
      <td>9.134000</td>
      <td>0.0</td>
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
<div class="prompt input_prompt">In&nbsp;[91]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="p">[</span><span class="mi">4</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="mi">4</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">8</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[91]:</div>



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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Np_mean</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Tp_mean</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Vp_mean</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Bx_mean</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">By_mean</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Bz_mean</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Bt_mean</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
    <span class="n">Np_mean</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">label</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> <span class="k">for</span> <span class="n">label</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
    <span class="n">Tp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">label</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> <span class="k">for</span> <span class="n">label</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
    <span class="n">Vp_mean</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">label</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> <span class="k">for</span> <span class="n">label</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
    <span class="n">Bx_mean</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">label</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> <span class="k">for</span> <span class="n">label</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
    <span class="n">By_mean</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">label</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> <span class="k">for</span> <span class="n">label</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
    <span class="n">Bz_mean</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">label</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> <span class="k">for</span> <span class="n">label</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
    <span class="n">Bt_mean</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">label</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> <span class="k">for</span> <span class="n">label</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
    
    
    
<span class="n">Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">Np_mean</span><span class="p">)</span>
<span class="n">Tp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">Tp_mean</span><span class="p">)</span>
<span class="n">Vp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">Vp_mean</span><span class="p">)</span>
<span class="n">Bx</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">Bx_mean</span><span class="p">)</span>
<span class="n">By</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">By_mean</span><span class="p">)</span>
<span class="n">Bz</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">Bz_mean</span><span class="p">)</span>
<span class="n">Bt</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">Bt_mean</span><span class="p">)</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">10</span><span class="p">):</span>
  <span class="n">Np</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="n">Np</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Tp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="n">Tp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Vp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="n">Vp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bx</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="n">Bx</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">By</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">By</span><span class="p">[</span><span class="n">By</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bz</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">Bz</span><span class="p">[</span><span class="n">Bz</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">Bt</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">Bt</span><span class="p">[</span><span class="n">Bt</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">False</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[120]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Bz</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[120]:</div>



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
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
      <th>6</th>
      <th>7</th>
      <th>8</th>
      <th>9</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.069856</td>
      <td>0.778952</td>
      <td>0.443451</td>
      <td>-0.368124</td>
      <td>-1.109517</td>
      <td>-3.035642</td>
      <td>-5.142558</td>
      <td>-3.026831</td>
      <td>4.323374</td>
      <td>-42.690957</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.111847</td>
      <td>0.799285</td>
      <td>0.329001</td>
      <td>-0.356807</td>
      <td>-0.935169</td>
      <td>-1.857241</td>
      <td>-3.476728</td>
      <td>-6.631132</td>
      <td>-20.217079</td>
      <td>-31.846141</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1.157240</td>
      <td>0.786337</td>
      <td>0.324723</td>
      <td>-0.307652</td>
      <td>-1.023648</td>
      <td>-2.291930</td>
      <td>-5.268418</td>
      <td>-3.881140</td>
      <td>-14.896745</td>
      <td>-15.420942</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.975019</td>
      <td>0.771696</td>
      <td>0.311705</td>
      <td>-0.131831</td>
      <td>-1.217405</td>
      <td>-2.149459</td>
      <td>-3.280143</td>
      <td>-6.066274</td>
      <td>-5.751746</td>
      <td>-17.001981</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.973834</td>
      <td>0.743570</td>
      <td>0.428617</td>
      <td>-0.034090</td>
      <td>-0.748605</td>
      <td>-2.460048</td>
      <td>-3.761991</td>
      <td>-7.163063</td>
      <td>-1.076051</td>
      <td>-15.353650</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.653433</td>
      <td>0.447430</td>
      <td>0.458239</td>
      <td>-0.041519</td>
      <td>-1.023140</td>
      <td>-2.823228</td>
      <td>-4.595074</td>
      <td>-4.279988</td>
      <td>-19.229984</td>
      <td>-2.406558</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0.433063</td>
      <td>0.621420</td>
      <td>0.385874</td>
      <td>-0.208408</td>
      <td>-0.818336</td>
      <td>-2.645028</td>
      <td>-4.334537</td>
      <td>-15.047739</td>
      <td>-6.192664</td>
      <td>-20.640122</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0.918140</td>
      <td>0.660973</td>
      <td>0.410903</td>
      <td>-0.389511</td>
      <td>-1.405145</td>
      <td>-2.465788</td>
      <td>-2.816038</td>
      <td>-6.196434</td>
      <td>-10.992370</td>
      <td>-6.969363</td>
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
<div class="prompt input_prompt">In&nbsp;[128]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">Bx</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>-0.011535297249565044
0.09072879970109894
0.08358592435886487
-0.003236129142525402
-0.3073147169421354
-0.5015342395377074
-0.2562539842738285
0.2592715918155077
1.8886062024575463
-1.7220077394308637
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[125]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">]:</span>
    <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
    
    <span class="k">if</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Np&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Np</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Np</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Tp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Tp</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Vp</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Vp</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
    <span class="k">elif</span> <span class="n">col</span> <span class="o">==</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">:</span>
      <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
        <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span><span class="o">&amp;</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&lt;=</span><span class="n">Bx</span><span class="p">[</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>    
      <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">col</span><span class="p">]</span><span class="o">&gt;</span><span class="n">Bx</span><span class="p">[</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()),</span><span class="nb">str</span><span class="p">(</span><span class="n">col</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_range&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">9</span>
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

    <div class="prompt output_prompt">Out[125]:</div>



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
      <th>Np</th>
      <th>Tp</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
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
      <td>1999.0</td>
      <td>1.0</td>
      <td>6.637235</td>
      <td>86877.080247</td>
      <td>406.902346</td>
      <td>-3.314080</td>
      <td>-0.275105</td>
      <td>4.545235</td>
      <td>6.919617</td>
      <td>0</td>
      <td>4</td>
      <td>2</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1999.0</td>
      <td>2.0</td>
      <td>6.342774</td>
      <td>77740.109756</td>
      <td>412.214024</td>
      <td>-0.239470</td>
      <td>3.134634</td>
      <td>2.821256</td>
      <td>5.819366</td>
      <td>1</td>
      <td>4</td>
      <td>2</td>
      <td>1</td>
      <td>7</td>
      <td>9</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1999.0</td>
      <td>3.0</td>
      <td>5.491739</td>
      <td>48466.732919</td>
      <td>371.531988</td>
      <td>-2.328727</td>
      <td>2.885615</td>
      <td>-0.673273</td>
      <td>5.032745</td>
      <td>2</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>9</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1999.0</td>
      <td>4.0</td>
      <td>9.321573</td>
      <td>21668.737805</td>
      <td>358.070549</td>
      <td>-0.205140</td>
      <td>7.432841</td>
      <td>-1.374963</td>
      <td>7.673750</td>
      <td>1</td>
      <td>6</td>
      <td>0</td>
      <td>0</td>
      <td>7</td>
      <td>9</td>
      <td>5</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1999.0</td>
      <td>5.0</td>
      <td>5.148043</td>
      <td>50250.957055</td>
      <td>329.185767</td>
      <td>-3.360411</td>
      <td>0.614294</td>
      <td>-7.282914</td>
      <td>8.205785</td>
      <td>3</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>5</td>
      <td>8</td>
      <td>4</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;B_gsm_y_range&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[127]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([0, 9, 5, 7, 8, 4, 6, 3, 1])</pre>
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
