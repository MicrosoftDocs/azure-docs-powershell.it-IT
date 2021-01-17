---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476127"
---
# <span data-ttu-id="9ba04-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9ba04-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="9ba04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ba04-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba04-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="9ba04-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9ba04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ba04-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ba04-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ba04-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba04-106">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="9ba04-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9ba04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ba04-107">EXAMPLES</span></span>

### <span data-ttu-id="9ba04-108">Esempio 1: creare una regola di rete virtuale per un MariaDB</span><span class="sxs-lookup"><span data-stu-id="9ba04-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="9ba04-109">Questo comando crea una regola di rete virtuale per un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="9ba04-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="9ba04-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ba04-110">PARAMETERS</span></span>

### <span data-ttu-id="9ba04-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ba04-111">-AsJob</span></span>
<span data-ttu-id="9ba04-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="9ba04-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9ba04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba04-113">-DefaultProfile</span></span>
<span data-ttu-id="9ba04-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ba04-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ba04-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="9ba04-116">Creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="9ba04-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="9ba04-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ba04-117">-Name</span></span>
<span data-ttu-id="9ba04-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ba04-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="9ba04-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="9ba04-119">-NoWait</span></span>
<span data-ttu-id="9ba04-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="9ba04-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9ba04-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ba04-121">-PassThru</span></span>
<span data-ttu-id="9ba04-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="9ba04-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9ba04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba04-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ba04-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ba04-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9ba04-125">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="9ba04-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9ba04-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9ba04-126">-ServerName</span></span>
<span data-ttu-id="9ba04-127">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="9ba04-127">The name of the server.</span></span>

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

### <span data-ttu-id="9ba04-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9ba04-128">-SubnetId</span></span>
<span data-ttu-id="9ba04-129">ID risorsa ARM della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ba04-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="9ba04-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ba04-130">-SubscriptionId</span></span>
<span data-ttu-id="9ba04-131">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba04-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9ba04-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ba04-132">-Confirm</span></span>
<span data-ttu-id="9ba04-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ba04-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba04-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba04-134">-WhatIf</span></span>
<span data-ttu-id="9ba04-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ba04-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba04-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ba04-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba04-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba04-137">CommonParameters</span></span>
<span data-ttu-id="9ba04-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba04-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba04-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ba04-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba04-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ba04-140">INPUTS</span></span>

## <span data-ttu-id="9ba04-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ba04-141">OUTPUTS</span></span>

### <span data-ttu-id="9ba04-142">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9ba04-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="9ba04-143">Note</span><span class="sxs-lookup"><span data-stu-id="9ba04-143">NOTES</span></span>

<span data-ttu-id="9ba04-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9ba04-144">ALIASES</span></span>

## <span data-ttu-id="9ba04-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ba04-145">RELATED LINKS</span></span>

