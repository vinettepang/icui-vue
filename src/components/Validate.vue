<template>
	<div class="card-header">
		<div class="login-container loginform-fixed">
        <div class="login_logo">
            <a href="/">
                <img src="../assets/images/logo.png" height="54" width="176"></a>
        </div>
        <ul class="login-tab">
            <li class="active"><a>登录</a></li>
            <li><a>注册</a></li>
        </ul> 
        <div class="tab-content">
            <div class="tab-pane active">
                <form id="loginformnew" autocomplete="off" class="loginForm" novalidate="novalidate">
                    <div class="loginform-container">
                        <div class="input-group">
                           <input type="text" name="loginphone" value="" placeholder="请输入邮箱或手机号">
                           <p class="icon-tips"><i class="nc-icon-outline ui-1_check"></i><i class="nc-icon-outline ui-1_simple-remove"></i></p>
                        </div>
                        <div class="input-group">
                            <input type="password" autocomplete="off" name="loginpassword" placeholder="输入密码">
                            <div id="editpw"> <a class="icon-user offpw changeps" id="changeps"></a></div>
                        </div>
                        <div class="login-btn-group">
                           <input type="submit" class="login-btn btn btn-secondary" value="登录">
                            <!-- <input type="submit" id="submitLogin" class="login-btn btn btn-secondary" value="登录" /> -->
                            <a class="login-btn wechat-btn btn" id="wxlogin"><i class="icon-wechat"></i>用微信登录</a> 
                        </div>
                        <a class="ft14" href="/user/findpasswordphone">忘记密码？</a>
                    </div>
                </form>
            </div>
            <div class="tab-pane ">
                <form id="demo" autocomplete="off" class="loginForm" novalidate="novalidate">
                    <div class="loginform-container">
                        <div class="input-group">
                           <input type="text" autocomplete="off" name="nickname" placeholder="昵称 (至少4个字符)">
                           <p class="icon-tips"><i class="nc-icon-outline ui-1_check"></i><i class="nc-icon-outline ui-1_simple-remove"></i></p>
                        </div>
                        <div class="input-group">
                            <input type="text" name="phone" placeholder="手机号" value="">
                            <p class="icon-tips"><i class="nc-icon-outline ui-1_check"></i><i class="nc-icon-outline ui-1_simple-remove"></i></p>
                        </div>
                        <div class="input-group">
                            <input type="text" name="verify" value="" placeholder="" autocomplete="off">
                            <img class="verifyimg reloadverify" alt="点击切换" src="/User/verify" style="cursor:pointer;">
                            <div class="verifyimgtip">
                                <i class="tiptri"></i>看不清？换一张</div>
                        </div>
                        <div class="input-group">
                            <input type="text" autocomplete="off" name="phoneverify" placeholder="验证码">
                            <a class="sendverify phoneverify">发送验证码</a>
                                <!-- <img  class="verifyimg reloadverify" alt="点击切换" src="/User/verify" style="cursor:pointer;"> -->
                        </div>
                        <div class="input-group">
                            <input type="password" autocomplete="off" name="password" placeholder="设置密码">
                            <div id="editpw"> <a class="icon-user offpw changeps" id="changeps"></a></div>
                        </div>
                        <div class="login-btn-group">
                            <input type="submit" class="login-btn btn btn-secondary" value="注册">
                        </div>
                       <!--  <input type="submit" id="submitReg" class="login-btn btn btn-secondary" value="注册" /> -->
                        <a class="ft14 tab-to-login">已有帐号？</a>
                    </div>
                </form>
            </div>
        </div>
        
    </div>
	</div>
</template>
<style type="text/css">
	body{
       /* background-color: #ffd733;*/
    }
	    /* override */
    .fancybox-wrap{
        width: auto !important;
    }
    .fancybox-skin{
        padding: 0 !important;
    }
   .login_logo{

        text-align: center;
        margin-bottom: 10px;
    }
    .login_logo img{
        max-width: 86px;
    }
    span.tip-light i{
       /* background-image: url('../images/tip-light.png');*/
        width: 12px;
        height: 18px;
        background-size: 12px 18px;
        display: inline-block;
    }
    span.tip-light{
        padding-right: 15px;
    }
    p.reg-tip{
        padding: 18px 22px 23px 22px;
        background: #F6EBD6;
    }
    .tab-content > .active {
        display: block !important;
    }
    .tab-content > .tab-pane {
        display: none;
    }
    input : -webkit-autofill {
        -webkit-box-shadow : 0 0 0px 1000px white inset ;
        border : 1px solid #CCC !important ;
    }
    input : -webkit-autofill {
    -webkit-box-shadow : 0 0 0px 1000px white inset ;
    border : 1px solid #CCC !important ;
    height : 27px !important ;
    line-height : 27px !important ;
    border-radius : 0 4px 4px 0 ;
    }
    .login-container{
        margin: 0 auto;
        width: 460px;
        min-height: 666px;
        box-sizing: border-box;
        padding: 45px 59px 72px 59px; 
        background: #fff;
        box-shadow: 0 0 4px 0 rgba(74,73,74,0.30);
        border-radius: 6px;
    }
    .login-container .active{
        background: none;
    }
    form.loginForm .loginform-container{
        box-sizing: border-box;
    }
    form.loginForm .loginform-container .input-group{
        display: block;
        position: relative;
        margin: 0;
    }
    form.loginForm .loginform-container .input-group .sendverify{
        outline: 0;
        border: none;
        font-size: 14px;
        color: #482929;
        background-color: #fff;
        position: absolute;
        top:15px;
        right:20px;
    }
    form.loginForm .loginform-container .input-group .sendverify.grey{
        background-color: #fff;
        color: #666;

    }
    form.loginForm .loginform-container .input-group:last-child{
        margin:0 0 40px 0 !important;
    }
    form.loginForm .loginform-container .input-group .verifyimg {
        position: absolute;
        top: 10px;
        right: 12px;
        max-width: 120px;
    }
    .verifyimgtip {
    display: none;
    position: absolute;
    top: -60px;
    right: 0;
    z-index: 999;
    width: 130px;
    text-align: center;
    line-height: 45px;
    height: 45px;
    color: #fff;
    font-size: 14px;
    opacity: 0.9;
    background-color: #6f3400;
    border-radius: 2px;
}
.verifyimgtip .tiptri {
    position: absolute;
    width: 0;
    height: 0;
    border-left: 8px solid transparent;
    border-right: 8px solid transparent;
    border-top: 8px solid #6f3400;
    bottom: -8px;
    left: 50%;
    margin-left: -4px;
}
    form.loginForm .loginform-container .input-group input[type=text],.loginform-container .input-group input[type=password]{
            transition: border 0.2s ease-in 0s;
                outline: none;
                    width: 340px;
    padding: 6px 25px;
        border-radius: 0;
        border: none;
        height: 50px;
        box-sizing: border-box;
        font-size: 14px;
        background-color: #fff !important;
        border-bottom: 1px solid #E5E5E5;
        margin: 0;
    }
    form.loginForm .loginform-container .input-group input[type=text].right,.loginform-container .input-group input[type=password].right{
        border-bottom: 1px solid #FFD733;
    }
    form.loginForm .loginform-container .input-group input[type=text].false,.loginform-container .input-group input[type=password].false{
        border-bottom: 1px solid #C60000;
    }
    .cb-green{
        color: green !important;
    }
    .login-tab{
        padding: 0 20px;
    }
    .login-tab li:nth-child(1){
        margin-right: 115px;
    }
    .login-tab li{
        display: inline;
    }
    .login-tab li a{
        font-size: 18px;
        text-align: center;
        color: #B89D86;
        line-height: 57px;
        display: inline-block;
        width: 90px;
        height: 57px;
    }
    .login-tab li.active a{
        color: #482929;
        border-bottom: 3px solid #FFD733;
    }
    .false .icon-tips,.right .icon-tips{
        display: block;
    }
    .false .icon-tips i.ui-1_simple-remove{
        display: block;
        width: 18px;
        height:18px;
        overflow: hidden;
    }
    .right .icon-tips i.ui-1_check{
        display: block;
        width: 18px;
        height:18px;
        overflow: hidden;
    }
    .icon-tips {
        display: none;
        position: absolute;
        top:15px;
        right:20px;
        width: 17px;
        height: 20px;
        overflow: hidden;
    }
    .icon-tips  i{
        width: 18px;
        height:18px;
        overflow: hidden;
        display: none;
        font-size: 18px;
    }
    /*设置默认的错误提示的样式*/
    .prompot {
        margin-left: 115px;
        max-width: 485px;
        clear: both;
    }
    .false span.false{
        font-size: 14px;
        display: block;
        padding: 8px 0 12px 20px;
    }
    .cb-error {
        display: none;
        color: #C60000;
        font-size: 14px;
        padding: 8px 0 12px 20px;
    }
    .false {
        color: #C60000;
    }
    .right {
        color: #FFD733;
    }
    input.false {
        border: 1px solid #C60000;
    }
    input.right {
        border: 1px solid green;
    }
    input:-webkit-autofill, textarea:-webkit-autofill, select:-webkit-autofill {
        -webkit-box-shadow: 0 0 0px 1000px #fff inset; color:#482929;
        background-color: #fff !important;
        background-image: none;
        color: rgb(0, 0, 0);
    }

    .login-btn{
        box-sizing: border-box;
        width: 100% !important;
        color: #482929;
        padding-top: 14px !important;
        padding-bottom: 14px !important;
        margin: 0 0 14px 0;
        font-size: 16px !important;
    }
    .login-btn-group{
        margin-top: 40px;
    }

    .loginform-fixed{
        /*position: fixed;
        top:50%;
        left:50%;
        margin-top: -333px !important;
        margin-left: -230px !important;*/
    }
    .login-tab.center{
        text-align: center;
    }
    .login-tab.center li{
        margin: 0 !important;
    }

    #editpw,
#editpww{ position:absolute; right:10px; top:4px;}
#editpw a,
#editpww a{display:block; width:40px; height:40px;}
#editpw a:hover,
#editpww a:hover{color: #333; }
#editpw .onpw:before,
#editpww .onpw:before{ content: "\ed07";font-size: 27px;position: absolute;right: -12px;top: 7px;/*background:url(../images/icopw.png) center -74px no-repeat;*/}
#editpw .offpw:before,
#editpww .offpw:before{ content: "\ed09";font-size: 27px;position: absolute;right: -12px;top: 7px;/*background:url(../images/icopw.png) center 12px no-repeat;*/}

</style>
<script type="text/javascript">
	
  $(function() {
  	  $('.loginpop').click(function(event) {
    var type = $(this).attr('data-type');
    if (type == 'reg') {
      $('.login-tab li').eq(1).addClass("active").siblings().removeClass("active");
      $(".login-container .tab-pane").eq(1).addClass("active").siblings().removeClass("active");
    } else if (type == 'log') {
      $('.login-tab li').eq(0).addClass("active").siblings().removeClass("active");
      $(".login-container .tab-pane").eq(0).addClass("active").siblings().removeClass("active");
    }
  });
$('.login-tab li').click(function() {
    $(this).addClass("active").siblings().removeClass("active");
    $(".login-container .tab-pane").eq($('.login-tab li').index(this)).addClass("active").siblings().removeClass("active")
  });
  $('.tab-to-login').click(function(event) {
    $('.login-tab li:first-child').addClass("active").siblings().removeClass("active");
    $(".login-container .tab-pane:first-child").addClass("active").siblings().removeClass("active");
  });
    jQuery.validator.addMethod("byteRangeLength", function(value, element, param) {
        var length = value.length;
        for (var i = 0; i < value.length; i++) {
            if (value.charCodeAt(i) > 127) {
                length++;
            }
        }
        return this.optional(element) || (length >= param[0] && length <= param[1]);
    }, $.validator.format("请确保输入的值在{0}-{1}个字节之间(一个中文字算2个字节)"));
    jQuery.validator.addMethod('phone', function(value, element) {
        //var telmatch = /^1[0-9]{10}$/;
        var telmatch = /^(13[0-9]{9})|(18[0-9]{9})|(14[0-9]{9})|(17[0-9]{9})|(15[0-9]{9})$/;
        return this.optional(element) || (telmatch.test(value));
    }, '请输入正确的手机号码');

    jQuery.validator.addMethod('loginphone', function(value, element) {
        var telmatch = /^(13[0-9]{9})|(18[0-9]{9})|(14[0-9]{9})|(17[0-9]{9})|(15[0-9]{9})$/;
        var emailreg = /^\w+((-\w+)|(\.\w+))*\@[A-Za-z0-9]+((\.|-)[A-Za-z0-9]+)*\.[A-Za-z0-9]+$/;
        return this.optional(element) || (telmatch.test(value)) || (emailreg.test(value));
    }, '请输入正确的手机号码或邮箱');

    $('#demo').validate({
        errorElement: 'span',
        errorClass: 'false',
        validClass: 'right',
        // onsubmit:function(element){    
        //     $(element).valid();
        // },
        //onkeyup: function(element){
        onkeyout: function(element) {
            $(element).valid();
        },
        errorPlacement: function(error, element) {
            element.parent().append(error);
        },
        highlight: function(element, errorClass, validClass) {
            $(element).removeClass('right').addClass('false');
            $(element).parent().removeClass('right').addClass('false').find('i').html('&#xe606;');
        },
        success: function(span) {
            span.parent().removeClass('false').addClass('right');
            span.prev('.iconfont').html('&#xe607;');
        },
        rules: {
            nickname: {
                required: true,
                //minlength: 4,
                //maxlength: 10
                remote: {
                    url: "/User/checknickname",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'nickname': function() {
                            return $('input[name="nickname"]').val();
                        }
                    }
                },
                byteRangeLength: [4, 10]

            },
            password: {
                required: true,
                minlength: 8,
                maxlength: 16
            },
            phone: {
                required: true,
                phone: true,
                minlength: 11,
                maxlength: 11,
                //isphoneexist: '/User/checkphonenum',
                remote: {
                    url: "/User/checkphonenum",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'phone': function() {
                            return $('input[name="phone"]').val();
                        }
                    }
                },
                digits: true
            },
            verify: {
                required: true,
                // maxlength: 4,
                remote: {
                    url: "/User/checkverify",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'verify': function() {
                            return $('input[name="verify"]').val();
                        }
                    }
                }

            },
            phoneverify: {
                required: true,
                // maxlength: 4,
                remote: {
                    url: "/User/checkphonecerify",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'phoneverify': function() {
                            return $('input[name="phoneverify"]').val();
                        }
                    }
                }

            }

        },
        messages: {
            nickname: {
                required: '请设置一个用户名',
                remote: '昵称已被注册',
                //minlength: '请输入2-5个汉字（4-10个字母）',
                byteRangeLength: '请输入2-5个汉字(4-10个字母)'
                    // maxlength: '请输入4-10个字符'
            },
            password: {
                required: '请设置一个密码',
                minlength: '密码长度不小于8个字符',
                maxlength: '密码长度不大于16个字符'
            },
            phone: {
                remote: '手机号已存在',
                required: '请输入您的常用手机号码',
                minlength: '手机号码长度为11位',
                maxlength: '手机号码长度为11位',
                digits: '手机号码只能输入数字'
            },
            verify: {
                required: '请输入验证码',
                //maxlength:'max 4',
                remote: '验证码输入错误'
            },
            phoneverify: {
                required: '请输入验证码',
                //maxlength:'max 4',
                remote: '验证码输入错误'
            }
        },
        submitHandler: function(a) {
            var c = $('input[name="nickname"]', a).val(),
                d = $('input[name="password"]', a).val(),
                e = $('input[name="phone"]', a).val(),
                f = $('input[name="verify"]', a).val(),
                g = $('input[name="phoneverify"]', a).val(),
                recommend_link = window.location.href;
            $(a).find(":submit").val("注册中...").attr("disabled", !0),
            $.ajax({
                url: ctx + "User/registerphonenew",
                type: "post",
                data: {
                    nickname: c,
                    password: d,
                    phone: e,
                    verify: f,
                    phoneverify: g,
                    recommend_link: recommend_link,
                },
                dataType: "json"
            }).done(function(data) {
                if (data.status) {
                    $('.fancybox-close').click();
                    if (window.location.href.indexOf('user/register') != -1 ) {   
                        location.href = data.url;
                    }else{
                        location.reload();
                    } 
                } else {
                    $('input[type="submit"]').attr("disabled", false);
                    $('input[type="submit"]').val('注册');
                    $('#reg-cb-error').css('display', 'block').text(data.error);
                    $(".verifyimg").click();
                }
            })
        }
    });

    $('#loginformnew').validate({
        errorElement: 'span',
        errorClass: 'false',
        validClass: 'right',
        //onkeyup: function(element){
        onkeyout: function(element) {
            $(element).valid();
        },
        //  onsubmit:function(element){    
        //     $(element).valid();
        // },
        errorPlacement: function(error, element) {
            element.parent().append(error);
        },
        highlight: function(element, errorClass, validClass) {
            $(element).removeClass('right').addClass('false');
            $(element).parent().removeClass('right').addClass('false').find('i').html('&#xe606;');
        },
        success: function(span) {
            span.parent().removeClass('false').addClass('right');
            span.prev('.iconfont').html('&#xe607;');
        },
        rules: {
            loginphone: {
                required: true,
                loginphone: true,
                remote: {
                    url: "/User/logincheckphone",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'loginphone': function() {
                            return $('input[name="loginphone"]').val();
                        }
                    }
                }
            },
            loginpassword: {
                required: true,
                remote: {
                    url: "/User/logincheckpw",
                    data: {
                        loginphone: function() {
                            return $('input[name="loginphone"]').val();
                        },
                        loginpassword: function() {
                            return $('input[name="loginpassword"]').val();
                        }
                    },
                    type: "post",
                    dataType: 'json'
                }
            }

        },
        messages: {
            loginphone: {
                required: '请输入手机或邮箱',
                loginphone: '请输入正确的手机或邮箱',
                remote: '手机号或邮箱不存在'
            },
            loginpassword: {
                required: '请输入密码',
                remote: '密码输入错误'
            }
        },
        submitHandler: function(a) {

            var c = $('input[name="loginphone"]', a).val(),
                d = $('input[name="loginpassword"]', a).val();
            $(a).find(":submit").val("登录中...").attr("disabled", !0),
                $.ajax({
                    url: ctx + "User/loginphonenew",
                    type: "post",
                    data: {
                        nickname: c,
                        password: d,
                    },
                    dataType: "json"
                }).done(function(data) {
                    console.log(data);
                    if (data.status) {
                        $('.fancybox-close').click();
                        location.reload();

                    } else {
                        $('input[type="submit"]').attr("disabled", false);
                        $('input[type="submit"]').val('登录');
                        $('#login-cb-error').css('display', 'block').text(data.info);
                        $(".verifyimg").click();
                    }
                })
        }
    });

    $('#logWechatPhoneForm').validate({
        errorElement: 'span',
        errorClass: 'false',
        validClass: 'right',
        //onkeyup: function(element){
        onkeyout: function(element) {
            $(element).valid();
        },
        errorPlacement: function(error, element) {
            element.parent().append(error);
        },
        highlight: function(element, errorClass, validClass) {
            $(element).removeClass('right').addClass('false');
            $(element).parent().removeClass('right').addClass('false').find('i').html('&#xe606;');
        },
        success: function(span) {
            span.parent().removeClass('false').addClass('right');
            span.prev('.iconfont').html('&#xe607;');
        },
        rules: {
            password: {
                required: true,
                minlength: 8,
                maxlength: 16
            },
            phone: {
                // remote:{
                //     url: "/User/loginwechatcheckphone",
                //     type: "post",
                //     dataType: 'json',
                //     data: {
                //         'phone': function(){return $('input[name="phone"]').val();}
                //     }
                // },
                required: true,
                minlength: 11,
                maxlength: 11

            },
            verify: {
                //required: true,
                // maxlength: 4,
                //remote:{
                // url: "/User/checkverify"
                // type: "get",
                // dataType: 'json',
                // data: {
                //     'verify': function(){return $('input[name="verify"]:checked').val();}
                // }
                //}

            }

        },
        messages: {

            password: {
                required: '请设置一个密码',
                minlength: '密码长度不小于8个字符',
                maxlength: '密码长度不大于16个字符'
            },
            phone: {
                //  remote:'你的账号已绑定了其它微信号，请确认用户名',
                required: '请输入您的常用手机号码',
                minlength: '手机号码长度为11位',
                maxlength: '手机号码长度为11位',
                digits: '手机号码只能输入数字'
            },
            verify: {
                required: '请输入验证码',
                //maxlength:'max 4',
                remote: '验证码输入错误'
            }
        },
        submitHandler: function(a) {
            var
                d = $('input[name="password"]', a).val(),
                e = $('input[name="phone"]', a).val();
            // f = $('input[name="verify"]', a).val(),
            // g = $('input[name="phoneverify"]', a).val();
            $(a).find(":submit").val("登录中...").attr("disabled", !0),
                $.ajax({
                    url: ctx + "User/loginwechat",
                    type: "post",
                    data: {
                        // nickname: c,
                        password: d,
                        phone: e,
                        // verify: f,
                        // phoneverify: g,
                    },
                    dataType: "json"
                }).done(function(data) {
                    if (data.status) {
                        //console.log(data);
                        window.location.href = ctx + data.url
                        $('#reg-cb-error').css('display', 'none').text(data.info);
                    } else {
                        $('input[type="submit"]').attr("disabled", false);
                        $('input[type="submit"]').val('登录');
                        $('#reg-cb-error').css('display', 'block').text(data.info);
                        $(".verifyimg").click();
                        $('#logWechatPhoneForm .false').css('display', 'none');
                    }
                    //window.location.href = ctx + data.url
                    console.log(data);

                })
        }
    });

    $('#boundphone').validate({
        errorElement: 'span',
        errorClass: 'false',
        validClass: 'right',

        onkeyout: function(element) {
            $(element).valid();
        },
        errorPlacement: function(error, element) {
            element.parent().append(error);
        },
        highlight: function(element, errorClass, validClass) {
            $(element).removeClass('right').addClass('false');
            $(element).parent().removeClass('right').addClass('false').find('i').html('&#xe606;');
        },
        success: function(span) {
            span.parent().removeClass('false').addClass('right');
            span.prev('.iconfont').html('&#xe607;');
        },
        rules: {
            boundphone: {
                required: true,
                phone: true,
                minlength: 11,
                maxlength: 11,
                //isphoneexist: '/User/checkphonenum',
                remote: {
                    url: "/User/checkphonenum",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'phone': function() {
                            return $('input[name="boundphone"]').val();
                        }
                    }
                }
            },
            boundverify: {
                required: true,
                // maxlength: 4,
                remote: {
                    url: "/User/checkverify",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'verify': function() {
                            return $('input[name="boundverify"]').val();
                        }
                    }
                }

            },
            boundphoneverify: {
                required: true,
                // maxlength: 4,
                remote: {
                    url: "/User/checkphonecerify",
                    type: "post",
                    dataType: 'json',
                    data: {
                        'phoneverify': function() {
                            return $('input[name="boundphoneverify"]').val();
                        }
                    }
                }
            }
        },
        messages: {
            boundphone: {
                //remote:'手机号已存在',
                required: '请输入您的常用手机号码',
                minlength: '手机号码长度为11位',
                maxlength: '手机号码长度为11位',
                digits: '手机号码只能输入数字',
                remote: '该手机号已经被绑定'
            },
            boundverify: {
                required: '请输入验证码',
                //maxlength:'max 4',
                remote: '验证码输入错误'
            },
            boundphoneverify: {
                required: '请输入验证码',
                //maxlength:'max 4',
                remote: '验证码输入错误'
            }
        },
        submitHandler: function(a) {
            var e = $('input[name="boundphone"]', a).val(),
                f = $('input[name="boundverify"]', a).val(),
                g = $('input[name="boundphoneverify"]', a).val();
            $(a).find(":submit").val("绑定中...").attr("disabled", !0),
                $.ajax({
                    url: ctx + "User/boundUserPhone",
                    type: "post",
                    data: {
                        phone: e,
                        verify: f,
                        phoneverify: g,
                    },
                    dataType: "json"
                }).done(function(data) {
                    if (data.status) {
                        $.fancybox.close();
                        $('.fancybox-close').click();
                        $('#bindingPhone').text(data.phone);
                        //  location.reload();
                        if (data.type == '1') {
                            $('.setting-pop').fadeIn().find('span').text('绑定成功');
                        } else {
                            $('.setting-pop').fadeIn().find('span').text('保存成功');
                        }
                        setTimeout("$('.setting-pop').fadeOut()", 1500);
                        $('#boundphone')[0].reset();
                        $('#boundphone .loginform-container').children().removeClass('right');
                        $('#boundphone .input-group').children().removeClass('right');
                        $('input[type="submit"]').attr("disabled", false);
                        $('input[type="submit"]').val('绑定');
                        $('#reg-cb-error').css('display', 'none').text(data.error);
                    } else {
                        $('input[type="submit"]').attr("disabled", false);
                        $('input[type="submit"]').val('绑定');
                        $('#reg-cb-error').css('display', 'block').text(data.error);
                        $(".verifyimg").click();
                    }

                })
        }
    });

})
</script>