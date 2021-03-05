---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: ea8390de90fff5fb1e228884b131551a5be86e48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992360"
---
# <span data-ttu-id="36cfa-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="36cfa-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="36cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="36cfa-103">Interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="36cfa-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="36cfa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36cfa-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36cfa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36cfa-105">DESCRIPTION</span></span>
<span data-ttu-id="36cfa-106">Il cmdlet **Stop-AzSqlSyncGroupSync** interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="36cfa-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="36cfa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36cfa-107">EXAMPLES</span></span>

### <span data-ttu-id="36cfa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36cfa-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="36cfa-109">Questo comando interrompe la sincronizzazione in corso per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="36cfa-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="36cfa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36cfa-110">PARAMETERS</span></span>

### <span data-ttu-id="36cfa-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36cfa-111">-DatabaseName</span></span>
<span data-ttu-id="36cfa-112">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="36cfa-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="36cfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cfa-113">-DefaultProfile</span></span>
<span data-ttu-id="36cfa-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="36cfa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36cfa-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36cfa-115">-PassThru</span></span>
<span data-ttu-id="36cfa-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="36cfa-116">Defines Whether return the sync group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36cfa-117">-ResourceGroupName</span></span>
<span data-ttu-id="36cfa-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36cfa-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="36cfa-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36cfa-119">-ServerName</span></span>
<span data-ttu-id="36cfa-120">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="36cfa-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="36cfa-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="36cfa-121">-SyncGroupName</span></span>
<span data-ttu-id="36cfa-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="36cfa-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36cfa-123">-Confirm</span></span>
<span data-ttu-id="36cfa-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36cfa-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36cfa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36cfa-125">-WhatIf</span></span>
<span data-ttu-id="36cfa-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36cfa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36cfa-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36cfa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36cfa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cfa-128">CommonParameters</span></span>
<span data-ttu-id="36cfa-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36cfa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cfa-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36cfa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cfa-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="36cfa-131">INPUTS</span></span>

### <span data-ttu-id="36cfa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="36cfa-132">System.String</span></span>

## <span data-ttu-id="36cfa-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36cfa-133">OUTPUTS</span></span>

### <span data-ttu-id="36cfa-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="36cfa-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="36cfa-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="36cfa-135">NOTES</span></span>

## <span data-ttu-id="36cfa-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36cfa-136">RELATED LINKS</span></span>

[<span data-ttu-id="36cfa-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="36cfa-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

