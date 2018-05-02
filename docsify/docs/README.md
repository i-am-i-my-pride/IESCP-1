# IESCP

`IESCP`，全称为`ISoftstone Enterprise Service Cloud Platform`，软通企业服务云平台。是软通动力保险事业部专门开发的一套j2ee应用开发平台，支持传统的B/S架构，以及分布式架构。从前端、中间接入层，到后端，专门针对保险业务场景进行优化，能更好的满足于保险行业系统对快速、稳定、高效、安全的要求

## 菜单栏配置

菜单栏直接通过后台配置，通过 `method:menuAction.getMenuData` 返回给前台，即可自动加载菜单栏，返回的数据格式如下：

```JSON
{
	"status": "0",
	"data": {
		"menuList": [ {
			"label" : "UI示例",
			"url" : "",
			"icon" : "",
			"subMenu" : [ {
				"label" : "列表示例",
				"url" : "page/demo/demo-list.html",
				"icon" : "",
				"subMenu" : []
			}, {
				"label" : "表单示例",
				"url" : "page/demo/demo-form.html",
				"icon" : "",
				"subMenu" : []
			}, {
				"label" : "选项卡示例",
				"url" : "page/demo/demo-tabs.html",
				"icon" : "",
				"subMenu" : []
	  		} ]
	  	}, {
			"label" : "服务管理",
			"url" : "",
			"icon" : "",
			"subMenu" : [  {
				"label" : "服务机构管理",
				"url" : "page/health/service-dpt.html",
				"icon" : "",
				"subMenu" : []
		  	}, {
				"label" : "服务项目管理",
				"url" : "page/health/service-proj.html",
				"icon" : "",
				"subMenu" : []
		  	} ]
	  	}, {
			"label" : "客户管理",
			"url" : "",
			"icon" : "",
			"subMenu" : [ {
				"label" : "客户服务管理",
				"url" : "page/health/cus-service.html",
				"icon" : "",
				"subMenu" : []
		  	}, {
				"label" : "客户挂号记录",
				"url" : "page/health/cus-register.html",
				"icon" : "",
				"subMenu" : []
		  	}, {
		  		"label" : "客户二次诊断",
		  		"url" : "page/health/cus-second.html",
		  		"icon" : "",
		  		"subMenu" : []
		  	}, {
		  		"label" : "客户体检",
		  		"url" : "page/health/cus-inspect.html",
		  		"icon" : "",
		  		"subMenu" : []
		  	}, {
		  		"label" : "客户问诊记录",
		  		"url" : "page/health/cus-inquiry.html",
		  		"icon" : "",
		  		"subMenu" : []
		  	}, {
		  		"label" : "客户重疾绿通记录",
		  		"url" : "page/health/cus-stricken.html",
		  		"icon" : "",
		  		"subMenu" : []
		  	}, {
		  		"label" : "客户海外转诊",
		  		"url" : "page/health/cus-abroad.html",
		  		"icon" : "",
		  		"subMenu" : []
		  	} ]
	  	}, {
	  		"label" : "合约管理",
	  		"url" : "",
	  		"icon" : "",
	  		"subMenu" : [ {
		  		"label" : "合约管理",
		  		"url" : "page/health/contract.html",
		  		"icon" : "",
		  		"subMenu" : []
		  	} ]
	  	}, {
	  		"label" : "洁牙管理",
	  		"url" : "",
	  		"icon" : "",
	  		"subMenu" : [ {
	  			"label" : "洁牙管理",
	  			"url" : "page/health/card.html",
	  			"icon" : "",
	  			"subMenu" : []
	  		} ]
	  	}, {
	  		"label" : "系统设置",
	  		"url" : "",
	  		"icon" : "",
	  		"subMenu" : [ {
	  			"label" : "个人资料",
	  			"url" : "page/info.html",
	  			"icon" : "",
	  			"subMenu" : []
	  		} ]
	  	} ]
	}
}
```

* [效果]()

## iss-panel面板组件

>示例1 | 带标题

* 代码

```HTML
<div v-cloak id="pageDiv">
	<div is="iss-panel" title="带标题面板"></div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-panel1.html)

>示例2 | 不带标题

* 代码

```HTML
<div v-cloak id="pageDiv">
	<div is="iss-panel" title=" "></div> //注意title里面是空格
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-panel2.html)

>示例3 | 副标题区的使用

* 代码

```HTML
<div v-cloak id="pageDiv">
	<div is="iss-panel" title="副标题区的使用">
		<i slot="subtitle" style="font-style:normal;">| 副标题</i>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-panel3.html)

>示例4 | 脚注区的使用

* 代码

```HTML
<div v-cloak id="pageDiv">
	<div is="iss-panel" title="脚注区的使用">
		<div slot="footer">脚注区</div>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-panel4.html)

## iss-card卡片组件

>示例1 | 带标题

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="查询条件"></div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-card1.html)

>示例2 | 不带标题

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title=" "></div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-card2.html)

>示例3 | 副标题区的使用

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="查询条件">
	    <i slot="subtitle" style="font-style:normal;">| 副标题</i>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-card3.html)

>示例4 | 脚注区的使用

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="脚注区的使用">		
		<div slot="footer">脚注区</div>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-card4.html)

## iss-radio单选组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-radio">
		<input is="iss-radio" :datasource="[{CCde:'1', CCnm:'公司'},{CCde:'2', CCnm:'个人'},{CCde:'3', CCnm:'其他'}]"/>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-radio.html)

## iss-checkbox复选组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-checkbox">
		<input is="iss-checkbox" title="车损" value="car" />
		<input is="iss-checkbox" title="物损" value="prop" />
		<input is="iss-checkbox" title="人伤" value="person" />
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-checkbox.html)

## iss-tag标签组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-tag">
		<input is="iss-tag" title="标签组件" value="car" />
		<input is="iss-tag" title="标签组件fly" value="fly" />
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-tag.html)

## iss-date日期组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-date">
		<table is="iss-form">
			<tr>
				<td style="width: 120px;">年月日时分秒</td>
				<td><input is="iss-date" dateFmt="yyyy-MM-dd HH:mm:ss" /></td>
				<td style="width: 120px;">年月日</td>
				<td><input is="iss-date" dateFmt="yyyy-MM-dd" /></td>
				<td style="width: 120px;">时分秒</td>
				<td><input is="iss-date" dateFmt="HH:mm:ss" /></td>
			</tr>
		</table>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-date.html)

## iss-switch开关组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-switch">
		<table is="iss-form" ref="vFilter">
			<tr>
				<td style="width: 120px;">默认是否</td>
				<td><input is="iss-switch"  v-model="filter.DStatus" /></td>
				<td style="width: 120px;">自定义</td>
				<td><input is="iss-switch" :datasource="dict.teethCardStatus" v-model="filter.CStatus" /></td>
			</tr>
		</table>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-switch.html)

## iss-img图片组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-img">
		<table is="iss-form" ref="vFilter">
			<tr>
				<td style="width: 120px;">图片</td>
				<td><input is="iss-img" style="width:40px;height:40px;border: 0px;" v-model="DStatus"  @click="uploadIcon"/></td>
			</tr>
		</table>
	</div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					DStatus: ""
				},
				mounted: function () {},
				methods: {}
			});
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-img.html)

## iss-link链接组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-link">
		<table is="iss-form">
			<tr>
				<td style="width: 120px;">链接</td>
				<td><input is="iss-link" v-model="filter.DStatus" value="这是个链接" @click="alert('click')"></td>
			</tr>
		</table>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-link.html)

## iss-btn按钮组件

>示例1 | 小按钮类型

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div >
		<input is="iss-btn" type="append" value="我是增加按钮" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="view" value="查看" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="update" value="修改" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="remove" value="删除" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="set" value="设置" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="release" value="启用" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="cancelrelease" value="禁用" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="relate" value="关联" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="relateCancel" value="取消关联" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="pause" value="暂停" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="restart" value="重启" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="common" value="通用小按钮" @click="layer.warn('按钮组件')"/>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-btn1.html)

>示例2 | 大按钮类型

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div >
		<input is="iss-btn" type="query" value="查询" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="reset" value="重置" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="insert" value="增加" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="save" value="保存" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="submit" value="提交" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="delete" value="删除" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="modify" value="修改" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="pass" value="允许/审核通过" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="nopass" value="拒绝/审核不通过" @click="layer.warn('按钮组件')"/>
		<input is="iss-btn" type="base" value="通用大按钮" @click="layer.warn('按钮组件')"/>
	</div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-btn2.html)

## iss-input输入框组件

>示例

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-input">
		<table is="iss-form" ref="vFilter">
			<tr>
				<td style="width: 120px;">单行</td>
				<td><input is="iss-input" v-model="CStatus" /></td>
			</tr>
			<tr>
				<td style="width: 120px;">多行</td>
				<td><input is="iss-input" v-model="DStatus" multiline="true"/></td>
			</tr>
		</table>
	</div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					CStatus："",
					DStatus: ""
				},
				mounted: function () {},
				methods: {}
			});
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-input.html)

## iss-select下拉组件

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-select">
		<table is="iss-form" ref="vFilter">
			<tr>
				<td style="width: 120px;">根据js的数据获取下拉值</td>
				<td><input is="iss-select" :datasource="dataSourceDemo" v-model="filter.CStatus"/></td>
			</tr>
			<tr>
				<td style="width: 120px;">根据数据表t_dict获取下拉值</td>
				<td><input is="iss-select" :datasource="dict.sex" v-model="filter.DStatus"/></td>
			</tr>
		</table>
	</div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					filter: {
                		CStatus: "",
						DStatus:""
                	},
					dataSourceDemo: [
                        {"CCde": "111", "CCnm": "天河区"},
                        {"CCde": "112", "CCnm": "白云区"},
                        {"CCde": "113", "CCnm": "黄埔区"},
                        {"CCde": "114", "CCnm": "越秀区"}
                    ]
				},
				mounted: function () {},
				methods: {}
			});
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-select.html)

## iss-cascade级联组件

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-cascade">
		<table is="iss-form" ref="vFilter">
			<tr>
				<td style="width: 120px;">地址</td>
				<td><input is="iss-cascade" v-model="filter.DStatus" /></td>
			</tr>
			<tr>
				<td style="width: 120px;">自定义</td>
				<td><input is="iss-cascade" :datasource="dataSourceDemo1" v-model="filter.CStatus" /></td>
			</tr>
		</table>
	</div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					filter: {
                		CStatus: "",
						DStatus:""
                	},
					dataSourceDemo: [
                        {"CCde": "111", "CCnm": "天河区"},
                        {"CCde": "112", "CCnm": "白云区"},
                        {"CCde": "113", "CCnm": "黄埔区"},
                        {"CCde": "114", "CCnm": "越秀区"}
                    ],
					dataSourceDemo1: [
                    	{
                    		"CCde": "11",
                    		"CCnm": "广州市",
                    		"list": [
	                            {"CCde": "111", "CCnm": "天河区","list":[{"CCde": "1111", "CCnm": "高普路"}]},
	                            {"CCde": "112", "CCnm": "白云区"},
	                            {"CCde": "113", "CCnm": "黄埔区"},
	                            {"CCde": "114", "CCnm": "越秀区"}
                            ]
                    	},
                    	{
                    		"CCde": "12",
                    		"CCnm": "深圳市",
                    		"list": [
	                            {"CCde": "121", "CCnm": "南山区"},
	                            {"CCde": "122", "CCnm": "福田区"},
	                            {"CCde": "123", "CCnm": "罗湖区"},
	                            {"CCde": "124", "CCnm": "龙岗区"}
                            ]
                    	}
                    ]
				},
				mounted: function () {},
				methods: {}
			});
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-cascade.html)

## iss-form表单组件

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-form">
        <table is="iss-form">
            <tr style="float:left;">
                <td>这是iss-form</td>
                <td><input is="iss-input"></td>
            </tr>   
        </table>
    </div>
</div>
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-form.html)

## iss-index行序组件

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-index行序组件">
		<table is="iss-list" :datasource="rowsData">
			<thead>
				<tr>
					<th rowspan="2" class="index selector more">全选</th>
					<th rowspan="2" style="width: 439px;"></th>
					<th rowspan="2" style="width: 439px;"></th>
				</tr>
			</thead>
			<tbody>
				<tr v-for="(row, idx) of rowsData">
					<td is="iss-index" v-model="row._select">{{idx + 1}}</td>
				</tr>
			</tbody>
		</table>
	</div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					rowsData: [ {
                		CProCode: "", //项目编码
                		CProjectName: "", //项目名称
                		CIcon: "", //图标
                		CUrl: "", //URL
                		CDeductionWay: "", //扣减方式(01-次数，02-金额)
                		NNum: "", //次数
                		NAmt: "", //金额
                		TBgnTime: "", //有效起期
                		TEngTime: "", //有效止期
                		NPrice: "", //售价
                		CSex: "", //适用性别
                		NMinAge: "", //适用最小年龄
                		NMaxAge: "", //适用最大年龄 
                		CSynopsis: "", //简介
                		NCostPrice: "", //成本价
                		CEnabledState: null, //启用标志(0禁用，1启用)
                		CIssueStatus: null, //启用标志(0未发布，1已发布)
                		CCrtCde: "", //创建人员
                		TCrtTm: "", //创建时间
                		CUpdCde: "", //修改人员
                		TUpdTm: "", //修改时间
                		CType: "", // 类型
                		COrganCode: "" // 供应商
                	} ],
				},
				mounted: function() { // 页面加载后,vue挂载完成开始查询数据
                	this.$nextTick( function () {
	    				this.list();
                	} );
    			},
				methods: {
					list: function(pageno,pagesize) {
    	                issapi.post( {
	                        method: "projectMgrAction.list",
	                        onSuccess: function(jqXHR, textStatus, response) {
	                        vm.rowsData = response.data; 
	                    }
	                } );
                  }
				}
			});
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-index.html)

## iss-list列表组件

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-list列表组件">
        <table is="iss-list" :datasource="rowsData" >
            <tbody>
                <tr v-for="(row, idx) of rowsData">
                    <td><input is="iss-input" style="width: 439px;" v-model="row.CProCode" /></td>
                    <td><input is="iss-input" style="width: 439px;" v-model="row.CProjectName" /></td>
                    <td><input is="iss-input" style="width: 439px;" v-model="row.CUrl" /></td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					rowsData: [ {
                		CProCode: "", //项目编码
                		CProjectName: "", //项目名称
                		CIcon: "", //图标
                		CUrl: "", //URL
                		CDeductionWay: "", //扣减方式(01-次数，02-金额)
                		NNum: "", //次数
                		NAmt: "", //金额
                		TBgnTime: "", //有效起期
                		TEngTime: "", //有效止期
                		NPrice: "", //售价
                		CSex: "", //适用性别
                		NMinAge: "", //适用最小年龄
                		NMaxAge: "", //适用最大年龄 
                		CSynopsis: "", //简介
                		NCostPrice: "", //成本价
                		CEnabledState: null, //启用标志(0禁用，1启用)
                		CIssueStatus: null, //启用标志(0未发布，1已发布)
                		CCrtCde: "", //创建人员
                		TCrtTm: "", //创建时间
                		CUpdCde: "", //修改人员
                		TUpdTm: "", //修改时间
                		CType: "", // 类型
                		COrganCode: "" // 供应商
                	} ],
				},
				mounted: function() { // 页面加载后,vue挂载完成开始查询数据
                	this.$nextTick( function () {
	    				this.list();
                	} );
    			},
				methods: {
					list: function(pageno,pagesize) {
    	                issapi.post( {
	                        method: "projectMgrAction.list",
	                        onSuccess: function(jqXHR, textStatus, response) {
	                        vm.rowsData = response.data; 
	                    }
	                } );
                  }
				}
			});
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-list.html)

## iss-form,iss-list,iss-index综合示例

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="表单列表综合示例">
        <table is="iss-list"  ref="dpt" :datasource="rowsData" :gotopage="list" >
        <thead>
            <tr>
                <th rowspan="2" class="index selector more">全选</th>
                <th rowspan="2" style="width: 400px;">项目编码</th>
                <th rowspan="2" style="width: 400px;">项目名称</th>
                <th rowspan="2" style="width: 400px;">url</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(row, idx) of rowsData">
                <td is="iss-index" v-model="row._select">{{idx + 1}}</td>
                <td is="iss-index" v-model="row._select"><input is="iss-input" style="width: 400px;" v-model="row.CProCode" /></td>
                <td is="iss-index" v-model="row._select"><input is="iss-input" style="width: 400px;" v-model="row.CProjectName" /></td>
                <td is="iss-index" v-model="row._select"><input is="iss-input" style="width: 470px;"  v-model="row.CUrl" /></td>
            </tr>
        </tbody>
    </table>
    </div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					rowsData: [ {
                		CProCode: "", //项目编码
                		CProjectName: "", //项目名称
                		CIcon: "", //图标
                		CUrl: "", //URL
                		CDeductionWay: "", //扣减方式(01-次数，02-金额)
                		NNum: "", //次数
                		NAmt: "", //金额
                		TBgnTime: "", //有效起期
                		TEngTime: "", //有效止期
                		NPrice: "", //售价
                		CSex: "", //适用性别
                		NMinAge: "", //适用最小年龄
                		NMaxAge: "", //适用最大年龄 
                		CSynopsis: "", //简介
                		NCostPrice: "", //成本价
                		CEnabledState: null, //启用标志(0禁用，1启用)
                		CIssueStatus: null, //启用标志(0未发布，1已发布)
                		CCrtCde: "", //创建人员
                		TCrtTm: "", //创建时间
                		CUpdCde: "", //修改人员
                		TUpdTm: "", //修改时间
                		CType: "", // 类型
                		COrganCode: "" // 供应商
                	} ],
				},
				mounted: function() { // 页面加载后,vue挂载完成开始查询数据
                	this.$nextTick( function () {
	    				this.list();
                	} );
    			},
				methods: {
					list: function(pageno,pagesize) {
    					issapi.post( {
	            			method: "projectMgrAction.list",
	            			data: vm.filter,
	        				pageno: vm.$refs.dpt.pageno=(pageno || 1),
	        				pagesize: vm.$refs.dpt.pagesize=(pagesize || 10),
	        				onSuccess: function(jqXHR, textStatus, response) {
	        					vm.rowsData = response.data; 
	        					vm.$refs.dpt.total = response.total;
	        				}
	            		} );
    		         }	
				}
			});
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-zonghe.html)

## iss-shuttle穿梭框组件

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
    <div is="iss-card" title="iss-shuttle穿梭表组件">
        <input is="iss-shuttle" :fromdatasource="fromData" :todatasource="toData"/>
    </div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					fromData: [ //穿梭表模拟源数据
						{
							text1: "源列表",
							text2: "目的列表",
							type: [{
								id: "1",
								text: "数据1"
							}, {
								id: "2",
								text: "数据2"
							}, {
								id: "3",
								text: "数据3"
							}, {
								id: "4",
								text: "数据4"
							}, {
								id: "5",
								text: "数据5"
							}, {
								id: "6",
								text: "数据6"
							}, {
								id: "7",
								text: "数据7"
							}, {
								id: "8",
								text: "数据8"
							}, {
								id: "9",
								text: "数据9"
							}, {
								id: "10",
								text: "数据10"
							}, {
								id: "11",
								text: "数据11"
							}, {
								id: "12",
								text: "数据12"
							}, {
								id: "13",
								text: "数据13"
							}]
						}
					],
					toData: [], //穿梭表模拟目的数据
				},
				mounted: function () {},
				methods: {}
			});
		}
	};
})
```

* [效果](http://139.159.235.176:9110/demo/page/components/iss-shuttle.html)

## layer

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
	<div is="iss-card" title="layer">
		<input is="iss-input" style="width:80px;cursor:pointer;color:#41cdbb"
			class="readonly" value="请点击选择" @click="getBBren" /><input
			is="iss-input" style="width:145px;" v-model="BBcheckbox1" />
		<div is="iss-card" id="BBren" class="dialog">
			<span v-for="(items,index) of BBcheckbox"> &nbsp;&nbsp; <input
				is="iss-tag" :title="items" :value="items" v-model="BBcheckbox1" />
			</span>
		</div>
	</div>
</div>
```

```JS
;"use strict";

define( function(require, exports, module) {
	module.exports = {
		init : function() {
			var vm = new Vue( {
                el: "#pageDiv",
                data: {
                	BBcheckbox:["张三丰","刘德华","陈奕迅","王健林","马云"],
                	BBcheckbox1:""                                  
                },
                mounted: function() {},    			
    			methods: {
    				getBBren: function() { 
    					layer.open( {
							type: 1,
							title: "我是一个弹窗标题",
							area: ["700px", "440px"],
							content: $("#BBren"),
							shadeClose: false,
							scrollbar: false,
							btn: [ "确定", "取消" ],
							btn1: function(index,layero) {
								layer.close(index);
							},
							end: function() {
								layer.msg('完成操作', {icon: 1});  // 不是必需
							}
						} );
    				}    				
    			}
            } );
		}
	};
} );
```

* [效果](http://139.159.235.176:9110/demo/page/components/layer.html)

## ztree

>示例 

* 代码

```HTML
<div v-cloak id="pageDiv">
	<div is="iss-card" title="ztree 树">
		<div style="width: 20%; float: left;">
			<ul id="treeDemo" class="ztree"></ul>
		</div>
	</div>
</div>
```

```JS
;"use strict";
define(function (require, exports, module) {
	module.exports = {
		init: function () {
			var zTree;
			var vm = new Vue({
				el: "#pageDiv",
				data: {
					rowsData: [ 
                		{id:1, pId:0, name:"董事长", open:true},
                        {id:101, pId:1, name:"副董1"},
                        {id:102, pId:1, name:"副董2"},
                        {id:103, pId:1, name:"副董3"},
                        {id:10101, pId:101, name:"行政部"},
                        {id:10102, pId:101, name:"财务部"},            
                        {id:10103, pId:101, name:"业务部"},
                        {id:10104, pId:101, name:"生产部"},
                        {id:10201, pId:102, name:"后勤部"},
                        {id:10202, pId:102, name:"人事部"},
                        {id:10203, pId:102, name:"技术部"}
                	]
				},
				methods: {}
			});
			var setting = {
				data: {
					simpleData: {
						enable: true, //表示使用简单数据模式
					}
				},
				callback: { //返回函数; 根据需求选择合适的监听事件
					onClick: function (treeId, treeNode) { // onClick展开树
						var zTree = $.fn.zTree.getZTreeObj("tree");
					}
				}
			};
			$.fn.zTree.init($("#treeDemo"), setting, vm.rowsData);
		}
	};
});
```

* [效果](http://139.159.235.176:9110/demo/page/components/ztree.html)