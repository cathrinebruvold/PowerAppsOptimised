nfHTML = "<p style='
margin:60px 20px 20px 20px;
color:red;
transform: rotate(-45deg);
position: relative;
font-weight:normal;
font-size:30px'>
TEST MODE
</p>
";

nfLoadingSVG =  "data:image/svg+xml;utf8," & EncodeUrl(
            "
<svg xmlns='http://www.w3.org/2000/svg' width='500' height='500'>
  <defs>
    <linearGradient id='circleGradient' x1='0%' y1='0%' x2='100%' y2='100%'>
      <stop offset='0%' stop-color='pink' />
      <stop offset='60%' stop-color='purple' />
      <stop offset='100%' stop-color='darkpurple' />
    </linearGradient>
  </defs>
  <!-- Larger background circle -->
  <circle cx='250' cy='250' r='220' fill='rgba(255, 182, 193, 0.1)' />
  <!-- Static outline -->
  <circle cx='250' cy='250' r='220'
          fill='none' stroke='lightpink' stroke-width='2' />
  <!-- Animated border stroke -->
  <circle cx='250' cy='250' r='220'
          fill='none'
          stroke='url(#circleGradient)'
          stroke-width='5'
          stroke-linecap='round'
          stroke-dasharray='1382.3'
          stroke-dashoffset='1382.3'>
    <animate attributeName='stroke-dashoffset'
             from='1382.3' to='0'
             dur='3s'
             repeatCount='3'
             fill='freeze' />
  </circle>
  <!-- Centered text (scaled up) -->
  <text x='250' y='250' dominant-baseline='middle' text-anchor='middle'
        font-size='22' font-family='Segoe UI' font-weight='bold' fill='black'>
    Loading cool things... ✨
  </text>
</svg>
"
        );
colMorePurchaseOrder = Table(
    {
        vendorId: "Vendor001",
        vendorName: "Acme Corp",
        manuallyProcessedInApp: false,
        poNumber: "PO12345",
        warehouseId: "WH001",
        result: "Success",
        LastModified: DateAdd(
            Today(),
            -5,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Courier",
        linesCount: 10
    },
    {
        vendorId: "Vendor002",
        vendorName: "Global Supplies",
        manuallyProcessedInApp: false,
        poNumber: "PO67890",
        warehouseId: "WH002",
        result: "Pending",
        LastModified: DateAdd(
            Today(),
            -3,
            TimeUnit.Days
        ),
        Datasource: "SharePoint",
        deliveryMethod: "Email",
        linesCount: 5
    },
    {
        vendorId: "Vendor003",
        vendorName: "Tech Distributors",
        manuallyProcessedInApp: false,
        poNumber: "PO11223",
        warehouseId: "WH003",
        result: "Failed",
        LastModified: DateAdd(
            Today(),
            -7,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "FTP",
        linesCount: 15
    },
    {
        vendorId: "Vendor004",
        vendorName: "FastTrack Logistics",
        manuallyProcessedInApp: false,
        poNumber: "PO44556",
        warehouseId: "WH004",
        result: "Success",
        LastModified: DateAdd(
            Today(),
            -1,
            TimeUnit.Days
        ),
        Datasource: "SharePoint",
        deliveryMethod: "Courier",
        linesCount: 8
    },
    {
        vendorId: "Vendor005",
        vendorName: "Northern Lights",
        manuallyProcessedInApp: false,
        poNumber: "PO77889",
        warehouseId: "WH005",
        result: "Pending",
        LastModified: DateAdd(
            Today(),
            -2,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Email",
        linesCount: 20
    },
        // Additional Rows with Mixed Datasources

    {
        vendorId: "Vendor011",
        vendorName: "Skyline Supplies",
        manuallyProcessedInApp: false,
        poNumber: "PO33456",
        warehouseId: "WH011",
        result: "Success",
        LastModified: DateAdd(
            Today(),
            -6,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Courier",
        linesCount: 13
    },
    {
        vendorId: "Vendor012",
        vendorName: "NextGen Industries",
        manuallyProcessedInApp: false,
        poNumber: "PO77801",
        warehouseId: "WH012",
        result: "Failed",
        LastModified: DateAdd(
            Today(),
            -4,
            TimeUnit.Days
        ),
        Datasource: "SharePoint",
        deliveryMethod: "Email",
        linesCount: 6
    },
    {
        vendorId: "Vendor013",
        vendorName: "Alpha Distributors",
        manuallyProcessedInApp: false,
        poNumber: "PO88912",
        warehouseId: "WH013",
        result: "Pending",
        LastModified: DateAdd(
            Today(),
            -9,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "FTP",
        linesCount: 9
    },
    {
        vendorId: "Vendor014",
        vendorName: "Unified Logistics",
        manuallyProcessedInApp: false,
        poNumber: "PO99865",
        warehouseId: "WH014",
        result: "Success",
        LastModified: DateAdd(
            Today(),
            -8,
            TimeUnit.Days
        ),
        Datasource: "SharePoint",
        deliveryMethod: "Courier",
        linesCount: 11
    },
    {
        vendorId: "Vendor015",
        vendorName: "Bright Horizons",
        manuallyProcessedInApp: false,
        poNumber: "PO12945",
        warehouseId: "WH015",
        result: "Failed",
        LastModified: DateAdd(
            Today(),
            -10,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Email",
        linesCount: 4
    }
);
nfSVG = "data:image/svg+xml;utf8," & EncodeUrl(
    "<svg width='100%' height='100%' id='svg' viewBox='0 0 1440 490' xmlns='http://www.w3.org/2000/svg' class='transition duration-300 ease-in-out delay-150'><style>
          .path-0{
            animation:pathAnim-0 4s;
            animation-timing-function: linear;
            animation-iteration-count: infinite;
          }
          @keyframes pathAnim-0{
            0%{
              d: path('M 0,500 L 0,125 C 95.72248803827753,106.16746411483254 191.44497607655506,87.33492822966508 284,111 C 376.55502392344494,134.66507177033492 465.9425837320574,200.82775119617224 562,219 C 658.0574162679426,237.17224880382776 760.7846889952153,207.35406698564591 873,216 C 985.2153110047847,224.64593301435409 1106.9186602870814,271.75598086124404 1203,313 C 1299.0813397129186,354.24401913875596 1369.5406698564593,389.62200956937795 1440,425 L 1440,500 L 0,500 Z');
            }
            25%{
              d: path('M 0,500 L 0,125 C 107.99043062200957,99.16267942583731 215.98086124401914,73.32535885167462 313,101 C 410.01913875598086,128.67464114832538 496.0669856459331,209.86124401913878 583,244 C 669.9330143540669,278.1387559808612 757.7511961722488,265.22966507177034 849,276 C 940.2488038277512,286.77033492822966 1034.9282296650717,321.2200956937799 1134,350 C 1233.0717703349283,378.7799043062201 1336.5358851674641,401.88995215311 1440,425 L 1440,500 L 0,500 Z');
            }
            50%{
              d: path('M 0,500 L 0,125 C 94.25837320574166,97.11483253588517 188.51674641148333,69.22966507177034 288,98 C 387.4832535885167,126.77033492822966 492.1913875598085,212.1961722488038 597,256 C 701.8086124401915,299.8038277511962 806.7177033492824,301.98564593301444 886,298 C 965.2822966507176,294.01435406698556 1018.9377990430623,283.8612440191387 1107,304 C 1195.0622009569377,324.1387559808613 1317.531100478469,374.56937799043067 1440,425 L 1440,500 L 0,500 Z');
            }
            75%{
              d: path('M 0,500 L 0,125 C 115.15789473684208,119.65071770334929 230.31578947368416,114.30143540669857 313,130 C 395.68421052631584,145.69856459330143 445.8947368421053,182.44497607655498 540,196 C 634.1052631578947,209.55502392344502 772.1052631578948,199.9186602870813 873,233 C 973.8947368421052,266.0813397129187 1037.6842105263158,341.88038277511964 1126,381 C 1214.3157894736842,420.11961722488036 1327.157894736842,422.5598086124402 1440,425 L 1440,500 L 0,500 Z');
            }
            100%{
              d: path('M 0,500 L 0,125 C 95.72248803827753,106.16746411483254 191.44497607655506,87.33492822966508 284,111 C 376.55502392344494,134.66507177033492 465.9425837320574,200.82775119617224 562,219 C 658.0574162679426,237.17224880382776 760.7846889952153,207.35406698564591 873,216 C 985.2153110047847,224.64593301435409 1106.9186602870814,271.75598086124404 1203,313 C 1299.0813397129186,354.24401913875596 1369.5406698564593,389.62200956937795 1440,425 L 1440,500 L 0,500 Z');
            }
          }</style><defs><linearGradient id='gradient' x1='0%' y1='50%' x2='100%' y2='50%'><stop offset='5%' stop-color='#F78DA7'></stop><stop offset='95%' stop-color='#8ED1FC'></stop></linearGradient></defs><path d='M 0,500 L 0,125 C 95.72248803827753,106.16746411483254 191.44497607655506,87.33492822966508 284,111 C 376.55502392344494,134.66507177033492 465.9425837320574,200.82775119617224 562,219 C 658.0574162679426,237.17224880382776 760.7846889952153,207.35406698564591 873,216 C 985.2153110047847,224.64593301435409 1106.9186602870814,271.75598086124404 1203,313 C 1299.0813397129186,354.24401913875596 1369.5406698564593,389.62200956937795 1440,425 L 1440,500 L 0,500 Z' stroke='none' stroke-width='0' fill='url(#gradient)' fill-opacity='0.53' class='transition-all duration-300 ease-in-out delay-150 path-0'></path><style>
          .path-1{
            animation:pathAnim-1 4s;
            animation-timing-function: linear;
            animation-iteration-count: infinite;
          }
          @keyframes pathAnim-1{
            0%{
              d: path('M 0,500 L 0,291 C 94.30622009569379,281.7942583732057 188.61244019138758,272.58851674641147 291,278 C 393.3875598086124,283.41148325358853 503.8564593301435,303.4401913875598 605,350 C 706.1435406698565,396.5598086124402 797.9617224880383,469.6507177033493 889,487 C 980.0382775119617,504.3492822966507 1070.2966507177034,465.95693779904303 1162,474 C 1253.7033492822966,482.04306220095697 1346.8516746411483,536.5215311004785 1440,591 L 1440,500 L 0,500 Z');
            }
            25%{
              d: path('M 0,500 L 0,291 C 94.35406698564591,254.3397129186603 188.70813397129183,217.6794258373206 273,231 C 357.29186602870817,244.3205741626794 431.52153110047846,307.62200956937795 524,359 C 616.4784688995215,410.37799043062205 727.2057416267942,449.83253588516743 824,469 C 920.7942583732058,488.16746411483257 1003.6555023923445,487.0478468899522 1104,504 C 1204.3444976076555,520.9521531100478 1322.1722488038276,555.9760765550238 1440,591 L 1440,500 L 0,500 Z');
            }
            50%{
              d: path('M 0,500 L 0,291 C 94.85167464114832,275.35406698564594 189.70334928229664,259.7081339712919 272,278 C 354.29665071770336,296.2918660287081 424.0382775119617,348.5215311004784 526,387 C 627.9617224880383,425.4784688995216 762.1435406698564,450.2057416267943 876,469 C 989.8564593301436,487.7942583732057 1083.3875598086127,500.6555023923445 1174,520 C 1264.6124401913873,539.3444976076555 1352.3062200956938,565.1722488038278 1440,591 L 1440,500 L 0,500 Z');
            }
            75%{
              d: path('M 0,500 L 0,291 C 114.55502392344502,281.13397129186603 229.11004784689004,271.267942583732 332,271 C 434.88995215310996,270.732057416268 526.1148325358851,280.0622009569379 606,322 C 685.8851674641149,363.9377990430621 754.4306220095694,438.48325358851673 852,479 C 949.5693779904306,519.5167464114833 1076.1626794258375,526.0047846889952 1179,539 C 1281.8373205741625,551.9952153110048 1360.9186602870814,571.4976076555024 1440,591 L 1440,500 L 0,500 Z');
            }
            100%{
              d: path('M 0,500 L 0,291 C 94.30622009569379,281.7942583732057 188.61244019138758,272.58851674641147 291,278 C 393.3875598086124,283.41148325358853 503.8564593301435,303.4401913875598 605,350 C 706.1435406698565,396.5598086124402 797.9617224880383,469.6507177033493 889,487 C 980.0382775119617,504.3492822966507 1070.2966507177034,465.95693779904303 1162,474 C 1253.7033492822966,482.04306220095697 1346.8516746411483,536.5215311004785 1440,591 L 1440,500 L 0,500 Z');
            }
          }</style><defs><linearGradient id='gradient' x1='0%' y1='50%' x2='100%' y2='50%'><stop offset='5%' stop-color='#F78DA7'></stop><stop offset='95%' stop-color='#8ED1FC'></stop></linearGradient></defs><path d='M 0,500 L 0,291 C 94.30622009569379,281.7942583732057 188.61244019138758,272.58851674641147 291,278 C 393.3875598086124,283.41148325358853 503.8564593301435,303.4401913875598 605,350 C 706.1435406698565,396.5598086124402 797.9617224880383,469.6507177033493 889,487 C 980.0382775119617,504.3492822966507 1070.2966507177034,465.95693779904303 1162,474 C 1253.7033492822966,482.04306220095697 1346.8516746411483,536.5215311004785 1440,591 L 1440,500 L 0,500 Z' stroke='none' stroke-width='0' fill='url(#gradient)' fill-opacity='1' class='transition-all duration-300 ease-in-out delay-150 path-1'></path></svg>"
);

nfSVGStatic = "data:image/svg+xml;utf8," &EncodeUrl("<svg width='100%' height='100%' id='svg' viewBox='0 0 1440 590' xmlns='http://www.w3.org/2000/svg' class='transition duration-300 ease-in-out delay-150'><defs><linearGradient id='gradient' x1='0%' y1='50%' x2='100%' y2='50%'><stop offset='5%' stop-color='#F78DA7'></stop><stop offset='95%' stop-color='#8ED1FC'></stop></linearGradient></defs><path d='M 0,600 L 0,150 C 110.25837320574163,166.91866028708134 220.51674641148327,183.83732057416267 322,177 C 423.48325358851673,170.16267942583733 516.1913875598086,139.5693779904306 607,153 C 697.8086124401914,166.4306220095694 786.7177033492823,223.88516746411483 878,263 C 969.2822966507177,302.11483253588517 1062.9377990430621,322.8899521531101 1157,351 C 1251.0622009569379,379.1100478468899 1345.531100478469,414.555023923445 1440,450 L 1440,600 L 0,600 Z' stroke='none' stroke-width='0' fill='url(#gradient)' fill-opacity='0.53' class='transition-all duration-300 ease-in-out delay-150 path-0'></path><defs><linearGradient id='gradient' x1='0%' y1='50%' x2='100%' y2='50%'><stop offset='5%' stop-color='#F78DA7'></stop><stop offset='95%' stop-color='#8ED1FC'></stop></linearGradient></defs><path d='M 0,600 L 0,350 C 89.98086124401917,317.5598086124402 179.96172248803833,285.1196172248804 289,290 C 398.03827751196167,294.8803827751196 526.1339712918659,337.0813397129187 611,398 C 695.8660287081341,458.9186602870813 737.5023923444977,538.555023923445 825,566 C 912.4976076555023,593.444976076555 1045.8564593301435,568.6985645933014 1156,574 C 1266.1435406698565,579.3014354066986 1353.0717703349283,614.6507177033493 1440,650 L 1440,600 L 0,600 Z' stroke='none' stroke-width='0' fill='url(#gradient)' fill-opacity='1' class='transition-all duration-300 ease-in-out delay-150 path-1'></path></svg>");
nfData = Table(
    {
        vendorId: "V001",
        vendorName: "Vendor A",
        manuallyProcessedInApp: false,
        poNumber: "PO12345",
        warehouseId: "WH01",
        result: "Pending",
        LastModified: DateAdd(
            Now(),
            -2,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Truck",
        linesCount: 10
    },
    {
        vendorId: "V002",
        vendorName: "Vendor B",
        manuallyProcessedInApp: false,
        poNumber: "PO12346",
        warehouseId: "WH02",
        result: "Approved",
        LastModified: DateAdd(
            Now(),
            -5,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Air",
        linesCount: 5
    },
    {
        vendorId: "V003",
        vendorName: "Vendor C",
        manuallyProcessedInApp: true,
        poNumber: "PO12347",
        warehouseId: "WH03",
        result: "Rejected",
        LastModified: DateAdd(
            Now(),
            -10,
            TimeUnit.Days
        ),
        Datasource: "Sharepoint",
        deliveryMethod: "Sea",
        linesCount: 15
    },
    {
        vendorId: "V004",
        vendorName: "Vendor D",
        manuallyProcessedInApp: false,
        poNumber: "PO12348",
        warehouseId: "WH04",
        result: "Pending",
        LastModified: DateAdd(
            Now(),
            -1,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Truck",
        linesCount: 20
    },
    {
        vendorId: "V005",
        vendorName: "Vendor E",
        manuallyProcessedInApp: true,
        poNumber: "PO12349",
        warehouseId: "WH05",
        result: "Approved",
        LastModified: Now(),
        Datasource: "Sharepoint",
        deliveryMethod: "Drone",
        linesCount: 8
    },
    {
        vendorId: "Vendor001",
        vendorName: "Acme Corp",
        manuallyProcessedInApp: false,
        poNumber: "PO12345",
        warehouseId: "WH001",
        result: "Success",
        LastModified: DateAdd(
            Now(),
            -5,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Courier",
        linesCount: 10
    },
    {
        vendorId: "Vendor002",
        vendorName: "Global Supplies",
        manuallyProcessedInApp: false,
        poNumber: "PO67890",
        warehouseId: "WH002",
        result: "Pending",
        LastModified: DateAdd(
            Now(),
            -3,
            TimeUnit.Days
        ),
        Datasource: "Sharepoint",
        deliveryMethod: "Email",
        linesCount: 5
    },
    {
        vendorId: "Vendor003",
        vendorName: "Tech Distributors",
        manuallyProcessedInApp: false,
        poNumber: "PO11223",
        warehouseId: "WH003",
        result: "Failed",
        LastModified: DateAdd(
            Now(),
            -7,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "FTP",
        linesCount: 15
    },
    {
        vendorId: "Vendor004",
        vendorName: "FastTrack Logistics",
        manuallyProcessedInApp: false,
        poNumber: "PO44556",
        warehouseId: "WH004",
        result: "Success",
        LastModified: DateAdd(
            Now(),
            -1,
            TimeUnit.Days
        ),
        Datasource: "Sharepoint",
        deliveryMethod: "Courier",
        linesCount: 8
    },
    {
        vendorId: "Vendor005",
        vendorName: "Northern Lights",
        manuallyProcessedInApp: false,
        poNumber: "PO77889",
        warehouseId: "WH005",
        result: "Pending",
        LastModified: DateAdd(
            Now(),
            -2,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Email",
        linesCount: 20
    },
        // Additional Rows

    {
        vendorId: "Vendor006",
        vendorName: "NextGen Supplies",
        manuallyProcessedInApp: false,
        poNumber: "PO33445",
        warehouseId: "WH006",
        result: "Success",
        LastModified: DateAdd(
            Now(),
            -6,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Courier",
        linesCount: 12
    },
    {
        vendorId: "Vendor007",
        vendorName: "Alpha Distributors",
        manuallyProcessedInApp: false,
        poNumber: "PO55667",
        warehouseId: "WH007",
        result: "Failed",
        LastModified: DateAdd(
            Now(),
            -4,
            TimeUnit.Days
        ),
        Datasource: "Sharepoint",
        deliveryMethod: "Email",
        linesCount: 6
    },
    {
        vendorId: "Vendor008",
        vendorName: "Global Traders",
        manuallyProcessedInApp: false,
        poNumber: "PO88990",
        warehouseId: "WH008",
        result: "Pending",
        LastModified: DateAdd(
            Now(),
            -9,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "FTP",
        linesCount: 9
    },
    {
        vendorId: "Vendor009",
        vendorName: "Pro Logistics",
        manuallyProcessedInApp: false,
        poNumber: "PO99887",
        warehouseId: "WH009",
        result: "Success",
        LastModified: DateAdd(
            Now(),
            -8,
            TimeUnit.Days
        ),
        Datasource: "Sharepoint",
        deliveryMethod: "Courier",
        linesCount: 11
    },
    {
        vendorId: "Vendor010",
        vendorName: "Blue Horizons",
        manuallyProcessedInApp: false,
        poNumber: "PO12399",
        warehouseId: "WH010",
        result: "Failed",
        LastModified: DateAdd(
            Now(),
            -10,
            TimeUnit.Days
        ),
        Datasource: "Dataverse",
        deliveryMethod: "Email",
        linesCount: 4
    }
);

nfAdminUser =
    
       LookUp(
        [@'Security Roles'],
        "System Administrator" in Name,
        Role
    ) in Concat(
        LookUp(
            [@Users],
            'Primary Email' = User().Email
        ).'Security Roles (systemuserroles_association)',
        Role & ";"
    );

    
    /* If(LookUp(
        [@'Security Roles'],
        "System Administrator" in Name,
        Role
    ) in Concat(
        LookUp(
            [@Users],
            'Primary Email' = User().Email
        ).'Security Roles (systemuserroles_association)',
        Role & ";"
    ),true, false);*/