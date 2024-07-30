public class Cliente {
private String nome;
private String cpf;
public Cliente (String nome, String cpf){
this.nome=nome;
this.cpf= cpf;
}
public String getNome(){
return nome;
}
public void setNome(String nome){
this.nome = nome;
}
public String getCpf(){
return cpf;
}
public setCpf(String cpf){
this.cpf = cpf;
}
}
public class Conta{
private Cliente cliente;
private double saldo;
public Conta(Cliente cliente){
this.cliente = cliente;
this.saldo = 0.0;
}
public Cliente getCliente(){
return cliente;
}
public double getSaldo(){
return saldo;
}
public void depositar(double valor){
if(valor > 0){
saldo += valor;
}
}
public void sacar(double sacar){
if(valor > 0 && saldo >= valor){
saldo -= valor;
}
}
}
import java.util.ArrayList;
import java.util.List;
public class Banco {
private String nome;
private List<Conta> contas;
public Banco(String nome){
this.nome = nome;
this.contas = new ArrayList<>();
}
public void adicionarConta(Conta conta){
contas.add(conta);
}
public void listarClientes(){
for(Conta conta: contas){
Cliente cliente = conta.getCliente();
System.out.println("Cilente: " + cliente.getCliente() + ", CPF: " + cliente.getCpf);
}
public static void main(String [] args){
Banco banco = new Banco("Banco Digital");


