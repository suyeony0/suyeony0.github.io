---
layout: post
title: Space Calamity - Preprocessing_1
date: 2020-06-13
description: Space Calamity - Preprocessing_1
thumbnail: person1.jpeg
categories: DataMining

# Information for the author block
author : Loui
---

<html>
<head><meta charset="utf-8" />

<title>Space Calamity - Preprocessing_1</title>

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
<h1 id="checking-test-set-format">checking test set format<a class="anchor-link" href="#checking-test-set-format">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/test/test.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">test</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Preprocessing-1-&#54616;&#47336;&#47196;-&#47564;&#46308;&#44592;">Preprocessing 1 &#54616;&#47336;&#47196; &#47564;&#46308;&#44592;<a class="anchor-link" href="#Preprocessing-1-&#54616;&#47336;&#47196;-&#47564;&#46308;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>B류 평소 : 교란 =&gt; -5 ~ 5 : -30~+30</p>
<hr>
<p>Vp : 300~400 : 500이상</p>
<hr>
<p>Np : 10대 : 수십대</p>
<hr>
<p>Tp : 10^4~5 제곱 : 10^6제곱 이상 (칼빈온도)</p>
<hr>
<p>라벨 : 3이하 : 5이상</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_middle/ace_18h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df1</span><span class="o">=</span><span class="n">ace0</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">df1</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#각 데이터프레임에 라벨이름 재설정 해줘야함</span>
<span class="n">df1</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_18h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df1</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>

<span class="c1">#remove outlier for every columns</span>
<span class="c1"># &#39;Bt&#39; have to be changed to all columns</span>
<span class="n">df2</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">df2</span><span class="o">=</span><span class="n">df1</span><span class="p">[</span><span class="n">df1</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9000</span><span class="p">]</span>
<span class="n">df2</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9000</span><span class="p">]</span>
<span class="n">df2</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9000</span><span class="p">]</span>
<span class="n">df2</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9000</span><span class="p">]</span>
<span class="n">df2</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9000</span><span class="p">]</span>
<span class="n">df2</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9000</span><span class="p">]</span>
<span class="n">df2</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">9000</span><span class="p">]</span>
<span class="n">df2</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>

<span class="c1">#aggregate all columns using mean based on year and doy</span>
<span class="n">df3</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>

<span class="c1">#doy를 categorical_feature를 위해 int로 형변환</span>

<span class="c1">#pd.to_numeric(df3[&#39;doy&#39;],errors=&#39;corece&#39;)</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df3</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;int&#39;</span><span class="p">)</span>

<span class="c1">#year 삭제</span>
<span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>6.786193</td>
      <td>92031.124224</td>
      <td>415.767640</td>
      <td>-1.300820</td>
      <td>3.243174</td>
      <td>1.587342</td>
      <td>5.524373</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>5.416263</td>
      <td>55342.681250</td>
      <td>392.025500</td>
      <td>-1.680063</td>
      <td>3.012363</td>
      <td>1.857756</td>
      <td>5.193706</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>5.863227</td>
      <td>31828.478528</td>
      <td>336.980920</td>
      <td>-2.090411</td>
      <td>2.994663</td>
      <td>1.024534</td>
      <td>4.786687</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>5.347939</td>
      <td>14382.795420</td>
      <td>328.038473</td>
      <td>-0.051763</td>
      <td>8.586718</td>
      <td>-3.811710</td>
      <td>9.455557</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>9.628747</td>
      <td>71225.895062</td>
      <td>330.459815</td>
      <td>0.087247</td>
      <td>-4.287531</td>
      <td>0.752198</td>
      <td>6.476105</td>
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
<h1 id="&#45796;&#47480;-preprocessing-&#47784;&#45944;-&#54616;&#45208;&#47196;-&#47564;&#46308;&#44592;&#50948;&#54616;&#50668;-&#47784;&#46304;-&#44163;-&#45796;-&#54633;&#54616;&#44592;">&#45796;&#47480; preprocessing &#47784;&#45944; &#54616;&#45208;&#47196; &#47564;&#46308;&#44592;&#50948;&#54616;&#50668; &#47784;&#46304; &#44163; &#45796; &#54633;&#54616;&#44592;<a class="anchor-link" href="#&#45796;&#47480;-preprocessing-&#47784;&#45944;-&#54616;&#45208;&#47196;-&#47564;&#46308;&#44592;&#50948;&#54616;&#50668;-&#47784;&#46304;-&#44163;-&#45796;-&#54633;&#54616;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#ace0=pd.read_csv(&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_0h.csv&#39;,engine=&#39;python&#39;)</span>
<span class="n">ace3</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_3h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">ace6</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_6h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">ace9</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_9h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>

<span class="n">ace12</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_12h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">ace15</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_15h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">ace18</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_18h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">ace21</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_21h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df1</span><span class="o">=</span><span class="n">ace0</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">df1</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#각 데이터프레임에 라벨이름 재설정 해줘야함</span>
<span class="n">df1</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_0h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">df1</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">#remove outlier for every columns</span>
<span class="sd"># &#39;Bt&#39; have to be changed to all columns</span>
<span class="sd">df2=pd.DataFrame()</span>
<span class="sd">df2=df1[df1[&#39;Np&#39;]&gt;-9000]</span>
<span class="sd">df2=df2[df2[&#39;Tp&#39;]&gt;-9000]</span>
<span class="sd">df2=df2[df2[&#39;Vp&#39;]&gt;-9000]</span>
<span class="sd">df2=df2[df2[&#39;B_gsm_x&#39;]&gt;-9000]</span>
<span class="sd">df2=df2[df2[&#39;B_gsm_y&#39;]&gt;-9000]</span>
<span class="sd">df2=df2[df2[&#39;B_gsm_z&#39;]&gt;-9000]</span>
<span class="sd">df2=df2[df2[&#39;Bt&#39;]&gt;-9000]</span>
<span class="sd">print(df2.shape)</span>
<span class="sd">&#39;&#39;&#39;</span>


<span class="c1">#aggregate all columns using mean based on year and doy</span>
<span class="n">df3</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df3</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>

<span class="c1">#doy를 categorical_feature를 위해 int로 형변환</span>

<span class="n">df3</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df3</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="s1">&#39;int&#39;</span><span class="p">)</span>

<span class="c1">#year 삭제</span>
<span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(928729, 12)
(582227, 12)
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
      <td>1</td>
      <td>6.637235</td>
      <td>86877.080247</td>
      <td>406.902346</td>
      <td>-3.314080</td>
      <td>-0.275105</td>
      <td>4.545235</td>
      <td>6.919617</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>6.342774</td>
      <td>77740.109756</td>
      <td>412.214024</td>
      <td>-0.239470</td>
      <td>3.134634</td>
      <td>2.821256</td>
      <td>5.819366</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>5.491739</td>
      <td>48466.732919</td>
      <td>371.531988</td>
      <td>-2.328727</td>
      <td>2.885615</td>
      <td>-0.673273</td>
      <td>5.032745</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>9.321573</td>
      <td>21668.737805</td>
      <td>358.070549</td>
      <td>-0.205140</td>
      <td>7.432841</td>
      <td>-1.374963</td>
      <td>7.673750</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>5.148043</td>
      <td>50250.957055</td>
      <td>329.185767</td>
      <td>-3.360411</td>
      <td>0.614294</td>
      <td>-7.282914</td>
      <td>8.205785</td>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#ace0은 맨처음테스트로 처리함</span>
<span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merged_by_after/ace_0h.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="c1">#df=[ace3.copy(),ace6.copy(),ace9.copy(),ace12.copy(),ace15.copy(),ace18.copy(),ace21.copy()]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ace0</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Unnamed: 0    False
year          False
doy           False
hr            False
min           False
Np            False
Tp            False
Vp            False
B_gsm_x       False
B_gsm_y       False
B_gsm_z       False
Bt            False
kp_0h         False
dtype: bool</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="-9999&#47484;-&#54644;&#45817;-&#51068;&#51088;&#51032;-mean&#44050;&#51004;&#47196;-&#45824;&#52404;&#54616;&#44592;"><strong>-9999&#47484; &#54644;&#45817; &#51068;&#51088;&#51032; mean&#44050;&#51004;&#47196; &#45824;&#52404;&#54616;&#44592;</strong><a class="anchor-link" href="#-9999&#47484;-&#54644;&#45817;-&#51068;&#51088;&#51032;-mean&#44050;&#51004;&#47196;-&#45824;&#52404;&#54616;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">k</span><span class="o">=</span><span class="mi">1</span>
<span class="k">for</span> <span class="n">ace0</span> <span class="ow">in</span> <span class="n">df</span><span class="p">:</span>
  <span class="n">df_Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df_Vp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df_Tp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>

      <span class="n">mean_np</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
      <span class="n">Np</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)]</span>
      <span class="n">Np</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_np</span>
      <span class="n">df_Np</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_Np</span><span class="p">,</span><span class="n">Np</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

      <span class="k">if</span> <span class="n">j</span><span class="o">%</span><span class="k">100</span>==0:
        <span class="nb">print</span><span class="p">(</span><span class="n">j</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Np &quot;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>

  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_Np</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
      <span class="n">mean_vp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
      <span class="n">Vp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)]</span>
      <span class="n">Vp</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_vp</span>
      <span class="n">df_Vp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_Vp</span><span class="p">,</span><span class="n">Vp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

      <span class="k">if</span> <span class="n">j</span><span class="o">%</span><span class="k">100</span>==0:
        <span class="nb">print</span><span class="p">(</span><span class="n">j</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Vp &quot;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>    

  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_Vp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>


  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
      <span class="n">mean_tp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
      <span class="n">Tp</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)]</span>
      <span class="n">Tp</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_tp</span>
      <span class="n">df_Tp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_Tp</span><span class="p">,</span><span class="n">Tp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

      <span class="k">if</span> <span class="n">j</span><span class="o">%</span><span class="k">100</span>==0:
        <span class="nb">print</span><span class="p">(</span><span class="n">j</span><span class="p">)</span>

    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Tp&quot;</span> <span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>



  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_Tp</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">save</span><span class="p">[</span><span class="n">k</span><span class="p">]</span><span class="o">=</span><span class="n">ace0</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
  <span class="n">k</span><span class="o">+=</span><span class="mi">1</span>
  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">-</span><span class="mi">1</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39; 번째 df 끝&#39;</span><span class="p">)</span>
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
<pre>100.0
200.0
300.0
Np 1999.0 done
100.0
200.0
300.0
Np 2000.0 done
100.0
200.0
300.0
Np 2001.0 done
100.0
200.0
300.0
Np 2002.0 done
100.0
200.0
300.0
Np 2003.0 done
100.0
200.0
300.0
Np 2004.0 done
100.0
200.0
300.0
Np 2005.0 done
100.0
200.0
300.0
Np 2006.0 done
100.0
200.0
300.0
Np 2007.0 done
100.0
200.0
300.0
Np 2008.0 done
100.0
200.0
300.0
Np 2009.0 done
100.0
200.0
300.0
Np 2010.0 done
100.0
200.0
300.0
Np 2011.0 done
100.0
200.0
300.0
Np 2012.0 done
100.0
200.0
300.0
Np 2013.0 done
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:27: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>100.0
200.0
300.0
Vp 1999.0 done
100.0
200.0
300.0
Vp 2000.0 done
100.0
200.0
300.0
Vp 2001.0 done
100.0
200.0
300.0
Vp 2002.0 done
100.0
200.0
300.0
Vp 2003.0 done
100.0
200.0
300.0
Vp 2004.0 done
100.0
200.0
300.0
Vp 2005.0 done
100.0
200.0
300.0
Vp 2006.0 done
100.0
200.0
300.0
Vp 2007.0 done
100.0
200.0
300.0
Vp 2008.0 done
100.0
200.0
300.0
Vp 2009.0 done
100.0
200.0
300.0
Vp 2010.0 done
100.0
200.0
300.0
Vp 2011.0 done
100.0
200.0
300.0
Vp 2012.0 done
100.0
200.0
300.0
Vp 2013.0 done
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
<pre>100.0
200.0
300.0
Tp1999.0 done
100.0
200.0
300.0
Tp2000.0 done
100.0
200.0
300.0
Tp2001.0 done
100.0
200.0
300.0
Tp2002.0 done
100.0
200.0
300.0
Tp2003.0 done
100.0
200.0
300.0
Tp2004.0 done
100.0
200.0
300.0
Tp2005.0 done
100.0
200.0
300.0
Tp2006.0 done
100.0
200.0
300.0
Tp2007.0 done
100.0
200.0
300.0
Tp2008.0 done
100.0
200.0
300.0
Tp2009.0 done
100.0
200.0
300.0
Tp2010.0 done
100.0
200.0
300.0
Tp2011.0 done
100.0
200.0
300.0
Tp2012.0 done
100.0
200.0
300.0
Tp2013.0 done
2012.0 번째 df 끝
100.0
200.0
300.0
Np 1999.0 done
100.0
200.0
300.0
Np 2000.0 done
100.0
200.0
300.0
Np 2001.0 done
100.0
200.0
300.0
Np 2002.0 done
100.0
200.0
300.0
Np 2003.0 done
100.0
200.0
300.0
Np 2004.0 done
100.0
200.0
300.0
Np 2005.0 done
100.0
200.0
300.0
Np 2006.0 done
100.0
200.0
300.0
Np 2007.0 done
100.0
200.0
300.0
Np 2008.0 done
100.0
200.0
300.0
Np 2009.0 done
100.0
200.0
300.0
Np 2010.0 done
100.0
200.0
300.0
Np 2011.0 done
100.0
200.0
300.0
Np 2012.0 done
100.0
200.0
300.0
Np 2013.0 done
100.0
200.0
300.0
Vp 1999.0 done
100.0
200.0
300.0
Vp 2000.0 done
100.0
200.0
300.0
Vp 2001.0 done
100.0
200.0
300.0
Vp 2002.0 done
100.0
200.0
300.0
Vp 2003.0 done
100.0
200.0
300.0
Vp 2004.0 done
100.0
200.0
300.0
Vp 2005.0 done
100.0
200.0
300.0
Vp 2006.0 done
100.0
200.0
300.0
Vp 2007.0 done
100.0
200.0
300.0
Vp 2008.0 done
100.0
200.0
300.0
Vp 2009.0 done
100.0
200.0
300.0
Vp 2010.0 done
100.0
200.0
300.0
Vp 2011.0 done
100.0
200.0
300.0
Vp 2012.0 done
100.0
200.0
300.0
Vp 2013.0 done
100.0
200.0
300.0
Tp1999.0 done
100.0
200.0
300.0
Tp2000.0 done
100.0
200.0
300.0
Tp2001.0 done
100.0
200.0
300.0
Tp2002.0 done
100.0
200.0
300.0
Tp2003.0 done
100.0
200.0
300.0
Tp2004.0 done
100.0
200.0
300.0
Tp2005.0 done
100.0
200.0
300.0
Tp2006.0 done
100.0
200.0
300.0
Tp2007.0 done
100.0
200.0
300.0
Tp2008.0 done
100.0
200.0
300.0
Tp2009.0 done
100.0
200.0
300.0
Tp2010.0 done
100.0
200.0
300.0
Tp2011.0 done
100.0
200.0
300.0
Tp2012.0 done
100.0
200.0
300.0
Tp2013.0 done
2012.0 번째 df 끝
100.0
200.0
300.0
Np 1999.0 done
100.0
200.0
300.0
Np 2000.0 done
100.0
200.0
300.0
Np 2001.0 done
100.0
200.0
300.0
Np 2002.0 done
100.0
200.0
300.0
Np 2003.0 done
100.0
200.0
300.0
Np 2004.0 done
100.0
200.0
300.0
Np 2005.0 done
100.0
200.0
300.0
Np 2006.0 done
100.0
200.0
300.0
Np 2007.0 done
100.0
200.0
300.0
Np 2008.0 done
100.0
200.0
300.0
Np 2009.0 done
100.0
200.0
300.0
Np 2010.0 done
100.0
200.0
300.0
Np 2011.0 done
100.0
200.0
300.0
Np 2012.0 done
100.0
200.0
300.0
Np 2013.0 done
100.0
200.0
300.0
Vp 1999.0 done
100.0
200.0
300.0
Vp 2000.0 done
100.0
200.0
300.0
Vp 2001.0 done
100.0
200.0
300.0
Vp 2002.0 done
100.0
200.0
300.0
Vp 2003.0 done
100.0
200.0
300.0
Vp 2004.0 done
100.0
200.0
300.0
Vp 2005.0 done
100.0
200.0
300.0
Vp 2006.0 done
100.0
200.0
300.0
Vp 2007.0 done
100.0
200.0
300.0
Vp 2008.0 done
100.0
200.0
300.0
Vp 2009.0 done
100.0
200.0
300.0
Vp 2010.0 done
100.0
200.0
300.0
Vp 2011.0 done
100.0
200.0
300.0
Vp 2012.0 done
100.0
200.0
300.0
Vp 2013.0 done
100.0
200.0
300.0
Tp1999.0 done
100.0
200.0
300.0
Tp2000.0 done
100.0
200.0
300.0
Tp2001.0 done
100.0
200.0
300.0
Tp2002.0 done
100.0
200.0
300.0
Tp2003.0 done
100.0
200.0
300.0
Tp2004.0 done
100.0
200.0
300.0
Tp2005.0 done
100.0
200.0
300.0
Tp2006.0 done
100.0
200.0
300.0
Tp2007.0 done
100.0
200.0
300.0
Tp2008.0 done
100.0
200.0
300.0
Tp2009.0 done
100.0
200.0
300.0
Tp2010.0 done
100.0
200.0
300.0
Tp2011.0 done
100.0
200.0
300.0
Tp2012.0 done
100.0
200.0
300.0
Tp2013.0 done
2012.0 번째 df 끝
100.0
200.0
300.0
Np 1999.0 done
100.0
200.0
300.0
Np 2000.0 done
100.0
200.0
300.0
Np 2001.0 done
100.0
200.0
300.0
Np 2002.0 done
100.0
200.0
300.0
Np 2003.0 done
100.0
200.0
300.0
Np 2004.0 done
100.0
200.0
300.0
Np 2005.0 done
100.0
200.0
300.0
Np 2006.0 done
100.0
200.0
300.0
Np 2007.0 done
100.0
200.0
300.0
Np 2008.0 done
100.0
200.0
300.0
Np 2009.0 done
100.0
200.0
300.0
Np 2010.0 done
100.0
200.0
300.0
Np 2011.0 done
100.0
200.0
300.0
Np 2012.0 done
100.0
200.0
300.0
Np 2013.0 done
100.0
200.0
300.0
Vp 1999.0 done
100.0
200.0
300.0
Vp 2000.0 done
100.0
200.0
300.0
Vp 2001.0 done
100.0
200.0
300.0
Vp 2002.0 done
100.0
200.0
300.0
Vp 2003.0 done
100.0
200.0
300.0
Vp 2004.0 done
100.0
200.0
300.0
Vp 2005.0 done
100.0
200.0
300.0
Vp 2006.0 done
100.0
200.0
300.0
Vp 2007.0 done
100.0
200.0
300.0
Vp 2008.0 done
100.0
200.0
300.0
Vp 2009.0 done
100.0
200.0
300.0
Vp 2010.0 done
100.0
200.0
300.0
Vp 2011.0 done
100.0
200.0
300.0
Vp 2012.0 done
100.0
200.0
300.0
Vp 2013.0 done
100.0
200.0
300.0
Tp1999.0 done
100.0
200.0
300.0
Tp2000.0 done
100.0
200.0
300.0
Tp2001.0 done
100.0
200.0
300.0
Tp2002.0 done
100.0
200.0
300.0
Tp2003.0 done
100.0
200.0
300.0
Tp2004.0 done
100.0
200.0
300.0
Tp2005.0 done
100.0
200.0
300.0
Tp2006.0 done
100.0
200.0
300.0
Tp2007.0 done
100.0
200.0
300.0
Tp2008.0 done
100.0
200.0
300.0
Tp2009.0 done
100.0
200.0
300.0
Tp2010.0 done
100.0
200.0
300.0
Tp2011.0 done
100.0
200.0
300.0
Tp2012.0 done
100.0
200.0
300.0
Tp2013.0 done
2012.0 번째 df 끝
100.0
200.0
300.0
Np 1999.0 done
100.0
200.0
300.0
Np 2000.0 done
100.0
200.0
300.0
Np 2001.0 done
100.0
200.0
300.0
Np 2002.0 done
100.0
200.0
300.0
Np 2003.0 done
100.0
200.0
300.0
Np 2004.0 done
100.0
200.0
300.0
Np 2005.0 done
100.0
200.0
300.0
Np 2006.0 done
100.0
200.0
300.0
Np 2007.0 done
100.0
200.0
300.0
Np 2008.0 done
100.0
200.0
300.0
Np 2009.0 done
100.0
200.0
300.0
Np 2010.0 done
100.0
200.0
300.0
Np 2011.0 done
100.0
200.0
300.0
Np 2012.0 done
100.0
200.0
300.0
Np 2013.0 done
100.0
200.0
300.0
Vp 1999.0 done
100.0
200.0
300.0
Vp 2000.0 done
100.0
200.0
300.0
Vp 2001.0 done
100.0
200.0
300.0
Vp 2002.0 done
100.0
200.0
300.0
Vp 2003.0 done
100.0
200.0
300.0
Vp 2004.0 done
100.0
200.0
300.0
Vp 2005.0 done
100.0
200.0
300.0
Vp 2006.0 done
100.0
200.0
300.0
Vp 2007.0 done
100.0
200.0
300.0
Vp 2008.0 done
100.0
200.0
300.0
Vp 2009.0 done
100.0
200.0
300.0
Vp 2010.0 done
100.0
200.0
300.0
Vp 2011.0 done
100.0
200.0
300.0
Vp 2012.0 done
100.0
200.0
300.0
Vp 2013.0 done
100.0
200.0
300.0
Tp1999.0 done
100.0
200.0
300.0
Tp2000.0 done
100.0
200.0
300.0
Tp2001.0 done
100.0
200.0
300.0
Tp2002.0 done
100.0
200.0
300.0
Tp2003.0 done
100.0
200.0
300.0
Tp2004.0 done
100.0
200.0
300.0
Tp2005.0 done
100.0
200.0
300.0
Tp2006.0 done
100.0
200.0
300.0
Tp2007.0 done
100.0
200.0
300.0
Tp2008.0 done
100.0
200.0
300.0
Tp2009.0 done
100.0
200.0
300.0
Tp2010.0 done
100.0
200.0
300.0
Tp2011.0 done
100.0
200.0
300.0
Tp2012.0 done
100.0
200.0
300.0
Tp2013.0 done
2012.0 번째 df 끝
100.0
200.0
300.0
Np 1999.0 done
100.0
200.0
300.0
Np 2000.0 done
100.0
200.0
300.0
Np 2001.0 done
100.0
200.0
300.0
Np 2002.0 done
100.0
200.0
300.0
Np 2003.0 done
100.0
200.0
300.0
Np 2004.0 done
100.0
200.0
300.0
Np 2005.0 done
100.0
200.0
300.0
Np 2006.0 done
100.0
200.0
300.0
Np 2007.0 done
100.0
200.0
300.0
Np 2008.0 done
100.0
200.0
300.0
Np 2009.0 done
100.0
200.0
300.0
Np 2010.0 done
100.0
200.0
300.0
Np 2011.0 done
100.0
200.0
300.0
Np 2012.0 done
100.0
200.0
300.0
Np 2013.0 done
100.0
200.0
300.0
Vp 1999.0 done
100.0
200.0
300.0
Vp 2000.0 done
100.0
200.0
300.0
Vp 2001.0 done
100.0
200.0
300.0
Vp 2002.0 done
100.0
200.0
300.0
Vp 2003.0 done
100.0
200.0
300.0
Vp 2004.0 done
100.0
200.0
300.0
Vp 2005.0 done
100.0
200.0
300.0
Vp 2006.0 done
100.0
200.0
300.0
Vp 2007.0 done
100.0
200.0
300.0
Vp 2008.0 done
100.0
200.0
300.0
Vp 2009.0 done
100.0
200.0
300.0
Vp 2010.0 done
100.0
200.0
300.0
Vp 2011.0 done
100.0
200.0
300.0
Vp 2012.0 done
100.0
200.0
300.0
Vp 2013.0 done
100.0
200.0
300.0
Tp1999.0 done
100.0
200.0
300.0
Tp2000.0 done
100.0
200.0
300.0
Tp2001.0 done
100.0
200.0
300.0
Tp2002.0 done
100.0
200.0
300.0
Tp2003.0 done
100.0
200.0
300.0
Tp2004.0 done
100.0
200.0
300.0
Tp2005.0 done
100.0
200.0
300.0
Tp2006.0 done
100.0
200.0
300.0
Tp2007.0 done
100.0
200.0
300.0
Tp2008.0 done
100.0
200.0
300.0
Tp2009.0 done
100.0
200.0
300.0
Tp2010.0 done
100.0
200.0
300.0
Tp2011.0 done
100.0
200.0
300.0
Tp2012.0 done
100.0
200.0
300.0
Tp2013.0 done
2012.0 번째 df 끝
100.0
200.0
300.0
Np 1999.0 done
100.0
200.0
300.0
Np 2000.0 done
100.0
200.0
300.0
Np 2001.0 done
100.0
200.0
300.0
Np 2002.0 done
100.0
200.0
300.0
Np 2003.0 done
100.0
200.0
300.0
Np 2004.0 done
100.0
200.0
300.0
Np 2005.0 done
100.0
200.0
300.0
Np 2006.0 done
100.0
200.0
300.0
Np 2007.0 done
100.0
200.0
300.0
Np 2008.0 done
100.0
200.0
300.0
Np 2009.0 done
100.0
200.0
300.0
Np 2010.0 done
100.0
200.0
300.0
Np 2011.0 done
100.0
200.0
300.0
Np 2012.0 done
100.0
200.0
300.0
Np 2013.0 done
100.0
200.0
300.0
Vp 1999.0 done
100.0
200.0
300.0
Vp 2000.0 done
100.0
200.0
300.0
Vp 2001.0 done
100.0
200.0
300.0
Vp 2002.0 done
100.0
200.0
300.0
Vp 2003.0 done
100.0
200.0
300.0
Vp 2004.0 done
100.0
200.0
300.0
Vp 2005.0 done
100.0
200.0
300.0
Vp 2006.0 done
100.0
200.0
300.0
Vp 2007.0 done
100.0
200.0
300.0
Vp 2008.0 done
100.0
200.0
300.0
Vp 2009.0 done
100.0
200.0
300.0
Vp 2010.0 done
100.0
200.0
300.0
Vp 2011.0 done
100.0
200.0
300.0
Vp 2012.0 done
100.0
200.0
300.0
Vp 2013.0 done
100.0
200.0
300.0
Tp1999.0 done
100.0
200.0
300.0
Tp2000.0 done
100.0
200.0
300.0
Tp2001.0 done
100.0
200.0
300.0
Tp2002.0 done
100.0
200.0
300.0
Tp2003.0 done
100.0
200.0
300.0
Tp2004.0 done
100.0
200.0
300.0
Tp2005.0 done
100.0
200.0
300.0
Tp2006.0 done
100.0
200.0
300.0
Tp2007.0 done
100.0
200.0
300.0
Tp2008.0 done
100.0
200.0
300.0
Tp2009.0 done
100.0
200.0
300.0
Tp2010.0 done
100.0
200.0
300.0
Tp2011.0 done
100.0
200.0
300.0
Tp2012.0 done
100.0
200.0
300.0
Tp2013.0 done
2012.0 번째 df 끝
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
      <th>kp_21h</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>21.0</td>
      <td>0.0</td>
      <td>6.898000</td>
      <td>80552.0</td>
      <td>404.380000</td>
      <td>-1.803</td>
      <td>5.257</td>
      <td>-1.394</td>
      <td>5.789</td>
      <td>1</td>
    </tr>
    <tr>
      <th>928772</th>
      <td>1</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>21.0</td>
      <td>1.0</td>
      <td>6.934344</td>
      <td>83036.8</td>
      <td>406.732468</td>
      <td>-3.149</td>
      <td>4.001</td>
      <td>-2.746</td>
      <td>5.838</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>21.0</td>
      <td>2.0</td>
      <td>6.930000</td>
      <td>91507.0</td>
      <td>399.330000</td>
      <td>-2.757</td>
      <td>4.494</td>
      <td>-2.370</td>
      <td>5.803</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>21.0</td>
      <td>3.0</td>
      <td>7.420000</td>
      <td>84794.0</td>
      <td>399.000000</td>
      <td>-2.575</td>
      <td>4.343</td>
      <td>-2.654</td>
      <td>5.772</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>1999.0</td>
      <td>1.0</td>
      <td>21.0</td>
      <td>4.0</td>
      <td>7.339000</td>
      <td>86177.0</td>
      <td>399.550000</td>
      <td>-2.671</td>
      <td>4.197</td>
      <td>-1.908</td>
      <td>5.722</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">save</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">save</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace0.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace3.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace6.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace9.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>

<span class="n">save</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace12.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace15.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace18.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace21.csv&#39;</span><span class="p">,</span> <span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
  <span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="s1">&#39;Unnamed: 0.1&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#B류 -9999처리하기</span>
<span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">save</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">deal_all</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">k</span><span class="o">=</span><span class="mi">0</span>
<span class="k">for</span> <span class="n">ace0</span> <span class="ow">in</span> <span class="n">df</span><span class="p">:</span>
  <span class="n">df_gsm_x</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df_gsm_y</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df_gsm_z</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="n">df_gsm_t</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
      <span class="n">mean_x</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">1000</span><span class="p">)][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
      <span class="n">gsm_x</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">1000</span><span class="p">)]</span>
      <span class="n">gsm_x</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_x</span>
      <span class="n">df_gsm_x</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_gsm_x</span><span class="p">,</span><span class="n">gsm_x</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;gsm_x &quot;</span> <span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>
  
  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_gsm_x</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
  
    
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
      <span class="n">mean_y</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">1000</span><span class="p">)][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
      <span class="n">gsm_y</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">1000</span><span class="p">)]</span>
      <span class="n">gsm_y</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_y</span>
      <span class="n">df_gsm_y</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_gsm_y</span><span class="p">,</span><span class="n">gsm_y</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;gsm_y &quot;</span> <span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>
    
  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_gsm_y</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    
    
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
      <span class="n">mean_z</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">1000</span><span class="p">)][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
      <span class="n">gsm_z</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">1000</span><span class="p">)]</span>
      <span class="n">gsm_z</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_z</span>
      <span class="n">df_gsm_z</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_gsm_z</span><span class="p">,</span><span class="n">gsm_z</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;gsm_z &quot;</span> <span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>

  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_gsm_z</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
    
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">():</span>
      <span class="n">mean_t</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">1000</span><span class="p">)][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
      <span class="n">gsm_t</span><span class="o">=</span><span class="n">ace0</span><span class="p">[(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">j</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">1000</span><span class="p">)]</span>
      <span class="n">gsm_t</span><span class="p">[</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">mean_t</span>
      <span class="n">df_gsm_t</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df_gsm_t</span><span class="p">,</span><span class="n">gsm_t</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Bt &quot;</span> <span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot; done&quot;</span><span class="p">)</span>

  <span class="n">ace0</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">ace0</span><span class="p">,</span><span class="n">df_gsm_t</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  <span class="n">ace0</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;hr&#39;</span><span class="p">,</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">keep</span><span class="o">=</span><span class="s1">&#39;last&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
  
  <span class="n">deal_all</span><span class="p">[</span><span class="n">k</span><span class="p">]</span><span class="o">=</span><span class="n">ace0</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
  <span class="n">k</span><span class="o">+=</span><span class="mi">1</span>
  <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">k</span><span class="o">-</span><span class="mi">1</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39; 번째 df 끝&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>gsm_x 1999.0 done
gsm_x 2000.0 done
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:13: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  del sys.path[0]
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:28: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:42: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:56: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
0 번째 df 끝
gsm_x 1999.0 done
gsm_x 2000.0 done
gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
1 번째 df 끝
gsm_x 1999.0 done
gsm_x 2000.0 done
gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
2 번째 df 끝
gsm_x 1999.0 done
gsm_x 2000.0 done
gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
3 번째 df 끝
gsm_x 1999.0 done
gsm_x 2000.0 done
gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
4 번째 df 끝
gsm_x 1999.0 done
gsm_x 2000.0 done
gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
5 번째 df 끝
gsm_x 1999.0 done
gsm_x 2000.0 done
gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
6 번째 df 끝
gsm_x 1999.0 done
gsm_x 2000.0 done
gsm_x 2001.0 done
gsm_x 2002.0 done
gsm_x 2003.0 done
gsm_x 2004.0 done
gsm_x 2005.0 done
gsm_x 2006.0 done
gsm_x 2007.0 done
gsm_x 2008.0 done
gsm_x 2009.0 done
gsm_x 2010.0 done
gsm_x 2011.0 done
gsm_x 2012.0 done
gsm_x 2013.0 done
gsm_y 1999.0 done
gsm_y 2000.0 done
gsm_y 2001.0 done
gsm_y 2002.0 done
gsm_y 2003.0 done
gsm_y 2004.0 done
gsm_y 2005.0 done
gsm_y 2006.0 done
gsm_y 2007.0 done
gsm_y 2008.0 done
gsm_y 2009.0 done
gsm_y 2010.0 done
gsm_y 2011.0 done
gsm_y 2012.0 done
gsm_y 2013.0 done
gsm_z 1999.0 done
gsm_z 2000.0 done
gsm_z 2001.0 done
gsm_z 2002.0 done
gsm_z 2003.0 done
gsm_z 2004.0 done
gsm_z 2005.0 done
gsm_z 2006.0 done
gsm_z 2007.0 done
gsm_z 2008.0 done
gsm_z 2009.0 done
gsm_z 2010.0 done
gsm_z 2011.0 done
gsm_z 2012.0 done
gsm_z 2013.0 done
Bt 1999.0 done
Bt 2000.0 done
Bt 2001.0 done
Bt 2002.0 done
Bt 2003.0 done
Bt 2004.0 done
Bt 2005.0 done
Bt 2006.0 done
Bt 2007.0 done
Bt 2008.0 done
Bt 2009.0 done
Bt 2010.0 done
Bt 2011.0 done
Bt 2012.0 done
Bt 2013.0 done
7 번째 df 끝
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">deal_all</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace0.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">deal_all</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace3.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">deal_all</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace6.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">deal_all</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace9.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">deal_all</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace12.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">deal_all</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace15.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">deal_all</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace18.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">deal_all</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace21.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">ace0</span><span class="p">[</span><span class="n">ace0</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">1000</span><span class="p">]</span>
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
      <th>kp_21h</th>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aaa</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9_process_for_all/ace0.csv&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aaa</span><span class="p">[</span><span class="n">aaa</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
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
      <th>kp_0h</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1498</th>
      <td>1498</td>
      <td>1999.0</td>
      <td>9.0</td>
      <td>2.0</td>
      <td>36.0</td>
      <td>1.94300</td>
      <td>85188.000000</td>
      <td>478.650000</td>
      <td>0.0</td>
      <td>-7.465</td>
      <td>1.244</td>
      <td>7.750</td>
      <td>3</td>
    </tr>
    <tr>
      <th>76301</th>
      <td>76301</td>
      <td>2000.0</td>
      <td>87.0</td>
      <td>1.0</td>
      <td>31.0</td>
      <td>1.86400</td>
      <td>76160.000000</td>
      <td>472.920000</td>
      <td>-0.0</td>
      <td>1.402</td>
      <td>3.494</td>
      <td>3.780</td>
      <td>2</td>
    </tr>
    <tr>
      <th>85404</th>
      <td>85404</td>
      <td>2000.0</td>
      <td>141.0</td>
      <td>1.0</td>
      <td>50.0</td>
      <td>1.70800</td>
      <td>128730.000000</td>
      <td>585.660000</td>
      <td>-0.0</td>
      <td>-0.191</td>
      <td>4.604</td>
      <td>4.676</td>
      <td>2</td>
    </tr>
    <tr>
      <th>114161</th>
      <td>114161</td>
      <td>2000.0</td>
      <td>312.0</td>
      <td>0.0</td>
      <td>58.0</td>
      <td>3.93100</td>
      <td>16789.000000</td>
      <td>556.830000</td>
      <td>-0.0</td>
      <td>13.480</td>
      <td>-10.843</td>
      <td>17.666</td>
      <td>5</td>
    </tr>
    <tr>
      <th>122595</th>
      <td>122595</td>
      <td>2000.0</td>
      <td>362.0</td>
      <td>0.0</td>
      <td>41.0</td>
      <td>4.42700</td>
      <td>17787.000000</td>
      <td>428.390000</td>
      <td>-0.0</td>
      <td>-10.190</td>
      <td>0.776</td>
      <td>10.255</td>
      <td>1</td>
    </tr>
    <tr>
      <th>168181</th>
      <td>168181</td>
      <td>2001.0</td>
      <td>266.0</td>
      <td>1.0</td>
      <td>55.0</td>
      <td>7.18851</td>
      <td>59569.322581</td>
      <td>338.423077</td>
      <td>-0.0</td>
      <td>6.362</td>
      <td>1.354</td>
      <td>6.514</td>
      <td>0</td>
    </tr>
    <tr>
      <th>168879</th>
      <td>168879</td>
      <td>2001.0</td>
      <td>270.0</td>
      <td>2.0</td>
      <td>19.0</td>
      <td>6.05900</td>
      <td>144320.000000</td>
      <td>439.650000</td>
      <td>-0.0</td>
      <td>-1.856</td>
      <td>-3.275</td>
      <td>3.777</td>
      <td>1</td>
    </tr>
    <tr>
      <th>174479</th>
      <td>174479</td>
      <td>2001.0</td>
      <td>303.0</td>
      <td>2.0</td>
      <td>43.0</td>
      <td>4.04700</td>
      <td>35954.000000</td>
      <td>391.950000</td>
      <td>-0.0</td>
      <td>4.691</td>
      <td>-2.347</td>
      <td>5.271</td>
      <td>2</td>
    </tr>
    <tr>
      <th>177092</th>
      <td>177092</td>
      <td>2001.0</td>
      <td>319.0</td>
      <td>1.0</td>
      <td>6.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>288.490000</td>
      <td>0.0</td>
      <td>0.349</td>
      <td>3.715</td>
      <td>3.733</td>
      <td>0</td>
    </tr>
    <tr>
      <th>255348</th>
      <td>255348</td>
      <td>2003.0</td>
      <td>53.0</td>
      <td>0.0</td>
      <td>14.0</td>
      <td>3.68200</td>
      <td>111090.000000</td>
      <td>575.990000</td>
      <td>-0.0</td>
      <td>6.009</td>
      <td>0.601</td>
      <td>6.055</td>
      <td>2</td>
    </tr>
    <tr>
      <th>264729</th>
      <td>264729</td>
      <td>2003.0</td>
      <td>108.0</td>
      <td>1.0</td>
      <td>46.0</td>
      <td>3.35800</td>
      <td>139130.000000</td>
      <td>656.270000</td>
      <td>-0.0</td>
      <td>3.297</td>
      <td>3.014</td>
      <td>5.005</td>
      <td>2</td>
    </tr>
    <tr>
      <th>266435</th>
      <td>266435</td>
      <td>2003.0</td>
      <td>118.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.60200</td>
      <td>160370.000000</td>
      <td>533.430000</td>
      <td>-0.0</td>
      <td>-4.962</td>
      <td>-3.517</td>
      <td>6.188</td>
      <td>3</td>
    </tr>
    <tr>
      <th>278835</th>
      <td>278835</td>
      <td>2003.0</td>
      <td>192.0</td>
      <td>0.0</td>
      <td>9.0</td>
      <td>7.97000</td>
      <td>17072.000000</td>
      <td>356.040000</td>
      <td>0.0</td>
      <td>7.880</td>
      <td>-5.769</td>
      <td>9.780</td>
      <td>3</td>
    </tr>
    <tr>
      <th>317595</th>
      <td>317595</td>
      <td>2004.0</td>
      <td>56.0</td>
      <td>2.0</td>
      <td>40.0</td>
      <td>3.48700</td>
      <td>31882.000000</td>
      <td>373.670000</td>
      <td>0.0</td>
      <td>-1.983</td>
      <td>-2.539</td>
      <td>3.226</td>
      <td>2</td>
    </tr>
    <tr>
      <th>336952</th>
      <td>336952</td>
      <td>2004.0</td>
      <td>171.0</td>
      <td>1.0</td>
      <td>53.0</td>
      <td>3.99200</td>
      <td>124050.000000</td>
      <td>500.020000</td>
      <td>0.0</td>
      <td>4.284</td>
      <td>3.587</td>
      <td>5.881</td>
      <td>2</td>
    </tr>
    <tr>
      <th>345599</th>
      <td>345599</td>
      <td>2004.0</td>
      <td>222.0</td>
      <td>2.0</td>
      <td>23.0</td>
      <td>NaN</td>
      <td>26158.000000</td>
      <td>385.650000</td>
      <td>0.0</td>
      <td>5.198</td>
      <td>0.602</td>
      <td>5.236</td>
      <td>2</td>
    </tr>
    <tr>
      <th>350132</th>
      <td>350132</td>
      <td>2004.0</td>
      <td>249.0</td>
      <td>1.0</td>
      <td>51.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>307.150000</td>
      <td>-0.0</td>
      <td>2.105</td>
      <td>-0.413</td>
      <td>2.158</td>
      <td>1</td>
    </tr>
    <tr>
      <th>357391</th>
      <td>357391</td>
      <td>2004.0</td>
      <td>292.0</td>
      <td>1.0</td>
      <td>42.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>300.720000</td>
      <td>0.0</td>
      <td>0.604</td>
      <td>1.728</td>
      <td>1.833</td>
      <td>0</td>
    </tr>
    <tr>
      <th>371762</th>
      <td>371762</td>
      <td>2005.0</td>
      <td>11.0</td>
      <td>1.0</td>
      <td>48.0</td>
      <td>6.09700</td>
      <td>119570.000000</td>
      <td>448.740000</td>
      <td>0.0</td>
      <td>4.120</td>
      <td>2.118</td>
      <td>4.659</td>
      <td>1</td>
    </tr>
    <tr>
      <th>399252</th>
      <td>399252</td>
      <td>2005.0</td>
      <td>174.0</td>
      <td>2.0</td>
      <td>42.0</td>
      <td>NaN</td>
      <td>58619.000000</td>
      <td>359.780000</td>
      <td>-0.0</td>
      <td>6.403</td>
      <td>-10.339</td>
      <td>12.187</td>
      <td>4</td>
    </tr>
    <tr>
      <th>420272</th>
      <td>420272</td>
      <td>2005.0</td>
      <td>299.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>11.61600</td>
      <td>63149.000000</td>
      <td>438.910000</td>
      <td>-0.0</td>
      <td>3.752</td>
      <td>0.229</td>
      <td>3.849</td>
      <td>1</td>
    </tr>
    <tr>
      <th>423017</th>
      <td>423017</td>
      <td>2005.0</td>
      <td>315.0</td>
      <td>1.0</td>
      <td>43.0</td>
      <td>15.08800</td>
      <td>38627.000000</td>
      <td>348.320000</td>
      <td>0.0</td>
      <td>-3.528</td>
      <td>-0.586</td>
      <td>3.600</td>
      <td>1</td>
    </tr>
    <tr>
      <th>438008</th>
      <td>438008</td>
      <td>2006.0</td>
      <td>39.0</td>
      <td>0.0</td>
      <td>50.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>318.700000</td>
      <td>0.0</td>
      <td>-2.430</td>
      <td>-3.096</td>
      <td>3.947</td>
      <td>2</td>
    </tr>
    <tr>
      <th>439931</th>
      <td>439931</td>
      <td>2006.0</td>
      <td>50.0</td>
      <td>1.0</td>
      <td>58.0</td>
      <td>16.96100</td>
      <td>40100.000000</td>
      <td>369.800000</td>
      <td>0.0</td>
      <td>-5.629</td>
      <td>-0.297</td>
      <td>5.644</td>
      <td>2</td>
    </tr>
    <tr>
      <th>471268</th>
      <td>471268</td>
      <td>2006.0</td>
      <td>236.0</td>
      <td>1.0</td>
      <td>41.0</td>
      <td>3.89600</td>
      <td>37714.000000</td>
      <td>423.090000</td>
      <td>0.0</td>
      <td>4.411</td>
      <td>0.335</td>
      <td>4.429</td>
      <td>3</td>
    </tr>
    <tr>
      <th>473962</th>
      <td>473962</td>
      <td>2006.0</td>
      <td>252.0</td>
      <td>1.0</td>
      <td>47.0</td>
      <td>7.68500</td>
      <td>26634.000000</td>
      <td>362.190000</td>
      <td>0.0</td>
      <td>1.230</td>
      <td>0.500</td>
      <td>1.348</td>
      <td>1</td>
    </tr>
    <tr>
      <th>484873</th>
      <td>484873</td>
      <td>2006.0</td>
      <td>317.0</td>
      <td>0.0</td>
      <td>42.0</td>
      <td>1.83100</td>
      <td>61914.000000</td>
      <td>472.850000</td>
      <td>-0.0</td>
      <td>1.532</td>
      <td>-0.788</td>
      <td>1.732</td>
      <td>0</td>
    </tr>
    <tr>
      <th>494774</th>
      <td>494774</td>
      <td>2007.0</td>
      <td>10.0</td>
      <td>2.0</td>
      <td>27.0</td>
      <td>5.90700</td>
      <td>73086.000000</td>
      <td>395.770000</td>
      <td>-0.0</td>
      <td>-8.117</td>
      <td>-0.695</td>
      <td>8.248</td>
      <td>1</td>
    </tr>
    <tr>
      <th>507174</th>
      <td>507174</td>
      <td>2007.0</td>
      <td>84.0</td>
      <td>0.0</td>
      <td>34.0</td>
      <td>24.75400</td>
      <td>34338.000000</td>
      <td>370.700000</td>
      <td>0.0</td>
      <td>1.745</td>
      <td>11.284</td>
      <td>11.425</td>
      <td>2</td>
    </tr>
    <tr>
      <th>523804</th>
      <td>523804</td>
      <td>2007.0</td>
      <td>182.0</td>
      <td>1.0</td>
      <td>46.0</td>
      <td>5.05400</td>
      <td>45804.000000</td>
      <td>416.610000</td>
      <td>0.0</td>
      <td>3.782</td>
      <td>0.964</td>
      <td>3.914</td>
      <td>2</td>
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
    </tr>
    <tr>
      <th>582392</th>
      <td>582392</td>
      <td>2008.0</td>
      <td>164.0</td>
      <td>2.0</td>
      <td>44.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>316.600000</td>
      <td>-0.0</td>
      <td>-0.006</td>
      <td>0.217</td>
      <td>0.274</td>
      <td>1</td>
    </tr>
    <tr>
      <th>598202</th>
      <td>598202</td>
      <td>2008.0</td>
      <td>258.0</td>
      <td>1.0</td>
      <td>23.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>275.320000</td>
      <td>-0.0</td>
      <td>-1.239</td>
      <td>1.365</td>
      <td>1.849</td>
      <td>0</td>
    </tr>
    <tr>
      <th>599559</th>
      <td>599559</td>
      <td>2008.0</td>
      <td>266.0</td>
      <td>1.0</td>
      <td>28.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>294.890802</td>
      <td>-0.0</td>
      <td>-2.097</td>
      <td>3.270</td>
      <td>3.914</td>
      <td>3</td>
    </tr>
    <tr>
      <th>640323</th>
      <td>640323</td>
      <td>2009.0</td>
      <td>142.0</td>
      <td>0.0</td>
      <td>59.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>328.710000</td>
      <td>0.0</td>
      <td>0.873</td>
      <td>3.955</td>
      <td>4.068</td>
      <td>1</td>
    </tr>
    <tr>
      <th>642013</th>
      <td>642013</td>
      <td>2009.0</td>
      <td>152.0</td>
      <td>0.0</td>
      <td>59.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>327.883711</td>
      <td>-0.0</td>
      <td>3.138</td>
      <td>-1.519</td>
      <td>3.489</td>
      <td>1</td>
    </tr>
    <tr>
      <th>645000</th>
      <td>645000</td>
      <td>2009.0</td>
      <td>170.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>318.450000</td>
      <td>0.0</td>
      <td>2.064</td>
      <td>2.110</td>
      <td>2.956</td>
      <td>2</td>
    </tr>
    <tr>
      <th>657991</th>
      <td>657991</td>
      <td>2009.0</td>
      <td>246.0</td>
      <td>2.0</td>
      <td>37.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>328.150000</td>
      <td>-0.0</td>
      <td>-0.441</td>
      <td>-0.168</td>
      <td>0.491</td>
      <td>1</td>
    </tr>
    <tr>
      <th>663867</th>
      <td>663867</td>
      <td>2009.0</td>
      <td>281.0</td>
      <td>1.0</td>
      <td>55.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>274.280000</td>
      <td>0.0</td>
      <td>2.039</td>
      <td>-2.736</td>
      <td>3.419</td>
      <td>1</td>
    </tr>
    <tr>
      <th>667912</th>
      <td>667912</td>
      <td>2009.0</td>
      <td>305.0</td>
      <td>1.0</td>
      <td>43.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>322.420000</td>
      <td>0.0</td>
      <td>4.656</td>
      <td>1.226</td>
      <td>4.819</td>
      <td>0</td>
    </tr>
    <tr>
      <th>747273</th>
      <td>747273</td>
      <td>2011.0</td>
      <td>21.0</td>
      <td>1.0</td>
      <td>33.0</td>
      <td>NaN</td>
      <td>52999.000000</td>
      <td>417.420000</td>
      <td>0.0</td>
      <td>4.154</td>
      <td>1.195</td>
      <td>4.440</td>
      <td>0</td>
    </tr>
    <tr>
      <th>749152</th>
      <td>749152</td>
      <td>2011.0</td>
      <td>32.0</td>
      <td>1.0</td>
      <td>55.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>367.915556</td>
      <td>0.0</td>
      <td>3.771</td>
      <td>-5.348</td>
      <td>6.586</td>
      <td>2</td>
    </tr>
    <tr>
      <th>750297</th>
      <td>750297</td>
      <td>2011.0</td>
      <td>39.0</td>
      <td>1.0</td>
      <td>18.0</td>
      <td>1.96600</td>
      <td>47499.000000</td>
      <td>449.050000</td>
      <td>0.0</td>
      <td>-1.640</td>
      <td>-2.769</td>
      <td>3.230</td>
      <td>2</td>
    </tr>
    <tr>
      <th>773364</th>
      <td>773364</td>
      <td>2011.0</td>
      <td>176.0</td>
      <td>1.0</td>
      <td>29.0</td>
      <td>1.61600</td>
      <td>133130.000000</td>
      <td>602.640000</td>
      <td>-0.0</td>
      <td>-1.978</td>
      <td>2.479</td>
      <td>3.185</td>
      <td>2</td>
    </tr>
    <tr>
      <th>774515</th>
      <td>774515</td>
      <td>2011.0</td>
      <td>183.0</td>
      <td>0.0</td>
      <td>55.0</td>
      <td>6.08200</td>
      <td>58209.000000</td>
      <td>396.040000</td>
      <td>0.0</td>
      <td>1.259</td>
      <td>5.007</td>
      <td>5.181</td>
      <td>0</td>
    </tr>
    <tr>
      <th>776998</th>
      <td>776998</td>
      <td>2011.0</td>
      <td>197.0</td>
      <td>2.0</td>
      <td>59.0</td>
      <td>4.35100</td>
      <td>23403.000000</td>
      <td>394.010000</td>
      <td>-0.0</td>
      <td>3.363</td>
      <td>-2.111</td>
      <td>3.972</td>
      <td>1</td>
    </tr>
    <tr>
      <th>784692</th>
      <td>784692</td>
      <td>2011.0</td>
      <td>243.0</td>
      <td>1.0</td>
      <td>34.0</td>
      <td>NaN</td>
      <td>44645.000000</td>
      <td>362.000000</td>
      <td>-0.0</td>
      <td>-1.508</td>
      <td>-0.572</td>
      <td>1.623</td>
      <td>0</td>
    </tr>
    <tr>
      <th>818574</th>
      <td>818574</td>
      <td>2012.0</td>
      <td>79.0</td>
      <td>0.0</td>
      <td>6.0</td>
      <td>NaN</td>
      <td>80233.000000</td>
      <td>502.960000</td>
      <td>0.0</td>
      <td>-4.219</td>
      <td>0.782</td>
      <td>4.294</td>
      <td>2</td>
    </tr>
    <tr>
      <th>828198</th>
      <td>828198</td>
      <td>2012.0</td>
      <td>136.0</td>
      <td>0.0</td>
      <td>57.0</td>
      <td>2.39000</td>
      <td>26232.000000</td>
      <td>424.430000</td>
      <td>0.0</td>
      <td>-3.606</td>
      <td>-0.396</td>
      <td>3.644</td>
      <td>2</td>
    </tr>
    <tr>
      <th>828712</th>
      <td>828712</td>
      <td>2012.0</td>
      <td>139.0</td>
      <td>1.0</td>
      <td>8.0</td>
      <td>10.41100</td>
      <td>65765.000000</td>
      <td>419.970000</td>
      <td>-0.0</td>
      <td>-10.316</td>
      <td>0.643</td>
      <td>10.346</td>
      <td>3</td>
    </tr>
    <tr>
      <th>846717</th>
      <td>846717</td>
      <td>2012.0</td>
      <td>246.0</td>
      <td>0.0</td>
      <td>22.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>307.080000</td>
      <td>0.0</td>
      <td>5.610</td>
      <td>-3.260</td>
      <td>6.493</td>
      <td>2</td>
    </tr>
    <tr>
      <th>858259</th>
      <td>858259</td>
      <td>2012.0</td>
      <td>314.0</td>
      <td>1.0</td>
      <td>16.0</td>
      <td>NaN</td>
      <td>32836.000000</td>
      <td>383.340000</td>
      <td>-0.0</td>
      <td>-3.833</td>
      <td>-0.349</td>
      <td>3.861</td>
      <td>0</td>
    </tr>
    <tr>
      <th>862160</th>
      <td>862160</td>
      <td>2012.0</td>
      <td>337.0</td>
      <td>1.0</td>
      <td>31.0</td>
      <td>16.46900</td>
      <td>11036.000000</td>
      <td>348.430000</td>
      <td>0.0</td>
      <td>9.986</td>
      <td>-4.068</td>
      <td>10.794</td>
      <td>2</td>
    </tr>
    <tr>
      <th>863566</th>
      <td>863566</td>
      <td>2012.0</td>
      <td>345.0</td>
      <td>2.0</td>
      <td>28.0</td>
      <td>NaN</td>
      <td>50695.000000</td>
      <td>316.200000</td>
      <td>-0.0</td>
      <td>4.978</td>
      <td>1.342</td>
      <td>5.176</td>
      <td>2</td>
    </tr>
    <tr>
      <th>867593</th>
      <td>867593</td>
      <td>2013.0</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>57.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>304.342671</td>
      <td>-0.0</td>
      <td>-1.613</td>
      <td>1.046</td>
      <td>1.949</td>
      <td>0</td>
    </tr>
    <tr>
      <th>867606</th>
      <td>867606</td>
      <td>2013.0</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>11.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>304.650000</td>
      <td>-0.0</td>
      <td>-0.560</td>
      <td>1.652</td>
      <td>1.753</td>
      <td>0</td>
    </tr>
    <tr>
      <th>879216</th>
      <td>879216</td>
      <td>2013.0</td>
      <td>72.0</td>
      <td>1.0</td>
      <td>16.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>332.180000</td>
      <td>-0.0</td>
      <td>1.586</td>
      <td>2.628</td>
      <td>3.119</td>
      <td>1</td>
    </tr>
    <tr>
      <th>880876</th>
      <td>880876</td>
      <td>2013.0</td>
      <td>82.0</td>
      <td>0.0</td>
      <td>44.0</td>
      <td>6.11700</td>
      <td>23948.000000</td>
      <td>384.530000</td>
      <td>-0.0</td>
      <td>0.020</td>
      <td>0.306</td>
      <td>0.339</td>
      <td>2</td>
    </tr>
    <tr>
      <th>906760</th>
      <td>906760</td>
      <td>2013.0</td>
      <td>236.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.33400</td>
      <td>72091.000000</td>
      <td>508.040000</td>
      <td>-0.0</td>
      <td>7.927</td>
      <td>0.203</td>
      <td>7.938</td>
      <td>2</td>
    </tr>
    <tr>
      <th>918753</th>
      <td>918753</td>
      <td>2013.0</td>
      <td>306.0</td>
      <td>2.0</td>
      <td>55.0</td>
      <td>6.26200</td>
      <td>17895.000000</td>
      <td>340.080000</td>
      <td>-0.0</td>
      <td>-0.644</td>
      <td>-1.642</td>
      <td>1.901</td>
      <td>1</td>
    </tr>
    <tr>
      <th>925570</th>
      <td>925570</td>
      <td>2013.0</td>
      <td>347.0</td>
      <td>0.0</td>
      <td>55.0</td>
      <td>NaN</td>
      <td>12802.000000</td>
      <td>273.630000</td>
      <td>0.0</td>
      <td>1.693</td>
      <td>-0.450</td>
      <td>1.755</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>62 rows × 13 columns</p>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="p">[</span><span class="n">train</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
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
      <th>3945</th>
      <td>3945</td>
      <td>1999.0</td>
      <td>3.0</td>
      <td>22.0</td>
      <td>8.0</td>
      <td>7.749</td>
      <td>18800.0</td>
      <td>350.74</td>
      <td>0.0</td>
      <td>5.489</td>
      <td>0.586</td>
      <td>5.543</td>
    </tr>
    <tr>
      <th>10946</th>
      <td>10946</td>
      <td>1999.0</td>
      <td>9.0</td>
      <td>2.0</td>
      <td>36.0</td>
      <td>1.943</td>
      <td>85188.0</td>
      <td>478.65</td>
      <td>0.0</td>
      <td>-7.465</td>
      <td>1.244</td>
      <td>7.750</td>
    </tr>
    <tr>
      <th>34230</th>
      <td>34230</td>
      <td>1999.0</td>
      <td>26.0</td>
      <td>8.0</td>
      <td>32.0</td>
      <td>6.409</td>
      <td>37600.0</td>
      <td>397.74</td>
      <td>0.0</td>
      <td>-1.082</td>
      <td>-5.172</td>
      <td>5.299</td>
    </tr>
    <tr>
      <th>44816</th>
      <td>44816</td>
      <td>1999.0</td>
      <td>34.0</td>
      <td>4.0</td>
      <td>44.0</td>
      <td>-9999.900</td>
      <td>-9999.9</td>
      <td>291.03</td>
      <td>-0.0</td>
      <td>-5.709</td>
      <td>0.742</td>
      <td>5.794</td>
    </tr>
    <tr>
      <th>62950</th>
      <td>62950</td>
      <td>1999.0</td>
      <td>47.0</td>
      <td>15.0</td>
      <td>7.0</td>
      <td>2.434</td>
      <td>46189.0</td>
      <td>467.10</td>
      <td>0.0</td>
      <td>0.808</td>
      <td>3.863</td>
      <td>3.949</td>
    </tr>
    <tr>
      <th>88018</th>
      <td>88018</td>
      <td>1999.0</td>
      <td>66.0</td>
      <td>4.0</td>
      <td>46.0</td>
      <td>6.728</td>
      <td>41055.0</td>
      <td>455.56</td>
      <td>0.0</td>
      <td>-4.503</td>
      <td>-6.604</td>
      <td>8.037</td>
    </tr>
    <tr>
      <th>102218</th>
      <td>102218</td>
      <td>1999.0</td>
      <td>76.0</td>
      <td>17.0</td>
      <td>13.0</td>
      <td>5.642</td>
      <td>81275.0</td>
      <td>428.10</td>
      <td>-0.0</td>
      <td>5.571</td>
      <td>1.627</td>
      <td>6.205</td>
    </tr>
    <tr>
      <th>123678</th>
      <td>123678</td>
      <td>1999.0</td>
      <td>92.0</td>
      <td>14.0</td>
      <td>43.0</td>
      <td>13.506</td>
      <td>40178.0</td>
      <td>436.01</td>
      <td>0.0</td>
      <td>-8.398</td>
      <td>0.108</td>
      <td>8.400</td>
    </tr>
    <tr>
      <th>124904</th>
      <td>124904</td>
      <td>1999.0</td>
      <td>93.0</td>
      <td>12.0</td>
      <td>31.0</td>
      <td>10.080</td>
      <td>52440.0</td>
      <td>404.88</td>
      <td>0.0</td>
      <td>-4.216</td>
      <td>1.283</td>
      <td>4.504</td>
    </tr>
    <tr>
      <th>131392</th>
      <td>131392</td>
      <td>1999.0</td>
      <td>98.0</td>
      <td>7.0</td>
      <td>51.0</td>
      <td>15.575</td>
      <td>18948.0</td>
      <td>362.39</td>
      <td>-0.0</td>
      <td>-0.959</td>
      <td>0.575</td>
      <td>1.130</td>
    </tr>
    <tr>
      <th>141723</th>
      <td>141723</td>
      <td>1999.0</td>
      <td>105.0</td>
      <td>23.0</td>
      <td>31.0</td>
      <td>3.663</td>
      <td>39175.0</td>
      <td>425.23</td>
      <td>0.0</td>
      <td>2.378</td>
      <td>5.404</td>
      <td>6.088</td>
    </tr>
    <tr>
      <th>163933</th>
      <td>163933</td>
      <td>1999.0</td>
      <td>122.0</td>
      <td>10.0</td>
      <td>22.0</td>
      <td>2.399</td>
      <td>121740.0</td>
      <td>568.03</td>
      <td>0.0</td>
      <td>-3.132</td>
      <td>-1.480</td>
      <td>3.497</td>
    </tr>
    <tr>
      <th>194655</th>
      <td>194655</td>
      <td>1999.0</td>
      <td>145.0</td>
      <td>4.0</td>
      <td>32.0</td>
      <td>9.228</td>
      <td>333970.0</td>
      <td>512.33</td>
      <td>0.0</td>
      <td>-2.064</td>
      <td>4.158</td>
      <td>4.696</td>
    </tr>
    <tr>
      <th>204733</th>
      <td>204733</td>
      <td>1999.0</td>
      <td>152.0</td>
      <td>15.0</td>
      <td>42.0</td>
      <td>10.977</td>
      <td>22774.0</td>
      <td>370.31</td>
      <td>0.0</td>
      <td>3.833</td>
      <td>-4.089</td>
      <td>5.609</td>
    </tr>
    <tr>
      <th>206734</th>
      <td>206734</td>
      <td>1999.0</td>
      <td>154.0</td>
      <td>3.0</td>
      <td>16.0</td>
      <td>4.448</td>
      <td>27066.0</td>
      <td>430.48</td>
      <td>-0.0</td>
      <td>7.433</td>
      <td>6.769</td>
      <td>10.059</td>
    </tr>
    <tr>
      <th>226328</th>
      <td>226328</td>
      <td>1999.0</td>
      <td>168.0</td>
      <td>15.0</td>
      <td>36.0</td>
      <td>5.789</td>
      <td>56328.0</td>
      <td>404.45</td>
      <td>-0.0</td>
      <td>7.266</td>
      <td>0.707</td>
      <td>7.314</td>
    </tr>
    <tr>
      <th>228880</th>
      <td>228880</td>
      <td>1999.0</td>
      <td>170.0</td>
      <td>12.0</td>
      <td>58.0</td>
      <td>6.004</td>
      <td>52238.0</td>
      <td>373.54</td>
      <td>0.0</td>
      <td>4.130</td>
      <td>-1.701</td>
      <td>4.476</td>
    </tr>
    <tr>
      <th>236097</th>
      <td>236097</td>
      <td>1999.0</td>
      <td>175.0</td>
      <td>21.0</td>
      <td>17.0</td>
      <td>-9999.900</td>
      <td>-9999.9</td>
      <td>297.27</td>
      <td>-0.0</td>
      <td>4.576</td>
      <td>-1.506</td>
      <td>4.838</td>
    </tr>
    <tr>
      <th>256755</th>
      <td>256755</td>
      <td>1999.0</td>
      <td>191.0</td>
      <td>4.0</td>
      <td>32.0</td>
      <td>3.666</td>
      <td>13368.0</td>
      <td>323.15</td>
      <td>0.0</td>
      <td>-5.028</td>
      <td>-0.553</td>
      <td>5.060</td>
    </tr>
    <tr>
      <th>258441</th>
      <td>258441</td>
      <td>1999.0</td>
      <td>192.0</td>
      <td>10.0</td>
      <td>30.0</td>
      <td>-9999.900</td>
      <td>-9999.9</td>
      <td>281.14</td>
      <td>-0.0</td>
      <td>-3.466</td>
      <td>-3.425</td>
      <td>4.878</td>
    </tr>
    <tr>
      <th>260066</th>
      <td>260066</td>
      <td>1999.0</td>
      <td>193.0</td>
      <td>15.0</td>
      <td>24.0</td>
      <td>-9999.900</td>
      <td>-9999.9</td>
      <td>305.34</td>
      <td>-0.0</td>
      <td>-1.064</td>
      <td>-4.662</td>
      <td>4.810</td>
    </tr>
    <tr>
      <th>283784</th>
      <td>283784</td>
      <td>1999.0</td>
      <td>211.0</td>
      <td>5.0</td>
      <td>3.0</td>
      <td>4.499</td>
      <td>32235.0</td>
      <td>368.18</td>
      <td>-0.0</td>
      <td>3.166</td>
      <td>-6.403</td>
      <td>7.231</td>
    </tr>
    <tr>
      <th>293139</th>
      <td>293139</td>
      <td>1999.0</td>
      <td>218.0</td>
      <td>3.0</td>
      <td>21.0</td>
      <td>24.985</td>
      <td>18650.0</td>
      <td>345.13</td>
      <td>-0.0</td>
      <td>1.675</td>
      <td>5.868</td>
      <td>6.145</td>
    </tr>
    <tr>
      <th>303125</th>
      <td>303125</td>
      <td>1999.0</td>
      <td>225.0</td>
      <td>12.0</td>
      <td>53.0</td>
      <td>12.779</td>
      <td>28150.0</td>
      <td>379.03</td>
      <td>0.0</td>
      <td>-4.277</td>
      <td>-0.278</td>
      <td>4.291</td>
    </tr>
    <tr>
      <th>317693</th>
      <td>317693</td>
      <td>1999.0</td>
      <td>236.0</td>
      <td>7.0</td>
      <td>52.0</td>
      <td>11.936</td>
      <td>158990.0</td>
      <td>434.28</td>
      <td>-0.0</td>
      <td>-3.302</td>
      <td>-4.838</td>
      <td>5.880</td>
    </tr>
    <tr>
      <th>334200</th>
      <td>334200</td>
      <td>1999.0</td>
      <td>248.0</td>
      <td>13.0</td>
      <td>20.0</td>
      <td>7.646</td>
      <td>60555.0</td>
      <td>385.43</td>
      <td>-0.0</td>
      <td>5.492</td>
      <td>-1.099</td>
      <td>5.606</td>
    </tr>
    <tr>
      <th>339071</th>
      <td>339071</td>
      <td>1999.0</td>
      <td>252.0</td>
      <td>3.0</td>
      <td>55.0</td>
      <td>9.553</td>
      <td>56186.0</td>
      <td>405.32</td>
      <td>0.0</td>
      <td>-4.433</td>
      <td>4.829</td>
      <td>6.600</td>
    </tr>
    <tr>
      <th>342124</th>
      <td>342124</td>
      <td>1999.0</td>
      <td>254.0</td>
      <td>10.0</td>
      <td>12.0</td>
      <td>3.376</td>
      <td>150450.0</td>
      <td>526.19</td>
      <td>0.0</td>
      <td>-3.739</td>
      <td>3.633</td>
      <td>5.237</td>
    </tr>
    <tr>
      <th>360017</th>
      <td>360017</td>
      <td>1999.0</td>
      <td>267.0</td>
      <td>16.0</td>
      <td>18.0</td>
      <td>5.580</td>
      <td>35698.0</td>
      <td>470.09</td>
      <td>0.0</td>
      <td>-6.152</td>
      <td>0.957</td>
      <td>6.252</td>
    </tr>
    <tr>
      <th>367120</th>
      <td>367120</td>
      <td>1999.0</td>
      <td>272.0</td>
      <td>22.0</td>
      <td>34.0</td>
      <td>4.614</td>
      <td>118410.0</td>
      <td>565.61</td>
      <td>-0.0</td>
      <td>5.259</td>
      <td>-4.963</td>
      <td>7.244</td>
    </tr>
    <tr>
      <th>368262</th>
      <td>368262</td>
      <td>1999.0</td>
      <td>273.0</td>
      <td>18.0</td>
      <td>52.0</td>
      <td>4.751</td>
      <td>126830.0</td>
      <td>512.57</td>
      <td>0.0</td>
      <td>2.912</td>
      <td>1.758</td>
      <td>3.647</td>
    </tr>
    <tr>
      <th>373723</th>
      <td>373723</td>
      <td>1999.0</td>
      <td>277.0</td>
      <td>19.0</td>
      <td>57.0</td>
      <td>10.976</td>
      <td>135690.0</td>
      <td>457.53</td>
      <td>0.0</td>
      <td>5.383</td>
      <td>-4.447</td>
      <td>7.013</td>
    </tr>
    <tr>
      <th>392228</th>
      <td>392228</td>
      <td>1999.0</td>
      <td>291.0</td>
      <td>12.0</td>
      <td>56.0</td>
      <td>5.557</td>
      <td>49221.0</td>
      <td>451.80</td>
      <td>0.0</td>
      <td>4.271</td>
      <td>-2.302</td>
      <td>5.072</td>
    </tr>
    <tr>
      <th>392328</th>
      <td>392328</td>
      <td>1999.0</td>
      <td>291.0</td>
      <td>14.0</td>
      <td>43.0</td>
      <td>7.250</td>
      <td>51580.0</td>
      <td>447.29</td>
      <td>-0.0</td>
      <td>-0.431</td>
      <td>-4.287</td>
      <td>4.336</td>
    </tr>
    <tr>
      <th>452061</th>
      <td>452061</td>
      <td>1999.0</td>
      <td>335.0</td>
      <td>20.0</td>
      <td>38.0</td>
      <td>10.283</td>
      <td>37365.0</td>
      <td>349.93</td>
      <td>-0.0</td>
      <td>-9.866</td>
      <td>-0.242</td>
      <td>9.874</td>
    </tr>
    <tr>
      <th>460901</th>
      <td>460901</td>
      <td>1999.0</td>
      <td>342.0</td>
      <td>9.0</td>
      <td>47.0</td>
      <td>3.476</td>
      <td>167630.0</td>
      <td>567.19</td>
      <td>0.0</td>
      <td>3.939</td>
      <td>3.456</td>
      <td>5.331</td>
    </tr>
    <tr>
      <th>471784</th>
      <td>471784</td>
      <td>1999.0</td>
      <td>350.0</td>
      <td>11.0</td>
      <td>15.0</td>
      <td>5.705</td>
      <td>90743.0</td>
      <td>445.08</td>
      <td>0.0</td>
      <td>-1.231</td>
      <td>7.127</td>
      <td>7.249</td>
    </tr>
    <tr>
      <th>472421</th>
      <td>472421</td>
      <td>1999.0</td>
      <td>350.0</td>
      <td>22.0</td>
      <td>35.0</td>
      <td>4.149</td>
      <td>-9999.9</td>
      <td>479.27</td>
      <td>0.0</td>
      <td>-2.869</td>
      <td>-6.423</td>
      <td>7.243</td>
    </tr>
    <tr>
      <th>476506</th>
      <td>476506</td>
      <td>1999.0</td>
      <td>353.0</td>
      <td>23.0</td>
      <td>12.0</td>
      <td>4.749</td>
      <td>60334.0</td>
      <td>397.50</td>
      <td>-0.0</td>
      <td>-2.888</td>
      <td>4.717</td>
      <td>5.537</td>
    </tr>
    <tr>
      <th>480536</th>
      <td>480536</td>
      <td>1999.0</td>
      <td>356.0</td>
      <td>22.0</td>
      <td>51.0</td>
      <td>-9999.900</td>
      <td>-9999.9</td>
      <td>286.49</td>
      <td>-0.0</td>
      <td>-3.160</td>
      <td>1.286</td>
      <td>3.413</td>
    </tr>
    <tr>
      <th>486231</th>
      <td>486231</td>
      <td>1999.0</td>
      <td>361.0</td>
      <td>4.0</td>
      <td>6.0</td>
      <td>10.936</td>
      <td>100700.0</td>
      <td>420.43</td>
      <td>0.0</td>
      <td>-1.493</td>
      <td>7.875</td>
      <td>8.072</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">deal_all</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
<span class="ansi-red-fg">NameError</span>                                 Traceback (most recent call last)
<span class="ansi-green-fg">&lt;ipython-input-14-f5625a714ca3&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-fg">----&gt; 1</span><span class="ansi-red-fg"> </span>deal_all<span class="ansi-blue-fg">[</span><span class="ansi-cyan-fg">0</span><span class="ansi-blue-fg">]</span><span class="ansi-blue-fg">.</span>head<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">)</span>

<span class="ansi-red-fg">NameError</span>: name &#39;deal_all&#39; is not defined</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span> <span class="n">ace0</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace0.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace3.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace6.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace9.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace12.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace15.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace18.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">save</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace21.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">tf</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/9999_process/ace3.csv&#39;</span><span class="p">)</span>
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
      <th>Unnamed: 0.1</th>
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
      <th>kp_3h</th>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">tf</span><span class="p">[</span><span class="n">tf</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
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
      <th>Unnamed: 0.1</th>
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
      <th>kp_3h</th>
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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="-9999&#52376;&#47532;&#54620;&#44144;-mean&#51060;&#45208;-sum&#54616;&#44592;">-9999&#52376;&#47532;&#54620;&#44144; mean&#51060;&#45208; sum&#54616;&#44592;<a class="anchor-link" href="#-9999&#52376;&#47532;&#54620;&#44144;-mean&#51060;&#45208;-sum&#54616;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0908_new_final_nan_csv/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#frame copy and remove redundant columns and rename label</span>



<span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_0h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_3h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_6h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_9h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">df</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_12h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_15h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_18h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;kp_21h&#39;</span><span class="p">:</span><span class="s1">&#39;label&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;copy, drop, rename done&#39;</span><span class="p">)</span>

<span class="c1">#merging the frames baesd on year and day using mean</span>
<span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>



<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">for i in range(8):</span>
<span class="sd">  </span>
<span class="sd">  merged[i][&#39;Np&#39;]=df[i][&#39;Np&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  merged[i][&#39;Vp&#39;]=df[i][&#39;Vp&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  merged[i][&#39;Tp&#39;]=df[i][&#39;Tp&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  </span>
<span class="sd">  merged[i][&#39;B_gsm_x&#39;]=df[i][&#39;B_gsm_x&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  merged[i][&#39;B_gsm_y&#39;]=df[i][&#39;B_gsm_y&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  merged[i][&#39;B_gsm_z&#39;]=df[i][&#39;B_gsm_z&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  </span>
<span class="sd">  merged[i][&#39;Bt&#39;]=df[i][&#39;Bt&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  merged[i][&#39;label&#39;]=df[i][&#39;label&#39;].groupby([df[i][&#39;year&#39;],df[i][&#39;doy&#39;]]).mean()</span>
<span class="sd">  merged[i].reset_index(inplace=True)</span>

<span class="sd">&#39;&#39;&#39;</span>



<span class="c1">#sum으로 하려면 B_gsm_x,y,z, Bt 모두 -9999처리해줘야함</span>
<span class="c1">#sum으로 하니까 null갑이 생김</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;doy&#39;</span><span class="p">]])</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>


<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;merging done&#39;</span><span class="p">)</span>
  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>copy, drop, rename done
merging done
</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[10]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>year       False
doy        False
Np         False
Vp         False
Tp         False
B_gsm_x    False
B_gsm_y    False
B_gsm_z    False
Bt         False
label      False
dtype: bool</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace0.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace3.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace6.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace9.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>

<span class="n">merged</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace12.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace15.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace18.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_9_process_merged_all/ace21.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;save done&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>save done
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([0.21409202, 0.2450566 , 0.261     , ...,        nan,        nan,
               nan]), array([1, 1, 1, ..., 1, 1, 1]))</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="B&#47448;&#46308;&#46020;--9999&#52376;&#47532;&#54644;&#50556;&#46104;&#45716;&#45936;-&#45824;&#52404;&#47196;-2011&#45380;-318&#51068;">B&#47448;&#46308;&#46020; -9999&#52376;&#47532;&#54644;&#50556;&#46104;&#45716;&#45936; &#45824;&#52404;&#47196; 2011&#45380; 318&#51068;<a class="anchor-link" href="#B&#47448;&#46308;&#46020;--9999&#52376;&#47532;&#54644;&#50556;&#46104;&#45716;&#45936;-&#45824;&#52404;&#47196;-2011&#45380;-318&#51068;">&#182;</a></h1><hr>
<h1 id="&#44536;&#45285;-&#46300;&#47213;-&#54616;&#51088;">&#44536;&#45285; &#46300;&#47213; &#54616;&#51088;<a class="anchor-link" href="#&#44536;&#45285;-&#46300;&#47213;-&#54616;&#51088;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace0.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace3.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace6.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace9.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>

<span class="n">merged</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace12.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace15.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace18.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace21.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;load done&#39;</span><span class="p">)</span>

<span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;copy done&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>load done
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp2</span><span class="p">[(</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">2013</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">336</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;hr&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">4</span><span class="p">)]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>Unnamed: 0.1</th>
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
      <th>kp_3h</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>923487</th>
      <td>923487</td>
      <td>923487</td>
      <td>2013.0</td>
      <td>336.0</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>1.025000</td>
      <td>64597.000000</td>
      <td>456.160000</td>
      <td>-8.127</td>
      <td>1.651</td>
      <td>4.823</td>
      <td>9.625</td>
      <td>0</td>
    </tr>
    <tr>
      <th>923488</th>
      <td>923488</td>
      <td>923488</td>
      <td>2013.0</td>
      <td>336.0</td>
      <td>4.0</td>
      <td>1.0</td>
      <td>0.900000</td>
      <td>66888.000000</td>
      <td>462.670000</td>
      <td>-7.990</td>
      <td>3.122</td>
      <td>4.398</td>
      <td>9.648</td>
      <td>0</td>
    </tr>
    <tr>
      <th>923489</th>
      <td>923489</td>
      <td>923489</td>
      <td>2013.0</td>
      <td>336.0</td>
      <td>4.0</td>
      <td>2.0</td>
      <td>0.856000</td>
      <td>68654.000000</td>
      <td>454.920000</td>
      <td>-8.087</td>
      <td>2.924</td>
      <td>4.255</td>
      <td>9.604</td>
      <td>0</td>
    </tr>
    <tr>
      <th>923490</th>
      <td>923490</td>
      <td>923490</td>
      <td>2013.0</td>
      <td>336.0</td>
      <td>4.0</td>
      <td>3.0</td>
      <td>0.944000</td>
      <td>81516.000000</td>
      <td>458.790000</td>
      <td>-8.222</td>
      <td>1.858</td>
      <td>4.494</td>
      <td>9.564</td>
      <td>0</td>
    </tr>
    <tr>
      <th>923491</th>
      <td>1156716</td>
      <td>923491</td>
      <td>2013.0</td>
      <td>336.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>0.915621</td>
      <td>65448.590909</td>
      <td>447.960758</td>
      <td>-8.203</td>
      <td>1.098</td>
      <td>4.693</td>
      <td>9.521</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#0~4까지는 다죽었고, 그 이후는 조금씩 살다가 마지막쯤에는 다살음</span>
<span class="n">aa</span><span class="o">=</span><span class="mi">1</span>
<span class="n">df</span><span class="p">[</span><span class="n">aa</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">&lt;-</span><span class="mi">2000</span><span class="p">)]</span>
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
      <th>year</th>
      <th>doy</th>
      <th>Np</th>
      <th>Vp</th>
      <th>Tp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4571</th>
      <td>2011.0</td>
      <td>189.0</td>
      <td>NaN</td>
      <td>349.931525</td>
      <td>36762.572650</td>
      <td>-2560.899464</td>
      <td>-2561.561274</td>
      <td>-2561.091744</td>
      <td>-2556.065381</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4700</th>
      <td>2011.0</td>
      <td>318.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>-9999.900000</td>
      <td>-9999.900000</td>
      <td>-9999.900000</td>
      <td>-9999.900000</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5449</th>
      <td>2013.0</td>
      <td>336.0</td>
      <td>0.915621</td>
      <td>447.960758</td>
      <td>65448.590909</td>
      <td>-5269.492574</td>
      <td>-5267.443000</td>
      <td>-5263.748272</td>
      <td>-5261.740462</td>
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
<h1 id="train-and-test">train and test<a class="anchor-link" href="#train-and-test">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#min max 별로임</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">col_list</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">columns</span>
  <span class="n">col_list</span><span class="o">=</span><span class="n">col_list</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;label&#39;</span><span class="p">])</span>
  <span class="k">for</span> <span class="n">bb</span> <span class="ow">in</span> <span class="n">col_list</span><span class="p">:</span>
    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">-</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">.</span><span class="n">min</span><span class="p">())</span><span class="o">/</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">.</span><span class="n">max</span><span class="p">()</span><span class="o">-</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">.</span><span class="n">min</span><span class="p">())</span>
<span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_no_nan/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
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
<span class="c1">#for i in range(8):</span>
 <span class="c1"># df[i].drop(&#39;Unnamed: 0&#39;,axis=1, inplace=True)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;copy done&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>copy done
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#log</span>
<span class="n">col_list</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">columns</span>
<span class="n">col_list</span><span class="o">=</span><span class="n">col_list</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;label&#39;</span><span class="p">])</span>
<span class="k">for</span> <span class="n">bb</span> <span class="ow">in</span> <span class="n">col_list</span><span class="p">:</span>
  <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="nb">str</span><span class="p">(</span><span class="n">bb</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_log&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">bb</span><span class="p">])</span>

    <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:5: RuntimeWarning: invalid value encountered in log
  &#34;&#34;&#34;
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
      <th>year</th>
      <th>doy</th>
      <th>Np</th>
      <th>Vp</th>
      <th>Tp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
      <th>Np_log</th>
      <th>Vp_log</th>
      <th>Tp_log</th>
      <th>B_gsm_x_log</th>
      <th>B_gsm_y_log</th>
      <th>B_gsm_z_log</th>
      <th>Bt_log</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1999.0</td>
      <td>1.0</td>
      <td>7.402352</td>
      <td>425.707640</td>
      <td>109935.283951</td>
      <td>-1.835858</td>
      <td>3.037065</td>
      <td>2.483077</td>
      <td>6.230290</td>
      <td>1</td>
      <td>2.001798</td>
      <td>6.053753</td>
      <td>11.607647</td>
      <td>NaN</td>
      <td>1.110892</td>
      <td>0.909498</td>
      <td>1.829423</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1999.0</td>
      <td>2.0</td>
      <td>5.331951</td>
      <td>406.027362</td>
      <td>61804.944785</td>
      <td>-0.601349</td>
      <td>5.326024</td>
      <td>-0.250278</td>
      <td>6.160053</td>
      <td>2</td>
      <td>1.673717</td>
      <td>6.006421</td>
      <td>11.031739</td>
      <td>NaN</td>
      <td>1.672605</td>
      <td>NaN</td>
      <td>1.818085</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1999.0</td>
      <td>3.0</td>
      <td>5.683902</td>
      <td>355.041472</td>
      <td>41349.815951</td>
      <td>-3.249450</td>
      <td>1.174722</td>
      <td>1.707473</td>
      <td>4.783450</td>
      <td>0</td>
      <td>1.737638</td>
      <td>5.872235</td>
      <td>10.629823</td>
      <td>NaN</td>
      <td>0.161031</td>
      <td>0.535015</td>
      <td>1.565162</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1999.0</td>
      <td>4.0</td>
      <td>11.659652</td>
      <td>347.978589</td>
      <td>14243.000000</td>
      <td>2.117769</td>
      <td>6.795408</td>
      <td>-0.884858</td>
      <td>7.579379</td>
      <td>3</td>
      <td>2.456134</td>
      <td>5.852141</td>
      <td>9.564021</td>
      <td>0.750363</td>
      <td>1.916247</td>
      <td>NaN</td>
      <td>2.025431</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1999.0</td>
      <td>5.0</td>
      <td>5.755743</td>
      <td>318.875644</td>
      <td>51164.669725</td>
      <td>0.106361</td>
      <td>-3.854432</td>
      <td>-5.464183</td>
      <td>6.880911</td>
      <td>2</td>
      <td>1.750198</td>
      <td>5.764801</td>
      <td>10.842805</td>
      <td>-2.240917</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.928751</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#컬럼 곱하기</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bzt&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">])</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;VNp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Np&#39;</span><span class="p">])</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;VTp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tp&#39;</span><span class="p">])</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bxy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bxz&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span>

  
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>  

<span class="n">df</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:4: RuntimeWarning: divide by zero encountered in log
  after removing the cwd from sys.path.
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
      <th>year</th>
      <th>doy</th>
      <th>Vp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
      <th>Bzt</th>
      <th>VNp</th>
      <th>VTp</th>
      <th>Bxy</th>
      <th>Bxz</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1999.0</td>
      <td>1.0</td>
      <td>71944.591118</td>
      <td>-310.260</td>
      <td>513.264</td>
      <td>419.640</td>
      <td>1052.919</td>
      <td>1</td>
      <td>2920.409710</td>
      <td>513086.987408</td>
      <td>1.204176e+06</td>
      <td>-159245.288640</td>
      <td>-130197.506400</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1999.0</td>
      <td>2.0</td>
      <td>68618.624172</td>
      <td>-101.628</td>
      <td>900.098</td>
      <td>-42.297</td>
      <td>1041.049</td>
      <td>2</td>
      <td>-293.878885</td>
      <td>466854.763305</td>
      <td>1.108989e+06</td>
      <td>-91475.159544</td>
      <td>4298.559516</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1999.0</td>
      <td>3.0</td>
      <td>60002.008834</td>
      <td>-549.157</td>
      <td>198.528</td>
      <td>288.563</td>
      <td>808.403</td>
      <td>0</td>
      <td>1931.946800</td>
      <td>412065.995078</td>
      <td>9.456150e+05</td>
      <td>-109023.040896</td>
      <td>-158466.391391</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1999.0</td>
      <td>4.0</td>
      <td>58808.381534</td>
      <td>357.903</td>
      <td>1148.424</td>
      <td>-149.541</td>
      <td>1280.915</td>
      <td>3</td>
      <td>-1070.015195</td>
      <td>446122.328133</td>
      <td>8.641256e+05</td>
      <td>411024.394872</td>
      <td>-53521.172523</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1999.0</td>
      <td>5.0</td>
      <td>53889.983865</td>
      <td>17.975</td>
      <td>-651.399</td>
      <td>-923.447</td>
      <td>1162.874</td>
      <td>2</td>
      <td>-6518.288988</td>
      <td>370768.309563</td>
      <td>8.607687e+05</td>
      <td>-11708.897025</td>
      <td>-16598.959825</td>
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
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;cate_sum&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bx&#39;</span><span class="p">]</span><span class="o">+</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;By&#39;</span><span class="p">]</span><span class="o">+</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Bz&#39;</span><span class="p">]</span><span class="o">+</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Btt&#39;</span><span class="p">]</span><span class="o">+</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Npp&#39;</span><span class="p">]</span><span class="o">+</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Tpp&#39;</span><span class="p">]</span><span class="o">+</span><span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;Vpp&#39;</span><span class="p">]</span>
<span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>year</th>
      <th>doy</th>
      <th>Np</th>
      <th>Vp</th>
      <th>Tp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
      <th>Bx</th>
      <th>By</th>
      <th>Bz</th>
      <th>Btt</th>
      <th>Npp</th>
      <th>Tpp</th>
      <th>Vpp</th>
      <th>Bxt</th>
      <th>cate_sum</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2003.0</td>
      <td>304.0</td>
      <td>1.683513</td>
      <td>1175.210086</td>
      <td>716041.396552</td>
      <td>2.236627</td>
      <td>-1.223746</td>
      <td>10.176047</td>
      <td>29.548811</td>
      <td>8</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>7.573317</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2004.0</td>
      <td>209.0</td>
      <td>3.179357</td>
      <td>971.587628</td>
      <td>851524.615385</td>
      <td>1.105905</td>
      <td>-3.710432</td>
      <td>3.226645</td>
      <td>18.587976</td>
      <td>8</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>3.232025</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2005.0</td>
      <td>19.0</td>
      <td>2.639108</td>
      <td>944.268679</td>
      <td>128122.012579</td>
      <td>-2.469722</td>
      <td>14.238438</td>
      <td>0.214249</td>
      <td>15.732337</td>
      <td>6</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>-6.805858</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2000.0</td>
      <td>198.0</td>
      <td>1.664094</td>
      <td>964.456563</td>
      <td>55538.380952</td>
      <td>24.098565</td>
      <td>35.564381</td>
      <td>12.669679</td>
      <td>46.218560</td>
      <td>8</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>92.378994</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1999.0</td>
      <td>43.0</td>
      <td>13.158856</td>
      <td>464.733459</td>
      <td>236061.687500</td>
      <td>-2.757651</td>
      <td>15.518964</td>
      <td>2.078325</td>
      <td>17.036870</td>
      <td>4</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>-7.818988</td>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#year제거</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;_sum.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">temp</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
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
      <th>year</th>
      <th>doy</th>
      <th>Np</th>
      <th>Vp</th>
      <th>Tp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4700</th>
      <td>2011.0</td>
      <td>318.0</td>
      <td>1060.613067</td>
      <td>52663.674855</td>
      <td>4.522338e+06</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
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

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(43832, 10)</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">all_merged</span><span class="p">[(</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;year&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">1999</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)]</span>
<span class="n">all_merged</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#all_merged[&#39;VNp&#39;]=all_merged[&#39;Vp&#39;]*np.log(all_merged[&#39;Np&#39;])</span>

<span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;Bxy&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">]</span>
<span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;Bxz&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">]</span>
<span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;VTp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span>
<span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;NTp&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;Np&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;Tp&#39;</span><span class="p">]</span>

<span class="c1">#all_merged.drop([&#39;Vp&#39;,&#39;Tp&#39;,&#39;Bt&#39;],axis=1,inplace=True)  </span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp1</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">][:</span><span class="mi">2000</span><span class="p">]</span>
<span class="n">temp2</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">][:</span><span class="mi">2000</span><span class="p">]</span>
<span class="n">temp3</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">2</span><span class="p">][:</span><span class="mi">2000</span><span class="p">]</span>
<span class="n">temp4</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">3</span><span class="p">][:</span><span class="mi">5000</span><span class="p">]</span>
<span class="n">temp5</span><span class="o">=</span><span class="n">all_merged</span><span class="p">[</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">3</span><span class="p">]</span>
<span class="n">all_merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">temp1</span><span class="p">,</span><span class="n">temp2</span><span class="p">,</span><span class="n">temp3</span><span class="p">,</span><span class="n">temp4</span><span class="p">,</span><span class="n">temp5</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">all_merged</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9]),
 array([2000, 2000, 2000, 5000, 3703, 1251,  372,  119,   40,   19]))</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#split data for test and train, valid</span>
<span class="n">df3</span><span class="o">=</span><span class="n">all_merged</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="n">frac</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>


<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">eight=int(df3.shape[0]*0.8)</span>
<span class="sd">x_test=df3[:365]</span>
<span class="sd">y_test=x_test[&#39;label&#39;]</span>
<span class="sd">check=x_test.copy()</span>
<span class="sd">x_test.drop([&#39;label&#39;],axis=1,inplace=True)</span>
<span class="sd">df3=df3[365:]</span>
<span class="sd">&#39;&#39;&#39;</span>

<span class="n">x_test</span><span class="o">=</span><span class="n">df3</span><span class="p">[:</span><span class="mi">365</span><span class="p">]</span>
<span class="n">y_test</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span>
<span class="n">check</span><span class="o">=</span><span class="n">x_test</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#temp1=df3[:10958]</span>
<span class="c1">#temp2=df3[11323:]</span>
<span class="c1">#df3=pd.concat([temp1,temp2],ignore_index=True)</span>
<span class="n">df3</span><span class="o">=</span><span class="n">df3</span><span class="p">[</span><span class="mi">365</span><span class="p">:]</span>

<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>

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
<pre>Training until validation scores don&#39;t improve for 100 rounds.
[100]	valid_0&#39;s l2: 1.52384
[200]	valid_0&#39;s l2: 1.07565
[300]	valid_0&#39;s l2: 0.877031
[400]	valid_0&#39;s l2: 0.784124
[500]	valid_0&#39;s l2: 0.736411
[600]	valid_0&#39;s l2: 0.709981
[700]	valid_0&#39;s l2: 0.6953
[800]	valid_0&#39;s l2: 0.686448
[900]	valid_0&#39;s l2: 0.681007
[1000]	valid_0&#39;s l2: 0.678043
[1100]	valid_0&#39;s l2: 0.676548
[1200]	valid_0&#39;s l2: 0.674887
[1300]	valid_0&#39;s l2: 0.673738
[1400]	valid_0&#39;s l2: 0.673391
[1500]	valid_0&#39;s l2: 0.672704
[1600]	valid_0&#39;s l2: 0.672038
[1700]	valid_0&#39;s l2: 0.671292
[1800]	valid_0&#39;s l2: 0.670563
[1900]	valid_0&#39;s l2: 0.67052
[2000]	valid_0&#39;s l2: 0.670235
[2100]	valid_0&#39;s l2: 0.670054
[2200]	valid_0&#39;s l2: 0.669749
[2300]	valid_0&#39;s l2: 0.669083
Early stopping, best iteration is:
[2296]	valid_0&#39;s l2: 0.669022
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

<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">model</span><span class="p">,</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/model5/no_nan_sum.pkl&#39;</span><span class="p">)</span>
 
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&#39;/content/drive/My Drive/sun_wind/model5/no_nan_sum.pkl&#39;]</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">ExtraTreesRegressor</span>
<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="n">df3</span><span class="o">=</span><span class="n">all_merged</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="n">frac</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="n">x_test</span><span class="o">=</span><span class="n">df3</span><span class="p">[:</span><span class="mi">365</span><span class="p">]</span>
<span class="n">y_test</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">]</span>
<span class="n">check</span><span class="o">=</span><span class="n">x_test</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df3</span><span class="o">=</span><span class="n">df3</span><span class="p">[</span><span class="mi">365</span><span class="p">:]</span>

<span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df3</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.066</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">)</span>
<span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
<span class="n">lgb_eval</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>

<span class="n">models</span><span class="o">=</span><span class="p">[</span>
    
    <span class="p">[</span>
        
      
        <span class="n">ExtraTreesRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">2000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">max_features</span><span class="o">=</span><span class="mi">6</span><span class="p">,</span><span class="n">max_leaf_nodes</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">criterion</span><span class="o">=</span><span class="s1">&#39;mse&#39;</span><span class="p">),</span>
        <span class="n">LGBMRegressor</span><span class="p">(</span><span class="n">boosting_type</span><span class="o">=</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span><span class="n">objective</span><span class="o">=</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span><span class="n">num_tree</span><span class="o">=</span><span class="mi">4500</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">200</span><span class="p">,</span><span class="n">max_bin</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">num_leaves</span><span class="o">=</span><span class="mi">10000</span><span class="p">,</span><span class="n">feature_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_freq</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span><span class="n">min_data_in_leaf</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.05</span><span class="p">)</span>
    <span class="p">],</span>
    
    <span class="p">[</span>
   
        <span class="n">LGBMRegressor</span><span class="p">(</span><span class="n">boosting_type</span><span class="o">=</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span><span class="n">objective</span><span class="o">=</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span><span class="n">num_tree</span><span class="o">=</span><span class="mi">4500</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">200</span><span class="p">,</span><span class="n">max_bin</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">num_leaves</span><span class="o">=</span><span class="mi">10000</span><span class="p">,</span><span class="n">feature_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_freq</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span><span class="n">min_data_in_leaf</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.05</span><span class="p">)</span>
    <span class="p">]</span>
    
<span class="p">]</span>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">pystacknet.pystacknet</span> <span class="kn">import</span> <span class="n">StackNetClassifier</span>
<span class="kn">from</span> <span class="nn">pystacknet.pystacknet</span> <span class="kn">import</span> <span class="n">StackNetRegressor</span>
<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">model=StackNetClassifier(models, metric=&quot;accuracy&quot;, folds=4,</span>
<span class="sd">	restacking=False,use_retraining=True, use_proba=True, </span>
<span class="sd">	random_state=12345,n_jobs=1, verbose=1)</span>

<span class="sd">&#39;&#39;&#39;</span>
<span class="n">model</span><span class="o">=</span><span class="n">StackNetRegressor</span><span class="p">(</span><span class="n">models</span><span class="p">,</span> <span class="n">metric</span><span class="o">=</span><span class="s2">&quot;rmse&quot;</span><span class="p">,</span> <span class="n">folds</span><span class="o">=</span><span class="mi">4</span><span class="p">,</span>
	<span class="n">restacking</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span><span class="n">use_retraining</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
	<span class="n">random_state</span><span class="o">=</span><span class="mi">12345</span><span class="p">,</span><span class="n">n_jobs</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">verbose</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="c1">#x_train.sort_index(inplace=True,axis=1)</span>
<span class="c1">#x_valid.sort_index(inplace=True,axis=1)</span>



<span class="n">model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>====================== Start of Level 0 ======================
Input Dimensionality 12 at Level 0 
2 models included in Level 0 
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/lightgbm/engine.py:118: UserWarning: Found `num_tree` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="weighted-rmse"><strong>weighted rmse</strong><a class="anchor-link" href="#weighted-rmse">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
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
<pre>weighted rmse:  0.9251444513654372
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

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>weighted rmse:  0.7948477500354606
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
RK5CYII=
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
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">data</span> <span class="o">=</span> <span class="n">all_merged</span><span class="o">.</span><span class="n">corr</span><span class="p">(</span><span class="n">method</span><span class="o">=</span><span class="s1">&#39;pearson&#39;</span><span class="p">),</span> <span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">fmt</span> <span class="o">=</span> <span class="s1">&#39;.3f&#39;</span><span class="p">,</span> <span class="n">linewidths</span><span class="o">=.</span><span class="mi">1</span><span class="p">,</span> <span class="n">cmap</span><span class="o">=</span><span class="s1">&#39;Oranges&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7fcf84828550&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
YII=
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># regression_l2했을때 데이터 프레임</span>
<span class="n">aa</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">pred</span><span class="p">)</span>

<span class="c1"># multiclass 했을때 데이터 프레임</span>
<span class="c1">#aa=pd.DataFrame(pred)</span>

<span class="n">bb</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">y_test</span><span class="p">)</span>
<span class="n">aa</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">aa</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">bb</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">bb</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">bb</span><span class="p">[</span><span class="s1">&#39;pred&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">aa</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">bb</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">20</span><span class="p">)</span>
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
      <th>label</th>
      <th>pred</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>3</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>3</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>5</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>3</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>3</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>0</td>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_absolute_error</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_squared_error</span>

<span class="c1">#prediction</span>
<span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="n">pred</span><span class="o">=</span><span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">y_pred</span><span class="p">[</span><span class="n">i</span><span class="p">])</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">y_pred</span><span class="p">))]</span>

<span class="c1">#multiclass</span>
<span class="c1">#y_pred=np.round(y_pred)</span>
<span class="c1">#print(&quot;rmae : &quot;, mean_absolute_error(y_test,pred))</span>
<span class="c1">#print(np.sqrt(mean_squared_error(y_test,pred)))</span>

<span class="c1">#regression</span>
<span class="c1">#y_pred=np.round(y_pred)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;mae : &quot;</span><span class="p">,</span> <span class="n">mean_absolute_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">y_pred</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;rmse : &quot;</span><span class="p">,</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">y_pred</span><span class="p">)))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>mae :  0.6498305695016439
rmse :  0.8244769702265333
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
63jqjJZNnL+Sw53lwVHbeSg9w3nqqaf8Lc5PO+00pk2bxlNPPYXP56OkpOSwM6Ht27ezfv16mjVr
VmZ89erV5OfnH/eZU0FBgZ19uWoyF3WqMKnqDyLyKdCXQ23TZ+N0ou0CJOI0AXwPuIKK26aPE5Hb
VDX1CPux1urlhEsr7apYHhy1nYeKWpyXdoQdPnw4AD///DM33ngjmzdv9i+XlZVFUlJShS2/P/zw
w+NuBV6T7cTrunBvrV56Oa+0MA0HmgKfqupXACIyE+hBBYXpaFlrdUe4tNKuiuXBUdt5qKzF+fbt
2/3LREdHlylKpu6qa58xgVOQeolIJyBKVVe641puufLvjTF11LZt2+jZsycpKSmcf/75pKenH/F2
7+XLl9OqVStef/11br75ZpKSkvzzfvWrX/Hb3/6WBQsW0KpVK95///1Kt2NCo86dMalqgXt33nTK
3vTQRUTa4FzKuwr3UlwlikSkoaoWBTFUY0wNqazFeaCCggL/9Pnnn8/WrVsrXO7jjz+u0dhMzauL
Z0zgFKSOlC1My4EpwOfAFuDNCtYrNRVYKyKvBC1CY4wxx6TOnTEBqOpcQMoN71HVan2VW1XHAmNr
PDBjjDHHra6eMRljjKmn6uQZU3mq6gN85cdFZBlwQrnh61R1XS2EZYwx5hjUi8JUGVXtGuoYjDHG
HB27lGeMMcZTjrowicjJIpISjGCMMcaYahUmEfGJyC9E5BQgG3hORJ4IbmjGGGPCUXXPmE5S1T04
z597yf3s5uLghWWMMSZcVbcwRYpILDAIeCuI8RhjjAlz1S1MDwDvA/9T1eUi0hbYFLywjDHGhKtq
FSZVfV1VU0q7xKrqV6p6ZXBDM8bUR/v376dLly507NiRpKQk7rvvPgAGDx7MOeecQ4cOHbjhhhso
KnIeZamqjBw5kvj4eFJSUsjOzgacnkrdu3cnKSmJlJQUZs2aFbJjMjWrujc/nC0iC0TkM/d9ioj8
JbihHRsRURGZFPD+TyIyIYQhGWMCnHDCCSxcuJA1a9awevVq3nvvPZYuXcrgwYP54osvWLduHYWF
hUybNg2Ad999l02bNrFp0yamTp3KiBEjAIiKiuKll15i/fr1vPfee4wePZrdu3eH8tBMDanuF2yf
A8YA/wBQ1bUi8irwYLACOw4/A1eIyCOq+v3xbqywqIS4cW/XQFh1253JxQy1PFgeXMeah5zM/ogI
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
z7b+HQAAAABJRU5ErkJggg==
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">bb</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">feature_importance</span><span class="p">()</span>
<span class="n">bb</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">bb</span><span class="p">)</span>
<span class="n">cc</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">x_test</span><span class="o">.</span><span class="n">columns</span><span class="p">)</span>
<span class="n">bb</span><span class="p">[</span><span class="s1">&#39;columns&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">cc</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">bb</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="n">ascending</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
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
      <th>columns</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>7</th>
      <td>2258</td>
      <td>VNp</td>
    </tr>
    <tr>
      <th>0</th>
      <td>2162</td>
      <td>doy</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1870</td>
      <td>B_gsm_z</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1822</td>
      <td>Bt</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1803</td>
      <td>Vp</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1443</td>
      <td>VTp</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1433</td>
      <td>Bzt</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1320</td>
      <td>B_gsm_y</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1127</td>
      <td>Bxy</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1005</td>
      <td>B_gsm_x</td>
    </tr>
    <tr>
      <th>10</th>
      <td>983</td>
      <td>Bxz</td>
    </tr>
    <tr>
      <th>11</th>
      <td>930</td>
      <td>BxT</td>
    </tr>
    <tr>
      <th>12</th>
      <td>654</td>
      <td>BxV</td>
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
<h1 id="plotting">plotting<a class="anchor-link" href="#plotting">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#라벨부터 보자규</span>
<span class="n">vari</span><span class="o">=</span><span class="s1">&#39;Np&#39;</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">vari</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#log 취해보기</span>
<span class="n">cur</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="c1">#cur[vari]=np.log(df3[vari])</span>

<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">cur</span><span class="p">[</span><span class="n">vari</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7fb4e2c2b630&gt;</pre>
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
<h1 id="&#46972;&#48296;&#44284;-&#54532;&#47112;&#46357;&#46300;-&#52264;&#51060;-&#48372;&#44592;">&#46972;&#48296;&#44284; &#54532;&#47112;&#46357;&#46300; &#52264;&#51060; &#48372;&#44592;<a class="anchor-link" href="#&#46972;&#48296;&#44284;-&#54532;&#47112;&#46357;&#46300;-&#52264;&#51060;-&#48372;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#weight rmse from 개최자</span>
<span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_valid</span><span class="p">)</span>

<span class="c1">#multiclass</span>
<span class="c1">#pred=[np.argmax(y_pred[i]) for i in range(len(y_pred))]</span>

<span class="c1">#regression</span>
<span class="n">pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">round</span><span class="p">(</span><span class="n">y_pred</span><span class="p">)</span>

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
<pre>weighted rmse:  0.8907235428302466
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># regression_l2했을때 데이터 프레임</span>
<span class="n">aa</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">pred</span><span class="p">)</span>

<span class="c1"># multiclass 했을때 데이터 프레임</span>
<span class="c1">#aa=pd.DataFrame(pred)</span>

<span class="n">bb</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">y_valid</span><span class="p">)</span>
<span class="n">aa</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">aa</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">bb</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">bb</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">bb</span><span class="p">[</span><span class="s1">&#39;pred&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">aa</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">bb</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">10</span><span class="p">)</span>
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
      <th>label</th>
      <th>pred</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2</td>
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
QmCC
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
<h1 id="&#47784;&#46304;-csv&#45796;-&#54633;&#52824;&#44592;">&#47784;&#46304; csv&#45796; &#54633;&#52824;&#44592;<a class="anchor-link" href="#&#47784;&#46304;-csv&#45796;-&#54633;&#52824;&#44592;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>Vp</th>
      <th>Tp</th>
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
      <td>1.0</td>
      <td>6.977939</td>
      <td>416.138466</td>
      <td>102955.228395</td>
      <td>-3.020280</td>
      <td>1.972732</td>
      <td>2.324583</td>
      <td>6.576893</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.0</td>
      <td>6.176919</td>
      <td>399.755155</td>
      <td>76055.310559</td>
      <td>-1.810173</td>
      <td>3.969613</td>
      <td>-0.375524</td>
      <td>5.900768</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3.0</td>
      <td>5.401828</td>
      <td>359.163333</td>
      <td>46367.790123</td>
      <td>-3.237863</td>
      <td>2.426060</td>
      <td>1.541935</td>
      <td>5.022179</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.0</td>
      <td>10.342584</td>
      <td>355.505404</td>
      <td>18423.246914</td>
      <td>0.373976</td>
      <td>6.518536</td>
      <td>-4.317833</td>
      <td>8.014887</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>4.904797</td>
      <td>323.523395</td>
      <td>49548.283784</td>
      <td>-1.600262</td>
      <td>-1.695738</td>
      <td>-6.380881</td>
      <td>7.057613</td>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
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

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(43832, 10)</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aa</span><span class="o">=</span><span class="mi">2</span>
<span class="n">df</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Nan&#44050;-&#50696;&#52769;&#54616;&#45716;-&#47784;&#45944;-&#47564;&#46308;&#44592;">Nan&#44050; &#50696;&#52769;&#54616;&#45716; &#47784;&#45944; &#47564;&#46308;&#44592;<a class="anchor-link" href="#Nan&#44050;-&#50696;&#52769;&#54616;&#45716;-&#47784;&#45944;-&#47564;&#46308;&#44592;">&#182;</a></h1><hr>
<h1 id="0&#44050;&#46308;&#46020;-&#50696;&#52769;&#54644;&#50556;&#54632;">0&#44050;&#46308;&#46020; &#50696;&#52769;&#54644;&#50556;&#54632;<a class="anchor-link" href="#0&#44050;&#46308;&#46020;-&#50696;&#52769;&#54644;&#50556;&#54632;">&#182;</a></h1><hr>
<h1 id="no_nan&#51060;-0&#52376;&#47532;&#46020;-&#54644;&#51468;">no_nan&#51060; 0&#52376;&#47532;&#46020; &#54644;&#51468;<a class="anchor-link" href="#no_nan&#51060;-0&#52376;&#47532;&#46020;-&#54644;&#51468;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Vp</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Tp</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">Np</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="n">temp</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Vp-&gt;Tp-&gt;Np 순서로 NaN값에 예측값 넣기</span>
<span class="c1"># sum한 데이터프레임에는 NaN이 없고 0으로 대체되어있는듯.</span>
<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="k">for</span> <span class="n">bb</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">]:</span>
  <span class="k">for</span> <span class="n">aa</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>



   <span class="c1"># x_test=merged[aa][merged[aa][bb].isnull()==True]</span>
    <span class="n">x_test</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
    <span class="c1">#x_test=pd.concat([x_test,zero],ignore_index=True)</span>
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

    <span class="c1">#temp1=merged[aa][merged[aa][bb].isnull()==False]</span>
    <span class="n">df3</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">][</span><span class="n">bb</span><span class="p">]</span><span class="o">!=</span><span class="mi">0</span><span class="p">]</span>
    <span class="c1">#df3=pd.concat([temp1,temp2],ignore_index=True)</span>



   
    <span class="k">if</span> <span class="n">bb</span><span class="o">==</span><span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="n">bb</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df3</span><span class="p">[</span><span class="n">bb</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.066</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">bb</span><span class="o">==</span><span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="n">bb</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df3</span><span class="p">[</span><span class="n">bb</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.066</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">)</span>
    <span class="k">else</span> <span class="p">:</span>
      <span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="n">bb</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df3</span><span class="p">[</span><span class="n">bb</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.066</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">)</span>
    

    <span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
    <span class="n">lgb_eval</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>


    <span class="c1">#configure parameters</span>
    <span class="n">params</span><span class="o">=</span><span class="p">{</span>
        <span class="s1">&#39;boosting_type&#39;</span> <span class="p">:</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
        <span class="c1">#&#39;objective&#39;:&#39;multiclass&#39;,</span>
        <span class="s1">&#39;objective&#39;</span><span class="p">:</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span>
        <span class="s1">&#39;num_tree&#39;</span><span class="p">:</span><span class="mi">20000</span><span class="p">,</span>
        <span class="c1">#&quot;num_class&quot; : 10,</span>
        <span class="s1">&#39;max_bin&#39;</span> <span class="p">:</span> <span class="mi">10000</span><span class="p">,</span>
        <span class="s1">&#39;max_depth&#39;</span> <span class="p">:</span><span class="mi">50</span><span class="p">,</span>
        <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">100</span><span class="p">,</span>
        <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.08</span><span class="p">,</span>
        <span class="s1">&#39;feature_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
        <span class="s1">&#39;bagging_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
        <span class="s1">&#39;bagging_freq&#39;</span><span class="p">:</span> <span class="mi">5</span><span class="p">,</span>    
        <span class="s1">&#39;num_leavs&#39;</span><span class="p">:</span> <span class="mi">5000</span><span class="p">,</span>
        <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:</span><span class="s1">&#39;doy&#39;</span>
    <span class="p">}</span>

    <span class="c1">#model train</span>
    <span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span><span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_eval</span><span class="p">,</span><span class="n">verbose_eval</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span><span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">30</span><span class="p">)</span>
    <span class="c1">#model save</span>
    <span class="k">if</span> <span class="n">bb</span><span class="o">==</span><span class="s1">&#39;Vp&#39;</span><span class="p">:</span>
      <span class="n">Vp</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
    <span class="k">elif</span> <span class="n">bb</span><span class="o">==</span><span class="s1">&#39;Tp&#39;</span><span class="p">:</span>
      <span class="n">Tp</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
    <span class="k">else</span> <span class="p">:</span>
      <span class="n">Np</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">=</span><span class="n">model</span>
    

    <span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
    <span class="n">check</span><span class="p">[</span><span class="n">bb</span><span class="p">]</span><span class="o">=</span><span class="n">y_pred</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">df3</span><span class="p">,</span><span class="n">check</span><span class="p">],</span><span class="n">ignore_index</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="n">temp</span><span class="p">[</span><span class="n">aa</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
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
[100]	valid_0&#39;s l2: 1.66542e+08
Early stopping, best iteration is:
[91]	valid_0&#39;s l2: 1.66084e+08
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 1.58161e+08
Early stopping, best iteration is:
[90]	valid_0&#39;s l2: 1.57613e+08
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 1.47248e+08
Early stopping, best iteration is:
[128]	valid_0&#39;s l2: 1.4682e+08
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 1.60763e+08
Early stopping, best iteration is:
[103]	valid_0&#39;s l2: 1.60053e+08
Training until validation scores don&#39;t improve for 30 rounds.
Early stopping, best iteration is:
[52]	valid_0&#39;s l2: 1.75567e+08
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 1.87678e+08
Early stopping, best iteration is:
[154]	valid_0&#39;s l2: 1.84208e+08
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 1.57732e+08
Early stopping, best iteration is:
[107]	valid_0&#39;s l2: 1.56907e+08
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 5.01677e+13
Early stopping, best iteration is:
[90]	valid_0&#39;s l2: 4.99938e+13
Training until validation scores don&#39;t improve for 30 rounds.
Early stopping, best iteration is:
[45]	valid_0&#39;s l2: 5.0955e+13
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 4.87248e+13
Early stopping, best iteration is:
[160]	valid_0&#39;s l2: 4.77864e+13
Training until validation scores don&#39;t improve for 30 rounds.
Early stopping, best iteration is:
[27]	valid_0&#39;s l2: 5.11218e+13
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 7.77725e+13
Early stopping, best iteration is:
[120]	valid_0&#39;s l2: 7.70098e+13
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 4.03787e+13
[200]	valid_0&#39;s l2: 3.90303e+13
Early stopping, best iteration is:
[178]	valid_0&#39;s l2: 3.86033e+13
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 6.57575e+13
Early stopping, best iteration is:
[70]	valid_0&#39;s l2: 6.49511e+13
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 198256
Early stopping, best iteration is:
[74]	valid_0&#39;s l2: 195398
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 508094
[200]	valid_0&#39;s l2: 479380
Early stopping, best iteration is:
[176]	valid_0&#39;s l2: 474480
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 277402
Early stopping, best iteration is:
[108]	valid_0&#39;s l2: 276094
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 234696
Early stopping, best iteration is:
[138]	valid_0&#39;s l2: 226310
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 247899
Early stopping, best iteration is:
[124]	valid_0&#39;s l2: 244187
Training until validation scores don&#39;t improve for 30 rounds.
[100]	valid_0&#39;s l2: 204475
Early stopping, best iteration is:
[97]	valid_0&#39;s l2: 204040
Training until validation scores don&#39;t improve for 30 rounds.
Early stopping, best iteration is:
[38]	valid_0&#39;s l2: 192445
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#no_nan_dataframe save</span>
<span class="n">temp</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace0_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace3_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace6_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace9_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>

<span class="n">temp</span><span class="p">[</span><span class="mi">4</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace12_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="p">[</span><span class="mi">5</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace15_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="p">[</span><span class="mi">6</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace18_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="p">[</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_train/ace21_sum.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#model save</span>

<span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>

<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp0.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp1.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp2.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">3</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp3.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">4</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp4.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">5</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp5.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">6</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp6.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Vp</span><span class="p">[</span><span class="mi">7</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Vp7.pkl&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Vp done&#39;</span><span class="p">)</span>

<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp0.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp1.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp2.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">3</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp3.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">4</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp4.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">5</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp5.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">6</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp6.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Tp</span><span class="p">[</span><span class="mi">7</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Tp7.pkl&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Tp done&#39;</span><span class="p">)</span>

<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np0.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np1.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np2.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">3</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np3.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">4</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np4.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">5</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np5.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">6</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np6.pkl&#39;</span><span class="p">)</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">Np</span><span class="p">[</span><span class="mi">7</span><span class="p">],</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/0907_no_nan_sum_model/Np7.pkl&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Np done&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Vp done
Tp done
Np done
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="stacknet-&#49444;&#52824;">stacknet &#49444;&#52824;<a class="anchor-link" href="#stacknet-&#49444;&#52824;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">!</span>git clone https://github.com/h2oai/pystacknet
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Cloning into &#39;pystacknet&#39;...
remote: Enumerating objects: 42, done.
remote: Total 42 (delta 0), reused 0 (delta 0), pack-reused 42
Unpacking objects: 100% (42/42), done.
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ls</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre><span class="ansi-blue-intense-fg ansi-bold">drive</span>/  <span class="ansi-blue-intense-fg ansi-bold">pystacknet</span>/  <span class="ansi-blue-intense-fg ansi-bold">sample_data</span>/
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cd</span> <span class="s1">&#39;pystacknet&#39;</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>/content/pystacknet
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">!</span>python setup.py install
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>warning: pypandoc module not found, could not convert Markdown to RST
running install
running bdist_egg
running egg_info
creating pystacknet.egg-info
writing pystacknet.egg-info/PKG-INFO
writing dependency_links to pystacknet.egg-info/dependency_links.txt
writing requirements to pystacknet.egg-info/requires.txt
writing top-level names to pystacknet.egg-info/top_level.txt
writing manifest file &#39;pystacknet.egg-info/SOURCES.txt&#39;
writing manifest file &#39;pystacknet.egg-info/SOURCES.txt&#39;
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_py
creating build
creating build/lib
creating build/lib/pystacknet
copying pystacknet/metrics.py -&gt; build/lib/pystacknet
copying pystacknet/pystacknet.py -&gt; build/lib/pystacknet
copying pystacknet/__init__.py -&gt; build/lib/pystacknet
creating build/lib/pystacknet/test
copying pystacknet/test/test_amazon.py -&gt; build/lib/pystacknet/test
copying pystacknet/test/test_pystacknet.py -&gt; build/lib/pystacknet/test
copying pystacknet/test/__init__.py -&gt; build/lib/pystacknet/test
creating build/bdist.linux-x86_64
creating build/bdist.linux-x86_64/egg
creating build/bdist.linux-x86_64/egg/pystacknet
creating build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/test/test_amazon.py -&gt; build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/test/test_pystacknet.py -&gt; build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/test/__init__.py -&gt; build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/metrics.py -&gt; build/bdist.linux-x86_64/egg/pystacknet
copying build/lib/pystacknet/pystacknet.py -&gt; build/bdist.linux-x86_64/egg/pystacknet
copying build/lib/pystacknet/__init__.py -&gt; build/bdist.linux-x86_64/egg/pystacknet
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/test/test_amazon.py to test_amazon.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/test/test_pystacknet.py to test_pystacknet.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/test/__init__.py to __init__.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/metrics.py to metrics.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/pystacknet.py to pystacknet.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/__init__.py to __init__.cpython-36.pyc
creating build/bdist.linux-x86_64/egg/EGG-INFO
copying pystacknet.egg-info/PKG-INFO -&gt; build/bdist.linux-x86_64/egg/EGG-INFO
copying pystacknet.egg-info/SOURCES.txt -&gt; build/bdist.linux-x86_64/egg/EGG-INFO
copying pystacknet.egg-info/dependency_links.txt -&gt; build/bdist.linux-x86_64/egg/EGG-INFO
copying pystacknet.egg-info/requires.txt -&gt; build/bdist.linux-x86_64/egg/EGG-INFO
copying pystacknet.egg-info/top_level.txt -&gt; build/bdist.linux-x86_64/egg/EGG-INFO
zip_safe flag not set; analyzing archive contents...
creating dist
creating &#39;dist/pystacknet-0.0.1-py3.6.egg&#39; and adding &#39;build/bdist.linux-x86_64/egg&#39; to it
removing &#39;build/bdist.linux-x86_64/egg&#39; (and everything under it)
Processing pystacknet-0.0.1-py3.6.egg
Copying pystacknet-0.0.1-py3.6.egg to /usr/local/lib/python3.6/dist-packages
Adding pystacknet 0.0.1 to easy-install.pth file

Installed /usr/local/lib/python3.6/dist-packages/pystacknet-0.0.1-py3.6.egg
Processing dependencies for pystacknet==0.0.1
Searching for scikit-learn==0.21.3
Best match: scikit-learn 0.21.3
Adding scikit-learn 0.21.3 to easy-install.pth file

Using /usr/local/lib/python3.6/dist-packages
Searching for scipy==1.3.1
Best match: scipy 1.3.1
Adding scipy 1.3.1 to easy-install.pth file

Using /usr/local/lib/python3.6/dist-packages
Searching for numpy==1.16.5
Best match: numpy 1.16.5
Adding numpy 1.16.5 to easy-install.pth file
Installing f2py script to /usr/local/bin
Installing f2py3 script to /usr/local/bin
Installing f2py3.6 script to /usr/local/bin

Using /usr/local/lib/python3.6/dist-packages
Searching for joblib==0.13.2
Best match: joblib 0.13.2
Adding joblib 0.13.2 to easy-install.pth file

Using /usr/local/lib/python3.6/dist-packages
Finished processing dependencies for pystacknet==0.0.1
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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="stacking-model&#49324;&#50857;">stacking model&#49324;&#50857;<a class="anchor-link" href="#stacking-model&#49324;&#50857;">&#182;</a></h1><hr>
<h1 id="1.13">1.13<a class="anchor-link" href="#1.13">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span>  
  
<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">merged=[i for i in range(8)]</span>
<span class="sd">for i in range(8):</span>
<span class="sd">  merged[i]=pd.read_csv(&#39;/content/drive/My Drive/sun_wind/merge_after_9999/ace&#39;+str(i*3)+&#39;.csv&#39;)</span>
<span class="sd">  merged[i].drop(&#39;Unnamed: 0&#39;,axis=1,inplace=True)</span>
<span class="sd">  </span>
<span class="sd">&#39;&#39;&#39;</span>  
<span class="n">merged</span><span class="o">=</span><span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/0905_no_nan/ace&#39;</span><span class="o">+</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">*</span><span class="mi">3</span><span class="p">)</span><span class="o">+</span><span class="s1">&#39;.csv&#39;</span><span class="p">)</span>
  <span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">df</span><span class="o">=</span><span class="p">[</span><span class="n">merged</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">)]</span>
<span class="c1">#for i in range(8):</span>
 <span class="c1"># df[i].drop(&#39;Unnamed: 0&#39;,axis=1, inplace=True)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;copy done&#39;</span><span class="p">)</span>

<span class="c1">#year제거</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">8</span><span class="p">):</span>
  <span class="n">df</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;year&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
  
  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>copy done
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="s1">&#39;Bt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">==</span><span class="kc">True</span><span class="p">]</span>
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
      <th>Vp</th>
      <th>Tp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
      <th>label</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4571</th>
      <td>189.0</td>
      <td>2.209312</td>
      <td>520.16204</td>
      <td>116378.911675</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#NaN 값 처리</span>
<span class="n">df</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="mi">4571</span><span class="p">],</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="n">df3</span><span class="o">=</span><span class="n">df</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>


<span class="n">x_train</span><span class="p">,</span><span class="n">x_valid</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_valid</span><span class="o">=</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">df3</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span><span class="n">df3</span><span class="p">[</span><span class="s1">&#39;label&#39;</span><span class="p">],</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.066</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#classfier</span>
<span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">RandomForestClassifier</span><span class="p">,</span> <span class="n">ExtraTreesClassifier</span><span class="p">,</span> <span class="n">GradientBoostingClassifier</span><span class="p">,</span> <span class="n">AdaBoostClassifier</span>
<span class="kn">from</span> <span class="nn">sklearn.linear_model</span> <span class="kn">import</span> <span class="n">LogisticRegression</span>
<span class="kn">from</span> <span class="nn">sklearn.tree</span> <span class="kn">import</span> <span class="n">DecisionTreeClassifier</span>
<span class="kn">from</span> <span class="nn">lightgbm</span> <span class="kn">import</span> <span class="n">LGBMClassifier</span>
<span class="n">models</span><span class="o">=</span><span class="p">[</span> 
        <span class="c1">######## First level ########</span>
        <span class="p">[</span><span class="n">RandomForestClassifier</span> <span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span> <span class="n">criterion</span><span class="o">=</span><span class="s2">&quot;entropy&quot;</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span> <span class="n">max_features</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>
         <span class="n">ExtraTreesClassifier</span> <span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span> <span class="n">criterion</span><span class="o">=</span><span class="s2">&quot;entropy&quot;</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span> <span class="n">max_features</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>
         <span class="n">GradientBoostingClassifier</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span> <span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span> <span class="n">max_features</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>
         <span class="n">LGBMClassifier</span><span class="p">(</span><span class="n">boosting_type</span><span class="o">=</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span><span class="n">objective</span><span class="o">=</span><span class="s1">&#39;multiclass&#39;</span><span class="p">,</span><span class="n">num_class</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span><span class="n">max_bin</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.05</span><span class="p">,</span><span class="n">bagging_freq</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span><span class="n">num_leaves</span><span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">categorical_features</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">],</span><span class="n">num_tree</span><span class="o">=</span><span class="mi">2000</span><span class="p">),</span>
         
         <span class="p">],</span>
        <span class="c1">######## Second level ########</span>
        <span class="p">[</span><span class="n">RandomForestClassifier</span> <span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">2000</span><span class="p">,</span> <span class="n">criterion</span><span class="o">=</span><span class="s2">&quot;entropy&quot;</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span> <span class="n">max_features</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>
        <span class="n">LGBMClassifier</span><span class="p">(</span><span class="n">boosting_type</span><span class="o">=</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span><span class="n">objective</span><span class="o">=</span><span class="s1">&#39;multiclass&#39;</span><span class="p">,</span><span class="n">num_class</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span><span class="n">max_bin</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.05</span><span class="p">,</span><span class="n">bagging_freq</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span><span class="n">num_leaves</span><span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">categorical_features</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">],</span><span class="n">num_tree</span><span class="o">=</span><span class="mi">2000</span><span class="p">)],</span>
       
    
     
        <span class="p">[</span>
           <span class="n">RandomForestClassifier</span> <span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span> <span class="n">criterion</span><span class="o">=</span><span class="s2">&quot;entropy&quot;</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span> <span class="n">max_features</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
            
        <span class="p">],</span>

        <span class="p">]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">AdaBoostRegressor</span><span class="p">,</span> <span class="n">RandomForestRegressor</span><span class="p">,</span> <span class="n">ExtraTreesRegressor</span>
<span class="kn">from</span> <span class="nn">sklearn.neighbors</span> <span class="kn">import</span> <span class="n">KNeighborsRegressor</span>
<span class="kn">from</span> <span class="nn">xgboost</span> <span class="kn">import</span> <span class="n">XGBRegressor</span>
<span class="kn">from</span> <span class="nn">lightgbm</span> <span class="kn">import</span> <span class="n">LGBMRegressor</span>
<span class="n">models</span><span class="o">=</span><span class="p">[</span>
    
    <span class="p">[</span>
        
        <span class="n">RandomForestRegressor</span><span class="p">(</span><span class="n">n_estimators</span> <span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">min_samples_leaf</span> <span class="o">=</span><span class="mi">20</span><span class="p">),</span>
        
        <span class="n">XGBRegressor</span><span class="p">(</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.05</span><span class="p">,</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">20</span><span class="p">,),</span>
        <span class="n">ExtraTreesRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">max_features</span><span class="o">=</span><span class="mi">6</span><span class="p">,</span><span class="n">max_leaf_nodes</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">criterion</span><span class="o">=</span><span class="s1">&#39;mse&#39;</span><span class="p">),</span>
        <span class="n">LGBMRegressor</span><span class="p">(</span><span class="n">boosting_type</span><span class="o">=</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span><span class="n">objective</span><span class="o">=</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span><span class="n">num_tree</span><span class="o">=</span><span class="mi">10000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">max_bin</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">num_leaves</span><span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">feature_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_freq</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">min_data_in_leaf</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
    <span class="p">],</span>
    
    <span class="p">[</span>
        <span class="n">RandomForestRegressor</span><span class="p">(</span><span class="n">n_estimators</span> <span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">min_samples_leaf</span> <span class="o">=</span><span class="mi">20</span><span class="p">),</span>
        <span class="n">LGBMRegressor</span><span class="p">(</span><span class="n">boosting_type</span><span class="o">=</span><span class="s1">&#39;gbdt&#39;</span><span class="p">,</span><span class="n">objective</span><span class="o">=</span><span class="s1">&#39;regression_l2&#39;</span><span class="p">,</span><span class="n">num_tree</span><span class="o">=</span><span class="mi">10000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">max_bin</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">num_leaves</span><span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">feature_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_freq</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">min_data_in_leaf</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
    <span class="p">],</span>
    
    <span class="p">[</span>
        
        <span class="n">ExtraTreesRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">5000</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">max_leaf_nodes</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">criterion</span><span class="o">=</span><span class="s1">&#39;mse&#39;</span><span class="p">,)</span>
    <span class="p">]</span>
    
<span class="p">]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">pystacknet.pystacknet</span> <span class="kn">import</span> <span class="n">StackNetClassifier</span>
<span class="kn">from</span> <span class="nn">pystacknet.pystacknet</span> <span class="kn">import</span> <span class="n">StackNetRegressor</span>
<span class="sd">&#39;&#39;&#39;</span>
<span class="sd">model=StackNetClassifier(models, metric=&quot;accuracy&quot;, folds=4,</span>
<span class="sd">	restacking=False,use_retraining=True, use_proba=True, </span>
<span class="sd">	random_state=12345,n_jobs=1, verbose=1)</span>

<span class="sd">&#39;&#39;&#39;</span>
<span class="n">model</span><span class="o">=</span><span class="n">StackNetRegressor</span><span class="p">(</span><span class="n">models</span><span class="p">,</span> <span class="n">metric</span><span class="o">=</span><span class="s2">&quot;rmse&quot;</span><span class="p">,</span> <span class="n">folds</span><span class="o">=</span><span class="mi">4</span><span class="p">,</span>
	<span class="n">restacking</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span><span class="n">use_retraining</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
	<span class="n">random_state</span><span class="o">=</span><span class="mi">12345</span><span class="p">,</span><span class="n">n_jobs</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">verbose</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="n">x_train</span><span class="o">.</span><span class="n">sort_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">x_valid</span><span class="o">.</span><span class="n">sort_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="n">model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>====================== Start of Level 0 ======================
Input Dimensionality 8 at Level 0 
4 models included in Level 0 
[15:18:48] WARNING: /workspace/src/objective/regression_obj.cu:152: reg:linear is now deprecated in favor of reg:squarederror.
</pre>
</div>
</div>

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
<pre>Fold 1/4 , model 0 , rmse===0.819210 
Fold 1/4 , model 1 , rmse===0.863055 
Fold 1/4 , model 2 , rmse===0.796097 
Fold 1/4 , model 3 , rmse===0.846716 
=========== end of fold 1 in level 0 ===========
[15:23:03] WARNING: /workspace/src/objective/regression_obj.cu:152: reg:linear is now deprecated in favor of reg:squarederror.
</pre>
</div>
</div>

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
<pre>Fold 2/4 , model 0 , rmse===0.876106 
Fold 2/4 , model 1 , rmse===0.878917 
Fold 2/4 , model 2 , rmse===0.836998 
Fold 2/4 , model 3 , rmse===0.862660 
=========== end of fold 2 in level 0 ===========
[15:27:18] WARNING: /workspace/src/objective/regression_obj.cu:152: reg:linear is now deprecated in favor of reg:squarederror.
</pre>
</div>
</div>

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
<pre>Fold 3/4 , model 0 , rmse===0.840449 
Fold 3/4 , model 1 , rmse===0.878736 
Fold 3/4 , model 2 , rmse===0.818890 
Fold 3/4 , model 3 , rmse===0.851740 
=========== end of fold 3 in level 0 ===========
[15:31:34] WARNING: /workspace/src/objective/regression_obj.cu:152: reg:linear is now deprecated in favor of reg:squarederror.
</pre>
</div>
</div>

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
<pre>Fold 4/4 , model 0 , rmse===0.893561 
Fold 4/4 , model 1 , rmse===0.893381 
Fold 4/4 , model 2 , rmse===0.859943 
Fold 4/4 , model 3 , rmse===0.890935 
=========== end of fold 4 in level 0 ===========
[15:36:15] WARNING: /workspace/src/objective/regression_obj.cu:152: reg:linear is now deprecated in favor of reg:squarederror.
</pre>
</div>
</div>

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
<pre>Output dimensionality of level 0 is 4 
====================== End of Level 0 ======================
 level 0 lasted 1340.508096 seconds 
====================== Start of Level 1 ======================
Input Dimensionality 4 at Level 1 
2 models included in Level 1 
</pre>
</div>
</div>

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
<pre>Fold 1/4 , model 0 , rmse===0.802687 
Fold 1/4 , model 1 , rmse===1.004032 
=========== end of fold 1 in level 1 ===========
</pre>
</div>
</div>

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
<pre>Fold 2/4 , model 0 , rmse===0.839593 
Fold 2/4 , model 1 , rmse===0.991961 
=========== end of fold 2 in level 1 ===========
</pre>
</div>
</div>

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
<pre>Fold 3/4 , model 0 , rmse===0.838982 
Fold 3/4 , model 1 , rmse===1.023180 
=========== end of fold 3 in level 1 ===========
</pre>
</div>
</div>

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
<pre>Fold 4/4 , model 0 , rmse===0.880530 
Fold 4/4 , model 1 , rmse===1.059676 
=========== end of fold 4 in level 1 ===========
</pre>
</div>
</div>

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
<pre>Output dimensionality of level 1 is 2 
====================== End of Level 1 ======================
 level 1 lasted 661.942844 seconds 
====================== Start of Level 2 ======================
Input Dimensionality 2 at Level 2 
1 models included in Level 2 
Fold 1/4 , model 0 , rmse===0.843129 
=========== end of fold 1 in level 2 ===========
Fold 2/4 , model 0 , rmse===0.871041 
=========== end of fold 2 in level 2 ===========
Fold 3/4 , model 0 , rmse===0.859094 
=========== end of fold 3 in level 2 ===========
Fold 4/4 , model 0 , rmse===0.893849 
=========== end of fold 4 in level 2 ===========
Output dimensionality of level 2 is 1 
====================== End of Level 2 ======================
 level 2 lasted 67.948534 seconds 
====================== End of fit ======================
 fit() lasted 2070.402297 seconds 
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

<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">model</span><span class="p">,</span> <span class="s1">&#39;/content/drive/My Drive/sun_wind/model4/stacking_regression2.pkl&#39;</span><span class="p">)</span>
 
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&#39;/content/drive/My Drive/sun_wind/model4/stacking_regression2.pkl&#39;]</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">=</span> <span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/sun_wind/model4/stacking_regression.pkl&#39;</span><span class="p">)</span>  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[12:49:57] WARNING: /workspace/src/objective/regression_obj.cu:152: reg:linear is now deprecated in favor of reg:squarederror.
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_valid</span><span class="o">=</span><span class="n">x_valid</span><span class="o">.</span><span class="n">as_matrix</span><span class="p">()</span>
<span class="n">x_valid</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:1: FutureWarning: Method .as_matrix will be removed in a future version. Use .values instead.
  &#34;&#34;&#34;Entry point for launching an IPython kernel.
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([ 5.36271006e+00, -1.90269822e+00,  5.47197633e+00,  8.53824260e+00,
        6.33355118e+00,  5.50984646e+04,  3.23997516e+02,  3.35000000e+02])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_valid</span><span class="p">)</span>
<span class="n">y_pred</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>====================== Start of Level 0 ======================
1 estimators included in Level 0 
====================== Start of Level 1 ======================
1 estimators included in Level 1 
====================== Start of Level 2 ======================
1 estimators included in Level 2 
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[0.42497899],
       [3.08351247],
       [1.29010732],
       [2.26160334],
       [2.23084816],
       [1.01613217],
       [2.21192437],
       [1.11314039],
       [1.44429742],
       [2.35757185],
       [5.19457553],
       [0.55098658],
       [4.22470465],
       [2.79316617],
       [0.36922034],
       [1.08035688],
       [1.78490923],
       [1.07460621],
       [2.19602401],
       [5.15019236],
       [3.83430565],
       [3.61145345],
       [0.72378805],
       [0.44463816],
       [1.96620632],
       [0.2533803 ],
       [2.85836655],
       [2.54530208],
       [0.85450247],
       [1.97189663],
       [0.94280999],
       [2.17094025],
       [2.33080707],
       [1.87856379],
       [3.59726546],
       [2.54355231],
       [3.85592018],
       [2.59323133],
       [1.14190951],
       [2.47957448],
       [3.43767044],
       [0.85500637],
       [3.05351449],
       [0.89606775],
       [2.22318793],
       [0.3977447 ],
       [2.12860973],
       [2.88375007],
       [2.18581127],
       [1.17299233],
       [1.1946012 ],
       [2.22946192],
       [1.96726051],
       [2.00622796],
       [2.89393174],
       [0.23465967],
       [2.48359502],
       [0.37761293],
       [3.28917552],
       [1.05242958],
       [4.33203196],
       [0.44718331],
       [3.59463936],
       [4.15496842],
       [1.82719138],
       [1.09885717],
       [0.89814135],
       [0.39853684],
       [0.9854424 ],
       [2.52822592],
       [2.06463766],
       [2.61909572],
       [2.14415526],
       [1.35536623],
       [0.26505517],
       [0.24493924],
       [1.37679253],
       [1.75662488],
       [0.65260673],
       [0.79439567],
       [3.33105798],
       [2.03768165],
       [1.70576713],
       [1.13963334],
       [0.23192211],
       [0.80702924],
       [1.82383677],
       [1.74957914],
       [0.23418107],
       [1.44687947],
       [0.22215245],
       [1.24597867],
       [0.69162499],
       [0.84453216],
       [0.46485001],
       [1.01793194],
       [0.99657038],
       [0.2852136 ],
       [1.87650402],
       [3.83354095],
       [0.77090891],
       [3.20721697],
       [1.95235728],
       [2.05009385],
       [2.17049893],
       [4.52690627],
       [0.41396874],
       [0.25662281],
       [3.03954231],
       [2.2416681 ],
       [1.15362935],
       [1.0965913 ],
       [0.37741771],
       [0.40355637],
       [1.10115225],
       [0.36976049],
       [2.58772103],
       [1.20838287],
       [0.09925361],
       [5.02175275],
       [0.22832012],
       [1.89481965],
       [1.77529324],
       [1.14389633],
       [0.28531986],
       [2.93257287],
       [0.25302904],
       [4.26596137],
       [1.52661057],
       [1.23954278],
       [2.33599102],
       [1.07407993],
       [1.20991624],
       [2.93587652],
       [2.10526479],
       [5.29710913],
       [0.23243344],
       [0.23660058],
       [0.70851748],
       [0.76398077],
       [0.64719654],
       [0.35785959],
       [1.22132102],
       [0.35187994],
       [4.54158373],
       [1.15676168],
       [1.23574134],
       [0.78216097],
       [0.2447049 ],
       [2.44383191],
       [1.22539147],
       [1.51058126],
       [0.26573574],
       [1.92077588],
       [1.09923424],
       [0.48138405],
       [0.22786032],
       [1.34455952],
       [0.8040661 ],
       [0.37855431],
       [0.39311958],
       [3.48415288],
       [1.20881918],
       [2.81437225],
       [1.0851878 ],
       [0.96715087],
       [0.22794269],
       [0.95423175],
       [1.1234997 ],
       [4.1821449 ],
       [0.39105748],
       [0.20429905],
       [3.02922865],
       [2.32475416],
       [2.52746214],
       [3.77518932],
       [0.83025176],
       [0.68891011],
       [0.66260116],
       [2.20949063],
       [3.58988966],
       [2.58247883],
       [1.31928658],
       [0.45000848],
       [3.61966888],
       [0.76382848],
       [1.74076302],
       [1.21488406],
       [3.27821016],
       [1.68252906],
       [3.42258177],
       [3.98406471],
       [1.00498747],
       [0.35212594],
       [1.68492342],
       [1.63557229],
       [1.94799246],
       [2.3995128 ],
       [1.11334909],
       [2.02959456],
       [2.77030069],
       [1.15683131],
       [1.01180656],
       [4.26994609],
       [0.34250626],
       [0.79327346],
       [0.55151522],
       [2.99172412],
       [0.187401  ],
       [4.51349342],
       [2.28090089],
       [0.75533269],
       [1.96918837],
       [1.84927683],
       [2.54643402],
       [0.70246401],
       [2.83969233],
       [0.40044574],
       [0.28886491],
       [1.8444662 ],
       [0.63583484],
       [1.8689096 ],
       [1.01742779],
       [0.39461548],
       [1.94582579],
       [1.87586317],
       [2.4920187 ],
       [4.70680487],
       [1.67043605],
       [0.26879196],
       [4.19805763],
       [1.87705275],
       [0.80406813],
       [1.56948588],
       [1.1805945 ],
       [0.09709191],
       [2.71024867],
       [3.34673726],
       [2.22323465],
       [2.25851282],
       [5.25496881],
       [1.0894677 ],
       [2.61927005],
       [3.18386342],
       [0.23344723],
       [0.27618742],
       [0.42607879],
       [0.24201603],
       [2.31390708],
       [2.97580466],
       [1.81921757],
       [2.09968905],
       [0.74265756],
       [0.82011479],
       [0.41074838],
       [0.36063037],
       [0.89783306],
       [4.08630937],
       [0.74835857],
       [0.70637202],
       [1.29370913],
       [1.37554364],
       [0.10255006],
       [0.23369333],
       [1.33451148],
       [0.76508705],
       [1.678466  ],
       [0.89846476],
       [1.74699264],
       [0.81882307],
       [3.6885161 ],
       [1.28620908],
       [0.13458414],
       [4.9463649 ],
       [1.81386527],
       [0.23600034],
       [0.75386457],
       [0.36392427],
       [5.22605153],
       [2.53240413],
       [0.94198131],
       [1.00920107],
       [1.80314255],
       [3.10847243],
       [1.40199462],
       [0.99954368],
       [2.28431354],
       [0.35029036],
       [1.58938215],
       [0.34466226],
       [2.65729123],
       [3.19509602],
       [4.25534029],
       [0.87408204],
       [0.36444936],
       [0.28717726],
       [4.21999004],
       [1.46967371],
       [1.27384787],
       [0.9758491 ],
       [1.99238771],
       [2.08032768],
       [2.17895897],
       [2.24016276],
       [0.189811  ],
       [0.3462765 ],
       [0.35181415],
       [0.21099997],
       [1.81514991],
       [4.34128908],
       [0.92733944],
       [0.70772218],
       [3.29428051],
       [0.39699974],
       [1.07912673],
       [1.14712328],
       [1.06286069],
       [0.95810265],
       [2.32758447],
       [1.88068652],
       [5.17103462],
       [2.26043625],
       [1.29264003],
       [1.71137131],
       [1.65097008],
       [2.55704228],
       [0.60435623],
       [0.83758227],
       [3.93427981],
       [0.43554202],
       [1.78287655],
       [3.05570038],
       [1.01442166],
       [0.4318496 ],
       [0.11344825],
       [1.59919349],
       [1.20968383],
       [1.04104146],
       [2.23829531],
       [1.00484472],
       [1.20480404],
       [2.60029222],
       [0.42780793],
       [2.03725856],
       [0.69524736],
       [0.54430918],
       [1.9892104 ],
       [4.25625915],
       [4.17959288],
       [2.26738388],
       [1.21104218],
       [0.4125184 ],
       [4.63665193],
       [4.89005519],
       [1.67315123],
       [2.79828771],
       [0.48230836],
       [2.64248114],
       [5.25967697],
       [0.93802169],
       [0.10053457],
       [0.68239269]])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_valid</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span> <span class="s1">&#39;Np&#39;</span><span class="p">,</span> <span class="s1">&#39;Vp&#39;</span><span class="p">,</span> <span class="s1">&#39;Tp&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span> <span class="s1">&#39;B_gsm_z&#39;</span><span class="p">,</span> <span class="s1">&#39;Bt&#39;</span><span class="p">])</span>
<span class="n">x_valid</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>Vp</th>
      <th>Tp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4019</th>
      <td>2.0</td>
      <td>8.526023</td>
      <td>292.637104</td>
      <td>31986.271131</td>
      <td>1.000426</td>
      <td>3.484932</td>
      <td>5.550188</td>
      <td>6.841796</td>
    </tr>
    <tr>
      <th>2599</th>
      <td>43.0</td>
      <td>4.470427</td>
      <td>479.656463</td>
      <td>132059.780488</td>
      <td>-3.021793</td>
      <td>-0.153201</td>
      <td>1.675858</td>
      <td>4.654438</td>
    </tr>
    <tr>
      <th>5235</th>
      <td>122.0</td>
      <td>2.984033</td>
      <td>463.176025</td>
      <td>93150.295597</td>
      <td>1.105041</td>
      <td>-3.154308</td>
      <td>-0.973385</td>
      <td>4.510373</td>
    </tr>
    <tr>
      <th>1698</th>
      <td>238.0</td>
      <td>2.524446</td>
      <td>526.466043</td>
      <td>219300.863309</td>
      <td>-4.706550</td>
      <td>-0.822278</td>
      <td>1.282882</td>
      <td>5.109852</td>
    </tr>
    <tr>
      <th>1270</th>
      <td>175.0</td>
      <td>3.404780</td>
      <td>505.885793</td>
      <td>142502.926829</td>
      <td>-0.857219</td>
      <td>6.614444</td>
      <td>2.148497</td>
      <td>7.284870</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_train</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>Vp</th>
      <th>Tp</th>
      <th>B_gsm_x</th>
      <th>B_gsm_y</th>
      <th>B_gsm_z</th>
      <th>Bt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4501</th>
      <td>119.0</td>
      <td>4.379065</td>
      <td>376.384847</td>
      <td>74612.666667</td>
      <td>2.968663</td>
      <td>-3.529716</td>
      <td>0.465083</td>
      <td>5.262325</td>
    </tr>
    <tr>
      <th>2080</th>
      <td>255.0</td>
      <td>6.715164</td>
      <td>255.294667</td>
      <td>50838.394808</td>
      <td>5.415768</td>
      <td>-0.041911</td>
      <td>2.944810</td>
      <td>6.249042</td>
    </tr>
    <tr>
      <th>1976</th>
      <td>151.0</td>
      <td>11.886253</td>
      <td>429.546810</td>
      <td>74509.717791</td>
      <td>2.856160</td>
      <td>-6.308710</td>
      <td>0.041160</td>
      <td>8.571976</td>
    </tr>
    <tr>
      <th>4277</th>
      <td>260.0</td>
      <td>3.190858</td>
      <td>494.933994</td>
      <td>95897.671906</td>
      <td>0.803698</td>
      <td>-0.304441</td>
      <td>-1.533156</td>
      <td>3.350183</td>
    </tr>
    <tr>
      <th>3884</th>
      <td>232.0</td>
      <td>6.933509</td>
      <td>496.592577</td>
      <td>173485.889571</td>
      <td>3.242440</td>
      <td>-1.853202</td>
      <td>0.946905</td>
      <td>5.072030</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_valid</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;B_gsm_x&#39;</span><span class="p">,</span><span class="s1">&#39;doy&#39;</span><span class="p">,</span><span class="s1">&#39;Np&#39;</span><span class="p">,</span><span class="s1">&#39;Vp&#39;</span><span class="p">,</span><span class="s1">&#39;Bt&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_y&#39;</span><span class="p">,</span><span class="s1">&#39;Tp&#39;</span><span class="p">,</span><span class="s1">&#39;B_gsm_z&#39;</span><span class="p">])</span>
<span class="n">x_valid</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>B_gsm_x</th>
      <th>doy</th>
      <th>Np</th>
      <th>Vp</th>
      <th>Bt</th>
      <th>B_gsm_y</th>
      <th>Tp</th>
      <th>B_gsm_z</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>11</th>
      <td>4.665509</td>
      <td>12.0</td>
      <td>8.061702</td>
      <td>371.780688</td>
      <td>5.783822</td>
      <td>-1.625882</td>
      <td>43249.981366</td>
      <td>1.535751</td>
    </tr>
    <tr>
      <th>1567</th>
      <td>-2.563911</td>
      <td>107.0</td>
      <td>2.161512</td>
      <td>733.161049</td>
      <td>5.677321</td>
      <td>1.453577</td>
      <td>223708.765432</td>
      <td>-1.520935</td>
    </tr>
    <tr>
      <th>5323</th>
      <td>-4.020432</td>
      <td>210.0</td>
      <td>2.161141</td>
      <td>403.778820</td>
      <td>4.398391</td>
      <td>1.148118</td>
      <td>78057.938405</td>
      <td>-1.017101</td>
    </tr>
    <tr>
      <th>1309</th>
      <td>-6.001355</td>
      <td>214.0</td>
      <td>6.076848</td>
      <td>510.306159</td>
      <td>12.826036</td>
      <td>-8.313604</td>
      <td>22890.534146</td>
      <td>7.352450</td>
    </tr>
    <tr>
      <th>3862</th>
      <td>3.067929</td>
      <td>210.0</td>
      <td>3.546685</td>
      <td>371.019080</td>
      <td>3.953589</td>
      <td>0.517643</td>
      <td>50704.601227</td>
      <td>-1.626554</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#x_valid=x_valid.as_matrix()</span>
<span class="n">x_valid</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[ 4.66550888e+00,  1.20000000e+01,  8.06170186e+00, ...,
        -1.62588166e+00,  4.32499814e+04,  1.53575148e+00],
       [-2.56391071e+00,  1.07000000e+02,  2.16151235e+00, ...,
         1.45357738e+00,  2.23708765e+05, -1.52093452e+00],
       [-4.02043195e+00,  2.10000000e+02,  2.16114093e+00, ...,
         1.14811834e+00,  7.80579384e+04, -1.01710059e+00],
       ...,
       [ 6.24590533e+00,  2.68000000e+02,  8.68644614e+00, ...,
        -3.65134320e+00,  5.31593781e+04,  4.59630178e+00],
       [-6.30656548e+00,  1.78000000e+02,  9.21477848e+00, ...,
         7.74294643e+00,  2.68239304e+05,  3.35498810e+00],
       [-3.97014201e+00,  3.54000000e+02,  3.50125153e+00, ...,
         1.90011834e-01,  1.74676601e+05, -2.25143195e+00]])</pre>
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

<span class="c1">#multiclass</span>
<span class="c1">#pred=[np.argmax(y_pred[i]) for i in range(len(y_pred))]</span>

<span class="c1">#regression</span>
<span class="c1">#pred=np.round(y_pred)</span>
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
<pre>weighted rmse:  1.1391390587964187
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_absolute_error</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_squared_error</span>

<span class="c1">#prediction</span>
<span class="c1">#y_pred=model.predict(x_test)</span>
<span class="c1">#pred=[np.argmax(y_pred[i]) for i in range(len(y_pred))]</span>

<span class="c1">#multiclass</span>
<span class="c1">#y_pred=np.round(y_pred)</span>
<span class="c1">#print(&quot;rmae : &quot;, mean_absolute_error(y_test,pred))</span>
<span class="c1">#print(np.sqrt(mean_squared_error(y_test,pred)))</span>

<span class="c1">#regression</span>
<span class="c1">#y_pred=np.round(y_pred)</span>
<span class="c1">#print(&quot;mae : &quot;, mean_absolute_error(y_,y_pred))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;rmse : &quot;</span><span class="p">,</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_valid</span><span class="p">,</span><span class="n">pred</span><span class="p">)))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>rmse :  0.9460589962097461
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_valid</span><span class="p">[:</span><span class="mi">5</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>334     0
4798    4
2406    2
1845    3
1595    4
Name: label, dtype: int64</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="p">(</span><span class="n">pred</span><span class="o">-</span><span class="n">y_valid</span><span class="p">)[:</span><span class="mi">5</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[ 0., -4., -2., ..., -2.,  0.,  0.],
       [ 3., -1.,  1., ...,  1.,  3.,  3.],
       [ 1., -3., -1., ..., -1.,  1.,  1.],
       [ 2., -2.,  0., ...,  0.,  2.,  2.],
       [ 2., -2.,  0., ...,  0.,  2.,  2.]])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_valid</span><span class="p">[:</span><span class="mi">5</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([0, 4, 2, 3, 4])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred</span><span class="o">=</span><span class="nb">list</span><span class="p">(</span><span class="n">pred</span><span class="p">)</span>
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
<span class="ansi-red-fg">TypeError</span>                                 Traceback (most recent call last)
<span class="ansi-green-fg">&lt;ipython-input-91-f51b726af74e&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-fg">----&gt; 1</span><span class="ansi-red-fg"> </span>pred<span class="ansi-blue-fg">=</span>list<span class="ansi-blue-fg">(</span>pred<span class="ansi-blue-fg">)</span>

<span class="ansi-red-fg">TypeError</span>: iteration over a 0-d array</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred</span><span class="o">=</span><span class="n">pred</span><span class="o">.</span><span class="n">reshape</span><span class="p">(</span><span class="mi">362</span><span class="p">,</span><span class="n">order</span><span class="o">=</span><span class="s1">&#39;C&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_valid</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(362,)</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">tt</span><span class="p">)</span>
<span class="n">pred</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([0, 3, 1, 2, 2, 1, 2, 1, 1, 2, 5, 1, 4, 3, 0, 1, 2, 1, 2, 5, 4, 4,
       1, 0, 2, 0, 3, 3, 1, 2, 1, 2, 2, 2, 4, 3, 4, 3, 1, 2, 3, 1, 3, 1,
       2, 0, 2, 3, 2, 1, 1, 2, 2, 2, 3, 0, 2, 0, 3, 1, 4, 0, 4, 4, 2, 1,
       1, 0, 1, 3, 2, 3, 2, 1, 0, 0, 1, 2, 1, 1, 3, 2, 2, 1, 0, 1, 2, 2,
       0, 1, 0, 1, 1, 1, 0, 1, 1, 0, 2, 4, 1, 3, 2, 2, 2, 5, 0, 0, 3, 2,
       1, 1, 0, 0, 1, 0, 3, 1, 0, 5, 0, 2, 2, 1, 0, 3, 0, 4, 2, 1, 2, 1,
       1, 3, 2, 5, 0, 0, 1, 1, 1, 0, 1, 0, 5, 1, 1, 1, 0, 2, 1, 2, 0, 2,
       1, 0, 0, 1, 1, 0, 0, 3, 1, 3, 1, 1, 0, 1, 1, 4, 0, 0, 3, 2, 3, 4,
       1, 1, 1, 2, 4, 3, 1, 0, 4, 1, 2, 1, 3, 2, 3, 4, 1, 0, 2, 2, 2, 2,
       1, 2, 3, 1, 1, 4, 0, 1, 1, 3, 0, 5, 2, 1, 2, 2, 3, 1, 3, 0, 0, 2,
       1, 2, 1, 0, 2, 2, 2, 5, 2, 0, 4, 2, 1, 2, 1, 0, 3, 3, 2, 2, 5, 1,
       3, 3, 0, 0, 0, 0, 2, 3, 2, 2, 1, 1, 0, 0, 1, 4, 1, 1, 1, 1, 0, 0,
       1, 1, 2, 1, 2, 1, 4, 1, 0, 5, 2, 0, 1, 0, 5, 3, 1, 1, 2, 3, 1, 1,
       2, 0, 2, 0, 3, 3, 4, 1, 0, 0, 4, 1, 1, 1, 2, 2, 2, 2, 0, 0, 0, 0,
       2, 4, 1, 1, 3, 0, 1, 1, 1, 1, 2, 2, 5, 2, 1, 2, 2, 3, 1, 1, 4, 0,
       2, 3, 1, 0, 0, 2, 1, 1, 2, 1, 1, 3, 0, 2, 1, 1, 2, 4, 4, 2, 1, 0,
       5, 5, 2, 3, 0, 3, 5, 1, 0, 1])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([0, 3, 1, 2, 2, 1, 2, 1, 1, 2, 5, 1, 4, 3, 0, 1, 2, 1, 2, 5, 4, 4,
       1, 0, 2, 0, 3, 3, 1, 2, 1, 2, 2, 2, 4, 3, 4, 3, 1, 2, 3, 1, 3, 1,
       2, 0, 2, 3, 2, 1, 1, 2, 2, 2, 3, 0, 2, 0, 3, 1, 4, 0, 4, 4, 2, 1,
       1, 0, 1, 3, 2, 3, 2, 1, 0, 0, 1, 2, 1, 1, 3, 2, 2, 1, 0, 1, 2, 2,
       0, 1, 0, 1, 1, 1, 0, 1, 1, 0, 2, 4, 1, 3, 2, 2, 2, 5, 0, 0, 3, 2,
       1, 1, 0, 0, 1, 0, 3, 1, 0, 5, 0, 2, 2, 1, 0, 3, 0, 4, 2, 1, 2, 1,
       1, 3, 2, 5, 0, 0, 1, 1, 1, 0, 1, 0, 5, 1, 1, 1, 0, 2, 1, 2, 0, 2,
       1, 0, 0, 1, 1, 0, 0, 3, 1, 3, 1, 1, 0, 1, 1, 4, 0, 0, 3, 2, 3, 4,
       1, 1, 1, 2, 4, 3, 1, 0, 4, 1, 2, 1, 3, 2, 3, 4, 1, 0, 2, 2, 2, 2,
       1, 2, 3, 1, 1, 4, 0, 1, 1, 3, 0, 5, 2, 1, 2, 2, 3, 1, 3, 0, 0, 2,
       1, 2, 1, 0, 2, 2, 2, 5, 2, 0, 4, 2, 1, 2, 1, 0, 3, 3, 2, 2, 5, 1,
       3, 3, 0, 0, 0, 0, 2, 3, 2, 2, 1, 1, 0, 0, 1, 4, 1, 1, 1, 1, 0, 0,
       1, 1, 2, 1, 2, 1, 4, 1, 0, 5, 2, 0, 1, 0, 5, 3, 1, 1, 2, 3, 1, 1,
       2, 0, 2, 0, 3, 3, 4, 1, 0, 0, 4, 1, 1, 1, 2, 2, 2, 2, 0, 0, 0, 0,
       2, 4, 1, 1, 3, 0, 1, 1, 1, 1, 2, 2, 5, 2, 1, 2, 2, 3, 1, 1, 4, 0,
       2, 3, 1, 0, 0, 2, 1, 1, 2, 1, 1, 3, 0, 2, 1, 1, 2, 4, 4, 2, 1, 0,
       5, 5, 2, 3, 0, 3, 5, 1, 0, 1])</pre>
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
