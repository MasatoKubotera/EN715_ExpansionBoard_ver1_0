<html lang="en">
  <head>
    <meta charset="uft-8">
    <meta name="author" content="Masato Kubotera">
  </head>
  <body>
    <h1>EN715 Expansion Board Ver. 1.0</h1>
    <h2>About EN715 Expansion Board</h2>
    <p>
      The EN715 Expansion Board is a circuit board to expand the functions of the Carrier Board for NVIDIA Jetson manufactured by AverMedia.<br>
      <br>
      Note that this is Ver. 1.0. For other versions, please refer to the following repositories.
      <ul>
        <li><a href="https://github.com/MasatoKubotera/EN715_ExpansionBoard_ver1_1">EN715 Expansion Board Ver. 1.1</a></li>
        <li><a href="https://github.com/MasatoKubotera/EN715_ExpansionBoard_ver1_2">EN715 Expansion Board Ver. 1.2</a></li>
      </ul>
      <h2>About Ver. 1.0</h2>
      Ver 1.0 was designed to facilitate the development of the AverMedia EN715 environment. As such, it is designed to support multiple communication methods.<br>
      Ver. 1.0 has the 2-port USB 2.0 Hi-Speed Hub on the board, which can be used by connecting an external USB Mini-B cable.<br>
      In addition, the MPU-9250 (9-Axis MotionTracking Device Module) module from Strawberry Linux can be installed, and SPI or I2C can be selected as the communication method via a short land on the board.<br>
      Additionally, two I2C (I2C0 and I2S1) ports and a UART (UART2) port with 3.3V signal can be connected via JST XH connector.<br>
      To install in the AverMedia EN715, connect the pin socket to the EN715's "20-pin Expansion header" and secure using 13mm length M3 spacers (e.g. <a href="http://www.hirosugi.jp/products/A/ASL-BE.html">ASL-313BE</a>).<br><br>
      This version was intended for development purposes and was never installed and used on a real robot.
      <!--
      Ver1.0は，AverMedia EN715の環境整備を促進するために設計されました．そのため，複数の通信方式に対応できるように設計されています．
      Ver.1.1 では，基板上に4ポートのUSB 2.0 Hi-Speed Hubを搭載しており，外付けのUSB Mini-Bケーブルを接続することでことで利用できます．
      また，Strawberry Linux 社の MPU-9250 (9-Axis MotionTracking Device Module) モジュールを装着することができ，基板上のショートランドにより，通信方式としてSPIかI2Cを選択することができます．
      さらに，2つのI2C（I2C0とI2S1）ポートと3.3V信号のUART (UART2)ポートをJST XHコネクタで接続することが可能です．
      AverMedia EN715に取り付けるには，ピンソケットをEN715の「20pin Expansion header」に接続し，13mm長のM3スペーサー（例：ASL-313BE）で固定します．
      このバージョンは開発用で，実際のロボットにインストールされて使用されたことはありません．
      -->
      <table>
        <tr>
          <td>
            <a href="image/brd_bottom.png">
              <div align="center">
                <img src="image/brd_bottom.png" width="320px">
              </div>
            </a>
          </td>
          <td>
            <div align="center">
              <img src="https://user-images.githubusercontent.com/53966390/191902149-e14f257c-e7c8-4761-9931-4e38d012e227.jpeg" width="320px">
            </div>
          </td>
        </tr>
        <tr>
          <td>
            <div align="center">
              PCB preview image
            </div>
          </td>
          <td>
            <div align="center">
              After component mounting
            </div>
          </td>    
        </tr>
      </table>
    </p>
    <h2>Repository Contents</h2>
    <p>
    <dl>
      <dt>\image</dt>
      <dd>PCB preview images and capture of design screen</dd>
      <dt>\libraries</dt>
      <dd>Libraries used in Autodesk Eagle design</dd>
      <dt>Schematic.pdf</dt>
      <dd>Circuit diagram of this product</dd>
      <dt>BOM.txt</dt>
      <dd>Parts lists output from design data</dd>
      <dt>.brd</dt>
      <dd>Board wiring design file by Autodesk Eagle</dd>
      <dt>.sch</dt>
      <dd>Schematic design file by Autodesk Eagle</dd>
      <dt>Gerber_data.zip</dt>
      <dd>Zip folder of Gerber format files for PCB manufacturing requests.</dd>
      <dt>LICENSE</dt>
      <dd>This is a license to use this product. Please confirm before use.</dd>
      <dt>.gitignore</dt>
      <dd>File to exclude cache files from management.</dd>
    </dl>
    </p>
    <h2>Documentation</h2>
      <p>
        <h3>BOM</h3>
          <table>
            <thead>
              <tr>
                <th> Eagle Design Parts # </th>
                <th> Q'ty </th>
                <th> Mfr. Product # </th>
                <th> Supplier </th>
                <th> Description </th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td> C1, C2, C3 </td>
                <td> 3 </td>
                <td> GRM188R6YA106MA73 </td>
                <td> <a href="https://akizukidenshi.com/catalog/g/gP-13161/">Akizuki</a> </td>
                <td> Multilayer Ceramic Capacitors SMD/SMT 10uF 35V 20% 0603 </td>
              </tr>
              <tr>
                <td> C4 </td>
                <td> 1 </td>
                <td> GRM188B11H103KA01 </td>
                <td> <a href="https://akizukidenshi.com/catalog/g/gP-13387/">Akizuki</a> </td>
                <td> Multilayer Ceramic Capacitors SMD/SMT 0.01uF 50V 10% 0603 </td>
              </tr>
              <tr>
                <td> C5, C6 </td>
                <td> 2 </td>
                <td> C1608C0G1H220J080AA </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/TDK/C1608C0G1H220J080AA?qs=NRhsANhppD%2FvEAPMU6eN6g%3D%3D">Mouser</a> </td>
                <td> Multilayer Ceramic Capacitors SMD/SMT 22pF 50V 5% 0603 </td>
              </tr>
              <tr>
                <td> CH1 </td>
                <td> 1 </td>
                <td> FH-2x10SG </td>
                <td> <a href="https://akizukidenshi.com/catalog/g/gC-00083/">Akizuki</a> </td>
                <td> 2.54mm Pin Socket, 2 Row, 20 Pin </td>
              </tr>
              <tr>
                <td> CH2, </td>
                <td> 1 </td>
                <td> S4B-XH-A(LF)(SN) </td>
                <td> <a href="https://www.daisen-netstore.com/shopdetail/000000000028/ct15/page1/order/">DAISEN</a> </td>
                <td> Connector Header Through Hole, Right Angle 4 position 2.54mm RED </td>
              </tr>
              <tr>
                <td> CH3 </td>
                <td> 1 </td>
                <td> S4B-XH-A(LF)(SN) </td>
                <td> <a href="https://www.daisen-netstore.com/shopdetail/000000000028/ct15/page1/order/">DAISEN</a> </td>
                <td> Connector Header Through Hole, Right Angle 4 position 2.54mm YELLOW </td>
              </tr>
              <tr>
                <td> CH4 </td>
                <td> 1 </td>
                <td> S4B-XH-A(LF)(SN) </td>
                <td> <a href="https://www.daisen-netstore.com/shopdetail/000000000028/ct15/page1/order/">DAISEN</a> </td>
                <td> Connector Header Through Hole, Right Angle 4 position 2.54mm BLUE </td>
              </tr>
              <tr>
                <td> CR1 </td>
                <td> 1 </td>
                <td> FA-238V 12.0000MB-K3 </td>
                <td> <a href="https://akizukidenshi.com/catalog/g/gP-05225/">Akizuki</a> </td>
                <td> Crystals 12.0000MHz 50ppm 10pF -40C +85C </td>
              </tr>
              <tr>
                <td> D1, D2, D3, D4, D5, D6 </td>
                <td> 6 </td>
                <td> CG0603MLC-05E </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/Bourns/CG0603MLC-05E?qs=lDok7oSghXVLNKMK69q%252BFQ%3D%3D">Mouser</a> </td>
                <td> ESD Protectors 5V 0603 </td>
              </tr>
              <tr>
                <td> F1 </td>
                <td> 1 </td>
                <td> MF-MSMF050-2 </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/Bourns/MF-MSMF050-2?qs=t3shhpq1i1DZ7OBD5kLNoA%3D%3D">Mouser</a> </td>
                <td> PTC Resettable Fuses 15V .5A-HD 100A MAX </td>
              </tr>
              <tr>
                <td> FL1, FL2, FL3 </td>
                <td> 3 </td>
                <td> BLM18SD220SN1D </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/Murata-Electronics/BLM18SD220SN1D?qs=glnLrWX4TPq%2Fm8%2FdPQltLg%3D%3D">Mouser</a> </td>
                <td> Ferrite Beads 22 OHM 0603 </td>
              </tr>
              <tr>
                <td> IC1 </td>
                <td> 1 </td>
                <td> FE1.1S </td>
                <td> <a href="https://www.aitendo.com/product/16185">aitendo</a> </td>
                <td> USB Interface IC USB 2.0 Hi-Speed 4 Port Hub Controller </td>
              </tr>
              <tr>
                <td> LED1 </td>
                <td> 1 </td>
                <td> 150060VS86000 </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/Wurth-Elektronik/150060VS86000?qs=GedFDFLaBXGW9qOjzZ1Hmw%3D%3D">Mouser</a> </td>
                <td> Standard LEDs - SMD Green 2V 20mA 573nm 0603 </td>
              </tr>
              <tr>
                <td> LED2,LED3,LED4 </td>
                <td> 3 </td>
                <td> 150060YS75000 </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/Wurth-Elektronik/150060YS75000?qs=LlUlMxKIyB0nKmwefHgtZw%3D%3D">Mouser</a> </td>
                <td> Standard LEDs - SMD Yellow 2V 20mA 590nm 0603 </td>
              </tr>
              <tr>
                <td> M1 </td>
                <td> 1 </td>
                <td> MPU-9250 Module </td>
                <td> <a href="https://strawberry-linux.com/catalog/items?code=12250">Strawberry Linux</a> </td>
                <td> 9-Axis MotionTracking Device Module </td>
              </tr>
              <tr>
                <td> M1 </td>
                <td> 1 </td>
                <td> 6604S-40 </td>
                <td> <a href="https://akizukidenshi.com/catalog/g/gP-01591/">Akizuki</a> </td>
                <td> 2.54mm Pin Socket Strip, Single Row </td>
              </tr>
              <tr>
                <td> M1 </td>
                <td> 1 </td>
                <td> PHA-1x40SG </td>
                <td> <a href="https://akizukidenshi.com/catalog/g/gC-06631/">Akizuki</a> </td>
                <td> 2.54mm Pin Header Strip, Straight, Single Row </td>
              </tr>
              <tr>
                <td> R1, R3, R4, R5 </td>
                <td> 4 </td>
                <td> RC0603FR-101KL </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/YAGEO/RC0603FR-101KL?qs=EiqXWrxQq63MM0wzm69ZKg%3D%3D">Mouser</a> </td>
                <td> Thick Film Resistors - SMD 1 kOhms 100-200mW 1% 0603 </td>
              </tr>
              <tr>
                <td> R2 </td>
                <td> 1 </td>
                <td> RC0603FR-102K7L </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/YAGEO/RC0603FR-102K7L?qs=Iqe6t0HYRD6Xaw3IgOqXnw%3D%3D">Mouser</a> </td>
                <td> Thick Film Resistors - SMD 2.7 kOhms 100-200 mW 1% 0603 </td>
              </tr>
              <tr>
                <td> USB1 </td>
                <td> 1 </td>
                <td> MUSB-5B-NE-S175 </td>
                <td> <a href="https://akizukidenshi.com/catalog/g/gC-05843/">Akizuki</a> </td>
                <td> Mini USB Connector 5P B type, Female, SMT type, without standoff </td>
              </tr>
              <tr>
                <td> USB2, USB3 </td>
                <td> 2 </td>
                <td> USB1046-GF-0190-L-B-A </td>
                <td> <a href="https://www.mouser.jp/ProductDetail/640-USB1046GF0190LBA">Mouser</a> </td>
                <td> USB Connectors USB2.0 A, Top Mount, SMT </td>
              </tr>
            </tbody>
          </table>         
        <h3>PCB Fabrication</h3>
          PCB(Printed Circuit Board) manufacturing was outsourced to <a href="https://www.elecrow.com/pcb-manufacturing.html">Elecrow</a>.<br>
          The custom specifications are as follows.
          <ul>
            <li>Layer : 2 layers</li>
            <li>Dimensions : 87 x 50</li>
            <li>PCB Qty : 10</li>
            <li>Different PCB Design : 1eg</li>
            <li>PCB Thickness : 1.6</li>
            <li>PCB Color : Black</li>
            <li>Surface Finish : HASL Lead Free</li>
            <li>Castellated Hole : No</li>
            <li>Copper Weight : 1oz</li>
            <li>PCB Stencil : Stencil 15cm X 15cm no frame</li>
          </ul>
          The data used to order fabrication are as follows.
          <ul>
            <li>Eagle design rule : <a href="https://www.elecrow.com/download/Elecrow_PCB_eagle_rule.zip">Elecrow Eagle Design Rule</a></li>
            <li>Eagle CAM file : <a href="https://www.elecrow.com/download/Elecrow_Gerber_Generater_DrillAlign.zip">Elecrow CAM file</a></li>
            <li>Gerber format data : <a href="/Gerber_data.zip">Gerber_data.zip</a></li>
          </ul>
      </p>
    <h2>Contact</h2>
    <p>
    If you have any questions, please contact MasatoKubotera, the product's designer, by E-mail.<br>
    E-mail : <a href="mailto:masatokubotera06@yahoo.co.jp">masatokubotera06@yahoo.co.jp</a>
    </p>
    <h2>License Information</h2>
    <p>
      This product is open source.<br>
      Please review the <a href="/LICENSE">LICENSE file</a> for license information.<br>
      <br>
      <strong>EN715 Expansion Board Ver. 1.0</strong> by Masato Kubotera is licensed under a <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
    </p>    
  </body>
</html>
