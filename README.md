#include <iostream>
#include <cmath>
#include <iomanip>
using namespace std;

void sphere();
void cuboid();
void pyramid();
void cylinder();

int main() {
    int choice;

    cout << "==============================\n";
    cout << "  AREA AND VOLUME CALCULATOR  \n";
    cout << "==============================\n";
    cout << "1. Sphere\n";
    cout << "2. Cuboid\n";
    cout << "3. Pyramid\n";
    cout << "4. Cylinder\n";
    cout << "Enter your choice (1-4): ";
    cin >> choice;
    cout << endl;

    switch (choice) {
        case 1: sphere(); break;
        case 2: cuboid(); break;
        case 3: pyramid(); break;
        case 4: cylinder(); break;
        default: cout << "Invalid choice!" << endl;
    }

    return 0;
}

void sphere() {
    double r;
    cout << "Enter radius of sphere: ";
    cin >> r;

    double area = 4 * M_PI * r * r;
    double volume = (4.0 / 3.0) * M_PI * pow(r, 3);

    cout << fixed << setprecision(2);
    cout << "\nSurface Area of Sphere: " << area << endl;
    cout << "Volume of Sphere: " << volume << endl;
}

void cuboid() {
    double l, w, h;
    cout << "Enter length, width, height of cuboid: ";
    cin >> l >> w >> h;

    double area = 2 * (l*w + w*h + l*h);
    double volume = l * w * h;

    cout << fixed << setprecision(2);
    cout << "\nSurface Area of Cuboid: " << area << endl;
    cout << "Volume of Cuboid: " << volume << endl;
}

void pyramid() {
    double base, height;
    cout << "Enter base length and height of pyramid: ";
    cin >> base >> height;

    double slantHeight = sqrt(pow((base / 2), 2) + pow(height, 2));
    double area = base * base + 2 * base * slantHeight;
    double volume = (base * base * height) / 3;

    cout << fixed << setprecision(2);
    cout << "\nSurface Area of Pyramid: " << area << endl;
    cout << "Volume of Pyramid: " << volume << endl;
}
