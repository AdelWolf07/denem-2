# Crops & Coops tarzı oyun: ajan ekibi kurulumu

## Dosyaları yerleştir

Godot proje klasörünün kökünde:

```
.claude/agents/game-director.md
.claude/agents/idle-art-designer.md
.claude/agents/godot-incremental-dev.md
```

Klasörleri bir kez oluştur (ajanlar kendileri de açar ama baştan olması iyi):

```
design/research/
design/art/
assets/placeholders/
```

## Çalıştırma

Proje kökünde şunu çalıştır; game-director ana oturum olur ve diğer iki ajanı kendisi çağırır:

```
claude --agent game-director
```

Alt ajanlar birbirini çağıramaz, bu yüzden koordinasyon her zaman game-director üzerinden geçer.

## İlk komut örnekleri

1. "Idle çiftlik oyunlarını araştır, özgün bir oyun vizyonu ve GDD taslağı çıkar."
2. "Ekin ve kümes hatlarının ekonomisini tasarla, `economy.md` yaz."
3. "Stil rehberini oluştur ve ilk 5 ekinle 3 hayvanın tasarım föyünü ve yer tutucularını hazırla."
4. "Ekin yetiştirme sistemini (ekme, büyüme, hasat, satış) kodlat."

## Akış

game-director araştırır ve tasarlar, `design/` altına yazar, idle-art-designer varlıkları üretir (`design/art/`, `assets/placeholders/`), godot-incremental-dev bunları kullanarak kodlar, game-director sonucu denetler.
