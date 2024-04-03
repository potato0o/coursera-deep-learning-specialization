<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>Week 1 Introduction to Deep Learning</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	padding-inline-start: 0;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.page-description {
    margin-bottom: 2em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
	empty-cells: show;
}
.simple-table td {
	height: 29px;
	min-width: 120px;
}

.simple-table th {
	height: 29px;
	min-width: 120px;
}

.simple-table-header-color {
	background: rgb(247, 246, 243);
	color: black;
}
.simple-table-header {
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	max-height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-uiBlue { background-color: rgba(35, 131, 226, .07); }
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-transparentGray { background-color: rgba(227, 226, 224, 0); }
.select-value-color-translucentGray { background-color: rgba(255, 255, 255, 0.0375); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }
.select-value-color-pageGlass { background-color: undefined; }
.select-value-color-washGlass { background-color: undefined; }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="b69c69ca-582a-4c30-b458-197ca3cd0ea7" class="page sans"><header><h1 class="page-title">Week 1 Introduction to Deep Learning</h1><p class="page-description"></p><table class="properties"><tbody><tr class="property-row property-row-status"><th><span class="icon property-icon"><svg role="graphics-symbol" viewBox="0 0 16 16" style="width:14px;height:14px;display:block;fill:rgba(55, 53, 47, 0.45);flex-shrink:0" class="typesStatus"><path d="M8.75488 1.02344C8.75488 0.613281 8.41309 0.264648 8.00293 0.264648C7.59277 0.264648 7.25098 0.613281 7.25098 1.02344V3.11523C7.25098 3.51855 7.59277 3.86719 8.00293 3.86719C8.41309 3.86719 8.75488 3.51855 8.75488 3.11523V1.02344ZM3.91504 5.0293C4.20215 5.31641 4.69434 5.32324 4.97461 5.03613C5.26855 4.74902 5.26855 4.25684 4.98145 3.96973L3.53906 2.52051C3.25195 2.2334 2.7666 2.21973 2.47949 2.50684C2.19238 2.79395 2.18555 3.28613 2.47266 3.57324L3.91504 5.0293ZM10.9629 4.01758C10.6826 4.30469 10.6826 4.79688 10.9697 5.08398C11.2568 5.37109 11.749 5.36426 12.0361 5.07715L13.4854 3.62793C13.7725 3.34082 13.7725 2.84863 13.4785 2.55469C13.1982 2.27441 12.7061 2.27441 12.4189 2.56152L10.9629 4.01758ZM15.0234 8.78906C15.4336 8.78906 15.7822 8.44727 15.7822 8.03711C15.7822 7.62695 15.4336 7.28516 15.0234 7.28516H12.9385C12.5283 7.28516 12.1797 7.62695 12.1797 8.03711C12.1797 8.44727 12.5283 8.78906 12.9385 8.78906H15.0234ZM0.975586 7.28516C0.56543 7.28516 0.223633 7.62695 0.223633 8.03711C0.223633 8.44727 0.56543 8.78906 0.975586 8.78906H3.07422C3.48438 8.78906 3.83301 8.44727 3.83301 8.03711C3.83301 7.62695 3.48438 7.28516 3.07422 7.28516H0.975586ZM12.0361 10.9902C11.749 10.71 11.2568 10.71 10.9629 10.9971C10.6826 11.2842 10.6826 11.7764 10.9697 12.0635L12.4258 13.5127C12.7129 13.7998 13.2051 13.793 13.4922 13.5059C13.7793 13.2256 13.7725 12.7266 13.4854 12.4395L12.0361 10.9902ZM2.52051 12.4395C2.22656 12.7266 2.22656 13.2188 2.50684 13.5059C2.79395 13.793 3.28613 13.7998 3.57324 13.5127L5.02246 12.0703C5.31641 11.7832 5.31641 11.291 5.03613 11.0039C4.74902 10.7168 4.25684 10.71 3.96973 10.9971L2.52051 12.4395ZM8.75488 12.9658C8.75488 12.5557 8.41309 12.207 8.00293 12.207C7.59277 12.207 7.25098 12.5557 7.25098 12.9658V15.0576C7.25098 15.4609 7.59277 15.8096 8.00293 15.8096C8.41309 15.8096 8.75488 15.4609 8.75488 15.0576V12.9658Z"></path></svg></span>Progress</th><td><span class="status-value select-value-color-green"><div class="status-dot status-dot-color-green"></div>Done</span></td></tr><tr class="property-row property-row-text"><th><span class="icon property-icon"><svg role="graphics-symbol" viewBox="0 0 16 16" style="width:14px;height:14px;display:block;fill:rgba(55, 53, 47, 0.45);flex-shrink:0" class="typesText"><path d="M1.56738 3.25879H14.4258C14.7676 3.25879 15.0479 2.97852 15.0479 2.63672C15.0479 2.29492 14.7744 2.02148 14.4258 2.02148H1.56738C1.21875 2.02148 0.952148 2.29492 0.952148 2.63672C0.952148 2.97852 1.22559 3.25879 1.56738 3.25879ZM1.56738 6.84082H14.4258C14.7676 6.84082 15.0479 6.56055 15.0479 6.21875C15.0479 5.87695 14.7744 5.60352 14.4258 5.60352H1.56738C1.21875 5.60352 0.952148 5.87695 0.952148 6.21875C0.952148 6.56055 1.22559 6.84082 1.56738 6.84082ZM1.56738 10.4229H14.4258C14.7676 10.4229 15.0479 10.1426 15.0479 9.80078C15.0479 9.45898 14.7744 9.18555 14.4258 9.18555H1.56738C1.21875 9.18555 0.952148 9.45898 0.952148 9.80078C0.952148 10.1426 1.22559 10.4229 1.56738 10.4229ZM1.56738 14.0049H8.75879C9.10059 14.0049 9.38086 13.7246 9.38086 13.3828C9.38086 13.041 9.10742 12.7676 8.75879 12.7676H1.56738C1.21875 12.7676 0.952148 13.041 0.952148 13.3828C0.952148 13.7246 1.22559 14.0049 1.56738 14.0049Z"></path></svg></span>Summary</th><td>Introduction to Neural Network and Supervised Learning</td></tr></tbody></table></header><div class="page-body"><figure id="4819c4ce-2f17-4317-a1a6-351f224c0970"><div class="source"><a href="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/C1_W1.pdf">https://prod-files-secure.s3.us-west-2.amazonaws.com/a893bb2d-37b6-4bb7-8459-f364279775cd/772d8570-0998-4b49-afb6-3668417f5349/C1_W1.pdf</a></div></figure><h2 id="fb9ec4f2-36e9-4e24-94ef-13befacf5df2" class="">5 Courses in Specialization</h2><ol type="1" id="b669ca07-5fe7-4e1b-bba0-63279227a5bf" class="numbered-list" start="1"><li>Neural Networks and Deep Learning (this course)</li></ol><ol type="1" id="be03fe95-21b8-403a-849e-7dd09865c64f" class="numbered-list" start="2"><li>Improving deep Neural Networks: Hyperparameter tuning, regularization and Optimization</li></ol><ol type="1" id="a12671f6-40b6-42a1-8a19-95c70ea9a4fd" class="numbered-list" start="3"><li>Structuring your Machine Learning Project</li></ol><ol type="1" id="32928bc0-9ff1-4fac-ab85-e5665b588d77" class="numbered-list" start="4"><li>Convolutional Neural Networks</li></ol><ol type="1" id="a33baddf-5412-4b20-8692-b69255496a4f" class="numbered-list" start="5"><li>Natural Language Processing: Building sequence models</li></ol><p id="be04f612-beb3-48b3-ae8d-f8349ca1510a" class="">
</p><h2 id="33e50a4c-09b5-4997-a65a-c1c6ddd0fc8c" class="">Outline of this course</h2><ol type="1" id="fd25cb43-6ec0-4863-997f-5305634578d0" class="numbered-list" start="1"><li>Introduction</li></ol><ol type="1" id="845d42f9-5dfc-4951-b3ee-f85074963b6e" class="numbered-list" start="2"><li>Basics of neural Network Programming</li></ol><ol type="1" id="5d1b1402-0669-41e9-ae19-22c19a4549e3" class="numbered-list" start="3"><li>One Hidden Layer Neural Networks</li></ol><ol type="1" id="85095ff6-2174-4160-8dbc-3e3b3833cc57" class="numbered-list" start="4"><li>Deep Neural Networks</li></ol><p id="ef8e2849-83ff-4479-ab47-36e5441add06" class="">
</p><h1 id="7b9ddda0-560b-41b4-8f7b-ef359f0eaa1f" class="">Week 1: Introduction</h1><h2 id="089f5cee-bbb5-4831-aa52-d1d7bcd82e7f" class="">What is Neural Network?</h2><p id="5d5522b8-bbe2-404a-a2eb-b8e39df33a11" class="">A <strong>neural network</strong> is a machine learning model that imitates the way the human brain makes decisions. It achieves this by using processes that mimic the behavior of biological neurons. Let’s break down the key components of a neural network:</p><ol type="1" id="4204af42-daa5-4648-ac40-fbddaffcb2ca" class="numbered-list" start="1"><li><strong>Nodes (Artificial Neurons)</strong>: A neural network consists of interconnected nodes, also known as artificial neurons. These nodes are organized into layers:<ul id="d96db146-2a52-40c7-966b-0206e9d24a10" class="bulleted-list"><li style="list-style-type:disc"><strong>Input Layer</strong>: The initial layer that receives input data.</li></ul><ul id="daeb15d9-7da0-4b1c-a3a7-bdb21abf1b41" class="bulleted-list"><li style="list-style-type:disc"><strong>Hidden Layers</strong>: One or more intermediate layers between the input and output layers.</li></ul><ul id="0673f200-8f7d-4319-a56b-31ab5300fc0d" class="bulleted-list"><li style="list-style-type:disc"><strong>Output Layer</strong>: The final layer that produces the network’s output.</li></ul><figure id="f2bacc74-c7fd-434d-bc72-3e14997a8224" class="image"><a href="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled.png"><img style="width:192px" src="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled.png"/></a></figure><p id="a76254d2-bba0-4e83-8346-e88420858810" class="">
</p></li></ol><ol type="1" id="56df935a-29a2-4241-a530-e31eaa25ac68" class="numbered-list" start="2"><li><strong>Weights and Thresholds</strong>:<ul id="4499ced9-8a59-4139-b60d-f269d38b1651" class="bulleted-list"><li style="list-style-type:disc">Each node has its own associated weight and threshold.</li></ul><ul id="9ba47db2-d904-4d46-af61-9071db0990e9" class="bulleted-list"><li style="list-style-type:disc">Weights determine the importance of input variables, with larger weights contributing more significantly to the output.</li></ul><ul id="2520c657-7af5-47cd-b5a4-471345b03f1c" class="bulleted-list"><li style="list-style-type:disc">Thresholds define the activation condition for a node.</li></ul><figure id="0fe513ea-7812-4080-ba78-7ee802436a5f" class="image"><a href="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%201.png"><img style="width:288px" src="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%201.png"/></a></figure></li></ol><p id="54914fba-bfbf-4d26-9155-271f1bc58520" class="">
</p><ol type="1" id="7b0d2f07-0173-4cf5-8cec-2382edea323e" class="numbered-list" start="3"><li><strong>Activation Function</strong>:<ul id="b8b6d18f-fa23-4819-928c-568be8d68605" class="bulleted-list"><li style="list-style-type:disc">After multiplying inputs by their respective weights and summing them, the output passes through an activation function.</li></ul><ul id="b348dac8-1f8e-45b5-8ee4-f4b76dd43f7c" class="bulleted-list"><li style="list-style-type:disc">If the output exceeds a specified threshold, the node activates and passes data to the next layer.</li></ul><ul id="45caf060-a046-41a7-844e-71e88238a03d" class="bulleted-list"><li style="list-style-type:disc">This process defines the neural network as a <strong>feedforward network</strong>.</li></ul></li></ol><p id="bed04340-f0e1-4a43-8365-7c4f4cbe47cc" class="">
</p><h2 id="f85f58bd-de28-433b-99d8-5fd4df87bef6" class="">Supervised Learning</h2><ul id="849285a9-d8e3-4f04-9a80-77bdd47847da" class="bulleted-list"><li style="list-style-type:disc">Supervised learning, also known as <strong>supervised machine learning</strong>, involves using <strong>labeled data sets</strong> to train algorithms.</li></ul><ul id="1681c736-db81-4b2e-9507-9264fbe59b2f" class="bulleted-list"><li style="list-style-type:disc">The goal is to <strong>classify data</strong> or <strong>predict outcomes</strong> accurately based on input features and their corresponding labels.</li></ul><ul id="e67c3976-f179-456a-992e-8bdbab4e6028" class="bulleted-list"><li style="list-style-type:disc">The data need to provide both the input and output for the machine to learn and predict the output accodingly.</li></ul><figure id="f646c3f5-99fb-4e28-995a-c9d9c6ec5f36" class="image"><a href="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%202.png"><img style="width:432px" src="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%202.png"/></a></figure><ul id="3f985ae2-1de0-414e-8cb0-30e860da44b9" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-orange"><strong>Structured Data</strong></mark>: Structured data refers to organized information that follows a predefined format and resides in fixed fields within a record or file.</li></ul><ul id="83f0f541-8d34-4989-bcc9-6e052972c3bb" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-orange"><strong>Unstructured Data:</strong></mark> Unstructured data lacks a specific structure and doesn’t neatly fit into databases.<figure id="99f48a5c-3a7b-4d17-83c7-48f4e4a79fd8" class="image"><a href="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%203.png"><img style="width:451px" src="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%203.png"/></a></figure></li></ul><p id="957b91d5-9c4f-493c-bd86-2ff5be81c774" class="">
</p><h2 id="a5119cd0-2061-43a4-beaa-f4260dedbad5" class="">Why is Deep Learning taking off?</h2><figure id="f82bd03f-2ad6-4952-9373-99829057eb5c" class="image"><a href="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%204.png"><img style="width:578px" src="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%204.png"/></a></figure><ul id="4d5b7e72-3dcb-4831-8a26-856a91395c44" class="bulleted-list"><li style="list-style-type:disc">In traditional machine learning algorithm, its found that when the size of training data reached certain size, the performance of the model would not increase.</li></ul><ul id="17c6da0d-0025-4422-bb46-36baf0338336" class="bulleted-list"><li style="list-style-type:disc">In Neural Network, the larger NN will increase in performance when data size increase. Therefore larger NN had been used as data size had surged as a result from digitalize. </li></ul><figure id="656f667a-7198-4bec-a260-01768c59c2e9" class="image"><a href="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%205.png"><img style="width:479px" src="Week%201%20Introduction%20to%20Deep%20Learning%20b69c69ca582a4c30b458197ca3cd0ea7/Untitled%205.png"/></a></figure><ul id="9f4a8705-99b7-4356-b5a0-b03fd47602af" class="bulleted-list"><li style="list-style-type:disc">The significate improvement in data, computation and algorithms had greatly boost the development and employment of deep learning.</li></ul><p id="0643887a-7c91-4f59-8529-6995a8c40c27" class="">
</p><p id="f56d949e-c0b9-44e9-ae48-871b9f7b35ab" class="">
</p></div></article><span class="sans" style="font-size:14px;padding-top:2em"></span></body></html>
