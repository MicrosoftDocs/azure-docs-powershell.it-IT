---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 75065d50b8176b256c5cf91c136f4f4588232e55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964669"
---
# <span data-ttu-id="7263e-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="7263e-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="7263e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7263e-102">SYNOPSIS</span></span>
<span data-ttu-id="7263e-103">Creare elementi da un modello di immagine esistente</span><span class="sxs-lookup"><span data-stu-id="7263e-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="7263e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7263e-104">SYNTAX</span></span>

### <span data-ttu-id="7263e-105">Esegui (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7263e-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7263e-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7263e-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7263e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7263e-107">DESCRIPTION</span></span>
<span data-ttu-id="7263e-108">Creare elementi da un modello di immagine esistente</span><span class="sxs-lookup"><span data-stu-id="7263e-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="7263e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7263e-109">EXAMPLES</span></span>

### <span data-ttu-id="7263e-110">Esempio 1: Creare un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="7263e-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="7263e-111">Questo comando avvia un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="7263e-111">This command starts an image template.</span></span>

### <span data-ttu-id="7263e-112">Esempio 2: Creare un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="7263e-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="7263e-113">Questo comando avvia un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="7263e-113">This command starts an image template.</span></span>

## <span data-ttu-id="7263e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7263e-114">PARAMETERS</span></span>

### <span data-ttu-id="7263e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7263e-115">-AsJob</span></span>
<span data-ttu-id="7263e-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="7263e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7263e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7263e-117">-DefaultProfile</span></span>
<span data-ttu-id="7263e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7263e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7263e-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="7263e-119">-ImageTemplateName</span></span>
<span data-ttu-id="7263e-120">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="7263e-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7263e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7263e-121">-InputObject</span></span>
<span data-ttu-id="7263e-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7263e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7263e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7263e-123">-NoWait</span></span>
<span data-ttu-id="7263e-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="7263e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7263e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7263e-125">-PassThru</span></span>
<span data-ttu-id="7263e-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="7263e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7263e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7263e-127">-ResourceGroupName</span></span>
<span data-ttu-id="7263e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7263e-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7263e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7263e-129">-SubscriptionId</span></span>
<span data-ttu-id="7263e-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7263e-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7263e-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7263e-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7263e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7263e-132">-Confirm</span></span>
<span data-ttu-id="7263e-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7263e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7263e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7263e-134">-WhatIf</span></span>
<span data-ttu-id="7263e-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7263e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7263e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7263e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7263e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7263e-137">CommonParameters</span></span>
<span data-ttu-id="7263e-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7263e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7263e-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7263e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7263e-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="7263e-140">INPUTS</span></span>

### <span data-ttu-id="7263e-141">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.IImageImageImageIdentity</span><span class="sxs-lookup"><span data-stu-id="7263e-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="7263e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7263e-142">OUTPUTS</span></span>

### <span data-ttu-id="7263e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7263e-143">System.Boolean</span></span>

## <span data-ttu-id="7263e-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="7263e-144">NOTES</span></span>

<span data-ttu-id="7263e-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7263e-145">ALIASES</span></span>

<span data-ttu-id="7263e-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="7263e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7263e-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7263e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7263e-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7263e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7263e-149">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7263e-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7263e-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="7263e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7263e-151">`[ImageTemplateName <String>]`: nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="7263e-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="7263e-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7263e-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7263e-153">`[RunOutputName <String>]`: nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="7263e-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="7263e-154">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7263e-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7263e-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7263e-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7263e-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7263e-156">RELATED LINKS</span></span>

