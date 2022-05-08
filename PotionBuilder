package be.alexisdepris.MatoulandModeration.utils;

import org.bukkit.Color;
import org.bukkit.inventory.ItemStack;
import org.bukkit.inventory.meta.PotionMeta;
import org.bukkit.potion.PotionEffect;
import org.bukkit.potion.PotionEffectType;

public class PotionBuilder {

   private final PotionMeta pm;
   private final ItemStack im;

   public PotionBuilder(ItemStack potion) {
       this.im = potion;
       this.pm = (PotionMeta) this.im.getItemMeta();
   }

   public PotionBuilder setColor(Color color) {
       this.pm.setColor(color);
       return this;
   }

   public PotionBuilder addEffect(PotionEffectType type, int dura, int amp, boolean overwrite) {
       this.pm.addCustomEffect(new PotionEffect(type, dura, amp), overwrite);
       return this;
   }

   public PotionBuilder addEffect(PotionEffectType type, int dura, int amp) {
       this.pm.addCustomEffect(new PotionEffect(type, dura, amp), true);
       return this;
   }

   public PotionBuilder buildItemMeta() {
       this.im.setItemMeta(this.pm);
       return this;
   }

   public ItemStack build() {
       return this.im;
   }

}
