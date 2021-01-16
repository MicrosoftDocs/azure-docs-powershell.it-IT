---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339031"
---
# <span data-ttu-id="01611-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="01611-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="01611-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01611-102">SYNOPSIS</span></span>
<span data-ttu-id="01611-103">Annullare la build delle immagini a lunga durata in base al modello di immagine</span><span class="sxs-lookup"><span data-stu-id="01611-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="01611-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01611-104">SYNTAX</span></span>

### <span data-ttu-id="01611-105">Annulla (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01611-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01611-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01611-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01611-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01611-107">DESCRIPTION</span></span>
<span data-ttu-id="01611-108">Annullare la build delle immagini a lunga durata in base al modello di immagine</span><span class="sxs-lookup"><span data-stu-id="01611-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="01611-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01611-109">EXAMPLES</span></span>

### <span data-ttu-id="01611-110">Esempio 1: interrompere la creazione di modelli di immagine</span><span class="sxs-lookup"><span data-stu-id="01611-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="01611-111">Questo comando interrompe la creazione di modelli di immagine.</span><span class="sxs-lookup"><span data-stu-id="01611-111">This command stops image template creation.</span></span>

### <span data-ttu-id="01611-112">Esempio 2: interrompere la creazione di modelli di immagine</span><span class="sxs-lookup"><span data-stu-id="01611-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="01611-113">Questo comando interrompe la creazione di modelli di immagine.</span><span class="sxs-lookup"><span data-stu-id="01611-113">This command stops image template creation.</span></span>

## <span data-ttu-id="01611-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01611-114">PARAMETERS</span></span>

### <span data-ttu-id="01611-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01611-115">-AsJob</span></span>
<span data-ttu-id="01611-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="01611-116">Run the command as a job</span></span>

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

### <span data-ttu-id="01611-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01611-117">-DefaultProfile</span></span>
<span data-ttu-id="01611-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01611-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01611-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="01611-119">-ImageTemplateName</span></span>
<span data-ttu-id="01611-120">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="01611-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01611-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01611-121">-InputObject</span></span>
<span data-ttu-id="01611-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="01611-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01611-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="01611-123">-NoWait</span></span>
<span data-ttu-id="01611-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="01611-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01611-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01611-125">-PassThru</span></span>
<span data-ttu-id="01611-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="01611-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="01611-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01611-127">-ResourceGroupName</span></span>
<span data-ttu-id="01611-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01611-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01611-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01611-129">-SubscriptionId</span></span>
<span data-ttu-id="01611-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="01611-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="01611-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="01611-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01611-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01611-132">-Confirm</span></span>
<span data-ttu-id="01611-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01611-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01611-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01611-134">-WhatIf</span></span>
<span data-ttu-id="01611-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01611-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01611-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01611-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01611-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01611-137">CommonParameters</span></span>
<span data-ttu-id="01611-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01611-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01611-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01611-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01611-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01611-140">INPUTS</span></span>

### <span data-ttu-id="01611-141">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="01611-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="01611-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01611-142">OUTPUTS</span></span>

### <span data-ttu-id="01611-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01611-143">System.Boolean</span></span>

## <span data-ttu-id="01611-144">Note</span><span class="sxs-lookup"><span data-stu-id="01611-144">NOTES</span></span>

<span data-ttu-id="01611-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="01611-145">ALIASES</span></span>

<span data-ttu-id="01611-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01611-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01611-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="01611-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01611-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01611-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01611-149">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="01611-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01611-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="01611-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01611-151">`[ImageTemplateName <String>]`: Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="01611-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="01611-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01611-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="01611-153">`[RunOutputName <String>]`: Nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="01611-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="01611-154">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="01611-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="01611-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="01611-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="01611-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01611-156">RELATED LINKS</span></span>

