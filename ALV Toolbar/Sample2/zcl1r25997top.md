```abap
*&---------------------------------------------------------------------*
*& Include ZCL1R25997TOP                            - Report ZCL1R25997
*&---------------------------------------------------------------------*
REPORT zcl1r25997 MESSAGE-ID k5.

*************************************
* Tables
*************************************
TABLES : ztc1_25_01.

*************************************
* Class Instance
*************************************
DATA : go_cont TYPE REF TO cl_gui_docking_container,
       go_alv  TYPE REF TO cl_gui_alv_grid.

*************************************
* Itab and wa
*************************************
DATA : BEGIN OF gs_body.
         INCLUDE STRUCTURE ztc1_25_01.
DATA :   cell_tab TYPE lvc_t_styl,
         modi_yn(1),
       END OF gs_body,
       gt_body LIKE TABLE OF gs_body.

*-- data# ### # ## # data# ###### ## itab and wa --*
DATA : gs_delt TYPE ztc1_25_01,
       gt_delt TYPE TABLE OF ztc1_25_01.

*************************************
* For ALV
*************************************
DATA : gs_fcat    TYPE lvc_s_fcat,
       gt_fcat    TYPE lvc_t_fcat,
       gs_variant TYPE disvariant,
       gs_layo    TYPE lvc_s_layo.

DATA : gs_button TYPE stb_button.

*************************************
* Common Variable
*************************************
DATA : gv_okcode TYPE sy-ucomm,
       gv_mode   VALUE 'E'.

----------------------------------------------------------------------------------
Extracted by Direct Download Enterprise version 1.3.1 - E.G.Mellodew. 1998-2005 UK. Sap Release 758
