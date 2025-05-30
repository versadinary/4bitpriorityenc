

``` verilog

// synthesis verilog_input_version verilog_2001
module top_module (
    input [3:0] in,
    output reg [1:0] pos  );

   always @ (*) begin
      case (in[0])
        1'b1: pos = 2'd0;
        default:
          begin
             case (in[1])
               1'b1: pos = 2'd1;
               default:
                 begin
                    case (in[2])
                      1'b1: pos = 2'd2;
                      default:
                        begin
                           case (in[3])
                             1'b1: pos = 2'd3;
                             default: pos = 2'd0;
                           endcase // case (in[3])
                        end
                        endcase // case (in[2])
                 end
                 endcase // case (in[1])
          end
          endcase // case (in[0])


   end
   
endmodule


```
