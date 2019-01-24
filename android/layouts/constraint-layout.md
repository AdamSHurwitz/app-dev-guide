# ConstraintLayout

[Resources](#Resources)

[Implementation](#Implementation)

[Constraints](#Constraints)

---

## Resources

[Android Developer's Guide](https://developer.android.com/training/constraint-layout/index.html)

[Codelab](https://codelabs.developers.google.com/codelabs/constraint-layout/index.html?index=..%2F..%2Findex)

Documentation
- [ConstraintLayout](https://developer.android.com/reference/android/support/constraint/ConstraintLayout)
- [ConstraintSet](https://developer.android.com/reference/android/support/constraint/ConstraintSet.html)

[Android Developers Blog - Understanding the performance benefits of ConstraintLayout](https://android-developers.googleblog.com/2017/08/understanding-performance-benefits-of.html)

[Adding Views & Constraints to Android Constraint Layout Programmatically](http://www.zoftino.com/adding-views-&-constraints-to-android-constraint-layout-programmatically)

## Implementation

Update build.gradle

    dependencies {
        compile 'com.android.support.constraint:constraint-layout:x.x.x'
    }

**Existing layout**

1. Open your existing layout in Android Studio and click the Design tab at the bottom of the editor window.
2. In the Component Tree window, right-click the layout and then click Convert layout to ConstraintLayout.
New layout

## Constraints

Rules
Must have at least 2 constraints per view (vertical and horizontal)
Constraints only between edges on same plane (vertical or horizontal)

**Types**

- Parent constraint
- Position constraint
- Alignment constraint
- Baseline alignment constraint: hover mouse over baseline handle for 2 seconds until handle blinks white > drag to another baseline

**Constrain to guidelines**

- Autoconnect as you place views 
- Infer constraints for all views in layout 
- Grouped Actions
- Pack
- Align

**Sizing**
- Can mix 0dp and wrap_content
- Wrap Content  
- Any Size  
- Fixed  
- 0dp → match constraint
- Percent
- app:layout_constraintDimensionRatio=16:9
- app:layout_constraintDimensionRatio=H16:9 //respects height

**Layers**

Elements at the top of the xml created behind elements created lower in the xml.
