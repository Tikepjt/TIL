# Change activity

***

## Intent를 활용해 Button 클릭시 Activity를 이동한다.

```
Button OOButton = findViewById(R.id.ButtonO);

OOButton.setOnClickListener(new View.OnClickListener(){

        @Override
                public void onClick(View view) {

            Intent intent = new Intent(getApplicationContext(), OOActivity_01.class);
            startActivity(intent);
        }
        });
```
