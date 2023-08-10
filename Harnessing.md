#  Madara और Starknet Appchains
###  कैसे Madara blockchain infrastructure का भविष्य बदल रहा है 

##  संक्षेप में: 
- Madara एक तेज़ Starknet sequencer है, जिससे आप customizable [appchains](https://www.starknet.io/en/posts/ecosystem/the-starknet-stacks-growth-spurt) बना सकते हैं. 
- Substrate framework का इस्तेमाल करके, Madara Cairo VM की शक्तियों  को बढ़ता है, जो provable, secure और flexible programs की तरफ ले जाता है.
- इसको इस्तेमाल करने से कई फायदे मिलते हैं, जैसे की scalable infrastructure, ज़्यादा throughput और applications पर नियंत्रण.
- Madara की विशेषताओं में on-chain privacy का सपोर्ट, अलग अलग chains के बीच आसान interoperability, और मज़बूत execution शामिल है. 
- Madara dApp बनाने की दुनिया में एक नया रास्ता बना रही है, blockchain के क्षेत्र में सस्ता, scalable और customizable solution प्रदान करके. 

सोचो अगर आप अपनी application की ज़रूरतों  के हिसाब से एक blockchain बना सकते – appchains आपको यही करने का मौका देते हैं. Appchains application-specific blockchain होते हैं जो developers को blockchain के कई पहलुओं को अपनी application की ज़रूरतों के हिसाब से चयन करने का मौका देते हैं, चाहे वो एक अलग hash function हो या फिर एक consensus algorithm. और सबसे अच्छी बात? appchains जिस भी L2 या L1 के ऊपर बने हैं, उसकी security को प्राप्त (inherit) करते हैं. ऐसे में, developers को दोनों के फायदे उठा सकते हैं. 

पेश है, Madara, एक नया sequencer जो खेल बदल देगा, Madara flexible भी है और तेज़ भी. Sequencers transactions को execute करके उनको batches में group करते हैं.  अपने खुद के Starknet appchain को लॉन्च करने के लिए एक गेटवे के रूप में काम करते हुए, Madara ने Starknet ecosystem में प्रयोग के लिए संभावनाओं का एक क्षेत्र खोल दिया, जैसा पहले कभी नहीं था. 

Madara की क्षमताओं के बारे में जानने से पहले, सवाल करना ज़रूरी है कि developers क्यों Starknet के ऊपर एक  appchain बनाने का चयन करेंगे, [Starknet Validity Rollup](https://starkware.co/resource/scaling-ethereum-navigating-the-blockchain-trilemma/#:~:text=top%20of%20them.-,Validity%20Rollups,-Validity%20rollups%2C%20also) का सीधे उपयोग करने की बजाय। क्या Starknet ज़्यादातर परिस्थितियों के लिए काफी नहीं हैं? 

## Appchains के फायदे 
Madara को  StarkWare Explorations team ने बनाया है, जिसे [Keep Starknet Strange](https://github.com/keep-starknet-strange) के नाम से भी जाना जाता है, StarkWare के [Fractal Scaling](https://medium.com/starkware/fractal-scaling-from-l2-to-l3-7fe238ecfb4f) वाले vision को पूरा करने के लिए. कई काफी अच्छे कारण हैं जिनकी वजह से developers Starknet के ऊपर appchains या L3 बनाने का फैसला करेंगे, सीधे Starknet पर निर्भर होने की जगह. 

## Speed और Efficiency 
App developers को आज के blockchains में एक बड़ी दिक्कत का सामना करना पड़ता है: scalability. scalability के अंदर हम दो चीज़ों को देखते हैं: ज़्यादा स्पीड और काम फीस. हर layer में cost को 1000x काम करके, developers L2 से L3 तक overall cost को काफी काम कर सकते हैं, हो सकता हैं की 1,000,000x तक भी काम हो जाए. और इसके अलावा, किसी भी दूसरी application की activity से आपकी application की performance पर कोई फर्क नहीं पड़ता हैं, क्योंकि हर app के लिए एक अलग blockchain है, जिससे apps को आपस में resouces के लिए compete नहीं करना पड़ता है. ऐसा करके हमेशा एक जैसा अच्छा experience मिलता है. 

## Customizability 
Starknet और Ethereum जैसे जनरल-पर्पस blockchainस में सभी की सुविधा का ध्यान रखते हुए कई मेझस होते हैं, ताकि ये सुनिश्चित हो जाए की किसी को नेटवर्क इस्तेमाल करने म कोई दिक्कत ना हो. लेकिन appchains के साथ डेवलपरस अपने applications और infrastructure के अलग अलग पहलुओं को अपने हिसाब से सेट करके, अपनी ज़रूरतon के लिए एक बेहतर blockchain बना सकते हैं. Cairo VM का कोई फीचर पसंद नहीं आया? तो उससे अपनी appchains में से हटा दें. 

## Innovation
Appchains की customizability developers को ऐसे features के साथ काम करने का मौका देती है जो की Starknet जैसे blockchains में या तो उपलब्ध नहीं होते या नुकसानदायक हो सकते हैं. Appchains developers को अपनी marzi अनुसार code hints को लिखने और authorize करने देता है. इससे appchains के कई नए इस्तेमाल हो सकते हैं, जैसे की on-chain KYC करना, बिना किसी की private जानकारी को leak किये. 

## Madara's Effect on the Appchain Stack
चलो देखते हैं की appchains को संभव करने वाली layers आपस में कैसे काम करती हैं, और इनमे Madara का क्या काम है. 

- Execution: Execution layer तय करता है की blocks कैसे execute हों और state difference कैसे उत्पन्न होगा. Madara 2 execution crates के बीच switch करने की चॉइस देता है, StarkWare का Blockifier और LambdaClass का Starknet_in_Rust. चाहे जो भी crate इस्तेमाल हो, वो Cairo VM का इस्तेमाल करता है. Cairo provable programs बनाने में मदद करता हैं. 
- Settlement: एक Validity Rollup के तौर पर, Madara appchains के state को सिर्फ settlement layer को देख (examine) करके किआ जा सकता है. Starknet ल२ पर ज़्यादा बार settlement होने से, एक L3 appchains जल्दी से hard finality पा सकता है, जबकि Sequencing layer को decentralize करने से सख्त soft finality मिलती है. इस तरह, settlement दोनों तरफ से (hard और soft finality) सुधर जाती है. 
- Sequencing: Madara Sequencing की ज़िम्मेदारी उठाता है, जो की application की ज़रूरत के अनुसार modify किआ जा सकता है - चाहे वो FCFS हो, PGA हो या फिर Narwhall & Bullshark जैसी कठिन scheme हो. कुछ appchains encrypted mempools को deploy करने का चयन कर सकते हैं ताकि fair ordering को सुनिश्चित किया जा सके और MEV का असर काम हो सके.
- Data Availability: Data Availability पूरे state tree को accessible रखने की गारंटी देता है, दोनों  को विश्वास रहे की वो अपने assets की ownership को साबित कर सकें, अगर कभी Madara में दिक्कत आये तब भी. Madara developers को अलग अलग data Availability schemes में से चुनने की सुविधा देगा.
- Governance: हर Madara appchain अपनी governance model choose कर सकता है. [SnapshotX](https://twitter.com/SnapshotLabs) एक fully on-chain governance का option देता है जो Storage Proofs पर निर्भर है. दुसरे governance mechanisms भी exploration में हैं, जैसे की native Substrate governance pallet .On-chain governance Madara के लिए एक core value है.  

## Madara
Madara में, Cairo VM को Substrate framework का इस्तेमाल करके निखारा गया है. Substrate एक open-source Rust framework है जिसे customizable blockchains बनाने के लिए इस्तेमाल किआ जा सकता है, जो अपनी flexibility के लिए जाना जाता है. वहीँ, Cairo VM को इस मकसद से बनाया गया है की वो Validity Proofs efficiently generate कर सके. State tracking और smart contracts (Proofs को L2 पर verify करने के लिए) का इस्तेमाल करके, appchains Starknet के साथ integration सुनिश्चित कर सकता है. इस तरीके से, Madara Cairo का इस्तेमाल program execution की provability को सक्षम करने के लिए करता है. 

Substrate framework स्वाभाव से modular nature का है, जो developers को आसानी है appchains को customize करने की अनुमति देता है. कोई assumptions लागू नहीं होते, आप अपने हिसाब से consensus protocol, hash function, signature scheme, storage layout को चुन सकते हैं – जो भी आपको चाहिए, वो भी साथ में Cairo का इस्तेमाल करके Proofs generate करने के लिए. Developers बिना पाबंदी के कुछ भी कर सकते हैं, वो भी provable रहते हुए, और underlying chain की security को inherit करते हुए, चाहे वो Starknet हो या Ethereum. 

शुरुआत में, Madara Starknet से काफी सामान लगेगा, ताकि Starknet ecosystem के अंदर smart contracts की composability मुमकिन हो. आगे चलके, Starknet का Herodotus से integration होगा तो [Storage Proofs](https://book.starknet.io/chapter_8/storage_proofs.html) का इस्तेमाल होगा interoperability के लिए. Storage Proofs की मदद से Madara appchains दुसरे chains की state और liquidity को भी consider कर पाएंगे. 

Starknet की दुनिया में, Madara की वजह से कई नयी चीज़ों को संभव होते देखिये. 

