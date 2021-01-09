from django.shortcuts import render
from django.http import HttpResponse
import random

def home(request):
    return render(request,'generator/home.html')

def generator(request):
    key=''
    chars=list('abcdeghijklmnopqrstuvwxyz')
    length=int(request.GET.get('length',8))
    if request.GET.get('upper'):
        chars.extend(list('ABCDEFGHIJKLMNOPQRSTUVWXYZ'))
    if request.GET.get('digits'):
        chars.extend(list('0123456789'))
    if request.GET.get('special'):
        chars.extend(list('!@#$%^&*()'))

    for i in range(length):
        key+=random.choice(chars)

    return render(request,'generator/generate.html',{'key':key})

def about(request):
    return render(request,'generator/about.html')


