YUNI =1


r = "4565"
R = gg.prompt({"パスワード"})
if R[1] == r then
else
print('パスワードが違います')
os.exit()
end



function Main()
Menu = gg.choice({ 
"メニュー1",
"メニュー2",
"終了",
},nil,'ユニ')
if Menu == 1 then A() end
if Menu == 2 then B() end
if Menu == 3 then EXIT() end
YUNI=-1
end

function A()
YU = gg.multiChoice({
"内容1",
"内容2",
"内容3",
"戻る"
},nil,'メニュー1')
if YU == nil then
else
if YU[1] == true then A1() end
if YU[2] == true then A2() end
if YU[3] == true then A3() end
if YU[4] == true then Main() end
YUNI=-1
end
end

function A1()
gg.clearResults() 
gg.setRanges(gg.REGION_ANONYMOUS) 
gg.searchNumber("#検索", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1) 
gg.refineNumber("#リファイン",gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)--見せる範囲
gg.editAll("#変更値", gg.TYPE_DWORD)
--gg.toast("成功")
end

function A2()
gg.clearResults()
gg.setRanges(32)
gg.searchNumber("検索値",4,false,gg.SIGN_EQUAL,0,-1)
gg.refineNumber("リファイン",4,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(100)
gg.editAll("変更値",4)
gg.toast("成功")
end

function A3()
gg.clearResults()
gg.setRanges(32)
gg.searchNumber("検索値",4,false,gg.SIGN_EQUAL,0,-1)
gg.refineNumber("リファイン",4,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(100)
gg.editAll("変更値",4)
gg.toast("成功")
end


function B()
NI = gg.multiChoice({ 
"内容1",
"内容2",
"内容3",
"戻る"
},nil,'メニュー2')
if NI == nil then
else
if NI[1] == true then B1() end
if NI[2] == true then B2() end
if NI[3] == true then B3() end
if NI[4] == true then Main() end
YUNI=-1
end
end

function B1()
gg.clearResults()
gg.setRanges(32)
gg.searchNumber("検索値",4,false,gg.SIGN_EQUAL,0,-1)
gg.refineNumber("リファイン",4,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(100)
gg.editAll("変更値",4)
gg.toast("成功")
end

function B2()
gg.clearResults()
gg.setRanges(32)
gg.searchNumber("検索値",4,false,gg.SIGN_EQUAL,0,-1)
gg.refineNumber("リファイン",4,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(100)
gg.editAll("変更値",4)
gg.toast("成功")
end

function B3()
gg.clearResults()
gg.setRanges(32)
gg.searchNumber("検索値",4,false,gg.SIGN_EQUAL,0,-1)
gg.refineNumber("リファイン",4,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(100)
gg.editAll("変更値",4)
gg.toast("成功")
end

function EXIT()
EX = gg.alert('スクリプトを閉じますか?','はい','いいえ')

if EX == 1 then by() end
if EX == 2 then Main() end
end

function by()
os.exit()
end


while true   do
if gg.isVisible(true) then
YUNI = 1
gg.setVisible(false)
end
if YUNI==1 then Main() end
end
