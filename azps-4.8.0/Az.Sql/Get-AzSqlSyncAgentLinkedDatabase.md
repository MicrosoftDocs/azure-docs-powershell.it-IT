---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191188"
---
# <span data-ttu-id="62182-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="62182-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="62182-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62182-102">SYNOPSIS</span></span>
<span data-ttu-id="62182-103">Restituisce informazioni sui database di SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="62182-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="62182-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62182-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62182-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62182-105">DESCRIPTION</span></span>
<span data-ttu-id="62182-106">Il cmdlet **Get-AzSqlSyncAgentLinkedDatabase** restituisce informazioni sui database di SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="62182-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="62182-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62182-107">EXAMPLES</span></span>

### <span data-ttu-id="62182-108">Esempio 1: ottenere i database di SQL Server collegati per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="62182-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="62182-109">L'esempio seguente restituisce i database di SQL Server collegati collegati da un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="62182-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="62182-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62182-110">PARAMETERS</span></span>

### <span data-ttu-id="62182-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62182-111">-DefaultProfile</span></span>
<span data-ttu-id="62182-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62182-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62182-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62182-113">-ResourceGroupName</span></span>
<span data-ttu-id="62182-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62182-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62182-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="62182-115">-ServerName</span></span>
<span data-ttu-id="62182-116">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="62182-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62182-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="62182-117">-SyncAgentName</span></span>
<span data-ttu-id="62182-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="62182-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62182-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62182-119">CommonParameters</span></span>
<span data-ttu-id="62182-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62182-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62182-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62182-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62182-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62182-122">INPUTS</span></span>

### <span data-ttu-id="62182-123">System. String</span><span class="sxs-lookup"><span data-stu-id="62182-123">System.String</span></span>

## <span data-ttu-id="62182-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62182-124">OUTPUTS</span></span>

### <span data-ttu-id="62182-125">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="62182-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="62182-126">Note</span><span class="sxs-lookup"><span data-stu-id="62182-126">NOTES</span></span>

## <span data-ttu-id="62182-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62182-127">RELATED LINKS</span></span>
