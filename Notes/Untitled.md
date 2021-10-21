```lua
local newline_confirm = function(fallback)
	if cmp.visible() then
		cmp.confirm({select = true})
		feedkey("<S-CR>","")
	else
		fallback()
	end
end
cmp.setup({
     mapping = {
           --some mappings...
           ['<CR>'] = cmp.mapping(newline_confirm, {"i", "s"})
      }
       --recommended sources here...
})
```