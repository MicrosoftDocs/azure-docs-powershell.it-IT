---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475300"
---
# <span data-ttu-id="0c760-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="0c760-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="0c760-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c760-102">SYNOPSIS</span></span>
<span data-ttu-id="0c760-103">Creare o aggiornare i metadati di un DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0c760-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="0c760-104">Il modello usuale per modificare una proprietà consiste nel recuperare i metadati di DigitalTwinsInstance e di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0c760-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="0c760-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c760-105">SYNTAX</span></span>

### <span data-ttu-id="0c760-106">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c760-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0c760-107">Creare</span><span class="sxs-lookup"><span data-stu-id="0c760-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c760-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c760-108">DESCRIPTION</span></span>
<span data-ttu-id="0c760-109">Creare o aggiornare i metadati di un DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0c760-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="0c760-110">Il modello usuale per modificare una proprietà consiste nel recuperare i metadati di DigitalTwinsInstance e di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0c760-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="0c760-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c760-111">EXAMPLES</span></span>

### <span data-ttu-id="0c760-112">Esempio 1: creare un AzDigitalTwinsInstance per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0c760-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="0c760-113">Creare un AzDigitalTwinsInstance per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="0c760-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="0c760-114">Esempio 2: creare un oggetto AzDigitalTwinsInstance per AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="0c760-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="0c760-115">Creare un oggetto AzDigitalTwinsInstance per AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="0c760-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="0c760-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c760-116">PARAMETERS</span></span>

### <span data-ttu-id="0c760-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c760-117">-AsJob</span></span>
<span data-ttu-id="0c760-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="0c760-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0c760-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c760-119">-DefaultProfile</span></span>
<span data-ttu-id="0c760-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c760-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c760-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="0c760-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="0c760-122">Descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="0c760-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="0c760-123">Per costruire, vedere la sezione Note per le proprietà di DIGITALTWINSCREATE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0c760-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="0c760-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0c760-124">-Location</span></span>
<span data-ttu-id="0c760-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c760-125">The resource location.</span></span>

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

### <span data-ttu-id="0c760-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="0c760-126">-NoWait</span></span>
<span data-ttu-id="0c760-127">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="0c760-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0c760-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c760-128">-ResourceGroupName</span></span>
<span data-ttu-id="0c760-129">Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0c760-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="0c760-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0c760-130">-ResourceName</span></span>
<span data-ttu-id="0c760-131">Il nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0c760-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="0c760-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c760-132">-SubscriptionId</span></span>
<span data-ttu-id="0c760-133">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0c760-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="0c760-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c760-134">-Tag</span></span>
<span data-ttu-id="0c760-135">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0c760-135">The resource tags.</span></span>

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

### <span data-ttu-id="0c760-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c760-136">-Confirm</span></span>
<span data-ttu-id="0c760-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c760-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c760-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c760-138">-WhatIf</span></span>
<span data-ttu-id="0c760-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c760-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c760-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c760-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c760-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c760-141">CommonParameters</span></span>
<span data-ttu-id="0c760-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c760-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c760-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c760-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c760-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c760-144">INPUTS</span></span>

### <span data-ttu-id="0c760-145">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="0c760-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="0c760-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c760-146">OUTPUTS</span></span>

### <span data-ttu-id="0c760-147">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="0c760-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="0c760-148">Note</span><span class="sxs-lookup"><span data-stu-id="0c760-148">NOTES</span></span>

<span data-ttu-id="0c760-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0c760-149">ALIASES</span></span>

<span data-ttu-id="0c760-150">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c760-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0c760-151">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0c760-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0c760-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0c760-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0c760-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : la descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="0c760-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="0c760-154">`Location <String>`: La posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c760-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="0c760-155">`[Tag <IDigitalTwinsResourceTags>]`: I tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0c760-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="0c760-156">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c760-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="0c760-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c760-157">RELATED LINKS</span></span>

