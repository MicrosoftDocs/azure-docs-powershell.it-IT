---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 394975e341d52fb0067b420397189b0a8858cfcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190519"
---
# <span data-ttu-id="c9b86-101">New-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="c9b86-101">New-AzVMwareAuthorization</span></span>

## <span data-ttu-id="c9b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b86-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b86-103">Creare o aggiornare un'autorizzazione del circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="c9b86-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="c9b86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9b86-104">SYNTAX</span></span>

```
New-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c9b86-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9b86-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b86-106">Creare o aggiornare un'autorizzazione del circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="c9b86-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="c9b86-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9b86-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b86-108">Esempio 1: Creare l'autorizzazione</span><span class="sxs-lookup"><span data-stu-id="c9b86-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="c9b86-109">Questo cmdlet crea `azps-test-auth` l'autorizzazione nel cloud privato `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="c9b86-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="c9b86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9b86-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b86-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9b86-111">-AsJob</span></span>
<span data-ttu-id="c9b86-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c9b86-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c9b86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b86-113">-DefaultProfile</span></span>
<span data-ttu-id="c9b86-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b86-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b86-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c9b86-115">-Name</span></span>
<span data-ttu-id="c9b86-116">Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="c9b86-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="c9b86-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c9b86-117">-NoWait</span></span>
<span data-ttu-id="c9b86-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c9b86-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c9b86-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="c9b86-119">-PrivateCloudName</span></span>
<span data-ttu-id="c9b86-120">Nome del cloud privato.</span><span class="sxs-lookup"><span data-stu-id="c9b86-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="c9b86-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b86-121">-ResourceGroupName</span></span>
<span data-ttu-id="c9b86-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9b86-122">The name of the resource group.</span></span>
<span data-ttu-id="c9b86-123">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c9b86-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c9b86-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9b86-124">-SubscriptionId</span></span>
<span data-ttu-id="c9b86-125">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c9b86-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c9b86-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9b86-126">-Confirm</span></span>
<span data-ttu-id="c9b86-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b86-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b86-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b86-128">-WhatIf</span></span>
<span data-ttu-id="c9b86-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9b86-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b86-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9b86-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b86-131">CommonParameters</span></span>
<span data-ttu-id="c9b86-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b86-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9b86-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b86-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9b86-134">INPUTS</span></span>

## <span data-ttu-id="c9b86-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9b86-135">OUTPUTS</span></span>

### <span data-ttu-id="c9b86-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="c9b86-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="c9b86-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9b86-137">NOTES</span></span>

<span data-ttu-id="c9b86-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c9b86-138">ALIASES</span></span>

## <span data-ttu-id="c9b86-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9b86-139">RELATED LINKS</span></span>

