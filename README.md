//
//  main.m
//  Lesson_7_31_数组
//
//  Created by lanou3g on 15/7/31.
//  Copyright (c) 2015年 lanou3g. All rights reserved.
//

#import <Foundation/Foundation.h>

int main(int argc, const char * argv[]) {
    //    相同数据类型 的成员组成的  一组数据,叫做数组
    //    数组是一种 构造类型. 相同的 数据类型 组成的新数据类型
    //    一维数组的定义
    //    类型说明符  数组名[常量表达式] = {值1,值2...};
    //    int  array[50] = {10,20,30};
    //    float oc_score[40]= {30};
    //    1.达到数组规定长度
    //    int a[3]= {0,1,2};
    //    2.数组中没有设置初始值的元素,自动设置为0
    //    int b[5] = {1,2,3};
    //    3.不初始化,默认全是 0
    //    int c[5];
    //    4.根据初始化的设置,推断出数组元素的个数
    //int d[] = {1,2,3,4,5};
    
    //    int e[2] = {1,12,3,4} //错的,元素个数 < 数组长度
    //    int f[] = {0}; //既没有确定元素个数,也没有初始值.
    //    数组的地址空间的开辟
    //    1.空间大小 = 元素的个数  * 类型的字节数
    //    2.开辟的空间是连续的
    //    数组元素的访问
    //    1).不能一次调用所有元素的值
    //    2).基本数据类型存储一个值,数组中存储多数据
    //    3).使用下标实现数组元素的访问,   数组名[下标]
    //    4).下标:是数组元素在数组中的序号,数组是有序的,每个元素都有自己唯一的序号,序号是从0开始的,最后一个元素的下标是 n - 1
    
    
    //    int array[4] = {1,2,3,4};
    //    for (int i = 0; i < 4; i ++) {
    //            printf("%d\t",array[i]);
    //    }
    
    
    //    for (int i = 3; i >= 0; i --) {
    //        printf("%d\t",array[i]);
    //    }
    //
    //    printf("\n");
    //                         修改数组元素
    //    int array1[5];
    ////    for (int i = 0; i < 5;  i++) {   //遍历数组
    ////        printf("%d  ",array1[i]);
    ////    }
    //    printf("\n");
    //    for (int i = 0; i < 5; i ++ ) {
    //        array1[i]=( arc4random() % (20 - 10 + 1) + 10);
    //
    //    }
    //
    //    for (int i = 0; i < 5;  i++) {
    //        printf("%d  ",array1[i]);
    //    }
    //                       循环赋值,随机数  30 -42之间
    //    int array[10],temp;
    //    for (int i = 0 ; i < 10 ; i ++) {
    //        array[i] = arc4random() % ( 42 - 30 + 1) + 30;
    //    }
    //    for (int i = 0; i < 10;  i ++) {
    //        printf("%d\t",array[i]);
    //    }
    //    printf("\n");
    //    for (int j = 0 ; j < 9; j ++) {
    //        for (int i = 0 ; i < 9 - j; i++) {
    //            if (array[i] > array[i + 1]) {
    //                temp = array[i];
    //                array[i] = array[i+1];
    //                array[i+1] = temp;
    //
    //            }
    //        }
    //    }
    //    for (int i = 0; i < 10;  i ++) {
    //        printf("%d\t",array[i]);
    //    }
    //    printf("\n");
    //   int array[4] = {1,2,3,4,5}; 数组越界,下标超出的自己的范围,月截止后就反问了不属于自己的空间.
    //   而 且,编译器不会检测数组越界.
    //    注意!:数组作为一个整体式不能参与运算的,参与运算的都是其中的元素
    //    定义一个数组,具有 20个整形元素,每个元素的取值范围是 2 - 13之间
    //    int a[20],sum = 0;
    //    
    //    for (int i = 0;  i < 20; i ++) {
    //        a[i] = arc4random()  % (13 - 2 + 1) + 2;
    //        sum += a[i];
    //    }
    //    for (int i = 0;  i < 20;  i ++) {
    //        printf("%d  ",a[i]);
    //    }
    //    printf("\n%d\n",sum);
#pragma mark    复制一个数组,要有两个数组,把其中一个的值 赋给另一个
//    int a[10],b[10];
//       for (int i = 0;  i < 10; i ++) {
//         a[i] = arc4random()  % (13 - 2 + 1) + 2;
//       }
//     for (int i = 0;  i < 10;  i ++) {
//         printf("%d  ",a[i]);
//      }
//    printf("\n");
//    for (int i = 0; i < 10; i ++) {
//        b[i] = a[i];
//    }
//     for (int i = 0;  i < 10;  i ++) {
//           printf("%d  ",b[i]);
//        }
//    printf("\n");
    
#pragma mark    生成2 个数组,都是10个元素,范围是 20 - 30.数组对应的元素相加,存放到第3个数组中
    
    int a[10],b[10],c[10];
    for (int i = 0; i < 10 ; i ++) {
        a[i] = arc4random() % (30 - 20 + 1) + 20;
    }
    for (int i = 0; i < 10; i ++) {
        printf("%d\t",a[i]);
    }printf("\n");
    for (int i = 0; i < 10 ; i ++) {
        b[i] = arc4random() % (30 - 20 + 1) + 20;
    }
    for (int i = 0; i < 10; i ++) {
        printf("%d\t",b[i]);
    }printf("\n");
    for (int i = 0; i < 10; i ++) {
        c[i] = a[i] + b[i];
    }
    for (int i = 0; i < 10; i ++) {
        printf("%d\t",c[i]);
    }
    
    
    
    return 0;
}
