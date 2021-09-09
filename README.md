<script src="https://cdn.jsdelivr.net/npm/clipboard@2/dist/clipboard.min.js">
var clipboard = new ClipboardJS('.clip');

//成功した時のイベント
clipboard.on('success', function(e) {
    console.info('Action:', e.action);
    console.info('Text:', e.text);
    console.info('Trigger:', e.trigger);

    e.clearSelection();  //選択範囲解除
});

//エラー時のイベント
clipboard.on('error', function(e) {
    console.error('Action:', e.action);
    console.error('Trigger:', e.trigger);
});
</script>

# MonkeyGitTutorial

<div id="target-div">
    指定したid内の要素をクリップボードへコピーします。
</div>
<button class="clip" data-clipboard-target="#target-div">IDを指定してコピー</button>
