<!DOCTYPE html>
<html>
<head>
	<title>Full screen Modal</title>
	<style>
		#picture {
			border-radius: 5px;
			cursor: pointer;
			transition: 0.3s;
		}

		#picture:hover {opacity: 0.7s;}

		.modal {
			display: none;
			position: fixed;
			z-index: 1;
			padding-top: 100px;
			left: 0;
			top: 0;
			width: 100%;
			height: 100%;
			overflow: auto;
			background-color: rgb(0,0,0);
			background-color: rgba(0,0,0,0.9);
		}

		.modal-content {
			margin: auto;
			display: block;
			width: 80%;
			max-width: 700px;
			text-align: center;
			color: #ccc;
			padding: 10px 0;
			height: 500px;
		}
		.modal-content,#caption {
			-webkit-animation-name:zoom;
			-webkit-animation-duration:0.6s;
			animation-name:zoom;
			animation-duration:0.6s;

		}
		@-webkit-keyframes zoom {
			from {-webkit-transform: scale(0)}
			to {-webkit-transform: scale(1)}
		}

		@keyframes zoom {
			from {transform: scale(0)}
			to {transform: scale(1)}
		}
		@media only screen and (max-width: 700px) {
			.modal-content {
				width: 100%;

			}
		}

		.close {
			position: absolute;
			top: 15px;
			right: 35px;
			color: #f1f1f1;
			font-size: 50px;
			font-weight: bold;
			transition: 0.3s;

		}
		
		.close:hover;
		.close:focus {
			color: #bbb;
			text-decoration: none;
			cursor: pointer;
		}


	</style>
</head>
<body>
	<img id="picture" src="neet.ntaonline.in_frontend_web_scorecard_index (1)" alt="windows" style="width: 100%; max-width: 300px;">

	<div id="myModal" class="modal">
		<span class="close">&times;</span>
		<img class="modal-content" id="fullPicture">
		<div id="caption"></div>
	</div>

	<script>

		var modal = document.getElementById("myModal");
		var img = document.getElementById("picture");
		var modalImg = document.getElementById("fullPicture");
		var captionText = document.getElementById("caption");

		img.onclick = function() {
			modal.style.display = "block";
			modalImg.src = this.src;
			captionText.innerHTML = this.alt;
		}
		var span = document.getElementsByClassName("close")[0];

		span.onclick = function() {
			modal.style.display = "none";
		}
	</script>

</body>
</html>
