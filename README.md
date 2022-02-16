# 413.-Web-Service-Retornando-Objeto
Exibe informacoes de outra classe, Objeto Cliente
INICIO
______________________________________
package com.example.exerciciossb.controllers;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import com.example.exerciciossb.models.Cliente;

@RestController
@RequestMapping(path = "/clientes")
public class ClienteController {
	
	@GetMapping(path = "/clientes/qualquer")
	public Cliente obterCliente() {
		return new Cliente(28, "Pedro", "123.456.789-00");
	}
}
______________________________________
package com.example.exerciciossb.models;

public class Cliente {

	private int id;
	private String nome;
	private String cpf;
	
	public Cliente(int id, String nome, String cpf) {
		super();
		this.id = id;
		this.nome = nome;
		this.cpf = cpf;
	}
	public int getId() {
		return id;
	}
	public void setId(int id) {
		this.id = id;
	}
	public String getNome() {
		return nome;
	}
	public void setNome(String nome) {
		this.nome = nome;
	}
	public String getCpf() {
		return cpf;
	}
	public void setCpf(String cpf) {
		this.cpf = cpf;
	}
}

__________________________________________
![image](https://user-images.githubusercontent.com/95525963/154373273-d5455eaa-b01a-4018-8ec6-bd1f7c4b5331.png)
