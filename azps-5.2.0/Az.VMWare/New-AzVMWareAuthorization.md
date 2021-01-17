---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330751"
---
# <span data-ttu-id="dc104-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="dc104-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="dc104-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc104-102">SYNOPSIS</span></span>
<span data-ttu-id="dc104-103">Creare o aggiornare l'autorizzazione di un circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="dc104-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="dc104-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc104-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dc104-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc104-105">DESCRIPTION</span></span>
<span data-ttu-id="dc104-106">Creare o aggiornare l'autorizzazione di un circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="dc104-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="dc104-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc104-107">EXAMPLES</span></span>

### <span data-ttu-id="dc104-108">Esempio 1: creare autorizzazione</span><span class="sxs-lookup"><span data-stu-id="dc104-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="dc104-109">Questo cmdlet crea l'autorizzazione `azps-test-auth` in private cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="dc104-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="dc104-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc104-110">PARAMETERS</span></span>

### <span data-ttu-id="dc104-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc104-111">-AsJob</span></span>
<span data-ttu-id="dc104-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="dc104-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dc104-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc104-113">-DefaultProfile</span></span>
<span data-ttu-id="dc104-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc104-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc104-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc104-115">-Name</span></span>
<span data-ttu-id="dc104-116">Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="dc104-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="dc104-117">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="dc104-117">-NoWait</span></span>
<span data-ttu-id="dc104-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="dc104-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc104-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="dc104-119">-PrivateCloudName</span></span>
<span data-ttu-id="dc104-120">Nome del cloud privato.</span><span class="sxs-lookup"><span data-stu-id="dc104-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="dc104-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc104-121">-ResourceGroupName</span></span>
<span data-ttu-id="dc104-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc104-122">The name of the resource group.</span></span>
<span data-ttu-id="dc104-123">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dc104-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dc104-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc104-124">-SubscriptionId</span></span>
<span data-ttu-id="dc104-125">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dc104-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dc104-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc104-126">-Confirm</span></span>
<span data-ttu-id="dc104-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc104-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc104-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc104-128">-WhatIf</span></span>
<span data-ttu-id="dc104-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc104-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc104-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc104-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc104-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc104-131">CommonParameters</span></span>
<span data-ttu-id="dc104-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc104-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc104-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc104-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc104-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc104-134">INPUTS</span></span>

## <span data-ttu-id="dc104-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc104-135">OUTPUTS</span></span>

### <span data-ttu-id="dc104-136">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="dc104-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="dc104-137">Note</span><span class="sxs-lookup"><span data-stu-id="dc104-137">NOTES</span></span>

<span data-ttu-id="dc104-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dc104-138">ALIASES</span></span>

## <span data-ttu-id="dc104-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc104-139">RELATED LINKS</span></span>

