<p align="center">
<a href="https://connectorabi.com" _target="blank">
<img src="https://github.com/connectorabi/.github/raw/main/images/connectorabi-logo.png"  width="400" />
</a>
</p>


[![](https://img.shields.io/badge/%F0%9F%8C%90%20Powered_by-aliabi.org-blueviolet?style=flat&labelColor=%23323232)](https://aliabi.org) ![GitHub followers](https://img.shields.io/github/followers/miajupiter?label=AliAbi%20Collective&logo=github)


# ConnectorAbi

[![](https://img.shields.io/badge/ConnectorAbi%20Client%20API-Docs-chocolate?style=flat&logo=openapiinitiative&color=yellow)](https://docs.connectorabi.com)

Remote connector service. Client Connector provides you processing data from your server or computer via Rest service.

## Table of contents
- [Client Connector](#client-connector)
- [Supported Data Systems](#supported-data-systems)
- [Download & Install](#download--install)
- [clientId & clientPass](#clientid--clientpass)
- [Structure](#structure)
- [ConnectorAbi Client API](#connectorabi-client-api)
- [License - MIT License](#license---mit-license)

## Client Connector
Download & install this connector to reach to your pc/server over ConnectorAbi Restful Services.

## Supported Data Systems
- SQL Server
- MySQL
- PostgreSQL
- Excel
- File System
- Linux Shell
- Windows Command Prompt

## Download & Install
Download [ClientConnector (for Windows)](https://github.com/connectorabi/connector-server) client connector application.
Unpack zip file and run `connectorabi_setup.exe`

Setup needs administration privileges to install properly.

## clientId & clientPass
When the connector runs first time, it takes new id and password from ConnectorAbi Server. You need them for authentication.


## Structure

```mermaid
graph LR
cc(api.connectorabi.com/connector/:func/:param1/:param2);style cc fill:#1122dd,color:#eee;
conn(Connector Client);style conn fill:#1122dd,color:#eee;
mdb[(MongoDb)];style mdb fill:#548235,color:#eee;
mssql[(SQL Server)];style mssql fill:#548235,color:#eee;
mysql[(MySQL)];style mysql fill:#548235,color:#eee;
xls[Excel Files];style xls fill:#d4d235,color:#222;
fs[File System];style fs fill:#333333,color:#ddd;
cmd[shell/bash/cmd];style cmd fill:#333333,color:#ddd;
ra{{Rest API}};style ra fill:#4472c4,color:#eee;
socket{{Socket Server}};style socket fill:#4472c4,color:#eee;
internet(Internet);style internet fill:#dd72c4,color:#111;

mdb --- conn
mssql --- conn
mysql --- conn
xls --- conn
fs --- conn
cmd --- conn

conn --- internet
internet --> socket
socket --> ra
ra -->cc

subgraph UI [Local Server or Computer]
mdb
mssql
mysql
xls
fs
cmd
conn
end

subgraph dd [ConnectorAbi Server]
socket
cc
ra
end




```

## ConnectorAbi Client API

[ConnectorAbi Client API Documentation](https://docs.connectorabi.com)


## License

[Apache License 2.0](./LICENSE)

