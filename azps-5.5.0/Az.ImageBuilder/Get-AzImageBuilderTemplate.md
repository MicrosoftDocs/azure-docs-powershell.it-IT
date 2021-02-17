---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192446"
---
# <span data-ttu-id="a6746-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="a6746-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="a6746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6746-102">SYNOPSIS</span></span>
<span data-ttu-id="a6746-103">Ottenere informazioni su un modello di immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a6746-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="a6746-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6746-104">SYNTAX</span></span>

### <span data-ttu-id="a6746-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6746-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a6746-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a6746-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a6746-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6746-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6746-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="a6746-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a6746-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6746-109">DESCRIPTION</span></span>
<span data-ttu-id="a6746-110">Ottenere informazioni su un modello di immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a6746-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="a6746-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6746-111">EXAMPLES</span></span>

### <span data-ttu-id="a6746-112">Esempio 1: Elencare tutto il modello in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a6746-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="a6746-113">Questo comando elenca tutti i modelli di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a6746-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="a6746-114">Esempio 2: Elencare tutto il modello in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a6746-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="a6746-115">Questo comando elenca tutti i modelli in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6746-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="a6746-116">Esempio 3: Ottenere un modello in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a6746-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="a6746-117">Questo comando recupera un modello in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6746-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="a6746-118">Esempio 4: Ottenere un modello in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a6746-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="a6746-119">Questo comando recupera un modello in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6746-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="a6746-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6746-120">PARAMETERS</span></span>

### <span data-ttu-id="a6746-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6746-121">-DefaultProfile</span></span>
<span data-ttu-id="a6746-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6746-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6746-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="a6746-123">-ImageTemplateName</span></span>
<span data-ttu-id="a6746-124">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="a6746-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6746-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6746-125">-InputObject</span></span>
<span data-ttu-id="a6746-126">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a6746-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6746-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6746-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6746-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6746-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6746-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6746-129">-SubscriptionId</span></span>
<span data-ttu-id="a6746-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a6746-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6746-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a6746-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6746-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6746-132">CommonParameters</span></span>
<span data-ttu-id="a6746-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6746-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6746-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6746-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6746-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6746-135">INPUTS</span></span>

### <span data-ttu-id="a6746-136">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.IImageMagIdentity</span><span class="sxs-lookup"><span data-stu-id="a6746-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="a6746-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6746-137">OUTPUTS</span></span>

### <span data-ttu-id="a6746-138">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="a6746-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="a6746-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6746-139">NOTES</span></span>

<span data-ttu-id="a6746-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6746-140">ALIASES</span></span>

<span data-ttu-id="a6746-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a6746-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6746-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a6746-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6746-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6746-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6746-144">INPUTOBJECT <IImageBuilderIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="a6746-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6746-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a6746-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6746-146">`[ImageTemplateName <String>]`: nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="a6746-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="a6746-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6746-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a6746-148">`[RunOutputName <String>]`: il nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="a6746-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="a6746-149">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a6746-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a6746-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a6746-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a6746-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6746-151">RELATED LINKS</span></span>

