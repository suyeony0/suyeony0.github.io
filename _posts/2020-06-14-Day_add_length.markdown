---
layout: post
title: Big Contest - Adding day length
date: 2020-06-14
description: READ ME
thumbnail: food2.jpg
categories: BigContest

# Information for the author block
author : Loui
---

<html>
<head><meta charset="utf-8" />

<title>Day_add_length</title>

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
<span class="kn">import</span> <span class="nn">lightgbm</span> <span class="k">as</span> <span class="nn">lgb</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_activity</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;../OriginData/2019빅콘테스트_챔피언스리그_데이터_수정/train_activity.csv&#39;</span><span class="p">,</span> <span class="n">engine</span> <span class="o">=</span> <span class="s1">&#39;python&#39;</span><span class="p">)</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span> <span class="o">=</span> <span class="n">df_activity</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">df_day</span> <span class="o">=</span> <span class="n">df_temp</span><span class="p">[[</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span> <span class="s1">&#39;day&#39;</span><span class="p">]]</span>
<span class="n">df_day</span> <span class="o">=</span> <span class="n">df_day</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span> <span class="s1">&#39;day&#39;</span><span class="p">])</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_first</span> <span class="o">=</span> <span class="n">df_day</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;acc_id&#39;</span><span class="p">],</span> <span class="n">keep</span> <span class="o">=</span> <span class="s1">&#39;first&#39;</span><span class="p">)</span>

<span class="n">df_day_first</span><span class="o">.</span><span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span> <span class="s1">&#39;day_first&#39;</span><span class="p">]</span>

<span class="n">df_day_first</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">drop</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
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
      <th>acc_id</th>
      <th>day_first</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>75001</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>75711</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>72230</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>34253</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>83200</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>13896</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>54399</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>67385</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>21932</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>30937</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>53141</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>94123</td>
      <td>1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>76110</td>
      <td>1</td>
    </tr>
    <tr>
      <th>13</th>
      <td>128757</td>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>91114</td>
      <td>1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>32521</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>20575</td>
      <td>1</td>
    </tr>
    <tr>
      <th>17</th>
      <td>9300</td>
      <td>1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>15556</td>
      <td>1</td>
    </tr>
    <tr>
      <th>19</th>
      <td>69182</td>
      <td>1</td>
    </tr>
    <tr>
      <th>20</th>
      <td>87786</td>
      <td>1</td>
    </tr>
    <tr>
      <th>21</th>
      <td>58956</td>
      <td>1</td>
    </tr>
    <tr>
      <th>22</th>
      <td>3383</td>
      <td>1</td>
    </tr>
    <tr>
      <th>23</th>
      <td>92874</td>
      <td>1</td>
    </tr>
    <tr>
      <th>24</th>
      <td>97731</td>
      <td>1</td>
    </tr>
    <tr>
      <th>25</th>
      <td>121129</td>
      <td>1</td>
    </tr>
    <tr>
      <th>26</th>
      <td>32541</td>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>103844</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>3962</td>
      <td>1</td>
    </tr>
    <tr>
      <th>29</th>
      <td>37214</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>39970</th>
      <td>123223</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39971</th>
      <td>52885</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39972</th>
      <td>105395</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39973</th>
      <td>58765</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39974</th>
      <td>30358</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39975</th>
      <td>127132</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39976</th>
      <td>79097</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39977</th>
      <td>26795</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39978</th>
      <td>39550</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39979</th>
      <td>90754</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39980</th>
      <td>78420</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39981</th>
      <td>105828</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39982</th>
      <td>5279</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39983</th>
      <td>8508</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39984</th>
      <td>22772</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39985</th>
      <td>36308</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39986</th>
      <td>112234</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39987</th>
      <td>98507</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39988</th>
      <td>26110</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39989</th>
      <td>30604</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39990</th>
      <td>85587</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39991</th>
      <td>85033</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39992</th>
      <td>110981</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39993</th>
      <td>117125</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39994</th>
      <td>43726</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39995</th>
      <td>31169</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39996</th>
      <td>69980</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39997</th>
      <td>94182</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39998</th>
      <td>27017</td>
      <td>28</td>
    </tr>
    <tr>
      <th>39999</th>
      <td>1591</td>
      <td>28</td>
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
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">get_first_27</span><span class="p">(</span><span class="n">day_first</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">day_first</span> <span class="o">==</span> <span class="mi">28</span><span class="p">:</span>
        <span class="k">return</span> <span class="mi">27</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="n">day_first</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_first</span><span class="p">[</span><span class="s1">&#39;day_first&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df_day_first</span><span class="p">[</span><span class="s1">&#39;day_first&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">get_first_27</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>C:\Users\skagu\Anaconda3\lib\site-packages\ipykernel_launcher.py:1: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  &#34;&#34;&#34;Entry point for launching an IPython kernel.
</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_first</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[7]:</div>



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
      <th>day_first</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>75001</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>75711</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>72230</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>34253</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>83200</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>13896</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>54399</td>
      <td>1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>67385</td>
      <td>1</td>
    </tr>
    <tr>
      <th>13</th>
      <td>21932</td>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>30937</td>
      <td>1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>53141</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>94123</td>
      <td>1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>76110</td>
      <td>1</td>
    </tr>
    <tr>
      <th>20</th>
      <td>128757</td>
      <td>1</td>
    </tr>
    <tr>
      <th>21</th>
      <td>91114</td>
      <td>1</td>
    </tr>
    <tr>
      <th>23</th>
      <td>32521</td>
      <td>1</td>
    </tr>
    <tr>
      <th>25</th>
      <td>20575</td>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>9300</td>
      <td>1</td>
    </tr>
    <tr>
      <th>30</th>
      <td>15556</td>
      <td>1</td>
    </tr>
    <tr>
      <th>31</th>
      <td>69182</td>
      <td>1</td>
    </tr>
    <tr>
      <th>33</th>
      <td>87786</td>
      <td>1</td>
    </tr>
    <tr>
      <th>34</th>
      <td>58956</td>
      <td>1</td>
    </tr>
    <tr>
      <th>37</th>
      <td>3383</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39</th>
      <td>92874</td>
      <td>1</td>
    </tr>
    <tr>
      <th>42</th>
      <td>97731</td>
      <td>1</td>
    </tr>
    <tr>
      <th>43</th>
      <td>121129</td>
      <td>1</td>
    </tr>
    <tr>
      <th>45</th>
      <td>32541</td>
      <td>1</td>
    </tr>
    <tr>
      <th>46</th>
      <td>103844</td>
      <td>1</td>
    </tr>
    <tr>
      <th>47</th>
      <td>3962</td>
      <td>1</td>
    </tr>
    <tr>
      <th>48</th>
      <td>37214</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1596171</th>
      <td>123223</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596319</th>
      <td>52885</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596335</th>
      <td>105395</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596413</th>
      <td>58765</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596500</th>
      <td>30358</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596660</th>
      <td>127132</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596753</th>
      <td>79097</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596760</th>
      <td>26795</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1596952</th>
      <td>39550</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597014</th>
      <td>90754</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597027</th>
      <td>78420</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597125</th>
      <td>105828</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597219</th>
      <td>5279</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597397</th>
      <td>8508</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597423</th>
      <td>22772</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597477</th>
      <td>36308</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597499</th>
      <td>112234</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597586</th>
      <td>98507</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597600</th>
      <td>26110</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597644</th>
      <td>30604</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597693</th>
      <td>85587</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597695</th>
      <td>85033</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597696</th>
      <td>110981</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1597793</th>
      <td>117125</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1598039</th>
      <td>43726</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1598063</th>
      <td>31169</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1598595</th>
      <td>69980</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1598795</th>
      <td>94182</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1599112</th>
      <td>27017</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1599405</th>
      <td>1591</td>
      <td>27</td>
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
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_last</span> <span class="o">=</span> <span class="n">df_day</span><span class="p">[</span><span class="n">df_day</span><span class="o">.</span><span class="n">day</span> <span class="o">&lt;</span> <span class="mi">28</span><span class="p">]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_last</span> <span class="o">=</span> <span class="n">df_day_last</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">([</span><span class="s1">&#39;acc_id&#39;</span><span class="p">],</span> <span class="n">keep</span> <span class="o">=</span> <span class="s1">&#39;last&#39;</span><span class="p">)</span>
<span class="n">df_day_last</span> <span class="o">=</span> <span class="n">df_day_last</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">drop</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#df_day_first : 최초 접속일.</span>
<span class="c1">#df_day_last : 28일을 제외한 마지막 접속일.</span>
<span class="c1"># 합치지는 않았음.</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">df_day_first</span><span class="p">,</span> <span class="n">df_day_last</span><span class="p">,</span> <span class="n">on</span> <span class="o">=</span> <span class="s1">&#39;acc_id&#39;</span><span class="p">,</span> <span class="n">how</span> <span class="o">=</span> <span class="s1">&#39;outer&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span> <span class="o">=</span> <span class="n">df_day_temp</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>
<span class="n">df_day_temp</span><span class="o">.</span><span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;acc_id&#39;</span><span class="p">,</span> <span class="s1">&#39;day_first&#39;</span><span class="p">,</span> <span class="s1">&#39;day_last&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
      <th>acc_id</th>
      <th>day_first</th>
      <th>day_last</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>40000.000000</td>
      <td>40000.000000</td>
      <td>40000.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>65281.105550</td>
      <td>3.300150</td>
      <td>26.058625</td>
    </tr>
    <tr>
      <th>std</th>
      <td>37525.623536</td>
      <td>6.069928</td>
      <td>4.530944</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>32792.750000</td>
      <td>1.000000</td>
      <td>27.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>65359.000000</td>
      <td>1.000000</td>
      <td>27.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>97685.750000</td>
      <td>1.000000</td>
      <td>27.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>130473.000000</td>
      <td>27.000000</td>
      <td>27.000000</td>
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
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">set_last</span><span class="p">(</span><span class="n">row</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">row</span><span class="o">.</span><span class="n">day_last</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="k">return</span> <span class="n">row</span><span class="o">.</span><span class="n">day_first</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="n">row</span><span class="o">.</span><span class="n">day_last</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span><span class="p">[</span><span class="s1">&#39;day_last&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df_day_temp</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">set_last</span><span class="p">,</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[16]:</div>



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
      <th>day_first</th>
      <th>day_last</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>40000.000000</td>
      <td>40000.000000</td>
      <td>40000.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>65281.105550</td>
      <td>3.300150</td>
      <td>26.058625</td>
    </tr>
    <tr>
      <th>std</th>
      <td>37525.623536</td>
      <td>6.069928</td>
      <td>4.530944</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>32792.750000</td>
      <td>1.000000</td>
      <td>27.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>65359.000000</td>
      <td>1.000000</td>
      <td>27.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>97685.750000</td>
      <td>1.000000</td>
      <td>27.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>130473.000000</td>
      <td>27.000000</td>
      <td>27.000000</td>
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
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">grouped_acc</span> <span class="o">=</span> <span class="n">df_day</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;acc_id&#39;</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">grouped_acc</span><span class="o">.</span><span class="n">groups</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[18]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>{2: Int64Index([  37347,   91681,  146496,  201273,  256953,  312103,  367552,
              424045,  479835,  535631,  592419,  650408,  707347,  764199,
              820509,  876286,  931929,  988428, 1045677, 1103135, 1159272,
             1217339, 1275008, 1332488, 1391833, 1453263, 1514686, 1578474],
            dtype=&#39;int64&#39;),
 5: Int64Index([ 470668,  754788, 1093744, 1207643, 1265402, 1323037, 1382073,
             1442957, 1504501, 1567578],
            dtype=&#39;int64&#39;),
 8: Int64Index([  24570,   79342,  134295,  189203,  244676,  300061,  354936,
              411215,  467381,  523220,  579865,  637384,  694852,  751551,
              807778,  863845,  919457,  976098, 1033042, 1090466, 1146745,
             1204378, 1262157, 1319786, 1378656, 1439481, 1501108, 1563878],
            dtype=&#39;int64&#39;),
 17: Int64Index([  27644,   82279,  137233,  192126,  247630,  302966,  357982,
              414374,  470453,  526243,  582897,  640546,  697909,  754578,
              810861,  866814,  922478,  979073, 1036130, 1093551, 1149833,
             1207443, 1265202, 1322825, 1381850, 1442730, 1504271, 1567342],
            dtype=&#39;int64&#39;),
 20: Int64Index([  12324,   67248,  122231,  177173,  232358,  288062,  342441,
              398774,  455282,  511195,  567465,  624761,  682630,  739148,
              795536,  851722,  907396,  963967, 1078167, 1134513, 1191567,
             1249580, 1307187, 1365867, 1426144, 1487878, 1549637],
            dtype=&#39;int64&#39;),
 21: Int64Index([  96728,  151578,  206398,  262151,  317077,  372948,  429412,
              485017,  540869,  597713,  655769,  712759,  769425,  825749,
              881501,  937173,  993581, 1050978, 1108303, 1164484, 1222846,
             1280412, 1337768, 1397318, 1458977, 1584468],
            dtype=&#39;int64&#39;),
 31: Int64Index([  21033,   75893,  130890,  185726,  241177,  296579,  351417,
              407551,  463875,  519718,  576262,  633776,  691311,  747940,
              804206,  860378,  915956,  972562, 1029476, 1086916, 1143293,
             1200695, 1258567, 1316238, 1374953, 1435722, 1497388, 1559827],
            dtype=&#39;int64&#39;),
 38: Int64Index([  36399,   90707,  145515,  200369,  255985,  311125,  366556,
              423084,  478894,  534714,  591497,  649412,  706391,  763244,
              819508,  875302,  987474, 1044660, 1102112, 1158277, 1216292,
             1274056, 1331537, 1390798, 1452219, 1513575, 1577296],
            dtype=&#39;int64&#39;),
 41: Int64Index([1586788], dtype=&#39;int64&#39;),
 43: Int64Index([  33347,   87698,  142585,  197524,  253124,  308323,  363612,
              420109,  475978,  531832,  588552,  646397,  703477,  760270,
              816425,  872306,  927955, 1041801, 1099200, 1155393, 1213270,
             1271022, 1328527, 1387712, 1448988, 1510333, 1573855],
            dtype=&#39;int64&#39;),
 50: Int64Index([  36830,   91125,  145965,  200782,  366998,  423511,  479306,
              535137,  591900,  649878,  706825,  763686,  819952,  875764,
              931390,  987901, 1045149, 1102575, 1158738, 1216785, 1274498,
             1331952, 1391302, 1452722, 1514093, 1577831],
            dtype=&#39;int64&#39;),
 53: Int64Index([  37271,   91596,  146412,  201204,  256862,  312029,  367462,
              423965,  479753,  535558,  592342,  650333,  707269,  764125,
              820429,  876203,  931853,  988352, 1045599, 1103063, 1159189,
             1217248, 1274925, 1332410, 1391760, 1453174, 1514609, 1578360],
            dtype=&#39;int64&#39;),
 54: Int64Index([ 272755,  327471,  440289,  551841,  608822,  667146,  724263,
              780631,  836672,  892241,  948690, 1005081, 1062658, 1119571,
             1175895, 1233941, 1291343, 1349243, 1408951, 1471139, 1532491,
             1598880],
            dtype=&#39;int64&#39;),
 59: Int64Index([   9598,   64549,  119422,  174435,  229564,  285332,  339585,
              396001,  452540,  508455,  564675,  621942,  679849,  736356,
              792799,  848962,  904678,  961257, 1017902, 1075429, 1131799,
             1188785, 1246845, 1304360, 1362949, 1423053, 1484904, 1546398],
            dtype=&#39;int64&#39;),
 62: Int64Index([  37981,   92300,  147104,  201861,  257562,  312675,  368187,
              424682,  480471,  536225,  593040,  651037,  707960,  764816,
              821143,  876900,  932570,  989036, 1046299, 1103765, 1159903,
             1217994, 1275641, 1333107, 1392460, 1453916, 1515336, 1579151],
            dtype=&#39;int64&#39;),
 63: Int64Index([ 302824,  357831,  470305,  526117,  582761,  640410,  697778,
              754439,  810723,  866682,  922356,  978943, 1035997, 1093402,
             1149690, 1207302, 1265065, 1322678, 1381680, 1442595, 1504140,
             1567171],
            dtype=&#39;int64&#39;),
 65: Int64Index([  44351,  100951,  153257,  208085,  263878,  318766,  377287,
              431105,  489316,  542486,  599376,  657457,  714390,  771102,
              827368,  885633,  938808,  995217, 1052631, 1109961, 1166216,
             1224518, 1284377, 1339505, 1401628, 1460828, 1522084, 1586695],
            dtype=&#39;int64&#39;),
 66: Int64Index([  18838,   73715,  128730,  183549,  238924,  294481,  349144,
              405304,  461733,  517601,  574026,  631504,  689134,  745715,
              801960,  858134,  913800,  970350, 1027193, 1084684, 1141042,
             1198340, 1256275, 1313924, 1372607, 1433218, 1494908, 1557208],
            dtype=&#39;int64&#39;),
 67: Int64Index([  11728,   66636,  121607,  176537,  231684,  287438,  341764,
              398151,  454665,  510537,  566856,  624113,  681995,  738515,
              794904,  851087,  906786,  963360, 1020098, 1077549, 1190933,
             1306572, 1365204, 1425463, 1487203, 1548876],
            dtype=&#39;int64&#39;),
 69: Int64Index([  23504,   78259,  133265,  188144,  243619,  299004,  353861,
              410092,  466280,  522138,  578767,  636310,  693797,  750470,
              806690,  862801,  918390,  975015, 1089365, 1145656, 1203259,
             1261037, 1318683, 1377479, 1438325, 1499952, 1562620],
            dtype=&#39;int64&#39;),
 75: Int64Index([  28787,   83373,  193202,  248751,  304023,  359081,  386466,
              443098,  499176,  555116,  612074,  670467,  726829,  783281,
              839522,  895246,  952026, 1008408, 1065958, 1122250, 1178838,
             1236887, 1294576, 1352783, 1412681, 1474579, 1535325],
            dtype=&#39;int64&#39;),
 76: Int64Index([   8806,   63771,  118666,  173657,  228779,  284582,  338782,
              395189,  451763,  507693,  563897,  621134,  679075,  735550,
              791980,  848197,  903907,  960470, 1017098, 1074615, 1130991,
             1187918, 1245990, 1303583, 1362069, 1422161, 1484036, 1545484],
            dtype=&#39;int64&#39;),
 77: Int64Index([  25009,   79789,  134712,  189634,  245115,  300460,  355375,
              411677,  467835,  523678,  580322,  637860,  695287,  751990,
              808224,  864271,  919910,  976537, 1033494, 1090899, 1147183,
             1204829, 1262603, 1320225, 1379110, 1439951, 1501576, 1564389],
            dtype=&#39;int64&#39;),
 79: Int64Index([  37679,   91985,  146804,  201562,  257259,  312402,  367869,
              424378,  480158,  535929,  592741,  650742,  707661,  764504,
              820837,  876592,  932256,  988741, 1045992, 1103465, 1159602,
             1217691, 1275334, 1332817, 1392163, 1453614, 1515033, 1578843],
            dtype=&#39;int64&#39;),
 81: Int64Index([  18415,   73278,  128286,  183100,  238488,  294061,  348719,
              404867,  461315,  517163,  573589,  631053,  688683,  745272,
              801501,  857703,  913349,  969921, 1026757, 1084260, 1140599,
             1197862, 1255820, 1313454, 1372110, 1432727, 1494430, 1556685],
            dtype=&#39;int64&#39;),
 86: Int64Index([  30396,   84908,  139865,  194745,  250300,  305529,  360696,
              417113,  473123,  528899,  585638,  643342,  700606,  757273,
              813492,  869444,  925099,  981765, 1038924, 1096260, 1152512,
             1210287, 1268027, 1325604, 1384717, 1445769, 1507223, 1570440],
            dtype=&#39;int64&#39;),
 91: Int64Index([  15494,   70399,  125377,  180293,  235566,  291193,  345709,
              401962,  458457,  514311,  570700,  628045,  685736,  742324,
              798656,  854831,  910491,  967072, 1023910, 1081328, 1137693,
             1194852, 1252852, 1310439, 1369090, 1429590, 1491322, 1553321],
            dtype=&#39;int64&#39;),
 92: Int64Index([  35748,   90079,  144883,  199736,  255376,  310523,  365921,
              422449,  478308,  534092,  590873,  648789,  705800,  762619,
              818880,  874639,  930312,  986872, 1044066, 1101487, 1157632,
             1215640, 1273403, 1330894, 1390157, 1451543, 1512885, 1576573],
            dtype=&#39;int64&#39;),
 97: Int64Index([  16513,   71385,  126384,  181290,  236596,  292174,  346742,
              402981,  459439,  515276,  571651,  629064,  686722,  743322,
              799625,  855804,  911423,  967999, 1024880, 1082309, 1138655,
             1195841, 1253873, 1311431, 1370052, 1430659, 1492374, 1554472],
            dtype=&#39;int64&#39;),
 98: Int64Index([  39690,   93934,  148757,  203495,  259241,  314275,  369903,
              426411,  482093,  537939,  594724,  652738,  709606,  766482,
              822796,  878580,  934289,  990657, 1048015, 1105408, 1161560,
             1219714, 1277355, 1334795, 1394244, 1455684, 1517152, 1581109],
            dtype=&#39;int64&#39;),
 100: Int64Index([ 666539,  723640,  780010,  836109,  891652,  948018, 1004423,
             1061965, 1175198, 1233220, 1290638, 1348537, 1408222, 1470432,
             1531791, 1598114],
            dtype=&#39;int64&#39;),
 113: Int64Index([   4479,   59538,  114409,  224369,  280400,  334371,  390851,
              447421,  503425,  559592,  616662,  674768,  731247,  787639,
              899630,  956306, 1012736, 1126641, 1183392, 1241509, 1299102,
             1357428, 1417452, 1479349, 1540381],
            dtype=&#39;int64&#39;),
 119: Int64Index([  33367,   87711,  142606,  197539,  253142,  308337,  363626,
              420123,  475999,  531846,  588564,  646410,  703491,  760282,
              816438,  872324,  927972,  984654, 1041814, 1099213, 1155408,
             1213285, 1271034, 1328539, 1387731, 1449002, 1510349, 1573877],
            dtype=&#39;int64&#39;),
 125: Int64Index([619298, 733769, 958767, 1244121, 1543292], dtype=&#39;int64&#39;),
 129: Int64Index([  38315,   92607,  147421,  202162,  257878,  312973,  368490,
              424981,  480776,  536560,  593350,  651340,  708262,  765120,
              821448,  877224,  932922,  989364, 1046639, 1104077, 1160237,
             1218301, 1275967, 1333412, 1392777, 1454239, 1515703, 1579554],
            dtype=&#39;int64&#39;),
 133: Int64Index([  82933,  137881,  192763,  248298,  303605,  358630,  415056,
              471107,  526871,  583556,  641210,  698561,  755229,  811482,
              867465,  923097,  979721, 1036765, 1094187, 1150464, 1208148,
             1265898, 1323528, 1382565, 1443476, 1505017, 1568111],
            dtype=&#39;int64&#39;),
 137: Int64Index([  37559,   91870,  146692,  201456,  257145,  312291,  367747,
              424258,  480043,  535814,  592626,  650627,  707551,  764387,
              820713,  876481,  932137,  988638, 1045885, 1103348, 1159471,
             1217579, 1275215, 1332694, 1392047, 1453484, 1514907, 1578719],
            dtype=&#39;int64&#39;),
 138: Int64Index([ 103064,  157822,  212631,  268468,  325419,  379220,  435799,
              491322,  547174,  604216,  662317,  719474,  775837,  834345,
              889866,  946155, 1000063, 1060084, 1173255, 1346563, 1406235,
             1468323, 1529666, 1595784],
            dtype=&#39;int64&#39;),
 140: Int64Index([ 421182,  477090,  532917,  589655,  647510,  704558,  761374,
              817602,  873405,  985654, 1042825, 1100262, 1156431, 1214380,
             1272143, 1329622, 1388895, 1450158, 1575095],
            dtype=&#39;int64&#39;),
 145: Int64Index([  25160,   79911,  134820,  245238,  300571,  355490,  411804,
              467957,  580441,  637983,  675441,  752115,  808357,  864381,
              920070,  976676, 1033641, 1091028, 1135965, 1200965, 1262748,
             1320357, 1379251, 1440094, 1564544],
            dtype=&#39;int64&#39;),
 147: Int64Index([1588804], dtype=&#39;int64&#39;),
 149: Int64Index([  18159,   73052,  238282,  293842,  348493,  404668,  461117,
              516947,  573388,  630843,  688466,  745065,  801315,  857494,
              913135,  969715, 1026551, 1084045, 1140386, 1197664, 1255607,
             1313261, 1371871, 1432517, 1494208, 1556430],
            dtype=&#39;int64&#39;),
 154: Int64Index([  51442,   79921,  160575,  215359,  271250,  326048,  382069,
              438757,  494423,  550245,  835089,  890624, 1003354, 1060888,
             1117818, 1174069, 1232048, 1289521, 1407062, 1469190, 1530588,
             1596741],
            dtype=&#39;int64&#39;),
 155: Int64Index([   7999,   63012,  117907,  172873,  227978,  283827,  337989,
              394378,  450997,  506970,  563140,  620359,  678301,  734787,
              791211,  847451,  903136,  959706, 1016297, 1073824, 1187069,
             1245186, 1302759, 1361190, 1421282, 1483197, 1544523],
            dtype=&#39;int64&#39;),
 158: Int64Index([ 575754,  803683,  859839,  915465, 1086418, 1142771, 1200129,
             1258037, 1315709, 1374405, 1496815, 1559227],
            dtype=&#39;int64&#39;),
 160: Int64Index([ 271610,  326420,  835516,  947353, 1003790, 1061324, 1118238,
             1174512, 1232500, 1289963, 1347834, 1407536, 1469697, 1531071,
             1597285],
            dtype=&#39;int64&#39;),
 161: Int64Index([  26091,   80802,  135728,  165669,  246158,  301493,  356414,
              412740,  468880,  524706,  581354,  638938,  753051,  809283,
              865303,  920995,  952431, 1021790, 1091968, 1148235, 1205872,
             1321266, 1380191, 1441062, 1502682, 1565616],
            dtype=&#39;int64&#39;),
 163: Int64Index([   2568,   57665,  112548,  167642,  222490,  278597,  332462,
              388965,  445560,  501599,  557710,  614727,  672961,  729318,
              785782,  841959,  897728,  954506, 1010891, 1068455, 1124745,
             1181402, 1239518, 1297141, 1355365, 1415351, 1477270, 1538187],
            dtype=&#39;int64&#39;),
 172: Int64Index([  23662,   78413,  133422,  188287,  243773,  299163,  354026,
              410258,  466431,  522285,  578913,  636454,  693941,  750624,
              806838,  862954,  918549,  975168, 1032094, 1089528, 1145822,
             1203420, 1261197, 1318845, 1377629, 1438472, 1500105, 1562800],
            dtype=&#39;int64&#39;),
 173: Int64Index([  10760,   65664,  120588,  230734,  286451,  340742,  397145,
              509561,  623085,  680995,  737508,  793921,  850126,  905802,
              962389, 1019098, 1076573, 1132936, 1189982, 1247992, 1305541,
             1364174, 1424395, 1486158, 1547749],
            dtype=&#39;int64&#39;),
 174: Int64Index([  27055,   81722,  136670,  191553,  247044,  302383,  357380,
              413739,  469842,  525657,  582307,  639922,  697311,  753987,
              810250,  866234,  921893, 1092926, 1149237, 1206843, 1264601,
             1322254, 1381217, 1442095, 1503664, 1566653],
            dtype=&#39;int64&#39;),
 176: Int64Index([  49823,  104031,  162242,  213642,  269470,  324262,  384001,
              440658,  492310,  548177,  605203,  663352,  720466,  776788,
              832932,  892584, 1291740, 1345043, 1404682, 1471524, 1532897,
             1594033],
            dtype=&#39;int64&#39;),
 180: Int64Index([ 366415, 1101975, 1158115, 1216156, 1273906, 1331393, 1390650,
             1452068, 1513417, 1577125],
            dtype=&#39;int64&#39;),
 181: Int64Index([   9198,   64159,  119056,  174063,  229193,  284974,  339200,
              395609,  452184,  508110,  564321,  621576,  679494,  735986,
              792398,  848601,  904304,  960900, 1017540, 1075040, 1131423,
             1188377, 1246442, 1304000, 1362540, 1422641, 1484506, 1545972],
            dtype=&#39;int64&#39;),
 186: Int64Index([  26256,   80964,  135887,  190782,  246310,  301636,  356594,
              412924,  469043,  524870,  581503,  639104,  696530,  753207,
              809436,  921139,  977765, 1034778, 1092131, 1148408, 1206041,
             1263802, 1321431, 1380369, 1441236, 1502844, 1565781],
            dtype=&#39;int64&#39;),
 192: Int64Index([1579876], dtype=&#39;int64&#39;),
 194: Int64Index([1455553, 1517021, 1580972], dtype=&#39;int64&#39;),
 203: Int64Index([   5095,   60133,  115002,  170006,  224993,  280985,  335000,
              391469,  448005,  504035,  560192,  617289,  675358,  731863,
              788255,  844465,  900220,  956914, 1013352, 1070901, 1127247,
             1184034, 1242131, 1299742, 1358085, 1418101, 1479990, 1541089],
            dtype=&#39;int64&#39;),
 204: Int64Index([  15405,   70300,  125274,  180208,  235467,  291086,  345600,
              401846,  458355,  570622,  627938,  685628,  742230,  798561,
              854728,  910390,  966988, 1023811, 1194744, 1252739, 1310318,
             1369004, 1429479, 1491221, 1553192],
            dtype=&#39;int64&#39;),
 205: Int64Index([ 318991,  379909,  436475,  491992,  547855,  604859,  663004,
              720111,  776495,  832601,  888189,  944309, 1000769, 1058178,
             1115185, 1171452, 1229351, 1286913, 1344715, 1404377, 1466398,
             1527657, 1593624],
            dtype=&#39;int64&#39;),
 207: Int64Index([  46474,  433449,  488976,  607451,  659857,  716854,  779185,
              829690,  890866,  947159, 1061134, 1118057, 1174327, 1232300,
             1289763, 1347635, 1469476, 1530863, 1597055],
            dtype=&#39;int64&#39;),
 209: Int64Index([  29936,   84482,  139436,  194309,  249876,  305109,  360254,
              416680,  472690,  528480,  585197,  642867,  700162,  756823,
              813063,  869014,  924676,  981342, 1038433, 1095826, 1152065,
             1209836, 1267585, 1325143, 1384246, 1445272, 1506737, 1569931],
            dtype=&#39;int64&#39;),
 212: Int64Index([1254169, 1311710, 1370342, 1430932, 1492671, 1554798], dtype=&#39;int64&#39;),
 213: Int64Index([1570295], dtype=&#39;int64&#39;),
 215: Int64Index([  47188,  101371,  156146,  210989,  266778,  321657,  377674,
              434192,  489752,  545623,  602638,  660721,  717819,  774280,
              830461,  886063,  941945,  998413, 1055835, 1112984, 1169333,
             1227268, 1284826, 1342505, 1402079, 1464053, 1525366, 1591075],
            dtype=&#39;int64&#39;),
 216: Int64Index([  11008,   65901,  120850,  175795,  230960,  286679,  340996,
              397402,  453910,  509808,  566118,  623331,  681250,  737775,
              794171,  850362,  906058,  962643, 1019360, 1076828, 1133174,
             1190228, 1248244, 1305806, 1364439, 1424682, 1486414, 1548036],
            dtype=&#39;int64&#39;),
 217: Int64Index([   9973,   64933,  119802,  174797,  229932,  285691,  339946,
              396377,  452916,  508809,  565054,  622306,  680207,  736727,
              793161,  849332,  905037,  961612, 1018265, 1075778, 1132160,
             1189169, 1247220, 1304729, 1363335, 1423470, 1485299, 1546821],
            dtype=&#39;int64&#39;),
 218: Int64Index([  60664,  115517,  170508,  225532,  281504,  391984,  448515,
              504553,  560723,  617823,  675882,  732392,  788808,  844999,
              957425, 1013878, 1071425, 1127755, 1184572, 1242679, 1418660,
             1480579, 1541682],
            dtype=&#39;int64&#39;),
 219: Int64Index([ 180447,  235737,  345883,  570866,  685926,  742502,  855020,
              967245, 1024087, 1081524, 1137892, 1195039, 1253039, 1310626,
             1369255, 1429779, 1491509, 1553544],
            dtype=&#39;int64&#39;),
 223: Int64Index([  38842,   93122,  147929,  202688,  258426,  369047,  425528,
              481250,  537072,  593865,  651865,  708789,  765633,  821928,
              877720,  933472,  989864, 1047189, 1104569, 1160726, 1218845,
             1276491, 1333936, 1393353, 1454787, 1516278, 1580161],
            dtype=&#39;int64&#39;),
 226: Int64Index([  37477,   91795,  146606,  201387,  257067,  312214,  367668,
              424183,  479967,  535741,  592544,  650546,  764309,  820634,
              876400,  932058,  988558, 1045808, 1103266, 1159396, 1217473,
             1275132, 1332614, 1391965, 1453401, 1514821, 1578628],
            dtype=&#39;int64&#39;),
 232: Int64Index([  46853,  101016,  155805,  210633,  266448,  321293,  377347,
              433829,  489369,  545228,  602220,  660264,  717243,  773782,
              830030,  885678,  941517,  997994, 1055378, 1112480, 1168848,
             1226884, 1284420, 1342087, 1401670, 1463635, 1524906, 1590317],
            dtype=&#39;int64&#39;),
 247: Int64Index([  24648,   79426,  134362,  189290,  244763,  300131,  355008,
              411290,  467464,  523297,  579940,  637467,  694924,  751619,
              807848,  863910,  919537,  976190, 1033124, 1090540, 1146828,
             1204469, 1262247, 1319867, 1378736, 1439576, 1501194, 1563973],
            dtype=&#39;int64&#39;),
 250: Int64Index([  39471,   93717,  148532,  203280,  259022,  314064,  369684,
              426177,  481888,  537717,  594510,  652506,  709394,  766251,
              822567,  878360,  934075,  990455, 1047784, 1105179, 1161336,
             1219472, 1277115, 1334568, 1393997, 1455447, 1516916, 1580858],
            dtype=&#39;int64&#39;),
 251: Int64Index([ 160774,  326262,  382307,  438991,  494663,  550486,  607458,
              722863,  779191,  835340,  890871,  947164, 1003604, 1061141,
             1118062, 1174334, 1232307, 1289767, 1347639, 1407336, 1469480,
             1530867, 1597059],
            dtype=&#39;int64&#39;),
 253: Int64Index([ 150000,  204803,  260506,  315529,  371226,  483371,  539227,
              596003,  654067,  710888,  767767,  824049,  879816,  935503,
              991931, 1049298, 1106667, 1162807, 1221078, 1278627, 1336048,
             1395539, 1457092, 1518496, 1582566],
            dtype=&#39;int64&#39;),
 255: Int64Index([ 948470, 1004866, 1055551, 1119376, 1169014, 1227045, 1284611,
             1342265, 1401839, 1463811, 1525090, 1590512],
            dtype=&#39;int64&#39;),
 257: Int64Index([  13071,   68004,  122978,  177939,  233130,  288803,  343217,
              399532,  456061,  511966,  568275,  625547,  683393,  739968,
              796297,  852500,  908143, 1135298, 1192377, 1250352, 1307956,
             1366664, 1426986, 1488712, 1550519],
            dtype=&#39;int64&#39;),
 260: Int64Index([ 387150,  443776,  499848,  555800,  612780,  671123,  783913,
              840159,  895929, 1122933, 1237635, 1475280, 1536120],
            dtype=&#39;int64&#39;),
 262: Int64Index([  41999,   96151,  150971,  205802,  261551,  316485,  372322,
              428780,  484425,  540260,  597072,  655167,  711915,  768810,
              825097,  880855,  936544,  992984, 1050368, 1107675, 1163864,
             1222210, 1279763, 1337145, 1396664, 1458296, 1519679, 1583782],
            dtype=&#39;int64&#39;),
 266: Int64Index([  18523,   73391,  128404,  183212,  238605,  294183,  348840,
              404982,  461428,  517295,  573709,  631169,  688808,  745394,
              801636,  857830,  913475,  970039, 1026862, 1084378, 1140723,
             1197989, 1255941, 1313572, 1372236, 1432863, 1474841, 1535642],
            dtype=&#39;int64&#39;),
 268: Int64Index([1159390, 1217465, 1275128, 1332605, 1391957, 1453392, 1514813,
             1578620],
            dtype=&#39;int64&#39;),
 273: Int64Index([  29772,   84315,  139287,  194140,  249714,  304946,  360077,
              416502,  472523,  528318,  585035,  642696,  699997,  756664,
              812906,  868860,  924525,  981173, 1038259, 1095676, 1151904,
             1209670, 1267430, 1324981, 1384100, 1445097, 1506570, 1569750],
            dtype=&#39;int64&#39;),
 276: Int64Index([  10616,   65513,  120424,  230571,  286293,  340575,  396989,
              453515,  509400,  565696,  622921,  680823,  737350,  793763,
              849953,  905637,  962214, 1018920, 1076397, 1132763, 1189793,
             1247820, 1305385, 1364011, 1424208, 1485973, 1547557],
            dtype=&#39;int64&#39;),
 280: Int64Index([  37333,   91662,  146482,  201259,  256937,  312089,  367539,
              424030,  479819,  535619,  592405,  650391,  707332,  764184,
              820492,  876271,  931914,  988412, 1045663, 1103118, 1159254,
             1217323, 1274992, 1332473, 1391822, 1453249, 1514673, 1578455],
            dtype=&#39;int64&#39;),
 281: Int64Index([  56199,  221026,  277199,  330966,  387457,  444073,  500140,
              556134,  613100,  727749,  784233,  840465,  896217, 1009393,
             1066945, 1123250, 1237928, 1353801, 1413734, 1475610, 1536439],
            dtype=&#39;int64&#39;),
 283: Int64Index([  48968,  103161,  157907,  212707,  268552,  323332,  379304,
              435882,  491401,  547258,  604291,  662395,  719558,  775912,
              832077,  887658,  943648, 1000151, 1057567, 1114624, 1170871,
             1228768, 1286401, 1344115, 1403816, 1465783, 1527091, 1592961],
            dtype=&#39;int64&#39;),
 284: Int64Index([  44704,   98759,  153621,  208440,  264222,  319125,  375034,
              431433,  487012,  542855,  599754,  657832,  714780,  771487,
              827737,  883394,  939144,  995580, 1052992, 1110289, 1166525,
             1224832, 1282374, 1339850, 1399430, 1461212, 1522474, 1587259],
            dtype=&#39;int64&#39;),
 287: Int64Index([  76235,  131247,  186104,  241573,  296978,  351816,  407960,
              464251,  520103,  576656,  634178,  691693,  748337,  804599,
              860756,  916353,  972958, 1029878, 1087309, 1143682, 1201119,
             1258963, 1316634, 1375351, 1436149, 1497782, 1560287],
            dtype=&#39;int64&#39;),
 288: Int64Index([ 888329,  941722, 1000938, 1058360, 1115341, 1171587, 1228042,
             1285638, 1344871, 1404523, 1464939, 1526243, 1590543],
            dtype=&#39;int64&#39;),
 289: Int64Index([1529440, 1595543], dtype=&#39;int64&#39;),
 295: Int64Index([  23412,   78165,  133154,  188062,  243535,  298912,  353776,
              409994,  466187,  522030,  578685,  636223,  693713,  750374,
              806603,  862718,  918284,  974929, 1031866, 1089279, 1145581,
             1203159, 1260957, 1318580, 1377390, 1438233, 1499849, 1562526],
            dtype=&#39;int64&#39;),
 298: Int64Index([1561519], dtype=&#39;int64&#39;),
 299: Int64Index([  26576,   81272,  136186,  191087,  246597,  301935,  356904,
              413251,  469354,  525186,  581828,  639432,  696849,  753502,
              809742,  865764,  921425,  978076, 1035095, 1092449, 1148746,
             1206356, 1264102, 1321757, 1380703, 1441576, 1503162, 1566124],
            dtype=&#39;int64&#39;),
 305: Int64Index([  99412,  209050,  319742,  375634,  487760,  543673,  658678,
              772253,  828570,  884128,  939953,  996445, 1053859, 1110887,
             1167254, 1225313, 1282863, 1340449, 1400063, 1461894, 1523244,
             1588505],
            dtype=&#39;int64&#39;),
 308: Int64Index([ 249501,  304721,  359855,  416261,  584773,  642476,  699777,
              980942, 1209434, 1267183, 1324770, 1444827, 1506330, 1569475],
            dtype=&#39;int64&#39;),
 309: Int64Index([   1030,   56173,  111079,  166208,  221004,  277174,  330937,
              387421,  444044,  500113,  556105,  613072,  671390,  727719,
              784198,  840435,  896188,  953000, 1009369, 1066920, 1123219,
             1179839, 1237904, 1295562, 1353771, 1413703, 1475574, 1536409],
            dtype=&#39;int64&#39;),
 310: Int64Index([  17556,   72463,  127440,  182359,  237714,  293258,  347875,
              404065,  460516,  516366,  572773,  630240,  687861,  744455,
              800718,  856909,  912525,  969116, 1025974, 1083442, 1139804,
             1197034, 1255005, 1312649, 1371253, 1431878, 1493573, 1555776],
            dtype=&#39;int64&#39;),
 311: Int64Index([  53713,  108176,  163068,  218003,  273989,  328717,  384851,
              441527,  497350,  553100,  609993,  668333,  725520,  781792,
              837818,  893379,  949923, 1006290, 1063825, 1119769, 1176093,
             1234142, 1291552, 1349454, 1409176, 1471350, 1532713, 1599121],
            dtype=&#39;int64&#39;),
 326: Int64Index([  44134,  100771,  152999,  207862,  263634,  318519,  377099,
              430865,  489145,  542238,  599159,  657205,  714147,  770849,
              827149,  882822,  938562,  994985, 1052389, 1109748, 1165957,
             1226662, 1281842, 1339239, 1398832, 1460571, 1521840, 1586254],
            dtype=&#39;int64&#39;),
 327: Int64Index([512742, 1586279], dtype=&#39;int64&#39;),
 328: Int64Index([  18145,   73036,  128037,  182888,  238268,  293830,  348482,
              404644,  461101,  516927,  573371,  630826,  688446,  745049,
              801297,  857477,  913118,  969700, 1026536, 1084028, 1140374,
             1197649, 1255590, 1313243, 1371857, 1432503, 1494188, 1556413],
            dtype=&#39;int64&#39;),
 330: Int64Index([741326, 853875, 1136678, 1251807, 1309343, 1552133], dtype=&#39;int64&#39;),
 334: Int64Index([  42302,   96437,  151269,  206099,  261829,  316764,  372626,
              429096,  484722,  540569,  597369,  655458,  712453,  769097,
              825418,  881170,  936841,  993272, 1050662, 1108007, 1164185,
             1222519, 1280094, 1337465, 1396993, 1458631, 1519999, 1584110],
            dtype=&#39;int64&#39;),
 335: Int64Index([  28124,   82735,  137676,  192571,  248108,  303404,  358423,
              414862,  470915,  526673,  583357,  617320,  698358,  755027,
              811280,  867261,  922892,  979517, 1036559, 1093995, 1150263,
             1207910, 1265689, 1323298, 1382344, 1443254, 1504788, 1567884],
            dtype=&#39;int64&#39;),
 337: Int64Index([  39097,   93356,  148157,  166606,  229332,  285107,  339355,
              395749,  452314,  508243,  564455,  621711,  679627,  736125,
              792552,  848733,  904441,  961036, 1017679, 1075188, 1131567,
             1188538, 1246588, 1304128, 1362688, 1422804, 1484651, 1546124],
            dtype=&#39;int64&#39;),
 340: Int64Index([  35064,   89372,  144209,  199083,  254687,  309881,  365223,
              421779,  477635,  533442,  590209,  648080,  705118,  761931,
              818205,  873980,  907207,  986203, 1043412, 1100831, 1156979,
             1214980, 1272712, 1330183, 1389484, 1450771, 1512112, 1575759],
            dtype=&#39;int64&#39;),
 341: Int64Index([  10742,   65646,  120569,  175529,  230718,  286434,  340726,
              397130,  453653,  509541,  565852,  623065,  680972,  737489,
              793903,  850107,  905782,  962369, 1019079, 1076552, 1132917,
             1189959, 1247973, 1305522, 1364158, 1424375, 1486141, 1547726],
            dtype=&#39;int64&#39;),
 344: Int64Index([  23147,   77917,  132881,  187815,  243270,  298667,  353542,
              409734,  465945,  521790,  578436,  635972,  693467,  750120,
              806349,  862469,  918051,  974681, 1031625, 1089031, 1145337,
             1202903, 1260698, 1318332, 1377127, 1437978, 1499587, 1562247],
            dtype=&#39;int64&#39;),
 345: Int64Index([1504521, 1567594], dtype=&#39;int64&#39;),
 347: Int64Index([  52628,  107012,  158672,  216740,  272703,  327418,  383585,
              440241,  495989,  551793,  608775,  667112,  724226,  780591,
              836635,  892195,  948637, 1005034, 1062606, 1119519, 1175843,
             1233887, 1291284, 1349188, 1408899, 1471093, 1532441, 1598831],
            dtype=&#39;int64&#39;),
 350: Int64Index([    278,   55469,  110393,  165496,  220337,  276492,  330188,
              386675,  443317,  499402,  555336,  612293,  670687,  727024,
              783479,  839724,  895471,  952265, 1008632, 1066182, 1122462,
             1179064, 1237122, 1294807, 1353022, 1412945, 1474813, 1535616],
            dtype=&#39;int64&#39;),
 352: Int64Index([  45967,  100109,  154907,  209707,  265521,  320383,  376362,
              432927,  488457,  544325,  601315,  659363,  716368,  772910,
              829203,  884777,  940624,  997086, 1051623, 1111551, 1167949,
             1225998, 1283537, 1341142, 1400753, 1462643, 1523946, 1589248],
            dtype=&#39;int64&#39;),
 358: Int64Index([  29520,   84066,  139045,  193926,  249468,  359810,  416228,
              472251,  528039,  584738,  642439,  699747,  756401,  812663,
              868622,  924251,  980906, 1037961, 1095398, 1151626, 1209395,
             1267156, 1324742, 1383814, 1444787, 1506292, 1569435],
            dtype=&#39;int64&#39;),
 362: Int64Index([  39430,   93678,  148486,  203238,  258982,  314015,  369645,
              426136,  481846,  537671,  594466,  652465,  709350,  766207,
              822524,  878314,  934029,  990414, 1047742, 1105138, 1161296,
             1219430, 1277062, 1334519, 1393953, 1455401, 1516874, 1580812],
            dtype=&#39;int64&#39;),
 365: Int64Index([  11688,   66604,  176498,  231640,  287411,  341730,  398117,
              454635,  510499,  566824,  624075,  681961,  738481,  794870,
              851055,  906752,  963315, 1020067, 1077513, 1133861, 1190895,
             1248928, 1306522, 1365165, 1425418, 1487165, 1548824],
            dtype=&#39;int64&#39;),
 368: Int64Index([ 718996,  775397,  831542,  887132,  943111,  999591, 1057007,
             1114077, 1170343, 1228247, 1285855, 1343569, 1403256, 1465222,
             1526549, 1592351],
            dtype=&#39;int64&#39;),
 371: Int64Index([   1371,   56511,  111414,  166530,  221339,  277497,  331291,
              387790,  444394,  500470,  556492,  613487,  671807,  728121,
              784580,  840808,  896556,  953361, 1009732, 1067284, 1123590,
             1180214, 1238271, 1295924, 1354162, 1414111, 1476017, 1536865],
            dtype=&#39;int64&#39;),
 372: Int64Index([  61869,  116720,  171717,  226764,  282677,  336812,  393187,
              619127,  677114,  733590,  846260,  901962, 1243936, 1301490,
             1359910, 1419969, 1481916, 1543084],
            dtype=&#39;int64&#39;),
 373: Int64Index([ 215174,  271025,  325831,  381845,  438527,  494183,  550007,
              606984,  665274,  722351,  778671,  834817,  890351,  946656,
             1003091, 1060594, 1117512, 1173775, 1231743, 1289220, 1347065,
             1406748, 1468880, 1530267, 1596415],
            dtype=&#39;int64&#39;),
 390: Int64Index([  41025,   95157,  150009,  204816,  260521,  315540,  371238,
              427732,  483385,  539248,  654094,  710909,  767789,  824065,
              879837,  935519,  991957, 1049319, 1106683, 1336074, 1395560,
             1518525, 1582590],
            dtype=&#39;int64&#39;),
 391: Int64Index([  10150,  565244,  736898,  793340,  905194, 1018452, 1132322,
             1189359, 1247391, 1304916, 1363513, 1423675, 1485494, 1547022],
            dtype=&#39;int64&#39;),
 393: Int64Index([  38942,   93202,  148008,  202768,  258517,  313547,  369150,
              425617,  481364,  537159,  593960,  651971,  708865,  765722,
              822029,  877819,  933565,  989948, 1047276, 1104651, 1160825,
             1218925, 1276581, 1334028, 1393455, 1454877, 1516370, 1580268],
            dtype=&#39;int64&#39;),
 396: Int64Index([  17908,   72806,  127795,  182666,  238038,  293601,  348241,
              404407,  460855,  516698,  573136,  630583,  688209,  744807,
              801052,  857238,  912869,  969467, 1026302, 1083792, 1140152,
             1197412, 1255354, 1313007, 1371619, 1432259, 1493954, 1556166],
            dtype=&#39;int64&#39;),
 400: Int64Index([  22479,   77275,  132271,  187151,  242613,  297998,  352886,
              409047,  465316,  521144,  577717,  635295,  692799,  749427,
              805701,  861819,  917399,  974046, 1030942, 1088380, 1144699,
             1202243, 1260017, 1317677, 1376466, 1437286, 1498869, 1561494],
            dtype=&#39;int64&#39;),
 403: Int64Index([  28765,   83342,  138286,  193178,  248727,  303994,  359054,
              415484,  471506,  527285,  583983,  641627,  698996,  755653,
              811933,  867910,  923519,  980108, 1037174, 1094656, 1150890,
             1208614, 1266353, 1323967, 1383002, 1443932, 1505485, 1568592],
            dtype=&#39;int64&#39;),
 404: Int64Index([  29499,   84047,  139025,  193907,  249448,  304672,  359788,
              416209,  472233,  528024,  584719,  642421,  699734,  769683,
              812644,  868608,  924237,  980891, 1037944, 1095384, 1151614,
             1209384, 1267138, 1324719, 1383793, 1444758, 1506276, 1569412],
            dtype=&#39;int64&#39;),
 405: Int64Index([  12582,   67514,  122479,  177434,  232618,  288325,  342714,
              399042,  455556,  511472,  567753,  625026,  682894,  739439,
              795789,  851997,  907658,  964215, 1021012, 1078452, 1134808,
             1191863, 1249839, 1307446, 1366150, 1426453, 1488186, 1549950],
            dtype=&#39;int64&#39;),
 409: Int64Index([  48162,  102329,  157088,  211919,  267738,  322562,  378530,
              435075,  490630,  546484,  603508,  661603,  718723,  775162,
              831298,  886888,  942835,  999331, 1056735, 1113811, 1285652,
             1344889, 1402997, 1464952, 1526258, 1592052],
            dtype=&#39;int64&#39;),
 411: Int64Index([  30599,   85075,  140032,  166471,  221281,  305730,  360875,
              417322,  473293,  529072,  757476,  813665,  869627,  925282,
              981948, 1039111, 1096438, 1152697, 1210484, 1268215, 1325800,
             1384908, 1445964, 1507407, 1570668],
            dtype=&#39;int64&#39;),
 413: Int64Index([  12702,   67627,  122599,  177552,  232759,  288448,  342840,
              399166,  455684,  511595,  567889,  625160,  683024,  739578,
              795909,  852128,  907774,  964346, 1021149, 1078573, 1134928,
             1191996, 1249980, 1307561, 1366271, 1426584, 1488321, 1550095],
            dtype=&#39;int64&#39;),
 420: Int64Index([1060501, 1104568, 1173680, 1231649, 1289129, 1346972, 1406652,
             1468771, 1530162, 1596306],
            dtype=&#39;int64&#39;),
 423: Int64Index([  21772,   76578,  131590,  186439,  241901,  297316,  352171,
              408314,  464608,  520445,  576991,  634537,  692065,  748696,
              804944,  861105,  916703,  973311, 1030235, 1087678, 1144028,
             1201483, 1259306, 1316981, 1375725, 1436523, 1498136, 1560678],
            dtype=&#39;int64&#39;),
 425: Int64Index([  42083,   96236,  151054,  205889,  261629,  316568,  372418,
              428878,  484515,  540356,  597165,  655258,  711999,  768898,
              825184,  880951,  936643,  993083, 1050467, 1107773, 1163967,
             1222303, 1279860, 1337243, 1396769, 1458399, 1519782, 1583888],
            dtype=&#39;int64&#39;),
 426: Int64Index([ 157500,  212312,  268136,  322926,  378899,  435468,  490995,
              546845,  603882,  661984,  719137,  775533,  831677,  887262,
              943240,  999718, 1057134, 1114207, 1170473, 1228368, 1285981,
             1343710, 1403379, 1465355, 1528163, 1592506],
            dtype=&#39;int64&#39;),
 429: Int64Index([ 247287,  413994,  525919,  582550,  697573,  754234,  810512,
              866481,  922147,  978736, 1035781, 1093197, 1149479, 1207089,
             1264857, 1322489, 1381468, 1442369, 1503932, 1566941],
            dtype=&#39;int64&#39;),
 446: Int64Index([   7401,   62432,  117315,  172291,  227368,  283255,  337400,
              393748,  444443,  506345,  562501,  619715,  677688,  732042,
              790553,  846816,  902507,  959133, 1015689, 1073204, 1129619,
             1186441, 1244534, 1302090, 1360506, 1420609, 1482527, 1543784],
            dtype=&#39;int64&#39;),
 449: Int64Index([ 298963,  578732,  636271,  693763,  750431,  806649,  862762,
              918333,  974975, 1031913, 1089322, 1145627, 1203215, 1261003,
             1318640, 1438282, 1499905, 1562583],
            dtype=&#39;int64&#39;),
 456: Int64Index([  25122,   79869,  134788,  189717,  245196,  300536,  355461,
              411764,  467914,  523748,  580407,  637943,  695377,  752066,
              808314,  864344,  920010,  976635, 1033598, 1090990, 1147270,
             1262707, 1320316, 1379209, 1440051, 1501687, 1564501],
            dtype=&#39;int64&#39;),
 458: Int64Index([  15752,   70661,  125631,  180519,  235807,  291426,  345966,
              402227,  458716,  514559,  570935,  628299,  685992,  742582,
              798917,  855095,  910731,  967322, 1024164, 1081603, 1137965,
             1195116, 1253108, 1310705, 1369331, 1429861, 1491590, 1553627],
            dtype=&#39;int64&#39;),
 462: Int64Index([  51010,  105316,  160118,  214911,  270743,  325544,  381547,
              438241,  493766,  549697,  606666,  664943,  722019,  778339,
              834490,  890016,  946313,  965268, 1060245, 1117185, 1173426,
             1231374, 1288871, 1346719, 1367198, 1468485, 1529845, 1595984],
            dtype=&#39;int64&#39;),
 473: Int64Index([  24444,  134170,  189064,  244547,  299933,  354806,  523088,
              579740,  637273,  694736,  751436,  807656,  863724,  919343,
              975969, 1032914, 1090339, 1146604, 1204238, 1262022, 1319648,
             1378517, 1439338, 1563739],
            dtype=&#39;int64&#39;),
 474: Int64Index([  14933,   69821,  124817,  179784,  235012,  290630,  345134,
              685187,  909952, 1023385, 1080779, 1137159, 1194283, 1252282,
             1309847, 1368572, 1429002, 1490743, 1552644],
            dtype=&#39;int64&#39;),
 475: Int64Index([  50758,  105039,  159848,  214630,  270451,  325252,  381242,
              437922,  493450,  549379,  606327,  664573,  721677,  777986,
              834143,  889658,  945939, 1002412, 1059843, 1116812, 1230982,
             1288497, 1346352, 1406018, 1468103, 1529418, 1595519],
            dtype=&#39;int64&#39;),
 476: Int64Index([  23823,   78555,  133556,  188430,  243923,  299308,  354172,
              410412,  466576,  522431,  579064,  636615,  694081,  750770,
              806990,  863106,  918692,  975318, 1032250, 1089677, 1145966,
             1203571, 1261352, 1318999, 1377794, 1438636, 1500267, 1562975],
            dtype=&#39;int64&#39;),
 484: Int64Index([  20159,   75025,  130023,  184836,  240245,  295751,  350516,
              406632,  463055,  518899,  632843,  690444,  747050,  803311,
              859470,  915112,  971662, 1028527, 1086045, 1142397, 1199716,
             1257657, 1315311, 1374009, 1434647, 1496365, 1558756],
            dtype=&#39;int64&#39;),
 487: Int64Index([  44585,   98642,  153501,  208334,  264114,  319016,  374923,
              431332,  486898,  542735,  599646,  657723,  714652,  771361,
              827613,  883274,  939026,  995460, 1052862, 1110187, 1166415,
             1224717, 1282256, 1339740, 1399306, 1461076, 1522333, 1587126],
            dtype=&#39;int64&#39;),
 488: Int64Index([  27798,   82423,  137375,  192281,  303104,  358129,  414542,
              470623,  526389,  583047,  640694,  698050,  754732,  810990,
              866954,  922615,  979222, 1036266, 1093694, 1149971, 1207588,
             1265354, 1322981, 1382008, 1442888, 1504449, 1567520],
            dtype=&#39;int64&#39;),
 492: Int64Index([  14017,   68950,  123937,  178898,  234102,  289737,  344191,
              400493,  457022,  512883,  569263,  626539,  684309,  740901,
              797243,  853427,  909083,  965695, 1022498, 1079891, 1136232,
             1193366, 1251340, 1308921, 1367659, 1428031, 1489786, 1551605],
            dtype=&#39;int64&#39;),
 494: Int64Index([  41078,   95209,  204877,  260589,  315595,  371304,  483444,
              539304,  596074,  654154,  710964,  767841,  824130,  879888,
              935570,  992025, 1049388, 1106733, 1162879, 1221161, 1278694,
             1336122, 1395620, 1457183, 1518588, 1582657],
            dtype=&#39;int64&#39;),
 506: Int64Index([ 339849,  396273,  452804,  508719,  564955,  622216,  680123,
              736625,  793067,  849231,  904942,  961521, 1018170, 1075688,
             1132055, 1189063, 1247118, 1304633, 1363235, 1423351, 1485196,
             1546696],
            dtype=&#39;int64&#39;),
 510: Int64Index([  13190,   68121,  123089,  178052,  233243,  288919,  343338,
              399658,  456184,  512074,  568384,  625643,  683493,  740067,
              796398,  852595,  908249,  964836, 1021631, 1079057, 1135403,
             1192487, 1250471, 1308068, 1366790, 1427111, 1488848, 1550642],
            dtype=&#39;int64&#39;),
 523: Int64Index([  40978,   95108,  149967,  260464,  315487,  371182,  427679,
              483336,  539186,  595967,  654026,  710856,  767721,  824010,
              879779,  935467,  991889, 1049253, 1106626, 1162767, 1221023,
             1278571, 1395491, 1457042, 1518455, 1582519],
            dtype=&#39;int64&#39;),
 525: Int64Index([  78055,  133027,  187952,  243412,  298799,  353669,  409880,
              466073,  521931,  636114,  693607,  750265,  806487,  862607,
              918176,  974817, 1031758, 1145472, 1203038, 1260836, 1318464,
             1438115, 1499735, 1562403],
            dtype=&#39;int64&#39;),
 526: Int64Index([  10738,   65642,  120565,  175524,  230711,  286430,  340721,
              397125,  453648,  509536,  565846,  623060,  680965,  737484,
              793899,  850101,  905776,  962364, 1019074, 1076545, 1132909,
             1189954, 1247969, 1305517, 1364149, 1424368, 1486136, 1547718],
            dtype=&#39;int64&#39;),
 527: Int64Index([  37616,   91925,  146743,  201505,  257195,  312341,  367803,
              424310,  480097,  535864,  592676,  650680,  707602,  764438,
              820765,  876527,  932187,  988682, 1045939, 1103400, 1159531,
             1217628, 1275267, 1332749, 1392100, 1453545, 1514961, 1578778],
            dtype=&#39;int64&#39;),
 528: Int64Index([  36928,   91223,  367112,  423610,  535235,  592012,  649986,
              820070,  875866,  931496, 1045258, 1102679, 1158845, 1216882,
             1274599, 1332058, 1391408, 1452834, 1514216, 1577957],
            dtype=&#39;int64&#39;),
 532: Int64Index([  18664,   73541,  128561,  238756,  294324,  348980,  405133,
              461559,  517430,  573855,  631328,  688961,  745546,  801787,
              857967,  913615,  970176, 1027012, 1084503, 1140860, 1198144,
             1256088, 1313743, 1372397, 1433016, 1494703, 1557006],
            dtype=&#39;int64&#39;),
 536: Int64Index([ 576706,  634231,  691747,  748389,  804647,  860806,  916411,
              973008, 1029940, 1087367, 1143737, 1201176, 1259013, 1316684,
             1375406, 1436196, 1497831, 1560346],
            dtype=&#39;int64&#39;),
 538: Int64Index([   8139,   63146,  118032,  173000,  228108,  283957,  338121,
              394527,  451132,  507079,  563248,  620493,  678444,  734914,
              791342,  847578,  903270,  959848, 1016437, 1073954, 1130381,
             1187230, 1245322, 1302904, 1361350, 1421430, 1483338, 1544684],
            dtype=&#39;int64&#39;),
 541: Int64Index([  43037,   97105,  151915,  206730,  262518,  317436,  373316,
              429775,  485365,  541204,  598081,  656129,  713080,  769750,
              826104,  881817,  937541,  993928, 1051309, 1108653, 1164864,
             1223199, 1280770, 1338120, 1397675, 1459381, 1520722, 1584900],
            dtype=&#39;int64&#39;),
 542: Int64Index([  15614,   70523,  125499,  180386,  235678,  291302,  345818,
              402081,  458565,  514420,  570800,  628155,  685852,  742430,
              798772,  854951,  910599,  967180, 1024023, 1081450, 1137819,
             1194963, 1252969, 1310557, 1369188, 1429715, 1491421, 1553458],
            dtype=&#39;int64&#39;),
 546: Int64Index([  39496,   93741,  148558,  203305,  259046,  314091,  369709,
              426203,  481913,  537744,  594535,  652531,  709420,  766279,
              822594,  878387,  934102,  990482, 1047811, 1105208, 1161361,
             1219501, 1277140, 1334593, 1394023, 1455473, 1516943, 1580887],
            dtype=&#39;int64&#39;),
 550: Int64Index([  25418,   80165,  135061,  189986,  245486,  300830,  355738,
              412058,  468203,  524032,  580694,  638261,  695682,  752370,
              808605,  864645,  920319,  976934, 1033932, 1091284, 1147566,
             1205224, 1263010, 1320617, 1379527, 1440359, 1501978, 1564838],
            dtype=&#39;int64&#39;),
 555: Int64Index([  50397,   99658,  159493,  214268,  270089,  324876,  380809,
              437490,  493001,  548944,  605896,  662197,  721214,  777529,
              833669,  889194,  945471, 1001956, 1057351, 1116311, 1170659,
             1228558, 1288011, 1345871, 1403596, 1467588, 1528869, 1594961],
            dtype=&#39;int64&#39;),
 556: Int64Index([  10268,   65184,  120080,  175065,  230196,  285948,  340247,
              396641,  453172,  509070,  565352,  622581,  676868,  736998,
              793430,  849597,  905293,  961869, 1018553, 1076044, 1132424,
             1189457, 1247489, 1305010, 1363617, 1423796, 1485610, 1547142],
            dtype=&#39;int64&#39;),
 560: Int64Index([1282639, 1340214, 1399842, 1461638, 1522999, 1588058], dtype=&#39;int64&#39;),
 561: Int64Index([  39042,   93303,  148104,  202861,  258613,  313646,  369248,
              425723,  481467,  537259,  594063,  652071,  708965,  765818,
              822120,  877920,  933651,  990042, 1047375, 1104747, 1160907,
             1219016, 1276665, 1334123, 1393551, 1454982, 1516460, 1580365],
            dtype=&#39;int64&#39;),
 562: Int64Index([  45404,   99507,  375729,  432321,  487850,  543779,  600704,
              658764,  715808,  772355,  828652,  884218,  940050,  996534,
             1053947, 1110982, 1167353, 1225414, 1282967, 1340555, 1400152,
             1462002, 1523330, 1588615],
            dtype=&#39;int64&#39;),
 563: Int64Index([  15694,   70598,  125572,  180460,  235752,  291371,  345900,
              402162,  458657,  514504,  570880,  628239,  685938,  742524,
              798854,  855034,  910673,  967258, 1024102, 1081543, 1137909,
             1195053, 1253053, 1310640, 1429794, 1491523, 1553560],
            dtype=&#39;int64&#39;),
 571: Int64Index([  29456,   84001,  138971,  193849,  249405,  304628,  359743,
              416153,  472187,  527978,  584667,  642364,  699687,  756338,
              812600,  868553,  924191,  980834, 1037897, 1095338, 1151553,
             1209323, 1267087, 1324670, 1383735, 1444697, 1483750, 1569359],
            dtype=&#39;int64&#39;),
 574: Int64Index([  35910,   90241,  145056,  199893,  255529,  310679,  366077,
              422613,  478466,  534244,  591034,  648952,  705963,  762792,
              819054,  874815,  930482,  987029, 1044220, 1101655, 1157802,
             1215812, 1273577, 1331063, 1390318, 1451730, 1513060, 1576756],
            dtype=&#39;int64&#39;),
 582: Int64Index([  30517,  194831,  250386,  305620,  360785,  417224,  473214,
              528985,  585739,  643437,  700688,  757369,  813568,  869531,
              925188,  981849, 1039011, 1096347, 1152598, 1210371, 1268117,
             1384806, 1445864, 1507317, 1570553],
            dtype=&#39;int64&#39;),
 597: Int64Index([  50870,  105151,  159964,  214745,  270569,  325373,  381368,
              438047,  493583,  549502,  606465,  664722,  721809,  778127,
              834289,  889816,  946093, 1002566, 1060019, 1116968, 1173175,
             1231138, 1288651, 1346498, 1406168, 1468253, 1529600, 1595710],
            dtype=&#39;int64&#39;),
 598: Int64Index([  24074,   78808,  133802,  188678,  244160,  299534,  354405,
              410658,  466826,  522690,  579306,  636859,  694316,  751018,
              807270,  863353,  918934,  975558, 1032492, 1089928, 1146225,
             1203832, 1261621, 1319252, 1378072, 1438898, 1500531, 1563259],
            dtype=&#39;int64&#39;),
 604: Int64Index([ 326952,  608230,  666577,  723677,  780049,  836137,  891684,
              948050, 1004460, 1061996, 1118942, 1175238, 1233260, 1290674,
             1348578, 1408265, 1470474, 1531835, 1598158],
            dtype=&#39;int64&#39;),
 606: Int64Index([    280,   55472,  110395,  165498,  220338,  276494,  330190,
              386677,  443319,  499405,  555338,  612296,  670693,  727028,
              783482,  839726,  895473,  952267, 1008635, 1066187, 1122465,
             1179067, 1237125, 1294810, 1353025, 1412947, 1474816, 1535619],
            dtype=&#39;int64&#39;),
 611: Int64Index([  38178,   92491,  147292,  202038,  257755,  312860,  368357,
              424871,  480647,  536423,  593225,  651208,  708131,  764988,
              821321,  877080,  932776,  989228, 1046501, 1103958, 1122566,
             1218163, 1237226, 1333301, 1392649, 1454120, 1515564, 1579393],
            dtype=&#39;int64&#39;),
 612: Int64Index([ 160840,  210253,  997623, 1055023, 1112089, 1168441, 1226512,
             1284053, 1341679, 1401272, 1463213, 1524496, 1589847],
            dtype=&#39;int64&#39;),
 619: Int64Index([   5503,   60541,  115392,  170380,  225408,  281366,  335404,
              391866,  448400,  504436,  560600,  617704,  675758,  732262,
              788675,  844863,  900611,  957297, 1013741, 1071286, 1127625,
             1184437, 1242541, 1300137, 1358545, 1418520, 1480439, 1541537],
            dtype=&#39;int64&#39;),
 623: Int64Index([  50649,  104942,  157766,  214529,  270362,  325156,  381134,
              437799,  493322,  549260,  606208,  664440,  721546,  777870,
              834006,  889534, 1059699, 1116681, 1172891, 1230840, 1288361,
             1405867, 1467966, 1520777, 1592800],
            dtype=&#39;int64&#39;),
 625: Int64Index([  37940,   92249,  147061,  201821,  257521,  312635,  368131,
              424643,  480425,  536188,  593000,  650999,  707917,  764766,
              821102,  876855,  932526,  969774, 1046257, 1103719, 1159854,
             1217950, 1275600, 1333063, 1392415, 1453874, 1515293, 1579107],
            dtype=&#39;int64&#39;),
 632: Int64Index([  29197,   83775,  138742,  193637,  249193,  304422,  359513,
              415926,  471978,  527759,  584461,  699478,  742833,  812389,
              868339,  923987,  980594, 1037681, 1095127, 1151318, 1209087,
             1266844, 1324428, 1383496, 1444452, 1505977, 1569117],
            dtype=&#39;int64&#39;),
 633: Int64Index([  40949,   95078,  149932,  214135,  269946,  315454,  371144,
              427642,  483310,  539155,  595932,  653977,  710822,  767681,
              823971,  879735,  935428,  991848, 1049219, 1106594, 1162733,
             1220981, 1278546, 1335975, 1395452, 1457005, 1518417, 1582475],
            dtype=&#39;int64&#39;),
 635: Int64Index([   9471,   64426,  119303,  174320,  229444,  285220,  339468,
              395883,  452420,  508347,  564557,  621821,  679733,  736239,
              792680,  848840,  904560,  961142, 1017788, 1075306, 1131688,
             1188654, 1246718, 1304236, 1362811, 1422920, 1484762, 1546246],
            dtype=&#39;int64&#39;),
 636: Int64Index([  30901,   85348,  140313,  195189,  250752,  306029,  361170,
              417655,  473590,  529383,  586178,  643849,  701103,  757805,
              813996,  869954,  925617,  982283, 1039430, 1096768, 1153026,
             1210797, 1238358, 1326116, 1385231, 1446304, 1507740, 1571020],
            dtype=&#39;int64&#39;),
 637: Int64Index([    500,   55679,  110605,  165706,  276700,  330409,  386886,
              443531,  499622,  555539,  612524,  670886,  727231,  783691,
              895696, 1179310, 1237374, 1295031, 1353247, 1413172, 1475050,
             1535867],
            dtype=&#39;int64&#39;),
 644: Int64Index([   8969,   63929,  118813,  173832,  228945,  284742,  338949,
              395347,  451932,  507864,  564064,  621308,  679241,  735723,
              792137,  848365,  904063,  960633, 1017270, 1074783, 1131167,
             1188090, 1246171, 1303753, 1362256, 1422345, 1484203, 1545676],
            dtype=&#39;int64&#39;),
 648: Int64Index([   1435,  111479,  225207,  337419,  500532,  681044,  737557,
              877973,  896614,  957084, 1067339, 1123646, 1188515, 1246574,
             1311547, 1379342, 1448845, 1512717, 1570973],
            dtype=&#39;int64&#39;),
 652: Int64Index([  26090,   80801,  135726,  190625,  246157,  301491,  356412,
              412738,  468878,  524704,  581352,  638936,  696369,  753049,
              809281,  865301,  920993,  977603, 1034606, 1091966, 1148233,
             1205868, 1263645, 1321264, 1380190, 1441060, 1502679, 1565614],
            dtype=&#39;int64&#39;),
 656: Int64Index([  24890,   79657,  134586,  189514,  244986,  300343,  355254,
              411546,  467709,  523553,  580194,  637737,  695174,  751875,
              808096,  864149,  919790,  976415, 1033366, 1147062, 1204718,
             1262485, 1320108, 1378995, 1439825, 1501448, 1564252],
            dtype=&#39;int64&#39;),
 661: Int64Index([  11454,   66375,  121328,  176271,  231424,  287148,  341467,
              397869,  454388,  510279,  566574,  623814,  681723,  738250,
              794646,  850828,  906536,  963086, 1019812, 1077283, 1133625,
             1190669, 1248696, 1306275, 1364914, 1425174, 1486929, 1548567],
            dtype=&#39;int64&#39;),
 663: Int64Index([   5577,   60608,  115460,  170447,  281433,  335467,  391927,
              448460,  504495,  560665,  617768,  675823,  732329,  788739,
              844933,  900678,  957363, 1013816, 1071360, 1127695, 1184507,
             1242615, 1358615, 1418595, 1480505, 1541609],
            dtype=&#39;int64&#39;),
 665: Int64Index([  18044,   72938,  127937,  182793,  238175,  293736,  348383,
              404546,  460996,  516829,  573269,  630725,  688340,  744949,
              801190,  857371,  913018,  969597, 1026432, 1083923, 1140282,
             1197550, 1255488, 1313140, 1371752, 1432388, 1494083, 1556301],
            dtype=&#39;int64&#39;),
 667: Int64Index([  28455,   83061,  138004,  192896,  248435,  303732,  358761,
              415189,  471231,  527002,  583693,  641337,  698694,  755365,
              811631,  867617,  923227,  979853, 1036904, 1094343, 1150602,
             1208292, 1266050, 1323679, 1382711, 1443619, 1505163, 1568265],
            dtype=&#39;int64&#39;),
 668: Int64Index([  16678,   71553,  126552,  181460,  236766,  292350,  346929,
              403158,  459605,  515457,  571821,  629264,  686898,  743510,
              799812,  855980,  911616,  968186, 1025055, 1082505, 1138854,
             1196026, 1254071, 1311617, 1370253, 1430840, 1492576, 1554688],
            dtype=&#39;int64&#39;),
 674: Int64Index([  40240,   94408,  149232,  203983,  259687,  314727,  370412,
              426872,  482594,  538448,  595226,  653246,  710113,  766967,
              823263,  879039,  934740,  991125, 1045411, 1102863, 1159005,
             1217060, 1274744, 1332218, 1394726, 1452991, 1514411, 1578160],
            dtype=&#39;int64&#39;),
 677: Int64Index([  52422,  161673,  216489,  272441,  327194,  383331,  439973,
              495711,  551532,  608506,  666845,  723949,  836398,  891952,
              948346, 1004748, 1062310, 1119253, 1175548, 1233575, 1290978,
             1348894, 1408585, 1532161, 1598504],
            dtype=&#39;int64&#39;),
 678: Int64Index([  17959,   72859,  127853,  182710,  238093,  293657,  348297,
              404458,  460909,  516748,  573188,  630644,  688263,  744859,
              801106,  857290,  912926,  969519, 1026354, 1083841, 1140201,
             1197465, 1255404, 1313063, 1371676, 1432318, 1494006, 1556220],
            dtype=&#39;int64&#39;),
 687: Int64Index([  16935,   71802,  126820,  181720,  237040,  292602,  347191,
              403404,  459864,  515711,  572083,  629517,  687158,  743766,
              800066,  856234,  911873,  968450, 1025310, 1082769, 1139107,
             1196273, 1254333, 1311879, 1370500, 1431109, 1492843, 1554975],
            dtype=&#39;int64&#39;),
 689: Int64Index([ 197375,  252957,  531667,  588396,  646237,  703328,  760099,
              816254,  872138,  927790,  984486, 1041661, 1099033, 1155226,
             1213115, 1270844, 1328350, 1387559, 1448813, 1510155, 1573676],
            dtype=&#39;int64&#39;),
 691: Int64Index([  46292,  100438,  155206,  210038,  265853,  376743,  433276,
              488799,  544653,  601654,  659694,  716692,  773219,  829523,
              885106,  940946,  997436, 1054839, 1111892, 1168279, 1226328,
             1283861, 1341496, 1401071, 1463021, 1524282, 1589619],
            dtype=&#39;int64&#39;),
 695: Int64Index([  18965,   73837,  128847,  183658,  239053,  294591,  349279,
              405438,  461859,  517730,  574148,  631623,  689247,  745829,
              802076,  858248,  913910,  970490, 1027320, 1084817, 1141186,
             1198473, 1256394, 1314062, 1372725, 1433334, 1495031, 1557353],
            dtype=&#39;int64&#39;),
 696: Int64Index([   8823,   63791,  118686,  173675,  228797,  338803,  395206,
              451787,  507714,  563925,  621153,  679093,  735566,  791995,
              848223,  903926,  960485, 1017119, 1074635, 1131009, 1187937,
             1246015, 1303605, 1362088, 1422179, 1484055, 1545503],
            dtype=&#39;int64&#39;),
 697: Int64Index([   5315,   60357,  115219,  170195,  225228,  281200,  335211,
              391677,  448212,  504257,  560407,  617512,  675562,  732068,
              788472,  844669,  900419,  957104, 1013546, 1071099, 1127437,
             1184252, 1242330, 1358325, 1418313, 1480229, 1541324],
            dtype=&#39;int64&#39;),
 698: Int64Index([  33180,   87530,  142424,  197366,  252945,  308141,  363431,
              419940,  475809,  531659,  588383,  646222,  703312,  760082,
              816239,  872122,  927781,  984464, 1041644, 1099021, 1155215,
             1213105, 1270834, 1328334, 1387548, 1448801, 1510143, 1573664],
            dtype=&#39;int64&#39;),
 699: Int64Index([  19814,   74670,  129693,  184498,  239925,  295431,  350168,
              406304,  462733,  518555,  575048,  632501,  690091,  746702,
              802966,  859125,  914781,  971322, 1028178, 1085693, 1142051,
             1199369, 1257306, 1314967, 1373660, 1434307, 1495999, 1558395],
            dtype=&#39;int64&#39;),
 701: Int64Index([  17314,   73689,  128700,  183527,  238900,  294464,  349120,
              405274,  461699,  517577,  574000,  631476,  689106,  745684,
              801938,  858105,  913766,  970328, 1027166, 1084653, 1141012,
             1198312, 1256244, 1313892, 1372572, 1433188, 1494875, 1557178],
            dtype=&#39;int64&#39;),
 705: Int64Index([  44492,  153397,  208227,  264009,  318910,  374829,  431242,
              486807,  542633,  599531,  657611,  714540,  771252,  827514,
              883185,  938942,  995364, 1052773, 1110110, 1166359, 1224665,
             1282191, 1339660, 1399221, 1460984, 1522236, 1587024],
            dtype=&#39;int64&#39;),
 710: Int64Index([  17749,   72660,  127647,  182525,  237899,  293447,  348089,
              404240,  460699,  516544,  572973,  630427,  688059,  744650,
              800902,  857101,  912719,  969315, 1026151, 1083632, 1140002,
             1197251, 1255188, 1312846, 1371451, 1432096, 1493797, 1555992],
            dtype=&#39;int64&#39;),
 711: Int64Index([  21242,   76084,  131077,  185935,  241388,  296805,  351630,
              407780,  464071,  519932,  576480,  634010,  691515,  748160,
              804431,  860585,  916166,  972788, 1029693, 1087126, 1143512,
             1200925, 1258776, 1316450, 1375163, 1435946, 1497595, 1560086],
            dtype=&#39;int64&#39;),
 712: Int64Index([  52066,  106427,  161264,  216075,  271998,  318730,  382902,
              431075,  495268,  551081,  608060,  666385,  723489,  779858,
              835968,  891512,  947842, 1004257, 1061805, 1118735, 1175030,
             1233033, 1290469, 1348365, 1408051, 1470253, 1531619, 1597913],
            dtype=&#39;int64&#39;),
 714: Int64Index([  13298,   68220,  123174,  178151,  233343,  289012,  343443,
              399748,  456285,  512187,  568498,  625765,  683597,  740172,
              796512,  852690,  908341,  964944, 1021754, 1079172, 1135501,
             1192590, 1250572, 1308165, 1366883, 1427223, 1488970, 1550765],
            dtype=&#39;int64&#39;),
 722: Int64Index([    326,   55514,  110432,  165531,  220390,  276545,  330240,
              386711,  443365,  499446,  555378,  612339,  670728,  727063,
              783521,  839760,  895519,  952303, 1008687, 1066224, 1122507,
             1179117, 1237174, 1294853, 1353064, 1412995, 1474863, 1535684],
            dtype=&#39;int64&#39;),
 729: Int64Index([  14270,   69210,  124192,  179140,  234381,  290007,  344459,
              400769,  457280,  513131,  569518,  626796,  741150,  797508,
              853692,  909335, 1022755, 1080149, 1136493, 1193631, 1251601,
             1309165, 1367933, 1428312, 1490072, 1551905],
            dtype=&#39;int64&#39;),
 730: Int64Index([  15757,   70666,  125636,  180524,  235812,  291431,  345971,
              402232,  458720,  514566,  570940,  628304,  685997,  742587,
              798922,  855100,  910736,  967328, 1024170, 1081608, 1137973,
             1195121, 1253116, 1310716, 1369338, 1429866, 1491597, 1553636],
            dtype=&#39;int64&#39;),
 731: Int64Index([   8478,   63467,  118348,  173337,  228457,  284295,  338451,
              394872,  451487,  507409,  563611,  620834,  678793,  735261,
              791671,  847912,  903607,  960172, 1016791, 1074309, 1130708,
             1187574, 1245668, 1303275, 1361735, 1421824, 1483718, 1545107],
            dtype=&#39;int64&#39;),
 735: Int64Index([    163,   55344,  110301,  165403,  220228,  276405,  330071,
              386569,  443223,  499304,  555236,  612196,  670599,  726929,
              783392,  839632,  895356,  952162, 1008538, 1066071, 1122362,
             1178949, 1237016, 1294691, 1352909, 1412825, 1474693, 1535484],
            dtype=&#39;int64&#39;),
 736: Int64Index([   6881,   61913,  116768,  171768,  282727,  336860,  393235,
              449826,  505831,  561998,  619175,  677164,  733643,  790028,
              846297,  902008,  958656, 1015191, 1072693, 1129095, 1185908,
             1243981, 1301548, 1359960, 1420037, 1543152],
            dtype=&#39;int64&#39;),
 737: Int64Index([  32679,   87066,  141984,  196921,  252459,  307698,  362937,
              419418,  475319,  531176,  587891,  645705,  702831,  759575,
              815758,  871635,  927340,  984020, 1041189, 1098520, 1154754,
             1212624, 1270345, 1327855, 1387069, 1448283, 1509624, 1573060],
            dtype=&#39;int64&#39;),
 744: Int64Index([1290146, 1348031, 1469895, 1531268, 1597504], dtype=&#39;int64&#39;),
 745: Int64Index([  15179,   70080,  125063,  180008,  235267,  290872,  345389,
              401631,  458129,  570426,  627721,  685421,  742035,  798362,
              854528,  910186, 1023607, 1081022, 1137378, 1194536, 1252538,
             1310104, 1368808, 1429266, 1491008, 1552949],
            dtype=&#39;int64&#39;),
 748: Int64Index([  12847,   67774,  122750,  177704,  232907,  288593,  342993,
              399311,  455834,  511737,  568040,  625306,  683161,  739730,
              796054,  852273,  907917,  964500, 1021297, 1078715, 1135078,
             1192141, 1250120, 1307713, 1366430, 1426738, 1488464, 1550259],
            dtype=&#39;int64&#39;),
 753: Int64Index([   9692,   64639,  119511,  174527,  229646,  285422,  339673,
              396089,  452624,  508540,  564763,  622024,  679929,  736438,
              792891,  849048,  904766,  961341, 1017988, 1075516, 1131879,
             1188873, 1246929, 1304447, 1363031, 1423139, 1484990, 1546487],
            dtype=&#39;int64&#39;),
 758: Int64Index([  37398,   91728,  146541,  367600,  424109,  479895,  535679,
              592472,  650469,  707403,  764246,  876335,  931985,  988484,
             1045727, 1103195, 1159322, 1217389, 1275059, 1332536, 1391880,
             1453323, 1514747, 1578550],
            dtype=&#39;int64&#39;),
 760: Int64Index([1588259], dtype=&#39;int64&#39;),
 762: Int64Index([  34614,   88947,  143773,  198661,  254284,  309467,  364779,
              421312,  477231,  533037,  589787,  647654,  704699,  761515,
              817734,  873532,  929207,  985784, 1042972, 1100403, 1156567,
             1214533, 1272280, 1329758, 1389052, 1450326, 1511638, 1575246],
            dtype=&#39;int64&#39;),
 765: Int64Index([845166, 957567, 1014023, 1071583, 1184727, 1242829, 1418808,
             1541837],
            dtype=&#39;int64&#39;),
 766: Int64Index([1520639, 1548882], dtype=&#39;int64&#39;),
 768: Int64Index([  32955,   87323,  142224,  197183,  252745,  307943,  363220,
              419716,  475590,  531452,  588155,  646013,  703114,  759868,
              816030,  871900,  927575,  984283, 1041460, 1098799, 1155020,
             1212896, 1270621, 1328125, 1387345, 1448581, 1509922, 1573401],
            dtype=&#39;int64&#39;),
 775: Int64Index([   9842,   64797,  119665,  174682,  229789,  285567,  339819,
              396249,  452780,  622187,  680093,  736592,  793037,  849203,
              904917,  961488, 1247083, 1304603, 1363201, 1423321, 1485169,
             1546665],
            dtype=&#39;int64&#39;),
 777: Int64Index([  42830,   96908,  151740,  206582,  262343,  373134,  485208,
              541042,  597903,  655959,  712916,  769588,  881674,  937357,
              993769, 1051163, 1223030, 1459191, 1520538, 1584695],
            dtype=&#39;int64&#39;),
 778: Int64Index([  31117,   85557,  140551,  195397,  250958,  306239,  361365,
              417879,  473808,  529608,  586391,  644070,  701311,  758026,
              814209,  870173,  925828,  982499, 1039642, 1097000, 1153253,
             1211033, 1268809, 1326364, 1385460, 1446548, 1507992, 1571276],
            dtype=&#39;int64&#39;),
 783: Int64Index([  27643,   82278,  137232,  192125,  247629,  302965,  357981,
              414373,  470452,  526242,  582896,  640545,  697908,  754577,
              810860,  866813,  922477,  979072, 1036129, 1093550, 1149832,
             1207442, 1265201, 1322824, 1381849, 1442729, 1504270, 1567341],
            dtype=&#39;int64&#39;),
 784: Int64Index([  44775,   98831,  153666,  208507,  264291,  319191,  375092,
              431498,  487086,  542926,  599820,  657900,  714848,  771547,
              827810,  883438,  939206,  995633, 1053059, 1110331, 1166589,
             1224874, 1282428, 1339916, 1399499, 1461284, 1522546, 1587328],
            dtype=&#39;int64&#39;),
 785: Int64Index([   8232,   63239,  118116,  173093,  228204,  284041,  338214,
              394619,  451224,  507162,  563357,  620582,  678539,  735011,
              791433,  847672, 1016539, 1074063, 1130475, 1187322, 1245412,
             1302997, 1361433, 1421528, 1483444, 1544796],
            dtype=&#39;int64&#39;),
 787: Int64Index([  42387,   96507,  151339,  206170,  261899,  316841,  372700,
              429168,  484791,  540637,  597441,  655527,  712522,  769171,
              825497,  881249,  936920,  993354, 1050734, 1108079, 1164255,
             1222589, 1280171, 1337537, 1397070, 1458707, 1520072, 1584190],
            dtype=&#39;int64&#39;),
 792: Int64Index([   2785,   57882,  112766,  167890,  222714,  278809,  332689,
              389187,  445803,  501827,  557955,  614976,  673188,  729561,
              786013,  842199,  897947,  954705, 1011085, 1068677, 1124980,
             1181637, 1239765, 1297370, 1355612, 1415584, 1477520, 1538427],
            dtype=&#39;int64&#39;),
 794: Int64Index([  33475,   87788,  142677,  197611,  253226,  308410,  363699,
              420197,  476083,  531918,  588643,  646485,  703571,  760357,
              816517,  872396,  928041,  984727, 1041882, 1099282, 1155484,
             1213356, 1271104, 1328608, 1387816, 1449086, 1510430, 1573965],
            dtype=&#39;int64&#39;),
 795: Int64Index([  38398,   92684,  147496,  202236,  257964,  313052,  368574,
              425061,  480836,  536626,  593432,  651414,  708337,  765190,
              821513,  877302,  932997,  989440, 1046717, 1104151, 1160302,
             1218381, 1276048, 1333487, 1392871, 1454331, 1515792, 1579637],
            dtype=&#39;int64&#39;),
 797: Int64Index([  27919,   82551,  137494,  192394,  247894,  303225,  358238,
              414666,  470726,  502028,  583176,  615168,  698170,  754855,
              811107,  867070,  922724,  979340, 1011287, 1093811, 1150087,
             1207713, 1239970, 1323110, 1355834, 1443034, 1504587, 1567661],
            dtype=&#39;int64&#39;),
 799: Int64Index([  30853,   85313,  140271,  195150,  250712,  305982,  361131,
              417614,  473550,  529336,  586139,  643813,  701061,  757763,
              813954,  869913,  925568,  982244, 1039393, 1096724, 1152988,
             1210759, 1268511, 1326077, 1385193, 1446267, 1507695, 1570978],
            dtype=&#39;int64&#39;),
 800: Int64Index([  32102,   86503,  141474,  196337,  251879,  307146,  362334,
              418835,  474728,  530596,  587334,  645102,  702274,  758989,
              815190,  865292,  920985,  983457, 1040603, 1097953, 1154213,
             1212042, 1269786, 1327311, 1386464, 1447614, 1509025, 1572393],
            dtype=&#39;int64&#39;),
 804: Int64Index([  97009,  151825,  206661,  262442,  317358,  373238,  485297,
              541131,  598001,  656063,  713009,  769676,  826021,  881748,
              937455,  993851, 1051242, 1108572, 1164768, 1223131, 1338039,
             1397601, 1459303, 1520645, 1584808],
            dtype=&#39;int64&#39;),
 805: Int64Index([  32863,   87234,  142137,  197097,  252647,  307859,  363123,
              419613,  475501,  531373,  588073,  645909,  703020,  759767,
              815933,  876083,  931728,  988227, 1045479, 1102939, 1159067,
             1217129, 1274807, 1332285, 1391634, 1453054, 1514479, 1578228],
            dtype=&#39;int64&#39;),
 811: Int64Index([   3068,   58140,  113028,  168125,  222962,  279054,  332960,
              389461,  446054,  502080,  558226,  615224,  673432,  729817,
              786261,  842483,  898219,  954954, 1011348, 1068943, 1125259,
             1181906, 1240037, 1297631, 1355895, 1415858, 1477828, 1538748],
            dtype=&#39;int64&#39;),
 812: Int64Index([  32034,   86445,  141409,  196272,  251826,  307086,  362272,
              418787,  474671,  530541,  587273,  645040,  702224,  758933,
              815130,  871047,  926722,  983397, 1040550, 1097899, 1154149,
             1211978, 1269715, 1327253, 1386407, 1447546, 1508958, 1572326],
            dtype=&#39;int64&#39;),
 813: Int64Index([ 548872,  605829,  664033,  721144,  777455,  833595,  889121,
              945388, 1001868, 1059252, 1116224, 1172465, 1230364, 1245547,
             1345784, 1405418, 1467497, 1528776, 1594859],
            dtype=&#39;int64&#39;),
 817: Int64Index([  17835,   72731,  127726,  182599,  237967,  293528,  348160,
              404327,  460774,  516627,  573057,  630504,  688137,  744733,
              800978,  857169,  912796,  969383, 1026228, 1083712, 1140084,
             1197336, 1255271, 1312925, 1371533, 1432178, 1493875, 1556082],
            dtype=&#39;int64&#39;),
 819: Int64Index([  19111,   74012,  129013,  183821,  239207,  294738,  349452,
              405604,  462023,  517888,  574320,  631802,  689411,  745993,
              802244,  858404,  914083,  970644, 1027484, 1084981, 1141351,
             1198640, 1256561, 1314237, 1372906, 1433510, 1495218, 1557543],
            dtype=&#39;int64&#39;),
 820: Int64Index([  26397,  136030,  190923,  246444,  301777,  356744,  413089,
              469192,  525017,  581654,  639254,  696681,  753351,  809588,
              865616,  921282,  977919, 1034939, 1092276, 1148576, 1206197,
             1263957, 1321587, 1380537, 1441419, 1503006, 1565953],
            dtype=&#39;int64&#39;),
 826: Int64Index([  51688,  106045,  271539,  326349,  382393,  439078,  494753,
              550577,  607558,  665864,  722967,  779299,  835430,  890974,
              947275, 1061242, 1118160, 1174430, 1232413, 1289873, 1347738,
             1407445, 1469606, 1530991, 1597193],
            dtype=&#39;int64&#39;),
 833: Int64Index([  47807,  101964,  156714,  211551,  267364,  322193,  378175,
              434720,  490287,  546137,  603142,  661243,  718352,  774805,
              830961,  886564,  942460,  998947, 1056363, 1113487, 1169837,
             1227737, 1285304, 1342989, 1402608, 1464555, 1525865, 1591625],
            dtype=&#39;int64&#39;),
 839: Int64Index([   1221,   56354,  111271,  166381,  221191,  277351,  331130,
              387626,  444233,  500297,  556313,  613288,  671619,  727935,
              784403,  840636,  896392,  953189, 1009565, 1067116, 1123422,
             1180028, 1238092, 1295767, 1353984, 1413918, 1475824, 1536649],
            dtype=&#39;int64&#39;),
 848: Int64Index([  42447,   96560,  151394,  206229,  261959,  316896,  372761,
              429232,  484846,  540701,  597496,  655586,  712584,  769232,
              825564,  881313,  936982,  993414, 1050801, 1108140, 1164316,
             1222655, 1280236, 1337602, 1397136, 1458765, 1520131, 1584248],
            dtype=&#39;int64&#39;),
 849: Int64Index([  10677,   65584,  120504,  175469,  230643,  286369,  340648,
              397064,  453584,  509469,  565766,  622990,  680895,  737418,
              793826,  850030,  905711, 1076478, 1132842, 1189874, 1247897,
             1305456, 1364086, 1424303, 1486062, 1547650],
            dtype=&#39;int64&#39;),
 850: Int64Index([  48501,  102694,  157442,  212269,  268099,  322890,  378854,
              435408,  490945,  546790,  603831,  661933,  719075,  775464,
              831617,  887197,  943177,  999656, 1057071, 1114141, 1287316,
             1343640, 1404777, 1465298, 1526618, 1592437],
            dtype=&#39;int64&#39;),
 856: Int64Index([  28706,   71756,  126776,  193125,  248674,  292557,  359008,
              415437,  471457,  527230,  583921,  641572,  698942,  743719,
              811887,  867866,  923467,  980056, 1025264, 1094605, 1150837,
             1208558, 1266299, 1323917, 1382950, 1443884, 1505432, 1568537],
            dtype=&#39;int64&#39;),
 858: Int64Index([ 166892,  221725,  277886,  331656,  388184,  444752,  500828,
              556873,  613878,  672184,  728502,  784960,  841180,  896920,
              953732, 1010095, 1067662, 1123956, 1180595, 1238675, 1296316,
             1354537, 1414516, 1476404, 1537274],
            dtype=&#39;int64&#39;),
 862: Int64Index([1587971], dtype=&#39;int64&#39;),
 868: Int64Index([   8881,   63845,  173737,  228855,  284656,  338857,  395262,
              451843,  507775,  563981,  621203,  679145,  735628,  792053,
              848282,  903978, 1017174, 1074691, 1131069, 1246075, 1303662,
             1362152, 1422241, 1545568],
            dtype=&#39;int64&#39;),
 875: Int64Index([  20444,   75303,  130317,  185133,  240548,  296020,  350827,
              406932,  463332,  519171,  575667,  633136,  690727,  747360,
              803580,  859746,  915378,  971969, 1028839, 1086339, 1142691,
             1200029, 1257952, 1315617, 1374323, 1434991, 1496714, 1559119],
            dtype=&#39;int64&#39;),
 878: Int64Index([  52597,  161865,  216697,  272659,  383553,  440208,  495947,
              551751,  608732,  667070,  724184,  780550,  836603,  892163,
              948595, 1004992, 1062568, 1175801, 1233845, 1291241, 1349146,
             1408857, 1471058, 1598788],
            dtype=&#39;int64&#39;),
 880: Int64Index([  23421,   78175,  133163,  188070,  243543,  298920,  353784,
              410001,  466196,  522040,  578694,  636234,  693722,  750387,
              806612,  862727,  918292,  974937, 1031874, 1089285, 1145588,
             1203170, 1260964, 1318591, 1377401, 1438243, 1499860, 1562539],
            dtype=&#39;int64&#39;),
 881: Int64Index([   8188,   63200,  118072,  173049,  223937,  283998,  333968,
              394573,  451177,  507129,  563306,  620534,  678489,  734957,
              791385,  847620,  903314,  959897, 1016494, 1074007, 1126279,
             1187270, 1245362, 1302951, 1361399, 1421479, 1483389, 1544746],
            dtype=&#39;int64&#39;),
 882: Int64Index([  52608,  161876,  216708,  272670,  383564,  440219,  495958,
              551762,  608743,  667081,  724195,  780561,  836614,  892174,
              948606, 1005003, 1062579, 1175812, 1233856, 1291252, 1349157,
             1408868, 1471069, 1598800],
            dtype=&#39;int64&#39;),
 883: Int64Index([  11501,   66410,  121375,  176317,  231472,  287198,  341518,
              397916,  454444,  510330,  566623,  623869,  681770,  738297,
              794683,  850874,  906583,  963130, 1019863, 1077329, 1133669,
             1190711, 1248742, 1306320, 1364969, 1425228, 1486973, 1548615],
            dtype=&#39;int64&#39;),
 899: Int64Index([  33008,   87363,  142264,  197220,  252796,  307990,  363265,
              419758,  475634,  531489,  588192,  646052,  703155,  759918,
              816077,  871944,  927619,  984313, 1041487, 1098838, 1155059,
             1212932, 1270667, 1328166, 1387389, 1448621, 1509970, 1573444],
            dtype=&#39;int64&#39;),
 900: Int64Index([  10276,   65187,  120088,  175074,  230206,  340252,  396648,
              680483,  737000,  793436,  849602,  905297,  961876, 1018555,
             1076048, 1132425, 1189460, 1247498, 1305014, 1363624, 1423803,
             1485613, 1547146],
            dtype=&#39;int64&#39;),
 906: Int64Index([   2712,   57801,  112689,  167811,  222651,  278741,  332621,
              389122,  445726,  501754,  557877,  614900,  673117,  729480,
              785936,  842119,  897872, 1011029, 1124895, 1181549, 1239694,
             1297291, 1355545, 1415511, 1477428, 1538355],
            dtype=&#39;int64&#39;),
 908: Int64Index([  23851,   78583,  133581,  188456,  243949,  299335,  354197,
              410439,  466602,  522466,  579095,  636643,  694108,  750795,
              807022,  863132,  918717,  975345, 1032278, 1089705, 1145995,
             1203599, 1261379, 1319029, 1377823, 1438663, 1500299, 1563005],
            dtype=&#39;int64&#39;),
 912: Int64Index([   9457,   64412,  119289,  174307,  229429,  285206,  339453,
              395868,  452406,  508334,  564544,  621809,  679719,  736225,
              792666,  848826,  904546,  961130, 1017776, 1075292, 1131675,
             1188636, 1246701, 1304221, 1362797, 1422906, 1484748, 1546229],
            dtype=&#39;int64&#39;),
 924: Int64Index([   9635,   64585,  119456,  174466,  229590,  285364,  339619,
              396034,  474140,  529979,  586730,  644442,  701649,  758389,
              814574,  870505,  926161,  982849, 1039988, 1097340, 1153615,
             1211378, 1269149, 1326691, 1385822, 1446925, 1508359, 1571665],
            dtype=&#39;int64&#39;),
 929: Int64Index([   2774,   57868,  112745,  167872,  222699,  278795,  332676,
              389178,  445790,  501816,  557938,  614962,  673177,  729550,
              786000,  842188,  897937,  954696, 1011075, 1068663, 1124968,
             1181623, 1239753, 1297354, 1355598, 1415572, 1477508, 1538412],
            dtype=&#39;int64&#39;),
 932: Int64Index([ 439379,  550895,  607868,  666193,  723288,  779636,  835768,
              891304,  947633, 1004047, 1061593, 1118524, 1174806, 1232792,
             1290243, 1348134, 1469997, 1531375, 1597635],
            dtype=&#39;int64&#39;),
 935: Int64Index([  23867,   78600,  133602,  188475,  243964,  299351,  354218,
              410461,  466618,  522488,  579112,  636664,  694126,  750819,
              807040,  863146,  918732,  975359, 1032292, 1089722, 1146015,
             1261401, 1319047, 1377844, 1438682, 1563029],
            dtype=&#39;int64&#39;),
 941: Int64Index([  47613,  101775,  156546,  211386,  270901,  325704,  381705,
              438408,  490131,  549864,  606853,  665143,  722210,  778535,
              834681,  890211,  946521, 1002957, 1117387, 1173625, 1231597,
             1289076, 1346925, 1406602, 1468713, 1530105, 1596249],
            dtype=&#39;int64&#39;),
 944: Int64Index([  26554,   81253,  136169,  191069,  246580,  301918,  356888,
              413226,  469337,  525167,  639417,  696833,  753482,  809722,
              865747,  921411,  978060, 1035080, 1092430, 1148729, 1206339,
             1264086, 1321736, 1380682, 1441560, 1566105],
            dtype=&#39;int64&#39;),
 945: Int64Index([  31952,   86361,  141322,  196181,  251735,  306987,  362181,
              418689,  474563,  530444,  587183,  644934,  702133,  758840,
              815044,  870950,  926621, 1097816, 1154049, 1211891, 1269628,
             1327169, 1386329, 1447449, 1508858, 1572223],
            dtype=&#39;int64&#39;),
 951: Int64Index([  67102,  122089,  177042,  232222,  287929,  342308,  398644,
              455146,  511046,  567341,  624630,  682498,  739010,  795402,
              851590,  907263, 1020615, 1134385, 1191431, 1249447, 1365731,
             1426001, 1487743, 1549483],
            dtype=&#39;int64&#39;),
 955: Int64Index([  47890,  102043,  161167,  215980,  271893,  326689,  382798,
              439460,  495162,  550978,  607961,  666282,  723382,  779736,
              835865,  891403,  947732, 1004150, 1056451, 1118624, 1174909,
             1232905, 1290347, 1343070, 1407934, 1470117, 1531496, 1597773],
            dtype=&#39;int64&#39;),
 956: Int64Index([  29184,   83764,  138732,  193626,  249183,  304413,  359500,
              415913,  471965,  527739,  642111,  699460,  756111,  812375,
              868327,  923976,  980581, 1037671, 1095112, 1151303, 1209073,
             1266833, 1321160, 1383485, 1444439, 1505956, 1569097],
            dtype=&#39;int64&#39;),
 957: Int64Index([  51769,  106133,  160951,  168512,  223376,  326440,  382504,
              439181,  494869,  550691,  604546,  665980,  673832,  779408,
              835550,  891081,  947388, 1003821, 1061345, 1118270, 1174543,
             1232539, 1290002, 1347875, 1407565, 1469726, 1531104, 1597322],
            dtype=&#39;int64&#39;),
 964: Int64Index([  16616,   71491,  126489,  181392,  236695,  292276,  346850,
              403087,  459539,  515379,  571747,  629183,  686829,  743428,
              799732,  855915,  911544,  968101, 1024978, 1082421, 1138776,
             1195944, 1253989, 1311539, 1370166, 1430763, 1488173, 1549942],
            dtype=&#39;int64&#39;),
 967: Int64Index([  52903,  107336,  162214,  217106,  273088,  327821,  383973,
              440639,  496390,  552215,  609151,  667490,  724601,  780975,
              837019,  892569,  949013, 1005402, 1062972, 1119917, 1176252,
             1234315, 1291717, 1349617, 1409346, 1471502, 1532874, 1599292],
            dtype=&#39;int64&#39;),
 968: Int64Index([  40341,   94492,  149322,  204087,  259779,  314816,  370506,
              426988,  538555,  595334,  653351,  710211,  767063,  823357,
              879149,  934825,  991232, 1048614, 1105981, 1162135, 1220345,
             1277936, 1335355, 1394826, 1456336, 1517773, 1581773],
            dtype=&#39;int64&#39;),
 969: Int64Index([  84975,  139925,  194810,  250366,  305596,  360764,  417206,
              473198,  585722,  643413,  757349,  813553,  869510,  925172,
              981833, 1038994, 1096327, 1152582, 1210351, 1268088, 1384787,
             1445848, 1507300, 1570524],
            dtype=&#39;int64&#39;),
 973: Int64Index([  18907,   73775,  128790,  183607,  238995,  294547,  349225,
              461809,  517663,  574088,  631572,  689194,  745775,  802022,
              858188,  913864,  970434, 1027270, 1084756, 1141128, 1198419,
             1256342, 1314003, 1372669, 1433283, 1494978, 1557286],
            dtype=&#39;int64&#39;),
 981: Int64Index([  17915,   72815,  127802,  182672,  238045,  293609,  348250,
              404416,  460859,  516705,  573143,  630590,  688215,  744812,
              801058,  857243,  912876,  969474, 1026307, 1083797, 1140159,
             1197421, 1255360, 1313013, 1371624, 1432265, 1493960, 1556172],
            dtype=&#39;int64&#39;),
 983: Int64Index([1586891], dtype=&#39;int64&#39;),
 984: Int64Index([ 946027, 1002505, 1059953, 1116907, 1173104, 1231071, 1288589,
             1346436, 1406102, 1468190, 1529525, 1595628],
            dtype=&#39;int64&#39;),
 988: Int64Index([ 428679,  484318,  540156,  596977,  655056,  711819,  768706,
              824995,  880746,  936442,  992892, 1050272, 1107569, 1163737,
             1222097, 1279600, 1337035, 1396562, 1458174, 1519565, 1583660],
            dtype=&#39;int64&#39;),
 989: Int64Index([   3098,   58170,  113054,  168151,  222986,  279080,  332987,
              389490,  446078,  502107,  558256,  615249,  673451,  729842,
              786281,  842510,  898249,  954981, 1011378, 1068967, 1125285,
             1240059, 1297659, 1355916, 1415887, 1477861, 1538778],
            dtype=&#39;int64&#39;),
 992: Int64Index([  25396,   80145,  135038,  189958,  245461,  300801,  355712,
              412033,  468178,  524010,  580668,  638237,  695656,  752347,
              808583,  864617,  920285,  976908, 1033902, 1091259, 1147536,
             1205198, 1262979, 1320586, 1379499, 1440326, 1501949, 1564807],
            dtype=&#39;int64&#39;),
 998: Int64Index([277312, 613240, 727893, 840589, 1179987, 1413878, 1536588], dtype=&#39;int64&#39;),
 1001: Int64Index([  22348,   77129,  132128,  187004,  242475,  297850,  352727,
              408901,  465196,  521018,  577589,  635137,  692654,  749294,
              805554,  861682,  917254,  973909, 1030810, 1088244, 1144574,
             1202088, 1259887, 1317549, 1376317, 1437137, 1498725, 1561332],
            dtype=&#39;int64&#39;),
 1005: Int64Index([  13351,   68277,  123241,  178212,  233397,  289066,  343503,
              399811,  456350,  512239,  568562,  625821,  683652,  740232,
              796565,  852745,  908395,  964997, 1021821, 1079223, 1135553,
             1192657, 1250626, 1308217, 1366936, 1427271, 1489040, 1550821],
            dtype=&#39;int64&#39;),
 1007: Int64Index([  43863,  152720,  430627,  486169,  541967,  598891,  656933,
              713875,  770577,  826909,  882575,  938285,  994689, 1052093,
             1109475, 1165674, 1224001, 1281584, 1338940, 1398543, 1460262,
             1521549, 1585852],
            dtype=&#39;int64&#39;),
 1015: Int64Index([  27828,   82457,  137418,  192311,  247804,  303135,  358157,
              414585,  470649,  526417,  583077,  640729,  698076,  754763,
              811022,  866987,  922648,  979257, 1036303, 1093725, 1150007,
             1207624, 1265384, 1323017, 1382053, 1442935, 1504484, 1567560],
            dtype=&#39;int64&#39;),
 1017: Int64Index([  31100,   85542,  140538,  195389,  250946,  306229,  361357,
              417868,  473800,  529596,  586381,  644057,  701296,  758005,
              814189,  870155,  925808,  982484, 1039635, 1096982, 1153230,
             1211019, 1268789, 1326346, 1385443, 1446531, 1507978, 1571259],
            dtype=&#39;int64&#39;),
 1021: Int64Index([  43491,   97518,  152345,  207158,  262947,  317862,  373752,
              430224,  485782,  541587,  598502,  656546,  713480,  770151,
              826507,  882192,  937902,  994293, 1051692, 1109056, 1165274,
             1223578, 1281161, 1338532, 1398103, 1459820, 1521147, 1585387],
            dtype=&#39;int64&#39;),
 1022: Int64Index([  51784,  106147,  160965,  215765,  271646,  326456,  382521,
              439196,  494887,  550704,  607683,  665997,  723078,  779425,
              835565,  891097,  947407, 1003840, 1061364, 1118288, 1174561,
             1232558, 1290020, 1347895, 1469742, 1531123, 1597344],
            dtype=&#39;int64&#39;),
 1023: Int64Index([   9841,   64796,  119664,  174681,  229787,  285565,  339818,
              396247,  452779,  508694,  564926,  622186,  680092,  736591,
              793036,  849202,  904916,  961487, 1018140, 1075661, 1132019,
             1189032, 1247082, 1304602, 1363200, 1423320, 1485168, 1546664],
            dtype=&#39;int64&#39;),
 1026: Int64Index([ 891606,  947958, 1004363, 1061907, 1099290, 1175134, 1233151,
             1290577, 1348475, 1408157, 1470367, 1531731, 1598047],
            dtype=&#39;int64&#39;),
 1029: Int64Index([1241608, 1299193, 1357511, 1417538, 1479441, 1540492], dtype=&#39;int64&#39;),
 1033: Int64Index([   1253,   56389,  111303,  166419,  221222,  277384,  331171,
              387666,  444271,  500340,  556357,  613340,  671660,  727982,
              784444,  840667,  896425,  953225, 1009604, 1067157, 1123462,
             1180080, 1238136, 1295804, 1354032, 1413957, 1475860, 1536690],
            dtype=&#39;int64&#39;),
 1034: Int64Index([  10981,   65874,  120812,  175762,  230932,  286650,  340969,
              397377,  453884,  509778,  566093,  623301,  681223,  737746,
              794143,  850334,  906030,  962615, 1019329, 1076795, 1133147,
             1190201, 1248217, 1305776, 1364408, 1424648, 1486383, 1548005],
            dtype=&#39;int64&#39;),
 1037: Int64Index([  30610,   85090,  140047,  194931,  250496,  305754,  360894,
              417341,  473310,  529087,  585871,  643558,  700810,  757494,
              813693,  869650,  925304,  981968, 1039134, 1096466, 1152720,
             1210507, 1268233, 1325818, 1384923, 1445984, 1507426, 1570699],
            dtype=&#39;int64&#39;),
 1038: Int64Index([  19478,   74356,  129353,  184144,  239567,  295100,  349839,
              405976,  462394,  518241,  574688,  632169,  689763,  746361,
              802611,  858795,  914445,  970985, 1027832, 1085336, 1141696,
             1199003, 1256937, 1314603, 1373284, 1495611, 1557961],
            dtype=&#39;int64&#39;),
 1049: Int64Index([ 476899,  589458,  647299,  704356,  761179,  817383,  873210,
              928873,  985440, 1042626, 1100069, 1156264, 1214162, 1271951,
             1329432, 1388684, 1449936, 1574873],
            dtype=&#39;int64&#39;),
 1050: Int64Index([  41898,   96064,  150886,  205705,  261467,  316405,  372231,
              428691,  484333,  540166,  596989,  655069,  711828,  768721,
              825002,  880755,  936456,  992900, 1050280, 1107581, 1163746,
             1222106, 1279611, 1337048, 1396571, 1458189, 1519577, 1583672],
            dtype=&#39;int64&#39;),
 1055: Int64Index([  50901,  105187,  159999,  214782,  270612,  325407,  381408,
              438088,  493620,  549544,  606507,  664769,  721857,  778168,
              834332,  889854,  946141, 1002604, 1060071, 1117019, 1173239,
             1231195, 1288698, 1346547, 1406221, 1468311, 1529651, 1595768],
            dtype=&#39;int64&#39;),
 1056: Int64Index([  34733,   89055,  143892,  198760,  309570,  364893,  421427,
              477338,  533130,  589899,  647766,  704815,  761635,  817849,
              873631,  929308,  985891, 1043083, 1100523, 1156675, 1214634,
             1272393, 1329862, 1389166, 1450441, 1511752, 1575390],
            dtype=&#39;int64&#39;),
 1057: Int64Index([ 261898,  316840,  372698,  429167,  484790,  540636,  597439,
              655526,  712521,  769169,  825495,  881247,  936919,  993353,
             1050733, 1108077, 1164254, 1222588, 1280169, 1337536, 1397068,
             1458706, 1520071, 1584188],
            dtype=&#39;int64&#39;),
 1059: Int64Index([411264, 1563941], dtype=&#39;int64&#39;),
 1061: Int64Index([  39767,   72066,  127061,  181986,  237311,  292872,  347478,
              403653,  460112,  515985,  572355,  629819,  687430,  744054,
              800322,  856523,  912136,  968721, 1025557, 1083034, 1139397,
             1196582, 1254624, 1312199, 1370810, 1431434, 1493136, 1555304],
            dtype=&#39;int64&#39;),
 1064: Int64Index([  46856,  101018,  155809,  210635,  266454,  321296,  377351,
              433835,  489373,  545230,  602222,  660268,  717246,  773784,
              830034,  885683,  941523,  997999, 1055383, 1112484, 1168851,
             1226889, 1284425, 1342094, 1401676, 1463640, 1524910, 1590321],
            dtype=&#39;int64&#39;),
 1082: Int64Index([  44663,   98726,  153578,  208408,  264186,  319089,  374998,
              431396,  486970,  542811,  599718,  657799,  714734,  771454,
              827694,  883354,  939107,  995548, 1052950, 1110249, 1166488,
             1224798, 1282340, 1339823, 1399385, 1461172, 1522432, 1587215],
            dtype=&#39;int64&#39;),
 1086: Int64Index([  50332,  104583,  159428,  214207,  270015,  324806,  380727,
              437420,  491176,  547034,  604077,  662192,  719330,  775703,
              831866,  887454,  943431,  999919, 1057344, 1114404, 1170653,
             1228553, 1286182, 1343900, 1403590, 1465566, 1526873, 1592721],
            dtype=&#39;int64&#39;),
 1092: Int64Index([  41539,   95682,  150538,  205365,  261085,  316052,  371834,
              428316,  483948,  539801,  596596,  654657,  711461,  768333,
              824638,  880387,  936061,  992519, 1049887, 1107219, 1163380,
             1221701, 1279211, 1336653, 1396152, 1457747, 1519137, 1583226],
            dtype=&#39;int64&#39;),
 1106: Int64Index([1537483], dtype=&#39;int64&#39;),
 1109: Int64Index([  20051,   74900,  129909,  184720,  240129,  295646,  350394,
              406512,  462950,  518778,  575262,  632713,  690324,  746925,
              803185,  859344,  914995,  971532, 1028411, 1085926, 1142272,
             1199579, 1257534, 1315182, 1373878, 1434523, 1496240, 1558623],
            dtype=&#39;int64&#39;),
 1110: Int64Index([  39378,   93632,  148438,  203193,  258934,  313970,  369600,
              426088,  481802,  537626,  594418,  652421,  709306,  766162,
              822477,  878268,  933985,  990371, 1047697, 1105088, 1161248,
             1219376, 1277009, 1334469, 1393904, 1455354, 1516822, 1580756],
            dtype=&#39;int64&#39;),
 1112: Int64Index([  10531,   65430,  120345,  175330,  230488,  286211,  340502,
              396915,  453436,  509317,  565617,  622857,  680746,  737271,
              793692,  849868,  905553,  962135, 1018849, 1076314, 1132693,
             1189714, 1247753, 1305310, 1363932, 1424138, 1485907, 1547479],
            dtype=&#39;int64&#39;),
 1113: Int64Index([  23615,   78367,  133371,  188243,  243729,  299109,  353973,
              410211,  466383,  522237,  578866,  636408,  693892,  750574,
              806790,  862904,  918498,  975116, 1032043, 1089473, 1145772,
             1203363, 1261150, 1318793, 1377578, 1438420, 1500054, 1562740],
            dtype=&#39;int64&#39;),
 1122: Int64Index([   5273,   60315,  115173,  170162,  225187,  281168,  335180,
              391645,  448177,  504216,  560370,  617477,  675525,  732036,
              788425,  844629,  900379,  957067, 1013511, 1071066, 1184217,
             1299907, 1358279, 1418267, 1480180, 1541277],
            dtype=&#39;int64&#39;),
 1126: Int64Index([1525581, 1591299], dtype=&#39;int64&#39;),
 1129: Int64Index([ 431804,  487408,  543244,  600166,  658220,  715247,  771831,
              828125,  883715,  939513,  995982, 1053398, 1110576, 1166849,
             1522856, 1587767],
            dtype=&#39;int64&#39;),
 1133: Int64Index([  40807,   94940,  149806,  204573,  260274,  315306,  370992,
              427487,  483161,  539023,  595803,  653841,  710682,  767542,
              823838,  879600,  935308,  991708, 1049081, 1106470, 1162614,
             1220834, 1278410, 1335849, 1395313, 1456859, 1518279, 1582329],
            dtype=&#39;int64&#39;),
 1138: Int64Index([  50433,  104705,  159531,  214301,  270127,  324922,  380862,
              437536,  493046,  548991,  605948,  664160,  721264,  777584,
             1288058, 1345918, 1405559, 1467637, 1528928, 1595016],
            dtype=&#39;int64&#39;),
 1144: Int64Index([   1637,   56764,  111684,  166769,  221600,  277756,  331530,
              388052,  444636,  500715,  556746,  613753,  672042,  728376,
              784834,  841062,  896800,  953607, 1009973, 1067538, 1123839,
             1180465, 1238532, 1296180, 1354415, 1414361, 1476272, 1537129],
            dtype=&#39;int64&#39;),
 1145: Int64Index([  52184,  106549,  156872,  211717,  272148,  326923,  383041,
              439691,  495416,  551240,  608205,  666547,  723648,  780018,
              836113,  891653,  948023, 1004428, 1061970, 1118913, 1175205,
             1233227, 1290643, 1348542, 1408229, 1470439, 1531798, 1598123],
            dtype=&#39;int64&#39;),
 1146: Int64Index([  19022,   73899,  118641,  183720,  228743,  294647,  349335,
              405498,  461918,  517782,  574209,  631686,  689298,  745890,
              802134,  848170,  913971,  960441, 1027377, 1084880, 1141247,
             1187882, 1256448, 1314116, 1372776, 1433396, 1484009, 1557421],
            dtype=&#39;int64&#39;),
 1150: Int64Index([  12233,   67143,  122130,  177085,  232262,  287970,  342346,
              398687,  455193,  511091,  567376,  624671,  682537,  739053,
              795444,  851632,  907302,  963877, 1020652, 1078070, 1134419,
             1191466, 1249485, 1307086, 1365767, 1426034, 1487771, 1549514],
            dtype=&#39;int64&#39;),
 1153: Int64Index([  15373,   70269,  125238,  180175,  235431,  291055,  345558,
              401813,  458321,  514184,  570593,  685595,  742205,  798528,
              854699, 1081195, 1137546, 1194711, 1252701, 1310290, 1368971,
             1429444, 1491190, 1553158],
            dtype=&#39;int64&#39;),
 1154: Int64Index([1102920, 1217117, 1453042, 1514458, 1578215], dtype=&#39;int64&#39;),
 1156: Int64Index([  13960,   68894,  123876,  178837,  234045,  289688,  344131,
              400439,  456966,  512826,  569207,  626478,  684250,  740835,
              797173,  853355,  909014,  965628, 1022437, 1079822, 1136157,
             1193295, 1251269, 1308850, 1367586, 1427956, 1551527],
            dtype=&#39;int64&#39;),
 1163: Int64Index([  11903,   66820,  121790,  176741,  231908,  287627,  341975,
              398345,  454850,  510731,  624309,  682189,  738705,  851286,
              906969,  963536, 1020293, 1077714, 1134089, 1191125, 1249167,
             1306759, 1365422, 1425657, 1487418, 1549130],
            dtype=&#39;int64&#39;),
 1168: Int64Index([  31379,   85829,  140799,  195644,  251200,  306489,  361627,
              418152,  474058,  529894,  586647,  644355,  701571,  758307,
              814486,  870423,  926083,  982770, 1039907, 1097261, 1153537,
             1211299, 1269068, 1326612, 1385735, 1446839, 1508270, 1571578],
            dtype=&#39;int64&#39;),
 1170: Int64Index([  25468,   80206,  135106,  190026,  300872,  355777,  412099,
              468241,  524075,  580732,  638306,  695718,  752410,  808641,
              864685,  920363,  976974, 1091322, 1147602, 1205258, 1263049,
             1320655, 1379566, 1502015, 1564874],
            dtype=&#39;int64&#39;),
 1183: Int64Index([  22200,   76997,  131985,  186854,  242306,  297701,  352580,
              408752,  465043,  520857,  577429,  634977,  692494,  749138,
              805386,  861524,  917098,  973744, 1030654, 1088077, 1144415,
             1201926, 1259726, 1317395, 1376165, 1436973, 1498559, 1561171],
            dtype=&#39;int64&#39;),
 1184: Int64Index([   5207,   60260,  115121,  170113,  225123,  281112,  335116,
              391587,  448117,  504163,  560309,  617417,  675470,  731986,
              788375,  844577,  900332,  957013, 1013457, 1071016, 1299858,
             1358217, 1418211, 1480124, 1541227],
            dtype=&#39;int64&#39;),
 1192: Int64Index([  41745,   95909,  150739,  205570,  261319,  316254,  372059,
              428543,  484172,  540032,  596837,  654896,  711663,  768560,
              824847,  880600,  936302,  992741, 1050131, 1107416, 1163580,
             1221929, 1279438, 1336877, 1396395, 1458005, 1519389, 1583481],
            dtype=&#39;int64&#39;),
 1193: Int64Index([  41127,   95265,  150118,  204929,  260632,  315635,  371368,
              427861,  483511,  539360,  596131,  654196,  711018,  767892,
              824196,  879947,  935622,  992082, 1049444, 1106792, 1162936,
             1221222, 1278757, 1336185, 1395675, 1457240, 1518650, 1582726],
            dtype=&#39;int64&#39;),
 1197: Int64Index([  13010,   67944,  122917,  177872,  233073,  288746,  343148,
              399470,  455995,  511908,  568201,  625482,  683336,  739901,
              796236,  852443,  908077,  964667, 1021469, 1078882, 1192310,
             1250291, 1307886, 1366592, 1426910, 1488641, 1550442],
            dtype=&#39;int64&#39;),
 1201: Int64Index([  40931,   95065,  149919,  204705,  260405,  315439,  371127,
              427620,  483294,  539141,  582571,  653963,  710806,  767666,
              823956,  879721,  935414,  991828, 1049206, 1518403, 1582455],
            dtype=&#39;int64&#39;),
 1208: Int64Index([  22059,   76842,  131844,  186710,  242168,  297557,  408611,
              464910,  520727,  577299,  634829,  692362,  748993,  805231,
              861396,  916964,  973606, 1087944, 1144291, 1201781, 1259596,
             1317259, 1376027, 1436837, 1498423, 1561030],
            dtype=&#39;int64&#39;),
 1218: Int64Index([  31272,   85708,  140698,  195538,  251102,  306390,  361522,
              418040,  473947,  529779,  586542,  644235,  701460,  758192,
              814368,  870321,  925977,  982660, 1039797, 1097155, 1153427,
             1211195, 1268959, 1326513, 1385622, 1446712, 1508157, 1571447],
            dtype=&#39;int64&#39;),
 1219: Int64Index([  57117,  112032,  501051,  785214, 1124175, 1180833, 1238922,
             1296570, 1354779, 1414760, 1476659, 1537527],
            dtype=&#39;int64&#39;),
 1223: Int64Index([  11313,   66229,  121178,  176136,  231279,  286997,  341327,
              397718,  454242,  510121,  566429,  623656,  681564,  738108,
              791339,  850691,  906389,  962959, 1019682, 1077145, 1133484,
             1190528, 1248552, 1306130, 1364761, 1425013, 1486763, 1548391],
            dtype=&#39;int64&#39;),
 1229: Int64Index([  16140,   71026,  126009,  180903,  236211,  291806,  346365,
              402634,  459091,  514937,  571286,  628674,  686372,  742951,
              799279,  855461,  911083,  967669, 1024517, 1081967, 1138331,
             1195488, 1253510, 1311079, 1369706, 1430273, 1491987, 1554060],
            dtype=&#39;int64&#39;),
 1240: Int64Index([  30321,   84832,  139787,  194672,  250235,  305453,  360610,
              417022,  473046,  528832,  585575,  643269,  700522,  757200,
              813414,  869367,  925029,  981696, 1038837, 1096180, 1152449,
             1210218, 1267949, 1325518, 1384644, 1445686, 1507147, 1570347],
            dtype=&#39;int64&#39;),
 1241: Int64Index([  47651,  101814,  144484,  211417,  267216,  322065,  365492,
              434588,  490160,  546016,  603025,  661122,  718229,  774672,
              830858,  886457,  942332,  998826, 1056244, 1113379, 1169714,
             1227611, 1285179, 1342867, 1402479, 1464416, 1525745, 1591483],
            dtype=&#39;int64&#39;),
 1252: Int64Index([  51953,  106300,  161139,  215947,  271859,  318617,  374565,
              430977,  495123,  550935,  607914,  666239,  723338,  779695,
              835824,  891358,  947685, 1004099, 1061653, 1118585, 1174861,
             1232856, 1290302, 1348204, 1407884, 1470070, 1531447, 1597713],
            dtype=&#39;int64&#39;),
 1256: Int64Index([   3338,   58410,  113303,  168380,  223228,  279331,  333228,
              389744,  446305,  502347,  585909,  643591,  700841,  757525,
              813729,  869684,  925329,  982001, 1096502, 1152754, 1210535,
             1268269, 1325852, 1384952, 1446021, 1507462, 1570737],
            dtype=&#39;int64&#39;),
 1270: Int64Index([  26433,   81133,  136059,  190954,  246475,  301811,  356774,
              413120,  469225,  525045,  581685,  639295,  696713,  753379,
              809617,  865644,  921308,  977948, 1034969, 1092302, 1148601,
             1206232, 1263984, 1321619, 1380564, 1441448, 1503043, 1565983],
            dtype=&#39;int64&#39;),
 1273: Int64Index([   3615,   58694,  113578,  168629,  223512,  279591,  333511,
              446577,  502628,  558762,  615771,  673972,  730362,  786794,
              878123,  933848,  990225, 1047577, 1104953, 1161094, 1219227,
             1276869, 1334320, 1393749, 1455201, 1516681, 1580604],
            dtype=&#39;int64&#39;),
 1274: Int64Index([  38184,   92496,  147296,  202042,  257761,  312863,  368364,
              424875,  480650,  536434,  593229,  651214,  708136,  764993,
              821327,  877088,  932780,  989233, 1046512, 1103964, 1160111,
             1218169, 1275852, 1333305, 1454124, 1579399],
            dtype=&#39;int64&#39;),
 1276: Int64Index([  14728,   69637,  124621,  179602,  234831,  290446,  344939,
              401227,  457725,  513570,  569983,  627269,  685002,  741590,
              797948,  854133,  909766,  966397, 1023185, 1080596, 1136943,
             1194088, 1252072, 1309643, 1368395, 1428795, 1490548, 1552436],
            dtype=&#39;int64&#39;),
 1282: Int64Index([  26149,   80864,  135786,  190685,  246217,  301537,  356482,
              412810,  468937,  524771,  581405,  638991,  696427,  753103,
              809333,  865359,  921047,  977662, 1034672, 1092030, 1321321,
             1380263, 1441118, 1502738, 1565675],
            dtype=&#39;int64&#39;),
 1284: Int64Index([  51555,  105904,  160704,  215503,  271382,  326185,  382229,
              438898,  494573,  550399,  607374,  665683,  722776,  779104,
              835252,  890793,  947081, 1003517, 1061049, 1117975, 1174237,
             1232217, 1289679, 1347532, 1407234, 1469375, 1530762, 1596940],
            dtype=&#39;int64&#39;),
 1285: Int64Index([176653, 231801, 341873, 398242, 738620, 794997, 1249082, 1487325,
             1549008],
            dtype=&#39;int64&#39;),
 1287: Int64Index([  25366,   80109,  135005,  189926,  245431,  300765,  355680,
              411999,  468149,  523978,  580635,  638201,  695624,  752313,
              808549,  864586,  976872, 1033868, 1147504, 1205161, 1262943,
             1320553, 1379465, 1440294, 1501919, 1564768],
            dtype=&#39;int64&#39;),
 1288: Int64Index([  38991,   93246,  148057,  202812,  258559,  313594,  369199,
              425670,  481412,  537209,  594012,  652021,  708924,  765770,
              822073,  877871,  933604,  989997, 1047321, 1104692, 1160863,
             1218969, 1276622, 1334072, 1393501, 1454926, 1516414, 1580318],
            dtype=&#39;int64&#39;),
 1289: Int64Index([  12922,   67850,  122825,  177776,  232979,  288660,  343065,
              399383,  455905,  511816,  568114,  625388,  683240,  739813,
              796145,  852351,  907994,  964580, 1021380, 1078792, 1192217,
             1250209, 1307799, 1366509, 1426823, 1488548, 1550346],
            dtype=&#39;int64&#39;),
 1291: Int64Index([  40140,   94306,  149147,  203894,  259599,  314633,  370315,
              426784,  482500,  538364,  595133,  653161,  710018,  766873,
              823171,  878949,  934662,  991038, 1048413, 1105793, 1161936,
             1220150, 1277749, 1335186, 1394641, 1456139, 1517581, 1581560],
            dtype=&#39;int64&#39;),
 1295: Int64Index([  30644,   85118,  140078,  194957,  250521,  305784,  360922,
              417368,  473340,  529116,  585907,  643589,  700839,  757523,
              813725,  869682,  981999, 1039164, 1096500, 1152752, 1210533,
             1446019, 1507460, 1570734],
            dtype=&#39;int64&#39;),
 1299: Int64Index([  19309,   74208,  129196,  184008,  239409,  294945,  405811,
              462227,  518071,  574510,  631992,  689602,  746182,  802446,
              858616,  914269,  970827, 1027675, 1085165, 1141519, 1198818,
             1256759, 1314438, 1373116, 1433720, 1495416, 1557746],
            dtype=&#39;int64&#39;),
 1306: Int64Index([ 485050,  540899,  937214, 1051016, 1108336, 1164514, 1222879,
             1397367, 1459032, 1520367, 1584525],
            dtype=&#39;int64&#39;),
 1307: Int64Index([   7610,   62634,  117527,  172499,  227587,  283456,  337607,
              393980,  450595,  506569,  562737,  619950,  677904,  734389,
              790799,  847033,  902739,  959343, 1015920, 1073426, 1129850,
             1186655, 1244778, 1302315, 1360753, 1420846, 1482754, 1544049],
            dtype=&#39;int64&#39;),
 1311: Int64Index([  34360,   88695,  143538,  198427,  254033,  309225,  421076,
              476978,  532809,  589545,  647395,  704448,  761263,  817485,
              873304,  928952,  985535, 1042716, 1100159, 1156331, 1214256,
             1272029, 1388767, 1450039, 1511387, 1574973],
            dtype=&#39;int64&#39;),
 1313: Int64Index([  37931,   92239,  147052,  201809,  257511,  312627,  368120,
              424634,  480413,  536181,  592991,  650989,  707906,  764757,
              821096,  876848,  932514,  988986, 1046249, 1103712, 1159845,
             1217938, 1275594, 1333050, 1453867, 1515285, 1579095],
            dtype=&#39;int64&#39;),
 1316: Int64Index([  22488,   77285,  187166,  242626,  352905,  409060,  465330,
              521155,  577730,  635307,  692811,  749441,  805712,  861832,
              917412,  974057, 1030953, 1088391, 1144712, 1202255, 1317692,
             1376477, 1437296, 1561509],
            dtype=&#39;int64&#39;),
 1317: Int64Index([ 477721,  705204,  986303, 1215069, 1272794, 1330270, 1389568,
             1450867, 1475684, 1575868],
            dtype=&#39;int64&#39;),
 1318: Int64Index([   9190,   64150,  119049,  229188,  284963,  339186,  395601,
              452174,  621565,  792386, 1303992, 1362525, 1422630, 1484489,
             1545956],
            dtype=&#39;int64&#39;),
 1329: Int64Index([  36034,   90356,  145170,  200005,  255638,  310782,  366188,
              422743,  478590,  534371,  591145,  649067,  706072,  762911,
              819175,  874927,  930603,  987144, 1044336, 1101773, 1157921,
             1215934, 1273697, 1331185, 1390432, 1451856, 1513184, 1576878],
            dtype=&#39;int64&#39;),
 1330: Int64Index([  17914,   72814,  127801,  182671,  238044,  293608,  348249,
              404415,  460858,  516704,  573142,  630589,  688214,  744811,
              801057,  857242,  912874,  969473, 1026306, 1083796, 1140156,
             1197420, 1255359, 1313012, 1371623, 1432264, 1493959, 1556171],
            dtype=&#39;int64&#39;),
 1333: Int64Index([  40923,   95054,  149905,  204694,  260396,  315425,  371115,
              427602,  483276,  539129,  595902,  653946,  710790,  767652,
              879706,  935402,  991808, 1049187, 1106565, 1162707, 1220956,
             1278521, 1335951, 1395420, 1456976, 1518389, 1582437],
            dtype=&#39;int64&#39;),
 1334: Int64Index([  34604,   88940,  143766,  198656,  254275,  309461,  364773,
              421306,  477220,  533031,  589773,  647645,  704691,  761507,
              817728,  873525,  929197,  985774, 1042964, 1100394, 1156558,
             1214521, 1272268, 1329749, 1389042, 1450318, 1511631, 1575239],
            dtype=&#39;int64&#39;),
 1337: Int64Index([  71747,  292546,  687109,  743710,  800016,  856184,  911819,
              968400, 1025249, 1082722, 1139063, 1431056, 1492795, 1554922],
            dtype=&#39;int64&#39;),
 1338: Int64Index([  32105,   86507,  141477,  196345,  251885,  307149,  362340,
              418842,  474734,  530598,  587340,  645107,  702277,  758992,
              815193,  871114,  926781,  983460, 1040606, 1097959, 1154220,
             1212045, 1269791, 1327315, 1386473, 1447620, 1509028, 1572398],
            dtype=&#39;int64&#39;),
 1339: Int64Index([  19554,   74422,  129425,  184212,  239633,  295166,  349905,
              406052,  462459,  518305,  574760,  632238,  689829,  746426,
              802679,  858858,  914505,  971049, 1027889, 1085409, 1141768,
             1199072, 1257003, 1314680, 1373368, 1434003, 1495697, 1558054],
            dtype=&#39;int64&#39;),
 1340: Int64Index([  24370,  134103,  188989,  244467,  299853,  354721,  411004,
              467156,  523014,  579642,  637185,  694645,  751359,  807586,
              863653,  975884, 1032834, 1090257, 1146532, 1204164, 1261937,
             1319572, 1378426, 1439250, 1500897, 1563653],
            dtype=&#39;int64&#39;),
 1341: Int64Index([  46901,  101073,  155853,  210683,  266500,  321337,  377399,
              433890,  489429,  545286,  602278,  660331,  717306,  773841,
              830093,  885741,  941585,  998063, 1055437, 1112537, 1168909,
             1226952, 1284485, 1342149, 1401730, 1463695, 1524963, 1590382],
            dtype=&#39;int64&#39;),
 1342: Int64Index([  49865,  104078,  158926,  213688,  269515,  324302,  380208,
              436867,  492355,  552329,  609253,  663394,  720507,  776830,
              837127,  892680,  944736, 1001207, 1058600, 1115556, 1176370,
             1229698, 1287269, 1345107, 1404739, 1471631, 1528084, 1594094],
            dtype=&#39;int64&#39;),
 1346: Int64Index([1141839, 1199152, 1257085, 1314745, 1373452, 1434082, 1495773,
             1558135],
            dtype=&#39;int64&#39;),
 1355: Int64Index([ 881011,  936698,  993119, 1050504, 1107837, 1164023, 1222360,
             1279921, 1337301, 1396825, 1458456, 1519833, 1583944],
            dtype=&#39;int64&#39;),
 1357: Int64Index([  21318,   76152,  131150,  186013,  241473,  296888,  351716,
              407860,  464149,  520007,  576555,  634082,  691592,  748241,
              804512,  860663,  916241, 1029784, 1087216, 1143588, 1258863,
             1316535, 1375246, 1436045, 1497674, 1560183],
            dtype=&#39;int64&#39;),
 1359: Int64Index([  42507,   96608,  151449,  262021,  316957,  372828,  434275,
              489847,  540762,  597565,  660809,  712645,  774364,  830542,
              943330,  998513, 1050867, 1113065, 1169402, 1227323, 1284879,
             1342583, 1402172, 1464114, 1525433, 1591153],
            dtype=&#39;int64&#39;),
 1360: Int64Index([ 992589, 1049954, 1107280, 1163445, 1221771, 1279288, 1336717,
             1396225, 1457830, 1519210, 1583300],
            dtype=&#39;int64&#39;),
 1361: Int64Index([ 128518,  183328,  238720,  294293,  405108,  461526,  517396,
              573815,  631289,  688927,  745507,  857940,  913586,  970146,
             1026980, 1084475, 1140835, 1256057, 1313704, 1372362, 1432980,
             1494669, 1556967],
            dtype=&#39;int64&#39;),
 1362: Int64Index([  33950,   88284,  143150,  198055,  253663,  308857,  364123,
              420676,  476578,  532417,  589147,  647013,  704062,  760870,
              817081,  872911,  928565,  985127, 1042330, 1099764, 1155958,
             1213833, 1271635, 1329116, 1388355, 1449601, 1510950, 1574489],
            dtype=&#39;int64&#39;),
 1370: Int64Index([  37493,   91807,  146622,  201401,  257084,  312230,  367680,
              424196,  479982,  535753,  592560,  650564,  707485,  764326,
              820654,  876419,  932075,  988573, 1045824, 1103284, 1159410,
             1217497, 1275150, 1332630, 1391981, 1453417, 1514837, 1578643],
            dtype=&#39;int64&#39;),
 1371: Int64Index([1346090, 1405736, 1595222], dtype=&#39;int64&#39;),
 1374: Int64Index([  34403,   88732,  143581,  198470,  254085,  309274,  364565,
              421122,  477020,  532846,  589596,  647447,  704494,  761312,
              817542,  873345,  929002,  985588, 1042767, 1100210, 1156373,
             1214303, 1272080, 1329556, 1388819, 1450095, 1511435, 1575023],
            dtype=&#39;int64&#39;),
 1375: Int64Index([  26160,  135795,  190693,  246232,  301550,  356499,  412825,
              468949,  524785,  581416,  639005,  696439,  753115,  809346,
              865375,  921058,  977675, 1034685, 1092043, 1148311, 1205946,
             1263712, 1321339, 1380275, 1441133, 1502753, 1565685],
            dtype=&#39;int64&#39;),
 1379: Int64Index([   7640,   62662,  117555,  172526,  227625,  283486,  337635,
              394007,  450624,  506601,  562769,  619981,  677932,  734422,
              790835,  847072,  902773,  959374, 1015950, 1073463, 1129894,
             1186687, 1244815, 1302350, 1360795, 1420880, 1482798, 1544085],
            dtype=&#39;int64&#39;),
 1384: Int64Index([  12855,   67783,  122758,  177711,  232912,  288600,  342997,
              399318,  455837,  511744,  568044,  625313,  683167,  739740,
              796066,  852281,  907925,  964504, 1021303, 1078718, 1135085,
             1192144, 1250127, 1307719, 1366433, 1426744, 1488471, 1550265],
            dtype=&#39;int64&#39;),
 1388: Int64Index([  42185,   96329,  151159,  205994,  261731,  316659,  372519,
              428982,  484608,  540458,  597260,  655354,  712331,  768995,
              825296,  881059,  936738,  993158, 1050549, 1107879, 1164075,
             1222410, 1279976, 1337353, 1396876, 1458524, 1519882, 1583995],
            dtype=&#39;int64&#39;),
 1390: Int64Index([  40881,   95011,  149867,  204638,  260351,  315383,  371078,
              402406,  483234,  539090,  595861,  653910,  710752,  767616,
              823913,  879666,  935374,  991770, 1049144, 1106535, 1162677,
             1220919, 1278485, 1335914, 1395377, 1456939, 1518348, 1582393],
            dtype=&#39;int64&#39;),
 1397: Int64Index([   9400,   64362,  119245,  174261,  229382,  285161,  339405,
              395813,  452365,  508291,  564504,  621763,  679677,  736179,
              792620,  848785,  904504,  961091, 1017736, 1075249, 1131634,
             1188596, 1246651, 1304178, 1362742, 1422858, 1484701, 1546186],
            dtype=&#39;int64&#39;),
 1405: Int64Index([  39481,   93727,  148543,  203290,  259032,  314074,  369694,
              426188,  481898,  537728,  594520,  652516,  709405,  766261,
              822577,  878370,  934085,  990465, 1047794, 1105190, 1161345,
             1219483, 1277125, 1334578, 1394007, 1455457, 1516927, 1580869],
            dtype=&#39;int64&#39;),
 1413: Int64Index([  44563,   98617,  153478,  208308,  264089,  318989,  374899,
              431309,  486877,  542713,  599623,  657699,  714627,  771337,
              827593,  883259,  939009,  995441, 1052845, 1110171, 1166409,
             1224712, 1282248, 1339728, 1399291, 1461059, 1522314, 1587106],
            dtype=&#39;int64&#39;),
 1414: Int64Index([  15077,   69960,  124947,  179899,  235151,  290761,  345278,
              401536,  458039,  513905,  570321,  627625,  685318,  741931,
              798265,  851670,  910082,  966695, 1023522, 1080911, 1137274,
             1194426, 1252429, 1310000, 1368713, 1429160, 1490890, 1552821],
            dtype=&#39;int64&#39;),
 1415: Int64Index([ 565535,  622765,  680659,  737186,  793608,  849775,  905468,
              962045, 1018766, 1076225, 1132603, 1189629, 1247668, 1305213,
             1363840, 1424028, 1485797, 1547365],
            dtype=&#39;int64&#39;),
 1419: Int64Index([  26299,   81013,  135936,  190834,  246355,  301681,  356647,
              412969,  469089,  524918,  581556,  639155,  696582,  753256,
              809483,  865507,  921185,  977819, 1034833, 1092175, 1148467,
             1206093, 1263845, 1321481, 1380418, 1441287, 1502894, 1565840],
            dtype=&#39;int64&#39;),
 1420: Int64Index([  13685,   68616,  123593,  178556,  233775,  289402,  333048,
              389574,  456706,  512563,  568933,  626195,  683989,  740561,
              853074,  908727,  965358, 1022156, 1079549, 1135887, 1192992,
             1240133, 1308542, 1367295, 1427662, 1489408, 1551208],
            dtype=&#39;int64&#39;),
 1423: Int64Index([  32640,  141932,  252410,  307638,  362870,  419369,  475269,
              531124,  587846,  645654,  702762,  759515,  815703,  871585,
              927275,  983957, 1041121, 1098465, 1154697, 1212563, 1270282,
             1327793, 1387008, 1448211, 1509562, 1572978],
            dtype=&#39;int64&#39;),
 1431: Int64Index([  25635,   80361,  135258,  190170,  245681,  301031,  355944,
              412259,  468401,  524245,  580898,  638471,  695876,  752569,
              808808,  864843,  920526,  977127, 1034124, 1091483, 1147755,
             1205416, 1263206, 1320811, 1379726, 1440563, 1502189, 1565051],
            dtype=&#39;int64&#39;),
 1436: Int64Index([944994, 955845, 1014054, 1071614, 1127957, 1184765, 1242860,
             1300428, 1541874],
            dtype=&#39;int64&#39;),
 1437: Int64Index([  13963,   68897,  123879,  178840,  234048,  289691,  344134,
              400442,  456969,  512829,  569210,  626481,  684253,  740838,
              797176,  853358,  909018,  965631, 1022440, 1079825, 1367589,
             1427959, 1489704, 1551530],
            dtype=&#39;int64&#39;),
 1439: Int64Index([  91233,  200881,  311710,  367122,  423625,  479414,  535243,
              592021,  649994,  706931,  763795,  820081,  875876,  931506,
              988009, 1158854, 1216893, 1452846, 1514229, 1577982],
            dtype=&#39;int64&#39;),
 1441: Int64Index([  22607,   77396,  132389,  187288,  242729,  298139,  353033,
              409191,  465437,  521269,  577866,  635431,  692935,  749568,
              805828,  861943,  917527,  974164, 1031063, 1088503, 1144824,
             1202363, 1260148, 1317796, 1437412, 1499001, 1561634],
            dtype=&#39;int64&#39;),
 1442: Int64Index([  49192,  103392,  158136,  212958,  268785,  323577,  379550,
              436131,  491641,  547487,  604525,  662631,  719789,  776136,
              832288,  887870,  943907, 1000414, 1057801, 1114839, 1171105,
             1229019, 1286632, 1347788, 1404051, 1466038, 1527323, 1593232],
            dtype=&#39;int64&#39;),
 1449: Int64Index([ 324714,  437327,  492837,  889006,  945272, 1230250, 1287800,
             1345657, 1405284, 1467371, 1528637, 1594708],
            dtype=&#39;int64&#39;),
 1450: Int64Index([  35490,   89782,  144620,  199474,  255104,  310265,  365656,
              422180,  478038,  533831,  590633,  648530,  705539,  762360,
              818613,  874375,  930045,  986617, 1389882, 1512602, 1576265],
            dtype=&#39;int64&#39;),
 1459: Int64Index([   7687,   62703,  117599,  172564,  227662,  283523,  337674,
              394048,  450668,  506641,  562812,  620024,  677971,  734472,
              790878,  847116,  902816,  959404, 1015987, 1073504, 1129937,
             1186730, 1244859, 1302396, 1360836, 1420926, 1482845, 1544141],
            dtype=&#39;int64&#39;),
 1460: Int64Index([ 139370,  249804,  305046,  360183,  700092,  812997, 1038359,
             1095767, 1151994, 1267517, 1325068, 1445190, 1569840],
            dtype=&#39;int64&#39;),
 1463: Int64Index([  15643,   70552,  125529,  180415,  235708,  291331,  345846,
              402111,  458595,  514448,  570828,  628186,  685884,  742461,
              798801,  854984,  910627,  967210, 1024054, 1081483, 1137847,
             1195000, 1253000, 1310588, 1369217, 1429744, 1491454, 1553489],
            dtype=&#39;int64&#39;),
 1467: Int64Index([  45126,   99226,  154069,  208871,  264674,  319551,  375462,
              432066,  487584,  543506,  600437,  658494,  715542,  772093,
              828387,  883969,  939778,  996259, 1053675, 1110748, 1225146,
             1282693, 1340276, 1410376, 1461714, 1523063, 1588149],
            dtype=&#39;int64&#39;),
 1468: Int64Index([1495107, 1557446], dtype=&#39;int64&#39;),
 1474: Int64Index([  37938,   92247,  201819,  257519,  312634,  368130,  424640,
              480419,  536187,  592999,  650998,  707916,  764764,  821101,
              876853,  932519,  988992, 1046255, 1103718, 1159852, 1217949,
             1275599, 1333061, 1392413, 1453873, 1515292, 1579105],
            dtype=&#39;int64&#39;),
 1475: Int64Index([   5935,   60976,  115813,  170806,  225808,  281806,  335836,
              392280,  448840,  504875,  561055,  618141,  676180,  732695,
              789088,  845342,  901033,  957723, 1014190, 1071740, 1128103,
             1184909, 1243003, 1300556, 1358994, 1418974, 1480918, 1542027],
            dtype=&#39;int64&#39;),
 1476: Int64Index([   7382,   62417,  117301,  172274,  227350,  283241,  337376,
              393736,  450359,  506330,  562487,  619700,  677671,  734145,
              790537,  846801,  902494,  959122, 1015676, 1073191, 1129609,
             1186428, 1244518, 1302079, 1360493, 1420591, 1482513, 1543765],
            dtype=&#39;int64&#39;),
 1480: Int64Index([    587,   55749,  110672,  165770,  220618,  276765,  330477,
              386961,  443594,  499697,  555627,  612594,  670965,  727307,
              783751,  839980,  895770,  952539, 1008949, 1066464, 1122756,
             1179388, 1237450, 1295101, 1353313, 1413242, 1475117, 1535946],
            dtype=&#39;int64&#39;),
 1483: Int64Index([  47294,  101477,  156249,  266903,  321749,  377762,  434292,
              489863,  545730,  602755,  660828,  717934,  774379,  830560,
              886160,  942043,  998532, 1055942, 1113078, 1169412, 1227337,
             1284891, 1342593, 1402185, 1464127, 1525454, 1591171],
            dtype=&#39;int64&#39;),
 1487: Int64Index([  17068,   71948,  126946,  181866,  237180,  292758,  347331,
              403545,  460000,  515865,  572235,  629673,  687314,  743923,
              800205,  856400,  912020,  968608, 1082921, 1139271, 1196447,
             1254490, 1312058, 1370682, 1431290, 1493006, 1555155],
            dtype=&#39;int64&#39;),
 1490: Int64Index([1137431, 1194590, 1252589, 1310163, 1491060, 1553015], dtype=&#39;int64&#39;),
 1494: Int64Index([ 431910,  543345,  600273,  658324,  715368,  771934,  828228,
              883808,  939612,  996085, 1053507, 1166955, 1587894],
            dtype=&#39;int64&#39;),
 1500: Int64Index([  34975,   89282,  144128,  199003,  254596,  309789,  365125,
              421691,  477543,  533355,  590125,  647998,  705035,  761848,
              818110,  873880,  929529,  986107, 1043307, 1100743, 1156890,
             1214881, 1272625, 1330096, 1389382, 1450680, 1511999, 1575661],
            dtype=&#39;int64&#39;),
 1501: Int64Index([  22766,   77555,  132544,  187448,  242914,  298304,  353194,
              409355,  465597,  521433,  578036,  635609,  693110,  749753,
              806005,  862105,  917688,  974313, 1031248, 1088674, 1144995,
             1202530, 1260322, 1317975, 1376756, 1437601, 1499188, 1561831],
            dtype=&#39;int64&#39;),
 1502: Int64Index([ 723256,  779602,  835736,  891278,  947601, 1004012, 1061561,
             1118498, 1174770, 1290211, 1348098, 1407790, 1469961, 1531346,
             1597596],
            dtype=&#39;int64&#39;),
 1506: Int64Index([  16139,   71025,  126008,  180902,  236210,  346364,  402631,
              459090,  514936,  571285,  628673,  686371,  742950,  799278,
              855460,  911082,  967668, 1024516, 1081966, 1138330, 1195486,
             1253508, 1311078, 1369705, 1430272, 1491986, 1554058],
            dtype=&#39;int64&#39;),
 1507: Int64Index([    676,   55841,  110759,  165867,  220696,  276845,  330577,
              387080,  443699,  499773,  555713,  612693,  671050,  727392,
              783830,  840081,  895845,  952630, 1009032, 1066558, 1179471,
             1237535, 1295193, 1353405, 1413343, 1475203, 1536036],
            dtype=&#39;int64&#39;),
 1510: Int64Index([  40426,   94562,  149401,  204176,  259863,  314902,  370579,
              427071,  482782,  538637,  595422,  653432,  710305,  767152,
              823438,  879238,  934912,  991324, 1048711, 1106080, 1162223,
             1220446, 1278017, 1335447, 1394918, 1456443, 1517867, 1581883],
            dtype=&#39;int64&#39;),
 1511: Int64Index([  35504,   89794,  144630,  199484,  255111,  310274,  365666,
              422190,  478048,  533840,  590643,  648541,  705551,  762372,
              818625,  874389,  930056,  986626, 1043818, 1101228, 1157386,
             1215389, 1273148, 1330632, 1389894, 1451266, 1512617, 1576284],
            dtype=&#39;int64&#39;),
 1516: Int64Index([  39238,   93495,  148285,  203054,  258797,  313840,  369449,
              425943,  481666,  537474,  594262,  652262,  709166,  766016,
              822321,  878116,  933842,  990219, 1047571, 1104947, 1161089,
             1219221, 1276862, 1334314, 1393743, 1455195, 1516674, 1580598],
            dtype=&#39;int64&#39;),
 1518: Int64Index([  19404,   74292,  184086,  239494,  295043,  349768,  405901,
              462319,  518177,  574613,  632099,  689687,  746281,  802546,
              858717,  914366,  970921, 1027768, 1085257, 1141610, 1198917,
             1256860, 1314526, 1373210, 1433832, 1495528, 1557859],
            dtype=&#39;int64&#39;),
 1521: Int64Index([  23768,   78510,  133514,  188376,  243876,  299261,  354126,
              410364,  466528,  522385,  579016,  636567,  694036,  750719,
              806942,  863059,  918643,  975264, 1032197, 1089621, 1145924,
             1203522, 1261301, 1318951, 1377741, 1438585, 1500216, 1562919],
            dtype=&#39;int64&#39;),
 1522: Int64Index([  47373,  101538,  156303,  211146,  321795,  434352,  489915,
              545786,  602795,  717990,  774427,  830621,  886218,  942092,
              998589, 1056001, 1113134, 1342637, 1405385, 1464177, 1525512,
             1591219],
            dtype=&#39;int64&#39;),
 1523: Int64Index([   7944,   62958,  117847,  172816,  227924,  283768,  337935,
              394318,  450938,  506908,  563080,  620297,  678242,  734732,
              791151,  847393,  903080, 1073766, 1130192, 1187009, 1245125,
             1302701, 1361132, 1421222, 1483133, 1544463],
            dtype=&#39;int64&#39;),
 1530: Int64Index([   6918,   61954,  116803,  171806,  226842,  282761,  336897,
              393270,  449866,  505862,  562026,  619203,  677202,  733685,
              790063,  846334,  902042,  958683, 1015221, 1072723, 1129124,
             1185935, 1244019, 1301583, 1359998, 1420071, 1481996, 1543191],
            dtype=&#39;int64&#39;),
 1532: Int64Index([   8598,   63565,  118464,  173452,  284387,  338565,  394982,
              451575,  507507,  563724,  620940,  678886,  735352,  791785,
              848007,  903711,  960268, 1016896, 1074409, 1130800, 1187697,
             1245789, 1303374, 1361851, 1421936, 1483832, 1545226],
            dtype=&#39;int64&#39;),
 1534: Int64Index([   4782,   59830,  114701,  169726,  224692,  280705,  334700,
              391151,  447731,  503733,  559903,  616986,  675083,  731561,
              787937,  844186,  899931,  956618, 1013040, 1070597, 1126936,
             1183727, 1241814, 1299400, 1357742, 1417777, 1479663, 1540744],
            dtype=&#39;int64&#39;),
 1535: Int64Index([  43271,   97299,  152113,  262730,  317653,  430005,  485569,
              541384,  598283,  656335,  713272,  769963,  826300,  882006,
              937725,  994122, 1051504, 1108844, 1165045, 1223388, 1338319,
             1397881, 1459580, 1520920, 1585137],
            dtype=&#39;int64&#39;),
 1537: Int64Index([  44749,   98805,  153662,  208486,  264268,  319170,  375069,
              431477,  487065,  542905,  599800,  657878,  714827,  771524,
              827783,  883433,  939184,  995626, 1053036, 1110323, 1166562,
             1224869, 1282407, 1339895, 1399475, 1461257, 1522523, 1587307],
            dtype=&#39;int64&#39;),
 1538: Int64Index([   1946,   57068,  111986,  167055,  221896,  278052,  331831,
              388370,  444943,  501007,  557057,  614064,  672370,  728688,
              785159,  841362,  897109,  953910, 1010274, 1067843, 1124123,
             1180780, 1238858, 1296519, 1354726, 1414709, 1476602, 1537474],
            dtype=&#39;int64&#39;),
 1539: Int64Index([  24729,   79496,  134422,  189347,  244817,  300199,  355088,
              411359,  467536,  523371,  580005,  637538,  694989,  751693,
              807908,  863982,  919613,  976247, 1033186, 1090601, 1146885,
             1204536, 1262309, 1319934, 1378803, 1439647, 1501259, 1564043],
            dtype=&#39;int64&#39;),
 1542: Int64Index([  19962,   67925,  129827,  184627,  240056,  295566,  350296,
              397580,  454106,  509990,  566308,  623522,  681439,  737967,
              794357,  864870,  920553,  977154, 1034151, 1091510, 1147773,
             1205444, 1240900, 1298468, 1356780, 1416762, 1478723, 1539690],
            dtype=&#39;int64&#39;),
 1550: Int64Index([  37447,  125339,  180257,  235529,  291154,  345666,  401915,
              458423,  685690,  742288,  798612,  854790,  910447,  967031,
             1023873, 1081294, 1137655, 1194809, 1252817, 1369056, 1429556,
             1491281, 1553279],
            dtype=&#39;int64&#39;),
 1552: Int64Index([  48027,  102181,  156941,  211779,  267585,  322418,  378399,
              434934,  490502,  546360,  603375,  661468,  718582,  775030,
              832583,  886762,  942685,  999184, 1056589, 1113696, 1170058,
             1285520, 1343209, 1402839, 1464781, 1526089, 1591880],
            dtype=&#39;int64&#39;),
 1553: Int64Index([  47376,  101542,  156307,  211151,  377817,  434355,  489920,
              545790,  717992,  774429,  830625,  886224,  942097,  998593,
             1056005, 1113140, 1169474, 1227398, 1284948, 1342644, 1402246,
             1464183, 1525519, 1591225],
            dtype=&#39;int64&#39;),
 1556: Int64Index([  51233,   67314,  160344,  215162,  271009,  325814,  381814,
              438511,  494166,  549987,  606969,  665261,  722333,  778659,
              834802,  890337,  946643, 1003079, 1060582, 1117498, 1173762,
             1231728, 1289205, 1347050, 1406732, 1468862, 1530248, 1596396],
            dtype=&#39;int64&#39;),
 1557: Int64Index([  21111,   75959,  130955,  185799,  241260,  296662,  351485,
              407624,  463937,  519790,  576346,  633842,  691370,  748013,
              804282,  860451,  916028,  972641, 1029562, 1086992, 1143369,
             1200779, 1258644, 1316317, 1375033, 1435807, 1497464, 1559917],
            dtype=&#39;int64&#39;),
 1562: Int64Index([ 382728,  439400,  495096,  550910,  607885,  666212,  723310,
              779662,  835795,  891329,  947654, 1004070, 1061621, 1118548,
             1174827, 1232814, 1290268, 1348161, 1407845, 1470025, 1531401,
             1597661],
            dtype=&#39;int64&#39;),
 1563: Int64Index([  24521,   79289,  134257,  189155,  244629,  300019,  354894,
              467339,  523180,  579820,  637345,  694819,  807738,  863798,
              919423,  976060, 1032994, 1090421, 1146690, 1204337, 1262113,
             1319738, 1378608, 1439433, 1501061, 1563832],
            dtype=&#39;int64&#39;),
 1565: Int64Index([  31517,   85967,  140939,  195790,  251332,  306620,  361773,
              418302,  474203,  530039,  586796,  644515,  701717,  758451,
              814640,  870568,  926224,  982916, 1040055, 1097404, 1153680,
             1211446, 1269220, 1326761, 1385895, 1447001, 1508433, 1571738],
            dtype=&#39;int64&#39;),
 1566: Int64Index([1381685, 1442600, 1567179], dtype=&#39;int64&#39;),
 1571: Int64Index([ 576707,  634232,  691748,  748390,  804648,  860807,  916412,
              973009, 1029941, 1087368, 1143738, 1201177, 1259014, 1316685,
             1375407, 1436197, 1497832, 1560347],
            dtype=&#39;int64&#39;),
 1573: Int64Index([1174232, 1232214, 1347526, 1407229, 1469370, 1530757, 1596936], dtype=&#39;int64&#39;),
 1585: Int64Index([1585967], dtype=&#39;int64&#39;),
 1586: Int64Index([   7770,   62777,  117676,  172637,  227740,  283599,  337754,
              394125,  450754,  506727,  562897,  620108,  678051,  734549,
             1302490, 1360932, 1421022, 1482934, 1544244],
            dtype=&#39;int64&#39;),
 1589: Int64Index([   7568,   62592,  117482,  172455,  227548,  283417,  337567,
              393936,  450552,  506526,  562690,  619903,  677862,  734348,
              790750,  846990,  902692,  959307, 1015887, 1073384, 1129802,
             1186609, 1244731, 1302266, 1360704, 1420797, 1482709, 1543996],
            dtype=&#39;int64&#39;),
 1591: Int64Index([1599405], dtype=&#39;int64&#39;),
 1596: Int64Index([  21309,  131141,  185999,  241458,  296880,  351707,  407850,
              464138,  519997,  576545,  634071,  691582,  748232,  804503,
              860653,  916231,  972856, 1029774, 1143575, 1200997, 1258851,
             1316523, 1375233, 1436033, 1560173],
            dtype=&#39;int64&#39;),
 1599: Int64Index([   7699,   62714,  117610,  172575,  227674,  283534,  337685,
              394058,  450679,  506654,  562823,  620035,  677983,  734483,
              818953,  847130,  902827,  959415, 1015999, 1073519, 1129948,
             1186741, 1244870, 1302411, 1360851, 1420938, 1482856, 1544152],
            dtype=&#39;int64&#39;),
 1600: Int64Index([1138536, 1195712, 1253751, 1311290, 1369920, 1430510, 1492221,
             1554319],
            dtype=&#39;int64&#39;),
 1607: Int64Index([  47397,  101569,  156334,  211181,  266992,  321825,  377837,
              434375,  489946,  545815,  602825,  660905,  774455,  830646,
              886245,  942125,  998618, 1056036, 1113166, 1169500, 1227416,
             1342667, 1402269, 1464206, 1525543, 1591250],
            dtype=&#39;int64&#39;),
 1613: Int64Index([  37043,   91363,  146195,  200986,  256656,  311815,  367237,
              423744,  479524,  535345,  592125,  650106,  707042,  763904,
              820206,  875990,  931627,  988123, 1045372, 1102824, 1158963,
             1217018, 1274716, 1332180, 1391537, 1452953, 1514363, 1578114],
            dtype=&#39;int64&#39;),
 1615: Int64Index([  15055,   69940,  179884,  235130,  290744,  345257,  401515,
              513884,  570305,  627607,  685303,  741914,  910065,  966672,
             1023499, 1137256, 1194402, 1252405, 1368689, 1429141, 1490865,
             1552793],
            dtype=&#39;int64&#39;),
 1616: Int64Index([  88686,  143529,  198416,  309214,  336165,  476969,  532798,
              647382,  704435,  761253,  817474,  873294,  928943,  958024,
             1042706, 1072031, 1185244, 1272017, 1388754, 1574962],
            dtype=&#39;int64&#39;),
 1618: Int64Index([  42843,   96919,  151751,  206591,  262354,  317281,  373148,
              429614,  485220,  541056,  597913,  825934,  881683,  937364,
              993776, 1051170, 1108492, 1164684, 1223045, 1280593, 1337957,
             1397526, 1520556, 1584707],
            dtype=&#39;int64&#39;),
 1623: Int64Index([   2828,   57923,  112795,  167920,  222744,  278849,  332729,
              389221,  445839,  501862,  557989,  615013,  673218,  729599,
              786054,  842235,  897987,  954736, 1011123, 1068718, 1125027,
             1181679, 1239804, 1297404, 1355658, 1415629, 1477567, 1538475],
            dtype=&#39;int64&#39;),
 1629: Int64Index([    266,   55455,  110382,  165482,  220325,  276477,  330171,
              386660,  443301,  499390,  555323,  612280,  670675,  727011,
              783469,  839707,  895458,  952247, 1008614, 1066160, 1122445,
             1179046, 1237105, 1294794, 1353007, 1412923, 1474790, 1535594],
            dtype=&#39;int64&#39;),
 1633: Int64Index([  14396,   69345,  124330,  179281,  234515,  344602,  400923,
              457426,  513263,  569674,  684710,  741289,  797647,  853823,
              909464, 1022891, 1080274, 1136632, 1193767, 1251758, 1490202,
             1552078],
            dtype=&#39;int64&#39;),
 1638: Int64Index([   7521,   62547,  117441,  172410,  227504,  283375,  337528,
              393886,  450500,  506476,  562643,  619851,  677810,  734292,
              790697,  846936,  902633,  959252, 1015825, 1073335, 1129747,
             1186556, 1244673, 1302216, 1360650, 1420746, 1482653, 1543941],
            dtype=&#39;int64&#39;),
 1639: Int64Index([  33820,   88123,  143017,  197939,  253538,  308738,  420560,
              476442,  532280,  589012,  646856,  703927,  760732,  816904,
              872758,  928414, 1042188, 1099621, 1155836, 1213692, 1271481,
             1328971, 1388196, 1449464, 1510800, 1574344],
            dtype=&#39;int64&#39;),
 1642: Int64Index([ 259246,  369906,  426414,  482096,  537943,  594728,  652742,
              709612,  766486,  822799,  878585,  934296,  990663, 1048019,
             1105412, 1161566, 1219719, 1277359, 1394247, 1455694, 1517156,
             1581114],
            dtype=&#39;int64&#39;),
 1644: Int64Index([  52975,  107425,  162316,  217200,  273187,  327935,  384077,
              440725,  496493,  552320,  609241,  667577,  724705,  781073,
              837117,  892670,  949121, 1005503, 1120019, 1176359, 1234425,
             1291843, 1349747, 1409474, 1471620, 1533004, 1599420],
            dtype=&#39;int64&#39;),
 1654: Int64Index([  38090,   92420,  147212,  201966,  257667,  312775,  368284,
              424787,  480568,  536337,  593144,  651134,  708052,  764914,
              821240,  877002,  932679,  989146, 1046406, 1103871, 1160010,
             1218090, 1275755, 1333207, 1392562, 1454022, 1515474, 1579288],
            dtype=&#39;int64&#39;),
 1658: Int64Index([  13304,   68231,  123192,  178162,  233350,  289017,  343454,
              399759,  456299,  512192,  568507,  625772,  683602,  740179,
              796524,  852698,  908351,  964954, 1021770, 1079181, 1135510,
             1192599, 1250580, 1308175, 1366894, 1427228, 1488983, 1550772],
            dtype=&#39;int64&#39;),
 1659: Int64Index([   6408,   61421,  116268,  171270,  226328,  282260,  336324,
              392738,  449324,  505312,  561508,  618642,  676664,  733140,
              789542,  845818,  901497,  958183, 1014678, 1072186, 1128584,
             1185413, 1243449, 1301021, 1359461, 1419473, 1481418, 1542560],
            dtype=&#39;int64&#39;),
 1662: Int64Index([ 214670,  270492,  325290,  437961,  493495,  549417,  606361,
              664620,  721722,  778030,  945987, 1002459, 1059914, 1116868,
             1173065, 1231030, 1288553, 1346394, 1406069, 1468149, 1529477,
             1595582],
            dtype=&#39;int64&#39;),
 1666: Int64Index([  40707,   94833,  149693,  204450,  260138,  315187,  370875,
              427357,  483052,  538908,  595698,  653715,  710573,  767427,
              823721,  879496,  935196,  991595, 1048989, 1106350, 1162493,
             1220723, 1278300, 1335729, 1395203, 1582205],
            dtype=&#39;int64&#39;),
 1667: Int64Index([  13795,   68735,  123709,  178679,  233889,  289512,  343971,
              400274,  456819,  512671,  569052,  626327,  684105,  740677,
              797021,  853202,  908848,  965472, 1022278, 1136001, 1193131,
             1251098, 1308672, 1367430, 1427802, 1489542, 1551357],
            dtype=&#39;int64&#39;),
 1669: Int64Index([   1983,   57104,  112018,  167091,  221936,  278089,  331872,
              388415,  444980,  501037,  557091,  614106,  672409,  728725,
              785199,  841401,  897139,  953946, 1010309, 1067882, 1124158,
             1180814, 1238898, 1296556, 1354762, 1414748, 1476640, 1537515],
            dtype=&#39;int64&#39;),
 1672: Int64Index([ 306494,  361632,  418156,  474062,  529898,  586655,  644359,
              701575,  758310,  814490,  870428,  926086,  982775, 1039910,
             1097264, 1153540, 1211302, 1269072, 1326615, 1385738, 1446843,
             1508274, 1571582],
            dtype=&#39;int64&#39;),
 1673: Int64Index([  42762,   96844,  203481,  259224,  314269,  373075,  429541,
              485147,  540985,  594714,  655894,  712865,  769530,  825864,
              881617,  934281,  993711, 1051102, 1108422, 1164604, 1222966,
             1280526, 1337883, 1397456, 1459123, 1520473, 1584618],
            dtype=&#39;int64&#39;),
 1674: Int64Index([  42197,   96340,  151171,  206006,  261744,  316671,  372531,
              428992,  484619,  540469,  597272,  655365,  712349,  769005,
              825308,  881073,  936752,  993171, 1050562, 1107897, 1164088,
             1222422, 1279989, 1326461, 1396891, 1458540, 1519896, 1584008],
            dtype=&#39;int64&#39;),
 1676: Int64Index([  38558,   92826,  147648,  202391,  258146,  313193,  368735,
              425234,  480983,  536788,  593576,  651566,  708487,  765347,
              821659,  877449,  933168,  989595, 1046889, 1104301, 1160448,
             1218551, 1276212, 1333630, 1393034, 1454488, 1515962, 1579827],
            dtype=&#39;int64&#39;),
 1678: Int64Index([  22123,   76916,  131906,  186778,  242230,  297630,  352500,
              408675,  464971,  520789,  577355,  634888,  692414,  749063,
              805291,  861445,  917023,  973655, 1030572, 1088002, 1144349,
             1201841, 1259649, 1317314, 1376090, 1436884, 1498476, 1561093],
            dtype=&#39;int64&#39;),
 1688: Int64Index([  29179,   83752,  138722,  193619,  249176,  304404,  359488,
              415907,  471956,  527732,  642101,  699448,  756103,  812367,
              923970,  980568, 1037663, 1095103, 1151294, 1209065, 1324404,
             1383476, 1444429, 1505947, 1569081],
            dtype=&#39;int64&#39;),
 1690: Int64Index([   3594,  113559,  446556,  502611,  558735,  615759, 1125790,
             1182494, 1416469, 1478408, 1539363],
            dtype=&#39;int64&#39;),
 1691: Int64Index([   7109,   62154,  117005,  172003,  227051,  282954,  337087,
              393450,  450063,  506045,  562208,  619400,  733870,  790243,
              846513,  902219,  958865, 1015404, 1072902, 1129308, 1186121,
             1244228, 1301768, 1360198, 1482182, 1543402],
            dtype=&#39;int64&#39;),
 1696: Int64Index([   3762,   58832,  113706,  168767,  223650,  279719,  333655,
              390144,  446723,  502767,  558897,  615915,  674105,  730518,
              786942,  843177,  898920,  955631, 1012031, 1069643, 1125971,
             1182674, 1240784, 1298355, 1356665, 1416649, 1478602, 1539566],
            dtype=&#39;int64&#39;),
 1700: Int64Index([  10232,   65155,  120049,  175041,  230169,  285926,  340217,
              396614,  453147,  509044,  565326,  622556,  680451,  736974,
              793408,  849562,  905267,  961844, 1076017, 1132400, 1189434,
             1247469, 1304988, 1485574, 1547112],
            dtype=&#39;int64&#39;),
 1703: Int64Index([  31528,   85979,  140950,  195801,  251343,  306630,  361783,
              418312,  474213,  530049,  586808,  644526,  701729,  758462,
              814650,  870582,  926234,  982926, 1040065, 1097414, 1153690,
             1211458, 1269231, 1326772, 1385906, 1447016, 1508446, 1571749],
            dtype=&#39;int64&#39;),
 1707: Int64Index([   6119,   61156,  116004,  170997,  226039,  281992,  336030,
              392456,  449033,  505052,  561264,  618341,  676385,  732877,
              789273,  845538,  901212,  957914, 1014386, 1071925, 1128302,
             1185129, 1243170, 1300731, 1359187, 1419180, 1481121, 1542241],
            dtype=&#39;int64&#39;),
 1709: Int64Index([   4572,   59639,  114512,  169518,  224491,  280495,  334483,
              390962,  447529,  503524,  559694,  616763,  674882,  731357,
              787730,  843974,  899728,  956409, 1012841, 1070412, 1126739,
             1183507, 1241620, 1299207, 1357524, 1417557, 1479451, 1540508],
            dtype=&#39;int64&#39;),
 1710: Int64Index([   1918,   57044,  111958,  167034,  221873,  278027,  331809,
              388339,  444915,  500976,  557033,  614038,  672341,  728663,
              785133,  841337,  897082,  953888, 1010250, 1067821, 1124101,
             1180745, 1238829, 1296492, 1354695, 1414678, 1476573, 1537441],
            dtype=&#39;int64&#39;),
 1711: Int64Index([  27513,   82160,  137112,  192018,  247509,  302843,  357857,
              414253,  470331,  526137,  582786,  640425,  697792,  754460,
              810744,  866700,  922378,  978958, 1036014, 1093422, 1149709,
             1207330, 1265082, 1322699, 1381712, 1442614, 1504158, 1567203],
            dtype=&#39;int64&#39;),
 1712: Int64Index([  19952,   74789,  129817,  184619,  240048,  295557,  350288,
              406411,  462853,  518676,  575164,  632624,  690226,  746826,
              803095,  859244,  914904,  971442, 1028302, 1085825, 1142173,
             1199488, 1257439, 1315087, 1373784, 1434435, 1496137, 1558529],
            dtype=&#39;int64&#39;),
 1721: Int64Index([  45294,   99405,  154244,  209038,  264851,  319736,  375622,
              432211,  487748,  543663,  600607,  658668,  715715,  772249,
              828564,  884122,  939942,  996438, 1053849, 1110878, 1167247,
             1225303, 1282853, 1340436, 1400057, 1461883, 1523235, 1588484],
            dtype=&#39;int64&#39;),
 1722: Int64Index([  48762,  435679,  491192,  547043,  604088,  662203,  719338,
              775711,  831876,  887465,  943442,  999932, 1057360, 1114415,
             1170668, 1228564, 1286195, 1343911, 1403606, 1465580, 1526884,
             1592734],
            dtype=&#39;int64&#39;),
 1724: Int64Index([  44803,   98856,  153695,  208532,  264327,  319216,  375128,
              431536,  487135,  542967,  599858,  657935,  714894,  771582,
              827856,  883481,  939244,  995676, 1053105, 1110371, 1285654,
             1339945, 1399542, 1461319, 1522588, 1587383],
            dtype=&#39;int64&#39;),
 1727: Int64Index([  30938,   85386,  140354,  195230,  250786,  306062,  361207,
              417699,  473626,  529418,  586215,  643882,  701144,  757841,
              814037,  869992,  925656,  982324, 1039474, 1096815, 1153074,
             1210843, 1268611, 1326168, 1385269, 1446355, 1507794, 1571068],
            dtype=&#39;int64&#39;),
 1728: Int64Index([   5532,   60572,  115422,  170412,  225437,  281392,  335433,
              391892,  448430,  504464,  560628,  617733,  675786,  732295,
              788700,  844894,  900638, 1071320, 1127653, 1184465, 1242568,
             1300166, 1358573, 1418552, 1480466, 1541563],
            dtype=&#39;int64&#39;),
 1730: Int64Index([ 280897,  617190,  675261,  731769,  788155,  844376,  900137,
              956828, 1013253, 1070802, 1127153, 1183933, 1242022, 1299630,
             1357961, 1418006, 1479892, 1540976],
            dtype=&#39;int64&#39;),
 1732: Int64Index([  31422,   85871,  140846,  195693,  251239,  306531,  361677,
              418200,  474100,  529940,  586695,  644404,  701613,  758351,
              814536,  870468,  926125,  982813, 1039950, 1097303, 1153579,
             1211338, 1269112, 1326654, 1385784, 1446887, 1508322, 1571628],
            dtype=&#39;int64&#39;),
 1733: Int64Index([  19989,   74823,  129852,  184650,  240076,  295588,  350317,
              406443,  462892,  518712,  575197,  632652,  690263,  746862,
              803127,  859279,  914937,  971473, 1028344, 1085861, 1142209,
             1199522, 1257476, 1373814, 1434470, 1496181, 1558561],
            dtype=&#39;int64&#39;),
 1735: Int64Index([  42977,   97042,  151856,  206687,  262468,  317386,  373271,
              429724,  485326,  541159,  598027,  656088,  713037,  769703,
              826051,  881770,  937490,  993882, 1051264, 1108598, 1164806,
             1223154, 1280723, 1338069, 1397630, 1459331, 1520669, 1584841],
            dtype=&#39;int64&#39;),
 1736: Int64Index([  26453,   81153,  136075,  190973,  246498,  301832,  356799,
              413140,  469242,  525068,  581717,  639321,  696732,  753398,
              809636,  865663,  921327,  977968, 1034988, 1092327, 1148629,
             1206253, 1264007, 1321638, 1380587, 1441466, 1503059, 1566005],
            dtype=&#39;int64&#39;),
 1738: Int64Index([  39133,   93396,  148194,  202953,  258700,  313738,  369347,
              425832,  481558,  537361,  594153,  652164,  709061,  765918,
              822221,  878020,  933738,  990120, 1047469, 1104847, 1160994,
             1219118, 1276762, 1334215, 1393647, 1455089, 1516560, 1580480],
            dtype=&#39;int64&#39;),
 1743: Int64Index([  37155,   91477,  146297,  201096,  256753,  311914,  367345,
              423848,  479621,  535442,  592231,  650212,  707147,  764007,
              820309,  876090,  931735,  988234, 1045486, 1102947, 1159080,
             1217137, 1274814, 1332292, 1391641, 1453062, 1514490, 1578235],
            dtype=&#39;int64&#39;),
 1747: Int64Index([  71549,  126548,  181456,  236760,  292345,  346922,  403153,
              459601,  515454,  571815,  629259,  686894,  743505,  799808,
              855975,  911611,  968181, 1071196, 1138850, 1196020, 1254066,
             1311611, 1370247, 1430833, 1492569, 1554681],
            dtype=&#39;int64&#39;),
 1748: Int64Index([  42316,   96449,  151281,  206111,  261841,  316776,  372638,
              429108,  484734,  540581,  597381,  655470,  712465,  769110,
              825431,  881184,  936855,  993286, 1050675, 1108019, 1164198,
             1222531, 1280107, 1337478, 1397006, 1458644, 1520013, 1584123],
            dtype=&#39;int64&#39;),
 1764: Int64Index([   1369,   56509,  111412,  166528,  221337,  277495,  331289,
              387788,  444392,  500467,  556490,  613485,  671803,  728119,
              784574,  840806,  896554,  953359, 1009730, 1067281, 1123588,
             1180206, 1238269, 1295922, 1354160, 1414109, 1476015, 1536863],
            dtype=&#39;int64&#39;),
 1768: Int64Index([  30349,  139821,  194694,  250258,  305483,  360650,  417056,
              473071,  528861,  585599,  643296,  700555,  757229,  813441,
              869399,  925059,  981722, 1038880, 1096209, 1152473, 1210238,
             1267978, 1325545, 1384673, 1445729, 1507172, 1570397],
            dtype=&#39;int64&#39;),
 1770: Int64Index([  32778,   87154,  142065,  197001,  252572,  307781,  363025,
              419516,  475417,  531284,  587991,  645816,  702930,  759677,
              815849,  871730,  927427,  984108, 1041281, 1098615, 1154837,
             1212719, 1270442, 1327955, 1387169, 1448390, 1509731, 1573187],
            dtype=&#39;int64&#39;),
 1771: Int64Index([1174420, 1232400, 1289864, 1347730, 1407437, 1469594, 1530977,
             1597182],
            dtype=&#39;int64&#39;),
 1775: Int64Index([  50556,  104840,  270267,  493214,  664328,  706572,  777750,
              833889,  945690, 1059571, 1116546, 1230709, 1346095, 1405740,
             1529131, 1595230],
            dtype=&#39;int64&#39;),
 1779: Int64Index([  33294,   87647,  142530,  197470,  253062,  308258,  363553,
              420051,  475918,  515432,  588493,  646336,  703422,  760200,
              816356,  872244,  927899,  984583, 1041749, 1099134, 1155326,
             1213213, 1270958, 1328456, 1387650, 1448930, 1510264, 1573785],
            dtype=&#39;int64&#39;),
 1780: Int64Index([ 439807,  495547,  551366,  608333,  666677,  723786,  780161,
              836237,  891790,  948160, 1004563, 1062123, 1119049, 1168932,
             1226973, 1284506, 1342168, 1408395, 1463717, 1524986, 1590403],
            dtype=&#39;int64&#39;),
 1783: Int64Index([  22850,   77639,  132621,  187526,  242980,  298381,  353263,
              409428,  465664,  521509,  578122,  635681,  693190,  806073,
              862190,  917769,  974394, 1031333, 1088755, 1145067, 1202618,
             1260402, 1318053, 1376829, 1561929],
            dtype=&#39;int64&#39;),
 1785: Int64Index([  35867,   90200,  145011,  199856,  255489,  310633,  366033,
              422567,  478424,  534201,  590990,  648908,  705916,  762738,
              819007,  874767,  930436,  986985, 1044176, 1101615, 1157755,
             1215765, 1273530, 1331014, 1390276, 1451675, 1513009, 1576704],
            dtype=&#39;int64&#39;),
 1787: Int64Index([876585, 932249, 1103462, 1159597, 1392159, 1578839], dtype=&#39;int64&#39;),
 1790: Int64Index([  24041,   78778,  133771,  188648,  244131,  299506,  354378,
              410632,  466799,  522664,  579278,  636831,  694290,  750991,
              807244,  863325,  918908,  975533, 1032465, 1089901, 1146197,
             1203804, 1261593, 1319221, 1378040, 1438865, 1500500, 1563229],
            dtype=&#39;int64&#39;),
 1798: Int64Index([  97738,  152537,  215239,  267232,  318050,  378062,  438615,
              494273,  550099,  607075,  665370,  722451,  778781,  834920,
              890448, 1003187, 1060699, 1117622, 1173879, 1231861, 1289333,
             1347172, 1530375, 1596536],
            dtype=&#39;int64&#39;),
 1804: Int64Index([  29750,   84296,  139266,  194121,  249687,  304925,  360051,
              416478,  472500,  528292,  585013,  642676,  699975,  756646,
              812885,  868841,  924501,  981147, 1038234, 1095651, 1151878,
             1209649, 1267409, 1324962, 1384074, 1445074, 1506548, 1569726],
            dtype=&#39;int64&#39;),
 1806: Int64Index([  38150,   92465,  147271,  202015,  257729,  312836,  368337,
              424845,  480622,  536389,  593197,  651183,  708109,  764969,
              821296,  877056,  932749,  989203, 1046476, 1103934, 1160076,
             1218140, 1275814, 1333272, 1392615, 1454089, 1515535, 1579369],
            dtype=&#39;int64&#39;),
 1807: Int64Index([  41988,   96140,  150961,  205792,  261539,  316474,  372312,
              428770,  484416,  540247,  597061,  655156,  711904,  768798,
              825083,  880843,  936532,  992973, 1050357, 1107664, 1163852,
             1222196, 1279751, 1337131, 1396652, 1458285, 1519665, 1583769],
            dtype=&#39;int64&#39;),
 1813: Int64Index([  29496,   84045,  139023,  193905,  249443,  304669,  359784,
              416204,  472230,  528020,  584716,  642418,  699731,  756384,
              812641,  868602,  924234,  980888, 1037941, 1095381, 1151610,
             1209382, 1267134, 1324716, 1383790, 1444756, 1506274, 1569409],
            dtype=&#39;int64&#39;),
 1814: Int64Index([   2497,   57594,  112485,  167575,  222421,  278534,  332392,
              388905,  445475,  501524,  557654,  614660,  672900,  729252,
              785719,  841888,  897661,  954450, 1010830, 1068388, 1124685,
             1181341, 1239448, 1297080, 1355305, 1415292, 1477197, 1538112],
            dtype=&#39;int64&#39;),
 1817: Int64Index([  47850,   85405,  140382,  195252,  250805,  306080,  361224,
              417718,  473649,  529441,  586238,  643907,  701163,  757860,
              814060,  870009,  925674,  982341, 1039492, 1096835, 1153093,
             1210863, 1268634, 1326189, 1385288, 1446375, 1507817, 1571099],
            dtype=&#39;int64&#39;),
 1818: Int64Index([  41711,   95871,  205533,  261281,  316219,  372018,  428493,
              484133,  539995,  596791,  654843,  711626,  768517,  824812,
              880563,  936256,  992699, 1050080, 1163542, 1221884, 1279398,
             1336831, 1396343, 1457949, 1519328, 1583415],
            dtype=&#39;int64&#39;),
 1820: Int64Index([   1467,   56604,  111517,  166619,  221429,  277588,  331376,
              387883,  444477,  500559,  556581,  613581,  671887,  728210,
              784673,  840893,  896644,  953445, 1009819, 1067367, 1123681,
             1180303, 1238371, 1296016, 1354249, 1414197, 1476106, 1536957],
            dtype=&#39;int64&#39;),
 1829: Int64Index([ 341753,  566847,  681986, 1133884, 1248959, 1306556, 1365190,
             1425449, 1487193, 1548861],
            dtype=&#39;int64&#39;),
 1830: Int64Index([  10450,   65358,  120271,  175242,  230394,  286130,  340425,
              396837,  453351,  509237,  565533,  622763,  680657,  737185,
              793607,  849773,  905466,  962044, 1018764, 1076223, 1132601,
             1189627, 1247666, 1305211, 1363836, 1424024, 1485795, 1547362],
            dtype=&#39;int64&#39;),
 1833: Int64Index([  19803,   74659,  129676,  184489,  239913,  295421,  350161,
              406294,  462723,  518546,  575039,  632493,  690078,  746693,
              802956,  859117,  914775,  971314, 1028167, 1085682, 1142040,
             1199359, 1257293, 1314950, 1373650, 1434297, 1495986, 1558381],
            dtype=&#39;int64&#39;),
 1834: Int64Index([   5232,   60283,  115142,  170132,  225148,  281136,  335143,
              391614,  448143,  504183,  560336,  617445,  675492,  732008,
              788397,  844597,  900352,  957035, 1013481, 1071041, 1127375,
             1184172, 1242271, 1299881, 1358244, 1418243, 1480154, 1541249],
            dtype=&#39;int64&#39;),
 1836: Int64Index([  32643,   87020,  141933,  196882,  252413,  307641,  362874,
              419372,  475270,  531128,  587849,  645657,  702766,  759518,
              815704,  871587,  927277,  983960, 1041123, 1098468, 1154699,
             1212566, 1270284, 1327795, 1387012, 1448213, 1509565, 1572981],
            dtype=&#39;int64&#39;),
 1838: Int64Index([  28535,   83129,  138075,  192971,  248517,  303807,  358853,
              415277,  471310,  527083,  583772,  641414,  698781,  755452,
              811721,  867710,  923306,  979942, 1036991, 1094437, 1150697,
             1208387, 1266138, 1323765, 1382794, 1443708, 1505261, 1568364],
            dtype=&#39;int64&#39;),
 1840: Int64Index([  23995,   78732,  133720,  188596,  244087,  299466,  354338,
              410589,  466759,  522616,  579233,  636790,  694245,  750949,
              807193,  863276,  918859,  975492, 1032423, 1089855, 1146148,
             1203750, 1261542, 1319177, 1377995, 1438821, 1500455, 1563181],
            dtype=&#39;int64&#39;),
 1843: Int64Index([  33395,   87733,  142629,  197563,  253166,  308357,  363648,
              420147,  476022,  531870,  588588,  646433,  703514,  760305,
              816463,  872346,  927996,  984673, 1041832, 1099236, 1155430,
             1213311, 1271058, 1328563, 1387759, 1449027, 1510372, 1573900],
            dtype=&#39;int64&#39;),
 1849: Int64Index([  29044,   83604,  138557,  193474,  249024,  304270,  359335,
              415749,  471797,  527582,  584286,  641939,  699302,  755957,
              812223,  868177,  923814,  980406, 1037505, 1094955, 1151160,
             1208908, 1266668, 1324253, 1383318, 1444255, 1505788, 1568932],
            dtype=&#39;int64&#39;),
 1853: Int64Index([  31056,   85490,  140471,  195343,  250909,  306186,  361316,
              417830,  473753,  529531,  586338,  644017,  701259,  757963,
              814152,  870110,  925770,  982441, 1039595, 1096941, 1153186,
             1210968, 1268752, 1326296, 1385402, 1446487, 1507934, 1571208],
            dtype=&#39;int64&#39;),
 1855: Int64Index([  77937,  132902,  187832,  243285,  298687,  353565,  409759,
              465967,  521811,  578461,  635990,  693487,  750146,  806368,
              862487,  918071,  974698, 1031644, 1089047, 1145358, 1202926,
             1260724, 1318356, 1377150, 1437998, 1499608, 1562271],
            dtype=&#39;int64&#39;),
 1858: Int64Index([  48817,  102995,  157762,  212555,  268393,  323188,  379158,
              435730,  491263,  544068,  604148,  662261,  719405,  775769,
              831934,  887517,  943503,  999988, 1114467, 1170723, 1228625,
             1286255, 1343968, 1403659, 1465630, 1526939, 1592798],
            dtype=&#39;int64&#39;),
 1860: Int64Index([  10008,   83797,  138767,  193663,  249220,  304444,  359537,
              415948,  452955,  527785,  584483,  642165,  699501,  756151,
              812412,  849371,  924010,  980625, 1037699, 1095146, 1132196,
             1209118, 1266876, 1304764, 1383534, 1444489, 1506009, 1569146],
            dtype=&#39;int64&#39;),
 1862: Int64Index([  21999,   76783,  131782,  186647,  242096,  297495,  352371,
              408528,  464829,  520655,  577214,  634749,  692292,  748927,
              805165,  861321,  916894,  973536, 1030461, 1087874, 1144220,
             1201704, 1259523, 1317188, 1375949, 1436753, 1498350, 1560935],
            dtype=&#39;int64&#39;),
 1863: Int64Index([  18137,   73026,  128024,  182880,  238259,  293821,  348473,
              404635,  461092,  516917,  573362,  630814,  688436,  745039,
              801288,  857469,  913110,  969692, 1026525, 1084020, 1140364,
             1197640, 1255580, 1313235, 1371845, 1432492, 1494177, 1556403],
            dtype=&#39;int64&#39;),
 1864: Int64Index([   1029,   56172,  111078,  166207,  221003,  277173,  330936,
              387420,  444043,  500112,  556104,  613071,  671389,  727718,
              784197,  840434,  896187,  952999, 1009368, 1066919, 1123218,
             1179838, 1237903, 1295561, 1353770, 1413702, 1475573, 1536408],
            dtype=&#39;int64&#39;),
 1872: Int64Index([ 119515,  279791,  333728,  390222,  446793,  615995,  674175,
              730599,  787023, 1478679, 1539651],
            dtype=&#39;int64&#39;),
 1874: Int64Index([  20397,  350783,  575616,  859704,  971912, 1028791, 1086284,
             1142638, 1199974, 1257902, 1374260, 1496640, 1559048],
            dtype=&#39;int64&#39;),
 1876: Int64Index([  32040,   86448,  141416,  196281,  251830,  307092,  362277,
              418791,  474677,  530547,  587282,  645044,  702229,  758938,
              815136,  871052,  926727,  983403, 1040555, 1097905, 1154153,
             1211983, 1269718, 1327257, 1386410, 1447550, 1508961, 1572332],
            dtype=&#39;int64&#39;),
 1877: Int64Index([   3037,   58104,  113002,  168095,  222933,  279028,  332934,
              389433,  446028,  502053,  558192,  615189,  673405,  729783,
              786229,  842446,  898182,  954923, 1011306, 1068907, 1125222,
             1181867, 1239994, 1297587, 1355861, 1415823, 1477792, 1538707],
            dtype=&#39;int64&#39;),
 1879: Int64Index([   1615,   56739,  111657,  166741,  221574,  277726,  331510,
              388031,  444614,  500694,  556726,  613727,  672015,  728352,
              784812,  841041,  896779,  953586, 1009954, 1067521, 1123815,
             1180447, 1238513, 1296159, 1354394, 1414347, 1476251, 1537115],
            dtype=&#39;int64&#39;),
 1880: Int64Index([  47004,  101185,  155960,  210799,  266615,  321469,  377509,
              434010,  489563,  545437,  602420,  660468,  717466,  773983,
              830254,  885872,  941731,  998204, 1055587, 1112686, 1169052,
             1227078, 1284639, 1342297, 1401871, 1463847, 1525119, 1590575],
            dtype=&#39;int64&#39;),
 1884: Int64Index([  35914,   90245,  145060,  199897,  255534,  310684,  366082,
              422617,  478470,  534249,  591038,  648956,  705967,  762796,
              819058,  874819,  930486,  987034, 1044224, 1101659, 1157806,
             1215816, 1273581, 1331067, 1390322, 1451735, 1513064, 1576760],
            dtype=&#39;int64&#39;),
 1886: Int64Index([  22101,   76896,  131886,  186760,  242211,  297610,  352483,
              408654,  464949,  520763,  577336,  634866,  692396,  749047,
              805268,  861425,  917004,  973642, 1030554, 1087984, 1144324,
             1201818, 1259630, 1317297, 1376068, 1436871, 1498458, 1561066],
            dtype=&#39;int64&#39;),
 1887: Int64Index([  24135,   78863,  133868,  188749,  244217,  299606,  354473,
              410722,  466890,  522755,  579368,  636924,  694381,  863409,
              918997, 1032558, 1261687, 1500608, 1563324],
            dtype=&#39;int64&#39;),
 1893: Int64Index([ 106279,  215924,  271834,  326628,  382727,  439399,  495095,
              550909,  607884,  666211,  723309,  779661,  835794,  891328,
              947653, 1061620, 1118547, 1232813, 1290267, 1348159, 1407843,
             1597659],
            dtype=&#39;int64&#39;),
 1897: Int64Index([   9679,   64626,  119498,  174511,  229633,  285409,  339660,
              396076,  452611,  508527,  564750,  622011,  679916,  736425,
              792878,  849035,  904753,  961328, 1017974, 1075503, 1131866,
             1188860, 1246916, 1304434, 1363018, 1423126, 1484977, 1546474],
            dtype=&#39;int64&#39;),
 1899: Int64Index([  30367,   84878,  139836,  194713,  250274,  305496,  360669,
              417072,  473094,  528875,  585610,  643315,  700573, 1267994,
             1325567, 1384691, 1445747, 1507189, 1570411],
            dtype=&#39;int64&#39;),
 1903: Int64Index([   5986,   61025,  115868,  170865,  225876,  281861,  335898,
              392333,  448899,  504929,  561114,  618195,  676235,  732752,
              789142,  845401,  901088,  957781, 1014248, 1071791, 1128161,
             1184974, 1243055, 1300610, 1359041, 1419029, 1480975, 1542082],
            dtype=&#39;int64&#39;),
 1905: Int64Index([   3205,   58291,  168252,  223094,  279195,  333089,  389616,
              446175,  502209,  558362,  615369,  673556,  729962,  786377,
              842621,  898354,  955096, 1011496, 1069058, 1125395, 1182056,
             1240177, 1297772, 1356028, 1416004, 1477979, 1538893],
            dtype=&#39;int64&#39;),
 1912: Int64Index([   2916,   57997,  112885,  167990,  222832,  278915,  332829,
              389301,  445930,  501946,  558079,  615093,  673297,  729678,
              786128,  842320,  898066,  954819, 1011206, 1068805, 1125112,
             1181754, 1239885, 1297480, 1355742, 1415710, 1477666, 1538573],
            dtype=&#39;int64&#39;),
 1913: Int64Index([  13786,   68725,  123697,  178665,  233872,  289504,  343963,
              400266,  456809,  512664,  569039,  626314,  684095,  740671,
              797007,  853193,  908841,  965465, 1022270, 1079653, 1123595,
             1193119, 1251090, 1308665, 1367421, 1427787, 1489527, 1551338],
            dtype=&#39;int64&#39;),
 1916: Int64Index([  34793,   89115,  143934,  254424,  309624,  364940,  421482,
              477382,  533185,  589949,  647819,  704861,  761680,  817904,
              873689,  929349,  985932, 1043131, 1100564, 1156717, 1214695,
             1272437, 1329921, 1389217, 1450498, 1511804, 1575443],
            dtype=&#39;int64&#39;),
 1919: Int64Index([  14883,   69776,  124771,  179736,  234974,  290585,  345088,
              401359,  457862,  513719,  570136,  627422,  685137,  741723,
              798080,  854259,  909909, 1080741, 1137107, 1194233, 1252242,
             1309803, 1368531, 1428930, 1490693, 1552599],
            dtype=&#39;int64&#39;),
 1920: Int64Index([  15272,   70167,  125142,  290956,  345473,  401716,  458215,
              514096,  570503,  627798,  685492,  742112,  798431,  854601,
              910261,  966867, 1023677, 1081099, 1137450, 1194611, 1252608,
             1310187, 1368876, 1429342, 1491085, 1553040],
            dtype=&#39;int64&#39;),
 1929: Int64Index([  29380,   83929,  138889,  193787,  249336,  304554,  359669,
              416081,  472118,  527906,  584610,  642299,  699617,  756270,
              812530,  868481,  924121,  980759, 1037836, 1095268, 1151478,
             1209247, 1267006, 1324588, 1383658, 1444624, 1506137, 1569270],
            dtype=&#39;int64&#39;),
 1930: Int64Index([   6756,   61785,  116640,  171635,  226687,  336713,  393105,
              449692,  505705,  619027,  677023,  733492,  789895,  846171,
              958517, 1072544, 1128953, 1419875, 1542985],
            dtype=&#39;int64&#39;),
 1934: Int64Index([  27821,   82453,  137413,  192308,  247799,  358152,  414580,
              470645,  526413,  583074,  640724,  698072,  754759,  811018,
              866983,  922644,  979250, 1036300, 1093722, 1150004, 1207620,
             1265381, 1323014, 1382048, 1442930, 1504481, 1567556],
            dtype=&#39;int64&#39;),
 1935: Int64Index([ 496044,  551853,  780642,  836682,  892251,  948702, 1005093,
             1119584, 1175908, 1233954, 1287112, 1339987, 1408964, 1461373,
             1527905, 1598893],
            dtype=&#39;int64&#39;),
 1937: Int64Index([  41766,   95929,  150757,  205582,  261334,  316280,  372078,
              428560,  484191,  540048,  596856,  654926,  711684,  768580,
              824864,  880622,  936320,  992756, 1050143, 1107437, 1163603,
             1221952, 1279464, 1336904, 1396415, 1458029, 1519418, 1583505],
            dtype=&#39;int64&#39;),
 1938: Int64Index([  47773,  101930,  156684,  211526,  267324,  322164,  378148,
              434685,  491554,  546107,  604448,  661211,  719709,  774777,
              835349, 1057725, 1118070, 1171032, 1227707, 1285271, 1342964,
             1402580, 1465954, 1525833, 1591590],
            dtype=&#39;int64&#39;),
 1939: Int64Index([  33554,   87873,  142765,  197682,  308485,  363775,  420282,
              476169,  532004,  588721,  646566,  703654,  760446,  816608,
              872479,  928127, 1099358, 1155569, 1213433, 1271190, 1328699,
             1387909, 1449177, 1510518, 1574059],
            dtype=&#39;int64&#39;),
 1940: Int64Index([  31817,   86250,  141205,  196068,  251625,  306879,  362066,
              418571,  474464,  530335,  587071,  644798,  702009,  758732,
              814926,  870840,  926506,  983205, 1040336, 1097698, 1153930,
             1211762, 1269511, 1327052, 1386205, 1447316, 1508732, 1572081],
            dtype=&#39;int64&#39;),
 1942: Int64Index([  13113,   59144,  110272,  173039,  240217,  295721,  330034,
              392273,  443191,  504869,  555204,  632817,  726905,  789083,
              841523,  915086,  971629, 1028501, 1086017, 1126267, 1182969,
             1253269, 1315281, 1352883, 1434617, 1474662, 1558716],
            dtype=&#39;int64&#39;),
 1943: Int64Index([   3159,   58228,  113112,  168203,  223045,  279149,  333044,
              389562,  446128,  502162,  558314,  615317,  673505,  729909,
              786329,  842566,  898300,  955042, 1011447, 1069015, 1125347,
             1182006, 1240126, 1297722, 1355974, 1415945, 1477923, 1538851],
            dtype=&#39;int64&#39;),
 1945: Int64Index([  34798,   89120,  143939,  198825,  254432,  421492,  477387,
              647824,  704867,  761690,  817912,  873696,  985938, 1100573,
             1156724, 1214702, 1272443, 1329925, 1511814, 1575454],
            dtype=&#39;int64&#39;),
 1949: Int64Index([  23632,   78386,  133393,  188261,  243747,  299131,  353997,
              410229,  466402,  522255,  578884,  636427,  693912,  750593,
              806810,  862926,  918524,  975136, 1032064, 1089497, 1145791,
             1203387, 1261170, 1318813, 1377599, 1438441, 1500071, 1562763],
            dtype=&#39;int64&#39;),
 1950: Int64Index([ 568475,  683575,  740152,  796490,  908324,  964924, 1014466,
             1071997, 1128376, 1185200, 1243238, 1300796, 1359264, 1419261,
             1481196, 1542331],
            dtype=&#39;int64&#39;),
 1952: Int64Index([  32931,   87294,  142200,  197150,  252710,  307913,  363183,
              419685,  475561,  531428,  588129,  645979,  703082,  815995,
              871865,  927554,  984253, 1041429, 1098769, 1154988, 1270597,
             1387314, 1448551, 1509892, 1573366],
            dtype=&#39;int64&#39;),
 1953: Int64Index([1432677, 1556628], dtype=&#39;int64&#39;),
 1954: Int64Index([  19708,   74569,  129583,  184391,  239815,  295321,  350061,
              406204,  462628,  518459,  574938,  632400,  689983,  746597,
              802851,  859017,  914676,  971216, 1028064, 1085581, 1141938,
             1199254, 1257190, 1314847, 1373554, 1434185, 1495885, 1558271],
            dtype=&#39;int64&#39;),
 1968: Int64Index([ 665561,  722644,  778981,  835134,  890658,  946950, 1174107,
             1232088, 1289561, 1347413, 1469230, 1596795],
            dtype=&#39;int64&#39;),
 1970: Int64Index([  51474,  105819,  160609,  215391,  271280,  326084,  382100,
              438792,  494461,  550274,  607271,  665567,  722650,  778989,
              835142,  890665,  946956, 1003397, 1060925, 1117859, 1174111,
             1232092, 1289566, 1347419, 1407106, 1469239, 1530637, 1596804],
            dtype=&#39;int64&#39;),
 1972: Int64Index([ 325069,  381025,  549157,  606102,  664338,  777761,  833899,
              889426, 1002187, 1059582, 1108600, 1172783, 1230725, 1288251,
             1405756, 1467852, 1595244],
            dtype=&#39;int64&#39;),
 1974: Int64Index([ 495173,  550993,  607972,  666300,  723398,  779754,  835882,
              891420,  947748, 1004171, 1061717, 1118638, 1174927, 1232920,
             1290365, 1348262, 1407946, 1470137, 1531506, 1597792],
            dtype=&#39;int64&#39;),
 1975: Int64Index([  20661,   75522,  130527,  185355,  240780,  296209,  351040,
              407143,  463523,  519363,  575884,  633373,  690935,  747560,
              803806,  859987,  915584,  972183, 1029080, 1086531, 1142901,
             1200281, 1258154, 1315842, 1374529, 1435249, 1496955, 1559369],
            dtype=&#39;int64&#39;),
 1976: Int64Index([ 100394,  155163,  320667,  433231,  494286,  607086,  722461,
              778794,  834933,  890462,  946763, 1003205, 1060716, 1117638,
             1173900, 1231880, 1347189, 1406876, 1469004, 1530396, 1596558],
            dtype=&#39;int64&#39;),
 1977: Int64Index([1071467, 1127784, 1184606, 1242712, 1300298, 1358709, 1418690,
             1480612, 1541717],
            dtype=&#39;int64&#39;),
 1986: Int64Index([  24711,   79476,  134407,  189334,  244808,  300182,  355070,
              411338,  467518,  523356,  579989,  637523,  694970,  751676,
              807891,  863962,  919595,  976232, 1033175, 1090590, 1146873,
             1204521, 1262298, 1319917, 1378790, 1439634, 1501244, 1564026],
            dtype=&#39;int64&#39;),
 1990: Int64Index([  39618,   93868,  148674,  203414,  259167,  314218,  369827,
              426322,  482025,  537863,  594647,  652665,  709530,  766399,
              822707,  878497,  934210,  990590, 1047932, 1105328, 1161474,
             1219626, 1277270, 1334717, 1394162, 1455602, 1517068, 1581027],
            dtype=&#39;int64&#39;),
 1991: Int64Index([ 110169,  165267,  220089,  276264,  329912,  386437,  443072,
              499147,  555085,  612045,  670431,  726792,  783255,  839498,
              895226,  952000, 1008385, 1065928, 1122224, 1178813, 1236860,
             1294552, 1352755, 1412647, 1474553, 1535295],
            dtype=&#39;int64&#39;),
 1996: Int64Index([1404770, 1461729, 1523079, 1592430], dtype=&#39;int64&#39;),
 1998: Int64Index([  42469,   96577,  151414,  206245,  261977,  316918,  372783,
              429255,  484865,  540719,  597515,  655604,  712603,  769253,
              825586,  881333,  937001, 1108159, 1164331, 1222675, 1280254,
             1337620, 1397155, 1458786, 1520152, 1584267],
            dtype=&#39;int64&#39;),
 1999: Int64Index([  79255,  134210,  189106,  244586,  299974,  354851,  411132,
              467292,  523136,  579773,  637304,  694773,  751469,  807696,
              863759,  976008, 1032946, 1090379, 1146646, 1204284, 1262066,
             1319689, 1439377, 1501014, 1563780],
            dtype=&#39;int64&#39;),
 2000: Int64Index([ 135952,  419226,  475132,  530976,  587705,  645499,  702629,
              759373,  815566,  871453,  927140,  983813, 1040977, 1098328,
             1154571, 1270145, 1327648, 1386852, 1448039, 1509410, 1572821],
            dtype=&#39;int64&#39;),
 2005: Int64Index([  87166,  142075,  363038,  419531,  531302,  588004,  645833,
              759691,  871741,  927437,  984121, 1041292, 1098625, 1154850,
             1212729, 1270455, 1327965, 1387181, 1448405, 1573202],
            dtype=&#39;int64&#39;),
 2013: Int64Index([  17449,   72361,  127335,  182256,  237597,  293147,  347760,
              572659,  630128, 1025863, 1083324, 1196911, 1312534, 1431754,
             1555643],
            dtype=&#39;int64&#39;),
 2014: Int64Index([ 126142,  628810,  686490,  743064,  799389,  855571,  911191,
              967767, 1024634, 1082076, 1138429, 1195605, 1253630, 1554190],
            dtype=&#39;int64&#39;),
 2016: Int64Index([  21297,   76129,  131128,  185986,  241442,  296866,  351691,
              407834,  464124,  519984,  576533,  613472,  677607,  748218,
              804489,  860632,  911505,  972839, 1024942, 1071003, 1127345,
             1184139, 1242231, 1299845, 1375217, 1426382, 1488108, 1549875],
            dtype=&#39;int64&#39;),
 2017: Int64Index([  41354,   95502,  205163,  260884,  315854,  371618,  428109,
              483744,  539592,  596379,  654445,  711262,  768116,  824435,
              880185,  992312, 1049687, 1107010, 1163162, 1221478, 1279001,
             1336426, 1395916, 1457494, 1518911, 1582984],
            dtype=&#39;int64&#39;),
 2020: Int64Index([  25619,   80348,  135245,  245666,  301018,  355930,  412246,
              468388,  580883,  695864,  752556,  808791,  864830,  920513,
              977112, 1091470, 1205401, 1263193, 1320798, 1440550, 1502174,
             1565038],
            dtype=&#39;int64&#39;),
 2022: Int64Index([ 138976,  193855,  304634,  359747,  416163,  472192,  584671,
              642374,  699690,  756342,  980840, 1095343, 1151560, 1209334,
             1267092, 1324676, 1383745, 1444703, 1506228, 1569366],
            dtype=&#39;int64&#39;),
 2023: Int64Index([   3780,   58849,  113722,  168782,  333673,  390160,  446738,
              502784,  558914,  615933,  674121,  730533,  786960,  843197,
              898936,  955645, 1012045, 1069657, 1125986, 1182688, 1240802,
             1298376, 1356686, 1416669, 1478621, 1539587],
            dtype=&#39;int64&#39;),
 2025: Int64Index([1389601, 1450910, 1512282, 1575917], dtype=&#39;int64&#39;),
 2026: Int64Index([57671, 167648, 332467, 501604, 557715, 614733, 897734, 954511,
             1477275, 1538193],
            dtype=&#39;int64&#39;),
 2027: Int64Index([  25445,   80181,  135077,  190001,  245501,  300846,  355754,
              412075,  468219,  524047,  580709,  638277,  695698,  752386,
              808622,  864662,  920336,  976948, 1033949, 1091298, 1147582,
             1263027, 1320634, 1379541, 1440376, 1501994, 1564852],
            dtype=&#39;int64&#39;),
 2034: Int64Index([  35415,   89700,  144542,  199388,  255011,  310203,  365580,
              422114,  533766,  590556,  648430,  705465,  762274,  818531,
              874311,  929966, 1043728, 1101142, 1152676, 1273060, 1330536,
             1389807, 1451167, 1576167],
            dtype=&#39;int64&#39;),
 2036: Int64Index([15965, 247304, 302641, 414022, 470126, 1322513, 1381490, 1503954,
             1566967],
            dtype=&#39;int64&#39;),
 2042: Int64Index([  34728,   89048,  143883,  198754,  309565,  364886,  589894,
              647763,  704809,  761630,  929303, 1043076, 1156666, 1272385,
             1389160, 1450433, 1511747, 1575382],
            dtype=&#39;int64&#39;),
 2043: Int64Index([  22931,  749918,  806167,  862285,  917872,  974493, 1088840,
             1145160, 1260503, 1318150, 1376926, 1437787, 1499374, 1562035],
            dtype=&#39;int64&#39;),
 2045: Int64Index([614721, 1010885, 1124738, 1239511, 1355358, 1415345, 1477260,
             1538179],
            dtype=&#39;int64&#39;),
 2058: Int64Index([  50697,  104980,  159789,  214570,  270402,  325191,  381173,
              437849,  493378,  549312,  606253,  664496,  721601,  777916,
              834056,  889582,  945852, 1002330, 1059760, 1116735, 1172945,
             1230894, 1288424, 1346274, 1405931, 1468029, 1529329, 1595436],
            dtype=&#39;int64&#39;),
 2062: Int64Index([  40161,   94331,  149166,  203916,  259621,  314653,  370342,
              426802,  482524,  538384,  595162,  653181,  710040,  766897,
              823191,  878973,  934680,  991062, 1048433, 1105813, 1161957,
             1220174, 1277775, 1335205, 1394665, 1456162, 1517605, 1581589],
            dtype=&#39;int64&#39;),
 2068: Int64Index([  46106,  100236,  152391,  207220,  263000,  317907,  373804,
              430270,  485827,  541626,  598556,  656595,  713536,  770208,
              826559,  884904,  940742,  997224, 1054640, 1109110, 1165324,
             1223635, 1281217, 1338587, 1398168, 1459881, 1521201, 1585446],
            dtype=&#39;int64&#39;),
 2069: Int64Index([121085, 1133396, 1364666, 1548293], dtype=&#39;int64&#39;),
 2075: Int64Index([  20552,   75419,  130428,  185263,  240674,  296115,  350946,
              407046,  463443,  519272,  575788,  633260,  690840,  747474,
              803716,  859885,  915499,  972087, 1028978, 1086443, 1142801,
             1200171, 1258066, 1315744, 1374436, 1435125, 1496849, 1559269],
            dtype=&#39;int64&#39;),
 2079: Int64Index([  30265,   84796,  139738,  250192,  305413,  416983,  473004,
              585524,  643228,  700473,  757150,  813373,  869324,  924981,
              981646, 1096132, 1152398, 1325479, 1384589, 1507104, 1570285],
            dtype=&#39;int64&#39;),
 2081: Int64Index([  15701,   70607,  125581,  180471,  235759,  291379,  345908,
              402171,  458665,  514511,  570887,  628247,  685945,  742532,
              798862,  855040,  910681,  967265, 1024108, 1081550, 1137917,
             1195064, 1253060, 1310649, 1369276, 1429804, 1491531, 1553569],
            dtype=&#39;int64&#39;),
 2092: Int64Index([ 600146,  668324,  725511,  781783,  837809,  893370,  949914,
             1006281, 1048933, 1106291, 1162442, 1220669, 1278247, 1335679,
             1518095, 1582141],
            dtype=&#39;int64&#39;),
 2094: Int64Index([ 106782,  158521,  216456,  272406,  327162,  383294,  439944,
              495685,  551502,  608475,  666814,  723918,  780296,  836371,
              891922,  948312, 1004709, 1062270, 1119210, 1175501, 1233533,
             1290947, 1348859, 1408551, 1470758, 1532122, 1598465],
            dtype=&#39;int64&#39;),
 2098: Int64Index([  46115,  103153,  157900,  209845,  268544,  323323,  379295,
              435872,  491393,  547246,  604284,  662388,  719550,  775905,
              832069,  887650,  943641, 1000144, 1057556, 1114616, 1170862,
             1228762, 1286393, 1344108, 1403809, 1465775, 1527084, 1592954],
            dtype=&#39;int64&#39;),
 2103: Int64Index([  22907,   77695,  132675,  187588,  243052,  298445,  353320,
              409492,  465727,  521571,  578190,  635745,  693246,  749891,
              806139,  862255,  917836,  974460, 1031399, 1088814, 1145130,
             1202683, 1260470, 1318118, 1376904, 1437753, 1499343, 1562003],
            dtype=&#39;int64&#39;),
 2104: Int64Index([  12875,   67805,  122778,  177732,  232932,  288616,  343019,
              399339,  455858,  511762,  568066,  625336,  683191,  739761,
              796092,  852304,  907947,  964526, 1021324, 1078742, 1135107,
             1192164, 1250158, 1307746, 1366458, 1426771, 1488497, 1550293],
            dtype=&#39;int64&#39;),
 2110: Int64Index([  20295,   75155,  130147,  184972,  240377,  295872,  350666,
              406769,  463183,  519031,  575511,  632980,  690561,  747199,
              803434,  859608,  915228,  971796, 1028677, 1086184, 1142539,
             1199871, 1257799, 1315449, 1374150, 1434806, 1496526, 1558927],
            dtype=&#39;int64&#39;),
 2111: Int64Index([1277065, 1334522, 1393957, 1455404, 1516877, 1580816], dtype=&#39;int64&#39;),
 2114: Int64Index([   3486,   58559,  113460,  168515,  223384,  279478,  333381,
              389890,  446449,  502499,  558632,  615658,  673836,  730231,
              786664,  842911,  898635,  955379, 1011777, 1069370, 1125686,
             1182377, 1240486, 1298071, 1356360, 1416348, 1478290, 1539241],
            dtype=&#39;int64&#39;),
 2117: Int64Index([  68127,  123096,  178059,  233248,  288923,  343342,  399660,
              456192,  512082,  568387,  625648,  683501,  740075,  796405,
              852604,  908254, 1021636, 1079065, 1135408, 1192492, 1250476,
             1308075, 1366795, 1427116, 1488860, 1550650],
            dtype=&#39;int64&#39;),
 2118: Int64Index([  40671,   94798,  149649,  204412,  260097,  315136,  370832,
              427311,  483012,  538865,  595658,  653674,  710529,  767383,
              823677,  879453,  935149,  991551, 1048948, 1106302, 1162452,
             1220681, 1278260, 1335689, 1395159, 1456707, 1518104, 1582153],
            dtype=&#39;int64&#39;),
 2124: Int64Index([   4726,   59779,  114660,  169673,  224638,  280647,  334643,
              391100,  447675,  503684,  559856,  616933,  675033,  731502,
              787883,  844130,  899881, 1012993, 1070557, 1126888, 1183680,
             1241759, 1299353, 1417712, 1479606, 1540683],
            dtype=&#39;int64&#39;),
 2128: Int64Index([    238,   55420,  110358,  165459,  220297,  276451,  330142,
              386633,  443275,  499352,  555296,  612246,  670648,  726989,
              783443,  839684,  895430,  952223, 1008588, 1066126, 1122415,
             1179017, 1237077, 1294763, 1352978, 1412899, 1474763, 1535559],
            dtype=&#39;int64&#39;),
 2133: Int64Index([  35602,   89933,  144742,  199602,  255219,  310378,  365782,
              422306,  478164,  533949,  590743,  648646,  705665,  762483,
              818732,  874496,  930165,  986735, 1043927, 1101329, 1157487,
             1215494, 1273258, 1330746, 1390002, 1451387, 1512732, 1576409],
            dtype=&#39;int64&#39;),
 2139: Int64Index([  33462,   87777,  142669,  197603,  253214,  308401,  363688,
              420187,  476075,  531910,  588632,  646476,  703558,  760345,
              816506,  872387,  928031,  984716, 1041873, 1099273, 1155474,
             1213348, 1271096, 1328601, 1387806, 1449078, 1510420, 1573956],
            dtype=&#39;int64&#39;),
 2140: Int64Index([  29027,   83590,  138547,  193461,  249010,  304255,  359325,
              415734,  471787,  527568,  584273,  641922,  699286,  755941,
              812210,  868160,  923803,  980394, 1037491, 1094942, 1151148,
             1208898, 1266654, 1324244, 1383303, 1444246, 1505776, 1568918],
            dtype=&#39;int64&#39;),
 2143: Int64Index([  18519,   73386,  128397,  183208,  238600,  294181,  348838,
              404973,  461423,  517284,  573701,  631161,  688800,  745383,
              801628,  845485,  913463,  970035, 1014338, 1071882, 1128251,
             1197984, 1255937, 1313568, 1372230, 1432859, 1494547, 1556828],
            dtype=&#39;int64&#39;),
 2145: Int64Index([  44926,   99024,  153859,  208685,  264479,  319370,  378665,
              431674,  487283,  543113,  600017,  658090,  715037,  776723,
              827992,  887010,  939382,  995851, 1053257, 1113937, 1166717,
             1228134, 1282540, 1340091, 1399703, 1461488, 1522744, 1587557],
            dtype=&#39;int64&#39;),
 2147: Int64Index([  20274,   75132,  130124,  184937,  240351,  295851,  350634,
              406747,  463158,  519007,  575486,  632957,  690538,  747171,
              803413,  859585,  915202,  971766, 1028646, 1086162, 1142508,
             1199842, 1257766, 1315419, 1374114, 1434767, 1496492, 1558885],
            dtype=&#39;int64&#39;),
 2151: Int64Index([  23090,   77870,  409692,  465895,  521751,  693426,  750072,
              806303,  862430,  918010, 1088981, 1145288, 1202856, 1260644,
             1318280, 1377078, 1437933, 1499531, 1562193],
            dtype=&#39;int64&#39;),
 2155: Int64Index([  46722,   98286,  153141,  207991,  263779,  318646,  374594,
              433689,  486562,  542370,  599285,  657338,  717119,  770992,
              827271,  882950,  938699,  997871, 1052531, 1109867, 1166091,
             1224408, 1284296, 1339391, 1401542, 1460707, 1521973, 1586575],
            dtype=&#39;int64&#39;),
 2156: Int64Index([1586308], dtype=&#39;int64&#39;),
 2158: Int64Index([  42218,   96364,  151193,  206031,  261768,  316693,  372557,
              429015,  484647,  540492,  597296,  655384,  712374,  769030,
              825335,  881095,  936772,  993194, 1050584, 1107926, 1164109,
             1222445, 1280017, 1337387, 1396916, 1458562, 1519920, 1584029],
            dtype=&#39;int64&#39;),
 2160: Int64Index([872091, 984436, 1098980, 1213067, 1328300, 1387513, 1448761,
             1573623],
            dtype=&#39;int64&#39;),
 2162: Int64Index([ 122483,  288329,  342718,  399048,  511477,  567759,  625031,
              682900,  739444,  795795,  852003,  907663,  964219, 1021016,
             1078458, 1134813, 1191869, 1249845, 1307452, 1366155, 1426458,
             1488191, 1549955],
            dtype=&#39;int64&#39;),
 2172: Int64Index([  28271,   82891,  137834,  192722,  248256,  303562,  358590,
              415009,  471063,  526828,  583514,  641167,  698522,  755179,
              811432,  867419,  923055,  979679, 1036715, 1094144, 1150418,
             1208100, 1265849, 1323479, 1382520, 1443436, 1504977, 1568067],
            dtype=&#39;int64&#39;),
 2175: Int64Index([  26870,   81547,  136488,  191369,  246863,  302206,  357188,
              413550,  469657,  525476,  582125,  639724,  697130,  753795,
              810048,  866041,  921701,  978346, 1035365, 1092736, 1149032,
             1206645, 1264407, 1322058, 1381023, 1441892, 1503464, 1566452],
            dtype=&#39;int64&#39;),
 2178: Int64Index([   2864,  112836,  167949,  222779,  278880,  332769,  389253,
              445873,  501898,  615046,  673252,  729633,  786082,  842270,
              898023,  954770, 1011160, 1068754, 1125060, 1181716, 1297435,
             1415660, 1477612, 1538510],
            dtype=&#39;int64&#39;),
 2182: Int64Index([   3001,   58074,  112967,  168065,  222903,  279000,  332906,
              389400,  446001,  502023,  558161,  673375,  729755,  786200,
              842418,  898153,  954899, 1011282, 1068882, 1125196, 1181844,
             1239965, 1297562, 1355829, 1415794, 1477765, 1538665],
            dtype=&#39;int64&#39;),
 2184: Int64Index([   2811,   57902,  112783,  167909,  278835,  332715,  389209,
              445826,  501849,  557977,  615002,  673206,  729587,  786039,
              842217,  897967,  954725, 1011108, 1068699, 1125006, 1181662,
             1239788, 1297391, 1355639, 1415610, 1477548, 1538459],
            dtype=&#39;int64&#39;),
 2187: Int64Index([  41792,   95951,  150781,  205608,  261362,  316303,  372109,
              428586,  484220,  540070,  596883,  654948,  711712,  768608,
              824892,  880648,  936342,  992784, 1050174, 1107469, 1163633,
             1221981, 1279493, 1336929, 1396442, 1458054, 1519441, 1583530],
            dtype=&#39;int64&#39;),
 2188: Int64Index([  21553,   76368,  131380,  186231,  241702,  297111,  351951,
              408093,  464389,  520228,  576785,  634311,  691834,  748478,
              804720,  860890,  916495,  973093, 1030023, 1087451, 1143811,
             1201255, 1259095, 1316765, 1375493, 1436293, 1497923, 1560437],
            dtype=&#39;int64&#39;),
 2190: Int64Index([  35646,   89975,  144784,  199637,  255277,  310423,  365828,
              422344,  478198,  533993,  590788,  648690,  705707,  762520,
              818779,  874543,  930204,  986774, 1043967, 1101380, 1157529,
             1215538, 1273300, 1330788, 1390054, 1451436, 1512779, 1576455],
            dtype=&#39;int64&#39;),
 2192: Int64Index([  36282,   90603,  145400,  200250,  255869,  311008,  366444,
              422977,  478806,  534607,  591393,  649305,  706298,  763119,
              819406,  875178,  930840,  987370, 1044552, 1102005, 1158154,
             1216191, 1273952, 1331426, 1390691, 1452106, 1513460, 1577166],
            dtype=&#39;int64&#39;),
 2195: Int64Index([  21760,   76567,  131574,  186427,  241889,  297304,  352156,
              408303,  464591,  520429,  576979,  634524,  692051,  748684,
              804926,  861090,  916687,  973297, 1030220, 1087665, 1144018,
             1201471, 1259293, 1316969, 1375712, 1436511, 1498122, 1560664],
            dtype=&#39;int64&#39;),
 2196: Int64Index([  32572,   86953,  141868,  196801,  252339,  307571,  362803,
              419293,  475200,  531047,  587777,  642944,  702692,  759448,
              815633,  871516,  927203,  983890, 1041048, 1098398, 1154628,
             1212490, 1270214, 1327717, 1386924, 1448130, 1509492, 1572903],
            dtype=&#39;int64&#39;),
 2198: Int64Index([  51747,  106116,  160931,  215732,  326421,  550659,  607637,
              665954,  835518,  947355, 1003794, 1061325, 1118240, 1232501,
             1289964, 1347835, 1469698, 1597286],
            dtype=&#39;int64&#39;),
 2202: Int64Index([ 364135,  420696,  476599,  532434,  589171,  647031,  704083,
              760888,  817095, 1155979, 1449619, 1510972, 1574510],
            dtype=&#39;int64&#39;),
 2203: Int64Index([  42022,   96171,  150992,  205821,  261572,  316506,  372346,
              428803,  484446,  540277,  597089,  655185,  711933,  768827,
              825119,  880876,  936564,  993001, 1050390, 1107691, 1163887,
             1222228, 1279782, 1337166, 1396681, 1458316, 1519699, 1583800],
            dtype=&#39;int64&#39;),
 2210: Int64Index([  19895,   74735,  129759,  184564,  239991,  295496,  350234,
              406356,  462798,  518620,  575109,  632569,  690166,  746773,
              803038,  859189,  914850,  971391, 1028245, 1085765, 1142119,
             1199436, 1257379, 1315032, 1373729, 1434378, 1496075, 1558468],
            dtype=&#39;int64&#39;),
 2211: Int64Index([  12528,   67446,  122420,  177378,  232555,  288267,  342657,
              398981,  455495,  511409,  567692,  624965,  682828,  739364,
              795725,  851947,  907601,  964156, 1020952, 1078383, 1134744,
             1191793, 1249779, 1307388, 1366092, 1426385, 1488111, 1549877],
            dtype=&#39;int64&#39;),
 2219: Int64Index([  18383,  128262,  183078,  238460,  294038,  348688,  404848,
              461291,  517137,  573564,  631027,  688653,  745250,  801477,
              913320,  969891, 1026726, 1084232, 1140574, 1197834, 1255796,
             1372081, 1432695, 1494395, 1556657],
            dtype=&#39;int64&#39;),
 2221: Int64Index([  52353,  106741,  161603,  216418,  272365,  327126,  383257,
              439906,  495643,  551464,  608434,  666773,  723881,  780264,
             1063643, 1115208, 1408497, 1470702, 1532068, 1598406],
            dtype=&#39;int64&#39;),
 2227: Int64Index([  63641,  118538,  173532,  228651,  284473,  338642,  451647,
              507588,  563788,  621013,  678951,  735424,  848069,  903794,
              960344, 1074495, 1130863, 1187771, 1245882, 1422015, 1483900,
             1545321],
            dtype=&#39;int64&#39;),
 2229: Int64Index([  39515,   93761,  148578,  203325,  259065,  314110,  369728,
              426222,  481932,  537764,  594554,  652550,  709440,  766300,
              822614,  878409,  934123,  990500, 1047830, 1105230, 1161379,
             1219521, 1277162, 1334615, 1394043, 1455494, 1516964, 1580908],
            dtype=&#39;int64&#39;),
 2232: Int64Index([   3127,   58201,  113081,  204022,  221145,  277301,  371943,
              391380,  444180,  549880,  568917,  629023,  671558,  731785,
              784350,  840573,  896336,  953136, 1013275, 1067056, 1127168,
             1179973, 1238042, 1295708, 1360177, 1413864, 1475760, 1536574],
            dtype=&#39;int64&#39;),
 2237: Int64Index([  31078,   85516,  140516,  195366,  250925,  306204,  361333,
              417845,  473775,  529573,  586357,  644034,  701275,  757980,
              814169,  870128,  925790,  982459, 1039615, 1096961, 1153207,
             1210992, 1268770, 1326315, 1385420, 1446506, 1507955, 1571225],
            dtype=&#39;int64&#39;),
 2238: Int64Index([   9519,   64470,  119346,  174356,  229480,  285256,  339507,
              395924,  452463,  508380,  564596,  621857,  679774,  736277,
              792724,  848885,  904597,  961175, 1017824, 1075344, 1131726,
             1188699, 1246762, 1304277, 1362858, 1422964, 1484805, 1546293],
            dtype=&#39;int64&#39;),
 2240: Int64Index([   7673,   62691,  117586,  172554,  227651,  283513,  337663,
              394037,  450654,  506630,  562800,  620013,  677960,  734457,
              790867,  847104,  902806,  959397, 1015979, 1073495, 1129925,
             1186719, 1244847, 1302384, 1360824, 1420911, 1482833, 1544123],
            dtype=&#39;int64&#39;),
 2250: Int64Index([  71456,  126449,  181356,  236663,  292242,  346815,  403048,
              459501,  515345,  571711,  629140,  686796,  799690,  855876,
              911506,  968060, 1082384, 1253948, 1311505, 1370129, 1430727,
             1492445, 1554553],
            dtype=&#39;int64&#39;),
 2252: Int64Index([  34027,   88383,  872988,  928647,  985209, 1042418, 1099842,
             1156053, 1213918, 1271723, 1329206, 1388443, 1449701, 1511050,
             1574605],
            dtype=&#39;int64&#39;),
 2253: Int64Index([  40806,   94939,  149805,  204572,  260273,  315305,  370991,
              427486,  483160,  539022,  595802,  653839,  710681,  767541,
              823837,  879599,  935307,  991707, 1049080, 1106469, 1162613,
             1220833, 1278409, 1335844, 1395312, 1456858, 1518278, 1582328],
            dtype=&#39;int64&#39;),
 2255: Int64Index([ 105542,  160321,  215142,  270983,  325785,  381793,  438485,
              549962,  606938,  665229,  722307,  778631,  834774,  890307,
              946612, 1003053, 1060550, 1173730, 1231699, 1289176, 1347016,
             1406700, 1468820, 1530209, 1596358],
            dtype=&#39;int64&#39;),
 2258: Int64Index([  26535,   81241,  191055,  301907,  356874,  413211,  469319,
              525154,  581801,  639401,  696815,  753469,  809708,  865735,
              921399,  978046, 1035068, 1092421, 1148718, 1206329, 1264077,
             1321721, 1380671, 1441550, 1503130, 1566093],
            dtype=&#39;int64&#39;),
 2259: Int64Index([  26906,   81582,  136525,  191409,  246898,  302235,  357226,
              413584,  469691,  525507,  582163,  639766,  697167,  753835,
              810095,  866086,  921737,  978375, 1035400, 1092775, 1149078,
             1206689, 1264445, 1322099, 1381066, 1441934, 1503507, 1566496],
            dtype=&#39;int64&#39;),
 2263: Int64Index([ 922778,  979412, 1036454, 1093886, 1150148, 1207786, 1265557,
             1323173, 1382212, 1443118, 1504649, 1567738],
            dtype=&#39;int64&#39;),
 2264: Int64Index([  46560,  100690,  155496,  210332,  266148,  320984,  377015,
              433547,  489073,  544904,  601920,  659955,  716941,  829780,
              941217,  997699, 1168516, 1226589, 1284130, 1341759, 1401363,
             1463294, 1524571, 1589937],
            dtype=&#39;int64&#39;),
 2269: Int64Index([  77931,  132894,  298679,  353559,  521802,  693481,  750139,
              806363,  862482,  918065, 1031638, 1145351, 1260714, 1318346,
             1377139, 1437991, 1562262],
            dtype=&#39;int64&#39;),
 2272: Int64Index([  20210,   75081,  130078,  184889,  240308,  295804,  350575,
              406689,  463102,  518961,  575444,  632904,  690492,  747118,
              803366,  859535,  915162,  971720, 1028597, 1086104, 1142446,
             1199786, 1257715, 1315368, 1374063, 1434714, 1496426, 1558821],
            dtype=&#39;int64&#39;),
 2273: Int64Index([  11630,   66536,  121490,  176432,  231577,  287328,  341654,
              398026,  454562,  510441,  623994,  681893,  738408,  794798,
              850988,  906683,  963244, 1019985, 1077437, 1133790, 1190828,
             1248859, 1306442, 1365090, 1425348, 1487081, 1548741],
            dtype=&#39;int64&#39;),
 2274: Int64Index([  38383,   92669,  147487,  708323,  765177,  821501,  877285,
              989426, 1046697, 1104135, 1276035, 1392855, 1454314, 1515776,
             1579619],
            dtype=&#39;int64&#39;),
 2276: Int64Index([  28815,   83397,  138339,  193227,  248779,  304051,  359105,
              415535,  471554,  527331,  584035,  641681,  699049,  755710,
              811981,  867954,  923569,  980150, 1037228, 1094699, 1150934,
             1208668, 1266398, 1296625, 1383065, 1443995, 1505540, 1568652],
            dtype=&#39;int64&#39;),
 2278: Int64Index([  11306,   66221,  121171,  176129,  231273,  286991,  341319,
              397712,  454236,  510116,  566423,  623649,  681557,  738102,
              794492,  850684,  906382,  962950, 1019676, 1077139, 1133477,
             1190521, 1248546, 1306125, 1364754, 1425007, 1486753, 1548379],
            dtype=&#39;int64&#39;),
 2279: Int64Index([   3265,   58349,  113227,  168318,  223157,  279259,  333151,
              389673,  446229,  502278,  558424,  615429,  673616,  730021,
              786439,  842677,  898416,  955167, 1011563, 1069134, 1125460,
             1182125, 1240241, 1297833, 1356100, 1416085, 1478045, 1538970],
            dtype=&#39;int64&#39;),
 2280: Int64Index([ 113396,  223320,  333317,  389831,  446387,  502437,  558574,
              615597,  730171,  786601,  842851,  898570,  955316, 1125621,
             1182313, 1240417, 1298009, 1356280, 1416274, 1539167],
            dtype=&#39;int64&#39;),
 2281: Int64Index([  11007,   65900,  120849,  175794,  230959,  286678,  340995,
              397401,  453909,  509807,  566117,  623330,  681249,  737774,
              794170,  850361,  906057,  962642, 1019359, 1076827, 1133173,
             1190227, 1248243, 1305805, 1364437, 1424680, 1486412, 1548034],
            dtype=&#39;int64&#39;),
 2285: Int64Index([  19917,  129780,  184584,  240013,  295519,  350255,  406376,
              462818,  518642,  575131,  632591,  690191,  746792,  803059,
              859210,  971410, 1028270, 1085788, 1142139, 1199455, 1257402,
             1315053, 1434399, 1496099, 1558490],
            dtype=&#39;int64&#39;),
 2292: Int64Index([ 135954,  301704,  356665,  412993,  469111,  524935,  581581,
              639171,  696603,  753274,  809503,  865529,  921203,  977844,
             1034857, 1092198, 1148490, 1263871, 1321503, 1380443, 1441307,
             1502915, 1565862],
            dtype=&#39;int64&#39;),
 2294: Int64Index([1365904, 1426182, 1487923, 1549682], dtype=&#39;int64&#39;),
 2295: Int64Index([  28985,   83560,  138507,  193419,  248978,  304220,  359286,
              415700,  471744,  527521,  584229,  641877,  699238,  755893,
              812157,  868125,  923756,  980353, 1037448, 1094900, 1151107,
             1208859, 1266599, 1324208, 1383271, 1444203, 1505736, 1568863],
            dtype=&#39;int64&#39;),
 2297: Int64Index([  16813,   71675,  126686,  181594,  236894,  292472,  347058,
              403281,  459731,  515578,  571953,  629401,  687034,  743637,
              799943,  856112,  911746,  968325, 1010166, 1082648, 1138989,
             1196161, 1254218, 1311758, 1370386, 1430983, 1492720, 1554844],
            dtype=&#39;int64&#39;),
 2298: Int64Index([  35221,   89525,  144367,  199219,  254841,  310046,  365381,
              421935,  477795,  533597,  590386,  648253,  705273,  762095,
              818357,  874138,  929796,  986382, 1043570, 1100980, 1157145,
             1215140, 1272871, 1330338, 1389635, 1450951, 1512323, 1575970],
            dtype=&#39;int64&#39;),
 2299: Int64Index([  24337,   79091,  134066,  188957,  244419,  299815,  354679,
              410967,  467120,  522984,  579612,  637148,  694602,  751317,
              807548,  863617,  919230,  975853, 1032800, 1090225, 1146494,
             1204131, 1261900, 1319530, 1378379, 1439217, 1500852, 1563614],
            dtype=&#39;int64&#39;),
 2300: Int64Index([   2928,   58007,  112896,  168000,  222841,  278928,  332838,
              389317,  445941,  501954,  558089,  615102,  673304,  729688,
              786135,  842326,  898079, 1125116, 1181765, 1239897, 1297488,
             1355751, 1415720, 1477675, 1538588],
            dtype=&#39;int64&#39;),
 2301: Int64Index([1364894, 1425147, 1486909, 1548538], dtype=&#39;int64&#39;),
 2308: Int64Index([   7313,   62347,  117220,  172196,  227270,  283154,  337297,
              393658,  450280,  506259,  562421,  619620,  677599,  734077,
              790451,  846727,  902417,  959060, 1015611, 1073108, 1129541,
             1186335, 1244434, 1301989, 1360418, 1420503, 1482416, 1543670],
            dtype=&#39;int64&#39;),
 2314: Int64Index([ 397335,  453843,  681182,  737701,  794103,  962576, 1019289,
             1076757, 1190161, 1248178, 1305739, 1364364, 1424605, 1547954],
            dtype=&#39;int64&#39;),
 2315: Int64Index([  53138,  107596,  162476,  217371,  273368,  328132,  384277,
              440951,  496734,  552543,  609435,  667757,  724911,  781277,
              837315,  892864,  949351, 1005733, 1063298, 1120253, 1176597,
             1234674, 1292083, 1349977, 1409714, 1471860, 1533236, 1599671],
            dtype=&#39;int64&#39;),
 2317: Int64Index([  37560,   91871,  146693,  201457,  257146,  312292,  367748,
              424259,  480044,  535815,  592627,  650628,  707552,  764388,
              820714,  876482,  932138,  988640, 1045886, 1103349, 1159472,
             1217580, 1275216, 1332695, 1392048, 1453485, 1514908, 1578720],
            dtype=&#39;int64&#39;),
 2321: Int64Index([  11349,   66272,  121218,  176168,  231318,  287037,  341361,
              397763,  454281,  510165,  566464,  623700,  681607,  738148,
              794543,  850730,  906430,  962995, 1019718, 1077185, 1133529,
             1190570, 1248595, 1306169, 1364802, 1425053, 1486815, 1548431],
            dtype=&#39;int64&#39;),
 2326: Int64Index([ 129114,  183927,  239317,  294854,  349566,  462138,  517994,
              574435,  631914,  689527,  858525, 1433634, 1495331, 1557664],
            dtype=&#39;int64&#39;),
 2327: Int64Index([  12175,   67083,  122074,  177025,  232206,  287908,  342292,
              398620,  455131,  511026,  567325,  624609,  682477,  738994,
              795384,  851572,  907242,  963823, 1020590, 1078002, 1134363,
             1191412, 1249429, 1307039, 1365713, 1425977, 1487716, 1549461],
            dtype=&#39;int64&#39;),
 2328: Int64Index([  37028,   91346,  146184,  200977,  256640,  311804,  367221,
              423730,  479507,  592114,  650097,  707031,  763891,  820191,
              875975,  931610,  988113, 1045355, 1102802, 1158950, 1217002,
             1274702, 1391525, 1452943, 1514349, 1578096],
            dtype=&#39;int64&#39;),
 2332: Int64Index([  84004,  138978,  193857,  304635,  416164,  472193,  584673,
              642375,  699691,  756343,  980841, 1095345, 1151563, 1209335,
             1267094, 1324678, 1383746, 1444705, 1506229, 1569367],
            dtype=&#39;int64&#39;),
 2338: Int64Index([  24560,   79328,  134285,  189188,  244659,  300050,  354924,
              411206,  467370,  523211,  579853,  637376,  694841,  751542,
              807767,  863833,  919448,  976089, 1033032, 1090455, 1146729,
             1204371, 1262145, 1319773, 1378646, 1439469, 1501098, 1563868],
            dtype=&#39;int64&#39;),
 2340: Int64Index([ 303389,  358408,  419769,  475643,  531496,  588204,  646065,
              703163,  759931,  816088,  871952,  927629,  984323, 1041498,
             1098849, 1155069, 1212940, 1270680, 1328173, 1387400, 1448631,
             1509978, 1573464],
            dtype=&#39;int64&#39;),
 2341: Int64Index([  12030,   66937,  121915,  176867,  232042,  287754,  342132,
              398463,  454975,  510864,  567162,  624437,  682324,  738835,
              795218,  851410,  907089,  963674, 1020429, 1077838, 1134207,
             1191263, 1249273, 1306877, 1365558, 1425806, 1487559, 1549290],
            dtype=&#39;int64&#39;),
 2344: Int64Index([   3080,   58153,  113038,  168133,  222972,  279063,  332971,
              389477,  446063,  502091,  558242,  615237,  673439,  729827,
              786270,  842492,  898229,  954965, 1011358, 1068954, 1125270,
             1181920, 1240046, 1297642, 1355902, 1415868, 1477836, 1538756],
            dtype=&#39;int64&#39;),
 2345: Int64Index([1222026, 1279533, 1336968, 1396489, 1458104, 1519496, 1583573], dtype=&#39;int64&#39;),
 2348: Int64Index([  44630,   98683,  153548,  208374,  264160,  319061,  374970,
              431369,  486941,  542780,  599684,  657764,  714697,  771412,
              832658,  883318,  939070,  995502, 1052907, 1110225, 1166456,
             1224760, 1282304, 1339782, 1399350, 1461132, 1522386, 1587172],
            dtype=&#39;int64&#39;),
 2349: Int64Index([  30035,   84577,  139538,  194410,  249986,  305202,  360355,
              416782,  472799,  528581,  585284,  642993,  700259,  756922,
              813153,  869113,  924764,  981440, 1038545, 1095927, 1152174,
             1209927, 1267690, 1325254, 1384350, 1445396, 1506858, 1570041],
            dtype=&#39;int64&#39;),
 2353: Int64Index([  19569,   74435,  129439,  184227,  239646,  295179,  349918,
              406065,  462475,  518319,  574775,  632254,  689843,  746440,
              802692,  858871,  914519,  971062, 1027903, 1085425, 1141783,
             1199085, 1257017, 1314693, 1373382, 1434016, 1495710, 1558068],
            dtype=&#39;int64&#39;),
 2356: Int64Index([  18848,   73723,  128741,  183566,  238937,  294495,  349153,
              405321,  461748,  517610,  574036,  631517,  689143,  745723,
              801969,  858142,  913808,  970366, 1027207, 1084693, 1141053,
             1198348, 1256287, 1313937, 1372614, 1433227, 1494921, 1557221],
            dtype=&#39;int64&#39;),
 2359: Int64Index([  26114,   80821,  135751,  190653,  246180,  301509,  356438,
              412767,  468901,  524723,  581373,  638959,  721378,  753071,
              809300,  865328,  921014,  977621, 1034634, 1091992, 1148258,
             1205890, 1288174, 1321286, 1380215, 1441084, 1502701, 1565636],
            dtype=&#39;int64&#39;),
 2360: Int64Index([  23223,   77975,  187878,  243333,  298724,  353602,  409807,
              466000,  521850,  578499,  636030,  693532,  750183,  806412,
              862539,  918105,  974736, 1031679, 1089084, 1145394, 1202966,
             1260759, 1318390, 1377195, 1438034, 1562307],
            dtype=&#39;int64&#39;),
 2365: Int64Index([1199041, 1256976, 1314645, 1373335, 1433964, 1495660, 1558015], dtype=&#39;int64&#39;),
 2366: Int64Index([  52703,  107101,  161981,  216835,  272810,  327526,  383681,
              440343,  496096,  551909,  608876,  663211,  724303,  780690,
              836727,  892285,  948730, 1005113, 1062691, 1119623, 1175948,
             1233995, 1291397, 1349300, 1409013, 1471189, 1532546, 1598942],
            dtype=&#39;int64&#39;),
 2370: Int64Index([  38980,   93237,  148042,  202802,  258546,  313584,  369191,
              425657,  481403,  537201,  594001,  652009,  708909,  765761,
              822062,  877861,  933596, 1104682, 1160854, 1218957, 1276612,
             1334062, 1393490, 1454913, 1516402, 1580306],
            dtype=&#39;int64&#39;),
 2372: Int64Index([51330, 834929, 1406871, 1468998, 1530389, 1596552], dtype=&#39;int64&#39;),
 2373: Int64Index([  52531,  103828,  158619,  213419,  269255,  324056,  383476,
              436617,  492098,  547986,  604989,  666981,  720261,  776607,
              832721,  888314,  944450, 1000913, 1058336, 1115319, 1171562,
             1233745, 1291136, 1349042, 1404498, 1466542, 1527804, 1593781],
            dtype=&#39;int64&#39;),
 2385: Int64Index([  11598,   66509,  121466,  231555,  287300,  341629,  454535,
              510414,  566716,  623975,  681870,  738381,  794762,  850953,
              906657,  963214, 1019961, 1077411, 1133765, 1190801, 1248840,
             1306401, 1365064, 1425320, 1487062, 1548717],
            dtype=&#39;int64&#39;),
 2391: Int64Index([  41199,   95338,  150187,  205002,  260707,  315701,  371438,
              427939,  483591,  539431,  596210,  654274,  711097,  767968,
              824275,  880026,  935693,  992153, 1049532, 1106868, 1163003,
             1221306, 1278833, 1336265, 1395757, 1457321, 1518730, 1582811],
            dtype=&#39;int64&#39;),
 2393: Int64Index([   1543,   56678,  111596,  166683,  221510,  277664,  331449,
              387968,  444551,  500630,  556661,  613656,  671952,  728286,
              784748,  840969,  896712,  953512, 1009877, 1067442, 1123742,
             1180379, 1238443, 1296090, 1354320, 1414277, 1476178, 1537029],
            dtype=&#39;int64&#39;),
 2399: Int64Index([ 540297,  597109,  655205,  711950,  768844,  825141,  880901,
              936592,  993029, 1050413, 1107715, 1163911, 1222251, 1279802,
             1337184, 1396702, 1458336, 1519717, 1583828],
            dtype=&#39;int64&#39;),
 2400: Int64Index([  45219,   99320,  154166,  208963,  264771,  319654,  375547,
              432134,  487671,  543589,  600524,  658582,  715631,  775557,
              828474,  884053,  939864,  996349, 1053767, 1114240, 1167179,
             1225236, 1282777, 1340351, 1399978, 1461795, 1523154, 1588321],
            dtype=&#39;int64&#39;),
 2402: Int64Index([  15665,   70571,  125548,  199875,  255508,  310655,  366051,
              422590,  478446,  534225,  591013,  648932,  705941,  762764,
              819032,  874792,  930460,  987007, 1044196, 1101636, 1157778,
             1215790, 1273556, 1331039, 1390301, 1451706, 1513036, 1576731],
            dtype=&#39;int64&#39;),
 2404: Int64Index([  41986,   96137,  150959,  205790,  261537,  316472,  372310,
              428768,  484414,  540245,  597059,  655154,  711902,  768796,
              825081,  880837,  936528,  992969, 1050354, 1107660, 1163849,
             1222192, 1279747, 1337128, 1396649, 1458281, 1519662, 1583766],
            dtype=&#39;int64&#39;),
 2405: Int64Index([   3875,   58952,  113822,  168881,  223748,  279836,  333769,
              390261,  446839,  502873,  949270, 1005653, 1012146, 1120178,
             1126086, 1182794, 1240903, 1298472, 1356784, 1471784, 1478727,
             1599594],
            dtype=&#39;int64&#39;),
 2409: Int64Index([  36861,   91163,  146006,  200813,  256457,  311625,  367027,
              423543,  479343,  591935,  649907,  706862,  819998,  875795,
              931424,  987930, 1045182, 1102607, 1158770, 1216815, 1274530,
             1331990, 1391337, 1452751, 1514127, 1577865],
            dtype=&#39;int64&#39;),
 2411: Int64Index([  11263,   66172,  121114,  176070,  231228,  286942,  341273,
              454188,  510074,  566382,  623591,  681508,  738054,  794451,
              906327,  962911, 1019618, 1077094, 1133436, 1190474, 1306075,
             1364706, 1424953, 1486703, 1548331],
            dtype=&#39;int64&#39;),
 2412: Int64Index([  23865,   78598,  133600,  188470,  243961,  299347,  354216,
              410460,  466617,  522487,  579111,  636661,  694125,  807039,
              863145,  918731,  975358, 1032291, 1089721, 1146014, 1203618,
             1261399, 1319046, 1377843, 1438681, 1500316, 1563028],
            dtype=&#39;int64&#39;),
 2414: Int64Index([  28521,   83117,  138064,  192959,  248504,  303795,  358832,
              415261,  471298,  527071,  583762,  641403,  698769,  755442,
              811709,  867698,  923296,  979931, 1036977, 1094425, 1150682,
             1208371, 1266126, 1323753, 1382782, 1443694, 1505248, 1568350],
            dtype=&#39;int64&#39;),
 2417: Int64Index([  29952,   84501,  139451,  194327,  249894,  305126,  416701,
              528506,  585212,  642894,  700179,  756837,  813083,  869029,
             1038458, 1152085, 1209853, 1384266, 1445297, 1506762, 1569950],
            dtype=&#39;int64&#39;),
 2423: Int64Index([1175471, 1233502, 1290914, 1348832, 1408520, 1470728, 1532093,
             1598431],
            dtype=&#39;int64&#39;),
 2425: Int64Index([  34959,   89270,  144116,  198989,  254577,  309777,  365109,
              421677,  477530,  533343,  590109,  647981,  705021,  761829,
              818096,  873866,  929512,  986092, 1043295, 1100730, 1156875,
             1214868, 1272611, 1330082, 1389367, 1450664, 1511986, 1575634],
            dtype=&#39;int64&#39;),
 2427: Int64Index([ 757953,  814142,  870103,  925762,  982431, 1039585, 1096931,
             1153180, 1210962, 1268740, 1326289, 1385392, 1446477, 1507926,
             1571200],
            dtype=&#39;int64&#39;),
 2433: Int64Index([   6681,   61719,  116568,  171570,  226618,  282528,  336640,
              393035,  449628,  505633,  561801,  618954,  676944,  733431,
              789831,  901793,  958453, 1014978, 1072464, 1185718, 1243765,
             1301326, 1359761, 1419803, 1481748, 1542893],
            dtype=&#39;int64&#39;),
 2434: Int64Index([  14750,   69660,  124646,  179629,  234855,  290470,  344963,
              401248,  457746,  513597,  570015,  627300,  685024,  741613,
              797971,  909789,  966421, 1023209, 1080622, 1136971, 1194108,
             1252098, 1309668, 1368426, 1428821, 1490576, 1552467],
            dtype=&#39;int64&#39;),
 2435: Int64Index([   5285,   60322,  115183,  225198,  281175,  335188,  391652,
              448184,  504224,  560378,  617486,  675534,  732044,  788437,
              844635,  900387,  957076, 1013520, 1071073, 1127409, 1184224,
             1242304, 1299917, 1358288, 1418276, 1480190, 1541286],
            dtype=&#39;int64&#39;),
 2437: Int64Index([  33569,   87888,  142780,  197697,  308498,  363785,  420292,
              476191,  532024,  588741,  646585,  703674,  760464,  816631,
              872502,  928147, 1099366, 1155595, 1213454, 1271218, 1328719,
             1387927, 1449194, 1510540, 1574078],
            dtype=&#39;int64&#39;),
 2441: Int64Index([   2781,   57879,  112761,  167885,  222709,  278805,  332685,
              389185,  445800,  501825,  557953,  614971,  673186,  729559,
              786011,  842197,  954703, 1011083, 1124976, 1181633, 1239761,
             1297366, 1415579, 1477518, 1538423],
            dtype=&#39;int64&#39;),
 2442: Int64Index([  52537,  106934,  161808,  216623,  272591,  327330,  383483,
              440129,  495872,  551686,  608656,  666992,  724105,  780469,
              836516,  948510, 1004903, 1062483, 1119421, 1175718, 1233756,
             1291158, 1349065, 1408776, 1470974, 1532350, 1598704],
            dtype=&#39;int64&#39;),
 2443: Int64Index([1586914], dtype=&#39;int64&#39;),
 2447: Int64Index([  40417,   94553,  149392,  204167,  259853,  314893,  370570,
              427062,  482772,  538627,  595412,  653424,  710295,  767144,
              823428,  879229,  934902,  991313, 1048702, 1106069, 1162215,
             1220436, 1278008, 1335439, 1394908, 1456433, 1517855, 1581872],
            dtype=&#39;int64&#39;),
 2449: Int64Index([   9206,   64169,  119064,  564331,  621587,  679506,  735998,
              792408,  848612,  904314,  960910, 1017550, 1075048, 1131439,
             1188392, 1246454, 1304009, 1362552, 1484515, 1545980],
            dtype=&#39;int64&#39;),
 2467: Int64Index([  49175,  103375,  158120,  212943,  268767,  323555,  379530,
              436112,  491620,  547470,  604509,  662617,  719771,  776122,
              832271,  887861,  943890, 1000399, 1057784, 1114826, 1171090,
             1228999, 1286613, 1344352, 1404038, 1466017, 1527310, 1593216],
            dtype=&#39;int64&#39;),
 2468: Int64Index([  43481,   97505,  152334,  207148,  262934,  317853,  373743,
              430212,  485772,  541579,  598493,  656533,  713470,  770141,
              826499,  882182,  937894,  994290, 1051686, 1109046, 1165263,
             1223568, 1281151, 1338515, 1459805, 1521132, 1585368],
            dtype=&#39;int64&#39;),
 2470: Int64Index([  32629,   87009,  141921,  196871,  252401,  307629,  362862,
              419358,  475261,  531112,  587838,  645648,  702754,  759507,
              815695,  871578,  927266,  983949, 1041113, 1098457, 1154690,
             1212556, 1270271, 1327784, 1387000, 1448198, 1509555, 1572971],
            dtype=&#39;int64&#39;),
 2478: Int64Index([  31695,   86132,  141098,  195966,  251495,  306777,  361930,
              418460,  474354,  530195,  586952,  644675,  701878,  758602,
              814801,  870718,  926375,  983079, 1040209, 1097568, 1153808,
             1211626, 1269384, 1326930, 1386059, 1447178, 1508585, 1571911],
            dtype=&#39;int64&#39;),
 2479: Int64Index([  31944,   86354,  141311,  251725,  306980,  815038, 1269624,
             1327163, 1508852, 1572215],
            dtype=&#39;int64&#39;),
 2481: Int64Index([  31313,   85748,  140734,  195576,  251142,  306430,  361563,
              418081,  473987,  529821,  586580,  644284,  701506,  758238,
              814409,  870360,  926015,  982702, 1039841, 1097194, 1153470,
             1211236, 1268999, 1326550, 1385663, 1446758, 1508196, 1571495],
            dtype=&#39;int64&#39;),
 2488: Int64Index([  97665,  152470,  207300,  263071,  317976,  373903,  430355,
              485908,  541710,  598638,  656682,  713629,  770302,  826649,
              882323,  938033,  994424, 1051837, 1109207, 1165405, 1223731,
             1281306, 1338686, 1398246, 1459966, 1521283, 1585542],
            dtype=&#39;int64&#39;),
 2492: Int64Index([  45748,   99890,  154692,  209494,  265307,  320167,  376132,
              432700,  488236,  544121,  601081,  659135,  716166,  772713,
              828990,  884567,  940417,  996886, 1054301, 1111339, 1167725,
             1225789, 1283326, 1340930, 1400538, 1462396, 1523727, 1589003],
            dtype=&#39;int64&#39;),
 2493: Int64Index([  31123,   85563,  140557,  195403,  250964,  306244,  361371,
              417884,  473813,  529615,  586397,  644075,  701316,  758031,
              814215,  870179,  925833,  982506, 1039647, 1097005, 1153259,
             1211038, 1268814, 1326369, 1385465, 1446554, 1507998, 1571283],
            dtype=&#39;int64&#39;),
 2497: Int64Index([  21518,   76331,  131339,  186199,  241670,  297078,  351913,
              408062,  464355,  520200,  576755,  634278,  691805,  748445,
              804691,  860858,  916464,  973063, 1029994, 1087422, 1143782,
             1201223, 1259065, 1316732, 1375458, 1436259, 1497890, 1560404],
            dtype=&#39;int64&#39;),
 2500: Int64Index([   4579,   59649,  114522,  169530,  224501,  280508,  334500,
              390970,  447539,  503541,  559708,  616780,  674894,  731368,
              787742,  843983,  899741,  956421, 1012856, 1070421, 1126752,
             1183521, 1241632, 1299219, 1357535, 1417568, 1479462, 1540518],
            dtype=&#39;int64&#39;),
 2504: Int64Index([  13646,   68576,  123543,  178512,  233732,  289350,  343799,
              400096,  456650,  512528,  568881,  626146,  683942,  740518,
              796855,  853037,  908679,  965313, 1022121, 1079502, 1135839,
             1192952, 1250923, 1308494, 1367257, 1427603, 1489359, 1551156],
            dtype=&#39;int64&#39;),
 2505: Int64Index([  34075,   88444,  143303,  198205,  253795,  308989,  364261,
              420815,  476723,  532553,  589301,  647140,  704198,  761015,
              817218,  873047,  928702,  985273, 1042473, 1099901, 1139236,
             1213981, 1254455, 1329263, 1388503, 1449767, 1511119, 1574673],
            dtype=&#39;int64&#39;),
 2509: Int64Index([   5217,   60266,  115126,  170117,  225130,  281120,  335122,
              391593,  448123,  504167,  560317,  617423,  675476,  731992,
              788381,  844582,  900336,  957020, 1013464, 1071022, 1242248,
             1299861, 1358223, 1418216, 1480130, 1541232],
            dtype=&#39;int64&#39;),
 2513: Int64Index([ 798712,  854894,  910545, 1081393, 1137764, 1194908, 1252915,
             1310500, 1369135, 1429662, 1491373, 1553398],
            dtype=&#39;int64&#39;),
 2516: Int64Index([   1842,   56968,  111878,  166958,  221787,  277952,  331729,
              388258,  444827,  500900,  556952,  613959,  672257,  728582,
              785040,  841258,  896999,  953806, 1010171, 1067748, 1124019,
             1180664, 1238753, 1296405, 1354618, 1414597, 1476488, 1537355],
            dtype=&#39;int64&#39;),
 2518: Int64Index([  17048,   71927,  126928,  181850,  237158,  292727,  347311,
              403515,  459976,  515841,  572213,  629651,  687287,  743897,
              800187,  856374,  911993,  968589, 1025421, 1082899, 1139247,
             1196421, 1254468, 1312030, 1370655, 1431262, 1492980, 1555127],
            dtype=&#39;int64&#39;),
 2519: Int64Index([  16032,   70924,  125916,  180795,  236103,  291698,  346244,
              402518,  458979,  514829,  571186,  628569,  686261,  742846,
              799181,  855354,  910984,  967576, 1024434, 1081873, 1138231,
             1195383, 1253405, 1310967, 1369607, 1430161, 1491881, 1553937],
            dtype=&#39;int64&#39;),
 2520: Int64Index([1578832], dtype=&#39;int64&#39;),
 2521: Int64Index([  32949,   87317,  142219,  197178,  252737,  307939,  363214,
              419710,  475585,  531446,  588150,  646008,  703107,  759864,
              816023,  871889,  927570,  984279, 1041455, 1098793, 1155014,
             1212890, 1270615, 1328119, 1387341, 1448576, 1509917, 1573395],
            dtype=&#39;int64&#39;),
 2522: Int64Index([   7268,   70188,  125161,  180102,  235359,  290976,  345490,
              401732,  458237,  514111,  570517,  627816,  685513,  742128,
              798446,  854621,  910277,  966885, 1023693, 1081114, 1137467,
             1194628, 1252626, 1310205, 1368894, 1429364, 1491104, 1553068],
            dtype=&#39;int64&#39;),
 2526: Int64Index([  43341,   97371,  152190,  207002,  262798,  317716,  373616,
              430080,  485636,  541450,  598350,  656413,  713347,  770025,
              937780,  994177, 1051564, 1108910, 1165119, 1223444, 1281023,
             1338390, 1397956, 1459665, 1521000, 1585215],
            dtype=&#39;int64&#39;),
 2528: Int64Index([    505,   55684,  110609,  165711,  220557,  276704,  330413,
              386894,  443534,  499626,  555547,  612528,  670891,  727237,
              783695,  839922,  895701, 1179315, 1237379, 1295035, 1353252,
             1413180, 1475055, 1535872],
            dtype=&#39;int64&#39;),
 2530: Int64Index([  27593,  137190,  192080,  247586,  302922,  357943,  470409,
              526207,  582861,  640500,  697863,  754537,  810817,  866775,
              979034, 1036090, 1093496, 1149784, 1207402, 1265156, 1322773,
             1381797, 1442687, 1567298],
            dtype=&#39;int64&#39;),
 2532: Int64Index([  10750,   65654,  120577,  175537,  230725,  286442,  340734,
              397136,  453664,  509552,  565860,  623075,  680984,  737498,
              793910,  850115,  905791,  962378, 1019088, 1076562, 1132926,
             1189971, 1247983, 1305530, 1364164, 1424384, 1486148, 1547738],
            dtype=&#39;int64&#39;),
 2533: Int64Index([  84473,  194296,  249861,  305099,  360244,  416669,  472676,
              528463,  585187,  642855,  700147,  756807,  813050,  868998,
              924662,  981323, 1038417, 1095808, 1152045, 1209817, 1267565,
             1506723, 1569903],
            dtype=&#39;int64&#39;),
 2538: Int64Index([  32947,   87315,  197176,  252735,  307937,  363212,  419708,
              475583,  531444,  588148,  646006,  703105,  759862,  816018,
              927568,  984273, 1041453, 1098791, 1155012, 1212888, 1328117,
             1387339, 1448574, 1509915, 1573390],
            dtype=&#39;int64&#39;),
 2544: Int64Index([  84238,  139214,  194069,  249631,  304866,  359995,  472431,
              528227,  642618,  699912,  756587,  868782,  924441, 1038160,
             1095589, 1151812, 1209587, 1324906, 1384001, 1444999, 1506486,
             1569638],
            dtype=&#39;int64&#39;),
 2548: Int64Index([  21601,   76414,  131427,  186282,  241749,  297160,  352002,
              408145,  464439,  520281,  576832,  634361,  691897,  748529,
              804775,  860942,  916545,  973147, 1030078, 1087509, 1143865,
             1201312, 1259145, 1316815, 1375550, 1436346, 1497974, 1560488],
            dtype=&#39;int64&#39;),
 2549: Int64Index([   6770,  116653,  226699,  282603,  393117,  449704,  505715,
              619042,  677035,  733505,  789909,  846184,  901873,  958529,
             1072556, 1128966, 1185802, 1243852, 1301415, 1481843, 1542997],
            dtype=&#39;int64&#39;),
 2552: Int64Index([  48470,  102664,  162328,  212237,  273199,  327947,  384089,
              436870,  496510,  552332,  661896,  719030,  775424,  837130,
              892683,  944739,  999626, 1063086, 1114106, 1170379, 1228278,
             1285889, 1345110, 1403295, 1465257, 1526586, 1592393],
            dtype=&#39;int64&#39;),
 2556: Int64Index([   1225,   56358,  111275,  166386,  221195,  277354,  331137,
              387629,  444237,  500302,  556317,  613293,  671625,  727944,
              784412,  840640,  896395,  953192, 1009569, 1067120, 1123426,
             1180035, 1238098, 1295772, 1353988, 1413922, 1475828, 1536653],
            dtype=&#39;int64&#39;),
 2558: Int64Index([  51979,  106325,  161165,  215978,  271891,  326687,  382796,
              439458,  495159,  550976,  607959,  666280,  723380,  779734,
              835864,  891396,  947730, 1004145, 1061701, 1118620, 1174907,
             1232903, 1290345, 1348245, 1407932, 1470115, 1531494, 1597771],
            dtype=&#39;int64&#39;),
 2563: Int64Index([ 597394,  655483,  712478,  769123,  825445,  881198,  936869,
              993300, 1050689, 1108034, 1164212, 1222545, 1280124, 1337494,
             1397023, 1458660, 1520029, 1584139],
            dtype=&#39;int64&#39;),
 2565: Int64Index([  29981,   84531,  139483,  194357,  249924,  305154,  360303,
              416731,  472739,  528531,  585238,  642933,  700209,  756870,
              813109,  869059,  924715,  981390, 1038495, 1095874, 1152116,
             1209882, 1267638, 1325195, 1384302, 1445337, 1506803, 1569982],
            dtype=&#39;int64&#39;),
 2566: Int64Index([  14679,   69593,  124587,  179555,  234792,  290404,  344884,
              401183,  457676,  513525,  569937,  627226,  684957,  741538,
              797911,  854088,  909730,  966353, 1023136, 1080558, 1136901,
             1194040, 1252029, 1309593, 1368344, 1428739, 1490501, 1552391],
            dtype=&#39;int64&#39;),
 2568: Int64Index([  24072,   78806,  133798,  188675,  244158,  299532,  354402,
              410656,  466824,  522688,  579303,  636856,  694314,  751015,
              807268,  863351,  918932,  975556, 1032490, 1089926, 1146223,
             1203828, 1261619, 1319249, 1378069, 1438892, 1500528, 1563255],
            dtype=&#39;int64&#39;),
 2570: Int64Index([  23923,   78662,  133655,  208573,  264370,  319263,  375174,
              410526,  466684,  543008,  599905,  657978,  714937,  771621,
              807118,  883521,  939280,  995722, 1053149, 1110406, 1339979,
             1399590, 1461364, 1525153, 1563110],
            dtype=&#39;int64&#39;),
 2572: Int64Index([  40610,  291363,  345892,  482947,  538805,  653607,  710467,
              823612,  879403,  991493, 1048877, 1220616, 1335626, 1395088,
             1518046, 1582080],
            dtype=&#39;int64&#39;),
 2576: Int64Index([1375767, 1528243, 1594280], dtype=&#39;int64&#39;),
 2577: Int64Index([643488, 1507356, 1570608], dtype=&#39;int64&#39;),
 2584: Int64Index([  14877,   69770,  124767,  179731,  234972,  290580,  345085,
              401354,  457857,  513715,  570128,  627417,  685131,  741718,
              798073,  854254,  909905,  966518, 1023335, 1080736, 1137102,
             1194228, 1252236, 1309797, 1368527, 1428926, 1490689, 1552590],
            dtype=&#39;int64&#39;),
 2587: Int64Index([  17414,   72325,  127291,  182215,  237557,  293110,  347722,
              403912,  460373,  516215,  572616,  630080,  687702,  744302,
              800562,  856753,  912367,  968978, 1025811, 1083273, 1139641,
             1196849, 1254866, 1312478, 1371067, 1431700, 1493398, 1555589],
            dtype=&#39;int64&#39;),
 2593: Int64Index([  10370,   65271,  120186,  175162,  230307,  286043,  340338,
              396753,  453265,  509164,  565459,  622681,  680583,  737088,
              793521,  849688,  905391,  961970, 1018670, 1076146, 1132521,
             1189549, 1247589, 1305128, 1363744, 1423936, 1485709, 1547266],
            dtype=&#39;int64&#39;),
 2594: Int64Index([  17054,   71935,  126934,  181856,  237168,  292737,  347319,
              403527,  459983,  515853,  572223,  629659,  687295,  743906,
              800195,  856384,  912006,  968598, 1025433, 1082911, 1139257,
             1196431, 1254477, 1312040, 1370668, 1431271, 1492990, 1555140],
            dtype=&#39;int64&#39;),
 2596: Int64Index([  51237,  105568,  160347,  215166,  271013,  325817,  381818,
              438515,  494170,  549993,  606973,  665265,  722337,  778664,
              834806,  890342,  946647, 1003082, 1060586, 1117502, 1173767,
             1231733, 1289210, 1347056, 1406738, 1468868, 1530255, 1596402],
            dtype=&#39;int64&#39;),
 2599: Int64Index([ 819957,  875768,  931395,  987905, 1045154, 1102580, 1158743,
             1216790, 1331957, 1391307, 1452727, 1577836],
            dtype=&#39;int64&#39;),
 2605: Int64Index([  28353,   82969,  137915,  192802,  248337,  303638,  358668,
              415087,  471141,  526906,  583596,  641248,  698593,  755266,
              811519,  867507,  923134, 1036808, 1094236, 1150507, 1208186,
             1265940, 1323573, 1382610, 1443522, 1505062, 1568157],
            dtype=&#39;int64&#39;),
 2612: Int64Index([   9794,   64749,  119617,  174633,  229748,  285527,  339775,
              396202,  452735,  508643,  564876,  622130,  680035,  736541,
              792995,  849156,  904870,  961448, 1018095, 1075615, 1131980,
             1188986, 1247032, 1304557, 1363139, 1423254, 1485096, 1546594],
            dtype=&#39;int64&#39;),
 2616: Int64Index([ 947997, 1004402, 1061944, 1118889, 1175173, 1233196, 1290615,
             1348514, 1408198, 1470407, 1531769, 1598090],
            dtype=&#39;int64&#39;),
 2625: Int64Index([115665, 560906, 1242856, 1300423, 1418837, 1541865], dtype=&#39;int64&#39;),
 2626: Int64Index([  50550,  104837,  159658,  214436,  270264,  325056,  381012,
              437685,  493209,  549147,  606091,  664324,  721429,  777745,
              833886,  889412,  945685, 1002173, 1059566, 1116542, 1172767,
             1230704, 1288233, 1346091, 1405737, 1467832, 1529126, 1595223],
            dtype=&#39;int64&#39;),
 2627: Int64Index([240283, 406667, 1086083, 1142430, 1496403, 1558794], dtype=&#39;int64&#39;),
 2640: Int64Index([   9673,   64622,  119491,  174504,  229629,  285405,  339656,
              396072,  452607,  508523,  564746,  622007,  679912,  736421,
              792869,  849031,  904748,  961323, 1017969, 1075499, 1131862,
             1188855, 1246911, 1304429, 1363013, 1423121, 1484972, 1546469],
            dtype=&#39;int64&#39;),
 2644: Int64Index([  38396,   92681,  147494,  202234,  257959,  313050,  368568,
              425059,  480834,  536624,  593429,  651412,  708335,  765188,
              821509,  877297,  932995,  989438, 1046709, 1104148, 1160300,
             1218377, 1276045, 1333481, 1392869, 1454328, 1515785, 1579635],
            dtype=&#39;int64&#39;),
 2649: Int64Index([  75511,  240768,  463512,  519351,  690920,  747545, 1374519,
             1435236, 1496943, 1559356],
            dtype=&#39;int64&#39;),
 2657: Int64Index([  41593,   95738,  150592,  205414,  261140,  316106,  371894,
              428375,  483990,  539865,  596656,  654700,  711504,  768386,
              824686,  880437,  936121,  992571, 1049935, 1107263, 1163431,
             1221754, 1279265, 1336700, 1396210, 1457812, 1519190, 1583285],
            dtype=&#39;int64&#39;),
 2665: Int64Index([  41280,   95426,  150273,  205093,  260802,  315790,  371534,
              428034,  483680,  539514,  596300,  654363,  711176,  768053,
              824361,  880114,  935770,  992236, 1106949, 1163089, 1221390,
             1278925, 1336358, 1395839, 1457410, 1518825, 1582903],
            dtype=&#39;int64&#39;),
 2666: Int64Index([  51535,  105883,  160681,  215482,  271363,  326163,  382196,
              438869,  494548,  550373,  607356,  665661,  722753,  779082,
              835234,  890766,  943758, 1003492, 1061020, 1117957, 1174210,
             1232182, 1289652, 1347508, 1407203, 1469342, 1530731, 1596910],
            dtype=&#39;int64&#39;),
 2669: Int64Index([  39275,   93531,  148332,  203098,  258833,  313878,  369487,
              425979,  481701,  537516,  594301,  652305,  709204,  766060,
              822367,  878161,  933877,  990259, 1047606, 1104991, 1161129,
             1219263, 1276904, 1334354, 1393784, 1455236, 1516713, 1580636],
            dtype=&#39;int64&#39;),
 2672: Int64Index([  70962,  125954,  291739,  346296,  402561,  459027,  514871,
              571228,  628614,  686304,  742888,  799223,  855394,  911024,
              967613, 1081909, 1138271, 1195426, 1253445, 1311008, 1369649,
             1491931, 1553988],
            dtype=&#39;int64&#39;),
 2673: Int64Index([  43201,  265353,  317593,  376185,  437962,  493496,  549418,
              601141,  659203,  721723,  772761,  834189,  884616,  940464,
             1002460, 1054358, 1111392, 1173066, 1231031, 1288554, 1346395,
             1406070, 1462457, 1523768, 1589058],
            dtype=&#39;int64&#39;),
 2674: Int64Index([   9589,   64537,  119410,  174423,  229553,  285326,  339576,
              395993,  452529,  508446,  564664,  621931,  679837,  736345,
              792788,  848952,  904665,  961243, 1017889, 1075418, 1246834,
             1304344, 1362931, 1423037, 1484888, 1546378],
            dtype=&#39;int64&#39;),
 2678: Int64Index([  22526,   77326,  132326,  187219,  242666,  298063,  352957,
              409112,  465374,  521195,  577780,  635360,  692860,  749492,
              805760,  861886,  917459,  974103, 1031003, 1088441, 1144759,
             1202301, 1260074, 1317728, 1376525, 1437348, 1498933, 1561566],
            dtype=&#39;int64&#39;),
 2683: Int64Index([  44001,   98046,  152870,  207722,  263477,  318389,  374295,
              430749,  486297,  542099,  599026,  657068,  714005,  770721,
              827019,  882695,  938429,  994842, 1052228, 1109606, 1165807,
             1224142, 1281706, 1339081, 1398679, 1460417, 1521697, 1586004],
            dtype=&#39;int64&#39;),
 2690: Int64Index([   4460,   59525,  114392,  169418,  280389,  334359,  390839,
              447409,  503415,  559581,  674757,  731237,  787630,  843852,
              899619,  956293, 1012727, 1070306, 1126631, 1183381, 1479340,
             1540367],
            dtype=&#39;int64&#39;),
 2697: Int64Index([   5509,   60546,  115396,  170384,  225413,  281370,  335410,
              391870,  448404,  504440,  560604,  617710,  675763,  732266,
              788679,  844867,  900615,  957301, 1013747, 1071291, 1127629,
             1184440, 1242547, 1300141, 1358550, 1418525, 1480445, 1541541],
            dtype=&#39;int64&#39;),
 2701: Int64Index([  22561,   77349,  132347,  187239,  242688,  298087,  352985,
              409138,  465395,  521224,  577811,  635395,  692893,  749516,
              805788,  861906,  917480, 1031021, 1088458, 1144783, 1202327,
             1260101, 1317752, 1376552, 1437371, 1498954, 1561590],
            dtype=&#39;int64&#39;),
 2703: Int64Index([  36991,   91299,  146139,  200941,  256600,  311769,  367179,
              423690,  479469,  535300,  592078,  650059,  706999,  763854,
              820151,  875941,  931573,  988073, 1045321, 1102770, 1158919,
             1216963, 1274670, 1332130, 1391485, 1452905, 1514311, 1578056],
            dtype=&#39;int64&#39;),
 2710: Int64Index([ 414712,  470772,  526546,  583224,  640864,  698211,  754903,
              811141, 1036430, 1265526, 1323152, 1382194, 1443085, 1504622,
             1567709],
            dtype=&#39;int64&#39;),
 2712: Int64Index([  52520,  106917,  158600,  216609,  272577,  327311,  383462,
              440112,  495849,  551664,  608630,  666968,  724082,  780444,
              836497,  892068,  948482, 1004876, 1062444, 1119388, 1175695,
             1233732, 1291123, 1349028, 1408741, 1470938, 1532314, 1598666],
            dtype=&#39;int64&#39;),
 2713: Int64Index([   1757,   56886,  111794,  166883,  221716,  277876,  331648,
              388175,  444743,  500820,  556865,  613870,  672175,  728493,
              784951,  841171,  896910,  953718, 1010083, 1067651, 1123944,
             1180583, 1238663, 1296304, 1354524, 1537261],
            dtype=&#39;int64&#39;),
 2716: Int64Index([  35577,   89901,  144711,  199569,  255195,  310351,  365760,
              422277,  478135,  533921,  590719,  648622,  705642,  762458,
              818710,  874471,  930140,  986710, 1043899, 1101306, 1157465,
             1215471, 1273234, 1330720, 1389973, 1451353, 1512701, 1576378],
            dtype=&#39;int64&#39;),
 2719: Int64Index([ 426929,  482643,  538501,  595281,  653300,  767012,  823303,
              879087,  991177, 1048566, 1105930, 1162078, 1220297, 1394774,
             1456286, 1517726, 1581714],
            dtype=&#39;int64&#39;),
 2732: Int64Index([39719, 369926, 1581141], dtype=&#39;int64&#39;),
 2734: Int64Index([  12441,   67354,  122328,  177286,  232470,  288176,  342567,
              398894,  455394,  511311,  567589,  624870,  682741,  739273,
              795637,  851845,  907515,  964072, 1020849, 1078286, 1134647,
             1191700, 1249691, 1307302, 1365994, 1426265, 1488003, 1549756],
            dtype=&#39;int64&#39;),
 2736: Int64Index([  43510,   97537,  152361,  207177,  262963,  317876,  373768,
              430241,  485798,  541598,  598513,  656557,  713504,  770167,
              826523,  882211,  937917,  994312, 1051712, 1109077, 1165289,
             1223596, 1281179, 1338549, 1398121, 1459839, 1521160, 1585407],
            dtype=&#39;int64&#39;),
 2738: Int64Index([  40928,   95062,  149915,  204701,  260402,  315436,  371123,
              427617,  483291,  539138,  595914,  653959,  710801,  767662,
              823952,  879718,  935411,  991823, 1049202, 1106578, 1162716,
             1220964, 1278530, 1335957, 1395432, 1456987, 1518399, 1582451],
            dtype=&#39;int64&#39;),
 2740: Int64Index([  45690,   99842,  154647,  209453,  265263,  320125,  376085,
              432652,  488186,  544075,  601032,  659084,  716115,  772670,
              828948,  884524,  940367,  996834, 1054247, 1111294, 1167674,
             1225747, 1283266, 1340878, 1400474, 1462345, 1523668, 1588943],
            dtype=&#39;int64&#39;),
 2746: Int64Index([    135,   55317,  110277,  165378,  220190,  330040,  386545,
              443194,  499277,  555207,  612170,  670569,  726909,  783374,
              839610,  895332,  952137, 1008513, 1066044, 1122338, 1178927,
             1236989, 1294671, 1412796, 1474667, 1535449],
            dtype=&#39;int64&#39;),
 2747: Int64Index([  28257,   82879,  137821,  192711,  248244,  755166,  811416,
              867408,  923043,  979669, 1036702, 1094131, 1150402, 1208088,
             1265836, 1323465, 1382509, 1443425, 1504959, 1568048],
            dtype=&#39;int64&#39;),
 2748: Int64Index([  47137,   99129,  153966,  208786,  264582,  319471,  377624,
              431983,  487505,  543415,  600345,  658399,  715444,  772010,
              828304,  883880,  939690,  996160, 1053582, 1110675, 1171720,
             1225069, 1282625, 1342427, 1399811, 1463971, 1522959, 1588002],
            dtype=&#39;int64&#39;),
 2750: Int64Index([ 145003,  199852,  255485,  310628,  366028,  422563,  478417,
              534196,  648903,  705911,  762732,  818999,  874759,  930428,
              986979, 1044169, 1101608, 1157749, 1215758, 1273523, 1331008,
             1390270, 1451669, 1513003, 1576694],
            dtype=&#39;int64&#39;),
 2754: Int64Index([  50416,  104686,  159511,  249281,  304490,  380828,  437508,
              472050,  527839,  605913,  642228,  721232,  777547,  812467,
              868419,  924057,  980695, 1037770, 1095205, 1151414, 1209174,
             1266934, 1324511, 1383590, 1444550, 1528889, 1569198],
            dtype=&#39;int64&#39;),
 2759: Int64Index([ 134418,  300194,  355083,  411355,  467532,  523367,  637533,
             1090597, 1146882, 1204533, 1319931, 1378800, 1439643, 1564039],
            dtype=&#39;int64&#39;),
 2761: Int64Index([ 663993,  721094,  777393,  830614,  889067,  910944,  999912,
             1059202, 1116174, 1230317, 1287863, 1345726, 1405358, 1467437,
             1528712, 1594790],
            dtype=&#39;int64&#39;),
 2764: Int64Index([  44899,   98964,  153800,  208637,  264428,  319323,  375225,
              431636,  487238,  543067,  599966,  658043,  714994,  771675,
              827947,  883574,  939338,  995811, 1053215, 1110453, 1399655,
             1461437, 1522689, 1587498],
            dtype=&#39;int64&#39;),
 2771: Int64Index([ 495423,  551248,  608212,  666557,  723658,  891662,  948030,
             1004437, 1061978, 1118922, 1175214, 1233239, 1290652, 1348553,
             1408241, 1470450, 1482867, 1598133],
            dtype=&#39;int64&#39;),
 2775: Int64Index([  14730,   69640,  124624,  179604,  234833,  290448,  344941,
              401229,  457727,  513572,  569987,  627271,  685005,  741592,
              797950,  854135,  909768,  966398, 1023187, 1080598, 1136950,
             1252074, 1309645, 1368397, 1428797, 1490550, 1552443],
            dtype=&#39;int64&#39;),
 2776: Int64Index([358860, 1568374], dtype=&#39;int64&#39;),
 2779: Int64Index([   3270,   58351,  113232,  223159,  279264,  389676,  446231,
              502280,  558426,  615432,  730023,  786441,  842679,  898419,
              955169, 1011565, 1069136, 1125462, 1182131, 1240243, 1297836,
             1356103, 1416087, 1478047, 1538972],
            dtype=&#39;int64&#39;),
 2784: Int64Index([  46749,  100898,  210520,  266339,  321179,  377227,  433716,
              489261,  545112,  602112,  660155,  717142,  773670,  829950,
              885584,  941411,  997895, 1055280, 1112374, 1168729, 1226791,
             1284321, 1341980, 1401571, 1463527, 1524803, 1590197],
            dtype=&#39;int64&#39;),
 2785: Int64Index([  19405,   74293,  129290,  184090,  239497,  295045,  349770,
              405903,  462321,  518179,  574616,  632102,  689689,  746283,
              802548,  858719,  914368,  970923, 1027770, 1085260, 1141612,
             1198919, 1256862, 1314528, 1373212, 1433835, 1495530, 1557861],
            dtype=&#39;int64&#39;),
 2789: Int64Index([  28385,   82999,  137943,  192829,  248366,  303666,  358696,
              415119,  471168,  526935,  583625,  641274,  698621,  755294,
              811550,  867543,  923160,  979787, 1036835, 1094266, 1150535,
             1208215, 1265972, 1323604, 1382644, 1443553, 1505092, 1568188],
            dtype=&#39;int64&#39;),
 2795: Int64Index([  23005,   77797,  132766,  187684,  243135,  298534,  353417,
              409596,  465814,  521669,  578295,  635849,  693338,  749989,
              806234,  862352,  917936,  974560, 1031503, 1088902, 1145215,
             1202777, 1260574, 1318208, 1376992, 1437854, 1499443, 1562101],
            dtype=&#39;int64&#39;),
 2796: Int64Index([  44602,   98660,  883290,  939042,  995477, 1052878, 1166430,
             1224735, 1282273, 1339755, 1399322, 1461095, 1522350, 1587142],
            dtype=&#39;int64&#39;),
 2800: Int64Index([  35032,   89337,  144170,  199045,  254649,  309845,  365177,
              421741,  477595,  533401,  590175,  648044,  705080,  761897,
              818163,  873936,  929592,  986167, 1043378, 1100793, 1156942,
             1214938, 1272677, 1330149, 1389441, 1450732, 1512068, 1575717],
            dtype=&#39;int64&#39;),
 2803: Int64Index([  48070,  102231,  156984,  211826,  267639,  322474,  378442,
              434988,  490544,  546400,  603417,  661510,  718628,  776533,
              831205,  886806,  942745,  999239, 1056646, 1113740, 1170089,
             1227974, 1285568, 1343263, 1402897, 1464849, 1526148, 1591952],
            dtype=&#39;int64&#39;),
 2805: Int64Index([  10152,  230091,  285851,  468921,  736899,  793342, 1304918,
             1363514, 1423677, 1485496, 1547025],
            dtype=&#39;int64&#39;),
 2810: Int64Index([ 396412,  468754,  524586,  581228,  638810,  696232,  752916,
              809142,  865182,  920878,  977480, 1034481, 1148117, 1205761,
             1263525, 1321163, 1380069, 1440930, 1502548, 1565466],
            dtype=&#39;int64&#39;),
 2816: Int64Index([  11108,   66017,  120961,  175906,  231065,  286782,  341108,
              397505,  454018,  509911,  566225,  623437,  681354,  737887,
              794277,  850481,  906174,  962758, 1019460, 1076935, 1133291,
             1190338, 1248356, 1305923, 1364550, 1424798, 1486536, 1548166],
            dtype=&#39;int64&#39;),
 2818: Int64Index([720993, 777280, 1467323, 1528586, 1594654], dtype=&#39;int64&#39;),
 2828: Int64Index([  38336,   92632,  147443,  202184,  257911,  313000,  368514,
              425002,  480790,  536583,  593373,  651358,  765139,  821466,
              877252,  932941,  989383, 1046663, 1104096, 1160255, 1218320,
             1275992, 1333435, 1392814, 1454263, 1515726, 1579577],
            dtype=&#39;int64&#39;),
 2829: Int64Index([  50029,  104258,  159096,  174670,  269678,  324468,  437066,
              492572,  548437,  605442,  663620,  720726,  777019,  833168,
              888688,  944975, 1058801, 1115780, 1172010, 1287484, 1345344,
             1404955, 1467013, 1528287, 1594327],
            dtype=&#39;int64&#39;),
 2832: Int64Index([  46891,  101063,  210675,  266491,  321331,  377389,  433877,
              489412,  545270,  602262,  660313,  717288,  773826,  830076,
              885727,  941565, 1055418, 1112521, 1168891, 1226929, 1284465,
             1342130, 1401712, 1463677, 1524945, 1590364],
            dtype=&#39;int64&#39;),
 2840: Int64Index([1550879], dtype=&#39;int64&#39;),
 2841: Int64Index([   1296,   56439,  111341,  221272,  277427,  331218,  387712,
              444320,  500390,  556413,  613401,  671719,  728041,  784498,
              840715,  896474,  953280, 1009662, 1067219, 1123514, 1180130,
             1238182, 1295854, 1354083, 1414019, 1475921, 1536767],
            dtype=&#39;int64&#39;),
 2843: Int64Index([ 106524,  161365,  216184,  272114,  326894,  383005,  439659,
              495387,  551209,  608168,  666500,  723607,  779976,  836079,
              891616, 1004376, 1061920, 1118863, 1175147, 1233165, 1290589,
             1348488, 1408172, 1470381, 1531742, 1598064],
            dtype=&#39;int64&#39;),
 2847: Int64Index([  23132,   77907,  132869,  187803,  243260,  298656,  353530,
              409726,  465933,  521781,  578420,  635962,  693457,  750111,
              806336,  862459,  918039,  974672, 1031614, 1089013, 1145327,
             1202891, 1260688, 1318320, 1377110, 1437966, 1499570, 1562235],
            dtype=&#39;int64&#39;),
 2852: Int64Index([  41783,   95943,  150772,  316294,  372100,  428578,  484212,
              540062,  596875,  654941,  711698,  768599,  824885,  880641,
              936332,  992775, 1050161, 1107461, 1163623, 1221972, 1279480,
             1336921, 1396434, 1458044, 1519432, 1583521],
            dtype=&#39;int64&#39;),
 2855: Int64Index([ 142119,  197066,  759741,  815904,  871783, 1098678, 1154897,
             1212782, 1509790, 1573258],
            dtype=&#39;int64&#39;),
 2857: Int64Index([ 648481, 1043770, 1101180, 1157342, 1215343, 1273095, 1330579,
             1389846, 1451212, 1512560, 1576212],
            dtype=&#39;int64&#39;),
 2867: Int64Index([  12783,   67705,  122680,  177634,  232841,  288525,  342928,
              399240,  455768,  511673,  567975,  625242,  683099,  739666,
              795987,  852205,  907852,  964425, 1021228, 1078651, 1135015,
             1192079, 1250055, 1307649, 1366357, 1426669, 1488400, 1550176],
            dtype=&#39;int64&#39;),
 2868: Int64Index([   2139,   95012,  149868,  204639,  260352,  315384,  371079,
              388556,  445120,  501182,  557268,  614269,  672563,  728894,
              812130,  839621,  923731,  980319, 1037410, 1094874, 1151081,
             1208834, 1259554, 1317212, 1375976, 1436793, 1498373, 1560968],
            dtype=&#39;int64&#39;),
 2873: Int64Index([  31512,   85961,  140931,  195777,  251324,  306613,  361764,
              418295,  474194,  530031,  586786,  644504,  701711,  758444,
              814632,  870563,  926218,  982910, 1040046, 1097399, 1153674,
             1211440, 1269214, 1326754, 1385886, 1446993, 1508423, 1571729],
            dtype=&#39;int64&#39;),
 2880: Int64Index([ 417771,  473696,  529483,  586291,  643963,  701213,  757910,
              814105,  870058,  925714,  982391, 1039542, 1096889, 1153140,
             1210912, 1268689, 1385339, 1446430, 1507868, 1571148],
            dtype=&#39;int64&#39;),
 2890: Int64Index([ 313569,  369175,  425642,  481387,  537185,  593984,  651996,
              708894,  765749,  822049,  877850,  933585,  989972, 1047301,
             1104670, 1160843, 1218944, 1276601, 1334048, 1393476, 1454898,
             1516387, 1580291],
            dtype=&#39;int64&#39;),
 2891: Int64Index([  40197,   94367,  149196,  203948,  259651,  314684,  370371,
              426840,  482552,  538410,  595189,  653213,  710070,  766927,
              823220,  879006,  934707,  991096, 1048464, 1105847, 1161991,
             1220212, 1277802, 1335232, 1394696, 1456190, 1517634, 1581619],
            dtype=&#39;int64&#39;),
 2894: Int64Index([    295,   55490,  110407,  165506,  220354,  276512,  330213,
              386691,  443336,  499421,  555352,  612312,  670704,  727037,
              783499,  839739,  895489,  952276, 1008652, 1066199, 1122477,
             1179081, 1237138, 1294822, 1353037, 1412963, 1474828, 1535636],
            dtype=&#39;int64&#39;),
 2895: Int64Index([  20203,   93894,  148709,  203449,  259192,  314245,  369859,
              426355,  482051,  537894,  594677,  652694,  709555,  766436,
              822750,  878533,  934251,  990620, 1047962, 1105363, 1161507,
             1219658, 1277300, 1334748, 1394198, 1455636, 1517102, 1581065],
            dtype=&#39;int64&#39;),
 2897: Int64Index([  29111,  104527,  159367,  214144,  269956,  380663,  437364,
              492869,  548798,  605764,  663967,  699378,  777368,  833511,
              889039,  945312, 1001796, 1059167, 1116147, 1172385, 1230286,
             1287840, 1345699, 1405332, 1467411, 1528686, 1594760],
            dtype=&#39;int64&#39;),
 2904: Int64Index([  47712,  101871,  152698,  207526,  263312,  318231,  374166,
              434640,  490220,  546065,  603072,  656922,  718281,  774732,
              830900,  886501,  942385,  998874, 1052079, 1113419, 1169763,
             1227661, 1285231, 1342915, 1402527, 1464473, 1525790, 1591544],
            dtype=&#39;int64&#39;),
 2906: Int64Index([  14415,   69364,  124350,  179303,  234536,  290166,  344624,
              400946,  457453,  513299,  569703,  626971,  684732,  741312,
              797674,  853853,  909487,  966106, 1022917, 1080299, 1136662,
             1193799, 1251786, 1309324, 1368097, 1428493, 1490226, 1552115],
            dtype=&#39;int64&#39;),
 2907: Int64Index([ 128696,  183519,  238897,  294461,  349117,  405271,  461695,
              517574,  573997,  631472,  689103,  745681,  801925,  913757,
              970322, 1027158, 1084642, 1141005, 1198304, 1256239, 1313888,
             1372569, 1433183, 1494866, 1557174],
            dtype=&#39;int64&#39;),
 2908: Int64Index([   4510,   59570,  114440,  169458,  224408,  280427,  334397,
              390879,  447462,  503454,  559620,  616689,  674804,  731283,
              787668,  843900,  899659,  956339, 1012771, 1070351, 1126676,
             1183432, 1241557, 1299140, 1357460, 1417479, 1479384, 1540427],
            dtype=&#39;int64&#39;),
 2909: Int64Index([  40420,   94556,  149395,  204170,  259857,  314896,  370573,
              427065,  482775,  538630,  595415,  653427,  710298,  767147,
              823431,  879232,  934906,  991316, 1048705, 1106072, 1162217,
             1220438, 1278011, 1335442, 1394911, 1456436, 1517858, 1581875],
            dtype=&#39;int64&#39;),
 2911: Int64Index([  44166,   98208,  153051,  207906,  263683,  318565,  374497,
              430916,  486472,  542279,  599201,  657254,  714196,  770900,
              827192,  882868,  938610,  995031, 1052440, 1109791, 1224325,
             1281883, 1339295, 1398882, 1460617, 1521884, 1586427],
            dtype=&#39;int64&#39;),
 2912: Int64Index([  16569,   71432,  126430,  181340,  236645,  292224,  346800,
              403028,  459484,  515325,  571693,  629113,  686776,  743371,
              799668,  855856,  911480,  968044, 1024927, 1082361, 1138715,
             1195887, 1253924, 1311480, 1370110, 1430705, 1492421, 1554529],
            dtype=&#39;int64&#39;),
 2916: Int64Index([  39051,   93309,  148112,  202870,  258619,  313649,  369254,
              425731,  481476,  537266,  594070,  652076,  708974,  765822,
              822127,  877930,  933657,  990047, 1104755, 1160913, 1219021,
             1276670, 1334130, 1393554, 1454990, 1516465, 1580371],
            dtype=&#39;int64&#39;),
 2923: Int64Index([  21170,   76009,  131017,  185868,  241331,  296730,  351552,
              407706,  464008,  519868,  558354,  633934,  691439,  743317,
              804352,  860516,  916089,  972724, 1029627, 1087053, 1143438,
             1200845, 1258711, 1316380, 1370048, 1435876, 1497528, 1560005],
            dtype=&#39;int64&#39;),
 2926: Int64Index([   8791,   71151,  126141,  181033,  236354,  291929,  346490,
              402753,  459187,  515049,  571418,  628808,  686489,  743063,
              799387,  855570,  911190,  967766, 1024633, 1082075, 1138428,
             1195604, 1253628, 1311182, 1369815, 1430395, 1492110, 1554189],
            dtype=&#39;int64&#39;),
 2927: Int64Index([  28129,   82739,  137682,  192575,  248112,  303408,  358430,
              414866,  470920,  526677,  583362,  641004,  698363,  755031,
              811284,  867265,  922896,  979521, 1036563, 1093999, 1150267,
             1207914, 1265693, 1323302, 1382348, 1443258, 1504792, 1567888],
            dtype=&#39;int64&#39;),
 2929: Int64Index([  30127,   84679,  139631,  194505,  250082,  305300,  360452,
              416862,  472891,  528680,  585382,  643101,  700354,  757020,
              813242,  869208,  924859,  981524, 1038662, 1096014, 1152271,
             1210031, 1267773, 1325357, 1384456, 1445500, 1506958, 1570146],
            dtype=&#39;int64&#39;),
 2944: Int64Index([  35834,   90163,  144971,  199824,  255451,  310597,  365999,
              422530,  478386,  534168,  590952,  648872,  705879,  762701,
              818967,  874728,  930396,  986947, 1044138, 1101573, 1157718,
             1215721, 1273489, 1330977, 1390239, 1451629, 1512971, 1576661],
            dtype=&#39;int64&#39;),
 2950: Int64Index([  16390,   71258,  126253,  181160,  236469,  292035,  346608,
              402859,  459307,  515162,  571526,  628918,  686596,  743181,
              799496,  855679,  911298,  967876, 1024750, 1082185, 1138543,
             1195719, 1253760, 1311304, 1369928, 1430520, 1492228, 1554327],
            dtype=&#39;int64&#39;),
 2951: Int64Index([   6210,   61237,  116089,  171078,  226129,  282070,  336128,
              392534,  449107,  505112,  561333,  618424,  676470,  732955,
              789348,  845611,  901290,  957989, 1014468, 1071998, 1128378,
             1185204, 1243241, 1300798, 1359266, 1419262, 1481198, 1542333],
            dtype=&#39;int64&#39;),
 2958: Int64Index([  35079,   89388,  144227,  199101,  254707,  365234,  421790,
              477650,  533457,  590222,  648093,  705131,  761945,  818215,
              873995,  929657,  986219, 1043427, 1100849, 1156993, 1214993,
             1272724, 1330196, 1389497, 1450784, 1575773],
            dtype=&#39;int64&#39;),
 2959: Int64Index([ 215009,  270843,  381645,  438348,  493999, 1346847, 1406521,
             1468619, 1529998, 1596129],
            dtype=&#39;int64&#39;),
 2964: Int64Index([  15250,   70153,  125131,  180079,  235326,  290936,  345461,
              401705,  458199,  514079,  570494,  627785,  685482,  742099,
              798422,  854592,  910248,  966858, 1023669, 1081089, 1137442,
             1194602, 1252598, 1310175, 1368867, 1429329, 1491072, 1553027],
            dtype=&#39;int64&#39;),
 2966: Int64Index([   1814,   56947,  111855,  166938,  221767,  277931,  331709,
              388233,  444805,  500878,  556928,  613932,  672234,  728555,
              785012,  841235,  896973,  953783, 1010147, 1067717, 1124006,
             1180643, 1238725, 1296373, 1354595, 1414568, 1476462, 1537331],
            dtype=&#39;int64&#39;),
 2971: Int64Index([  50805,  105086,  214681,  270508,  325307,  437972,  549429,
              606375,  656299,  713231,  778043,  834203,  889718,  937680,
             1002475, 1116881, 1288565, 1346408, 1468162, 1529494, 1595600],
            dtype=&#39;int64&#39;),
 2972: Int64Index([    353,   55537,  110463,  220415,  276571,  386751,  443393,
              499477,  555403,  783555,  839784,  895554, 1008724, 1066249,
             1122544, 1179153, 1237205, 1294881, 1353089, 1474900, 1535728],
            dtype=&#39;int64&#39;),
 2982: Int64Index([  47259,  101444,  156219,  211062,  266846,  321710,  377726,
              434258,  489829,  545695,  602717,  660791,  717895,  774346,
              830528,  886128,  942011,  998496, 1055912, 1113048, 1342565,
             1402153, 1525418, 1591136],
            dtype=&#39;int64&#39;),
 2988: Int64Index([  39415,   93664,  148470,  203224,  258967,  314001,  369630,
              426121,  481832,  537656,  594451,  652450,  709336,  766193,
              822509,  878299,  934014,  990399, 1047728, 1105124, 1161282,
             1219415, 1277046, 1334505, 1393937, 1455386, 1516859, 1580795],
            dtype=&#39;int64&#39;),
 2993: Int64Index([  50895,  105181,  159994,  206965,  267129,  317696,  377954,
              490062,  549537,  606501,  664760,  721849,  778161,  834327,
              889848,  946129, 1002597, 1117009, 1169619, 1231186, 1406211,
             1468302, 1529643, 1595759],
            dtype=&#39;int64&#39;),
 2995: Int64Index([  23017,   77807,  132774,  187694,  243146,  353427,  521683,
              693353,  749998,  806240,  862360, 1031512, 1202785, 1260581,
             1318216, 1376999, 1437863, 1499454, 1562110],
            dtype=&#39;int64&#39;),
 2996: Int64Index([  26979,   81649,  136600,  191485,  246973,  302314,  357303,
              413663,  469767,  525588,  582242,  639850,  697241,  753912,
              810173,  866157,  921819,  978454, 1035468, 1092853, 1149158,
             1206763, 1264520, 1322180, 1381145, 1442015, 1503587, 1566577],
            dtype=&#39;int64&#39;),
 3000: Int64Index([   2404,   57494,  112401,  167487,  222338,  278451,  332311,
              388818,  445385,  501440,  557563,  614570,  672804,  729160,
              785620,  841804,  897571,  954362, 1010741, 1068295, 1124599,
             1181239, 1239346, 1296990, 1355222, 1415189, 1477099, 1538010],
            dtype=&#39;int64&#39;),
 3014: Int64Index([ 227530,  393919,  450536,  506510,  562677,  619888,  677845,
              734329,  790732,  846977,  902680,  959287, 1015871, 1073369,
             1129787, 1186592, 1244712, 1302247, 1360690, 1420782, 1482694,
             1543978],
            dtype=&#39;int64&#39;),
 3019: Int64Index([ 557224, 1010429, 1068009, 1124286, 1180937, 1239026, 1296690,
             1354899, 1414866, 1476765, 1537651],
            dtype=&#39;int64&#39;),
 3020: Int64Index([  33151,   87506,  142398,  197343,  419909,  475782,  531628,
              588349,  646198,  703286,  760057,  816208,  872096,  927753,
              984441, 1041618, 1098984, 1155185, 1213074, 1270806, 1328304,
             1387518, 1448770, 1510117, 1573630],
            dtype=&#39;int64&#39;),
 3023: Int64Index([  30991,   85430,  140415,  195288,  250844,  306117,  361258,
              417756,  473686,  529475,  586278,  643946,  701198,  757900,
              814097,  870046,  925702,  982379, 1039528, 1096875, 1153130,
             1210895, 1268670, 1326228, 1385327, 1446422, 1507856, 1571136],
            dtype=&#39;int64&#39;),
 3025: Int64Index([1521802, 1586166], dtype=&#39;int64&#39;),
 3027: Int64Index([    473,   55650,  110583,  165679,  220529,  276672,  330381,
              386867,  443507,  499599,  555513,  612503,  670868,  727208,
              783669,  839899,  895673,  952443, 1008860, 1066372, 1122664,
             1179286, 1237338, 1295004, 1353227, 1413153, 1475031, 1535844],
            dtype=&#39;int64&#39;),
 3029: Int64Index([   4681,   71161,  126155,  181046,  236367,  291942,  346502,
              402765,  459203,  515067,  571433,  628827,  686502,  743082,
              799405,  855587,  911207,  967781, 1024649, 1082089, 1138440,
             1195620, 1253648, 1311199, 1369827, 1430408, 1492124, 1554217],
            dtype=&#39;int64&#39;),
 3030: Int64Index([  21401,   76221,  131230,  186087,  241552,  296963,  351799,
              407934,  464236,  520083,  576642,  634163,  691672,  748324,
              804584,  860741,  916330,  972940, 1029863, 1087292, 1143666,
             1201100, 1258950, 1316616, 1375334, 1436133, 1497763, 1560272],
            dtype=&#39;int64&#39;),
 3032: Int64Index([  19234,   74120,  129112,  183923,  239314,  294851,  349557,
              405730,  462135,  517990,  574431,  631910,  689524,  746098,
              802357,  858522,  914186,  970745, 1027599, 1085083, 1141445,
             1198743, 1256675, 1314358, 1373026, 1433630, 1495327, 1557659],
            dtype=&#39;int64&#39;),
 3036: Int64Index([  11325,   66246,  121190,  176148,  231292,  287013,  341340,
              397733,  454256,  510139,  566444,  623673,  681583,  738127,
              794516,  850705,  906403,  962974, 1019694, 1077161, 1133498,
             1190543, 1248569, 1306145, 1364776, 1423354, 1485199, 1548404],
            dtype=&#39;int64&#39;),
 3041: Int64Index([  92196,  147008,  201771,  764716,  932466,  988947, 1269371,
             1326913, 1386045, 1447163, 1508570, 1571887],
            dtype=&#39;int64&#39;),
 3042: Int64Index([  16124,   71014,  125998,  180885,  236195,  291793,  346343,
              402609,  459075,  514918,  571272,  628659,  686353,  742933,
              799263,  855437,  911069,  967653, 1024502, 1081954, 1138316,
             1195470, 1253492, 1311065, 1430253, 1491972, 1554039],
            dtype=&#39;int64&#39;),
 3043: Int64Index([   6044,   61080,  115933,  170927,  225938,  281915,  335963,
              392394,  448964,  504996,  561192,  618267,  676316,  732812,
              789204,  845463,  901142,  957846, 1014307, 1071854, 1128230,
             1185057, 1243117, 1359117, 1419093, 1481047, 1542171],
            dtype=&#39;int64&#39;),
 3044: Int64Index([   3230,   58318,  113185,  168274,  223120,  279216,  333113,
              389642,  446200,  502236,  558392,  615392,  673589,  729987,
              786407,  842647,  898376,  953238, 1011529, 1069089, 1125421,
             1182083, 1240207, 1297798, 1354043, 1416041, 1478006, 1538922],
            dtype=&#39;int64&#39;),
 3055: Int64Index([   6669,   61707,  116545,  171553,  226605,  282513,  336625,
              449613,  505618,  561788,  618940,  676931,  733417,  789817,
              846082,  901777,  958439, 1014960, 1072449, 1128856, 1185696,
             1243747, 1359739, 1419783, 1481731, 1542873],
            dtype=&#39;int64&#39;),
 3057: Int64Index([  37795,   92105,  146910,  201669,  257375,  312505,  367978,
              424496,  480269,  536037,  592847,  650855,  707760,  764606,
              820951,  876700,  932362,  988841, 1046105, 1103570, 1159706,
             1217800, 1275448, 1332917, 1392270, 1453725, 1515140, 1578954],
            dtype=&#39;int64&#39;),
 3059: Int64Index([   2348,   57433,  112342,  167437,  222280,  278397,  332249,
              388763,  445324,  501390,  557497,  614508,  672744,  729077,
              785561,  841749,  897521,  954302, 1010683, 1068236, 1124545,
             1181178, 1239292, 1296935, 1355167, 1415120, 1477027, 1537930],
            dtype=&#39;int64&#39;),
 3065: Int64Index([  14232,   69174,  124154,  179102,  234341,  289968,  344418,
              400731,  457237,  513097,  569481,  626760,  684547,  741115,
              797475,  853644,  909297,  965914, 1022716, 1080109, 1136442,
             1193584, 1251558, 1309131, 1367884, 1428276, 1490041, 1551863],
            dtype=&#39;int64&#39;),
 3068: Int64Index([  10038,   64998,  119879,  229993,  285758,  340026,  396447,
              452985,  508862,  565124,  622358,  680284,  736799,  793235,
              849403,  905098,  961681, 1018336, 1075837, 1132227, 1189235,
             1247289, 1304799, 1363404, 1423562, 1485391, 1546912],
            dtype=&#39;int64&#39;),
 3071: Int64Index([  22230,   77028,  132014,  186882,  242339,  297739,  352611,
              408784,  465074,  520894,  577460,  635007,  692524,  749177,
              805412,  861552,  917135,  973779, 1030687, 1088114, 1144455,
             1201965, 1259760, 1317434, 1376199, 1437006, 1498599, 1561206],
            dtype=&#39;int64&#39;),
 3073: Int64Index([  16953,   71820,  126836,  181739,  237061,  292621,  347212,
              403427,  459881,  515731,  572111,  629540,  687181,  743793,
              800088,  856253,  911899,  968477, 1025327, 1082801, 1139128,
             1196302, 1254363, 1311907, 1370531, 1431137, 1492873, 1554999],
            dtype=&#39;int64&#39;),
 3074: Int64Index([  26496,   81199,  136124,  191019,  246542,  301876,  356841,
              413184,  469279,  525115,  581768,  639362,  696781,  753437,
              809678,  865704,  921368,  978014, 1035031, 1092374, 1148678,
             1206296, 1264045, 1321678, 1380634, 1441510, 1503103, 1566055],
            dtype=&#39;int64&#39;),
 3080: Int64Index([1574569], dtype=&#39;int64&#39;),
 3081: Int64Index([  16982,   71856,  126863,  181781,  237100,  292658,  347247,
              403458,  459913,  515769,  572144,  629584,  687219,  743829,
              800121,  856294,  911932,  968519, 1025358, 1082837, 1139174,
             1196344, 1254397, 1311950, 1370565, 1431182, 1492909, 1555045],
            dtype=&#39;int64&#39;),
 3086: Int64Index([   8094,   63103,  117995,  172967,  338074,  394491,  451085,
              563221,  678402,  734880,  791305,  847544,  903226,  959807,
             1016388, 1130337, 1187168, 1245278, 1302858, 1361296, 1421383,
             1483299, 1544635],
            dtype=&#39;int64&#39;),
 3092: Int64Index([  11411,   66331,  121280,  176223,  231381,  287099,  341419,
              397819,  454341,  510232,  566527,  623769,  681682,  738216,
              794606,  850786,  906488,  963043, 1019782, 1077242, 1133585,
             1190630, 1248655, 1306231, 1364870, 1425120, 1486889, 1548512],
            dtype=&#39;int64&#39;),
 3096: Int64Index([   6663,   61703,  116539,  226598,  282508,  336618,  449607,
              505614,  561783,  618931,  676928,  733411,  789813,  846078,
              901773,  958434, 1014953, 1072444, 1128852, 1185691, 1243742,
             1301304, 1359731, 1419778, 1481727, 1542867],
            dtype=&#39;int64&#39;),
 3097: Int64Index([  34040,   88398,  143252,  198159,  253751,  308953,  364216,
              420775,  476683,  532505,  589247,  647099,  704160,  760970,
              817176,  873004,  928663,  985223, 1042434, 1099856, 1156070,
             1213934, 1271738, 1329224, 1388457, 1449719, 1511068, 1574620],
            dtype=&#39;int64&#39;),
 3099: Int64Index([    434,   55608,  110539,  165631,  220489,  330337,  386828,
              443462,  499546,  555469,  612460,  670830,  727166,  783626,
              839855,  895631,  952394, 1008815, 1066327, 1122623, 1179238,
             1237283, 1294954, 1353173, 1413110, 1474978, 1535806],
            dtype=&#39;int64&#39;),
 3100: Int64Index([  47581,  101746,  156509,  211359,  267162,  321998,  377992,
              490097,  545959,  602958,  661049,  774614,  830802,  886400,
              942270,  998766, 1056188, 1113317, 1169659, 1227547, 1285114,
             1342810, 1402425, 1464368, 1525697, 1591428],
            dtype=&#39;int64&#39;),
 3105: Int64Index([116820, 171820, 226852, 1543200], dtype=&#39;int64&#39;),
 3107: Int64Index([ 125819,  180713,  236000,  291612,  346156,  402432,  458900,
              514739,  571104,  628479,  686176,  742762,  799100,  855271,
              910910,  967504, 1024349, 1081785, 1138152, 1195306, 1253311,
             1310884, 1369521, 1430064, 1491791, 1553847],
            dtype=&#39;int64&#39;),
 3113: Int64Index([  23620,   78374,  133378,  188249,  243735,  299114,  353980,
              410217,  466390,  522243,  578872,  636414,  693898,  750580,
              806796,  862912,  918506,  975123, 1032051, 1089483, 1145779,
             1203373, 1261158, 1318801, 1377586, 1438427, 1500061, 1562748],
            dtype=&#39;int64&#39;),
 3119: Int64Index([  34065,   88431,  143282,  198184,  253775,  308977,  364242,
              420803,  476709,  532533,  589279,  647124,  704182,  760999,
              817204,  873030,  928685,  985247, 1042455, 1099877, 1156095,
             1213960, 1271761, 1329245, 1388482, 1449742, 1511092, 1574649],
            dtype=&#39;int64&#39;),
 3121: Int64Index([  32633,   87015,  141928,  196878,  252406,  307635,  362867,
              419366,  475267,  531122,  587844,  645652,  702759,  759512,
              815700,  871584,  927272,  983955, 1041118, 1098462, 1154695,
             1212562, 1270279, 1327790, 1387006, 1448209, 1509560, 1572976],
            dtype=&#39;int64&#39;),
 3124: Int64Index([  15411,   70307,  125280,  180213,  235474,  291097,  345606,
              401854,  458363,  514221,  570631,  627946,  685635,  742235,
              798568,  854734,  910397,  966997, 1023820, 1081234, 1137587,
             1194756, 1252746, 1310325, 1369009, 1429485, 1491228, 1553201],
            dtype=&#39;int64&#39;),
 3126: Int64Index([    693,   55861,  110774,  165881,  220713,  276861,  330607,
              387096,  443722,  499789,  555734,  612716,  671072,  727413,
              783846,  840098,  895863,  952658, 1009054, 1066579, 1122862,
             1179488, 1237559, 1295218, 1353436, 1413366, 1475217, 1536051],
            dtype=&#39;int64&#39;),
 3130: Int64Index([  23687,   78425,  133436,  188302,  243790,  299181,  354042,
              410271,  466445,  522304,  578927,  636472,  693955,  750639,
              806854,  862976,  918570,  975185, 1032116, 1089543, 1145836,
             1203436, 1261213, 1318862, 1377648, 1438493, 1500126, 1562825],
            dtype=&#39;int64&#39;),
 3131: Int64Index([  21784,   76588,  131602,  186449,  241911,  297326,  352182,
              408326,  464620,  520459,  577003,  634548,  692078,  748708,
              804955,  861118,  916712,  973324, 1030247, 1087688, 1201498,
             1259316, 1316991, 1375736, 1436538, 1498148, 1560690],
            dtype=&#39;int64&#39;),
 3132: Int64Index([  42407,   96527,  151359,  206190,  261919,  316861,  372720,
              429188,  484810,  540656,  597461,  655547,  712544,  769193,
              825518,  881269,  936939,  993374, 1050754, 1108100, 1164276,
             1222609, 1280192, 1337557, 1397090, 1458727, 1520092, 1584210],
            dtype=&#39;int64&#39;),
 3134: Int64Index([   9480,   64439,  119310,  174327,  229451,  285226,  339477,
              395890,  452428,  508352,  564566,  621830,  679740,  736247,
              792688,  848849,  904568,  961149, 1017795, 1075315, 1131699,
             1188663, 1246730, 1304245, 1362818, 1422929, 1484773, 1546257],
            dtype=&#39;int64&#39;),
 3139: Int64Index([  10572,   65473,  120383,  175365,  230534,  286256,  340538,
              396950,  453473,  509360,  565657,  622889,  680787,  737316,
              793727,  849910,  905591,  962173, 1018889, 1076365, 1132733,
             1189759, 1247778, 1305345, 1363972, 1424176, 1485938, 1547522],
            dtype=&#39;int64&#39;),
 3141: Int64Index([  17135,   72025,  127010,  181944,  237261,  292828,  347426,
              403613,  460063,  515936,  572298,  629757,  687384,  743991,
              800262,  856473,  912089,  968674, 1025513, 1082989, 1139351,
             1196537, 1254567, 1312155, 1370760, 1431385, 1493088, 1555243],
            dtype=&#39;int64&#39;),
 3142: Int64Index([  51240,  105574,  160351,  215170,  271019,  325823,  381823,
              433147,  488672,  549998,  606979,  665268,  722340,  778667,
              834812,  890346,  946651, 1003085, 1060589, 1117507, 1173770,
             1231738, 1289216, 1347060, 1406742, 1468872, 1530259, 1596406],
            dtype=&#39;int64&#39;),
 3144: Int64Index([  36107,   90420,  145245,  200078,  255698,  310844,  366258,
              422816,  478653,  534438,  591207,  649131,  706145,  762974,
              819249,  875000,  930661,  987190, 1044382, 1101841, 1157982,
             1215999, 1273767, 1331242, 1390498, 1451921, 1513248, 1576947],
            dtype=&#39;int64&#39;),
 3145: Int64Index([1586384], dtype=&#39;int64&#39;),
 3148: Int64Index([  49186,  103386,  158130,  268779,  323570,  491634,  544872,
              601895,  659920,  719783,  776130,  832283,  885345,  943901,
             1000409, 1057795, 1171099, 1229012, 1286625, 1344363, 1404045,
             1466031, 1527317, 1593226],
            dtype=&#39;int64&#39;),
 3150: Int64Index([  32180,   86573,  141535,  196406,  251945,  307210,  362402,
              418908,  530655,  587391,  645169,  702333,  759058,  815255,
              871172,  926842, 1040668, 1154280, 1212105, 1269856, 1327380,
             1386534, 1509097, 1572478],
            dtype=&#39;int64&#39;),
 3158: Int64Index([  11049,   65953,  120900,  175840,  231008,  286726,  341043,
              397445,  453956,  566164,  623372,  681293,  737819,  794214,
              850413,  906109,  962689, 1019398, 1076871, 1133220, 1190275,
             1248291, 1364484, 1424727, 1486459, 1548082],
            dtype=&#39;int64&#39;),
 3159: Int64Index([  27266,   81936,  136882,  191781,  247267,  302600,  357594,
              413969,  470075,  525894,  582526,  640161,  697551,  754214,
              810490,  866458,  922125,  978717, 1035757, 1093175, 1149459,
             1207069, 1264840, 1322473, 1381443, 1442349, 1503912, 1566915],
            dtype=&#39;int64&#39;),
 3165: Int64Index([  40305,   94472,  149299,  204062,  259756,  314794,  370483,
              426950,  482668,  538527,  595307,  653326,  710187,  767035,
              823331,  879112,  934802,  991203, 1048589, 1105956, 1162109,
             1220322, 1277912, 1335332, 1394798, 1456312, 1517747, 1581742],
            dtype=&#39;int64&#39;),
 3168: Int64Index([  47321,  101496,  156267,  211106,  266923,  321763,  377776,
              434309,  489880,  545748,  602767,  660842,  717950,  772327,
              828634,  886173,  940027,  998551, 1055960, 1113093, 1169429,
             1227350, 1284907, 1342608, 1402204, 1464144, 1525471, 1591188],
            dtype=&#39;int64&#39;),
 3170: Int64Index([   7465,   62492,  117390,  172359,  227447,  283323,  337465,
              393819,  450439,  506412,  562579,  619782,  677751,  734229,
              790627,  846880,  902572,  959196, 1015762, 1073278, 1129690,
             1186504, 1244608, 1302161, 1360571, 1420684, 1482595, 1543883],
            dtype=&#39;int64&#39;),
 3171: Int64Index([  16644,   80071,  134969,  189903,  245408,  300735,  355642,
              411963,  468116,  523948,  580606,  638163,  695584,  752279,
              808513,  864551,  920222,  976841, 1015818, 1073328, 1147473,
             1205122, 1262907, 1320522, 1379426, 1440259, 1501883, 1564727],
            dtype=&#39;int64&#39;),
 3176: Int64Index([   2661,   57759,  112635,  167744,  222597,  278691,  332569,
              389065,  445679,  501711,  557819,  614834,  673061,  729428,
              785888,  842064,  897819,  954601, 1010987, 1068542, 1124842,
             1181485, 1239632, 1297237, 1355492, 1415455, 1477375, 1538300],
            dtype=&#39;int64&#39;),
 3182: Int64Index([  28537,   83131,  138078,  192973,  248519,  303809,  358855,
              415279,  471312,  527085,  583774,  641416,  698783,  755454,
              811723,  867712,  923308,  979945, 1036994, 1094440, 1150699,
             1208389, 1266140, 1323768, 1382797, 1443711, 1505264, 1568367],
            dtype=&#39;int64&#39;),
 3184: Int64Index([1122525, 1237191, 1474878, 1535705], dtype=&#39;int64&#39;),
 3185: Int64Index([   4036,   59136,  113989,  169028,  223916,  279996,  333943,
              390411,  447008,  503054,  559197,  616220,  674384,  730831,
              787238,  843475,  899209,  955910, 1012321, 1069929, 1126261,
             1182962, 1241088, 1298665, 1356958, 1416960, 1478920, 1539887],
            dtype=&#39;int64&#39;),
 3189: Int64Index([   4588,   59656,  114529,  224509,  334508,  674902,  843996,
             1012865, 1070430, 1126760, 1183531, 1299229, 1417578, 1479473,
             1540527],
            dtype=&#39;int64&#39;),
 3190: Int64Index([  21957,   76735,  131742,  186605,  242051,  297466,  352337,
              408486,  464789,  520614,  577171,  634714,  692259,  748886,
              861276,  916856,  973486, 1030414, 1087836, 1144188, 1201664,
             1259484, 1375909, 1436714, 1498314, 1560887],
            dtype=&#39;int64&#39;),
 3200: Int64Index([  18100,   72987,  127989,  182843,  238223,  293784,  348435,
              404601,  461051,  516882,  573325,  630779,  688395,  745003,
              801246,  857425,  913073,  969655, 1026488, 1083982, 1140331,
             1197600, 1255544, 1313196, 1371808, 1432449, 1494139, 1556364],
            dtype=&#39;int64&#39;),
 3204: Int64Index([ 891618,  947978, 1004383, 1061926, 1118870, 1175153, 1233172,
             1290595, 1348495, 1408179, 1470388, 1531749, 1598071],
            dtype=&#39;int64&#39;),
 3207: Int64Index([  28613,   83202,  138155,  188639,  244125,  303881,  358926,
              415354,  471382,  527158,  583842,  641487,  694285,  867788,
              918904,  979991, 1037047, 1094517, 1150770, 1203799, 1382872,
             1443789, 1505344, 1568453],
            dtype=&#39;int64&#39;),
 3208: Int64Index([  30633,   85107,  140067,  194947,  250510,  305773,  360911,
              417356,  473330,  529106,  585896,  643579,  700828,  757512,
              813715,  869672,  925318,  981989, 1039155, 1096486, 1152742,
             1210522, 1268258, 1325842, 1384941, 1446008, 1507451, 1570724],
            dtype=&#39;int64&#39;),
 3214: Int64Index([  40638,   94766,  149611,  204381,  260063,  315096,  370788,
              427270,  474134,  529973,  586724,  644436,  701643,  758383,
              814568,  870499,  926155,  982843, 1039982, 1097334, 1153609,
             1211372, 1269143, 1326685, 1385816, 1446919, 1508353, 1571659],
            dtype=&#39;int64&#39;),
 3216: Int64Index([  12693,  342831,  511585,  625148,  683014,  852119,  907765,
              964337, 1021136, 1078565, 1134919, 1249972, 1307551, 1366263,
             1426575, 1488307, 1550088],
            dtype=&#39;int64&#39;),
 3217: Int64Index([  34010,   88363,  143219,  198129,  253725,  308924,  364185,
              420746,  476653,  532473,  589214,  647075,  760941,  817147,
              872975,  928634,  985195, 1042404, 1099826, 1156040, 1213904,
             1271712, 1329189, 1388428, 1449684, 1511031, 1574589],
            dtype=&#39;int64&#39;),
 3222: Int64Index([895479, 952270, 1008641, 1179074, 1353032, 1412956, 1474822,
             1535631],
            dtype=&#39;int64&#39;),
 3227: Int64Index([  15352,   70256,  125226,  180161,  235417,  291042,  345547,
              401803,  458308,  514174,  570581,  627894,  685582,  742192,
              798515,  854680,  910344,  966943, 1023756, 1081181, 1137529,
             1194694, 1252683, 1310274, 1368955, 1429427, 1491169, 1553135],
            dtype=&#39;int64&#39;),
 3231: Int64Index([  14340,   69284,  124262,  179215,  234456,  290075,  344538,
              400857,  457368,  513207,  569608,  626881,  684655,  741232,
              797583,  853761,  909409,  966024, 1080222, 1136572, 1193702,
             1251690, 1309233, 1368011, 1428405, 1490138, 1552001],
            dtype=&#39;int64&#39;),
 3232: Int64Index([899295, 955999, 1012405, 1298764, 1417069, 1479023, 1539990], dtype=&#39;int64&#39;),
 3235: Int64Index([  36465,   90769,  145580,  200421,  256043,  311194,  366629,
              478958,  534783,  649476,  706453,  763318,  819568,  875366,
              930994,  987533, 1044738, 1102174, 1158351, 1216370, 1274129,
             1331600, 1390876, 1452296, 1513660, 1577380],
            dtype=&#39;int64&#39;),
 3236: Int64Index([  33503,   87821,  142708,  197639,  253249,  308436,  363727,
              420227,  476116,  531947,  588669,  646517,  703596,  760386,
              816548,  872424,  928067,  984750, 1041905, 1099310, 1155514,
             1213380, 1271132, 1328641, 1387848, 1449115, 1510456, 1573995],
            dtype=&#39;int64&#39;),
 3237: Int64Index([   1456,   56590,  111506,  166608,  221416,  277580,  331363,
              387870,  444464,  500546,  556571,  613572,  671876,  728202,
              784658,  840882,  896632,  953435, 1009806, 1067357, 1123665,
             1180291, 1238352, 1296005, 1354240, 1414189, 1476098, 1536949],
            dtype=&#39;int64&#39;),
 3238: Int64Index([  48899,  103072,  157829,  212638,  268474,  323258,  379224,
              435805,  491325,  547177,  604219,  662321,  719477,  775842,
              831998,  855625,  943567, 1000068, 1057480, 1114538, 1170790,
             1228696, 1286321, 1344033, 1403736, 1465706, 1527016, 1592879],
            dtype=&#39;int64&#39;),
 3241: Int64Index([  19465,   74348,  129348,  349833,  405970,  462390,  518239,
              574684,  632163,  689759,  746357,  802605,  858790,  914441,
              970981, 1027826, 1085329, 1141689, 1198995, 1256930, 1314600,
             1373281, 1433910, 1495606, 1557946],
            dtype=&#39;int64&#39;),
 3242: Int64Index([  26459,   81159,  190979,  301838,  356804,  469247,  525075,
              639326,  696736,  753404,  809642,  865668,  921331,  977974,
             1034993, 1092332, 1148634, 1264011, 1321644, 1380593, 1441470,
             1503063, 1566014],
            dtype=&#39;int64&#39;),
 3248: Int64Index([  21986,   76768,  131771,  186635,  242083,  297484,  352361,
              408513,  464815,  520637,  577201,  634738,  748911,  805151,
              861300,  973523, 1030445, 1087859, 1144211, 1201692, 1259507,
             1317174, 1375938, 1436738, 1498336, 1560914],
            dtype=&#39;int64&#39;),
 3250: Int64Index([   2372,   57463,  112371,  167460,  222303,  278426,  332283,
              388791,  445350,  501416,  557525,  614535,  672770,  729115,
              785589,  841773,  897547,  954330, 1010710, 1068269, 1124570,
             1181212, 1239321, 1296968, 1355187, 1415152, 1477068, 1537964],
            dtype=&#39;int64&#39;),
 3253: Int64Index([396590, 1547085], dtype=&#39;int64&#39;),
 3255: Int64Index([  52582,  106982,  161851,  216671,  272638,  327382,  383533,
              440184,  495927,  551727,  608712,  667047,  724162,  780524,
              836579,  948572, 1004963, 1062543, 1119479, 1175777, 1233817,
             1291219, 1349121, 1408835, 1471033, 1532407, 1598763],
            dtype=&#39;int64&#39;),
 3261: Int64Index([  46552,  106118,  160933,  215734,  271612,  326423,  382479,
              439160,  494843,  550667,  607645,  665961,  723034,  779384,
              835526,  891056,  947364, 1003800, 1061327, 1118249, 1174522,
             1232512, 1289975, 1347846, 1407546, 1469706, 1531081, 1597298],
            dtype=&#39;int64&#39;),
 3262: Int64Index([    169,   55349,  110305,  165407,  220235,  276409,  330077,
              386572,  443227,  499308,  555243,  612202,  670605,  726933,
              783394,  839637,  895362,  952172, 1008542, 1066076, 1122365,
             1178955, 1237020, 1294695, 1352914, 1412830, 1474699, 1535489],
            dtype=&#39;int64&#39;),
 3263: Int64Index([  50958,  105255,  160061,  214855,  270687,  325478,  438168,
              493700,  549626,  664859,  721950,  778264,  889942,  946243,
             1002697, 1060173, 1117114, 1173349, 1231294, 1288798, 1346646,
             1406321, 1468409, 1529767, 1595896],
            dtype=&#39;int64&#39;),
 3267: Int64Index([  36984,   91292,  146132,  200935,  256593,  311763,  367173,
              423683,  479461,  535291,  592070,  650052,  706990,  763846,
              820140,  875936,  931565,  988065, 1045316, 1102760, 1158909,
             1216957, 1274661, 1332123, 1391481, 1452901, 1514305, 1578048],
            dtype=&#39;int64&#39;),
 3269: Int64Index([  13882,   68817,  123795,  178760,  233970,  289604,  344053,
              400369,  456901,  512761,  569133,  626406,  684181,  740757,
              797100,  853279,  908941,  965554, 1022359, 1079748, 1136080,
             1193218, 1251190, 1308768, 1367508, 1427875, 1489630, 1551451],
            dtype=&#39;int64&#39;),
 3277: Int64Index([1467390, 1528657, 1594732], dtype=&#39;int64&#39;),
 3278: Int64Index([   5417,   60461,  115311,  170294,  225328,  281292,  335314,
              391784,  448317,  504356,  560507,  617618,  675677,  732168,
              788586,  844772,  900527,  957214, 1013654, 1071198, 1127541,
             1184358, 1242443, 1300046, 1358448, 1418418, 1480343, 1541447],
            dtype=&#39;int64&#39;),
 3282: Int64Index([1469132, 1530532, 1596684], dtype=&#39;int64&#39;),
 3283: Int64Index([  21139,   75984,  130987,  185829,  241293,  296696,  351517,
              407661,  463974,  519824,  576380,  633880,  691405,  748055,
              788203,  860481,  916058,  972687, 1029597, 1087022, 1143402,
             1200817, 1270568, 1375069, 1435840, 1497500, 1559968],
            dtype=&#39;int64&#39;),
 3288: Int64Index([1554783], dtype=&#39;int64&#39;),
 3290: Int64Index([1548294], dtype=&#39;int64&#39;),
 3293: Int64Index([  26857,   81534,  136474,  191350,  246842,  302189,  357173,
              413534,  469642,  525460,  582104,  639707,  697116,  753781,
              810029,  866026,  921686, 1092718, 1149018, 1206630, 1264393,
             1322043, 1381004, 1441873, 1503445, 1566436],
            dtype=&#39;int64&#39;),
 3296: Int64Index([  16727,   71596,  126604,  181515,  236813,  292399,  346975,
              403203,  459652,  515506,  571871,  629314,  686949,  743555,
              799860,  856032,  911660,  968235, 1025100, 1082553, 1138903,
             1196076, 1254121, 1311666, 1370305, 1430891, 1492627, 1554742],
            dtype=&#39;int64&#39;),
 3297: Int64Index([ 632523,  690115,  746726,  802989,  859147,  914802,  971342,
             1028200, 1085714, 1142076, 1199396, 1257331, 1314990, 1373685,
             1434330, 1496025, 1558423],
            dtype=&#39;int64&#39;),
 3304: Int64Index([  46655,  100809,  155614,  210438,  266243,  321080,  377119,
              433623,  489166,  545005,  602007,  660058,  717034,  773571,
              829858,  885480,  941320,  997795, 1055191, 1112268, 1168619,
             1226678, 1284215, 1341856, 1401463, 1463414, 1524683, 1590069],
            dtype=&#39;int64&#39;),
 3306: Int64Index([  11046,   65950,  120897,  175837,  231005,  286723,  341040,
              397442,  453953,  906106,  962686, 1076868, 1133217, 1190272,
             1248288, 1305851, 1364481, 1424724, 1486456, 1548079],
            dtype=&#39;int64&#39;),
 3310: Int64Index([1180681, 1238772, 1296427, 1354635, 1414615, 1476508, 1537375], dtype=&#39;int64&#39;),
 3317: Int64Index([   9873,   64822,  174700,  229815,  285587,  339841,  396267,
              452798,  508713,  564949,  622209,  680115,  736613,  793061,
              849225,  904935, 1018160, 1189056, 1247110, 1304625, 1363229,
             1423343, 1485188, 1546688],
            dtype=&#39;int64&#39;),
 3318: Int64Index([  20820,   75699,  130694,  185528,  240974,  296378,  351214,
              407326,  463685,  519532,  576058,  633548,  691102,  747731,
              803977,  860155,  915745,  972350, 1029249, 1086695, 1143069,
             1200470, 1258334, 1316017, 1374733, 1435449, 1497155, 1559580],
            dtype=&#39;int64&#39;),
 3320: Int64Index([  37593,   91908,  146726,  257179,  312322,  367782,  424294,
              480080,  535847,  592661,  650663,  707587,  764419,  820748,
              876510,  932173, 1045919, 1103378, 1159508, 1217613, 1275248,
             1332728, 1453527, 1514942, 1578760],
            dtype=&#39;int64&#39;),
 3321: Int64Index([  31415,   85865,  140837,  195686,  251232,  306524,  361670,
              418192,  474093,  529934,  586689,  644398,  701607,  758345,
              870462,  926119,  982806, 1039944, 1097297, 1153572, 1211332,
             1269106, 1326647, 1385777, 1446881, 1508316, 1571621],
            dtype=&#39;int64&#39;),
 3329: Int64Index([  23575,   78324,  133330,  188200,  243681,  299064,  353927,
              410154,  466340,  578822,  636366,  750526,  806745,  862858,
              918444,  975073, 1089429, 1145719, 1203317, 1261103, 1318749,
             1377534, 1438375, 1500011, 1562693],
            dtype=&#39;int64&#39;),
 3330: Int64Index([750841, 1211284, 1276980, 1563056], dtype=&#39;int64&#39;),
 ...}</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_cnt</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">({</span><span class="s1">&#39;day_cnt&#39;</span><span class="p">:</span> <span class="n">grouped_acc</span><span class="o">.</span><span class="n">size</span><span class="p">()})</span>
<span class="n">df_day_cnt</span> <span class="o">=</span> <span class="n">df_day_cnt</span><span class="o">.</span><span class="n">reset_index</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">df_day_temp</span><span class="p">,</span> <span class="n">df_day_cnt</span><span class="p">,</span> <span class="n">how</span> <span class="o">=</span> <span class="s1">&#39;outer&#39;</span><span class="p">,</span> <span class="n">on</span> <span class="o">=</span> <span class="s1">&#39;acc_id&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[21]:</div>



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
      <th>day_first</th>
      <th>day_last</th>
      <th>day_cnt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>75001</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>1</th>
      <td>75711</td>
      <td>1</td>
      <td>27.0</td>
      <td>14</td>
    </tr>
    <tr>
      <th>2</th>
      <td>72230</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
    </tr>
    <tr>
      <th>3</th>
      <td>34253</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>4</th>
      <td>83200</td>
      <td>1</td>
      <td>27.0</td>
      <td>25</td>
    </tr>
    <tr>
      <th>5</th>
      <td>13896</td>
      <td>1</td>
      <td>26.0</td>
      <td>20</td>
    </tr>
    <tr>
      <th>6</th>
      <td>54399</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>7</th>
      <td>67385</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>8</th>
      <td>21932</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>9</th>
      <td>30937</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>10</th>
      <td>53141</td>
      <td>1</td>
      <td>27.0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>11</th>
      <td>94123</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>12</th>
      <td>76110</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>13</th>
      <td>128757</td>
      <td>1</td>
      <td>27.0</td>
      <td>24</td>
    </tr>
    <tr>
      <th>14</th>
      <td>91114</td>
      <td>1</td>
      <td>27.0</td>
      <td>21</td>
    </tr>
    <tr>
      <th>15</th>
      <td>32521</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
    </tr>
    <tr>
      <th>16</th>
      <td>20575</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>17</th>
      <td>9300</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
    </tr>
    <tr>
      <th>18</th>
      <td>15556</td>
      <td>1</td>
      <td>27.0</td>
      <td>24</td>
    </tr>
    <tr>
      <th>19</th>
      <td>69182</td>
      <td>1</td>
      <td>27.0</td>
      <td>26</td>
    </tr>
    <tr>
      <th>20</th>
      <td>87786</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>21</th>
      <td>58956</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>22</th>
      <td>3383</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>23</th>
      <td>92874</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>24</th>
      <td>97731</td>
      <td>1</td>
      <td>26.0</td>
      <td>24</td>
    </tr>
    <tr>
      <th>25</th>
      <td>121129</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
    </tr>
    <tr>
      <th>26</th>
      <td>32541</td>
      <td>1</td>
      <td>27.0</td>
      <td>24</td>
    </tr>
    <tr>
      <th>27</th>
      <td>103844</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>28</th>
      <td>3962</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
    </tr>
    <tr>
      <th>29</th>
      <td>37214</td>
      <td>1</td>
      <td>27.0</td>
      <td>19</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>39970</th>
      <td>123223</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39971</th>
      <td>52885</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39972</th>
      <td>105395</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39973</th>
      <td>58765</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39974</th>
      <td>30358</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39975</th>
      <td>127132</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39976</th>
      <td>79097</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39977</th>
      <td>26795</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39978</th>
      <td>39550</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39979</th>
      <td>90754</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39980</th>
      <td>78420</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39981</th>
      <td>105828</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39982</th>
      <td>5279</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39983</th>
      <td>8508</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39984</th>
      <td>22772</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39985</th>
      <td>36308</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39986</th>
      <td>112234</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39987</th>
      <td>98507</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39988</th>
      <td>26110</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39989</th>
      <td>30604</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39990</th>
      <td>85587</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39991</th>
      <td>85033</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39992</th>
      <td>110981</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39993</th>
      <td>117125</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39994</th>
      <td>43726</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39995</th>
      <td>31169</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39996</th>
      <td>69980</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39997</th>
      <td>94182</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39998</th>
      <td>27017</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39999</th>
      <td>1591</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>40000 rows × 4 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span><span class="p">[</span><span class="s1">&#39;day_rate&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df_day_temp</span><span class="p">[</span><span class="s1">&#39;day_cnt&#39;</span><span class="p">]</span> <span class="o">/</span> <span class="mf">28.</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_day_temp</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[23]:</div>



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
      <th>day_first</th>
      <th>day_last</th>
      <th>day_cnt</th>
      <th>day_rate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>75001</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>75711</td>
      <td>1</td>
      <td>27.0</td>
      <td>14</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>72230</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
      <td>0.964286</td>
    </tr>
    <tr>
      <th>3</th>
      <td>34253</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>83200</td>
      <td>1</td>
      <td>27.0</td>
      <td>25</td>
      <td>0.892857</td>
    </tr>
    <tr>
      <th>5</th>
      <td>13896</td>
      <td>1</td>
      <td>26.0</td>
      <td>20</td>
      <td>0.714286</td>
    </tr>
    <tr>
      <th>6</th>
      <td>54399</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>67385</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>21932</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>30937</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>53141</td>
      <td>1</td>
      <td>27.0</td>
      <td>7</td>
      <td>0.250000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>94123</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>76110</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>128757</td>
      <td>1</td>
      <td>27.0</td>
      <td>24</td>
      <td>0.857143</td>
    </tr>
    <tr>
      <th>14</th>
      <td>91114</td>
      <td>1</td>
      <td>27.0</td>
      <td>21</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>32521</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
      <td>0.964286</td>
    </tr>
    <tr>
      <th>16</th>
      <td>20575</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>9300</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
      <td>0.964286</td>
    </tr>
    <tr>
      <th>18</th>
      <td>15556</td>
      <td>1</td>
      <td>27.0</td>
      <td>24</td>
      <td>0.857143</td>
    </tr>
    <tr>
      <th>19</th>
      <td>69182</td>
      <td>1</td>
      <td>27.0</td>
      <td>26</td>
      <td>0.928571</td>
    </tr>
    <tr>
      <th>20</th>
      <td>87786</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>58956</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>3383</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>92874</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>97731</td>
      <td>1</td>
      <td>26.0</td>
      <td>24</td>
      <td>0.857143</td>
    </tr>
    <tr>
      <th>25</th>
      <td>121129</td>
      <td>1</td>
      <td>27.0</td>
      <td>27</td>
      <td>0.964286</td>
    </tr>
    <tr>
      <th>26</th>
      <td>32541</td>
      <td>1</td>
      <td>27.0</td>
      <td>24</td>
      <td>0.857143</td>
    </tr>
    <tr>
      <th>27</th>
      <td>103844</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>28</th>
      <td>3962</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>37214</td>
      <td>1</td>
      <td>27.0</td>
      <td>19</td>
      <td>0.678571</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>39970</th>
      <td>123223</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39971</th>
      <td>52885</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39972</th>
      <td>105395</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39973</th>
      <td>58765</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39974</th>
      <td>30358</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39975</th>
      <td>127132</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39976</th>
      <td>79097</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39977</th>
      <td>26795</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39978</th>
      <td>39550</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39979</th>
      <td>90754</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39980</th>
      <td>78420</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39981</th>
      <td>105828</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39982</th>
      <td>5279</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39983</th>
      <td>8508</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39984</th>
      <td>22772</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39985</th>
      <td>36308</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39986</th>
      <td>112234</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39987</th>
      <td>98507</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39988</th>
      <td>26110</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39989</th>
      <td>30604</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39990</th>
      <td>85587</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39991</th>
      <td>85033</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39992</th>
      <td>110981</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39993</th>
      <td>117125</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39994</th>
      <td>43726</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39995</th>
      <td>31169</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39996</th>
      <td>69980</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39997</th>
      <td>94182</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39998</th>
      <td>27017</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>39999</th>
      <td>1591</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
  </tbody>
</table>
<p>40000 rows × 5 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#----------------------------------------------------------------------------</span>
<span class="c1"># 여기부터 lgb</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># sep 붙은 것들이 64를 제외한 것들</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[26]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># day별로 나눈 헌형이 파일을 썼음.</span>
<span class="c1"># week는 효과가 없는 것으로 판단됨.</span>
<span class="n">df_temp</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;../8-11일/new_merged_with_label.csv&#39;</span><span class="p">,</span> <span class="n">dtype</span> <span class="o">=</span> <span class="nb">float</span><span class="p">,</span> <span class="n">engine</span> <span class="o">=</span> <span class="s1">&#39;python&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">],</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
<span class="n">df_temp</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">df_temp</span><span class="p">,</span> <span class="n">df_day_temp</span><span class="p">,</span> <span class="n">how</span> <span class="o">=</span> <span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">on</span> <span class="o">=</span> <span class="s1">&#39;acc_id&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span> <span class="o">=</span> <span class="n">df_temp</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[29]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[29]:</div>



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
      <th>day</th>
      <th>acc_id</th>
      <th>day_npc_kill</th>
      <th>day_playtime</th>
      <th>day_solo_exp</th>
      <th>day_party_exp</th>
      <th>day_quest_exp</th>
      <th>day_boss_monster</th>
      <th>day_death</th>
      <th>day_revive</th>
      <th>...</th>
      <th>day_non_combat_play_time</th>
      <th>day_amount_spent</th>
      <th>day_item_amount</th>
      <th>day_item_price</th>
      <th>survival_time</th>
      <th>amount_spent</th>
      <th>day_first</th>
      <th>day_last</th>
      <th>day_cnt</th>
      <th>day_rate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.737490</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>3.053204e-06</td>
      <td>3.394319</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.405864</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>3.481725e-01</td>
      <td>0.198292</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>8.302572e-07</td>
      <td>1.504466</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.074617</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.050871</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.803853</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.403494</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.186889</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.410604</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.168262</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.659276</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.220994</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.005375</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.043031</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>5.356498e-08</td>
      <td>0.087230</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.043854</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>22.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.784892</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.075620</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>24.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>6.427798e-07</td>
      <td>1.367792</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>25.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>26.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>27.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>8.034747e-08</td>
      <td>0.225465</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>27</th>
      <td>28.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1.0</td>
      <td>8.0</td>
      <td>3.089008</td>
      <td>0.469284</td>
      <td>8.586580</td>
      <td>0.0</td>
      <td>0.374342</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000927</td>
      <td>1.056123</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.020310</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2.0</td>
      <td>8.0</td>
      <td>4.762727</td>
      <td>0.564089</td>
      <td>3.790739</td>
      <td>0.0</td>
      <td>0.006926</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.001158</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.020310</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
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
      <td>...</td>
    </tr>
    <tr>
      <th>947489</th>
      <td>28.0</td>
      <td>126332.0</td>
      <td>1.274604</td>
      <td>1.654344</td>
      <td>0.101286</td>
      <td>0.0</td>
      <td>0.003463</td>
      <td>1.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.365919</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>27.0</td>
      <td>0.067984</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947490</th>
      <td>28.0</td>
      <td>126336.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947491</th>
      <td>28.0</td>
      <td>126509.0</td>
      <td>0.004049</td>
      <td>0.085324</td>
      <td>0.000952</td>
      <td>0.0</td>
      <td>0.008919</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.173470</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.762857</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947492</th>
      <td>28.0</td>
      <td>126524.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947493</th>
      <td>28.0</td>
      <td>126553.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947494</th>
      <td>28.0</td>
      <td>126676.0</td>
      <td>0.000000</td>
      <td>0.018961</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000116</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947495</th>
      <td>28.0</td>
      <td>126697.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.005444</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947496</th>
      <td>28.0</td>
      <td>126831.0</td>
      <td>0.000337</td>
      <td>0.097175</td>
      <td>0.000006</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.035204</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947497</th>
      <td>28.0</td>
      <td>127100.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947498</th>
      <td>28.0</td>
      <td>127132.0</td>
      <td>0.061065</td>
      <td>0.149318</td>
      <td>0.044988</td>
      <td>0.0</td>
      <td>0.201739</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947499</th>
      <td>28.0</td>
      <td>127226.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015753</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947500</th>
      <td>28.0</td>
      <td>127436.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.005444</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947501</th>
      <td>28.0</td>
      <td>127472.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.002317</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947502</th>
      <td>28.0</td>
      <td>127497.0</td>
      <td>0.069837</td>
      <td>0.182499</td>
      <td>0.063027</td>
      <td>0.0</td>
      <td>5.307253</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000463</td>
      <td>0.000000</td>
      <td>8.034747e-07</td>
      <td>0.005268</td>
      <td>1.0</td>
      <td>0.328110</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947503</th>
      <td>28.0</td>
      <td>127508.0</td>
      <td>0.672726</td>
      <td>0.993081</td>
      <td>0.315336</td>
      <td>0.0</td>
      <td>0.134606</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947504</th>
      <td>28.0</td>
      <td>128157.0</td>
      <td>0.043184</td>
      <td>0.139837</td>
      <td>0.010905</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947505</th>
      <td>28.0</td>
      <td>128245.0</td>
      <td>0.000000</td>
      <td>0.009480</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.008571</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947506</th>
      <td>28.0</td>
      <td>128400.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.017838</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947507</th>
      <td>28.0</td>
      <td>128438.0</td>
      <td>0.000000</td>
      <td>0.009480</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947508</th>
      <td>28.0</td>
      <td>128791.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947509</th>
      <td>28.0</td>
      <td>129077.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.022471</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947510</th>
      <td>28.0</td>
      <td>129218.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947511</th>
      <td>28.0</td>
      <td>129235.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947512</th>
      <td>28.0</td>
      <td>129295.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.017838</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947513</th>
      <td>28.0</td>
      <td>129484.0</td>
      <td>0.024628</td>
      <td>0.047402</td>
      <td>0.277755</td>
      <td>0.0</td>
      <td>0.011523</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>...</td>
      <td>0.000232</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947514</th>
      <td>28.0</td>
      <td>129540.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.022471</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947515</th>
      <td>28.0</td>
      <td>129613.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947516</th>
      <td>28.0</td>
      <td>129690.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.005097</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947517</th>
      <td>28.0</td>
      <td>129761.0</td>
      <td>0.000000</td>
      <td>0.078214</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.437207e-06</td>
      <td>0.710871</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947518</th>
      <td>28.0</td>
      <td>130104.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
  </tbody>
</table>
<p>947519 rows × 41 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[30]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span><span class="o">.</span><span class="n">columns</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[30]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Index([&#39;day&#39;, &#39;acc_id&#39;, &#39;day_npc_kill&#39;, &#39;day_playtime&#39;, &#39;day_solo_exp&#39;,
       &#39;day_party_exp&#39;, &#39;day_quest_exp&#39;, &#39;day_boss_monster&#39;, &#39;day_death&#39;,
       &#39;day_revive&#39;, &#39;day_exp_recovery&#39;, &#39;day_fishing&#39;, &#39;day_private_shop&#39;,
       &#39;day_game_money_change&#39;, &#39;day_enchant_count&#39;, &#39;day_level&#39;,
       &#39;day_pledge_cnt&#39;, &#39;day_combat_random_attacker_cnt&#39;,
       &#39;day_combat_random_defender_cnt&#39;, &#39;day_temp_cnt_x&#39;,
       &#39;day_same_pledge_cnt_x&#39;, &#39;day_etc_cnt_x&#39;, &#39;day_num_opponent&#39;,
       &#39;day_play_char_cnt_mean&#39;, &#39;day_combat_char_cnt_mean&#39;,
       &#39;day_random_attacker_cnt&#39;, &#39;day_random_defender_cnt&#39;,
       &#39;day_same_pledge_cnt_y&#39;, &#39;day_temp_cnt_y&#39;, &#39;day_etc_cnt_y&#39;,
       &#39;day_combat_play_time&#39;, &#39;day_non_combat_play_time&#39;, &#39;day_amount_spent&#39;,
       &#39;day_item_amount&#39;, &#39;day_item_price&#39;, &#39;survival_time&#39;, &#39;amount_spent&#39;,
       &#39;day_first&#39;, &#39;day_last&#39;, &#39;day_cnt&#39;, &#39;day_rate&#39;],
      dtype=&#39;object&#39;)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[31]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">get_log</span><span class="p">(</span><span class="n">row</span><span class="p">):</span>
    <span class="n">row</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">log</span><span class="p">(</span><span class="n">row</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[32]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;day_npc_kill&#39;</span><span class="p">,</span> <span class="s1">&#39;day_solo_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;day_quest_exp&#39;</span><span class="p">,</span><span class="s1">&#39;day_party_exp&#39;</span><span class="p">,</span> <span class="s1">&#39;day_boss_monster&#39;</span><span class="p">,</span><span class="s1">&#39;day_exp_recovery&#39;</span><span class="p">,</span> <span class="s1">&#39;day_fishing&#39;</span><span class="p">,</span><span class="s1">&#39;day_private_shop&#39;</span> <span class="p">],</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>
<span class="c1"># my 전처리.</span>
<span class="c1">#-------------------------------------------</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[32]:</div>



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
      <th>day</th>
      <th>acc_id</th>
      <th>day_playtime</th>
      <th>day_death</th>
      <th>day_revive</th>
      <th>day_game_money_change</th>
      <th>day_enchant_count</th>
      <th>day_level</th>
      <th>day_pledge_cnt</th>
      <th>day_combat_random_attacker_cnt</th>
      <th>...</th>
      <th>day_non_combat_play_time</th>
      <th>day_amount_spent</th>
      <th>day_item_amount</th>
      <th>day_item_price</th>
      <th>survival_time</th>
      <th>amount_spent</th>
      <th>day_first</th>
      <th>day_last</th>
      <th>day_cnt</th>
      <th>day_rate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>2.737490</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>1.022652</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>3.053204e-06</td>
      <td>3.394319</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.0</td>
      <td>2.0</td>
      <td>3.405864</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-1.042002</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>3.481725e-01</td>
      <td>0.198292</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.450366</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>8.302572e-07</td>
      <td>1.504466</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.007215</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.015365</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.074617</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.003792</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.050871</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.363492</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8.0</td>
      <td>2.0</td>
      <td>2.803853</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.006605</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9.0</td>
      <td>2.0</td>
      <td>3.403494</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.010956</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.182357</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.022643</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.091739</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.186889</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.007243</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14.0</td>
      <td>2.0</td>
      <td>3.410604</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.043786</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.168262</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15.0</td>
      <td>2.0</td>
      <td>2.659276</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.006308</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16.0</td>
      <td>2.0</td>
      <td>3.220994</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.005288</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.005375</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.007158</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.005761</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.043031</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.019190</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>5.356498e-08</td>
      <td>0.087230</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.063430</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.043854</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.006988</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>22.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.007257</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23.0</td>
      <td>2.0</td>
      <td>2.784892</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.106340</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.075620</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>24.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.407511</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>6.427798e-07</td>
      <td>1.367792</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>25.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.034699</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>26.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.036085</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>27.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.054837</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>8.034747e-08</td>
      <td>0.225465</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>27</th>
      <td>28.0</td>
      <td>2.0</td>
      <td>3.412974</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.016598</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1.0</td>
      <td>8.0</td>
      <td>0.469284</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.731042</td>
      <td>0.0</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000927</td>
      <td>1.056123</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.020310</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2.0</td>
      <td>8.0</td>
      <td>0.564089</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.189372</td>
      <td>0.0</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.001158</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.020310</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
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
      <td>...</td>
    </tr>
    <tr>
      <th>947489</th>
      <td>28.0</td>
      <td>126332.0</td>
      <td>1.654344</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.027048</td>
      <td>0.0</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.365919</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>27.0</td>
      <td>0.067984</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947490</th>
      <td>28.0</td>
      <td>126336.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947491</th>
      <td>28.0</td>
      <td>126509.0</td>
      <td>0.085324</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.173470</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.762857</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947492</th>
      <td>28.0</td>
      <td>126524.0</td>
      <td>0.002370</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947493</th>
      <td>28.0</td>
      <td>126553.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947494</th>
      <td>28.0</td>
      <td>126676.0</td>
      <td>0.018961</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000116</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947495</th>
      <td>28.0</td>
      <td>126697.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.005444</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947496</th>
      <td>28.0</td>
      <td>126831.0</td>
      <td>0.097175</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.743850</td>
      <td>0.0</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.035204</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947497</th>
      <td>28.0</td>
      <td>127100.0</td>
      <td>0.002370</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947498</th>
      <td>28.0</td>
      <td>127132.0</td>
      <td>0.149318</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000053</td>
      <td>0.0</td>
      <td>8.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947499</th>
      <td>28.0</td>
      <td>127226.0</td>
      <td>0.002370</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.015753</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947500</th>
      <td>28.0</td>
      <td>127436.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.005444</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947501</th>
      <td>28.0</td>
      <td>127472.0</td>
      <td>0.002370</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>15.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.002317</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947502</th>
      <td>28.0</td>
      <td>127497.0</td>
      <td>0.182499</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.001599</td>
      <td>0.0</td>
      <td>14.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000463</td>
      <td>0.000000</td>
      <td>8.034747e-07</td>
      <td>0.005268</td>
      <td>1.0</td>
      <td>0.328110</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947503</th>
      <td>28.0</td>
      <td>127508.0</td>
      <td>0.993081</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.001559</td>
      <td>0.0</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947504</th>
      <td>28.0</td>
      <td>128157.0</td>
      <td>0.139837</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>-0.000859</td>
      <td>0.0</td>
      <td>15.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947505</th>
      <td>28.0</td>
      <td>128245.0</td>
      <td>0.009480</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>11.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.008571</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947506</th>
      <td>28.0</td>
      <td>128400.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.017838</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947507</th>
      <td>28.0</td>
      <td>128438.0</td>
      <td>0.009480</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947508</th>
      <td>28.0</td>
      <td>128791.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947509</th>
      <td>28.0</td>
      <td>129077.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.022471</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947510</th>
      <td>28.0</td>
      <td>129218.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947511</th>
      <td>28.0</td>
      <td>129235.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947512</th>
      <td>28.0</td>
      <td>129295.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.017838</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947513</th>
      <td>28.0</td>
      <td>129484.0</td>
      <td>0.047402</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>0.000006</td>
      <td>0.0</td>
      <td>11.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000232</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947514</th>
      <td>28.0</td>
      <td>129540.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.022471</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947515</th>
      <td>28.0</td>
      <td>129613.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947516</th>
      <td>28.0</td>
      <td>129690.0</td>
      <td>0.002370</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.005097</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947517</th>
      <td>28.0</td>
      <td>129761.0</td>
      <td>0.078214</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.003566</td>
      <td>0.0</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.437207e-06</td>
      <td>0.710871</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947518</th>
      <td>28.0</td>
      <td>130104.0</td>
      <td>0.004740</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
  </tbody>
</table>
<p>947519 rows × 33 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[33]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[33]:</div>



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
      <th>day</th>
      <th>acc_id</th>
      <th>day_npc_kill</th>
      <th>day_playtime</th>
      <th>day_solo_exp</th>
      <th>day_party_exp</th>
      <th>day_quest_exp</th>
      <th>day_boss_monster</th>
      <th>day_death</th>
      <th>day_revive</th>
      <th>...</th>
      <th>day_non_combat_play_time</th>
      <th>day_amount_spent</th>
      <th>day_item_amount</th>
      <th>day_item_price</th>
      <th>survival_time</th>
      <th>amount_spent</th>
      <th>day_first</th>
      <th>day_last</th>
      <th>day_cnt</th>
      <th>day_rate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.737490</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>3.053204e-06</td>
      <td>3.394319</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.405864</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>3.481725e-01</td>
      <td>0.198292</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>8.302572e-07</td>
      <td>1.504466</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.074617</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.050871</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.803853</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.403494</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.186889</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.410604</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.168262</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.659276</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.220994</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.005375</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.043031</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>5.356498e-08</td>
      <td>0.087230</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.043854</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>22.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>2.784892</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.075620</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>24.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>6.427798e-07</td>
      <td>1.367792</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>25.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>26.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>27.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>8.034747e-08</td>
      <td>0.225465</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>27</th>
      <td>28.0</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>3.412974</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.000000</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1.0</td>
      <td>8.0</td>
      <td>3.089008</td>
      <td>0.469284</td>
      <td>8.586580</td>
      <td>0.0</td>
      <td>0.374342</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000927</td>
      <td>1.056123</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.020310</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2.0</td>
      <td>8.0</td>
      <td>4.762727</td>
      <td>0.564089</td>
      <td>3.790739</td>
      <td>0.0</td>
      <td>0.006926</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.001158</td>
      <td>0.000000</td>
      <td>2.678249e-08</td>
      <td>0.000000</td>
      <td>64.0</td>
      <td>0.020310</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
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
      <td>...</td>
    </tr>
    <tr>
      <th>947489</th>
      <td>28.0</td>
      <td>126332.0</td>
      <td>1.274604</td>
      <td>1.654344</td>
      <td>0.101286</td>
      <td>0.0</td>
      <td>0.003463</td>
      <td>1.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.365919</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>27.0</td>
      <td>0.067984</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947490</th>
      <td>28.0</td>
      <td>126336.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947491</th>
      <td>28.0</td>
      <td>126509.0</td>
      <td>0.004049</td>
      <td>0.085324</td>
      <td>0.000952</td>
      <td>0.0</td>
      <td>0.008919</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.173470</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.762857</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947492</th>
      <td>28.0</td>
      <td>126524.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947493</th>
      <td>28.0</td>
      <td>126553.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947494</th>
      <td>28.0</td>
      <td>126676.0</td>
      <td>0.000000</td>
      <td>0.018961</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000116</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947495</th>
      <td>28.0</td>
      <td>126697.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.005444</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947496</th>
      <td>28.0</td>
      <td>126831.0</td>
      <td>0.000337</td>
      <td>0.097175</td>
      <td>0.000006</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.035204</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947497</th>
      <td>28.0</td>
      <td>127100.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947498</th>
      <td>28.0</td>
      <td>127132.0</td>
      <td>0.061065</td>
      <td>0.149318</td>
      <td>0.044988</td>
      <td>0.0</td>
      <td>0.201739</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947499</th>
      <td>28.0</td>
      <td>127226.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015753</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947500</th>
      <td>28.0</td>
      <td>127436.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.005444</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947501</th>
      <td>28.0</td>
      <td>127472.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.002317</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947502</th>
      <td>28.0</td>
      <td>127497.0</td>
      <td>0.069837</td>
      <td>0.182499</td>
      <td>0.063027</td>
      <td>0.0</td>
      <td>5.307253</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000463</td>
      <td>0.000000</td>
      <td>8.034747e-07</td>
      <td>0.005268</td>
      <td>1.0</td>
      <td>0.328110</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947503</th>
      <td>28.0</td>
      <td>127508.0</td>
      <td>0.672726</td>
      <td>0.993081</td>
      <td>0.315336</td>
      <td>0.0</td>
      <td>0.134606</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947504</th>
      <td>28.0</td>
      <td>128157.0</td>
      <td>0.043184</td>
      <td>0.139837</td>
      <td>0.010905</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947505</th>
      <td>28.0</td>
      <td>128245.0</td>
      <td>0.000000</td>
      <td>0.009480</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.008571</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947506</th>
      <td>28.0</td>
      <td>128400.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.017838</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947507</th>
      <td>28.0</td>
      <td>128438.0</td>
      <td>0.000000</td>
      <td>0.009480</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947508</th>
      <td>28.0</td>
      <td>128791.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947509</th>
      <td>28.0</td>
      <td>129077.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.022471</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947510</th>
      <td>28.0</td>
      <td>129218.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.023166</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947511</th>
      <td>28.0</td>
      <td>129235.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947512</th>
      <td>28.0</td>
      <td>129295.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.017838</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947513</th>
      <td>28.0</td>
      <td>129484.0</td>
      <td>0.024628</td>
      <td>0.047402</td>
      <td>0.277755</td>
      <td>0.0</td>
      <td>0.011523</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>...</td>
      <td>0.000232</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947514</th>
      <td>28.0</td>
      <td>129540.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.022471</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947515</th>
      <td>28.0</td>
      <td>129613.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947516</th>
      <td>28.0</td>
      <td>129690.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.005097</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947517</th>
      <td>28.0</td>
      <td>129761.0</td>
      <td>0.000000</td>
      <td>0.078214</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.437207e-06</td>
      <td>0.710871</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
    <tr>
      <th>947518</th>
      <td>28.0</td>
      <td>130104.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.015174</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
    </tr>
  </tbody>
</table>
<p>947519 rows × 41 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[34]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">get_bin_survived</span><span class="p">(</span><span class="n">survival_time</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">survival_time</span> <span class="o">==</span> <span class="mi">64</span><span class="p">:</span>
        <span class="k">return</span> <span class="mf">1.</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="mf">0.</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp</span><span class="p">[</span><span class="s1">&#39;survived&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df_temp</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">get_bin_survived</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[36]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp_sep</span> <span class="o">=</span> <span class="n">df_temp</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">df_temp</span><span class="o">.</span><span class="n">survived</span> <span class="o">==</span> <span class="mi">0</span><span class="p">]</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp_sep</span>
<span class="n">df_temp_sep</span> <span class="o">=</span> <span class="n">df_temp_sep</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">drop</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[38]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df_temp_sep</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[38]:</div>



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
      <th>day</th>
      <th>acc_id</th>
      <th>day_npc_kill</th>
      <th>day_playtime</th>
      <th>day_solo_exp</th>
      <th>day_party_exp</th>
      <th>day_quest_exp</th>
      <th>day_boss_monster</th>
      <th>day_death</th>
      <th>day_revive</th>
      <th>...</th>
      <th>day_amount_spent</th>
      <th>day_item_amount</th>
      <th>day_item_price</th>
      <th>survival_time</th>
      <th>amount_spent</th>
      <th>day_first</th>
      <th>day_last</th>
      <th>day_cnt</th>
      <th>day_rate</th>
      <th>survived</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>31.0</td>
      <td>1.707456</td>
      <td>1.739669</td>
      <td>0.006535</td>
      <td>0.006884</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.0</td>
      <td>31.0</td>
      <td>2.906488</td>
      <td>3.353721</td>
      <td>0.014150</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3.0</td>
      <td>31.0</td>
      <td>1.804283</td>
      <td>2.166290</td>
      <td>0.008928</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.49074</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.0</td>
      <td>31.0</td>
      <td>2.374447</td>
      <td>2.931840</td>
      <td>0.011193</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>31.0</td>
      <td>2.511084</td>
      <td>3.379792</td>
      <td>0.011816</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>2.142661e-01</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6.0</td>
      <td>31.0</td>
      <td>2.260415</td>
      <td>3.097748</td>
      <td>0.010672</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7.0</td>
      <td>31.0</td>
      <td>2.171348</td>
      <td>3.164111</td>
      <td>0.010334</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8.0</td>
      <td>31.0</td>
      <td>1.917304</td>
      <td>2.616613</td>
      <td>0.009501</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9.0</td>
      <td>31.0</td>
      <td>2.068111</td>
      <td>3.412974</td>
      <td>0.011694</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10.0</td>
      <td>31.0</td>
      <td>2.048880</td>
      <td>3.412974</td>
      <td>0.011602</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>5.356498e-08</td>
      <td>0.237074</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11.0</td>
      <td>31.0</td>
      <td>2.018854</td>
      <td>3.258916</td>
      <td>0.011386</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12.0</td>
      <td>31.0</td>
      <td>1.880193</td>
      <td>3.403494</td>
      <td>0.010573</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>3.079987e-01</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13.0</td>
      <td>31.0</td>
      <td>1.842069</td>
      <td>3.161741</td>
      <td>0.010423</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14.0</td>
      <td>31.0</td>
      <td>1.743556</td>
      <td>3.244695</td>
      <td>0.009960</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15.0</td>
      <td>31.0</td>
      <td>1.611979</td>
      <td>2.469666</td>
      <td>0.008127</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16.0</td>
      <td>31.0</td>
      <td>1.904821</td>
      <td>2.886807</td>
      <td>0.009225</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.49074</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17.0</td>
      <td>31.0</td>
      <td>2.348470</td>
      <td>3.412974</td>
      <td>0.011198</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18.0</td>
      <td>31.0</td>
      <td>3.280300</td>
      <td>3.325280</td>
      <td>0.015985</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19.0</td>
      <td>31.0</td>
      <td>3.591023</td>
      <td>3.412974</td>
      <td>0.017371</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20.0</td>
      <td>31.0</td>
      <td>3.284349</td>
      <td>3.412974</td>
      <td>0.015827</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21.0</td>
      <td>31.0</td>
      <td>2.396377</td>
      <td>2.583432</td>
      <td>0.011557</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>3.749549e-01</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>22.0</td>
      <td>31.0</td>
      <td>2.552244</td>
      <td>3.152261</td>
      <td>0.012070</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23.0</td>
      <td>31.0</td>
      <td>1.310366</td>
      <td>1.251424</td>
      <td>0.006555</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>24.0</td>
      <td>31.0</td>
      <td>1.902797</td>
      <td>1.941129</td>
      <td>0.009039</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>25.0</td>
      <td>31.0</td>
      <td>2.668301</td>
      <td>2.735119</td>
      <td>0.012477</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>26.0</td>
      <td>31.0</td>
      <td>3.079562</td>
      <td>3.375052</td>
      <td>0.014325</td>
      <td>0.000000</td>
      <td>0.000216</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>5.356498e-08</td>
      <td>0.216483</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>27.0</td>
      <td>31.0</td>
      <td>3.261407</td>
      <td>3.398753</td>
      <td>0.015189</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>28.0</td>
      <td>31.0</td>
      <td>3.042451</td>
      <td>3.412974</td>
      <td>0.014300</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>45.0</td>
      <td>0.051316</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1.0</td>
      <td>62.0</td>
      <td>3.537380</td>
      <td>0.668374</td>
      <td>25.944969</td>
      <td>0.000000</td>
      <td>0.166234</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>1.015056e+00</td>
      <td>0.000000</td>
      <td>13.0</td>
      <td>0.416438</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2.0</td>
      <td>62.0</td>
      <td>4.582231</td>
      <td>3.038495</td>
      <td>16.507469</td>
      <td>0.000000</td>
      <td>0.263203</td>
      <td>1.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.528062</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>13.0</td>
      <td>0.416438</td>
      <td>1</td>
      <td>27.0</td>
      <td>28</td>
      <td>1.000000</td>
      <td>0.0</td>
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
      <td>...</td>
    </tr>
    <tr>
      <th>375523</th>
      <td>28.0</td>
      <td>126332.0</td>
      <td>1.274604</td>
      <td>1.654344</td>
      <td>0.101286</td>
      <td>0.000000</td>
      <td>0.003463</td>
      <td>1.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>1.365919</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>27.0</td>
      <td>0.067984</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375524</th>
      <td>28.0</td>
      <td>126336.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375525</th>
      <td>28.0</td>
      <td>126509.0</td>
      <td>0.004049</td>
      <td>0.085324</td>
      <td>0.000952</td>
      <td>0.000000</td>
      <td>0.008919</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>...</td>
      <td>1.173470</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.762857</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375526</th>
      <td>28.0</td>
      <td>126524.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375527</th>
      <td>28.0</td>
      <td>126553.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375528</th>
      <td>28.0</td>
      <td>126676.0</td>
      <td>0.000000</td>
      <td>0.018961</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375529</th>
      <td>28.0</td>
      <td>126697.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375530</th>
      <td>28.0</td>
      <td>126831.0</td>
      <td>0.000337</td>
      <td>0.097175</td>
      <td>0.000006</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.035204</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375531</th>
      <td>28.0</td>
      <td>127100.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375532</th>
      <td>28.0</td>
      <td>127132.0</td>
      <td>0.061065</td>
      <td>0.149318</td>
      <td>0.044988</td>
      <td>0.000000</td>
      <td>0.201739</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375533</th>
      <td>28.0</td>
      <td>127226.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375534</th>
      <td>28.0</td>
      <td>127436.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375535</th>
      <td>28.0</td>
      <td>127472.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375536</th>
      <td>28.0</td>
      <td>127497.0</td>
      <td>0.069837</td>
      <td>0.182499</td>
      <td>0.063027</td>
      <td>0.000000</td>
      <td>5.307253</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>8.034747e-07</td>
      <td>0.005268</td>
      <td>1.0</td>
      <td>0.328110</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375537</th>
      <td>28.0</td>
      <td>127508.0</td>
      <td>0.672726</td>
      <td>0.993081</td>
      <td>0.315336</td>
      <td>0.000000</td>
      <td>0.134606</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375538</th>
      <td>28.0</td>
      <td>128157.0</td>
      <td>0.043184</td>
      <td>0.139837</td>
      <td>0.010905</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>2.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375539</th>
      <td>28.0</td>
      <td>128245.0</td>
      <td>0.000000</td>
      <td>0.009480</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375540</th>
      <td>28.0</td>
      <td>128400.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375541</th>
      <td>28.0</td>
      <td>128438.0</td>
      <td>0.000000</td>
      <td>0.009480</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375542</th>
      <td>28.0</td>
      <td>128791.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375543</th>
      <td>28.0</td>
      <td>129077.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375544</th>
      <td>28.0</td>
      <td>129218.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375545</th>
      <td>28.0</td>
      <td>129235.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375546</th>
      <td>28.0</td>
      <td>129295.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375547</th>
      <td>28.0</td>
      <td>129484.0</td>
      <td>0.024628</td>
      <td>0.047402</td>
      <td>0.277755</td>
      <td>0.000000</td>
      <td>0.011523</td>
      <td>0.0</td>
      <td>0.24537</td>
      <td>0.246819</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375548</th>
      <td>28.0</td>
      <td>129540.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375549</th>
      <td>28.0</td>
      <td>129613.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375550</th>
      <td>28.0</td>
      <td>129690.0</td>
      <td>0.000000</td>
      <td>0.002370</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>3.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375551</th>
      <td>28.0</td>
      <td>129761.0</td>
      <td>0.000000</td>
      <td>0.078214</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>2.437207e-06</td>
      <td>0.710871</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>375552</th>
      <td>28.0</td>
      <td>130104.0</td>
      <td>0.000000</td>
      <td>0.004740</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.000000</td>
      <td>...</td>
      <td>0.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>4.0</td>
      <td>0.000000</td>
      <td>27</td>
      <td>27.0</td>
      <td>1</td>
      <td>0.035714</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>375553 rows × 42 columns</p>
</div>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_train</span><span class="p">,</span> <span class="n">x_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">df_temp</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span> <span class="s1">&#39;survival_time&#39;</span><span class="p">,</span> <span class="s1">&#39;survived&#39;</span><span class="p">],</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">),</span>
                                                   <span class="n">df_temp</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span> <span class="n">random_state</span> <span class="o">=</span> <span class="mi">2019</span><span class="p">)</span>

<span class="n">x_sep_train</span><span class="p">,</span> <span class="n">x_sep_test</span><span class="p">,</span> <span class="n">y_sep_train</span><span class="p">,</span> <span class="n">y_sep_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">df_temp_sep</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;amount_spent&#39;</span><span class="p">,</span> <span class="s1">&#39;survival_time&#39;</span><span class="p">,</span> <span class="s1">&#39;survived&#39;</span><span class="p">],</span> <span class="n">axis</span> <span class="o">=</span><span class="mi">1</span><span class="p">)</span>
                                                                   <span class="p">,</span> <span class="n">df_temp_sep</span><span class="p">[</span><span class="s1">&#39;survival_time&#39;</span><span class="p">],</span> <span class="n">random_state</span> <span class="o">=</span> <span class="mi">2019</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[40]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lgb_train</span> <span class="o">=</span> <span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_train</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="n">y_train</span><span class="p">)</span>
<span class="n">lgb_eval</span> <span class="o">=</span> <span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_test</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="n">y_test</span><span class="p">)</span>

<span class="n">lgb_sep_train</span> <span class="o">=</span> <span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_sep_train</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="n">y_sep_train</span><span class="p">)</span>
<span class="n">lgb_sep_eval</span> <span class="o">=</span> <span class="n">lgb</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="n">x_sep_test</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="n">y_sep_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[41]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#feature_fraction : 데이터의 paremater들 중에 각 round에 몇 %의 parameter를 random으로 골라 학습시킬지 정해주는 인자</span>
<span class="n">params</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s1">&#39;boosting_type&#39;</span><span class="p">:</span> <span class="s1">&#39;gbdt&#39;</span><span class="p">,</span>
    <span class="s1">&#39;objective&#39;</span><span class="p">:</span> <span class="s1">&#39;regression_l1&#39;</span><span class="p">,</span>
    <span class="c1">#&#39;objective&#39;:&#39;mape&#39;, #이게 loss function 같은거고, metric이 valid할때 무슨 함수로 valid할지 정하는거임.</span>
    <span class="c1">#&#39;metric&#39;: &#39;regression_l1&#39;, #l2가 제곱 loss, mape는 %로 오차 나타내줌</span>
    <span class="c1">#&#39;metric&#39;: &#39;mae&#39;,</span>
    <span class="s1">&#39;num_leaves&#39;</span><span class="p">:</span><span class="mi">1000</span><span class="p">,</span>
    <span class="c1">#&#39;min_data&#39;:20,</span>
    <span class="s1">&#39;min_data_in_leaf&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span> <span class="c1">#20이 최적화라고 한다.</span>
    <span class="s1">&#39;max_depth&#39;</span><span class="p">:</span> <span class="mi">20</span><span class="p">,</span>
    <span class="s1">&#39;max_bin&#39;</span><span class="p">:</span><span class="mi">50</span><span class="p">,</span>
    <span class="s1">&#39;learning_rate&#39;</span><span class="p">:</span> <span class="mf">0.05</span><span class="p">,</span>
    <span class="c1">#&#39;feature_fraction&#39;: 0.8,</span>
    <span class="c1">#&#39;max_depth&#39;:20,</span>
    <span class="c1">#&#39;bagging_fraction&#39;: 0.8,</span>
    <span class="c1">#&#39;bagging_freq&#39;: 5,</span>
    <span class="s1">&#39;num_trees&#39;</span><span class="p">:</span><span class="mi">10000</span><span class="p">,</span> <span class="c1">#이게 train 반복횟수임</span>
    <span class="c1">#&#39;verbose&#39;: 0,</span>
    <span class="c1">#&#39;min_sum_hessian_in_leaf&#39;:11,</span>
    <span class="s1">&#39;n_estimators&#39;</span> <span class="p">:</span> <span class="mi">720</span><span class="p">,</span>
    <span class="c1">#&#39;categorical_features&#39; : [&#39;maxServerOfAcc&#39;,&#39;main_server&#39;]</span>
    <span class="c1">#&#39;max_cat_group&#39;:30</span>
    
<span class="p">}</span>
<span class="c1">#l1 절대 l2 제곱</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[42]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">gbm</span> <span class="o">=</span> <span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span>
               <span class="n">lgb_train</span><span class="p">,</span>
               <span class="n">valid_sets</span> <span class="o">=</span> <span class="n">lgb_eval</span><span class="p">,</span>
               <span class="n">verbose_eval</span> <span class="o">=</span> <span class="mi">200</span><span class="p">,</span>
               <span class="n">early_stopping_rounds</span> <span class="o">=</span> <span class="mi">100</span><span class="p">)</span>

<span class="n">gbm2</span> <span class="o">=</span> <span class="n">lgb</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">params</span><span class="p">,</span>
                <span class="n">lgb_sep_train</span><span class="p">,</span>
                <span class="n">valid_sets</span> <span class="o">=</span> <span class="n">lgb_sep_eval</span><span class="p">,</span>
                <span class="n">verbose_eval</span> <span class="o">=</span> <span class="mi">200</span><span class="p">,</span>
                <span class="n">early_stopping_rounds</span> <span class="o">=</span> <span class="mi">100</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>C:\Users\skagu\Anaconda3\lib\site-packages\lightgbm\engine.py:118: UserWarning: Found `num_trees` in params. Will use it instead of argument
  warnings.warn(&#34;Found `{}` in params. Will use it instead of argument&#34;.format(alias))
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Training until validation scores don&#39;t improve for 100 rounds.
[200]	valid_0&#39;s l1: 9.8115
[400]	valid_0&#39;s l1: 9.46996
[600]	valid_0&#39;s l1: 9.23875
[800]	valid_0&#39;s l1: 9.15104
[1000]	valid_0&#39;s l1: 9.11324
[1200]	valid_0&#39;s l1: 9.00459
[1400]	valid_0&#39;s l1: 8.95364
[1600]	valid_0&#39;s l1: 8.89977
[1800]	valid_0&#39;s l1: 8.87388
[2000]	valid_0&#39;s l1: 8.85787
[2200]	valid_0&#39;s l1: 8.85288
[2400]	valid_0&#39;s l1: 8.85126
[2600]	valid_0&#39;s l1: 8.84913
[2800]	valid_0&#39;s l1: 8.84563
[3000]	valid_0&#39;s l1: 8.84408
[3200]	valid_0&#39;s l1: 8.84124
[3400]	valid_0&#39;s l1: 8.83961
[3600]	valid_0&#39;s l1: 8.83778
[3800]	valid_0&#39;s l1: 8.83574
[4000]	valid_0&#39;s l1: 8.83467
[4200]	valid_0&#39;s l1: 8.83296
[4400]	valid_0&#39;s l1: 8.83195
[4600]	valid_0&#39;s l1: 8.83124
[4800]	valid_0&#39;s l1: 8.82891
[5000]	valid_0&#39;s l1: 8.82811
[5200]	valid_0&#39;s l1: 8.82763
[5400]	valid_0&#39;s l1: 8.82656
[5600]	valid_0&#39;s l1: 8.8252
[5800]	valid_0&#39;s l1: 8.82347
[6000]	valid_0&#39;s l1: 8.82242
[6200]	valid_0&#39;s l1: 8.82162
[6400]	valid_0&#39;s l1: 8.82094
[6600]	valid_0&#39;s l1: 8.81791
[6800]	valid_0&#39;s l1: 8.81742
[7000]	valid_0&#39;s l1: 8.81699
[7200]	valid_0&#39;s l1: 8.81646
[7400]	valid_0&#39;s l1: 8.81586
Early stopping, best iteration is:
[7332]	valid_0&#39;s l1: 8.81579
Training until validation scores don&#39;t improve for 100 rounds.
[200]	valid_0&#39;s l1: 9.34839
[400]	valid_0&#39;s l1: 8.99657
[600]	valid_0&#39;s l1: 8.9035
[800]	valid_0&#39;s l1: 8.78857
[1000]	valid_0&#39;s l1: 8.70469
[1200]	valid_0&#39;s l1: 8.60848
[1400]	valid_0&#39;s l1: 8.56615
[1600]	valid_0&#39;s l1: 8.51667
[1800]	valid_0&#39;s l1: 8.44761
[2000]	valid_0&#39;s l1: 8.41966
[2200]	valid_0&#39;s l1: 8.4078
[2400]	valid_0&#39;s l1: 8.40005
[2600]	valid_0&#39;s l1: 8.39204
[2800]	valid_0&#39;s l1: 8.38345
[3000]	valid_0&#39;s l1: 8.37676
[3200]	valid_0&#39;s l1: 8.37151
[3400]	valid_0&#39;s l1: 8.36377
[3600]	valid_0&#39;s l1: 8.35649
[3800]	valid_0&#39;s l1: 8.35211
[4000]	valid_0&#39;s l1: 8.34715
[4200]	valid_0&#39;s l1: 8.34445
[4400]	valid_0&#39;s l1: 8.34093
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-intense-fg ansi-bold">---------------------------------------------------------------------------</span>
<span class="ansi-red-intense-fg ansi-bold">KeyboardInterrupt</span>                         Traceback (most recent call last)
<span class="ansi-green-intense-fg ansi-bold">&lt;ipython-input-42-af44739ccf4e&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span>
<span class="ansi-green-fg">      9</span>                 valid_sets <span class="ansi-yellow-intense-fg ansi-bold">=</span> lgb_sep_eval<span class="ansi-yellow-intense-fg ansi-bold">,</span>
<span class="ansi-green-fg">     10</span>                 verbose_eval <span class="ansi-yellow-intense-fg ansi-bold">=</span> <span class="ansi-cyan-intense-fg ansi-bold">200</span><span class="ansi-yellow-intense-fg ansi-bold">,</span>
<span class="ansi-green-intense-fg ansi-bold">---&gt; 11</span><span class="ansi-yellow-intense-fg ansi-bold">                 early_stopping_rounds = 100)
</span>
<span class="ansi-green-intense-fg ansi-bold">~\Anaconda3\lib\site-packages\lightgbm\engine.py</span> in <span class="ansi-cyan-fg">train</span><span class="ansi-blue-intense-fg ansi-bold">(params, train_set, num_boost_round, valid_sets, valid_names, fobj, feval, init_model, feature_name, categorical_feature, early_stopping_rounds, evals_result, verbose_eval, learning_rates, keep_training_booster, callbacks)</span>
<span class="ansi-green-fg">    216</span>                                     evaluation_result_list=None))
<span class="ansi-green-fg">    217</span> 
<span class="ansi-green-intense-fg ansi-bold">--&gt; 218</span><span class="ansi-yellow-intense-fg ansi-bold">         </span>booster<span class="ansi-yellow-intense-fg ansi-bold">.</span>update<span class="ansi-yellow-intense-fg ansi-bold">(</span>fobj<span class="ansi-yellow-intense-fg ansi-bold">=</span>fobj<span class="ansi-yellow-intense-fg ansi-bold">)</span>
<span class="ansi-green-fg">    219</span> 
<span class="ansi-green-fg">    220</span>         evaluation_result_list <span class="ansi-yellow-intense-fg ansi-bold">=</span> <span class="ansi-yellow-intense-fg ansi-bold">[</span><span class="ansi-yellow-intense-fg ansi-bold">]</span>

<span class="ansi-green-intense-fg ansi-bold">~\Anaconda3\lib\site-packages\lightgbm\basic.py</span> in <span class="ansi-cyan-fg">update</span><span class="ansi-blue-intense-fg ansi-bold">(self, train_set, fobj)</span>
<span class="ansi-green-fg">   1800</span>             _safe_call(_LIB.LGBM_BoosterUpdateOneIter(
<span class="ansi-green-fg">   1801</span>                 self<span class="ansi-yellow-intense-fg ansi-bold">.</span>handle<span class="ansi-yellow-intense-fg ansi-bold">,</span>
<span class="ansi-green-intense-fg ansi-bold">-&gt; 1802</span><span class="ansi-yellow-intense-fg ansi-bold">                 ctypes.byref(is_finished)))
</span><span class="ansi-green-fg">   1803</span>             self<span class="ansi-yellow-intense-fg ansi-bold">.</span>__is_predicted_cur_iter <span class="ansi-yellow-intense-fg ansi-bold">=</span> <span class="ansi-yellow-intense-fg ansi-bold">[</span><span class="ansi-green-intense-fg ansi-bold">False</span> <span class="ansi-green-intense-fg ansi-bold">for</span> _ <span class="ansi-green-intense-fg ansi-bold">in</span> range_<span class="ansi-yellow-intense-fg ansi-bold">(</span>self<span class="ansi-yellow-intense-fg ansi-bold">.</span>__num_dataset<span class="ansi-yellow-intense-fg ansi-bold">)</span><span class="ansi-yellow-intense-fg ansi-bold">]</span>
<span class="ansi-green-fg">   1804</span>             <span class="ansi-green-intense-fg ansi-bold">return</span> is_finished<span class="ansi-yellow-intense-fg ansi-bold">.</span>value <span class="ansi-yellow-intense-fg ansi-bold">==</span> <span class="ansi-cyan-intense-fg ansi-bold">1</span>

<span class="ansi-red-intense-fg ansi-bold">KeyboardInterrupt</span>: </pre>
</div>
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
