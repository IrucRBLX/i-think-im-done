local name = "Iruc"
local p = Instance.new("Part")
p.Parent = workspace
p.Locked = true
p.BrickColor = BrickColor.new('Really Black')
p.Size = Vector3.new(8, 1.2, 8)
p.Anchored = true
p.Transparency = 0.5
p.BottomSurface = ("Smooth")
p.TopSurface = ("Smooth")
local m = Instance.new("SpecialMesh", N) m.MeshType = "Sphere"
m.Scale = Vector3.new(3, 20, 3)
m.Parent = p
while true do
    p.CFrame = CFrame.new(game.Players:findFirstChild(name).Character.Torso.CFrame.x, game.Players:findFirstChild(name).Character.Torso.CFrame.y - 4, game.Players:findFirstChild(name).Character.Torso.CFrame.z)
    wait()
end

function onTouched(part)
local h = part.Parent:findFirstChild("Humanoid")
if h~=nil then
h.Health = 0
end
end
script.p.Touched:connect(onTouched)
