<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HNB Global Network</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #e6f2ff;
            color: #003366;
        }
        h1 {
            text-align: center;
            color: #1e5f8c;
            margin-bottom: 30px;
        }
        label {
            font-weight: bold;
            color: #2a5885;
            display: block;
            margin-bottom: 10px;
        }
        select {
            width: 100%;
            padding: 12px;
            margin-bottom: 25px;
            font-size: 16px;
            border: 1px solid #a8c6e0;
            background-color: #f0f8ff;
            border-radius: 4px;
        }
        .section {
            margin-bottom: 30px;
            background-color: #f0f8ff;
            padding: 20px;
            border: 1px solid #a8c6e0;
            border-radius: 6px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .section-title {
            color: #1e5f8c;
            border-bottom: 1px solid #a8c6e0;
            padding-bottom: 10px;
            margin-bottom: 15px;
            font-size: 18px;
        }
        .item {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px dashed #a8c6e0;
        }
        .item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        .item-name {
            font-weight: bold;
            color: #1e5f8c;
            font-size: 16px;
            margin-bottom: 5px;
        }
        .item-detail {
            font-size: 14px;
            color: #4a6b8a;
            margin: 3px 0;
        }
        .item-contact {
            font-weight: bold;
        }
        .detail-row {
            margin-bottom: 10px;
            display: flex;
            align-items: flex-start;
        }
        .detail-label {
            font-weight: bold;
            width: 120px;
            flex-shrink: 0;
            color: #2a5885;
        }
        .detail-value {
            flex-grow: 1;
        }
        .rep-name {
            color: #0066cc;
            font-weight: bold;
        }
        .vacation-note {
            font-style: italic;
            color: #666;
            margin-left: 5px;
        }
        .no-data {
            text-align: center;
            color: #666;
            font-style: italic;
            padding: 15px;
        }
    </style>
</head>
<body>
    <h1>HNB Global Network</h1>
    
    <label for="country-select">Select a Country:</label>
    <select id="country-select">
        <option value="">-- Select a Country --</option>
        <option value="argentina">Argentina</option>
        <option value="australia">Australia</option>
        <option value="austria">Austria</option>
        <option value="bahrain">Bahrain</option>
        <option value="bangladesh">Bangladesh</option>
        <option value="belgium">Belgium</option>
        <option value="bolivia">Bolivia</option>
        <option value="brazil">Brazil</option>
        <option value="bulgaria">Bulgaria</option>
        <option value="canada">Canada</option>
        <option value="channel-islands">Channel Islands</option>
        <option value="chile">Chile</option>
        <option value="china">China</option>
        <option value="colombia">Colombia</option>
        <option value="cyprus">Cyprus</option>
        <option value="czech-republic">Czech Republic</option>
        <option value="denmark">Denmark</option>
        <option value="ecuador">Ecuador</option>
        <option value="egypt">Egypt</option>
        <option value="ethiopia">Ethiopia</option>
        <option value="finland">Finland</option>
        <option value="france">France</option>
        <option value="germany">Germany</option>
        <option value="georgia">Georgia</option>
        <option value="greece">Greece</option>
        <option value="hong-kong">Hong Kong</option>
        <option value="hungary">Hungary</option>
        <option value="india">India</option>
        <option value="indonesia">Indonesia</option>
        <option value="ireland">Ireland</option>
        <option value="isle-of-man">Isle of Man</option>
        <option value="israel">Israel</option>
        <option value="italy">Italy</option>
        <option value="japan">Japan</option>
        <option value="jordan">Jordan</option>
        <option value="kenya">Kenya</option>
        <option value="south-korea">South Korea</option>
        <option value="kosovo">Kosovo</option>
        <option value="kuwait">Kuwait</option>
        <option value="latvia">Latvia</option>
        <option value="lebanon">Lebanon</option>
        <option value="liechtenstein">Liechtenstein</option>
        <option value="luxembourg">Luxembourg</option>
        <option value="malaysia">Malaysia</option>
        <option value="maldives">Maldives</option>
        <option value="mauritius">Mauritius</option>
        <option value="macedonia">North Macedonia</option>
        <option value="mexico">Mexico</option>
        <option value="nepal">Nepal</option>
        <option value="netherlands">Netherlands</option>
        <option value="new-zealand">New Zealand</option>
        <option value="norway">Norway</option>
        <option value="oman">Oman</option>
        <option value="pakistan">Pakistan</option>
        <option value="peru">Peru</option>
        <option value="philippines">Philippines</option>
        <option value="poland">Poland</option>
        <option value="portugal">Portugal</option>
        <option value="qatar">Qatar</option>
        <option value="romania">Romania</option>
        <option value="saudi-arabia">Saudi Arabia</option>
        <option value="seychelles">Seychelles</option>
        <option value="slovenia">Slovenia</option>
        <option value="south-africa">South Africa</option>
        <option value="singapore">Singapore</option>
        <option value="slovakia">Slovakia</option>
        <option value="spain">Spain</option>
        <option value="sweden">Sweden</option>
        <option value="switzerland">Switzerland</option>
        <option value="taiwan">Taiwan</option>
        <option value="thailand">Thailand</option>
        <option value="turkey">Turkey</option>
        <option value="uae">United Arab Emirates</option>
        <option value="uk">United Kingdom</option>
        <option value="usa">United States</option>
        <option value="vietnam">Vietnam</option>
    </select>
    
    <div id="results-container">
        <!-- Content will be dynamically generated here -->
    </div>

    <script>
        // Exchange Houses Data
        const exchangeData = {
            "argentina": [
                { name: "Banco de la Nación Argentina", address: "Bartolomé Mitre 326, C1036AAH CABA, Argentina", contact: "+54 11 4347 6000" }
            ],
            "australia": [
                { name: "Aussie Forex and Finance Pty Ltd", address: "Level 5, 20 Hunter St, Sydney NSW 2000", contact: "+61 2 9235 1700" },
                { name: "CESA – Fast Cash PTY Ltd", address: "225 Bourke St, Melbourne VIC 3000", contact: "+61 3 9663 3577" },
                { name: "Ceylon Exchange Pty Ltd", address: "Shop 3, 90 Queen St, Brisbane QLD 4000", contact: "+61 7 3221 6777" },
                { name: "Commonwealth Bank of Australia", address: "48 Martin Place, Sydney NSW 2000", contact: "+61 2 9999 9999" },
                { name: "Lanka Currency Converter", address: "Shop 5, 800 Hay St, Perth WA 6000", contact: "+61 8 9321 8000" },
                { name: "National Australia Bank", address: "500 Bourke St, Melbourne VIC 3000", contact: "+61 3 8641 9083" },
                { name: "Yola Holdings Pvt Ltd", address: "91 King William St, Adelaide SA 5000", contact: "+61 8 8212 5000" }
            ],
            "austria": [
                { name: "Small World Financial Services", address: "Graben 21, 1010 Vienna, Austria", contact: "+43 1 532 0456" }
            ],
            "bahrain": [
                { name: "Bahrain Financing Co.", address: "Government Ave, Manama, Bahrain", contact: "+973 1721 1721" },
                { name: "National Finance and Exchange Co. WLL", address: "Building 59, Road 1701, Riffa, Bahrain", contact: "+973 1761 1761" },
                { name: "Zenj Exchange Co.", address: "Muharraq High St, Muharraq, Bahrain", contact: "+973 1733 1733" }
            ],
            "bangladesh": [
                { name: "AB Bank Ltd", address: "BCIC Bhaban, 30-31 Dilkusha C/A, Dhaka 1000, Bangladesh", contact: "+880 2 956 0311" },
                { name: "Mercantile Bank Ltd", address: "61 Dilkusha Commercial Area, Dhaka 1000, Bangladesh", contact: "+880 2 956 0312" }
            ],
            "belgium": [
                { name: "Small World Financial Services", address: "Avenue Louise 250, 1050 Brussels, Belgium", contact: "+32 2 640 5100" }
            ],
            "bolivia": [
                { name: "Banco BISA SA", address: "PO Box 1290, Avenida 16 de Julio, (Paseo El Prado) 1628, La Paz, Bolivia", contact: "" }
            ],
            "brazil": [
                { name: "Small World Brasil Servicos Financeiros", address: "Av. Paulista 2000, São Paulo, Brazil", contact: "+55 11 3016 4000" }
            ],
            "bulgaria": [
                { name: "UniCredit Bulbank", address: "7 Sveta Nedelya Sq, 1000 Sofia, Bulgaria", contact: "+359 2 923 0000" }
            ],
            "canada": [
                { name: "Habib Canadian Bank", address: "70 Yorkville Ave, Toronto, ON M5R 1B9, Canada", contact: "+1 416 963 6100" },
                { name: "Small World Financial Services Canada Ltd", address: "200 Granville St, Vancouver, BC V6C 1S4, Canada", contact: "+1 604 685 1000" }
            ],
            "channel-islands": [
                { name: "HSBC Channel Islands", address: "PO Box 64, St Helier, Jersey JE4 8PP", contact: "+44 1534 616 100" }
            ],
            "chile": [
                { name: "Small World Financial Services Chile SPA", address: "", contact: "" }
            ],
            "china": [
                { name: "Bank of China", address: "1 Fuxingmen Nei Ave, Xicheng District, Beijing, China", contact: "+86 10 6659 6688" }
            ],
            "colombia": [
                { name: "Bancolombia", address: "Carrera 48 #26-85, Medellín, Antioquia, Colombia", contact: "+57 1 343 0000" }
            ],
            "cyprus": [
                { name: "G S Cashline Ltd", address: "Stasikratous 10, Nicosia 1065, Cyprus", contact: "+357 22 761234" },
                { name: "Masari Payment Services Ltd", address: "Agiou Andreou 312, Limassol 3035, Cyprus", contact: "+357 25 345678" },
                { name: "Small World Financial Services", address: "Zinonos Kitieos 1, Larnaca 6023, Cyprus", contact: "+357 24 654321" }
            ],
            "czech-republic": [
                { name: "Česká spořitelna", address: "Olbrachtova 1929/62, 140 00 Praha 4, Czech Republic", contact: "+420 956 711 111" }
            ],
            "denmark": [
                { name: "Danske Bank", address: "Holmens Kanal 2-12, 1092 Copenhagen, Denmark", contact: "+45 33 44 00 00" },
                { name: "Small World Financial Services", address: "Sønder Alle 15, 8000 Aarhus, Denmark", contact: "+45 86 12 34 56" }
            ],
            "ecuador": [
                { name: "Banco Pichincha", address: "Av. Amazonas N37-29 y Naciones Unidas, Quito, Ecuador", contact: "+593 2 299 0000" }
            ],
            "egypt": [
                { name: "National Bank of Egypt", address: "1187 Corniche El Nil, Cairo, Egypt", contact: "+20 2 2390 0000" }
            ],
            "ethiopia": [
                { name: "Commercial Bank of Ethiopia", address: "Africa Avenue, Addis Ababa, Ethiopia", contact: "+251 11 551 0055" }
            ],
            "finland": [
                { name: "Small World Financial Services", address: "Aleksanterinkatu 7, 00100 Helsinki, Finland", contact: "+358 9 4242 4242" }
            ],
            "france": [
                { name: "Credit Agricole Corporate & Investment Bank", address: "9 Quai du Président Paul Doumer, 92400 Courbevoie, France", contact: "+33 1 41 89 10 00" },
                { name: "MoneyGlobe SAS", address: "25 Rue de la Villette, 69003 Lyon, France", contact: "+33 4 72 12 34 56" },
                { name: "NEC Money Transfer Ltd", address: "23 Rue Sainte, 13001 Marseille, France", contact: "+33 4 91 56 78 90" }
            ],
            "germany": [
                { name: "Commerzbank AG", address: "Kaiserplatz 1, 60311 Frankfurt, Germany", contact: "+49 69 136 20" },
                { name: "Small World Financial Services", address: "Friedrichstraße 200, 10117 Berlin, Germany", contact: "+49 30 2045 4545" }
            ],
            "georgia": [
                { name: "TBC Bank", address: "7 Marjanishvili St, Tbilisi 0102, Georgia", contact: "+995 32 227 27 27" }
            ],
            "greece": [
                { name: "Small World Financial Services", address: "Stadiou 4, 10562 Athens, Greece", contact: "+30 210 322 2222" }
            ],
            "hong-kong": [
                { name: "HSBC Hong Kong", address: "1 Queen's Road Central, Hong Kong", contact: "+852 2233 3000" }
            ],
            "hungary": [
                { name: "OTP Bank", address: "Nádor u. 16, 1051 Budapest, Hungary", contact: "+36 1 366 3888" }
            ],
            "india": [
                { name: "State Bank of India", address: "Corporate Centre, Madam Cama Road, Mumbai 400021, India", contact: "+91 22 2275 5858" }
            ],
            "indonesia": [
                { name: "Bank Mandiri", address: "Plaza Mandiri, Jl. Gatot Subroto Kav. 36-38, Jakarta 12190, Indonesia", contact: "+62 21 524 5000" }
            ],
            "ireland": [
                { name: "Small World Financial Services", address: "D'Olier Street 33, Dublin 2, Ireland", contact: "+353 1 642 0000" }
            ],
            "isle-of-man": [
                { name: "Isle of Man Bank", address: "2 Victoria St, Douglas IM1 2LN, Isle of Man", contact: "+44 1624 694 694" }
            ],
            "israel": [
                { name: "Global Remit-Currency Services Ltd", address: "Yigal Alon St 98, Tel Aviv, Israel", contact: "+972 3 624 4000" },
                { name: "Tifco Logistics & Trade Ltd", address: "Jaffa St 34, Jerusalem, Israel", contact: "+972 2 625 5555" }
            ],
            "italy": [
                { name: "NEC Money Transfer Ltd", address: "Via del Corso 306, 00186 Rome, Italy", contact: "+39 06 678 9012" },
                { name: "Small World Financial Services", address: "Via della Moscova 33, 20121 Milan, Italy", contact: "+39 02 3045 6789" }
            ],
            "japan": [
                { name: "MUFG Bank", address: "7-1, Marunouchi 2-Chome, Chiyoda-ku, Tokyo 100-8330, Japan", contact: "+81 3 3240 1111" }
            ],
            "jordan": [
                { name: "Alawneh Exchange LLC", address: "King Hussein St 15, Amman, Jordan", contact: "+962 6 566 6171" }
            ],
            "kenya": [
                { name: "Equity Bank Kenya", address: "Equity Centre, Hospital Road, Upper Hill, Nairobi, Kenya", contact: "+254 703 018 000" }
            ],
            "south-korea": [
                { name: "E9Pay Company Ltd", address: "", contact: "" },
                { name: "KEB Hana Bank", address: "Jungang-daero 91, Jung-gu, Busan, South Korea", contact: "+82 51 662 2000" },
                { name: "Kookmin Bank", address: "Songdo-dong 1, Yeonsu-gu, Incheon, South Korea", contact: "+82 32 729 6114" },
                { name: "Woori Bank", address: "203 Hoehyeon-dong, 1-ga, Jung-gu, Seoul, South Korea", contact: "" }
            ],
            "kosovo": [
                { name: "Raiffeisen Bank Kosovo", address: "Prishtina 10000, Kosovo", contact: "+383 38 222 222" }
            ],
            "kuwait": [
                { name: "Al Mulla International Exchange Co. WLL", address: "Ahmed Al Jaber St, Kuwait City, Kuwait", contact: "+965 2225 0000" },
                { name: "Almuzaini Exchange Co. SAK", address: "Beirut St, Hawalli, Kuwait", contact: "+965 2565 5555" },
                { name: "Aman Exchange Co.WLL", address: "Salem Al Mubarak St, Salmiya, Kuwait", contact: "+965 2573 3333" },
                { name: "Bahrain Exchange Co. WLL", address: "", contact: "" },
                { name: "Joyalukkas Exchange Co. WLL", address: "", contact: "" },
                { name: "National Money Exchange Co. WLL", address: "", contact: "" }
            ],
            "latvia": [
                { name: "Swedbank Latvia", address: "Balasta dambis 1a, Riga LV-1048, Latvia", contact: "+371 67 444 444" }
            ],
            "lebanon": [
                { name: "Banque Libano Francaise", address: "Rue Clemençeau, Beirut, Lebanon", contact: "+961 1 333 111" }
            ],
            "liechtenstein": [
                { name: "Liechtensteinische Landesbank", address: "Städtle 44, 9490 Vaduz, Liechtenstein", contact: "+423 236 88 11" }
            ],
            "luxembourg": [
                { name: "Small World Financial Services", address: "Avenue de la Liberté 1, Luxembourg City, Luxembourg", contact: "+352 26 44 12 34" }
            ],
            "malaysia": [
                { name: "Merchantrade Asia SDN BHD", address: "Jalan Sultan Ismail, Kuala Lumpur, Malaysia", contact: "+60 3 2026 1888" }
            ],
            "maldives": [
                { name: "Bank of Ceylon", address: "Aage 12, Boduthakurufaanu Magu, Male", contact: "" },
                { name: "Bank of Maldives", address: "Boduthakurufaanu Magu, Malé, Maldives", contact: "+960 333 3333" },
                { name: "The Mauritius Commercial Bank (Maldives) Private Ltd", address: "H. Sifa Building, Boduthakufaanu Magu, Male, Maldives", contact: "" }
            ],
            "mauritius": [
                { name: "AfrAsia Bank Limited", address: "Bowen Square, 10 Dr Ferriere Street, Port Louis, Mauritius", contact: "" }
            ],
            "macedonia": [
                { name: "Stopanska Banka", address: "11 Oktomvri No. 6, 1000 Skopje, North Macedonia", contact: "+389 2 310 3100" }
            ],
            "mexico": [
                { name: "Banco Azteca", address: "Calz. Ignacio Zaragoza 987, Iztapalapa, 09000 Ciudad de México, CDMX, Mexico", contact: "+52 55 1162 1000" }
            ],
            "nepal": [
                { name: "Nepal Investment Bank", address: "Durbar Marg, Kathmandu 44600, Nepal", contact: "+977 1-5970000" }
            ],
            "netherlands": [
                { name: "Small World Financial Services", address: "De Entree 201, 1101 Amsterdam, Netherlands", contact: "+31 20 799 9999" }
            ],
            "new-zealand": [
                { name: "ANZ Bank New Zealand", address: "23-29 Albert St, Auckland 1010, New Zealand", contact: "+64 9 357 4000" }
            ],
            "norway": [
                { name: "DNB Bank ASA", address: "Dronning Eufemias gate 30, Oslo, Norway", contact: "+47 915 04800" },
                { name: "Small World Financial Services", address: "Olav Kyrres gate 7, Bergen, Norway", contact: "+47 55 33 33 33" }
            ],
            "oman": [
                { name: "Joyalukkas Exchange LLC", address: "Al Khuwair, Muscat, Oman", contact: "+968 24 799900" },
                { name: "Oman Arab Bank", address: "Al Nahdah St, Salalah, Oman", contact: "+968 23 295555" },
                { name: "Sohar International Bank SAOG", address: "Al Harthy Complex, Sohar, Oman", contact: "+968 26 840000" }
            ],
            "pakistan": [
                { name: "Askari Bank Limited", address: "AWT Plaza, The Mall, Rawalpindi 46000, Pakistan", contact: "" },
                { name: "Bank Al Falah Ltd", address: "B.A. Building, I.I. Chundrigar Rd, Karachi, Pakistan", contact: "+92 21 32446939" },
                { name: "Bank Al Habib Ltd", address: "Sharif Plaza, The Mall, Lahore, Pakistan", contact: "+92 42 36308000" },
                { name: "Bank Islami Pakistan Ltd", address: "11th Floor, Executive Tower, Dolmen City, Karachi", contact: "" },
                { name: "Habib Metropolitan Bank Ltd", address: "Spencer's Building, I.I. Chundrigar Road, Karachi", contact: "" },
                { name: "Silk Bank Ltd", address: "Silk Bank Building, I.I. Chundrigar Road, Karachi", contact: "" },
                { name: "Sindh Bank Ltd", address: "3rd Floor, Federation House, Clifton, Karachi", contact: "" },
                { name: "Summit Bank Ltd", address: "Plot No. 6B, F-6 Super Market, Islamabad", contact: "" }
            ],
            "peru": [
                { name: "Banco de Crédito del Perú", address: "Calle Centenario 156, La Molina, Lima 15026, Peru", contact: "+51 1 211 9500" }
            ],
            "philippines": [
                { name: "BDO Unibank", address: "BDO Corporate Center, 7899 Makati Avenue, Makati City 0726, Philippines", contact: "+63 2 8840 7000" }
            ],
            "poland": [
                { name: "PKO Bank Polski", address: "ul. Puławska 15, 02-515 Warszawa, Poland", contact: "+48 22 599 0000" }
            ],
            "portugal": [
                { name: "Small World Financial Services", address: "Avenida da Liberdade 110, Lisbon, Portugal", contact: "+351 21 317 6000" }
            ],
            "qatar": [
                { name: "Al Dar For Exchange Works", address: "Al Sadd St, Doha, Qatar", contact: "+974 44 444 444" },
                { name: "Al Fardan Exchange Co.", address: "Al Wakrah Main Rd, Al Wakrah, Qatar", contact: "+974 44 666 666" },
                { name: "Al Mirqab Exchange Co. WLL", address: "", contact: "" },
                { name: "Al Zaman Exchange WLL", address: "", contact: "" },
                { name: "City Exchange Company WLL", address: "", contact: "" },
                { name: "Doha Bank QSC", address: "", contact: "" },
                { name: "Habib Qatar International Exchange Ltd", address: "", contact: "" },
                { name: "Islamic Exchange Co.", address: "", contact: "" }
            ],
            "romania": [
                { name: "Small World Financial Services", address: "Calea Victoriei 15, Bucharest, Romania", contact: "+40 21 310 3030" }
            ],
            "saudi-arabia": [
                { name: "Al Rajhi Banking & Investment Corporation", address: "King Abdullah Rd, Riyadh, Saudi Arabia", contact: "+966 11 211 6000" },
                { name: "Arab National Bank", address: "King Abdulaziz St, Jeddah, Saudi Arabia", contact: "+966 12 611 2222" },
                { name: "Bank Al Bilad", address: "Al Malaz-Sitteen Street, Riyadh", contact: "" }
            ],
            "seychelles": [
                { name: "Cash Plus Co Pty Ltd", address: "Francis Rachel St, Victoria, Seychelles", contact: "+248 4 293 000" },
                { name: "Doubleclick Exchange Pty Ltd", address: "Anse Boileau, Seychelles", contact: "+248 4 388 888" }
            ],
            "slovenia": [
                { name: "Small World Financial Services", address: "", contact: "" }
            ],
            "south-africa": [
                { name: "Standard Bank South Africa", address: "30 Baker St, Rosebank, Johannesburg, 2196, South Africa", contact: "+27 11 636 9111" }
            ],
            "singapore": [
                { name: "DBS Bank", address: "12 Marina Blvd, Marina Bay Financial Centre Tower 3, Singapore 018982", contact: "+65 6327 2265" }
            ],
            "slovakia": [
                { name: "VUB Banka", address: "Mlynské nivy 1, 829 90 Bratislava, Slovakia", contact: "+421 2 5955 1111" }
            ],
            "spain": [
                { name: "iTransfer Global Payments EPSA", address: "Calle de Alcalá 44, Madrid, Spain", contact: "+34 91 123 4567" },
                { name: "Small World Financial Services", address: "Passeig de Gràcia 11, Barcelona, Spain", contact: "+34 93 456 7890" },
                { name: "Titanes Telecomunicaciones SA", address: "", contact: "" }
            ],
            "sweden": [
                { name: "Small World Financial Services", address: "Kungsgatan 8, Stockholm, Sweden", contact: "+46 8 123 4567" }
            ],
            "switzerland": [
                { name: "Habib Bank AG Zurich", address: "Bahnhofstrasse 88, Zurich, Switzerland", contact: "+41 44 219 1111" },
                { name: "Swiss Transfers GmbH", address: "Rue du Rhône 100, Geneva, Switzerland", contact: "+41 22 818 8888" }
            ],
            "taiwan": [
                { name: "CTBC Bank", address: "No. 168, Jingmao 2nd Rd, Nangang District, Taipei City, Taiwan 115", contact: "+886 2 2182 1313" }
            ],
            "thailand": [
                { name: "Bangkok Bank", address: "333 Silom Road, Bangrak, Bangkok 10500, Thailand", contact: "+66 2 645 5555" }
            ],
            "turkey": [
                { name: "Ziraat Bankası", address: "Atatürk Bulvarı No:8, Ulus, 06050 Altındağ/Ankara, Turkey", contact: "+90 312 584 2000" }
            ],
            "uae": [
                { name: "Abu Dhabi Commercial Bank", address: "Khalifa St, Abu Dhabi, UAE", contact: "+971 2 616 0000" },
                { name: "Al Ahalia Money Exchange Bureau", address: "Al Mankhool Rd, Dubai, UAE", contact: "+971 4 396 8888" },
                { name: "Al Ansari Exchange Estb.", address: "", contact: "" },
                { name: "Al Fardan Exchange", address: "", contact: "" },
                { name: "Al Fuad Exchange", address: "", contact: "" },
                { name: "Delma Exchange", address: "", contact: "" },
                { name: "Economic Exchange Centre", address: "", contact: "" },
                { name: "Emirates NBD Bank PJSC", address: "Baniyas Road, Deira, Dubai, UAE", contact: "+971 4 609 0000" },
                { name: "Emirates Islamic Bank PJSC", address: "", contact: "" },
                { name: "Federal Exchange", address: "", contact: "" },
                { name: "GCC Exchange", address: "", contact: "" },
                { name: "Habib Bank AG Zurich", address: "", contact: "" },
                { name: "Index Exchange LLC", address: "", contact: "" },
                { name: "Joyalukkas Exchange", address: "", contact: "" },
                { name: "Lari Exchange Estb.", address: "", contact: "" },
                { name: "Lu Lu International Exchange LLC", address: "", contact: "" },
                { name: "Multinet Trust Exchange LLC", address: "", contact: "" },
                { name: "National Bank of Fujairah", address: "", contact: "" },
                { name: "National Bank of R.A.K PSC", address: "", contact: "" },
                { name: "National Bank of U.A.Q PSC", address: "", contact: "" },
                { name: "Redha Al-Ansari Exchange Estb.", address: "", contact: "" },
                { name: "Sharaf Exchange LLC", address: "", contact: "" },
                { name: "Sharjah Islamic Bank", address: "", contact: "" },
                { name: "Universal Exchange Centre", address: "", contact: "" },
                { name: "Wall Street Exchange Centre", address: "", contact: "" },
                { name: "Worldwide Cash Express Ltd", address: "", contact: "" }
            ],
            "uk": [
                { name: "AMO Money Transfer & Exchange Ltd", address: "", contact: "" },
                { name: "Barclays Bank Plc", address: "1 Churchill Place, London E14 5HP, UK", contact: "+44 20 7116 1000" },
                { name: "Global Exchange Ltd", address: "", contact: "" },
                { name: "iFast Global Bank Ltd", address: "", contact: "" },
                { name: "Lanka Services Ltd", address: "", contact: "" },
                { name: "LCC Trans-Sending Ltd", address: "", contact: "" },
                { name: "NEC Money Transfer Ltd", address: "", contact: "" },
                { name: "Tangopay Ltd", address: "", contact: "" },
                { name: "Taptap Send UK Ltd", address: "", contact: "" },
                { name: "Teeparam Exchange Ltd", address: "", contact: "" }
            ],
            "usa": [
                { name: "Choice Money Transfer Inc.", address: "", contact: "" },
                { name: "Citibank NA", address: "388 Greenwich St, New York, NY 10013, USA", contact: "+1 212 559 1000" },
                { name: "Deutsche Bank Trust Company Americas", address: "", contact: "" },
                { name: "Habib American Bank", address: "", contact: "" },
                { name: "JPMorgan Chase Bank", address: "270 Park Ave, New York, NY 10017, USA", contact: "+1 212 270 6000" },
                { name: "Mastercard Transaction Services (US) LLC", address: "", contact: "" },
                { name: "PayPal Pvt Ltd", address: "", contact: "" },
                { name: "Placid NK Corporation", address: "", contact: "" },
                { name: "Prabhu Money Transfer", address: "", contact: "" },
                { name: "Standard Chartered Bank", address: "", contact: "" }
            ],
            "vietnam": [
                { name: "Vietcombank", address: "198 Tran Quang Khai, Hoan Kiem, Hanoi, Vietnam", contact: "+84 24 3934 5932" }
            ]
        };

        // Correspondent Banks Data
        const correspondentData = {
            "argentina": [
                { name: "Banco de la Nación Argentina", address: "Bartolomé Mitre 326, C1036AAH CABA, Argentina", contact: "+54 11 4347 6000", swift: "NACNARBA" },
                { name: "BBVA Banco Francés SA", address: "Reconquista 199, Capital Federal, 1003 Buenos Aires, Argentina", contact: "", swift: "BFRPARBA" }
            ],
            "australia": [
                { name: "Commonwealth Bank of Australia", address: "48 Martin Place, Sydney NSW 2000, Australia", contact: "+61 2 9999 9999", swift: "CTBAAU2S" },
                { name: "Australia and New Zealand Banking Group Limited (ANZ Bank)", address: "ANZ Centre Melbourne, Level 9, 833 Collins Street, Docklands, VIC 3008, Australia", contact: "", swift: "ANZBAU3M" },
                { name: "Citigroup Pty Limited", address: "2 Park Street, Sydney, NSW 2000, Australia", contact: "", swift: "CITIAU2X" },
                { name: "Commonwealth Bank of Australia", address: "Commonwealth bank Place south, Level 1,11 Harbour street, Sydney, NSW 2000, Australia", contact: "", swift: "CTBAAU2S" },
                { name: "HSBC Bank Australia Limited", address: "Level 36, Tower 1, International Towers Sydney,100 barangaroo avenue, Sydney, NSW 2000, Australia", contact: "", swift: "HKBAAU2S" },
                { name: "JPMorgan Chase Bank NA, Australia", address: "85, Castlereagh Street, Sydney, NSW 2000, Australia", contact: "", swift: "CHASAU2X" },
                { name: "National Australia Bank Ltd", address: "800 Bourke Street, Docklands, Melbourne, VIC 3008, Australia", contact: "", swift: "NATAAU33" }
            ],
            "austria": [
                { name: "Erste Bank der oesterreichischen Sparkassen AG", address: "Am Belvedere 1, 1100 Vienna, Austria", contact: "", swift: "GIBAATWW" },
                { name: "Erste Group Bank AG", address: "Am Belvedere 1,1100, Vienna, Austria", contact: "", swift: "GIBAATWG" },
                { name: "Raiffeisenlandesbank Niederösterreich-Wien AG", address: "Friedrich-Wilhelm-Raiffeisen-Platz 1, A-1020 Vienna, Austria", contact: "", swift: "RLNWATWW" },
                { name: "Raiffeisen-Landesbank Steiermark AG", address: "Radetzkystrasse 15, 8010 Graz, Steiermark, Austria", contact: "", swift: "RZSTAT2G" },
                { name: "UniCredit Bank Austria AG", address: "Rothschildplatz 1,1020, Vienna, Austria", contact: "", swift: "BKAUATWW" }
            ],
            "bahrain": [
                { name: "Alubaf Arab International Bank BSC (c)", address: "Alubaf Tower, Bulding 854, Road 3618, Avenue 436, AL seef District,Manama, Bahrain", contact: "", swift: "ALUBBHBM" },
                { name: "Arab Banking Corporation (BSC)", address: "P O Box 5698, ABC Tower, Diplomatic Area, Manama, Bahrain", contact: "", swift: "ABCOBHBM" },
                { name: "BBK BSC", address: "PO Box 597, 43 Government Avenue, Manama 305, Bahrain", contact: "", swift: "BBKUBHBM" },
                { name: "National Bank of Bahrain BSC", address: "PO Box 106, Government Avenue, Manama, Bahrain", contact: "", swift: "NBOBBHBM" }
            ],
            "bangladesh": [
                { name: "AB Bank Limited", address: "Corporate Head Office, 'The Skymark', 18 Gulshan Avenue, Gulshan – 1Dhaka, 1212, Dhaka, Bangladesh", contact: "", swift: "ABBLBDDH" },
                { name: "Jamuna Bank Limited", address: "Jamuna Bank Tower, Plot #14, Bir Uttam A. K. Khandaker Road, Block# C, Gulshan-1 Dhaka, Bangladesh", contact: "", swift: "JAMUBDDH" },
                { name: "Mercantile Bank Lmited", address: "61 Dilkusha Commercial Area, Dhaka 1000, Dhaka, Dhaka, Bangladesh", contact: "", swift: "MBLBBDDH" },
                { name: "Standard Chartered Bank", address: "Alico Building, 18-20 Motijheel C/A, Dhaka 1000, Bangladesh", contact: "", swift: "SCBLBDDX" }
            ],
            "belgium": [
                { name: "Belfius Bank SA/NV", address: "Place Charles Rogier 11 B, 1000 Brussels, Belgium", contact: "", swift: "GKCCBEBB" },
                { name: "BNP Paribas Fortis SA/NV", address: "2FA3A Jodenstraat 172000, Antwerp Antwerpen,Belgium", contact: "", swift: "GEBABEBB" },
                { name: "KBC Bank NV", address: "Havenlaan 2, 1080 Brussels, Belgium", contact: "", swift: "KREDBEBB" }
            ],
            "bolivia": [
                { name: "Banco BISA SA", address: "PO Box 1290, Avenida 16 de Julio, (Paseo El Prado) 1628, La Paz, Bolivia", contact: "", swift: "" }
            ],
            "brazil": [
                { name: "Banco Citibank SA", address: "Andar 2° Parte, Avenida Paulista 1111, 01311-920 Bela Vista, SP, Brazil", contact: "", swift: "CITIBRBR" }
            ],
            "bulgaria": [
                { name: "UniCredit Bulbank AD", address: "7 Sveta Nedelya Sq, 1000 Sofia, Bulgaria", contact: "", swift: "UNCRBGSF" }
            ],
            "canada": [
                { name: "Canadian Imperial Bank of Commerce (CIBC)", address: "81 Bay Street, CIBC Square, Toronto, ON M5L 1A2, Canada", contact: "", swift: "CIBCCATT" },
                { name: "Habib Canadian Bank", address: "Suite 1-B, 918 Dundas Street East, Mississauga, ON L4Y 4H9, Canada", contact: "", swift: "HBZUCATT" },
                { name: "HSBC Bank Canada", address: "885 West Georgia Street, Vancouver, BC V6C 3E9, Canada", contact: "", swift: "HKBCCATT" },
                { name: "ICICI Bank Canada", address: "ICICI Bank Canada, Don Valley Business Park, 150 Ferrand Drive, Toronto, ON M3C 3E5, Canada", contact: "", swift: "ICICCATT" },
                { name: "JPMorgan Chase Bank, Canada", address: "66 Wellington Street West, Suite 4500, TD Bank Tower, Toronto Ontario M5K 1 E7, Canada", contact: "", swift: "CHASCATT" },
                { name: "The Toronto-Dominion Bank (TD; TD Bank Group)", address: "Toronto-Dominion Centre, 55 King Street West and Bay Street, Toronto, ON M5K 1A2, Canada", contact: "", swift: "TDOMCATT" },
                { name: "UBS Bank (Canada)", address: "Suite 800, 154 University Avenue, Toronto, ON M5H 3Z4, Canada", contact: "", swift: "UBSWCATT" }
            ],
            "channel-islands": [
                { name: "(RBS International) The Royal Bank of Scotland International Limited", address: "PO Box 64, Royal Bank House, 71 Bath Street, St. Helier, Jersey JE4 8PJ, Channel Islands", contact: "", swift: "RBOSJESX" }
            ],
            "china": [
                { name: "Agricultural Bank of China Limited", address: "No. 69 Jian Guo Men Nei Avenue, Dongcheng District, Beijing 100005, China", contact: "", swift: "ABOCCNBJ" },
                { name: "Bank of China Limited", address: "1 Fuxingmen Nei Dajie, Beijing 100818, China", contact: "+86 10 6659 6688", swift: "BKCHCNBJ" },
                { name: "Bank of Communications Co Ltd", address: "188 Yin Cheng Zhong Road, Shanghai 200120, China", contact: "", swift: "COMMCNSH" },
                { name: "Bank of Jiangsu Co Ltd", address: "No. 55 Hongwu Road (North), Nanjing, Jiangsu, China", contact: "", swift: "BOJSCNBN" },
                { name: "Bank of Jining Co Ltd", address: "58 Guhuai Rd, Shi Zhong District, Jining 272000, Shandong, China", contact: "", swift: "BKJNCNBJ" },
                { name: "Bank of Ningbo Co Ltd", address: "700 Ningnan south Road, Yinzhou Area, Ningbo 315100, Zhejiang, China", contact: "", swift: "BKNBCN2N" },
                { name: "Bank of RuiFeng", address: "No. 1418 Jinkeqiao Road, Shaoxing 312030, Zhejiang, China", contact: "", swift: "ZSRBCN2S" },
                { name: "Bank of Wenzhou Co Ltd", address: "No. 196 Chezhan Avenue, Wenzhou, Zhejiang, China", contact: "", swift: "WZCBCNSH" },
                { name: "China Construction Bank Corporation", address: "25 Finance Street, Xicheng District, Bejing 100032, China", contact: "", swift: "PCBCCNBJ" },
                { name: "China Development Bank Corporation", address: "29 Fuchengmenwai Street, Beijing 100037, China", contact: "", swift: "SDBCCNBJ" },
                { name: "China Everbright Bank Co Ltd", address: "Jia 25 Everbright Building, 25 Taiping Qiao Avenue, Beijing 100033, China", contact: "", swift: "EVERCNBJ" },
                { name: "China Guangfa Bank Co Ltd", address: "713 Dongfengdong Rd, Guangzhou 510080, Guangdong, China", contact: "", swift: "GDBKCN22" },
                { name: "China Merchants Bank Co Ltd", address: "China Merchants Bank Tower, No. 7088 Shennan Boulevard, Shenzhen 518040, Guangdong, China", contact: "", swift: "CMBCCNBS" },
                { name: "Chongqing Rural Commercial Bank", address: "10 Yanghe East Rd, Jiangbei District, Chongqing 400020, China", contact: "", swift: "CQRBCN22" },
                { name: "Citibank (China) Co Ltd", address: "Citigroup Tower, No 33 Hua Yuan Shi Qiao Road, Pudong, Shanghai 200120, China", contact: "", swift: "CITICNSX" },
                { name: "Hua Xia Bank Co Limited", address: "Hua Xia Bank Mansions, 22 Jianguomennei Street, Dongcheng District, Beijing 100005, China", contact: "", swift: "HXBKCNBJ" },
                { name: "Huishang Bank Corporation Ltd", address: "Huishang Bank Tower, 79 Anqing Road, Hefei 230001, Anhui, China", contact: "", swift: "HFCBCNSH" },
                { name: "Industrial & Commercial Bank of China Limited", address: "55 Fuxingmennei Dajie, Xicheng District, Beijing 100031, China", contact: "", swift: "ICBKCNBJ" },
                { name: "Industrial Bank Co Ltd", address: "Zhong Shan Building, 154 Hudong Road, Fuzhou 350003, Fujian, China", contact: "", swift: "FJIBCNBA" },
                { name: "Industrial Bank Of Korea (China) Limited", address: "30/31 Floor, The Exchange 2, 189 Nanjing Rd, Hpeace District, Tianjin 300050, China", contact: "", swift: "IBKOCNBT" },
                { name: "Jiangsu Jiangyin Rural Commercial Bank Co Ltd", address: "1 Chengjiang Zhong lu, Jiangyin 214431, Jiangsu, China", contact: "", swift: "JYCBCNSH" },
                { name: "Jinan Rural Commercial Bank Co., Ltd", address: "No. 72 Jing Shiyi Road, Jinan 250002, Shandong, China", contact: "", swift: "RFBKCNBJ" },
                { name: "Kookmin Bank ( China) Ltd", address: "Room 01-05 & 08, 19th Floor, Building 1, Jia 6 Jianguo Menwai Ave, Chaoyang Distric, Beijing, China", contact: "", swift: "CZNBCNBJ" },
                { name: "Laishang Bank Co Ltd", address: "No. 137 Longtan East Street, High - tech Development Zone, Laiwu, Shandong, China", contact: "", swift: "LWCBCNBJ" },
                { name: "Linshang Bank Co Ltd", address: "336 Yimeng Road, Linyi 276004, Shandong, China", contact: "", swift: "LYCBCNBL" },
                { name: "Mizuho Bank (China) Ltd", address: "21-23F, Shanghai World Financial Center, 100 Century Avenue, Pudong New Area, Shanghai 200120, China", contact: "", swift: "MHCBCNSH" },
                { name: "Ningbo Yuyao Rural Cooperative Bank", address: "69-87 Xinjian Road, Yuyao, Zhejiang, China", contact: "", swift: "YYBKCN2N" },
                { name: "Ping An Bank Co., Ltd", address: "5047 Shennan Road East, Luohu District, Shenzhen 518001, Guangdong, China", contact: "", swift: "SZDBCNBS" },
                { name: "QiLu Bank Co Ltd", address: "No. 176 Shunhe Street, Shizhong District, Jinan 250001, Shandong, China", contact: "", swift: "JNSHCNBN" },
                { name: "The Export-Import Bank of China", address: "West Tower, Chemsunny World Trade Center, 30 Fuxingmen Neidajie Str., Xicheng District, Beijing 100031, China", contact: "", swift: "EIBCCNBJ" },
                { name: "Yinzhou Bank", address: "88 Min Hui Xi Road, Yinzhou District, Ningbo 315100, Zhejiang, China", contact: "", swift: "YZBKCN2N" },
                { name: "Zhejiang Tailong Commercial Bank Co Ltd", address: "188 Nanguan Road, Luqiao, Taizhou, Zhejiang, China", contact: "", swift: "ZJTLCNBH" },
                { name: "Zhejiang Xiaoshan Rural Cooperative Bank", address: "258 Renmin Road, Xiaoshan, Hangzhou 311201, Zhejiang, China", contact: "", swift: "HXCBCN2H" }
            ],
            "colombia": [
                { name: "Banco Popular", address: "PO Box 6769, Calle 17 No 7- 43, Piso 3, Bogotá, Distrito Capital, Colombia", contact: "", swift: "BPOPCOBB" }
            ],
            "cyprus": [
                { name: "Bank of Cyprus Public Company Limited", address: "51 Stassinos Str - Ayia Paraskevi, Strovolos, Nicosia, Cyprus", contact: "", swift: "BCYPCY2N" },
                { name: "Hellenic Bank Public Company Limited", address: "PO Box 24747, 1394 Nicosia, Cyprus", contact: "", swift: "HEBACY2N" }
            ],
            "czech-republic": [
                { name: "Ceskoslovenska obchodni banka as (CSOB)", address: "Radlicka 333/150, 150 57 Prague 5, Czech Republic", contact: "", swift: "CEKOCZPP" },
                { name: "Montea Money Bank, A.S.", address: "Vyskocilova 1422/1a, BB Centrum, 140 28 Prague 4, Czech Republic", contact: "", swift: "AGBACZPP" },
                { name: "UniCredit Bank Czech Republic as", address: "Zeletavska 1525/1, 140 92 Prague 4, Czech Republic", contact: "", swift: "BACXCZPP" }
            ],
            "denmark": [
                { name: "Danske Bank A/S", address: "Bernstorffsgade 40, DK-1577 Copenhagen, Denmark", contact: "", swift: "DABADKKK" },
                { name: "Jyske Bank A/S", address: "Vestergade 8-16, DK-8600 Silkeborg, Denmark", contact: "", swift: "JYBADKKK" },
                { name: "Nordea Bank AB (publ)", address: "Satamaradankatu 500020, Helsinki,Denmark", contact: "", swift: "NDEADKKK" }
            ],
            "ecuador": [
                { name: "Banco Pichincha CA", address: "Edificio Casa Vivanco Piso 2, Av Amazonas 4600 y Pereira, Quito, Pichincha, Ecuador", contact: "", swift: "PICHECEQ" }
            ],
            "egypt": [
                { name: "Arab International Bank", address: "35 Abdel Khalek Sarwat Street, Cairo, Egypt", contact: "", swift: "ARIBEGCX" },
                { name: "Société Arabe Internationale de Banque (SAIB)", address: "56 Gamaeat El Dowal Al Arabia Street, Mohandessin, Gîza, Cairo, Egypt", contact: "", swift: "SBNKEGCX" }
            ],
            "ethiopia": [
                { name: "Commercial Bank of Ethiopia", address: "PO Box 255, Gambia Street, Addis Ababa, Ethiopia", contact: "", swift: "CBETETAA" }
            ],
            "finland": [
                { name: "Danske Bank A/S", address: "Holmens Kanal 2-121092, Copenhagen,Finland", contact: "", swift: "DABAFIHH" },
                { name: "Nordea Bank AB (publ)", address: "Aleksanterinkatu 36B, FI-00100 Helsinki, Finland", contact: "", swift: "NDEAFIHH" }
            ],
            "france": [
                { name: "Banque Palatine", address: "42 rue d'Anjou, 75382 Paris, France", contact: "", swift: "BSPFFRPP" },
                { name: "BNP Paribas SA", address: "16 Boulevard des Italiens, 75009 Paris, France", contact: "", swift: "BNPAFRPP" },
                { name: "Crédit Agricole Corporate and Investment Bank", address: "9 Quai du Président Paul Doumer, 92920 Paris La Défense Cedex, Dept 92, France", contact: "", swift: "BSUIFRPP" },
                { name: "Crédit Agricole SA", address: "12 Place des Etats-Unis92545, Montrouge, Dept 92, France", contact: "", swift: "AGRIFRPP" },
                { name: "LCL (former LE Crédit Lyonnais)", address: "19 Blvd des Italiens, 75002 Paris, France", contact: "", swift: "CRLYFRPP" },
                { name: "Crédit Mutuel Arkéa", address: "1 Rue Louis Lichou, 29480 Le Relecq-Kerhuon, Dept 29, France", contact: "", swift: "CMBRFR2B" },
                { name: "HSBC Continental Europe", address: "38 Av Kléber75016, Paris,France", contact: "", swift: "CCFRFRPP" },
                { name: "Monte Paschi Banque SA", address: "7 Rue Meyerbeer, 75009 Paris, France", contact: "", swift: "MONTFRPP" },
                { name: "Société Générale", address: "Tour Société Générale, 17 Cours Valmy, 92972 Paris La Défense, Dept 92, France", contact: "", swift: "SOGEFRPP" }
            ],
            "georgia": [
                { name: "TBC Bank JSC", address: "Head Office, 7 Marjanishvili Str, 0102 Tbilisi, Georgia", contact: "", swift: "TBCBGE22" }
            ],
            "germany": [
                { name: "Barclays Bank Ireland PLC", address: "One molesworth street, Dublin, Germany", contact: "", swift: "BARCDEFF" },
                { name: "Commerzbank AG", address: "D-60261 Frankfurt am Main, Germany", contact: "", swift: "COBADEFF" },
                { name: "Deutsche Bank AG", address: "D-60262 Frankfurt am Main, Germany", contact: "", swift: "DEUTDEFF" },
                { name: "Die Sparkasse Bremen AG", address: "Am Brill 1-3, 28195 Bremen, Germany", contact: "", swift: "SBREDE22" },
                { name: "DZ BANK AG Deutsche Zentral-Genossenschaftsbank", address: "Frankfurt am Main, Platz der Republik, D-60265 Frankfurt am Main, Germany", contact: "", swift: "GENODEFF" },
                { name: "Frankfurter Volksbank eG", address: "Postfach 100840, D-60008 Frankfurt am Main, Germany", contact: "", swift: "FFVBDEFF" },
                { name: "Joh. Berenberg, Gossler & Co. KG", address: "Neuer Jungfernstieg 20, 20354 Hamburg, Germany", contact: "", swift: "BEGODEHH" },
                { name: "J.P. Morgan SE", address: "Taunustor 1, 60310, Frankfurt am Main. Germany", contact: "", swift: "CHASDEFX" },
                { name: "Landesbank Baden-Württemberg", address: "Am Hauptbahnhof 2, D-70173 Stuttgart, Germany", contact: "", swift: "SOLADEST" },
                { name: "M.M. Warburg & CO KGaA", address: "Ferdinandstrasse 75, 20095 Hamburg, Germany", contact: "", swift: "WBWCDEHH" },
                { name: "Oldenburgische Landesbank AG", address: "Stau 15-17, D-26122 Oldenburg, Germany", contact: "", swift: "OLBODEH2" },
                { name: "UniCredit Bank GmbH", address: "Postfach 100101, 80311 Munich, Germany", contact: "", swift: "HYVEDEMM" },
                { name: "DZ BANK AG", address: "Platze der Repulik, Frankfurt head, Germany", contact: "", swift: "GENODEDD" }
            ],
            "greece": [
                { name: "Eurobank SA", address: "8 Othonos Street, GR 105 57 Athens, Attica, Greece", contact: "", swift: "ERBKGRAA" },
                { name: "National Bank of Greece SA", address: "86 Aeolou Street, Cotzia Square, GR 102 32 Athens, Attica, Greece", contact: "", swift: "ETHNGRAA" }
            ],
            "hong-kong": [
                { name: "Standard Chartered Bank (Hong Kong) Limited", address: "32nd Floor, Standard Chartered Bank Bldg, 4-4a Des Voeux Rd Central, Hong Kong, Hong Kong", contact: "", swift: "SCBLHKHH" },
                { name: "The Hongkong and Shanghai Banking Corporation Limited", address: "HSBC Main Building, 1 Queen Road Central, Hong Kong, Hong Kong", contact: "", swift: "HSBCHKHH" }
            ],
            "hungary": [
                { name: "Raiffeisen Bank Zrt", address: "Akadémia utca 6, H-1054 Budapest, Hungary", contact: "", swift: "UBRTHUHB" }
            ],
            "india": [
                { name: "Axis Bank Ltd", address: "3rd Floor, Trishul, Opp Samartheshwar Temple, Law Garden, Ellis Bridge Ahmedabad, 380 006, Gujarat, INDIA", contact: "", swift: "AXISINBB" },
                { name: "Bank of Ceylon", address: "No 20/21 Casa Major Road, No 02 (Old No.11) Zerald Garden, Second Lane, Egmore, Chennai,Tamilnadu,India", contact: "", swift: "BCEYIN5M" },
                { name: "Canara Bank", address: "PO Box 6648, 112 J.C. Road, Bangalore 560002, Karnataka, India", contact: "", swift: "CNRBINBB" },
                { name: "Central Bank of India", address: "Chander Mukhi, Nariman Point, Mumbai 400 021, Maharashtra, India (Intl Div)", contact: "", swift: "CBININBB" },
                { name: "City Union Bank Ltd", address: "No 149 T.S.R. Big Street, Kumbakonam 612001, Tanjore District, Tamil Nadu, India", contact: "", swift: "CIUBIN5M" },
                { name: "Dhanlaxmi Bank Limited", address: "Branches in Mumbai, Maharashtra, Mumbai, Maharashtra, India", contact: "", swift: "DLXBINBB" },
                { name: "HDFC Bank Ltd", address: "HDFC Bank House, Senapati Bapat Marg, Lower Parel, Mumbai 400 013, Maharashtra, India", contact: "", swift: "HDFCINBB" },
                { name: "ICICI Bank Limited", address: "ICICI Bank Towers, Vadodara, gujarat , India", contact: "", swift: "ICICINBB" },
                { name: "IDBI Bank Limited", address: "IDBI Tower, WTC Complex, Cuffe Parade, Mumbai 400 005, Maharashtra, India", contact: "", swift: "IBKLINBB" },
                { name: "IDFC First Bank", address: "Naman Chambers, C-32, G Block, Bandra-Kurla Complex, Mumbai 400051, India", contact: "", swift: "IDFBINBB" },
                { name: "Indian Overseas Bank", address: "763 Anna Salai, Chennai 600 002, Chennai, Tamil Nadu, India", contact: "", swift: "IOBAINBB" },
                { name: "IndusInd Bank Ltd", address: "2401 Gen. Thimmayya Road, Cantonment, Pune, 411 001, Maharashtra, India", contact: "", swift: "INDBINBB" },
                { name: "DBS BANK LIMITED", address: "Express Towers, Nariman Point, Mumbai, 400021, Maharashtra, India", contact: "", swift: "LAVBINBB" },
                { name: "Punjab National Bank", address: "7 Bhikhaiji Cama Place, Africa Avenue, New Delhi 110 066, India", contact: "", swift: "PUNBINBB" },
                { name: "Standard Chartered Bank", address: "Mumbai Main -23/25, Mahatma Gandhiroad, Fort, Mumbai 400001, Maharastra, India", contact: "", swift: "SCBL IN BB" },
                { name: "State Bank of India", address: "Corporate Centre, Madame Cama Road, Mumbai 400 021, Maharashtra, India", contact: "+91 22 2275 5858", swift: "SBININBB" },
                { name: "Tamilnad Mercantile Bank Ltd", address: "57 V.E. Road, Tuticorin 628 002, Tuticorin, Tamil Nadu, India", contact: "", swift: "TMBLINBB" },
                { name: "CSB Bank Ltd (The Catholic Syrian Bank Ltd", address: "PO Box 502, St Mary's College Road, Thrissur 680 020, Kerala, India", contact: "", swift: "CSYBIN55" },
                { name: "The Federal Bank Limited", address: "PO Box 103, Federal Towers, Alwaye 683 101, Kerala, India", contact: "", swift: "FDRLINBB" },
                { name: "The Karnataka Bank Ltd", address: "PO Box 599, Mahaveera Circle, Kankanady, Mangalore 575 002, Dakshin Kannad, Karnataka, India", contact: "", swift: "KARBINBB" },
                { name: "The Karur Vysya Bank Ltd", address: "PO Box 21, Erode Road, Karur 639002, Karur District, Tamil Nadu, India", contact: "", swift: "KVBLINBB" },
                { name: "The Saraswat Co-operative Bank Ltd", address: "Saraswat Bank Bhavan, Plot No 953, Appasaheb Marathe Marg, Prabhadevi, Mumbai 400 025, Maharashtra, India", contact: "", swift: "SRCBINBB" },
                { name: "The South Indian Bank Ltd", address: "SIB House, T B Road, Mission Quarters, Thrissur 680 001, Kerala, India", contact: "", swift: "SOININ55" },
                { name: "Union Bank of India", address: "239 Vidhan Bhavan Marg, Nariman Point, Mumbai 400 021, Maharashtra, India", contact: "", swift: "UBININBB" },
                { name: "Yes, Bank Ltd", address: "Nehru Centre, 9th Floor, Discovery of India Building, Dr AB Road, Worli, Mumbai 400 018, Maharashtra, India", contact: "", swift: "YESBINBB" }
            ],
            "indonesia": [
                { name: "PT Bank CIMB Niaga Tbk", address: "Graha Niaga, Jalan Jenderal Sudirman Kaveling 58, Jakarta 12190, Java, Indonesia", contact: "", swift: "BNIAIDJA" },
                { name: "PT Bank DBS Indonesia", address: "Ground Floor & 12th, Permata Plaza, Jalan M H Thamrin Kav 57, Jakarta 10350, Java, Indonesia", contact: "", swift: "DBSBIDJA" },
                { name: "PT Bank Mandiri (Persero) Tbk", address: "Plaza Mandiri, Jl. Jend Gatot Subroto Kav 36-38, Jakarta 12190, Java, Indonesia", contact: "", swift: "BMRIIDJA" },
                { name: "PT Bank Mega Tbk", address: "Menara Bank Mega, Jl Kapten Tendean Kav 12-14 A, Jakarta 12790, Java, Indonesia", contact: "", swift: "MEGAIDJA" },
                { name: "PT Bank Negara Indonesia (Persero) Tbk", address: "Jalan Jendral Sudirman Kav 1, Jakarta 10220, Java, Indonesia", contact: "", swift: "BNINIDJA" },
                { name: "PT Bank OCBC NISP Tbk", address: "OCBC NISP Tower, Jl Prof. Dr. Satiro Kav. 25, Karet Kuningan, Jakarta 12940, Java, Indonesia", contact: "", swift: "NISPIDJA" },
                { name: "PT Bank Pembangunan Daerah Jawa Barat Dan Banten Tbk", address: "Menara Bank Jabar Banten, JI Naripan No 12-14, Bandung 40111, Jawa Barat, Java, Indonesia", contact: "", swift: "PDJBIDJA" },
                { name: "PT Bank Sinarmas Tbk", address: "1st-2nd Floort, Tower 1, JI MH Thamrin No 51, Jakarta 10350, Java, Indonesia", contact: "", swift: "SBJKIDJA" }
            ],
            "ireland": [
                { name: "Bank of Ireland", address: "40 Mespil Road, Dublin 4, Ireland", contact: "", swift: "BOFIIE2D" },
                { name: "Barclays Bank Ireland plc", address: "Two Park Place, Hatch Street, Dublin 2, Ireland", contact: "", swift: "BARCIE2D" },
                { name: "Citibank Europe Plc", address: "1 North Wall Quay, Dublin 1, Ireland", contact: "", swift: "CITIIE2X" }
            ],
            "isle-of-man": [
                { name: "Isle of Man Bank Limited", address: "PO Box 13, 2 Athol Street, Douglas, IM99 1AN, Isle of Man", contact: "", swift: "RBOSIMD2" }
            ],
            "israel": [
                { name: "Bank Hapoalim BM", address: "PO Box 27, 50 Rothschild Blvd, Tel Aviv 61000, Israel", contact: "", swift: "POALILIT" },
                { name: "Bank Leumi le-Israel BM", address: "24-32 Yehuda Halevi St, Tel Aviv 65546, Israel", contact: "", swift: "LUMIILIT" },
                { name: "Israel Discount Bank Limited", address: "PO Box 456, 23 Yehuda Halevi Street, Tel Aviv 65136, Israel", contact: "", swift: "IDBLILIT" },
                { name: "Mercantile Discount Bank Ltd", address: "Hayovel Bldg, 125 Menachem Begin Rd, Tel Aviv 67012, Israel", contact: "", swift: "BARDILIT" }
            ],
            "italy": [
                { name: "Banca Monte dei Paschi di Siena SpA", address: "Piazza Salimbeni 3, 53100 Siena, SI, Italy", contact: "", swift: "PASCITMM" },
                { name: "Banca Nazionale del Lavoro SpA", address: "Via Vittorio Veneto 119, 00187 Rome, RM, Italy", contact: "", swift: "BNLIITRR" },
                { name: "Banca Popolare dell'Emilia Romagna Società Cooperativa", address: "Via San Carlo 8/20, 41121 Modena, MO, Italy", contact: "", swift: "BPMOIT22" },
                { name: "BANCA UBAE SpA", address: "PO Box 290, Via Quintino Sella 2, 00187 Rome, RM, Italy", contact: "", swift: "UBAIITRR" },
                { name: "Banco BPM S.P.A.", address: "Piazza Nogara 2, 37121 Verona, VR, Italy", contact: "", swift: "BAPPIT22" },
                { name: "Intesa Sanpaolo SpA", address: "Via Monte di Pietà 8, I-20121 Milan, MI, Italy", contact: "", swift: "BCITITMM" },
                { name: "UniCredit SpA", address: "Piazza Cordusio, 20123 Milan, MI, Italy", contact: "", swift: "UNCRITMM" }
            ],
            "japan": [
                { name: "Mizuho Bank Ltd", address: "1-3-3 Marunouchi, Chiyoda-ku, Tokyo 100-8210, Tokyo, Japan", contact: "", swift: "MHCBJPJT" },
                { name: "MUFG Bank Ltd", address: "7-1 Marunouchi, 2-Chome, Chiyoda-ku, Tokyo 100-8388, Tokyo, Japan", contact: "", swift: "BOTKJPJT" },
                { name: "Resona Bank Limited", address: "2-1, Bingomachi 2-chome, Chuo-ku, Osaka 540-8610, Osaka, Japan", contact: "", swift: "DIWAJPJT" },
                { name: "Saitama Resona Bank Limited", address: "4-1 Tokiwa 7-chome, Urawa-Ku, Saitama 330-9088, Saitama, Japan", contact: "", swift: "SAIBJPJT" },
                { name: "Standard Chartered Bank", address: "21st Floor, Sanno Park Tower, 2-11-1 Nagata-cho, Chiyoda-ku, Tokyo 100-6155", contact: "", swift: "SCBLJPJT" },
                { name: "Sumitomo Mitsui Banking Corporation", address: "1-2 Marunouchi, 1-chome, Chiyoda-ku, Tokyo 100-0005, Tokyo, Japan", contact: "", swift: "SMBCJPJT" },
                { name: "The Aichi Bank Ltd", address: "14-12 Sakae, 3-chome, Naka-ku, Nagoya 460-8678, Aichi, Japan", contact: "", swift: "AICHJPJN" },
                { name: "The Chiba Kogyo Bank Ltd", address: "1-2 Saiwaicho, 2-chome, Mihama-Ku, Chiba, Chiba, Japan", contact: "", swift: "CHIKJPJT" },
                { name: "The Iyo Bank Ltd", address: "1 Minami-Horibata-cho, Matsuyama 790-8514, Ehime, Japan", contact: "", swift: "IYOBJPJT" },
                { name: "The Okazaki Shinkin Bank", address: "41 Motosuga, Sugo-Cho, Okazaki 444-8602, Aichi, Japan", contact: "", swift: "OKSBJPJZ" },
                { name: "The Shizuoka Bank Ltd", address: "10 Gofukucho 1-chome, Aoi-ku, Shizuoka-shi, Shizuoka 420-8760, Shizuoka, Japan", contact: "", swift: "SHIZJPJT" }
            ],
            "jordan": [
                { name: "Arab Bank plc", address: "PO Box 950545, Shaker Bin Zaid Street, Shmeisani, 11195 Amman, Jordan", contact: "", swift: "ARABJOAX" },
                { name: "Bank Al Etihad", address: "PO Box 35104, Abd Al-Raheem Al-Wakid St., Shmeisani, 11118, Amman, Jordan", contact: "", swift: "UBSIJOAX" }
            ],
            "kenya": [
                { name: "KCB Bank Kenya Limited", address: "PO Box 48400-00100 GPO, Kencom House, Moi Avenue, Nairobi, Kenya", contact: "", swift: "KCBLKENX" }
            ],
            "south-korea": [
                { name: "Busan Bank", address: "830-38 Bomil-dong, Dong-gu, Busan 601-717, Korea (Republic of)", contact: "", swift: "PUSBKR2P" },
                { name: "Citibank Korea Inc", address: "39 Da-Dong, Chung-gu, Seoul 100-180, Korea (Republic of)", contact: "", swift: "CITIKRSX" },
                { name: "DAEGU BANK", address: "11/F, 118 Suseong-dong 2-ga, Suseong-gu, Daegu 706-712, Korea (Republic of)", contact: "", swift: "DAEBKR22" },
                { name: "Industrial Bank of Korea", address: "PO Box 4153, 50 Euljiro 2-ga, Chung-gu, Seoul 100-758, Korea (Republic of)", contact: "", swift: "IBKOKRSE" },
                { name: "KEB Hana Bank", address: "181 Eulji-ro 2-ga, Chung-gu, Seoul 100-793, Korea (Republic of)", contact: "", swift: "KOEXKRSE" },
                { name: "Kookmin Bank", address: "9-1 Namdaemunno 2-Ga, Jung-Gu, Seoul 100-703, Korea (Republic of)", contact: "", swift: "CZNBKRSE" },
                { name: "Kyongnam Bank", address: "246-1 Seokjeon-dong, Hoewon-gu, Masan 630-010, Gyeongsangnam-Do, Korea (Republic of)", contact: "", swift: "KYNAKR22" },
                { name: "Shinhan Bank", address: "120 Taepyeongno 2-ga, Jung-Gu, Seoul 100-865, Korea (Republic of)", contact: "", swift: "SHBKKRSE" },
                { name: "The Export-Import Bank of Korea", address: "PO Box 641, Yeouido, Seoul 150-606, Korea (Republic of)", contact: "", swift: "EXIKKRSE" },
                { name: "The Jeonbuk Bank Ltd", address: "17F, Seo Rin Bldg, Seo Rin-Dong 88, Jung-Gu, Seoul 110-790, Korea (Republic of)", contact: "", swift: "JEONKRSE" },
                { name: "The Kwangju Bank Ltd", address: "7-12 Daein-dong, Dong-ku, Kwangju 501-730, Korea (Republic of)", contact: "", swift: "KWABKRSE" },
                { name: "Woori Bank", address: "203 Hoehyeon-dong, 1-ga, Jung-gu, Seoul 100-792, Korea (Republic of)", contact: "", swift: "HVBKKRSE" }
            ],
            "kosovo": [
                { name: "Raiffeisen Bank Kosovo", address: "UÇK Street No. 51, 10000 Pristina, Kosovo", contact: "", swift: "RBKOXKPR" }
            ],
            "kuwait": [
                { name: "Commercial Bank of Kuwait SAK", address: "PO Box 2861, Mubarak Al-Kabir Street, 13029 Safat, Safat, Kuwait City, Kuwait", contact: "", swift: "COMBKWKW" },
                { name: "National Bank of Kuwait SAK", address: "PO Box 95, Abdullah Al Ahmed Street, Safat, 13001 Kuwait City, Kuwait", contact: "", swift: "NBOKKWKW" }
            ],
            "latvia": [
                { name: "AS Rietumu Banka", address: "7 Vesetas Street, LV-1013 Riga, Latvia", contact: "", swift: "RTMBLV2X" }
            ],
            "lebanon": [
                { name: "BankMed SAL", address: "BankMed Center, 482 Clemenceau Street, Kantari, 2022 9302 Beirut, Lebanon", contact: "", swift: "MEDLLBBX" },
                { name: "Banque Libano-Française SAL", address: "5, Rome Street, Beirut Liberty Plaza Bldg, Hamra, Beirut, Lebanon", contact: "", swift: "BLFSLBBX" },
                { name: "Federal Bank of Lebanon SAL", address: "PO Box 11-2209, 2nd Floor, Renno Bldg, Charles Malek Ave, St Nicolas Sector, Beirut, Lebanon", contact: "", swift: "FBLELBBX" },
                { name: "First National Bank SAL", address: "PO Box 110-435, 2012 6004 Allenby Street 147, Beirut Central District, Marfa, Beirut, Lebanon", contact: "", swift: "FINKLBBE" }
            ],
            "liechtenstein": [
                { name: "Liechtensteinische Landesbank Aktiengesellschaft", address: "PO Box 384, Städtle 44, 9490 Vaduz, Liechtenstein", contact: "", swift: "LILALI2X" }
            ],
            "luxembourg": [
                { name: "The Royal Bank of Scotland International Limited", address: "46 Avenue, J F Kennedy, L- 1855, Luxembourg", contact: "", swift: "RBOSJESX" }
            ],
            "macedonia": [
                { name: "Halk Banka AD Skopje", address: "Blvd Mito Hadzivasilev Jasmin BB, 1000 Skopje, Macedonia", contact: "", swift: "EXPCMK22" }
            ],
            "malaysia": [
                { name: "Alliance Bank Malaysia Berhad", address: "3rd Floor, Menara Multi-Purpose, Capital Square, No.8 Jalan Munshi Abdullah, 50100 Kuala Lumpur, Malaysia", contact: "", swift: "MFBBMYKL" },
                { name: "AmBank (M) Berhad", address: "Level 24, Bangunan Ambank Group, Jalan Raja Chulan, 50200 Kuala Lumpur, Malaysia", contact: "", swift: "ARBKMYKL" },
                { name: "Citibank Berhad", address: "Aras 45 Menara Citibank, 165 Jalan Ampang, 50450 Kuala Lumpur, Malaysia", contact: "", swift: "CITIMYKL" },
                { name: "CIMB Bank Berhad", address: "No 6 Jalan Tun Perak, 50050 Kuala Lumpur, Malaysia", contact: "", swift: "CIBBMYKL" },
                { name: "HSBC Bank Malaysia Berhad", address: "2 Leboh Ampang, 50100 Kuala Lumpur, Malaysia", contact: "", swift: "HBMBMYKL" },
                { name: "Malayan Banking Berhad", address: "Menara Maybank, 100 Jalan Tun Perak, 50050 Kuala Lumpur, Malaysia", contact: "", swift: "MBBEMYKL" },
                { name: "Mizuho Bank (Malaysia) Berhad", address: "Level 27, Menara Maxis, Kuala Lumpur City Centre, 50088 Kuala Lumpur, Malaysia", contact: "", swift: "MHCBMYKA" },
                { name: "OCBC Bank (Malaysia) Berhad", address: "19th Floor, Menara OCBC, 18 Jalan Tun Perak, 50050 Kuala Lumpur, Malaysia", contact: "", swift: "OCBCMYKL" },
                { name: "Public Bank Berhad", address: "Menara Public Bank, 146 Jalan Ampang, 50450 Kuala Lumpur, Malaysia", contact: "", swift: "PBBEMYKL" },
                { name: "RHB Bank Berhad", address: "Tower Two & Three, RHB Centre, Jalan Tun Razak, 50400 Kuala Lumpur, Malaysia", contact: "", swift: "RHBBMYKL" },
                { name: "RHB Islamic Bank Berhad", address: "Level 11, Menara Yayasan Tun Razak, 200, Jalan Bukit Bintang, 55100 Kuala Lumpur, Malaysia", contact: "", swift: "RHBAMYKL" },
                { name: "Standard Chartered Bank Malaysia Bhd", address: "Level 16, Menara Standard Chartered, No 30, Jalan Sultan Ismail, 50250 Kuala Lumpur, Malaysia", contact: "", swift: "SCBLMYKX" }
            ],
            "maldives": [
                { name: "Bank of Ceylon", address: "Aage 12, Boduthakurufaanu Magu, Male", contact: "", swift: "BCEYMVMV" },
                { name: "Bank of Maldives PLC", address: "11 Boduthakurufaanu Magu, Male 20094, Maldives", contact: "", swift: "MALBMVMV" },
                { name: "The Mauritius Commercial Bank (Maldives) Private Ltd", address: "H. Sifa Building, Boduthakufaanu Magu, Male, Maldives", contact: "", swift: "MCBLMVMV" }
            ],
            "mauritius": [
                { name: "AfrAsia Bank Limited", address: "Bowen Square, 10 Dr Ferriere Street, Port Louis, Mauritius", contact: "", swift: "AFBLMUMU" }
            ],
            "mexico": [
                { name: "Banco Nacional de Mexico SA", address: "Emilio Castelar 75, Col Polanco, 11560 México City", contact: "", swift: "BNMXMXMM" },
                { name: "Banco Santander (Mexico) SA", address: "Piso 2, Prolongacion Paseo de La Reforma No 500, Col Lomas de Santa Fe, Alvaro Obregón, 01219 México City, Distrito Federal, Mexico", contact: "", swift: "BMSXMXMM" }
            ],
            "nepal": [
                { name: "Laxmi Bank Ltd", address: "PO Box 19593, (Kathmandu Office), Hattisar, Kathmandu, Kathmandu Valley, Nepal", contact: "", swift: "LXBLNPKA" },
                { name: "Nabil Bank Limited", address: "PO Box 3729, Nabil Centre, Beena marg, Dubar Marg, Kathmandu, Kathmandu Valley, Nepal", contact: "", swift: "NARBNPKA" },
                { name: "NIC Asia Bank Ltd", address: "Corporate Office, Trade Tower Thapathali, Kathmandu Nepal, Kathmandu Valley, Nepal", contact: "", swift: "NICENPKA" },
                { name: "NMB Bank Ltd", address: "P O Box, 11543, NMB Bhawan, Babar Mahal, Katmandu, Nepal", contact: "", swift: "NMBBNPKA" },
                { name: "Sanima Development Bank", address: "Nagpokhari, Naxal, GPO Box:20394, Kathmandu, Kathmandu Valley, Nepal", contact: "", swift: "SNMANPKA" },
                { name: "Prabhu Bank Ltd", address: "Prabhu Building, Babamahal, Kathmandu, Kathmandu Valley, Nepal", contact: "", swift: "PRVUNPKA" }
            ],
            "netherlands": [
                { name: "ABN AMRO Bank NV", address: "Gustav Mahlerlaan 10, PO Box 238, 1000 EA Amsterdam, Netherlands", contact: "", swift: "ABNANL2A" },
                { name: "Cooperative Rabobank UA", address: "Croeselaan 18, 3521 CB Utrecht, Netherlands", contact: "", swift: "RABONL2U" }
            ],
            "new-zealand": [
                { name: "ANZ Bank New Zealand Limited", address: "Level 10, 170-186 Featherston Street, Wellington 6011, New Zealand", contact: "", swift: "ANZBNZ22" },
                { name: "Bank of New Zealand", address: "Level 4 80 Queen Street, Auckland, 1010, New Zealand", contact: "", swift: "BKNZNZ22" }
            ],
            "norway": [
                { name: "DNB Bank ASA", address: "Stranden 21, NO-0021 Oslo, Oslo, Norway", contact: "", swift: "DNBANOKK" },
                { name: "Danske Bank A/S", address: "Søndre Gate 13-15, N-7466 Trondheim, Norway", contact: "", swift: "DABANO22" },
                { name: "Nordea Bank Abp", address: "Middelthunsgt 17, N-0368 Oslo, Oslo, Norway", contact: "", swift: "NDEANOKK" },
                { name: "Sparebank 1 Nord-Norge", address: "PO Box 6800, 9298 Tromsø, Troms, Norway", contact: "", swift: "SNOWNO22" }
            ],
            "oman": [
                { name: "BankMuscat SAOG", address: "Street No. 62, Building No. 120/4, Block No. 311, Airport Heights, Seeb, Oman", contact: "", swift: "SNOWNO22" },
                { name: "National Bank of Oman SAOG", address: "PO Box 751, Ruwi, 112 Muscat, Oman", contact: "", swift: "NBOMOMRX" },
                { name: "Oman Arab Bank SAOC", address: "Al Ghubrah North,130, Muscat, Oman", contact: "", swift: "OMABOMRU" },
                { name: "Sohar International Bank SAOG", address: "Water-Front Building No: 166, Block No: 230, Way No 3017, Shatti Al Qurum Beach Area, Muscat, Oman", contact: "", swift: "BSHROMRU" }
            ],
            "pakistan": [
                { name: "Askari Bank Limited", address: "PO Box 1084, AWT Plaza, The Mall, Rawalpindi 46000, Punjab, Pakistan", contact: "", swift: "ASCMPKKA" },
                { name: "Bank AL Habib Limited", address: "126-C Old Bahawalpur Road, Multan, Multan, Punjab, Pakistan", contact: "", swift: "BAHLPKKA" },
                { name: "Bank Alfalah Limited", address: "PO Box 6773, B. A. Building, I. I. Chundrigar Road, Karachi, Sindh, Pakistan", contact: "", swift: "ALFHPKKA" },
                { name: "BankIslami Pakistan Limited", address: "11th Floor, Executive Tower, Dolmen City, Marine Drive, Block-4, Clifton, Karachi, Sindh, Pakistan", contact: "", swift: "BKIPPKKA" },
                { name: "Habib Bank Limited", address: "9th Floor, HBL Tower, Jinnah Avenue, Blue Area, Islamabad, Federal Capital, Pakistan", contact: "", swift: "HABBPKKA" },
                { name: "Habib Metropolitan Bank Ltd", address: "PO Box 1289, Spencer's Building, I.I. Chundrigar Road, Karachi 74200, Sindh, Pakistan", contact: "", swift: "MPBLPKKA" },
                { name: "MCB Bank Limited", address: "MCB Building, 15 Main Gulberg, Lahore 74000, Punjab, Pakistan", contact: "", swift: "MUCBPKKA" },
                { name: "Meezan Bank Limited", address: "2nd Floor, Meezan House, C-25 Estate Avenue, SITE, Karachi, Sindh, Pakistan", contact: "", swift: "MEZNPKKA" },
                { name: "National Bank of Pakistan", address: "NBP Building, I.I. Chundrigar Road, Karachi, Sindh, Pakistan", contact: "", swift: "NBPAPKKA" },
                { name: "Samba Bank Limited", address: "6th Floor, SIDCO Avenue Center, Maulana Deen Mohammad Wafai Road, Karachi, Sindh, Pakistan", contact: "", swift: "SAMBPKKA" },
                { name: "Silkbank Limited", address: "Silk Bank Building, I.I. Chundrigar Road, Karachi 74200, Sindh, Pakistan", contact: "", swift: "SAUDPKKA" },
                { name: "Sindh Bank Ltd", address: "3rd Floor, Federation House, Abdullah Shah Ghazi Road, Clifton, Karachi 75600, Sindh, Pakistan", contact: "", swift: "SINDPKKA" },
                { name: "Soneri Bank Ltd", address: "3rd Floor, Liberty Market, 90-B-C/11 Gulberg-III, Lahore, Punjab, Pakistan", contact: "", swift: "SONEPKKA" },
                { name: "Standard Chartered Bank (Pakistan) Limited", address: "PO Box 5556, 3rd Floor, Main Branch, I.I Chundrigar Road, Karachi 74000, Sindh, Pakistan", contact: "", swift: "SCBLPKKX" },
                { name: "Bank Makramah Limited", address: "Plot No. 6B, F-6 Super Market, Islamabad, 74000, Federal Capital, Pakistan", contact: "", swift: "SUMBPKKA" },
                { name: "The Bank of Punjab", address: "BOP Tower, 10-B Block E-II Main Boulevard Road, Gulberg III, Lahore, Lahore, Punjab, Pakistan", contact: "", swift: "BPUNPKKA" },
                { name: "United Bank Ltd", address: "PO Box 4306, State Life Building No 1, I.I. Chundrigar Road, Karachi 74000, Sindh, Pakistan", contact: "", swift: "UNILPKKA" }
            ],
            "peru": [
                { name: "Banco Continental (BBVA Banco Continental)", address: "Avenida Republica de Panama 3055, Lima, Peru", contact: "", swift: "BCONPEPL" }
            ],
            "philippines": [
                { name: "Asian Development Bank", address: "6 ADB Avenue, Mandaluyong City 1550, Metro Manila, Luzon, Philippines", contact: "", swift: "ASDBPHMM" }
            ],
            "poland": [
                { name: "Bank Handlowy w Warszawie SA", address: "ul Senatorska 16, 00-923 Warsaw, Mazowieckie, Poland", contact: "", swift: "CITIPLPX" },
                { name: "Bank Polska Kasa Opieki SA", address: "ul Grzybowska 53/57, 00-950 Warsaw, Mazowieckie, Poland", contact: "", swift: "PKOPPLPW" },
                { name: "mBank SA", address: "PO Box 728, ul Senatorska 18, 00-950 Warsaw, Mazowieckie, Poland", contact: "", swift: "BREXPLPW" }
            ],
            "portugal": [
                { name: "Novo Banco SA", address: "Banco Espírito Santo, Avenida da Liberdade 195, 1250-142 Lisbon, Portugal", contact: "", swift: "BESCPTPL" }
            ],
            "qatar": [
                { name: "Doha Bank", address: "PO Box 3818, Grand Hamad Avenue, Doha, Qatar", contact: "", swift: "DOHBQAQA" },
                { name: "Qatar Islamic Bank SAQ", address: "PO Box 559, Grand Hamad Street, Doha, Qatar", contact: "", swift: "QISBQAQA" },
                { name: "Qatar National Bank SAQ", address: "PO Box 1000, Cornish St, Doha, Qatar", contact: "", swift: "QNBAQAQA" }
            ],
            "romania": [
                { name: "Banca Comerciala Romana SA", address: "5 Regina Elisabeta Bulevard, 3rd district, 030016 Bucharest, Romania", contact: "", swift: "RNCBROBU" }
            ],
            "saudi-arabia": [
                { name: "Al Inma Bank", address: "P O Box 66674, Al-Anoud Tower, King Fahad Road, Riyadh 11586, Saudi Arabia", contact: "", swift: "INMASARI" },
                { name: "Al Rajhi Bank", address: "PO Box 28, Al Akariya Building, Oleya Street, Riyadh 11411, Saudi Arabia", contact: "+966 11 211 6000", swift: "RJHISARI" },
                { name: "Arab National Bank", address: "PO Box 56921, King Faisal St, North Murabba, Riyadh 11564, Saudi Arabia", contact: "", swift: "ARNBSARI" },
                { name: "Bank Al-Bilad", address: "PO Box 140, Al Malaz-Sitteen Street, Riyadh 11411, Saudi Arabia", contact: "", swift: "ALBISARI" },
                { name: "Banque Saudi Fransi", address: "PO Box 56006, Ma'ather Road, Riyadh 11554, Saudi Arabia", contact: "", swift: "BSFRSARI" },
                { name: "Riyad Bank", address: "PO Box 22622, King Abdulaziz Street, Riyadh 11416, Saudi Arabia", contact: "", swift: "RIBLSARI" },
                { name: "The Arab Investment Company SAA", address: "PO Box 4009, King Abdulaziz Road, Riyadh 11491, Saudi Arabia", contact: "", swift: "TAIQBHBM" },
                { name: "The Saudi British Bank", address: "PO Box 9084, Prince Abdulaziz Bin Mossaad Bin Jalawi Street, (Dabaab), Riyadh 11413, Saudi Arabia", contact: "", swift: "SABBSARI" }
            ],
            "seychelles": [
                { name: "Bank of Ceylon", address: "2 Floor, Capital City Building, 2-05 Independence Avenue, Victoria, Mahe, Seychelles", contact: "", swift: "BCEYSCSC" }
            ],
            "singapore": [
                { name: "DBS Bank Ltd", address: "DBS Building, Tower 1, 6 Shenton Way, Singapore 068809, Singapore", contact: "", swift: "DBSSSGSG" },
                { name: "Indian Bank – India", address: "Bharat Building, 3 Raffles Place, Singapore 048617", contact: "", swift: "IDIBSGSG" },
                { name: "JPMorgan Chase Bank National Association", address: "17th Floor, Capital Tower, 168 Robinson Rd, Singapore 068912", contact: "", swift: "CHASSGSG" },
                { name: "Oversea-Chinese Banking Corp Ltd", address: "65 Chulia Street, # 26-00, OCBC Centre, Singapore 049513, Singapore", contact: "", swift: "OCBCSGSG" },
                { name: "Standard Chartered Bank", address: "6 Battery Rd, Singapore 049909", contact: "", swift: "SCBLSGSG" }
            ],
            "slovakia": [
                { name: "VUB Banka", address: "Mlynské nivy 1, 829 90 Bratislava, Slovakia", contact: "", swift: "" }
            ],
            "slovenia": [
                { name: "Small World Financial Services", address: "", contact: "", swift: "" }
            ],
            "south-africa": [
                { name: "FirstRand Bank Ltd", address: "4 Merchant Place, Cnr Fredman Drive & Rivonia Road, Sandton 2196, Gauteng, South Africa", contact: "", swift: "FIRNZAJJ" },
                { name: "Nedbank Limited", address: "135 Rivonia Rd, Sandown, Sandton, Johannesburg 2196, Gauteng, South Africa", contact: "", swift: "NEDSZAJJ" },
                { name: "The Standard Bank of South Africa Ltd", address: "9th Floor, Standard Bank Centre, 5 Simmonds Street, Johannesburg 2001, Gauteng, South Africa", contact: "", swift: "SBZAZAJJ" }
            ],
            "spain": [
                { name: "Banco Bilbao Vizcaya Argentaria SA", address: "Pz de San Nicolás, 4,48005, Bilbao, Vizcaya, Spain", contact: "", swift: "BBVAESMM" },
                { name: "Banco de Sabadell SA", address: "Av. Óscar Esplá, 30,03007, Alicante, Alicante, Spain", contact: "", swift: "BSABESBB" },
                { name: "Banco Santander SA", address: "Cludad Grupo Santander, Ave de Cantabria s/n, 28660 Boadilla del Monte, Madrid,Spain", contact: "", swift: "BSCHESMM" },
                { name: "CaixaBank S.A.", address: "Cl Pintor Sorolla 2-4,46002, Valencia, Valencia, Spain", contact: "", swift: "CAIXESBB" }
            ],
            "sweden": [
                { name: "Nordea Bank AB (publ)", address: "Hamngatan 10, SE-105 71 Stockholm, Sweden", contact: "", swift: "NDEASESS" },
                { name: "Skandinaviska Enskilda Banken AB", address: "Kungsträdgårdsgatan 8, 10640 Stockholm, Sweden", contact: "", swift: "ESSESESS" },
                { name: "Svenska Handelsbanken AB (publ)", address: "Kungsträdgårdsgatan 2, 10670 Stockholm, Sweden", contact: "", swift: "HANDSESS" },
                { name: "Swedbank AB", address: "Landsvagen 40, 17263 Sundbyberg, Sweden", contact: "", swift: "SWEDSESS" }
            ],
            "switzerland": [
                { name: "Bank CIC (Schweiz) AG", address: "PO Box 216, Marktplatz 13, CH-4001 Basel, Switzerland", contact: "", swift: "CIALCHBB" },
                { name: "Banque Cantonale de Genève", address: "PO Box 2251, Quai de l'Ile 17, CH-1211 Geneva 2, Switzerland", contact: "", swift: "BCGECHGG" },
                { name: "Banque Cantonale Vaudoise (BCV)", address: "Place St. François 14, CH-1002 Lausanne, Vaud, Switzerland", contact: "", swift: "BCVLCH2L" },
                { name: "Basellandschaftliche Kantonalbank", address: "Rheinstrasse 7, 4410 Liestal, Basel-Landschaft, Switzerland", contact: "", swift: "BLKBCH22" },
                { name: "Habib Bank AG Zurich", address: "PO Box, 8042 Zürich, Switzerland", contact: "", swift: "BZUCHZZ" },
                { name: "Thurgauer Kantonalbank", address: "PO Box 160, Bankplatz 1, 8570 Weinfelden, Thurgau, Switzerland", contact: "", swift: "KBTGCH22" },
                { name: "UBS AG", address: "Bahnhofstrasse 45, CH-8001 Zürich, Switzerland", contact: "", swift: "UBSWCHZH" },
                { name: "Valiant Bank AG", address: "PO Box, Bundesplatz 4, 3001 Bern, Switzerland", contact: "", swift: "VABECH22" },
                { name: "Zürcher Kantonalbank", address: "Bahnhofstrasse 9, CH-8010 Zürich, Switzerland", contact: "", swift: "ZKBKCHZZ" }
            ],
            "taiwan": [
                { name: "Citibank Taiwan Limited", address: "1st & 2nd Floor, No. 1 Songjhih Rd, Taipei City 110, Taiwan", contact: "", swift: "CITITWTX" },
                { name: "Standard Chartered Bank (Taiwan) Limited", address: "106 Chungyang Road, Hsinchu City 300, Taiwan", contact: "", swift: "SCBLTWTP" },
                { name: "Sunny Bank Ltd", address: "90 Shih-Pai Road, Section 1, Pei-tou District, Taipei City 112, Taiwan", contact: "", swift: "SUNYTWTP" },
                { name: "Union Bank of Taiwan", address: "2nd Floor, 109 Min-Sheng East Road, Section 3, Taipei City 105, Taiwan", contact: "", swift: "UBOTTWTP" }
            ],
            "thailand": [
                { name: "Bangkok Bank Public Company Limited", address: "333 Silom Road, Suriwongse, Bangrak, Bangkok 10500, Thailand", contact: "", swift: "BKKBTHBK" },
                { name: "Bank of Ayudhya Public Company Ltd", address: "1222 Rama III Road, Phongphang Yan Nawa, Bangkok 10120, Thailand", contact: "", swift: "AYUDTHBK" },
                { name: "Export-Import Bank of Thailand", address: "EXIM Building, 1193 Phaholyothin Road, Samseannai, Phayathai, Bangkok 10400, Thailand", contact: "", swift: "EXTHTHBK" },
                { name: "KASIKORNBANK Public Company Limited", address: "1 Soi Kasikornthai, Ratburana Road, Bangkok 10140, Thailand", contact: "", swift: "KASITHBK" },
                { name: "Krung Thai Bank Public Co Ltd", address: "35 Sukhumvit Rd, North Klongtoey, Bangkok 10110, Thailand", contact: "", swift: "KRTHTHBK" },
                { name: "Standard Chartered Bank (Thai) Public Company Limited", address: "90 Sathontanee bld, North Sathorn Rd, Silom, Bangkok 10500, Thailand", contact: "", swift: "SCBLTHBX" }
            ],
            "turkey": [
                { name: "Albaraka Turk Participation Bank", address: "Saray Mahallesi, Dr Adnan Büyükdeniz Caddesi No: 6, Ümraniye, 34768 Istanbul, Turkey", contact: "", swift: "BTFHTRIS" },
                { name: "Alternatifbank AS", address: "Cumhuriyet Cad 46, Elmadag, 34367 Istanbul, Turkey", contact: "", swift: "ALFBTRIS" },
                { name: "Denizbank AS", address: "Büyükdere Cad 106, 34394 Esentepe, Istanbul, Turkey", contact: "", swift: "DENITRIS" },
                { name: "Odea Bank AS", address: "Levent 199, Buyukdere Cad. No: 19, KAT: 33-39, Sisli, 34394, Istanbul, Turkey", contact: "", swift: "ODEATRIS" },
                { name: "QNB Finansbank AS", address: "Büyükdere Cad No 129, Mecidiyeköy, 34394 Istanbul, Turkey", contact: "", swift: "FNNBTRIS" },
                { name: "Türk Ekonomi Bankasi AS", address: "TEB Kampus C ve D Blok, Saray Mah, Sokullu Cad No: 7A-7B, Ümraniye, 34768 Istanbul, Turkey", contact: "", swift: "TEBUTRIS" },
                { name: "Türkiye Cumhuriyeti Ziraat Bankasi AS", address: "Doganbey Mah, Ataturk Bulv No 8, 06107 Altindag, Ankara, Ankara, Turkey", contact: "", swift: "TCZBTR2A" },
                { name: "Türkiye Finans Katilim Bankasi AS", address: "Yakacik Mevkìì Hürriyet Mah, Adnan Kahveci Cad No 139, Kartal, 34876 Istanbul, Turkey", contact: "", swift: "AFKBTRIS" },
                { name: "Türkiye Garanti Bankasi AS", address: "Nispetiye Mah, Aytar Cad No 2 - Besiktas, Levent, 34340 Istanbul, Turkey", contact: "", swift: "TGBATRIS" },
                { name: "Türkiye Halk Bankasi AS", address: "Finanskent Mahallesi Finans Caddesi No:42/1,34760, Umraniye, Istanbul, Türkiye", contact: "", swift: "TRHBTR2A" },
                { name: "Turkiye Is Bankasi AS (ISBANK)", address: "Is Kuleleri, 34330 Levent, Istanbul, Turkey", contact: "", swift: "ISBKTRIS" },
                { name: "Yapi ve Kredi Bankasi AS", address: "Yapi Kredi Plaza - D Blok, Levent, 34330 Istanbul, Turkey", contact: "", swift: "YAPITRIS" }
            ],
            "uae": [
                { name: "Abu Dhabi Commercial Bank PJSC", address: "PO Box 939, Abu Dhabi Commercial Bank Building, Al Salam Street, Abu Dhabi, UAE", contact: "", swift: "ADCBAEAA" },
                { name: "Arab Bank for Investment and Foreign Trade", address: "PO Box 46733, AL-MASRAF Building, Sh Hamdan Street, Tourist Club Area, Abu Dhabi, UAE", contact: "", swift: "ABINAEAA" },
                { name: "Bank of Sharjah", address: "PO Box 1394, Al Hosn Avenue, Sharjah, UAE", contact: "", swift: "SHARAEAS" },
                { name: "Commercial Bank of Dubai PSC", address: "PO Box 2668, Al Ittihad Street, (Port Saeed), Deira, Dubai City, UAE", contact: "", swift: "CBDUAEAD" },
                { name: "Dubai Islamic Bank PJSC", address: "PO Box 1080, Airport Road, Deira, Dubai City, UAE", contact: "", swift: "DUIBAEAD" },
                { name: "Emirates Islamic Bank PJSC", address: "PO Box 6564, Dubai Festival City, Deira, Dubai City, UAE", contact: "", swift: "MEBLAEAD" },
                { name: "Emirates NBD PJSC", address: "PO Box 777, Dubai City, UAE", contact: "+971 4 609 0000", swift: "EBILAEAD" },
                { name: "First Abu Dhabi Bank PJSC", address: "PO Box 4, One NBAD Tower Bldg, Sheikh Khalifa Street, Abu Dhabi, UAE", contact: "", swift: "NBADAEAA" },
                { name: "Habib Bank AG Zurich", address: "PO Box 3306, Beniyas Square, Deira, Dubai City", contact: "", swift: "HBZUAEAD" },
                { name: "HSBC Bank Middle East Limited", address: "P O Box 66, HSBC Bank Bldg, 312/45 Al Suq Rd, Bur-Dubai, Dubai City", contact: "", swift: "BBMEAEAD" },
                { name: "MashreqBank PSC", address: "PO Box 1250, Omer Bin Al Khattab Street, Deira, Dubai City, UAE", contact: "", swift: "BOMLAEAD" },
                { name: "National Bank of Fujairah Psc", address: "PO Box 887, Hamad Bin Abdulla Street, Fujairah, UAE", contact: "", swift: "NBFUAEAF" },
                { name: "National Bank of Umm Al-Qaiwain psc", address: "PO Box 800, NBQ Building, King Faisal Street, Umm Al-Quwain, UAE", contact: "", swift: "UMMQAEAD" },
                { name: "Sharjah Islamic Bank", address: "PO Box 4, Al Boorj Avenue, Sharjah, UAE", contact: "", swift: "NBSHAEAS" },
                { name: "The National Bank of Ras Al-Khaimah PSC", address: "PO Box 5300, RAK Operations Centre, Emirates Road, Ras Al-Khaimah, UAE", contact: "", swift: "NRAKAEAK" }
            ],
            "uk": [
                { name: "Bank of America NA", address: "5 Canada Square, London, E14 5AQ", contact: "", swift: "BOFAGB22" },
                { name: "Bank of Ceylon (UK) Ltd", address: "1 Devonshire Square, London, EC2M 4WD, UK", contact: "", swift: "BCEYGB2L" },
                { name: "Barclays Bank PLC", address: "1 Churchill Place, London, E14 5HP, UK", contact: "+44 20 7116 1000", swift: "BARCGB22" },
                { name: "Barclays Bank UK PLC", address: "1 Churchill Place, London, E14 5HP, UK", contact: "", swift: "BUKBGB22" },
                { name: "British Arab Commercial Bank plc", address: "8/10 Mansion House Place, London, EC4N 8BJ, UK", contact: "", swift: "BACBGB2L" },
                { name: "Crédit Agricole Corporate and Investment Bank", address: "Broadwalk Hse, 5 Appold St, London, EC2A 2DA", contact: "", swift: "CRLYGB2L" },
                { name: "HSBC Bank plc", address: "8 Canada Square, London, E14 5HQ, UK", contact: "", swift: "MIDLGB22" },
                { name: "ICICI Bank UK PLC", address: "5 Thomas More Street, London, E1W 1YN, UK", contact: "", swift: "ICICGB2L" },
                { name: "ICBC Standard Bank Plc", address: "20 Gresham Street, London, EC2V 7JE, UK", contact: "", swift: "SBLLGB2L" },
                { name: "JPMorgan Chase Bank NA, London", address: "25, Bank Street, Canary Wharf, London, E14 5JP", contact: "", swift: "CHASGB2L" },
                { name: "National Westminster Bank Plc", address: "135 Bishopsgate, London, EC2M 3UR, UK", contact: "", swift: "NWBKGB2L" },
                { name: "Northern Bank Limited", address: "Donegall Square West, Belfast, Co. Antrim BT1 6JS, UK", contact: "", swift: "DABAGB2B" },
                { name: "Sonali Bank (UK) Limited", address: "29/33 Osborn Street, London, E1 6TD, UK", contact: "", swift: "BSONGB2L" },
                { name: "Standard Chartered Bank", address: "1 Basinghall Avenue, London, EC2V 5DD, UK", contact: "", swift: "SCBLGB2L" },
                { name: "The Royal Bank of Scotland plc", address: "PO Box 1000, Gogaburn, Edinburgh, EH12 1HQ, UK", contact: "", swift: "RBOSGB2L" }
            ],
            "usa": [
                { name: "Bank of America NA", address: "100 W 33rd St, 4th Fl, New York, 10001, USA", contact: "", swift: "BOFAUS3N" },
                { name: "Citibank NA", address: "ADR Department, 399 Park Avenue, New York, NY 10022, USA", contact: "+1 212 559 1000", swift: "CITIUS33" },
                { name: "Deutsche Bank Trust Company Americas", address: "60 Wall Street, New York, NY 10005, USA", contact: "", swift: "BKTRUS33" },
                { name: "First Horizon Bank", address: "15th Floor, 165 Madison Avenue, Memphis, TN 38103-2723, USA", contact: "", swift: "FTBMUS44" },
                { name: "Habib American Bank", address: "99 Madison Avenue, New York, NY 10016-7419, USA", contact: "", swift: "HANYUS33" },
                { name: "HSBC Bank USA NA", address: "Suite 50, 1800 Tysons Boulevard, McLean, VA 22102, USA", contact: "", swift: "MRMDUS33" },
                { name: "Huntington National Bank", address: "17 South High Street, Columbus, OH 43215, USA", contact: "", swift: "HUNTUS33" },
                { name: "Israel Discount Bank of New York", address: "511 Fifth Avenue, New York, NY 10017, USA", contact: "", swift: "IDBYUS33" },
                { name: "JPMorgan Chase Bank National Association", address: "383 Madison Ave, New York, NY 10017, USA", contact: "+1 212 270 6000", swift: "CHASUS33" },
                { name: "KeyBank NA", address: "127 Public Square, Cleveland, OH 44114-1306, USA", contact: "", swift: "KEYBUS33" },
                { name: "PNC Bank NA", address: "222 Delaware Ave Wilmington, DE 19899, USA", contact: "", swift: "PNCCUS33" },
                { name: "Regions Bank", address: "201 Milan kwy Birmingham, AL, 35211, USA", contact: "", swift: "UPNBUS44" },
                { name: "Standard Chartered Bank", address: "1095 Avenue of the Americas, New York, 10036, USA", contact: "", swift: "SCBLUS33" },
                { name: "The Bank of New York Mellon", address: "240 Greenwich St, 18th Fl, New York. NY, 10007, USA", contact: "", swift: "IRVTUS3N" },
                { name: "UMB Bank NA", address: "1010 Grand Boulevard, Kansas City, MO 64106, USA", contact: "", swift: "UMKCUS44" },
                { name: "US Bank NA", address: "800 Nicollet Mall, Minneapolis, MN 55402, USA", contact: "", swift: "USBKUS44" },
                { name: "Wells Fargo Bank NA", address: "101 N Phillips Ave, Sioux Falls, SD, 57104, USA", contact: "", swift: "PNBPUS33 / WFBIUS6S" },
                { name: "Hancock Whitney Bank", address: "2510 14th St, One Hancock Plz, Gulfport, MS, 39501, USA", contact: "", swift: "WHITUS44" }
            ],
            "vietnam": [
                { name: "Asia Commercial Bank", address: "442 Nguyen Thi Minh Khai Street, District 3, Ho Chi Minh City, Vietnam", contact: "", swift: "ASCBVNVX" },
                { name: "Joint Stock Commercial Bank for Investment and Development of Vietnam (BIDV)", address: "BIDV Tower, 194 Tran Quang Khai, Ly Thai To Ward, Hoan Kiem district, Hanoi, Vietnam", contact: "", swift: "BIDVVNVX" },
                { name: "Joint Stock Commercial Bank for Foreign Trade of Vietnam", address: "198 Tran Quang Khai Avenue, Hanoi, Vietnam", contact: "", swift: "BFTVVNVX" },
                { name: "Ocean Commercial Joint Stock Bank (Oceanbank)", address: "199 Nguyen Luong Bang, Hai Duong, Vietnam", contact: "", swift: "OJBAVNVX" },
                { name: "Shinhan Bank Vietnam Ltd", address: "138-142 Hai Ba Tung Street, DaKao Ward, District, Ho Chi Minh City Vietnam", contact: "", swift: "SHBKVNVX" }
            ]
        };

        // HNB Representatives Data
        const repData = {
            "uae": {
                title: "HNB Representative - UAE",
                contacts: [
                    {
                        name: "Mr Dilan De Silva",
                        address: "Building No.1/15, Al Khail Gate Residence Phase II, Al Quoz Industrial Area 2, Dubai, UAE",
                        mobile: "+971 58 571 4477 (Whatsapp/Voice)",
                        email: "dilan.desilva@hnb.lk"
                    }
                ]
            },
            "qatar": {
                title: "HNB Representatives - Qatar",
                contacts: [
                    {
                        name: "Mr Sampath Abeysekera",
                        company: "Al Mírqab Exchange Company Qatar",
                        address: "P O Box 1643, Doha, Qatar",
                        mobile: "+974 707 31300",
                        email: "sampath.abeysekera@hnb.lk"
                    },
                    {
                        name: "Mr Mohamed Risan",
                        vacation: "(On vacation from 21st March to 24th April 2025)",
                        mobile: "+974 314 62508 (Whatsapp/Voice)",
                        email: "mohamed.rizan@hnb.lk"
                    }
                ]
            },
            "saudi-arabia": {
                title: "HNB Representatives - Saudi Arabia",
                contacts: [
                    {
                        name: "Mr Rasika Madusanka",
                        company: "Arab National Bank Saudi Arabia",
                        address: "P O Box 3529, Al Khazan, Dammam 32242, Saudi Arabia",
                        email: "rasika.madhushanka@hnb.lk"
                    },
                    {
                        name: "Mr Sujitha Chamal",
                        company: "Bank Aljazira Saudi Arabia",
                        address: "Sahafa Branch, Thumamah Road, Opposite Tamimi Super Market, Riyadh, Saudi Arabia",
                        mobile: "+966 53 891 9672 (Imo/Messenger/Voice)",
                        altMobile: "+966 50 032 6402 (Imo/Messenger/Voice)",
                        email: "sujitha.attanayake@hnb.lk"
                    }
                ]
            },
            "israel": {
                title: "HNB Representative - Israel",
                contacts: [
                    {
                        name: "Mr Sumedha Wickramasinghe",
                        company: "Global Remit Currency Services Ltd",
                        address: "108 Levinsky Street Office 4228, Central Bus Station, Tahana Mercazi, Telaviv, Israel",
                        mobile: "+972 50 200 2527 (Whatsapp/Voice)",
                        email: "sumedha.wickramasinghe@hnb.lk"
                    }
                ]
            },
            "kuwait": {
                title: "HNB Representative - Kuwait",
                contacts: [
                    {
                        name: "Mr Ehanandasivam Abeesan",
                        company: "Al Muzaini Exchange Company Kuwait",
                        address: "P O Box 2156, Safat 13022, Kuwait",
                        mobile: "+965 66 769 023 (Whatsapp/Voice)",
                        email: "ehanandasivam.abeesan@hnb.lk"
                    }
                ]
            },
            "uk": {
                title: "HNB Representative - United Kingdom",
                contacts: [
                    {
                        name: "Mr Sanjayakanth Veerappan",
                        address: "171, Tooting High Street, London SW17 0SZ",
                        mobile: "+44 77 414 82584 (Whatsapp/Voice)",
                        email: "sanjaya.veerappan@hnb.lk"
                    }
                ]
            },
            "maldives": {
                title: "HNB Representative - Maldives",
                contacts: [
                    {
                        name: "Mr Gayan Gunasekara",
                        company: "Villa Travels & Tours Pvt Ltd",
                        address: "H. Sisil Hiya, Majeedhee Magu, Male', 20071, Republic of Maldives",
                        mobile: "+960 77 65181 (Whatsapp/Voice)",
                        email: "gayan.gunasekara@hnb.lk"
                    }
                ]
            },
            "italy": {
                title: "HNB Representative - Italy",
                contacts: [
                    {
                        name: "Mr Vikasitha Gayashan",
                        address: "Via Padova 36, 20131, Milano, Italy",
                        mobile: "+39 338 755 5996 (Whatsapp/Voice)",
                        email: "vikasitha.gayashan@hnb.lk"
                    }
                ]
            }
        };

        // Handle country selection
        document.getElementById('country-select').addEventListener('change', function() {
            const selectedCountry = this.value;
            const resultsContainer = document.getElementById('results-container');
            resultsContainer.innerHTML = '';
            
            if (!selectedCountry) {
                resultsContainer.innerHTML = '<div class="no-data">Please select a country to view information</div>';
                return;
            }
            
            // Display country name as heading
            const countryName = this.options[this.selectedIndex].text;
            const countryHeader = document.createElement('h2');
            countryHeader.textContent = countryName;
            countryHeader.style.color = '#1e5f8c';
            countryHeader.style.marginBottom = '20px';
            countryHeader.style.borderBottom = '2px solid #a8c6e0';
            countryHeader.style.paddingBottom = '10px';
            resultsContainer.appendChild(countryHeader);
            
            // Display Exchange Houses if available
            if (exchangeData[selectedCountry] && exchangeData[selectedCountry].length > 0) {
                const exchangeSection = document.createElement('div');
                exchangeSection.className = 'section';
                
                const exchangeTitle = document.createElement('div');
                exchangeTitle.className = 'section-title';
                exchangeTitle.textContent = 'Exchange Houses';
                exchangeSection.appendChild(exchangeTitle);
                
                exchangeData[selectedCountry].forEach(exchange => {
                    const exchangeItem = document.createElement('div');
                    exchangeItem.className = 'item';
                    
                    const nameDiv = document.createElement('div');
                    nameDiv.className = 'item-name';
                    nameDiv.textContent = exchange.name;
                    exchangeItem.appendChild(nameDiv);
                    
                    const addressDiv = document.createElement('div');
                    addressDiv.className = 'item-detail';
                    addressDiv.textContent = `Address: ${exchange.address || 'Not available'}`;
                    exchangeItem.appendChild(addressDiv);
                    
                    const contactDiv = document.createElement('div');
                    contactDiv.className = 'item-detail item-contact';
                    contactDiv.textContent = `Contact: ${exchange.contact || 'Not available'}`;
                    exchangeItem.appendChild(contactDiv);
                    
                    exchangeSection.appendChild(exchangeItem);
                });
                
                resultsContainer.appendChild(exchangeSection);
            }
            
            // Display Correspondent Banks if available
            if (correspondentData[selectedCountry] && correspondentData[selectedCountry].length > 0) {
                const correspondentSection = document.createElement('div');
                correspondentSection.className = 'section';
                
                const correspondentTitle = document.createElement('div');
                correspondentTitle.className = 'section-title';
                correspondentTitle.textContent = 'Correspondent Banks';
                correspondentSection.appendChild(correspondentTitle);
                
                correspondentData[selectedCountry].forEach(bank => {
                    const bankItem = document.createElement('div');
                    bankItem.className = 'item';
                    
                    const nameDiv = document.createElement('div');
                    nameDiv.className = 'item-name';
                    nameDiv.textContent = bank.name;
                    bankItem.appendChild(nameDiv);
                    
                    const addressDiv = document.createElement('div');
                    addressDiv.className = 'item-detail';
                    addressDiv.textContent = `Address: ${bank.address || 'Not available'}`;
                    bankItem.appendChild(addressDiv);
                    
                    const contactDiv = document.createElement('div');
                    contactDiv.className = 'item-detail item-contact';
                    contactDiv.textContent = `Contact: ${bank.contact || 'Not available'}`;
                    bankItem.appendChild(contactDiv);
                    
                    const swiftDiv = document.createElement('div');
                    swiftDiv.className = 'item-detail';
                    swiftDiv.textContent = `SWIFT: ${bank.swift || 'Not available'}`;
                    bankItem.appendChild(swiftDiv);
                    
                    correspondentSection.appendChild(bankItem);
                });
                
                resultsContainer.appendChild(correspondentSection);
            }
            
            // Display HNB Representatives if available
            if (repData[selectedCountry]) {
                const repSection = document.createElement('div');
                repSection.className = 'section';
                
                const repTitle = document.createElement('div');
                repTitle.className = 'section-title';
                repTitle.textContent = repData[selectedCountry].title;
                repSection.appendChild(repTitle);
                
                repData[selectedCountry].contacts.forEach(contact => {
                    const contactDiv = document.createElement('div');
                    contactDiv.className = 'item';
                    
                    // Contact Name
                    const nameRow = document.createElement('div');
                    nameRow.className = 'detail-row';
                    const nameLabel = document.createElement('span');
                    nameLabel.className = 'detail-label';
                    nameLabel.textContent = 'Contact:';
                    const nameValue = document.createElement('span');
                    nameValue.className = 'detail-value';
                    const nameSpan = document.createElement('span');
                    nameSpan.className = 'rep-name';
                    nameSpan.textContent = contact.name;
                    nameValue.appendChild(nameSpan);
                    
                    if (contact.vacation) {
                        const vacationSpan = document.createElement('span');
                        vacationSpan.className = 'vacation-note';
                        vacationSpan.textContent = contact.vacation;
                        nameValue.appendChild(vacationSpan);
                    }
                    
                    nameRow.appendChild(nameLabel);
                    nameRow.appendChild(nameValue);
                    contactDiv.appendChild(nameRow);
                    
                    // Company if available
                    if (contact.company) {
                        const companyRow = document.createElement('div');
                        companyRow.className = 'detail-row';
                        const companyLabel = document.createElement('span');
                        companyLabel.className = 'detail-label';
                        companyLabel.textContent = 'Company:';
                        const companyValue = document.createElement('span');
                        companyValue.className = 'detail-value';
                        companyValue.textContent = contact.company;
                        companyRow.appendChild(companyLabel);
                        companyRow.appendChild(companyValue);
                        contactDiv.appendChild(companyRow);
                    }
                    
                    // Address
                    if (contact.address) {
                        const addressRow = document.createElement('div');
                        addressRow.className = 'detail-row';
                        const addressLabel = document.createElement('span');
                        addressLabel.className = 'detail-label';
                        addressLabel.textContent = 'Address:';
                        const addressValue = document.createElement('span');
                        addressValue.className = 'detail-value';
                        addressValue.textContent = contact.address;
                        addressRow.appendChild(addressLabel);
                        addressRow.appendChild(addressValue);
                        contactDiv.appendChild(addressRow);
                    }
                    
                    // Mobile
                    if (contact.mobile) {
                        const mobileRow = document.createElement('div');
                        mobileRow.className = 'detail-row';
                        const mobileLabel = document.createElement('span');
                        mobileLabel.className = 'detail-label';
                        mobileLabel.textContent = 'Mobile:';
                        const mobileValue = document.createElement('span');
                        mobileValue.className = 'detail-value';
                        mobileValue.textContent = contact.mobile;
                        mobileRow.appendChild(mobileLabel);
                        mobileRow.appendChild(mobileValue);
                        contactDiv.appendChild(mobileRow);
                    }
                    
                    // Alternate Mobile if available
                    if (contact.altMobile) {
                        const altMobileRow = document.createElement('div');
                        altMobileRow.className = 'detail-row';
                        const altMobileLabel = document.createElement('span');
                        altMobileLabel.className = 'detail-label';
                        altMobileLabel.textContent = 'Alternate Mobile:';
                        const altMobileValue = document.createElement('span');
                        altMobileValue.className = 'detail-value';
                        altMobileValue.textContent = contact.altMobile;
                        altMobileRow.appendChild(altMobileLabel);
                        altMobileRow.appendChild(altMobileValue);
                        contactDiv.appendChild(altMobileRow);
                    }
                    
                    // Email
                    if (contact.email) {
                        const emailRow = document.createElement('div');
                        emailRow.className = 'detail-row';
                        const emailLabel = document.createElement('span');
                        emailLabel.className = 'detail-label';
                        emailLabel.textContent = 'Email:';
                        const emailValue = document.createElement('span');
                        emailValue.className = 'detail-value';
                        emailValue.textContent = contact.email;
                        emailRow.appendChild(emailLabel);
                        emailRow.appendChild(emailValue);
                        contactDiv.appendChild(emailRow);
                    }
                    
                    repSection.appendChild(contactDiv);
                    
                    // Add separator if multiple contacts
                    if (repData[selectedCountry].contacts.length > 1 && 
                        repData[selectedCountry].contacts.indexOf(contact) < repData[selectedCountry].contacts.length - 1) {
                        const separator = document.createElement('hr');
                        separator.style.margin = '15px 0';
                        separator.style.borderColor = '#a8c6e0';
                        repSection.appendChild(separator);
                    }
                });
                
                resultsContainer.appendChild(repSection);
            }
            
            // Show message if no data available for the country
            if ((!exchangeData[selectedCountry] || exchangeData[selectedCountry].length === 0) &&
                (!correspondentData[selectedCountry] || correspondentData[selectedCountry].length === 0) &&
                !repData[selectedCountry]) {
                resultsContainer.innerHTML = '<div class="no-data">No information available for the selected country</div>';
            }
        });

        // Initialize the page
        window.onload = function() {
            document.getElementById('results-container').innerHTML = '<div class="no-data">Please select a country to view information</div>';
        };
    </script>
</body>
</html>
