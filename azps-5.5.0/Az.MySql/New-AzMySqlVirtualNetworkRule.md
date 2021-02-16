---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180054"
---
# <span data-ttu-id="b00a1-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b00a1-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="b00a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b00a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b00a1-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="b00a1-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b00a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b00a1-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b00a1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b00a1-105">DESCRIPTION</span></span>
<span data-ttu-id="b00a1-106">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="b00a1-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b00a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b00a1-107">EXAMPLES</span></span>

### <span data-ttu-id="b00a1-108">Esempio 1: Creare una nuova regola di rete virtuale del server MySql</span><span class="sxs-lookup"><span data-stu-id="b00a1-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="b00a1-109">Questi cmdlet creano una regola di rete virtuale del server MySql.</span><span class="sxs-lookup"><span data-stu-id="b00a1-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="b00a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b00a1-110">PARAMETERS</span></span>

### <span data-ttu-id="b00a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b00a1-111">-AsJob</span></span>
<span data-ttu-id="b00a1-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b00a1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b00a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00a1-113">-DefaultProfile</span></span>
<span data-ttu-id="b00a1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b00a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b00a1-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b00a1-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b00a1-116">Creare una regola del firewall prima che la rete virtuale abbia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="b00a1-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b00a1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b00a1-117">-Name</span></span>
<span data-ttu-id="b00a1-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b00a1-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b00a1-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b00a1-119">-NoWait</span></span>
<span data-ttu-id="b00a1-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b00a1-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b00a1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b00a1-121">-PassThru</span></span>
<span data-ttu-id="b00a1-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b00a1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b00a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="b00a1-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b00a1-124">The name of the resource group.</span></span>
<span data-ttu-id="b00a1-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b00a1-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b00a1-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b00a1-126">-ServerName</span></span>
<span data-ttu-id="b00a1-127">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b00a1-127">The name of the server.</span></span>

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

### <span data-ttu-id="b00a1-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b00a1-128">-SubnetId</span></span>
<span data-ttu-id="b00a1-129">ID ARM della risorsa della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b00a1-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="b00a1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b00a1-130">-SubscriptionId</span></span>
<span data-ttu-id="b00a1-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b00a1-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b00a1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b00a1-132">-Confirm</span></span>
<span data-ttu-id="b00a1-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b00a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00a1-134">-WhatIf</span></span>
<span data-ttu-id="b00a1-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b00a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00a1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b00a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00a1-137">CommonParameters</span></span>
<span data-ttu-id="b00a1-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00a1-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b00a1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00a1-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b00a1-140">INPUTS</span></span>

## <span data-ttu-id="b00a1-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b00a1-141">OUTPUTS</span></span>

### <span data-ttu-id="b00a1-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b00a1-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="b00a1-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b00a1-143">NOTES</span></span>

<span data-ttu-id="b00a1-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b00a1-144">ALIASES</span></span>

## <span data-ttu-id="b00a1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b00a1-145">RELATED LINKS</span></span>

