---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188935"
---
# <span data-ttu-id="f3df3-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="f3df3-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="f3df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3df3-102">SYNOPSIS</span></span>
<span data-ttu-id="f3df3-103">Restituisce informazioni sui SQL Server database collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3df3-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="f3df3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3df3-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3df3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3df3-105">DESCRIPTION</span></span>
<span data-ttu-id="f3df3-106">Il cmdlet **Get-AzSqlSyncAgentLinkedDatabase** restituisce informazioni sui database SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3df3-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="f3df3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3df3-107">EXAMPLES</span></span>

### <span data-ttu-id="f3df3-108">Esempio 1: Ottenere i database di SQL Server collegati per un agente di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f3df3-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="f3df3-109">L'esempio seguente restituisce i database SQL Server collegati da un agente di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f3df3-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="f3df3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3df3-110">PARAMETERS</span></span>

### <span data-ttu-id="f3df3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3df3-111">-DefaultProfile</span></span>
<span data-ttu-id="f3df3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f3df3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3df3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3df3-113">-ResourceGroupName</span></span>
<span data-ttu-id="f3df3-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3df3-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3df3-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3df3-115">-ServerName</span></span>
<span data-ttu-id="f3df3-116">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3df3-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f3df3-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="f3df3-117">-SyncAgentName</span></span>
<span data-ttu-id="f3df3-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3df3-118">The sync agent name.</span></span>

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

### <span data-ttu-id="f3df3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3df3-119">CommonParameters</span></span>
<span data-ttu-id="f3df3-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3df3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3df3-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3df3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3df3-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3df3-122">INPUTS</span></span>

### <span data-ttu-id="f3df3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f3df3-123">System.String</span></span>

## <span data-ttu-id="f3df3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3df3-124">OUTPUTS</span></span>

### <span data-ttu-id="f3df3-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f3df3-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="f3df3-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3df3-126">NOTES</span></span>

## <span data-ttu-id="f3df3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3df3-127">RELATED LINKS</span></span>
