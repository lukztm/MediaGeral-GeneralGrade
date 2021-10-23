# Media Geral
 Recebe quantas notas o usuario quiser inserir e mostra a media total.

    import javax.swing.JOptionPane;

    public class DesafioWhile {

	public static void main(String[] args) {

		String aluno = JOptionPane.showInputDialog("Digite o nome do Aluno:");
		aluno = aluno.toUpperCase();

		String entrada = "";
		Double nota = (double) 0;
		int qntnotas = 0;
		Double media = nota;

		while (nota != -1) {
			entrada = JOptionPane.showInputDialog("Insira a nota do aluno (P/ TERMINAR DIGITE -1):");
			entrada = entrada.replace(',', '.');
			nota = Double.parseDouble(entrada);

			if (nota >= 0 && nota <= 10) {
				System.out.printf("%S %.2f %S", "Nota do aluno é:", nota, ".\n");
				media += nota; // media = media + nota;
				qntnotas++;
			} else if (nota != -1) {
				System.out.println("DIGITE UMA NOTA VÁLIDA!");
			}

		}
		media = media / qntnotas;
		System.out.printf("%S %S %S %.2f %S", "A media do aluno", aluno, "é:", media, ".");

		if (media >= 7) {
			System.out.println("\nAPROVADO.");
		} else {
			System.out.println("\nREPROVADO.");
		}
	}
    }

!!!ENGLISH!!!

# General Grade

Gets every grade that the user wants to type and shows the general grade.

    import javax.swing.JOptionPane;

    public class GeneralGrade {

	   public static void main(String[] args) {

		String aluno = JOptionPane.showInputDialog("Type student's name:");
		student = student.toUpperCase();

		String in = "";
		Double grade = (double) 0;
		int qtygrade = 0;
		Double average = grade;

		while (grade != -1) {
			in = JOptionPane.showInputDialog("Type the student's grade (TO EXIT TYPE -1):");
			in = in.replace(',', '.');
			grade = Double.parseDouble(in);

			if (grade >= 0 && grade <= 10) {
				System.out.printf("%S %.2f %S", "Student's grade:", grade, ".\n");
				average += grade; // average = average + grade;
				qtygrade++;
			} else if (grade != -1) {
				System.out.println("TYPE A VALID GRADE!");
			}

		}
		average = average / qtygrade;
		System.out.printf("%S %S %S %.2f %S", "The student's average grade", student, "is:", average, ".");

		if (average >= 7) {
			System.out.println("\nWell Done.");
		} else {
			System.out.println("\nStudy Harder.");
		}
	}
    }
