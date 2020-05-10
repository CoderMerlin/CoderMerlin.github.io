---
layout: false
---
{% raw %}
<!DOCTYPE HTML>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
	<title>I LOVE YOU</title>
	<meta http-equiv="content-type" content="text/html; charset=UTF-8">
	<style type="text/css">
		@font-face {
			font-family: digit;
			src: url('digital-7_mono.ttf') format("truetype");
		}
	</style>
	<link href="./twojscss/default.css" type="text/css" rel="stylesheet">
	<script type="text/javascript" src="./twojscss/jquery.js"></script>
	<script type="text/javascript" src="./twojscss/garden.js"></script>
    <script type="text/javascript" src="./twojscss/functions.js"></script>
</head>

<body>
	<div id="mainDiv">
		<div id="content">
			<div id="code">
				<span class="comments twocomments">娜：</span><br />
				<span class="space"/><span class="comments"> 当你第一次看到这段话的时候</span><br />
				<span class="space"/><span class="comments"> 也是我鼓起勇气正式向你表白的那天</span><br />
				<span class="space"/><span class="comments"> 很多不同的表白方式，不知在我脑海里模拟了多少遍</span><br />
				<span class="space"/><span class="comments"> 以这样的方式向你告白</span><br />
				<span class="space"/><span class="comments"> 可能更适合我现在的自己（程序员  (..•˘_˘•..) ）</span><br />
				<span class="space comments"/>有很多话想对你说，却不知从何说起~<br />
				<span class="space"/>算了，不管了。说到哪算到哪了<br />
				<span class="space"/>你还记得我与你第一次相识在哪吗？<br />
				<span class="space"/>QQ老乡群，那次我们都要去参加代考，然后加了好友<br />
				<span class="space"/>哈哈，好奇怪，我们竟然以这样的方式相识<br />
				<span class="space"/>初次见你，普普通通的女孩，却又显得格外特别<br />
				<span class="space"/>是温柔？是文雅大方？是自持？是独立？是努力？还是其他？<br />
				<span class="space"/>我不知道，至此心里却又默默有了你的影子<br />
				<span class="space"/>往后有机会我总会跟你聊几句<br />
				<span class="space"/>你还记得我第一次送你U盘上刻的字吗<br />
				<span class="space">明明是想跟你告白，却怂的不敢承认<br />
				<span class="space"/>正如你说的，你会与每个人都保持距离<br />
				<span class="space"/>那时候我也能感觉到，所以我们保持着友情，不再向前一步<br />
				<span class="space"/>毕业后，我以为我们像其他朋友一样，消失在彼此的对话框里<br />
				<span class="space"/>却意外的与你向我借钱断断续续的有着联系<br />
				<span class="space"/>上次得知你还没找男朋友，我却又暗自高兴<br />
				<span class="space"/>我讨厌之前大学那么怂的自己<br />
				<span class="space"/>我幻想过无数个跟你在一起的场景<br />
				<span class="space"/>跟你结婚，跟你生孩子，跟你一起养我们的孩子，跟你白头到老<br />
				<span class="space"/>我不想将来回忆没跟你说我心里的话会后悔<br />
				<span class="space myspance"/>我真的喜欢你！<br /></span> 
				<span class="space myspance"/>我真的喜欢你！<br /></span> 
				<span class="space myspance"/>我真的喜欢你！<br /></span> 
				<span class="space"/>情话是我学的，爱你是真的!</span> <br />
				<br />
			</div>
			<div id="loveHeart">
				<canvas id="garden"></canvas>
				<div id="words">
					<div id="messages">
						娜,我爱你！
							
						<div id="elapseClock"></div>
					</div>
					<div id="loveu">
						Love u forever and ever.<br/>
						<div class="signature">-- 迈</div>
					</div>
				</div>
			</div>
		</div>
	
	</div>
	<script type="text/javascript">
		var offsetX = $("#loveHeart").width() / 2;
		var offsetY = $("#loveHeart").height() / 2 - 55;
		var together = new Date();
		together.setFullYear(2014, 9, 24);
		together.setMinutes(0);
		together.setSeconds(0);
		together.setMilliseconds(0);
		
		if (!document.createElement('canvas').getContext) {
			var msg = document.createElement("div");
			msg.id = "errorMsg";
			msg.innerHTML = "Your browser doesn't support HTML5!<br/>Recommend use Chrome 14+/IE 9+/Firefox 7+/Safari 4+"; 
			document.body.appendChild(msg);
			$("#code").css("display", "none")
			$("#copyright").css("position", "absolute");
			$("#copyright").css("bottom", "10px");
		    document.execCommand("stop");
		} else {
			setTimeout(function () {
				startHeartAnimation();
			}, 5000);

			timeElapse(together);
			setInterval(function () {
				timeElapse(together);
			}, 500);

			//adjustCodePosition();
			$("#code").typewriter();
		}
	
	</script>
</body>
</html>


{% endraw %}