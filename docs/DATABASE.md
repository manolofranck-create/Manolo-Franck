# Modelo inicial do banco de dados (proposta)

**Estado:** esquema conceitual, ainda não implementado como migrations.

## Countries
- Id (GUID; PK)
- Name (obrigatório)
- Iso2 (único, 2 caracteres)
- Iso3 (único, 3 caracteres)
- Continent (obrigatório)
- Nationality (opcional)
- IsActive (booleano)

## Cities
- Id (GUID; PK)
- CountryId (FK Countries; obrigatório)
- Name (obrigatório)
- StateRegion (opcional)
- Population (opcional)
- Latitude, Longitude (opcionais)

## Clubs
- Id (GUID; PK)
- Name (obrigatório)
- ShortName (opcional)
- CountryId (FK Countries)
- CityId (FK Cities)
- FoundedYear (opcional)
- Reputation (0 a 10000)
- Balance (inteiro, menor unidade monetária; moeda a definir)
- PrimaryColor, SecondaryColor (HEX)
- IsActive (booleano)

## Players
- Id (GUID; PK)
- FirstName, LastName (obrigatórios)
- BirthDate (data ISO)
- CountryId (FK Countries; nacionalidade principal)
- ClubId (FK Clubs, opcional)
- Position (posição principal)
- PreferredFoot (direito, esquerdo, ambos)
- CurrentAbility, PotentialAbility (1 a 200)
- HeightCm, WeightKg (opcionais)

## Regras gerais
- GUIDs em representação estável, padronizada no armazenamento e contratos.
- Unicidade dos códigos ISO e índices para pesquisas.
- Chaves estrangeiras habilitadas; exclusão protegida quando houver dependências.
- Metadados de versão do esquema e timestamps quando pertinentes.
- Verificar coerência City.CountryId = Club.CountryId.
- Jogadores sem clube são permitidos.
- Atributos detalhados, contratos, múltiplas nacionalidades, temporadas e histórico serão tabelas futuras.

## Questões em aberto
- Convenções de país e continente, localização e moedas.
- Modelagem de atributos e posições para o simulador.
- Política de exclusão vs. desativação de entidades.
- Formato exato do banco publicado e consumo na Unity.
