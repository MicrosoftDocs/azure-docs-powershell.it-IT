---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188309"
---
# <span data-ttu-id="fb672-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fb672-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="fb672-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb672-102">SYNOPSIS</span></span>
<span data-ttu-id="fb672-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="fb672-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fb672-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb672-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb672-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb672-105">DESCRIPTION</span></span>
<span data-ttu-id="fb672-106">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="fb672-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fb672-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb672-107">EXAMPLES</span></span>

### <span data-ttu-id="fb672-108">Esempio 1: creare una nuova regola di rete virtuale del server PostgreSql</span><span class="sxs-lookup"><span data-stu-id="fb672-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="fb672-109">Questi cmdlet creano una regola di rete virtuale del server PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="fb672-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="fb672-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb672-110">PARAMETERS</span></span>

### <span data-ttu-id="fb672-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb672-111">-AsJob</span></span>
<span data-ttu-id="fb672-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="fb672-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fb672-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb672-113">-DefaultProfile</span></span>
<span data-ttu-id="fb672-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb672-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb672-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb672-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="fb672-116">Creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="fb672-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="fb672-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb672-117">-Name</span></span>
<span data-ttu-id="fb672-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb672-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="fb672-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="fb672-119">-NoWait</span></span>
<span data-ttu-id="fb672-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="fb672-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb672-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb672-121">-PassThru</span></span>
<span data-ttu-id="fb672-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="fb672-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fb672-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb672-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb672-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb672-124">The name of the resource group.</span></span>
<span data-ttu-id="fb672-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fb672-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb672-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fb672-126">-ServerName</span></span>
<span data-ttu-id="fb672-127">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="fb672-127">The name of the server.</span></span>

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

### <span data-ttu-id="fb672-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fb672-128">-SubnetId</span></span>
<span data-ttu-id="fb672-129">ID risorsa ARM della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb672-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="fb672-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb672-130">-SubscriptionId</span></span>
<span data-ttu-id="fb672-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb672-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb672-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb672-132">-Confirm</span></span>
<span data-ttu-id="fb672-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb672-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb672-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb672-134">-WhatIf</span></span>
<span data-ttu-id="fb672-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb672-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb672-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb672-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb672-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb672-137">CommonParameters</span></span>
<span data-ttu-id="fb672-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb672-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb672-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb672-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb672-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb672-140">INPUTS</span></span>

## <span data-ttu-id="fb672-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb672-141">OUTPUTS</span></span>

### <span data-ttu-id="fb672-142">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fb672-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="fb672-143">Note</span><span class="sxs-lookup"><span data-stu-id="fb672-143">NOTES</span></span>

<span data-ttu-id="fb672-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fb672-144">ALIASES</span></span>

## <span data-ttu-id="fb672-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb672-145">RELATED LINKS</span></span>

