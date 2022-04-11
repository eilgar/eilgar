public class ContaCorrente{
 
 private int conta, agencia;
 private double saldo;
 private String nomeCliente;
 
 public ContaCorrente(int conta, int agencia, double saldo, String nome){
  this.conta = conta;
  this.agencia = agencia;
  this.saldo = saldo;
  this.nomeCliente = nome;
 }
 
 public int sacar(double valorSaque){
  if (saldo >= valorSaque){
    saldo -= valorSaque;
    return 1;
  }
  
  return 0;
  
 }
 
 public void depositar(double valorDeposito){
  saldo += valorDeposito;
  
 }
 
 public void imprimir(){
  System.out.println("Nome do Cliente: " + nomeCliente);
  System.out.println("Agência: " + agencia);
  System.out.println("Conta: " + conta);
  System.out.println("Saldo: " + saldo);
  
 }
}
