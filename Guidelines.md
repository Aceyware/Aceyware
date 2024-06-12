# Aceyware Guidelines
Here you can find general information and guideines about 
-  Properties of projects
-  Code formatting and practises

## Properties of projects
- As of now, all of software are written on C or C++, no other languages are used and will not be allowed (fuck off with your rust).
- I usually code on Windows so it's generally the main target and build environment, though I try to make them cross platform as much as possible.
- Commits are done per new version only (so basically no mainline code going on, new code just gets pushed when it's completed.) but this behavior will change when people starts to contribute to projects.

### Naming of projects
All projects born with a codename if I cannot find a creative name, and often gets replaced with such creative names for retail use before release.
 I just use codenames for not wasting time on naming the project. Codenames are usually consists of feminine names.

 ## Code guidelines
 - Nobody uses 80 char terminals anymore. Write things on a single line instead chopping a single line to 5 different lines (unless they are really long).
 - Use Tabs for indention, NOT SPACES.
 - Function and variable names should use camelCases unless a reason to not do so exists.
 - Keep beginning braces ('\{') always on same line
 - Functions should be declared in ANSI format:
 `int main(int argc, char** argv) {...`
 - Variables should be named as what they do (unless they are used as counters, if so please describe what they are for in a comment.)

   `std::string requestPath; int flags = 0;` or `int pos = 0, b = 0; // pos is for iterator position, b is beginning offset of line.`
 - Conditions should be written as `[variable] [operator] [constant]`, not the other way around. Do

`if (pos == 0)` 

instead of 

`if (0 == pos)`
- Use indentation on switch-cases

```
switch (requestType) {
	case GET:
		doSomething();
		...
		break;
	case POST:
		doSomething();
		...
		break;
	...
	default:
		doSomething();
		...
		break;
}
```

If cases consists of few code, keep them on same lines.
```
	case 304: buf[pos] = 128 | 11; pos++; break;
	case 400: buf[pos] = 128 | 12; pos++; break;
	case 404: buf[pos] = 128 | 13; pos++; break;
	case 500: buf[pos] = 128 | 14; pos++; break;
```

- `goto` is mostly only used for getting out of branches. Don't use lots of `goto`s on code.
- Profanity is allowed but don't use it up to the point of getting repos banned.
- Add comments to beginning of functions for briefly telling what they do. Also describe what it does on complicated code. Add comments to lines for telling what they do.
  
That's all for now.