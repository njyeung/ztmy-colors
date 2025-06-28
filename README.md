<!DOCTYPE html>

<html lang="en">
<head><meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>zutomayo</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .pm { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation.Marker */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>
<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0 solid transparent;
  border-right: 0 solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0 solid transparent;
  border-bottom: 0 solid transparent;
}

/*
 * Lumino
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
}

.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.lm-AccordionPanel[data-orientation='horizontal'] > .lm-AccordionPanel-title {
  /* Title is rotated for horizontal accordion panel using CSS */
  display: block;
  transform-origin: top left;
  transform: rotate(-90deg) translate(-100%);
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-CommandPalette-search {
  flex: 0 0 auto;
}

.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}

.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}

.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}

.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
  border: 1px solid transparent;
  background-color: transparent;
  position: absolute;
  z-index: 1;
  right: 3%;
  top: 0;
  bottom: 0;
  margin: auto;
  padding: 7px 0;
  display: none;
  vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
  content: 'X';
  display: block;
  width: 15px;
  height: 15px;
  text-align: center;
  color: #000;
  font-weight: normal;
  font-size: 12px;
  cursor: pointer;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-DockPanel {
  z-index: 0;
}

.lm-DockPanel-widget {
  z-index: 0;
}

.lm-DockPanel-tabBar {
  z-index: 1;
}

.lm-DockPanel-handle {
  z-index: 2;
}

.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}

.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}

.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}

.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}

.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}

.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}

.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}

.lm-Menu-item {
  display: table-row;
}

.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}

.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}

.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}

.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}

.lm-MenuBar-item {
  box-sizing: border-box;
}

.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}

.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}

.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}

.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}

.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-SplitPanel-child {
  z-index: 0;
}

.lm-SplitPanel-handle {
  z-index: 1;
}

.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}

.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}

.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}

.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}

.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}

.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
  align-items: flex-end;
}

.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
  align-items: flex-end;
}

.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}

.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}

.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}

.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
  touch-action: none; /* Disable native Drag/Drop */
}

.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}

.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}

.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing: border-box;
}

.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}

.lm-TabBar-addButton.lm-mod-hidden {
  display: none !important;
}

.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}

.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}

.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}

.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

.lm-TabBar-tabLabel .lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing: border-box;
  background: inherit;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-TabPanel-tabBar {
  z-index: 1;
}

.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

.jp-Collapse-header {
  padding: 1px 12px;
  background-color: var(--jp-layout-color1);
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  align-items: center;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  text-transform: uppercase;
  user-select: none;
}

.jp-Collapser-icon {
  height: 16px;
}

.jp-Collapse-header-collapsed .jp-Collapser-icon {
  transform: rotate(-90deg);
  margin: auto 0;
}

.jp-Collapser-title {
  line-height: 25px;
}

.jp-Collapse-contents {
  padding: 0 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add-above: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwXzEzN18xOTQ5MikiPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGQ9Ik00Ljc1IDQuOTMwNjZINi42MjVWNi44MDU2NkM2LjYyNSA3LjAxMTkxIDYuNzkzNzUgNy4xODA2NiA3IDcuMTgwNjZDNy4yMDYyNSA3LjE4MDY2IDcuMzc1IDcuMDExOTEgNy4zNzUgNi44MDU2NlY0LjkzMDY2SDkuMjVDOS40NTYyNSA0LjkzMDY2IDkuNjI1IDQuNzYxOTEgOS42MjUgNC41NTU2NkM5LjYyNSA0LjM0OTQxIDkuNDU2MjUgNC4xODA2NiA5LjI1IDQuMTgwNjZINy4zNzVWMi4zMDU2NkM3LjM3NSAyLjA5OTQxIDcuMjA2MjUgMS45MzA2NiA3IDEuOTMwNjZDNi43OTM3NSAxLjkzMDY2IDYuNjI1IDIuMDk5NDEgNi42MjUgMi4zMDU2NlY0LjE4MDY2SDQuNzVDNC41NDM3NSA0LjE4MDY2IDQuMzc1IDQuMzQ5NDEgNC4zNzUgNC41NTU2NkM0LjM3NSA0Ljc2MTkxIDQuNTQzNzUgNC45MzA2NiA0Ljc1IDQuOTMwNjZaIiBmaWxsPSIjNjE2MTYxIiBzdHJva2U9IiM2MTYxNjEiIHN0cm9rZS13aWR0aD0iMC43Ii8+CjwvZz4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTExLjUgOS41VjExLjVMMi41IDExLjVWOS41TDExLjUgOS41Wk0xMiA4QzEyLjU1MjMgOCAxMyA4LjQ0NzcyIDEzIDlWMTJDMTMgMTIuNTUyMyAxMi41NTIzIDEzIDEyIDEzTDIgMTNDMS40NDc3MiAxMyAxIDEyLjU1MjMgMSAxMlY5QzEgOC40NDc3MiAxLjQ0NzcxIDggMiA4TDEyIDhaIiBmaWxsPSIjNjE2MTYxIi8+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzEzN18xOTQ5MiI+CjxyZWN0IGNsYXNzPSJqcC1pY29uMyIgd2lkdGg9IjYiIGhlaWdodD0iNiIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0ibWF0cml4KC0xIDAgMCAxIDEwIDEuNTU1NjYpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==);
  --jp-icon-add-below: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwXzEzN18xOTQ5OCkiPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGQ9Ik05LjI1IDEwLjA2OTNMNy4zNzUgMTAuMDY5M0w3LjM3NSA4LjE5NDM0QzcuMzc1IDcuOTg4MDkgNy4yMDYyNSA3LjgxOTM0IDcgNy44MTkzNEM2Ljc5Mzc1IDcuODE5MzQgNi42MjUgNy45ODgwOSA2LjYyNSA4LjE5NDM0TDYuNjI1IDEwLjA2OTNMNC43NSAxMC4wNjkzQzQuNTQzNzUgMTAuMDY5MyA0LjM3NSAxMC4yMzgxIDQuMzc1IDEwLjQ0NDNDNC4zNzUgMTAuNjUwNiA0LjU0Mzc1IDEwLjgxOTMgNC43NSAxMC44MTkzTDYuNjI1IDEwLjgxOTNMNi42MjUgMTIuNjk0M0M2LjYyNSAxMi45MDA2IDYuNzkzNzUgMTMuMDY5MyA3IDEzLjA2OTNDNy4yMDYyNSAxMy4wNjkzIDcuMzc1IDEyLjkwMDYgNy4zNzUgMTIuNjk0M0w3LjM3NSAxMC44MTkzTDkuMjUgMTAuODE5M0M5LjQ1NjI1IDEwLjgxOTMgOS42MjUgMTAuNjUwNiA5LjYyNSAxMC40NDQzQzkuNjI1IDEwLjIzODEgOS40NTYyNSAxMC4wNjkzIDkuMjUgMTAuMDY5M1oiIGZpbGw9IiM2MTYxNjEiIHN0cm9rZT0iIzYxNjE2MSIgc3Ryb2tlLXdpZHRoPSIwLjciLz4KPC9nPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMi41IDUuNUwyLjUgMy41TDExLjUgMy41TDExLjUgNS41TDIuNSA1LjVaTTIgN0MxLjQ0NzcyIDcgMSA2LjU1MjI4IDEgNkwxIDNDMSAyLjQ0NzcyIDEuNDQ3NzIgMiAyIDJMMTIgMkMxMi41NTIzIDIgMTMgMi40NDc3MiAxMyAzTDEzIDZDMTMgNi41NTIyOSAxMi41NTIzIDcgMTIgN0wyIDdaIiBmaWxsPSIjNjE2MTYxIi8+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzEzN18xOTQ5OCI+CjxyZWN0IGNsYXNzPSJqcC1pY29uMyIgd2lkdGg9IjYiIGhlaWdodD0iNiIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0ibWF0cml4KDEgMS43NDg0NmUtMDcgMS43NDg0NmUtMDcgLTEgNCAxMy40NDQzKSIvPgo8L2NsaXBQYXRoPgo8L2RlZnM+Cjwvc3ZnPgo=);
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bell: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE2IDE2IiB2ZXJzaW9uPSIxLjEiPgogICA8cGF0aCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMzMzMzMzIgogICAgICBkPSJtOCAwLjI5Yy0xLjQgMC0yLjcgMC43My0zLjYgMS44LTEuMiAxLjUtMS40IDMuNC0xLjUgNS4yLTAuMTggMi4yLTAuNDQgNC0yLjMgNS4zbDAuMjggMS4zaDVjMC4wMjYgMC42NiAwLjMyIDEuMSAwLjcxIDEuNSAwLjg0IDAuNjEgMiAwLjYxIDIuOCAwIDAuNTItMC40IDAuNi0xIDAuNzEtMS41aDVsMC4yOC0xLjNjLTEuOS0wLjk3LTIuMi0zLjMtMi4zLTUuMy0wLjEzLTEuOC0wLjI2LTMuNy0xLjUtNS4yLTAuODUtMS0yLjItMS44LTMuNi0xLjh6bTAgMS40YzAuODggMCAxLjkgMC41NSAyLjUgMS4zIDAuODggMS4xIDEuMSAyLjcgMS4yIDQuNCAwLjEzIDEuNyAwLjIzIDMuNiAxLjMgNS4yaC0xMGMxLjEtMS42IDEuMi0zLjQgMS4zLTUuMiAwLjEzLTEuNyAwLjMtMy4zIDEuMi00LjQgMC41OS0wLjcyIDEuNi0xLjMgMi41LTEuM3ptLTAuNzQgMTJoMS41Yy0wLjAwMTUgMC4yOCAwLjAxNSAwLjc5LTAuNzQgMC43OS0wLjczIDAuMDAxNi0wLjcyLTAuNTMtMC43NC0wLjc5eiIgLz4KPC9zdmc+Cg==);
  --jp-icon-bug-dot: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiPgogICAgICAgIDxwYXRoIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMTcuMTkgOEgyMFYxMEgxNy45MUMxNy45NiAxMC4zMyAxOCAxMC42NiAxOCAxMVYxMkgyMFYxNEgxOC41SDE4VjE0LjAyNzVDMTUuNzUgMTQuMjc2MiAxNCAxNi4xODM3IDE0IDE4LjVDMTQgMTkuMjA4IDE0LjE2MzUgMTkuODc3OSAxNC40NTQ5IDIwLjQ3MzlDMTMuNzA2MyAyMC44MTE3IDEyLjg3NTcgMjEgMTIgMjFDOS43OCAyMSA3Ljg1IDE5Ljc5IDYuODEgMThINFYxNkg2LjA5QzYuMDQgMTUuNjcgNiAxNS4zNCA2IDE1VjE0SDRWMTJINlYxMUM2IDEwLjY2IDYuMDQgMTAuMzMgNi4wOSAxMEg0VjhINi44MUM3LjI2IDcuMjIgNy44OCA2LjU1IDguNjIgNi4wNEw3IDQuNDFMOC40MSAzTDEwLjU5IDUuMTdDMTEuMDQgNS4wNiAxMS41MSA1IDEyIDVDMTIuNDkgNSAxMi45NiA1LjA2IDEzLjQyIDUuMTdMMTUuNTkgM0wxNyA0LjQxTDE1LjM3IDYuMDRDMTYuMTIgNi41NSAxNi43NCA3LjIyIDE3LjE5IDhaTTEwIDE2SDE0VjE0SDEwVjE2Wk0xMCAxMkgxNFYxMEgxMFYxMloiIGZpbGw9IiM2MTYxNjEiLz4KICAgICAgICA8cGF0aCBkPSJNMjIgMTguNUMyMiAyMC40MzMgMjAuNDMzIDIyIDE4LjUgMjJDMTYuNTY3IDIyIDE1IDIwLjQzMyAxNSAxOC41QzE1IDE2LjU2NyAxNi41NjcgMTUgMTguNSAxNUMyMC40MzMgMTUgMjIgMTYuNTY3IDIyIDE4LjVaIiBmaWxsPSIjNjE2MTYxIi8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yMCA4aC0yLjgxYy0uNDUtLjc4LTEuMDctMS40NS0xLjgyLTEuOTZMMTcgNC40MSAxNS41OSAzbC0yLjE3IDIuMTdDMTIuOTYgNS4wNiAxMi40OSA1IDEyIDVjLS40OSAwLS45Ni4wNi0xLjQxLjE3TDguNDEgMyA3IDQuNDFsMS42MiAxLjYzQzcuODggNi41NSA3LjI2IDcuMjIgNi44MSA4SDR2MmgyLjA5Yy0uMDUuMzMtLjA5LjY2LS4wOSAxdjFINHYyaDJ2MWMwIC4zNC4wNC42Ny4wOSAxSDR2MmgyLjgxYzEuMDQgMS43OSAyLjk3IDMgNS4xOSAzczQuMTUtMS4yMSA1LjE5LTNIMjB2LTJoLTIuMDljLjA1LS4zMy4wOS0uNjYuMDktMXYtMWgydi0yaC0ydi0xYzAtLjM0LS4wNC0uNjctLjA5LTFIMjBWOHptLTYgOGgtNHYtMmg0djJ6bTAtNGgtNHYtMmg0djJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik05IDE2LjE3TDQuODMgMTJsLTEuNDIgMS40MUw5IDE5IDIxIDdsLTEuNDEtMS40MXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBzaGFwZS1yZW5kZXJpbmc9Imdlb21ldHJpY1ByZWNpc2lvbiI+CiAgICA8cGF0aCBkPSJNNi41OSwzLjQxTDIsOEw2LjU5LDEyLjZMOCwxMS4xOEw0LjgyLDhMOCw0LjgyTDYuNTksMy40MU0xMi40MSwzLjQxTDExLDQuODJMMTQuMTgsOEwxMSwxMS4xOEwxMi40MSwxMi42TDE3LDhMMTIuNDEsMy40MU0yMS41OSwxMS41OUwxMy41LDE5LjY4TDkuODMsMTZMOC40MiwxNy40MUwxMy41LDIyLjVMMjMsMTNMMjEuNTksMTEuNTlaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-collapse-all: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTggMmMxIDAgMTEgMCAxMiAwczIgMSAyIDJjMCAxIDAgMTEgMCAxMnMwIDItMiAyQzIwIDE0IDIwIDQgMjAgNFMxMCA0IDYgNGMwLTIgMS0yIDItMnoiIC8+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTE4IDhjMC0xLTEtMi0yLTJTNSA2IDQgNnMtMiAxLTIgMmMwIDEgMCAxMSAwIDEyczEgMiAyIDJjMSAwIDExIDAgMTIgMHMyLTEgMi0yYzAtMSAwLTExIDAtMTJ6bS0yIDB2MTJINFY4eiIgLz4KICAgICAgICA8cGF0aCBkPSJNNiAxM3YyaDh2LTJ6IiAvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1jb25zb2xlLWljb24tYmFja2dyb3VuZC1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtY29uc29sZS1pY29uLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIj4KICAgIDxwYXRoIGQ9Ik0xMDUgMTI3LjNoNDB2MTIuOGgtNDB6TTUxLjEgNzdMNzQgOTkuOWwtMjMuMyAyMy4zIDEwLjUgMTAuNSAyMy4zLTIzLjNMOTUgOTkuOSA4NC41IDg5LjQgNjEuNiA2Ni41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copyright: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCI+CiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0xMS44OCw5LjE0YzEuMjgsMC4wNiwxLjYxLDEuMTUsMS42MywxLjY2aDEuNzljLTAuMDgtMS45OC0xLjQ5LTMuMTktMy40NS0zLjE5QzkuNjQsNy42MSw4LDksOCwxMi4xNCBjMCwxLjk0LDAuOTMsNC4yNCwzLjg0LDQuMjRjMi4yMiwwLDMuNDEtMS42NSwzLjQ0LTIuOTVoLTEuNzljLTAuMDMsMC41OS0wLjQ1LDEuMzgtMS42MywxLjQ0QzEwLjU1LDE0LjgzLDEwLDEzLjgxLDEwLDEyLjE0IEMxMCw5LjI1LDExLjI4LDkuMTYsMTEuODgsOS4xNHogTTEyLDJDNi40OCwyLDIsNi40OCwyLDEyczQuNDgsMTAsMTAsMTBzMTAtNC40OCwxMC0xMFMxNy41MiwyLDEyLDJ6IE0xMiwyMGMtNC40MSwwLTgtMy41OS04LTggczMuNTktOCw4LThzOCwzLjU5LDgsOFMxNi40MSwyMCwxMiwyMHoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-delete: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2cHgiIGhlaWdodD0iMTZweCI+CiAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIiAvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjI2MjYyIiBkPSJNNiAxOWMwIDEuMS45IDIgMiAyaDhjMS4xIDAgMi0uOSAyLTJWN0g2djEyek0xOSA0aC0zLjVsLTEtMWgtNWwtMSAxSDV2MmgxNFY0eiIgLz4KPC9zdmc+Cg==);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-duplicate: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTIuNzk5OTggMC44NzVIOC44OTU4MkM5LjIwMDYxIDAuODc1IDkuNDQ5OTggMS4xMzkxNCA5LjQ0OTk4IDEuNDYxOThDOS40NDk5OCAxLjc4NDgyIDkuMjAwNjEgMi4wNDg5NiA4Ljg5NTgyIDIuMDQ4OTZIMy4zNTQxNUMzLjA0OTM2IDIuMDQ4OTYgMi43OTk5OCAyLjMxMzEgMi43OTk5OCAyLjYzNTk0VjkuNjc5NjlDMi43OTk5OCAxMC4wMDI1IDIuNTUwNjEgMTAuMjY2NyAyLjI0NTgyIDEwLjI2NjdDMS45NDEwMyAxMC4yNjY3IDEuNjkxNjUgMTAuMDAyNSAxLjY5MTY1IDkuNjc5NjlWMi4wNDg5NkMxLjY5MTY1IDEuNDAzMjggMi4xOTA0IDAuODc1IDIuNzk5OTggMC44NzVaTTUuMzY2NjUgMTEuOVY0LjU1SDExLjA4MzNWMTEuOUg1LjM2NjY1Wk00LjE0MTY1IDQuMTQxNjdDNC4xNDE2NSAzLjY5MDYzIDQuNTA3MjggMy4zMjUgNC45NTgzMiAzLjMyNUgxMS40OTE3QzExLjk0MjcgMy4zMjUgMTIuMzA4MyAzLjY5MDYzIDEyLjMwODMgNC4xNDE2N1YxMi4zMDgzQzEyLjMwODMgMTIuNzU5NCAxMS45NDI3IDEzLjEyNSAxMS40OTE3IDEzLjEyNUg0Ljk1ODMyQzQuNTA3MjggMTMuMTI1IDQuMTQxNjUgMTIuNzU5NCA0LjE0MTY1IDEyLjMwODNWNC4xNDE2N1oiIGZpbGw9IiM2MTYxNjEiLz4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNOS40MzU3NCA4LjI2NTA3SDguMzY0MzFWOS4zMzY1QzguMzY0MzEgOS40NTQzNSA4LjI2Nzg4IDkuNTUwNzggOC4xNTAwMiA5LjU1MDc4QzguMDMyMTcgOS41NTA3OCA3LjkzNTc0IDkuNDU0MzUgNy45MzU3NCA5LjMzNjVWOC4yNjUwN0g2Ljg2NDMxQzYuNzQ2NDUgOC4yNjUwNyA2LjY1MDAyIDguMTY4NjQgNi42NTAwMiA4LjA1MDc4QzYuNjUwMDIgNy45MzI5MiA2Ljc0NjQ1IDcuODM2NSA2Ljg2NDMxIDcuODM2NUg3LjkzNTc0VjYuNzY1MDdDNy45MzU3NCA2LjY0NzIxIDguMDMyMTcgNi41NTA3OCA4LjE1MDAyIDYuNTUwNzhDOC4yNjc4OCA2LjU1MDc4IDguMzY0MzEgNi42NDcyMSA4LjM2NDMxIDYuNzY1MDdWNy44MzY1SDkuNDM1NzRDOS41NTM2IDcuODM2NSA5LjY1MDAyIDcuOTMyOTIgOS42NTAwMiA4LjA1MDc4QzkuNjUwMDIgOC4xNjg2NCA5LjU1MzYgOC4yNjUwNyA5LjQzNTc0IDguMjY1MDdaIiBmaWxsPSIjNjE2MTYxIiBzdHJva2U9IiM2MTYxNjEiIHN0cm9rZS13aWR0aD0iMC41Ii8+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-error: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj48Y2lyY2xlIGN4PSIxMiIgY3k9IjE5IiByPSIyIi8+PHBhdGggZD0iTTEwIDNoNHYxMmgtNHoiLz48L2c+CjxwYXRoIGZpbGw9Im5vbmUiIGQ9Ik0wIDBoMjR2MjRIMHoiLz4KPC9zdmc+Cg==);
  --jp-icon-expand-all: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTggMmMxIDAgMTEgMCAxMiAwczIgMSAyIDJjMCAxIDAgMTEgMCAxMnMwIDItMiAyQzIwIDE0IDIwIDQgMjAgNFMxMCA0IDYgNGMwLTIgMS0yIDItMnoiIC8+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTE4IDhjMC0xLTEtMi0yLTJTNSA2IDQgNnMtMiAxLTIgMmMwIDEgMCAxMSAwIDEyczEgMiAyIDJjMSAwIDExIDAgMTIgMHMyLTEgMi0yYzAtMSAwLTExIDAtMTJ6bS0yIDB2MTJINFY4eiIgLz4KICAgICAgICA8cGF0aCBkPSJNMTEgMTBIOXYzSDZ2MmgzdjNoMnYtM2gzdi0yaC0zeiIgLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-dot: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTE0LDEyVjE5Ljg4QzE0LjA0LDIwLjE4IDEzLjk0LDIwLjUgMTMuNzEsMjAuNzFDMTMuMzIsMjEuMSAxMi42OSwyMS4xIDEyLjMsMjAuNzFMMTAuMjksMTguN0MxMC4wNiwxOC40NyA5Ljk2LDE4LjE2IDEwLDE3Ljg3VjEySDkuOTdMNC4yMSw0LjYyQzMuODcsNC4xOSAzLjk1LDMuNTYgNC4zOCwzLjIyQzQuNTcsMy4wOCA0Ljc4LDMgNSwzVjNIMTlWM0MxOS4yMiwzIDE5LjQzLDMuMDggMTkuNjIsMy4yMkMyMC4wNSwzLjU2IDIwLjEzLDQuMTkgMTkuNzksNC42MkwxNC4wMywxMkgxNFoiIC8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWRvdCIgZmlsbD0iI0ZGRiI+CiAgICA8Y2lyY2xlIGN4PSIxOCIgY3k9IjE3IiByPSIzIj48L2NpcmNsZT4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-filter: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTE0LDEyVjE5Ljg4QzE0LjA0LDIwLjE4IDEzLjk0LDIwLjUgMTMuNzEsMjAuNzFDMTMuMzIsMjEuMSAxMi42OSwyMS4xIDEyLjMsMjAuNzFMMTAuMjksMTguN0MxMC4wNiwxOC40NyA5Ljk2LDE4LjE2IDEwLDE3Ljg3VjEySDkuOTdMNC4yMSw0LjYyQzMuODcsNC4xOSAzLjk1LDMuNTYgNC4zOCwzLjIyQzQuNTcsMy4wOCA0Ljc4LDMgNSwzVjNIMTlWM0MxOS4yMiwzIDE5LjQzLDMuMDggMTkuNjIsMy4yMkMyMC4wNSwzLjU2IDIwLjEzLDQuMTkgMTkuNzksNC42MkwxNC4wMywxMkgxNFoiIC8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-folder-favorite: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjRweCIgZmlsbD0iIzAwMDAwMCI+CiAgPHBhdGggZD0iTTAgMGgyNHYyNEgwVjB6IiBmaWxsPSJub25lIi8+PHBhdGggY2xhc3M9ImpwLWljb24zIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxNjE2MSIgZD0iTTIwIDZoLThsLTItMkg0Yy0xLjEgMC0yIC45LTIgMnYxMmMwIDEuMS45IDIgMiAyaDE2YzEuMSAwIDItLjkgMi0yVjhjMC0xLjEtLjktMi0yLTJ6bS0yLjA2IDExTDE1IDE1LjI4IDEyLjA2IDE3bC43OC0zLjMzLTIuNTktMi4yNCAzLjQxLS4yOUwxNSA4bDEuMzQgMy4xNCAzLjQxLjI5LTIuNTkgMi4yNC43OCAzLjMzeiIvPgo8L3N2Zz4K);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-home: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjRweCIgZmlsbD0iIzAwMDAwMCI+CiAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjxwYXRoIGNsYXNzPSJqcC1pY29uMyBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xMCAyMHYtNmg0djZoNXYtOGgzTDEyIDMgMiAxMmgzdjh6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-info: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUwLjk3OCA1MC45NzgiPgoJPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KCQk8cGF0aCBkPSJNNDMuNTIsNy40NThDMzguNzExLDIuNjQ4LDMyLjMwNywwLDI1LjQ4OSwwQzE4LjY3LDAsMTIuMjY2LDIuNjQ4LDcuNDU4LDcuNDU4CgkJCWMtOS45NDMsOS45NDEtOS45NDMsMjYuMTE5LDAsMzYuMDYyYzQuODA5LDQuODA5LDExLjIxMiw3LjQ1NiwxOC4wMzEsNy40NThjMCwwLDAuMDAxLDAsMC4wMDIsMAoJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoKCQkJIE00Mi4xMDYsNDIuMTA1Yy00LjQzMiw0LjQzMS0xMC4zMzIsNi44NzItMTYuNjE1LDYuODcyaC0wLjAwMmMtNi4yODUtMC4wMDEtMTIuMTg3LTIuNDQxLTE2LjYxNy02Ljg3MgoJCQljLTkuMTYyLTkuMTYzLTkuMTYyLTI0LjA3MSwwLTMzLjIzM0MxMy4zMDMsNC40NCwxOS4yMDQsMiwyNS40ODksMmM2LjI4NCwwLDEyLjE4NiwyLjQ0LDE2LjYxNyw2Ljg3MgoJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4KCQk8cGF0aCBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1MwoJCQljMC40NjgtMC41MzYsMC45MjMtMS4wNjIsMS4zNjctMS41NzVjMC42MjYtMC43NTMsMS4xMDQtMS40NzgsMS40MzYtMi4xNzVjMC4zMzEtMC43MDcsMC40OTUtMS41NDEsMC40OTUtMi41CgkJCWMwLTEuMDk2LTAuMjYtMi4wODgtMC43NzktMi45NzljLTAuNTY1LTAuODc5LTEuNTAxLTEuMzM2LTIuODA2LTEuMzY5Yy0xLjgwMiwwLjA1Ny0yLjk4NSwwLjY2Ny0zLjU1LDEuODMyCgkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkKCQkJYzEuMDYyLTEuNjQsMi44NTUtMi40ODEsNS4zNzgtMi41MjdjMi4xNiwwLjAyMywzLjg3NCwwLjYwOCw1LjE0MSwxLjc1OGMxLjI3OCwxLjE2LDEuOTI5LDIuNzY0LDEuOTUsNC44MTEKCQkJYzAsMS4xNDItMC4xMzcsMi4xMTEtMC40MSwyLjkxMWMtMC4zMDksMC44NDUtMC43MzEsMS41OTMtMS4yNjgsMi4yNDNjLTAuNDkyLDAuNjUtMS4wNjgsMS4zMTgtMS43MywyLjAwMgoJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5CgkJCUMyNi41ODksMzIuMjE4LDIzLjU3OCwzMi4yMTgsMjMuNTc4LDMyLjIxOHogTTIzLjU3OCwzOC4yMnYtMy40ODRoMy4wNzZ2My40ODRIMjMuNTc4eiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaW5zcGVjdG9yLWljb24tY29sb3IganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtanNvbi1pY29uLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0Y5QTgyNSI+CiAgICA8cGF0aCBkPSJNMjAuMiAxMS44Yy0xLjYgMC0xLjcuNS0xLjcgMSAwIC40LjEuOS4xIDEuMy4xLjUuMS45LjEgMS4zIDAgMS43LTEuNCAyLjMtMy41IDIuM2gtLjl2LTEuOWguNWMxLjEgMCAxLjQgMCAxLjQtLjggMC0uMyAwLS42LS4xLTEgMC0uNC0uMS0uOC0uMS0xLjIgMC0xLjMgMC0xLjggMS4zLTItMS4zLS4yLTEuMy0uNy0xLjMtMiAwLS40LjEtLjguMS0xLjIuMS0uNC4xLS43LjEtMSAwLS44LS40LS43LTEuNC0uOGgtLjVWNC4xaC45YzIuMiAwIDMuNS43IDMuNSAyLjMgMCAuNC0uMS45LS4xIDEuMy0uMS41LS4xLjktLjEgMS4zIDAgLjUuMiAxIDEuNyAxdjEuOHpNMS44IDEwLjFjMS42IDAgMS43LS41IDEuNy0xIDAtLjQtLjEtLjktLjEtMS4zLS4xLS41LS4xLS45LS4xLTEuMyAwLTEuNiAxLjQtMi4zIDMuNS0yLjNoLjl2MS45aC0uNWMtMSAwLTEuNCAwLTEuNC44IDAgLjMgMCAuNi4xIDEgMCAuMi4xLjYuMSAxIDAgMS4zIDAgMS44LTEuMyAyQzYgMTEuMiA2IDExLjcgNiAxM2MwIC40LS4xLjgtLjEgMS4yLS4xLjMtLjEuNy0uMSAxIDAgLjguMy44IDEuNC44aC41djEuOWgtLjljLTIuMSAwLTMuNS0uNi0zLjUtMi4zIDAtLjQuMS0uOS4xLTEuMy4xLS41LjEtLjkuMS0xLjMgMC0uNS0uMi0xLTEuNy0xdi0xLjl6Ii8+CiAgICA8Y2lyY2xlIGN4PSIxMSIgY3k9IjEzLjgiIHI9IjIuMSIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSI4LjIiIHI9IjIuMSIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-julia: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDMyNSAzMDAiPgogIDxnIGNsYXNzPSJqcC1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjY2IzYzMzIj4KICAgIDxwYXRoIGQ9Ik0gMTUwLjg5ODQzOCAyMjUgQyAxNTAuODk4NDM4IDI2Ni40MjE4NzUgMTE3LjMyMDMxMiAzMDAgNzUuODk4NDM4IDMwMCBDIDM0LjQ3NjU2MiAzMDAgMC44OTg0MzggMjY2LjQyMTg3NSAwLjg5ODQzOCAyMjUgQyAwLjg5ODQzOCAxODMuNTc4MTI1IDM0LjQ3NjU2MiAxNTAgNzUuODk4NDM4IDE1MCBDIDExNy4zMjAzMTIgMTUwIDE1MC44OTg0MzggMTgzLjU3ODEyNSAxNTAuODk4NDM4IDIyNSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzM4OTgyNiI+CiAgICA8cGF0aCBkPSJNIDIzNy41IDc1IEMgMjM3LjUgMTE2LjQyMTg3NSAyMDMuOTIxODc1IDE1MCAxNjIuNSAxNTAgQyAxMjEuMDc4MTI1IDE1MCA4Ny41IDExNi40MjE4NzUgODcuNSA3NSBDIDg3LjUgMzMuNTc4MTI1IDEyMS4wNzgxMjUgMCAxNjIuNSAwIEMgMjAzLjkyMTg3NSAwIDIzNy41IDMzLjU3ODEyNSAyMzcuNSA3NSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzk1NThiMiI+CiAgICA8cGF0aCBkPSJNIDMyNC4xMDE1NjIgMjI1IEMgMzI0LjEwMTU2MiAyNjYuNDIxODc1IDI5MC41MjM0MzggMzAwIDI0OS4xMDE1NjIgMzAwIEMgMjA3LjY3OTY4OCAzMDAgMTc0LjEwMTU2MiAyNjYuNDIxODc1IDE3NC4xMDE1NjIgMjI1IEMgMTc0LjEwMTU2MiAxODMuNTc4MTI1IDIwNy42Nzk2ODggMTUwIDI0OS4xMDE1NjIgMTUwIEMgMjkwLjUyMzQzOCAxNTAgMzI0LjEwMTU2MiAxODMuNTc4MTI1IDMyNC4xMDE1NjIgMjI1Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgPGcgY2xhc3M9ImpwLWp1cHl0ZXItaWNvbi1jb2xvciIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgIDxnIGNsYXNzPSJqcC1qdXB5dGVyLWljb24tY29sb3IiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launch: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMzIgMzIiIHdpZHRoPSIzMiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yNiwyOEg2YTIuMDAyNywyLjAwMjcsMCwwLDEtMi0yVjZBMi4wMDI3LDIuMDAyNywwLDAsMSw2LDRIMTZWNkg2VjI2SDI2VjE2aDJWMjZBMi4wMDI3LDIuMDAyNywwLDAsMSwyNiwyOFoiLz4KICAgIDxwb2x5Z29uIHBvaW50cz0iMjAgMiAyMCA0IDI2LjU4NiA0IDE4IDEyLjU4NiAxOS40MTQgMTQgMjggNS40MTQgMjggMTIgMzAgMTIgMzAgMiAyMCAyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4K);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-move-down: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNMTIuNDcxIDcuNTI4OTlDMTIuNzYzMiA3LjIzNjg0IDEyLjc2MzIgNi43NjMxNiAxMi40NzEgNi40NzEwMVY2LjQ3MTAxQzEyLjE3OSA2LjE3OTA1IDExLjcwNTcgNi4xNzg4NCAxMS40MTM1IDYuNDcwNTRMNy43NSAxMC4xMjc1VjEuNzVDNy43NSAxLjMzNTc5IDcuNDE0MjEgMSA3IDFWMUM2LjU4NTc5IDEgNi4yNSAxLjMzNTc5IDYuMjUgMS43NVYxMC4xMjc1TDIuNTk3MjYgNi40NjgyMkMyLjMwMzM4IDYuMTczODEgMS44MjY0MSA2LjE3MzU5IDEuNTMyMjYgNi40Njc3NFY2LjQ2Nzc0QzEuMjM4MyA2Ljc2MTcgMS4yMzgzIDcuMjM4MyAxLjUzMjI2IDcuNTMyMjZMNi4yOTI4OSAxMi4yOTI5QzYuNjgzNDIgMTIuNjgzNCA3LjMxNjU4IDEyLjY4MzQgNy43MDcxMSAxMi4yOTI5TDEyLjQ3MSA3LjUyODk5WiIgZmlsbD0iIzYxNjE2MSIvPgo8L3N2Zz4K);
  --jp-icon-move-up: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNMS41Mjg5OSA2LjQ3MTAxQzEuMjM2ODQgNi43NjMxNiAxLjIzNjg0IDcuMjM2ODQgMS41Mjg5OSA3LjUyODk5VjcuNTI4OTlDMS44MjA5NSA3LjgyMDk1IDIuMjk0MjYgNy44MjExNiAyLjU4NjQ5IDcuNTI5NDZMNi4yNSAzLjg3MjVWMTIuMjVDNi4yNSAxMi42NjQyIDYuNTg1NzkgMTMgNyAxM1YxM0M3LjQxNDIxIDEzIDcuNzUgMTIuNjY0MiA3Ljc1IDEyLjI1VjMuODcyNUwxMS40MDI3IDcuNTMxNzhDMTEuNjk2NiA3LjgyNjE5IDEyLjE3MzYgNy44MjY0MSAxMi40Njc3IDcuNTMyMjZWNy41MzIyNkMxMi43NjE3IDcuMjM4MyAxMi43NjE3IDYuNzYxNyAxMi40Njc3IDYuNDY3NzRMNy43MDcxMSAxLjcwNzExQzcuMzE2NTggMS4zMTY1OCA2LjY4MzQyIDEuMzE2NTggNi4yOTI4OSAxLjcwNzExTDEuNTI4OTkgNi40NzEwMVoiIGZpbGw9IiM2MTYxNjEiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtbm90ZWJvb2staWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iLTEwIC0xMCAxMzEuMTYxMzYxNjk0MzM1OTQgMTMyLjM4ODk5OTkzODk2NDg0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMzA2OTk4IiBkPSJNIDU0LjkxODc4NSw5LjE5Mjc0MjFlLTQgQyA1MC4zMzUxMzIsMC4wMjIyMTcyNyA0NS45NTc4NDYsMC40MTMxMzY5NyA0Mi4xMDYyODUsMS4wOTQ2NjkzIDMwLjc2MDA2OSwzLjA5OTE3MzEgMjguNzAwMDM2LDcuMjk0NzcxNCAyOC43MDAwMzUsMTUuMDMyMTY5IHYgMTAuMjE4NzUgaCAyNi44MTI1IHYgMy40MDYyNSBoIC0yNi44MTI1IC0xMC4wNjI1IGMgLTcuNzkyNDU5LDAgLTE0LjYxNTc1ODgsNC42ODM3MTcgLTE2Ljc0OTk5OTgsMTMuNTkzNzUgLTIuNDYxODE5OTgsMTAuMjEyOTY2IC0yLjU3MTAxNTA4LDE2LjU4NjAyMyAwLDI3LjI1IDEuOTA1OTI4Myw3LjkzNzg1MiA2LjQ1NzU0MzIsMTMuNTkzNzQ4IDE0LjI0OTk5OTgsMTMuNTkzNzUgaCA5LjIxODc1IHYgLTEyLjI1IGMgMCwtOC44NDk5MDIgNy42NTcxNDQsLTE2LjY1NjI0OCAxNi43NSwtMTYuNjU2MjUgaCAyNi43ODEyNSBjIDcuNDU0OTUxLDAgMTMuNDA2MjUzLC02LjEzODE2NCAxMy40MDYyNSwtMTMuNjI1IHYgLTI1LjUzMTI1IGMgMCwtNy4yNjYzMzg2IC02LjEyOTk4LC0xMi43MjQ3NzcxIC0xMy40MDYyNSwtMTMuOTM3NDk5NyBDIDY0LjI4MTU0OCwwLjMyNzk0Mzk3IDU5LjUwMjQzOCwtMC4wMjAzNzkwMyA1NC45MTg3ODUsOS4xOTI3NDIxZS00IFogbSAtMTQuNSw4LjIxODc1MDEyNTc5IGMgMi43Njk1NDcsMCA1LjAzMTI1LDIuMjk4NjQ1NiA1LjAzMTI1LDUuMTI0OTk5NiAtMmUtNiwyLjgxNjMzNiAtMi4yNjE3MDMsNS4wOTM3NSAtNS4wMzEyNSw1LjA5Mzc1IC0yLjc3OTQ3NiwtMWUtNiAtNS4wMzEyNSwtMi4yNzc0MTUgLTUuMDMxMjUsLTUuMDkzNzUgLTEwZS03LC0yLjgyNjM1MyAyLjI1MTc3NCwtNS4xMjQ5OTk2IDUuMDMxMjUsLTUuMTI0OTk5NiB6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2ZmZDQzYiIgZD0ibSA4NS42Mzc1MzUsMjguNjU3MTY5IHYgMTEuOTA2MjUgYyAwLDkuMjMwNzU1IC03LjgyNTg5NSwxNi45OTk5OTkgLTE2Ljc1LDE3IGggLTI2Ljc4MTI1IGMgLTcuMzM1ODMzLDAgLTEzLjQwNjI0OSw2LjI3ODQ4MyAtMTMuNDA2MjUsMTMuNjI1IHYgMjUuNTMxMjQ3IGMgMCw3LjI2NjM0NCA2LjMxODU4OCwxMS41NDAzMjQgMTMuNDA2MjUsMTMuNjI1MDA0IDguNDg3MzMxLDIuNDk1NjEgMTYuNjI2MjM3LDIuOTQ2NjMgMjYuNzgxMjUsMCA2Ljc1MDE1NSwtMS45NTQzOSAxMy40MDYyNTMsLTUuODg3NjEgMTMuNDA2MjUsLTEzLjYyNTAwNCBWIDg2LjUwMDkxOSBoIC0yNi43ODEyNSB2IC0zLjQwNjI1IGggMjYuNzgxMjUgMTMuNDA2MjU0IGMgNy43OTI0NjEsMCAxMC42OTYyNTEsLTUuNDM1NDA4IDEzLjQwNjI0MSwtMTMuNTkzNzUgMi43OTkzMywtOC4zOTg4ODYgMi42ODAyMiwtMTYuNDc1Nzc2IDAsLTI3LjI1IC0xLjkyNTc4LC03Ljc1NzQ0MSAtNS42MDM4NywtMTMuNTkzNzUgLTEzLjQwNjI0MSwtMTMuNTkzNzUgeiBtIC0xNS4wNjI1LDY0LjY1NjI1IGMgMi43Nzk0NzgsM2UtNiA1LjAzMTI1LDIuMjc3NDE3IDUuMDMxMjUsNS4wOTM3NDcgLTJlLTYsMi44MjYzNTQgLTIuMjUxNzc1LDUuMTI1MDA0IC01LjAzMTI1LDUuMTI1MDA0IC0yLjc2OTU1LDAgLTUuMDMxMjUsLTIuMjk4NjUgLTUuMDMxMjUsLTUuMTI1MDA0IDJlLTYsLTIuODE2MzMgMi4yNjE2OTcsLTUuMDkzNzQ3IDUuMDMxMjUsLTUuMDkzNzQ3IHoiLz4KPC9zdmc+Cg==);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-share: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTSAxOCAyIEMgMTYuMzU0OTkgMiAxNSAzLjM1NDk5MDQgMTUgNSBDIDE1IDUuMTkwOTUyOSAxNS4wMjE3OTEgNS4zNzcxMjI0IDE1LjA1NjY0MSA1LjU1ODU5MzggTCA3LjkyMTg3NSA5LjcyMDcwMzEgQyA3LjM5ODUzOTkgOS4yNzc4NTM5IDYuNzMyMDc3MSA5IDYgOSBDIDQuMzU0OTkwNCA5IDMgMTAuMzU0OTkgMyAxMiBDIDMgMTMuNjQ1MDEgNC4zNTQ5OTA0IDE1IDYgMTUgQyA2LjczMjA3NzEgMTUgNy4zOTg1Mzk5IDE0LjcyMjE0NiA3LjkyMTg3NSAxNC4yNzkyOTcgTCAxNS4wNTY2NDEgMTguNDM5NDUzIEMgMTUuMDIxNTU1IDE4LjYyMTUxNCAxNSAxOC44MDgzODYgMTUgMTkgQyAxNSAyMC42NDUwMSAxNi4zNTQ5OSAyMiAxOCAyMiBDIDE5LjY0NTAxIDIyIDIxIDIwLjY0NTAxIDIxIDE5IEMgMjEgMTcuMzU0OTkgMTkuNjQ1MDEgMTYgMTggMTYgQyAxNy4yNjc0OCAxNiAxNi42MDE1OTMgMTYuMjc5MzI4IDE2LjA3ODEyNSAxNi43MjI2NTYgTCA4Ljk0MzM1OTQgMTIuNTU4NTk0IEMgOC45NzgyMDk1IDEyLjM3NzEyMiA5IDEyLjE5MDk1MyA5IDEyIEMgOSAxMS44MDkwNDcgOC45NzgyMDk1IDExLjYyMjg3OCA4Ljk0MzM1OTQgMTEuNDQxNDA2IEwgMTYuMDc4MTI1IDcuMjc5Mjk2OSBDIDE2LjYwMTQ2IDcuNzIyMTQ2MSAxNy4yNjc5MjMgOCAxOCA4IEMgMTkuNjQ1MDEgOCAyMSA2LjY0NTAwOTYgMjEgNSBDIDIxIDMuMzU0OTkwNCAxOS42NDUwMSAyIDE4IDIgeiBNIDE4IDQgQyAxOC41NjQxMjkgNCAxOSA0LjQzNTg3MDYgMTkgNSBDIDE5IDUuNTY0MTI5NCAxOC41NjQxMjkgNiAxOCA2IEMgMTcuNDM1ODcxIDYgMTcgNS41NjQxMjk0IDE3IDUgQyAxNyA0LjQzNTg3MDYgMTcuNDM1ODcxIDQgMTggNCB6IE0gNiAxMSBDIDYuNTY0MTI5NCAxMSA3IDExLjQzNTg3MSA3IDEyIEMgNyAxMi41NjQxMjkgNi41NjQxMjk0IDEzIDYgMTMgQyA1LjQzNTg3MDYgMTMgNSAxMi41NjQxMjkgNSAxMiBDIDUgMTEuNDM1ODcxIDUuNDM1ODcwNiAxMSA2IDExIHogTSAxOCAxOCBDIDE4LjU2NDEyOSAxOCAxOSAxOC40MzU4NzEgMTkgMTkgQyAxOSAxOS41NjQxMjkgMTguNTY0MTI5IDIwIDE4IDIwIEMgMTcuNDM1ODcxIDIwIDE3IDE5LjU2NDEyOSAxNyAxOSBDIDE3IDE4LjQzNTg3MSAxNy40MzU4NzEgMTggMTggMTggeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtdGVybWluYWwtaWNvbi1iYWNrZ3JvdW5kLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZSIgd2lkdGg9IjIwIiBoZWlnaHQ9IjIwIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyIDIpIiBmaWxsPSIjMzMzMzMzIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtdGVybWluYWwtaWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUtaW52ZXJzZSIgZD0iTTUuMDU2NjQgOC43NjE3MkM1LjA1NjY0IDguNTk3NjYgNS4wMzEyNSA4LjQ1MzEyIDQuOTgwNDcgOC4zMjgxMkM0LjkzMzU5IDguMTk5MjIgNC44NTU0NyA4LjA4MjAzIDQuNzQ2MDkgNy45NzY1NkM0LjY0MDYyIDcuODcxMDkgNC41IDcuNzc1MzkgNC4zMjQyMiA3LjY4OTQ1QzQuMTUyMzQgNy41OTk2MSAzLjk0MzM2IDcuNTExNzIgMy42OTcyNyA3LjQyNTc4QzMuMzAyNzMgNy4yODUxNiAyLjk0MzM2IDcuMTM2NzIgMi42MTkxNCA2Ljk4MDQ3QzIuMjk0OTIgNi44MjQyMiAyLjAxNzU4IDYuNjQyNTggMS43ODcxMSA2LjQzNTU1QzEuNTYwNTUgNi4yMjg1MiAxLjM4NDc3IDUuOTg4MjggMS4yNTk3NyA1LjcxNDg0QzEuMTM0NzcgNS40Mzc1IDEuMDcyMjcgNS4xMDkzOCAxLjA3MjI3IDQuNzMwNDdDMS4wNzIyNyA0LjM5ODQ0IDEuMTI4OTEgNC4wOTU3IDEuMjQyMTkgMy44MjIyN0MxLjM1NTQ3IDMuNTQ0OTIgMS41MTU2MiAzLjMwNDY5IDEuNzIyNjYgMy4xMDE1NkMxLjkyOTY5IDIuODk4NDQgMi4xNzk2OSAyLjczNDM3IDIuNDcyNjYgMi42MDkzOEMyLjc2NTYyIDIuNDg0MzggMy4wOTE4IDIuNDA0MyAzLjQ1MTE3IDIuMzY5MTRWMS4xMDkzOEg0LjM4ODY3VjIuMzgwODZDNC43NDAyMyAyLjQyNzczIDUuMDU2NjQgMi41MjM0NCA1LjMzNzg5IDIuNjY3OTdDNS42MTkxNCAyLjgxMjUgNS44NTc0MiAzLjAwMTk1IDYuMDUyNzMgMy4yMzYzM0M2LjI1MTk1IDMuNDY2OCA2LjQwNDMgMy43NDAyMyA2LjUwOTc3IDQuMDU2NjRDNi42MTkxNCA0LjM2OTE0IDYuNjczODMgNC43MjA3IDYuNjczODMgNS4xMTEzM0g1LjA0NDkyQzUuMDQ0OTIgNC42Mzg2NyA0LjkzNzUgNC4yODEyNSA0LjcyMjY2IDQuMDM5MDZDNC41MDc4MSAzLjc5Mjk3IDQuMjE2OCAzLjY2OTkyIDMuODQ5NjEgMy42Njk5MkMzLjY1MDM5IDMuNjY5OTIgMy40NzY1NiAzLjY5NzI3IDMuMzI4MTIgMy43NTE5NUMzLjE4MzU5IDMuODAyNzMgMy4wNjQ0NSAzLjg3Njk1IDIuOTcwNyAzLjk3NDYxQzIuODc2OTUgNC4wNjgzNiAyLjgwNjY0IDQuMTc5NjkgMi43NTk3NyA0LjMwODU5QzIuNzE2OCA0LjQzNzUgMi42OTUzMSA0LjU3ODEyIDIuNjk1MzEgNC43MzA0N0MyLjY5NTMxIDQuODgyODEgMi43MTY4IDUuMDE5NTMgMi43NTk3NyA1LjE0MDYyQzIuODA2NjQgNS4yNTc4MSAyLjg4MjgxIDUuMzY3MTkgMi45ODgyOCA1LjQ2ODc1QzMuMDk3NjYgNS41NzAzMSAzLjI0MDIzIDUuNjY3OTcgMy40MTYwMiA1Ljc2MTcyQzMuNTkxOCA1Ljg1MTU2IDMuODEwNTUgNS45NDMzNiA0LjA3MjI3IDYuMDM3MTFDNC40NjY4IDYuMTg1NTUgNC44MjQyMiA2LjMzOTg0IDUuMTQ0NTMgNi41QzUuNDY0ODQgNi42NTYyNSA1LjczODI4IDYuODM5ODQgNS45NjQ4NCA3LjA1MDc4QzYuMTk1MzEgNy4yNTc4MSA2LjM3MTA5IDcuNSA2LjQ5MjE5IDcuNzc3MzRDNi42MTcxOSA4LjA1MDc4IDYuNjc5NjkgOC4zNzUgNi42Nzk2OSA4Ljc1QzYuNjc5NjkgOS4wOTM3NSA2LjYyMzA1IDkuNDA0MyA2LjUwOTc3IDkuNjgxNjRDNi4zOTY0OCA5Ljk1NTA4IDYuMjM0MzggMTAuMTkxNCA2LjAyMzQ0IDEwLjM5MDZDNS44MTI1IDEwLjU4OTggNS41NTg1OSAxMC43NSA1LjI2MTcyIDEwLjg3MTFDNC45NjQ4NCAxMC45ODgzIDQuNjMyODEgMTEuMDY0NSA0LjI2NTYyIDExLjA5OTZWMTIuMjQ4SDMuMzMzOThWMTEuMDk5NkMzLjAwMTk1IDExLjA2ODQgMi42Nzk2OSAxMC45OTYxIDIuMzY3MTkgMTAuODgyOEMyLjA1NDY5IDEwLjc2NTYgMS43NzczNCAxMC41OTc3IDEuNTM1MTYgMTAuMzc4OUMxLjI5Njg4IDEwLjE2MDIgMS4xMDU0NyA5Ljg4NDc3IDAuOTYwOTM4IDkuNTUyNzNDMC44MTY0MDYgOS4yMTY4IDAuNzQ0MTQxIDguODE0NDUgMC43NDQxNDEgOC4zNDU3SDIuMzc4OTFDMi4zNzg5MSA4LjYyNjk1IDIuNDE5OTIgOC44NjMyOCAyLjUwMTk1IDkuMDU0NjlDMi41ODM5OCA5LjI0MjE5IDIuNjg5NDUgOS4zOTI1OCAyLjgxODM2IDkuNTA1ODZDMi45NTExNyA5LjYxNTIzIDMuMTAxNTYgOS42OTMzNiAzLjI2OTUzIDkuNzQwMjNDMy40Mzc1IDkuNzg3MTEgMy42MDkzOCA5LjgxMDU1IDMuNzg1MTYgOS44MTA1NUM0LjIwMzEyIDkuODEwNTUgNC41MTk1MyA5LjcxMjg5IDQuNzM0MzggOS41MTc1OEM0Ljk0OTIyIDkuMzIyMjcgNS4wNTY2NCA5LjA3MDMxIDUuMDU2NjQgOC43NjE3MlpNMTMuNDE4IDEyLjI3MTVIOC4wNzQyMlYxMUgxMy40MThWMTIuMjcxNVoiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMuOTUyNjQgNikiIGZpbGw9IndoaXRlIi8+Cjwvc3ZnPgo=);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtdGV4dC1lZGl0b3ItaWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xNSAxNUgzdjJoMTJ2LTJ6bTAtOEgzdjJoMTJWN3pNMyAxM2gxOHYtMkgzdjJ6bTAgOGgxOHYtMkgzdjJ6TTMgM3YyaDE4VjNIM3oiLz4KPC9zdmc+Cg==);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik03LDVIMjFWN0g3VjVNNywxM1YxMUgyMVYxM0g3TTQsNC41QTEuNSwxLjUgMCAwLDEgNS41LDZBMS41LDEuNSAwIDAsMSA0LDcuNUExLjUsMS41IDAgMCwxIDIuNSw2QTEuNSwxLjUgMCAwLDEgNCw0LjVNNCwxMC41QTEuNSwxLjUgMCAwLDEgNS41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMy41QTEuNSwxLjUgMCAwLDEgMi41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMC41TTcsMTlWMTdIMjFWMTlIN000LDE2LjVBMS41LDEuNSAwIDAsMSA1LjUsMThBMS41LDEuNSAwIDAsMSA0LDE5LjVBMS41LDEuNSAwIDAsMSAyLjUsMThBMS41LDEuNSAwIDAsMSA0LDE2LjVaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-user: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE2IDdhNCA0IDAgMTEtOCAwIDQgNCAwIDAxOCAwek0xMiAxNGE3IDcgMCAwMC03IDdoMTRhNyA3IDAgMDAtNy03eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-users: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZlcnNpb249IjEuMSIgdmlld0JveD0iMCAwIDM2IDI0IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPgogPGcgY2xhc3M9ImpwLWljb24zIiB0cmFuc2Zvcm09Im1hdHJpeCgxLjczMjcgMCAwIDEuNzMyNyAtMy42MjgyIC4wOTk1NzcpIiBmaWxsPSIjNjE2MTYxIj4KICA8cGF0aCB0cmFuc2Zvcm09Im1hdHJpeCgxLjUsMCwwLDEuNSwwLC02KSIgZD0ibTEyLjE4NiA3LjUwOThjLTEuMDUzNSAwLTEuOTc1NyAwLjU2NjUtMi40Nzg1IDEuNDEwMiAwLjc1MDYxIDAuMzEyNzcgMS4zOTc0IDAuODI2NDggMS44NzMgMS40NzI3aDMuNDg2M2MwLTEuNTkyLTEuMjg4OS0yLjg4MjgtMi44ODA5LTIuODgyOHoiLz4KICA8cGF0aCBkPSJtMjAuNDY1IDIuMzg5NWEyLjE4ODUgMi4xODg1IDAgMCAxLTIuMTg4NCAyLjE4ODUgMi4xODg1IDIuMTg4NSAwIDAgMS0yLjE4ODUtMi4xODg1IDIuMTg4NSAyLjE4ODUgMCAwIDEgMi4xODg1LTIuMTg4NSAyLjE4ODUgMi4xODg1IDAgMCAxIDIuMTg4NCAyLjE4ODV6Ii8+CiAgPHBhdGggdHJhbnNmb3JtPSJtYXRyaXgoMS41LDAsMCwxLjUsMCwtNikiIGQ9Im0zLjU4OTggOC40MjE5Yy0xLjExMjYgMC0yLjAxMzcgMC45MDExMS0yLjAxMzcgMi4wMTM3aDIuODE0NWMwLjI2Nzk3LTAuMzczMDkgMC41OTA3LTAuNzA0MzUgMC45NTg5OC0wLjk3ODUyLTAuMzQ0MzMtMC42MTY4OC0xLjAwMzEtMS4wMzUyLTEuNzU5OC0xLjAzNTJ6Ii8+CiAgPHBhdGggZD0ibTYuOTE1NCA0LjYyM2ExLjUyOTQgMS41Mjk0IDAgMCAxLTEuNTI5NCAxLjUyOTQgMS41Mjk0IDEuNTI5NCAwIDAgMS0xLjUyOTQtMS41Mjk0IDEuNTI5NCAxLjUyOTQgMCAwIDEgMS41Mjk0LTEuNTI5NCAxLjUyOTQgMS41Mjk0IDAgMCAxIDEuNTI5NCAxLjUyOTR6Ii8+CiAgPHBhdGggZD0ibTYuMTM1IDEzLjUzNWMwLTMuMjM5MiAyLjYyNTktNS44NjUgNS44NjUtNS44NjUgMy4yMzkyIDAgNS44NjUgMi42MjU5IDUuODY1IDUuODY1eiIvPgogIDxjaXJjbGUgY3g9IjEyIiBjeT0iMy43Njg1IiByPSIyLjk2ODUiLz4KIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-word: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KIDxnIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzQxNDE0MSI+CiAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiA8L2c+CiA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSguNDMgLjA0MDEpIiBmaWxsPSIjZmZmIj4KICA8cGF0aCBkPSJtNC4xNCA4Ljc2cTAuMDY4Mi0xLjg5IDIuNDItMS44OSAxLjE2IDAgMS42OCAwLjQyIDAuNTY3IDAuNDEgMC41NjcgMS4xNnYzLjQ3cTAgMC40NjIgMC41MTQgMC40NjIgMC4xMDMgMCAwLjItMC4wMjMxdjAuNzE0cS0wLjM5OSAwLjEwMy0wLjY1MSAwLjEwMy0wLjQ1MiAwLTAuNjkzLTAuMjItMC4yMzEtMC4yLTAuMjg0LTAuNjYyLTAuOTU2IDAuODcyLTIgMC44NzItMC45MDMgMC0xLjQ3LTAuNDcyLTAuNTI1LTAuNDcyLTAuNTI1LTEuMjYgMC0wLjI2MiAwLjA0NTItMC40NzIgMC4wNTY3LTAuMjIgMC4xMTYtMC4zNzggMC4wNjgyLTAuMTY4IDAuMjMxLTAuMzA0IDAuMTU4LTAuMTQ3IDAuMjYyLTAuMjQyIDAuMTE2LTAuMDkxNCAwLjM2OC0wLjE2OCAwLjI2Mi0wLjA5MTQgMC4zOTktMC4xMjYgMC4xMzYtMC4wNDUyIDAuNDcyLTAuMTAzIDAuMzM2LTAuMDU3OCAwLjUwNC0wLjA3OTggMC4xNTgtMC4wMjMxIDAuNTY3LTAuMDc5OCAwLjU1Ni0wLjA2ODIgMC43NzctMC4yMjEgMC4yMi0wLjE1MiAwLjIyLTAuNDQxdi0wLjI1MnEwLTAuNDMtMC4zNTctMC42NjItMC4zMzYtMC4yMzEtMC45NzYtMC4yMzEtMC42NjIgMC0wLjk5OCAwLjI2Mi0wLjMzNiAwLjI1Mi0wLjM5OSAwLjc5OHptMS44OSAzLjY4cTAuNzg4IDAgMS4yNi0wLjQxIDAuNTA0LTAuNDIgMC41MDQtMC45MDN2LTEuMDVxLTAuMjg0IDAuMTM2LTAuODYxIDAuMjMxLTAuNTY3IDAuMDkxNC0wLjk4NyAwLjE1OC0wLjQyIDAuMDY4Mi0wLjc2NiAwLjMyNi0wLjMzNiAwLjI1Mi0wLjMzNiAwLjcwNHQwLjMwNCAwLjcwNCAwLjg2MSAwLjI1MnoiIHN0cm9rZS13aWR0aD0iMS4wNSIvPgogIDxwYXRoIGQ9Im0xMCA0LjU2aDAuOTQ1djMuMTVxMC42NTEtMC45NzYgMS44OS0wLjk3NiAxLjE2IDAgMS44OSAwLjg0IDAuNjgyIDAuODQgMC42ODIgMi4zMSAwIDEuNDctMC43MDQgMi40Mi0wLjcwNCAwLjg4Mi0xLjg5IDAuODgyLTEuMjYgMC0xLjg5LTEuMDJ2MC43NjZoLTAuODV6bTIuNjIgMy4wNHEtMC43NDYgMC0xLjE2IDAuNjQtMC40NTIgMC42My0wLjQ1MiAxLjY4IDAgMS4wNSAwLjQ1MiAxLjY4dDEuMTYgMC42M3EwLjc3NyAwIDEuMjYtMC42MyAwLjQ5NC0wLjY0IDAuNDk0LTEuNjggMC0xLjA1LTAuNDcyLTEuNjgtMC40NjItMC42NC0xLjI2LTAuNjR6IiBzdHJva2Utd2lkdGg9IjEuMDUiLz4KICA8cGF0aCBkPSJtMi43MyAxNS44IDEzLjYgMC4wMDgxYzAuMDA2OSAwIDAtMi42IDAtMi42IDAtMC4wMDc4LTEuMTUgMC0xLjE1IDAtMC4wMDY5IDAtMC4wMDgzIDEuNS0wLjAwODMgMS41LTJlLTMgLTAuMDAxNC0xMS4zLTAuMDAxNC0xMS4zLTAuMDAxNGwtMC4wMDU5Mi0xLjVjMC0wLjAwNzgtMS4xNyAwLjAwMTMtMS4xNyAwLjAwMTN6IiBzdHJva2Utd2lkdGg9Ii45NzUiLz4KIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddAboveIcon {
  background-image: var(--jp-icon-add-above);
}

.jp-AddBelowIcon {
  background-image: var(--jp-icon-add-below);
}

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}

.jp-BellIcon {
  background-image: var(--jp-icon-bell);
}

.jp-BugDotIcon {
  background-image: var(--jp-icon-bug-dot);
}

.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}

.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}

.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}

.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}

.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}

.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}

.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}

.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}

.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}

.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}

.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}

.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}

.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}

.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}

.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}

.jp-CodeCheckIcon {
  background-image: var(--jp-icon-code-check);
}

.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}

.jp-CollapseAllIcon {
  background-image: var(--jp-icon-collapse-all);
}

.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}

.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}

.jp-CopyrightIcon {
  background-image: var(--jp-icon-copyright);
}

.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}

.jp-DeleteIcon {
  background-image: var(--jp-icon-delete);
}

.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}

.jp-DuplicateIcon {
  background-image: var(--jp-icon-duplicate);
}

.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}

.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}

.jp-ErrorIcon {
  background-image: var(--jp-icon-error);
}

.jp-ExpandAllIcon {
  background-image: var(--jp-icon-expand-all);
}

.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}

.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}

.jp-FileIcon {
  background-image: var(--jp-icon-file);
}

.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}

.jp-FilterDotIcon {
  background-image: var(--jp-icon-filter-dot);
}

.jp-FilterIcon {
  background-image: var(--jp-icon-filter);
}

.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}

.jp-FolderFavoriteIcon {
  background-image: var(--jp-icon-folder-favorite);
}

.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}

.jp-HomeIcon {
  background-image: var(--jp-icon-home);
}

.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}

.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}

.jp-InfoIcon {
  background-image: var(--jp-icon-info);
}

.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}

.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}

.jp-JuliaIcon {
  background-image: var(--jp-icon-julia);
}

.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}

.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}

.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}

.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}

.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}

.jp-LaunchIcon {
  background-image: var(--jp-icon-launch);
}

.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}

.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}

.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}

.jp-ListIcon {
  background-image: var(--jp-icon-list);
}

.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}

.jp-MoveDownIcon {
  background-image: var(--jp-icon-move-down);
}

.jp-MoveUpIcon {
  background-image: var(--jp-icon-move-up);
}

.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}

.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}

.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}

.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}

.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}

.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}

.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}

.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}

.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}

.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}

.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}

.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}

.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}

.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}

.jp-RunIcon {
  background-image: var(--jp-icon-run);
}

.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}

.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}

.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}

.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}

.jp-ShareIcon {
  background-image: var(--jp-icon-share);
}

.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}

.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}

.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}

.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}

.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}

.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}

.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}

.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}

.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}

.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}

.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}

.jp-UserIcon {
  background-image: var(--jp-icon-user);
}

.jp-UsersIcon {
  background-image: var(--jp-icon-users);
}

.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}

.jp-WordIcon {
  background-image: var(--jp-icon-word);
}

.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.lm-TabBar .lm-TabBar-addButton {
  align-items: center;
  display: flex;
  padding: 4px;
  padding-bottom: 5px;
  margin-right: 1px;
  background-color: var(--jp-layout-color2);
}

.lm-TabBar .lm-TabBar-addButton:hover {
  background-color: var(--jp-layout-color1);
}

.lm-DockPanel-tabBar .lm-TabBar-tab {
  width: var(--jp-private-horizontal-tab-width);
}

.lm-DockPanel-tabBar .lm-TabBar-content {
  flex: unset;
}

.lm-DockPanel-tabBar[data-orientation='horizontal'] {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}

/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}

.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}

.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}

.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}

.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}

.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}

.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}

.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}

.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}

/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}

.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}

.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}

.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}

.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}

.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}

.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}

/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}

.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}

.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}

.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}

.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}

.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}

.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

.jp-icon-dot[fill] {
  fill: var(--jp-warn-color0);
}

.jp-jupyter-icon-color[fill] {
  fill: var(--jp-jupyter-icon-color, var(--jp-warn-color0));
}

.jp-notebook-icon-color[fill] {
  fill: var(--jp-notebook-icon-color, var(--jp-warn-color0));
}

.jp-json-icon-color[fill] {
  fill: var(--jp-json-icon-color, var(--jp-warn-color1));
}

.jp-console-icon-color[fill] {
  fill: var(--jp-console-icon-color, white);
}

.jp-console-icon-background-color[fill] {
  fill: var(--jp-console-icon-background-color, var(--jp-brand-color1));
}

.jp-terminal-icon-color[fill] {
  fill: var(--jp-terminal-icon-color, var(--jp-layout-color2));
}

.jp-terminal-icon-background-color[fill] {
  fill: var(
    --jp-terminal-icon-background-color,
    var(--jp-inverse-layout-color2)
  );
}

.jp-text-editor-icon-color[fill] {
  fill: var(--jp-text-editor-icon-color, var(--jp-inverse-layout-color3));
}

.jp-inspector-icon-color[fill] {
  fill: var(--jp-inspector-icon-color, var(--jp-inverse-layout-color3));
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* stylelint-disable selector-max-class, selector-max-compound-selectors */

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}

.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* stylelint-enable selector-max-class, selector-max-compound-selectors */

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) .jp-icon-hoverShow-content {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `lm-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FormGroup-content fieldset {
  border: none;
  padding: 0;
  min-width: 0;
  width: 100%;
}

/* stylelint-disable selector-max-type */

.jp-FormGroup-content fieldset .jp-inputFieldWrapper input,
.jp-FormGroup-content fieldset .jp-inputFieldWrapper select,
.jp-FormGroup-content fieldset .jp-inputFieldWrapper textarea {
  font-size: var(--jp-content-font-size2);
  border-color: var(--jp-input-border-color);
  border-style: solid;
  border-radius: var(--jp-border-radius);
  border-width: 1px;
  padding: 6px 8px;
  background: none;
  color: var(--jp-ui-font-color0);
  height: inherit;
}

.jp-FormGroup-content fieldset input[type='checkbox'] {
  position: relative;
  top: 2px;
  margin-left: 0;
}

.jp-FormGroup-content button.jp-mod-styled {
  cursor: pointer;
}

.jp-FormGroup-content .checkbox label {
  cursor: pointer;
  font-size: var(--jp-content-font-size1);
}

.jp-FormGroup-content .jp-root > fieldset > legend {
  display: none;
}

.jp-FormGroup-content .jp-root > fieldset > p {
  display: none;
}

/** copy of `input.jp-mod-styled:focus` style */
.jp-FormGroup-content fieldset input:focus,
.jp-FormGroup-content fieldset select:focus {
  -moz-outline-radius: unset;
  outline: var(--jp-border-width) solid var(--md-blue-500);
  outline-offset: -1px;
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-FormGroup-content fieldset input:hover:not(:focus),
.jp-FormGroup-content fieldset select:hover:not(:focus) {
  background-color: var(--jp-border-color2);
}

/* stylelint-enable selector-max-type */

.jp-FormGroup-content .checkbox .field-description {
  /* Disable default description field for checkbox:
   because other widgets do not have description fields,
   we add descriptions to each widget on the field level.
  */
  display: none;
}

.jp-FormGroup-content #root__description {
  display: none;
}

.jp-FormGroup-content .jp-modifiedIndicator {
  width: 5px;
  background-color: var(--jp-brand-color2);
  margin-top: 0;
  margin-left: calc(var(--jp-private-settingeditor-modifier-indent) * -1);
  flex-shrink: 0;
}

.jp-FormGroup-content .jp-modifiedIndicator.jp-errorIndicator {
  background-color: var(--jp-error-color0);
  margin-right: 0.5em;
}

/* RJSF ARRAY style */

.jp-arrayFieldWrapper legend {
  font-size: var(--jp-content-font-size2);
  color: var(--jp-ui-font-color0);
  flex-basis: 100%;
  padding: 4px 0;
  font-weight: var(--jp-content-heading-font-weight);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-arrayFieldWrapper .field-description {
  padding: 4px 0;
  white-space: pre-wrap;
}

.jp-arrayFieldWrapper .array-item {
  width: 100%;
  border: 1px solid var(--jp-border-color2);
  border-radius: 4px;
  margin: 4px;
}

.jp-ArrayOperations {
  display: flex;
  margin-left: 8px;
}

.jp-ArrayOperationsButton {
  margin: 2px;
}

.jp-ArrayOperationsButton .jp-icon3[fill] {
  fill: var(--jp-ui-font-color0);
}

button.jp-ArrayOperationsButton.jp-mod-styled:disabled {
  cursor: not-allowed;
  opacity: 0.5;
}

/* RJSF form validation error */

.jp-FormGroup-content .validationErrors {
  color: var(--jp-error-color0);
}

/* Hide panel level error as duplicated the field level error */
.jp-FormGroup-content .panel.errors {
  display: none;
}

/* RJSF normal content (settings-editor) */

.jp-FormGroup-contentNormal {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.jp-FormGroup-contentNormal .jp-FormGroup-contentItem {
  margin-left: 7px;
  color: var(--jp-ui-font-color0);
}

.jp-FormGroup-contentNormal .jp-FormGroup-description {
  flex-basis: 100%;
  padding: 4px 7px;
}

.jp-FormGroup-contentNormal .jp-FormGroup-default {
  flex-basis: 100%;
  padding: 4px 7px;
}

.jp-FormGroup-contentNormal .jp-FormGroup-fieldLabel {
  font-size: var(--jp-content-font-size1);
  font-weight: normal;
  min-width: 120px;
}

.jp-FormGroup-contentNormal fieldset:not(:first-child) {
  margin-left: 7px;
}

.jp-FormGroup-contentNormal .field-array-of-string .array-item {
  /* Display `jp-ArrayOperations` buttons side-by-side with content except
    for small screens where flex-wrap will place them one below the other.
  */
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.jp-FormGroup-contentNormal .jp-objectFieldWrapper .form-group {
  padding: 2px 8px 2px var(--jp-private-settingeditor-modifier-indent);
  margin-top: 2px;
}

/* RJSF compact content (metadata-form) */

.jp-FormGroup-content.jp-FormGroup-contentCompact {
  width: 100%;
}

.jp-FormGroup-contentCompact .form-group {
  display: flex;
  padding: 0.5em 0.2em 0.5em 0;
}

.jp-FormGroup-contentCompact
  .jp-FormGroup-compactTitle
  .jp-FormGroup-description {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color2);
}

.jp-FormGroup-contentCompact .jp-FormGroup-fieldLabel {
  padding-bottom: 0.3em;
}

.jp-FormGroup-contentCompact .jp-inputFieldWrapper .form-control {
  width: 100%;
  box-sizing: border-box;
}

.jp-FormGroup-contentCompact .jp-arrayFieldWrapper .jp-FormGroup-compactTitle {
  padding-bottom: 7px;
}

.jp-FormGroup-contentCompact
  .jp-objectFieldWrapper
  .jp-objectFieldWrapper
  .form-group {
  padding: 2px 8px 2px var(--jp-private-settingeditor-modifier-indent);
  margin-top: 2px;
}

.jp-FormGroup-contentCompact ul.error-detail {
  margin-block-start: 0.5em;
  margin-block-end: 0.5em;
  padding-inline-start: 1em;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-SidePanel {
  display: flex;
  flex-direction: column;
  min-width: var(--jp-sidebar-min-width);
  overflow-y: auto;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size1);
}

.jp-SidePanel-header {
  flex: 0 0 auto;
  display: flex;
  border-bottom: var(--jp-border-width) solid var(--jp-border-color2);
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin: 0;
  padding: 2px;
  text-transform: uppercase;
}

.jp-SidePanel-toolbar {
  flex: 0 0 auto;
}

.jp-SidePanel-content {
  flex: 1 1 auto;
}

.jp-SidePanel-toolbar,
.jp-AccordionPanel-toolbar {
  height: var(--jp-private-toolbar-height);
}

.jp-SidePanel-toolbar.jp-Toolbar-micro {
  display: none;
}

.lm-AccordionPanel .jp-AccordionPanel-title {
  box-sizing: border-box;
  line-height: 25px;
  margin: 0;
  display: flex;
  align-items: center;
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  font-size: var(--jp-ui-font-size0);
}

.jp-AccordionPanel-title {
  cursor: pointer;
  user-select: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  text-transform: uppercase;
}

.lm-AccordionPanel[data-orientation='horizontal'] > .jp-AccordionPanel-title {
  /* Title is rotated for horizontal accordion panel using CSS */
  display: block;
  transform-origin: top left;
  transform: rotate(-90deg) translate(-100%);
}

.jp-AccordionPanel-title .lm-AccordionPanel-titleLabel {
  user-select: none;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}

.jp-AccordionPanel-title .lm-AccordionPanel-titleCollapser {
  transform: rotate(-90deg);
  margin: auto 0;
  height: 16px;
}

.jp-AccordionPanel-title.lm-mod-expanded .lm-AccordionPanel-titleCollapser {
  transform: rotate(0deg);
}

.lm-AccordionPanel .jp-AccordionPanel-toolbar {
  background: none;
  box-shadow: none;
  border: none;
  margin-left: auto;
}

.lm-AccordionPanel .lm-SplitPanel-handle:hover {
  background: var(--jp-layout-color3);
}

.jp-text-truncated {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent::before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent::after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input[type='checkbox'].jp-mod-styled {
  appearance: checkbox;
  -webkit-appearance: checkbox;
  -moz-appearance: checkbox;
  height: auto;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper:not(.multiple) {
  height: 28px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

select.jp-mod-styled:not([multiple]) {
  height: 32px;
}

select.jp-mod-styled[multiple] {
  max-height: 200px;
  overflow-y: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
  font-family: var(--jp-ui-font-family);
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-switch-color, var(--jp-border-color1));
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-switch-true-position-color, var(--jp-warn-color0));
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 8;
  overflow-x: hidden;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0;
  margin: 0;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0 6px;
  margin: 0;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent > span {
  padding: 0;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
  font-family: var(--jp-ui-font-family);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-WindowedPanel-outer {
  position: relative;
  overflow-y: auto;
}

.jp-WindowedPanel-inner {
  position: relative;
}

.jp-WindowedPanel-window {
  position: absolute;
  left: 0;
  right: 0;
  overflow: visible;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

body {
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
}

/* Disable native link decoration styles everywhere outside of dialog boxes */
a {
  text-decoration: unset;
  color: unset;
}

a:hover {
  text-decoration: unset;
  color: unset;
}

/* Accessibility for links inside dialog box text */
.jp-Dialog-content a {
  text-decoration: revert;
  color: var(--jp-content-link-color);
}

.jp-Dialog-content a:hover {
  text-decoration: revert;
}

/* Styles for ui-components */
.jp-Button {
  color: var(--jp-ui-font-color2);
  border-radius: var(--jp-border-radius);
  padding: 0 12px;
  font-size: var(--jp-ui-font-size1);

  /* Copy from blueprint 3 */
  display: inline-flex;
  flex-direction: row;
  border: none;
  cursor: pointer;
  align-items: center;
  justify-content: center;
  text-align: left;
  vertical-align: middle;
  min-height: 30px;
  min-width: 30px;
}

.jp-Button:disabled {
  cursor: not-allowed;
}

.jp-Button:empty {
  padding: 0 !important;
}

.jp-Button.jp-mod-small {
  min-height: 24px;
  min-width: 24px;
  font-size: 12px;
  padding: 0 7px;
}

/* Use our own theme for hover styles */
.jp-Button.jp-mod-minimal:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Button.jp-mod-minimal {
  background: none;
}

.jp-InputGroup {
  display: block;
  position: relative;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border: none;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
  padding-bottom: 0;
  padding-top: 0;
  padding-left: 10px;
  padding-right: 28px;
  position: relative;
  width: 100%;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  font-size: 14px;
  font-weight: 400;
  height: 30px;
  line-height: 30px;
  outline: none;
  vertical-align: middle;
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input:disabled {
  cursor: not-allowed;
  resize: block;
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color2);
}

.jp-InputGroup input:disabled ~ span {
  cursor: not-allowed;
  color: var(--jp-ui-font-color2);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color2);
}

.jp-InputGroupAction {
  position: absolute;
  bottom: 1px;
  right: 0;
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

.jp-HTMLSelect.jp-DefaultStyle select:disabled {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color2);
  cursor: not-allowed;
  resize: block;
}

.jp-HTMLSelect.jp-DefaultStyle select:disabled ~ span {
  cursor: not-allowed;
}

/* Use our own theme for hover and option styles */
/* stylelint-disable-next-line selector-max-type */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}

select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-StatusBar-Widget {
  display: flex;
  align-items: center;
  background: var(--jp-layout-color2);
  min-height: var(--jp-statusbar-height);
  justify-content: space-between;
  padding: 0 10px;
}

.jp-StatusBar-Left {
  display: flex;
  align-items: center;
  flex-direction: row;
}

.jp-StatusBar-Middle {
  display: flex;
  align-items: center;
}

.jp-StatusBar-Right {
  display: flex;
  align-items: center;
  flex-direction: row-reverse;
}

.jp-StatusBar-Item {
  max-height: var(--jp-statusbar-height);
  margin: 0 2px;
  height: var(--jp-statusbar-height);
  white-space: nowrap;
  text-overflow: ellipsis;
  color: var(--jp-ui-font-color1);
  padding: 0 6px;
}

.jp-mod-highlighted:hover {
  background-color: var(--jp-layout-color3);
}

.jp-mod-clicked {
  background-color: var(--jp-brand-color1);
}

.jp-mod-clicked:hover {
  background-color: var(--jp-brand-color0);
}

.jp-mod-clicked .jp-StatusBar-TextItem {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-StatusBar-HoverItem {
  box-shadow: '0px 4px 4px rgba(0, 0, 0, 0.25)';
}

.jp-StatusBar-TextItem {
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  line-height: 24px;
  color: var(--jp-ui-font-color1);
}

.jp-StatusBar-GroupItem {
  display: flex;
  align-items: center;
  flex-direction: row;
}

.jp-Statusbar-ProgressCircle svg {
  display: block;
  margin: 0 auto;
  width: 16px;
  height: 24px;
  align-self: normal;
}

.jp-Statusbar-ProgressCircle path {
  fill: var(--jp-inverse-layout-color3);
}

.jp-Statusbar-ProgressBar-progress-bar {
  height: 10px;
  width: 100px;
  border: solid 0.25px var(--jp-brand-color2);
  border-radius: 3px;
  overflow: hidden;
  align-self: center;
}

.jp-Statusbar-ProgressBar-progress-bar > div {
  background-color: var(--jp-brand-color2);
  background-image: linear-gradient(
    -45deg,
    rgba(255, 255, 255, 0.2) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.2) 50%,
    rgba(255, 255, 255, 0.2) 75%,
    transparent 75%,
    transparent
  );
  background-size: 40px 40px;
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 14px;
  color: #fff;
  text-align: center;
  animation: jp-Statusbar-ExecutionTime-progress-bar 2s linear infinite;
}

.jp-Statusbar-ProgressBar-progress-bar p {
  color: var(--jp-ui-font-color1);
  font-family: var(--jp-ui-font-family);
  font-size: var(--jp-ui-font-size1);
  line-height: 10px;
  width: 100px;
}

@keyframes jp-Statusbar-ExecutionTime-progress-bar {
  0% {
    background-position: 0 0;
  }

  100% {
    background-position: 40px 40px;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);

  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-SearchIconGroup {
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  padding: 5px 5px 1px;
}

.jp-SearchIconGroup svg {
  height: 20px;
  width: 20px;
}

.jp-SearchIconGroup .jp-icon3[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color2);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item.lm-mod-active {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active .jp-icon-selectable[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.6;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty::after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0;
  left: 0;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px 24px 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);

  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-content.jp-Dialog-content-small {
  max-width: 500px;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-accept:focus,
button.jp-Dialog-button.jp-mod-styled.jp-mod-warn:focus,
button.jp-Dialog-button.jp-mod-styled.jp-mod-reject:focus {
  outline-offset: 4px;
  -moz-outline-radius: 0;
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-accept:focus {
  outline: 1px solid var(--jp-accept-color-normal, var(--jp-brand-color1));
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-warn:focus {
  outline: 1px solid var(--jp-warn-color-normal, var(--jp-error-color1));
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-reject:focus {
  outline: 1px solid var(--jp-reject-color-normal, var(--md-grey-600));
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color1);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-checkbox {
  padding-right: 5px;
}

.jp-Dialog-checkbox > input:focus-visible {
  outline: 1px solid var(--jp-input-active-border-color);
  outline-offset: 1px;
}

.jp-Dialog-spacer {
  flex: 1 1 auto;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-Input-Boolean-Dialog {
  flex-direction: row-reverse;
  align-items: end;
  width: 100%;
}

.jp-Input-Boolean-Dialog > label {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

.jp-MainAreaWidget .jp-MainAreaWidget-error {
  padding: 6px;
}

.jp-MainAreaWidget .jp-MainAreaWidget-error > pre {
  width: auto;
  padding: 10px;
  background: var(--jp-error-color3);
  border: var(--jp-border-width) solid var(--jp-error-color1);
  border-radius: var(--jp-border-radius);
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  white-space: pre-wrap;
  word-wrap: break-word;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;
  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;
  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #a0f;
  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;
  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;
  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;
  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;
  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;
  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;
  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;
  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;
  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;
  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ff0;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;
  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;
  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;
  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;
  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;
  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;
  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0;
  padding: 0;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}

.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}

.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}

.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}

.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}

.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}

.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}

.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}

.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}

.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}

.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}

.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}

.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}

.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}

.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}

.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}

.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);

  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

/* stylelint-disable selector-max-type, selector-max-compound-selectors */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0;
}

/* stylelint-enable selector-max-type, selector-max-compound-selectors */

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  table-layout: fixed;
  margin-left: auto;
  margin-bottom: 1em;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}

[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}

.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}

.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}

.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}

.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}

.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}

.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}

.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}

.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: var(--jp-ui-font-size0);
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-cursor-backdrop {
  position: fixed;
  width: 200px;
  height: 200px;
  margin-top: -100px;
  margin-left: -100px;
  will-change: transform;
  z-index: 100;
}

.lm-mod-drag-image {
  will-change: transform;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-lineFormSearch {
  padding: 4px 12px;
  background-color: var(--jp-layout-color2);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
  font-size: var(--jp-ui-font-size1);
}

.jp-lineFormCaption {
  font-size: var(--jp-ui-font-size0);
  line-height: var(--jp-ui-font-size1);
  margin-top: 4px;
  color: var(--jp-ui-font-color0);
}

.jp-baseLineForm {
  border: none;
  border-radius: 0;
  position: absolute;
  background-size: 16px;
  background-repeat: no-repeat;
  background-position: center;
  outline: none;
}

.jp-lineFormButtonContainer {
  top: 4px;
  right: 8px;
  height: 24px;
  padding: 0 12px;
  width: 12px;
}

.jp-lineFormButtonIcon {
  top: 0;
  right: 0;
  background-color: var(--jp-brand-color1);
  height: 100%;
  width: 100%;
  box-sizing: border-box;
  padding: 4px 6px;
}

.jp-lineFormButton {
  top: 0;
  right: 0;
  background-color: transparent;
  height: 100%;
  width: 100%;
  box-sizing: border-box;
}

.jp-lineFormWrapper {
  overflow: hidden;
  padding: 0 8px;
  border: 1px solid var(--jp-border-color0);
  background-color: var(--jp-input-active-background);
  height: 22px;
}

.jp-lineFormWrapperFocusWithin {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-lineFormInput {
  background: transparent;
  width: 200px;
  height: 100%;
  border: none;
  outline: none;
  color: var(--jp-ui-font-color0);
  line-height: 28px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/
.jp-DocumentSearch-input {
  border: none;
  outline: none;
  color: var(--jp-ui-font-color0);
  font-size: var(--jp-ui-font-size1);
  background-color: var(--jp-layout-color0);
  font-family: var(--jp-ui-font-family);
  padding: 2px 1px;
  resize: none;
}

.jp-DocumentSearch-overlay {
  position: absolute;
  background-color: var(--jp-toolbar-background);
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  border-left: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  top: 0;
  right: 0;
  z-index: 7;
  min-width: 405px;
  padding: 2px;
  font-size: var(--jp-ui-font-size1);

  --jp-private-document-search-button-height: 20px;
}

.jp-DocumentSearch-overlay button {
  background-color: var(--jp-toolbar-background);
  outline: 0;
}

.jp-DocumentSearch-overlay button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-overlay button:active {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-overlay-row {
  display: flex;
  align-items: center;
  margin-bottom: 2px;
}

.jp-DocumentSearch-button-content {
  display: inline-block;
  cursor: pointer;
  box-sizing: border-box;
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-button-content svg {
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-input-wrapper {
  border: var(--jp-border-width) solid var(--jp-border-color0);
  display: flex;
  background-color: var(--jp-layout-color0);
  margin: 2px;
}

.jp-DocumentSearch-input-wrapper:focus-within {
  border-color: var(--jp-cell-editor-active-border-color);
}

.jp-DocumentSearch-toggle-wrapper,
.jp-DocumentSearch-button-wrapper {
  all: initial;
  overflow: hidden;
  display: inline-block;
  border: none;
  box-sizing: border-box;
}

.jp-DocumentSearch-toggle-wrapper {
  width: 14px;
  height: 14px;
}

.jp-DocumentSearch-button-wrapper {
  width: var(--jp-private-document-search-button-height);
  height: var(--jp-private-document-search-button-height);
}

.jp-DocumentSearch-toggle-wrapper:focus,
.jp-DocumentSearch-button-wrapper:focus {
  outline: var(--jp-border-width) solid
    var(--jp-cell-editor-active-border-color);
  outline-offset: -1px;
}

.jp-DocumentSearch-toggle-wrapper,
.jp-DocumentSearch-button-wrapper,
.jp-DocumentSearch-button-content:focus {
  outline: none;
}

.jp-DocumentSearch-toggle-placeholder {
  width: 5px;
}

.jp-DocumentSearch-input-button::before {
  display: block;
  padding-top: 100%;
}

.jp-DocumentSearch-input-button-off {
  opacity: var(--jp-search-toggle-off-opacity);
}

.jp-DocumentSearch-input-button-off:hover {
  opacity: var(--jp-search-toggle-hover-opacity);
}

.jp-DocumentSearch-input-button-on {
  opacity: var(--jp-search-toggle-on-opacity);
}

.jp-DocumentSearch-index-counter {
  padding-left: 10px;
  padding-right: 10px;
  user-select: none;
  min-width: 35px;
  display: inline-block;
}

.jp-DocumentSearch-up-down-wrapper {
  display: inline-block;
  padding-right: 2px;
  margin-left: auto;
  white-space: nowrap;
}

.jp-DocumentSearch-spacer {
  margin-left: auto;
}

.jp-DocumentSearch-up-down-wrapper button {
  outline: 0;
  border: none;
  width: var(--jp-private-document-search-button-height);
  height: var(--jp-private-document-search-button-height);
  vertical-align: middle;
  margin: 1px 5px 2px;
}

.jp-DocumentSearch-up-down-button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-up-down-button:active {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-filter-button {
  border-radius: var(--jp-border-radius);
}

.jp-DocumentSearch-filter-button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-filter-button-enabled {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-filter-button-enabled:hover {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-search-options {
  padding: 0 8px;
  margin-left: 3px;
  width: 100%;
  display: grid;
  justify-content: start;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  justify-items: stretch;
}

.jp-DocumentSearch-search-filter-disabled {
  color: var(--jp-ui-font-color2);
}

.jp-DocumentSearch-search-filter {
  display: flex;
  align-items: center;
  user-select: none;
}

.jp-DocumentSearch-regex-error {
  color: var(--jp-error-color0);
}

.jp-DocumentSearch-replace-button-wrapper {
  overflow: hidden;
  display: inline-block;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color0);
  margin: auto 2px;
  padding: 1px 4px;
  height: calc(var(--jp-private-document-search-button-height) + 2px);
}

.jp-DocumentSearch-replace-button-wrapper:focus {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
}

.jp-DocumentSearch-replace-button {
  display: inline-block;
  text-align: center;
  cursor: pointer;
  box-sizing: border-box;
  color: var(--jp-ui-font-color1);

  /* height - 2 * (padding of wrapper) */
  line-height: calc(var(--jp-private-document-search-button-height) - 2px);
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-replace-button:focus {
  outline: none;
}

.jp-DocumentSearch-replace-wrapper-class {
  margin-left: 14px;
  display: flex;
}

.jp-DocumentSearch-replace-toggle {
  border: none;
  background-color: var(--jp-toolbar-background);
  border-radius: var(--jp-border-radius);
}

.jp-DocumentSearch-replace-toggle:hover {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.cm-editor {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;

  /* Changed to auto to autogrow */
}

.cm-editor pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .cm-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

.jp-CodeMirrorEditor {
  cursor: text;
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .cm-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .cm-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.cm-editor.jp-mod-readOnly .cm-cursor {
  display: none;
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.cm-searching,
.cm-searching span {
  /* `.cm-searching span`: we need to override syntax highlighting */
  background-color: var(--jp-search-unselected-match-background-color);
  color: var(--jp-search-unselected-match-color);
}

.cm-searching::selection,
.cm-searching span::selection {
  background-color: var(--jp-search-unselected-match-background-color);
  color: var(--jp-search-unselected-match-color);
}

.jp-current-match > .cm-searching,
.jp-current-match > .cm-searching span,
.cm-searching > .jp-current-match,
.cm-searching > .jp-current-match span {
  background-color: var(--jp-search-selected-match-background-color);
  color: var(--jp-search-selected-match-color);
}

.jp-current-match > .cm-searching::selection,
.cm-searching > .jp-current-match::selection,
.jp-current-match > .cm-searching span::selection {
  background-color: var(--jp-search-selected-match-background-color);
  color: var(--jp-search-selected-match-color);
}

.cm-trailingspace {
  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAgAAAAFCAYAAAB4ka1VAAAAsElEQVQIHQGlAFr/AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA7+r3zKmT0/+pk9P/7+r3zAAAAAAAAAAABAAAAAAAAAAA6OPzM+/q9wAAAAAA6OPzMwAAAAAAAAAAAgAAAAAAAAAAGR8NiRQaCgAZIA0AGR8NiQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQyoYJ/SY80UAAAAASUVORK5CYII=);
  background-position: center left;
  background-repeat: repeat-x;
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/* Styles for shared cursors (remote cursor locations and selected ranges) */
.jp-CodeMirrorEditor .cm-ySelectionCaret {
  position: relative;
  border-left: 1px solid black;
  margin-left: -1px;
  margin-right: -1px;
  box-sizing: border-box;
}

.jp-CodeMirrorEditor .cm-ySelectionCaret > .cm-ySelectionInfo {
  white-space: nowrap;
  position: absolute;
  top: -1.15em;
  padding-bottom: 0.05em;
  left: -1px;
  font-size: 0.95em;
  font-family: var(--jp-ui-font-family);
  font-weight: bold;
  line-height: normal;
  user-select: none;
  color: white;
  padding-left: 2px;
  padding-right: 2px;
  z-index: 101;
  transition: opacity 0.3s ease-in-out;
}

.jp-CodeMirrorEditor .cm-ySelectionInfo {
  transition-delay: 0.7s;
  opacity: 0;
}

.jp-CodeMirrorEditor .cm-ySelectionCaret:hover > .cm-ySelectionInfo {
  opacity: 1;
  transition-delay: 0s;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser .jp-SidePanel-content {
  display: flex;
  flex-direction: column;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  flex-wrap: wrap;
  row-gap: 12px;
  border-bottom: none;
  height: auto;
  margin: 8px 12px 0;
  box-shadow: none;
  padding: 0;
  justify-content: flex-start;
}

.jp-FileBrowser-Panel {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0 2px;
  padding: 0 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0;
  padding-right: 2px;
  align-items: center;
  height: unset;
}

.jp-FileBrowser-toolbar > .jp-Toolbar-item .jp-ToolbarButtonComponent {
  width: 40px;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: var(--jp-error-color1);
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileSize-hidden {
  display: none;
}

.jp-FileBrowser .lm-AccordionPanel > h3:first-child {
  display: none;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-DirListing-headerItem.jp-id-filesize {
  flex: 0 0 75px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.jp-DirListing-content .jp-DirListing-item.jp-mod-selected mark {
  color: var(--jp-ui-inverse-font-color0);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-checkboxWrapper {
  /* Increases hit area of checkbox. */
  padding: 4px;
}

.jp-DirListing-header
  .jp-DirListing-checkboxWrapper
  + .jp-DirListing-headerItem {
  padding-left: 4px;
}

.jp-DirListing-content .jp-DirListing-checkboxWrapper {
  position: relative;
  left: -4px;
  margin: -4px 0 -4px -8px;
}

.jp-DirListing-checkboxWrapper.jp-mod-visible {
  visibility: visible;
}

/* For devices that support hovering, hide checkboxes until hovered, selected...
*/
@media (hover: hover) {
  .jp-DirListing-checkboxWrapper {
    visibility: hidden;
  }

  .jp-DirListing-item:hover .jp-DirListing-checkboxWrapper,
  .jp-DirListing-item.jp-mod-selected .jp-DirListing-checkboxWrapper {
    visibility: visible;
  }
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemText:focus {
  outline-width: 2px;
  outline-color: var(--jp-inverse-layout-color1);
  outline-style: solid;
  outline-offset: 1px;
}

.jp-DirListing-item.jp-mod-selected .jp-DirListing-itemText:focus {
  outline-color: var(--jp-layout-color1);
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-itemFileSize {
  flex: 0 0 90px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon::before {
  color: var(--jp-success-color1);
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.jp-mod-running.jp-mod-selected
  .jp-DirListing-itemIcon::before {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: table;
  table-layout: fixed;
  width: 100%;
  overflow: hidden;
}

.jp-OutputPrompt {
  width: var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);

  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-OutputArea-prompt {
  display: table-cell;
  vertical-align: top;
}

.jp-OutputArea-output {
  display: table-cell;
  width: 100%;
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea .jp-RenderedText {
  padding-left: 1ch;
}

/**
 * Prompt overlay.
 */

.jp-OutputArea-promptOverlay {
  position: absolute;
  top: 0;
  width: var(--jp-cell-prompt-width);
  height: 100%;
  opacity: 0.5;
}

.jp-OutputArea-promptOverlay:hover {
  background: var(--jp-layout-color2);
  box-shadow: inset 0 0 1px var(--jp-inverse-layout-color0);
  cursor: zoom-out;
}

.jp-mod-outputsScrolled .jp-OutputArea-promptOverlay:hover {
  cursor: zoom-in;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `lm-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0;
  padding: 0;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

.jp-TrimmedOutputs pre {
  background: var(--jp-layout-color3);
  font-size: calc(var(--jp-code-font-size) * 1.4);
  text-align: center;
  text-transform: uppercase;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/* Hide empty lines in the output area, for instance due to cleared widgets */
.jp-OutputArea-prompt:empty {
  padding: 0;
  border: 0;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0;
  width: 100%;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;

  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;

  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0 0.25em;
  margin: 0 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input::placeholder {
  opacity: 0;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

.jp-Stdin-input:focus::placeholder {
  opacity: 1;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

@media print {
  .jp-OutputArea-child {
    break-inside: avoid-page;
  }
}

/*-----------------------------------------------------------------------------
| Mobile
|----------------------------------------------------------------------------*/
@media only screen and (max-width: 760px) {
  .jp-OutputPrompt {
    display: table-row;
    text-align: left;
  }

  .jp-OutputArea-child .jp-OutputArea-output {
    display: table-row;
    margin-left: var(--jp-notebook-padding);
  }
}

/* Trimmed outputs warning */
.jp-TrimmedOutputs > a {
  margin: 10px;
  text-decoration: none;
  cursor: pointer;
}

.jp-TrimmedOutputs > a:hover {
  text-decoration: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Table of Contents
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toc-active-width: 4px;
}

.jp-TableOfContents {
  display: flex;
  flex-direction: column;
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  height: 100%;
}

.jp-TableOfContents-placeholder {
  text-align: center;
}

.jp-TableOfContents-placeholderContent {
  color: var(--jp-content-font-color2);
  padding: 8px;
}

.jp-TableOfContents-placeholderContent > h3 {
  margin-bottom: var(--jp-content-heading-margin-bottom);
}

.jp-TableOfContents .jp-SidePanel-content {
  overflow-y: auto;
}

.jp-TableOfContents-tree {
  margin: 4px;
}

.jp-TableOfContents ol {
  list-style-type: none;
}

/* stylelint-disable-next-line selector-max-type */
.jp-TableOfContents li > ol {
  /* Align left border with triangle icon center */
  padding-left: 11px;
}

.jp-TableOfContents-content {
  /* left margin for the active heading indicator */
  margin: 0 0 0 var(--jp-private-toc-active-width);
  padding: 0;
  background-color: var(--jp-layout-color1);
}

.jp-tocItem {
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-tocItem-heading {
  display: flex;
  cursor: pointer;
}

.jp-tocItem-heading:hover {
  background-color: var(--jp-layout-color2);
}

.jp-tocItem-content {
  display: block;
  padding: 4px 0;
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow-x: hidden;
}

.jp-tocItem-collapser {
  height: 20px;
  margin: 2px 2px 0;
  padding: 0;
  background: none;
  border: none;
  cursor: pointer;
}

.jp-tocItem-collapser:hover {
  background-color: var(--jp-layout-color3);
}

/* Active heading indicator */

.jp-tocItem-heading::before {
  content: ' ';
  background: transparent;
  width: var(--jp-private-toc-active-width);
  height: 24px;
  position: absolute;
  left: 0;
  border-radius: var(--jp-border-radius);
}

.jp-tocItem-heading.jp-tocItem-active::before {
  background-color: var(--jp-brand-color1);
}

.jp-tocItem-heading:hover.jp-tocItem-active::before {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0;
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;

  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0;
  bottom: 0;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

/*
Hiding collapsers in print mode.

Note: input and output wrappers have "display: block" propery in print mode.
*/

@media print {
  .jp-Collapser {
    display: none;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0;
  width: 100%;
  padding: 0;
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: table;
  table-layout: fixed;
  width: 100%;
  overflow: hidden;
}

.jp-InputArea-editor {
  display: table-cell;
  overflow: hidden;
  vertical-align: top;

  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  display: table-cell;
  vertical-align: top;
  width: var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;

  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/*-----------------------------------------------------------------------------
| Mobile
|----------------------------------------------------------------------------*/
@media only screen and (max-width: 760px) {
  .jp-InputArea-editor {
    display: table-row;
    margin-left: var(--jp-notebook-padding);
  }

  .jp-InputPrompt {
    display: table-row;
    text-align: left;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: table;
  table-layout: fixed;
  width: 100%;
}

.jp-Placeholder-prompt {
  display: table-cell;
  box-sizing: border-box;
}

.jp-Placeholder-content {
  display: table-cell;
  padding: 4px 6px;
  border: 1px solid transparent;
  border-radius: 0;
  background: none;
  box-sizing: border-box;
  cursor: pointer;
}

.jp-Placeholder-contentContainer {
  display: flex;
}

.jp-Placeholder-content:hover,
.jp-InputPlaceholder > .jp-Placeholder-content:hover {
  border-color: var(--jp-layout-color3);
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

.jp-PlaceholderText {
  white-space: nowrap;
  overflow-x: hidden;
  color: var(--jp-inverse-layout-color3);
  font-family: var(--jp-code-font-family);
}

.jp-InputPlaceholder > .jp-Placeholder-content {
  border-color: var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0;
  margin: 0;

  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 24em;
  margin-left: var(--jp-private-cell-scrolling-output-offset);
  resize: vertical;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea[style*='height'] {
  max-height: unset;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea::after {
  content: ' ';
  box-shadow: inset 0 0 6px 2px rgb(0 0 0 / 30%);
  width: 100%;
  height: 100%;
  position: sticky;
  bottom: 0;
  top: 0;
  margin-top: -50%;
  float: left;
  display: block;
  pointer-events: none;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-child {
  padding-top: 6px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  width: calc(
    var(--jp-cell-prompt-width) - var(--jp-private-cell-scrolling-output-offset)
  );
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-promptOverlay {
  left: calc(-1 * var(--jp-private-cell-scrolling-output-offset));
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  display: table-cell;
  width: 100%;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/* collapseHeadingButton (show always if hiddenCellsButton is _not_ shown) */
.jp-collapseHeadingButton {
  display: flex;
  min-height: var(--jp-cell-collapser-min-height);
  font-size: var(--jp-code-font-size);
  position: absolute;
  background-color: transparent;
  background-size: 25px;
  background-repeat: no-repeat;
  background-position-x: center;
  background-position-y: top;
  background-image: var(--jp-icon-caret-down);
  right: 0;
  top: 0;
  bottom: 0;
}

.jp-collapseHeadingButton.jp-mod-collapsed {
  background-image: var(--jp-icon-caret-right);
}

/*
 set the container font size to match that of content
 so that the nested collapse buttons have the right size
*/
.jp-MarkdownCell .jp-InputPrompt {
  font-size: var(--jp-content-font-size1);
}

/*
  Align collapseHeadingButton with cell top header
  The font sizes are identical to the ones in packages/rendermime/style/base.css
*/
.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='1'] {
  font-size: var(--jp-content-font-size5);
  background-position-y: calc(0.3 * var(--jp-content-font-size5));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='2'] {
  font-size: var(--jp-content-font-size4);
  background-position-y: calc(0.3 * var(--jp-content-font-size4));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='3'] {
  font-size: var(--jp-content-font-size3);
  background-position-y: calc(0.3 * var(--jp-content-font-size3));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='4'] {
  font-size: var(--jp-content-font-size2);
  background-position-y: calc(0.3 * var(--jp-content-font-size2));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='5'] {
  font-size: var(--jp-content-font-size1);
  background-position-y: top;
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='6'] {
  font-size: var(--jp-content-font-size0);
  background-position-y: top;
}

/* collapseHeadingButton (show only on (hover,active) if hiddenCellsButton is shown) */
.jp-Notebook.jp-mod-showHiddenCellsButton .jp-collapseHeadingButton {
  display: none;
}

.jp-Notebook.jp-mod-showHiddenCellsButton
  :is(.jp-MarkdownCell:hover, .jp-mod-active)
  .jp-collapseHeadingButton {
  display: flex;
}

/* showHiddenCellsButton (only show if jp-mod-showHiddenCellsButton is set, which
is a consequence of the showHiddenCellsButton option in Notebook Settings)*/
.jp-Notebook.jp-mod-showHiddenCellsButton .jp-showHiddenCellsButton {
  margin-left: calc(var(--jp-cell-prompt-width) + 2 * var(--jp-code-padding));
  margin-top: var(--jp-code-padding);
  border: 1px solid var(--jp-border-color2);
  background-color: var(--jp-border-color3) !important;
  color: var(--jp-content-font-color0) !important;
  display: flex;
}

.jp-Notebook.jp-mod-showHiddenCellsButton .jp-showHiddenCellsButton:hover {
  background-color: var(--jp-border-color2) !important;
}

.jp-showHiddenCellsButton {
  display: none;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

/*
Using block instead of flex to allow the use of the break-inside CSS property for
cell outputs.
*/

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-notebook-toolbar-padding: 2px 5px 2px 2px;
}

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: var(--jp-notebook-toolbar-padding);

  /* disable paint containment from lumino 2.0 default strict CSS containment */
  contain: style size !important;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

.jp-Toolbar-responsive-popup {
  position: absolute;
  height: fit-content;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: flex-end;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: var(--jp-notebook-toolbar-padding);
  z-index: 1;
  right: 0;
  top: 0;
}

.jp-Toolbar > .jp-Toolbar-responsive-opener {
  margin-left: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-Notebook-ExecutionIndicator {
  position: relative;
  display: inline-block;
  height: 100%;
  z-index: 9997;
}

.jp-Notebook-ExecutionIndicator-tooltip {
  visibility: hidden;
  height: auto;
  width: max-content;
  width: -moz-max-content;
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color1);
  text-align: justify;
  border-radius: 6px;
  padding: 0 5px;
  position: fixed;
  display: table;
}

.jp-Notebook-ExecutionIndicator-tooltip.up {
  transform: translateX(-50%) translateY(-100%) translateY(-32px);
}

.jp-Notebook-ExecutionIndicator-tooltip.down {
  transform: translateX(calc(-100% + 16px)) translateY(5px);
}

.jp-Notebook-ExecutionIndicator-tooltip.hidden {
  display: none;
}

.jp-Notebook-ExecutionIndicator:hover .jp-Notebook-ExecutionIndicator-tooltip {
  visibility: visible;
}

.jp-Notebook-ExecutionIndicator span {
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  color: var(--jp-ui-font-color1);
  line-height: 24px;
  display: block;
}

.jp-Notebook-ExecutionIndicator-progress-bar {
  display: flex;
  justify-content: center;
  height: 100%;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*
 * Execution indicator
 */
.jp-tocItem-content::after {
  content: '';

  /* Must be identical to form a circle */
  width: 12px;
  height: 12px;
  background: none;
  border: none;
  position: absolute;
  right: 0;
}

.jp-tocItem-content[data-running='0']::after {
  border-radius: 50%;
  border: var(--jp-border-width) solid var(--jp-inverse-layout-color3);
  background: none;
}

.jp-tocItem-content[data-running='1']::after {
  border-radius: 50%;
  border: var(--jp-border-width) solid var(--jp-inverse-layout-color3);
  background-color: var(--jp-inverse-layout-color3);
}

.jp-tocItem-content[data-running='0'],
.jp-tocItem-content[data-running='1'] {
  margin-right: 12px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-Notebook-footer {
  height: 27px;
  margin-left: calc(
    var(--jp-cell-prompt-width) + var(--jp-cell-collapser-width) +
      var(--jp-cell-padding)
  );
  width: calc(
    100% -
      (
        var(--jp-cell-prompt-width) + var(--jp-cell-collapser-width) +
          var(--jp-cell-padding) + var(--jp-cell-padding)
      )
  );
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  color: var(--jp-ui-font-color3);
  margin-top: 6px;
  background: none;
  cursor: pointer;
}

.jp-Notebook-footer:focus {
  border-color: var(--jp-cell-editor-active-border-color);
}

/* For devices that support hovering, hide footer until hover */
@media (hover: hover) {
  .jp-Notebook-footer {
    opacity: 0;
  }

  .jp-Notebook-footer:focus,
  .jp-Notebook-footer:hover {
    opacity: 1;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-side-by-side-output-size: 1fr;
  --jp-side-by-side-resized-cell: var(--jp-side-by-side-output-size);
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

/* stylelint-disable selector-max-class */

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-MainAreaWidget-ContainStrict .jp-Notebook * {
  contain: strict;
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* cell is dirty */
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt {
  color: var(--jp-warn-color1);
}

.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt::before {
  color: var(--jp-warn-color1);
  content: '•';
}

.jp-Notebook .jp-Cell.jp-mod-active.jp-mod-dirty .jp-Collapser {
  background: var(--jp-warn-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: block;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0 rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0 rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);

  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-ActiveCellTool {
  padding: 12px 0;
  display: flex;
}

.jp-ActiveCellTool-Content {
  flex: 1 1 auto;
}

.jp-ActiveCellTool .jp-ActiveCellTool-CellContent {
  background: var(--jp-cell-editor-background);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0;
  min-height: 29px;
}

.jp-ActiveCellTool .jp-InputPrompt {
  min-width: calc(var(--jp-cell-prompt-width) * 0.75);
}

.jp-ActiveCellTool-CellContent > pre {
  padding: 5px 4px;
  margin: 0;
  white-space: normal;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label,
.jp-NumberSetter label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0;
}

.jp-NumberSetter input {
  width: 100%;
  margin-top: 4px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Side-by-side Mode (.jp-mod-sideBySide)
|----------------------------------------------------------------------------*/
.jp-mod-sideBySide.jp-Notebook .jp-Notebook-cell {
  margin-top: 3em;
  margin-bottom: 3em;
  margin-left: 5%;
  margin-right: 5%;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell {
  display: grid;
  grid-template-columns: minmax(0, 1fr) min-content minmax(
      0,
      var(--jp-side-by-side-output-size)
    );
  grid-template-rows: auto minmax(0, 1fr) auto;
  grid-template-areas:
    'header header header'
    'input handle output'
    'footer footer footer';
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell.jp-mod-resizedCell {
  grid-template-columns: minmax(0, 1fr) min-content minmax(
      0,
      var(--jp-side-by-side-resized-cell)
    );
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellHeader {
  grid-area: header;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-Cell-inputWrapper {
  grid-area: input;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-Cell-outputWrapper {
  /* overwrite the default margin (no vertical separation needed in side by side move */
  margin-top: 0;
  grid-area: output;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellFooter {
  grid-area: footer;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellResizeHandle {
  grid-area: handle;
  user-select: none;
  display: block;
  height: 100%;
  cursor: ew-resize;
  padding: 0 var(--jp-cell-padding);
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellResizeHandle::after {
  content: '';
  display: block;
  background: var(--jp-border-color2);
  height: 100%;
  width: 5px;
}

.jp-mod-sideBySide.jp-Notebook
  .jp-CodeCell.jp-mod-resizedCell
  .jp-CellResizeHandle::after {
  background: var(--jp-border-color0);
}

.jp-CellResizeHandle {
  display: none;
}

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Cell-Placeholder {
  padding-left: 55px;
}

.jp-Cell-Placeholder-wrapper {
  background: #fff;
  border: 1px solid;
  border-color: #e5e6e9 #dfe0e4 #d0d1d5;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  margin: 10px 15px;
}

.jp-Cell-Placeholder-wrapper-inner {
  padding: 15px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body {
  background-repeat: repeat;
  background-size: 50% auto;
}

.jp-Cell-Placeholder-wrapper-body div {
  background: #f6f7f8;
  background-image: -webkit-linear-gradient(
    left,
    #f6f7f8 0%,
    #edeef1 20%,
    #f6f7f8 40%,
    #f6f7f8 100%
  );
  background-repeat: no-repeat;
  background-size: 800px 104px;
  height: 104px;
  position: absolute;
  right: 15px;
  left: 15px;
  top: 15px;
}

div.jp-Cell-Placeholder-h1 {
  top: 20px;
  height: 20px;
  left: 15px;
  width: 150px;
}

div.jp-Cell-Placeholder-h2 {
  left: 15px;
  top: 50px;
  height: 10px;
  width: 100px;
}

div.jp-Cell-Placeholder-content-1,
div.jp-Cell-Placeholder-content-2,
div.jp-Cell-Placeholder-content-3 {
  left: 15px;
  right: 15px;
  height: 10px;
}

div.jp-Cell-Placeholder-content-1 {
  top: 100px;
}

div.jp-Cell-Placeholder-content-2 {
  top: 120px;
}

div.jp-Cell-Placeholder-content-3 {
  top: 140px;
}

</style>
<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0 2px 1px -1px var(--jp-shadow-umbra-color),
    0 1px 1px 0 var(--jp-shadow-penumbra-color),
    0 1px 3px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0 3px 1px -2px var(--jp-shadow-umbra-color),
    0 2px 2px 0 var(--jp-shadow-penumbra-color),
    0 1px 5px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0 2px 4px -1px var(--jp-shadow-umbra-color),
    0 4px 5px 0 var(--jp-shadow-penumbra-color),
    0 1px 10px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0 3px 5px -1px var(--jp-shadow-umbra-color),
    0 6px 10px 0 var(--jp-shadow-penumbra-color),
    0 1px 18px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0 5px 5px -3px var(--jp-shadow-umbra-color),
    0 8px 10px 1px var(--jp-shadow-penumbra-color),
    0 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0 7px 8px -4px var(--jp-shadow-umbra-color),
    0 12px 17px 2px var(--jp-shadow-penumbra-color),
    0 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0 8px 10px -5px var(--jp-shadow-umbra-color),
    0 16px 24px 2px var(--jp-shadow-penumbra-color),
    0 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0 10px 13px -6px var(--jp-shadow-umbra-color),
    0 20px 31px 3px var(--jp-shadow-penumbra-color),
    0 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0 11px 15px -7px var(--jp-shadow-umbra-color),
    0 24px 38px 3px var(--jp-shadow-penumbra-color),
    0 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-inverse-border-color: var(--md-grey-600);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;
  --jp-ui-font-family: system-ui, -apple-system, blinkmacsystemfont, 'Segoe UI',
    helvetica, arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;
  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);
  --jp-content-link-color: var(--md-blue-900);
  --jp-content-font-family: system-ui, -apple-system, blinkmacsystemfont,
    'Segoe UI', helvetica, arial, sans-serif, 'Apple Color Emoji',
    'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: menlo, consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-900);
  --jp-brand-color1: var(--md-blue-700);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);
  --jp-accent-color0: var(--md-green-900);
  --jp-accent-color1: var(--md-green-700);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-900);
  --jp-warn-color1: var(--md-orange-700);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);
  --jp-error-color0: var(--md-red-900);
  --jp-error-color1: var(--md-red-700);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);
  --jp-success-color0: var(--md-green-900);
  --jp-success-color1: var(--md-green-700);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);
  --jp-info-color0: var(--md-cyan-900);
  --jp-info-color1: var(--md-cyan-700);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;
  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;
  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);
  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);

  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;

  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Statusbar specific styles */

  --jp-statusbar-height: 24px;

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-inverse-border-color);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: rgb(0, 54, 109);
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #a2f;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #a2f;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /*
    RTC user specific colors.
    These colors are used for the cursor, username in the editor,
    and the icon of the user.
  */

  --jp-collaborator-color1: #ffad8e;
  --jp-collaborator-color2: #dac83d;
  --jp-collaborator-color3: #72dd76;
  --jp-collaborator-color4: #00e4d0;
  --jp-collaborator-color5: #45d4ff;
  --jp-collaborator-color6: #e2b1ff;
  --jp-collaborator-color7: #ff9de6;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);

  /* Button colors */
  --jp-accept-color-normal: var(--md-blue-700);
  --jp-accept-color-hover: var(--md-blue-800);
  --jp-accept-color-active: var(--md-blue-900);
  --jp-warn-color-normal: var(--md-red-700);
  --jp-warn-color-hover: var(--md-red-800);
  --jp-warn-color-active: var(--md-red-900);
  --jp-reject-color-normal: var(--md-grey-600);
  --jp-reject-color-hover: var(--md-grey-700);
  --jp-reject-color-active: var(--md-grey-800);

  /* File or activity icons and switch semantic variables */
  --jp-jupyter-icon-color: #f37626;
  --jp-notebook-icon-color: #f37626;
  --jp-json-icon-color: var(--md-orange-700);
  --jp-console-icon-background-color: var(--md-blue-700);
  --jp-console-icon-color: white;
  --jp-terminal-icon-background-color: var(--md-grey-800);
  --jp-terminal-icon-color: var(--md-grey-200);
  --jp-text-editor-icon-color: var(--md-grey-700);
  --jp-inspector-icon-color: var(--md-grey-700);
  --jp-switch-color: var(--md-grey-400);
  --jp-switch-true-position-color: var(--md-orange-900);
}
</style>
<style type="text/css">
/* Force rendering true colors when outputing to pdf */
* {
  -webkit-print-color-adjust: exact;
}

/* Misc */
a.anchor-link {
  display: none;
}

/* Input area styling */
.jp-InputArea {
  overflow: hidden;
}

.jp-InputArea-editor {
  overflow: hidden;
}

.cm-editor.cm-s-jupyter .highlight pre {
/* weird, but --jp-code-padding defined to be 5px but 4px horizontal padding is hardcoded for pre.cm-line */
  padding: var(--jp-code-padding) 4px;
  margin: 0;

  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
  color: inherit;

}

.jp-OutputArea-output pre {
  line-height: inherit;
  font-family: inherit;
}

.jp-RenderedText pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
}

/* Hiding the collapser by default */
.jp-Collapser {
  display: none;
}

@page {
    margin: 0.5in; /* Margin for each printed piece of paper */
}

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }
}
</style>
<!-- Load mathjax -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-AMS_CHTML-full,Safe"> </script>
<!-- MathJax configuration -->
<script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: {
                    automatic: true
                    }
                }
            });

            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
<!-- End of mathjax configuration --><script type="module">
  document.addEventListener("DOMContentLoaded", async () => {
    const diagrams = document.querySelectorAll(".jp-Mermaid > pre.mermaid");
    // do not load mermaidjs if not needed
    if (!diagrams.length) {
      return;
    }
    const mermaid = (await import("https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.7.0/mermaid.esm.min.mjs")).default;
    const parser = new DOMParser();

    mermaid.initialize({
      maxTextSize: 100000,
      maxEdges: 100000,
      startOnLoad: false,
      fontFamily: window
        .getComputedStyle(document.body)
        .getPropertyValue("--jp-ui-font-family"),
      theme: document.querySelector("body[data-jp-theme-light='true']")
        ? "default"
        : "dark",
    });

    let _nextMermaidId = 0;

    function makeMermaidImage(svg) {
      const img = document.createElement("img");
      const doc = parser.parseFromString(svg, "image/svg+xml");
      const svgEl = doc.querySelector("svg");
      const { maxWidth } = svgEl?.style || {};
      const firstTitle = doc.querySelector("title");
      const firstDesc = doc.querySelector("desc");

      img.setAttribute("src", `data:image/svg+xml,${encodeURIComponent(svg)}`);
      if (maxWidth) {
        img.width = parseInt(maxWidth);
      }
      if (firstTitle) {
        img.setAttribute("alt", firstTitle.textContent);
      }
      if (firstDesc) {
        const caption = document.createElement("figcaption");
        caption.className = "sr-only";
        caption.textContent = firstDesc.textContent;
        return [img, caption];
      }
      return [img];
    }

    async function makeMermaidError(text) {
      let errorMessage = "";
      try {
        await mermaid.parse(text);
      } catch (err) {
        errorMessage = `${err}`;
      }

      const result = document.createElement("details");
      result.className = 'jp-RenderedMermaid-Details';
      const summary = document.createElement("summary");
      summary.className = 'jp-RenderedMermaid-Summary';
      const pre = document.createElement("pre");
      const code = document.createElement("code");
      code.innerText = text;
      pre.appendChild(code);
      summary.appendChild(pre);
      result.appendChild(summary);

      const warning = document.createElement("pre");
      warning.innerText = errorMessage;
      result.appendChild(warning);
      return [result];
    }

    async function renderOneMarmaid(src) {
      const id = `jp-mermaid-${_nextMermaidId++}`;
      const parent = src.parentNode;
      let raw = src.textContent.trim();
      const el = document.createElement("div");
      el.style.visibility = "hidden";
      document.body.appendChild(el);
      let results = null;
      let output = null;
      try {
        let { svg } = await mermaid.render(id, raw, el);
        svg = cleanMermaidSvg(svg);
        results = makeMermaidImage(svg);
        output = document.createElement("figure");
        results.map(output.appendChild, output);
      } catch (err) {
        parent.classList.add("jp-mod-warning");
        results = await makeMermaidError(raw);
        output = results[0];
      } finally {
        el.remove();
      }
      parent.classList.add("jp-RenderedMermaid");
      parent.appendChild(output);
    }


    /**
     * Post-process to ensure mermaid diagrams contain only valid SVG and XHTML.
     */
    function cleanMermaidSvg(svg) {
      return svg.replace(RE_VOID_ELEMENT, replaceVoidElement);
    }


    /**
     * A regular expression for all void elements, which may include attributes and
     * a slash.
     *
     * @see https://developer.mozilla.org/en-US/docs/Glossary/Void_element
     *
     * Of these, only `<br>` is generated by Mermaid in place of `\n`,
     * but _any_ "malformed" tag will break the SVG rendering entirely.
     */
    const RE_VOID_ELEMENT =
      /<\s*(area|base|br|col|embed|hr|img|input|link|meta|param|source|track|wbr)\s*([^>]*?)\s*>/gi;

    /**
     * Ensure a void element is closed with a slash, preserving any attributes.
     */
    function replaceVoidElement(match, tag, rest) {
      rest = rest.trim();
      if (!rest.endsWith('/')) {
        rest = `${rest} /`;
      }
      return `<${tag} ${rest}>`;
    }

    void Promise.all([...diagrams].map(renderOneMarmaid));
  });
</script>
<style>
  .jp-Mermaid:not(.jp-RenderedMermaid) {
    display: none;
  }

  .jp-RenderedMermaid {
    overflow: auto;
    display: flex;
  }

  .jp-RenderedMermaid.jp-mod-warning {
    width: auto;
    padding: 0.5em;
    margin-top: 0.5em;
    border: var(--jp-border-width) solid var(--jp-warn-color2);
    border-radius: var(--jp-border-radius);
    color: var(--jp-ui-font-color1);
    font-size: var(--jp-ui-font-size1);
    white-space: pre-wrap;
    word-wrap: break-word;
  }

  .jp-RenderedMermaid figure {
    margin: 0;
    overflow: auto;
    max-width: 100%;
  }

  .jp-RenderedMermaid img {
    max-width: 100%;
  }

  .jp-RenderedMermaid-Details > pre {
    margin-top: 1em;
  }

  .jp-RenderedMermaid-Summary {
    color: var(--jp-warn-color2);
  }

  .jp-RenderedMermaid:not(.jp-mod-warning) pre {
    display: none;
  }

  .jp-RenderedMermaid-Summary > pre {
    display: inline-block;
    white-space: normal;
  }
</style>
<!-- End of mermaid configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">
<main><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=20489794-7d8e-4534-a494-da40f0e5edac">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [44]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">PIL</span> <span class="kn">import</span> <span class="n">Image</span>
<span class="kn">from</span> <span class="nn">sklearn.cluster</span> <span class="kn">import</span> <span class="n">KMeans</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">os</span>
<span class="kn">from</span> <span class="nn">tqdm</span> <span class="kn">import</span> <span class="n">tqdm</span>

<span class="k">def</span> <span class="nf">get_dominant_colors</span><span class="p">(</span><span class="n">image_path</span><span class="p">,</span> <span class="n">k</span><span class="o">=</span><span class="mi">5</span><span class="p">):</span>
    <span class="n">img</span> <span class="o">=</span> <span class="n">Image</span><span class="o">.</span><span class="n">open</span><span class="p">(</span><span class="n">image_path</span><span class="p">)</span><span class="o">.</span><span class="n">convert</span><span class="p">(</span><span class="s2">"RGB"</span><span class="p">)</span><span class="o">.</span><span class="n">resize</span><span class="p">((</span><span class="mi">100</span><span class="p">,</span> <span class="mi">100</span><span class="p">))</span>
    <span class="n">pixels</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">img</span><span class="p">)</span><span class="o">.</span><span class="n">reshape</span><span class="p">(</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">)</span>
    <span class="n">kmeans</span> <span class="o">=</span> <span class="n">KMeans</span><span class="p">(</span><span class="n">n_clusters</span><span class="o">=</span><span class="n">k</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">pixels</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">kmeans</span><span class="o">.</span><span class="n">cluster_centers_</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="nb">int</span><span class="p">)</span>

<span class="n">frame_dirs</span> <span class="o">=</span> <span class="p">[</span><span class="s1">'study_me_frames'</span><span class="p">,</span> 
              <span class="s1">'cream_frames'</span><span class="p">,</span> 
              <span class="s1">'kuzuri_frames'</span><span class="p">,</span> 
              <span class="s1">'hippo_pain_frames'</span><span class="p">,</span> 
              <span class="s1">'truth_in_lies_frames'</span><span class="p">,</span> 
              <span class="s1">'mirror_tune_frames'</span><span class="p">,</span> 
              <span class="s1">'milabo_frames'</span><span class="p">,</span> 
              <span class="s1">'time_left_frames'</span><span class="p">]</span>

<span class="n">mv_colors</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">frame_dir</span> <span class="ow">in</span> <span class="n">frame_dirs</span><span class="p">:</span>
    <span class="n">all_colors</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="k">for</span> <span class="n">fname</span> <span class="ow">in</span> <span class="n">tqdm</span><span class="p">(</span><span class="nb">sorted</span><span class="p">(</span><span class="n">os</span><span class="o">.</span><span class="n">listdir</span><span class="p">(</span><span class="n">frame_dir</span><span class="p">))):</span>
        <span class="n">path</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">frame_dir</span><span class="p">,</span> <span class="n">fname</span><span class="p">)</span>
        <span class="k">try</span><span class="p">:</span>
            <span class="n">colors</span> <span class="o">=</span> <span class="n">get_dominant_colors</span><span class="p">(</span><span class="n">path</span><span class="p">,</span> <span class="n">k</span><span class="o">=</span><span class="mi">5</span><span class="p">)</span>
            <span class="n">all_colors</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span><span class="n">colors</span><span class="p">)</span>
        <span class="k">except</span><span class="p">:</span>
            <span class="k">continue</span>
    <span class="n">mv_colors</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">all_colors</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr" tabindex="0">
<pre> 94%|██████████████████████████████████████▌  | 272/289 [00:04&lt;00:00, 63.72it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (2) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|████████████████████████████████████████▊| 288/289 [00:04&lt;00:00, 67.27it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (2) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|█████████████████████████████████████████| 289/289 [00:04&lt;00:00, 64.43it/s]
 98%|███████████████████████████████████████▉ | 234/240 [00:04&lt;00:00, 51.30it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (3) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (3) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|█████████████████████████████████████████| 240/240 [00:04&lt;00:00, 57.41it/s]
 96%|███████████████████████████████████████▍ | 231/240 [00:03&lt;00:00, 60.33it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (3) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (3) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|█████████████████████████████████████████| 240/240 [00:03&lt;00:00, 62.08it/s]
 94%|██████████████████████████████████████▍  | 183/195 [00:03&lt;00:00, 56.29it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
 97%|███████████████████████████████████████▋ | 189/195 [00:03&lt;00:00, 52.41it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (2) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|█████████████████████████████████████████| 195/195 [00:03&lt;00:00, 52.11it/s]
 92%|█████████████████████████████████████▋   | 252/274 [00:04&lt;00:00, 64.92it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
 97%|███████████████████████████████████████▉ | 267/274 [00:04&lt;00:00, 60.94it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (2) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|█████████████████████████████████████████| 274/274 [00:04&lt;00:00, 60.50it/s]
  0%|                                                   | 0/254 [00:00&lt;?, ?it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
 69%|████████████████████████████▍            | 176/254 [00:03&lt;00:01, 49.67it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
 81%|█████████████████████████████████▍       | 207/254 [00:03&lt;00:00, 50.71it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|█████████████████████████████████████████| 254/254 [00:04&lt;00:00, 51.64it/s]
100%|█████████████████████████████████████████| 266/266 [00:03&lt;00:00, 70.97it/s]
  0%|                                                   | 0/234 [00:00&lt;?, ?it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
 60%|████████████████████████▌                | 140/234 [00:02&lt;00:01, 69.51it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
 87%|███████████████████████████████████▌     | 203/234 [00:03&lt;00:00, 62.56it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
 95%|███████████████████████████████████████  | 223/234 [00:03&lt;00:00, 49.08it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|████████████████████████████████████████▊| 233/234 [00:03&lt;00:00, 59.59it/s]/opt/anaconda3/lib/python3.12/site-packages/sklearn/base.py:1473: ConvergenceWarning: Number of distinct clusters (1) found smaller than n_clusters (5). Possibly due to duplicate points in X.
  return fit_method(estimator, *args, **kwargs)
100%|█████████████████████████████████████████| 234/234 [00:03&lt;00:00, 62.11it/s]
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs" id="cell-id=b9bf65c3-ad40-4fdc-88b5-eaf021c8fa35">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [98]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">reduce_palette</span><span class="p">(</span><span class="n">colors</span><span class="p">,</span> <span class="n">final_k</span><span class="o">=</span><span class="mi">12</span><span class="p">):</span>
    <span class="n">kmeans</span> <span class="o">=</span> <span class="n">KMeans</span><span class="p">(</span><span class="n">n_clusters</span><span class="o">=</span><span class="n">final_k</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">colors</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">kmeans</span><span class="o">.</span><span class="n">cluster_centers_</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="nb">int</span><span class="p">)</span>

<span class="n">final_palettes</span> <span class="o">=</span> <span class="p">[]</span>
<span class="k">for</span> <span class="n">all_colors</span> <span class="ow">in</span> <span class="n">mv_colors</span><span class="p">:</span>
    <span class="n">final_palettes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">reduce_palette</span><span class="p">(</span><span class="n">all_colors</span><span class="p">,</span> <span class="n">final_k</span><span class="o">=</span><span class="mi">10</span><span class="p">))</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=bc2856b1-8db0-4d75-9d3b-6fcb634856c4">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [99]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="k">def</span> <span class="nf">plot_palette</span><span class="p">(</span><span class="n">palette</span><span class="p">):</span>
    <span class="n">swatch_size</span> <span class="o">=</span> <span class="mi">100</span>
    <span class="n">n</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">palette</span><span class="p">)</span>
    <span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="n">n</span><span class="p">,</span> <span class="mi">2</span><span class="p">))</span>
    
    <span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">color</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">palette</span><span class="p">):</span>
        <span class="n">rgb</span> <span class="o">=</span> <span class="nb">tuple</span><span class="p">(</span><span class="nb">int</span><span class="p">(</span><span class="n">c</span><span class="p">)</span> <span class="k">for</span> <span class="n">c</span> <span class="ow">in</span> <span class="n">color</span><span class="p">)</span>
        <span class="n">hex_val</span> <span class="o">=</span> <span class="s1">'#</span><span class="si">%02x%02x%02x</span><span class="s1">'</span> <span class="o">%</span> <span class="n">rgb</span>
        <span class="n">rect</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">Rectangle</span><span class="p">((</span><span class="n">i</span><span class="p">,</span> <span class="mi">0</span><span class="p">),</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">rgb</span><span class="p">)</span><span class="o">/</span><span class="mi">255</span><span class="p">)</span>
        <span class="n">ax</span><span class="o">.</span><span class="n">add_patch</span><span class="p">(</span><span class="n">rect</span><span class="p">)</span>
        <span class="n">ax</span><span class="o">.</span><span class="n">text</span><span class="p">(</span><span class="n">i</span> <span class="o">+</span> <span class="mf">0.5</span><span class="p">,</span> <span class="o">-</span><span class="mf">0.15</span><span class="p">,</span> <span class="nb">str</span><span class="p">(</span><span class="n">hex_val</span><span class="p">),</span> <span class="n">ha</span><span class="o">=</span><span class="s1">'center'</span><span class="p">,</span> <span class="n">va</span><span class="o">=</span><span class="s1">'top'</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">9</span><span class="p">)</span>

    <span class="n">ax</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="n">n</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">'off'</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">final_palettes</span><span class="p">)):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">frame_dirs</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    <span class="n">plot_palette</span><span class="p">(</span><span class="n">final_palettes</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>study_me_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA90AAAC6CAYAAACz1y75AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAAAeOElEQVR4nO3cfXBU1f3H8W8SQkiyyW5CSAIGghAeEh6loIIiIBZBFGKnUMBQEGREZKaOpSKKD6M/qlJRFBjKk4k6tMM4ApaHolYgohKqQoWIiECgSAIYCMhDIGT3+/uDyR022d27JBw3Ke/XTP7IPffevXvOnnPu5969G6aqKgAAAAAA4JoLD/UBAAAAAADwv4rQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGNAp2xekbfyuVnksmjwUBnCv1yLrHLwhNEDpxDpdMGvMnadQoMtSHct06d84t/1xbKh5PqI/k+tW4ySXp0adIwiM01Idy3XLERcvY3w+WRo0iQn0o163i4mK5a+gguVhxMdSHct2KahwjPbsOlfBw+kGoxDmiZdxYxqKQOtVIIua1krBK7qOG0j3ft7ddJ+gWInCH1sUzQuAOsZgmsQTuEKu46CFwh1hkpJvAHWLRTaI4yQ2xk6fKCNwh1qhRFIE7xJpEMxaF3PkIAncDQSsBAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwJAwVdVQHwQAAAAAAP+LuNMNAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABD/udDd15ennTv3t1v+fPPPy/Z2dm/2PEAQG2MHz9eHnvssVAfBnBNnTp1SsLCwuTgwYOhPhQADYjd+b1p/fv3l7lz54bs9euDULeBLy6XSzZv3hzqw/Cp3oTuBx98UN59910REenYsaMUFRWJiMif//xncTgc1l9sbKyEhYXJypUrRURk3bp1cscdd0hCQoIkJyfLb3/7W/nxxx+NHOPo0aMlLCxM/vOf/xjZf6j5a4OSkhIZNmyYtGjRolbvf9OmTTJgwABxOp3icrkCrmtXx3Utbwj8tYOIyNy5c6VNmzbicDjkzjvvlH379nlt+/nnn0u3bt0kJiZGunfvLlu3brXK7PoSLvNX/9u3b5df/epXkpiYKC6XS/r06SOffvpp0Pt99dVXpWvXrhIfHy9paWkybdo0qaiosMrz8vIkIiLCq41mz54d9P47derktW1UVJTEx8cHvX19Utv54EqLFi2SsLCwGidFp06dkoceekiSkpIkPj5eevbsKefPnw/quM6ePSuTJ0+W1NRUcblc8uCDD9bYdtGiRdKqVSuJjY2VoUOHSklJSS1qIPQCjUOBXM1470swdRyM8vJyycjIqNUx1BeB2iDQWH8lf/3A9PZ2c1VDEUw/8FVHdudNdZ1PRER2794td999t8TFxUliYqJMnDjRKqtrP6xPajsWFRYWyt133y1JSUkSFhYmp06duqrXreucOn78eGncuLHXPvz1s/qutm2wefNmCQsL86qDqVOnWuVvv/223HzzzeJ0OqV58+YyceLEGu30448/yogRI8TlconL5ZK777476OOurKyUp59+Wlq2bCnx8fFy//33y/Hjx4Pe/lqrN6H7q6++kl69esnp06fl5MmTcuONN4qIyFNPPSVnz561/t555x1xOp0yZMgQERE5ffq0TJ8+XQ4fPixFRUUSHx8vI0eOvObHt379+gZ78hQsf20QHh4ugwcPltWrV9dqv7GxsTJhwgR57bXXAq5nV8d1LW8o/LXD3//+d5kzZ46sX79eysrKpE+fPnLfffeJ2+0WEZGTJ0/KvffeK1OnTpWysjJ59NFH5d5777UGMLu+hMv81X96erqsXLlSTpw4IWVlZTJt2jQZOnSolJeXB7Vft9sty5YtkxMnTkhBQYFs3rxZnn/+ea91unTp4tVGTzzx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TaZOnSqNGzeW2267TbKzs+Uf//iHiNi34RtvvCHp6enSrVs36dGjhwwbNkxE5Kr7YH0XqA3sxgk7xcXFXp/j6p9puzoONNbs379fFixYIK+++mpdqyDkArWB3ecsmH5gcnu7uaqhCNQGdnV0NWoznzgcDsnOzpbbbrtNGjduLFOnTpWoqCj54osv6nw89YndfGB3fh/Ivn37ZPjw4dKiRQuJj4+XnJwcKS0trbFeoDn1yvErMjJSmjdvbr1+jx49pFmzZhIRESG33nqrPPnkk7JixYqgjq0+qUsbpKamSufOnSUiIkJSU1Nl8eLF8s0338jevXu99rFx40bJycmRlStXSpcuXazlDodDevfuLffff79ERkZKdna29OjRw7rbXX0+SUlJ8coCM2bMkEGDBknfvn2lffv20r17d3E4HKEbi0IS9fXyc11Op1OdTqeGh4er0+lUh8OhERER6nQ69fbbb/da/+OPP9YmTZroyZMna+xr165dmpyc7PPZVV9XYR555JGAd7qHDBmiL774ohYVFWl4eLimpKRYfyKiTZs2ta5odujQwXqutaG52jZQ9X3FduLEiTp8+HA9fvy4ql6+Iis+rir6uuJqV8d1LW8IatMOqqqlpaUaHR2thYWFqnr5ObvOnTt7rdOpUyev51lU/felhx9+WKdPn+73ODt27KjvvPOOz7LrrR9UadeunTXuBNMPli9frklJSbp9+3bb4/ruu+80PDxcz549q6q+73RnZmbWuGL7wAMP6O9+97ug3nt9ca3mg/T0dE1KSrLGgsjISI2Li9MRI0aoqupbb73l9byY6uXnsP/0pz+pavBjWZX169dramqqddU+JydHp06dapUfO3aswTzTHWwb2I0TVYK9071t27aAz9hVr+NAY01ubq42adLEav+EhAQNCwvTlJQU3bZtm+0xh1qwbWA31tv1A9PbV1d9rqrPgm0Duzq6kq/zJl+uZj75/e9/r2PHjvXaPi0tTdetW+e1rCHe6Q62DezO76v4u9M9cOBAfeSRR6zlq1at8llX/uZUuzvd1S1cuFBvueWWYKog5K51G1Q5e/ashoeH63fffWct27hxoyYkJOiGDRtqrP/ss896/faNqurtt99uPTde/U73sWPHvO50V7d7926NiorSEydOBFcR11jIv16+YcMG6yuUzzzzjL700ks+1xs1apSO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"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>cream_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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WVmaOHGi383xAq2LpKa1Nm0yV+Btt93m66R+/fr53airwtKlS9WhQ4dq75BXXXHPy8vTbbfdpsTEREVHR2vIkCHKzMyU9NPnDmbPnq24uDjFxcXpjjvu8JuUK+6KGBUVpYEDB+qxxx7zC91ffvmlLr/8csXHxysuLk6XXnqp0tPTG75jfgaB+v7VV19Vt27d5PV6lZCQoPHjx+uLL77wte/evVsXXnihIiMj1bNnT61cubLWidaq+VzF+vXrFRkZWePn4l988UV16dJFUVFRGjp0qN/NMCRpxYoV6tChg7xer8aNG1ftTRSaskBjkJaWph49eigyMlJt2rTRJZdcUuVuvGZW5aviDo/Tpk2Tx+NRZGSk31flex78+OOPatmyZVB3+a3us321Hb85CKYGLVmyRF27dlVkZKQ6deqkRYsW+Rb7wYzRtm3bNHjwYHm9XvXo0cPvhiLBbF/b8c/UXD/THcw4vPPOOxo0aJCio6PVvn17392tA9WiuXPnKjExUV6vV+3bt9f111/v91cOKu4IPGnSJEVGRqpPnz41foawujlnypQpatOmjbxer7p27ar58+fXeDfbpiqY/t+0aZP69u2riIgI9evXT5988omv7cy7lyclJWnZsmV+269du1bnnXeeIiIiNGzYsCrH+PLLL+XxeKr9CxQV/X7mV+W7Fgfaf3PREPNCbTUnmPbKqqsptc0bzTl013dNKtU+JwazbqptXROoVh07dkzXXHONYmJimu3dywONQTB9WNvaMS8vTzNmzFC7du0UHR2tvn37+v3lnEDta9euVZcuXRQZGamRI0f6/hRxZffdd59GjhzZgL3y82qI66A+NWbfvn06//zz5fV6de655+qee+7xu9GyFHhd1JTWpp7/PSEAAAAAANDAms8HzgAAAAAAaGYI3QAAAAAAOELoBgAAAADAEUI3AAAAAACOELoBAAAAAHCE0A0AAAAAgCOEbgAAAAAAHCF0AwAAAADgCKEbAAAAAABHCN0AAAAAADhC6AYAAAAAwJH/B3ZdpWK+JyEIAAAAAElFTkSuQmCC"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>kuzuri_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA90AAAC6CAYAAACz1y75AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAAAceklEQVR4nO3de3AV5f3H8W9OzP2cJJBAIAQSIsr9poCDKZdysUJHQKeUAQUJkUEhLZQfaCvSmSpS7FQRKYNgFAfFqXZApFy0KFeRBAdoM1xCKw3hkiC3BEJCyO37+4Of++MkJ2cPSR6To+/XDDNkn312l+c5zz77ye5ZAlRVBQAAAAAANDpHUx8AAAAAAAA/VIRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADDkLl9X/FfWLlGtNnks8OLCxUvyVPo8qaioaOpD+dGKigiV//nlgxJ0V2BTH8qP1vWbVbLxnxekSpv6SH687goMkE7xUeIICGjqQ/nRuiskTJIeHCWOQM5FTSU8JFhG9+8lgQ7uXTSVqrISufT1JyJcmzaZaxUia08HSZUyHzSVyIAymRl2UO4KYBw0peQ5m2zX8Xm2IHA3rWvXigncTSwiNIjA3cRuVlYTuJvYXQ4HgbuJBQaHELibWEjQXQTuJlZdUUbgbmJlVQEE7iYWHlBJ4PYTzBgAAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMCRAVbWpDwIAAAAAgB8i7nQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAA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"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>hippo_pain_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA90AAAC6CAYAAACz1y75AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAAAghUlEQVR4nO3deXRU5eH/8WcSluwzWZDsaACBAAnIUrcWFFCBCtqCFqUi4JJKKx7cWb5YFbEtVNlqlSAqlqNHNkWRihAqgsHWAIrIUcpOoKwBYkImmfn8/uDk/pgsMwPhmkTfr3M4hzt3npk7z3Pv8zyfmXtvHJJkAAAAAADARRdS3xsAAAAAAMCPFaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbNAn2if987j/GWyE7twV+nDpTbF754l3j8Xrqe1N+stxlJWbblx8ZyVvfm/KTFW2amPuatzZN+L6w3oQ1NeYXbZua0BBHfW/KT9Zhj0zOkTJTXt8b8hMW2SzC3N7ll6ZJSGh9b8pPVtPoYtPh3sUmpAnzovrS5ESUaT3ldhNSEXScwEVWZJqa2Y52poJ5Ub36x4dXBHxO0C1E4K5fJRVlBO56VlFRRuCuZxGOJgTuetYs1EHgrmenvCJw17OwJs0J3PWsScQZAnc9a1IcRuCuZyWmCYG7kaCVAAAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmxC6AQAAAACwCaEbAAAAAACbELoBAAAAALAJoRsAAAAAAJsQugEAAAAAsAmhGwAAAAAAmzgkqb43AgAAAACAHyN+6QYAAAAAwCaEbgAAAAAAbELoBgAAAADAJoRuAAAAAABsQugGAAAAAMAmhG4AAAAAAGxC6AYAAAAAwCaEbgAAAAAAbELoBgAAAADAJoRuAAAAAABsQugGAAAAAMAmhG4AAAAAAGxC6AYAAAAAwCaEbgAAAAAAbELoBgAAAADA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"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>truth_in_lies_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA90AAAC6CAYAAACz1y75AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAAAa+UlEQVR4nO3de3BU9f3/8ffmQiCbZJMQuSUQGn9cioTE4aLoSCgCFVQuFVoF2nBpBwRGHMeiINgZ5GLnSwcFHQoi8QdTvrQiRYs3GExbNEAvQQoCVUoSLonDpUkg5LKb5P39w8mZLEn2bNh82I0+HzP5Y/dzPntOPp9z3p99JdkTh6qqAAAAAACANhcW7AMAAAAAAODbitANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIZE+LvhwD7DpKbGbfJY4ENCnFNefHKqREb4PWVoY+EdOkiPjExxhPGzqmApve6R//nfs1Jbp8E+lO8sj9stZ86cEVXmIFgixS39OnwpYcIcBEuEM1Z6TckWRzhrcrA43NXS6Ys8cWh9sA/lO6v8+jXZtP3/S11dXbAP5TsrMbKDvPT/Bkok702Daubnn9pu4/cMEbiDyxndkcAdZGEREQTuILtRXUfgDrLaujoCd5BFOOoI3EEW1rEjgTvIHLVuAneQVVVVE7iDLCY8gsDdTjBLAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADDEoaoa7IMAAAAAAODbiN90AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAA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"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>mirror_tune_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>milabo_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA90AAAC6CAYAAACz1y75AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAAAcxUlEQVR4nO3deXRV1f338W8IhJDc3IQQMkBowihQZpC1kAdkVCsYYxfwFOpABGWorSxKKShDlYKs1gop+AAhbSgsqFpFbbEiLgZlkGGRICJgZQqQMJOQpJmT7/MHv5xfboZ7LsMmufh+rZU/7t1nn3Oy97l77w/35OCjqioAAAAAAOCua1DXJwAAAAAAwP2K0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhjT0dMNjJw6Iqpo8F7iRmXlRRjw6WoqLiuv6VH6wnEFBMjXhWWnY0OOPDe6ygsJC2X0gVcrLy+v6VH6wggID5dkx8dKwoW9dn8oPln9AE/k/ccPE15c+qCvFRcXyn0Pfsi6qQ7m5ebJh7T+krKysrk/lByvQr4H8365h0rCBT12fyg9Wvq+/bGk5SMp9mA/q0v979qe223j8TTcTS93KzsomcNexgCb+BO46VlJSSuCuY/7+jQncdaxRYz8Cdx0rKy1lXVTHCgsKCdx1zL9hAwJ3HSvy9SNwewluLwcAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIT6qqnV9EgAAAAAA3I/4phsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAih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"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>time_left_frames
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA90AAAC6CAYAAACz1y75AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAAAeNklEQVR4nO3dfVTUZf7/8TegIswAI5oiYCSJFYnQje0pT1p5c8rWu45m3pSaWa61a6fTGq65nizLr8e2rDyW0dLm6tnWNNu0KFetTIP2BGmmVt6AN2CigoDcDMy8f3/483McuZmB4QrQ5+Mc/pi55prPZ67r+lyf6+V85mOAqqoAAAAAAIBmF9jSOwAAAAAAwKWK0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhrTz9YXLZ/2fuGpcJvcFDSg5WyZvf/y+uFz0QUvpFhgsq7v+ToID+LeqlpJfXS5DD2eIU90tvSuXLVtHm4y9Y7QEBQW19K5ctsLCw2T6jEelXTufT+FoZkWnTsviefOlpqampXflsmULtcnY4WOkHXNRiykuLZGl778tNaxNW4xdA2W8O1LaSUBL78plbUruBq+v8Tk9ELhbVnlVJYG7hUUEtidwt7AiVxWBu4V17BBM4G5hoSGhBO4WdrasjMDdwjoGdyRwt7DyynICdwvrKIEE7jaCBAEAAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwjdAAAAAAAYQugGAAAAAMAQQjcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdAMAAAAAYAihGwAAAAAAQwJUVVt6JwAAAAAAuBTxTTcAAAAAAIYQugEAAAAAMITQDQAAAACAIYRuAAAAAAAMIXQDAAAAAGAIoRsAAAAAAEMI3QAAAAAAGELoBgAAAADAEEI3AAAAAACGELoBAAAAADCE0A0AAAAAgCGEbgAAAAAADCF0AwAAAABgCKEbAAAAAABDCN0AAAAAABhC6AYAAAAAwBBCNwAAAAAAhhC6AQAAAAAwhNANAAAAAIAhhG4AAAAAAAwhdOM3kZKSIu+++67Pr3/77bele/fuYrfbJScnx+vrCwsL5a677pLw8HAZO3asH3sKfz366KMSGRkpUVFRLb0rl5V3331XUlJSWno3LhmMY6Dx5+LLCXMu0Him1/et+bhsNaF76tSpsnLlShERufbaa+XQoUNW2auvvirx8fFit9vlrrvukv3791tl2dnZctNNN0lkZKQ4HA657bbb5KuvvvJ47+LiYnnkkUekS5cuEh4eLjfffLOUl5f7tF81NTXy5JNPSnR0tEREREj//v3l22+/tcrfffddCQoKErvdbv0tXrzYn6ZoNerrk4KCAhkxYoRER0dLQECAfP/9941+7+3bt0tycrKEhoZKSkqKfPPNN1ZZdXW1zJo1S95//30pKyuTG264Qd544w25+eabJTg4WEaNGlXr/VasWCFBQUFSXFwsa9asadLnbU0aOh4asnXrVrnzzjslIiJCHA5HrfIlS5ZI3759JTw8XGJjY+Xpp58Wp9Nplfs73rdv3y4ffPCBHDp0SI4fP97ET9+yGmr7hsbtiy++6NEuNptNAgICZN26dT7Vv9Bbb70lAQEB8uqrr3o872v9S0VDfeHPvH6h8ePH15rH6hrHqiovvfSSXHXVVWKz2aR3796SlZXl3wds5Zo6D4mcG8NXXnml2Gw2uffee6WgoMCnemVlZTJjxgyJiooSh8MhU6dObVS/ejtXtEX19UNubq4EBAR4zDvDhw+36nkr37hxowwYMEA6deokXbt2lTFjxsjRo0et8rrOxedVVFRIr1696jzPXGqaehzU1NTI3LlzpUePHhIeHi6jR4+WEydOeLxm4cKFEhcXJ+Hh4ZKSkiIZGRmNqn85qK/9/V3/exv/3spN54/WrKmZrbnX9/WtlVotbSX69Omje/fu1eLiYr3iiius51evXq2xsbG6d+9edTqdOnfuXL322mu1pqZGVVVPnjypubm56na71e1269q1a9Vut2t5ebmqqrpcLu3fv7/OmDFDT506pS6XS7Ozs9XpdPq0X3/729+0Z8+empubqzU1Nfr8889r9+7d1e12q6pqenq6JicnN29jtBL19cnx48d12bJlmpWVpSKiOTk5Xt8rOTlZ09PTVVX11KlT6nA4dMWKFVpZWakrVqzQyMhILSoqUlXVI0eOqIhYj1VV165dqx9++KE+/vjjOnLkyFrvP23aNJ01a1bTP2wrU1/be5OVlaXvvfeepqWlaURERK3yRYsW6bfffqtOp1OPHDmiN910k86ZM8cq93e8r1y5ss0fD/W1vbdxe7EPPvhAIyIirLnI1/r5+fkaHx+vffr00VdeecXn7V+Kc1F9feHvvH7exo0bdeDAgbXmsbrG8Zw5c7R///76yy+/qNvt1tzcXM3Pz/fn47V6TZ2HNm/erBEREZqZmallZWU6depUvfPOO32q++ijj+qQIUP09OnTevr0aR06dKhOnz7d5217O1e0RfX1w6FDh2qdKy/krXzVqlW6YcMGLS0ttfrp1ltvtcrrOhef9/TTT+vAgQPrPM9cauprf29z7osvvqjJycl69OhRLS8v18mTJ+uQIUOs8nXr1qnD4dBdu3ap2+3W9957T0NDQ/XUqVM+1b9c1Nf+/q7/vY1/b+Wm80dr1tTM1pzr+/rWSq15LdQqQndZWZl26tRJ3W63btq0Se+++26rbOzYsTpv3jzrsdPp1Pbt2+vWrVtrvY/L5dL169eriOjBgwdVVXXDhg3ao0cPra6urnPbeXl5OnjwYO3SpYs6HA4dNmyYHjp0yCr/4x//6HHCP3r0qIqIFhYWqmrr7lx/NNQnF6ovdL/++usaGxurkZGR+pe//MUjdKelpen111/v8frExET9+9//rtnZ2RoaGqoiojabTePj4z1eN3/+/FoH5ZgxY7Rdu3bavn17tdlsmpaW1uTP3Rp4a/tNmzZpv379NCIiQhMTE/Wjjz6q9R5bt271aTG0dOlSvf32263H/oz3pUuXanBwsAYGBqrNZtPJkyd7/7CtTENt39C4rcs999yjM2bMaHT90aNHa3p6ug4cONDjROKt/vm+mTNnjkZGRmqPHj102bJlvn/4VqahvvB3XldVLS0t1YSEBN23b5/HPFbXOD516pQGBwfrTz/9VO/+Tpw4Ubt3765hYWF644036pYtW/xug5bkzzw0adIkffzxx63Hx48f18DAQD1w4ICqnjtXL126VK+55hq12+3aq1cv/fTTT1VV9YorrtDNmzdbdb/44gvt2LGjtZB1u91W3YiICB04cKDu2bOn1v7Xda5oixrqB39D98V27typgYGBWl1d3eC5+LvvvtPExETNyMiodZ55+eWXtVevXmq32zU+Pl5f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rZK3vmjqvF5dXS3Tp0+X5cuX1/lNXV3sdruIiDz33HNit9vlyiuvlFmzZslHH30kIue+gZo7d64kJCRIeHi4OBwOOXPmjJw8ebKZW+W348885G2s5uXlSUJCQp3bXbp0qcTFxUlycrLceOONMmLECBER65yfm5srkyZN8th2UVGRxw2OLiXejoNbbrlF2rdvLw6HQ5YsWSLV1dWyY8cOn8rP++GHH+Tuu++WN954Q4YMGVLvvhw4cECWLVsmS5Ysqfc1q1atkhtvvFE6deokDodDPvnkk0v2OBBpeM6dM2eODB06VG6//Xbp3bu3pKSkiN1ut8byggUL5NNPP5Wff/5ZnE6nrF+/XsaNGyc7d+70qf7+/ftl5MiREh0dLeHh4TJp0iSrrQsLC6W8vLze46yt8HUt2pT1/3nexr8vx4c/229rmiuzNZW3tZJI610LtVjorqqqsk6YO3bskN///vcSGRkpJSUlEhUVJbfffruIiAQEBEhqaqrs379fCgsLJTU1VQ4ePCgDBgyo972rq6utS9GSk5MlICCg3tfOmTNHysvLJTs7W0pKSqzLD/T/Xx6Rk5MjU6ZMke7du0u7du1kzJgxEhYWVu/lUoGBgR712xJf+8Sb6OhoycvLsx5XV1d73Lm2b9++te54/v3330tSUlKzfI62yNe279Gjh8yaNUuKi4utv7KyMlm+fLnP21q9erU8+eSTkpGR4XFpucjlNd7P87XtfR23mzdvloKCApk4caLH897qf/755/LGG29IVFSUREVFyY4dO+Svf/2r3H///T5vPz8/3+OS58OHD0tMTEyj26Sl+NoX/szrx44dkz179si4ceOsthYRGTx4cL13QE1OThYRqXebq1evltWrV8vGjRvlzJkzUlxcLBEREW3uuGiueejisXrixAkpKCiwxmpcXJzHHW0vFBERIe+8844cO3ZM8vLypFevXhIVFWUtsHr06CFr1qzx2HZ5ebmMHz/eYMv8tpp6Lg4ICGjwuKirfPfu3TJ48GBZtGiRTJo0qcH92rZtmxQWFsr1118vUVFRct9991n79O2338rhw4dl8uTJsnjxYiksLJTi4mIZNmzYJXsciDQ85wYHB8uSJUskLy9P8vPzZdiwYeJ0OuV3v/udiJw7344dO1auvvpqCQwMlDvuuEP69u0rmzZt8qn+jBkzJCYmRvbs2SMl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"/>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=2ad9e4c2-56d3-4879-85eb-f0a7c9f5707f">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [103]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Flatten all colors into a single list</span>
<span class="n">all_video_colors</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">vstack</span><span class="p">(</span><span class="n">final_palettes</span><span class="p">)</span>

<span class="n">k</span> <span class="o">=</span> <span class="mi">15</span>

<span class="n">kmeans</span> <span class="o">=</span> <span class="n">KMeans</span><span class="p">(</span><span class="n">n_clusters</span><span class="o">=</span><span class="n">k</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>
<span class="n">kmeans</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">all_video_colors</span><span class="p">)</span>
<span class="n">merged_palette</span> <span class="o">=</span> <span class="n">kmeans</span><span class="o">.</span><span class="n">cluster_centers_</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="nb">int</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"Merged palette"</span><span class="p">)</span>
<span class="n">plot_palette</span><span class="p">(</span><span class="n">merged_palette</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Merged palette
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABdEAAAC6CAYAAABBXgQ0AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAAAkYElEQVR4nO3daZRV1Z03/l0goFVFUZagjI6AI4MTHWVp7KiJxoiYaDu0+SugkU7b6nLZBqKGXtoa038nWl0ag2IcWG2MaMdZ40CcUJcQDUHadgAVsEFklKGKqt/zwof7UMC558IFqWo+n7V4UbXvPvfc/Ttn73O+3HurIiIiAQAAAAAA62mztXcAAAAAAABaKiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABk2K7UB065/scpGhu25L6Q438Wr0g/vvXVVL+6aWvvyjatY+1OacRl16ft2rXf2ruyTVu+dEl64YHfpKbGxq29K9u0zjvtmMaOvSq1b99ua+/KNi0Wrkir/+3llKwPW9XStik9sGvb1FhRsbV3ZZu2/coV6ci3Xkptm5wPW1V1VWrz//0ope3abu092aZ9tWJ5+s8XX0xNzoetqrGxKi3+4u/SRtx+swVsv+PC9Le/+P9T23art/aubNOavuqQvvrDISk1eU/n1tR2ZVXq8eaPUkWTeWlrWtJmWRrf5cHUWCHX2NreePrG3MeUPGsJ0Le+xcsbBOgtwA5VHQXoLUD9yuUC9BagY021AL0l+KpegN4CrGybBOgtQPuGegF6S7DD9gL0FmBlfb0AvQWIpu2TAH3ra1/1lQC9BYhV2wnQW4C2DdsL0FuAFW1WCtBbETMXAAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABAhoqIiK29EwAAAAAA0BJ5JzoAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOgAAAAAAZBCiAwAAAABABiE6AAAAAABkEKIDAAAAAEAGIToAAAAAAGQQogMAAAAAQAYhOrBR7rnnnjRw4MCtvRuQaeDAgemee+7ZYu3lPv+2wji0Duq0+W3pdfJf/uVf0tChQ7fY9v+3cL2ybbKGAy3Fb37zm9StW7dUXV2dpk6durV3Z5v2k5/8JNXV1aWuXbtusP3iiy9O55xzzje7U7RKLS5EHzZsWLrvvvtSSints88+6eOPPy57m+PGjUt9+/ZNHTt2TPvss09h+6W0z5w5M1VUVKTq6urCvxNPPLHQfu211zZrq6qqShUVFWnixIll7/fWUqwGr776ahowYECqrKxMAwcOTK+//nrJ283re/PNN6c999wzVVdXp+985zvpgw8+KLTNnTs3DRkyJHXv3j1VVFSkP//5z8365rW3RsXqkHdMlzPWa/v1r3+dKioq0s0337xR+/7ZZ5+lU089NdXW1qba2tr0ve99b6P6tyRZdZgyZUo6+OCDU11dXaqtrU2HH354+tOf/lTo98QTT6Qjjzwy7bjjjmnnnXdOp5xySvrss89Kbk+p/DqVc762NFtibShFXp1LkXe+tibl1KHUccg6nvP6550v28r5sGjRonTuueemzp07p5qamnTIIYek5cuXl7ztcvovW7YsjRw5MnXt2jXV1tamYcOGZfY944wzWv16Xc75UGyd/O1vf5sGDRqUOnXqlLp165ZGjBiRFi1atEn7uKFx3pg6tQbl1OGaa65Ju+22W6qpqUkDBw5MTz/9dKFt9erV6fLLL0+9evVKNTU16eSTT07z5s0ruX1bk1WHvHupUm3KNenmeu7WpJTzYVPGcvz48WnvvfdOnTp1Sp07d04//OEP0yeffNLsMdOnT0/f+973UseOHVNdXV0aMWJESdu+/vrrU//+/VNNTU3q2bNnuvTSS1N9fX3J+9YSFatD3vVKuet4lrwarl69Ol188cWpe/fuqVOnTmnw4MHpzTffLPt5t7Zy7qnLqVVDQ0O66KKL0oMPPpiWLVuWDjzwwGZzUXV1dWrXrl3q379/YXvnnHNOat++fbPHtObr1XVt6nqdd2zmzSGvvvpq+v3vf58+/vjj9Pnnn+c+38svv7xerdq0aZMuvPDCjXzFLcum5hoplT4vbWh9yctM89pbXNYXLcwBBxwQ7733XixatCi6dOlS9vamTJkS7dq1ixdeeCGamprij3/8Y7Rv3z7++te/ltT+8ccfR0opFi5cWNLz/f73v49OnTrF8uXLy973rSWrBgsWLIja2tq48847Y+XKlXHnnXdGXV1dSWOT13fChAnRs2fPeO+996K+vj4uv/zy2GeffWL16tUREfH555/HbbfdFm+88UaklGLq1KnNtp/X3hpl1SHvmC13rNeYM2dO7LnnnnHAAQfETTfdVPj9+PHjY8CAAZn7vWzZsujdu3dcffXVsWTJkmhoaIg333xzs43LNy2rDl988UXMnDkzmpqaoqmpKR5++OGorq4unPsPPPBAPP7447F06dJYtmxZDBs2LA477LBC/7z2cutUzvnaEm3M2jBgwIAYP378ZmnPq3Ne/7zztbXZ1DqUOg5Zx3Ne/7zzZVs5HxobG2Pw4MExcuTIWLBgQTQ2NsaUKVOivr4+c1tr12lT+q/tJz/5SRx77LHx5Zdfxpdffhnf/e5347zzzlvvcU888UR8+9vfbvXrdVYdyl0nb7vttnjxxRdjxYoVsWDBgjj++OPjjDPOKLSPGTMmTjrppNz9yxrnUuvUWmxqHSZOnBi1tbXx7rvvRlNTU9x7771RWVkZCxYsiIiIa6+9NgYMGBCfffZZLF++PM4+++w49thjC/3z2rc1WXXY2HupDclaGzZk7TltU5477xqhpctbpzdmLNc2c+bMmD9/fkRErFixIi699NI4+uijC+2zZ8+OnXfeOcaNGxfLly+PlStXxttvv13Stq+77rp48803o76+Pj799NM4+OCDY/To0SXvW0uUVYe865Vy1+Fi8mp44403xh577BEzZ86M1atXx9VXXx3dunWLpqamsp97a9rUe+pya/Xpp5/mzj/9+vWLa665pvDz2WefHRdddNHmH4QWYlOzvrxjM28Oue+++4peD0REXHTRRXH22WdvsO3zzz+P7bbbLl599dWS97kl2tRco9R5qdT1JS8zXbe9pWV9LSpEX7ZsWey4447R1NQUzz33XBx33HHN2p999tkYNGhQdOrUKbp27RrXXnttbtvDDz8cffr0abad3r17x0MPPVRS+8ZefB1//PExcuTIjXrdLUmxGowbNy7233//Zo/fb7/94u677y78nFWHvL6nnnpqXHnllYW2+vr6aNeuXbz44ovr7WPeidMSTqxyFatD3jG7ucb65JNPjvHjx8e3v/3tDYboo0ePjrq6uujVq1fcdttthfZbb701vvWtb5X1+luKvDlpjcbGxnj00UcjpRQfffTRBh/zzjvvRJs2baKhoaGk9nLrVMr52lrk1eGWW26Jnj17Rl1dXfz85z9f7wa43PY1supcrH/e+dqalFOHUsch63jO6593vmwr58Pjjz8evXr1ypxnIorXKa//rFmz4phjjonOnTtHbW1tfP/734+PP/640N6lS5d4/vnnCz+/9NJLsf322ze7SF66dGn06dMnZsyY0arX62J12Nzr5H/+539Gr169Cj+PGTMmTjjhhBg+fHh07NgxevfuHRMnTmzWp9g4l1Kn1qKcOtxwww3rhd7t2rWLt956KyIiDj300LjrrrsKbTNnzoyUUuGYz2ufMmVKDB48OHbcccfo3LlznH766fHFF18UHn///ffH/vvvH9XV1dGrV6+44oorWm1YVawOpdxLFbvHi8heGyKKz2mlPHep1wCtQSnXrVljmTe/r2358uVx2WWXxa677lr43aWXXtrsP/vW1djYGGPHjo299947qquro3fv3vHUU09t8LFjx46NI444orQX3QIVq0Pe9Uop63jW+VJuDf/pn/6p2X+ofvbZZ5FSKgTvrVE599Tl1GrKlClRWVkZKaWoqqqKPffcc73HvPHGG9G2bduYPXt24Xf/m0P0YrXIO3Y39thcew4ZO3ZsdOjQIdq0aRNVVVWFoHzSpElxwAEHRFVVVZx88skxfPjwzBD9V7/6Vey7777lDcBWVk6uUcq8FFF8rV5bXmZarL0l3Du0iK9zmThxYqqtrU277LJLWrp0adpxxx3TiSeemF566aVUW1ubrrnmmjR16tR00kknpcsuuyzNnz8/zZgxI/3t3/5tSikVbVvzkbLnnnsuNTU1pWeeeSYtXLgwDR48uKT2NQ444IDUtWvXNGTIkDRjxowNvo7PPvssPfPMM+ncc8/dgqO1ZZRSg3fffXe975YcOHBgevfdd1NKxeuQ17epqSl9fU78PxFRaN9WlFKHvGN2c4z1ww8/nBYuXJj5vWDTpk1LFRUVae7cuenBBx9Mo0aNKnzkZ9KkSal3795p6NChaaeddkqHHHJIeuaZZzbTCH0zSqnDGrW1tal9+/Zp6NCh6cc//nHaY489NrjNSZMmpX333Tdtt912JbWXW6e846A1KKUOL7zwQrr88svT7373uzR37tyU0tfH5xrltq+RVee8/qWuMS3Z5qhDKeNQ7HjO6593vmwr58OaeeT8889PO+20UzrggAOafTQ5r055/ZuamtIll1ySPv300zRr1qxUWVmZzjvvvGbta9ehqakprVy5Mv33f/934XejR49OZ555Ztp77723yDhtaaWuD5tznZw0aVKzj3unlNLTTz+dBg0alL788st04403pjPOOCN9+OGHhfZi41xKnVq6zVGH0047LX3++edp6tSpqbGxMY0fPz5179497b///imlDY9TSinzemrd9jZt2qTrrrsu/c///E+aNm1amj17dho1alTh8XV1dWnixIlpyZIl6Q9/+EO6884704QJE7bUkG0RG3O9lHUvVez+IaXia0Opa3jWc5fav6UrtQ7FxjJvfk8ppVdeeSXV1tamysrKdOONN6bLL7+80DZp0qS08847p6OOOip17tw5HXHEEemtt94qtN96663p5ptvTg888EBasmRJev7559Nuu+22wdezoTmvNSilDnnXK3nrcLHzpdwajhgxIr399tvpww8/TA0NDWncuHFp0KBBqXPnzltqyLaYzXFPXU6tDjzwwPTXv/41pfR1RrT2+rzGXXfdlY4//vjUvXv3Zr+/9957U11dXdp///3TDTfcUFhbWqtSz4tix+7GHptrzyEXXnhhuuOOO1K/fv3SsmXL0j333JMWLlyYhgwZki644IK0aNGiNGzYsHT//fdnvoa777675K+namk2R66RNy+llJ8frZGXmbaKTPWbz+2zXXHFFYWPs3znO9+JSZMmFdpGjhwZw4YN22C/Ym1NTU1xww03xPbbbx9t27aN9u3bxwMPPFBy+9KlS+ONN96I+vr6WLhwYVxyySXRs2fPWLx48XrPddVVV8XAgQM36bW3FMVqMHz48PjHf/zHZo//6U9/GiNGjIiI4nXI6zt+/Pjo0aNHTJs2LVauXBk/+9nPoqKiIq6++ur1tpW2gXeiF6tD3jFb7lgvXLgwdt9995gxY0ZExAbfiV5TU9Ps4zsjR44sbP/oo4+Otm3bxsSJE6O+vj4eeeSRqKysjA8++GAzjtA3o1gd1rZ8+fK477774je/+c0G26dMmRKdOnWKZ599tuT2cuuUdxy0Jnnz0j/8wz8Ufq6vr4+amprCu8jKbV/bhuqc1z/vfG1NyqlD3jjkHc95/fPOl23lfBgxYkSklOKWW26JVatWxSuvvBLV1dXx8ssvR0R+nfL6r2vq1KnRvn37aGxsjIiv30F19NFHx/z58+OLL76IY445JlJKhf6vv/567LvvvrFy5cqIaN3rdbE6bM518sknn4yampp49913C78bM2bMeu+IOu644wrHe94459WpNSmnDvX19fGzn/0s2rRpE23bto1OnTo1e4f+mDFjol+/fjFr1qxYunRpnHXWWVFRURH33XdfSe3reuSRR6J3796Zr+Wiiy6Kc889d9MHYysqVoe8e6li9w+lXOsUm9PynntjrgFag2J1yBvLda07v69t/vz58ctf/rLZnLHXXntFdXV1vPLKK7Fq1aq45ZZbokuXLoVPAeyzzz7x29/+Nvc13HnnnbHLLrvEnDlzSnnJLVLevFTseiVvHS52vqxrY2u4ZMmSGDZsWKSUom3bttG9e/dma09rVM49dbm1KvZJmK+++ipqamri0Ucfbfb7t99+O+bNmxerV6+O119/PXr16hU33njj5h6WraLU++qI9Y/djTk2NzSHrPv1bvfee+8Gr6M29E70P/3pT9GuXbuYN29eqS+1RSon18g71jdmfcnLTPPaW8K9Q4t4J/oaL730UjryyCNTQ0NDmjp1aho0aFChbdasWalPnz4b7Fes7e6770433HBDmjx5cqqvr09vvvlmGjVqVHrqqadKaq+urk6DBg1K7dq1S7W1ten6669PDQ0N6bXXXmv2PBGRxo8f32r/h2qNYjWorq5Oixcvbvb4xYsXp44dO6aUitchr+/ZZ5+dLrjggnTSSSelnj17psbGxrTffvulnXbaaXO+vFajWB1KOWbLGevLLrssnXPOOUXfJdi9e/fUrl27ws+77bZbmj17duH5DzvssHTyySendu3apaFDh6aDDjqo1b0bPaXidVjbDjvskM4666x00003pVdeeaVZ21/+8pd03HHHpVtvvTUde+yx6/XNai+3TnnHQWtSrA5z5sxp9k6mdu3apW7dum229rVtqM55/fPO19aknDrkjUPe8ZzXP+982VbOh+rq6tSzZ890wQUXpPbt26fBgwenoUOHpj/84Q8ppfw65fWfP39+OvPMMwt/SPHII49M9fX1aenSpSmllMaOHZt22223NGDAgHTQQQelIUOGpJRS2mmnnVJDQ0M677zz0u233546dOiwxcdpS8tbHzbHOvnCCy+ks846K02cODH169evWdu67+Bcs/1SxrlYnVqbcupw1VVXpaeeeiq9//77qb6+Pj366KPptNNOS++8805K6et383/3u99NRxxxROrbt28aOHBgqq6uLoxTXvsHH3yQTjrppNS9e/dUU1OTzjrrrPTFF18U9uWZZ55Jhx9+eOrcuXPq1KlTuuOOO5q1tyZ581Kxe6li9w95a0Mpc1qx596Ya4DWoFgd8sYyb35fW+fOndOIESPSD37wg/TVV1+llL4e66FDh6bBgwen9u3bpwsuuCB16NChpDqv8cADD6QrrrgiPfvss/9r61DK9UqxdbjYOJZbw5/+9Kfpk08+SXPmzEkrV65MY8eOTUcffXThUxqtUTn31OXWqpjf/e53qbKyMp1wwgnNfn/QQQelLl26pLZt26ZvfetbadSoUenBBx/cjCOy9RSrRd6xW+qxWeocsu7cn9L611Vr3HXXXWnIkCGpS5cum/rSW4Ryco28Y72U/Cil/My0tWSqWz1EX7VqVaqtrU21tbXptddeSz/4wQ9SXV1dWrJkSeratWs64ogjUkpfH9Tr/jXkNYq1TZ06NR1//PFpwIABqU2bNmnAgAHp2GOPTU888URJ7euqqKhIFRUV6/3++eefT3Pnzk1///d/vynDsFWVWoP+/fuv95dw//znPxdu7IrVIa9vRUVFGjVqVPrggw/S/Pnz06hRo9JHH32UjjzyyM37YluwUuuQd8yWO9bPPvtsuvXWW1PXrl1T165d02uvvZZ+8YtfpL/7u78rbG/OnDmpoaGh8PMnn3ySevTokVJKacCAARs8R1qLUuuwIQ0NDc0+Dj9t2rR0zDHHpOuuuy6dddZZ6z2+WHu5dco7Dlq6UuvQvXv3NGvWrEK/hoaGZhdU5bZvyNp1zuu/sWtMS7O56pA3DnnHc17/vPNlWzkf8ubfvDrl9R89enRavnx5mjJlSlqyZEnhazHi/37cuVOnTumuu+5Ks2fPTrNmzUq9e/dOXbt2TXvvvXeaPXt2mj59ejrttNMKdU4ppWOOOSbdfPPNmzw236SNWR/KXSdffPHFdMopp6QJEyako48+er32teu49vZLGedidWoNNlcdpk6dmk499dS01157pTZt2qSjjjoq9e/fPz333HMppZQ6dOiQrr/++jRr1qw0Z86c9P3vfz/V19env/mbvympfeTIkalHjx5p+vTpacmSJen+++8vnCv19fXphz/8YTr//PPT7Nmz0+LFi9PIkSPX++qAlmxTr5fWvZcqdv+QtzZs7Bq+7nNvyjVAS1NqHfLGMm9+X1dDQ0NavHhxmjdvXkopf14rVueUUpowYUK6+OKL09NPP90qv8ql1DrkXa+UM47l1nDq1KnpnHPOSd26dUvbbbddOuWUU1LHjh3Tq6++usnjsjVsrnvqcmtVzLhx49LZZ5+d+TWfa7Rps9XjurKUWou8Y7eUY3Nj5pB15/6Uvr4+WNeSJUvSQw891LK/WqSIzZVr5B3rpeRHKeVnpq0mU91q74Ffx9NPPx1DhgyJiIgrr7wyfvnLXzZrf/vtt2OHHXaIiRMnRkNDQyxatChef/313Lb7778/evbsGdOmTYuIiGnTpkWPHj1i3LhxJbVPnjw5pk+fHqtXr46lS5fGZZddFt26dYtFixY127/TTz89zjzzzC00Ot+MvBosWLAgamtrY9y4cbFq1aoYN25c1NXVxZdffhkRxeuQ13fhwoUxY8aMaGpqitmzZ8eQIUPW++M0K1asiBUrVkRKKd54441YsWJFs4+n5bW3Fnl1yDtmyx3refPmxdy5cwv/DjvssLjqqqsK/cePHx9t27aNK6+8MlatWhWTJ0+OmpqaeOGFFyIi4oMPPojKysp47LHHorGxMR577LFW+XUueXV47LHH4p133omGhob46quv4pprrokddtih8DqnTZsWO++8c/z617/e4Pbz2sutU95x0Frk1eG5556LmpqamDx5cqxatSquuOKKaNu2beGj2OW259U5r3/e+dpalFuHvHHIO57z+uedL9vK+bBw4cLo3Llz3H777bF69eqYPHlydOzYsfBxy7w65fU/9dRT44wzzoj6+vr44osvYujQoc0+qvzRRx/F559/Hk1NTTFlypTYe++9C3Pc6tWrm9V47ty5kVKKP/7xj7Fs2bJvYPQ2n7w6lLtOvvjii1FbWxuPP/74Bp9/zJgx0bZt27jzzjujoaEhHn/88ejQoUO8//77JY1zsTq1JuXW4V//9V9jwIABMXPmzGhqaip8PPm5556LiIg5c+YU2t5///047LDDYvTo0YXt57Ufeuihcdlll0VjY2N88skncfjhh0enTp0i4uuPprdp0yYee+yxiPj6fqNLly5x0kknbanh2mLy6pB3L1Xs/iFvbcib0/KeO69/a5JXh7yxzJvf77777vj000+jqakp5s6dGz/60Y+ib9++hT+G+/LLL0fHjh1j8uTJsXr16rj99tubfZ3LTTfdFHvttVdMnTo1mpqaYtasWTF9+vSIiJgwYULU1dUV/qhva1bKOl3seiVvHS52vpRbw3PPPTeOPfbYmDdvXjQ2NsbEiROjffv2ha9oaG3Kvacut1ZZX+cyY8aMqKioiP/6r/9ab58ffPDBWLx4cTQ1NcVbb70Vu+22W/zbv/3bZhuTrSWvFnnHbt6xmTeHrPt1LgsWLIiampr1rqPW/TqXO+64I3r16tUqM6W1lZtr5B3reevLGnmZabH2lpT1tZgQ/fzzzy9MWP3794/33ntvvcc8+eSTcfDBB0fHjh2jW7ducd1115XUdu2118Yee+wRVVVVseuuu8aVV15ZWCzy2idMmBB77rlnVFZWRufOneOEE06Iv/zlL832a8GCBdGhQ4fCRXlrVUoNXn755ejXr19sv/320b9//3j11VebtRerQ7G+H3/8cey7775RWVkZu+yyS1xyySWF7/JcI6W03r81fx27lPbWopQ65B3T5Y712jb0negDBgyI0aNHR11dXfTs2TNuueWWZn2efPLJ2HfffaOqqioGDBgQTz311KYOx1aTV4fx48dH3759o6qqKnbaaac46qijms0B55xzTlRUVERVVVWzf7NmzSqpvdw6ReSfr61BKefD2LFjo0ePHlFXVxc///nPY8CAAc1ugMtpz6tzKdvPO19bg81Rh40Zhw0dz8X6l3K+bCvnwxtvvBGHHHJIVFZWRt++fePee+9t1p5Xp2L9p0+fHoceemhUVVUVgte1b3IeeeSR6NGjR+ywww7Rp0+fzL8TsUZqAd9ruClKWR/KWSePOuqoaNOmzXrrwxpjxoyJE044IYYPHx4dO3aMvfbaKx566KHM/V13nDe2Ti1VuXWor68vfEd2dXV19OnTJ/793/+90D558uTYc889Y4cddohdd901rrnmmmZzVl77yy+/HPvtt19UVVXFgQceGDfccEMhRI+IuP3226Nbt27RsWPHOPHEE+OCCy5olSF6Xh1KuZcqdv+wtg2tDcXmtFKeO29ObC1KWR/Wtu5Y5s3vF154YXTv3j0qKyujW7ducfrpp8eHH37YbJv33HNP7L777lFdXR2HHXZYvPnmm4W2xsbGuP7666NPnz5RVVUVffr0iaeffjoiInbffffYbrvtms13++2332YYlW9eXh1KuV7JW8ezzpdya7ho0aIYPnx4dO3aNTp27Bj9+vWL//iP/9jcQ/SNKfeeutxaZYXo//zP/xxHHnnkBvf5iCOOiE6dOkVVVVX07ds3fvWrX7X6ADcivxZ5x27esZk3h6wbokd8/YaF/fffP6qqqmLo0KExfPjw9UL0Qw89NH7xi19svoHYSsrNNSLy56W1bWitzstM89pbUtZX8X93CAAAAAAAWEfr/pIlAAAAAADYgoToAAAAAACQQYgOAAAAAAAZhOgAAAAAAJBBiA4AAAAAABmE6AAAAAAAkEGIDgAAAAAAGYToAAAAAACQQYgOAAAAAAAZhOgAAAAAAJBBiA4AAAAAABn+D5yr5CzBq6BFAAAAAElFTkSuQmCC"/>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs" id="cell-id=a29744e9-083e-4459-97be-29121d86f3bf">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span> 
</pre></div>
</div>
</div>
</div>
</div>
</div>
</main>
</body>
</html>
