# WordleAPI
This Wordle API is made to return either a word or a list of words based on the parameters passed. This API was made because I couldn't find a API suited to my needs of my project. This API can only be accessed using Python. In case this API is used please attribute this website.

## Deployment
The API is deployed on pythonanywhere.com at [manvendra27.pythonanywhere.com](https://manvendra27.pythonanywhere.com).

## Usage
### Python

```python
import requests

response = requests.get('manvendra27.pythonanywhere.com/<parameters>')
```

"parameters" are the conditions according to the user, which consists of strings i.e. the string which are present, not present, perfectly present in the word.

## Parameters

The following functions are supposed to be appended at the end of manvendra.pythonanywhere.com while calling the API

### 1) When only good strings and perfect strings are present

### Syntax
/good&perfect/good_string/perfect_string

### Example
![image](https://user-images.githubusercontent.com/72267209/193898682-3919ecb4-d8f6-4997-855f-27e3c33df169.png)
```python
import requests

response = requests.get('manvendra27.pythonanywhere.com/good&perfect/cra/___sh')

#returns a random word satisfying the conditions in a JSON format i.e {word: 'crash'}
```

### 2) When only bad strings and perfect strings are present

### Syntax
/bad&perfect/bad_string/perfect_string

### Example
![image](https://user-images.githubusercontent.com/72267209/193901703-248b8c54-10ae-4983-817a-a8e90b91cdf0.png)
```python
import requests

response = requests.get('manvendra27.pythonanywhere.com/bad&perfect/c/mar_h')

#returns a random word satisfying the conditions in a JSON format i.e {word: 'marsh'}
```

### 3) When all good strings, bad strings and perfect strings are present

### Syntax
/all/good_string/bad_string/perfect_string

### Example
![image](https://user-images.githubusercontent.com/72267209/193902964-a674d08c-83ed-4564-97ed-2416d04eb976.png)
```python
import requests

response = requests.get('manvendra27.pythonanywhere.com/all/r/pe/_a___')

#returns a random word satisfying the conditions in a JSON format i.e {word: 'mayor'}
```

If you want a list of all the words possible for a certain condition add "/list" to the end of any of the above conditions. eg)
<ul>
<li>/good&perfect/good_string/perfect_string/list
<li>/bad&perfect/bad_string/perfect_string/list
<li>/all/good_string/bad_string/perfect_string/list
</ul>

This would return a list of all the words in a JSON format i.e. {words: [mayor, marsh, march......]}

## Scope for Improvement/Help Needed
<ul>
<li>I would like to simplify the code from having almost 4000-5000 lines of if-else statements.
<li>I would like the code to display the API swagger documentation on the home page.
<li>The code is currently deployed on pythonanywhere.com because I ran into some errors while trying to deploy it on heroku. I would like some help on this issue.
</ul>

<h4 align="center">Made with ❤ by <a href="https://github.com/Manv3ndra">Manvendra Prasad</a></h4>
