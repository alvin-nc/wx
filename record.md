   
	Component({
		relations: {
			
		}
	})

# 数据监听器 #
    Component({
		attached: function() {
			this.setData({
				numberA: 1,
				numberB: 2,
			})
		},
		observers: {
			'numberA, numberB': function(numberA, numberB) {
				this.setData({
					sum: numberA + numberB
				})
			}
		}
	})

# 在linux上安装Node.js #
- 下载安装包

    `wget https://nodejs.org/dist/v10.9.0/node-v10.9.0-linux-x64.tar.xz`
- 解压
	
	`tar -xvf node-v10.9.0-linux-x64.tar.xz`
- 设置软链接文件

        ln -s nodejs/bin/npm /usr/local/bin
	    ln -s nodejs/bin/node /usr/local/bin