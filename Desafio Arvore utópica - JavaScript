//As árvores utópicas  crescem de uma forma particular, em dois ciclos:

//cada primavera dobram seu tamanho
//cada verão crescem um metro
//Se Laura planta uma árvore utópica com um metro, no final do outono, qual seria sua altura depois de N ciclos?

//Alguns exemplos:

//si N = 0, sua altura será 1 metro (não cresceu nada)
//si N = 1, sua altura será de 2 metros (dobrou a altura na primavera)
//si N = 2, sua altura será de 3 metros (cresceu um metro mais no verão)
//si N = 3, sua altura será de 6 metros (dobrou a altura na primavera seguinte)
//E assim ...



function alturaArvoreUtopica(num){
  var altura = 1                                      //Diego Lins
  for(var i = 1; i<=num; i++){
     if(num == 0){
       altura = 1
     }
     else if(i%2 == 0){
       altura += 1;
     }else if(i%2 == 1){
       altura *= 2;
     }
  }
  return altura;
}
console.log(alturaArvoreUtopica(0))
