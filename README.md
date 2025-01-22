# COM-13
-- MySQL Administrator dump 1.4
--
-- ------------------------------------------------------
-- Server version	5.5.5-10.4.32-MariaDB


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8 */;

/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;


--
-- Create schema purchase
--

CREATE DATABASE IF NOT EXISTS purchase;
USE purchase;

--
-- Definition of table `chat`
--

DROP TABLE IF EXISTS `chat`;
CREATE TABLE `chat` (
  `cid` int(11) DEFAULT NULL,
  `question` varchar(50) DEFAULT NULL,
  `answer` varchar(50) DEFAULT NULL,
  `user` varchar(50) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci ROW_FORMAT=COMPACT;

--
-- Dumping data for table `chat`
--

/*!40000 ALTER TABLE `chat` DISABLE KEYS */;
INSERT INTO `chat` (`cid`,`question`,`answer`,`user`) VALUES 
 (999,NULL,NULL,NULL),
 (1001,'hi','hi, welcome','sathish'),
 (1002,'ss','ss','sathish'),
 (1003,'hh','body temperature please','sathish');
/*!40000 ALTER TABLE `chat` ENABLE KEYS */;


--
-- Definition of table `chatbot`
--

DROP TABLE IF EXISTS `chatbot`;
CREATE TABLE `chatbot` (
  `cid` int(11) DEFAULT NULL,
  `question` varchar(255) DEFAULT NULL,
  `Answer` varchar(255) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci ROW_FORMAT=COMPACT;

--
-- Dumping data for table `chatbot`
--

/*!40000 ALTER TABLE `chatbot` DISABLE KEYS */;
INSERT INTO `chatbot` (`cid`,`question`,`Answer`) VALUES 
 (1000,'hi','hi, welcome'),
 (1001,'ss','ss'),
 (1002,'hh','body temperature please');
/*!40000 ALTER TABLE `chatbot` ENABLE KEYS */;


--
-- Definition of table `feedback`
--

DROP TABLE IF EXISTS `feedback`;
CREATE TABLE `feedback` (
  `pid` varchar(255) DEFAULT NULL,
  `pname` varchar(255) DEFAULT NULL,
  `price` varchar(255) DEFAULT NULL,
  `rate` int(255) DEFAULT NULL,
  `feedback` varchar(255) DEFAULT NULL,
  `uname` varchar(255) DEFAULT NULL,
  `gname` varchar(255) DEFAULT NULL,
  `feed` varchar(255) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `feedback`
--

/*!40000 ALTER TABLE `feedback` DISABLE KEYS */;
INSERT INTO `feedback` (`pid`,`pname`,`price`,`rate`,`feedback`,`uname`,`gname`,`feed`) VALUES 
 ('1000','HTC Chacha Touch Qwe','16000',1,'       bnbnbn     ','sridhar','GNAME','Good'),
 ('1000','HTC Chacha Touch Qwe','16000',2,'          bnbnbn  ','sridhar','GNAME','Better'),
 ('1000','HTC Chacha Touch Qwe','16000',3,'          bnbnbn  ','sridhar','GNAME','Good'),
 ('1000','HTC Chacha Touch Qwe','16000',4,'            bnbnbn','sridhar','GNAME','Worst'),
 ('100003','Samsung','26000',1,'     2211212       ','krishna','GNAME','Good'),
 ('100001','Samsung','5000',4,'        ghhggh    ','krishna','GNAME','Good'),
 ('100001','Samsung','5000',2,'         ggh   ','krishna','GNAME','Best');
/*!40000 ALTER TABLE `feedback` ENABLE KEYS */;


--
-- Definition of table `login`
--

DROP TABLE IF EXISTS `login`;
CREATE TABLE `login` (
  `uname` varchar(50) DEFAULT NULL,
  `pass` varchar(50) DEFAULT NULL,
  `ipaddres` varchar(50) DEFAULT NULL,
  `ldate` varchar(50) DEFAULT NULL,
  `status` varchar(50) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `login`
--

/*!40000 ALTER TABLE `login` DISABLE KEYS */;
INSERT INTO `login` (`uname`,`pass`,`ipaddres`,`ldate`,`status`) VALUES 
 ('sathish','sathish','192.168.1.69','Thu Mar 13 02:13:32 IST 2014','Illegal Process'),
 ('sathish','sathish','192.168.1.69','Thu Mar 13 02:15:55 IST 2014','Illegal Process'),
 ('sathish','sathish','192.168.1.69','Thu Mar 13 02:18:16 IST 2014','Illegal Process'),
 ('sridhar','sridhar','192.168.1.69','Thu Mar 13 02:19:45 IST 2014','Correct User'),
 ('sridhar','sridhar','192.168.1.69','Thu Mar 13 13:35:34 IST 2014','Correct User');
/*!40000 ALTER TABLE `login` ENABLE KEYS */;


--
-- Definition of table `offers`
--

DROP TABLE IF EXISTS `offers`;
CREATE TABLE `offers` (
  `oid` int(250) NOT NULL,
  `pid` varchar(50) NOT NULL DEFAULT '',
  `pname` varchar(255) NOT NULL,
  `pdetail` longtext DEFAULT NULL,
  `price` varchar(255) DEFAULT NULL,
  `discount` varchar(255) DEFAULT NULL,
  `stock` varchar(255) DEFAULT NULL,
  `uname` varchar(255) DEFAULT NULL,
  `dates` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`oid`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci ROW_FORMAT=DYNAMIC;

--
-- Dumping data for table `offers`
--

/*!40000 ALTER TABLE `offers` DISABLE KEYS */;
INSERT INTO `offers` (`oid`,`pid`,`pname`,`pdetail`,`price`,`discount`,`stock`,`uname`,`dates`) VALUES 
 (999999,'100001','SAMSUNG Galaxy F05 ','Description\r\nThe latest Samsung Galaxy F05 PLS LCD display provides immersive viewing experience with 20:9 Aspect Ratio Full HD+ Resolution with 720 x 1600 Pixels and 60Hz Refresh Rate. 5000mAh battery gives you power to use your smartphone without worrying about frequent charging. And you get up to 2 generations of Android Upgrades with 4 years of security updates that provides you the best OS experience available for the next 2 years with Samsung One UI. Powered by MediaTek Helio G85 processor you can easily multi-task and play games with ease. Brilliant 50MP Camera with 8MP Selfie Camera lets you capture memories beautifully which you can share with your friends & family.AM)','15000','10','120','admin','2024-11-15'),
 (1000000,'100001','SAMSUNG Galaxy F05 ','Description\r\nThe latest Samsung Galaxy F05 PLS LCD display provides immersive viewing experience with 20:9 Aspect Ratio Full HD+ Resolution with 720 x 1600 Pixels and 60Hz Refresh Rate. 5000mAh battery gives you power to use your smartphone without worrying about frequent charging. And you get up to 2 generations of Android Upgrades with 4 years of security updates that provides you the best OS experience available for the next 2 years with Samsung One UI. Powered by MediaTek Helio G85 processor you can easily multi-task and play games with ease. Brilliant 50MP Camera with 8MP Selfie Camera lets you capture memories beautifully which you can share with your friends & family.AM)','15000','10','10','admin','2024-11-15'),
 (1000001,'100002','OPPO F9','Network	Technology	\r\nGSM / HSPA / LTE / 5G\r\nLaunch	Announced	2021  March 08\r\nStatus	Available. Released 2021  March 17\r\nBody	Dimensions	160.1 x 73.4 x 7.8 mm (6.30 x 2.89 x 0.31 in)\r\nWeight	173 g (6.10 oz)\r\nSIM	Dual SIM (Nano-SIM  dual stand-by)\r\nDisplay	Type	Super AMOLED  430 nits (typ)  800 nits (peak)\r\nSize	6.43 inches  99.8 cm2 (~84.9% screen-to-body ratio)\r\nResolution	1080 x 2400 pixels  20:9 ratio (~409 ppi density)\r\nProtection	Corning Gorilla Glass 5\r\nPlatform	OS	Android 11  upgradable to Android 12  ColorOS 12\r\nChipset	Mediatek Dimensity 800U (7 nm)\r\nCPU	Octa-core (2x2.4 GHz Cortex-A76 & 6x2.0 GHz Cortex-A55)\r\nGPU	Mali-G57 MC3\r\nMemory	Card slot	microSDXC (dedicated slot)\r\nInternal	128GB 8GB RAM\r\n 	UFS 2.1\r\nMain Camera	Quad	48 MP  f/1.7  25mm (wide)  1/2.0\"  0.8?m  PDAF\r\n8 MP  f/2.2  16mm  119?? (ultrawide)  1/4.0\"  1.12?m\r\n2 MP  f/2.4  (macro)\r\n2 MP  f/2.4  (depth)\r\nFeatures	LED flash  HDR  panorama\r\nVideo	4K@30fps  1080p@30/120fps; gyro-EIS  HDR\r\nSelfie camera	Single	16 MP  f/2.4  26mm (wide)  1/3.09\"  1.0?m\r\nFeatures	HDR\r\nVideo	1080p@30fps\r\nSound	Loudspeaker	Yes\r\n3.5mm jack	Yes\r\nComms	WLAN	Wi-Fi 802.11 a/b/g/n/ac  dual-band  Wi-Fi Direct\r\nBluetooth	5.1  A2DP  LE  aptX HD\r\nPositioning	GPS  GLONASS  GALILEO  BDS\r\nNFC	No\r\nRadio	Unspecified\r\nUSB	USB Type-C 2.0  OTG\r\nFeatures	Sensors	Fingerprint (under display  optical)  accelerometer  gyro  proximity  compass\r\nBattery	Type	Li-Po 4310 mAh  non-removable\r\nCharging	50W wired  100% in 48 min (advertised)\r\nMisc	Colors	Fluid Black  Space Silver  Cosmo Blue\r\nModels	CPH2213\r\nPrice	About 300 EUR','15000','10','0','admin','2024-11-15');
/*!40000 ALTER TABLE `offers` ENABLE KEYS */;


--
-- Definition of table `product`
--

DROP TABLE IF EXISTS `product`;
CREATE TABLE `product` (
  `pid` int(250) NOT NULL,
  `pname` varchar(255) NOT NULL,
  `image` varchar(255) DEFAULT NULL,
  `pdetail` longtext DEFAULT NULL,
  `price` varchar(255) DEFAULT NULL,
  `discount` varchar(255) DEFAULT NULL,
  `stock` varchar(255) DEFAULT NULL,
  `type` varchar(255) DEFAULT NULL,
  `uname` varchar(255) DEFAULT NULL,
  `rank` int(11) DEFAULT NULL,
  `category` varchar(50) DEFAULT NULL,
  `cprice` int(11) DEFAULT NULL,
  `pcount` int(11) DEFAULT NULL,
  PRIMARY KEY (`pid`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `product`
--

/*!40000 ALTER TABLE `product` DISABLE KEYS */;
INSERT INTO `product` (`pid`,`pname`,`image`,`pdetail`,`price`,`discount`,`stock`,`type`,`uname`,`rank`,`category`,`cprice`,`pcount`) VALUES 
 (100001,'SAMSUNG Galaxy F05 ','100002.jpg','Description\r\nThe latest Samsung Galaxy F05 PLS LCD display provides immersive viewing experience with 20:9 Aspect Ratio Full HD+ Resolution with 720 x 1600 Pixels and 60Hz Refresh Rate. 5000mAh battery gives you power to use your smartphone without worrying about frequent charging. And you get up to 2 generations of Android Upgrades with 4 years of security updates that provides you the best OS experience available for the next 2 years with Samsung One UI. Powered by MediaTek Helio G85 processor you can easily multi-task and play games with ease. Brilliant 50MP Camera with 8MP Selfie Camera lets you capture memories beautifully which you can share with your friends & family.AM)','15000','10','250','Samsung','admin',0,'Mobile',13000,0),
 (100002,'OPPO F9','100003.jpg','Network	Technology	\r\nGSM / HSPA / LTE / 5G\r\nLaunch	Announced	2021  March 08\r\nStatus	Available. Released 2021  March 17\r\nBody	Dimensions	160.1 x 73.4 x 7.8 mm (6.30 x 2.89 x 0.31 in)\r\nWeight	173 g (6.10 oz)\r\nSIM	Dual SIM (Nano-SIM  dual stand-by)\r\nDisplay	Type	Super AMOLED  430 nits (typ)  800 nits (peak)\r\nSize	6.43 inches  99.8 cm2 (~84.9% screen-to-body ratio)\r\nResolution	1080 x 2400 pixels  20:9 ratio (~409 ppi density)\r\nProtection	Corning Gorilla Glass 5\r\nPlatform	OS	Android 11  upgradable to Android 12  ColorOS 12\r\nChipset	Mediatek Dimensity 800U (7 nm)\r\nCPU	Octa-core (2x2.4 GHz Cortex-A76 & 6x2.0 GHz Cortex-A55)\r\nGPU	Mali-G57 MC3\r\nMemory	Card slot	microSDXC (dedicated slot)\r\nInternal	128GB 8GB RAM\r\n 	UFS 2.1\r\nMain Camera	Quad	48 MP  f/1.7  25mm (wide)  1/2.0\"  0.8?m  PDAF\r\n8 MP  f/2.2  16mm  119?? (ultrawide)  1/4.0\"  1.12?m\r\n2 MP  f/2.4  (macro)\r\n2 MP  f/2.4  (depth)\r\nFeatures	LED flash  HDR  panorama\r\nVideo	4K@30fps  1080p@30/120fps; gyro-EIS  HDR\r\nSelfie camera	Single	16 MP  f/2.4  26mm (wide)  1/3.09\"  1.0?m\r\nFeatures	HDR\r\nVideo	1080p@30fps\r\nSound	Loudspeaker	Yes\r\n3.5mm jack	Yes\r\nComms	WLAN	Wi-Fi 802.11 a/b/g/n/ac  dual-band  Wi-Fi Direct\r\nBluetooth	5.1  A2DP  LE  aptX HD\r\nPositioning	GPS  GLONASS  GALILEO  BDS\r\nNFC	No\r\nRadio	Unspecified\r\nUSB	USB Type-C 2.0  OTG\r\nFeatures	Sensors	Fingerprint (under display  optical)  accelerometer  gyro  proximity  compass\r\nBattery	Type	Li-Po 4310 mAh  non-removable\r\nCharging	50W wired  100% in 48 min (advertised)\r\nMisc	Colors	Fluid Black  Space Silver  Cosmo Blue\r\nModels	CPH2213\r\nPrice	About 300 EUR','15000','10','130','OPPO','admin',0,'Mobile',12000,0);
/*!40000 ALTER TABLE `product` ENABLE KEYS */;


--
-- Definition of table `purchase`
--

DROP TABLE IF EXISTS `purchase`;
CREATE TABLE `purchase` (
  `pid` int(255) NOT NULL,
  `uname` varchar(45) NOT NULL,
  `pname` varchar(45) NOT NULL,
  `price` varchar(45) NOT NULL,
  `discount` varchar(45) NOT NULL,
  `amount` varchar(45) NOT NULL,
  `nproduct` varchar(45) NOT NULL,
  `total` varchar(45) NOT NULL,
  `date` varchar(45) NOT NULL,
  `type` varchar(45) NOT NULL,
  `upname` varchar(45) NOT NULL,
  `category` varchar(45) NOT NULL,
  `proid` varchar(45) NOT NULL,
  `selling` varchar(45) NOT NULL,
  `costing` varchar(45) NOT NULL,
  PRIMARY KEY (`pid`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `purchase`
--

/*!40000 ALTER TABLE `purchase` DISABLE KEYS */;
INSERT INTO `purchase` (`pid`,`uname`,`pname`,`price`,`discount`,`amount`,`nproduct`,`total`,`date`,`type`,`upname`,`category`,`proid`,`selling`,`costing`) VALUES 
 (1000000,'mahendra','Mobile','26000','520','25480','1','25480','2024-01-11','Samsung','admin','samsung-metro-e2202','100003','26000','23000'),
 (1000001,'asvp','Mobile','26000','520','25480','9','229320','2024-11-14','Samsung','admin','samsung-metro-e2202','100003','26000','23000');
/*!40000 ALTER TABLE `purchase` ENABLE KEYS */;


--
-- Definition of table `purchases`
--

DROP TABLE IF EXISTS `purchases`;
CREATE TABLE `purchases` (
  `pid` int(255) NOT NULL,
  `uname` varchar(255) NOT NULL,
  `pname` varchar(255) NOT NULL,
  `price` varchar(299) NOT NULL,
  `discount` varchar(299) NOT NULL,
  `amount` varchar(255) NOT NULL,
  `nproduct` varchar(255) NOT NULL,
  `total` varchar(255) NOT NULL,
  `date` varchar(255) NOT NULL,
  `type` varchar(255) NOT NULL,
  `sid` varchar(255) NOT NULL,
  `ipaddress` varchar(255) NOT NULL,
  `rtime` varchar(255) NOT NULL,
  `page1` varchar(255) NOT NULL,
  PRIMARY KEY (`pid`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci ROW_FORMAT=COMPACT;

--
-- Dumping data for table `purchases`
--

/*!40000 ALTER TABLE `purchases` DISABLE KEYS */;
INSERT INTO `purchases` (`pid`,`uname`,`pname`,`price`,`discount`,`amount`,`nproduct`,`total`,`date`,`type`,`sid`,`ipaddress`,`rtime`,`page1`) VALUES 
 (10001,'sridhar','sdsd','10','24','221','10','2210','2013-04-09','sdsd','1000001','192.168.1.65','Tue Apr 09 14:46:50 IST 2013','http://localhost:8084/VirtualOnlineShopping/p1?a1=1000'),
 (10002,'sridhar','sdsdsd','10','24','221','10','2210','2013-04-09','sdsd','1000002','192.168.1.65','Tue Apr 09 15:14:28 IST 2013','http://localhost:8084/VirtualOnlineShopping/p1?a1=1000'),
 (10003,'sridhar','Mobile','0','0','16000','2','32000','2014-03-04','HTC Chacha Touch Qwe','1000003','192.168.1.69','Tue Mar 04 11:27:39 IST 2014','http://localhost:8084/VirtualOnlineShopping/p1?a1=1000');
/*!40000 ALTER TABLE `purchases` ENABLE KEYS */;


--
-- Definition of table `question`
--

DROP TABLE IF EXISTS `question`;
CREATE TABLE `question` (
  `qid` varchar(20) NOT NULL,
  `question` varchar(255) NOT NULL,
  PRIMARY KEY (`qid`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `question`
--

/*!40000 ALTER TABLE `question` DISABLE KEYS */;
INSERT INTO `question` (`qid`,`question`) VALUES 
 ('0','Select  the Security Question'),
 ('1','What is your Pet name?'),
 ('2','What is your first mobile name?'),
 ('3','What is your father name?'),
 ('4','What is your hobby?'),
 ('5','What is your partner name?'),
 ('6','What is your partner petname?');
/*!40000 ALTER TABLE `question` ENABLE KEYS */;


--
-- Definition of table `randomno`
--

DROP TABLE IF EXISTS `randomno`;
CREATE TABLE `randomno` (
  `name` varchar(20) DEFAULT NULL,
  `password` varchar(45) DEFAULT NULL,
  `random1` varchar(45) DEFAULT NULL,
  `cal` varchar(45) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `randomno`
--

/*!40000 ALTER TABLE `randomno` DISABLE KEYS */;
INSERT INTO `randomno` (`name`,`password`,`random1`,`cal`) VALUES 
 ('sridhar','sridhar','99281','1285091246'),
 ('sathish','sathish','36328','-1949718502'),
 ('mahesh','mahesh','2286','0'),
 ('mahendran','mahendran','94053','-1928804');
/*!40000 ALTER TABLE `randomno` ENABLE KEYS */;


--
-- Definition of table `randoms`
--

DROP TABLE IF EXISTS `randoms`;
CREATE TABLE `randoms` (
  `uname` varchar(50) DEFAULT NULL,
  `rdm` varchar(50) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `randoms`
--

/*!40000 ALTER TABLE `randoms` DISABLE KEYS */;
INSERT INTO `randoms` (`uname`,`rdm`) VALUES 
 ('10','972'),
 ('siva','507'),
 ('mahendra','324'),
 ('asvp','885');
/*!40000 ALTER TABLE `randoms` ENABLE KEYS */;


--
-- Definition of table `register`
--

DROP TABLE IF EXISTS `register`;
CREATE TABLE `register` (
  `userid` varchar(20) NOT NULL,
  `username` varchar(45) NOT NULL,
  `password` varchar(45) NOT NULL,
  `name` varchar(45) NOT NULL,
  `dob` varchar(45) NOT NULL,
  `email` varchar(45) NOT NULL,
  `address` varchar(255) NOT NULL,
  `question` varchar(255) NOT NULL,
  `answer` varchar(255) NOT NULL,
  `mobile` varchar(45) NOT NULL,
  `image` varchar(45) NOT NULL,
  `creditcard` varchar(255) NOT NULL,
  `gname` varchar(255) NOT NULL,
  `role` varchar(255) NOT NULL,
  `amt` varchar(255) NOT NULL,
  `img` varchar(255) NOT NULL,
  PRIMARY KEY (`userid`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `register`
--

/*!40000 ALTER TABLE `register` DISABLE KEYS */;
INSERT INTO `register` (`userid`,`username`,`password`,`name`,`dob`,`email`,`address`,`question`,`answer`,`mobile`,`image`,`creditcard`,`gname`,`role`,`amt`,`img`) VALUES 
 ('478','asvp','asvp','asvp','1986-11-12','asvperumal@gmail.com','cbe','What is your Pet name?','asvp','9791334452','','1234567890123456','','User','0','');
/*!40000 ALTER TABLE `register` ENABLE KEYS */;


--
-- Definition of table `uproduct`
--

DROP TABLE IF EXISTS `uproduct`;
CREATE TABLE `uproduct` (
  `rid` int(255) NOT NULL,
  `pid` varchar(50) NOT NULL DEFAULT '',
  `pname` varchar(50) NOT NULL DEFAULT '',
  `uname` varchar(45) NOT NULL,
  `phone` varchar(45) NOT NULL,
  `mails` varchar(45) NOT NULL,
  `name` varchar(45) NOT NULL,
  `nos` int(11) NOT NULL,
  PRIMARY KEY (`rid`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci ROW_FORMAT=DYNAMIC;

--
-- Dumping data for table `uproduct`
--

/*!40000 ALTER TABLE `uproduct` DISABLE KEYS */;
INSERT INTO `uproduct` (`rid`,`pid`,`pname`,`uname`,`phone`,`mails`,`name`,`nos`) VALUES 
 (100001,'100002','OPPO F9','asvp','9791334452','asvperumal@gmail.com','asvp',4);
/*!40000 ALTER TABLE `uproduct` ENABLE KEYS */;




/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
