---
layout: post
title: "django项目添加日志（转载）"
date: 2012-06-17 14:38
comments: true
categories: 
- note
---


+ 我用的django的版本是1.3，听闻django可以配置日志模块，不用自己单独写，于是一阵狂搜加看官方文档解决了我的需求。

- 我的需求是需要配置多个日志文件，网上搜出来大部分是一个的，所以给大家一个我的例子做参考。

<!--more-->

1. 在setting.py里面配置如下：

<pre class="prettyprint lang-python">

    LOGGING = {
        'version': 1,
        'disable_existing_loggers': True,
        'formatters': {
            'standard': {
                    'format': '%(levelname)s %(asctime)s %(message)s'
                    },
        },
        'filters': {
        },
        'handlers': {
            'mail_admins': {
                'level': 'ERROR',
                'class': 'django.utils.log.AdminEmailHandler',
                'formatter':'standard',
            },
            'test1_handler': {
                'level':'DEBUG',
                'class':'logging.handlers.RotatingFileHandler',
                'filename':'path1',
                'formatter':'standard',
            },
            'test2_handler': {
                'level':'DEBUG',
                       'class':'logging.handlers.RotatingFileHandler',
                'filename':'path2',
                'formatter':'standard',
            },
        },
        'loggers': {
            'django.request': {
                'handlers': ['mail_admins'],
                'level': 'ERROR',
                'propagate': True,
            },
            'test1':{
                'handlers': ['test1_handler'],
                'level': 'INFO',
                'propagate': False
            },
             'test2':{
                'handlers': ['test2_handler'],
                'level': 'INFO',
                              'propagate': False
            },
        }
    }

</pre>




2. 里面的level什么的可以自己调整，需要几个文件就配几个handler和logger，还是很方面的。用的时候怎么用呢，看下面吧。
3. 在要用log的view.py里面，如果想用test1这个日志，则:

<pre>
log=logging.getLogger('test1')
log.error（“日志内容”） 
</pre>
      


4. 如果，想要在日志内容里面传递变量，怎么办:

        log.error(" %s : execute %s failed",变量1,变量2)，比较像c的printf，还是很方便的










