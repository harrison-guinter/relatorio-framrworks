Os frameworks funcionam como um modelo para a criação de softwares e aplicativos. Eles oferecem uma série de estruturas básicas que facilitam o trabalho do programador. Por oferecerem uma estrutura base para agilizar o desenvolvimento, os frameworks dão a vantagem de não começar o desenvolvimento completamente do zero.

<?php
 
namespace App\Mail;
 
use App\Models\Order;
use Illuminate\Bus\Queueable;
use Illuminate\Mail\Mailable;
use Illuminate\Queue\SerializesModels;
 
class OrderShipped extends Mailable
{
    use Queueable, SerializesModels;
     public $order;
     public function __construct(Order $order)
    {
        $this->order = $order;
    }
     public function build()
    {
        return $this->view('emails.orders.shipped');
    }
}


Os frameworks funcionam como um modelo para a criação de softwares e aplicativos. Eles oferecem uma série de estruturas básicas que facilitam o trabalho do programador. Por oferecerem uma estrutura base para agilizar o desenvolvimento, os frameworks dão a vantagem de não começar o desenvolvimento completamente do zero.


https://carbon.now.sh/





·         Angular
Framework frontend desenvolvido pela Google, lançado inicialmente em 2010 sob o nome de AngularJS, apenas com suporte para JavaScript e seus bibliotecas, sofreu inúmeras atualizações e mudanças, especialmente na versão conhecida como Angular 2, atualmente, encontra-se na versão 15 e na quarta posição de framework frontend mais amado segundo a pesquisa anual de 2021 realizada pelo GitHub. Angular é um framework robusto, multiparadigmal e muito popular por possuir suporte e compatibilidade com TypeScript, um superconjunto de JavaScript para introduzir tipagem forte e outras funcionalidades à linguagem. Sua diferencial principal é a componentização de sistemas com “blocos” de HTML, CSS e JS/TS reutilizáveis, desta forma, diminuindo a quantidade total de código e facilitando a manutenção.
·         Java Spring
O Spring é um framework  com foco em desenvolvimento backend baseado em microserviços disponibilizado em 2002, atualmente na versão 5.3.19, Java utilizado para receber requisições HTTP, trata-las, processa-las e responder para o frontend, funcionando como uma API, possui compatibilidade com inúmeras ferramentas que facilitam o processo de desenvolvimento, como JPA e Hibernate para persistência de objetos e integração com o banco de dados, pode ser criado como um projeto Maven e possui ferramentas para fácil criação de projetos no site start.spring.io. Atualmente, encontra-se na versão 15 e na quarta posição de fra
mework backend mais amado segundo a pesquisa anual de 2021 realizada pelo GitHub, ainda possui grande demanda no mercado especialmente de projetos robustos que precisam de grande mão de obra para manutenção.
·         NodeJS
		Node é um framework de código aberto extremamente popular por permitir a utilização de JavaScript no backend, por meio do interpretador V8 do Google e utilizado para comunicação com banco de dados, geração de arquivos com o auxílio de outras bibliotecas JS. Node foi lançado inicialmente em 2009 e faz parte do gerenciador de pacotes NPM, atualmente representa uma boa fração do mercado de desenvolvimento web, especialmente por permitir uma stack de JS no backend, desta forma, o mesmo profissional pode atuar como fullstack. Além de ser extremamente rápido, otimizado e de fácil aprendizado
·         Flask
		Flask é um framework da linguagem Python, considerado um microframework por possuir uma estrutura consideravelmente simples, mas de fácil expansão. Disponibilizado pela primeira vez em 2010, sofrendo constantes atualizações desde então. Flask é baseado nos seguintes projetos: Pocoo, Werkzeug e Jinja2. Werkzeug é uma biblioteca de utiltários em Python, por outro lado Jinja2 é um padrão de templates para o Flask, facilitando assim, a utilização de HTML dentro dos projetos com Python.







Spring

@SpringBootApplication
@RestController
public class FirstApplication {
	@GetMapping("/helloworld")
	public String hello() {
		return "Hello World!";
	}
}

O código acima cria um endpoint que recebe requisições com a URL base do projeto + "/helloworld".
Executando o projeto localmente na porta padrão e realizando uma requisição para "localhost:8080/helloworld" resultará em uma string contendo "Hello World!" como resposta.




























Angular

import { FormGroup, FormControl, Validator, Validators, FormBuilder } from "@angular/forms";

@Component({
  selector: 'app-form-login',
  templateUrl: './form-login.component.html',
  styleUrls: ['./form-login.component.css']
})

export class FormularioLoginComponent {
	public formulario: FormGroup

	constructor(formBuilder: FormBuilder) {
		formBuilder.group({
			email: ['', Validators.required]
			senha: ['', Validators.required]
			senhaConfirmacao: ['', Validators.required]
		})				
	}
}

O código acima representa a criação do arquivo TypeScript de um componente de login, sendo criado um formulário no momento que o componente é construído.



















Flask

from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Olá mundo!"

if __name__ == "__main__":
    app.run()

O código acima representa uma aplicação que apenas imprime o texto “Olá mundo !” na tela.






























NodeJS

// include file system module
var fs = require('fs');
 
// read file nomedoarquivo.txt
fs.readFile('nomedoarquivo.txt',
    // callback function that is called when reading file is done
    function(err, data) {   	
        if (err) throw err;
        // data is a buffer containing file content
        console.log(data.toString('utf8'))
});


O trecho de código acima lê o conteúdo de um arquivo e imprime seu conteúdo na tela.
