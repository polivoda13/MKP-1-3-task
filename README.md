# MKP-1-3-task
Task3 in MKP1
class Element {
int data;
Element previous;

Element(int x) {
    data = x;
}
}

class Stack {
Element last;

void push(int x) {
    Element newElement = new Element(x);
    if (last == null) {
        last = newElement;
    } else {
        newElement.previous = last;
        last = newElement;
    }
}

int pop() {
    if (last == null) {
        throw new IllegalStateException("Stack is empty");
    }
    
    int poppedData = last.data;
    last = last.previous;
    
    return poppedData;
}
}
