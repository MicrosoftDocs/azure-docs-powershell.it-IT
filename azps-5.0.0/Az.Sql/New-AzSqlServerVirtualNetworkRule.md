---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200117"
---
# <span data-ttu-id="fd34b-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fd34b-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="fd34b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd34b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd34b-103">Crea una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fd34b-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="fd34b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd34b-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd34b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd34b-105">DESCRIPTION</span></span>
<span data-ttu-id="fd34b-106">Crea una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fd34b-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="fd34b-107">Le regole di rete virtuale vengono usate per connettere Azure SQL Server a una rete virtuale specifica per limitare l'accesso a Azure SQL Server solo per essere disponibile all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd34b-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="fd34b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd34b-108">EXAMPLES</span></span>

### <span data-ttu-id="fd34b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd34b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="fd34b-110">Crea una regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="fd34b-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="fd34b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd34b-111">PARAMETERS</span></span>

### <span data-ttu-id="fd34b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd34b-112">-AsJob</span></span>
<span data-ttu-id="fd34b-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fd34b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd34b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd34b-114">-DefaultProfile</span></span>
<span data-ttu-id="fd34b-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fd34b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd34b-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fd34b-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="fd34b-117">Creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="fd34b-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="fd34b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd34b-118">-ResourceGroupName</span></span>
<span data-ttu-id="fd34b-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd34b-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd34b-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fd34b-120">-ServerName</span></span>
<span data-ttu-id="fd34b-121">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fd34b-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fd34b-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="fd34b-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="fd34b-123">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fd34b-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="fd34b-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="fd34b-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="fd34b-125">ID subnet della rete virtuale che specifica i dettagli di Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="fd34b-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="fd34b-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd34b-126">-Confirm</span></span>
<span data-ttu-id="fd34b-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd34b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd34b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd34b-128">-WhatIf</span></span>
<span data-ttu-id="fd34b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd34b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd34b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd34b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd34b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd34b-131">CommonParameters</span></span>
<span data-ttu-id="fd34b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd34b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd34b-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd34b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd34b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd34b-134">INPUTS</span></span>

### <span data-ttu-id="fd34b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fd34b-135">System.String</span></span>

## <span data-ttu-id="fd34b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd34b-136">OUTPUTS</span></span>

### <span data-ttu-id="fd34b-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="fd34b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="fd34b-138">Note</span><span class="sxs-lookup"><span data-stu-id="fd34b-138">NOTES</span></span>

## <span data-ttu-id="fd34b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd34b-139">RELATED LINKS</span></span>
