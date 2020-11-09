---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310434"
---
# <span data-ttu-id="98173-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="98173-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="98173-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98173-102">SYNOPSIS</span></span>
<span data-ttu-id="98173-103">Creare o aggiornare l'autorizzazione di un circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="98173-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="98173-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98173-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="98173-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98173-105">DESCRIPTION</span></span>
<span data-ttu-id="98173-106">Creare o aggiornare l'autorizzazione di un circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="98173-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="98173-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98173-107">EXAMPLES</span></span>

### <span data-ttu-id="98173-108">Esempio 1: creare autorizzazione</span><span class="sxs-lookup"><span data-stu-id="98173-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="98173-109">Questo cmdlet crea l'autorizzazione `azps-test-auth` in private cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="98173-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="98173-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98173-110">PARAMETERS</span></span>

### <span data-ttu-id="98173-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98173-111">-AsJob</span></span>
<span data-ttu-id="98173-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="98173-112">Run the command as a job</span></span>

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

### <span data-ttu-id="98173-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98173-113">-DefaultProfile</span></span>
<span data-ttu-id="98173-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98173-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98173-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="98173-115">-Name</span></span>
<span data-ttu-id="98173-116">Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="98173-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="98173-117">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="98173-117">-NoWait</span></span>
<span data-ttu-id="98173-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="98173-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="98173-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="98173-119">-PrivateCloudName</span></span>
<span data-ttu-id="98173-120">Nome del cloud privato.</span><span class="sxs-lookup"><span data-stu-id="98173-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="98173-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98173-121">-ResourceGroupName</span></span>
<span data-ttu-id="98173-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="98173-122">The name of the resource group.</span></span>
<span data-ttu-id="98173-123">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="98173-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="98173-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98173-124">-SubscriptionId</span></span>
<span data-ttu-id="98173-125">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="98173-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="98173-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98173-126">-Confirm</span></span>
<span data-ttu-id="98173-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98173-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98173-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98173-128">-WhatIf</span></span>
<span data-ttu-id="98173-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98173-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98173-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98173-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98173-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98173-131">CommonParameters</span></span>
<span data-ttu-id="98173-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98173-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98173-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98173-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98173-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98173-134">INPUTS</span></span>

## <span data-ttu-id="98173-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98173-135">OUTPUTS</span></span>

### <span data-ttu-id="98173-136">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="98173-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="98173-137">Note</span><span class="sxs-lookup"><span data-stu-id="98173-137">NOTES</span></span>

<span data-ttu-id="98173-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="98173-138">ALIASES</span></span>

## <span data-ttu-id="98173-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98173-139">RELATED LINKS</span></span>

