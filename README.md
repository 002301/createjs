# createjs
createjs 1.0.0
原来的
stage = new createjs.Stage(canvas); 改成
stage = new createjs.StageGL(canvas);
如果需要修改fps
createjs.Ticker.framerate = 60;

注意！！！：矢量对象，滤镜，叠加模式都需要cache后才能使用，一般是加个container后cache（如果会动的需要在tick里每帧cache）。
如果自适应时需要修改canvas的大小，就必须要调用stage.updateViewport(canvas.width,canvas.height)
