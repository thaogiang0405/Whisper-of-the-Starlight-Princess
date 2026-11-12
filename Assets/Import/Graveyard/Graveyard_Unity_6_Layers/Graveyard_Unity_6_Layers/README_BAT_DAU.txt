BO ASSET CHIA 6 NHOM - UNITY 2D GRAVEYARD

Day la bo sap xep LAI cac PNG ma nguoi dung da upload, KHONG PHAI scene Unity da hoan thanh.
File PNG trong nhom Background/Ground/Platform co the la ATLAS hoac CANH CO NHIỀU THANH PHAN; khong phai tat ca deu la sprite tach rieng.
Ban co the giu nguyen anh toan bo hoac dung Sprite Mode: Multiple + Sprite Editor de slice (nhat la Final/Final/Tiles.png).
Mot so sprite CraftPix co phong cach vector va kich thuoc khac anh pixel-art goc; dieu chinh kich thuoc va mau sac neu dung chung.

CAU TRUC THU MUC:
  01_Background  (IDs 01-08): bau troi, nha tho, cay, mo, tuong, hang rao hau canh
  02_Ground_Wall (IDs 09-10): nen va tuong da - CAN COLLLIDER
  03_Platform    (IDs 11-13): be dung, cau, thang (thang la trigger leo)
  04_Props       (IDs 15-20, 23, 33): quan tai, thung, hop, den, duoc, bia mo, bien, dau lau
  05_Player_Enemy(IDs 24-26, 30-31): player va skeleton; ma/dơi CHUA CO
  06_Traps_Collectibles (IDs 14,21,22,27-29,32): gai, cua, nuoc, coin, key, chest, portal

THIET LAP UNITY GOI Y:
  - Unity 2D: Sprite Texture Type = Sprite (2D and UI)
  - Pixel art: Filter Mode = Point, Compression = None, ban dau dat PPU thich hop (vd 32) va dong nhat kich thuoc khi ghep.
  - Sorting Layers (thu tu sau ra truoc): BG_Sky, BG_Church, BG_Decor, Ground, Props_Back, Player, Props_Front, UI.
  - Ground: TilemapCollider2D + CompositeCollider2D; tren TilemapRenderer tuy chinh Sorting Layer.
  - Wall: Collider2D co dinh ngan player di xuyen.
  - Platform: Collider2D; neu muon nhay xuyen tu duoi len, dung PlatformEffector2D One Way va Used By Effector.
  - Ladder: BoxCollider2D Is Trigger + script climbing; khong lam vat chan duong.
  - Props: thuong khong collider, tru crate/barrel nen co neu dung lam chuong ngai vat.
  - Player: Rigidbody2D + CapsuleCollider2D/BoxCollider2D; set Layer: Player.
  - Enemy: Rigidbody2D/Collider2D + script patrol/attack; set Layer: Enemy.
  - Traps: trigger gay damage, tuy ban co the them collider rieng cho mat nen.
  - Collectibles: trigger va script nhat item; Portal: trigger hoan thanh level.

CHU Y:
  - IDs 22 (nuoc), 30 (ma), 31 (doi) CHUA CO file dung giong anh minh hoa trong tai nguyen ban dau.
  - IDs 02/03, 05/07, 08/09/11 co the dung lai chung anh goc, nen danh dau trung file la binh thuong.
  - ID 06 la tuong trang tri nen sau; co the chuyen sang Props_Back neu muon tuong nam gan player.
  - ID 18 la den co asset tuong duong, chua co day va khung den treo giong anh.
  - ID 21 la ban cua xoay, chua co day xich/qua cau gai giong minh hoa.
  - File Source trong BANG_PHAN_LOAI_33.csv chi ra vi tri asset ban da gui.

Nguon CraftPix: tai tu cac goi ZIP nguoi dung cung cap. Khi chia se/phan phoi game, hay kiem tra license cua tung bo asset CraftPix va khong tu y phat tan bo asset rieng.
