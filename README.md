# Flask-
Templates 
<!DOCTYPE html>
<html>
<head>
    <title>Manage Warehouses</title>
</head>
<body>
    <h1>Manage Warehouses</h1>
    <ul>
        {% for warehouse in warehouses %}
        <li>{{ warehouse.warehouse_name }} - {{ warehouse.warehouse_address }} - {{ warehouse.warehouse_contact }}</li>
        {% endfor %}
    </ul>
</body>
</html>
