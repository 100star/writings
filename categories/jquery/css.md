# CSS

	$(...).css('background-color');
	$(...).css('backgroundColor'); // same
	$(...).css([ "width", "height" ]);
	
	$(...).css('background-color', '#00ff00');	$(...).css({
		'background-color': '#00ff00',
		'border': '1px solid #000000
	});
	
	$(...).addClass('class1 class2 class3');
	$(...).removeClass('class3');
	$(...).toggleClass('class2');
	
	if ($(...).hasClass('class1')) {...}
	
	$(document).ready(function() {
			num *= 1.4;