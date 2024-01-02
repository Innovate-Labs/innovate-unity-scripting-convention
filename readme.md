# Innovate Labs Scripting Convention 

#### 0. Update keyboard mapping scheme

* Go to Tools or press Ctrl + comma(,).
* Go to Environment > Keyboard.
* From the given keyboard mapping scheme, set it to 'Visual Studio Code'.

#### 1. Comments

* Instead of using block-style comments (/* ... */), linear comments (//...).

* Use Ctrl + slash(/) shortcut to apply it on the selected lines.

Example:
```
public void Start()
{
    ❌❌❌
    /* var renderer = GetComponent<MeshRenderer>();
    var collider = GetComponent<MeshCollider>(); */

    ✅✅✅
    // var renderer = GetComponent<MeshRenderer>();
    // var collider = GetComponent<MeshCollider>();
}
```

#### 2. Indentation

* Use Allman style indentation.
* Usually Unity uses this to write clean code.

Example:
```
public void Start()
{
    ❌❌❌
    for(int i=0;i<10;i++)
           for(int j=0;j<i;j++) Console.WriteLine(i*j);
                

    ✅✅✅
    for(int i=0;i<10;i++)
    {
        for(int j=0;j<i;j++) 
        {
            Console.WriteLine(i*j);
        }
    }

}
```

#### 3. Naming Convention: 

* public member variables and properties - PascalCase

```
public int HealthPoints;
```

* private member variables - underscore (_) with camelCase

```
private int _healthPoints;
```

* private local variables - camelCase

```
void IncreaseHealthByOne()
{
    int currentHealth = _healthPoints;
    currentHealth += 1;
}
```


* method names - PascalCase

```
private void DestroyEnemy()
{
}

public void TakeDamage()
{
}
```

* method parameters - camelCase

```
private void DecreaseEnemyHealth(Enemy enemyObject, int decreasePoint)
{
    enemyObject.health -= decreasePoint;
}
```

* Files, Structs, Classes, Enums etc. should be named using PascalCase.
