CLASS zcl_date_operations DEFINITION
  PUBLIC
  FINAL
  CREATE PUBLIC .

  PUBLIC SECTION.

    CLASS-METHODS first_day_of_last_month
      IMPORTING
        !iv_date       TYPE sydatum
      RETURNING
        VALUE(rv_date) TYPE sydatum .
    CLASS-METHODS first_day_of_next_month
      IMPORTING
        !iv_date       TYPE sydatum
      RETURNING
        VALUE(rv_date) TYPE sydatum .
    CLASS-METHODS last_day_of_last_month
      IMPORTING
        !iv_date       TYPE sydatum
      RETURNING
        VALUE(rv_date) TYPE sydatum .
    CLASS-METHODS last_day_of_last_year
      IMPORTING
        !iv_date       TYPE sydatum
      RETURNING
        VALUE(rv_date) TYPE sydatum .
    CLASS-METHODS last_day_of_next_month
      IMPORTING
        !iv_date       TYPE sydatum
      RETURNING
        VALUE(rv_date) TYPE sydatum .
    CLASS-METHODS last_day_of_this_month
      IMPORTING
        !iv_date       TYPE sydatum
      RETURNING
        VALUE(rv_date) TYPE sydatum .
  PROTECTED SECTION.
  PRIVATE SECTION.
ENDCLASS.



CLASS ZCL_DATE_OPERATIONS IMPLEMENTATION.


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Static Public Method ZCL_DATE_OPERATIONS=>FIRST_DAY_OF_LAST_MONTH
* +-------------------------------------------------------------------------------------------------+
* | [--->] IV_DATE                        TYPE        SYDATUM
* | [<-()] RV_DATE                        TYPE        SYDATUM
* +--------------------------------------------------------------------------------------</SIGNATURE>
  METHOD first_day_of_last_month.

    rv_date = last_day_of_last_month( iv_date ).
    rv_date+6(2) = '01'.

  ENDMETHOD.


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Static Public Method ZCL_DATE_OPERATIONS=>FIRST_DAY_OF_NEXT_MONTH
* +-------------------------------------------------------------------------------------------------+
* | [--->] IV_DATE                        TYPE        SYDATUM
* | [<-()] RV_DATE                        TYPE        SYDATUM
* +--------------------------------------------------------------------------------------</SIGNATURE>
  METHOD first_day_of_next_month.

    rv_date = iv_date(6) && '01'.
    ADD 31 TO rv_date.
    rv_date+6(2) = '01'.

  ENDMETHOD.


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Static Public Method ZCL_DATE_OPERATIONS=>LAST_DAY_OF_LAST_MONTH
* +-------------------------------------------------------------------------------------------------+
* | [--->] IV_DATE                        TYPE        SYDATUM
* | [<-()] RV_DATE                        TYPE        SYDATUM
* +--------------------------------------------------------------------------------------</SIGNATURE>
  METHOD last_day_of_last_month.

    rv_date = iv_date(6) && '01'.
    SUBTRACT 1 FROM rv_date.

  ENDMETHOD.


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Static Public Method ZCL_DATE_OPERATIONS=>LAST_DAY_OF_LAST_YEAR
* +-------------------------------------------------------------------------------------------------+
* | [--->] IV_DATE                        TYPE        SYDATUM
* | [<-()] RV_DATE                        TYPE        SYDATUM
* +--------------------------------------------------------------------------------------</SIGNATURE>
  METHOD last_day_of_last_year.

    rv_date = iv_date(4) && '0101'.
    SUBTRACT 1 FROM rv_date.

  ENDMETHOD.


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Static Public Method ZCL_DATE_OPERATIONS=>LAST_DAY_OF_NEXT_MONTH
* +-------------------------------------------------------------------------------------------------+
* | [--->] IV_DATE                        TYPE        SYDATUM
* | [<-()] RV_DATE                        TYPE        SYDATUM
* +--------------------------------------------------------------------------------------</SIGNATURE>
  METHOD last_day_of_next_month.

    rv_date = iv_date(6) && '01'.
    ADD 62 TO rv_date.
    rv_date+6(2) = '01'.
    SUBTRACT 1 FROM rv_date.

  ENDMETHOD.


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Static Public Method ZCL_DATE_OPERATIONS=>LAST_DAY_OF_THIS_MONTH
* +-------------------------------------------------------------------------------------------------+
* | [--->] IV_DATE                        TYPE        SYDATUM
* | [<-()] RV_DATE                        TYPE        SYDATUM
* +--------------------------------------------------------------------------------------</SIGNATURE>
  METHOD last_day_of_this_month.

    rv_date = iv_date(6) && '01'.
    ADD 32 TO rv_date.
    rv_date+6(2) = '01'.
    SUBTRACT 1 FROM rv_date.

  ENDMETHOD.
ENDCLASS.
