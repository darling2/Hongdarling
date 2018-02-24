<? include $_SERVER[DOCUMENT_ROOT]."/main/header/head.php"; ?>



<script type="text/javascript">
$(function(){
  $('.bx_num1').bxSlider({
		captions: true,
		slideWidth: 900
  });
});
</script>
<style type="text/css">
	.pos_r{position:relative;}
	textarea{width:100%;height:500px;border:none;}
	.bx_num1{overflow:hidden;height:261px;}
	.bx_num1 .bx-caption{position:absolute;bottom:0;left:0;width:100%;padding-left:20px;height:50px;line-height:50px;background:rgba(80, 80, 80, 0.75);}
	.bx_num1 .bx-caption span{color:#fff}
</style>
<div class="pos_r">
	<ul class="bx_num1">
		<li>
			<img src="http://image.hackers.ac/images/china/2017/basic_painting/slide_01.jpg"  title="김지영 선생님 수강후기 " alt="" />
		</li>
		<li>
			<img src="http://image.hackers.ac/images/china/2017/basic_painting/slide_02.jpg"  title="이젠 중국으로 가요" alt="" />
		</li>
		<li>
			<img src="http://image.hackers.ac/images/china/2017/basic_painting/slide_03.jpg"  title="고민할 시간 없어요! 김지영 선생님 수강강의" alt="" />
		</li>
	</ul>
</div>

<textarea>
	<ul class="bx_num1">
		<li>
			<img src="http://image.hackers.ac/images/china/2017/basic_painting/slide_01.jpg"  title="김지영 선생님 수강후기 " alt="" />
		</li>
		<li>
			<img src="http://image.hackers.ac/images/china/2017/basic_painting/slide_02.jpg"  title="이젠 중국으로 가요" alt="" />
		</li>
		<li>
			<img src="http://image.hackers.ac/images/china/2017/basic_painting/slide_03.jpg"  title="고민할 시간 없어요! 김지영 선생님 수강강의" alt="" />
		</li>
	</ul>
</textarea>

