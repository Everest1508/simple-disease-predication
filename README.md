# Disease Prediction

Gives the probable diagnosis after entering the symptoms

## Model

The data set has 132 symptoms which lead to the cause of 41 diseases.

### RFC

```
clf_rf = RandomForestClassifier(random_state=43)
clr_rf = clf_rf.fit(x_train,y_train)
```

### Accuracy

The model has an accuracy of **97.62%**

## Flask

### POST method

```
    if request.method=='POST':
        col=x_test.columns
        inputt = [str(x) for x in request.form.values()]

        b=[0]*132
        for x in range(0,132):
            for y in inputt:
                if(col[x]==y):
                    b[x]=1

```

## HTML

### Jinja

```
{{pred}}
```
