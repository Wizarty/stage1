class IntBuilder {
  
  constructor(n) {
    this.value=n;
    }
  
  plus(...args) {
    this.value += args.reduce((plus, current) => plus + current);
    return this;
}

  minus(...args) {
    this.value = this.value - args.reduce((minus, current) => minus + current );
    return this;
  }
  
  multiply(n){
    this.value = this.value * n
    return this;
  }
  divide(n){
     this.value = (this.value / n)
     //this.value = Math.floor(this.value / n)
     return this;
  }
   mod(n){
     this.value = (this.value % n)
     return this;
  }
   get() {
    return this.value;
  }

}


a = new IntBuilder(10)

console.log(a.plus(2,3,2).minus(1,2).multiply(2).divide(4).mod(3).get())
