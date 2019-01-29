# WZKMiniDouyin-v1.2

迷你抖音，实现基本滑动刷新浏览，点开放大播放暂停，权限申请，视频拍摄、录制、预览、上传

### 
主页面添加了2个可用的btn
@Override
    public void onClick(View v) {
        switch (v.getId()) {
            case R.id.page_message:
                startActivity(new Intent(this, MessageActivity.class));
                break;
            case R.id.btn_add:
                if (ContextCompat.checkSelfPermission(MainActivity.this,
                        Manifest.permission.CAMERA) != PackageManager.PERMISSION_GRANTED
                        || ContextCompat.checkSelfPermission(MainActivity.this,
                        Manifest.permission.RECORD_AUDIO) != PackageManager.PERMISSION_GRANTED
                        ||ContextCompat.checkSelfPermission(MainActivity.this,
                        Manifest.permission.WRITE_EXTERNAL_STORAGE) != PackageManager.PERMISSION_GRANTED) {
                    ActivityCompat.requestPermissions(MainActivity.this,
                            new String[]{Manifest.permission.RECORD_AUDIO, Manifest.permission.CAMERA,
                                    Manifest.permission.WRITE_EXTERNAL_STORAGE},
                            REQUEST_VIDEO_CAPTURE);
                }else{
                    startActivity(new Intent(this,Solution2C2Activity.class));
                }
        }
    }


### 
界面：
### 
![png](https://github.com/peterlong0612/WZKMiniDouyin_V1.2/blob/master/PPT/1ad4aa86325a2c09f4fede770129001.png)
###
![jpg](https://github.com/peterlong0612/WZKMiniDouyin_V1.2/blob/master/PPT/9f0e2bb4b1414f951641f658f575f67.jpg)
###
![png](https://github.com/peterlong0612/WZKMiniDouyin_V1.2/blob/master/PPT/a9dd517b33898c35da92e88315ddfff.png)
###
![png](https://github.com/peterlong0612/WZKMiniDouyin_V1.2/blob/master/PPT/e98b73db59dad5c2bc06b4af429054e.png)

