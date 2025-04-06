def func_decorator(func):
    def wrapper(x,*args, **kwargs):
        
        res = 5
        for i in range(len(x)):
            res+=x[i]
        return res
 
    return wrapper

@func_decorator
def func_sum(x):
    return x

n=list(map(int,input().split()))
print(func_sum(n))
