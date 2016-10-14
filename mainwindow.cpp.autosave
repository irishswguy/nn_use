#include "mainwindow.h"
#include "ui_mainwindow.h"
#include "floatfann.h"
#include <QDebug>


MainWindow::MainWindow(QWidget *parent) :
    QMainWindow(parent),
    ui(new Ui::MainWindow)
{
    ui->setupUi(this);
}

MainWindow::~MainWindow()
{
    delete ui;
}



int USE_NN()
{
    fann_type *calc_out;
    fann_type input[2];

    struct fann *ann = fann_create_from_file("/home/louis/Projects/qt5/nn/xor_float.net");

    input[0] = -1;
    input[1] = 1;
    calc_out = fann_run(ann, input);

    qDebug() << "xor test (" << input[0] << "," << input[1] << ") -> " <<calc_out[0];

    fann_destroy(ann);
    return 0;
}
void MainWindow::on_pushButton_clicked()
{
    USE_NN();
}
