---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487304"
---
# <span data-ttu-id="1b144-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="1b144-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="1b144-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b144-102">SYNOPSIS</span></span>
<span data-ttu-id="1b144-103">Elimina un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="1b144-103">Deletes an existing job.</span></span>
<span data-ttu-id="1b144-104">Solo i processi nello stato di creazione o completamento possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="1b144-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="1b144-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b144-105">SYNTAX</span></span>

### <span data-ttu-id="1b144-106">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b144-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1b144-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1b144-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b144-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b144-108">DESCRIPTION</span></span>
<span data-ttu-id="1b144-109">Elimina un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="1b144-109">Deletes an existing job.</span></span>
<span data-ttu-id="1b144-110">Solo i processi nello stato di creazione o completamento possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="1b144-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="1b144-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b144-111">EXAMPLES</span></span>

### <span data-ttu-id="1b144-112">Esempio 1: rimuovere il processo di ImportExport per resourceGroup e il nome del server</span><span class="sxs-lookup"><span data-stu-id="1b144-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="1b144-113">Questo cmdlet rimuove il processo ImportExport in base a resourceGroup e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="1b144-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="1b144-114">Esempio 2: rimuovere il processo di ImportExport per identità</span><span class="sxs-lookup"><span data-stu-id="1b144-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="1b144-115">Questi cmdlet rimuovono ImportExport processo per identità.</span><span class="sxs-lookup"><span data-stu-id="1b144-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="1b144-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b144-116">PARAMETERS</span></span>

### <span data-ttu-id="1b144-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="1b144-117">-AcceptLanguage</span></span>
<span data-ttu-id="1b144-118">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="1b144-118">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b144-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b144-119">-DefaultProfile</span></span>
<span data-ttu-id="1b144-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b144-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b144-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b144-121">-InputObject</span></span>
<span data-ttu-id="1b144-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1b144-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b144-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b144-123">-Name</span></span>
<span data-ttu-id="1b144-124">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="1b144-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b144-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b144-125">-PassThru</span></span>
<span data-ttu-id="1b144-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="1b144-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1b144-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b144-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b144-128">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="1b144-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="1b144-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b144-129">-SubscriptionId</span></span>
<span data-ttu-id="1b144-130">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b144-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="1b144-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b144-131">-Confirm</span></span>
<span data-ttu-id="1b144-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b144-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b144-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b144-133">-WhatIf</span></span>
<span data-ttu-id="1b144-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b144-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b144-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b144-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b144-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b144-136">CommonParameters</span></span>
<span data-ttu-id="1b144-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b144-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b144-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b144-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b144-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b144-139">INPUTS</span></span>

### <span data-ttu-id="1b144-140">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="1b144-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="1b144-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b144-141">OUTPUTS</span></span>

### <span data-ttu-id="1b144-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b144-142">System.Boolean</span></span>

## <span data-ttu-id="1b144-143">Note</span><span class="sxs-lookup"><span data-stu-id="1b144-143">NOTES</span></span>

<span data-ttu-id="1b144-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1b144-144">ALIASES</span></span>

<span data-ttu-id="1b144-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b144-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1b144-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1b144-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b144-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1b144-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1b144-148">INPUTOBJECT <IImportExportIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1b144-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b144-149">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1b144-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b144-150">`[JobName <String>]`: Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="1b144-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="1b144-151">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="1b144-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="1b144-152">Ad esempio, ovest degli Stati Uniti o westus.</span><span class="sxs-lookup"><span data-stu-id="1b144-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="1b144-153">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="1b144-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="1b144-154">`[SubscriptionId <String>]`: ID abbonamento per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b144-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="1b144-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b144-155">RELATED LINKS</span></span>

