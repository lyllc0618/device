# device
CREATE TABLE `device` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `user_id` int(11) DEFAULT NULL COMMENT '用户ID',
  `name` int(11) DEFAULT NULL COMMENT '设备名称',
  `create_time` int(11) DEFAULT NULL COMMENT '创建时间',
  `status` tinyint(4) DEFAULT NULL COMMENT '状态',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

CREATE TABLE `device_test_data` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `device_id` int(11) DEFAULT NULL COMMENT '设备ID',
  `user_id` int(11) DEFAULT NULL COMMENT '检测用户ID',
  `voltage_value` int(11) DEFAULT NULL COMMENT '电压值',
  `test_time` datetime DEFAULT NULL COMMENT '测试时间',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

CREATE TABLE `user` (
  `ID` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `person_id` int(11) unsigned DEFAULT NULL,
  `USER_NAME` varchar(64) DEFAULT NULL,
  `PASSWORD` varchar(64) DEFAULT NULL,
  `TELEPHONE` char(11) DEFAULT NULL,
  PRIMARY KEY (`ID`),
  KEY `idx_person_id` (`person_id`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=utf8;
