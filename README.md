#### Creación Dojos:
* Dojo.create(name:"CodingDojo Silicon Valley", city:"Mountain View", state:"CA")
* Dojo.create(name:"CodingDojo Seattle", city:"Seattle", state:"WA")
* Dojo.create(name:"CodingDojo New York", city:"New York", state:"NY")

#### Creación Ninja:
* Ninja.create(first_name:"Dante", last_name:"Navarro",dojo_id:1)
* Ninja.create(first_name:"Gaby", last_name:"Rodriguez",dojo_id:1)
* Ninja.create(first_name:"Sara", last_name:"Castro",dojo_id:1)

* Ninja.create(first_name:"Yorch", last_name:"Sepulveda",dojo_id:2)
* Ninja.create(first_name:"Cristian, last_name:"Uribe",dojo_id:2)
* Ninja.create(first_name:"Esthephanie", last_name:"Jimenez",dojo_id:2)

* Ninja.create(first_name:"Yorch", last_name:"Sepulveda",dojo_id:3)
* Ninja.create(first_name:"Cristian, last_name:"Uribe",dojo_id:3)
* Ninja.create(first_name:"Esthephanie", last_name:"Jimenez",dojo_id:3)

#### Creación Dojos comando new:

#### Eliminación Dojos comando new:






#### Al modificar el modelo dojo y eliminar el dojo con id 2 el resultado es:

* Comando: Dojo.find(2).destroy

(0.4ms)  SELECT sqlite_version(*)
  Dojo Load (0.3ms)  SELECT "dojos".* FROM "dojos" WHERE "dojos"."id" = ? LIMIT ?  [["id", 2], ["LIMIT", 1]]
  TRANSACTION (0.1ms)  begin transaction
  Ninja Load (0.2ms)  SELECT "ninjas".* FROM "ninjas" WHERE "ninjas"."dojo_id" = ?  [["dojo_id", 2]]
  Ninja Destroy (0.2ms)  DELETE FROM "ninjas" WHERE "ninjas"."id" = ?  [["id", 4]]
  Ninja Destroy (0.0ms)  DELETE FROM "ninjas" WHERE "ninjas"."id" = ?  [["id", 5]]
  Ninja Destroy (0.0ms)  DELETE FROM "ninjas" WHERE "ninjas"."id" = ?  [["id", 6]]
  Dojo Destroy (0.0ms)  DELETE FROM "dojos" WHERE "dojos"."id" = ?  [["id", 2]]
  TRANSACTION (0.3ms)  commit transaction
 => 
#<Dojo:0x0000000112c5e618
 id: 2,
 name: "CodingDojo Seattle",
 city: "Seattle",
 state: "WA",
 created_at: Tue, 26 Jul 2022 01:10:49.428758000 UTC +00:00,
 updated_at: Tue, 26 Jul 2022 01:10:49.428758000 UTC +00:00> 
