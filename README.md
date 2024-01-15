# UAS_MOBILE_SM3

Nama: Abdul Aziz<br>
Kelas : TI 22.A.1<br>
NIM: 312210022<br>
Matakuliah : Pemrograman Mobile<br>
Dosen pengajar : Donny Maulana, S.Kom., M.M.S.I.

<h3>Assalamualaikum Wr.Wb disini saya akan menampilkan hasil akhir project atau Project UAS ,serta menampilkan codingan yang berfungsi untuk menampilkan Fragment serta menammpilkan video yang didalamnya ada kode youtube di dalam Fragment java nya serta memasukan gambar dengan fungsi imagebutton berikut adalah hasilnya dan juga ada beberapa project sebelumnnya</h3>

  
## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|helloworld|[Click Here](Helloword)|
|2|Count|[Click Here](#Count)|
|3|Sianida|[Click Here](#java)|
|4|FragmentActivity|[Click Here](#video)|
|5|Secondfragment|[Click Here](#layout)|
|2|Fragment3|[Click Here](#string)|
|3|twoactivity|[Click Here](#java)|
|4|twoactivity2|[Click Here](#video)|




## Helloworld


> Beikut kodaingan java Hello World

                                          package com.example.tugas9;
                                          import android.os.Bundle;
                                          import androidx.appcompat.app.AppCompatActivity;
                                          
                                          public class Hello extends AppCompatActivity {
                                          
                                              @Override
                                              protected void onCreate(Bundle savedInstanceState) {
                                                  super.onCreate(savedInstanceState);
                                                  setContentView(R.layout.hello); // Sesuaikan dengan nama file XML yang Anda miliki
                                          
                                          
                                              }
                                          }
                            
                            > Berikut XMl nya
                            <?xml version="1.0" encoding="utf-8"?>
                            <androidx.constraintlayout.widget.ConstraintLayout
                                xmlns:android="http://schemas.android.com/apk/res/android"
                                xmlns:app="http://schemas.android.com/apk/res-auto"
                                xmlns:tools="http://schemas.android.com/tools"
                                android:layout_width="match_parent"
                                android:layout_height="match_parent"
                                tools:context=".Hello">
                            
                                <ImageView
                                    android:id="@+id/background"
                                    android:layout_width="match_parent"
                                    android:layout_height="match_parent"
                                    android:background="@drawable/earth"
                                    android:adjustViewBounds="true"
                                    android:scaleType="centerCrop"/>
                            
                            
                                <TextView
                                    android:id="@+id/Texthello"
                                    android:layout_width="wrap_content"
                                    android:layout_height="wrap_content"
                                    android:fontFamily="courier"
                                    android:gravity="center"
                                    android:text="HEllo world"
                                    android:textColor="@color/black"
                                    android:textSize="11pt"
                                    android:textStyle="bold"
                                    app:layout_constraintBottom_toBottomOf="parent"
                                    app:layout_constraintEnd_toEndOf="parent"
                                    app:layout_constraintStart_toStartOf="parent"
                                    app:layout_constraintTop_toTopOf="parent"
                                    tools:ignore="TextSizeCheck" />
                            
                            </androidx.constraintlayout.widget.ConstraintLayout>

<h2>disini hasil run nya https://github.com/lampubohlam/intent_mobile-V2.git </h2>
                        

## Count


<h3> berikutnya kodingan project count/bilangan Fibonance JAVA dan XML nya nya</h3>

><h3> Java nya</h3>
            package com.example.tugas9;
            
            import android.annotation.SuppressLint;
            import android.os.Bundle;
            import android.view.View;
            import android.widget.TextView;
            import android.widget.Toast;
            
            import androidx.appcompat.app.AppCompatActivity;
            
            public class Count extends AppCompatActivity {
                private int nCount = 0;
            
                private TextView nShowCount;
            
                @SuppressLint("MissingInflatedId")
                @Override
                protected void onCreate(Bundle savedInstanceState) {
                    super.onCreate(savedInstanceState);
                    setContentView(R.layout.activity_count);
                    nShowCount = findViewById(R.id.show_count);
                }
            
                public void showToast(View view){
                    Toast toast = Toast.makeText(this, "Menghitung Bilangan",
                            Toast.LENGTH_SHORT);
                    toast.show();
                }
            
                @SuppressLint("SetTextI18n")
                public void countUp(View view){
                    nCount++;
                    if (nShowCount != null)
                        nShowCount.setText(Integer.toString(nCount));
                }
            }


  > <h3>XML Fibonance/Count</h3>

  
                 <?xml version="1.0" encoding="utf-8"?>
          <androidx.constraintlayout.widget.ConstraintLayout
              xmlns:android="http://schemas.android.com/apk/res/android"
              xmlns:app="http://schemas.android.com/apk/res-auto"
              xmlns:tools="http://schemas.android.com/tools"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              tools:context=".Count">
          
              <ImageView
                  android:id="@+id/background"
                  android:layout_width="match_parent"
                  android:layout_height="match_parent"
                  android:background="@drawable/bck_count"
                  android:adjustViewBounds="true"
                  android:scaleType="centerCrop" />
          
              <Button
                  android:id="@+id/button_toast"
                  android:layout_width="0dp"
                  android:layout_height="wrap_content"
                  android:layout_marginEnd="8dp"
                  android:layout_marginStart="8dp"
                  android:layout_marginTop="8dp"
                  android:background="@color/ColorPrimary"
                  android:onClick="showToast"
                  android:text="@string/button_label_toast"
                  android:textColor="@android:color/white"
                  app:layout_constraintEnd_toEndOf="parent"
                  app:layout_constraintStart_toStartOf="parent"
                  app:layout_constraintTop_toTopOf="parent"
                  tools:ignore="UsingOnClickInXml"/>
          
              <Button
                  android:id="@+id/button_count"
                  android:layout_width="0dp"
                  android:layout_height="wrap_content"
                  android:layout_marginEnd="8dp"
                  android:layout_marginStart="8dp"
                  android:layout_marginBottom="8dp"
                  android:background="@color/ColorPrimary"
                  android:onClick="countUp"
                  android:text="@string/button_label_count"
                  android:textColor="@android:color/white"
                  app:layout_constraintEnd_toEndOf="parent"
                  app:layout_constraintStart_toStartOf="parent"
                  app:layout_constraintBottom_toBottomOf="parent"
                  tools:ignore="UsingOnClickInXml" />
          
              <TextView
                  android:id="@+id/show_count"
                  android:layout_width="0dp"
                  android:layout_height="wrap_content"
                  android:layout_marginStart="8dp"
                  android:layout_marginEnd="8dp"
                  android:text="@string/count_initial_value"
                  android:textAlignment="center"
                  android:textColor="@color/ColorPrimary"
                  android:textSize="160sp"
                  android:textStyle="bold"
                  app:layout_constraintBottom_toTopOf="@+id/button_count"
                  app:layout_constraintEnd_toEndOf="parent"
                  app:layout_constraintStart_toStartOf="parent"
                  app:layout_constraintTop_toBottomOf="@+id/button_toast"
                  tools:ignore="RtlCompat" />
          
          </androidx.constraintlayout.widget.ConstraintLayout>



hasil run


https://github.com/lampubohlam/UAS_MOBILE_SM3/assets/151606175/d07a5854-0c67-4c47-bac1-41bee69f0ea7

