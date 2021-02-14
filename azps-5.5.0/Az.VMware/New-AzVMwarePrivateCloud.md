---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.VMware/new-azVMwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 3e5e8fa4d098ce68899294a25866b4636c80878e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188727"
---
# <span data-ttu-id="7a5ec-101">New-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7a5ec-101">New-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="7a5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5ec-103">Creare o aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="7a5ec-103">Create or update a private cloud</span></span>

## <span data-ttu-id="7a5ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a5ec-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a5ec-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7a5ec-105">DESCRIPTION</span></span>
<span data-ttu-id="7a5ec-106">Creare o aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="7a5ec-106">Create or update a private cloud</span></span>

## <span data-ttu-id="7a5ec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a5ec-107">EXAMPLES</span></span>

### <span data-ttu-id="7a5ec-108">Esempio 1: Creare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="7a5ec-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7a5ec-109">Creare cloud privato</span><span class="sxs-lookup"><span data-stu-id="7a5ec-109">Create private cloud</span></span>

## <span data-ttu-id="7a5ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a5ec-110">PARAMETERS</span></span>

### <span data-ttu-id="7a5ec-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="7a5ec-111">-AcceptEULA</span></span>
<span data-ttu-id="7a5ec-112">Accettare il contratto di licenza di AVS, il termine legale verrà visualizzato senza questo parametro fornito</span><span class="sxs-lookup"><span data-stu-id="7a5ec-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="7a5ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a5ec-113">-AsJob</span></span>
<span data-ttu-id="7a5ec-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="7a5ec-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7a5ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5ec-115">-DefaultProfile</span></span>
<span data-ttu-id="7a5ec-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a5ec-117">-Internet</span><span class="sxs-lookup"><span data-stu-id="7a5ec-117">-Internet</span></span>
<span data-ttu-id="7a5ec-118">La connettività a Internet è abilitata o disabilitata</span><span class="sxs-lookup"><span data-stu-id="7a5ec-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5ec-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7a5ec-119">-Location</span></span>
<span data-ttu-id="7a5ec-120">Luogo della risorsa</span><span class="sxs-lookup"><span data-stu-id="7a5ec-120">Resource location</span></span>

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

### <span data-ttu-id="7a5ec-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="7a5ec-121">-ManagementClusterSize</span></span>
<span data-ttu-id="7a5ec-122">Le dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="7a5ec-122">The cluster size</span></span>

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

### <span data-ttu-id="7a5ec-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7a5ec-123">-Name</span></span>
<span data-ttu-id="7a5ec-124">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="7a5ec-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="7a5ec-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="7a5ec-125">-NetworkBlock</span></span>
<span data-ttu-id="7a5ec-126">Il blocco di indirizzi deve essere univoco sia in VNet nell'abbonamento che in locale.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="7a5ec-127">Assicurarsi che il formato CIDR sia conforme a (A.B.C.D/X) in cui A,B,C,D è compreso tra 0 e 255 e X è compreso tra 0 e 22</span><span class="sxs-lookup"><span data-stu-id="7a5ec-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="7a5ec-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7a5ec-128">-NoWait</span></span>
<span data-ttu-id="7a5ec-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="7a5ec-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7a5ec-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="7a5ec-130">-NsxtPassword</span></span>
<span data-ttu-id="7a5ec-131">Facoltativamente, impostare la password di Gestione NSX-T al momento della creazione del cloud privato</span><span class="sxs-lookup"><span data-stu-id="7a5ec-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="7a5ec-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5ec-132">-ResourceGroupName</span></span>
<span data-ttu-id="7a5ec-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-133">The name of the resource group.</span></span>
<span data-ttu-id="7a5ec-134">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7a5ec-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="7a5ec-135">-Sku</span></span>
<span data-ttu-id="7a5ec-136">Nome dello SKU.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="7a5ec-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a5ec-137">-SubscriptionId</span></span>
<span data-ttu-id="7a5ec-138">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7a5ec-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a5ec-139">-Tag</span></span>
<span data-ttu-id="7a5ec-140">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="7a5ec-140">Resource tags</span></span>

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

### <span data-ttu-id="7a5ec-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="7a5ec-141">-VcenterPassword</span></span>
<span data-ttu-id="7a5ec-142">Facoltativamente, impostare la password di amministratore vCenter al momento della creazione del cloud privato</span><span class="sxs-lookup"><span data-stu-id="7a5ec-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="7a5ec-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a5ec-143">-Confirm</span></span>
<span data-ttu-id="7a5ec-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a5ec-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5ec-145">-WhatIf</span></span>
<span data-ttu-id="7a5ec-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a5ec-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a5ec-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5ec-148">CommonParameters</span></span>
<span data-ttu-id="7a5ec-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5ec-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5ec-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="7a5ec-151">INPUTS</span></span>

## <span data-ttu-id="7a5ec-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a5ec-152">OUTPUTS</span></span>

### <span data-ttu-id="7a5ec-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7a5ec-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="7a5ec-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="7a5ec-154">NOTES</span></span>

<span data-ttu-id="7a5ec-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7a5ec-155">ALIASES</span></span>

## <span data-ttu-id="7a5ec-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a5ec-156">RELATED LINKS</span></span>

