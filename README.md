Table::Table(int width, int height, int val = 0){
    std::vector<std::vector<int>> cols(width);
    std::vector<int> rows(height);
    for (int i = 0; i < width; i++){
        for (int q = 0; q < rows; q++){
            rows.at(q) == val;
        }
        cols.at(i) = rows;
        rows.clear();
        rows.resize(height);
    }
}
