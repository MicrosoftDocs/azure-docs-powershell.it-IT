---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 35942c51aa383dbc7dcbe071083eee575228372a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957997"
---
# <span data-ttu-id="87493-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="87493-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="87493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87493-102">SYNOPSIS</span></span>
<span data-ttu-id="87493-103">Crea una chiave dell'SQL di sincronizzazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="87493-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="87493-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87493-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87493-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="87493-105">DESCRIPTION</span></span>
<span data-ttu-id="87493-106">Il cmdlet **New-AzSqlSyncAgentKey** crea una chiave dell'SQL di sincronizzazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="87493-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="87493-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87493-107">EXAMPLES</span></span>

### <span data-ttu-id="87493-108">Esempio 1: Creare una chiave dell'agente di sincronizzazione per un SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="87493-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="87493-109">Questo comando crea una chiave dell'agente di sincronizzazione per un agente di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="87493-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="87493-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87493-110">PARAMETERS</span></span>

### <span data-ttu-id="87493-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87493-111">-DefaultProfile</span></span>
<span data-ttu-id="87493-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="87493-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87493-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87493-113">-ResourceGroupName</span></span>
<span data-ttu-id="87493-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87493-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="87493-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="87493-115">-ServerName</span></span>
<span data-ttu-id="87493-116">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="87493-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="87493-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="87493-117">-SyncAgentName</span></span>
<span data-ttu-id="87493-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="87493-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87493-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87493-119">-Confirm</span></span>
<span data-ttu-id="87493-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87493-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87493-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87493-121">-WhatIf</span></span>
<span data-ttu-id="87493-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87493-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87493-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87493-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87493-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87493-124">CommonParameters</span></span>
<span data-ttu-id="87493-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87493-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87493-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87493-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87493-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="87493-127">INPUTS</span></span>

### <span data-ttu-id="87493-128">System.String</span><span class="sxs-lookup"><span data-stu-id="87493-128">System.String</span></span>

## <span data-ttu-id="87493-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87493-129">OUTPUTS</span></span>

### <span data-ttu-id="87493-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="87493-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="87493-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="87493-131">NOTES</span></span>

## <span data-ttu-id="87493-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87493-132">RELATED LINKS</span></span>
