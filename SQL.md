# 新项目清理数据
- 通常为测试后执行，或非同国项目时执行。
> 解决报错 
> api/user/info:current_price 因切换股票导致总持仓无法计算。

```sql
-- 清空指定的数据表
TRUNCATE TABLE ptr_goods_bigbill;
TRUNCATE TABLE ptr_goods_discount;
TRUNCATE TABLE ptr_goods_duanda;
TRUNCATE TABLE ptr_goods_kline_day;
TRUNCATE TABLE ptr_goods_kline_fen_shi;
TRUNCATE TABLE ptr_goods_scramble;
TRUNCATE TABLE ptr_goods_shengou;
TRUNCATE TABLE ptr_goods_short;
TRUNCATE TABLE ptr_goods_vip_scramble;
TRUNCATE TABLE ptr_jijin_log;
TRUNCATE TABLE ptr_jijin_order;
TRUNCATE TABLE ptr_order;
TRUNCATE TABLE ptr_order_bigbill;
TRUNCATE TABLE ptr_order_buy;
TRUNCATE TABLE ptr_order_buy_bigbill;
TRUNCATE TABLE ptr_order_sell;
TRUNCATE TABLE ptr_user_bank_card;
TRUNCATE TABLE ptr_user_goods_collect;
TRUNCATE TABLE ptr_user_money_log;
TRUNCATE TABLE ptr_user_pay;
TRUNCATE TABLE ptr_user_scramble;
TRUNCATE TABLE ptr_user_shengou;
TRUNCATE TABLE ptr_user_withdraw;
TRUNCATE TABLE admin_operation_log;
TRUNCATE TABLE ptr_admin_agent_users;
TRUNCATE TABLE ptr_admin_agent_users_xiaoshou;
TRUNCATE TABLE ptr_rinei_order;
TRUNCATE TABLE ptr_rinei_sh;

-- 清除 ptr_user 表中除了 uid 为 75 的所有数据
DELETE FROM ptr_user WHERE uid <> 75;

-- 清除 admin_users 表中 id 大于 165 的数据
DELETE FROM admin_users WHERE id > 165;

-- 清除 admin_role_users 表中 user_id 大于 165 的数据
DELETE FROM admin_role_users WHERE user_id > 165;

```