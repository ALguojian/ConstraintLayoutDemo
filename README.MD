# 约束布局属性以及用法：

```

   <android.support.constraint.ConstraintLayout
             android:layout_width="match_parent"
             android:layout_height="wrap_content"
             android:orientation="vertical">

             <Button
                 android:id="@+id/button13"
                 android:layout_width="0dp"
                 android:layout_height="0dp"
                 android:layout_marginStart="32dp"
                 android:layout_marginTop="16dp"
                 android:text="Button"
                //设置宽高比例
                app:layout_constraintDimensionRatio="H,0.33"
                //设置权重
                app:layout_constraintHorizontal_weight="1"
                app:layout_constraintLeft_toRightOf="@id/imageView2"
                app:layout_constraintRight_toRightOf="parent"
                app:layout_constraintTop_toTopOf="parent" />

             <ImageView
                 android:id="@+id/imageView2"
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:layout_marginStart="24dp"
                 app:layout_constraintBottom_toBottomOf="@+id/button13"
                 app:layout_constraintEnd_toStartOf="@+id/button13"
                 app:layout_constraintStart_toStartOf="parent"
                 app:layout_constraintTop_toTopOf="@+id/button13"
                 app:srcCompat="?attr/actionModeCloseDrawable" />

             <Button
                 android:id="@+id/button2"
                 android:layout_width="0dp"
                 android:layout_height="0dp"
                 android:layout_marginTop="100dp"
                 android:text="asdasd"
                 app:layout_constraintBaseline_toBaselineOf="button3"
                 app:layout_constraintDimensionRatio="H,3:1"
                 app:layout_constraintEnd_toEndOf="parent"
                 app:layout_constraintHorizontal_weight="1"
                 app:layout_constraintStart_toStartOf="parent"
                 app:layout_constraintTop_toBottomOf="@+id/imageView2" />

             <Button
                 android:id="@+id/button3"
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:layout_marginTop="20dp"
                 //设置横向偏移量，默认居中
                 app:layout_constraintHorizontal_bias="0.25"
                 app:layout_constraintLeft_toLeftOf="parent"
                 app:layout_constraintRight_toRightOf="parent"
                 app:layout_constraintTop_toBottomOf="@id/button2" />


                //设置辅助线
             <android.support.constraint.Guideline
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 // //设置横向以及竖向位置
                 app:layout_constraintGuide_percent="0.5" />

         </android.support.constraint.ConstraintLayout>
```