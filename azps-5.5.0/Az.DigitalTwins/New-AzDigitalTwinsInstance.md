---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200382"
---
# <span data-ttu-id="e095e-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e095e-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="e095e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e095e-102">SYNOPSIS</span></span>
<span data-ttu-id="e095e-103">Creare o aggiornare i metadati di un'istanza di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e095e-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="e095e-104">Il modello più comune per modificare una proprietà è recuperare DigitalTwinsInstance e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e095e-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="e095e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e095e-105">SYNTAX</span></span>

### <span data-ttu-id="e095e-106">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e095e-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e095e-107">Crea</span><span class="sxs-lookup"><span data-stu-id="e095e-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e095e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e095e-108">DESCRIPTION</span></span>
<span data-ttu-id="e095e-109">Creare o aggiornare i metadati di un'istanza di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e095e-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="e095e-110">Il modello più comune per modificare una proprietà è recuperare DigitalTwinsInstance e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e095e-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="e095e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e095e-111">EXAMPLES</span></span>

### <span data-ttu-id="e095e-112">Esempio 1: Creare una AzDigitalTwinsInstance per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e095e-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e095e-113">Creare una AzDigitalTwinsInstance per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e095e-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="e095e-114">Esempio 2: Creare un oggetto AzDigitalTwinsInstance da AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="e095e-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e095e-115">Creare un oggetto AzDigitalTwinsInstance da AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="e095e-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="e095e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e095e-116">PARAMETERS</span></span>

### <span data-ttu-id="e095e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e095e-117">-AsJob</span></span>
<span data-ttu-id="e095e-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e095e-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e095e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e095e-119">-DefaultProfile</span></span>
<span data-ttu-id="e095e-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e095e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e095e-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="e095e-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="e095e-122">Descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="e095e-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="e095e-123">Per creare, vedere la sezione NOTE per le proprietà DIGITALTWINSCREATE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e095e-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e095e-124">-Location</span><span class="sxs-lookup"><span data-stu-id="e095e-124">-Location</span></span>
<span data-ttu-id="e095e-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e095e-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e095e-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e095e-126">-NoWait</span></span>
<span data-ttu-id="e095e-127">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e095e-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e095e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e095e-128">-ResourceGroupName</span></span>
<span data-ttu-id="e095e-129">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e095e-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e095e-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e095e-130">-ResourceName</span></span>
<span data-ttu-id="e095e-131">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e095e-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e095e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e095e-132">-SubscriptionId</span></span>
<span data-ttu-id="e095e-133">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e095e-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="e095e-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="e095e-134">-Tag</span></span>
<span data-ttu-id="e095e-135">I tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e095e-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e095e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e095e-136">-Confirm</span></span>
<span data-ttu-id="e095e-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e095e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e095e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e095e-138">-WhatIf</span></span>
<span data-ttu-id="e095e-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e095e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e095e-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e095e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e095e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e095e-141">CommonParameters</span></span>
<span data-ttu-id="e095e-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e095e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e095e-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e095e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e095e-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="e095e-144">INPUTS</span></span>

### <span data-ttu-id="e095e-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="e095e-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="e095e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e095e-146">OUTPUTS</span></span>

### <span data-ttu-id="e095e-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="e095e-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="e095e-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="e095e-148">NOTES</span></span>

<span data-ttu-id="e095e-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e095e-149">ALIASES</span></span>

<span data-ttu-id="e095e-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e095e-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e095e-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e095e-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e095e-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e095e-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e095e-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="e095e-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="e095e-154">`Location <String>`: posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e095e-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="e095e-155">`[Tag <IDigitalTwinsResourceTags>]`: i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e095e-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="e095e-156">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e095e-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="e095e-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e095e-157">RELATED LINKS</span></span>

