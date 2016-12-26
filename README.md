# CustomOres-API
API to make CustomOres

Make sure that you register the class "MineCustomOre" into your main class

You will make your custom items in the main class:

	public void registerOres() {
		
		ItemStack sulfuri = new ItemStack(Material.GLOWSTONE_DUST);
		ItemMeta sulm = sulfuri.getItemMeta();
		sulm.setDisplayName(ChatColor.YELLOW + "Sulfur");
		sulfuri.setItemMeta(sulm);
		
		CustomOre sulfur = new CustomOre(Material.GOLD_ORE);
		sulfur.setNumber(1);
		sulfur.setDrop(sulfuri);
		sulfur.registerCustomOre();
		
	}
  
  the "setNumber(int)" cannot be the same as another, and the number has to start at one and cannot ecced the amount of custom ores that you have
  ex:
  CustomOre sulfur = new CustomOre(Material.GOLD_ORE);
  sulfur.setNumber(1);
  sulfur.registerCustomOre();
  
  CustomOre ruby = new CustomOre(Material.REDSTONE_ORE);
  ruby.setNumber(2);
  ruby.registerCustomOre();
