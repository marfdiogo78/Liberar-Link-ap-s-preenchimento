# Liberar-Link-ap-s-preenchimento
Liberar Link apos preenchimento

$(document).ready(function(){

    // #login botao submit
    $("#login").click(function(e){
	    // bloqueando envio do form
	    e.preventDefault();
	    var erros = 0;
	    // verifica se ha campos vazios
	    $("#formulario input").each(function(){
		    // conta erros
    		$(this).val() == "" ? erros++ : "";
	    });
	    if(erros > 0 ){	 
		    alert("Existe "+erros+" campo(os) vazio neste fomulário");
        }else{
	    	$("#formulario").submit()
	    }				
   	});
});
