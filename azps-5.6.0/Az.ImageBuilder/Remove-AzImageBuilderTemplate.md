---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 3d22fa9626d7e0e6de8baf36a07ae679ffb9ed0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013021"
---
# <span data-ttu-id="ddd2e-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="ddd2e-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="ddd2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd2e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd2e-103">Eliminare un modello di immagine di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ddd2e-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="ddd2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddd2e-104">SYNTAX</span></span>

### <span data-ttu-id="ddd2e-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddd2e-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ddd2e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ddd2e-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddd2e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ddd2e-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd2e-108">Eliminare un modello di immagine di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ddd2e-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="ddd2e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddd2e-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd2e-110">Esempio 1: Rimuovere un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="ddd2e-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="ddd2e-111">Questo comando rimuove un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-111">This command removes a image template.</span></span>

### <span data-ttu-id="ddd2e-112">Esempio 2: Rimuovere un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="ddd2e-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="ddd2e-113">Questo comando rimuove un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-113">This command removes a image template.</span></span>

## <span data-ttu-id="ddd2e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddd2e-114">PARAMETERS</span></span>

### <span data-ttu-id="ddd2e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd2e-115">-AsJob</span></span>
<span data-ttu-id="ddd2e-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ddd2e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ddd2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd2e-117">-DefaultProfile</span></span>
<span data-ttu-id="ddd2e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd2e-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="ddd2e-119">-ImageTemplateName</span></span>
<span data-ttu-id="ddd2e-120">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="ddd2e-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddd2e-121">-InputObject</span></span>
<span data-ttu-id="ddd2e-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ddd2e-123">-NoWait</span></span>
<span data-ttu-id="ddd2e-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ddd2e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ddd2e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddd2e-125">-PassThru</span></span>
<span data-ttu-id="ddd2e-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="ddd2e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ddd2e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd2e-127">-ResourceGroupName</span></span>
<span data-ttu-id="ddd2e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddd2e-129">-SubscriptionId</span></span>
<span data-ttu-id="ddd2e-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ddd2e-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddd2e-132">-Confirm</span></span>
<span data-ttu-id="ddd2e-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd2e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd2e-134">-WhatIf</span></span>
<span data-ttu-id="ddd2e-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd2e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd2e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd2e-137">CommonParameters</span></span>
<span data-ttu-id="ddd2e-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd2e-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd2e-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="ddd2e-140">INPUTS</span></span>

### <span data-ttu-id="ddd2e-141">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.IImageImageImageIdentity</span><span class="sxs-lookup"><span data-stu-id="ddd2e-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="ddd2e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddd2e-142">OUTPUTS</span></span>

### <span data-ttu-id="ddd2e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddd2e-143">System.Boolean</span></span>

## <span data-ttu-id="ddd2e-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="ddd2e-144">NOTES</span></span>

<span data-ttu-id="ddd2e-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ddd2e-145">ALIASES</span></span>

<span data-ttu-id="ddd2e-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ddd2e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ddd2e-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ddd2e-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ddd2e-149">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ddd2e-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ddd2e-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="ddd2e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ddd2e-151">`[ImageTemplateName <String>]`: nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="ddd2e-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="ddd2e-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ddd2e-153">`[RunOutputName <String>]`: nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="ddd2e-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="ddd2e-154">`[SubscriptionId <String>]`: le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ddd2e-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ddd2e-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddd2e-156">RELATED LINKS</span></span>

