---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: b583c8339ebec74fdf8df4116204b7ad5523c258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997274"
---
# <span data-ttu-id="3733d-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3733d-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="3733d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3733d-102">SYNOPSIS</span></span>
<span data-ttu-id="3733d-103">Modifica la configurazione di una regola di azure SQL Server rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3733d-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="3733d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3733d-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3733d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3733d-105">DESCRIPTION</span></span>
<span data-ttu-id="3733d-106">Questo comando modifica la configurazione di una regola di azure SQL Server rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3733d-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="3733d-107">Per controllare il set di regole di rete virtuale nel server, usare invece "Add-AzSqlServerVirtualNetworkRule" e "Remove-AzSqlServerVirtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="3733d-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="3733d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3733d-108">EXAMPLES</span></span>

### <span data-ttu-id="3733d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3733d-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="3733d-110">Modifica una regola di rete virtuale esistente con il nuovo ID subnet della rete virtuale che contiene informazioni sulla nuova rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3733d-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="3733d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3733d-111">PARAMETERS</span></span>

### <span data-ttu-id="3733d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3733d-112">-AsJob</span></span>
<span data-ttu-id="3733d-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3733d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3733d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3733d-114">-DefaultProfile</span></span>
<span data-ttu-id="3733d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3733d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3733d-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3733d-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3733d-117">Creare una regola del firewall prima che per la rete virtuale sia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="3733d-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3733d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3733d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3733d-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3733d-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="3733d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3733d-120">-ServerName</span></span>
<span data-ttu-id="3733d-121">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3733d-121">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3733d-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="3733d-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="3733d-123">Nome della regola di rete virtuale del server sql di Azure.</span><span class="sxs-lookup"><span data-stu-id="3733d-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3733d-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="3733d-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="3733d-125">ID subnet della rete virtuale per la regola.</span><span class="sxs-lookup"><span data-stu-id="3733d-125">The Virtual Network Subnet Id for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3733d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3733d-126">-Confirm</span></span>
<span data-ttu-id="3733d-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3733d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3733d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3733d-128">-WhatIf</span></span>
<span data-ttu-id="3733d-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3733d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3733d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3733d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3733d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3733d-131">CommonParameters</span></span>
<span data-ttu-id="3733d-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3733d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3733d-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3733d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3733d-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="3733d-134">INPUTS</span></span>

### <span data-ttu-id="3733d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3733d-135">System.String</span></span>

## <span data-ttu-id="3733d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3733d-136">OUTPUTS</span></span>

### <span data-ttu-id="3733d-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="3733d-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="3733d-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="3733d-138">NOTES</span></span>

## <span data-ttu-id="3733d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3733d-139">RELATED LINKS</span></span>
