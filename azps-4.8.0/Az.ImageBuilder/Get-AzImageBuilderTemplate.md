---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191331"
---
# <span data-ttu-id="84bb6-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="84bb6-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="84bb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="84bb6-103">Ottenere informazioni su un modello di immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="84bb6-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="84bb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84bb6-104">SYNTAX</span></span>

### <span data-ttu-id="84bb6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84bb6-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="84bb6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="84bb6-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="84bb6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="84bb6-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="84bb6-108">List1</span><span class="sxs-lookup"><span data-stu-id="84bb6-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="84bb6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84bb6-109">DESCRIPTION</span></span>
<span data-ttu-id="84bb6-110">Ottenere informazioni su un modello di immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="84bb6-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="84bb6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84bb6-111">EXAMPLES</span></span>

### <span data-ttu-id="84bb6-112">Esempio 1: elenca tutti i modelli in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="84bb6-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="84bb6-113">Questo comando elenca tutti i modelli in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="84bb6-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="84bb6-114">Esempio 2: elenca tutti i modelli in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="84bb6-114">Example 2: List all template under a resource group</span></span>
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

<span data-ttu-id="84bb6-115">Questo comando elenca tutti i modelli in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84bb6-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="84bb6-116">Esempio 3: ottenere un modello in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="84bb6-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="84bb6-117">Questo comando ottiene un modello in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84bb6-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="84bb6-118">Esempio 4: ottenere un modello in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="84bb6-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="84bb6-119">Questo comando ottiene un modello in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84bb6-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="84bb6-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84bb6-120">PARAMETERS</span></span>

### <span data-ttu-id="84bb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bb6-121">-DefaultProfile</span></span>
<span data-ttu-id="84bb6-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84bb6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84bb6-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="84bb6-123">-ImageTemplateName</span></span>
<span data-ttu-id="84bb6-124">Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="84bb6-124">The name of the image Template</span></span>

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

### <span data-ttu-id="84bb6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84bb6-125">-InputObject</span></span>
<span data-ttu-id="84bb6-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="84bb6-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="84bb6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bb6-127">-ResourceGroupName</span></span>
<span data-ttu-id="84bb6-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84bb6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="84bb6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84bb6-129">-SubscriptionId</span></span>
<span data-ttu-id="84bb6-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84bb6-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84bb6-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="84bb6-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="84bb6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bb6-132">CommonParameters</span></span>
<span data-ttu-id="84bb6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84bb6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bb6-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84bb6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bb6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84bb6-135">INPUTS</span></span>

### <span data-ttu-id="84bb6-136">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="84bb6-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="84bb6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84bb6-137">OUTPUTS</span></span>

### <span data-ttu-id="84bb6-138">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="84bb6-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="84bb6-139">Note</span><span class="sxs-lookup"><span data-stu-id="84bb6-139">NOTES</span></span>

<span data-ttu-id="84bb6-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="84bb6-140">ALIASES</span></span>

<span data-ttu-id="84bb6-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84bb6-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84bb6-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="84bb6-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84bb6-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84bb6-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84bb6-144">INPUTOBJECT <IImageBuilderIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="84bb6-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="84bb6-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="84bb6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84bb6-146">`[ImageTemplateName <String>]`: Nome del modello di immagine</span><span class="sxs-lookup"><span data-stu-id="84bb6-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="84bb6-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84bb6-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="84bb6-148">`[RunOutputName <String>]`: Nome dell'output di esecuzione</span><span class="sxs-lookup"><span data-stu-id="84bb6-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="84bb6-149">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84bb6-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="84bb6-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="84bb6-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="84bb6-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84bb6-151">RELATED LINKS</span></span>

