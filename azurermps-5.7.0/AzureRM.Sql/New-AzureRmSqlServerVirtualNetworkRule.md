---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 2955834fdb5c902b7495fe212cb9e697b0cee940
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686290"
---
# <span data-ttu-id="ddda5-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ddda5-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="ddda5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddda5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddda5-103">Crea una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ddda5-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddda5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddda5-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddda5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddda5-105">DESCRIPTION</span></span>
<span data-ttu-id="ddda5-106">Crea una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ddda5-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="ddda5-107">Le regole di rete virtuale vengono usate per connettere Azure SQL Server a una rete virtuale specifica per limitare l'accesso a Azure SQL Server solo per essere disponibile all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ddda5-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="ddda5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddda5-108">EXAMPLES</span></span>

### <span data-ttu-id="ddda5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddda5-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="ddda5-110">Crea una regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="ddda5-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="ddda5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddda5-111">PARAMETERS</span></span>

### <span data-ttu-id="ddda5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddda5-112">-AsJob</span></span>
<span data-ttu-id="ddda5-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ddda5-113">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddda5-114">-DefaultProfile</span></span>
<span data-ttu-id="ddda5-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ddda5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ddda5-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ddda5-117">Creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="ddda5-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddda5-118">-ResourceGroupName</span></span>
<span data-ttu-id="ddda5-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ddda5-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ddda5-120">-ServerName</span></span>
<span data-ttu-id="ddda5-121">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ddda5-121">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="ddda5-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="ddda5-123">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ddda5-123">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="ddda5-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="ddda5-125">ID subnet della rete virtuale che specifica i dettagli di Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="ddda5-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddda5-126">-Confirm</span></span>
<span data-ttu-id="ddda5-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddda5-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddda5-128">-WhatIf</span></span>
<span data-ttu-id="ddda5-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddda5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddda5-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddda5-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddda5-131">CommonParameters</span></span>
<span data-ttu-id="ddda5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddda5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddda5-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddda5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddda5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddda5-134">INPUTS</span></span>

### <span data-ttu-id="ddda5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ddda5-135">System.String</span></span>

## <span data-ttu-id="ddda5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddda5-136">OUTPUTS</span></span>

### <span data-ttu-id="ddda5-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="ddda5-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="ddda5-138">Note</span><span class="sxs-lookup"><span data-stu-id="ddda5-138">NOTES</span></span>

## <span data-ttu-id="ddda5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddda5-139">RELATED LINKS</span></span>
