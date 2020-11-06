---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c71f8284cc3b1a2648e3523c77f0e9e2dd2d3876
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513348"
---
# <span data-ttu-id="b3bd9-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b3bd9-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b3bd9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bd9-103">Modifica la configurazione di una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3bd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3bd9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3bd9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3bd9-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bd9-106">Questo comando consente di modificare la configurazione di una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="b3bd9-107">Per controllare il set di regole di rete virtuale nel server, USA invece ' Add-AzureRmSqlServerVirtualNetworkRule ' è Remove-AzureRmSqlServerVirtualNetworkRule '.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="b3bd9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3bd9-108">EXAMPLES</span></span>

### <span data-ttu-id="b3bd9-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3bd9-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="b3bd9-110">Modifica una regola di rete virtuale esistente con l'ID subnet della nuova rete virtuale che contiene informazioni sulla nuova rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b3bd9-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="b3bd9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3bd9-111">PARAMETERS</span></span>

### <span data-ttu-id="b3bd9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3bd9-112">-AsJob</span></span>
<span data-ttu-id="b3bd9-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b3bd9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3bd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bd9-114">-DefaultProfile</span></span>
<span data-ttu-id="b3bd9-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3bd9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3bd9-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3bd9-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b3bd9-117">Creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b3bd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3bd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="b3bd9-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="b3bd9-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b3bd9-120">-ServerName</span></span>
<span data-ttu-id="b3bd9-121">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b3bd9-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b3bd9-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b3bd9-123">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="b3bd9-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="b3bd9-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="b3bd9-125">ID subnet di rete virtuale per la regola.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="b3bd9-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3bd9-126">-Confirm</span></span>
<span data-ttu-id="b3bd9-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3bd9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3bd9-128">-WhatIf</span></span>
<span data-ttu-id="b3bd9-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3bd9-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3bd9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bd9-131">CommonParameters</span></span>
<span data-ttu-id="b3bd9-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3bd9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bd9-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3bd9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bd9-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3bd9-134">INPUTS</span></span>

### <span data-ttu-id="b3bd9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b3bd9-135">System.String</span></span>

## <span data-ttu-id="b3bd9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3bd9-136">OUTPUTS</span></span>

### <span data-ttu-id="b3bd9-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="b3bd9-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b3bd9-138">Note</span><span class="sxs-lookup"><span data-stu-id="b3bd9-138">NOTES</span></span>

## <span data-ttu-id="b3bd9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3bd9-139">RELATED LINKS</span></span>
