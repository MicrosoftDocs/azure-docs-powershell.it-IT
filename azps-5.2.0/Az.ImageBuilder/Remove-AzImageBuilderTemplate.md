---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339064"
---
# <span data-ttu-id="3c608-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="3c608-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="3c608-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c608-102">SYNOPSIS</span></span>
<span data-ttu-id="3c608-103">Eliminare un modello di immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3c608-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="3c608-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c608-104">SYNTAX</span></span>

### <span data-ttu-id="3c608-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c608-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3c608-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c608-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c608-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c608-107">DESCRIPTION</span></span>
<span data-ttu-id="3c608-108">Eliminare un modello di immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3c608-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="3c608-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c608-109">EXAMPLES</span></span>

### <span data-ttu-id="3c608-110">Esempio 1: rimuovere un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="3c608-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="3c608-111">Questo comando rimuove un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="3c608-111">This command removes a image template.</span></span>

### <span data-ttu-id="3c608-112">Esempio 2: rimuovere un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="3c608-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="3c608-113">Questo comando rimuove un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="3c608-113">This command removes a image template.</span></span>

## <span data-ttu-id="3c608-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c608-114">PARAMETERS</span></span>

### <span data-ttu-id="3c608-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c608-115">-AsJob</span></span>
<span data-ttu-id="3c608-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3c608-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3c608-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c608-117">-DefaultProfile</span></span>
<span data-ttu-id="3c608-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c608-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c608-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="3c608-119">-ImageTemplateName</span></span>
<span data-ttu-id="3c608-120">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="3c608-120">The name of the image Template</span></span>

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

### <span data-ttu-id="3c608-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c608-121">-InputObject</span></span>
<span data-ttu-id="3c608-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3c608-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c608-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="3c608-123">-NoWait</span></span>
<span data-ttu-id="3c608-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3c608-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c608-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c608-125">-PassThru</span></span>
<span data-ttu-id="3c608-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="3c608-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c608-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c608-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c608-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c608-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c608-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c608-129">-SubscriptionId</span></span>
<span data-ttu-id="3c608-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c608-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c608-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3c608-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c608-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c608-132">-Confirm</span></span>
<span data-ttu-id="3c608-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c608-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c608-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c608-134">-WhatIf</span></span>
<span data-ttu-id="3c608-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c608-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c608-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c608-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c608-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c608-137">CommonParameters</span></span>
<span data-ttu-id="3c608-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c608-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c608-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c608-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c608-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c608-140">INPUTS</span></span>

### <span data-ttu-id="3c608-141">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="3c608-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="3c608-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c608-142">OUTPUTS</span></span>

### <span data-ttu-id="3c608-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c608-143">System.Boolean</span></span>

## <span data-ttu-id="3c608-144">Note</span><span class="sxs-lookup"><span data-stu-id="3c608-144">NOTES</span></span>

<span data-ttu-id="3c608-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3c608-145">ALIASES</span></span>

<span data-ttu-id="3c608-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c608-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c608-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3c608-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c608-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c608-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c608-149">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3c608-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c608-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="3c608-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c608-151">`[ImageTemplateName <String>]`: Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="3c608-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="3c608-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c608-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3c608-153">`[RunOutputName <String>]`: Nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="3c608-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="3c608-154">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c608-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c608-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3c608-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3c608-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c608-156">RELATED LINKS</span></span>

