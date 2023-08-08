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

# New Templates:

# notifications.html
<!DOCTYPE html>
<html>
<head>
    <title>Notifications</title>
</head>
<body>
    <h1>Notifications</h1>
    <!-- Display notifications using flash messages -->
    {% with messages = get_flashed_messages() %}
    {% if messages %}
    <ul>
        {% for message in messages %}

<!DOCTYPE html>
<html>
<head>
    <title>Add Warehouse</title>
</head>
<body>
    <h1>Add Warehouse</h1>
    <form method="POST" enctype="multipart/form-data">
        {{ form.hidden_tag() }}
        <div>
            {{ form.warehouse_name.label }} {{ form.warehouse_name() }}
        </div>
        <div>
            {{ form.warehouse_address.label }} {{ form.warehouse_address() }}
        </div>
        <div>
            {{ form.warehouse_contact.label }} {{ form.warehouse_contact() }}
        </div>
        <div>
            {{ form.submit() }}
        </div>
    </form>
</body>
</html>
        
        <li>{{ message }}</li>
        {% endfor %}
    </ul>
    {% endif %}
    {% endwith %}
</body>
</html>
