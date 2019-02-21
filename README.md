# 2-06
display.setDefault( "background", 45, 0, 95 )
local lengthOfSquareTextField = native.newTextField( display.contentCenterX, display.contentCenterY + 140, 300, 40 )
lengthOfSquareTextField.id = "length textField"

 local hightOfSquareTextField = native.newTextField( display.contentCenterX, display.contentCenterY + 100, 300, 40 )
hightOfSquareTextField.id = "hightOfSquare textField"

lengthOfSquareTextField.id = "length textField"
local areaOfSquareTextField = display.newText( "Answer", display.contentCenterX, display.contentCenterY - 200, native.systemFont, 40 )
 
 local WidthOfSquareTextField = native.newTextField( display.contentCenterX, display.contentCenterY + 220, 300, 40 )
lengthOfSquareTextField.id = "length textField"


areaOfSquareTextField.id = "area textField"
areaOfSquareTextField:setFillColor( 2, 1, 1 )

local calculateButton = display.newImageRect( "Button.png", 406, 157 )
calculateButton.x = display.contentCenterX
calculateButton.y = display.contentCenterY
calculateButton.id = "calculate Button"
 
local function calculateButtonTouch( event )

    local hightOfSquare
    local lengthOfSquare
    local areaOfSquare
    local WidthOfSquare

    WidthOfSquare = WidthOfSquareTextField.text
    hightOfSquare = hightOfSquareTextField.text
    lengthOfSquare = lengthOfSquareTextField.text
    areaOfSquare = lengthOfSquare * WidthOfSquare/2 * hightOfSquare 
    -- print( areaOfSquare )
    areaOfSquareTextField.text = "The area is " .. areaOfSquare

    return true
end

calculateButton:addEventListener( "touch", calculateButtonTouch )
