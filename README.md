# AI_Project
Under the guidance of Prof. Dr. Sanjay Kumar Singh , IIT(BHU) CSE Dept • Implemented **Support Vector Machine** Model to predict the output current for an Electric car, in the dataset containing input currents and phase value of current . • Using the percentage loss of current , predicted the battery life. • Achieved **97%** accuracy. Exposure : Python ,XgBoost Regressor , Machine Learning , Support Vector Machine , Linear Regression . Link to the code : https://github.com/neshvig10/AI_Project 

Link to the dataset used : https://www.kaggle.com/datasets/hankelea/system-identification-of-an-electric-motor

Fields in the dataset : 

- id_k : d-current at time k in A (Ampere)
- iq_k : q-current at time k in A (Ampere)
- epsilon_k : rotor angle at time k in rad (Radian)
- n_k : elementary vector (inverter switching command) applied between time k and time (k+1)
- n_1k : elementary vector (inverter switching command) applied between time (k-1) and time k
- id_k1 : d-current at time (k+1) in A (Ampere)
- iq_k1 : q-current at time (k+1) in A (Ampere)

The dataset used here is derived from PADERBORN University , Germany and it has around 10 million rows of data 

Contributors : 
- S Vigneshwaran (21075073) - myself
- Saikat Mondal (21075075) 

The drivetrain of an electric vehicle consists of a battery, an inverter, an electric motor, and a controller. In our experiment, we always keep our battery ideal
throughout the experiment. The inverter is a power electronic gadget with switchable semiconductors that converts the electric energy provided by the battery from a
two-phase DC voltage to a three-phase AC voltage with varying amplitude and frequency and the generated three currents are transformed to d-q currents using
Clarke and Park transformation. This is required to operate the motor at different rotational speeds with a certain torque generated. Since we are considering the battery to be ideal, we are mainly focusing on the interaction between the inverter, motor, and controller.


![image](https://github.com/neshvig10/AI_Project/assets/104668723/65daf797-c07f-4dae-9c5a-68122874188c)

Figure shows the basic setup of an electric drivetrain of an electric vehicle. Consider, the voltage of the battery be UDC and the inverter consists of three switches (sa, sb, sc) each having a possibility of (+1, -1). Thus, with these 2 different possibilities and 3 switches eight different combinations of switching states are possible generating different voltages at terminals a, b, c as shown in table-1. The instance of all the possibilities of the switches is known as elementary vectors (vn) where n is the index of the vector.


![image](https://github.com/neshvig10/AI_Project/assets/104668723/5b0a9044-2d1f-4908-ab81-4996435aa698)

Because of the structure and setup of the inverter the v1 and v8 produce the same voltage so we consider both of them as a single vector. The motor is generally operated in the dq coordinate system. The dq coordinate system is commonly used in motor control because it simplifies the mathematical modeling and control of the motor. In this coordinate system, the stator currents and voltages are represented in two orthogonal axes: the d-axis and the q-axis.
