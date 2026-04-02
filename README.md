# Learn Vim

## Getting Started
- Vim is an open-source, improved text editor for Vi.
- The classic Unix text editor.
- Development of Vim started in 1988
- First release in 1992.

![vim-meme](./docs/images/vim_meme.jpg)

## Prequisites
- Touch typing
- IDE: vim plugin

## Pros
- Code editing faster
- Navigation without mouse
- Customization
- Light Weight, Performant

## Cons
- Courbe d'apprentissage
- Hard to configure
- Can not cover all Modern IDE feature

Question: Is it worth learning Vim ?


# Modes
- Normal: Escape (defaut)
- Insert: i/a
- Visual
- Select
- Command line
- Replace
- Operator-pending

## Normal mode (default)
### Text example for practice:
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi id rutrum nisl. Nam mattis, elit vitae congue aliquet, odio ex suscipit dui, id mollis diam odio eget lacus. Integer ultricies sapien nec ante egestas, non eleifend mauris suscipit. Donec imperdiet nulla enim, id ultrices neque consectetur porta. Donec cursus sollicitudin risus a porta. Phasellus neque ipsum, condimentum id massa a, efficitur bibendum ligula. Fusce pellentesque, ante nec fringilla tincidunt, ligula mi faucibus eros, non facilisis ipsum dolor id elit. Duis vestibulum odio sed justo maximus vehicula. In eu pulvinar enim. In consequat odio quis tortor tincidunt porta.
Aliquam in porta turpis, sed blandit orci. Mauris quis nisi tempor, convallis lacus quis, luctus diam. Nulla nibh erat, interdum id risus id, pharetra feugiat dolor. Morbi vestibulum odio sed tortor ultricies, vel molestie nisi pretium. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Vestibulum quis sapien at enim congue egestas in sit amet sapien. Nunc at eros sapien.
Suspendisse dignissim est ut arcu placerat euismod. Vestibulum in nulla tellus. Aenean elementum non enim a ultrices. In hac habitasse platea dictumst. Ut eu libero orci. Etiam ac dui id quam bibendum dictum et id erat. Nunc arcu nisl, finibus a accumsan tincidunt, mollis et nulla. Sed ut ipsum id mi luctus laoreet tristique vel ante. In id libero vehicula nisl pellentesque condimentum nec et mi. Ut id fringilla justo. Phasellus tempor, nisl id malesuada congue, turpis urna scelerisque ligula, convallis rutrum metus dolor ac erat. Nunc convallis risus ex, sit amet dapibus risus maximus a. Proin pulvinar a erat vitae facilisis.
Morbi sit amet luctus turpis. In vitae blandit tortor. Phasellus justo tellus, viverra porta hendrerit lacinia, interdum vel purus. Nam viverra mi odio. Aliquam eget ex tempor, vehicula nunc sit amet, rhoncus lorem. Phasellus auctor ex sodales fringilla fringilla. Phasellus ac ex id ipsum iaculis hendrerit et ac risus. Mauris mattis tempus ante vulputate mattis. Curabitur ut imperdiet est, nec dignissim nisl. Donec lorem nunc, fermentum ac nisi sed, vulputate fermentum lectus.
Proin nec tortor vitae lorem tempus pellentesque. Curabitur consequat, turpis sed tempus lobortis, nibh ipsum finibus magna, at dictum sapien nisl vitae ipsum. Nam vel tortor metus. Aenean iaculis tortor sit amet arcu tempus pulvinar. Aliquam faucibus dignissim scelerisque. Aenean luctus ipsum at felis lobortis, accumsan porta justo dignissim. Cras viverra dapibus est vitae mollis. Aliquam a eleifend nisi. Maecenas est magna, aliquet vel justo non, fermentum dapibus est. Duis eu vestibulum felis, hendrerit lobortis turpis. Maecenas tincidunt ultricies augue id vulputate. Quisque sed ex vel dolor faucibus finibus a eget enim. Cras in leo aliquam, fermentum libero non, molestie libero. Etiam at scelerisque enim. Proin faucibus scelerisque lectus, a dignissim felis consectetur iaculis.


### Basics:
- Navigation: hjkl
- Normal mode: escape
- Insert mode: i/a, I/A
    - new line insert: o/O
- Undo: u
- Redo: <C-r>
- Replace: r
- Delete a line: dd
- Copy a line: yy -> paste: p (unnamed register "")


### Vim Motion
- Word: w/W, b/B, e/E, ge/gE
- 0, $
- Begin of first letter: ^
- Go to first line: gg
- Go to last line: G
- Go to a line: <line>G
- Move to the next occurrence of <char> on the line: f<char>
    - navigate to next: ;/,
- search a pattern: /<pattern>
    - navigate to next/prev: n/N

- jump matching: %
```java
public class HelloWorld {
    public static void main(String [] args) {
        System.out.println("Hello WOrld!");
    }
}
```

### Vim Action
Action = <Count> + Motion + Operator

### Vim Operator
- Delete: d
- Yank (copy): y
- Change: c
- Upper case: gU
- Lower case: gu

### Vim text object
Operate on blocks

Example:
- delete around word: daw/daW
- change inside parenthesis: ci(
- change inside double quotes: ci"
- visual select around paragraph: vap

- operate on html tag: it/at
```html
    <div>oneeee</div>
    <div>two</div>
    <div>threeee</div>
    <div>four not working<\div>
```

## Insert Mode
- Insert text
- delete a word: <C-w>
- delete a line: <C-u>
- delete a character: <C-h>
- paste yank: <C-r>0
- addition / substraction: <C-r>=<operation>
- character decimal code: <C-v>{123}
    - hexadecimal: <C-v>u{123}


## Visual Mode
Allows you to highlight a specific range of text and then apply a command

### 3 Types:
- Character visual select: v
- Line visual select: V
- Blocks visual select: <C-v>

#### Practice Visual:
##### Make it pretty
Chapter        Page
Normal mode     15
Insert mode     31
Visual mode     44

##### Comment all lines
```python
def main():
    print("hello")
    print("world")
    print("Christian")

if __name__ == "__main__":
    main()
```

##### Add missing ; at en of java program
```java
public class Main {
    public static void main(String args[]) {
        System.out.println("Hello")
        System.out.println("World")
        System.out.println("Christian")
    }
}
```


## Command Line Mode
