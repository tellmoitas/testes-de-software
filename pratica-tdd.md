

# Prática TDD

Regras do Jogo: Qualquer número divisível por três é substituído pela palavra fizz e
qualquer número divisível por 5 pela palavra buzz. Números divisíveis por ambos são
substituídos por fizzbuzz. Um jogador que comete um erro tem que beber uma xícara de
café. 

```java
public class FizzBuzz implements IFizzBuzz
{
 public string Answer(int i)
 {
 throw new NotImplementedException();
 }
}
public interface IFizzBuzz
{
 /// <summary>
 /// Implemente o Jogo usando a técnica TDD
 /// </summary>
 /// <param name="number">um número da sequência do jogo</param>
 /// <returns>resposta apropriada para o corrente número</returns>
 public String Answer(int number);
}
