
<template>
    <header>
        <noscript><p class="tip">您的瀏覽器不支援JavaScript功能，若網頁功能無法正常使用時，請開啟瀏覽器 JavaScript 為可使用狀態</p></noscript>
        <a href="https://6000.gov.tw/Register/Index#content" aria-label="跳到中央內容區塊" tabindex="0" class="getMainBtn">跳到中央內容區塊</a>
        <a href="https://6000.gov.tw/" class="logo">
            <p>財政部</p>
        </a>
        <aside>
            <div class="link">
                <!-- 導盲磚快捷鍵設置 -->
                <a accesskey="U" class="guidePoint textWhite" href="javascript:void(0);" aria-label="上方功能區塊">:::</a>
                <button aria-label="誰能領(另開新視窗)" >誰能領</button>
                <button aria-label="如何領(另開新視窗)" >如何領</button>
                <button aria-label="直接入帳(另開新視窗)" >直接入帳</button>
                <button aria-label="常見問題(另開新視窗)" >常見問題</button>
                <button aria-label="防詐騙專區(另開新視窗)" >防詐騙專區</button>
            </div>
            <p class="time" id="datePeriod" aria-label="登記期間:112年3月22日~112年10月31日">登記期間:112年3月22日~112年10月31日</p>
        </aside>
    </header>
    <main>
        <section id="content" tabindex="-1" class="contentLayout">
            <a accesskey="C" class="guidePoint" href="javascript:void(0);" aria-label="中央內容區塊">:::</a>
            <div class="indexLeft textCenter">
                <h1>
                    <img alt="全民共享普發現金" src="../assets/cash.png">
                </h1>
            </div>
            <div class="indexRight textCenter formColumn">
                <!--<script src="./Copy6000_files/jquery.min.js.下載"></script>-->

                <div class="subTitle">
                    <h2>資料登記</h2>
                    <p>請備妥發放對象之健保卡號 與 本人/代領人之金融機構帳號</p>
                </div>
                <form action="https://6000.gov.tw/Register/Index" id="Register" method="post" role="form"  @submit.prevent="registerAnswer">
                    <input name="__RequestVerificationToken" type="hidden" value="you-Npdc5463XsVSr_Q1F-A_iaWRwca7piw9GK2_C3L1RCkwQhtB_ogujgmXeIkhYLKZ0EVlVVbgvZiT2qR4QLxHn2kDw7OecnPOHe8Rqp41">    <div class="hr">
                    <fieldset>
                        <legend class="visually-hidden">本人/代領人資訊</legend>
                        <div class="item">
                            <label for="RegisterBE_ParentId">本人/代領人身分證字號或居留證統一證號</label>
                            <div>
                                <input maxlength="10" aria-label="本人/代領人身分證字號或居留證統一證號" id="RegisterBE_ParentId" v-model="ParentId" name="RegisterBE.ParentId" placeholder="10位英數字(必填)" type="text" >
                            </div>
                        </div>
                        <div class="item">
                            <label for="RegisterBE_SelectedBank">本人/代領人金融機構代號 <span class="visually-hidden">(限本人同身分證字號之金融機構代號)</span></label>
                            <div>
                                <select id="RegisterBE_SelectedBank" name="RegisterBE.SelectedBank" aria-label="選擇金融機構代號(限本人同身分證字號之金融機構代號)" v-model="SelectedBank">
                                    <option label="選擇金融機構代號" selected="selected" value="">請選擇</option>
                                    <option value="004">004臺灣銀行</option><option value="005">005臺灣土地銀行</option><option value="006">006合作金庫商業銀行</option><option value="007">007第一商業銀行</option><option value="008">008華南商業銀行</option><option value="009">009彰化商業銀行</option><option value="011">011上海商業儲蓄銀行</option><option value="012">012台北富邦商業銀行</option><option value="013">013國泰世華商業銀行</option><option value="016">016高雄銀行</option><option value="017">017兆豐國際商業銀行</option><option value="018">018全國農業金庫</option><option value="021">021花旗(台灣)商業銀行</option><option value="048">048王道商業銀行</option><option value="050">050臺灣中小企業銀行</option><option value="052">052渣打國際商業銀行</option><option value="053">053台中商業銀行</option><option value="054">054京城商業銀行</option><option value="081">081匯豐(台灣)銀行</option><option value="101">101瑞興商業銀行</option><option value="102">102華泰商業銀行</option><option value="103">103臺灣新光商業銀行</option><option value="104">104台北市第五信用合作社</option><option value="108">108陽信商業銀行</option><option value="114">114基隆第一信用合作社</option><option value="115">115基隆市第二信用合作社</option><option value="118">118板信商業銀行</option><option value="119">119淡水第一信用合作社</option><option value="120">120新北市淡水信用合作社</option><option value="124">124宜蘭信用合作社</option><option value="127">127桃園信用合作社</option><option value="130">130新竹第一信用合作社</option><option value="132">132新竹第三信用合作社</option><option value="146">146台中市第二信用合作社</option><option value="147">147三信商業銀行</option><option value="158">158彰化第一信用合作社</option><option value="161">161彰化第五信用合作社</option><option value="162">162彰化第六信用合作社</option><option value="163">163彰化第十信用合作社</option><option value="165">165彰化縣鹿港信用合作社</option><option value="178">178嘉義市第三信用合作社</option><option value="188">188台南第三信用合作社</option><option value="204">204高雄市第三信用合作社</option><option value="215">215花蓮第一信用合作社</option><option value="216">216花蓮第二信用合作社</option><option value="222">222澎湖縣第一信用合作社</option><option value="223">223澎湖第二信用合作社</option><option value="224">224金門縣信用合作社</option><option value="501">501宜蘭縣蘇澳區漁會</option><option value="502">502宜蘭縣頭城區漁會</option><option value="506">506桃園區漁會</option><option value="507">507新竹區漁會</option><option value="508">508通苑區漁會</option><option value="510">510南龍區漁會</option><option value="511">511彰化區漁會</option><option value="512">512雲林區漁會</option><option value="513">513新北市瑞芳區漁會</option><option value="514">514新北市萬里區漁會</option><option value="515">515嘉義區漁會</option><option value="516">516基隆區漁會</option><option value="517">517南市區漁會</option><option value="518">518南縣區漁會</option><option value="519">519新化區農會</option><option value="520">520高雄市漁會(小港區、高雄區等)</option><option value="521">521高雄市漁會(彌陀區、林園區、梓官區、永安區、興達港區等)</option><option value="523">523屏東縣漁會(東港區、枋寮區、林邊區、琉球區等)</option><option value="524">524新港區漁會</option><option value="525">525澎湖區漁會</option><option value="526">526金門區漁會</option><option value="538">538宜蘭市農會</option><option value="541">541白河區農會</option><option value="542">542麻豆區農會</option><option value="547">547後壁區農會</option><option value="549">549下營區農會</option><option value="551">551官田區農會</option><option value="552">552大內區農會</option><option value="556">556學甲區農會</option><option value="557">557新市區農會</option><option value="558">558安定區農會</option><option value="559">559山上區農會</option><option value="561">561左鎮區農會</option><option value="562">562仁德區農會</option><option value="564">564關廟區農會</option><option value="565">565龍崎區農會</option><option value="567">567南化區農會</option><option value="568">568七股區農會</option><option value="570">570南投市農會</option><option value="573">573埔里鎮農會</option><option value="574">574竹山鎮農會</option><option value="575">575中寮鄉農會</option><option value="577">577魚池鄉農會</option><option value="578">578水里鄉農會</option><option value="579">579國姓鄉農會</option><option value="580">580鹿谷鄉農會</option><option value="581">581信義鄉農會</option><option value="582">582仁愛鄉農會</option><option value="583">583東山區農會</option><option value="585">585頭城鎮農會</option><option value="586">586羅東鎮農會</option><option value="587">587礁溪鄉農會</option><option value="588">588壯圍鄉農會</option><option value="589">589員山鄉農會</option><option value="596">596五結鄉農會</option><option value="598">598蘇澳地區農會</option><option value="599">599三星地區農會</option><option value="600">600農金資訊股份有限公司</option><option value="602">602中華民國農會中壢辦事處信用部</option><option value="605">605高雄市高雄地區農會</option><option value="612">612臺中市農會(神岡區、豐原區等)</option><option value="613">613南投縣農會(名間鄉、集集鎮等)</option><option value="614">614彰化地區農會(員林市、二林鎮、秀水鄉、埔心鄉、永靖鄉、埤頭鄉、竹塘鄉、芬園鄉等)</option><option value="615">615基隆市農會</option><option value="616">616雲林地區農會(斗六市、虎尾鎮、西螺鎮、斗南鎮、古坑鄉、大埤鄉、莿桐鄉、二崙鄉等)</option><option value="617">617嘉義地區農會(朴子市、布袋鎮、大林鎮、民雄鄉、溪口鄉、東石鄉、義竹鄉、鹿草鄉等)</option><option value="618">618台南地區農會(鹽水區、佳里區、善化區、柳營區、六甲區、西港區、將軍區、北門區等)</option><option value="619">619高雄地區農會(鳳山區、岡山區、旗山區、小港區、美濃區、橋頭區、燕巢區、田寮區等)</option><option value="620">620屏東地區農會(東港鎮、恆春鎮、麟洛鄉、九如鄉、里港鄉、崁頂鄉、南州鄉、琉球鄉等)</option><option value="621">621花蓮縣農會(吉安鄉、壽豐鄉、富里鄉、新秀地區等)</option><option value="622">622台東縣農會(關山鎮、成功鎮、池上鄉、長濱鄉、台東地區、鹿野地區、太麻里地區等)</option><option value="624">624澎湖縣農會信用部</option><option value="625">625臺中地區農會信用部</option><option value="627">627連江縣農會</option><option value="628">628鹿港鎮農會</option><option value="629">629和美鎮農會</option><option value="631">631溪湖鎮農會</option><option value="632">632田中鎮農會</option><option value="633">633北斗鎮農會</option><option value="635">635線西鄉農會</option><option value="636">636伸港鄉農會</option><option value="638">638花壇鄉農會</option><option value="639">639大村鄉農會</option><option value="642">642社頭鄉農會</option><option value="643">643二水鄉農會</option><option value="646">646大城鄉農會</option><option value="647">647溪州鄉農會</option><option value="649">649埔鹽鄉農會</option><option value="650">650福興鄉農會</option><option value="651">651彰化市農會</option><option value="683">683北港鎮農會</option><option value="685">685土庫鎮農會</option><option value="693">693東勢鄉農會</option><option value="696">696水林鄉農會</option><option value="697">697元長鄉農會</option><option value="698">698麥寮鄉農會</option><option value="699">699林內鄉農會</option><option value="700">700中華郵政股份有限公司</option><option value="749">749內埔地區農會</option><option value="762">762大溪區農會</option><option value="763">763桃園區農會</option><option value="764">764平鎮區農會</option><option value="765">765楊梅區農會</option><option value="766">766大園區農會</option><option value="767">767蘆竹區農會</option><option value="768">768龜山區農會</option><option value="769">769八德區農會</option><option value="770">770新屋區農會</option><option value="771">771龍潭區農會</option><option value="772">772復興區農會</option><option value="773">773觀音區農會</option><option value="775">775土城區農會</option><option value="776">776三重區農會</option><option value="777">777中和地區農會</option><option value="778">778淡水區農會</option><option value="779">779樹林區農會</option><option value="780">780鶯歌區農會</option><option value="781">781三峽區農會</option><option value="785">785蘆洲區農會</option><option value="786">786五股區農會</option><option value="787">787林口區農會</option><option value="788">788泰山區農會</option><option value="789">789坪林區農會</option><option value="790">790八里區農會</option><option value="791">791金山地區農會</option><option value="792">792瑞芳地區農會</option><option value="793">793新店地區農會</option><option value="795">795深坑區農會</option><option value="796">796石碇區農會</option><option value="797">797平溪區農會</option><option value="798">798石門區農會</option><option value="799">799三芝區農會</option><option value="803">803聯邦商業銀行</option><option value="805">805遠東國際商業銀行</option><option value="806">806元大商業銀行</option><option value="807">807永豐商業銀行</option><option value="808">808玉山商業銀行</option><option value="809">809凱基商業銀行</option><option value="810">810星展(台灣)商業銀行</option><option value="812">812台新國際商業銀行</option><option value="816">816安泰商業銀行</option><option value="822">822中國信託商業銀行</option><option value="823">823將來商業銀行</option><option value="824">824連線商業銀行</option><option value="826">826樂天國際商業銀行</option><option value="860">860中埔鄉農會</option><option value="866">866阿里山鄉農會</option><option value="868">868東勢區農會</option><option value="869">869清水區農會</option><option value="870">870梧棲區農會</option><option value="871">871大甲區農會</option><option value="872">872沙鹿區農會</option><option value="874">874霧峰區農會</option><option value="875">875太平區農會</option><option value="876">876烏日區農會</option><option value="877">877后里區農會</option><option value="878">878大雅區農會</option><option value="879">879潭子區農會</option><option value="880">880石岡區農會</option><option value="881">881新社區農會</option><option value="882">882大肚區農會</option><option value="883">883外埔區農會</option><option value="884">884大安區農會</option><option value="885">885龍井區農會</option><option value="886">886和平區農會</option><option value="891">891花蓮市農會</option><option value="895">895瑞穗鄉農會</option><option value="896">896玉溪地區農會</option><option value="897">897鳳榮地區農會</option><option value="898">898光豐地區農會</option><option value="901">901大里區農會</option><option value="902">902苗栗市農會</option><option value="903">903汐止區農會</option><option value="904">904新莊區農會信用部</option><option value="906">906頭份市農會</option><option value="907">907竹南鎮農會</option><option value="908">908通霄鎮農會</option><option value="909">909苑裡鎮農會</option><option value="912">912冬山鄉農會</option><option value="913">913後龍鎮農會</option><option value="914">914卓蘭鎮農會</option><option value="915">915西湖鄉農會</option><option value="916">916草屯鎮農會</option><option value="917">917公館鄉農會</option><option value="918">918銅鑼鄉農會</option><option value="919">919三義鄉農會</option><option value="920">920造橋鄉農會</option><option value="921">921南庄鄉農會</option><option value="922">922臺南地區農會信用部</option><option value="923">923獅潭鄉農會</option><option value="924">924頭屋鄉農會</option><option value="925">925三灣鄉農會</option><option value="926">926苗栗縣大湖地區農會</option><option value="928">928板橋區農會信用部</option><option value="929">929關西鎮農會</option><option value="930">930新埔鎮農會</option><option value="931">931竹北市農會</option><option value="932">932湖口鄉農會</option><option value="933">933芎林鄉農會</option><option value="934">934寶山鄉農會</option><option value="935">935峨眉鄉農會</option><option value="936">936北埔鄉農會</option><option value="937">937竹東地區農會</option><option value="938">938橫山地區農會</option><option value="939">939新豐鄉農會</option><option value="940">940新竹市農會信用部</option><option value="952">952財團法人農漁會南區資訊中心</option><option value="953">953田尾鄉農會</option><option value="984">984北投區農會</option><option value="985">985士林區農會</option><option value="986">986內湖區農會</option><option value="987">987南港區農會</option><option value="988">988木柵區農會</option><option value="989">989景美區農會</option></select>
                                <p class="note" aria-hidden="true">限本人同身分證字號之金融機構代號/帳號</p>
                            </div>
                        </div>
                        <div class="item">
                            <label for="RegisterBE_BankAccount">本人/代領人金融機構帳號</label>
                            <div>
                                <input maxlength="16" aria-label="本人/代領人金融機構帳號" id="RegisterBE_BankAccount" name="RegisterBE.BankAccount" placeholder="8-16位數字(必填)" type="text" v-model="BankAccount">
                            </div>
                        </div>
                    </fieldset>
                    <fieldset id="childList">
                        <legend class="visually-hidden">發放對象健保卡號</legend>

                        <div class="item" id="healtNum">
                            <label for="RegisterBE_HealthId">發放對象健保卡號 <span class="visually-hidden">代領上限為4位(含本人5位)</span></label>
                            <div>
                                <div>
                                    <input maxlength="12" aria-label="發放對象健保卡號#1，代領上限為4位(含本人5位)" id="RegisterBE_HealthId" name="RegisterBE.HealthId" placeholder="12位數字(必填)" type="text" v-model="HealthId">
                                    <button id="removeNum" class="r delete" aria-label="刪除卡號#1">刪除</button>
                                </div>
                            </div>
                        </div>
                        <p class="note mlLabel" aria-hidden="true">代領上限為4位(含本人5位)</p>
                        <button id="addNum" class="g add indent" aria-label="新增">新增</button>
                    </fieldset>
                </div>
                    <div class="btns">
                        <button class="gray" type="button" aria-label="上一頁" >上一頁</button>
                        <button type="submit" aria-label="下一頁" >下一頁</button>
                    </div>
                    <input length="0" id="RegisterBE_SelectedBank" name="RegisterBE.SelectedBank" type="hidden" value=""><input id="SelectedBankName" name="SelectedBankName" type="hidden" value=""><input id="RegisterBE_HiddenHealth" name="RegisterBE.HiddenHealth" type="hidden" value="">
                </form>


            </div>
        </section>
    </main>
    <footer>
        <div>
            <a accesskey="B" class="guidePoint textWhite" href="javascript:void(0);" aria-label="下方功能區塊">:::</a>
            <a href="https://6000.gov.tw/EnRegister" aria-label="切換成英文語系(另開新視窗)" class="linkPage">(中文/English)</a>
            <span class="mobileShow"></span>
            <a href="https://6000.gov.tw/Register/Index#"  aria-label="隱私權聲明 (另開新視窗)">隱私權聲明</a>
            <a href="https://6000.gov.tw/Register/Index#"  aria-label="個人資料保護法告知義務內容 (另開新視窗)">個人資料保護法告知義務內容</a>
        </div>
        <a href="https://6000.gov.tw/Register/Index#"  aria-label="通過AA檢測等級無障礙網頁檢測(另開新視窗)">
            <img alt="" src="../assets/AA.png" style="height:31px; width:88px">
        </a>
    </footer>
</template>
<script>
export default {
    name: "Page6000",
    data() {
        return {
            ParentId: '',
            SelectedBank: '',
            BankAccount:'',
            HealthId:''
        }
    },
    methods: {

        registerAnswer() {
            if(this.ParentId.length!== 0 && this.SelectedBank.length!==0&& this.BankAccount.length!==0 && this.HealthId.length!==0){
                alert("資料已送出");
            }
            else if (this.ParentId.length!== 0&& this.SelectedBank.length!==0&& this.BankAccount.length!==0 && this.HealthId.length===0){
                alert( "健保卡未輸入\n");
            }
            else if (this.ParentId.length!== 0&& this.SelectedBank.length!==0&& this.BankAccount.length===0 && this.HealthId.length!==0){
                alert( "金融帳號未輸入\n");0
            }
            else if (this.ParentId.length!== 0&& this.SelectedBank.length!==0&& this.BankAccount.length===0 && this.HealthId.length===0){
                alert( "金融帳號未輸入\n"+"健保卡未輸入\n");
            }
            else if (this.ParentId.length!== 0&& this.SelectedBank.length===0&& this.BankAccount.length!==0 && this.HealthId.length!==0){
                alert("金融代碼未輸入\n");
            }
            else if (this.ParentId.length!== 0&& this.SelectedBank.length===0&& this.BankAccount.length!==0 && this.HealthId.length===0){
                alert("金融代碼未輸入\n"+"健保卡未輸入\n");
            }
            else if (this.ParentId.length!== 0&& this.SelectedBank.length===0&& this.BankAccount.length===0 && this.HealthId.length!==0){
                alert( "金融代碼未輸入\n"+"金融帳號未輸入\n");
            }
            else if (this.ParentId.length!== 0&& this.SelectedBank.length===0&& this.BankAccount.length===0 && this.HealthId.length===0){
                alert(  "金融代碼未輸入\n"+"金融帳號未輸入\n"+"健保卡未輸入\n");
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length!==0&& this.BankAccount.length!==0 && this.HealthId.length!==0){
                alert("身分證未輸入\n" );
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length!==0&& this.BankAccount.length!==0 && this.HealthId.length===0){
                alert("身分證未輸入\n" +"健保卡未輸入\n");
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length!==0&& this.BankAccount.length===0 && this.HealthId.length!==0){
                alert("身分證未輸入\n" +"金融帳號未輸入\n");
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length!==0&& this.BankAccount.length===0 && this.HealthId.length===0){
                alert("身分證未輸入\n"+"金融帳號未輸入\n"+"健保卡未輸入\n");
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length===0!==0&& this.BankAccount.length!==0 && this.HealthId.length!==0){
                alert("身分證未輸入\n" + "金融代碼未輸入\n");
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length===0!==0&& this.BankAccount.length!==0 && this.HealthId.length===0){
                alert("身分證未輸入\n" + "金融代碼未輸入\n"+"健保卡未輸入\n");
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length===0!==0&& this.BankAccount.length===0 && this.HealthId.length!==0){
                alert("身分證未輸入\n" + "金融代碼未輸入\n"+"金融帳號未輸入\n");
            }
            else if (this.ParentId.length===0 && this.SelectedBank.length===0!==0&& this.BankAccount.length===0 && this.HealthId.length===0){
                alert("身分證未輸入\n" + "金融代碼未輸入\n"+"金融帳號未輸入\n"+"健保卡未輸入\n");

            }
        }
    }
}
</script>
<style scoped>

</style>