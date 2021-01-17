---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386816"
---
# <span data-ttu-id="ab09e-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="ab09e-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="ab09e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab09e-102">SYNOPSIS</span></span>
<span data-ttu-id="ab09e-103">Ottenere l'output di esecuzione specificato per la risorsa del modello di immagine specificata</span><span class="sxs-lookup"><span data-stu-id="ab09e-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="ab09e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab09e-104">SYNTAX</span></span>

### <span data-ttu-id="ab09e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab09e-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab09e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ab09e-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab09e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ab09e-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab09e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab09e-108">DESCRIPTION</span></span>
<span data-ttu-id="ab09e-109">Ottenere l'output di esecuzione specificato per la risorsa del modello di immagine specificata</span><span class="sxs-lookup"><span data-stu-id="ab09e-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="ab09e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab09e-110">EXAMPLES</span></span>

### <span data-ttu-id="ab09e-111">Esempio 1: elenca tutti i risultati dell'esecuzione in un modello</span><span class="sxs-lookup"><span data-stu-id="ab09e-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="ab09e-112">Questo comando elenca tutti i risultati dell'esecuzione in un modello.</span><span class="sxs-lookup"><span data-stu-id="ab09e-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="ab09e-113">Esempio 2: ottenere un risultato di esecuzione in un modello</span><span class="sxs-lookup"><span data-stu-id="ab09e-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="ab09e-114">Questo comando ottiene un risultato di esecuzione in un modello.</span><span class="sxs-lookup"><span data-stu-id="ab09e-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="ab09e-115">Esempio 3: ottenere un risultato di esecuzione in un modello</span><span class="sxs-lookup"><span data-stu-id="ab09e-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="ab09e-116">Questo comando ottiene un risultato di esecuzione in un modello.</span><span class="sxs-lookup"><span data-stu-id="ab09e-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="ab09e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab09e-117">PARAMETERS</span></span>

### <span data-ttu-id="ab09e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab09e-118">-DefaultProfile</span></span>
<span data-ttu-id="ab09e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab09e-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="ab09e-120">-ImageTemplateName</span></span>
<span data-ttu-id="ab09e-121">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="ab09e-121">The name of the image Template</span></span>

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

### <span data-ttu-id="ab09e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab09e-122">-InputObject</span></span>
<span data-ttu-id="ab09e-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ab09e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab09e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab09e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab09e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab09e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab09e-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="ab09e-126">-RunOutputName</span></span>
<span data-ttu-id="ab09e-127">Nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="ab09e-127">The name of the run output</span></span>

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

### <span data-ttu-id="ab09e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab09e-128">-SubscriptionId</span></span>
<span data-ttu-id="ab09e-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ab09e-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ab09e-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ab09e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab09e-131">CommonParameters</span></span>
<span data-ttu-id="ab09e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab09e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab09e-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab09e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab09e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab09e-134">INPUTS</span></span>

### <span data-ttu-id="ab09e-135">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="ab09e-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="ab09e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab09e-136">OUTPUTS</span></span>

### <span data-ttu-id="ab09e-137">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IRunOutput</span><span class="sxs-lookup"><span data-stu-id="ab09e-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="ab09e-138">Note</span><span class="sxs-lookup"><span data-stu-id="ab09e-138">NOTES</span></span>

<span data-ttu-id="ab09e-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ab09e-139">ALIASES</span></span>

<span data-ttu-id="ab09e-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab09e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab09e-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ab09e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab09e-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab09e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab09e-143">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ab09e-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab09e-144">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ab09e-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab09e-145">`[ImageTemplateName <String>]`: Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="ab09e-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="ab09e-146">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab09e-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ab09e-147">`[RunOutputName <String>]`: Nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="ab09e-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="ab09e-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ab09e-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ab09e-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ab09e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab09e-150">RELATED LINKS</span></span>

