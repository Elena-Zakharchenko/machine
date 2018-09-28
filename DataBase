#include <iostream>
#include <string>

struct Patient
{
    std::string name;
    std::string surname;
    int age;
    bool sex;
    std::string city;
    int visitAmount;
};

class DataBase
{
private:
    Patient *patients[100];
    int currentId;
    int currentAmount = 0;
    
public:
    void addPatient()
    {
        int currentId = currentAmount;
        currentAmount ++;
        patients[currentId] = new Patient();
        std::cout << "name:" << std::endl;
        std::cin >> this -> patients[currentId] -> name;
        std::cout << "surname:" << std::endl;
        std::cin >> this -> patients[currentId] -> surname;
        std::cout << "age:" << std::endl;
        std::cin >> this -> patients[currentId] -> age;
        std::cout << "sex (female = 1, male = 0):" << std::endl;
        std::cin >> this -> patients[currentId] -> sex;
        std::cout << "city:" << std::endl;
        std::cin >> this -> patients[currentId] -> city;
        std::cout << "amount of visiting:" << std::endl;
        std::cin >> this -> patients[currentId] -> visitAmount;
        std::cout << "ID:" << currentId << std::endl;
    }
    
    void findPatient(int currentId)
    {
        if (currentId > currentAmount)
        {
            std::cout << "Error ID" << std::endl;
        }
        else
        {
            std::cout << "name:" << this -> patients[currentId] -> name << std::endl;
            std::cout << "surname:" << this -> patients[currentId] -> surname << std::endl;
            std::cout << "sex:";
            if (this -> patients[currentId] -> sex)
            {
                std::cout << "female" << std::endl;
            }
            else
            {
                std::cout << "male" << std::endl;
            }
            std::cout << "city:" << this -> patients[currentId] -> city << std::endl;
            std::cout << "amount of visiting:" << this -> patients[currentId] -> visitAmount << std::endl;
        }
    }
};

int main()
{
    Patient patients[100];
    DataBase db;
    int currentAmount = 0;
    int p = 1;

    
    while(true)
    {
        std::cout << "To add patient push 1" << std::endl;
        std::cout << "To find out the information about the patient push 2" << std::endl;
        std::cout << "To quit the program push 3" << std::endl;
        std::cin >> p;
        int currentId = 0;
        switch(p)
        {
        case 1: 
            db.addPatient();
            break;
        case 2:
            std::cout << "Enter ID of the patient" << std::endl;
            std::cin >> currentId;
            db.findPatient(currentId);
            break;
        case 3:
            break;
        default:
            std::cout << "Error" << std::endl;
        }
    }
}

