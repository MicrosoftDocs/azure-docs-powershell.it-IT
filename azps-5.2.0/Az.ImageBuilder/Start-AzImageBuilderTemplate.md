---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339040"
---
# <span data-ttu-id="bb63f-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="bb63f-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="bb63f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb63f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb63f-103">Creare elementi da un modello di immagine esistente</span><span class="sxs-lookup"><span data-stu-id="bb63f-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="bb63f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb63f-104">SYNTAX</span></span>

### <span data-ttu-id="bb63f-105">Esegui (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb63f-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bb63f-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb63f-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb63f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb63f-107">DESCRIPTION</span></span>
<span data-ttu-id="bb63f-108">Creare elementi da un modello di immagine esistente</span><span class="sxs-lookup"><span data-stu-id="bb63f-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="bb63f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb63f-109">EXAMPLES</span></span>

### <span data-ttu-id="bb63f-110">Esempio 1: avviare un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="bb63f-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="bb63f-111">Questo comando avvia un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="bb63f-111">This command starts an image template.</span></span>

### <span data-ttu-id="bb63f-112">Esempio 2: avviare un modello di immagine</span><span class="sxs-lookup"><span data-stu-id="bb63f-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="bb63f-113">Questo comando avvia un modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="bb63f-113">This command starts an image template.</span></span>

## <span data-ttu-id="bb63f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb63f-114">PARAMETERS</span></span>

### <span data-ttu-id="bb63f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb63f-115">-AsJob</span></span>
<span data-ttu-id="bb63f-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="bb63f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bb63f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb63f-117">-DefaultProfile</span></span>
<span data-ttu-id="bb63f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb63f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb63f-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="bb63f-119">-ImageTemplateName</span></span>
<span data-ttu-id="bb63f-120">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="bb63f-120">The name of the image Template</span></span>

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

### <span data-ttu-id="bb63f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb63f-121">-InputObject</span></span>
<span data-ttu-id="bb63f-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bb63f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb63f-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="bb63f-123">-NoWait</span></span>
<span data-ttu-id="bb63f-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="bb63f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bb63f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb63f-125">-PassThru</span></span>
<span data-ttu-id="bb63f-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="bb63f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bb63f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb63f-127">-ResourceGroupName</span></span>
<span data-ttu-id="bb63f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb63f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb63f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb63f-129">-SubscriptionId</span></span>
<span data-ttu-id="bb63f-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bb63f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bb63f-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="bb63f-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bb63f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb63f-132">-Confirm</span></span>
<span data-ttu-id="bb63f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb63f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb63f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb63f-134">-WhatIf</span></span>
<span data-ttu-id="bb63f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb63f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb63f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb63f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb63f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb63f-137">CommonParameters</span></span>
<span data-ttu-id="bb63f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb63f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb63f-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb63f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb63f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb63f-140">INPUTS</span></span>

### <span data-ttu-id="bb63f-141">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="bb63f-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="bb63f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb63f-142">OUTPUTS</span></span>

### <span data-ttu-id="bb63f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb63f-143">System.Boolean</span></span>

## <span data-ttu-id="bb63f-144">Note</span><span class="sxs-lookup"><span data-stu-id="bb63f-144">NOTES</span></span>

<span data-ttu-id="bb63f-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bb63f-145">ALIASES</span></span>

<span data-ttu-id="bb63f-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb63f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb63f-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bb63f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb63f-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb63f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb63f-149">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bb63f-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb63f-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="bb63f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb63f-151">`[ImageTemplateName <String>]`: Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="bb63f-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="bb63f-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb63f-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bb63f-153">`[RunOutputName <String>]`: Nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="bb63f-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="bb63f-154">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bb63f-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bb63f-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="bb63f-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bb63f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb63f-156">RELATED LINKS</span></span>

