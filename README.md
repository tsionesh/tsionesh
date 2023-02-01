My first readme
 ans = k
        white = 0
        black=0
        for i in range(len(blocks)):
            if blocks[i] == "W":
                white += 1

            while i - black + 1 > k:
                if blocks[black] == "W":
                    white -= 1

                black += 1
            if i - black + 1 == k:
                ans = min(ans, white)
        
        return ans
        
