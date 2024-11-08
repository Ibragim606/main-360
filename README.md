# main-360
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -moz-user-select: none;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
  -ms-text-size-adjust: none;
  -moz-text-size-adjust: none;
  -webkit-text-size-adjust: none;
  text-size-adjust: none;
  -webkit-user-drag: none;
  -webkit-touch-callout: none;
  -ms-content-zooming: none;
  -webkit-tap-highlight-color: rgba(0,0,0,0);
}

html, body {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  overflow: hidden;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 16px;
  background-color: #000;
  color: #fff;
}

a, a:hover, a:active, a:visited {
  text-decoration: none;
  color: inherit;
}

#pano {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

#titleBar {
  position: absolute;
  top: 0;
  left: 0;
  right: 40px;
  height: 40px;
  text-align: center;
}

.mobile #titleBar {
  height: 50px;
  right: 50px;
}

/* If there is a fullscreen button the title bar must make space for it */
body.fullscreen-enabled #titleBar {
  right: 80px;
}

body.fullscreen-enabled.mobile #titleBar {
  right: 100px;
}

/* If there are multiple scenes the title bar must make space for the scene list toggle */
body.multiple-scenes #titleBar {
  left: 40px;
}

body.multiple-scenes.mobile #titleBar {
  left: 50px;
}

#titleBar .sceneName {
  width: 100%;
  height: 100%;
  line-height: 30px;
  padding: 5px;
  background-color: rgb(58,68,84);
  background-color: rgba(58,68,84,0.8);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;

  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
  user-select: text;
}

.mobile #titleBar .sceneName {
  line-height: 40px;
}

#fullscreenToggle {
  display: none;
  position: absolute;
  top: 0;
  right: 0;
  width: 40px;
  height: 40px;
  padding: 5px;
  background-color: rgb(103,115,131);
  background-color: rgba(103,115,131,0.8);
}

.mobile #fullscreenToggle {
  width: 50px;
  height: 50px;
}

body.fullscreen-enabled #fullscreenToggle {
  display: block;
}

#fullscreenToggle .icon {
  position: absolute;
  top: 5px;
  right: 5px;
  width: 30px;
  height: 30px;
}

.mobile #fullscreenToggle .icon {
  top: 10px;
  right: 10px;
}

#fullscreenToggle .icon.on {
  display: none;
}

#fullscreenToggle .icon.off {
  display: block;
}

#fullscreenToggle.enabled .icon.on {
  display: block;
}

#fullscreenToggle.enabled .icon.off {
  display: none;
}

#autorotateToggle {
  display: block;
  position: absolute;
  top: 0;
  right: 0;
  width: 40px;
  height: 40px;
  padding: 5px;
  background-color: rgb(103,115,131);
  background-color: rgba(103,115,131,0.8);
}

.mobile #autorotateToggle {
  width: 50px;
  height: 50px;
}

/* If there is a fullscreen button, autorotate must placed a bit to the left */
body.fullscreen-enabled #autorotateToggle {
  right: 40px;
}

body.fullscreen-enabled.mobile #autorotateToggle {
  right: 50px;
}

#autorotateToggle .icon {
  position: absolute;
  top: 5px;
  right: 5px;
  width: 30px;
  height: 30px;
}

.mobile #autorotateToggle .icon {
  top: 10px;
  right: 10px;
}

#autorotateToggle .icon.on {
  display: none;
}

#autorotateToggle .icon.off {
  display: block;
}

#autorotateToggle.enabled .icon.on {
  display: block;
}

#autorotateToggle.enabled .icon.off {
  display: none;
}

#sceneListToggle {
  position: absolute;
  top: 0;
  left: 0;
  width: 40px;
  height: 40px;
  padding: 5px;
  background-color: rgb(103,115,131);
  background-color: rgba(103,115,131,0.8);
}

.mobile #sceneListToggle {
  width: 50px;
  height: 50px;
}

#sceneListToggle .text {
  position: absolute;
  top: 5px;
  left: 15px;
  width: 100%;
  line-height: 30px;
}

#sceneListToggle .icon {
  position: absolute;
  top: 5px;
  right: 5px;
  width: 30px;
  height: 30px;
}

.mobile #sceneListToggle .icon {
  top: 10px;
  right: 10px;
}

#sceneListToggle .icon.on {
  display: none;
}

#sceneListToggle .icon.off {
  display: block;
}

#sceneListToggle.enabled .icon.on {
  display: block;
}

#sceneListToggle.enabled .icon.off {
  display: none;
}

#sceneList {
  position: absolute;
  top: 0;
  left: -220px;
  padding-top: 40px;
  width: 220px;
  max-height: 100%;
  overflow-x: hidden;
  overflow-y: auto;
  margin-left: 0;
  -webkit-transition: margin-left 0.5s ease-in-out;
  transition: margin-left 0.5s ease-in-out;
}

.mobile #sceneList {
  padding-top: 50px;
}

#sceneList .scenes {
  width: 100%;
  background-color: rgb(58,68,84);
  background-color: rgba(58,68,84,0.8);
}

.mobile #sceneList {
  width: 100%;
  height: 100%;
  left: -100%;
}

.mobile #sceneList.enabled {
  margin-left: 100%;
}

.mobile #sceneList .scenes {
  height: 100%;
}

#sceneList.enabled {
  margin-left: 220px;
}

#sceneList .scene {
  display: block;
  width: 100%;
  height: 30px;
}

.mobile #sceneList .scene {
  height: 40px;
}

#sceneList .scene .text {
  width: 100%;
  height: 100%;
  padding: 0 15px;
  line-height: 30px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.mobile #sceneList .scene .text {
  line-height: 40px;
}

.no-touch #sceneList .scene:hover {
  background-color: rgb(103,115,131);
  background-color: rgba(103,115,131,0.8);
}

#sceneList .scene.current {
  background-color: rgb(103,115,131);
  background-color: rgba(103,115,131,0.8);
}

/* Hide scene list when only a single scene exists */
body.single-scene #sceneList, body.single-scene #sceneListToggle {
  display: none;
}

/* Link hotspot */

.link-hotspot {
  width: 60px;
  height: 60px;
  margin-left: -30px;
  margin-top: -30px;
  opacity: 0.9;
  -webkit-transition: opacity 0.2s;
  transition: opacity 0.2s;
}

.no-touch .link-hotspot:hover {
  opacity: 1;
}

.mobile .link-hotspot {
  width: 70px;
  height: 70px;
}

.link-hotspot-icon {
  width: 100%;
  height: 100%;
  cursor: pointer;
}

.link-hotspot-tooltip {
  position: absolute;
  left: 100%;
  top: 14px; /* ( 60 - (16 + 2*8) ) / 2 */

  margin-left: 3px;

  font-size: 16px;

  max-width: 300px;

  padding: 8px 10px;

  border-radius: 5px;

  background-color: rgb(58,68,84);
  background-color: rgba(58,68,84,0.8);

  color: #fff;

  white-space: nowrap;
  text-overflow: ellipsis;
  overflow: hidden;

  cursor: pointer;

  opacity: 0;

  -ms-transform: translateX(-8px);
  -webkit-transform: translateX(-8px);
  transform: translateX(-8px);

  -webkit-transition: -ms-transform 0.3s,
                      -webkit-transform 0.3s,
                      transform 0.3s,
                      opacity 0.3s;
  transition: -ms-transform 0.3s,
              -webkit-transform 0.3s,
              transform 0.3s,
              opacity 0.3s;
}

.mobile .link-hotspot {
  top: 19px; /* ( 70 - (16 + 2*8) ) / 2 */
}

.no-touch .link-hotspot:hover .link-hotspot-tooltip {
  opacity: 1;
  -ms-transform: translateX(0);
  -webkit-transform: translateX(0);
  transform: translateX(0);
}

/* Prevent tooltip from triggering */
.link-hotspot-tooltip {
  pointer-events: none;
}
.no-touch .link-hotspot:hover .link-hotspot-tooltip {
  pointer-events: all;
}

/* Fallback mode without pointer-events (IE8-10) */
.tooltip-fallback .link-hotspot-tooltip {
  display: none;
}
.no-touch .tooltip-fallback .link-hotspot:hover .link-hotspot-tooltip {
  display: block;
}

/* Info hotspot */

.info-hotspot {
  line-height: 1.2em;
  opacity: 0.9;
  -webkit-transition: opacity 0.2s 0.2s;
  transition: opacity 0.2s 0.2s;
}

.no-touch .info-hotspot:hover {
  opacity: 1;
  -webkit-transition: opacity 0.2s;
  transition: opacity 0.2s;
}

.info-hotspot.visible {
  opacity: 1;
}

.info-hotspot .info-hotspot-header {
  width: 40px;
  height: 40px;
  border-radius: 20px;
  background-color: rgb(103,115,131);
  cursor: pointer;
  -webkit-transition: width 0.3s ease-in-out 0.5s,
                      border-radius 0.3s ease-in-out 0.5s;
  transition: width 0.3s ease-in-out 0.5s,
              border-radius 0.3s ease-in-out 0.5s;
}

.mobile .info-hotspot .info-hotspot-header {
  width: 50px;
  height: 50px;
  border-radius: 25px;
}

.desktop.no-touch .info-hotspot .info-hotspot-header:hover {
  width: 260px;
  border-radius: 5px;
  -webkit-transition: width 0.3s ease-in-out,
                      border-radius 0.3s ease-in-out;
  transition: width 0.3s ease-in-out,
              border-radius 0.3s ease-in-out;
}

.desktop .info-hotspot.visible .info-hotspot-header,
.desktop.no-touch .info-hotspot.visible .info-hotspot-header:hover {
  width: 260px;
  border-radius: 5px;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
  -webkit-transition: width 0.3s ease-in-out,
                      border-radius 0.3s ease-in-out;
  transition: width 0.3s ease-in-out,
              border-radius 0.3s ease-in-out;
}

.info-hotspot .info-hotspot-icon-wrapper {
  width: 40px;
  height: 40px;
}

.mobile .info-hotspot .info-hotspot-icon-wrapper {
  width: 50px;
  height: 50px;
}

.info-hotspot .info-hotspot-icon {
  width: 90%;
  height: 90%;
  margin: 5%;
}

.info-hotspot .info-hotspot-title-wrapper {
  position: absolute;
  left: 40px;
  top: 0;
  width: 0;
  height: 40px;
  padding: 0;
  overflow: hidden;
  -webkit-transition: width 0s 0.4s,
                      padding 0s 0.4s;
  transition: width 0s 0.4s,
              padding 0s 0.4s;
}

.desktop .info-hotspot.visible .info-hotspot-title-wrapper,
.desktop.no-touch .info-hotspot .info-hotspot-header:hover .info-hotspot-title-wrapper {
  width: 220px;
  padding: 0 5px;
  -webkit-transition: width 0s 0.4s,
                      padding 0s 0.4s;
  transition: width 0s 0.4s,
              padding 0s 0.4s;
}

.info-hotspot .info-hotspot-title-wrapper:before {
  content: '';
  display: inline-block;
  vertical-align: middle;
  height: 100%;
}

.info-hotspot .info-hotspot-title {
  display: inline-block;
  vertical-align: middle;

  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
  user-select: text;
}

.info-hotspot .info-hotspot-close-wrapper {
  position: absolute;
  left: 260px;
  top: 0;
  height: 40px;
  width: 40px;
  border-top-right-radius: 5px;
  background-color: rgb(78,88,104);
  visibility: hidden;
  -ms-transform: perspective(200px) rotateY(90deg);
  -webkit-transform: perspective(200px) rotateY(90deg);
  transform: perspective(200px) rotateY(90deg);
  -ms-transform-origin: 0 50% 0;
  -webkit-transform-origin: 0 50% 0;
  transform-origin: 0 50% 0;
  -webkit-transition: -ms-transform 0.3s 0.3s,
                      -webkit-transform 0.3s 0.3s,
                      transform 0.3s 0.3s,
                      visibility 0s 0.6s;
  transition: -ms-transform 0.3s 0.3s,
              -webkit-transform 0.3s 0.3s,
              transform 0.3s 0.3s,
              visibility 0s 0.6s;
}

.desktop .info-hotspot.visible .info-hotspot-close-wrapper {
  visibility: visible;
  -ms-transform: perspective(200px) rotateY(0deg);
  -webkit-transform: perspective(200px) rotateY(0deg);
  transform: perspective(200px) rotateY(0deg);
  -webkit-transition: -ms-transform 0.3s,
                      -webkit-transform 0.3s,
                      transform 0.3s,
                      visibility 0s 0s;
  transition: -ms-transform 0.3s,
              -webkit-transform 0.3s,
              transform 0.3s,
              visibility 0s 0s;
}

.info-hotspot .info-hotspot-close-icon {
  width: 70%;
  height: 70%;
  margin: 15%;
}

.info-hotspot .info-hotspot-text {
  position: absolute;
  width: 300px;
  height: auto;
  max-height: 200px;
  top: 40px;
  left: 0;
  padding: 10px;
  background-color: rgb(58,68,84);
  border-bottom-right-radius: 5px;
  border-bottom-left-radius: 5px;
  overflow-y: auto;
  visibility: hidden;
  /* rotate(90deg) causes transition flicker on Firefox 58 */
  -ms-transform: perspective(200px) rotateX(-89.999deg);
  -webkit-transform: perspective(200px) rotateX(-89.999deg);
  transform: perspective(200px) rotateX(-89.999deg);
  -ms-transform-origin: 50% 0 0;
  -webkit-transform-origin: 50% 0 0;
  transform-origin: 50% 0 0;
  -webkit-transition: -ms-transform 0.3s,
                      -webkit-transform 0.3s,
                      transform 0.3s,
                      visibility 0s 0.3s;
  transition: -ms-transform 0.3s,
              -webkit-transform 0.3s,
              transform 0.3s,
              visibility 0s 0.3s;

  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
  user-select: text;
}

.desktop .info-hotspot.visible .info-hotspot-text {
  visibility: visible;
  -ms-transform: perspective(200px) rotateX(0deg);
  -webkit-transform: perspective(200px) rotateX(0deg);
  transform: perspective(200px) rotateX(0deg);
  -webkit-transition: -ms-transform 0.3s 0.3s,
                      -webkit-transform 0.3s 0.3s,
                      transform 0.3s 0.3s,
                      visibility 0s 0s;
  transition: -ms-transform 0.3s 0.3s,
              -webkit-transform 0.3s 0.3s,
              transform 0.3s 0.3s,
              visibility 0s 0s;
}

/* Info hotspot modal */

.desktop .info-hotspot-modal {
  display: none;
}

.info-hotspot-modal {
  top: 0;
  left: 0;
  position: absolute;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 11000 !important;
  background-color: rgba(0,0,0,.5);
  line-height: 1.2em;
  opacity: 0;
  visibility: hidden;
  -webkit-transition: opacity 0.2s ease-in-out 0.5s,
                      visibility 0s 0.7s;
  transition: opacity 0.2s ease-in-out 0.5s,
              visibility 0s 0.7s;
}

.info-hotspot-modal.visible {
  opacity: 1;
  visibility: visible;
  -webkit-transition: opacity 0.2s ease-in-out,
                      visibility 0s 0s;
  transition: opacity 0.2s ease-in-out,
              visibility 0s 0s;
}

.info-hotspot-modal .info-hotspot-header {
  position: absolute;
  top: 60px;
  left: 10px;
  right: 10px;
  width: auto;
  height: 50px;
  background-color: rgb(103,115,131);
  background-color: rgba(103,115,131,0.8);
  opacity: 0;
  -webkit-transition: opacity 0.3s ease-in-out 0.2s;
  transition: opacity 0.3s ease-in-out 0.2s;
}

.info-hotspot-modal.visible .info-hotspot-header {
  opacity: 1;
  -webkit-transition: opacity 0.3s ease-in-out 0.2s;
  transition: opacity 0.3s ease-in-out 0.2s;
}

.info-hotspot-modal .info-hotspot-icon-wrapper {
  width: 50px;
  height: 50px;
}

.info-hotspot-modal .info-hotspot-icon {
  width: 90%;
  height: 90%;
  margin: 5%;
}

.info-hotspot-modal .info-hotspot-title-wrapper {
  position: absolute;
  top: 0;
  left: 50px;
  right: 50px;
  width: auto;
  height: 50px;
  padding: 0 10px;
}

.info-hotspot-modal .info-hotspot-title-wrapper:before {
  content: '';
  display: inline-block;
  vertical-align: middle;
  height: 100%;
}

.info-hotspot-modal .info-hotspot-title {
  display: inline-block;
  vertical-align: middle;

  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
  user-select: text;
}

.info-hotspot-modal .info-hotspot-close-wrapper {
  position: absolute;
  top: 0;
  right: 0;
  width: 50px;
  height: 50px;
  background-color: rgb(78,88,104);
  background-color: rgba(78,88,104,0.8);
  cursor: pointer;
}

.info-hotspot-modal .info-hotspot-close-icon {
  width: 70%;
  height: 70%;
  margin: 15%;
}

.info-hotspot-modal .info-hotspot-text {
  position: absolute;
  top: 110px;
  bottom: 10px;
  left: 10px;
  right: 10px;
  padding: 10px;
  background-color: rgb(58,68,84);
  background-color: rgba(58,68,84,0.8);
  overflow-y: auto;
  opacity: 0;
  -webkit-transition: opacity 0.3s ease-in-out;
  transition: opacity 0.3s ease-in-out;

  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
  user-select: text;
}

.info-hotspot-modal.visible .info-hotspot-text {
  opacity: 1;
  -webkit-transition: opacity 0.3s ease-in-out 0.4s;
  transition: opacity 0.3s ease-in-out 0.4s;
}

/* View control buttons */

.viewControlButton {
  display: none;
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 40px;
  height: 40px;
  padding: 5px;
  background-color: rgb(103,115,131);
  background-color: rgba(103,115,131,0.8);
}

body.view-control-buttons .viewControlButton {
  display: block;
}

/* Hide controls when width is too small */
@media (max-width: 600px) {
  body.view-control-buttons .viewControlButton {
    display: none;
  }
}

.viewControlButton .icon {
  position: absolute;
  top: 5px;
  right: 5px;
  width: 30px;
  height: 30px;
}

/* Center is at margin-left: -20px */
.viewControlButton-1 {
  margin-left: -145px;
}
.viewControlButton-2 {
  margin-left: -95px;
}
.viewControlButton-3 {
  margin-left: -45px;
}
.viewControlButton-4 {
  margin-left: 5px;
}
.viewControlButton-5 {
  margin-left: 55px;
}
.viewControlButton-6 {
  margin-left: 105px;
}
