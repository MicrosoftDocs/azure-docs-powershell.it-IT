---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: ce69f6b087a7ed61f415e3d6a649f757bb10178f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995090"
---
# <span data-ttu-id="5aba2-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5aba2-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="5aba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aba2-102">SYNOPSIS</span></span>
<span data-ttu-id="5aba2-103">Rimuove un gruppo di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="5aba2-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5aba2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5aba2-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5aba2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5aba2-105">DESCRIPTION</span></span>
<span data-ttu-id="5aba2-106">Il cmdlet **Remove-AzSqlSyncGroup** rimuove un gruppo di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="5aba2-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5aba2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5aba2-107">EXAMPLES</span></span>

### <span data-ttu-id="5aba2-108">Esempio 1: Rimuovere un gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5aba2-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="5aba2-109">Questo comando rimuove il gruppo di SQL database di Azure denominato syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="5aba2-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="5aba2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5aba2-110">PARAMETERS</span></span>

### <span data-ttu-id="5aba2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5aba2-111">-DatabaseName</span></span>
<span data-ttu-id="5aba2-112">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5aba2-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5aba2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aba2-113">-DefaultProfile</span></span>
<span data-ttu-id="5aba2-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5aba2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aba2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5aba2-115">-Force</span></span>
<span data-ttu-id="5aba2-116">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="5aba2-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5aba2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5aba2-117">-Name</span></span>
<span data-ttu-id="5aba2-118">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5aba2-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aba2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5aba2-119">-PassThru</span></span>
<span data-ttu-id="5aba2-120">Definisce se restituire o meno il gruppo di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="5aba2-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="5aba2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aba2-121">-ResourceGroupName</span></span>
<span data-ttu-id="5aba2-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5aba2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5aba2-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5aba2-123">-ServerName</span></span>
<span data-ttu-id="5aba2-124">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5aba2-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5aba2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5aba2-125">-Confirm</span></span>
<span data-ttu-id="5aba2-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aba2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aba2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aba2-127">-WhatIf</span></span>
<span data-ttu-id="5aba2-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5aba2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aba2-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5aba2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aba2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aba2-130">CommonParameters</span></span>
<span data-ttu-id="5aba2-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aba2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aba2-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5aba2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aba2-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="5aba2-133">INPUTS</span></span>

### <span data-ttu-id="5aba2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5aba2-134">System.String</span></span>

## <span data-ttu-id="5aba2-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5aba2-135">OUTPUTS</span></span>

### <span data-ttu-id="5aba2-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5aba2-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5aba2-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="5aba2-137">NOTES</span></span>

## <span data-ttu-id="5aba2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5aba2-138">RELATED LINKS</span></span>

[<span data-ttu-id="5aba2-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5aba2-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="5aba2-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5aba2-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="5aba2-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5aba2-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

