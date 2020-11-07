---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 8fceaa92f14c6218d723b7fa7153970f118855a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687408"
---
# <span data-ttu-id="539d2-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="539d2-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="539d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="539d2-102">SYNOPSIS</span></span>
<span data-ttu-id="539d2-103">Restituisce informazioni sui database di SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="539d2-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="539d2-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="539d2-105">DESCRIPTION</span></span>
<span data-ttu-id="539d2-106">Il cmdlet **Get-AzureRmSqlSyncAgentLinkedDatabases** restituisce informazioni sui database di SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="539d2-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="539d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="539d2-107">EXAMPLES</span></span>

### <span data-ttu-id="539d2-108">Esempio 1: ottenere i database di SQL Server collegati per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="539d2-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="539d2-109">Questo comando restituisce i database di SQL Server collegati collegati da un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="539d2-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="539d2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="539d2-110">PARAMETERS</span></span>

### <span data-ttu-id="539d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539d2-111">-DefaultProfile</span></span>
<span data-ttu-id="539d2-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="539d2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="539d2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="539d2-113">-ResourceGroupName</span></span>
<span data-ttu-id="539d2-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="539d2-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="539d2-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="539d2-115">-ServerName</span></span>
<span data-ttu-id="539d2-116">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="539d2-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="539d2-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="539d2-117">-SyncAgentName</span></span>
<span data-ttu-id="539d2-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="539d2-118">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="539d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539d2-119">CommonParameters</span></span>
<span data-ttu-id="539d2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539d2-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539d2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539d2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="539d2-122">INPUTS</span></span>

### <span data-ttu-id="539d2-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="539d2-123">None</span></span>
<span data-ttu-id="539d2-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="539d2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="539d2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="539d2-125">OUTPUTS</span></span>

### <span data-ttu-id="539d2-126">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="539d2-126">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="539d2-127">Note</span><span class="sxs-lookup"><span data-stu-id="539d2-127">NOTES</span></span>

## <span data-ttu-id="539d2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="539d2-128">RELATED LINKS</span></span>
