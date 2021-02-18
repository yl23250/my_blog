```sql
## 删除单据（无合同）
DELETE FROM kc_stock_out WHERE id = '2281'
DELETE FROM kc_stock_out_item WHERE stock_out_id = '2281'
DELETE FROM dms_order WHERE order_no = 'XSDD-20210210-000004'
DELETE FROM dms_order_detail  WHERE order_no = 'XSDD-20210210-000004'
DELETE FROM dms_delivery  t1 WHERE  delivery_no='FHTZD-20210210-0005'
DELETE FROM dms_delivery_detail WHERE delivery_no = 'FHTZD-20210210-0005'
```

```sql
## 再次同步YS入库单
UPDATE `yyigou_dsrp`.`kc_stock_in` SET ys_sync_flag=0 WHERE ys_sync_flag=2 AND enterprise_no='6021605625';

## 再次同步wms物料sql
UPDATE `yyigou_dsrp`.`bdc_goods` SET push_wms_status=0 WHERE push_wms_status=2 AND enterprise_no='6021605625';
```

