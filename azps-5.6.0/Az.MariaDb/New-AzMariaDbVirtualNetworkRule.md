---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cfbbfd9472d18d75dea3da68cb4d2e06cf54c9a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970573"
---
# <span data-ttu-id="51e55-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="51e55-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="51e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51e55-102">SYNOPSIS</span></span>
<span data-ttu-id="51e55-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="51e55-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="51e55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51e55-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51e55-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51e55-105">DESCRIPTION</span></span>
<span data-ttu-id="51e55-106">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="51e55-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="51e55-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51e55-107">EXAMPLES</span></span>

### <span data-ttu-id="51e55-108">Esempio 1: Creare una regola di rete virtuale per un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="51e55-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="51e55-109">Questo comando crea una regola di rete virtuale per un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="51e55-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="51e55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51e55-110">PARAMETERS</span></span>

### <span data-ttu-id="51e55-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51e55-111">-AsJob</span></span>
<span data-ttu-id="51e55-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="51e55-112">Run the command as a job</span></span>

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

### <span data-ttu-id="51e55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e55-113">-DefaultProfile</span></span>
<span data-ttu-id="51e55-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51e55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e55-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e55-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="51e55-116">Creare una regola del firewall prima che per la rete virtuale sia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="51e55-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="51e55-117">-Name</span><span class="sxs-lookup"><span data-stu-id="51e55-117">-Name</span></span>
<span data-ttu-id="51e55-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="51e55-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e55-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="51e55-119">-NoWait</span></span>
<span data-ttu-id="51e55-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="51e55-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="51e55-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51e55-121">-PassThru</span></span>
<span data-ttu-id="51e55-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="51e55-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="51e55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e55-123">-ResourceGroupName</span></span>
<span data-ttu-id="51e55-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="51e55-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="51e55-125">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="51e55-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="51e55-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="51e55-126">-ServerName</span></span>
<span data-ttu-id="51e55-127">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="51e55-127">The name of the server.</span></span>

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

### <span data-ttu-id="51e55-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="51e55-128">-SubnetId</span></span>
<span data-ttu-id="51e55-129">ID ARM della risorsa della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="51e55-129">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e55-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51e55-130">-SubscriptionId</span></span>
<span data-ttu-id="51e55-131">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="51e55-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e55-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51e55-132">-Confirm</span></span>
<span data-ttu-id="51e55-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51e55-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e55-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e55-134">-WhatIf</span></span>
<span data-ttu-id="51e55-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51e55-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e55-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51e55-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e55-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e55-137">CommonParameters</span></span>
<span data-ttu-id="51e55-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e55-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e55-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51e55-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e55-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="51e55-140">INPUTS</span></span>

## <span data-ttu-id="51e55-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51e55-141">OUTPUTS</span></span>

### <span data-ttu-id="51e55-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="51e55-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="51e55-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="51e55-143">NOTES</span></span>

<span data-ttu-id="51e55-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="51e55-144">ALIASES</span></span>

## <span data-ttu-id="51e55-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51e55-145">RELATED LINKS</span></span>

