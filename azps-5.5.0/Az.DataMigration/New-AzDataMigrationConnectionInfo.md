---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177071"
---
# <span data-ttu-id="4322e-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="4322e-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="4322e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4322e-102">SYNOPSIS</span></span>
<span data-ttu-id="4322e-103">Crea un nuovo oggetto Informazioni connessione che specifica il tipo e il nome del server per la connessione.</span><span class="sxs-lookup"><span data-stu-id="4322e-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="4322e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4322e-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4322e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4322e-105">DESCRIPTION</span></span>
<span data-ttu-id="4322e-106">Il cmdlet New-AzDataMigrationConnectionInfo crea un nuovo oggetto Informazioni connessione specificando il tipo di server per la connessione.</span><span class="sxs-lookup"><span data-stu-id="4322e-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="4322e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4322e-107">EXAMPLES</span></span>

### <span data-ttu-id="4322e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4322e-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="4322e-109">Nell'esempio precedente viene creato un nuovo oggetto Informazioni di connessione che fornisce SQL come parametro ServerType.</span><span class="sxs-lookup"><span data-stu-id="4322e-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="4322e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4322e-110">PARAMETERS</span></span>

### <span data-ttu-id="4322e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4322e-111">-DefaultProfile</span></span>
<span data-ttu-id="4322e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4322e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4322e-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="4322e-113">-ServerType</span></span>
<span data-ttu-id="4322e-114">Enumerazione che descrive il tipo di server a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="4322e-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="4322e-115">I valori attualmente supportati SQL per SQL Server, istanza gestita di Azure SQL, MongoDb, BlobsDb e Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4322e-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4322e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4322e-116">CommonParameters</span></span>
<span data-ttu-id="4322e-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4322e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4322e-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4322e-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4322e-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="4322e-119">INPUTS</span></span>

### <span data-ttu-id="4322e-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4322e-120">None</span></span>

## <span data-ttu-id="4322e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4322e-121">OUTPUTS</span></span>

### <span data-ttu-id="4322e-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="4322e-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="4322e-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="4322e-123">NOTES</span></span>

## <span data-ttu-id="4322e-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4322e-124">RELATED LINKS</span></span>
