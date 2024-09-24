\c lab1;

CREATE TABLE IF NOT EXISTS clients (
    client_id SERIAL,
    first_name VARCHAR(60),
    last_name VARCHAR(60),
    email VARCHAR(100),
    date_joined DATE,
    PRIMARY KEY (client_id)
);

ALTER TABLE clients
ADD COLUMN IF NOT EXISTS status INT;

ALTER TABLE clients
ALTER COLUMN status TYPE BOOLEAN
USING (status::boolean);

CREATE TABLE IF NOT EXISTS orders (
    order_id SERIAL,
    order_name VARCHAR(100),
    client_id INT,
    PRIMARY KEY (order_id),
    FOREIGN KEY (client_id) REFERENCES clients(client_id)
);

DROP TABLE orders;

DROP DATABASE lab1;
