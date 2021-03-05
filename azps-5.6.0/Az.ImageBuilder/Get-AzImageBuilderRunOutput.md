---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4f1c88e48847c1ecf560d7ed9d390131455b1d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013085"
---
# <span data-ttu-id="f3776-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="f3776-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="f3776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3776-102">SYNOPSIS</span></span>
<span data-ttu-id="f3776-103">Ottenere l'output di esecuzione specificato per la risorsa modello di immagine specificata</span><span class="sxs-lookup"><span data-stu-id="f3776-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="f3776-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3776-104">SYNTAX</span></span>

### <span data-ttu-id="f3776-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3776-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f3776-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f3776-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f3776-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3776-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3776-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3776-108">DESCRIPTION</span></span>
<span data-ttu-id="f3776-109">Ottenere l'output di esecuzione specificato per la risorsa modello di immagine specificata</span><span class="sxs-lookup"><span data-stu-id="f3776-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="f3776-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3776-110">EXAMPLES</span></span>

### <span data-ttu-id="f3776-111">Esempio 1: Elencare tutti i risultati eseguiti in un modello</span><span class="sxs-lookup"><span data-stu-id="f3776-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="f3776-112">Questo comando elenca tutti i risultati eseguiti in un modello.</span><span class="sxs-lookup"><span data-stu-id="f3776-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="f3776-113">Esempio 2: Ottenere un risultato di esecuzione in un modello</span><span class="sxs-lookup"><span data-stu-id="f3776-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="f3776-114">Questo comando ottiene un risultato di esecuzione in un modello.</span><span class="sxs-lookup"><span data-stu-id="f3776-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="f3776-115">Esempio 3: Ottenere un risultato di esecuzione in un modello</span><span class="sxs-lookup"><span data-stu-id="f3776-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="f3776-116">Questo comando ottiene un risultato di esecuzione in un modello.</span><span class="sxs-lookup"><span data-stu-id="f3776-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="f3776-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3776-117">PARAMETERS</span></span>

### <span data-ttu-id="f3776-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3776-118">-DefaultProfile</span></span>
<span data-ttu-id="f3776-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3776-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3776-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="f3776-120">-ImageTemplateName</span></span>
<span data-ttu-id="f3776-121">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="f3776-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3776-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3776-122">-InputObject</span></span>
<span data-ttu-id="f3776-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f3776-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3776-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3776-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3776-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3776-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3776-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="f3776-126">-RunOutputName</span></span>
<span data-ttu-id="f3776-127">Nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="f3776-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3776-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3776-128">-SubscriptionId</span></span>
<span data-ttu-id="f3776-129">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f3776-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f3776-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f3776-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3776-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3776-131">CommonParameters</span></span>
<span data-ttu-id="f3776-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3776-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3776-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3776-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3776-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3776-134">INPUTS</span></span>

### <span data-ttu-id="f3776-135">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.IImageMagIdentity</span><span class="sxs-lookup"><span data-stu-id="f3776-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="f3776-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3776-136">OUTPUTS</span></span>

### <span data-ttu-id="f3776-137">Microsoft.Azure.PowerShell.Cmdlets.ImageWl.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="f3776-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="f3776-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3776-138">NOTES</span></span>

<span data-ttu-id="f3776-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f3776-139">ALIASES</span></span>

<span data-ttu-id="f3776-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f3776-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3776-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f3776-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3776-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3776-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3776-143">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f3776-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3776-144">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f3776-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3776-145">`[ImageTemplateName <String>]`: nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="f3776-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="f3776-146">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3776-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f3776-147">`[RunOutputName <String>]`: nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="f3776-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="f3776-148">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f3776-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f3776-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f3776-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f3776-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3776-150">RELATED LINKS</span></span>

