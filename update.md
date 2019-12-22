## 更新日志
## 2019年12月21日

1. 优化:新增切换博客主题模板功能。
2. 新增：博客主题管理功能。

菜单sql:
INSERT INTO `sys_menu` (`menu_id`, `menu_name`, `parent_id`, `order_num`, `url`, `target`, `menu_type`, `visible`, `perms`, `icon`, `create_by`, `create_time`, `update_by`, `update_time`, `remark`) VALUES ('3096', '博客主题', '2025', '1', '/cms/blogTheme', 'menuItem', 'C', '0', 'cms:blogTheme:view', '#', 'admin', '2019-12-21 08:50:08', '', NULL, '');

CREATE TABLE `blog_theme` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(100) DEFAULT NULL COMMENT '主题名称',
  `code` varchar(50) DEFAULT NULL COMMENT '主题代码',
  `cover_img` varchar(255) DEFAULT NULL COMMENT '封面图片',
  `create_time` datetime DEFAULT NULL COMMENT '创建时间',
  `create_by` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8;

INSERT INTO `blog_theme` VALUES ('1', 'Avatar响应式博客模版主题', 'avatar', '/images/cover/1561132050443308.jpg', '2019-12-21 08:55:00', 'ry');
INSERT INTO `blog_theme` VALUES ('2', '葡萄资讯模板主题，葡萄内容管理系统模板主题', 'pnews', '/images/cover/201903051436106979.jpg', '2019-12-21 08:55:31', 'ry');
INSERT INTO `blog_theme` VALUES ('3', '“pblog”个性博客模版主题，PT-CMS模版主题，免费下载', 'pblog', '/images/cover/pblog.jpg', '2019-12-21 08:55:58', 'ry');