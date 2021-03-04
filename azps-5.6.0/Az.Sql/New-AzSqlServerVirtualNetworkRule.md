---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f5dbea3701f7f0fdaf9c503e58e03fdcc9237530
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955197"
---
# <span data-ttu-id="56a54-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56a54-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="56a54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56a54-102">SYNOPSIS</span></span>
<span data-ttu-id="56a54-103">Crea una regola di SQL Server virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="56a54-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="56a54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56a54-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56a54-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56a54-105">DESCRIPTION</span></span>
<span data-ttu-id="56a54-106">Crea una regola di SQL Server virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="56a54-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="56a54-107">Le regole di rete virtuale vengono usate per connettere il SQL Server di Azure a una rete virtuale specifica per limitare l'accesso al SQL Server di Azure in modo che sia disponibile solo all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56a54-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="56a54-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56a54-108">EXAMPLES</span></span>

### <span data-ttu-id="56a54-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56a54-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="56a54-110">Crea una regola di SQL Server virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="56a54-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="56a54-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56a54-111">PARAMETERS</span></span>

### <span data-ttu-id="56a54-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56a54-112">-AsJob</span></span>
<span data-ttu-id="56a54-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="56a54-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56a54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a54-114">-DefaultProfile</span></span>
<span data-ttu-id="56a54-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56a54-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56a54-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a54-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="56a54-117">Creare una regola del firewall prima che la rete virtuale abbia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="56a54-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="56a54-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a54-118">-ResourceGroupName</span></span>
<span data-ttu-id="56a54-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56a54-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="56a54-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56a54-120">-ServerName</span></span>
<span data-ttu-id="56a54-121">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="56a54-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="56a54-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="56a54-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="56a54-123">Nome della regola della rete virtuale di Sql Server di Azure.</span><span class="sxs-lookup"><span data-stu-id="56a54-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="56a54-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="56a54-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="56a54-125">ID subnet della rete virtuale che specifica i dettagli di Microsoft.Network</span><span class="sxs-lookup"><span data-stu-id="56a54-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="56a54-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56a54-126">-Confirm</span></span>
<span data-ttu-id="56a54-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56a54-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56a54-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56a54-128">-WhatIf</span></span>
<span data-ttu-id="56a54-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56a54-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56a54-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56a54-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56a54-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a54-131">CommonParameters</span></span>
<span data-ttu-id="56a54-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56a54-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a54-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56a54-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a54-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="56a54-134">INPUTS</span></span>

### <span data-ttu-id="56a54-135">System.String</span><span class="sxs-lookup"><span data-stu-id="56a54-135">System.String</span></span>

## <span data-ttu-id="56a54-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56a54-136">OUTPUTS</span></span>

### <span data-ttu-id="56a54-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="56a54-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="56a54-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="56a54-138">NOTES</span></span>

## <span data-ttu-id="56a54-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56a54-139">RELATED LINKS</span></span>
