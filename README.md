<style>
* {margin: 0;padding: 0;}
html,body {height: 100%;width: 100%;}

.🔫 {position: fixed;top: 0;left: 0;-webkit-appearance: none;width: 100%;height: 100%;overflow: hidden;border: none;background: none;}

.🔫:checked ~ .🚁 {
	top: 80%;
	transform-origin: 0 0;
	transform: rotate(-80deg);
	transition: transform 0.5s linear, top 0.8s linear;
	animation-play-state: paused;
}
.🔫 ~ .🚁 > em {
	font-style: normal;
	opacity: 1;
}
.🔫:checked ~ .🚁 > em {
	animation: noPlane 0.1s 0.8s 1 forwards linear;
}
@keyframes noPlane {
	form {opacity: 1;}
	to {opacity: 0;}
}

.🚁 {
	position: fixed;
	top: 0.266667rem;
	right: -1.333333rem;
	font-size: 1.6rem;
	animation: plane 5s 0s infinite cubic-bezier(0.22, 0.47, 0.4, 0.64);
}
@keyframes plane {
	form {right: -1.333333rem;}
	to {right: 100%;}
}

.💥 {
	position: absolute;
	top: 50%;
	left: 50%;
	z-index: 2;
	opacity: 0;
	transform-origin: center;
	transform: translate(-50%,-50%);
}
.🔫:checked ~ .🚁 > .💥 {
	animation: boom 0.35s 0.9s 1 linear;
}
@keyframes boom {
	0% {font-size: 0.013333rem;opacity: 0;}
	10%,80% {opacity: 1;}
	100% {font-size: 6.666667rem;opacity: 0;}
}
</style>
<input type="radio" class="🔫"><label class="🚁"><em>🚁</em><span class="💥">💥</span></label>
