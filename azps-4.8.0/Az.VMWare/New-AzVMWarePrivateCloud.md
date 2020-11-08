---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191395"
---
# <span data-ttu-id="e07e6-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="e07e6-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="e07e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e07e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e07e6-103">Creare o aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e07e6-103">Create or update a private cloud</span></span>

## <span data-ttu-id="e07e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e07e6-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e07e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e07e6-105">DESCRIPTION</span></span>
<span data-ttu-id="e07e6-106">Creare o aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e07e6-106">Create or update a private cloud</span></span>

## <span data-ttu-id="e07e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e07e6-107">EXAMPLES</span></span>

### <span data-ttu-id="e07e6-108">Esempio 1: creare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e07e6-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="e07e6-109">Creare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e07e6-109">Create private cloud</span></span>

## <span data-ttu-id="e07e6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e07e6-110">PARAMETERS</span></span>

### <span data-ttu-id="e07e6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e07e6-111">-AsJob</span></span>
<span data-ttu-id="e07e6-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e07e6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e07e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07e6-113">-DefaultProfile</span></span>
<span data-ttu-id="e07e6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e07e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07e6-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="e07e6-115">-Internet</span></span>
<span data-ttu-id="e07e6-116">La connettività a Internet è abilitata o disabilitata</span><span class="sxs-lookup"><span data-stu-id="e07e6-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07e6-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e07e6-117">-Location</span></span>
<span data-ttu-id="e07e6-118">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="e07e6-118">Resource location</span></span>

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

### <span data-ttu-id="e07e6-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="e07e6-119">-ManagementClusterSize</span></span>
<span data-ttu-id="e07e6-120">Dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="e07e6-120">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07e6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e07e6-121">-Name</span></span>
<span data-ttu-id="e07e6-122">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="e07e6-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07e6-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="e07e6-123">-NetworkBlock</span></span>
<span data-ttu-id="e07e6-124">Il blocco di indirizzi deve essere univoco in VNet nell'abbonamento e anche in locale.</span><span class="sxs-lookup"><span data-stu-id="e07e6-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="e07e6-125">Verificare che il formato CIDR sia conforme (a. B. C. D/X) in cui A, B, C, D sia compreso tra 0 e 255 e X sia compreso tra 0 e 22</span><span class="sxs-lookup"><span data-stu-id="e07e6-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="e07e6-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e07e6-126">-NoWait</span></span>
<span data-ttu-id="e07e6-127">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e07e6-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e07e6-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="e07e6-128">-NsxtPassword</span></span>
<span data-ttu-id="e07e6-129">Facoltativamente, imposta la password di Manager NSX-T quando viene creato il cloud privato</span><span class="sxs-lookup"><span data-stu-id="e07e6-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="e07e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="e07e6-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e07e6-131">The name of the resource group.</span></span>
<span data-ttu-id="e07e6-132">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e07e6-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e07e6-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="e07e6-133">-Sku</span></span>
<span data-ttu-id="e07e6-134">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="e07e6-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="e07e6-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e07e6-135">-SubscriptionId</span></span>
<span data-ttu-id="e07e6-136">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e07e6-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e07e6-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e07e6-137">-Tag</span></span>
<span data-ttu-id="e07e6-138">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="e07e6-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07e6-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="e07e6-139">-VcenterPassword</span></span>
<span data-ttu-id="e07e6-140">Facoltativamente, imposta la password di amministratore vCenter quando viene creato il cloud privato</span><span class="sxs-lookup"><span data-stu-id="e07e6-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="e07e6-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e07e6-141">-Confirm</span></span>
<span data-ttu-id="e07e6-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07e6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07e6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07e6-143">-WhatIf</span></span>
<span data-ttu-id="e07e6-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e07e6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07e6-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e07e6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07e6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07e6-146">CommonParameters</span></span>
<span data-ttu-id="e07e6-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07e6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07e6-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e07e6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07e6-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e07e6-149">INPUTS</span></span>

## <span data-ttu-id="e07e6-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e07e6-150">OUTPUTS</span></span>

### <span data-ttu-id="e07e6-151">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="e07e6-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="e07e6-152">Note</span><span class="sxs-lookup"><span data-stu-id="e07e6-152">NOTES</span></span>

<span data-ttu-id="e07e6-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e07e6-153">ALIASES</span></span>

## <span data-ttu-id="e07e6-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e07e6-154">RELATED LINKS</span></span>

