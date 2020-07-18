//Faça um programa em Java que leia o nome de um vendedor, o seu salário fixo e o total de vendas efetuadas por ele no mês (em dinheiro). Sabendo que este vendedor ganha 15% de comissão sobre suas vendas efetuadas, informar o total a receber no final do mês.

//DIEGO LINS

package apartamento;

import javax.swing.JOptionPane;

public class Controle {

	public static void main(String[] args) {

		int ligada = JOptionPane.showConfirmDialog(null,"Deseja ligar a luz?", " ",JOptionPane.YES_NO_OPTION);
		 if(JOptionPane.YES_OPTION == ligada){

			Luz luz = new Luz(true);
			JOptionPane.showMessageDialog(null,"Luz: " + luz.isLigado());       //Diego Lins
		}
		String ligadoAr = JOptionPane.showInputDialog("Deseja ligar o Arcondicionado?(sim/não)?");
		if (ligadoAr.equalsIgnoreCase("Sim")) {

			ArCondicionado ar = new ArCondicionado();
			String tempeAr = JOptionPane.showInputDialog("Digite a Temperatura:");
			int intTemp = Integer.parseInt(tempeAr);
			ar.setTemperatura(intTemp);

			JOptionPane.showMessageDialog(null, "A Temperatura é: " + intTemp);
			String aumentarAr = JOptionPane.showInputDialog("Deseja aumentar ou diminuir a temperatura?(+/-)? sair(s)");
			while((aumentarAr.equalsIgnoreCase("s") == false)) {
				    if(aumentarAr.equalsIgnoreCase("+")) {
					ar.setAumentarTempe();
					JOptionPane.showMessageDialog(null, "A Temperatura : " + ar.getTemperatura());
					aumentarAr = JOptionPane.showInputDialog("Deseja aumentar ou diminuir a temperatura?(+/-)? sair(s)");
				}
				    else if(aumentarAr.equalsIgnoreCase("-")) {
					ar.setDiminuirVoTempe();
					JOptionPane.showMessageDialog(null, "A Temperatura : " + ar.getTemperatura());
					aumentarAr = JOptionPane.showInputDialog("Deseja aumentar a temperatura?(sim/não)? sair(s)");
				}
				    else {
				    	JOptionPane.showMessageDialog(null, "A Temperatura : " + ar.getTemperatura());
				    }
			}

		}
		String somLigado = JOptionPane.showInputDialog("Deseja ligar o Som?(sim/não)?");
		if (somLigado.equalsIgnoreCase("Sim")) {

			Som som = new Som();
			String somVol = JOptionPane.showInputDialog("Digite o volume: ");
			int intSom = Integer.parseInt(somVol);
			som.setVolume(intSom);
			
			JOptionPane.showMessageDialog(null, "O volume é: " + intSom);
			String aumentarSom = JOptionPane.showInputDialog("Deseja aumentar ou diminuir o som?(+/-)? sair(s)");
			while(aumentarSom.equalsIgnoreCase("s") == false) {
				JOptionPane.showMessageDialog(null, "o Volume : " + som.getVolume());
				
				if(aumentarSom.equalsIgnoreCase("+")) {
					som.setAumentarVolume();
					JOptionPane.showMessageDialog(null, "o Volume : " + som.getVolume());
					aumentarSom = JOptionPane.showInputDialog("Deseja aumentar ou diminuir o som?(+/-)? sair(s)");
				}else if(aumentarSom.equalsIgnoreCase("-")) {
					som.setDiminuirVolume();
					JOptionPane.showMessageDialog(null, "O volume : " + som.getVolume());
					aumentarSom = JOptionPane.showInputDialog("Deseja aumentar ou diminuir o som?(sim/não)? sair(s)");
				}else {
					JOptionPane.showMessageDialog(null, "O volume : " + som.getVolume());
				}
			} 
			

		}
	}
}


public class ArCondicionado {

	private boolean arLigado = false;
	private int temperatura;
	public boolean isArLigado() {
		return arLigado;
	}
	public void setArLigado(boolean arLigado) {
		this.arLigado = arLigado;
	}
	public int getTemperatura() {
		return temperatura;
	}
	public void setTemperatura(int temperatura) {
		this.temperatura = temperatura;
	}
	
	public void setAumentarTempe(){
        this.temperatura += 1;
    }

    public void setDiminuirVoTempe(){
        this.temperatura -= 1;
    }
	
}

package apartamento;

public class Luz {


	private boolean ligado = false;

	public Luz(boolean ligado) {
		this.ligado = ligado;
	}

	public boolean isLigado() {
		return ligado;
	}

	public void setLigado(boolean ligado) {
		this.ligado = ligado;
	}
}

package apartamento;

public class Som {

	private int volume;
	private boolean somLigado = false;
	
	
	public int getVolume() {
		return volume;
	}
	public void setVolume(int volume) {
		this.volume = volume;
	}
	public boolean isSomLigado() {
		return somLigado;
	}
	public void setSomLigado(boolean somLigado) {
		this.somLigado = somLigado;
	}
    
    public void setAumentarVolume(){
        this.volume += 1;
    }

    public void setDiminuirVolume(){
        this.volume -= 1;
    }
	
	
	}
	
	



