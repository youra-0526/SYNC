```abap
*&---------------------------------------------------------------------*
*& Include ZCL1R25994TOP                            - Report ZCL1R25994
*&---------------------------------------------------------------------*
REPORT zcl1r25994 MESSAGE-ID zcl1msg25.

*************************************
* Tables
*************************************
TABLES : mara.

*************************************
* Itab and wa
*************************************
DATA : BEGIN OF gs_body,
         matnr TYPE mara-matnr,
         ersda TYPE mara-ersda,
         vpsta TYPE mara-vpsta,
         pstat TYPE mara-pstat,
         mtart TYPE mara-mtart,
         mtbez TYPE t134t-mtbez,
         ntgew TYPE mara-ntgew,
         gewei TYPE mara-gewei,
       END OF gs_body,
       gt_body LIKE TABLE OF gs_body.

DATA : gs_text TYPE t134t,
       gt_text TYPE TABLE OF t134t.

----------------------------------------------------------------------------------
Extracted by Mass Download version 1.5.5 - E.G.Mellodew. 1998-2025. Sap Release 753
