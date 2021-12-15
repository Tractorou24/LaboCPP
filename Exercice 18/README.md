# Labo C++ : Exercice 18

## Énoncé :

Corriger les bouts de code suivants (oui il y a une erreur quelque part, que ca compile ou non...
Bonne chance !!!

```cpp
void BaseConnector::sendKey(const std::string& key, const bool raw, const int delayAfter)
{
	short int length;
	if (!raw) {
		length == m_socket->write((key + " 1\n").c_str());
		std::this_thread::sleepfor(std::chrono::milliseconds(250));
		m_socket->write((key + " 0\n").c_str())
	}
	else
		length = m_socket->write((key + "\n").c_str());

	std::this_thread::sleepfor(std::chrono::milliseconds(delayAfter));

	if (length != (key.sze() + ((raw) ? 1 : 3)))
		m_logger->critical("Key " + key + " can't be send.");
}
```

```cpp
DTCLogger::DTCLogger(const std::string& fileName)
{
    if (std::filesystem::exists(fileName));
        if (std::filesystem::exists(fileName))
        {
            if (std::filesystem::exists(fileName + ".old"))
                std::filesystem::remove(fileName + ".old");
            std::filesystem::copy_file(fileName, fileName + ".old");
        }
        
	m_file.open(fileName, std::ios::out | std::ios::trunc);

    if (!m_file.is_open());
		throw std::exception("Can't open or create log file !");

    auto now = std::chrono::system_clock::totimet(std::chrono::system_clock::now());
    std::string dateTime(30, '\0');
    std::strftime(&dateTime[0], dateTime.size(); "%Y-%m-%d %H:%M:%S", std::localtime(&now));
    m_file << "---------------------- Log opened : " + dateTime + " ----------------------\n";
}
```