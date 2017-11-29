# panCell
TableViewCell自定义左滑菜单
1、创建 cell 继承 PanTableViewCell  
2、添加PanTableViewCellDelegate协议方法
3、实现协议方法
#import "PanCellButton.h"
- (NSArray<PanCellButton *> *)panTableViewCell:(PanTableViewCell *)cell tableView:(UITableView *)tableView rightPanCellButtonsAtIndexPath:(NSIndexPath *)indexPath{
    
    PanCellButton *removeFollowUserButton = [[PanCellButton alloc] initWithTitle:nil image:[UIImage imageNamed:@"UserView_follow1"] onClickCallback:^(UIButton *panButton) {
        [self CancelFollowAction];
    }];
    
    PanCellButton *hiddenUserButton = [[PanCellButton alloc] initWithTitle:nil image:[UIImage imageNamed:@"UserView_follow2"] onClickCallback:^(UIButton *panButton) {
        [self ShieldingUser];
    }];
    
    return @[hiddenUserButton,removeFollowUserButton];
}
