

template <class T>
class Vector{
    private:
    	int max_size;
    	int size;
    	T *arr;

    public:
    	//constructs an empty vector
    	Vector<T>(){
        	size=0;
        	max_size=0;
        	arr = new T[max_size];
    	}
    //constructs a vector with n copies of val
    	Vector<T>(int n, const T &val){
        	size=n;
        	arr = new T[size];
        	max_size=size;
        	for(int i=0; i<n; i++){
            	arr[i]=val;
        	}
    	}
    	//construct copy of v
    	Vector<T>(const Vector<T>& v){
        	size=v.size();
        	max_size=v.max_size;
        	for(int i=0; i<v.size(); i++){
            	arr[i]=v.at(i);
        	}
       	}
       	//destructor
       	~Vector<T>(){
		   delete [] arr;
		}
		
	
		unsigned int Vector<T>::get_size();
		void Vector<T>::push_back(const T&);
		void Vector<T>::pop_back();
		T& Vector<T>::at(int);
		T& Vector<T>::front();
		T& Vector<T>::back();
		bool Vector<T>::empty();
		void Vector<T>::insert (const T&, int);
		void Vector<T>::erase(int);
		void Vector<T>::erase(int, int);
		void Vector<T>::resize();

};
