# Base class
class Device:
    def __init__(self, brand, model):
        self._brand = brand          # Protected attribute
        self._model = model

    def device_info(self):
        return f"{self._brand} {self._model}"

# Subclass with inheritance and encapsulation
class Smartphone(Device):
    def __init__(self, brand, model, storage, camera_megapixels):
        super().__init__(brand, model)
        self.__storage = storage                 # Private attribute
        self.__camera_megapixels = camera_megapixels

    def take_photo(self):
        return f"Taking a photo with {self.__camera_megapixels}MP camera!"

    def get_storage(self):
        return f"Storage: {self.__storage}GB"

# Creating an object
phone1 = Smartphone("Samsung", "Galaxy S21", 128, 64)

print(phone1.device_info())
print(phone1.take_photo())
print(phone1.get_storage())
