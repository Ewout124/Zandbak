---
layout: landing-page
title: OAS-specificatie voor Meldingen
---
openapi: "3.0.0"
servers:
- description: "SwaggerHub API Auto Mocking"
  url: "https://virtserver.swaggerhub.com/VNGRealisatie/api/jzv_meldingen/v1"
- description: "Referentie-implementatie"
  url: "https://www.voorbeeldgemeente.nl/api/jzv_meldingen/v1"
info:
  title: "JZV Meldingen"
  version: "1.0"
  x-imvertor-generator-version: "Nightly-build.18 - EVALUATION VERSION, PLEASE REGISTER!"
  x-yamlCompiler-stylesheets-version: "20231117"
  contact:
    url: ""
  license:
    name: "European Union Public License, version 1.2 (EUPL-1.2)"
    url: "https://eupl.eu/1.2/nl/"
paths:
  /meldingen:
    get:
      operationId: "getcollectionmeldingen"
      responses:
        200:
          description: "Zoekactie geslaagd"
          headers:
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
            warning:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/warning"
            X-Rate-Limit-Limit:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Limit"
            X-Rate-Limit-Remaining:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Remaining"
            X-Rate-Limit-Reset:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Reset"
          content:
            application/json:
              schema:
                type: "array"
                items:
                  $ref: "#/components/schemas/Melding"
        400:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/400"
        401:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/401"
        403:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/403"
        409:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/409"
        410:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/410"
        415:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/415"
        429:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/429"
        500:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/500"
        501:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/501"
        503:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/503"
        default:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/default"
      tags:
      - "Meldingen"
    post:
      operationId: "postmeldingen"
      requestBody:
        content:
          application/json:
            schema:
              $ref: "#/components/schemas/Melding"
      responses:
        201:
          description: "OK"
          headers:
            Location:
              description: "URI van de nieuwe resource"
              schema:
                type: "string"
                format: "uri"
                example: "/meldingen/"
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
            warning:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/warning"
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Melding"
        400:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/400"
        401:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/401"
        403:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/403"
        409:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/409"
        410:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/410"
        415:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/415"
        429:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/429"
        500:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/500"
        501:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/501"
        503:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/503"
        default:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/default"
      tags:
      - "Meldingen"
    put:
      operationId: "putmeldingen"
      requestBody:
        content:
          application/json:
            schema:
              $ref: "#/components/schemas/Melding"
      responses:
        200:
          description: "Zoekactie geslaagd"
          headers:
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
            warning:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/warning"
            X-Rate-Limit-Limit:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Limit"
            X-Rate-Limit-Remaining:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Remaining"
            X-Rate-Limit-Reset:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Reset"
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Melding"
        400:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/400"
        401:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/401"
        403:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/403"
        409:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/409"
        410:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/410"
        415:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/415"
        429:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/429"
        500:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/500"
        501:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/501"
        503:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/503"
        default:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/default"
      tags:
      - "Meldingen"
  /meldingen/{registratienummer}:
    delete:
      operationId: "deletemeldingenRegistratienummer"
      parameters:
      - in: "path"
        name: "registratienummer"
        required: true
        schema:
          type: "string"
      responses:
        200:
          description: "Verwijderactie geslaagd"
          headers:
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
        204:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/204"
        404:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/404"
      tags:
      - "Meldingen"
    get:
      operationId: "getresourcemeldingenRegistratienummer"
      parameters:
      - in: "path"
        name: "registratienummer"
        required: true
        schema:
          type: "string"
      responses:
        200:
          description: "Zoekactie geslaagd"
          headers:
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
            warning:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/warning"
            X-Rate-Limit-Limit:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Limit"
            X-Rate-Limit-Remaining:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Remaining"
            X-Rate-Limit-Reset:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Reset"
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Melding"
        400:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/400"
        401:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/401"
        403:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/403"
        404:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/404"
        409:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/409"
        410:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/410"
        415:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/415"
        429:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/429"
        500:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/500"
        501:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/501"
        503:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/503"
        default:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/default"
      tags:
      - "Meldingen"
  /uitkomstmeldingen:
    post:
      operationId: "postuitkomstmeldingen"
      requestBody:
        content:
          application/json:
            schema:
              $ref: "#/components/schemas/UitkomstMelding"
      responses:
        201:
          description: "OK"
          headers:
            Location:
              description: "URI van de nieuwe resource"
              schema:
                type: "string"
                format: "uri"
                example: "/uitkomstmeldingen/"
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
            warning:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/warning"
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/UitkomstMelding"
        400:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/400"
        401:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/401"
        403:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/403"
        409:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/409"
        410:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/410"
        415:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/415"
        429:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/429"
        500:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/500"
        501:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/501"
        503:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/503"
        default:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/default"
      tags:
      - "Uitkomstmeldingen"
    put:
      operationId: "putuitkomstmeldingen"
      requestBody:
        content:
          application/json:
            schema:
              $ref: "#/components/schemas/UitkomstMelding"
      responses:
        200:
          description: "Zoekactie geslaagd"
          headers:
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
            warning:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/warning"
            X-Rate-Limit-Limit:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Limit"
            X-Rate-Limit-Remaining:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Remaining"
            X-Rate-Limit-Reset:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Reset"
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/UitkomstMelding"
        400:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/400"
        401:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/401"
        403:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/403"
        409:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/409"
        410:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/410"
        415:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/415"
        429:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/429"
        500:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/500"
        501:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/501"
        503:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/503"
        default:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/default"
      tags:
      - "Uitkomstmeldingen"
  /uitkomstmeldingen/{registratienummer}:
    get:
      operationId: "getresourceuitkomstmeldingenRegistratienummer"
      parameters:
      - in: "path"
        name: "registratienummer"
        required: true
        schema:
          type: "string"
      responses:
        200:
          description: "Zoekactie geslaagd"
          headers:
            api-version:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/api_version"
            warning:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/warning"
            X-Rate-Limit-Limit:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Limit"
            X-Rate-Limit-Remaining:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Remaining"
            X-Rate-Limit-Reset:
              $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/headers/X_Rate_Limit_Reset"
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/UitkomstMelding"
        400:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/400"
        401:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/401"
        403:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/403"
        404:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/404"
        409:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/409"
        410:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/410"
        415:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/415"
        429:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/429"
        500:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/500"
        501:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/501"
        503:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/503"
        default:
          $ref: "https://raw.githubusercontent.com/VNG-Realisatie/API-Kennisbank/master/common/common.yaml#/components/responses/default"
      tags:
      - "Uitkomstmeldingen"

components:
  schemas:
    Melding:
      allOf:
      - $ref: "#/components/schemas/MeldingAbstract"
      - type: "object"
        description: "Een verstrekking van informatie over een bepaalde situatie."
        required:
        - "incident"
        - "natuurlijkPersoon"
        - "overigeInformatie"
        - "zorgelijkeSituatie"
        - "soort"
        - "datumTijd"
        - "verzoek"
        - "terugkoppelingGewenst"
        properties:
          incident:
            $ref: "#/components/schemas/Incident"
          natuurlijkPersoon:
            $ref: "#/components/schemas/NatuurlijkPersoon"
          overigeInformatie:
            $ref: "#/components/schemas/Informatie"
          zorgelijkeSituatie:
            $ref: "#/components/schemas/ZorgelijkeSituatie"
          soort:
            $ref: "#/components/schemas/SoortMeldingEnum"
          datumTijd:
            type: "string"
            title: "datumTijd"
            description: "De datumtijd waarop de melding gedaan is."
            format: "date-time"
          verzoek:
            type: "string"
            title: "verzoek"
            description: "Een verzoek aan de ontvanger van de melding."
            minLength: 1
          terugkoppelingGewenst:
            type: "boolean"
            title: "terugkoppelingGewenst"
            description: "Aanduiding die aangeeft of de indiener van de melding een\
              \ terugkoppeling verwacht."
    UitkomstMelding:
      allOf:
      - $ref: "#/components/schemas/MeldingAbstract"
      - type: "object"
        description: ""
        required:
        - "status"
        properties:
          status:
            $ref: "#/components/schemas/StatusEnum"
    Adres:
      type: "object"
      description: ""
      required:
      - "soortAdres"
      - "straatAdres"
      properties:
        soortAdres:
          $ref: "#/components/schemas/SoortAdresEnum"
        straatAdres:
          $ref: "#/components/schemas/Straatadres"
    Communicatiemiddel:
      type: "object"
      description: "Een manier om met de natuurlijk persoon in contact te komen."
      required:
      - "type"
      - "waarde"
      properties:
        type:
          $ref: "#/components/schemas/CommunicatiemiddelEnum"
        waarde:
          type: "string"
          title: "waarde"
          description: ""
          minLength: 1
    Geboorte:
      type: "object"
      description: "Gegevens over de geboorte van een natuurlijk persoon, zoals beschreven\
        \ in het Burgerlijk Wetboek."
      required:
      - "datum"
      properties:
        datum:
          type: "string"
          title: "datum"
          description: "De datum van de geboorte of de geboortedatum volgens het Art\
            \ 1:19b BW."
          format: "date"
    Incident:
      type: "object"
      description: "Een al dan niet strafbare verstoring van de orde of overtreding\
        \ van wet- of regelgeving."
      required:
      - "datumTijd"
      - "locatie"
      - "omschrijving"
      - "periodeVanTot"
      properties:
        datumTijd:
          type: "string"
          title: "datumTijd"
          description: "De datum plus tijd waarop het incident plaatsvond."
          format: "date-time"
        locatie:
          type: "string"
          title: "locatie"
          description: "Een aanduiding van de locatie, in vrije tekst."
          minLength: 1
        omschrijving:
          type: "string"
          title: "omschrijving"
          description: "De omschrijving van de aard van het incident."
          minLength: 1
        periodeVanTot:
          $ref: "#/components/schemas/Periode"
    Informatie:
      type: "object"
      description: ""
      required:
      - "omschrijving"
      - "uRL"
      properties:
        omschrijving:
          type: "string"
          title: "omschrijving"
          description: ""
          minLength: 1
        uRL:
          type: "string"
          title: "URL"
          description: ""
          format: "uri"
    Naam:
      type: "object"
      description: "De verzameling van tot een persoon behorende gegevens waarmede\
        \ deze (rechtens) aan het maatschappelijk verkeer deel neemt."
      required:
      - "geslachtsnaam"
      properties:
        geslachtsnaam:
          type: "string"
          title: "geslachtsnaam"
          description: "De (geslachts)naam waarvan de eventueel aanwezige voorvoegsels\
            \ (tabel 36) en adellijke titel/predikaat (tabel 38) zijn afgesplitst."
          minLength: 1
        voorletters1:
          type: "string"
          title: "voorletters1"
          description: "De verzameling letters die wordt gevormd door de eerste letter\
            \ van alle in volgorde voorkomende voornamen."
        voornamen:
          type: "string"
          title: "voornamen"
          description: "De verzameling namen die, gescheiden door spaties, aan de\
            \ geslachtsnaam voorafgaat."
        voorvoegselGeslachtsnaam:
          type: "string"
          title: "voorvoegselGeslachtsnaam"
          description: "Dat deel van de geslachtsnaam dat voorkomt in Tabel 36, Voorvoegseltabel\
            \ en, gescheiden door een spatie, vooraf gaat aan de rest van de geslachtsnaam."
    NatuurlijkPersoon:
      type: "object"
      description: "Een persoon die drager is van rechten en plichten."
      required:
      - "adres"
      - "burgerservicenummer"
      - "naam"
      properties:
        adres:
          $ref: "#/components/schemas/Adres"
        burgerservicenummer:
          type: "string"
          title: "burgerservicenummer"
          description: "De identificatie zoals bedoeld in artikel 1.1 van de Wet algemene\
            \ bepalingen burgerservicenummer."
          pattern: "^[0-9]{9}$"
        communicatiemiddel:
          type: "array"
          minItems: 0
          items:
            $ref: "#/components/schemas/Communicatiemiddel"
        geboorte:
          $ref: "#/components/schemas/Geboorte"
        geslachtsaanduiding:
          $ref: "#/components/schemas/GeslachtEnum"
        naam:
          $ref: "#/components/schemas/Naam"
    Periode:
      type: "object"
      description: "Een tijdsduur of een specifieke tijdspanne die begrensd is door\
        \ begin- en einddatum."
      required:
      - "datumTijdBegin"
      - "datumTijdEinde"
      properties:
        datumTijdBegin:
          type: "string"
          title: "datumTijdBegin"
          description: "Het tijdstip op een bepaalde datum waarop de periode begint."
          format: "date-time"
        datumTijdEinde:
          type: "string"
          title: "datumTijdEinde"
          description: ""
          format: "date-time"
    Straatadres:
      type: "object"
      description: ""
      required:
      - "huisletter"
      - "huisnummer"
      - "straatnaam"
      properties:
        huisletter:
          type: "string"
          title: "huisletter"
          description: ""
          minLength: 1
        huisnummer:
          type: "number"
          title: "huisnummer"
          description: ""
        straatnaam:
          type: "string"
          title: "straatnaam"
          description: ""
          minLength: 1
    VraagAntwoord:
      type: "object"
      description: "Een combinatie van een vraag en een antwoord, ter nadere verduidelijking\
        \ van datgene waarop de vraag betrekking heeft."
      required:
      - "vraag"
      - "antwoord"
      properties:
        vraag:
          $ref: "#/components/schemas/VraagEnum"
        antwoord:
          type: "string"
          title: "antwoord"
          description: ""
          minLength: 1
    ZorgelijkeSituatie:
      type: "object"
      description: "Een situatie die aanleiding vormt voor het doen van een melding\
        \ aan een instantie in het sociale domein."
      required:
      - "nadereOmschrijving"
      - "situatieSchets"
      - "vraagAntwoord"
      properties:
        nadereOmschrijving:
          type: "string"
          title: "nadereOmschrijving"
          description: "Een nadere omschrijving van de situatie, in vrije tekst."
          minLength: 1
        situatieSchets:
          type: "string"
          title: "situatieSchets"
          description: "Een beschrijving van de achtergrond, de context van de situatie."
          minLength: 1
        vraagAntwoord:
          $ref: "#/components/schemas/VraagAntwoord"
    MeldingAbstract:
      type: "object"
      description: ""
      required:
      - "registratienummer"
      properties:
        registratienummer:
          type: "string"
          title: "registratienummer"
          description: "De unieke identificatie van een melding."
          minLength: 1
    CommunicatiemiddelEnum:
      type: "string"
      description: "<body><ul><li>`Vaste telefoon` - 01 </li><li>`Mobiele telefoon`\
        \ - 02 </li><li>`Emailadres` - 03 </li></ul></body>"
      enum:
      - "Vaste telefoon"
      - "Mobiele telefoon"
      - "Emailadres"
    GeslachtEnum:
      type: "string"
      description: "<body><ul><li>`man` - Man </li><li>`vrouw` - Vrouw </li><li>`anders`\
        \ - Anders </li><li>`onbekend` - Onbekend </li></ul></body>"
      enum:
      - "man"
      - "vrouw"
      - "anders"
      - "onbekend"
    SoortAdresEnum:
      type: "string"
      description: "<body><ul><li>`01` - Post- of correspondentieadres </li><li>`02`\
        \ - Woon- of verblijfadres </li><li>`03` - GBA-adres </li></ul></body>"
      enum:
      - "01"
      - "02"
      - "03"
    SoortMeldingEnum:
      type: "string"
      description: "<body><ul><li>`NAZ` - Niet-acute Zorg </li><li>`VT` - Veilig Thuis\
        \ </li><li>`ZVH` - Zorg- en Veiligheidshuizen </li></ul></body>"
      enum:
      - "NAZ"
      - "VT"
      - "ZVH"
    StatusEnum:
      type: "string"
      description: "<body><ul><li>`VT-00` - Melding niet ontvankelijk </li><li>`VT-01-01`\
        \ - Uitkomst veiligheidsbeoordeling: Vervolgstappen belegd bij VT </li><li>`VT-01-02`\
        \ - Uitkomst veiligheidsbeoordeling: Overdracht </li><li>`VT-01-03` - Uitkomst\
        \ veiligheidsbeoordeling: Geen vervolgstappen nodig </li><li>`VT-01-04` -\
        \ Uitkomst veiligheidsbeoordeling: Inzet regionaal maatwerk VT </li><li>`VT-02`\
        \ - Overdracht </li><li>`VT-03` - Afsluiting zonder overdracht </li><li>`VT-99`\
        \ - Melding onjuist geadresseerd </li></ul></body>"
      enum:
      - "VT-00"
      - "VT-01-01"
      - "VT-01-02"
      - "VT-01-03"
      - "VT-01-04"
      - "VT-02"
      - "VT-03"
      - "VT-99"
    VraagEnum:
      type: "string"
      description: "<body><ul><li>`NAZ-001` - Vraag 001 voor NAZ-Melding. </li><li>`NAZ-002`\
        \ - Vraag 002 voor NAZ-Melding. </li><li>`VT-001` - Is er sprake van bestaande\
        \ hulpverlening? </li><li>`VT-002` - Is er sprake van een tijdelijk huisverbod?\
        \ </li><li>`ZVH-001` - Vraag 001 voor ZVH-Melding. </li><li>`ZVH-002` - Vraag\
        \ 002 voor ZVH-Melding. </li></ul></body>"
      enum:
      - "NAZ-001"
      - "NAZ-002"
      - "VT-001"
      - "VT-002"
      - "ZVH-001"
      - "ZVH-002"
