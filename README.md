# CHINAGoogleCDN
360极速/谷歌浏览器,谷歌字体及前端谷歌库国内使用
chrome.webRequest.onBeforeRequest.addListener(
    function(request) {
        var url = request.url.replace('ajax.googleapis.com', 'ajax.c2cmalls.com');
		url = request.url.replace('fonts.googleapis.com/css', 'font.c2cmalls.com');
		url = request.url.replace('fonts.googleapis.com/icon', 'fonts.lug.ustc.edu.cn/icon');
        url = url.replace('themes.googleusercontent.com', 'google-themes.lug.ustc.edu.cn');
        return {redirectUrl: url};
    },
    {
        urls: [
            "*://ajax.googleapis.com/*",
            "*://fonts.googleapis.com/*",
            "*://themes.googleusercontent.com/*"
        ]
    },
    ["blocking"]
);
