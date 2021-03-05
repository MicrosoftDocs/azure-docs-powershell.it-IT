---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: b27aee4c665dd2725bfd8643cb12ca005a5c4e1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014494"
---
# <span data-ttu-id="74490-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="74490-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="74490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74490-102">SYNOPSIS</span></span>
<span data-ttu-id="74490-103">Restituisce informazioni su SQL Server database collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="74490-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="74490-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74490-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74490-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="74490-105">DESCRIPTION</span></span>
<span data-ttu-id="74490-106">Il cmdlet **Get-AzSqlSyncAgentLinkedDatabase** restituisce informazioni sui database SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="74490-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="74490-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74490-107">EXAMPLES</span></span>

### <span data-ttu-id="74490-108">Esempio 1: Ottenere i database di SQL Server collegati per un agente di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="74490-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="74490-109">L'esempio seguente restituisce i database SQL Server collegati da un agente di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="74490-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="74490-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74490-110">PARAMETERS</span></span>

### <span data-ttu-id="74490-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74490-111">-DefaultProfile</span></span>
<span data-ttu-id="74490-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="74490-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74490-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74490-113">-ResourceGroupName</span></span>
<span data-ttu-id="74490-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="74490-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="74490-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="74490-115">-ServerName</span></span>
<span data-ttu-id="74490-116">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="74490-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="74490-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="74490-117">-SyncAgentName</span></span>
<span data-ttu-id="74490-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="74490-118">The sync agent name.</span></span>

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

### <span data-ttu-id="74490-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74490-119">CommonParameters</span></span>
<span data-ttu-id="74490-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74490-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74490-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74490-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74490-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="74490-122">INPUTS</span></span>

### <span data-ttu-id="74490-123">System.String</span><span class="sxs-lookup"><span data-stu-id="74490-123">System.String</span></span>

## <span data-ttu-id="74490-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74490-124">OUTPUTS</span></span>

### <span data-ttu-id="74490-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="74490-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="74490-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="74490-126">NOTES</span></span>

## <span data-ttu-id="74490-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74490-127">RELATED LINKS</span></span>
