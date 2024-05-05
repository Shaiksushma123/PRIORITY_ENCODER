# PRIORITY_ENCODER
![image](https://github.com/RESMIRNAIR/PRIORITY_ENCODER/assets/154305926/016b3b20-1d4d-48fd-9012-a2c725b822db)
# Truth Table
![image](https://github.com/RESMIRNAIR/PRIORITY_ENCODER/assets/154305926/3da43bab-6ee6-456f-858f-4553d3623f8c)
# Program
module priority_encoder(

  input [7:0] D,
  
  output reg [2:0] y);
  
  always@(D) begin
  
    casex(D)
    
      8'b1xxx_xxxx: y = 3'b111;
      
      8'b01xx_xxxx: y = 3'b110;
      
      8'b001x_xxxx: y = 3'b101;
      
      8'b0001_xxxx: y = 3'b100;
      
      8'b0000_1xxx: y = 3'b011;
      
      8'b0000_01xx: y = 3'b010;
      
      8'b0000_001x: y = 3'b001;
      
      8'b0000_0001: y = 3'b000;
      
      default: $display("Invalid data received");
    
    endcase
  
  end

endmodule

## Output
![image](https://github.com/Shaiksushma123/PRIORITY_ENCODER/assets/159005642/20c210cd-bcb9-4ffa-8328-f64aa28e145c)
