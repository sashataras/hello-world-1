#pragma once

#include <iostream>
#include <vector>
#include <random>

class Table {
 private:
  std::vector<std::vector<int>> t_;  // 2D vector of long
  int width_;                        // how wide is t_ (how many columns)
  int height_;                       // how high is t_ (how many rows)

public:

  void FillRandom(int low, int high, int seed = 0)
  {
    std::mt19937 generator(seed);
        std::uniform_int_distribution<int> distribution(low,high);

        /* generate ten numbers in [1,6] (always the same sequence!) */
        for (size_t i = 0; i < 10; ++i)
        {
            std::cout << distribution(generator) << ' ';
        }
        std::cout << std::endl;
  }

  Table(int width, int height, int val = 0)
  {
    std::vector<std::vector<int>> cols(width);
    std::vector<int> rows(height);
    for (int i = 0; i < width; i++)
      { for (int q = 0; q < height; q++)
            { rows.at(q) = val; }
        cols.at(i) = rows;
        rows.clear(); rows.resize(height); }
      }

  void PrintTable(std::ostream& cout) const
  {
    for (int i = 0; i < width_; i++)
  }

  bool SetValue(int x, int y, int val)
  {

    if
    //x = height
    //y = width of height vector
  }

  int GetValue(int x, int y) const
  {
    for ()
  }

};

