function regtofloat(val1, val2) {
	var reg1;
	var reg2;
	var bin32;

    function toBinary(value){
        return (value >>> 0).toString(2);
    }
    
    reg2 = toBinary(val2);
    reg1 = toBinary(val1);

    function to16bits(bin){
    	var num_zero;
        var i = 0;
        num_zero = 16 - parseInt(bin.length);
        while (i < num_zero) {
            bin = '0' + bin;        
            i = i +1;
        }
        return bin;
    }

    bin32 = to16bits(reg1) + to16bits(reg2);
    
    function BinToFloat32(str) {
        var int = parseInt(str, 2);
        var i;
        if (int > 0 || int < 0) {
            var sign = (int >>> 31) ? -1 : 1;
            var exponent = (int >>> 23 & 0xff) - 127;
            var mantissa = ((int & 0x7fffff) + 0x800000).toString(2);
            var float32 = 0;
            for (i = 0; i < mantissa.length; i += 1) { 
            float32 += parseInt(mantissa[i]) ? Math.pow(2, exponent) : 0; exponent-- ;
            }
            return float32 * sign;
        } else {
        return 0;}
    }
    return BinToFloat32(bin32);
}
