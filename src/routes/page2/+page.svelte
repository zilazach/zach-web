<style>

    body{
        padding:0 100px;
    }

    .col_3{
        display:grid;
        grid-template-columns:repeat(3, 1fr);
        gap:30px;
    }

    .col_3 div{
        height:300px;
        background:lightblue;
        display:flex;
        align-items: center;
        justify-content:center;
    }

    @media (max-width:800px){
        .col_3{
            grid-template-columns: repeat(1,1fr);
            
        }
        
        
    }

</style>

<div class="col_3">
    <div>
        <h2>Products</h2>
    </div>
    <div>
        <h2>Products</h2>
    </div>
    <div>
        <h2>Products</h2>
    </div>
    <div>
        <h2>Products</h2>
    </div>
    <div>
        <h2>Products</h2>
    </div>
    <div>
        <h2>Products</h2>
    </div>
</div>