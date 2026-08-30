### Descripción de los Atributos

| **Atributo**                   	| **Descripción**                                                                 	|
|--------------------------------	|---------------------------------------------------------------------------------	|
| id_encuentro                   	| Identificador único de cada consulta o ingreso   hospitalario.                  	|
| id_paciente                    	| Identificador único del paciente.                                               	|
| raza                           	| Grupo étnico u origen del paciente.                                             	|
| genero                         	| Género del paciente.                                                            	|
| edad                           	| Rango de edad del paciente agrupado en intervalos de   10 años.                 	|
| peso                           	| Peso del paciente en libras.                                                    	|
| id_tipo_admision               	| Identificador numérico del tipo de admisión (ej. Urgencia, Electiva).         	|
| desc_tipo_admision             	| Descripción textual del tipo de admisión hospitalaria.                          	|
| id_origen_admision             	| Identificador numérico del origen o canal de ingreso del paciente.            	|
| desc_origen_admision           	| Descripción textual de la procedencia de la admisión.                           	|
| id_disposicion_alta            	| Identificador numérico del destino del paciente al ser dado de alta.          	|
| desc_disposicion_alta          	| Descripción textual del motivo o condición de alta del paciente.              	|
| dias_hospitalizacion           	| Duración de la estancia hospitalaria medida en días.                            	|
| codigo_pagador                 	| Código del proveedor de seguro médico o entidad pagadora.                     	|
| especialidad_medica            	| Especialidad del médico tratante a cargo de la admisión.                      	|
| num_visitas_ambulatorias       	| Número de consultas ambulatorias realizadas en el año previo.                 	|
| num_visitas_urgencias          	| Número de visitas a la sala de urgencias en el año previo.                    	|
| num_hospitalizaciones_previas  	| Número de ingresos hospitalarios en el año previo.                              	|
| diagnostico_1                  	| Diagnóstico primario codificado según el estándar ICD-9.                      	|
| diagnostico_2                  	| Diagnóstico secundario codificado según el estándar ICD-9.                    	|
| diagnostico_3                  	| Diagnóstico adicional secundario codificado según el estándar ICD-9.          	|
| num_diagnosticos               	| Número total de diagnósticos registrados para el encuentro.                   	|
| num_procedimientos_laboratorio 	| Número total de pruebas de laboratorio realizadas durante el ingreso.         	|
| num_procedimientos_no_lab      	| Número de procedimientos médicos o quirúrgicos no rutinarios realizados.      	|
| num_medicamentos               	| Número total de medicamentos administrados durante la estancia.               	|
| prueba_glucosa_suero           	| Resultado del análisis de glucosa en suero (None, Normal, >200, >300).        	|
| resultado_a1c                  	| Resultado de la prueba de hemoglobina glucosilada A1C (None, Normal, >7, >8). 	|
| metformina                     	| Estado de prescripción/dosis de metformina (No, Down, Steady, Up).            	|
| repaglinida                    	| Estado de prescripción/dosis de repaglinida (No, Down, Steady, Up).           	|
| nateglinida                    	| Estado de prescripción/dosis de nateglinida (No, Down, Steady, Up).           	|
| clorpropamida                  	| Estado de prescripción/dosis de clorpropamida (No, Down, Steady, Up).         	|
| glimepirida                    	| Estado de prescripción/dosis de glimepirida (No, Down, Steady, Up).           	|
| acetohexamida                  	| Estado de prescripción/dosis de acetohexamida (No, Down, Steady, Up).         	|
| glipizida                      	| Estado de prescripción/dosis de glipizida (No, Down, Steady, Up).             	|
| gliburida                      	| Estado de prescripción/dosis de gliburida (No, Down, Steady, Up).             	|
| tolbutamida                    	| Estado de prescripción/dosis de tolbutamida (No, Down, Steady, Up).           	|
| pioglitazona                   	| Estado de prescripción/dosis de pioglitazona (No, Down, Steady, Up).          	|
| rosiglitazona                  	| Estado de prescripción/dosis de rosiglitazona (No, Down, Steady, Up).         	|
| acarbosa                       	| Estado de prescripción/dosis de acarbosa (No, Down, Steady, Up).              	|
| miglitol                       	| Estado de prescripción/dosis de miglitol (No, Down, Steady, Up).              	|
| troglitazona                   	| Estado de prescripción/dosis de troglitazona (No, Down, Steady, Up).          	|
| tolazamida                     	| Estado de prescripción/dosis de tolazamida (No, Down, Steady, Up).            	|
| examida                        	| Estado de prescripción/dosis de examida (No, Down, Steady, Up).               	|
| citogliptina                   	| Estado de prescripción/dosis de citogliptina (No, Down, Steady, Up).          	|
| insulina                       	| Estado de prescripción/dosis de insulina (No, Down, Steady, Up).              	|
| gliburida_metformina           	| Prescripción de la combinación fija gliburida y metformina.                   	|
| glipizida_metformina           	| Prescripción de la combinación fija glipizida y metformina.                   	|
| glimepirida_pioglitazona       	| Prescripción de la combinación fija glimepirida y pioglitazona.               	|
| metformina_rosiglitazona       	| Prescripción de la combinación fija metformina y rosiglitazona.               	|
| metformina_pioglitazona        	| Prescripción de la combinación fija metformina y pioglitazona.                	|
| cambio_medicacion              	| Indica si hubo un cambio o ajuste en la medicación para la diabetes (Yes/No). 	|
| prescripcion_med_diabetes      	| Indica si se prescribió algún medicamento para la diabetes (Yes/No).          	|
| readmitido                     	| Variable objetivo: reingreso del paciente (<30 días, >30 días o NO).            |


🎯 La variable objetivo es `readmitido` y contiene las siguientes categorías:
* `<30`: El paciente fue readmitido dentro de los 30 días posteriores al alta (Alto riesgo).
* `>30`: El paciente fue readmitido, pero después de 30 días.
* `NO`: No hay constancia de reingreso.
