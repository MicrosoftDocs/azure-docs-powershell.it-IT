---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 30c0cca7fb1d8eab2c5d0abe4d6c0d556cc92d7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995145"
---
# <span data-ttu-id="5d23c-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="5d23c-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="5d23c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d23c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d23c-103">Rimuove un agente di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d23c-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="5d23c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d23c-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d23c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d23c-105">DESCRIPTION</span></span>
<span data-ttu-id="5d23c-106">Il cmdlet **Remove-AzSqlSyncAgent** rimuove un agente di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d23c-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="5d23c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d23c-107">EXAMPLES</span></span>

### <span data-ttu-id="5d23c-108">Esempio 1: Rimuovere un agente di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5d23c-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="5d23c-109">Questo comando rimuove l'agente di SQL Azure denominato syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="5d23c-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="5d23c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d23c-110">PARAMETERS</span></span>

### <span data-ttu-id="5d23c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d23c-111">-DefaultProfile</span></span>
<span data-ttu-id="5d23c-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5d23c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d23c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5d23c-113">-Force</span></span>
<span data-ttu-id="5d23c-114">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="5d23c-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5d23c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5d23c-115">-Name</span></span>
<span data-ttu-id="5d23c-116">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5d23c-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d23c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d23c-117">-PassThru</span></span>
<span data-ttu-id="5d23c-118">Definisce se restituire l'agente di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="5d23c-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="5d23c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d23c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d23c-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d23c-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d23c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d23c-121">-ServerName</span></span>
<span data-ttu-id="5d23c-122">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5d23c-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="5d23c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d23c-123">-Confirm</span></span>
<span data-ttu-id="5d23c-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d23c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d23c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d23c-125">-WhatIf</span></span>
<span data-ttu-id="5d23c-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d23c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d23c-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d23c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d23c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d23c-128">CommonParameters</span></span>
<span data-ttu-id="5d23c-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d23c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d23c-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d23c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d23c-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d23c-131">INPUTS</span></span>

### <span data-ttu-id="5d23c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5d23c-132">System.String</span></span>

## <span data-ttu-id="5d23c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d23c-133">OUTPUTS</span></span>

### <span data-ttu-id="5d23c-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="5d23c-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="5d23c-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d23c-135">NOTES</span></span>

## <span data-ttu-id="5d23c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d23c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d23c-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="5d23c-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="5d23c-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="5d23c-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

