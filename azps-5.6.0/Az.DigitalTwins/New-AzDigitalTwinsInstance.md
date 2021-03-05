---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: 54fdbcfe83dd93101030d92f9f3eec19d1a2564f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984939"
---
# <span data-ttu-id="be0ac-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="be0ac-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="be0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="be0ac-103">Creare o aggiornare i metadati di una DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="be0ac-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="be0ac-104">Il modello più comune per modificare una proprietà è recuperare DigitalTwinsInstance e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="be0ac-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="be0ac-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be0ac-105">SYNTAX</span></span>

### <span data-ttu-id="be0ac-106">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be0ac-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be0ac-107">Crea</span><span class="sxs-lookup"><span data-stu-id="be0ac-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be0ac-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be0ac-108">DESCRIPTION</span></span>
<span data-ttu-id="be0ac-109">Creare o aggiornare i metadati di una DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="be0ac-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="be0ac-110">Il modello più comune per modificare una proprietà è recuperare DigitalTwinsInstance e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="be0ac-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="be0ac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be0ac-111">EXAMPLES</span></span>

### <span data-ttu-id="be0ac-112">Esempio 1: Creare una AzDigitalTwinsInstance per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="be0ac-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="be0ac-113">Creare una AzDigitalTwinsInstance per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="be0ac-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="be0ac-114">Esempio 2: Creare un oggetto AzDigitalTwinsInstance da AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="be0ac-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="be0ac-115">Creare un oggetto AzDigitalTwinsInstance da AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="be0ac-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="be0ac-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be0ac-116">PARAMETERS</span></span>

### <span data-ttu-id="be0ac-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be0ac-117">-AsJob</span></span>
<span data-ttu-id="be0ac-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="be0ac-118">Run the command as a job</span></span>

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

### <span data-ttu-id="be0ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0ac-119">-DefaultProfile</span></span>
<span data-ttu-id="be0ac-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be0ac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be0ac-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="be0ac-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="be0ac-122">Descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="be0ac-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="be0ac-123">Per creare, vedere la sezione NOTE per le proprietà DIGITALTWINSCREATE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="be0ac-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="be0ac-124">-Location</span><span class="sxs-lookup"><span data-stu-id="be0ac-124">-Location</span></span>
<span data-ttu-id="be0ac-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be0ac-125">The resource location.</span></span>

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

### <span data-ttu-id="be0ac-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be0ac-126">-NoWait</span></span>
<span data-ttu-id="be0ac-127">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="be0ac-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be0ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be0ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="be0ac-129">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="be0ac-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="be0ac-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="be0ac-130">-ResourceName</span></span>
<span data-ttu-id="be0ac-131">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="be0ac-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="be0ac-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be0ac-132">-SubscriptionId</span></span>
<span data-ttu-id="be0ac-133">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="be0ac-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="be0ac-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="be0ac-134">-Tag</span></span>
<span data-ttu-id="be0ac-135">I tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="be0ac-135">The resource tags.</span></span>

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

### <span data-ttu-id="be0ac-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be0ac-136">-Confirm</span></span>
<span data-ttu-id="be0ac-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be0ac-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be0ac-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be0ac-138">-WhatIf</span></span>
<span data-ttu-id="be0ac-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be0ac-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be0ac-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be0ac-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be0ac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0ac-141">CommonParameters</span></span>
<span data-ttu-id="be0ac-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be0ac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0ac-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be0ac-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0ac-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="be0ac-144">INPUTS</span></span>

### <span data-ttu-id="be0ac-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="be0ac-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="be0ac-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be0ac-146">OUTPUTS</span></span>

### <span data-ttu-id="be0ac-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="be0ac-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="be0ac-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="be0ac-148">NOTES</span></span>

<span data-ttu-id="be0ac-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="be0ac-149">ALIASES</span></span>

<span data-ttu-id="be0ac-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="be0ac-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be0ac-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="be0ac-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be0ac-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be0ac-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be0ac-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="be0ac-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="be0ac-154">`Location <String>`: posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be0ac-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="be0ac-155">`[Tag <IDigitalTwinsResourceTags>]`: i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="be0ac-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="be0ac-156">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="be0ac-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="be0ac-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be0ac-157">RELATED LINKS</span></span>

