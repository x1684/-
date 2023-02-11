#include <iostream>
#include <string>
#include <cmath>

using namespace std;

// 定义烟花类
class Firework {
public:
  Firework(int x, int y, int size, int speed, int color);
  void show();
  void move();

private:
  int x;
  int y;
  int size;
  int speed;
  int color;
  int shape;
};

// 定义构造函数
Firework::Firework(int x, int y, int size, int speed, int color, int shape) {
  this->x = x;
  this->y = y;
  this->size = size;
  this->speed = speed;
  this->color = color;
  this->shape = shape;
}

// 定义显示函数
void Firework::show() {
  cout << "烟花位置：(" << this->x << ", " << this->y << ")" << endl;
  cout << "烟花大小：" << this->size << endl;
  cout << "烟花速度：" << this->speed << endl;
  cout << "烟花颜色：" << this->color << endl;
  cout << "烟花形状：" << this->shape << endl;
}

// 定义移动函数
void Firework::move() {
  this->x += this->speed * cos(this->x);
  this->y += this->speed * sin(this->y);
}

int main() {
  Firework firework(10, 10, 5, 10, 0xff0000, "笨柯");
  firework.show();
  firework.move();
  firework.show();
  return 0;
}<|im_end|><|im_end|><|im_end|>
