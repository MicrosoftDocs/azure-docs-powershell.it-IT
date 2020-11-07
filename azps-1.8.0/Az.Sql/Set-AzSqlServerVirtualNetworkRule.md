---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3b318e08e4dbf900b54581b18f551a3accb75480
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676703"
---
# <span data-ttu-id="8341c-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8341c-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="8341c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8341c-102">SYNOPSIS</span></span>
<span data-ttu-id="8341c-103">Modifica la configurazione di una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8341c-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="8341c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8341c-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8341c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8341c-105">DESCRIPTION</span></span>
<span data-ttu-id="8341c-106">Questo comando consente di modificare la configurazione di una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8341c-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="8341c-107">Per controllare il set di regole di rete virtuale nel server, USA invece ' Add-AzSqlServerVirtualNetworkRule ' è Remove-AzSqlServerVirtualNetworkRule '.</span><span class="sxs-lookup"><span data-stu-id="8341c-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="8341c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8341c-108">EXAMPLES</span></span>

### <span data-ttu-id="8341c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8341c-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="8341c-110">Modifica una regola di rete virtuale esistente con l'ID subnet della nuova rete virtuale che contiene informazioni sulla nuova rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8341c-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="8341c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8341c-111">PARAMETERS</span></span>

### <span data-ttu-id="8341c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8341c-112">-AsJob</span></span>
<span data-ttu-id="8341c-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8341c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8341c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8341c-114">-DefaultProfile</span></span>
<span data-ttu-id="8341c-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8341c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8341c-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8341c-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="8341c-117">Creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="8341c-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="8341c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8341c-118">-ResourceGroupName</span></span>
<span data-ttu-id="8341c-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8341c-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="8341c-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8341c-120">-ServerName</span></span>
<span data-ttu-id="8341c-121">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8341c-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8341c-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="8341c-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="8341c-123">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8341c-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="8341c-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="8341c-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="8341c-125">ID subnet di rete virtuale per la regola.</span><span class="sxs-lookup"><span data-stu-id="8341c-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="8341c-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8341c-126">-Confirm</span></span>
<span data-ttu-id="8341c-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8341c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8341c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8341c-128">-WhatIf</span></span>
<span data-ttu-id="8341c-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8341c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8341c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8341c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8341c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8341c-131">CommonParameters</span></span>
<span data-ttu-id="8341c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8341c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8341c-133">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8341c-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8341c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8341c-134">INPUTS</span></span>

### <span data-ttu-id="8341c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8341c-135">System.String</span></span>

## <span data-ttu-id="8341c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8341c-136">OUTPUTS</span></span>

### <span data-ttu-id="8341c-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="8341c-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="8341c-138">Note</span><span class="sxs-lookup"><span data-stu-id="8341c-138">NOTES</span></span>

## <span data-ttu-id="8341c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8341c-139">RELATED LINKS</span></span>
