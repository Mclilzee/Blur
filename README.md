    for (int i = 0; i < height; i++)
    {
        for (int j = 0; j < width; j++)
        {
            int r = image[i][j].rgbtRed;
            int g = image[i][j].rgbtGreen;
            int b = image[i][j].rgbtBlue;
            
            if (j - 1 >= 0)
            {
                r += image[i][j - 1].rgbtRed;
                g += image[i][j - 1].rgbtGreen;
                b += image[i][j - 1].rgbtBlue;
                
            }
            if (j + 1 < width)
            {
                r += image[i][j + 1].rgbtRed;
                g += image[i][j + 1].rgbtGreen;
                b += image[i][j + 1].rgbtBlue;
            }
            if (i - 1 >= 0)
            {
                r += image[i - 1][j].rgbtRed;
                g += image[i - 1][j].rgbtGreen;
                b += image[i- 1][j].rgbtBlue;
                if (j - 1 >= 0)
                {
                    r += image[i - 1][j - 1].rgbtRed;
                    g += image[i - 1][j - 1].rgbtGreen;
                    b += image[i- 1][j - 1].rgbtBlue;
                    
                }
                if (j + 1 < width)
                {
                    r += image[i - 1][j + 1].rgbtRed;
                    g += image[i - 1][j + 1].rgbtGreen;
                    b += image[i- 1][j + 1].rgbtBlue;
                    
                }
                
            }
            if (i + 1 < height)
            {
                r += image[i + 1][j].rgbtRed;
                g += image[i + 1][j].rgbtGreen;
                b += image[i + 1][j].rgbtBlue;
                if (j - 1 >= 0)
                {
                    r += image[i + 1][j - 1].rgbtRed;
                    g += image[i + 1][j - 1].rgbtGreen;
                    b += image[i + 1][j - 1].rgbtBlue;
                }
                if (j + 1 < width)
                {
                    r += image[i + 1][j + 1].rgbtRed;
                    g += image[i + 1][j + 1].rgbtGreen;
                    b += image[i + 1][j + 1].rgbtBlue;
                    
                }
                    image[i][j].rgbtRed = r;
                    image[i][j].rgbtGreen = g;
                    image[i][j].rgbtBlue = b;
            }
        }
    }
