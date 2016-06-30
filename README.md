## install
- clone the code and enter the folder
- python install setup.py
- or you can directly place the pisces into your project.


## example

    # -*- coding: utf-8 -*-
    from pisces.main import main

    if __name__ == '__main__':
        # image search keyword: kitchen fire
        url = 'https://www.google.com/search?safe=strict&hl=zh-CN&site=imghp&tbm=isch&source=hp&biw=1372&bih=661&q=%E7%81%AB%E7%81%BE&oq=%E7%81%AB%E7%81%BE&gs_l=img.3...1527.6030.0.6271.25.13.7.0.0.0.333.333.3-1.1.0....0...1ac.1j4.64.img..18.7.33...0.m7j-m12CPV0'
        # if you are in china, use the url below instand, unless you're using VPN
        # url = 'http://image.baidu.com/search/index?tn=baiduimage&ipn=r&ct=201326592&cl=2&lm=-1&st=-1&fm=result&fr=&sf=1&fmq=&pv=&ic=0&nc=1&z=&se=&showtab=0&fb=0&width=&height=&face=0&istype=2&ie=utf-8&word=%E7%81%AB%E7%81%BE'

        output_dir = '/tmp/output_fire/'

        main(url, output_dir, image_count=200, quiet=False, close=True, browser='firefox')
        # similar to the below:
        # main(url, output_dir)

## tip
- The code uses selenuim. Selenium Python bindings provides a simple API to write functional/acceptance tests using Selenium WebDriver. More info to see http://selenium-python.readthedocs.io/installation.html
- default browser is firefox;
- tools/chromedriver is only for chrome, to see http://chromedriver.storage.googleapis.com/index.html for more info.
- browser safari/IE/opera may not work if you don't have any support
- I recommend to use the default browser - firefox.
