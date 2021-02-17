---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188294"
---
# <span data-ttu-id="b06eb-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b06eb-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="b06eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b06eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b06eb-103">Elimina un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="b06eb-103">Deletes an existing job.</span></span>
<span data-ttu-id="b06eb-104">È possibile eliminare solo i processi negli stati Creazione o Completata.</span><span class="sxs-lookup"><span data-stu-id="b06eb-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="b06eb-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b06eb-105">SYNTAX</span></span>

### <span data-ttu-id="b06eb-106">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b06eb-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b06eb-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b06eb-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b06eb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b06eb-108">DESCRIPTION</span></span>
<span data-ttu-id="b06eb-109">Elimina un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="b06eb-109">Deletes an existing job.</span></span>
<span data-ttu-id="b06eb-110">È possibile eliminare solo i processi negli stati Creazione o Completata.</span><span class="sxs-lookup"><span data-stu-id="b06eb-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="b06eb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b06eb-111">EXAMPLES</span></span>

### <span data-ttu-id="b06eb-112">Esempio 1: Rimuovere il processo ImportExport in base a resourceGroup e al nome del server</span><span class="sxs-lookup"><span data-stu-id="b06eb-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="b06eb-113">Questo cmdlet rimuove il processo ImportExport in base a resourceGroup e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="b06eb-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="b06eb-114">Esempio 2: Rimuovere il processo ImportExport in base all'identità</span><span class="sxs-lookup"><span data-stu-id="b06eb-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="b06eb-115">Questo cmdlet rimuove il processo ImportExport in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="b06eb-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="b06eb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b06eb-116">PARAMETERS</span></span>

### <span data-ttu-id="b06eb-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="b06eb-117">-AcceptLanguage</span></span>
<span data-ttu-id="b06eb-118">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="b06eb-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="b06eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06eb-119">-DefaultProfile</span></span>
<span data-ttu-id="b06eb-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b06eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b06eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b06eb-121">-InputObject</span></span>
<span data-ttu-id="b06eb-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b06eb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b06eb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b06eb-123">-Name</span></span>
<span data-ttu-id="b06eb-124">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="b06eb-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="b06eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b06eb-125">-PassThru</span></span>
<span data-ttu-id="b06eb-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b06eb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b06eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b06eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="b06eb-128">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b06eb-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="b06eb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b06eb-129">-SubscriptionId</span></span>
<span data-ttu-id="b06eb-130">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="b06eb-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="b06eb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b06eb-131">-Confirm</span></span>
<span data-ttu-id="b06eb-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b06eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b06eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b06eb-133">-WhatIf</span></span>
<span data-ttu-id="b06eb-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b06eb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b06eb-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b06eb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b06eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06eb-136">CommonParameters</span></span>
<span data-ttu-id="b06eb-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b06eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06eb-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b06eb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06eb-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b06eb-139">INPUTS</span></span>

### <span data-ttu-id="b06eb-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="b06eb-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="b06eb-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b06eb-141">OUTPUTS</span></span>

### <span data-ttu-id="b06eb-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b06eb-142">System.Boolean</span></span>

## <span data-ttu-id="b06eb-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b06eb-143">NOTES</span></span>

<span data-ttu-id="b06eb-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b06eb-144">ALIASES</span></span>

<span data-ttu-id="b06eb-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b06eb-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b06eb-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b06eb-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b06eb-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b06eb-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b06eb-148">INPUTOBJECT <IImportExportIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b06eb-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b06eb-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b06eb-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b06eb-150">`[JobName <String>]`: nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="b06eb-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="b06eb-151">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b06eb-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="b06eb-152">Ad esempio, Stati Uniti occidentali o Ovest.</span><span class="sxs-lookup"><span data-stu-id="b06eb-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="b06eb-153">`[ResourceGroupName <String>]`: il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b06eb-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="b06eb-154">`[SubscriptionId <String>]`: ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="b06eb-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="b06eb-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b06eb-155">RELATED LINKS</span></span>

