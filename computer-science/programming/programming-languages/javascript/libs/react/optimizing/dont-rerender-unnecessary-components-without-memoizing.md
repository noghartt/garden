# Do't rerender unnecessary components without memoizing
Toda vez que o React cria um novo elemento (por consequência da atualização de um estado interno, por exemplo), também recria seu respectivo objeto `props`. Como podemos garantir que o componente permanece o mesmo, isto é, não houve alterações? Reutilizando o elemento que já fora criado uma vez, assim, garantindo que tudo se mantém idêntico.

Como fazer isso? Conforme o próprio exemplo do post diz: podemos elevar o componente garantindo que ele esteja num "wrapper", assim tornando os componentes `children` (um exemplo) consistente entre os *rerenders*.

## References 
- [One simple trick to optimize React re-renders](https://kentcdodds.com/blog/optimize-react-re-renders)