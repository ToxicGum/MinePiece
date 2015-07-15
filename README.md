package com.MinePiece.com;

import cpw.mods.fml.common.Mod;
import cpw.mods.fml.common.Mod.EventHandler;
import cpw.mods.fml.common.event.FMLInitializationEvent;
import cpw.mods.fml.common.event.FMLPostInitializationEvent;
import cpw.mods.fml.common.event.FMLPreInitializationEvent;
import cpw.mods.fml.common.registry.GameRegistry;
import net.minecraft.item.Item;
import net.minecraft.item.ItemFood;
import net.minecraft.potion.Potion;

@Mod(modid = "mp", name = "MinePiece", version = "1.0")
public class MinePiece {
	public static  Item itemOnigiri;
	public static Item itemClearClearFruit;
	public static Item itemSpringSpringFruit;
	
@EventHandler
public void preInit(FMLPreInitializationEvent event){
	//item blocks
	itemOnigiri = new ItemFood(4, 1.0F, true ).setUnlocalizedName("Itemonigiri").setTextureName("mp:itemonigiri");
	GameRegistry.registerItem(itemOnigiri, ((Item) itemOnigiri).getUnlocalizedName().substring(5));
	
	itemClearClearFruit = ((ItemFood) new ItemFood(1, (float) 0.2, true)).setPotionEffect(Potion.invisibility.id, 50000000, 4, 1.0F).setTextureName("mp:itemclearclearfruit");
	GameRegistry.registerItem(itemClearClearFruit, ((Item) itemClearClearFruit).getUnlocalizedName().substring(5));;
	
	itemSpringSpringFruit = ((ItemFood) new ItemFood(1, (float) 0.2, true)).setPotionEffect(Potion.jump.id, 50000000, 4, 1.0F).setTextureName("mp:itemclearclearfruit");
	GameRegistry.registerItem(itemSpringSpringFruit, ((Item) itemSpringSpringFruit).getUnlocalizedName().substring(5));;
}
@EventHandler
public void init(FMLInitializationEvent event) {
	//gui tileentity etc
	
	
}
@EventHandler
public void postInit(FMLPostInitializationEvent event){
	//creative tabs crafting recipes etc
}



}
