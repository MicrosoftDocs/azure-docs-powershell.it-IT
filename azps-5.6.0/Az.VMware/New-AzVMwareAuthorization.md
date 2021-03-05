---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 7c532f6aca8c959367d4e67725f36b44e4978840
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991814"
---
# <span data-ttu-id="e99e5-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="e99e5-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="e99e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e99e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e99e5-103">Creare o aggiornare un'autorizzazione del circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e99e5-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e99e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e99e5-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e99e5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e99e5-105">DESCRIPTION</span></span>
<span data-ttu-id="e99e5-106">Creare o aggiornare un'autorizzazione del circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e99e5-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e99e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e99e5-107">EXAMPLES</span></span>

### <span data-ttu-id="e99e5-108">Esempio 1: Creare l'autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e99e5-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="e99e5-109">Questo cmdlet crea `azps-test-auth` l'autorizzazione nel cloud privato `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="e99e5-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="e99e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e99e5-110">PARAMETERS</span></span>

### <span data-ttu-id="e99e5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e99e5-111">-AsJob</span></span>
<span data-ttu-id="e99e5-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e99e5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e99e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99e5-113">-DefaultProfile</span></span>
<span data-ttu-id="e99e5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e99e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e99e5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e99e5-115">-Name</span></span>
<span data-ttu-id="e99e5-116">Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="e99e5-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99e5-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e99e5-117">-NoWait</span></span>
<span data-ttu-id="e99e5-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e99e5-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e99e5-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="e99e5-119">-PrivateCloudName</span></span>
<span data-ttu-id="e99e5-120">Nome del cloud privato.</span><span class="sxs-lookup"><span data-stu-id="e99e5-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="e99e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e99e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="e99e5-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e99e5-122">The name of the resource group.</span></span>
<span data-ttu-id="e99e5-123">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e99e5-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e99e5-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e99e5-124">-SubscriptionId</span></span>
<span data-ttu-id="e99e5-125">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e99e5-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e99e5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e99e5-126">-Confirm</span></span>
<span data-ttu-id="e99e5-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e99e5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e99e5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e99e5-128">-WhatIf</span></span>
<span data-ttu-id="e99e5-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e99e5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e99e5-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e99e5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e99e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99e5-131">CommonParameters</span></span>
<span data-ttu-id="e99e5-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99e5-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e99e5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99e5-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="e99e5-134">INPUTS</span></span>

## <span data-ttu-id="e99e5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e99e5-135">OUTPUTS</span></span>

### <span data-ttu-id="e99e5-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="e99e5-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="e99e5-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e99e5-137">NOTES</span></span>

<span data-ttu-id="e99e5-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e99e5-138">ALIASES</span></span>

## <span data-ttu-id="e99e5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e99e5-139">RELATED LINKS</span></span>

