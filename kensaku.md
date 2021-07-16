'''uml
@startuml
ユーザー -> webサイト :検索(商品)
webサイト -> DB :検索処理(商品)
DB -> DB :検索処理
DB -> webサイト :検索結果
webサイト -> ユーザー :検索結果
@enduml
'''
