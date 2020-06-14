---
layout: post
title: Big Contest - Linearization (Log)
date: 2020-06-14
description: READ ME
thumbnail: building1.jpg
categories: BigContest

# Information for the author block
author : Loui
---


<html>
<head><meta charset="utf-8" />

<title>linearization</title>

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
<pre>Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount(&#34;/content/drive&#34;, force_remount=True).
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[676]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/loged.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[676]:</div>



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
      <td>0</td>
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
      <td>1</td>
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
      <td>2</td>
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
      <td>3</td>
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
      <td>4</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp2</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_model/nam_40000_total.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[678]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/row40000.csv&#39;</span><span class="p">,</span><span class="n">engine</span><span class="o">=</span><span class="s1">&#39;python&#39;</span><span class="p">)</span>
<span class="n">temp</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[678]:</div>



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
      <td>0</td>
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
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
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
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
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
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
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
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
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
<div class="prompt input_prompt">In&nbsp;[702]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">new</span><span class="o">=</span><span class="n">temp</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="c1">#new=pd.merge(new,label,how=&#39;left&#39;,on=&#39;acc_id&#39;)</span>
<span class="n">new</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">new</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[702]:</div>



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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">new</span><span class="p">[</span><span class="n">new</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(16438, 39)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[704]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#new.drop([&#39;class&#39;,&#39;level&#39;],axis=1,inplace=True)</span>
<span class="n">col_list</span><span class="o">=</span><span class="n">new</span><span class="o">.</span><span class="n">columns</span>

<span class="n">col_list</span><span class="o">=</span><span class="n">col_list</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span><span class="s1">&#39;playtime&#39;</span><span class="p">,</span><span class="s1">&#39;class&#39;</span><span class="p">,</span><span class="s1">&#39;level&#39;</span><span class="p">,</span><span class="s1">&#39;0&#39;</span><span class="p">,</span> <span class="s1">&#39;1&#39;</span><span class="p">,</span> <span class="s1">&#39;2&#39;</span><span class="p">,</span> <span class="s1">&#39;3&#39;</span><span class="p">,</span> <span class="s1">&#39;4&#39;</span><span class="p">,</span> <span class="s1">&#39;5&#39;</span><span class="p">,</span> <span class="s1">&#39;6&#39;</span><span class="p">,</span> <span class="s1">&#39;7&#39;</span><span class="p">,</span> <span class="s1">&#39;afternoon&#39;</span><span class="p">,</span><span class="s1">&#39;dawn&#39;</span><span class="p">,</span><span class="s1">&#39;maxServerOfAcc&#39;</span><span class="p">,</span><span class="s1">&#39;min_level&#39;</span><span class="p">,</span> <span class="s1">&#39;morning&#39;</span><span class="p">,</span> <span class="s1">&#39;pledge_importance&#39;</span><span class="p">,</span> <span class="s1">&#39;week_cnt&#39;</span><span class="p">,</span><span class="s1">&#39;survival_time&#39;</span><span class="p">,</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">])</span>
<span class="n">col_list</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[704]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Index([&#39;death&#39;, &#39;enchant_count&#39;, &#39;exp_recovery&#39;, &#39;fishing&#39;,
       &#39;game_money_change&#39;, &#39;npc_kill&#39;, &#39;party_exp&#39;, &#39;private_shop&#39;,
       &#39;quest_exp&#39;, &#39;revive&#39;, &#39;rich_monster&#39;, &#39;solo_exp&#39;, &#39;real_day&#39;,
       &#39;etc_cnt_x&#39;, &#39;num_opponent&#39;, &#39;pledge_cnt&#39;, &#39;random_attacker_cnt_x&#39;,
       &#39;random_defender_cnt_x&#39;, &#39;same_pledge_cnt_x&#39;, &#39;temp_cnt_x&#39;,
       &#39;item_amount&#39;, &#39;item_price&#39;, &#39;combat_char_cnt&#39;, &#39;combat_play_time&#39;,
       &#39;etc_cnt_y&#39;, &#39;non_combat_play_time&#39;, &#39;play_char_cnt&#39;,
       &#39;pledge_combat_cnt&#39;, &#39;random_attacker_cnt_y&#39;, &#39;random_defender_cnt_y&#39;,
       &#39;same_pledge_cnt_y&#39;, &#39;temp_cnt_y&#39;, &#39;amount_spent_per_day&#39;, &#39;class_cnt&#39;,
       &#39;level_range0&#39;, &#39;level_range1&#39;, &#39;level_range2&#39;, &#39;level_range3&#39;,
       &#39;level_range4&#39;, &#39;max_level&#39;],
      dtype=&#39;object&#39;)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[691]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">new</span><span class="o">.</span><span class="n">columns</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">tolist</span><span class="p">())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;acc_id&#39;, &#39;death&#39;, &#39;enchant_count&#39;, &#39;exp_recovery&#39;, &#39;fishing&#39;, &#39;game_money_change&#39;, &#39;npc_kill&#39;, &#39;party_exp&#39;, &#39;playtime&#39;, &#39;private_shop&#39;, &#39;quest_exp&#39;, &#39;revive&#39;, &#39;rich_monster&#39;, &#39;solo_exp&#39;, &#39;real_day&#39;, &#39;etc_cnt_x&#39;, &#39;num_opponent&#39;, &#39;pledge_cnt&#39;, &#39;random_attacker_cnt_x&#39;, &#39;random_defender_cnt_x&#39;, &#39;same_pledge_cnt_x&#39;, &#39;temp_cnt_x&#39;, &#39;item_amount&#39;, &#39;item_price&#39;, &#39;combat_char_cnt&#39;, &#39;combat_play_time&#39;, &#39;etc_cnt_y&#39;, &#39;non_combat_play_time&#39;, &#39;play_char_cnt&#39;, &#39;pledge_combat_cnt&#39;, &#39;random_attacker_cnt_y&#39;, &#39;random_defender_cnt_y&#39;, &#39;same_pledge_cnt_y&#39;, &#39;temp_cnt_y&#39;, &#39;amount_spent_per_day&#39;, &#39;class&#39;, &#39;level&#39;, &#39;0&#39;, &#39;1&#39;, &#39;2&#39;, &#39;3&#39;, &#39;4&#39;, &#39;5&#39;, &#39;6&#39;, &#39;7&#39;, &#39;afternoon&#39;, &#39;amount_spent&#39;, &#39;class_cnt&#39;, &#39;dawn&#39;, &#39;level_range0&#39;, &#39;level_range1&#39;, &#39;level_range2&#39;, &#39;level_range3&#39;, &#39;level_range4&#39;, &#39;maxServerOfAcc&#39;, &#39;max_level&#39;, &#39;min_level&#39;, &#39;morning&#39;, &#39;pledge_importance&#39;, &#39;survival_time&#39;, &#39;week_cnt&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[705]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">col_list</span><span class="p">:</span>
  <span class="n">new</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">new</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">new</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">())</span>

<span class="n">new</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:3: RuntimeWarning: invalid value encountered in log
  This is separate from the ipykernel package so we can avoid doing imports until
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[705]:</div>



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
      <td>2</td>
      <td>0.675939</td>
      <td>NaN</td>
      <td>0.244889</td>
      <td>1.910799</td>
      <td>NaN</td>
      <td>2.934524</td>
      <td>1.427837</td>
      <td>91.533663</td>
      <td>4.547821</td>
      <td>1.172883</td>
      <td>0.503349</td>
      <td>1.371441</td>
      <td>2.121855</td>
      <td>6.585755</td>
      <td>1.924804</td>
      <td>2.239612</td>
      <td>1.570491</td>
      <td>-0.570605</td>
      <td>1.244709</td>
      <td>0.356199</td>
      <td>0.513446</td>
      <td>1.157584</td>
      <td>0.429484</td>
      <td>2.524802</td>
      <td>3.394050</td>
      <td>2.670516</td>
      <td>-4.773437</td>
      <td>3.519788</td>
      <td>1.744948</td>
      <td>1.877961</td>
      <td>1.795066</td>
      <td>1.920833</td>
      <td>2.767090</td>
      <td>-2.373253</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.972983</td>
      <td>1.0</td>
      <td>-0.318347</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>-0.534435</td>
      <td>-0.865063</td>
      <td>20</td>
      <td>2.542725</td>
      <td>0</td>
      <td>1.000000</td>
      <td>1.750000</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>0.793789</td>
      <td>NaN</td>
      <td>0.244889</td>
      <td>2.322525</td>
      <td>NaN</td>
      <td>3.093267</td>
      <td>1.582058</td>
      <td>6.116132</td>
      <td>2.253991</td>
      <td>1.206674</td>
      <td>0.642690</td>
      <td>2.560402</td>
      <td>2.351570</td>
      <td>5.923447</td>
      <td>1.924804</td>
      <td>2.250009</td>
      <td>1.570491</td>
      <td>-0.570605</td>
      <td>1.244709</td>
      <td>0.356199</td>
      <td>0.765825</td>
      <td>1.157647</td>
      <td>0.670672</td>
      <td>2.644496</td>
      <td>3.552027</td>
      <td>2.725328</td>
      <td>-4.354188</td>
      <td>3.672115</td>
      <td>1.744948</td>
      <td>2.137324</td>
      <td>1.938710</td>
      <td>1.920833</td>
      <td>2.916863</td>
      <td>-2.373253</td>
      <td>3.600000</td>
      <td>15.000000</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.666667</td>
      <td>0.000000</td>
      <td>2.157077</td>
      <td>0.0</td>
      <td>-0.318347</td>
      <td>-1.041571</td>
      <td>NaN</td>
      <td>-0.534435</td>
      <td>0.351378</td>
      <td>16</td>
      <td>3.321948</td>
      <td>1</td>
      <td>0.666667</td>
      <td>3.333333</td>
      <td>60</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>4.542510</td>
      <td>NaN</td>
      <td>0.244889</td>
      <td>2.448097</td>
      <td>NaN</td>
      <td>3.911726</td>
      <td>1.427837</td>
      <td>18.797802</td>
      <td>2.253991</td>
      <td>1.567021</td>
      <td>4.544977</td>
      <td>1.781882</td>
      <td>3.684765</td>
      <td>6.585755</td>
      <td>2.048299</td>
      <td>2.520248</td>
      <td>1.596835</td>
      <td>1.576100</td>
      <td>1.537940</td>
      <td>0.356199</td>
      <td>1.706358</td>
      <td>1.727234</td>
      <td>0.462791</td>
      <td>4.255897</td>
      <td>5.115993</td>
      <td>4.328122</td>
      <td>-3.163584</td>
      <td>5.459941</td>
      <td>2.133330</td>
      <td>3.693168</td>
      <td>3.323791</td>
      <td>3.590941</td>
      <td>4.685532</td>
      <td>0.404011</td>
      <td>17.321429</td>
      <td>15.964286</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0.500000</td>
      <td>0.020310</td>
      <td>1.293583</td>
      <td>0.5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.720263</td>
      <td>2.004317</td>
      <td>14</td>
      <td>3.357394</td>
      <td>11</td>
      <td>0.000000</td>
      <td>2.500000</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>1.304830</td>
      <td>NaN</td>
      <td>0.244889</td>
      <td>3.032519</td>
      <td>NaN</td>
      <td>3.897303</td>
      <td>2.564393</td>
      <td>28.464708</td>
      <td>2.253991</td>
      <td>1.714457</td>
      <td>1.219534</td>
      <td>3.216514</td>
      <td>2.868039</td>
      <td>6.585755</td>
      <td>2.018825</td>
      <td>2.376160</td>
      <td>1.570491</td>
      <td>-0.570605</td>
      <td>1.764397</td>
      <td>2.626563</td>
      <td>1.615248</td>
      <td>1.817190</td>
      <td>2.171304</td>
      <td>3.531585</td>
      <td>4.558916</td>
      <td>3.294421</td>
      <td>-4.773437</td>
      <td>4.654815</td>
      <td>1.826464</td>
      <td>2.758181</td>
      <td>2.826878</td>
      <td>2.130382</td>
      <td>3.964554</td>
      <td>-2.373253</td>
      <td>1.214286</td>
      <td>16.000000</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>0.070642</td>
      <td>1.293583</td>
      <td>1.0</td>
      <td>-0.318347</td>
      <td>-1.041571</td>
      <td>NaN</td>
      <td>0.950112</td>
      <td>0.351378</td>
      <td>16</td>
      <td>3.357394</td>
      <td>1</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>20</td>
      <td>1.081605</td>
      <td>NaN</td>
      <td>0.244889</td>
      <td>2.402815</td>
      <td>NaN</td>
      <td>3.968644</td>
      <td>1.446856</td>
      <td>25.588043</td>
      <td>2.521173</td>
      <td>1.198391</td>
      <td>0.972142</td>
      <td>2.479980</td>
      <td>2.154260</td>
      <td>6.546352</td>
      <td>3.148243</td>
      <td>2.970258</td>
      <td>1.807091</td>
      <td>-0.570605</td>
      <td>1.537940</td>
      <td>0.356199</td>
      <td>0.765825</td>
      <td>1.880140</td>
      <td>3.092693</td>
      <td>3.637680</td>
      <td>4.566827</td>
      <td>4.075101</td>
      <td>-4.773437</td>
      <td>4.484912</td>
      <td>2.616666</td>
      <td>2.918560</td>
      <td>2.533757</td>
      <td>2.888519</td>
      <td>3.790797</td>
      <td>-0.010345</td>
      <td>5.851852</td>
      <td>17.000000</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1.000000</td>
      <td>0.052137</td>
      <td>1.293583</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>-0.485848</td>
      <td>-0.534435</td>
      <td>0.351378</td>
      <td>6</td>
      <td>3.391628</td>
      <td>6</td>
      <td>1.000000</td>
      <td>1.750000</td>
      <td>64</td>
      <td>4.0</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">new</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_model/loged_final.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">,</span><span class="n">index</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">new</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">new</span><span class="p">[</span><span class="s1">&#39;fishing&#39;</span><span class="p">])</span>

  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f242f834a90&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
aRggKYsAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[683]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">temp2</span><span class="o">.</span><span class="n">columns</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">tolist</span><span class="p">())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;Unnamed: 0&#39;, &#39;acc_id&#39;, &#39;pledge_random_attacker_cnt_min&#39;, &#39;party_exp_min&#39;, &#39;combat_play_time_min&#39;, &#39;fishing_min&#39;, &#39;amount_spent_min&#39;, &#39;pledge_play_char_cnt_mean_min&#39;, &#39;playtime_min&#39;, &#39;pledge_same_pledge_cnt_min&#39;, &#39;solo_exp_min&#39;, &#39;num_opponent_min&#39;, &#39;combat_temp_cnt_min&#39;, &#39;quest_exp_min&#39;, &#39;combat_random_defender_cnt_min&#39;, &#39;combat_etc_cnt_min&#39;, &#39;item_amount_min&#39;, &#39;combat_pledge_cnt_min&#39;, &#39;total_exp_min&#39;, &#39;pledge_char_cnt_mean_min&#39;, &#39;revive_min&#39;, &#39;death_min&#39;, &#39;boss_monster_min&#39;, &#39;pledge_random_defender_cnt_min&#39;, &#39;pledge_temp_cnt_min&#39;, &#39;game_money_change_min&#39;, &#39;exp_recovery_min&#39;, &#39;combat_random_attacker_cnt_min&#39;, &#39;non_combat_play_time_min&#39;, &#39;private_shop_min&#39;, &#39;pledge_etc_cnt_min&#39;, &#39;npc_kill_min&#39;, &#39;level_min&#39;, &#39;enchant_count_min&#39;, &#39;item_price_min&#39;, &#39;combat_same_pledge_cnt_min&#39;, &#39;pledge_random_attacker_cnt_mean&#39;, &#39;party_exp_mean&#39;, &#39;combat_play_time_mean&#39;, &#39;fishing_mean&#39;, &#39;amount_spent_mean&#39;, &#39;pledge_play_char_cnt_mean_mean&#39;, &#39;playtime_mean&#39;, &#39;pledge_same_pledge_cnt_mean&#39;, &#39;solo_exp_mean&#39;, &#39;num_opponent_mean&#39;, &#39;combat_temp_cnt_mean&#39;, &#39;quest_exp_mean&#39;, &#39;combat_random_defender_cnt_mean&#39;, &#39;combat_etc_cnt_mean&#39;, &#39;item_amount_mean&#39;, &#39;combat_pledge_cnt_mean&#39;, &#39;total_exp_mean&#39;, &#39;pledge_char_cnt_mean_mean&#39;, &#39;revive_mean&#39;, &#39;death_mean&#39;, &#39;boss_monster_mean&#39;, &#39;pledge_random_defender_cnt_mean&#39;, &#39;pledge_temp_cnt_mean&#39;, &#39;game_money_change_mean&#39;, &#39;exp_recovery_mean&#39;, &#39;combat_random_attacker_cnt_mean&#39;, &#39;non_combat_play_time_mean&#39;, &#39;private_shop_mean&#39;, &#39;pledge_etc_cnt_mean&#39;, &#39;npc_kill_mean&#39;, &#39;level_mean&#39;, &#39;enchant_count_mean&#39;, &#39;item_price_mean&#39;, &#39;combat_same_pledge_cnt_mean&#39;, &#39;pledge_random_attacker_cnt_max&#39;, &#39;party_exp_max&#39;, &#39;combat_play_time_max&#39;, &#39;fishing_max&#39;, &#39;amount_spent_max&#39;, &#39;pledge_play_char_cnt_mean_max&#39;, &#39;playtime_max&#39;, &#39;pledge_same_pledge_cnt_max&#39;, &#39;solo_exp_max&#39;, &#39;num_opponent_max&#39;, &#39;combat_temp_cnt_max&#39;, &#39;quest_exp_max&#39;, &#39;combat_random_defender_cnt_max&#39;, &#39;combat_etc_cnt_max&#39;, &#39;item_amount_max&#39;, &#39;combat_pledge_cnt_max&#39;, &#39;total_exp_max&#39;, &#39;pledge_char_cnt_mean_max&#39;, &#39;revive_max&#39;, &#39;death_max&#39;, &#39;boss_monster_max&#39;, &#39;pledge_random_defender_cnt_max&#39;, &#39;pledge_temp_cnt_max&#39;, &#39;game_money_change_max&#39;, &#39;exp_recovery_max&#39;, &#39;combat_random_attacker_cnt_max&#39;, &#39;non_combat_play_time_max&#39;, &#39;private_shop_max&#39;, &#39;pledge_etc_cnt_max&#39;, &#39;npc_kill_max&#39;, &#39;level_max&#39;, &#39;enchant_count_max&#39;, &#39;item_price_max&#39;, &#39;combat_same_pledge_cnt_max&#39;, &#39;pledge_random_attacker_cnt_sum&#39;, &#39;party_exp_sum&#39;, &#39;combat_play_time_sum&#39;, &#39;fishing_sum&#39;, &#39;amount_spent_sum&#39;, &#39;pledge_play_char_cnt_mean_sum&#39;, &#39;playtime_sum&#39;, &#39;pledge_same_pledge_cnt_sum&#39;, &#39;solo_exp_sum&#39;, &#39;num_opponent_sum&#39;, &#39;combat_temp_cnt_sum&#39;, &#39;quest_exp_sum&#39;, &#39;combat_random_defender_cnt_sum&#39;, &#39;combat_etc_cnt_sum&#39;, &#39;item_amount_sum&#39;, &#39;combat_pledge_cnt_sum&#39;, &#39;total_exp_sum&#39;, &#39;pledge_char_cnt_mean_sum&#39;, &#39;revive_sum&#39;, &#39;death_sum&#39;, &#39;boss_monster_sum&#39;, &#39;pledge_random_defender_cnt_sum&#39;, &#39;pledge_temp_cnt_sum&#39;, &#39;game_money_change_sum&#39;, &#39;exp_recovery_sum&#39;, &#39;combat_random_attacker_cnt_sum&#39;, &#39;non_combat_play_time_sum&#39;, &#39;private_shop_sum&#39;, &#39;pledge_etc_cnt_sum&#39;, &#39;npc_kill_sum&#39;, &#39;level_sum&#39;, &#39;enchant_count_sum&#39;, &#39;item_price_sum&#39;, &#39;combat_same_pledge_cnt_sum&#39;, &#39;0&#39;, &#39;1&#39;, &#39;2&#39;, &#39;3&#39;, &#39;4&#39;, &#39;5&#39;, &#39;6&#39;, &#39;7&#39;, &#39;afternoon&#39;, &#39;amount_spent&#39;, &#39;class_cnt&#39;, &#39;dawn&#39;, &#39;level_range0&#39;, &#39;level_range1&#39;, &#39;level_range2&#39;, &#39;level_range3&#39;, &#39;level_range4&#39;, &#39;maxServerOfAcc&#39;, &#39;max_level&#39;, &#39;min_level&#39;, &#39;morning&#39;, &#39;pledge_importance&#39;, &#39;survival_time&#39;, &#39;week_cnt&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[703]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aa</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">aa</span><span class="o">=</span><span class="n">temp2</span><span class="p">[[</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span> <span class="s1">&#39;0&#39;</span><span class="p">,</span> <span class="s1">&#39;1&#39;</span><span class="p">,</span> <span class="s1">&#39;2&#39;</span><span class="p">,</span> <span class="s1">&#39;3&#39;</span><span class="p">,</span> <span class="s1">&#39;4&#39;</span><span class="p">,</span> <span class="s1">&#39;5&#39;</span><span class="p">,</span> <span class="s1">&#39;6&#39;</span><span class="p">,</span> <span class="s1">&#39;7&#39;</span><span class="p">,</span> <span class="s1">&#39;afternoon&#39;</span><span class="p">,</span> <span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span> <span class="s1">&#39;class_cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;dawn&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range0&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range1&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range2&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range3&#39;</span><span class="p">,</span> <span class="s1">&#39;level_range4&#39;</span><span class="p">,</span> <span class="s1">&#39;maxServerOfAcc&#39;</span><span class="p">,</span> <span class="s1">&#39;max_level&#39;</span><span class="p">,</span> <span class="s1">&#39;min_level&#39;</span><span class="p">,</span> <span class="s1">&#39;morning&#39;</span><span class="p">,</span> <span class="s1">&#39;pledge_importance&#39;</span><span class="p">,</span> <span class="s1">&#39;survival_time&#39;</span><span class="p">,</span> <span class="s1">&#39;week_cnt&#39;</span><span class="p">]]</span>
<span class="n">new</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">new</span><span class="p">,</span><span class="n">aa</span><span class="p">,</span><span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span><span class="n">on</span><span class="o">=</span><span class="s1">&#39;acc_id&#39;</span><span class="p">)</span>
<span class="n">new</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[703]:</div>



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
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1</td>
      <td>1.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>20</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>1.750000</td>
      <td>64</td>
      <td>4.0</td>
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
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.666667</td>
      <td>0.000000</td>
      <td>7</td>
      <td>0.0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>15</td>
      <td>1</td>
      <td>0.666667</td>
      <td>3.333333</td>
      <td>60</td>
      <td>3.0</td>
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
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0.500000</td>
      <td>0.020310</td>
      <td>2</td>
      <td>0.5</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>5</td>
      <td>7</td>
      <td>14</td>
      <td>16</td>
      <td>11</td>
      <td>0.000000</td>
      <td>2.500000</td>
      <td>64</td>
      <td>4.0</td>
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
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>0.070642</td>
      <td>2</td>
      <td>1.0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>16</td>
      <td>16</td>
      <td>1</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>64</td>
      <td>4.0</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1.000000</td>
      <td>0.052137</td>
      <td>2</td>
      <td>1.0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>6</td>
      <td>17</td>
      <td>6</td>
      <td>1.000000</td>
      <td>1.750000</td>
      <td>64</td>
      <td>4.0</td>
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
<div class="prompt input_prompt">In&nbsp;[688]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">new</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[688]:</div>



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
      <td>2</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>NaN</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>91.533663</td>
      <td>4.441483</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>6.006353</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-16.853322</td>
      <td>-4.296833</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1</td>
      <td>1.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>20</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>1.750000</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>-1.402898</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>1.236317</td>
      <td>-1.930012</td>
      <td>1.174478</td>
      <td>-0.363433</td>
      <td>6.116132</td>
      <td>-inf</td>
      <td>-2.197734</td>
      <td>-1.397004</td>
      <td>2.197225</td>
      <td>0.767992</td>
      <td>4.007333</td>
      <td>-inf</td>
      <td>-2.321475</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>-0.734536</td>
      <td>-8.509887</td>
      <td>-0.837717</td>
      <td>0.462431</td>
      <td>1.628771</td>
      <td>-0.205794</td>
      <td>-5.425792</td>
      <td>1.715194</td>
      <td>-inf</td>
      <td>0.660918</td>
      <td>-0.072670</td>
      <td>-inf</td>
      <td>0.944279</td>
      <td>-inf</td>
      <td>3.600000</td>
      <td>15.000000</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.666667</td>
      <td>0.000000</td>
      <td>7</td>
      <td>0.0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>15</td>
      <td>1</td>
      <td>0.666667</td>
      <td>3.333333</td>
      <td>60</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>4.521358</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>1.570244</td>
      <td>-3.894539</td>
      <td>3.439540</td>
      <td>-inf</td>
      <td>18.797802</td>
      <td>-inf</td>
      <td>0.445362</td>
      <td>4.527252</td>
      <td>0.693147</td>
      <td>3.449643</td>
      <td>6.006353</td>
      <td>-0.104370</td>
      <td>1.112512</td>
      <td>-2.052850</td>
      <td>1.451819</td>
      <td>0.168108</td>
      <td>-inf</td>
      <td>1.344905</td>
      <td>0.893161</td>
      <td>-2.723441</td>
      <td>4.060988</td>
      <td>4.919104</td>
      <td>4.116667</td>
      <td>-3.386624</td>
      <td>5.304827</td>
      <td>0.999650</td>
      <td>3.515470</td>
      <td>3.079408</td>
      <td>3.382406</td>
      <td>4.526729</td>
      <td>0.339784</td>
      <td>17.321429</td>
      <td>15.964286</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0.500000</td>
      <td>0.020310</td>
      <td>2</td>
      <td>0.5</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>5</td>
      <td>7</td>
      <td>14</td>
      <td>16</td>
      <td>11</td>
      <td>0.000000</td>
      <td>2.500000</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>0.543013</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>2.638411</td>
      <td>NaN</td>
      <td>3.416311</td>
      <td>2.177373</td>
      <td>28.464708</td>
      <td>-inf</td>
      <td>0.842586</td>
      <td>0.548906</td>
      <td>3.044522</td>
      <td>2.225256</td>
      <td>6.006353</td>
      <td>-0.392052</td>
      <td>0.317582</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>0.861255</td>
      <td>2.517557</td>
      <td>1.211374</td>
      <td>1.089338</td>
      <td>1.980569</td>
      <td>3.076837</td>
      <td>4.185001</td>
      <td>2.526878</td>
      <td>-inf</td>
      <td>4.267072</td>
      <td>-0.720974</td>
      <td>2.222565</td>
      <td>2.386261</td>
      <td>0.464636</td>
      <td>3.605076</td>
      <td>-inf</td>
      <td>1.214286</td>
      <td>16.000000</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1.000000</td>
      <td>0.070642</td>
      <td>2</td>
      <td>1.0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>16</td>
      <td>16</td>
      <td>1</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>64</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>20</td>
      <td>-0.016603</td>
      <td>-inf</td>
      <td>-inf</td>
      <td>1.457630</td>
      <td>NaN</td>
      <td>3.529303</td>
      <td>-2.524975</td>
      <td>25.588043</td>
      <td>1.070730</td>
      <td>-2.483114</td>
      <td>-0.010710</td>
      <td>2.079442</td>
      <td>-1.291342</td>
      <td>5.934894</td>
      <td>2.799795</td>
      <td>2.313254</td>
      <td>0.249735</td>
      <td>-inf</td>
      <td>0.168108</td>
      <td>-inf</td>
      <td>-0.734536</td>
      <td>1.215561</td>
      <td>3.021083</td>
      <td>3.239272</td>
      <td>4.196479</td>
      <td>3.793443</td>
      <td>-inf</td>
      <td>4.005365</td>
      <td>2.074982</td>
      <td>2.482775</td>
      <td>1.884169</td>
      <td>2.410546</td>
      <td>3.345665</td>
      <td>-0.109222</td>
      <td>5.851852</td>
      <td>17.000000</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1.000000</td>
      <td>0.052137</td>
      <td>2</td>
      <td>1.0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>6</td>
      <td>17</td>
      <td>6</td>
      <td>1.000000</td>
      <td>1.750000</td>
      <td>64</td>
      <td>4.0</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">new</span><span class="o">.</span><span class="n">to_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_pre/loged2.csv&#39;</span><span class="p">,</span><span class="n">mode</span><span class="o">=</span><span class="s1">&#39;w&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">label</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;/content/drive/My Drive/new_original/train_label.csv&#39;</span><span class="p">)</span>
<span class="c1">#label.drop(&#39;Unnamed: 0&#39;,axis=1,inplace=True)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lab</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">lab</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">label</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span>
<span class="n">lab</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">lab</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">lab</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">lab</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">lab</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">lab</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">lab</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:7: RuntimeWarning: divide by zero encountered in log
  import sys
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f242fa9f748&gt;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ee</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="n">ee</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">=</span><span class="p">(</span><span class="n">lab</span><span class="p">[(</span><span class="n">lab</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">&gt;-</span><span class="mi">4</span><span class="p">)</span><span class="o">&amp;</span><span class="p">(</span><span class="n">lab</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">]</span><span class="o">&lt;</span><span class="mi">0</span><span class="p">)][</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">ee</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">ee</span><span class="p">[</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">])</span>
<span class="n">ee</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(19790, 1)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
/wPj6AsVSzRYtQAAAABJRU5ErkJggg==
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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="mi">1</span><span class="o">/</span><span class="n">new</span><span class="p">[</span><span class="n">col</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0        0.000000
1       -0.641789
2       -0.360674
3       -0.360965
4       -0.621335
5       -0.363033
6        0.000000
7       -0.368623
8       -0.360674
9       -1.442695
10      -1.442695
11      -1.442695
12      -0.399118
13      -1.442695
14      -0.378923
15      -0.551761
16      -0.378923
17      -0.360674
18      -0.390711
19       0.000000
20      -0.352956
21       0.000000
22      -0.371020
23       0.000000
24      -0.401471
25      -0.352956
26      -0.378923
27      -0.360674
28      -0.417032
29            inf
           ...   
39970   -0.352956
39971   -0.379955
39972   -0.352956
39973   -0.352956
39974   -0.362436
39975   -0.362140
39976   -0.352956
39977   -0.352956
39978   -0.360674
39979   -0.360674
39980   -0.360674
39981   -0.352956
39982   -0.352956
39983   -0.360674
39984   -0.352956
39985   -0.352956
39986   -0.352956
39987   -0.352956
39988   -0.352956
39989   -0.360674
39990   -0.360674
39991   -0.360674
39992   -0.360674
39993   -0.360674
39994   -0.352956
39995   -0.352956
39996   -0.378167
39997   -0.352956
39998   -0.376399
39999   -0.352956
Name: level, Length: 40000, dtype: float64</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">playtimeplaytimeimport</span> <span class="n">matplotlib</span><span class="o">.</span><span class="n">pyplot</span> <span class="k">as</span> <span class="n">plt</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="kn">import</span> <span class="nn">tensorflow</span> <span class="k">as</span> <span class="nn">tf</span>
<span class="kn">from</span> <span class="nn">tensorflow</span> <span class="kn">import</span> <span class="n">keras</span>
<span class="kn">from</span> <span class="nn">tensorflow.keras</span> <span class="kn">import</span> <span class="n">layers</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>


<span class="n">sns</span><span class="o">.</span><span class="n">pairplot</span><span class="p">(</span><span class="n">df_day1</span><span class="p">[[</span><span class="s2">&quot;game_money_change&quot;</span><span class="p">,</span> <span class="s2">&quot;npc_kill&quot;</span><span class="p">,</span> <span class="s2">&quot;party_exp&quot;</span><span class="p">,</span> <span class="s2">&quot;playtime&quot;</span><span class="p">]],</span> <span class="n">diag_kind</span><span class="o">=</span><span class="s2">&quot;kde&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f2459a73668&gt;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">new</span><span class="p">[</span><span class="n">new</span><span class="p">[</span><span class="s1">&#39;fishing&#39;</span><span class="p">]</span><span class="o">&gt;</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(21360, 37)</pre>
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
<span class="n">cur</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;fishing&#39;</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f24465ef3c8&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXYAAAD8CAYAAABjAo9vAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDMuMC4zLCBo
dHRwOi8vbWF0cGxvdGxpYi5vcmcvnQurowAAE3hJREFUeJzt3XvQXHV9x/H31yRAqmCgICKQBm8w
4gXwEbS0FgUaCgzwh9PRasdLx8xodbyGEsNYmJGRQqvg6Og8IiqFekNMVVAaWmmrI8FggHCVAAoE
NKFItRhu8ds/9oRsHp7bPnt2z2Xfr5mdnP2ds7/z++3ZfJ7f/s7Z3chMJEnt8YyqGyBJKpfBLkkt
Y7BLUssY7JLUMga7JLWMwS5JLWOwS1LLGOyS1DKlBHtELIqISyPitoi4NSJeU0a9kqTezS+pnvOB
72fmGyJiJ+APptt4zz33zCVLlpS0a0kaDdddd92DmbnXTNv1HewR8WzgtcDbADLzceDx6R6zZMkS
1q5d2++uJWmkRMQvZrNdGVMxBwCbgS9GxLqIuCAinjlJg5ZFxNqIWLt58+YSditJmkwZwT4fOAz4
bGYeCjwCnDZxo8wcz8yxzBzba68Z30lIkuaojGC/D7gvM9cU9y+lE/SSpAr0HeyZ+Uvg3og4sCg6
Gril33olSXNT1lUx7wUuKa6IuQt4e0n1SpJ6VEqwZ+b1wFgZdUlSG61at5Fzr7yd+x/ewvMWLWT5
0gM55dB9B7KvskbskqQprFq3keWX3sATWzu/WLfx4S0sv/QGgIGEu18pIEkDduZ3bn4q1Ld5Ymty
5nduHsj+DHZJGrBf/+6Jnsr7ZbBLUssY7JI0QKevWj/0fRrskjRAF19zz5TrFi1cMJB9GuySVJEz
Tjp4IPUa7JJUkUFdx26wS1LLGOyS1DIGuyS1jMEuSS1jsEvSgCw57fJK9muwS1LLGOySNABVjdbB
YJek0lUZ6uD3sUtSaXoJ9Bc955kDa4fBLkl9mssIffUHjyq/IYXSgj0i5gFrgY2ZeWJZ9UpS3bz5
8z/mR3c+NOfHH/mCPUpszdOVOWJ/H3ArsFuJdUpSLZQ5b37JO19TWl2TKSXYI2I/4ATgLOCDZdQp
SVUbxEnQn599Qul1TlTWiP084FRg15Lqk6ShG/TVLMMIdSgh2CPiRGBTZl4XEUdNs90yYBnA4sWL
+92tJJViWJcmDivUoZwR+5HASRFxPLALsFtEXJyZb+neKDPHgXGAsbGxfHo1kjQcw7zOfJiBvk3f
wZ6ZK4AVAMWI/cMTQ12SqjbMMN9t53nceOZxQ9vfRF7HLqm12j4yn0qpwZ6ZVwNXl1mnJM3WQSuv
4NGtw5vprVOYd3PELqnRhv29LHUN824Gu6RGMchnZrBLqq0jzlrNr377+ND328Qw72awS6qNKr/u
tulh3s1gl1SZqr+3vE1h3s1glzQUVU2rTNTWMO9msEsamKpH5DAaQT6RwS6pNHUIchjNMO9msEua
szoEeQB3j3iQT2SwS5q1OgT5qI/GZ8NglzSlA067nKq/itUg753BLukpjsjbwWCXRljVQW6ID4bB
Lo2QqoMcDPNhMNilFqs6yHeZF9x21vGVtmEUGexSSwz7u8in4oi8ega71FBVj8a3Mcjrx2CXaq4u
Ab6NQV5/fQd7ROwPXATsDSQwnpnn91uvNIrqFuJgkDdRGSP2J4EPZeZPI2JX4LqIWJ2Zt5RQt9RK
dQzwbQzy5us72DPzAeCBYvm3EXErsC9gsGvk1TnAtzHI26fUOfaIWAIcCqwps16p7poQ4NsY5O1X
WrBHxLOAbwLvz8zfTLJ+GbAMYPHixWXtVhqqJgU4GOKjqpRgj4gFdEL9ksy8bLJtMnMcGAcYGxur
/mJbaRpNC3AwxLVdGVfFBPAF4NbM/ET/TZIG74UrLufJBg8vDHFNp4wR+5HAXwPrI+L6ouwjmXlF
CXVLc3bsJ67mjk2PVN2Mvhni6lUZV8X8kM6PmEhD18Qpk6kY4CqLnzxVrbUpuLcxwDVoBrsq18bw
BgNc1THYNRRtDe/ddp7HjWceV3UzpB0Y7CpNXb42dlAcgaspDHb1rK2jb4NbbWGwa1ptC3HDW6PA
YBfQrgA3vDXqDPYR1PQQN7il6RnsLdfUEDe8pbkz2FumSUFueEuDYbA3WBNC3PCWhs9gb5i6hrkB
LtWHwV5zdQvy+QEbPm6IS3VmsNdQXcLcUbjUTAZ7TVQd5oa41B4Ge4WqCnNDXGo3g33Iqghzg1wa
LQb7kAwr0A1xSQb7ABnmkqpQSrBHxHHA+cA84ILMPLuMeptq0IFukEuaTt/BHhHzgM8AxwL3AT+J
iG9n5i391t0kx37iau7Y9MjA6jfMJc1WGSP2w4ENmXkXQER8FTgZGIlgH+To3DCXNBdlBPu+wL1d
9+8Djpi4UUQsA5YBLF68uITdVmtQgW6YS+rX0E6eZuY4MA4wNjbW2B/GHESgG+aSylRGsG8E9u+6
v19R1iplB/reu+7EmpXHllqnJEE5wf4T4EURcQCdQH8j8Fcl1FsbZYa6o3NJg9Z3sGfmkxHxHuBK
Opc7XpiZN/fdshow0CU1USlz7Jl5BXBFGXXVwUErr+DRrf2fBjDMJVXBT55OUMYo3UCXVCWDvUs/
oe7JUEl1YbDT/yjdEbqkOhn5YO8n1A10SXX0jKobUCVDXVIbjeSI/fRV67n4mnvm9FgDXVLdjVyw
zzXUDXRJTTFyUzGGuqS2G6lg73VO/cgX7GGoS2qckZiKmcv0i4EuqalaP2I31CWNmtYHu6EuadS0
Oth7mVMPDHVJ7dDaYO/1ROndhrqklmhtsPfCkbqkNmndVTHHfuJq7tj0yKy3N9QltU2rRuyGuiS1
LNgNdUnqM9gj4tyIuC0iboyIb0XEorIaNkiGuqQ263fEvhp4aWa+HPgZsKL/Js3NbK+C2XvXnQbc
EkmqVl/Bnpn/lplPFnevAfbrv0mD5c/XSWq7MufY3wF8b6qVEbEsItZGxNrNmzeXuNvZj9adgpE0
Cma83DEirgKeO8mqlZn5r8U2K4EngUumqiczx4FxgLGxsZxTa/tgqEsaFTMGe2YeM936iHgbcCJw
dGYOPbAPWnnFsHcpSbXW1weUIuI44FTgzzLzd+U0qTePbp35b4mjdUmjpN859k8DuwKrI+L6iPhc
CW2atX5+jFqS2qqvEXtmvrCshgyKo3VJo6ZVnzyVJDU42GczDeNoXdIoamywS5Im19pgd7QuaVQ1
Mthf/vffr7oJklRbjQz23zy2ddr1jtYljbJGBrskaWoGuyS1TOOC3U+bStL0GhfsM3F+XdKoa12w
S9KoM9glqWVaFezzo+oWSFL1WhXsGz7u/LokNSrY/cSpJM2sUcE+0ydOJUkNC3ZJ0swMdklqmVKC
PSI+FBEZEXuWUd9cvOXVi6vatSTVSt/BHhH7A38O3NN/c+buY6e8rMrdS1JtlDFi/yRwKpAl1CVJ
6lNfwR4RJwMbM/OGktojSerT/Jk2iIirgOdOsmol8BE60zAziohlwDKAxYt7nw9/8+d/3PNjJGkU
zRjsmXnMZOUR8TLgAOCGiADYD/hpRByemb+cpJ5xYBxgbGys52mbH935UK8PkaSRNGOwTyUz1wPP
2XY/In4OjGXmgyW0S5I0R17HLkktM+cR+0SZuaSsunrltzpK0natGLH7rY6StF0rgl2StJ3BLkkt
Y7BLUssY7JLUMga7JLWMwS5JLWOwS1LLGOyS1DIGuyS1jMEuSS1jsEtSyxjsktQyjQj2Ves2Vt0E
SWqMRgT7ym+tr7oJktQYjQj2Rx7fOuW6RQsXDLElklR/jQj26Zxx0sFVN0GSaqXxwX7KoftW3QRJ
qpW+gz0i3hsRt0XEzRFxThmNkiTNXV+/eRoRrwNOBl6RmY9FxHPKaZYkaa76HbG/Czg7Mx8DyMxN
/Tfp6aY6QeqJU0l6un6D/cXAn0bEmoj4z4h4VRmNmujEV+zTU7kkjbIZgz0iroqImya5nUxnKmcP
4NXAcuDrERFT1LMsItZGxNrNmzf31MjLb3ygp3JJGmUzzrFn5jFTrYuIdwGXZWYC10bE74E9gacl
d2aOA+MAY2Nj2Usjf/27J3oql6RR1u9UzCrgdQAR8WJgJ+DBfhslSZq7vq6KAS4ELoyIm4DHgbcW
o3dJUkX6CvbMfBx4S0ltkSSVoPGfPJUk7chgl6SWMdglqWUaEezzJr80fspySRpljQj2rVNcaDNV
uSSNskYE+76LFvZULkmjrBHBvnzpgSxcMG+HsoUL5rF86YEVtUiS6qvfDygNxbYf0zj3ytu5/+Et
PG/RQpYvPdAf2ZCkSTQi2KET7ga5JM2sEVMxkqTZM9glqWUMdklqGYNdklrGYJekljHYJallDHZJ
ahmDXZJaxmCXpJYx2CWpZfoK9og4JCKuiYjrI2JtRBxeVsMkSXPT74j9HODMzDwE+GhxX5JUoX6D
PYHdiuVnA/f3WZ8kqU/9frvj+4ErI+If6fyR+OOpNoyIZcAygMWLF/e5W0nSVGYM9oi4CnjuJKtW
AkcDH8jMb0bEXwJfAI6ZrJ7MHAfGAcbGxvxNO0kakBmDPTMnDWqAiLgIeF9x9xvABSW162lWrdvo
D21I0iz0O8d+P/BnxfLrgTv6rG9Sq9ZtZMVl69n48BYS2PjwFlZctp5V6zYOYneS1Gj9zrG/Ezg/
IuYDj1LMoZft3CtvZ8sTW3co2/LEVs698nZH7ZI0QV/Bnpk/BF5ZUlumdP/DW3oql6RR1ohPnj5v
0cKeyiVplDUi2JcvPZCFC+btULZwwTyWLz2wohZJUn31O8c+FNvm0b0qRpJm1ohgh064G+SSNLNG
TMVIkmbPYJeklmnMVMzpq9bzlTX3sjWTeRG86Yj9+dgpL6u6WZJUO40I9tNXrefia+556v7WzKfu
G+6StKNGTMV8Zc29PZVL0ihrRLBvzcm/DHKqckkaZY0I9nkRPZVL0ihrRLC/6Yj9eyqXpFHWiJOn
206QelWMJM0ssoJ56rGxsVy7du3Q9ytJTRYR12Xm2EzbNWIqRpI0ewa7JLWMwS5JLWOwS1LLGOyS
1DKVXBUTEZuBX8zhoXsCD5bcnLqzz6PBPo+Ofvr9R5m510wbVRLscxURa2dzqU+b2OfRYJ9HxzD6
7VSMJLWMwS5JLdO0YB+vugEVsM+jwT6PjoH3u1Fz7JKkmTVtxC5JmsHQgz0iLoyITRFxU1fZGRGx
MSKuL27Hd61bEREbIuL2iFjaVX5cUbYhIk7rKj8gItYU5V+LiJ2G17vJRcT+EfGDiLglIm6OiPcV
5XtExOqIuKP4d/eiPCLiU0UfboyIw7rqemux/R0R8dau8ldGxPriMZ+KqPbL6qfpc2uPdUTsEhHX
RsQNRZ/PnK6dEbFzcX9DsX5JV109PRdVmabPX4qIu7uO8yFFeeNf29tExLyIWBcR3y3u1+c4Z+ZQ
b8BrgcOAm7rKzgA+PMm2LwFuAHYGDgDuBOYVtzuB5wM7Fdu8pHjM14E3FsufA9417D5O0o99gMOK
5V2BnxV9Owc4rSg/DfiHYvl44HtAAK8G1hTlewB3Ff/uXizvXqy7ttg2isf+RU373NpjXTz3zyqW
FwBrimMyaTuBdwOfK5bfCHxtrs9FDfv8JeANk2zf+Nd2V18+CPwL8N3pXo9VHOehj9gz87+Ah2a5
+cnAVzPzscy8G9gAHF7cNmTmXZn5OPBV4OTiL/nrgUuLx38ZOKXUDsxBZj6QmT8tln8L3ArsS6d/
Xy42627rycBF2XENsCgi9gGWAqsz86HM/DWwGjiuWLdbZl6TnVfMRVTc72n6PJXGH+vieP1fcXdB
cUumbmf38b8UOLroV0/PxYC7Na1p+jyVxr+2ASJiP+AE4ILi/nSvx6Ef5zrNsb+neGt2YRRTEnSC
oPsXq+8ryqYq/0Pg4cx8ckJ5bRRvww6lM7LZOzMfKFb9Eti7WO613/sWyxPLa2FCn6HFx7p4e349
sIlOON3J1O18qm/F+v+l069en4tKTexzZm47zmcVx/mTEbFzUdaW1/Z5wKnA74v7070eh36c6xLs
nwVeABwCPAD8U7XNGYyIeBbwTeD9mfmb7nXFaKR1lyhN0udWH+vM3JqZhwD70Rl5HVRxkwZuYp8j
4qXACjp9fxWd6ZW/q7CJpYqIE4FNmXld1W2ZSi2CPTN/Vbw4fg98ns5/CICNQPcPm+5XlE1V/j90
3trNn1BeuYhYQCfgLsnMy4riXxVvNSn+3VSU99rvjcXyxPJKTdbnUTjWAJn5MPAD4DVM3c6n+las
fzadfvX6XNRCV5+PK6biMjMfA77I3I9zHV/bRwInRcTP6UyTvB44nzod52GdaOi+AUvY8eTpPl3L
H6Az7wRwMDueXLiLzomF+cXyAWw/uXBw8ZhvsOMJjHdX0ccJ/Q06c4PnTSg/lx1Pnp5TLJ/AjieY
rs3tJ5jupnNyafdieY+c/ATT8TXtc2uPNbAXsKhYXgj8N3DiVO0E/pYdT6p9fa7PRQ37vE/X6+A8
4Oy2vLYn9P8otp88rc1xruKJ+Aqdt+BP0Jk7+hvgn4H1wI3Atyf8519JZ57ydrrOhtM5u/6zYt3K
rvLnFy+EDcUTvXMNDv6f0JlmuRG4vrgdT2ee7d+BO4Crul7IAXym6Nt6YKyrrncUfdsAvL2rfAy4
qXjMpyk+fFbDPrf2WAMvB9YVfbsJ+Oh07QR2Ke5vKNY/f67PRQ37/B/Fcb4JuJjtV840/rU9of9H
sT3Ya3Oc/eSpJLVMLebYJUnlMdglqWUMdklqGYNdklrGYJekljHYJallDHZJahmDXZJa5v8B+vXU
aRggKYsAAAAASUVORK5CYII=
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cur</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">()</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">col_list</span><span class="p">:</span>
  <span class="n">cur</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="mi">1</span><span class="o">/</span><span class="n">new</span><span class="p">[</span><span class="n">col</span><span class="p">])</span>
  
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:5: RuntimeWarning: divide by zero encountered in log
  &#34;&#34;&#34;
/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:5: RuntimeWarning: invalid value encountered in log
  &#34;&#34;&#34;
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
<span class="n">cur</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;enchant_count&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;enchant_count&#39;</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f24477c9470&gt;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cur</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">new</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">])</span>
<span class="n">cur</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;playtime&#39;</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">cur</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
      <th>index</th>
      <th>playtime</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1023</td>
      <td>0.002341</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1396</td>
      <td>0.002341</td>
    </tr>
    <tr>
      <th>2</th>
      <td>11423</td>
      <td>0.002341</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3988</td>
      <td>0.002341</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5233</td>
      <td>0.002341</td>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">cur</span><span class="p">[</span><span class="s1">&#39;playtime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">min</span><span class="p">())</span>

<span class="c1">#cur[&#39;level&#39;]=np.exp(cur[&#39;level&#39;])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:1: RuntimeWarning: invalid value encountered in log
  &#34;&#34;&#34;Entry point for launching an IPython kernel.
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">new</span><span class="o">.</span><span class="n">columns</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">tolist</span><span class="p">())</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">new</span><span class="p">[</span><span class="s1">&#39;level_range0&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([  1,   0,   2,   3,   4,  21,  13,   5,  16,   8,   9,  10,   6,
        11,   7,  25,  18,  19,  17,  33,  36,  20,  23,  12,  42,  27,
        29,  14,  34, 147, 133,  43,  91,  32,  58,  15,  60,  35,  30,
        31,  24,  26, 117,  41,  51,  81,  22,  47,  37,  64,  39,  73,
       227,  44,  28])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">variable</span><span class="o">=</span><span class="s1">&#39;combat_same_pledge_cnt_sum&#39;</span>
<span class="n">cur</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">new</span><span class="p">[</span><span class="n">variable</span><span class="p">])</span>
<span class="n">cur</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">variable</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">cur</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>



<span class="n">cur</span><span class="p">[</span><span class="n">variable</span><span class="p">]</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">cur</span><span class="p">[</span><span class="n">variable</span><span class="p">]</span><span class="o">-</span><span class="mi">1</span><span class="o">+</span><span class="n">cur</span><span class="p">[</span><span class="n">variable</span><span class="p">]</span><span class="o">.</span><span class="n">min</span><span class="p">())</span>

<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">cur</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">cur</span><span class="p">[</span><span class="n">variable</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:8: RuntimeWarning: invalid value encountered in log
  
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x7f242e5eddd8&gt;</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">cur</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[0]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(23562, 2)</pre>
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
