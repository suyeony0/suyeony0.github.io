---
layout: post
title: Big Contest - Model Train
date: 2020-06-14
description: READ ME
thumbnail: food1.jpg
categories: BigContest

# Information for the author block
author : Loui
---

<html>
<head><meta charset="utf-8" />

<title>binCon_model_train</title>

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
<div class="prompt input_prompt">In&nbsp;[3]:</div>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/new_flatten.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/new_before_flatten.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/row40000.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged2</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/loged_hyun.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged2</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s2">&quot;Unnamed: 0&quot;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">merged2</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>acc_id</th>
      <th>pledge_random_attacker_cnt_min</th>
      <th>party_exp_min</th>
      <th>combat_play_time_min</th>
      <th>fishing_min</th>
      <th>amount_spent_min</th>
      <th>pledge_play_char_cnt_mean_min</th>
      <th>playtime_min</th>
      <th>pledge_same_pledge_cnt_min</th>
      <th>solo_exp_min</th>
      <th>num_opponent_min</th>
      <th>combat_temp_cnt_min</th>
      <th>quest_exp_min</th>
      <th>combat_random_defender_cnt_min</th>
      <th>combat_etc_cnt_min</th>
      <th>item_amount_min</th>
      <th>combat_pledge_cnt_min</th>
      <th>total_exp_min</th>
      <th>pledge_char_cnt_mean_min</th>
      <th>revive_min</th>
      <th>death_min</th>
      <th>boss_monster_min</th>
      <th>pledge_random_defender_cnt_min</th>
      <th>pledge_temp_cnt_min</th>
      <th>game_money_change_min</th>
      <th>exp_recovery_min</th>
      <th>combat_random_attacker_cnt_min</th>
      <th>non_combat_play_time_min</th>
      <th>private_shop_min</th>
      <th>pledge_etc_cnt_min</th>
      <th>npc_kill_min</th>
      <th>level_min</th>
      <th>enchant_count_min</th>
      <th>item_price_min</th>
      <th>combat_same_pledge_cnt_min</th>
      <th>pledge_random_attacker_cnt_mean</th>
      <th>party_exp_mean</th>
      <th>combat_play_time_mean</th>
      <th>fishing_mean</th>
      <th>amount_spent_mean</th>
      <th>...</th>
      <th>revive_sum</th>
      <th>death_sum</th>
      <th>boss_monster_sum</th>
      <th>pledge_random_defender_cnt_sum</th>
      <th>pledge_temp_cnt_sum</th>
      <th>game_money_change_sum</th>
      <th>exp_recovery_sum</th>
      <th>combat_random_attacker_cnt_sum</th>
      <th>non_combat_play_time_sum</th>
      <th>private_shop_sum</th>
      <th>pledge_etc_cnt_sum</th>
      <th>npc_kill_sum</th>
      <th>level_sum</th>
      <th>enchant_count_sum</th>
      <th>item_price_sum</th>
      <th>combat_same_pledge_cnt_sum</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
      <th>6</th>
      <th>7</th>
      <th>afternoon</th>
      <th>amount_spent</th>
      <th>class_cnt</th>
      <th>dawn</th>
      <th>level_range0</th>
      <th>level_range1</th>
      <th>level_range2</th>
      <th>level_range3</th>
      <th>level_range4</th>
      <th>maxServerOfAcc</th>
      <th>max_level</th>
      <th>min_level</th>
      <th>morning</th>
      <th>pledge_importance</th>
      <th>survival_time</th>
      <th>week_cnt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.296617</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>5.517650</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.227366</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>4.701920</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>4.465503</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>1.885895</td>
      <td>0.0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>1.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>20</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.559616</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>62974.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.432652</td>
      <td>0.484487</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>5.521825</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>4.394449</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.921402</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.239445</td>
      <td>0.000000</td>
      <td>3.341215</td>
      <td>1.892560</td>
      <td>4.701997</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.426884</td>
      <td>0.000000</td>
      <td>1.116025</td>
      <td>3.481865</td>
      <td>7.714677</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4</td>
      <td>0.0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>21</td>
      <td>2.833213</td>
      <td>2.833213</td>
      <td>0.0</td>
      <td>1.386294</td>
      <td>8</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>62955.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.495664</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.165893</td>
      <td>0.004729</td>
      <td>0.0</td>
      <td>0.000025</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000025</td>
      <td>0.035453</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>5.521388</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.00000</td>
      <td>0.001685</td>
      <td>4.394449</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.772814</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.219432</td>
      <td>0.000000</td>
      <td>2.124382</td>
      <td>1.057366</td>
      <td>4.701625</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.837022</td>
      <td>4.072100</td>
      <td>7.601402</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2</td>
      <td>0.0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>21</td>
      <td>2.833213</td>
      <td>2.833213</td>
      <td>0.0</td>
      <td>1.386294</td>
      <td>8</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>62952.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.000112</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.566401</td>
      <td>0.007085</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.584428</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.251634</td>
      <td>0.782346</td>
      <td>5.521825</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.19838</td>
      <td>0.000000</td>
      <td>3.713572</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.203702</td>
      <td>0.0</td>
      <td>1.045898</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.401215</td>
      <td>0.399272</td>
      <td>0.693147</td>
      <td>1.350992</td>
      <td>2.378566</td>
      <td>4.702001</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.136679</td>
      <td>0.219083</td>
      <td>5.545177</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2</td>
      <td>0.0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>0</td>
      <td>16</td>
      <td>2.484907</td>
      <td>2.197225</td>
      <td>0.0</td>
      <td>1.098612</td>
      <td>1</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>62942.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.208599</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>5.515018</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.132130</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>4.708347</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>4.459695</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>2.994125</td>
      <td>0.0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>1.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>10</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>1.386294</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 161 columns</p>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged2</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">yy</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">yy</span><span class="o">=</span><span class="n">merged2</span><span class="p">[[</span><span class="s1">&#39;playtime_sum&#39;</span><span class="p">,</span><span class="s1">&#39;acc_id&#39;</span><span class="p">]]</span>
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
      <th>playtime_sum</th>
      <th>acc_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4.539923</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>17484</th>
      <td>1.972796</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>28898</th>
      <td>2.997335</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>33049</th>
      <td>3.395202</td>
      <td>17.0</td>
    </tr>
    <tr>
      <th>27993</th>
      <td>3.292416</td>
      <td>20.0</td>
    </tr>
    <tr>
      <th>34897</th>
      <td>3.139995</td>
      <td>21.0</td>
    </tr>
    <tr>
      <th>15150</th>
      <td>4.432161</td>
      <td>31.0</td>
    </tr>
    <tr>
      <th>37089</th>
      <td>4.286321</td>
      <td>38.0</td>
    </tr>
    <tr>
      <th>15152</th>
      <td>0.002367</td>
      <td>41.0</td>
    </tr>
    <tr>
      <th>20360</th>
      <td>1.801353</td>
      <td>43.0</td>
    </tr>
    <tr>
      <th>15161</th>
      <td>4.378268</td>
      <td>50.0</td>
    </tr>
    <tr>
      <th>15127</th>
      <td>4.511283</td>
      <td>53.0</td>
    </tr>
    <tr>
      <th>15135</th>
      <td>3.466143</td>
      <td>54.0</td>
    </tr>
    <tr>
      <th>15139</th>
      <td>4.538201</td>
      <td>59.0</td>
    </tr>
    <tr>
      <th>31243</th>
      <td>3.676367</td>
      <td>62.0</td>
    </tr>
    <tr>
      <th>34834</th>
      <td>3.612895</td>
      <td>63.0</td>
    </tr>
    <tr>
      <th>15165</th>
      <td>4.179630</td>
      <td>65.0</td>
    </tr>
    <tr>
      <th>36055</th>
      <td>3.874592</td>
      <td>66.0</td>
    </tr>
    <tr>
      <th>17176</th>
      <td>2.902331</td>
      <td>67.0</td>
    </tr>
    <tr>
      <th>27944</th>
      <td>3.199050</td>
      <td>69.0</td>
    </tr>
    <tr>
      <th>23327</th>
      <td>1.900713</td>
      <td>75.0</td>
    </tr>
    <tr>
      <th>15203</th>
      <td>4.535054</td>
      <td>76.0</td>
    </tr>
    <tr>
      <th>15198</th>
      <td>4.535028</td>
      <td>77.0</td>
    </tr>
    <tr>
      <th>15169</th>
      <td>4.535384</td>
      <td>79.0</td>
    </tr>
    <tr>
      <th>34960</th>
      <td>3.763314</td>
      <td>81.0</td>
    </tr>
    <tr>
      <th>15173</th>
      <td>4.536806</td>
      <td>86.0</td>
    </tr>
    <tr>
      <th>38041</th>
      <td>4.434413</td>
      <td>91.0</td>
    </tr>
    <tr>
      <th>15178</th>
      <td>4.511413</td>
      <td>92.0</td>
    </tr>
    <tr>
      <th>15124</th>
      <td>4.535003</td>
      <td>97.0</td>
    </tr>
    <tr>
      <th>36093</th>
      <td>4.417915</td>
      <td>98.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>14762</th>
      <td>4.539442</td>
      <td>130383.0</td>
    </tr>
    <tr>
      <th>15022</th>
      <td>0.392808</td>
      <td>130384.0</td>
    </tr>
    <tr>
      <th>31969</th>
      <td>2.675470</td>
      <td>130386.0</td>
    </tr>
    <tr>
      <th>14893</th>
      <td>4.529317</td>
      <td>130390.0</td>
    </tr>
    <tr>
      <th>34445</th>
      <td>3.448591</td>
      <td>130391.0</td>
    </tr>
    <tr>
      <th>23764</th>
      <td>2.640081</td>
      <td>130392.0</td>
    </tr>
    <tr>
      <th>21105</th>
      <td>2.949348</td>
      <td>130398.0</td>
    </tr>
    <tr>
      <th>28081</th>
      <td>3.573915</td>
      <td>130401.0</td>
    </tr>
    <tr>
      <th>14885</th>
      <td>3.782867</td>
      <td>130403.0</td>
    </tr>
    <tr>
      <th>29564</th>
      <td>3.694972</td>
      <td>130405.0</td>
    </tr>
    <tr>
      <th>15012</th>
      <td>4.447651</td>
      <td>130408.0</td>
    </tr>
    <tr>
      <th>31830</th>
      <td>2.712957</td>
      <td>130411.0</td>
    </tr>
    <tr>
      <th>14993</th>
      <td>4.388740</td>
      <td>130413.0</td>
    </tr>
    <tr>
      <th>35194</th>
      <td>3.960097</td>
      <td>130414.0</td>
    </tr>
    <tr>
      <th>22257</th>
      <td>4.291329</td>
      <td>130415.0</td>
    </tr>
    <tr>
      <th>14755</th>
      <td>4.483191</td>
      <td>130416.0</td>
    </tr>
    <tr>
      <th>21802</th>
      <td>1.641311</td>
      <td>130420.0</td>
    </tr>
    <tr>
      <th>34481</th>
      <td>3.607639</td>
      <td>130433.0</td>
    </tr>
    <tr>
      <th>24144</th>
      <td>2.611083</td>
      <td>130434.0</td>
    </tr>
    <tr>
      <th>15246</th>
      <td>4.521488</td>
      <td>130445.0</td>
    </tr>
    <tr>
      <th>22160</th>
      <td>2.463927</td>
      <td>130447.0</td>
    </tr>
    <tr>
      <th>31017</th>
      <td>3.439433</td>
      <td>130449.0</td>
    </tr>
    <tr>
      <th>15287</th>
      <td>4.534265</td>
      <td>130459.0</td>
    </tr>
    <tr>
      <th>15314</th>
      <td>0.264957</td>
      <td>130461.0</td>
    </tr>
    <tr>
      <th>19041</th>
      <td>1.921744</td>
      <td>130462.0</td>
    </tr>
    <tr>
      <th>15075</th>
      <td>3.937250</td>
      <td>130463.0</td>
    </tr>
    <tr>
      <th>19459</th>
      <td>0.883645</td>
      <td>130468.0</td>
    </tr>
    <tr>
      <th>31336</th>
      <td>4.082493</td>
      <td>130469.0</td>
    </tr>
    <tr>
      <th>16360</th>
      <td>3.192257</td>
      <td>130470.0</td>
    </tr>
    <tr>
      <th>38802</th>
      <td>4.310288</td>
      <td>130473.0</td>
    </tr>
  </tbody>
</table>
<p>40000 rows × 2 columns</p>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">kk</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">merged</span><span class="p">,</span><span class="n">yy</span><span class="p">,</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="s1">&#39;acc_id&#39;</span><span class="p">)</span>
<span class="n">kk</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>acc_id</th>
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
      <th>playtime_sum</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>-0.008746</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>91.533663</td>
      <td>84.900753</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>406</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>0.013612</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>4.539923</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>0.245883</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>3.442909</td>
      <td>0.145146</td>
      <td>3.236452</td>
      <td>0.695285</td>
      <td>6.116132</td>
      <td>0.000000</td>
      <td>0.111055</td>
      <td>0.247337</td>
      <td>9</td>
      <td>2.155434</td>
      <td>55</td>
      <td>0.000000</td>
      <td>0.098129</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>2.014665e-04</td>
      <td>0.432697</td>
      <td>1.587930</td>
      <td>5.097608</td>
      <td>0.814001</td>
      <td>0.004402</td>
      <td>5.557755</td>
      <td>0.000000</td>
      <td>1.936569</td>
      <td>0.929907</td>
      <td>0.000000</td>
      <td>2.570959</td>
      <td>0.000000</td>
      <td>3.600000</td>
      <td>15.000000</td>
      <td>1.972796</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>91.960416</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.807823</td>
      <td>0.020353</td>
      <td>31.172609</td>
      <td>0.000000</td>
      <td>18.797802</td>
      <td>0.000000</td>
      <td>1.561055</td>
      <td>92.504000</td>
      <td>2</td>
      <td>31.489136</td>
      <td>406</td>
      <td>0.900892</td>
      <td>3.041991</td>
      <td>0.128368</td>
      <td>4.270875</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>3.837822</td>
      <td>2.442839e+00</td>
      <td>0.065648</td>
      <td>58.031626</td>
      <td>136.879854</td>
      <td>61.354404</td>
      <td>0.033823</td>
      <td>201.306223</td>
      <td>2.717332</td>
      <td>33.631748</td>
      <td>21.745527</td>
      <td>29.441536</td>
      <td>92.455650</td>
      <td>1.404644</td>
      <td>17.321429</td>
      <td>15.964286</td>
      <td>2.997335</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>1.721184</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>13.990954</td>
      <td>-0.027696</td>
      <td>30.456852</td>
      <td>8.823094</td>
      <td>28.464708</td>
      <td>0.000000</td>
      <td>2.322365</td>
      <td>1.731358</td>
      <td>21</td>
      <td>9.255848</td>
      <td>406</td>
      <td>0.675669</td>
      <td>1.373803</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.366129</td>
      <td>12.398273</td>
      <td>3.358094</td>
      <td>2.972307e+00</td>
      <td>7.246862</td>
      <td>21.689681</td>
      <td>65.693573</td>
      <td>12.514373</td>
      <td>0.000000</td>
      <td>71.312495</td>
      <td>0.486279</td>
      <td>9.230979</td>
      <td>10.872764</td>
      <td>1.591434</td>
      <td>36.784494</td>
      <td>0.000000</td>
      <td>1.214286</td>
      <td>16.000000</td>
      <td>3.395202</td>
    </tr>
    <tr>
      <th>4</th>
      <td>20</td>
      <td>0.983534</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.295766</td>
      <td>-0.370192</td>
      <td>34.100184</td>
      <td>0.080060</td>
      <td>25.588043</td>
      <td>2.917510</td>
      <td>0.083483</td>
      <td>0.989348</td>
      <td>8</td>
      <td>0.274902</td>
      <td>378</td>
      <td>16.441283</td>
      <td>10.107262</td>
      <td>1.283685</td>
      <td>0.000000</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>3.372187e+00</td>
      <td>20.513500</td>
      <td>25.515149</td>
      <td>66.451919</td>
      <td>44.409036</td>
      <td>0.000000</td>
      <td>54.891855</td>
      <td>7.964404</td>
      <td>11.974452</td>
      <td>6.580883</td>
      <td>11.140041</td>
      <td>28.379435</td>
      <td>0.896531</td>
      <td>5.851852</td>
      <td>17.000000</td>
      <td>3.292416</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">kk</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;playtime_sum&#39;</span><span class="p">:</span><span class="s1">&#39;playtime&#39;</span><span class="p">},</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">kk</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>acc_id</th>
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
      <th>playtime</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>-0.008746</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>91.533663</td>
      <td>84.900753</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>406</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>0.013612</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>4.539923</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>0.245883</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>3.442909</td>
      <td>0.145146</td>
      <td>3.236452</td>
      <td>0.695285</td>
      <td>6.116132</td>
      <td>0.000000</td>
      <td>0.111055</td>
      <td>0.247337</td>
      <td>9</td>
      <td>2.155434</td>
      <td>55</td>
      <td>0.000000</td>
      <td>0.098129</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>2.014665e-04</td>
      <td>0.432697</td>
      <td>1.587930</td>
      <td>5.097608</td>
      <td>0.814001</td>
      <td>0.004402</td>
      <td>5.557755</td>
      <td>0.000000</td>
      <td>1.936569</td>
      <td>0.929907</td>
      <td>0.000000</td>
      <td>2.570959</td>
      <td>0.000000</td>
      <td>3.600000</td>
      <td>15.000000</td>
      <td>1.972796</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>91.960416</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.807823</td>
      <td>0.020353</td>
      <td>31.172609</td>
      <td>0.000000</td>
      <td>18.797802</td>
      <td>0.000000</td>
      <td>1.561055</td>
      <td>92.504000</td>
      <td>2</td>
      <td>31.489136</td>
      <td>406</td>
      <td>0.900892</td>
      <td>3.041991</td>
      <td>0.128368</td>
      <td>4.270875</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>3.837822</td>
      <td>2.442839e+00</td>
      <td>0.065648</td>
      <td>58.031626</td>
      <td>136.879854</td>
      <td>61.354404</td>
      <td>0.033823</td>
      <td>201.306223</td>
      <td>2.717332</td>
      <td>33.631748</td>
      <td>21.745527</td>
      <td>29.441536</td>
      <td>92.455650</td>
      <td>1.404644</td>
      <td>17.321429</td>
      <td>15.964286</td>
      <td>2.997335</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>1.721184</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>13.990954</td>
      <td>-0.027696</td>
      <td>30.456852</td>
      <td>8.823094</td>
      <td>28.464708</td>
      <td>0.000000</td>
      <td>2.322365</td>
      <td>1.731358</td>
      <td>21</td>
      <td>9.255848</td>
      <td>406</td>
      <td>0.675669</td>
      <td>1.373803</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.366129</td>
      <td>12.398273</td>
      <td>3.358094</td>
      <td>2.972307e+00</td>
      <td>7.246862</td>
      <td>21.689681</td>
      <td>65.693573</td>
      <td>12.514373</td>
      <td>0.000000</td>
      <td>71.312495</td>
      <td>0.486279</td>
      <td>9.230979</td>
      <td>10.872764</td>
      <td>1.591434</td>
      <td>36.784494</td>
      <td>0.000000</td>
      <td>1.214286</td>
      <td>16.000000</td>
      <td>3.395202</td>
    </tr>
    <tr>
      <th>4</th>
      <td>20</td>
      <td>0.983534</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.295766</td>
      <td>-0.370192</td>
      <td>34.100184</td>
      <td>0.080060</td>
      <td>25.588043</td>
      <td>2.917510</td>
      <td>0.083483</td>
      <td>0.989348</td>
      <td>8</td>
      <td>0.274902</td>
      <td>378</td>
      <td>16.441283</td>
      <td>10.107262</td>
      <td>1.283685</td>
      <td>0.000000</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>3.372187e+00</td>
      <td>20.513500</td>
      <td>25.515149</td>
      <td>66.451919</td>
      <td>44.409036</td>
      <td>0.000000</td>
      <td>54.891855</td>
      <td>7.964404</td>
      <td>11.974452</td>
      <td>6.580883</td>
      <td>11.140041</td>
      <td>28.379435</td>
      <td>0.896531</td>
      <td>5.851852</td>
      <td>17.000000</td>
      <td>3.292416</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_model/40000개.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>acc_id</th>
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.704009</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>91.533663</td>
      <td>4.453193</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>6.006353</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>0.013520</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.693147</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>125006</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.419866</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.872524</td>
      <td>0.000624</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>5.703782</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>7.877995e-01</td>
      <td>0.994733</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.850716</td>
      <td>2.458087</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.749200</td>
    </tr>
    <tr>
      <th>2</th>
      <td>43978</td>
      <td>0.906362</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.704116</td>
      <td>4.692193</td>
      <td>0.000000</td>
      <td>90.089479</td>
      <td>0.000000</td>
      <td>0.021139</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.522136</td>
      <td>6.006353</td>
      <td>4.670417</td>
      <td>3.592543</td>
      <td>1.749136</td>
      <td>0.0</td>
      <td>0.78073</td>
      <td>0.0</td>
      <td>0.391858</td>
      <td>2.396984e-08</td>
      <td>0.000000</td>
      <td>2.44252</td>
      <td>3.826882</td>
      <td>4.102057</td>
      <td>0.000000</td>
      <td>2.541046</td>
      <td>2.040805</td>
      <td>0.0</td>
      <td>0.999437</td>
      <td>0.000000</td>
      <td>1.495352</td>
      <td>0.0</td>
      <td>1.609438</td>
      <td>2.833213</td>
    </tr>
    <tr>
      <th>3</th>
      <td>43983</td>
      <td>2.741300</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.704066</td>
      <td>0.008078</td>
      <td>3.408623</td>
      <td>81.958042</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.664181</td>
      <td>0.0</td>
      <td>0.000518</td>
      <td>6.006353</td>
      <td>0.203123</td>
      <td>0.331111</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.672667</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.09357</td>
      <td>4.258933</td>
      <td>0.186703</td>
      <td>3.356605</td>
      <td>3.213061</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.762907</td>
      <td>1.882517</td>
      <td>1.300149</td>
      <td>0.0</td>
      <td>1.421386</td>
      <td>2.831110</td>
    </tr>
    <tr>
      <th>4</th>
      <td>43999</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.675435</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>82.650876</td>
      <td>4.394099</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>6.006353</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.191429e-02</td>
      <td>0.000000</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.040297</td>
      <td>0.102798</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>2.101517</td>
      <td>1.791759</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">label</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_original/train_label.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/loged.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">merged</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s2">&quot;Unnamed: 0&quot;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">merged</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>acc_id</th>
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.704009</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>91.533663</td>
      <td>4.453193</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>6.006353</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>0.013520</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.693147</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>125006</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.419866</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.872524</td>
      <td>0.000624</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>5.703782</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>7.877995e-01</td>
      <td>0.994733</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.850716</td>
      <td>2.458087</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.749200</td>
    </tr>
    <tr>
      <th>2</th>
      <td>43978</td>
      <td>0.906362</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.704116</td>
      <td>4.692193</td>
      <td>0.000000</td>
      <td>90.089479</td>
      <td>0.000000</td>
      <td>0.021139</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.522136</td>
      <td>6.006353</td>
      <td>4.670417</td>
      <td>3.592543</td>
      <td>1.749136</td>
      <td>0.0</td>
      <td>0.78073</td>
      <td>0.0</td>
      <td>0.391858</td>
      <td>2.396984e-08</td>
      <td>0.000000</td>
      <td>2.44252</td>
      <td>3.826882</td>
      <td>4.102057</td>
      <td>0.000000</td>
      <td>2.541046</td>
      <td>2.040805</td>
      <td>0.0</td>
      <td>0.999437</td>
      <td>0.000000</td>
      <td>1.495352</td>
      <td>0.0</td>
      <td>1.609438</td>
      <td>2.833213</td>
    </tr>
    <tr>
      <th>3</th>
      <td>43983</td>
      <td>2.741300</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.704066</td>
      <td>0.008078</td>
      <td>3.408623</td>
      <td>81.958042</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.664181</td>
      <td>0.0</td>
      <td>0.000518</td>
      <td>6.006353</td>
      <td>0.203123</td>
      <td>0.331111</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.672667</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.09357</td>
      <td>4.258933</td>
      <td>0.186703</td>
      <td>3.356605</td>
      <td>3.213061</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.762907</td>
      <td>1.882517</td>
      <td>1.300149</td>
      <td>0.0</td>
      <td>1.421386</td>
      <td>2.831110</td>
    </tr>
    <tr>
      <th>4</th>
      <td>43999</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.675435</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>82.650876</td>
      <td>4.394099</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>6.006353</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.191429e-02</td>
      <td>0.000000</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.040297</td>
      <td>0.102798</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>2.101517</td>
      <td>1.791759</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aa</span><span class="o">=</span><span class="n">merged2</span><span class="o">.</span><span class="n">columns</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">tolist</span><span class="p">()</span>
<span class="nb">print</span><span class="p">(</span><span class="n">aa</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;acc_id&#39;, &#39;pledge_random_attacker_cnt_min&#39;, &#39;party_exp_min&#39;, &#39;combat_play_time_min&#39;, &#39;fishing_min&#39;, &#39;amount_spent_min&#39;, &#39;pledge_play_char_cnt_mean_min&#39;, &#39;playtime_min&#39;, &#39;pledge_same_pledge_cnt_min&#39;, &#39;solo_exp_min&#39;, &#39;num_opponent_min&#39;, &#39;combat_temp_cnt_min&#39;, &#39;quest_exp_min&#39;, &#39;combat_random_defender_cnt_min&#39;, &#39;combat_etc_cnt_min&#39;, &#39;item_amount_min&#39;, &#39;combat_pledge_cnt_min&#39;, &#39;total_exp_min&#39;, &#39;pledge_char_cnt_mean_min&#39;, &#39;revive_min&#39;, &#39;death_min&#39;, &#39;boss_monster_min&#39;, &#39;pledge_random_defender_cnt_min&#39;, &#39;pledge_temp_cnt_min&#39;, &#39;game_money_change_min&#39;, &#39;exp_recovery_min&#39;, &#39;combat_random_attacker_cnt_min&#39;, &#39;non_combat_play_time_min&#39;, &#39;private_shop_min&#39;, &#39;pledge_etc_cnt_min&#39;, &#39;npc_kill_min&#39;, &#39;level_min&#39;, &#39;enchant_count_min&#39;, &#39;item_price_min&#39;, &#39;combat_same_pledge_cnt_min&#39;, &#39;pledge_random_attacker_cnt_mean&#39;, &#39;party_exp_mean&#39;, &#39;combat_play_time_mean&#39;, &#39;fishing_mean&#39;, &#39;amount_spent_mean&#39;, &#39;pledge_play_char_cnt_mean_mean&#39;, &#39;playtime_mean&#39;, &#39;pledge_same_pledge_cnt_mean&#39;, &#39;solo_exp_mean&#39;, &#39;num_opponent_mean&#39;, &#39;combat_temp_cnt_mean&#39;, &#39;quest_exp_mean&#39;, &#39;combat_random_defender_cnt_mean&#39;, &#39;combat_etc_cnt_mean&#39;, &#39;item_amount_mean&#39;, &#39;combat_pledge_cnt_mean&#39;, &#39;total_exp_mean&#39;, &#39;pledge_char_cnt_mean_mean&#39;, &#39;revive_mean&#39;, &#39;death_mean&#39;, &#39;boss_monster_mean&#39;, &#39;pledge_random_defender_cnt_mean&#39;, &#39;pledge_temp_cnt_mean&#39;, &#39;game_money_change_mean&#39;, &#39;exp_recovery_mean&#39;, &#39;combat_random_attacker_cnt_mean&#39;, &#39;non_combat_play_time_mean&#39;, &#39;private_shop_mean&#39;, &#39;pledge_etc_cnt_mean&#39;, &#39;npc_kill_mean&#39;, &#39;level_mean&#39;, &#39;enchant_count_mean&#39;, &#39;item_price_mean&#39;, &#39;combat_same_pledge_cnt_mean&#39;, &#39;pledge_random_attacker_cnt_max&#39;, &#39;party_exp_max&#39;, &#39;combat_play_time_max&#39;, &#39;fishing_max&#39;, &#39;amount_spent_max&#39;, &#39;pledge_play_char_cnt_mean_max&#39;, &#39;playtime_max&#39;, &#39;pledge_same_pledge_cnt_max&#39;, &#39;solo_exp_max&#39;, &#39;num_opponent_max&#39;, &#39;combat_temp_cnt_max&#39;, &#39;quest_exp_max&#39;, &#39;combat_random_defender_cnt_max&#39;, &#39;combat_etc_cnt_max&#39;, &#39;item_amount_max&#39;, &#39;combat_pledge_cnt_max&#39;, &#39;total_exp_max&#39;, &#39;pledge_char_cnt_mean_max&#39;, &#39;revive_max&#39;, &#39;death_max&#39;, &#39;boss_monster_max&#39;, &#39;pledge_random_defender_cnt_max&#39;, &#39;pledge_temp_cnt_max&#39;, &#39;game_money_change_max&#39;, &#39;exp_recovery_max&#39;, &#39;combat_random_attacker_cnt_max&#39;, &#39;non_combat_play_time_max&#39;, &#39;private_shop_max&#39;, &#39;pledge_etc_cnt_max&#39;, &#39;npc_kill_max&#39;, &#39;level_max&#39;, &#39;enchant_count_max&#39;, &#39;item_price_max&#39;, &#39;combat_same_pledge_cnt_max&#39;, &#39;pledge_random_attacker_cnt_sum&#39;, &#39;party_exp_sum&#39;, &#39;combat_play_time_sum&#39;, &#39;fishing_sum&#39;, &#39;amount_spent_sum&#39;, &#39;pledge_play_char_cnt_mean_sum&#39;, &#39;playtime_sum&#39;, &#39;pledge_same_pledge_cnt_sum&#39;, &#39;solo_exp_sum&#39;, &#39;num_opponent_sum&#39;, &#39;combat_temp_cnt_sum&#39;, &#39;quest_exp_sum&#39;, &#39;combat_random_defender_cnt_sum&#39;, &#39;combat_etc_cnt_sum&#39;, &#39;item_amount_sum&#39;, &#39;combat_pledge_cnt_sum&#39;, &#39;total_exp_sum&#39;, &#39;pledge_char_cnt_mean_sum&#39;, &#39;revive_sum&#39;, &#39;death_sum&#39;, &#39;boss_monster_sum&#39;, &#39;pledge_random_defender_cnt_sum&#39;, &#39;pledge_temp_cnt_sum&#39;, &#39;game_money_change_sum&#39;, &#39;exp_recovery_sum&#39;, &#39;combat_random_attacker_cnt_sum&#39;, &#39;non_combat_play_time_sum&#39;, &#39;private_shop_sum&#39;, &#39;pledge_etc_cnt_sum&#39;, &#39;npc_kill_sum&#39;, &#39;level_sum&#39;, &#39;enchant_count_sum&#39;, &#39;item_price_sum&#39;, &#39;combat_same_pledge_cnt_sum&#39;, &#39;0&#39;, &#39;1&#39;, &#39;2&#39;, &#39;3&#39;, &#39;4&#39;, &#39;5&#39;, &#39;6&#39;, &#39;7&#39;, &#39;afternoon&#39;, &#39;amount_spent&#39;, &#39;class_cnt&#39;, &#39;dawn&#39;, &#39;level_range0&#39;, &#39;level_range1&#39;, &#39;level_range2&#39;, &#39;level_range3&#39;, &#39;level_range4&#39;, &#39;maxServerOfAcc&#39;, &#39;max_level&#39;, &#39;min_level&#39;, &#39;morning&#39;, &#39;pledge_importance&#39;, &#39;survival_time&#39;, &#39;week_cnt&#39;]
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cur</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">cur</span><span class="o">=</span><span class="n">merged2</span><span class="p">[[</span><span class="s1">&#39;0&#39;</span><span class="p">,</span> <span class="s1">&#39;1&#39;</span><span class="p">,</span> <span class="s1">&#39;2&#39;</span><span class="p">,</span> <span class="s1">&#39;3&#39;</span><span class="p">,</span> <span class="s1">&#39;4&#39;</span><span class="p">,</span> <span class="s1">&#39;5&#39;</span><span class="p">,</span> <span class="s1">&#39;6&#39;</span><span class="p">,</span> <span class="s1">&#39;7&#39;</span><span class="p">,</span> <span class="s1">&#39;afternoon&#39;</span><span class="p">,</span> <span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span> <span class="s1">&#39;class_cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;dawn&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range0&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range1&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range2&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range3&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range4&#39;</span><span class="p">,</span> <span class="s1">&#39;maxServerOfAcc&#39;</span><span class="p">,</span> <span class="s1">&#39;max_level&#39;</span><span class="p">,</span> <span class="s1">&#39;min_level&#39;</span><span class="p">,</span> <span class="s1">&#39;morning&#39;</span><span class="p">,</span> <span class="s1">&#39;pledge_importance&#39;</span><span class="p">,</span> <span class="s1">&#39;survival_time&#39;</span><span class="p">,</span> <span class="s1">&#39;week_cnt&#39;</span><span class="p">,</span><span class="s1">&#39;acc_id&#39;</span><span class="p">]]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">bb</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">merged</span><span class="p">,</span><span class="n">cur</span><span class="p">,</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="s1">&#39;acc_id&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="o">=</span><span class="n">bb</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">temp</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;0&#39;</span><span class="p">,</span> <span class="s1">&#39;1&#39;</span><span class="p">,</span> <span class="s1">&#39;2&#39;</span><span class="p">,</span> <span class="s1">&#39;3&#39;</span><span class="p">,</span> <span class="s1">&#39;4&#39;</span><span class="p">,</span> <span class="s1">&#39;5&#39;</span><span class="p">,</span> <span class="s1">&#39;6&#39;</span><span class="p">,</span> <span class="s1">&#39;7&#39;</span><span class="p">,</span><span class="s1">&#39;level_range0&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range1&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range2&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range3&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range4&#39;</span><span class="p">,</span> <span class="s1">&#39;week_cnt&#39;</span> <span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
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
      <th>acc_id</th>
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
      <th>afternoon</th>
      <th>amount_spent</th>
      <th>class_cnt</th>
      <th>dawn</th>
      <th>maxServerOfAcc</th>
      <th>max_level</th>
      <th>min_level</th>
      <th>morning</th>
      <th>pledge_importance</th>
      <th>survival_time</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>-0.008746</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>91.533663</td>
      <td>84.900753</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>406</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>0.013612</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1</td>
      <td>1.0</td>
      <td>20</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.559616</td>
      <td>64</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>0.245883</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>3.442909</td>
      <td>0.145146</td>
      <td>3.236452</td>
      <td>0.695285</td>
      <td>6.116132</td>
      <td>0.000000</td>
      <td>0.111055</td>
      <td>0.247337</td>
      <td>9</td>
      <td>2.155434</td>
      <td>55</td>
      <td>0.000000</td>
      <td>0.098129</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>2.014665e-04</td>
      <td>0.432697</td>
      <td>1.587930</td>
      <td>5.097608</td>
      <td>0.814001</td>
      <td>0.004402</td>
      <td>5.557755</td>
      <td>0.000000</td>
      <td>1.936569</td>
      <td>0.929907</td>
      <td>0.000000</td>
      <td>2.570959</td>
      <td>0.000000</td>
      <td>3.600000</td>
      <td>15.000000</td>
      <td>0.666667</td>
      <td>0.000000</td>
      <td>7</td>
      <td>0.0</td>
      <td>16</td>
      <td>2.772589</td>
      <td>0.693147</td>
      <td>0.666667</td>
      <td>1.203973</td>
      <td>60</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>91.960416</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.807823</td>
      <td>0.020353</td>
      <td>31.172609</td>
      <td>0.000000</td>
      <td>18.797802</td>
      <td>0.000000</td>
      <td>1.561055</td>
      <td>92.504000</td>
      <td>2</td>
      <td>31.489136</td>
      <td>406</td>
      <td>0.900892</td>
      <td>3.041991</td>
      <td>0.128368</td>
      <td>4.270875</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>3.837822</td>
      <td>2.442839e+00</td>
      <td>0.065648</td>
      <td>58.031626</td>
      <td>136.879854</td>
      <td>61.354404</td>
      <td>0.033823</td>
      <td>201.306223</td>
      <td>2.717332</td>
      <td>33.631748</td>
      <td>21.745527</td>
      <td>29.441536</td>
      <td>92.455650</td>
      <td>1.404644</td>
      <td>17.321429</td>
      <td>15.964286</td>
      <td>0.500000</td>
      <td>0.020310</td>
      <td>2</td>
      <td>0.5</td>
      <td>14</td>
      <td>2.833213</td>
      <td>2.484907</td>
      <td>0.000000</td>
      <td>0.916291</td>
      <td>64</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>1.721184</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>13.990954</td>
      <td>-0.027696</td>
      <td>30.456852</td>
      <td>8.823094</td>
      <td>28.464708</td>
      <td>0.000000</td>
      <td>2.322365</td>
      <td>1.731358</td>
      <td>21</td>
      <td>9.255848</td>
      <td>406</td>
      <td>0.675669</td>
      <td>1.373803</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.366129</td>
      <td>12.398273</td>
      <td>3.358094</td>
      <td>2.972307e+00</td>
      <td>7.246862</td>
      <td>21.689681</td>
      <td>65.693573</td>
      <td>12.514373</td>
      <td>0.000000</td>
      <td>71.312495</td>
      <td>0.486279</td>
      <td>9.230979</td>
      <td>10.872764</td>
      <td>1.591434</td>
      <td>36.784494</td>
      <td>0.000000</td>
      <td>1.214286</td>
      <td>16.000000</td>
      <td>1.000000</td>
      <td>0.070642</td>
      <td>2</td>
      <td>1.0</td>
      <td>16</td>
      <td>2.833213</td>
      <td>0.693147</td>
      <td>1.000000</td>
      <td>0.693147</td>
      <td>64</td>
    </tr>
    <tr>
      <th>4</th>
      <td>20</td>
      <td>0.983534</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.295766</td>
      <td>-0.370192</td>
      <td>34.100184</td>
      <td>0.080060</td>
      <td>25.588043</td>
      <td>2.917510</td>
      <td>0.083483</td>
      <td>0.989348</td>
      <td>8</td>
      <td>0.274902</td>
      <td>378</td>
      <td>16.441283</td>
      <td>10.107262</td>
      <td>1.283685</td>
      <td>0.000000</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>3.372187e+00</td>
      <td>20.513500</td>
      <td>25.515149</td>
      <td>66.451919</td>
      <td>44.409036</td>
      <td>0.000000</td>
      <td>54.891855</td>
      <td>7.964404</td>
      <td>11.974452</td>
      <td>6.580883</td>
      <td>11.140041</td>
      <td>28.379435</td>
      <td>0.896531</td>
      <td>5.851852</td>
      <td>17.000000</td>
      <td>1.000000</td>
      <td>0.052137</td>
      <td>2</td>
      <td>1.0</td>
      <td>6</td>
      <td>2.890372</td>
      <td>1.945910</td>
      <td>1.000000</td>
      <td>0.559616</td>
      <td>64</td>
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
<h1 id="&#50668;&#44592;&#49436;&#48512;&#53552;&#44032;-&#49884;&#51089;"><strong>&#50668;&#44592;&#49436;&#48512;&#53552;&#44032; &#49884;&#51089;</strong><a class="anchor-link" href="#&#50668;&#44592;&#49436;&#48512;&#53552;&#44032;-&#49884;&#51089;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#merged=pd.read_csv(&#39;/content/drive/My Drive/new_model/loged_final.csv&#39;,engine=&#39;python&#39;)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/row40000.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">label</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_original/train_label.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[490]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">merged</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">merged</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">merged</span><span class="p">,</span><span class="n">label</span><span class="p">,</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="s1">&#39;acc_id&#39;</span><span class="p">)</span>
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
<span class="ansi-green-fg">&lt;ipython-input-490-ad7e66500914&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-fg">----&gt; 1</span><span class="ansi-red-fg"> </span>merged<span class="ansi-blue-fg">.</span>drop<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">&#39;Unnamed: 0&#39;</span><span class="ansi-blue-fg">,</span>axis<span class="ansi-blue-fg">=</span><span class="ansi-cyan-fg">1</span><span class="ansi-blue-fg">,</span>inplace<span class="ansi-blue-fg">=</span><span class="ansi-green-fg">True</span><span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">      2</span> merged<span class="ansi-blue-fg">=</span>pd<span class="ansi-blue-fg">.</span>merge<span class="ansi-blue-fg">(</span>merged<span class="ansi-blue-fg">,</span>label<span class="ansi-blue-fg">,</span>how<span class="ansi-blue-fg">=</span><span class="ansi-blue-fg">&#39;left&#39;</span><span class="ansi-blue-fg">,</span>on<span class="ansi-blue-fg">=</span><span class="ansi-blue-fg">&#39;acc_id&#39;</span><span class="ansi-blue-fg">)</span>

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

<span class="ansi-red-fg">KeyError</span>: &#34;[&#39;Unnamed: 0&#39;] not found in axis&#34;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="n">merged</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="c1">#temp2 는 y햇을 걸러내기위함</span>
<span class="n">temp2</span><span class="o">=</span><span class="n">merged</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>

<span class="c1">#temp3는 under64를 위하여 바이너리로 변환시키지 않은것</span>
<span class="n">temp3</span><span class="o">=</span><span class="n">merged</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>

<span class="n">temp2</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">temp</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;acc_id&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[605]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 0,1 분류</span>
<span class="n">aa</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">64</span><span class="p">]</span>
<span class="n">bb</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">!=</span><span class="mi">64</span><span class="p">]</span>

<span class="n">aa</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
<span class="n">bb</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>


<span class="c1">#과금 분류</span>
<span class="c1">#aa=temp[temp[&#39;amount_spent&#39;]!=0]</span>
<span class="c1">#bb=temp[temp[&#39;amount_spent&#39;]==0]</span>
<span class="c1">#aa[&#39;amount_spent&#39;]=1</span>
<span class="c1">#bb[&#39;amount_spent&#39;]=0</span>



<span class="n">temp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">temp</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">aa</span><span class="p">)</span>
<span class="n">temp</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">bb</span><span class="p">)</span>
<span class="n">temp</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:4: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  after removing the cwd from sys.path.
/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:5: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  &#34;&#34;&#34;
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[605]:</div>



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
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
      <th>survival_time</th>
      <th>amount_spent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>-0.008746</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>91.533663</td>
      <td>84.900753</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>406</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>0.013612</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>91.960416</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.807823</td>
      <td>0.020353</td>
      <td>31.172609</td>
      <td>0.000000</td>
      <td>18.797802</td>
      <td>0.000000</td>
      <td>1.561055</td>
      <td>92.504000</td>
      <td>2</td>
      <td>31.489136</td>
      <td>406</td>
      <td>0.900892</td>
      <td>3.041991</td>
      <td>0.128368</td>
      <td>4.270875</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>3.837822</td>
      <td>2.442839e+00</td>
      <td>0.065648</td>
      <td>58.031626</td>
      <td>136.879854</td>
      <td>61.354404</td>
      <td>0.033823</td>
      <td>201.306223</td>
      <td>2.717332</td>
      <td>33.631748</td>
      <td>21.745527</td>
      <td>29.441536</td>
      <td>92.455650</td>
      <td>1.404644</td>
      <td>17.321429</td>
      <td>15.964286</td>
      <td>1</td>
      <td>0.020310</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.721184</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>13.990954</td>
      <td>-0.027696</td>
      <td>30.456852</td>
      <td>8.823094</td>
      <td>28.464708</td>
      <td>0.000000</td>
      <td>2.322365</td>
      <td>1.731358</td>
      <td>21</td>
      <td>9.255848</td>
      <td>406</td>
      <td>0.675669</td>
      <td>1.373803</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.366129</td>
      <td>12.398273</td>
      <td>3.358094</td>
      <td>2.972307e+00</td>
      <td>7.246862</td>
      <td>21.689681</td>
      <td>65.693573</td>
      <td>12.514373</td>
      <td>0.000000</td>
      <td>71.312495</td>
      <td>0.486279</td>
      <td>9.230979</td>
      <td>10.872764</td>
      <td>1.591434</td>
      <td>36.784494</td>
      <td>0.000000</td>
      <td>1.214286</td>
      <td>16.000000</td>
      <td>1</td>
      <td>0.070642</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.983534</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.295766</td>
      <td>-0.370192</td>
      <td>34.100184</td>
      <td>0.080060</td>
      <td>25.588043</td>
      <td>2.917510</td>
      <td>0.083483</td>
      <td>0.989348</td>
      <td>8</td>
      <td>0.274902</td>
      <td>378</td>
      <td>16.441283</td>
      <td>10.107262</td>
      <td>1.283685</td>
      <td>0.000000</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>3.372187e+00</td>
      <td>20.513500</td>
      <td>25.515149</td>
      <td>66.451919</td>
      <td>44.409036</td>
      <td>0.000000</td>
      <td>54.891855</td>
      <td>7.964404</td>
      <td>11.974452</td>
      <td>6.580883</td>
      <td>11.140041</td>
      <td>28.379435</td>
      <td>0.896531</td>
      <td>5.851852</td>
      <td>17.000000</td>
      <td>1</td>
      <td>0.052137</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>14.846620</td>
      <td>0.021332</td>
      <td>10.771165</td>
      <td>0.380025</td>
      <td>21.831291</td>
      <td>0.000000</td>
      <td>9.524346</td>
      <td>0.000000</td>
      <td>3</td>
      <td>20.064853</td>
      <td>351</td>
      <td>0.225223</td>
      <td>0.785030</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.878367</td>
      <td>2.109422e+00</td>
      <td>2.853494</td>
      <td>0.360893</td>
      <td>0.501896</td>
      <td>0.035391</td>
      <td>0.875103</td>
      <td>1.660109</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.071531</td>
      <td>0.000000</td>
      <td>0.791064</td>
      <td>2.695461</td>
      <td>0.038462</td>
      <td>15.076923</td>
      <td>1</td>
      <td>0.184267</td>
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
<div class="prompt input_prompt">In&nbsp;[606]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aa</span><span class="o">=</span><span class="n">temp2</span><span class="p">[</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">64</span><span class="p">]</span>
<span class="n">bb</span><span class="o">=</span><span class="n">temp2</span><span class="p">[</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">!=</span><span class="mi">64</span><span class="p">]</span>
<span class="n">aa</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
<span class="n">bb</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>


<span class="c1">#과금 분류</span>
<span class="c1">#aa=temp2[temp2[&#39;amount_spent&#39;]!=0]</span>
<span class="c1">#bb=temp2[temp2[&#39;amount_spent&#39;]==0]</span>

<span class="c1">#aa[&#39;amount_spent&#39;]=1</span>
<span class="c1">#bb[&#39;amount_spent&#39;]=0</span>


<span class="n">temp2</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">temp2</span><span class="o">=</span><span class="n">temp2</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">aa</span><span class="p">)</span>
<span class="n">temp2</span><span class="o">=</span><span class="n">temp2</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">bb</span><span class="p">)</span>
<span class="n">temp2</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:4: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  after removing the cwd from sys.path.
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[606]:</div>



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
      <th>acc_id</th>
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
      <th>survival_time</th>
      <th>amount_spent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>-0.008746</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>91.533663</td>
      <td>84.900753</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>406</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>0.013612</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>91.960416</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.807823</td>
      <td>0.020353</td>
      <td>31.172609</td>
      <td>0.000000</td>
      <td>18.797802</td>
      <td>0.000000</td>
      <td>1.561055</td>
      <td>92.504000</td>
      <td>2</td>
      <td>31.489136</td>
      <td>406</td>
      <td>0.900892</td>
      <td>3.041991</td>
      <td>0.128368</td>
      <td>4.270875</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>3.837822</td>
      <td>2.442839e+00</td>
      <td>0.065648</td>
      <td>58.031626</td>
      <td>136.879854</td>
      <td>61.354404</td>
      <td>0.033823</td>
      <td>201.306223</td>
      <td>2.717332</td>
      <td>33.631748</td>
      <td>21.745527</td>
      <td>29.441536</td>
      <td>92.455650</td>
      <td>1.404644</td>
      <td>17.321429</td>
      <td>15.964286</td>
      <td>1</td>
      <td>0.020310</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>1.721184</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>13.990954</td>
      <td>-0.027696</td>
      <td>30.456852</td>
      <td>8.823094</td>
      <td>28.464708</td>
      <td>0.000000</td>
      <td>2.322365</td>
      <td>1.731358</td>
      <td>21</td>
      <td>9.255848</td>
      <td>406</td>
      <td>0.675669</td>
      <td>1.373803</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.366129</td>
      <td>12.398273</td>
      <td>3.358094</td>
      <td>2.972307e+00</td>
      <td>7.246862</td>
      <td>21.689681</td>
      <td>65.693573</td>
      <td>12.514373</td>
      <td>0.000000</td>
      <td>71.312495</td>
      <td>0.486279</td>
      <td>9.230979</td>
      <td>10.872764</td>
      <td>1.591434</td>
      <td>36.784494</td>
      <td>0.000000</td>
      <td>1.214286</td>
      <td>16.000000</td>
      <td>1</td>
      <td>0.070642</td>
    </tr>
    <tr>
      <th>4</th>
      <td>20</td>
      <td>0.983534</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>4.295766</td>
      <td>-0.370192</td>
      <td>34.100184</td>
      <td>0.080060</td>
      <td>25.588043</td>
      <td>2.917510</td>
      <td>0.083483</td>
      <td>0.989348</td>
      <td>8</td>
      <td>0.274902</td>
      <td>378</td>
      <td>16.441283</td>
      <td>10.107262</td>
      <td>1.283685</td>
      <td>0.000000</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>3.372187e+00</td>
      <td>20.513500</td>
      <td>25.515149</td>
      <td>66.451919</td>
      <td>44.409036</td>
      <td>0.000000</td>
      <td>54.891855</td>
      <td>7.964404</td>
      <td>11.974452</td>
      <td>6.580883</td>
      <td>11.140041</td>
      <td>28.379435</td>
      <td>0.896531</td>
      <td>5.851852</td>
      <td>17.000000</td>
      <td>1</td>
      <td>0.052137</td>
    </tr>
    <tr>
      <th>5</th>
      <td>21</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>14.846620</td>
      <td>0.021332</td>
      <td>10.771165</td>
      <td>0.380025</td>
      <td>21.831291</td>
      <td>0.000000</td>
      <td>9.524346</td>
      <td>0.000000</td>
      <td>3</td>
      <td>20.064853</td>
      <td>351</td>
      <td>0.225223</td>
      <td>0.785030</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.878367</td>
      <td>2.109422e+00</td>
      <td>2.853494</td>
      <td>0.360893</td>
      <td>0.501896</td>
      <td>0.035391</td>
      <td>0.875103</td>
      <td>1.660109</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.071531</td>
      <td>0.000000</td>
      <td>0.791064</td>
      <td>2.695461</td>
      <td>0.038462</td>
      <td>15.076923</td>
      <td>1</td>
      <td>0.184267</td>
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
<div class="prompt input_prompt">In&nbsp;[607]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#데이터 셔플</span>
<span class="n">temp</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="n">frac</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">temp2</span><span class="o">=</span><span class="n">temp2</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="n">frac</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">temp</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[607]:</div>



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
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
      <th>survival_time</th>
      <th>amount_spent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>365</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>57.951697</td>
      <td>-1.046961</td>
      <td>15.612495</td>
      <td>0.0</td>
      <td>77.700391</td>
      <td>0.000000</td>
      <td>0.002223</td>
      <td>0.000000</td>
      <td>4</td>
      <td>0.052903</td>
      <td>406</td>
      <td>0.225223</td>
      <td>0.785030</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.183064</td>
      <td>0.0</td>
      <td>2.398639</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>0.685697</td>
      <td>1.6726</td>
      <td>0.665357</td>
      <td>1.934031</td>
      <td>3.284128</td>
      <td>0.491742</td>
      <td>0.0</td>
      <td>0.071531</td>
      <td>0.0</td>
      <td>1.384363</td>
      <td>1.060817</td>
      <td>1.107143</td>
      <td>17.000000</td>
      <td>1</td>
      <td>0.113297</td>
    </tr>
    <tr>
      <th>37461</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.847241</td>
      <td>0.007097</td>
      <td>0.0</td>
      <td>89.560491</td>
      <td>71.680772</td>
      <td>0.018961</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.001782</td>
      <td>406</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>4.793968e-08</td>
      <td>1.661565</td>
      <td>0.000000</td>
      <td>0.0000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.697041</td>
      <td>5.607143</td>
      <td>0.535714</td>
      <td>1</td>
      <td>0.030449</td>
    </tr>
    <tr>
      <th>36797</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.115745</td>
      <td>-0.081736</td>
      <td>3.580475</td>
      <td>0.0</td>
      <td>0.493878</td>
      <td>0.000000</td>
      <td>0.001301</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.032475</td>
      <td>3</td>
      <td>0.000000</td>
      <td>0.098129</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.479728</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0000</td>
      <td>0.000000</td>
      <td>0.001158</td>
      <td>0.144357</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>7.000000</td>
      <td>16.000000</td>
      <td>0</td>
      <td>1.040110</td>
    </tr>
    <tr>
      <th>26728</th>
      <td>0.983534</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.496687</td>
      <td>-0.193206</td>
      <td>2.981646</td>
      <td>0.0</td>
      <td>7.948865</td>
      <td>0.000000</td>
      <td>0.893642</td>
      <td>0.989348</td>
      <td>1</td>
      <td>2.610310</td>
      <td>253</td>
      <td>0.112612</td>
      <td>0.098129</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.162537e-05</td>
      <td>0.747565</td>
      <td>0.000000</td>
      <td>0.0000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.360255</td>
      <td>3.681818</td>
      <td>14.909091</td>
      <td>0</td>
      <td>0.003642</td>
    </tr>
    <tr>
      <th>29067</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>2.060289</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>90.108204</td>
      <td>85.597839</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>406</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>7.000000</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>


<span class="n">x_train</span><span class="p">,</span> <span class="n">x_valid</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_valid</span><span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">temp</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>\
                                                     <span class="n">temp</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">,</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">)</span>

<span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
<span class="n">lgb_valid</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#영준쓰 파라미터</span>
<span class="c1">#feature_fraction : 데이터의 paremater들 중에 각 round에 몇 %의 parameter를 random으로 골라 학습시킬지 정해주는 인자</span>
<span class="n">params</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s1">&#39;boosting_type&#39;</span><span class="p">:</span> <span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
    <span class="s1">&#39;objective&#39;</span><span class="p">:</span> <span class="s1">&#39;binary&#39;</span><span class="p">,</span>
    <span class="c1">#&#39;metric&#39;:&#39;mape&#39;,</span>
    <span class="s1">&#39;num_leaves&#39;</span><span class="p">:</span><span class="mi">950</span><span class="p">,</span>
 
    <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span> <span class="c1">#20이 최적화라고 한다.</span>
    <span class="s1">&#39;max_depth&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
    <span class="s1">&#39;max_bin&#39;</span><span class="p">:</span><span class="mi">50</span><span class="p">,</span>
    <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.05</span><span class="p">,</span>
    <span class="s1">&#39;feature_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
  
    <span class="s1">&#39;bagging_freq&#39;</span><span class="p">:</span> <span class="mi">5</span><span class="p">,</span>
    <span class="s1">&#39;num_trees&#39;</span><span class="p">:</span><span class="mi">1000</span><span class="p">,</span> <span class="c1">#이게 train 반복횟수임</span>

    <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:</span> <span class="s1">&#39;auto&#39;</span>

    
<span class="p">}</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[610]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span>
               <span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_valid</span><span class="p">,</span>
               <span class="n">verbose_eval</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span>
               <span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">50</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/lightgbm/engine.py:118: UserWarning: Found `num_trees` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 50 rounds.
[10]	valid_0&#39;s binary_logloss: 0.576243
[20]	valid_0&#39;s binary_logloss: 0.526587
[30]	valid_0&#39;s binary_logloss: 0.501997
[40]	valid_0&#39;s binary_logloss: 0.487789
[50]	valid_0&#39;s binary_logloss: 0.480763
[60]	valid_0&#39;s binary_logloss: 0.478167
[70]	valid_0&#39;s binary_logloss: 0.477476
[80]	valid_0&#39;s binary_logloss: 0.478058
[90]	valid_0&#39;s binary_logloss: 0.478384
[100]	valid_0&#39;s binary_logloss: 0.480102
[110]	valid_0&#39;s binary_logloss: 0.480801
Early stopping, best iteration is:
[67]	valid_0&#39;s binary_logloss: 0.47717
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[129]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.externals</span> <span class="kn">import</span> <span class="n">joblib</span>
<span class="kn">from</span> <span class="nn">lightgbm</span> <span class="kn">import</span> <span class="n">LGBMClassifier</span>
 
<span class="c1"># save model</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">model</span><span class="p">,</span> <span class="s1">&#39;/content/drive/My Drive/new_model/survival_binary.pkl&#39;</span><span class="p">)</span>
 
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[129]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&#39;/content/drive/My Drive/new_model/survival_binary.pkl&#39;]</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_test</span><span class="o">=</span><span class="n">temp2</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span><span class="s1">&#39;survival_time&#39;</span><span class="p">,</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">y_test</span><span class="o">=</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[591]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">aa</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[591]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([1]), array([21996]))</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[612]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#전체 셋을 다주어 예측값 뽑아냄</span>


<span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="c1">#convert into binary values</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="nb">len</span><span class="p">(</span><span class="n">y_pred</span><span class="p">)):</span>
    <span class="k">if</span> <span class="n">y_pred</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">&gt;=</span><span class="mf">0.5</span><span class="p">:</span>       <span class="c1"># setting threshold to .5</span>
       <span class="n">y_pred</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span>
    <span class="k">else</span><span class="p">:</span>  
       <span class="n">y_pred</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">=</span><span class="mi">0</span>
<span class="c1">#Confusion |matrix</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">confusion_matrix</span>
<span class="n">cm</span> <span class="o">=</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">y_pred</span><span class="p">)</span>

<span class="c1">#Accuracy</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">accuracy_score</span>
<span class="n">accuracy</span><span class="o">=</span><span class="n">accuracy_score</span><span class="p">(</span><span class="n">y_pred</span><span class="p">,</span><span class="n">y_test</span><span class="p">)</span>

<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">f1_score</span>

<span class="n">f1</span><span class="o">=</span><span class="n">f1_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">y_pred</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">cm</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">accuracy</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">f1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[[16555  1449]
 [ 1085 20911]]
0.93665
0.9428713139146903
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[613]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">y_pred</span><span class="p">)</span>
<span class="c1">#인덱스 리셋해줘야 알맞게 들어감</span>
<span class="n">temp2</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">temp2</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">y_</span><span class="p">[</span><span class="s1">&#39;acc_id&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;acc_id&#39;</span><span class="p">]</span>
<span class="n">y_</span><span class="p">[</span><span class="s1">&#39;true&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">temp2</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span>

<span class="n">y_</span><span class="p">[</span><span class="n">y_</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
<span class="c1">#y_ 뽑기</span>
<span class="n">under64</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="c1">#survival은 y_==0인거 amount는 1인거 뽑아야됨</span>
<span class="n">under64</span><span class="p">[</span><span class="s1">&#39;acc_id&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">y_</span><span class="p">[</span><span class="n">y_</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;acc_id&#39;</span><span class="p">]</span>
<span class="c1">#under64[&#39;acc_id&#39;]=y_[y_[0]==1][&#39;acc_id&#39;]</span>
<span class="n">under64</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[613]:</div>



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
      <th>acc_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>84131</td>
    </tr>
    <tr>
      <th>7</th>
      <td>52933</td>
    </tr>
    <tr>
      <th>9</th>
      <td>7594</td>
    </tr>
    <tr>
      <th>12</th>
      <td>82754</td>
    </tr>
    <tr>
      <th>13</th>
      <td>94954</td>
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
<div class="prompt input_prompt">In&nbsp;[614]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#y_이 0인 데이터뽑아오기</span>

<span class="n">temp_under_64</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">temp_under_64</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">under64</span><span class="p">,</span><span class="n">temp3</span><span class="p">,</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="s1">&#39;acc_id&#39;</span><span class="p">)</span>
<span class="c1">#multi classification을 하기위하여</span>
<span class="c1">#temp_under_64[&#39;amount_spent&#39;]=temp_under_64[&#39;amount_spent&#39;]</span>

<span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span>

<span class="n">temp_under_64</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[614]:</div>



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
      <th>acc_id</th>
      <th>death</th>
      <th>enchant_count</th>
      <th>exp_recovery</th>
      <th>fishing</th>
      <th>game_money_change</th>
      <th>npc_kill</th>
      <th>party_exp</th>
      <th>playtime</th>
      <th>private_shop</th>
      <th>quest_exp</th>
      <th>revive</th>
      <th>rich_monster</th>
      <th>solo_exp</th>
      <th>real_day</th>
      <th>etc_cnt_x</th>
      <th>num_opponent</th>
      <th>pledge_cnt</th>
      <th>random_attacker_cnt_x</th>
      <th>random_defender_cnt_x</th>
      <th>same_pledge_cnt_x</th>
      <th>temp_cnt_x</th>
      <th>item_amount</th>
      <th>item_price</th>
      <th>combat_char_cnt</th>
      <th>combat_play_time</th>
      <th>etc_cnt_y</th>
      <th>non_combat_play_time</th>
      <th>play_char_cnt</th>
      <th>pledge_combat_cnt</th>
      <th>random_attacker_cnt_y</th>
      <th>random_defender_cnt_y</th>
      <th>same_pledge_cnt_y</th>
      <th>temp_cnt_y</th>
      <th>amount_spent_per_day</th>
      <th>class</th>
      <th>level</th>
      <th>survival_time</th>
      <th>amount_spent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>84131</td>
      <td>2.212951</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>3.647170</td>
      <td>0.343996</td>
      <td>15.802417</td>
      <td>0.071335</td>
      <td>14.490996</td>
      <td>0.422488</td>
      <td>1.611860</td>
      <td>1.978695</td>
      <td>6</td>
      <td>1.487016</td>
      <td>300</td>
      <td>0.788281</td>
      <td>21.588326</td>
      <td>16.880456</td>
      <td>0.0</td>
      <td>1.183064</td>
      <td>0.000000</td>
      <td>2.398639</td>
      <td>2.294656e+00</td>
      <td>0.821994</td>
      <td>26.309114</td>
      <td>39.141277</td>
      <td>6.604022</td>
      <td>0.023977</td>
      <td>41.610985</td>
      <td>22.401595</td>
      <td>24.207112</td>
      <td>8.369167</td>
      <td>52.915194</td>
      <td>34.609067</td>
      <td>5.315820</td>
      <td>2.625000</td>
      <td>16.000000</td>
      <td>64</td>
      <td>0.102174</td>
    </tr>
    <tr>
      <th>1</th>
      <td>52933</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.003206</td>
      <td>1.832311</td>
      <td>0.000000</td>
      <td>2.265754</td>
      <td>0.025786</td>
      <td>2.033822</td>
      <td>0.000000</td>
      <td>1</td>
      <td>10.952721</td>
      <td>28</td>
      <td>0.563058</td>
      <td>0.686901</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.918911</td>
      <td>2.636682e-07</td>
      <td>0.128039</td>
      <td>2.057091</td>
      <td>4.728223</td>
      <td>1.153757</td>
      <td>0.002201</td>
      <td>9.347134</td>
      <td>0.005464</td>
      <td>0.000000</td>
      <td>0.715313</td>
      <td>0.000000</td>
      <td>3.856439</td>
      <td>0.116174</td>
      <td>11.428571</td>
      <td>12.428571</td>
      <td>8</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7594</td>
      <td>0.737650</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2.475633</td>
      <td>-0.004807</td>
      <td>17.310982</td>
      <td>0.000000</td>
      <td>19.668526</td>
      <td>0.000000</td>
      <td>0.689041</td>
      <td>0.494674</td>
      <td>2</td>
      <td>30.646798</td>
      <td>378</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>12.398273</td>
      <td>0.000000</td>
      <td>2.396984e-08</td>
      <td>0.189695</td>
      <td>29.881956</td>
      <td>92.529771</td>
      <td>9.739693</td>
      <td>0.000000</td>
      <td>179.255649</td>
      <td>2.932241</td>
      <td>15.783037</td>
      <td>10.801232</td>
      <td>44.560163</td>
      <td>54.978975</td>
      <td>0.000000</td>
      <td>1.074074</td>
      <td>14.629630</td>
      <td>64</td>
      <td>0.202510</td>
    </tr>
    <tr>
      <th>3</th>
      <td>82754</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>1.683346</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>35.133235</td>
      <td>30.390443</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>190</td>
      <td>0.000000</td>
      <td>0.098129</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.479728</td>
      <td>7.599152e+00</td>
      <td>1.794830</td>
      <td>0.036089</td>
      <td>0.000811</td>
      <td>0.000000</td>
      <td>0.001853</td>
      <td>0.144357</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.098883</td>
      <td>0.000000</td>
      <td>4.894737</td>
      <td>11.000000</td>
      <td>54</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>94954</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>3.637378</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>0.000000</td>
      <td>276</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>6.351720</td>
      <td>11.304646</td>
      <td>3.546211</td>
      <td>0.000232</td>
      <td>16.925891</td>
      <td>0.193054</td>
      <td>5.002803</td>
      <td>2.360534</td>
      <td>7.957172</td>
      <td>9.591656</td>
      <td>0.000000</td>
      <td>3.173913</td>
      <td>16.000000</td>
      <td>8</td>
      <td>0.000000</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#라벨 개수 비슷하게 뽑기</span>

<span class="n">new_frame</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">new_frame</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span><span class="mi">65</span><span class="p">):</span>
  
  <span class="n">new_frame</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">new_frame</span><span class="p">,</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">==</span><span class="n">i</span><span class="p">][:</span><span class="mi">100</span><span class="p">],</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;outer&#39;</span><span class="p">)</span>
  <span class="c1">#new_frame=new_frame[:272]</span>
  <span class="n">new_frame</span><span class="o">.</span><span class="n">tail</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[616]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">new_frame</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[616]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16, 17,
        18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34,
        35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51,
        52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64]),
 array([1002,  100,  100,  100,  100,  100,  100,  100,  100,  100,  100,
         100,  100,  100,  100,  100,  100,  100,  100,  100,  100,  100,
         100,  100,  100,  100,  100,  100,  100,  100,  100,  100,  100,
         100,  100,  100,  100,  100,  100,  100,  100,   83,  100,  100,
          93,  100,   89,  100,   99,  100,  100,  100,   98,   96,  100,
         100,  100,  100,  100,  100,  100,  100,   85,  100]))</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[617]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="c1">#0이어서 뽑아와진 데이터 survival_time 을 그래프로 보기/ 로그 안취하는게 좋음</span>
<span class="n">new_frame</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;survival_time&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#new_frame.sort_values(&#39;amount_spent&#39;,inplace=True)</span>
<span class="n">new_frame</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">new_frame</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="c1">#new_frame[&#39;survival_time&#39;]=np.log(new_frame[&#39;survival_time&#39;]-1+new_frame[&#39;survival_time&#39;].min())</span>

<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">new_frame</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">new_frame</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">])</span>
<span class="c1">#plt.scatter(new_frame.index,new_frame</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[617]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f848cd4ac88&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
6rdkJRN0EbwAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[518]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="c1">#0이어서 뽑아와진 데이터 survival_time 을 그래프로 보기/ 로그 안취하는게 좋음</span>
<span class="n">temp_under_64</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;survival_time&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="c1">#temp_under_64.sort_values(&#39;amount_spent&#39;,inplace=True)</span>
<span class="n">temp_under_64</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">temp_under_64</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="c1">#temp_under_64[&#39;survival_time&#39;]=np.log(temp_under_64[&#39;survival_time&#39;]-1+temp_under_64[&#39;survival_time&#39;].min())</span>

<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">temp_under_64</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">])</span>
<span class="c1">#plt.scatter(temp_under_64.index,temp_under_64[&#39;amount_spent&#39;])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[518]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f848cebcc88&gt;</pre>
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
<div class="prompt input_prompt">In&nbsp;[436]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># y_ 기반으로 뽑은 데이터에 64인 개수</span>
<span class="c1">#temp_under_64[temp_under_64[&#39;survival_time&#39;]==64].shape</span>
<span class="n">temp_under_64</span><span class="p">[</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[436]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(980, 39)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[437]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#컬럼들 보기</span>
<span class="nb">print</span><span class="p">(</span><span class="n">temp_under_64</span><span class="o">.</span><span class="n">columns</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">tolist</span><span class="p">())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;acc_id&#39;, &#39;death&#39;, &#39;enchant_count&#39;, &#39;exp_recovery&#39;, &#39;fishing&#39;, &#39;game_money_change&#39;, &#39;npc_kill&#39;, &#39;party_exp&#39;, &#39;playtime&#39;, &#39;private_shop&#39;, &#39;quest_exp&#39;, &#39;revive&#39;, &#39;rich_monster&#39;, &#39;solo_exp&#39;, &#39;real_day&#39;, &#39;etc_cnt_x&#39;, &#39;num_opponent&#39;, &#39;pledge_cnt&#39;, &#39;random_attacker_cnt_x&#39;, &#39;random_defender_cnt_x&#39;, &#39;same_pledge_cnt_x&#39;, &#39;temp_cnt_x&#39;, &#39;item_amount&#39;, &#39;item_price&#39;, &#39;combat_char_cnt&#39;, &#39;combat_play_time&#39;, &#39;etc_cnt_y&#39;, &#39;non_combat_play_time&#39;, &#39;play_char_cnt&#39;, &#39;pledge_combat_cnt&#39;, &#39;random_attacker_cnt_y&#39;, &#39;random_defender_cnt_y&#39;, &#39;same_pledge_cnt_y&#39;, &#39;temp_cnt_y&#39;, &#39;amount_spent_per_day&#39;, &#39;class&#39;, &#39;level&#39;, &#39;survival_time&#39;, &#39;amount_spent&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[519]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#각 feature들이 선형적으로 되도록 전처리</span>

<span class="n">convert_log</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;fishing&#39;</span><span class="p">,</span> <span class="s1">&#39;npc_kill&#39;</span><span class="p">,</span> <span class="s1">&#39;party_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;private_shop&#39;</span><span class="p">,</span> <span class="s1">&#39;quest_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;solo_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;pledge_cnt&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;item_amount&#39;</span><span class="p">,</span> <span class="s1">&#39;item_price&#39;</span><span class="p">,</span> <span class="s1">&#39;combat_play_time&#39;</span><span class="p">,</span> <span class="s1">&#39;etc_cnt_y&#39;</span><span class="p">,</span> <span class="s1">&#39;non_combat_play_time&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;pledge_combat_cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;random_attacker_cnt_y&#39;</span><span class="p">,</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span>
<span class="n">log_convert</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">,</span> <span class="s1">&#39;exp_recovery&#39;</span><span class="p">,</span> <span class="s1">&#39;npc_kill&#39;</span><span class="p">,</span> <span class="s1">&#39;playtime&#39;</span><span class="p">,</span> <span class="s1">&#39;revive&#39;</span><span class="p">,</span> <span class="s1">&#39;rich_monster&#39;</span><span class="p">,</span> <span class="s1">&#39;num_opponent&#39;</span><span class="p">,</span> <span class="s1">&#39;real_day&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;etc_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;random_attacker_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;random_defender_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;combat_char_cnt&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;play_char_cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;random_defender_cnt_y&#39;</span> <span class="p">,</span><span class="s1">&#39;temp_cnt_y&#39;</span><span class="p">,</span> <span class="s1">&#39;class&#39;</span><span class="p">,</span> <span class="s1">&#39;level&#39;</span><span class="p">]</span>
<span class="n">log_</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;enchant_count&#39;</span><span class="p">,</span> <span class="s1">&#39;game_money_change&#39;</span><span class="p">,</span> <span class="s1">&#39;same_pledge_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;temp_cnt_x&#39;</span><span class="p">,</span>\
      <span class="s1">&#39;same_pledge_cnt_y&#39;</span><span class="p">,</span> <span class="s1">&#39;amount_spent_per_day&#39;</span><span class="p">,]</span>

<span class="n">mean_survival_time</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">mean_amount_spent</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">convert_log</span><span class="p">:</span>
  <span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="mi">1</span><span class="o">/</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="mi">1</span><span class="o">/</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
  
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">log_convert</span><span class="p">:</span>
  <span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
  
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">log_</span><span class="p">:</span>
   <span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
    
<span class="c1">#amount spent만 따로 관리</span>

<span class="c1">#temp_under_64[&#39;amount_spent&#39;]=np.log(1/temp_under_64[&#39;amount_spent&#39;]+1+1/temp_under_64[&#39;amount_spent&#39;].mean())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:9: RuntimeWarning: invalid value encountered in log
  if __name__ == &#39;__main__&#39;:
/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:15: RuntimeWarning: invalid value encountered in log
  from ipykernel import kernelapp as app
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[529]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#각 feature들이 선형적으로 되도록 전처리</span>
<span class="c1">#new_frame : 라벨 개수 맞춘거</span>

<span class="n">convert_log</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;fishing&#39;</span><span class="p">,</span> <span class="s1">&#39;npc_kill&#39;</span><span class="p">,</span> <span class="s1">&#39;party_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;private_shop&#39;</span><span class="p">,</span> <span class="s1">&#39;quest_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;solo_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;pledge_cnt&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;item_amount&#39;</span><span class="p">,</span> <span class="s1">&#39;item_price&#39;</span><span class="p">,</span> <span class="s1">&#39;combat_play_time&#39;</span><span class="p">,</span> <span class="s1">&#39;etc_cnt_y&#39;</span><span class="p">,</span> <span class="s1">&#39;non_combat_play_time&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;pledge_combat_cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;random_attacker_cnt_y&#39;</span><span class="p">,</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span>
<span class="n">log_convert</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">,</span> <span class="s1">&#39;exp_recovery&#39;</span><span class="p">,</span> <span class="s1">&#39;npc_kill&#39;</span><span class="p">,</span> <span class="s1">&#39;playtime&#39;</span><span class="p">,</span> <span class="s1">&#39;revive&#39;</span><span class="p">,</span> <span class="s1">&#39;rich_monster&#39;</span><span class="p">,</span> <span class="s1">&#39;num_opponent&#39;</span><span class="p">,</span> <span class="s1">&#39;real_day&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;etc_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;random_attacker_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;random_defender_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;combat_char_cnt&#39;</span><span class="p">,</span>\
             <span class="s1">&#39;play_char_cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;random_defender_cnt_y&#39;</span> <span class="p">,</span><span class="s1">&#39;temp_cnt_y&#39;</span><span class="p">,</span> <span class="s1">&#39;class&#39;</span><span class="p">,</span> <span class="s1">&#39;level&#39;</span><span class="p">]</span>
<span class="n">log_</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;enchant_count&#39;</span><span class="p">,</span> <span class="s1">&#39;game_money_change&#39;</span><span class="p">,</span> <span class="s1">&#39;same_pledge_cnt_x&#39;</span><span class="p">,</span> <span class="s1">&#39;temp_cnt_x&#39;</span><span class="p">,</span>\
      <span class="s1">&#39;same_pledge_cnt_y&#39;</span><span class="p">,</span> <span class="s1">&#39;amount_spent_per_day&#39;</span><span class="p">,]</span>

<span class="n">mean_survival_time</span><span class="o">=</span><span class="n">new_frame</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">mean_amount_spent</span><span class="o">=</span><span class="n">new_frame</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">convert_log</span><span class="p">:</span>
  <span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="mi">1</span><span class="o">/</span><span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="mi">1</span><span class="o">/</span><span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
  
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">log_convert</span><span class="p">:</span>
  <span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="mi">1</span><span class="o">/</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
  
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">log_</span><span class="p">:</span>
   <span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">new_frame</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>
    
<span class="c1">#amount spent만 따로 관리</span>

<span class="c1">#new_frame[&#39;amount_spent&#39;]=np.log(1/new_frame[&#39;amount_spent&#39;]+1+1/new_frame[&#39;amount_spent&#39;].mean())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:9: RuntimeWarning: invalid value encountered in log
  if __name__ == &#39;__main__&#39;:
/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:15: RuntimeWarning: invalid value encountered in log
  from ipykernel import kernelapp as app
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#amount_spent inf 제거</span>
<span class="n">temp_under_64</span><span class="p">[</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">100</span><span class="p">]</span>
<span class="n">temp_under_64</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">!=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">max</span><span class="p">()]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[442]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">vari</span><span class="o">=</span><span class="s1">&#39;amount_spent&#39;</span>

<span class="n">temp_under_64</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">vari</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">temp_under_64</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">temp_under_64</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">cur</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>

<span class="c1">#역수 후 로그</span>
<span class="c1">#cur[vari]=np.log(1/temp_under_64[vari]-1+1/temp_under_64[vari].mean())</span>

<span class="c1">#로그 후 역수</span>
<span class="c1">#cur[vari]=1/np.log(temp_under_64[vari]-1+temp_under_64[vari].mean())</span>

<span class="c1">#그냥 로그</span>
<span class="c1">#cur[vari]=np.log(temp_under_64[vari]-1+temp_under_64[vari].mean())</span>

<span class="c1">#아무것도 안함</span>
<span class="n">cur</span><span class="p">[</span><span class="n">vari</span><span class="p">]</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">vari</span><span class="p">]</span>

<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">cur</span><span class="p">[</span><span class="n">vari</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[442]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f848ea30940&gt;</pre>
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
<div class="prompt input_prompt">In&nbsp;[414]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp_under_64</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[414]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0        1.416105
1        1.417480
2        1.418163
3        1.419481
4        1.420071
5        1.420211
6        1.420311
7        1.420574
8        1.421987
9        1.422606
10       1.423040
11       1.423540
12       1.424239
13       1.424239
14       1.424702
15       1.424850
16       1.425014
17       1.425313
18       1.425638
19       1.426330
20       1.426439
21       1.426462
22       1.427215
23       1.427779
24       1.427816
25       1.427881
26       1.429229
27       1.429335
28       1.430222
29       1.430389
           ...   
22794    6.894915
22795    6.894915
22796    6.894915
22797    6.894915
22798    6.894915
22799    6.961339
22800    7.032530
22801    7.070137
22802    7.070137
22803    7.109223
22804    7.236655
22805    7.331697
22806    7.554304
22807    7.554304
22808    7.554304
22809    7.554304
22810    7.554304
22811    7.554304
22812    7.554304
22813    7.554304
22814    7.554304
22815    7.554304
22816    7.554304
22817    7.554304
22818    7.554304
22819    7.554304
22820    7.554304
22821    7.554304
22822    7.554304
22823    7.554304
Name: amount_spent, Length: 22824, dtype: float64</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#셔플</span>
<span class="c1">#temp_under_64=temp_under_64.sample(frac=1)</span>
<span class="n">new_frame</span><span class="o">=</span><span class="n">new_frame</span><span class="o">.</span><span class="n">sample</span><span class="p">(</span><span class="n">frac</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[554]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">eight</span><span class="o">=</span><span class="nb">int</span><span class="p">(</span><span class="n">temp_under_64</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">*</span><span class="mf">0.9</span><span class="p">)</span>
<span class="n">x_test</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[</span><span class="n">eight</span><span class="p">:]</span>
<span class="c1">#y_test=x_test[&#39;amount_spent&#39;]</span>
<span class="n">y_test</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span>
<span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;survival_time&#39;</span><span class="p">,</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">temp5</span><span class="o">=</span><span class="n">temp_under_64</span><span class="p">[:</span><span class="n">eight</span><span class="p">]</span>
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
<div class="prompt input_prompt">In&nbsp;[627]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#new_frame</span>
<span class="n">eight</span><span class="o">=</span><span class="nb">int</span><span class="p">(</span><span class="n">new_frame</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">*</span><span class="mf">0.9</span><span class="p">)</span>
<span class="n">x_test</span><span class="o">=</span><span class="n">new_frame</span><span class="p">[</span><span class="n">eight</span><span class="p">:]</span>
<span class="c1">#y_test=x_test[&#39;amount_spent&#39;]</span>
<span class="n">y_test</span><span class="o">=</span><span class="n">x_test</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span>
<span class="n">x_test</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;survival_time&#39;</span><span class="p">,</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">temp5</span><span class="o">=</span><span class="n">new_frame</span><span class="p">[:</span><span class="n">eight</span><span class="p">]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>


<span class="n">x_train</span><span class="p">,</span> <span class="n">x_valid</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_valid</span><span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">temp5</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>\
                                                     <span class="n">temp5</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span><span class="n">random_state</span><span class="o">=</span><span class="mi">2019</span><span class="p">,</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">)</span>

<span class="n">lgb_train</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">y_train</span><span class="p">)</span>
<span class="n">lgb_valid</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_valid</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="n">y_valid</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#멀티클래스보다 리그레션이 더 잘 맞춤</span>

<span class="n">params</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s1">&#39;boosting_type&#39;</span><span class="p">:</span> <span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
    <span class="s1">&#39;objective&#39;</span><span class="p">:</span> <span class="s1">&#39;regression_l1&#39;</span><span class="p">,</span>
    <span class="c1">#&#39;metric&#39;:&#39;mape&#39;,</span>
    <span class="s1">&#39;num_leaves&#39;</span><span class="p">:</span><span class="mi">950</span><span class="p">,</span>
    <span class="c1">#&quot;num_class&quot; : 64,</span>
    <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span> <span class="c1">#20이 최적화라고 한다.</span>
    <span class="s1">&#39;max_depth&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
    <span class="s1">&#39;max_bin&#39;</span><span class="p">:</span><span class="mi">50</span><span class="p">,</span>
    <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.05</span><span class="p">,</span>
    <span class="s1">&#39;feature_fraction&#39;</span><span class="p">:</span> <span class="mf">0.8</span><span class="p">,</span>
  
    <span class="s1">&#39;bagging_freq&#39;</span><span class="p">:</span> <span class="mi">5</span><span class="p">,</span>
    <span class="s1">&#39;num_trees&#39;</span><span class="p">:</span><span class="mi">1000</span><span class="p">,</span> <span class="c1">#이게 train 반복횟수임</span>

    <span class="s1">&#39;categorical_features&#39;</span> <span class="p">:</span> <span class="s1">&#39;auto&#39;</span>

    
<span class="p">}</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[630]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">=</span><span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span><span class="n">lgb_train</span><span class="p">,</span>
               <span class="n">valid_sets</span><span class="o">=</span><span class="n">lgb_valid</span><span class="p">,</span>
               <span class="n">verbose_eval</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span>
               <span class="n">early_stopping_rounds</span><span class="o">=</span><span class="mi">50</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/lightgbm/engine.py:118: UserWarning: Found `num_trees` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 50 rounds.
[10]	valid_0&#39;s l1: 15.8975
[20]	valid_0&#39;s l1: 14.8196
[30]	valid_0&#39;s l1: 14.2535
[40]	valid_0&#39;s l1: 13.9771
[50]	valid_0&#39;s l1: 13.8541
[60]	valid_0&#39;s l1: 13.7502
[70]	valid_0&#39;s l1: 13.6895
[80]	valid_0&#39;s l1: 13.6347
[90]	valid_0&#39;s l1: 13.6057
[100]	valid_0&#39;s l1: 13.5753
[110]	valid_0&#39;s l1: 13.5701
[120]	valid_0&#39;s l1: 13.5641
[130]	valid_0&#39;s l1: 13.548
[140]	valid_0&#39;s l1: 13.5403
[150]	valid_0&#39;s l1: 13.5394
[160]	valid_0&#39;s l1: 13.5419
[170]	valid_0&#39;s l1: 13.5414
[180]	valid_0&#39;s l1: 13.5423
[190]	valid_0&#39;s l1: 13.5482
Early stopping, best iteration is:
[146]	valid_0&#39;s l1: 13.5362
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[631]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_absolute_error</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_squared_error</span>

<span class="n">y_pred</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">x_test</span><span class="p">)</span>
<span class="c1">#y_pred=1/(np.exp(y_pred)+1+(1/mean_amount_spent))</span>
<span class="c1">#멀티클래스 분류는 이거로 해줘야함</span>

<span class="c1">#y_pred=[np.argmax(y_pred[i])+1 for i in range(y_pred.shape[0])]</span>


<span class="c1">#print(&quot;rmse : &quot;, mean_squared_error(y_valid,y_pred)**0.5)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;rmae :&quot;</span> <span class="p">,</span><span class="n">mean_absolute_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">y_pred</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>rmae : 14.156723257241612
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[536]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_test</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[536]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>2973    30
2417    24
2214    22
1940    19
4461    45
2456    24
4186    42
83       1
4817    48
4387    44
1202    12
2231    22
3912    39
6153    62
6277    63
1408    14
4771    48
2735    27
4191    42
3649    36
4903    49
5827    58
5351    54
592      6
3671    36
1067    10
4658    47
3609    36
2163    21
3789    38
        ..
0        1
5567    56
4415    44
4106    41
5557    56
4039    40
3622    36
5703    57
1011    10
1317    13
2750    27
5995    60
6097    61
4547    45
389      4
3741    37
3413    34
3490    35
4765    48
2179    22
165      2
2790    28
3516    35
2274    23
4584    46
1237    12
783      8
6293    63
587      6
4181    42
Name: survival_time, Length: 641, dtype: int64</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_pred</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">y_pred</span><span class="p">)</span>
<span class="n">y_test</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">y_test</span><span class="p">)</span>
<span class="n">y_test</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">y_test</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">y_pred</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">y_test</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span>
<span class="n">y_pred</span>
<span class="c1">#mul=y_pred[&#39;amount_spent&#39;]/y_pred[0]</span>
<span class="c1">#mul</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[451]:</div>
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
/w/CcUwWZkofIwAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[453]:</div>
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

    <div class="prompt output_prompt">Out[453]:</div>



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
      <th>0</th>
      <td>4171</td>
      <td>acc_id</td>
    </tr>
    <tr>
      <th>22</th>
      <td>4072</td>
      <td>item_amount</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3659</td>
      <td>party_exp</td>
    </tr>
    <tr>
      <th>10</th>
      <td>3598</td>
      <td>quest_exp</td>
    </tr>
    <tr>
      <th>8</th>
      <td>3526</td>
      <td>playtime</td>
    </tr>
    <tr>
      <th>35</th>
      <td>3344</td>
      <td>class</td>
    </tr>
    <tr>
      <th>13</th>
      <td>3004</td>
      <td>solo_exp</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2716</td>
      <td>item_price</td>
    </tr>
    <tr>
      <th>34</th>
      <td>2712</td>
      <td>amount_spent_per_day</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2567</td>
      <td>non_combat_play_time</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2567</td>
      <td>etc_cnt_x</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2432</td>
      <td>pledge_combat_cnt</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2349</td>
      <td>num_opponent</td>
    </tr>
    <tr>
      <th>31</th>
      <td>2191</td>
      <td>random_defender_cnt_y</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2187</td>
      <td>play_char_cnt</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2104</td>
      <td>rich_monster</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2039</td>
      <td>death</td>
    </tr>
    <tr>
      <th>33</th>
      <td>1937</td>
      <td>temp_cnt_y</td>
    </tr>
    <tr>
      <th>21</th>
      <td>1933</td>
      <td>temp_cnt_x</td>
    </tr>
    <tr>
      <th>32</th>
      <td>1932</td>
      <td>same_pledge_cnt_y</td>
    </tr>
    <tr>
      <th>24</th>
      <td>1776</td>
      <td>combat_char_cnt</td>
    </tr>
    <tr>
      <th>36</th>
      <td>1765</td>
      <td>level</td>
    </tr>
    <tr>
      <th>19</th>
      <td>1417</td>
      <td>random_defender_cnt_x</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1416</td>
      <td>real_day</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1397</td>
      <td>revive</td>
    </tr>
    <tr>
      <th>17</th>
      <td>876</td>
      <td>pledge_cnt</td>
    </tr>
    <tr>
      <th>9</th>
      <td>782</td>
      <td>private_shop</td>
    </tr>
    <tr>
      <th>4</th>
      <td>766</td>
      <td>fishing</td>
    </tr>
    <tr>
      <th>26</th>
      <td>652</td>
      <td>etc_cnt_y</td>
    </tr>
    <tr>
      <th>30</th>
      <td>519</td>
      <td>random_attacker_cnt_y</td>
    </tr>
    <tr>
      <th>18</th>
      <td>473</td>
      <td>random_attacker_cnt_x</td>
    </tr>
    <tr>
      <th>20</th>
      <td>381</td>
      <td>same_pledge_cnt_x</td>
    </tr>
    <tr>
      <th>25</th>
      <td>351</td>
      <td>combat_play_time</td>
    </tr>
    <tr>
      <th>5</th>
      <td>247</td>
      <td>game_money_change</td>
    </tr>
    <tr>
      <th>3</th>
      <td>186</td>
      <td>exp_recovery</td>
    </tr>
    <tr>
      <th>6</th>
      <td>69</td>
      <td>npc_kill</td>
    </tr>
    <tr>
      <th>2</th>
      <td>62</td>
      <td>enchant_count</td>
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
<div class="prompt input_prompt">In&nbsp;[421]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_test</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[421]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>18126    3.609236
21500    5.043261
15258    3.322875
12925    2.994614
10496    2.680631
10859    2.722802
10863    2.723069
12911    2.992546
9372     2.560719
20445    4.245348
14389    3.201847
9879     2.613283
1400     1.819875
5687     2.200077
2618     1.948126
21425    4.951465
15581    3.384174
4865     2.131406
20707    4.407248
69       1.454093
14062    3.157872
14710    3.242755
19655    4.067707
13981    3.149500
12156    2.887539
21773    5.301936
22804    7.236655
19545    4.027227
13020    3.008429
20145    4.225289
           ...   
2973     1.977961
11501    2.801529
471      1.640428
20530    4.263796
14992    3.266251
332      1.571595
17879    3.609236
19730    4.094640
4612     2.107296
15310    3.335546
1850     1.876641
22784    6.894915
7344     2.351618
11365    2.789749
9595     2.586556
9017     2.522846
16786    3.474742
11923    2.857405
11515    2.803669
8481     2.468578
20843    4.496546
4292     2.084741
19804    4.125969
6779     2.300747
14716    3.243348
12104    2.881951
16231    3.459545
931      1.768800
4793     2.124823
4378     2.091094
Name: amount_spent, Length: 2283, dtype: float64</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cur</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">new</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">])</span>
<span class="n">cur</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;playtime&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">cur</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>

<span class="n">cur</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">min</span><span class="p">())</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">])</span><span class="c1">#survival</span>
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
<span class="kn">from</span> <span class="nn">lightgbm</span> <span class="kn">import</span> <span class="n">LGBMClassifier</span>
 
<span class="c1"># save model</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">model</span><span class="p">,</span> <span class="s1">&#39;/content/drive/My Drive/new_model/survival.pkl&#39;</span><span class="p">)</span>
 
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_train</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;survival_time&#39;</span><span class="p">,</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">y_train</span><span class="o">=</span><span class="n">temp</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span>
<span class="n">y_train</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0    64
1    60
2    64
3    64
4    64
Name: survival_time, dtype: int64</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">RandomForestClassifier</span><span class="p">,</span> <span class="n">RandomForestRegressor</span><span class="p">,</span> <span class="n">ExtraTreesClassifier</span><span class="p">,</span> <span class="n">ExtraTreesRegressor</span><span class="p">,</span> <span class="n">GradientBoostingClassifier</span><span class="p">,</span><span class="n">GradientBoostingRegressor</span>
<span class="kn">from</span> <span class="nn">sklearn.linear_model</span> <span class="kn">import</span> <span class="n">LogisticRegression</span><span class="p">,</span> <span class="n">Ridge</span>
<span class="kn">from</span> <span class="nn">sklearn.decomposition</span> <span class="kn">import</span> <span class="n">PCA</span>
<span class="kn">from</span> <span class="nn">lightgbm</span> <span class="kn">import</span> <span class="n">LGBMClassifier</span>



<span class="n">models</span><span class="o">=</span><span class="p">[</span> 
            
            <span class="p">[</span><span class="n">RandomForestClassifier</span> <span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span> <span class="n">criterion</span><span class="o">=</span><span class="s2">&quot;entropy&quot;</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span> <span class="n">max_features</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>
             <span class="n">ExtraTreesClassifier</span> <span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span> <span class="n">criterion</span><span class="o">=</span><span class="s2">&quot;entropy&quot;</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span> <span class="n">max_features</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span>
             
             
             <span class="n">LGBMClassifier</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">1000</span><span class="p">,</span><span class="n">objective</span><span class="o">=</span><span class="s1">&#39;multiclass&#39;</span><span class="p">,</span><span class="n">num_leavs</span><span class="o">=</span><span class="mi">500</span><span class="p">,</span><span class="n">min_data_in_leaf</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span><span class="n">max_bin</span><span class="o">=</span><span class="mi">50</span><span class="p">,</span><span class="n">feature_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">bagging_freq</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span><span class="n">bagging_fraction</span><span class="o">=</span><span class="mf">0.8</span><span class="p">),</span>
            <span class="n">PCA</span><span class="p">(</span><span class="n">n_components</span><span class="o">=</span><span class="mi">4</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">)],</span>
            <span class="p">[</span>
             <span class="n">LGBMClassifier</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">1000</span><span class="p">)],</span>           
            
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

<span class="n">model</span><span class="o">=</span><span class="n">StackNetClassifier</span><span class="p">(</span><span class="n">models</span><span class="p">,</span> <span class="n">metric</span><span class="o">=</span><span class="s2">&quot;accuracy&quot;</span><span class="p">,</span> <span class="n">folds</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span>
	<span class="n">restacking</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span><span class="n">use_retraining</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">use_proba</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> 
	<span class="n">random_state</span><span class="o">=</span><span class="mi">12345</span><span class="p">,</span><span class="n">n_jobs</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">verbose</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

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
Input Dimensionality 1792 at Level 0 
4 models included in Level 0 
Level 0, fold 1/5 , model 0 , accuracy===0.654687 
Level 0, fold 1/5 , model 1 , accuracy===0.654375 
Level 0, fold 1/5 , model 2 , accuracy===0.358281 
=========== end of fold 1 in level 0 ===========
Level 0, fold 2/5 , model 0 , accuracy===0.642813 
Level 0, fold 2/5 , model 1 , accuracy===0.641563 
Level 0, fold 2/5 , model 2 , accuracy===0.336875 
=========== end of fold 2 in level 0 ===========
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
<span class="kn">from</span> <span class="nn">lightgbm</span> <span class="kn">import</span> <span class="n">LGBMClassifier</span>
 
<span class="c1"># save model</span>
<span class="n">joblib</span><span class="o">.</span><span class="n">dump</span><span class="p">(</span><span class="n">model</span><span class="p">,</span> <span class="s1">&#39;/content/drive/My Drive/new_model/survival_REL_params.pkl&#39;</span><span class="p">)</span>
<span class="n">output</span><span class="o">=</span><span class="n">model</span><span class="o">.</span><span class="n">predict_proba</span><span class="p">(</span><span class="n">x_valid</span><span class="p">)</span>
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

<span class="n">model_a</span><span class="o">=</span><span class="n">joblib</span><span class="o">.</span><span class="n">load</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_model/survival_REL_params.pkl&#39;</span><span class="p">)</span>
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
<span class="ansi-red-fg">FileNotFoundError</span>                         Traceback (most recent call last)
<span class="ansi-green-fg">&lt;ipython-input-29-5bd8f2bb919c&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-intense-fg ansi-bold">      1</span> <span class="ansi-green-fg">from</span> sklearn<span class="ansi-blue-fg">.</span>externals <span class="ansi-green-fg">import</span> joblib
<span class="ansi-green-intense-fg ansi-bold">      2</span> 
<span class="ansi-green-fg">----&gt; 3</span><span class="ansi-red-fg"> </span>model_a<span class="ansi-blue-fg">=</span>joblib<span class="ansi-blue-fg">.</span>load<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">&#39;/content/drive/My Drive/new_model/survival_REL_params.pkl&#39;</span><span class="ansi-blue-fg">)</span>

<span class="ansi-green-fg">/usr/local/lib/python3.6/dist-packages/joblib/numpy_pickle.py</span> in <span class="ansi-cyan-fg">load</span><span class="ansi-blue-fg">(filename, mmap_mode)</span>
<span class="ansi-green-intense-fg ansi-bold">    588</span>             obj <span class="ansi-blue-fg">=</span> _unpickle<span class="ansi-blue-fg">(</span>fobj<span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">    589</span>     <span class="ansi-green-fg">else</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-fg">--&gt; 590</span><span class="ansi-red-fg">         </span><span class="ansi-green-fg">with</span> open<span class="ansi-blue-fg">(</span>filename<span class="ansi-blue-fg">,</span> <span class="ansi-blue-fg">&#39;rb&#39;</span><span class="ansi-blue-fg">)</span> <span class="ansi-green-fg">as</span> f<span class="ansi-blue-fg">:</span>
<span class="ansi-green-intense-fg ansi-bold">    591</span>             <span class="ansi-green-fg">with</span> _read_fileobject<span class="ansi-blue-fg">(</span>f<span class="ansi-blue-fg">,</span> filename<span class="ansi-blue-fg">,</span> mmap_mode<span class="ansi-blue-fg">)</span> <span class="ansi-green-fg">as</span> fobj<span class="ansi-blue-fg">:</span>
<span class="ansi-green-intense-fg ansi-bold">    592</span>                 <span class="ansi-green-fg">if</span> isinstance<span class="ansi-blue-fg">(</span>fobj<span class="ansi-blue-fg">,</span> _basestring<span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">:</span>

<span class="ansi-red-fg">FileNotFoundError</span>: [Errno 2] No such file or directory: &#39;/content/drive/My Drive/new_model/survival_REL_params.pkl&#39;</pre>
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
<span class="n">y_pred</span> <span class="o">=</span> <span class="n">model</span><span class="o">.</span><span class="n">predict_proba</span><span class="p">(</span><span class="n">x_train</span><span class="p">)</span>
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
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[9.72675732e-05, 1.30530100e-04, 5.39551282e-05, ...,
        6.73680058e-06, 7.09324834e-06, 9.86435464e-01],
       [8.62744661e-03, 5.55733898e-03, 1.50604523e-02, ...,
        3.07416740e-03, 2.75945353e-04, 2.71020583e-01],
       [3.38657811e-03, 1.23190589e-03, 8.14909370e-04, ...,
        8.94472583e-04, 7.42015231e-04, 8.35507364e-01],
       ...,
       [6.98878101e-04, 4.89106330e-04, 1.61123188e-03, ...,
        5.38300292e-05, 1.64346536e-04, 8.78040564e-01],
       [2.82152186e-03, 1.07561824e-03, 7.14134030e-04, ...,
        6.49121762e-04, 5.31246502e-04, 8.55234847e-01],
       [1.28851904e-04, 1.28453325e-04, 3.47807327e-04, ...,
        7.82043185e-05, 1.50265338e-05, 9.75787240e-01]])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred</span><span class="o">=</span><span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">output</span><span class="p">[</span><span class="n">i</span><span class="p">])</span><span class="o">+</span><span class="mi">1</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">40000</span><span class="p">)]</span>

<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_absolute_error</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;rmae;&quot;</span><span class="p">,</span> <span class="n">mean_absolute_error</span><span class="p">(</span><span class="n">y_valid</span><span class="p">,</span><span class="n">pred</span><span class="p">))</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cd</span> <span class="s1">&#39;/content/pystacknet&#39;</span>
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
copying pystacknet/__init__.py -&gt; build/lib/pystacknet
copying pystacknet/pystacknet.py -&gt; build/lib/pystacknet
copying pystacknet/metrics.py -&gt; build/lib/pystacknet
creating build/lib/pystacknet/test
copying pystacknet/test/__init__.py -&gt; build/lib/pystacknet/test
copying pystacknet/test/test_amazon.py -&gt; build/lib/pystacknet/test
copying pystacknet/test/test_pystacknet.py -&gt; build/lib/pystacknet/test
creating build/bdist.linux-x86_64
creating build/bdist.linux-x86_64/egg
creating build/bdist.linux-x86_64/egg/pystacknet
copying build/lib/pystacknet/__init__.py -&gt; build/bdist.linux-x86_64/egg/pystacknet
copying build/lib/pystacknet/pystacknet.py -&gt; build/bdist.linux-x86_64/egg/pystacknet
creating build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/test/__init__.py -&gt; build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/test/test_amazon.py -&gt; build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/test/test_pystacknet.py -&gt; build/bdist.linux-x86_64/egg/pystacknet/test
copying build/lib/pystacknet/metrics.py -&gt; build/bdist.linux-x86_64/egg/pystacknet
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/__init__.py to __init__.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/pystacknet.py to pystacknet.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/test/__init__.py to __init__.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/test/test_amazon.py to test_amazon.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/test/test_pystacknet.py to test_pystacknet.cpython-36.pyc
byte-compiling build/bdist.linux-x86_64/egg/pystacknet/metrics.py to metrics.cpython-36.pyc
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
Searching for numpy==1.16.4
Best match: numpy 1.16.4
Adding numpy 1.16.4 to easy-install.pth file
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aa</span><span class="o">=</span><span class="n">merged</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[489]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">aa</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span><span class="n">return_counts</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[489]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16, 17,
        18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34,
        35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51,
        52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64]),
 array([ 1012,   483,   719,   712,   269,   264,   262,  1219,   343,
          462,   309,   198,   230,   244,   341,   348,   337,   369,
          273,   299,   335,   499,   436,   215,   190,   200,   248,
          243,  1500,   159,   233,   170,   153,   172,   179,   476,
          229,   120,   206,   198,   122,    89,   154,   170,   102,
          189,    98,   132,   114,   206,   131,   126,   118,   113,
          122,   128,   208,   212,   132,   145,   123,   124,    92,
        21996]))</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[484]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">help</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Help on function unique in module numpy:

unique(ar, return_index=False, return_inverse=False, return_counts=False, axis=None)
    Find the unique elements of an array.
    
    Returns the sorted unique elements of an array. There are three optional
    outputs in addition to the unique elements:
    
    * the indices of the input array that give the unique values
    * the indices of the unique array that reconstruct the input array
    * the number of times each unique value comes up in the input array
    
    Parameters
    ----------
    ar : array_like
        Input array. Unless `axis` is specified, this will be flattened if it
        is not already 1-D.
    return_index : bool, optional
        If True, also return the indices of `ar` (along the specified axis,
        if provided, or in the flattened array) that result in the unique array.
    return_inverse : bool, optional
        If True, also return the indices of the unique array (for the specified
        axis, if provided) that can be used to reconstruct `ar`.
    return_counts : bool, optional
        If True, also return the number of times each unique item appears
        in `ar`.
    
        .. versionadded:: 1.9.0
    
    axis : int or None, optional
        The axis to operate on. If None, `ar` will be flattened. If an integer,
        the subarrays indexed by the given axis will be flattened and treated
        as the elements of a 1-D array with the dimension of the given axis,
        see the notes for more details.  Object arrays or structured arrays
        that contain objects are not supported if the `axis` kwarg is used. The
        default is None.
    
        .. versionadded:: 1.13.0
    
    Returns
    -------
    unique : ndarray
        The sorted unique values.
    unique_indices : ndarray, optional
        The indices of the first occurrences of the unique values in the
        original array. Only provided if `return_index` is True.
    unique_inverse : ndarray, optional
        The indices to reconstruct the original array from the
        unique array. Only provided if `return_inverse` is True.
    unique_counts : ndarray, optional
        The number of times each of the unique values comes up in the
        original array. Only provided if `return_counts` is True.
    
        .. versionadded:: 1.9.0
    
    See Also
    --------
    numpy.lib.arraysetops : Module with a number of other functions for
                            performing set operations on arrays.
    
    Notes
    -----
    When an axis is specified the subarrays indexed by the axis are sorted.
    This is done by making the specified axis the first dimension of the array
    and then flattening the subarrays in C order. The flattened subarrays are
    then viewed as a structured type with each element given a label, with the
    effect that we end up with a 1-D array of structured types that can be
    treated in the same way as any other 1-D array. The result is that the
    flattened subarrays are sorted in lexicographic order starting with the
    first element.
    
    Examples
    --------
    &gt;&gt;&gt; np.unique([1, 1, 2, 2, 3, 3])
    array([1, 2, 3])
    &gt;&gt;&gt; a = np.array([[1, 1], [2, 3]])
    &gt;&gt;&gt; np.unique(a)
    array([1, 2, 3])
    
    Return the unique rows of a 2D array
    
    &gt;&gt;&gt; a = np.array([[1, 0, 0], [1, 0, 0], [2, 3, 4]])
    &gt;&gt;&gt; np.unique(a, axis=0)
    array([[1, 0, 0], [2, 3, 4]])
    
    Return the indices of the original array that give the unique values:
    
    &gt;&gt;&gt; a = np.array([&#39;a&#39;, &#39;b&#39;, &#39;b&#39;, &#39;c&#39;, &#39;a&#39;])
    &gt;&gt;&gt; u, indices = np.unique(a, return_index=True)
    &gt;&gt;&gt; u
    array([&#39;a&#39;, &#39;b&#39;, &#39;c&#39;],
           dtype=&#39;|S1&#39;)
    &gt;&gt;&gt; indices
    array([0, 1, 3])
    &gt;&gt;&gt; a[indices]
    array([&#39;a&#39;, &#39;b&#39;, &#39;c&#39;],
           dtype=&#39;|S1&#39;)
    
    Reconstruct the input array from the unique values:
    
    &gt;&gt;&gt; a = np.array([1, 2, 6, 4, 2, 3, 2])
    &gt;&gt;&gt; u, indices = np.unique(a, return_inverse=True)
    &gt;&gt;&gt; u
    array([1, 2, 3, 4, 6])
    &gt;&gt;&gt; indices
    array([0, 1, 4, 3, 1, 2, 1])
    &gt;&gt;&gt; u[indices]
    array([1, 2, 6, 4, 2, 3, 2])

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
    </div>
  </div>
</body>

 


</html>
