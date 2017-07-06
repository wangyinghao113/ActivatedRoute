# ActivatedRoute
angular2/4 路由取参
```
import { ActivatedRoute, Params } from '@angular/router';

constructor(public activatedRoute: ActivatedRoute) {
        activatedRoute.params
            .subscribe((params: Params) => {
               this.id = params['id'];
            });
  }
  ```
  
  ```
###接口参数
interface ActivatedRoute {
    snapshot : ActivatedRouteSnapshot
    url : Observable<UrlSegment[]>
    params : Observable<Params>
    queryParams : Observable<Params>
    fragment : Observable<string>
    data : Observable<Data>
    outlet : string
    component : Type<any>|string
    routeConfig : Route
    root : ActivatedRoute
    parent : ActivatedRoute
    firstChild : ActivatedRoute
    children : ActivatedRoute[]
    pathFromRoot : ActivatedRoute[]
    paramMap : Observable<ParamMap>
    queryParamMap : Observable<ParamMap>
    toString() : string
}
```
###用法
```
snapshot : ActivatedRouteSnapshot
该路由的当前快照

url : Observable<UrlSegment[]>
可观察到此路由匹配的网址段

params : Observable<Params>
对该路线的范围的矩阵参数的可观察

queryParams : Observable<Params>
可观察到所有路由共享的查询参数

fragment : Observable<string>
所有路由共享的URL片段的可观察

data : Observable<Data>
可观察到此路由的静态和解析数据。

outlet : string
路线的出口名称。这是一个常数

component : Type<any>|string
路线的组成部分。这是一个常数

routeConfig : Route
用于匹配此路由的配置

root : ActivatedRoute
路由器状态的根

parent : ActivatedRoute
路由器状态树中该路由的父节点

firstChild : ActivatedRoute
路由器状态树中此路由的第一个子节点

children : ActivatedRoute[]
路由器状态树中的这条路由的子节点

pathFromRoot : ActivatedRoute[]
从路由器状态树根到该路由的路径

paramMap : Observable<ParamMap>
queryParamMap : Observable<ParamMap>
toString() : string
```
