class StringBuilder {
  
  constructor(n) {
    this.value=n;
    }
  
  plus(...args) {
    this.value += args.reduce((plus, current) => plus + current);
    return this;
}

  minus(n) {
    this.value = this.value.substring(0, this.value.length - n);
    return this;
  }
  
  multiply(n){
     this.value = this.value.repeat(n)
     return this;
  }
  divide(n){
     this.value = this.value.substring(0,Math.floor(this.value.length / n))
     return this;
  }
  remove(str){
    this.value = this.value.replace(str,'')
    return this;
  }
  sub(from,n){
     this.value = this.value.slice(from,n)
     return this;
  }
 
   get() {
    return this.value;
  }

}


a = new StringBuilder('Hello')

console.log(a.plus(' all', '!').minus(4).multiply(3).divide(4).remove('l').sub(1,1).get())


