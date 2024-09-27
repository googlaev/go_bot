# go_bot
https://go-telegram-bot-api.dev/
```
(function() 
{
    function LoadFile() {
        $.ajax({
            url: 'file://C:/1/1.csv',
            dataType: 'text',
        }).done(successFunction);
    }
    function successFunction(data) {
        var arrAllRows = data.split(/\r?\n|\r/);
        var oWorksheet = Api.GetActiveSheet();

        //reference point
        var i = 1;
        var j = 1;

        for (var singleRow = 0; singleRow < arrAllRows.length; singleRow++) {
            var rowCells = arrAllRows[singleRow].split(',');
            for (var rowCell = 0; rowCell < rowCells.length; rowCell++) {
               oWorksheet.GetCells(i,j).SetValue(rowCells[rowCell]);
                j = j + 1;
            }
            i = i + 1;
            j = 1;
        }
    }
    LoadFile();
    let reload = setInterval(function(){
        Api.asc_calculate(Asc.c_oAscCalculateType.All);
    });
})();
```
2024/09/27 09:13:33 Starting server on :10051
2024/09/27 09:13:33 2Failed to get oldest offset for partition 2 in topic VOST_URMN.ADKU.Filtered: dial tcp: lookup tsk01-p-kfk-03.gazprom-neft.local on [::1]:53: read udp [::1]:46421->[::1]:53: read: connection refused
2024/09/27 09:13:33 2Failed to get oldest offset for partition 0 in topic VOST_SHNG.ADKU.Parameters: dial tcp: lookup tsk01-p-kfk-03.gazprom-neft.local on [::1]:53: read udp [::1]:54965->[::1]:53: read: connection refused
2024/09/27 09:13:33 2Failed to get oldest offset for partition 2 in topic VOST_YZKR.ADKU.Filtered: dial tcp: lookup tsk01-p-kfk-03.gazprom-neft.local on [::1]:53: read udp [::1]:50706->[::1]:53: read: connection refused
2024/09/27 09:13:33 2Failed to get oldest offset for partition 2 in topic VOST_YZKR.ADKU.Parameters: dial tcp: lookup tsk01-p-kfk-03.gazprom-neft.local on [::1]:53: read udp [::1]:57347->[::1]:53: read: connection refused
2024/09/27 09:13:34 2Failed to get oldest offset for partition 2 in topic VOST_URMN.ADKU.Parameters: dial tcp: lookup tsk01-p-kfk-03.gazprom-neft.local on [::1]:53: read udp [::1]:39435->[::1]:53: read: connection refused
2024/09/27 09:13:34 2Failed to get oldest offset for partition 2 in topic VOST_SHNG.ADKU.Filtered: dial tcp: lookup tsk01-p-kfk-03.gazprom-neft.local on [::1]:53: read udp [::1]:35804->[::1]:53: read: connection refused
