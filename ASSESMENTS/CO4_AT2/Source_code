#include <stdio.h>

int main()
{
    int n, m;
    int graph[20][20];
    int score[20];
    int i, j, k, temp;

    printf("Enter number of students: ");
    scanf("%d", &n);

    printf("Enter number of contents: ");
    scanf("%d", &m);

    printf("Enter the student-content matrix:\n");

    for (i = 0; i < n; i++)
    {
        for (j = 0; j < m; j++)
        {
            scanf("%d", &graph[i][j]);
        }
    }

    /* Calculate ranking score */
    for (j = 0; j < m; j++)
    {
        score[j] = 0;

        for (i = 0; i < n; i++)
        {
            score[j] += graph[i][j];
        }
    }

    /* Sort contents by score in descending order */
    for (i = 0; i < m - 1; i++)
    {
        for (j = i + 1; j < m; j++)
        {
            if (score[i] < score[j])
            {
                temp = score[i];
                score[i] = score[j];
                score[j] = temp;
            }
        }
    }

    printf("\nRecommended Content Ranking:\n");

    for (k = 0; k < m; k++)
    {
        printf("Rank %d : Score = %d\n", k + 1, score[k]);
    }

    return 0;
}
