---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686414"
---
# <span data-ttu-id="e6418-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e6418-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="e6418-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6418-102">SYNOPSIS</span></span>
<span data-ttu-id="e6418-103">Crea un nuovo oggetto info connessione che specifica il tipo e il nome del server per la connessione.</span><span class="sxs-lookup"><span data-stu-id="e6418-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6418-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6418-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6418-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6418-105">DESCRIPTION</span></span>
<span data-ttu-id="e6418-106">Il cmdlet New-AzureRmDataMigrationConnectionInfo crea un nuovo oggetto info di connessione che specifica il tipo di server per la connessione.</span><span class="sxs-lookup"><span data-stu-id="e6418-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="e6418-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6418-107">EXAMPLES</span></span>

### <span data-ttu-id="e6418-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6418-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="e6418-109">Nell'esempio precedente viene creato un nuovo oggetto info di connessione che fornisce SQL come parametro ServerType.</span><span class="sxs-lookup"><span data-stu-id="e6418-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="e6418-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6418-110">PARAMETERS</span></span>

### <span data-ttu-id="e6418-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6418-111">-DefaultProfile</span></span>
<span data-ttu-id="e6418-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6418-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6418-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="e6418-113">-ServerType</span></span>
<span data-ttu-id="e6418-114">Enum che descrive il tipo di server a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="e6418-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="e6418-115">I valori attualmente supportati sono SQL per SQL Server, un'istanza gestita di Azure SQL e un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6418-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6418-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6418-116">CommonParameters</span></span>
<span data-ttu-id="e6418-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6418-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6418-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6418-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6418-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6418-119">INPUTS</span></span>

### <span data-ttu-id="e6418-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6418-120">None</span></span>

## <span data-ttu-id="e6418-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6418-121">OUTPUTS</span></span>

### <span data-ttu-id="e6418-122">Microsoft. Azure. Management. DataMigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e6418-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="e6418-123">Note</span><span class="sxs-lookup"><span data-stu-id="e6418-123">NOTES</span></span>

## <span data-ttu-id="e6418-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6418-124">RELATED LINKS</span></span>
