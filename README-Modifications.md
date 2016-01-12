###2.0.1版修改

#####AFSoundQueue.m文件
1. -(void)playItem:(AFSoundItem *)item方法。
修改后，保证音频暂停后重新播放时，timer重新开始

#####AFSoundItem.m文件
1. -(void)fetchMetadata方法。
修改后，不会读取音频的专辑名称、作者等信息，但是还是会获取到音频的时长

#####AFSoundItem.h文件
1. 属性duration和timePlayed的数据类型由NSInteger改为CGFloat。
修改后，读取的音频文件播放时间精度增加。

#####AFSoundRecord.m文件
1. -(id)initWithFilePath:(NSString *)filePath方法。
修改后，设置录音音频的采样率等信息

#####AFSoundPlayback.m文件
1. -(void)setUpItem:(AFSoundItem *)item方法。
修改后，初始化后不会立即播放
