        
#### 小程序可写在app.js判断场景值，小游戏可写在loading登录时判断场景值。其中1023，安卓系统桌面图标；其中1104，IOS的微信聊天主界面下拉，“我的小程序”栏

        /**
        * 当小程序启动，或从后台进入前台显示，会触发 onShow
        */
        onShow: function (options) {
            console.log(options);
            this.scene = options.scene;
        },


#### 判断程序是Android，IOS运行平台

        isAndroidOrIos() { //判断运行平台
            var sUserAgent = window.navigator.userAgent.toLowerCase();
            var bIsAndroid = sUserAgent.match(/android/i) == "android";
            var bIsIphoneOs = sUserAgent.match(/iphone os/i) == "iphone os";
            window.bIsAndroid = 0;
            if (bIsAndroid) {
                window.bIsAndroid = 1;
                return;
            }
        },
        