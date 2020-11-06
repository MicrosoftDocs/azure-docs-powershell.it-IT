---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511188"
---
# <span data-ttu-id="c3ed8-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="c3ed8-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="c3ed8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ed8-103">Crea un nuovo oggetto info connessione che specifica il tipo e il nome del server per la connessione.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3ed8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3ed8-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="c3ed8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ed8-106">Il cmdlet New-AzureRmDataMigrationConnectionInfo crea un nuovo oggetto info di connessione che specifica il tipo di server per la connessione.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="c3ed8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ed8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3ed8-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="c3ed8-109">Nell'esempio precedente viene creato un nuovo oggetto info di connessione che fornisce SQL come parametro ServerType.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="c3ed8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="c3ed8-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3ed8-111">-Confirm</span></span>
<span data-ttu-id="c3ed8-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="c3ed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ed8-113">-DefaultProfile</span></span>
<span data-ttu-id="c3ed8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed8-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="c3ed8-115">-ServerType</span></span>
<span data-ttu-id="c3ed8-116">Enum che descrive il tipo di server a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="c3ed8-117">I valori attualmente supportati sono SQL per SQL Server e SQLDB per database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="c3ed8-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="c3ed8-118">-AuthType</span></span>
<span data-ttu-id="c3ed8-119">Tipo di autenticazione da usare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-119">Authentication type to use for connection.</span></span> <span data-ttu-id="c3ed8-120">I valori possibili sono SQLAUTHentication e WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c3ed8-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed8-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="c3ed8-121">-DataSource</span></span>
<span data-ttu-id="c3ed8-122">Server address\name a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed8-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="c3ed8-123">-TrustServerCertificate</span></span>
<span data-ttu-id="c3ed8-124">Valore booleano che indica di garantire che la crittografia avvenga.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ed8-125">-WhatIf</span></span>
<span data-ttu-id="c3ed8-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ed8-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```





## <span data-ttu-id="c3ed8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3ed8-128">INPUTS</span></span>

### <span data-ttu-id="c3ed8-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3ed8-129">None</span></span>


## <span data-ttu-id="c3ed8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3ed8-130">OUTPUTS</span></span>

### <span data-ttu-id="c3ed8-131">Microsoft. Azure. Management. DataMigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="c3ed8-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="c3ed8-132">Note</span><span class="sxs-lookup"><span data-stu-id="c3ed8-132">NOTES</span></span>

## <span data-ttu-id="c3ed8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3ed8-133">RELATED LINKS</span></span>

