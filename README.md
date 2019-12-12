# FGamePixel
FillAmeaPixel - Core 2.0
# FPixelGame

由于PocketMine-MP支持的原版特性实在是太少了
又考虑到FillAmePixel-Core是基于GenisysPro的,一切都
太烂了，所以我们开发了这个版本，它是一个全新的构架，
主目录为fpixelgame\


# FillAmeaPixel
下一个PocketMine，代号FPixelGame

# 核心架设
FPixelGame分为PocketGroup和fpixelgame两部分。PocketGroup将不同的客户端数据储存为txt数据，用于群组系统；fpixelgame server处理群组信息，并实现游戏逻辑。PocketGroup用来运行动态数据转发和处理分配。同时PocketGroup通过FPixelGame，从本地服务器上收集信息并上传至MYSQL，实现静态资源的调配；同时利用配置文件实现群组系统的分配

## 预设处理
支持批量发送







## GameServer 群组架设
IP: 0.0.0.0
port:8888
LobbyServer: true


## NewAPI
核心分为API，Event，Function三个部分，所有调用都在API，扩展功能都在Function


## 启动服务器
```php
// Start Server
namespace fpixelgame;
use fpixelgame\Server\Server;

class FPixelGame{
const NAME = FillAmeaPixelGame

public function start{


	$this->logger->info("Saving levels...");

		foreach($this->levels as $level){
			$level->save();
		}

		$this->pluginManager->disablePlugins();
		$this->pluginManager->clearPlugins();
		$this->commandMap->clearCommands();

		$this->logger->info("Reloading properties...");
		$this->properties->reload();
		$this->advancedConfig->reload();
		$this->loadAdvancedConfig();
		$this->maxPlayers = $this->getConfigInt("max-players", 2019);

		if($this->getConfigBoolean("hardcore", false) === true and $this->getDifficulty() < 3){
			$this->setConfigInt("difficulty", 3);

}

```

# 预增功能
##1.FWorldAdmin-世界管理
##2.MoneyAPI-经济组件
##3.RedStoneAPI-红石全特性
##4.BossBarAPI-血条组件
##5.GUIAPI-弹窗组件
##6.FMusicAPI-红石音乐
##7.GameNPCAPI-小游戏接口


## 开发团队
本项目由FillAmeaPixelNetWork直接进行开发
如果你想参与这个项目
你需要安装PHP、PHPStorm以及适合开发PHP的IDE。


如果你支持，点个星标吧
